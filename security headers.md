**1 – Strict-Transport-Security**

HTTP Strict Transport Security, nâmi diger HSTS, kullanicilarin internet tarayicilarini her talep için HTTPS 
kullanmaya zorlayarak downgrade adi verilen saldirilara karsi çözüm üretmek ve tüm trafigin güvenligini saglamak 
adina güzel bir çözümdür.

**2 – X-Frame-Options**

Web uygulama güvenligi konularindan bir tanesi olan Clickjacking, X-Frame-Options baslik bilgisi ile dogrudan 
iliskilidir. Saldirganin kendi kontrolü altinda olan web sitesi içerisinde iframe çagrisi gerçeklestiren 
saldirganlar, kullanicilara istemedikleri aksiyonlari aldirmaya çalisirlar.

X-Frame-Options’in 3 farkli parametresi bulunmaktadir.

**Deny** = Sayfanin herhangi bir frame içerisinde çagirilmasini tamamiyle engelle.

**SAMEORIGIN** = Kendi domain’imden baska herhangi bir domainin frame içerisinde çagirmasini engelle.

**ALLOW-FROM uri** = Parametre olarak verilen uri adresinin iframe çagrilarini kabul et. Haricindekileri engelle.


**3 – X-XSS-Protection**
Kullanicilari XSS saldirilarindan korumak için X-XSS-Protection baslik bilgisi kullanilmalidir. Tabi öncelik 
uygulama tarafinda XSS zafiyetlerini gidermek olmalidir. Kod bazli güvenlik saglandiktan sonra, korumayi bir 
kat arttirarak internet tarayicilarinda da XSS güvenligi aktiflestirilmelidir.

Modern tarayicilar, uygulama tarafindan olusturulan içerik üzerinde filtreleme gerçeklestirerek potansiyel 
XSS payloadlarini tespit edebilirler. Bu özelligi aktiflestirmek içinse X-XSS-Protection baslik bilgisi kullanilir.

**4 – X-Content-Type-Options**
HTTP spesifikasyonuna göre bos olmayan her HTTP yaniti, ilgili içerigin tarayici tarafindan nasil yorumlanacagini belirleyen bir Content-Type headeri belirtmeli:

örnegin: Content-Type text/html; charset=ISO-8859-4

Mime Type Sniffing, sunulan içerigin tipi belirtilmedigi durumlarda, tarayicilarin sayfa görüntülenmesinde en dogru yolu bulabilmek için, içerigi degerlendirmesi islemidir.
Kisaca sunulan belgede Content-Type header’i ile içerigin tipi belirtilmedigi takdirde, tarayici içerigi "koklayarak", kaynagi en dogru biçimde görüntülemeye çalisir.

Özellikle de upload fonksiyonlariyla beraber, sniffing islemi bir takim tehlikeler arz edebilir. Örnegin, kullanicinin zararsiz addedilen bir text dosyasi upload ettigini 
varsayalim. Eger bu text dosyasi HTML ve script taglari, JavaScript kodlari içeriyorsa ve biz bu yüklenen dosyayi tekrar kullaniciya sunarken bir Content-Type belirtmiyorsak, 
tarayici bu sayfanin içerigini koklayarak bunun pek tabii bir "text/html" tipinde bir dosya olduguna karar verecektir ve bu sayfadaki zararli kodlar da çalisacaktir.

Iste bu gibi durumlarda, tarayicinin sayfa içerigini koklayarak, inceleyerek servis edecegi tipe karar vermesinin önüne geçmek için X-Content-Type-Options headeri kullanilmaktadir.

**5- HttpOnly flag**

Web uygulamalari kullanicilarin oturumlarini session ID üzerinden takip etmektedir. Bu deger kullaniciya HTTp Set-Cookie baslik bilgisi ile iletilmektedir. Internet tarayicilari bu 
degeri saklayarak, Cookie’nin geçerli oldugu kapsam için olusturulacak her HTTP talebinde bu degeri otomatik olarak talebe ekleyecektir.
Bu deger uç durumlar hariç, sadece ve sadece HTTP talebi içerisinde kullanilmalidir. Bir diger ifade ile;
Oturum anahtari bilgisine Javascript vb client-site programming ile ulasilmamasi gerekir..!

Cookie set isleminde gönderilen HttpOnly degerine dikkat ediniz. HttpOnly bayragini gören internet tarayici document.cookie degiskeni üzerinden Cookie’e erisim yapildiginda HttpOnly 
bayragi olan degerleri isleme almayacaktir.


**6- Secure flag**

Set-Cookie isleminde Secure bayraginin kullanilmasi, bu Cookie degerinin sadece ve sadece HTTPS taleplerde header’a eklenecegini ifade etmektedir. Dolayisiyla bu cookie bilgisini
MITM saldirilarindan korur.

