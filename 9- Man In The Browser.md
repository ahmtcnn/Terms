**Man In The Browser**
Aslında man in the middle ile benzerlik gösteren bir saldırı türü.

* Bilgisayara indirilen bir trojan yazılımı bizim tarayıcımıın ayarlarına bir eklenti (extension) yüklüyor.
* Tarayıcıyı açtığımızda bu eklenti çalışıyor. Bütün girilen url leri saldırı yapmak üzere inceliyor. Saldırı yapacağı
urllerin listesini kendisinde tutuyor. örn : https://bankx.com/account/send_money

* Kullanıcı submit butonuna tıkladığı an eklenti bu sayfayının tüm içeriğini alıyor ve hatırlıyor.
* Daha sonra içeriğini DOM arayüzü ile değiştiriyor ve tarayıcıya devam et diyor.
* Form değiştirilmiş biçimde submit ediliyor. 


Kaynak:https://www.owasp.org/index.php/Man-in-the-browser_attack

