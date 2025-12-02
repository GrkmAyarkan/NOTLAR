* [CSS](https://github.com/GrkmAyarkan/NOTLAR/blob/main/CSS.md#csscascading-style-sheets-nedir)






# CSS(Cascading Style Sheets) Nedir?
CSS (Basamaklanmış Stil Katmanları), web sayfasını şekillendirmek için kullanılan bir kodlama türüdür. CSS kullanarak web sayfasının görünümünü ve düzenini değiştirebiliriz. Bir web sitesinin görünümünün masaüstü bilgisayarlar, tabletler ve mobil cihazlar gibi farklı ekranlarda nasıl değiştiğini de tanımlayabiliriz. CSS, C++ veya JavaScript gibi bir programlama dili değildir. Bunun nedeni, CSS'in amacının web tarayıcıları için biçimlendirmeye(HTML'e) stil vermek olmasıdır. HTML yalnızca içeriği "işaretleyen" bir dildir - yani, belgeye belirli bir görsel ve yapısal biçimlendirme verir.
#### Kullanım örneği
Bir başlığı renklendirelim:
```html
<h1>BAŞLIK</h1>
```
![Html Başlık Siyah](https://github.com/GrkmAyarkan/NOTLAR/blob/main/images/Html%20Başlık%20Örnek%2001.png)

Öncelikle, CSS'e HTML öğesini nasıl bulacağını söylememiz gerekir. Bunu selector denen bir özellik ile yapabiliriz. CSS'de bir selector, HTML öğelerini etiket adı, sınıf adı, kimliği ve çok daha fazlasına göre bulmak için kullanılır.

```html
<style> h1 { color: red; } </style>
<h1>BAŞLIK</h1>
```
![Kırmızı Başlık](https://github.com/GrkmAyarkan/NOTLAR/blob/main/images/Html%20Kırmızı%20Başlık.png)

Bunların yanı sıra CSS kodlarımızı .css uzantılı bir dosya içerisinde tutar ve bu dosyayı HTML sayfası içerisine basit bir kodla çağırabiliriz. Örneğin CSS dosyamızın adı "**baslik.css**" olsun ve bu dosyayı Html sayfaya eklemek için HTML içine yazmamız gereken kod şu şekildedir.
```html
<head> <link rel="stylesheet" type="text/css" href="baslik.css" /> </head>
```

Bir CSS selector tanımlamanın birçok farklı yolu vardır, aşağıda selector türlerinin bazı örneklerini görebilirsiniz:
* Class Selector: HTML öğelerini sınıf özelliklerine göre bulur.
* ID Selector: Öğeleri belirli kimliğine göre bulur.
* Element Selector: Öğeleri etiket adlarına göre bulur.

#### Açıklama Satırı
```css
/* açıklama */
```

## CSS Yardımcı Kaynak
<a href="https://www.w3schools.com/css/default.asp">
  <img src="https://github.com/GrkmAyarkan/NOTLAR/blob/main/images/logolar/w3schools-LOGO.png" width="70">
</a>



.
