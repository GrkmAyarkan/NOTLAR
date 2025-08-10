# HTML

### İçindekiler
* Etiketler


## ETİKETLER

### HTML Etiketi
Bu etiket, kendi altında mutlaka `<head>` ve `<body>` etiketlerini barındırmalıdır. Eğer bir HTML dökümanı oluşturmak isterseniz ilk yapacağınız iş bir `<html>` etiketi oluşturmaktır. Ardından HTML etiketi altına `<head>` ve `<body>` etiketlerini yazmalısınız.
```
<html>   <head></head> 
  <body></body>
</html>
```

### HEAD Etiketi
`<head>` etiketi, site ziyaretçileri tarafından görülmesi gerekmeyen kodları içerir. Bu etiket altına yazılan kodlar genellikle arama motorları ve örümcekler (Crawler veya Spider diye geçer) içindir. Head etiketi altında bütün etiketleri kullanabilmeniz mümkün değil. Kullanabileceğiniz etiketler;
* <title> (Bu etiketi kullanmak şarttır)
* <meta>
* <style>
* <script>
* <noscript>
* <link>
* <base>
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
















.
