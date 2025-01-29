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





