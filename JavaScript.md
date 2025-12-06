# JavaScript
JavaScript (kısaca JS), web sitelerini interaktif (etkileşimli) ve dinamik hale getiren, dünyanın en popüler programlama dilidir.

İnternet tarayıcınızın (Chrome, Safari, Firefox vb.) anladığı ve çalıştırabildiği ana dildir. Eğer bir web sitesini statik bir belgeden (sadece yazı ve resim) yaşayan bir uygulamaya dönüştürmek istiyorsanız, JavaScript kullanırsınız.
#### Öncelikle Konsolda Çıktı Almanın Yolları
* `console.log("Hello World)`
* `alert("Hello World")`
* `document.write("Hello World")`

## Değişken Tanımlama
#### Değişken Tanımlama Sırasında Dikkat Edilmesi Gerekenler
* Değişken isimleri Türkçe karakter **içermemelidir**.
* Değişken isimleri büyük ve küçük harf **duyarlıdır**. **(case-sensitive)**
* Değişken isimlerinde ilk karakter bir sayı **olamaz**.
* Değişken isimlerinde JavaScript etiketleri **kullanılamaz**.
* Değişken isimlerinde sayı, harf, alt çizgi ve dolar işareti **kullanılabilir**; boşluk, noktalama işareti veya sembol **kullanılamaz**.
* Değişken isimleri **harf**, **_** veya **$** ile başlayabilir. Fakat ES5 (ECMAScript 5) birlikte gelen özellikle UNICODE kodları kullanılırken kaçış karakteri olarak kullanılan \ işareti ilk karakter olarak kullanılabilir.
* İlk harften sonra değişken isimlerinde rakamlar da kullanılabilir. $ ve _ dışında başka noktalama işaretleri kullanılamaz.
#### Değişkene Değer Atama ve Veri Türleri
* Bir değişkene değer atamak için **=** operatörü kullanılır.
* Tanımlayıcı öncesi **var**, **let** veya **const** deklarasyonlarından biri kullanılarak deklare edilir.
  - **var**: Eski, kapsamı geniş ve riskli. Modern JS’te neredeyse hiç kullanılmaz.
  - **let**: En güvenli ve en çok kullanılan değiştirilebilir değişken. Değeri zaman içinde değişmesi gereken değişkenlerde kullanılır.
  - **const**: Sabit değerler veya değişmeyecek referanslar için.
#### Örnek değişken tanımlamaları: 
* **var** ile değişken tanımlama
```js
var name = "Görkem"
```
* **let** ile değişken tanımlama
```js
let surname = "Ayarkan"
```
* **const** ile değişken tanımlama
```js
const number = 1234
```
### Farklı veri tipleri için değişken tanımlama örnekleri:
#### let
```js
let sehir = "İzmir"; // String
let sicaklik = 30; // Number
let girisYapildiMi = false; //Boolean
let ogrenciListesi = ["Ayşe", "Mehmet", "Zeynep"]; //Array
let kitap = {      // Object
    baslik: "Dune",
    yazar: "Frank Herbert",
    sayfa: 894
};
let sonuc = null; //Null
let bildirim; // Undefined
```
#### const
```js
const ulke = "Japonya"; // String
const maxHiz = 220; // Number
const odemeTamamlandi = true; // Boolean
const koordinatlar = [40.98, 29.12, 523]; // Array
const profil = {    // Object
    kullaniciAdi: "mav3rick",
    takipci: 1240
};
const hata = null; // Null
const bekleyenDeger = undefined; // Undefied
```
### let üerinde yapılabilecek değişiklikler
```js
let name = "Görkem"
// Değikenin değerini değiştirmek
name = "Nehir"
console.log(name) // çıktı: Nehir
// Birleştirme veya ekleme işlemi
name = name + "Ayarkan"
// Veya
name += " Ayarkan"
console.log(name) // çıktı: Nehir Ayarkan
```
### Number Veri Tipi Üzerinde Yapılabilecek İşlemler
JavaScript, **weakly-typed** yani güçsüz türlü bir dildir. Değişkenlerin ve parametrelerin türlerini bildirmek gerekmez, tür değişkenin kullanım şeklinden belirlenir.
```js
let x = 3; //integer
let x = 3.2; //float
```
### Aritmetik Operatörler
* Toplama: +
* Çıkarma: -
* Çarpma: *
* Üs Alma: **
* Bölme: /
* Mod Alma: %
* Arttırma: ++
* Eksiltme: --
#### Ek Bilgi
Arttırma ve azaltma operatörlerinin kullanım şekiline göre etkisi değişir.
```js
let sayi = 1;
   let a = ++sayi;
   alert(a); // 2

   let sayi = 1;
   let a = sayi++; 
   alert(a); // 1
   console.log(sayi); // 2 değerini verir.
```
### Değişken Türünü Kontrol Etme
Veri tiplerini kontrol ederken sıkça **typeof** kullanılır.
```js
console.log(typeof 42)
// beklenen çıktı: "number"
console.log(typeof "kodluyoru")
// beklenen çıktı: "string"
```
**isInteger()**, **isFiniter()** veya **isNaN()** kullanmak

**isInteger()** sayıların tam sayı olup olmadıklarını kontrol eder.
```js
Number.isInteger(-123) //true
Number.isInteger(0.5) //false
```
**isFinite()** bir değerin sonlu bir sayı olup olmadığını belirler.
```js
Number.isFinite(0) //true
Number.isFinite('123') //false
Number.isFinite('hello') //false
```
**isNaN()** bir değerin NaN (Not-A-Number) olup olmadığını belirler.
```js
Number.isNaN(123) //false
Number.isNaN(0) //false
Number.isNaN('123') //false
Number.isNaN("Hello") //false
```
### Değişken Türünü Değiştirme (Type Coercion)
* Explicit Coercion
* Implicit Coercion
asdawd











.
