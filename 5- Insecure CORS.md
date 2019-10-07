**Insecure CORS - Cross-Origin Resource Sharing (Kökenler arasi kaynak paylasimi)**

 web tarayicisi tarafindan yönetilen ve ek HTTP basliklari kullanilarak, bir kökende çalisan web uygulamasinin, 
farkli bir kökende yer alan web uygulamasina erisim izni kontrolünü saglayan mekanizmadir.Web uygulamasi, internet 
tarayicisi üzerinden farkli bir kökene (protokol, domain ve port) herhangi bir istek gönderirse cross-origin HTTP istegi olusturmus olur.
Örnegin, http://domain-a.com üzerinde yer alan bir web uygulamasinin JavaScript tarafindan ajax istegi göndererek, 
http://domain-b.com‘a erismesi bir cross origin istegidir.

Not: Eger frontend (browser) tarafindan degil de backend tarafindan (Örnegin C# koduyla) domain-b.com’a erisseydi bu bir cross origin istek olmayacakti.

Günümüzdeki birçok modern internet tarayicisi, JavaScript kodu üzerinden baslatilan HTTP isteklerini güvenlik 
nedenlerinden dolayi kisitlar. Ajax istekleri, tarayici üzerinde gerçeklesirken same-origin policy‘i (ayni köken 
politikasini) izler. Bu nedenle, ajax istegi gerçeklestiren bir web sitesi, sadece kendi sitesi üzerindeki 
kaynaklara erisim saglama yetkisi vardir. Eger farkli bir siteye erismek istiyorsa ilgili sitenin yer aldigi 
uygulamada CORS basliklarinin uygun sekilde ayarlanmasi gereklidir.

Internet tarayicisi, bir domain’e yapilan isteklerde, o domain ile ilgili cookie’leri de yapilan istege iliskilendirir 
ve sunucuya iletir. Login islemleri için kullanilan session cookie’leri buna güzel bir örnektir. Kullanici siteye 
giris yaptiktan sonra oturum açilmis olur ve geri dönen session cookie bilgisi tarayicida saklanir. Sonraki 
isteklerde otomatik olarak session cookie bilgisi de sunucuya iletilir.

Normalde zararsiz gibi görünen bu yöntem, kullanicinin kendi tarayicisinda açtigi kötü niyetli bir sitenin, mevcut 
session cookie bilgisini kullanarak arka planda ilgili siteye istek göndermesi ile faciaya yol açabilir.
Same-origin policy bu gibi güvenlik nedenlerinden dolayi olusturulmustur.

Birçok kisi tarafindan CORS bir güvenlik mekanizmasi gibi görünse de aslinda tam tersini icra etmektedir. Same-origin 
policy güvenligi saglarken CORS, istenen siteler için istisnai durumlari olusturmayi saglar. SOP engeller, CORS ise izin verir. 
Bu nedenle, CORS için sitenin binevi disariya açilan kapisi gibi düsünebiliriz.

Hangi istek türleri için CORS ayarlanmalidir?
Ajax çagrilari adini verdigimiz XMLHttpRequest ve fetch() API çagrilari,
Web fontlarinin kullanimi (CSS üzerinden @font-face ile yapilan çagrimlar)
WebGL tarafindan istek edilen görsel çagrilari
Canvas’a drawImage() metodu kullanilarak çizilen görsel ve videolar.


CORS için server'in response header inda olmasi gereken basslik bilgisi
Access-Control-Allow-Origin: http://ahmetcan.com

yani burdan gelenleri SOP a bakmaksizin kabul ediyor. Veya;
Access-Control-Allow-Origin: * 

iste bu bütün sitelere izin veriyor.

Request blocked varsa sikinti yok

Aslinda request header'a da Origin basligi ile bir site ekleyerek görebiliyorsak burdada zafiyet olabilir anlamina geliyor. 



