**SPF ( Sender Policy Frameword ) Record**

SPF kaydı, e-postanın teslimi sırasında sahte gönderen adreslerini tespit etmek için tasarlanmış bir e-posta doğrulama yöntemidir.
Microsoft'un spamları engellemek için başlatmış olduğu bir hizmettir. Sunucunun gerçek bir sunucu olduğunu
doğrulamaktadır.

Alan adının DNS kayıtlarında, o alan adının hangi ip adreslerinden email gönderdiğini belirten TXT kayıtlarına 
verilen isimdir. Eposta gönderimlerinde gönderici için "kimlik ibrazı" da denilebilir. Özellikler Gmail,Hotmail,Yahoo 
gibi mail servislerinin kontrol ettiği SPF kayıt doğrulaması ile ISS'ler , aldıkları e-posta mesajının, gönderim 
yapılan sunucu ile gönderici mail adresinin gerçek gönderici olduğunu teyid etmek isterler. SPF kaydı dns veritabanında tutulur
DNS in "text" kaydında tutulur.

-kitterman.com/spf/validate.html adresinden kontrol edilebilir
-anonymousmail.me adresinden, eğer domaine ait spf kaydı yok ise onların adına mail gönderebilirsin ve sahteliği belli olmaz.

