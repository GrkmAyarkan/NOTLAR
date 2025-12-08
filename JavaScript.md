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
* Explicit Coercion, Metotlarla yapılan dönüşümdlerdir.
* Implicit Coercion, Operatörlerle veya JavaScriptin kendi yaptığı dönüşümlerdir.
#### Explicit Dönüşümleri
##### String'e Dönüşüm
Number -> String
```js
let sayi = 42;
let metin = String(sayi);  // "42"
```
Boolean -> String
```js
let durum = true;
let yazi = String(durum);  // "true"
```
##### Number'a Dönüşüm
String -> Nuber
```js
let metin = "123";
let sayi = Number(metin);   // 123
```
Boolean -> Number
```js
Number(true);   // 1
Number(false);  // 0
```
Geçersiz Bir String İfadeyi Number'a Dönüştürmeye Çalışmak
```js
Number("abc");  // NaN
```
##### Boolean'a Dönüşüm
Number -> Boolean
```js
Boolean(1);   // true
Boolean(0);   // false
```
String -> Boolean
```js
Boolean("Merhaba"); // true
Boolean("");        // false
```
#### Implicit Dönüşümleri
String + Number
```js
let sonuc = "10" + 5;   // "105" (string birleştirme)
```
Number + Number (string içinde olsa bile)
```js
let toplam = "10" - 2;  // 8
```
#### parseInt ve parseFloat
Sayısal string -> Tam sayı
```js
parseInt("42");     // 42
parseInt("42px");   // 42
parseFloat("3.14"); // 3.14
```
### Template Literals Kullanımı
Template Literals (önceki adıyla Template Strings), kod okunabilirliği ve yazım kolaylığı sağlayan ES6 ile gelmiş bir string yazma şeklidir.

Normalde sıklıkla kullandığımız şekli ile string yazma şeklimiz:
```js
let ad = "Görkem"
let soyad = "Ayarkan"
console.log("Merhaba "+ ad + " " + soyad + ", sitemize hoş geldin.")
```
Bunun yerine kullanabileceğimiz diğer yöntem ise şu şekildedir:
```js
let ad = "Görkem"
let soyad = "Ayarkan"
let email = "grkm.ayarkan@gmail.com"
let info = `
Merhaba ${ad} ${soyad}, sitemize hoş geldin.
Email: ${email} -> Mail Uzunluğu: ${email.length}
Hesap: ${(200+450)*10}$
Anlık Saat Bilgisi: ${new Date().getHours()}
İsminizin ilk harfi: ${ad[0]}
Soyadınızın il 3 harfi: ${soyad.slice(0,3)}
`
console.log(info)
```
## String Veri Türü İşlemleri
### Length - Uzunluk Değerini Alma
String veri tipindeki ifadenin karakter sayısını verir.
```js
let ad = "Görkem"
console.log(ad.length)
```
Çıktı: 6
### indexOf - Metin İçinde Arama Yapma
Metinin içinde aramak istediğimiz değerin index numarasını verir.
```js
let ad = "Görkem"
console.log(ad.indexOf("ke"))
```
Çıktı: 3
### lastIndexOf - Metin içinde Arama Yapma
indexOf ile arasındaki tek fark aranan kelime birden fazla geçiyor ise en son eşleşmeden gelen index numarasını döndürür.
```js
let soyad = "Ayarkan"
console.log(soyad.lastIndexOf("a"))
```
Çıktı: 5
### search - Metin İçinde Arama Yapma
indexOf ile aynı sonuçlara ulaşırız genel olarak "Regular Expressions" işlemleri için çok kullanılan bir metottur.
```js
let ad = "Görkem"
console.log(ad.search("ke"))
```
Çıktı: 3
### slice - Metinden Parça Almak
Metin içinden almak istediğimiz yerlerin index numaralarını vererek metin içinde bulunan parçayı alabiliriz.
```js
let adSoyad = "Görkem Ayarkan"
console.log(adSoyad.slice(4, 11)) //Bitiş indeksindeki eleman sonuca dahil edilmez.
```
Çıktı: em Ayar
```js
let adSoyad = "Görkem Ayarkan"
console.log(adSoyad.slice(3)) //Bitiş indeksindeki eleman sonuca dahil edilmez.
```
Çıktı: kem Ayarkan

Not: Tek index yazmak ise yazılan index numarasından sonra gelen tüm karakterleri almasına neden olur.
### replace – Metin Bulma ve Değiştirme
Aranan metni istediğimiz metin ile değiştirmemize olanak sağlar.
```js
console.log(adSoyad.replace("Görkem", "Nehir"))  //Çıktı: Nehir Ayarkan
console.log(adSoyad)                             //Çıktı: Görkem Ayarkan
```
**replace** değişkende tanımlı olan veriyi temelli olarak değiştirmez o yüzden ilk çıktı "Nehir Ayarkan" olarka verilmesine rağmen daha sonra değişkeni tekrar yazdırmak istedğimizde eski değeri olan "Görkem Ayarkan" çıktısını alırız.
### toUpperCase ve toLowerCase
* **toUpperCase**: metindeki tüm harfleri büyük harfe çevirir.
* **toLowerCase**: metindeki tüm harfleri küçük harfe çevirir.
```js
console.log(adSoyad.toUpperCase()) //Çıktı: GÖRKEM AYARKAN
console.log(adSoyad.toLowerCase()) //Çıktı: görkem ayarkan
``` 
### concat - Metin Birleştirme
Elimizde bulunan iki string türündeki veriyi birleştirmemize olanak sağlar. Ama bu değişiklik kalıcı bir değişiklik değildir.
```js
console.log(ad.concat(" " + soyad)) // ad = Görkem, soyad = Ayarkan
```
Çıktı: Görkem Ayarkan
### charAt- İndex Numarasına Göre Karakter Bulmak
Belirtilen index numarasında yer alan karakteri verir.
```js
console.log(adSoyad.charAt(10))
```














.
