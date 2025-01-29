# Main Metodu
Java'da bir program çalışacağı zaman, kodlar ilk olarak main metodu içerisinden başlar. Main metodu sayesinde derleyiciye, programı buradan başlatılması konusunda referans oluşturulur.
``` java
public class JavaPatika {
    public static void main(String[] args) {
        System.out.println("Hello World!");
    }
}
```
Artık programı çalıştırdığımızda, derleyici ilk olarak main metodu okuyup sonrasında gerekli işlemleri yapacaktır.\
Main metodu yazılırken, args yerine başka bir isimlendirme yapılabilir. Ancak genellikle args sözcüğü kullanılır ve bu sözcük arguments sözcüğünün kısaltmasıdır. Arguments ile ifade edilen kısım, sınıf çalıştırılırken JVM tarafından bu sınıfa verilen parametrelerdir.

# Syntax 
Syntax terimi herhangi bir programlama dilinin yazım kurallarını belirler.
![Java-Syntax](https://github.com/GrkmAyarkan/NOTLAR/blob/main/images/java-syntax.jpg)

# Ekrana Veri Yazdırma
Aynı satırda kalınması isteniyorsa;
````
System.out.print("Hello World!")
````
Yazınlan komuttan sonra yeni satıra inilmesi isteniyorsa;
````
System.out.println("Hello World!")
````

# Escape Karakterleri
| Kaçış Karakterleri| Açıklamalar|
| :--- | :---: |
| `\t` | "Tab" boşluk ekler |
| `\b` | "Backspace" ekler |
| `\n` | Bir satır aşşağı atlar |
| `\r` | Metne bir satır başı ekler |
| `\f` | Sayfa sonunu belirtmek için kullanılır |
| `\\` | Ters eğik çizgi eklemek için kullanılır |
| `\'` | Tek tırnak eklemek için kullanılır |
| `\"` | Çift tırnak eklemek için kullanılır |

# Yorum Satırı
Yorum Satırları `*//*` ve `/* ... */` ile oluşturulur.
Yazılış:
``` java
// Bu bir yorum satırıdır!
int number = 10; // Bu da bir yorum satırdır!
/* Birden fazla
satırda yorum
satırı yapmak
istediğimizde böyle
yapabiliriz. */
```
`/** ... */` ile yapılan açıklamalar:
Bir uygulama geliştirilirken kod içi belgeleme yapmak güzel bir programlama alışkanlığıdır.\
Bu tarzda yazılan açıklama satırlarına Javadoc adı verilmektedir. Javadoc için kullanılabilecek bazı örnekler ve ne için kullanılabilecekleri aşağıda listelenmiştir:
| Etiket| Açıklama | Syntax |
| :--- | :---: | :--- |
| `@author` | Class'ı yazan kişi | @author grkmayarkan |
| `{@code}` | Metodun kullanım örneğini vermek için | {@code ...} |
| `@exception` | Metot istisnası ve açıklaması | @exception istisna açıklama |
| `@param` | Değişkenler, değişken tipleri ve bu değişkenlerin açıklamaları | @param değişken - açıklama|
| `@return` | Metottan bir değer dönüyorsa açıklaması | @return açıklama |
| `@see` | Başka bir metod ya da açıklamaya referans göstermek için kullanılır | @see referans |
| `@since` | Metodun oluşturma tarihi | @since tarih |
| `@version` | Sınıfın version numarası | @version version numarası |
```
/**
 * @author GrkmAyarkan - 29.01.2025
 */
public class AciklamaSatiriOrnegi {
    /**
     * Verilen sayının karekökünü bularak döndürür.
     * Sayının sıfırdan küçük olmadığını varsayar.
     *
     * @param sayi Karekökü alınacak sayı
     * @return Sayının karekökü
     */public double karekok(double sayi) {
        double kkok = 0;
        // burada karekök bulma algoritmasının çalıştığını kabul edelim return kkok;
    }
}
```
# Değişken Tanımlama
### <veri tipi> <değişken ismi> = veri (değer)
İlk önce değişkenin veri tipini ve değişkenin ismini yazarız ve istenirse aynı matematikteki gibi "=" eşittir ile değerini atarız.
``` java
int number;
// number isminde, int veri tipinde bir değişken tanımlanır.
```
Veri tipleri aynı olan değişkenleri aynı satırda tanımlayabiliriz;
``` java
int a, b, c;
// int veri tipinde 3 tane değişken tanımlanır.
```
Değişkeni tanımladıktan sonra, atama operatörü (=) kullanarak değişkene atayabiliriz;
``` java
double pi; // ilk başta double türünde bir değişken tanımladık
pi = 3.14; // Daha sonra bu değişkene bir değer atadık
```
Eğer bir değişkene hemen değer atayacaksanız, bunu iki satırda yapmak yerine tek bir satırda yapabiliriz;
``` java
double pi = 3.14;
```
Aynı satırda aynı türden birden fazla değişken tanımlayabiliriz;
``` java
int a = 1 , b = 2;
// Aynı satırda int türünde 2 farklı değişken tanımlanmış ve ikisine de değer verilmiş
```
Değişkene verilen değer sonrasında değiştirilebilir, ama aynı isimde ikinci bir değişken oluşturulamaz.

# Java'daki İlkel Veri Tipleri
* Tam Sayılar
* Byte
* Short
* Integer
* Long
* Ondalıklı Sayılar
* Float
* Double
* Karakterler
* Char
* Mantıksal Değerler
* Boolean



