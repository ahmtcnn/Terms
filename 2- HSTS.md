**HSTS - Http Strict Transport Security**

HTTP Strict Transport Security, nâmi diger HSTS, kullanicilarin internet tarayicilarini her talep için HTTPS 
kullanmaya zorlayarak downgrade adi verilen saldirilara karsi çözüm üretmek ve tüm trafigin güvenligini saglamak
adina güzel bir çözümdür. 

Strict-Transport-Security: max-age=16070400; includeSubDomains

Internet tarayicisi bu bayragi gördükten sonra max-age degiskeninde tanimlanan saniye kadar cache’te tutulacaktir.
 Belirlenen bu zaman dilimi içerisinde kullanici tarafindan olusturulan tüm talepler dogrudan HTTPS olarak 
baslatilacaktir. Örnegin; kullanici https://www.mehmetince.net veya protokol tanimlamasini belirtmeden direk 
mehmetince.net olarak web sitesine erisim yapilmak istenirse, internet tarayicisi otomatik olarak protokolü https
olarak belirtecek ve güvenli baglanti gerçeklestirecektir.