# SQL
### İçindekiler
* [SQL Nedir?](https://github.com/GrkmAyarkan/NOTLAR/blob/main/SQL.md#sql-structured-query-language-nedir)
* [Veri ve Veritabanı](https://github.com/GrkmAyarkan/NOTLAR/blob/main/SQL.md#veri-ve-veritaban%C4%B1)

## SQL (Structured Query Language) Nedir?
SQL Türkçe ifadesiyle yapılandırılmış sorgu dili anlamına gelmektedir. Biz SQL sayesinde verilerimizin bulunduğu veritabanı ile iletişime geçeriz. \
SQL bir programlama dili midir? Evet, SQL ilişkisel veritabanı yönetim sistemleri ile ilişki kurmamızı sağlayan bir declarative bildirimsel bir programlama dilidir.
### Bildirimsel Yaklaşım
``` sql
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










