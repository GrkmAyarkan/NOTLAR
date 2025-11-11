# HTML

### İçindekiler
* [EN ÇOK KULLANILAN ETİKETLER](https://github.com/GrkmAyarkan/NOTLAR/blob/main/HTML.md#eti%CC%87ketler-en-%C3%A7ok-kullan%C4%B1lan-etiketler)
  - [HTML Etiketi](https://github.com/GrkmAyarkan/NOTLAR/blob/main/HTML.md#html-etiketi)
  - [HEAD Etiketi](https://github.com/GrkmAyarkan/NOTLAR/blob/main/HTML.md#head-etiketi)
  - [BODY Etiketi](https://github.com/GrkmAyarkan/NOTLAR/blob/main/HTML.md#body-etiketi)
  - [!DOCTYPE html Etiketi](https://github.com/GrkmAyarkan/NOTLAR/blob/main/HTML.md#doctype-html-etiketi)
  - [H Etiketi (Başlık)](https://github.com/GrkmAyarkan/NOTLAR/blob/main/HTML.md#h-etiketi-ba%C5%9Fl%C4%B1k)
  - [P Etiketi (Paragraf)](https://github.com/GrkmAyarkan/NOTLAR/blob/main/HTML.md#p-etiketi-paragraf)
  - [BR Etiketi (Satır Atlama)](https://github.com/GrkmAyarkan/NOTLAR/blob/main/HTML.md#br-etiketi-sat%C4%B1r-atlama)
  - [A Etiketi (Linkleme)](https://github.com/GrkmAyarkan/NOTLAR/blob/main/HTML.md#a-etiketi-linkleme)
  - [UL - OL - Li Etiketi (Liste Etiketi)](https://github.com/GrkmAyarkan/NOTLAR/blob/main/HTML.md#ul---ol---li-etiketi-liste-etiketi)
  - [HR Etiketi (Geçiş Etiketi)](https://github.com/GrkmAyarkan/NOTLAR/blob/main/HTML.md#hr-etiketi-ge%C3%A7i%C5%9F-etiketi)
  - [STRONG ve B Etiketi (Metin Kalınlaştırma Ve Önem Belirtme)](https://github.com/GrkmAyarkan/NOTLAR/blob/main/HTML.md#strong-ve-b-etiketi-metin-kal%C4%B1nla%C5%9Ft%C4%B1rma-ve-%C3%B6nem-belirtme)
  - [Script Etiketi](https://github.com/GrkmAyarkan/NOTLAR/blob/main/HTML.md#script-etiketi)
  - [BUTTON Etiketi](https://github.com/GrkmAyarkan/NOTLAR/blob/main/HTML.md#button-etiketi)
  - [IMG Etiketi (Resim Etiketi)](https://github.com/GrkmAyarkan/NOTLAR/blob/main/HTML.md#img-etiketi-resim-etiketi)
  - [IFRAME Etiketi](https://github.com/GrkmAyarkan/NOTLAR/blob/main/HTML.md#iframe-etiketi)
  - [Yorum Satırı](https://github.com/GrkmAyarkan/NOTLAR/blob/main/HTML.md#yorum-sat%C4%B1r%C4%B1)
* [BAŞLIK ETİKETLERİNİN KULLANIMI](https://github.com/GrkmAyarkan/NOTLAR/blob/main/HTML.md#ba%C5%9Flik-eti%CC%87ketleri%CC%87ni%CC%87n-kullanimi)
  - [TİTLE Etiketi](https://github.com/GrkmAyarkan/NOTLAR/blob/main/HTML.md#ti%CC%87tle-etiketi)
  - [Style ve Script Etiketleri](https://github.com/GrkmAyarkan/NOTLAR/blob/main/HTML.md#style-ve-script-etiketleri)
    * [Style Etiketi](https://github.com/GrkmAyarkan/NOTLAR/blob/main/HTML.md#style-etiketi)
    * [Script Etiketleri](https://github.com/GrkmAyarkan/NOTLAR/blob/main/HTML.md#script-etiketleri-javascript)
      - [Script Tag Özellikleri](https://github.com/GrkmAyarkan/NOTLAR/blob/main/HTML.md#script-tag-%C3%B6zellikleri) 
      - [Güvenlik (crossorigin ve integrity)](https://github.com/GrkmAyarkan/NOTLAR/blob/main/HTML.md#crossorigin)

## ETİKETLER (En Çok Kullanılan Etiketler)

### HTML Etiketi
Bu etiket, kendi altında mutlaka `<head>` ve `<body>` etiketlerini barındırmalıdır. Eğer bir HTML dökümanı oluşturmak isterseniz ilk yapacağınız iş bir `<html>` etiketi oluşturmaktır. Ardından HTML etiketi altına `<head>` ve `<body>` etiketlerini yazmalısınız.
```html
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
```html
<html>   <HEAD>
    <title> Sekmede Görülecek İsim </title>
    <meta name="Keywords" content="HTML,Kodluyoruz">
  </HEAD> 
  
  <BODY></BODY>
  
</html>
```

### BODY Etiketi
Web sayfamızda görmek istediğimiz bütün içerikleri `<body>` etiketi altına yazıyoruz. Anlatacağım diğer etiketleri `<body>` etiketi içerisine yazacağız.
```html
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
```html
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
```html
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
```html
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
```html
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
```html
<body>
    <a href="https://github.com/GrkmAyarkan">Görkem Ayarkan Github</a>
</body>
```

### UL - OL - Li Etiketi (Liste Etiketi)
`<ul>` ve `<ol>` etiketleri liste oluşturma etiketleridir. Listeyi oluşturduktan sonra içeriğini oluşturmak için `<li>` etiketini kullanıyoruz. /
`<ul>` = "**unordered list**" sırasız liste anlamına geliyor. `<ol>` = "**ordered list**" sıralı liste anlamına geliyor.
```html
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
```html
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
```html
<body>
    <h2><strong> Kodluyoruz </strong></h2>
    <p><b> HTML </b> Etiketleri </p>
</body>
```

### Script Etiketi
`<script>` etiketi **JavaScript** kodlarını **HTML** içerisine yazabilmemizi sağlar.
```html
<body>
    <script>
        document.write("Kodluyoruz")
    </script>
</body>
```

### BUTTON Etiketi
`<button>` etiketini buton oluşturmak için kullanırız. Buton üzerine yazmak istediğiniz içeriği etiketin içine yazmanız yeterlidir.
```html
<body>
    <button> Buton </button>
</body>
```

### IMG Etiketi (Resim Etiketi)
Resim eklemek için `<img>` etiketini kullanıyoruz. `<img src=”resim.jpg” alt=”açıklama yazısı” />`, `src=""` kısmına eklemek istediğimiz görselin yolunu yani kaynağını yazmalıyız. Eğer görselimiz ve HTML dosyamız aynı klasörde ise görselin adını ve uzantısını yazmamız yeterlidir. alt="" kısmına görselin açıklamasını yazıyoruz fakat isterseniz boş bırakabilirsiniz. Bu etiket kapanmaya ihtiyaç duymaz.
```html
<body>
    <img src="https://github.com/GrkmAyarkan/NOTLAR/blob/main/images/pixelArt.gif" alt="Görkem Ayarkan" />
</body>
```

### IFRAME Etiketi
Belge içinde belge gösterebilmemizi sağlayan etikettir. Genelde başka bir sitedeki belgeyi kendi sayfamızda göstermek için kullanırız. örn: Youtube'dan bir videoyu sayfamızda göstermek istersek `<iframe>` kodlarını sayfamıza eklememiz yeterli.(video üzerinde sağ tıklayıp yerleştirme kodunu kopyala diyerek **iframe** kodunu kopyalayabiliriz.)
```html
<body>
    <iframe width="789" height="444" src="https://www.youtube.com/embed/dQw4w9WgXcQ" frameborder="0" 
      allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; 
      allowfullscreen></iframe>
</body>
```

### Yorum Satırı
HTML dilinde yorum satırı `<!--` ile başlar `-->` ile biter.
```html
<body>
    <!-- Örnek Yorum Satırı -->
    <!-- 
        2. Örnek Yorum Satırı 
    -->   
</body>
```

## BAŞLIK ETİKETLERİNİN KULLANIMI
##### (`<head></head>` etiketi arasına yazılan etiketler)

### TİTLE Etiketi
"**BAŞLIK**" görevini üstlenir.
```html
<title> GÖRKEM AYARKAN </title>
```
Bu şekilde başlık belirlediğimizde:
* Sekme isminde "**GÖRKEM AYARKAN**" yazdığını görürüz.
* Sayfayı favorilere eklerken görünür.
* Arama motorları sayfanın bu kısmına bakarak siteyi listeler.

## Style ve Script Etiketleri
### Style Etiketi
`<style></style>` etiketleri arasında sayfamızı güzelleştiren, renklendiren belli özellikler tanımlayabiliyoruz. Bu kısımlarda, bir html dökümanında hangi alanın nerede ve nasıl görünmesi gerektiğini tasarlayabiliriz. Belli kuralları olan bu belirteçlere **CSS** diyoruz. \
NOT: HTML dökümanı işlenirken ve görüntülenirken sayfa sırayla işlendiği için her zaman sırasıyla en altta kalan stil belirlemeleri baskın gelecektir.

### Script Etiketleri (JavaScript)
Bu etiketle web sayfalarının, browser yardımıyla çalıştırabildiği kodlar yazabiliriz. Sayfamızı canlandırabilir, hareketlendirebilir her alanda değişiklik yapabiliriz.
#### Script Tag Özellikleri
Eğer script etiketini kullanırken herhangi bir özellik eklemezsek browser sırası geldiğinde doğrudan işlenir. Ve bu kısım işlenmeden sayfa yüklenmeye devam etmez. Bu noktada da async özelliğimiz devreye giriyor. Eğer sayfanın yüklenmeye devam ederken eşzamanlı olarak bu etiketlerle belirlediğimiz scriptlerin de yüklenmesini ve hazırlanmasını istiyorsak, yani bu kısmın asenkron çalışmasını istiyorsak etiketimize bu özelliği ekliyoruz. Herhangi bir değer girmemize gerek yok şu şekilde kullanabiliriz:
```html
<script src="myJavascript.js" async></script>
```
Eğer bu etiketin sayfa yüklendikten sonra yüklenip çalıştırılmasını istiyorsak o zaman async özelliğinin yanına defer özelliğini de eklememiz gerekiyor. Ancak bu iki özellik de yalnızca sayfa harici kaynaktan yani bu HTML içinde yazmadığımız javascripti yüklerken kullanabileceğimiz özellikler. Buna da dikkat etmemiz gerekiyor.

Bu alanın doğru şekilde korunması ve kullanılması için kullanılacak iki özellik vardır. 

#### Crossorigin
Bunlardan biri **Crossorigin**.

crossorigin, HTML’de genellikle <img>, <script>, <link> gibi etiketlerde kullanılan bir özelliktir.
Amaç: farklı bir kaynaktan (domain, port veya protokol) gelen veriye tarayıcının nasıl davranacağını belirtmektir.

Kısaca:
Bir dosyayı (örneğin bir script veya resim) başka bir siteden yüklüyorsan, crossorigin tarayıcıya “bu isteği kimlik bilgileriyle mi, yoksa anonim mi yapayım?” diye söyleyen bir ayardır.
```html
<script src="https://example.com/script.js" crossorigin="anonymous"></script>
```
Üç olası değeri vardır:
* anonymous → Kimlik bilgileri (çerez, token vs.) gönderilmez.
* use-credentials → Kimlik bilgileri gönderilir.
* (boş bırakılırsa) → Tarayıcı varsayılan olarak kimlik bilgisi göndermez.

#### Integrity
İkinci özellik ise **integrity**.

Integrity genellikle crossorigin ile birlikte kullanılan bir HTML özelliğidir ve dosyanın bozulmadığından veya değiştirilmediğinden emin olmak için kullanılır. Tarayıcıya, “Bu dosyanın içeriği şu hash değerine eşit olmalı, değilse yükleme!” demektir. 

Bir CDN’den (örneğin Bootstrap veya jQuery) dosya yüklüyorsan, biri o dosyayı gizlice değiştirirse tarayıcı fark eder ve dosyayı çalıştırmaz.
```html
<script src="https://cdn.jsdelivr.net/npm/bootstrap@5.3.0/dist/js/bootstrap.bundle.min.js"
        integrity="sha384-kenU1KFdBIe4zVF0s0G1M5b4hcpxyD9F7jL+rrZn/t0I3zZVnN0v7l6GCEa8hZsj"
        crossorigin="anonymous"></script>
```
Buradaki integrity değeri (hash) dosyanın SHA384 kontrol özetidir.
Tarayıcı dosyayı indirir → hash değerini hesaplar → bu değer integrity ile uyuşmazsa dosyayı çalıştırmaz.

Özetle:
* **crossorigin** → Dosyayı nasıl isteyeceğini belirler.
* **integrity** → Dosyanın güvenli ve değişmemiş olduğunu doğrular.

#### referrerpolicy
Ayrıca bir diğer etiketimiz de **refreferrerpolicy**. Bu etiket de scripti yükleyeceğimiz zaman, alacağımız kaynağa atacağımız verileri eklemek için kullınılır.
**referrerpolicy**, tarayıcıya hangi “referrer” bilgisini (yani geldikleri sayfanın adresini) başka bir siteye gönderip göndermemesi gerektiğini söyler.

“**Referrer**” = Kullanıcı bir bağlantıya tıkladığında, hedef siteye hangi sayfadan geldiğini gösteren bilgidir.
Ama bazen gizlilik veya güvenlik nedeniyle bu bilgi gönderilmez ya da kısıtlanır.
```html
<a href="https://example.com" referrerpolicy="no-referrer">Example'a git</a>
```
Yaygın değerler:
* **no-referrer** → Hiç referrer göndermez.
* **origin** → Sadece alan adını gönderir (https://mysite.com gibi).
* **strict-origin-when-cross-origin** → Aynı sitede tam adresi gönderir, farklı sitede sadece alan adını.
* **unsafe-url** → Her zaman tam adresi gönderir (en az güvenli seçenek).









.
