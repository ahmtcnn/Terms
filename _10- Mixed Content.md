**Mixed Content**

Web uygulamamıza SSL/TLS sertifikası dahil ederek HTTPS protokolünü kullanırız. Dolayısıyla
web sunucumucla client arasındaki iletişim şifreli, güvenli olarak iletilir.
Ancak HTTP den HTTPS e geçtiğimizde bazı sorunlar yaşayabiliyoruz. Mixed Content de bunlardan biri

Sitemiz HTTPS kullanırken site içeriğinde dış kaynaktan çekilen veriler olabilir. Bir resim veya bir js 
dosyası vs. Bu dış kaynak içerikleri, içeri dahil edilirken http kullanılıyorsa, bu istekler browser tarafından
otomatik olarak engellenir. Eğer sitemiz HTTPS kullanıyorsa o kaynaktan çekilen veri de HTTPS ile olmalıdır.

Bunun için tüm linkleri vs. HTTPS e geçirmeli.

Ya da farklı bir çözüm olarak tüm dış kaynaklara bağlantıyı HTTPS üzerinden yapılmasını zorunlu kılan bir header
kullanabiliriz:

**Content-Security-Policy** : **upgrade-insecure-requests;**