**SSRF - Server Side Request Forgery - Sunucu taraflı istek sahteciliği**

Web sunucusunun uzak kaynakları çağırmasına izin verlien domainler ve protokoller denetlenmediği için bu zafiyet ortaya çıkmıştır.
Anladığım kadarıyla bu zafiyet RFI dan kaynaklanıyor. Yani dış kaynakla bir alışverişin olduğu parametreyi kullanarak bu zafiyet sömürülebilir

Bununla birlikte:

Normal olarak erişilemeyen iç ağlarda keşif ve saldırı,
Siteler arası betik çalıştırma, (SSRF to Reflected XSS)
Uzaktan kod çalıştırma, (SSRF to RCE)
Sunucudan dosya okunması, (SSRF to LFI)
URL şemaları kullanarak sunucuya işlem yaptırılması, (ftp://, dict://, http://, gopher://, file:// vb.)
Cloud servislerin meta-data bilgilerinin çekilmesi,
Whitelist ve DNS çözümlemelerinin aşılması gibi faaliyetler yapılabilir.




