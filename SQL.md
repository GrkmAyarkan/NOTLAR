# SQL
### İçindekiler
* [SQL Nedir?](https://github.com/GrkmAyarkan/NOTLAR/blob/main/SQL.md#sql-structured-query-language-nedir)
* [Veri ve Veritabanı](https://github.com/GrkmAyarkan/NOTLAR/blob/main/SQL.md#veri-ve-veritaban%C4%B1)
* [Veritabanı Yönetim Sistemi (DBMS)](https://github.com/GrkmAyarkan/NOTLAR/blob/main/SQL.md#veritaban%C4%B1-y%C3%B6netim-sistemi-dbms)
* [SELECT (Seçim Yapmak)](https://github.com/GrkmAyarkan/NOTLAR/blob/main/SQL.md#select)
* [WHERE (Koşul Ekleme)](https://github.com/GrkmAyarkan/NOTLAR/blob/main/SQL.md#where-ve-kar%C5%9F%C4%B1la%C5%9Ft%C4%B1rma-operat%C3%B6rleri)
* [BETWEEN ve IN]()

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



































.
