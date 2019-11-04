**_11- SSL Sertifika Türleri**

Kullanılan SSL sertifikaları 3 farklı türden oluşuyor:
	* Domain Validation [DV]
	* Organization Validation [OV]
	* Extended Validation [EV]
	
* Domain Validation da CA (Certifica Authority) yalnızca siteye girilen adresin (domain namein) sizin olup olmadığını doğrular.
Eğer web istesi seninse, bunu bazı prosedürleri uygulayarak alabilirsin.
* Organization Validation için CA 'lar, domain name dışında, şirketin adresi, telefonu, sertifikayı almak isteyen kişinin yetkisini
vesayire doğrular. Bu doğrulama genelde telefonda yapılırmış.
* Extended Validationda şirketin kurulduğu ülkedeki ticari kayıtları, kuruluş belgesi vs. gibi bir sürü belge istenir. Bu sertifikayı alanlar
web urlsinin yanında aynı zamanda şirket ismi olanlardır.

Son yıllarda çıkan Let't Encrypt  ile ücretsiz DV tipi sertifikalar almak mümkün.