**User Agent String**

Kullandığımız tarayıcıların tümü içerisinde bir User Agent stringi barındırıyor. Bu string, bağlandığımız sunuculara gönderiliyor.
User Agent bilgisi içinde hangi tarayıcıyı ve hangi işletim sistemini kullandığımız yazıyor. http://www.useragentstring.com adresinden 
user agent bilgimizin nasıl göründüğüne bakabiliriz. curl, wget veya python-request ile istek attığımızda user-agent bilgisi olarak
direk python ve diğer toolların isimlerinin olduğunu gördük. Bunları değiştirebiliriz. Curl için -A parameteresi kullanılır örneğin. Tarayıcıda
da User Agent Switcher eklentisi var. Oradan istediğini veya kendi yazdığın user-agent ı kullanabilirsin.

