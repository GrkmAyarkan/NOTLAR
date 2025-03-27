# SQL
### İçindekiler
* [SQL Nedir?](https://github.com/GrkmAyarkan/NOTLAR/blob/main/SQL.md#sql-structured-query-language-nedir)
* [Veri ve Veritabanı](https://github.com/GrkmAyarkan/NOTLAR/blob/main/SQL.md#veri-ve-veritaban%C4%B1)
* [Veritabanı Yönetim Sistemi (DBMS)](https://github.com/GrkmAyarkan/NOTLAR/blob/main/SQL.md#veritaban%C4%B1-y%C3%B6netim-sistemi-dbms)
* [SELECT (Seçim Yapmak)](https://github.com/GrkmAyarkan/NOTLAR/blob/main/SQL.md#select)
* [WHERE (Koşul Ekleme)](https://github.com/GrkmAyarkan/NOTLAR/blob/main/SQL.md#where-ve-kar%C5%9F%C4%B1la%C5%9Ft%C4%B1rma-operat%C3%B6rleri)
* [BETWEEN ve IN (Aralık Belirtme ve Seçim Yapma)](https://github.com/GrkmAyarkan/NOTLAR/blob/main/SQL.md#between-ve-in)
* [LIKE ve ILIKE (Karakter Bulundurma Koşulu)](https://github.com/GrkmAyarkan/NOTLAR/blob/main/SQL.md#like-ve-ilike)
* [DISTINCT ve COUNT (Sütundaki Farklı Değerler ve Sonucun Veri Sayısı)](https://github.com/GrkmAyarkan/NOTLAR/blob/main/SQL.md#distinct-ve-count)
* [PSQL (Cmd Arayüz)](https://github.com/GrkmAyarkan/NOTLAR/blob/main/SQL.md#psql-1)
* [ORDER BY (Sıralama)](https://github.com/GrkmAyarkan/NOTLAR/blob/main/SQL.md#order-by)
* [LIMIT ve OFFSET (Limit ve Pass Geçme)](https://github.com/GrkmAyarkan/NOTLAR/blob/main/SQL.md#limit-ve-offset)
* [Aggregate (Topluluk) Fonksiyonlar - MIN, MAX, SUM, AVG ](https://github.com/GrkmAyarkan/NOTLAR/blob/main/SQL.md#aggregate-fonksiyonlar---min-max-sum-avg)
* [GROUP BY (Verileri Gruplama)](https://github.com/GrkmAyarkan/NOTLAR/blob/main/SQL.md#group-by)
* [HAVING (Gruplandırılmış Verilere Koşul Ekleme)](https://github.com/GrkmAyarkan/NOTLAR/blob/main/SQL.md#having)

## SQL (Structured Query Language) Nedir?
SQL Türkçe ifadesiyle yapılandırılmış sorgu dili anlamına gelmektedir. Biz SQL sayesinde verilerimizin bulunduğu veritabanı ile iletişime geçeriz. \
SQL bir programlama dili midir? Evet, SQL ilişkisel veritabanı yönetim sistemleri ile ilişki kurmamızı sağlayan bir declarative bildirimsel bir programlama dilidir.
### Bildirimsel Yaklaşım
``` sql
-- Yorum Satırı
SELECT title FROM book
WHERE page_number > 200;
```
Yukarıdaki sorgumuzda, veritabanındaki book tablosundan sayfa sayısı 200 den daha fazla olan kitapları görmek istiyoruz. Burada biz işin sonuç kısmıyla ilgileniyoruz. SQL, DBMS ile nasıl çalışır, arka tarafta yapılan işlemin bizim açımızdan önemi yoktur. Bundan dolayı SQL declarative yani bildirimsel, beyan edici bir yaklaşıma sahiptir.

## Veri ve Veritabanı
### Veri
Ölçüm, sayım, deney, gözlem veya araştırma sonucuyla elde edilen ham bilgilerdir.
### Veritabanı
Verilerin organize bir şekilde depolanmasını sağlayan sistemlerdir.

## Veritabanı Yönetim Sistemi (DBMS)
Veritabanı verilerimizi organize bir şekilde depolamımızı sağlayan yapılardı. İşte bu veritabanımızı oluşturmamızı, yönetmemizi ve SQL yardımıyla gerekli gördüğümüz sorguları yapmamızı sağlayan yazılımlara "**Database Management System**" veritabanı yönetim sistemi adı verilir. \
![DBMS](https://github.com/GrkmAyarkan/NOTLAR/blob/main/images/DBMS.jpg) \
Yukarıdaki şekilde de gördüğümüz üzere farklı kaynaklardan gelen sorgular DBMS yazılımı sayesinde farklı veritabanlarında kullanılır. \
Farklı ihtiyaçlara göre çeşitli veritabanı yönetim sistemleri bulunur. \
Temel veritabanı yönetim sistemleri:
* Hiyerarşik Veritabanı
* Ağ Veritabanı
* İlişkisel Veritabanı (RDBMS)
* Nesneye Yönelik Veritabanı

### İlişkisel Veritabanı (RDBMS) Yönetim Sistemleri
İlişkisel veritabanı sistemleri, verilerin birbirleri ile ilişkili tablolarda tutulduğu sistemlerdir. \
Aşağıda popüler veritabanı yönetim sistemi yazılımlarını görebilirsiniz. \
![RDBMS](https://github.com/GrkmAyarkan/NOTLAR/blob/main/images/RDBMS.png)

## SELECT
**SELECT** veritabanından belirtilen sütunlardaki verileri çekmemizi sağlar. Ayrıca SELECT komutunu çoğunlukla diğer SQL komutlarıyla birlikte kullanırız. SQL komutlarının büyük harf - küçük harf duyarlılıkları yoktur. (Case Insensitive)
#### SELECT Söz Dizimi
``` sql
SELECT <sütun_adı>, <sütun_adı>, ...
FROM <tablo_adı>;
```
Eğer tablodaki tüm sütunlardaki verileri çekmek istersek " * " karakterinden faydalanırız.
``` sql
SELECT *
FROM <tablo_adı>;
```

## WHERE ve Karşılaştırma Operatörleri
**SELECT** komutu ile yaptığımız çalışmalarda, çoğu durumda verilerin tamamını değil belirli koşulları sağlayan verileri görmek isteriz. Bunun için **WHERE** anahtar kelimesini kullanırız.
#### WHERE Söz Dizimi
``` sql
SELECT <sütun_adı>, <sütun_adı>, ...
FROM <tablo_adı>
WHERE <koşul>;
```
#### Örnek Kullanım
``` sql
SELECT title, rating
FROM film
WHERE rating > 6.5;
```
Bu sorgumuzda veritabanında bulunan **film** tablosundaki **title** ve **rating** sütunlarında bulunan verileri çekiyoruz ancak bu kez tüm verileri değil **rating > 6.5** koşulunu sağlayan verileri alıyoruz.
### Karşılaştırma Operatörleri
Aşağıda SQL ile birlikte kullanılan karşılaştırma operatörlerini görebilirsiniz. \
![SQL Karşılaştırma Operatörleri](https://github.com/GrkmAyarkan/NOTLAR/blob/main/images/SQL%20Karsilastirma%20Operatorleri.png)
### Mantıksal Operatörler
#### Örnek Kullanımlar
``` sql
SELECT *
FROM actor
WHERE firs_name = 'Tom' AND age < 25 ;
WHERE age < 25 OR age > 35 ;
```
**AND** operatörünün true sonucu dönmesi için bu iki koşulumuzun da sağlanması gerekiyor. \
**OR** operatörünün true sonucu dönmesi için bu iki koşulumuzunda herhangi birinin sağlanması yeterlidir.
``` sql
SELECT *
FROM film 
WHERE NOT rating <= 4.99 ;
```
**NOT** operatörü bize hangi koşulun olmaması gerektiğini belirtir. Bu örnekte **film** tablosundaki **rating**i 4.99 ve altı olanlar haricindeki veriler listelenir. \
Mantıksal operatörler birlikte kullanılabilir.
``` sql
SELECT *
FROM film 
WHERE NOT (rating = 4.99 OR rating = 2.99) ;
```

## BETWEEN ve IN
### BETWEEN 
``` sql
SELECT * FROM film
WHERE length >= 100 AND length <= 140;
```
Bu örnekte yapılan sorguda belli bir aralıktaki verileri istiyoruz. Bunu kısa yoldan **BETWEEN ... AND** yapısını kullanarak yapabiliriz.
``` sql
SELECT * FROM film
WHERE length BETWEEN 100 AND 140; -- WHERE length >= 100 AND length <= 140 ifadesi ile aynı sonucu verir.
```
Burada dikkat edilmesi gereken nokta 100 ve 140 sınır değerleri aralığa dahildir.
### IN
Şöyle bir senaryo düşünelim, yine film tablosundan uzunluğu 30, 60, 90 veya 120 dakikaya eşit olan verileri sıralayalım.
``` sql
SELECT * FROM film
WHERE length = 30 OR length = 60 OR length = 90 OR length = 120;
```
Bu örnekte olduğu gibi az sasyıda eşitlik yerine çok sayıda sorgu olduğunda, sürekli **OR** mantıksal operatörünü kullanmak yerine istenilen değerleri liste haline geitip **IN** anahtar kelimesiyle kullanabiliriz.
#### IN Söz Dizimi
``` sql
SELECT <sütun_adı>, <sütun_adı>, ... FROM <tablo_adı>
WHERE <sütun_adı> IN (değer1, değer2, ...);
```
#### Örnek
``` sql
SELECT * FROM film
WHERE length IN (30,60,90,120);
```
## LIKE ve ILIKE
Bizler bazı durumlarda tam eşleşme değil belirli şablonlara uyan koşulların sağlanmasını isteriz. Örneğin sorgumuzda **first_name** sütununun belli bir isme eşit olmasını değil, ilk harfin 'P' olması koşulunu sağlayan sorguya ihtiyacımız var. Bunun için **LIKE** operatörünü kullanırız.
``` sql
SELECT *
FROM actor
WHERE first_name LIKE 'P%';
```
Burada kullanılan **%** karakteri sıfır, bir veya daha fazla karakteri temsil eder ve **Wildcard** olarak isimlendirilir. Bir diğer **wildcard** karakteri **_** karakteridir ve bir karakteri temsil eder.
#### LIKE Söz Dizimi
``` sql
SELECT <sütun_adı>, <sütun_adı>, ...
FROM <tablo_adı>
WHERE <sütun_adı> LIKE <şablon>;
```
**ILIKE** operatörü **LIKE** operatörünün **case - insensitive** (**BÜYÜK - küçük** harf duyarsız.)  versiyonudur. \
**LIKE** operatörünün kıllanımını ihtiyacımıza göre şekillendirebiliriz.
#### Örnek
``` sql
SELECT *
FROM actor
WHERE first_name LIKE 'P%'; -- Bize P ile başlayan isimleri listeler.
WHERE first_name LIKE '%y'; -- y ile biten isimleri listeler.
WHERE first_name LIKE 'A%n'; -- A ile başlayıp n ile biten isimleri listeler.
WHERE first_name LIKE '%g%'; -- İçerisinde g harfi bulunan isimleri listeler. Ancak baş harfi büyük G harfi olanları da listelemesini istersel ILIKE kullanmalıyız.
WHERE first_name LIKE 'J_'; -- Sadece 2 harfli ve ilk harfi J olan isimleri listeler.
```
Şeklinde örneklendirebiliriz.
## DISTINCT ve COUNT
### DISTINCT
Şimdiye kadar yaptığımız SQL sorgularında genellikle verileri belirli koşullar altında sıraladık. Bazı sütunlar birbirini tekrar eden verilerden oluşmaktadır. Bazı durumlarda bir sütun içerisinde bulunan farklı değerleri görmek isteriz. Bu durumda **DISTINCT** kullanırız.
#### DISTINCT Söz Dizimi
``` sql
SELECT DISTINCT <sütun_adı>, <sütun_adı>, ...
FROM <tablo_adı>;
```
Örnek olarak bir **car** tablomuz olduğunu ve bunun içinde **engine** sütununda bulunan birbirinden farklı kaç motor seçeneği olduğunu ve bunların ne olduğunu görmek isteyelim.
``` sql
SELECT DISTINCT engine
FROM car
```
Örnek Çıktı: 
| | engine |
| :---: | :---: |
| 1 | 1.0 |
| 2 | 1.3 |
| 3 | 1.4 |
## COUNT
**COUNT** **aggregate** (Toplama, Bütünleme) fonksiyonu ilgili sorgu sonucunda oluşan veri sayısını bildirir.
``` sql
SELECT COUNT(*)
FROM actor
WHERE first_name = 'Penelope';
```
COUNT(*) veya COUNT(sütun_adı) aynı sonucu verir. \
Bu sorguda adı Penelope olana kişileri listelemiyoruz, onun yerine adı Penelope olan kişilerin sayısını istiyoruz. Örneğin sonuç 4 olsun o halde çıktımız şu şekilde olacak:
| | count |
| :---: | :---: |
| 1 | 4 |

DISTINCT ve COUNT ifadelerini birlikte de kullanabiliriz.
``` sql
SELECT COUNT(DISTINCT first_name) FROM actor;
```
Bu bize **actor** tablosunda **first_name**'i birbirimnden farklı kaç aktör olduğunun sayısını verecektir.
``` sql
SELECT first_name, COUNT(*) AS ActorCount FROM actor GROUP BY first_name
```
Bu sorguda [GROUP BY](https://github.com/GrkmAyarkan/NOTLAR/blob/main/SQL.md#group-by) ile **first_name** sütunundaki birbiri ile aynı olana değerleri gruplarız. Bu grupları **SELECT first_name** sorgusu ile yazdırırız ve **SELECT COUNT(*) AS ActorCount** sorgusu ile yanlarına bu isimde kaç aktör olduğu bilgisini **ActorCount** sütunu altında yazdırırız. Sütunun adını belirleyen kısım ise [AS (ALIAS)](). \
Örnek çıktımız şu şekilde olur: 
| | first_name | ActorCount |
| :---: | :---: | :---: |
| 1 | Christian | 3 |
| 2 | Kenneth | 4 |
| 3 | Cameron | 3 |
| 4 | Mary | 2 |
| 5 | Jada | 1 |
| 6 | Christopher | 3 |

## PSQL 1
PSQL, PostgreSQL ile birlikte gelen terminal tabanlı bir kullanıcı arayüzüdür. PSQL sayesinde komut satırında sorgular yazıp, sonuçlarını görebiliriz. Aşağıda temel PSQL komutlarının ilk bölümünü bulabilirsiniz.
* PSQL ile PostgreSQL'e bağlanmak.
```
psql -U <kullanıcı_adı> -- otomatik gelen kullanıcı adı "postgres" olabilir. 
```
* Kullanıcıya ait şifreyi girdikten sonra varsayılan veritabanı postgres'e bağlanıyor.
```
postgres=#
```
* Bulunan veritabanlarını listelemek için:
```
\l veya \list
```
* Bizim örneğimizde dvdrental veritabanına bağlanacağız.
```
\c dvdrental veya \connect dvdrental
```
* Bağlanılan dvdrental veritabanında bulunan tabloları listelemek için:
```
\dt
```
* Herhangi bir tablonun sütunlarını ve tablo detaylarını görmek için:
```
\d <tablo_adı>
```
PSQL terminal ekranından çıkmak için:
```
\q
```
## ORDER BY
**ORDER BY** anahtar kelimesi sayesinde bizler verilerimizi herhangi bir sütunda bulunan değerlere göre azalan veya artan bir şekilde sıralayabiliriz.
#### ORDER BY Söz Dizimi
``` sql
SELECT <sütun_adı>, <sütun_adı>, ...
FROM <tablo_adı>
ORDER BY <sütun_adı>, <sütun_adı>, ... ASC|DESC;
```
#### ORDER BY Örnek Kullanım
``` sql
SELECT *
FROM film
ORDER BY title ASC;
```
Bu sorgumuzda dvdrental veritabanında bulunan film tablosundaki tüm sütunları title sütununda bulunan verilere göre artan (ASC) şeklinde sıralıyoruz. \
ASC sıralama varsayılan olduğu için ayrı bir şekilde yazılması zorunluluğu yoktur ancak sorguyu belirginleştirmesi açısından genelde yazılır.
``` sql
SELECT *
FROM film
ORDER BY title ASC, length DESC;
```
Sıralama birden fazla sütuna göre de yapılabilir. Yukarıdaki örneğimizde sıralama title sütununa göre artan length sütununa göre azalan şeklinde yapılıyor. \
**ASC -> ARTAN** \
**DESC -> AZALAN**
``` sql
SELECT *
FROM film
WHERE title LIKE 'A%'
ORDER BY title ASC, length DESC;
```
Sıralama işlemi, koşuldan sonra yazılır.

## LIMIT ve OFFSET
### LIMIT
Belirli koşulları sağlayan tüm verileri değil de belirli sayıda veriyi istediğimizde LIMIT anahtar kelimesini kullanırız.
#### Söz Dizimi
``` sql
SELECT <sütun_adı>, <sütun_adı>, ...
FROM <tablo_adı>
ORDER BY <sütun_adı>, <sütun_adı>, ... ASC|DESC
LIMIT <sayı>;
```
#### Örnek Senaryo
Uzunluğu yüksekten düşüğe doğru sıralanmış ve baş harfi 'B' ile başlayan ilk 10 filmin film_id, title, rental_rate, length bilgilerini listeleyelim.
``` sql
SELECT film_id, title, rental_rate, length
FROM film
WHERE title LIKE 'B%'
ORDER BY length DESC
LIMIT 10;
```
### OFFSET
Bazı durumlarda sonuç olarak gördüğümüz veri grubu içerisinden bazılarını "pass" geçmek isteriz. Yukarıdaki senaryomuzu tekrar düşünelim, Uzunluğu yüksekten düşüğe doğru sıralanmış ve baş harfi 'B' ile başlayan filmlerin film_id, title, rental_rate, length bilgilerini listeleyelim ancak en uzun 6 filmi "pass" geçelim ve sonrasındaki 4 filmi sıralayalım..
``` sql
SELECT film_id, title, rental_rate, length
FROM film
WHERE title LIKE 'B%'
ORDER BY length DESC
OFFSET 6
LIMIT 4;
```

## Aggregate Fonksiyonlar - MIN, MAX, SUM, AVG
Aggregate fonksiyonları yardımıyla bizler veri kümelerimizden sonuçlar çıkarabiliriz. Belirli veri kümelerinden tek bir sonuç çıkarmak için aggregate fonksiyonları kullanırız.
#### Örnekler
#### AVG
**AVG** sütundaki sayısal değerlerin **ORTALAMA**SINI almamızı sağlar.
``` sql
SELECT AVG(length) 
FROM film;
```
#### SUM
**SUM** sütundaki sayısal değerlerin **TOPLAM**ını almamızı sağlar.
``` sql
SELECT SUM(length) 
FROM film;
```
#### MAX
**MAX** sütundaki değerler arasındaki **EN YÜKSEK DEĞER**İ almamızı sağlar.
``` sql
SELECT MAX(length) 
FROM film;
```
#### MIN
**MIN** sütundaki değerler arasındaki **EN DÜŞÜK DEĞER**İ almamızı sağlar.
``` sql
SELECT MIN(length) 
FROM film;
```

## GROUP BY
Verileri gruplama için **GROUP BY** anahtar kelimesi kullanılır.
#### GROUP BY Söz Dizimi
``` sql
SELECT <sütun_adı>, <sütun_adı>, ... (veya aggregate func) FROM <tablo_adı>
GROUP BY <sütun_adı>, <sütun_adı>, ...
```
Burada şuna dikkat etmemiz gerekir, SELECT anahtar kelimesinde bulunan sütunların GROUP BY anahtar kelimesi içerisinde bulunması gerekir. \
#### Örnek
**Film** tablosunda **rental_rate** sütununda bizim 3 farklı değerimiz var **(0.99, 2.99, 4.99)**. Biz bu 3 farklı değer için **en uzun** filmi bulmaya çalışalım. \
Öncelikle GROUP BY olmadan nasıl yapabileceğimize bakalım.
``` sql
SELECT MAX(length)
FROM film
WHERE rental_rate = 0.99;
```
Bu şekilde her biri için teker teker sorgu yapmalıyız. \
Şimdi GROUP BY ile nasıl yapabileceğimize bakalım. 
``` sql
SELECT rental_rate, MAX(length)
FROM film
GROUP BY rental_rate;
```
Bu şekilde her bir değeri ve karşılığında gelen en yüksek uzunluk değerini tablo şeklinde görebiliriz. \
Örnek çıktımız:
| rental_rate | max |
| :---: | :---: |
|2.99|185|
|4.99|185|
|0.99|184|

## HAVING
HAVING anahtar kelimesi sayesinde gruplandırılmış verilere koşullar ekleyebiliriz.
#### Örnek Kullanım:
Her bir rental_rate oranına karşılık gelen film sayısını bulalım ve toplam film sayısı 325 ten fazla olan rental_rate oranlarını görelim. \
Bu durumda GROUP BY ile elde ettiğimiz toplam film sayılarına koşul eklememiz gerekir.
``` sql
SELECT rental_rate, COUNT(*)
FROM film
GROUP BY rental_rate HAVING COUNT(*) > 325;
```








.
