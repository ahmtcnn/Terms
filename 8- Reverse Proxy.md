**Reverse Proxy Vs Proxy**

- Bu ikisinin farkını ilk basta anlayamamistim. Burada kalsın.
Proxy internete bir adrese erişim sırasında kullanılan vekil sunucudur. 
Yani http/s isteğini ilk olarak bu proxy ye yolluyorsun o bilgisayarda,
senin için o isteği oraya iletip cevabı yine kendi üzerinden sana dönüyor
Bu sayede kimliğini gizleyebiliyorsun. İşte farkta burada, normal proxy de client
kendi kimliğini koruyor. Burada proxy client adına çalışıyor.

- Reverse proxy ise sunucuya hizmet eder. Gelen istekleri arkasındaki sunucuya iletir, 
cevapları ordan alır ve adrese geri yollar. Ancak burada sunucunun ip adresi vs saklanmış
olur. Aynı zamanda tabiki bizim sunucumuzun önünde başka bir sunucu tutarak web serverın yükü
de azaltılabilir