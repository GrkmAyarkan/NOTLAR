# JAVA
İçindekiler;
* [Main Metodu](https://github.com/GrkmAyarkan/NOTLAR/blob/main/Java.md#main-metodu)
* [Syntax](https://github.com/GrkmAyarkan/NOTLAR/blob/main/Java.md#syntax)
* [Ekrana Veri Yazdırma](https://github.com/GrkmAyarkan/NOTLAR/blob/main/Java.md#ekrana-veri-yazd%C4%B1rma)
* [Escape Karakterleri](https://github.com/GrkmAyarkan/NOTLAR/blob/main/Java.md#escape-karakterleri)
* [Yorum Satırı](https://github.com/GrkmAyarkan/NOTLAR/blob/main/Java.md#yorum-sat%C4%B1r%C4%B1)
* [Değişken Tanımlama](https://github.com/GrkmAyarkan/NOTLAR/blob/main/Java.md#de%C4%9Fi%C5%9Fken-tan%C4%B1mlama)
* [Java Veri Tipleri](https://github.com/GrkmAyarkan/NOTLAR/blob/main/Java.md#java-veri-tipleri)
  - [Java'daki İlkel Veri Tipleri](https://github.com/GrkmAyarkan/NOTLAR/blob/main/Java.md#javadaki-i%CC%87lkel-veri-tipleri)
  - [Tam Sayı Veri Tipleri](https://github.com/GrkmAyarkan/NOTLAR/blob/main/Java.md#tam-say%C4%B1-veri-tipleri)
  - [Ondalıklı Sayı Veri Tipleri](https://github.com/GrkmAyarkan/NOTLAR/blob/main/Java.md#ondal%C4%B1kl%C4%B1-say%C4%B1-veri-tipleri)
  - [Özel Karakter ve Mantıksal Eleman Veri Tipleri](https://github.com/GrkmAyarkan/NOTLAR/blob/main/Java.md#%C3%B6zel-karakter-ve-mant%C4%B1ksal-eleman-veri-tipleri)
  - [String Veri Tipi](https://github.com/GrkmAyarkan/NOTLAR/blob/main/Java.md#string)
* [Temel Operatörler](https://github.com/GrkmAyarkan/NOTLAR/blob/main/Java.md#temel-operat%C3%B6rler)
  - [Atama Operatörü](https://github.com/GrkmAyarkan/NOTLAR/blob/main/Java.md#atama-operat%C3%B6r%C3%BC)
  - [Aritmetik Operatörler](https://github.com/GrkmAyarkan/NOTLAR/blob/main/Java.md#aritmetik-operat%C3%B6rler)
  - [Karşılaştırma Operatörleri](https://github.com/GrkmAyarkan/NOTLAR/blob/main/Java.md#kar%C5%9F%C4%B1la%C5%9Ft%C4%B1rma-operat%C3%B6rleri)
  - [Mantıksal Operatörler](https://github.com/GrkmAyarkan/NOTLAR/blob/main/Java.md#mant%C4%B1ksal-operat%C3%B6rler)
  - [Koşul Operatörü](https://github.com/GrkmAyarkan/NOTLAR/blob/main/Java.md#ko%C5%9Ful-operat%C3%B6r%C3%BC)
* [Kullanıcıdan Veri Alma](https://github.com/GrkmAyarkan/NOTLAR/blob/main/Java.md#kullan%C4%B1c%C4%B1dan-veri-alma)
* [if, else, else if](https://github.com/GrkmAyarkan/NOTLAR/blob/main/Java.md#if-else-else-if)

## Main Metodu
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

## Syntax 
Syntax terimi herhangi bir programlama dilinin yazım kurallarını belirler.
![Java-Syntax](https://github.com/GrkmAyarkan/NOTLAR/blob/main/images/java-syntax.jpg)

## Ekrana Veri Yazdırma
Aynı satırda kalınması isteniyorsa;
````
System.out.print("Hello World!")
````
Yazınlan komuttan sonra yeni satıra inilmesi isteniyorsa;
````
System.out.println("Hello World!")
````

## Escape Karakterleri
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

## Yorum Satırı
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
## Değişken Tanımlama
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

## Java Veri Tipleri 
### Java'daki İlkel Veri Tipleri
* Tam Sayılar
  - Byte
  - Short
  - Integer
  - Long
* Ondalıklı Sayılar
  - Float
  - Double
* Karakterler
  - Char
* Mantıksal Değerler
  - Boolean

### Tam Sayı Veri Tipleri
#### Byte
* 8 bit uzunluğundadır. Max 127, Min -128 değerleri arasındadır.
* Anahtar sözcük: **byte**
#### Short
* 16 bit uzunluğundadır. Max 32,767, Min -32,768 değerleri arasındadır.
* Anahtar sözcük: **short**
#### Integer
* 32 bit uzunluğundadır. Max 2,147,483,647 , Min -2,147,483,648 değerleri arasındadır.
* Anahtar sözcük : **int**
#### Long 
* 64 bit uzunluğundadır. Max 9,223,372,036,854,775,807 , Min -9,223,372,036,854,775,808 değerleri arasındadır.
* Anahtar sözcük : **long**

### Ondalıklı Sayı Veri Tipleri
#### Float
* 32 Bit boyutundadır ve 1.4×10^-45 ile 3.4×10^38 aralığında bir değer tanımlanabilir.
* Float içerisine tam sayı yazdığımız zamanda bile o sayı 1.0 şeklinde ondalıklı olarak algılar.
* Float ile double ayırmak için , float tanımlamalardan sonra ‘f’ veya ‘F’ konulmalıdır.
* Anahtar Sözcük : **float**
#### Double
* 64 Bit boyutundadır ve 4.9×10^-324 ile 1.8×10^308 aralığında bir değer tanımlanabilir.
* Üst düzey matematiksel işlemlerde kullanılır
* Anahtar Sözcük : **double**
``` java
float number1 = 3.14F;
float number2 = 3.14f;
double number3 = 3.14;
```

### Özel Karakter ve Mantıksal Eleman Veri Tipleri
#### Char
Java'da karakter değişkenleri saklamak için Char kullanılır. Char veri tipleri birleşerek String Sınıfından bir yapıya dönüşür.

* Karakterler Char ile saklanır.
* Diğer dillere göre Char Java’da 16 bittir.
* Java Unicode karakter setini kullanır ve tüm dilleri içerir.
* Java evrensel bir dil olarak tasarlandığı için karakter seti de evrensel set olan Unicode ile tanımlanmıştır.
* Anahtar Sözcük : **char**

#### Boolean
Java, mantıksal değerleri saklamak için boolean adında bir tipe sahiptir.

* Boolean sadece iki değer alabilir : True ve False
* Genellikle koşul ve döngü işlemlerinde, kontrol amaçlı olarak kullanılır.
* Anahtar Sözcük : **boolean**
```
public class JavaPatika {
    public static void main(String[] args) {
        char letter = 'u';
        boolean logic1 = true;
        boolean logic2 = false;
    }
}
```

### String
String sınıfı java.lang kütüphanelerinde bulunan ve metinlerle ilgili her türlü işlemin yapıldığı sınıftır. Java'da genellikle kelime tutmak için char yerine String sınıfı kullanılır. Basitçe şöyle düşünebiliriz , Char veri tipi tek bir karakter tutabiliyorken, charların birleşmesiyle oluşan sözcükleri String Sınıfı tutmaktadır.
```
public class JavaPatika {
    public static void main(String[] args) {
        String words = "Hello World";
    }
}
```

## Temel Operatörler
Java dilinde operatörler birçok işlemi yapabilmenize olanak tanır.

Java'da operatörler aşağıdaki gibi listelenebilir:

* Atama Operatörleri
* Aritmetiksel Operatörler
* İlişkisel ve Eşitlik Operatörler
* Mantıksal Operatörler
* Koşul Operatörler

### Atama Operatörü 
| Operatör| Açıklama| Örnek|
| :--- | :---: | ---: |
| = | Basit atama operatörüdür. Operatörün sağındaki değer solundaki değişkene atanır. | `C = A + B;` A + B'nin değerini C'ye atar. |
| += | Sağdaki değeri, solundaki değişkenin değeri ile toplayıp tekrar soldaki değişkene atar. | `C += A;` ile `C = C + A;` eşittir. |
| -= | Sağdaki değeri, solundaki değişkenin değerinden çıkartıp tekrar soldaki değişkene atar. | `C -= A;` ile `C = C - A;` eşittir. |
| *= | Sağdaki değeri, solundaki değişkenin değeri ile çarpıp tekrar soldaki değişkene atar. | `C *= A;` ile `C = C * A;` eşittir. |
| /= | Soldaki değişkenin değerini, sağdaki değere bölüp tekrar soldaki değişkene atar. | `C /= A;` ile `C = C / A;`  eşittir. |
| %= | Soldaki değişkenin değerini, sağdaki değere göre modunu alıp tekrar soldaki değişkene atar. | `C %= A;` ile `C = C % A;`  eşittir. |

### Aritmetik Operatörler
Java'da Aritmetik Operatörler adından da anlaşılacağı üzere matematiksel işlemleri programlama dilinde uygulamamızı sağlarlar.

* Toplama: `a + b`
* Çıkarma: `a – b`
* Çarpma: `a * b`
* Bölme: `a / b`
* Mod alma: `a % b`
* 1 arttırma: `a++`
* 1 eksiltme: `b--`

### Karşılaştırma Operatörleri
Java'da Karşılaştırma Operatörleri iki nesnenin birbirleriyle olan durumlarını belirler.

* Eşitlik: `a == b`
* Eşit Değil: `a != b`
* Büyüktür: `a > b`
* Küçüktür: `a < b`
* Büyük Eşittir: `a >= b`
* Küçük Eşittir: `a <= b`

### Mantıksal Operatörler
Java'da Mantıksal Operatörler , nesnelerin veya ifadelerin mantıksal değerlerini yansıtır.

* Ve: `a && b`
* Veya: `a || b`
* Değil: `!(a&&b)`

### Koşul Operatörü
Java'da Koşul Operatörleri ifadelerin sonucunda oluşacak olayları belirler.
``` java
a = 5 ;
b = (a == 1) ? 1 : 0
Çıktısı : 0
```

## Kullanıcıdan Veri Alma
Java’da kullanıcıdan veri almak için Scanner sınıfı kullanılır. Ama bu sınıfı kullanmadan önce kodumuza Scanner sınıfını dahil etmemiz gerekir. Bunun için **import** deyimi kullanılır ;
``` java
import java.util.Scanner;
```
İmport deyimi projenin en başına yazılır.
 
Veriyi kullanıcıdan almak için yapmamız gereken **Scanner** sınıfını kullanmak. Scanner sınıfından türeyen adı **input** olan bir nesne tanımlayalım. Scanner sınıfından nesne ürettikten sonra değişkenimize veri almak için, değişkenimizin türüne göre bir kod yazmamız gerekecektir. Eğer değişkenimizin **integer** türünde ise `input.nextInt()` veya double türünde ise `input.nextDouble()` kod bloğu kullanılmalıdır.
``` java
import java.util.Scanner;

public class JavaNotlar {
    public static void main(String[] args) {
        Scanner input = new Scanner(System.in);
        int a,b;

        System.out.println("A sayısını giriniz : ");
        a = input.nextInt();

        System.out.println("B sayısını giriniz : ");
        b = input.nextInt();

        System.out.println("A Sayısı : " + a);
        System.out.println("B Sayısı : " + b);
    }
}
```

### Veri Tiplerine Göre Scanner Metotları
| Method | Açıklama |
| :--- | :---: |
| nextBoolean() | Boolean değişkenlere veri almak için kullanılır. |
| nextByte() | Byte değişkenlere veri almak için kullanılır. |
| nextDouble() | Double değişkenlere veri almak için kullanılır. |
| nextFloat() | Float değişkenlere veri almak için kullanılır. |
| nextInt() | Integer değişkenlere veri almak için kullanılır. |
| nextLine() | String değişkenlere veri almak için kullanılır. |
| nextLong() | Long değişkenlere veri almak için kullanılır. |
| nextShort() | Short değişkenlere veri almak için kullanılır. |

``` java
import java.util.Scanner;

public class JavaNotlar {public static void main(String[] args) {
        Scanner inp = new Scanner(System.in);
        
        // String Örneği
        String adSoyad = inp.nextLine();
        
        // Sayı Örnekleri
        int yas = inp.nextInt();
        double maas = inp.nextDouble();
        
        // Çıktılar
        System.out.println("Ad Soyad: " + adSoyad);
        System.out.println("Yaş : " + yas);
        System.out.println("Maaş : " + maas);
    }
}
```
## IF, ELSE, ELSE IF
### **if**
`if`, Java'da belirli bir koşulu kontrol eden ve koşul **doğru** (**true**) olduğunda kod bloğunu çalıştıran bir kontrol yapısıdır.
``` java
if (sayi > 0) {
    System.out.println("Sayı pozitiftir.");
}
```
### **else**
`else`, `if` koşulu sağlanmadığında (**false** olduğunda) çalışacak alternatif kod bloğunu belirler.
``` java
if (sayi > 0) {
    System.out.println("Sayı pozitiftir.");
} else {
    System.out.println("Sayı negatif veya sıfırdır.");
}
```
### **else if**
`else if`, birden fazla koşulu sıralı şekilde kontrol etmek için kullanılır.
``` java
if (sayi > 0) {
    System.out.println("Sayı pozitiftir.");
} else if (sayi < 0) {
    System.out.println("Sayı negatiftir.");
} else {
    System.out.println("Sayı sıfırdır.");
}
```







