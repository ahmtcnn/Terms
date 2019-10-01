**SSL - Secure Sockets Layer - Güvenli Giris Katmani / TLS - Transport Layer Security**

Server ile alici iletisimi esnasinda verilerin sifrelenerek yapilmasi islemi
Bu sifrelemede PKI (Public Key Infrastructure) türü kullanilir.
PKI sifreleme genellikle RSA ve ECC ( Elliptic Curve Cryptography ) kullaniliyor.

Kimlik dogrultmaya ihtiyaç duydugunuzda: Herhangi bir sunucu sizin sunucunuz gibi davranarak,
insanlarin bu esnada transfer ettigi bilgiye erisebilir. SSL/TLS sayesinde sunucunuzun kimligini 
dogrulayabilir ve böylece insanlar sizin söylediginiz kisi oldugunuzu bilebilir.

Güven saglamak: EGer bir eTicaret sitesi sahibiyseniz veya insanlardan onlar için önemli olan bilgilerini 
istiyorsaniz belirli bir seviye güven insa etmelisiniz. Bir SSL sertifikasi kullanarak insanlara görsel bir
sekilde size güvenebileceklerini gösterebilirsiniz. Bu, sizin kendiniz hakkinda söyleyeceginiz herseyden daha 
etkilidir.

Piyasa standartlarina uyum saglamaniz gerekiyorsa: Finans sektörü gibi bazi sektörlerde, belirli seviye
güvenlige sahip olmak gerekmektedir. Ayrica eger websitenizde kredi karti bilgisi kabul etmek istiyorsaniz,
Payment Card Industry (PCI) standartlarini uygulamaniz gerekiyor. Bu gerekliliklerden biriside SSL/TLS 
sertifikasidir.


**SSL vs TLS**

SSL ve TSL’in her ikisi de özünde birer sifreleme ve yetkilendirme protokolüdür. Bu protokoller yardimiyla sunucudan sunucuya veya sunucudan 
istemciye güvenli sekilde veri transferi gerçeklestirilir. SSL, TSL’in daha ilkel halidir. Bilisim ve internet dünyasinda yillarca geçen 
gelistirmelerin bir sonucu olarak SSL’in daha yeni sürümü olarak kabul edebilecegimi TSL ortaya çikmistir.

SSL ilk olarak Netscape tarafindan 1995 yilinda SSL 2.0 olarak yayinlanmisti. SSL’in ilk sürümü olan SSL 1.0 protokolü hiçbir 
zaman tüm kullanicilara açik olarak kullanima sunulmamisti. Piyasada bir süre kullanilan SSL 2.0 çok geçmeden patlak verdi ve 
ciddi güvenlik açiklarina sahip oldugu ortaya çikti. Kisa süre sonra 1996 yilinda, SSL 2.0’in yerini daha yeni sürümü olan SSL 3.0 aldi.

1999 Yilina gelindiginde ise daha güçlü bir sifreleme katmani olarak TLS kullanima sunuldu. Bir nevi SSL’in yetersiz kalmasi 
TLS 1.0’in dogmasina neden oldu. Aralarinda yapisal anlamda büyük farkliliklar olmamasina karsin TLS’in daha güvenli bir protokol
 oldugunu söyleyebiliriz. Özellikle söz konusu olan mesaj yetkilendirmesi ve anahtar malzeme üretimi oldugunda TLS algoritmasi 
açisindan daha güvenli bir katman olma rolünü üstleniyor. 
