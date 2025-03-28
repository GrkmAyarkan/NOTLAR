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
* [ALIAS (AS) (Tablo İsimlendirme)](https://github.com/GrkmAyarkan/NOTLAR/blob/main/SQL.md#alias-as)
* [CREATE - DROP (Tablo Oluşturma ve Silme)](https://github.com/GrkmAyarkan/NOTLAR/blob/main/SQL.md#create---drop-tablo-olu%C5%9Fturma-ve-silme)
* [INSERT INTO (Veri Ekleme)](https://github.com/GrkmAyarkan/NOTLAR/blob/main/SQL.md#insert-into-veri-ekleme)
* [UPDATE - DELETE (Tablo Verilerini Güncellemek - Silmek)](https://github.com/GrkmAyarkan/NOTLAR/blob/main/SQL.md#update---delete-tablo-verilerini-g%C3%BCncellemek---silmek)
* [PRIMARY KEY - FOREIGN KEY](https://github.com/GrkmAyarkan/NOTLAR/blob/main/SQL.md#primary-key---foreign-key)

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
### COUNT
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
Bu sorguda [GROUP BY](https://github.com/GrkmAyarkan/NOTLAR/blob/main/SQL.md#group-by) ile **first_name** sütunundaki birbiri ile aynı olana değerleri gruplarız. Bu grupları **SELECT first_name** sorgusu ile yazdırırız ve **SELECT COUNT(*) AS ActorCount** sorgusu ile yanlarına bu isimde kaç aktör olduğu bilgisini **ActorCount** sütunu altında yazdırırız. Sütunun adını belirleyen kısım ise [AS (ALIAS)](https://github.com/GrkmAyarkan/NOTLAR/blob/main/SQL.md#alias-as). \
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

## ALIAS (AS)
AS anahtar kelimesi sayesinde sorgular sonucu oluşturduğumuz sanal tablo ve sütunlara geçici isimler verebiliriz.
#### ALIAS Sütun Kullanımı
``` sql
SELECT <sütun_adı> AS <geçici_ad>
FROM <tablo_adı>;
```
#### ALIAS Tablo Kullanımı
``` sql
SELECT <sütun_adı>, <sütun_adı>...
FROM <tablo_adı> AS <geçici_ad>;
```

## CREATE - DROP (Tablo Oluşturma ve Silme)
### CREATE - Tablo Oluşturma
SQL ile yeni bir tablo oluşturmak için CREATE anahtar kelimesi kullanılır. 
#### Tablo Oluşturmak - CREATE Söz Dizimi:
``` sql
CREATE TABLE <tablo_adı> (
    <sütun_adı> <veri_tip> (kısıtlama_adı>,
    <sütun_adı> <veri_tip> (kısıtlama_adı>,
   ....
);
```
#### Tablo Oluşturmak - CREATE Örnek Kullanım
**author** isminde bir tablo oluşturalım, **id**, **first_name**, **last_name**, **email**, **birthday** sütunları olsun.
``` sql
CREATE TABLE author (
  id SERIAL PRIMARY KEY,
  first_name VARCHAR(50) NOT NULL,
  last_name VARCHAR(50) NOT NULL,
  email VARCHAR(100)
  birthday DATE
);
```
### DROP - Tablo Silmek
Oluşturduğumuz tabloları silmek için DROP anahtar kelimesi kullanılır.
#### Tablo Silmek - DROP Söz Dizimi:
``` sql
DROP TABLE (IF EXISTS) <tablo_adı>;
```
Burada **IF EXISTS** yapısını kullanarak yanlış tablo ismi yazımı durumunda hata mesajı almayı önleriz.
#### Tablo Silmek - DROP Örnek Kullanım
"test" isimli tablomuzu silmek istersek;
``` sql
DROP TABLE IF EXISTS test;
```

## INSERT INTO (Veri Ekleme)
Bir tabloya veri eklemek için INSERT INTO komutunu kullanırız.
#### INSERT INTO Söz Dizimi
``` sql
INSERT INTO <tablo adı> (column1, column2, column3, ...)
VALUES (value1, value2, value3, ...);
```
#### Örnek Tablo
| | id | name | price |
| :---: | :---: | :---: | :---: |
| 1 | 1 | Baldur's Gate 3 | $34.99 |
| 2 | 2 | Mount & Blade II: Bannerlord | $19.99 |
| 3 | 3 | EA Sports FC 24 | $69.99 |
| 4 | 4 | Cyberpunk 2077 | $44.99 |
| 5 | 5 | The Last of Us Part I | $59.99 |

#### Örnek Ekleme İşlemi
``` sql
INSERT INTO games (id, name, price)
VALUES (6, 'The Witcher 3', $29.99);
```
#### Sonuç Tablosu
| | id | name | price |
| :---: | :---: | :---: | :---: |
| 1 | 1 | Baldur's Gate 3 | $34.99 |
| 2 | 2 | Mount & Blade II: Bannerlord | $19.99 |
| 3 | 3 | EA Sports FC 24 | $69.99 |
| 4 | 4 | Cyberpunk 2077 | $44.99 |
| 5 | 5 | The Last of Us Part I | $59.99 |
| 6 | 6 | The Witcher 3 | $29.99 |

## UPDATE - DELETE (Tablo Verilerini Güncellemek - Silmek)
Örnek bir tablo oluşturalım.
``` sql
CREATE TABLE games (
	id INT,
	name VARCHAR(50),
	price VARCHAR(50)
);
INSERT INTO games (id, name, price) VALUES (1, 'Baldur's Gate 3', '$34.99');
INSERT INTO games (id, name, price) VALUES (2, 'Mount & Blade II: Bannerlord', '$19.99');
INSERT INTO games (id, name, price) VALUES (3, 'EA Sports FC 24', '$69.99');
INSERT INTO games (id, name, price) VALUES (4, 'Cyberpunk 2077', '$44.99');
INSERT INTO games (id, name, price) VALUES (5, 'The Last of Us Part I', '$59.99');
```
#### Tablo
| | id | name | price |
| :---: | :---: | :---: | :---: |
| 1 | 1 | Baldur's Gate 3 | $34.99 |
| 2 | 2 | Mount & Blade II: Bannerlord | $19.99 |
| 3 | 3 | EA Sports FC 24 | $69.99 |
| 4 | 4 | Cyberpunk 2077 | $44.99 |
| 5 | 5 | The Last of Us Part I | $59.99 |
### UPDATE - Veri Güncelleme
UPDATE anahtar kelimesi sayesinde tablomuzda bulunan verileri güncelleyebiliriz.
#### UPDATE Söz Dizimi:
``` sql
UPDATE <tablo_adı>
SET <sütun_adı> = değer, 
    <sütun_adı> = değer,
    ----
WHERE <koşul_adı>;
```
UPDATE Örnek Kullanım
games tablosunda bulunan ve **id** 3' ye eşit olan verimizin **name** sütunundaki degerini 'Cities: Skylines II' **price** sütunundaki değerini '$49.99' ile değiştirelim.
``` sql
UPDATE games
SET name = 'Cities: Skylines II',
    price = '$49.99'
WHERE id = 3
RETURNING *;
```
#### Çıktı
| | id | name | price |
| :---: | :---: | :---: | :---: |
| 1 | 3 | Cities: Skylines II | $49.99 |

Burada **RETURNING** anahtar kelimesi ile * kullanarak değişiklik yapılan veri satırının tamamını yazdırırız. RETURNING kullanılmazsa program bize sadece değişiklik yapıldığını bildirir ancak bir çıktı vermez.
#### Yeni Tablo
| | id | name | price |
| :---: | :---: | :---: | :---: |
| 1 | 1 | Baldur's Gate 3 | $34.99 |
| 2 | 2 | Mount & Blade II: Bannerlord | $19.99 |
| 3 | 4 | Cyberpunk 2077 | $44.99 |
| 4 | 5 | The Last of Us Part I | $59.99 |
| 5 | 3 | Cities: Skylines II | $49.99 |

En son üzerinde işlem yapılan veriyi tablonun en sonunda gönderir.
### DELETE - Veri Silme
DELETE anahtar kelimesi sayesinde tablomuzda bulunan verileri silebiliriz.
#### DELETE Söz Dizimi:
``` sql
DELETE FROM <tablo_adı>
WHERE <koşul_adı>;
```
#### DELETE Örnek Kullanım
games tablosunda bulunan **name** sütunundaki verisi 'Cyberpunk 2077' olan satırı silelim.
``` sql
DELETE FROM games
WHERE name = 'Cyberpunk 2077'
RETURNING *;
```
Silme işleminde de **RETURNING** kullanabiliriz. Burada silinen veri satırlarını yazdırır.
#### Çıktı
| | id | name | price |
| :---: | :---: | :---: | :---: |
| 1 | 4 | Cyberpunk 2077 | $44.99 |
#### Yeni Tablo
| | id | name | price |
| :---: | :---: | :---: | :---: |
| 1 | 1 | Baldur's Gate 3 | $34.99 |
| 2 | 2 | Mount & Blade II: Bannerlord | $19.99 |
| 3 | 5 | The Last of Us Part I | $59.99 |
| 4 | 3 | Cities: Skylines II | $49.99 |

Bir veri silindiğinde onun **id**'si silinir ama geri kalan verilerin id'lerinde bir değişiklik olmaz.

## PRIMARY KEY - FOREIGN KEY
#### **games** Tablosu
| | game_id | name | price | pub_id |
| :---: | :---: | :---: | :---: | :---: |
| 1 | game001 | Baldur's Gate 3 | $34.99 | pub003 |
| 2 | game002 | Mount & Blade II: Bannerlord | $19.99 | pub005 |
| 3 | game003 | EA Sports FC 24 | $69.99 | pub002 |
| 4 | game004 | Cyberpunk 2077 | $44.99 | pub001 |
| 5 | game005 | The Last of Us Part I | $59.99 | pub004 |
| 6 | game006 | God of War (2018) | $49.99 | pub004 |
#### **publishers** Tablosu
| | pub_id | name | founding_year |
| :---: | :---: | :---: | :---: |
| 1 | pub001 | CD Projekt | 1994 |
| 2 | pub002 | Electronic Arts (EA) | 1982 |
| 3 | pub003 | Larian Studios | 1996 |
| 4 | pub004 | Sony Interactive Entertainment | 1993 |
| 5 | pub005 | TaleWorlds Entertainment | 2005 |
| 6 | pub006 | Paradox Interactive | 1999 |
### PRIMARY KEY
PRIMARY KEY bir tabloda bulunan veri sıralarını birbirinden ayırmamızı sağlayan bir kısıtlama (constraint) yapısıdır. O tabloda bulunan veri sıralarına ait bir "benzersiz tanımlayıcıdır".
#### Şartları:
* Benzersiz (Unique) Olmalıdır.
* NULL değerde olamaz.
* Bir tabloda en fazla 1 tane bulunabilir.

Yukarıdaki **games** tablosundaki **game_id** ve **publishers** tablosundaki **pub_id**, **PRIMARY KEY**'dir. Her bir veriyi diğerlerinden ayırmamızı sağlar.
### FOREIGN KEY
FOREIGN KEY bir tabloda bulunan herhangi bir sütundaki verilerin genelde başka bir tablo sütununa referans vermesi durumudur, tablolar arası ilişki kurulmasını sağlar.
* Bir tabloda birden fazla sütun FK olarak tanımlanabilir.
* Aynı sütunun içerisinde aynı değerler bulunabilir.

Yukarıda bulunan tablolarda da gördüğünüz gibi **games** tablosunda bulunan **pub_id** sütunu FOREIGN KEY yapısındadır ve başka bir tablo olan **publishers** tablosundaki **pub_id** sütununa referans verir.


.
