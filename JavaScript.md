# JavaScript
JavaScript (kısaca JS), web sitelerini interaktif (etkileşimli) ve dinamik hale getiren, dünyanın en popüler programlama dilidir.

İnternet tarayıcınızın (Chrome, Safari, Firefox vb.) anladığı ve çalıştırabildiği ana dildir. Eğer bir web sitesini statik bir belgeden (sadece yazı ve resim) yaşayan bir uygulamaya dönüştürmek istiyorsanız, JavaScript kullanırsınız.
#### Öncelikle Konsolda Çıktı Almanın Yolları
* `console.log("Hello World)`
* `alert("Hello World")`
* `document.write("Hello World")`

## Değişken Tanımlama
#### Değişken Tanımlama Sırasında Dikkat Edilmesi Gerekenler
* Değişken isimleri **harf**, **_** veya **$** ile başlayabilir. Fakat ES5 (ECMAScript 5) birlikte gelen özellikle UNICODE kodları kullanılırken kaçış karakteri olarak kullanılan \ işareti ilk karakter olarak kullanılabilir.
* İlk harften sonra değişken isimlerinde rakamlar da kullanılabilir. $ ve _ dışında başka noktalama işaretleri kullanılamaz.
* Değişken isminde boşluk kullanılamaz.
#### Değişkene Değer Atama ve Veri Türleri
* Bir değişkene değer atamak için **=** operatörü kullanılır.
* Tanımlayıcı öncesi **var**, **let** veya **const** deklarasyonlarından biri kullanılarak deklare edilir.
  - **var**: Eski, kapsamı geniş ve riskli. Modern JS’te neredeyse hiç kullanılmaz.
  - **let**: En güvenli ve en çok kullanılan değiştirilebilir değişken. Değeri zaman içinde değişmesi gereken değişkenlerde kullanılır.
  - **const**: Sabit değerler veya değişmeyecek referanslar için.
#### Örnek değişken tanımlamaları: 
```js
// var ile değişken tanımlama
var name = "Görkem"
```
