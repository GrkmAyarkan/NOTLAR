# **MARKDOWN ÖZELLİKLERİ**
## Başlıklar
Başlık oluşturmak içim satır başına "#" işareti koyulur.\
Yazılış şekilleri:
````
# Başlık 1
## Başlık 2
### Başlık 3
#### Başlık 4
##### Başlık 5
###### Başlık 6
````
### **Çıktı**
# Başlık 1
## Başlık 2
### Başlık 3
#### Başlık 4
##### Başlık 5
###### Başlık 6

## Kalın ve Eğik Yazmak 
Yazılış Şekli:
````
*Eğik*
**Kalın**
***Eğik Hem Kalın***
````
### **Çıktı**
*Eğik*\
**Kalın**\
***Eğik ve Kalın***

## Kod Satırı
Kodun bir üst ve bir alt satırına üç veya 4 adet backtick (```) karakteri eklenir.
Yazılış şekli:
````
```
System.out.println("Hello, World!");
```
````
### **Çıktı**
```
System.out.println("Hello, World!");
```
Yazılım diline göre kod bloğundaki ifadelerin stillendirilmesini isterseniz, kod bloğunun başındaki 3 adet backtick ifadesinden sonra java, javascript, python, css gibi etiket ekleybilirsiniz.
### **Çıktı**
``` java
if (90 > 28) {
  System.out.println("90 sayısı 28'den büyüktür");
}
```

## Listeler
Liste oluşturmak için - ve * karakterleri kullanılır.
Yazılış Şekli:
```
- Satır 1
- Satır 2
- Satır 3

* Satır 1
* Satır 2
* Satır 3
```
### **Çıktı**
- Satır 1
- Satır 2
- Satır 3

* Satır 1
* Satır 2
* Satır 3

## Tablolar
Tablo oluşturmak için aşağıdaki yapı kullanılır. Satır çizgisi için kullanılan - karaterine, : işareti eklenerek tabloda sola, sağa veya ortaya hizalama yapılabilir.
```
| Numaralar| İsimler| Açıklamalar|
| :--- | :---: | ---: |
| 1 | İsim 1 | Açıklama 1 |
| 2 | İsim 2 | Açıklama 2 |
| 3 | İsim 3 | Açıklama 3 |
```
### **Çıktı**
| Numaralar| İsimler| Açıklamalar|
| 1 | İsim 1 | Açıklama 1 |
| 2 | İsim 2 | Açıklama 2 |
| 3 | İsim 3 | Açıklama 3 |
