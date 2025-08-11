# HTML

### İçindekiler
* [ETİKETLER (En Çok Kullanılan Etiketler)](https://github.com/GrkmAyarkan/NOTLAR/blob/main/HTML.md#eti%CC%87ketler-en-%C3%A7ok-kullan%C4%B1lan-etiketler)
  - [HTML Etiketi](https://github.com/GrkmAyarkan/NOTLAR/blob/main/HTML.md#html-etiketi)
  - [HEAD Etiketi](https://github.com/GrkmAyarkan/NOTLAR/blob/main/HTML.md#head-etiketi)
  - [BODY Etiketi](https://github.com/GrkmAyarkan/NOTLAR/blob/main/HTML.md#body-etiketi)
  - [!DOCTYPE html Etiketi](https://github.com/GrkmAyarkan/NOTLAR/blob/main/HTML.md#doctype-html-etiketi)
  - [H Etiketi (Başlık)](https://github.com/GrkmAyarkan/NOTLAR/blob/main/HTML.md#h-etiketi-ba%C5%9Fl%C4%B1k)
  - [P Etiketi (Paragraf)](https://github.com/GrkmAyarkan/NOTLAR/blob/main/HTML.md#p-etiketi-paragraf)
  - [BR Etiketi (Satır Atlama)](https://github.com/GrkmAyarkan/NOTLAR/blob/main/HTML.md#br-etiketi-sat%C4%B1r-atlama)
  - [A Etiketi (Linkleme)](https://github.com/GrkmAyarkan/NOTLAR/blob/main/HTML.md#a-etiketi-linkleme)
  - [UL - OL - Li Etiketi (Liste Etiketi)](https://github.com/GrkmAyarkan/NOTLAR/blob/main/HTML.md#ul---ol---li-etiketi-liste-etiketi)
  - [HR Etiketi (Geçiş Etiketi)](https://www.google.com/)
  - [STRONG ve B Etiketi (Metin Kalınlaştırma Ve Önem Belirtme)](https://www.google.com/)
  - [Script Etiketi](https://www.google.com/)
  - [BUTTON Etiketi](https://www.google.com/)
  - [IMG Etiketi (Resim Etiketi)](https://www.google.com/)
  - [IFRAME Etiketi](https://www.google.com/)
  - [Yorum Satırı](https://www.google.com/)


## ETİKETLER (En Çok Kullanılan Etiketler)

### HTML Etiketi
Bu etiket, kendi altında mutlaka `<head>` ve `<body>` etiketlerini barındırmalıdır. Eğer bir HTML dökümanı oluşturmak isterseniz ilk yapacağınız iş bir `<html>` etiketi oluşturmaktır. Ardından HTML etiketi altına `<head>` ve `<body>` etiketlerini yazmalısınız.
```
<html>   <head></head> 
  <body></body>
</html>
```

### HEAD Etiketi
`<head>` etiketi, site ziyaretçileri tarafından görülmesi gerekmeyen kodları içerir. Bu etiket altına yazılan kodlar genellikle arama motorları ve örümcekler (Crawler veya Spider diye geçer) içindir. Head etiketi altında bütün etiketleri kullanabilmeniz mümkün değil. Kullanabileceğiniz etiketler;
* `<title>` (Bu etiketi kullanmak şarttır)
* `<meta>`
* `<style>`
* `<script>`
* `<noscript>`
* `<link>`
* `<base>`
```
<html>   <HEAD>
    <title> Sekmede Görülecek İsim </title>
    <meta name="Keywords" content="HTML,Kodluyoruz">
  </HEAD> 
  
  <BODY></BODY>
  
</html>
```

### BODY Etiketi
Web sayfamızda görmek istediğimiz bütün içerikleri `<body>` etiketi altına yazıyoruz. Anlatacağım diğer etiketleri `<body>` etiketi içerisine yazacağız.
```
<html>   <HEAD>
    <title> Sekmede Görülecek İsim </title>
    <meta name="Keywords" content="HTML,Kodluyoruz">
  </HEAD> 
  
  <BODY>
    Site İçeriği
  </BODY>
</html>
```

### !DOCTYPE html Etiketi
`<!DOCTYPE html>` : Dökümanımızın HTML dilinde olduğunu tarayıcımıza bildiren talimattır. /
`<html lang="en">` : Site içeriğinin dilini belirten etiket, "**en**" yerine "**tr**" yazabilirsiniz.
```
<!DOCTYPE html> <html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>
</head>
<body>

</body>
</html>
```

### H Etiketi (Başlık)
`<h>` etiketleri başlık etiketleridir. Büyükten küçüğe doğru ilerler;
```
<h1>
<h2>
<h3>
<h4>
<h5>
<h6>
```
**Not:** HTML otomatik olarak Başlık etiketlerinin öncesine ve sonrasına satır atlatır.

### P Etiketi (Paragraf)
`<p>` etiketi paragraf etiketidir. Sayfa içerisinde oluşturacağımız metinleri `<p>` etiketi ile oluştururuz. \
**Not:** HTML otomatik olarak Paragraf etiketinin öncesine ve sonrasına satır atlatır.
```
<!DOCTYPE html> <html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>
</head>
<body>
    <h2>Kodluyoruz</h2>
    <p>HTML Etiketleri</p>
</body>
</html>
```

### BR Etiketi (Satır Atlama)
`<br>` etiketi satır atlatma etiketidir ve kapatmaya ihtiyaç duymayan etiketlerden biridir. Atlatmak istediğiniz satır sayısı kadar `<br>` etiketi kullanabilirsiniz. / 
**NOT:** <br> etiketinin farklı kullanımlarını görebilirsiniz. örn.( `<br>`,`<br/>`,`<br />`) Hepsi aynı işlevi yerine getirir.
```
<!DOCTYPE html> <html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>
</head>
<body>
    <h2>Kodluyoruz</h2> <br>
    <p>HTML <br> Etiketleri</p>
</body>
</html>
```

### A Etiketi (Linkleme)
`<a>` etiketinin en önemli özelliği **href** özelliğidir. Bu etiket ile sayfaları linkleyebiliriz. Etiket içerisine yazılan içerik sayfa üzerinde gösterilecek içeriktir. **href** içine yazılan ise tıklandığında gideceği URL'dir.
```
<body>
    <a href="https://github.com/GrkmAyarkan">Görkem Ayarkan Github</a>
</body>
```

### UL - OL - Li Etiketi (Liste Etiketi)
`<ul>` ve `<ol>` etiketleri liste oluşturma etiketleridir. Listeyi oluşturduktan sonra içeriğini oluşturmak için `<li>` etiketini kullanıyoruz. /
`<ul>` = "**unordered list**" sırasız liste anlamına geliyor. `<ol>` = "**ordered list**" sıralı liste anlamına geliyor.
```
<body>
    <ul>
        <li>HTML</li>
        <li>CSS</li>
        <li>JavaScript</li>
    </ul>
    <ol>
        <li>HTML</li>
        <li>CSS</li>
        <li>JavaScript</li>
    </ol>
</body>
```

### HR Etiketi (Geçiş Etiketi)
`<hr>` etiketi konusal bir geçişi temsil eder. Yazı yazarken yeni bir paragrafa başlamaya benzetebiliriz. Varsayılan olarak sayfaya yatay bir çizgi ekler ama bu özelliği değiştirilebilir. Bu etiket kapatılmaya ihtiyaç duymaz.
```
<body>
    <p>
      Filmin odaklandığı yakın gelecekte yeryüzündeki yaşam;
    </p>
    <hr>
    <p>
      Artan kuraklık ve iklim değişiklikleri nedeniyle tehlikeye girmiştir.
      İnsan ırkı yok olma tehlikesiyle karşı karşıyadır.
      Bu sırada yeni keşfedilen bir solucan deliği, tüm insanlığın umudu hâline gelir.
    </p>
    <hr>
    <p>
      Bir grup astronot-kaşif, buradan geçip boyut değiştirerek daha önce
      hiçbir insanoğlunun erişemediği yerlere ulaşmak ve insanoğlunun
      yeni yaşam alanlarını araştırmakla görevlendirilir.
    </p>
  </body>
```

### STRONG ve B Etiketi (Metin Kalınlaştırma Ve Önem Belirtme)
`<strong>` etiketi bir metinin arama motorlarına önemli olduğunu bildirmek için kullanılır. Kullanıldığı zaman metini kalın yapar. Eğer sadece metini kalınlaştırmak isterseniz `<b>` etiketini kullanabilirsiniz.
```
<body>
    <h2><strong> Kodluyoruz </strong></h2>
    <p><b> HTML </b> Etiketleri </p>
</body>
```

### Script Etiketi
`<script>` etiketi **JavaScript** kodlarını **HTML** içerisine yazabilmemizi sağlar.
```
<body>
    <script>
        document.write("Kodluyoruz")
    </script>
</body>
```

### BUTTON Etiketi
`<button>` etiketini buton oluşturmak için kullanırız. Buton üzerine yazmak istediğiniz içeriği etiketin içine yazmanız yeterlidir.
```
<body>
    <button> Buton </button>
</body>
```

### IMG Etiketi (Resim Etiketi)
Resim eklemek için `<img>` etiketini kullanıyoruz. `<img src=”resim.jpg” alt=”açıklama yazısı” />`, `src=""` kısmına eklemek istediğimiz görselin yolunu yani kaynağını yazmalıyız. Eğer görselimiz ve HTML dosyamız aynı klasörde ise görselin adını ve uzantısını yazmamız yeterlidir. alt="" kısmına görselin açıklamasını yazıyoruz fakat isterseniz boş bırakabilirsiniz. Bu etiket kapanmaya ihtiyaç duymaz.
```
<body>
    <img src="https://github.com/GrkmAyarkan/NOTLAR/blob/main/images/pixelArt.gif" alt="Görkem Ayarkan" />
</body>
```

### IFRAME Etiketi
Belge içinde belge gösterebilmemizi sağlayan etikettir. Genelde başka bir sitedeki belgeyi kendi sayfamızda göstermek için kullanırız. örn: Youtube'dan bir videoyu sayfamızda göstermek istersek `<iframe>` kodlarını sayfamıza eklememiz yeterli.(video üzerinde sağ tıklayıp yerleştirme kodunu kopyala diyerek **iframe** kodunu kopyalayabiliriz.)
```
<body>
    <iframe width="789" height="444" src="https://www.youtube.com/embed/dQw4w9WgXcQ" frameborder="0" 
      allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; 
      allowfullscreen></iframe>
</body>
```

### Yorum Satırı
HTML dilinde yorum satırı `<!--` ile başlar `-->` ile biter.
```
<body>
    <!-- Örnek Yorum Satırı -->
    <!-- 
        2. Örnek Yorum Satırı 
    -->   
</body>
```













.
