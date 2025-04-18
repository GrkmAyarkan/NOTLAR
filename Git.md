# **GIT**
İçindekiler;
* [git init (Git Deposu Oluşturma)](https://github.com/GrkmAyarkan/NOTLAR/blob/main/Git.md#git-init)
* [git config (Yapılandırma ve Yönetme)](https://github.com/GrkmAyarkan/NOTLAR/blob/main/Git.md#git-config)
* [git add (Değişiklikleri Ekleme)](https://github.com/GrkmAyarkan/NOTLAR/blob/main/Git.md#git-add)
* [git rm (Takibi Bırakma veya Silme)](https://github.com/GrkmAyarkan/NOTLAR/blob/main/Git.md#git-rm)
* [git status (Durum Bilgisi Alma)](https://github.com/GrkmAyarkan/NOTLAR/blob/main/Git.md#git-status)
* [git commit (Local Repo.’e Gönderme)](https://github.com/GrkmAyarkan/NOTLAR/blob/main/Git.md#git-commit)
* [git log (Commit Geçmişi)](https://github.com/GrkmAyarkan/NOTLAR/blob/main/Git.md#git-log)
* [git branch (dal) (Eklemek, Silmek, Listelemek)](https://github.com/GrkmAyarkan/NOTLAR/blob/main/Git.md#git-branch)
* [git checkout (Dal veya Commit'e Geçiş)](https://github.com/GrkmAyarkan/NOTLAR/blob/main/Git.md#git-checkout)
* [git merge (Dalları Birleştirme)](https://github.com/GrkmAyarkan/NOTLAR/blob/main/Git.md#git-merge)
* [git clone (Repo. Kopyalama)](https://github.com/GrkmAyarkan/NOTLAR/blob/main/Git.md#git-clone)
* [git push (Değişiklikleri Gönderme)](https://github.com/GrkmAyarkan/NOTLAR/blob/main/Git.md#git-push)
* [git pull (Değişiklikleri İndirme, Birleştirme)](https://github.com/GrkmAyarkan/NOTLAR/blob/main/Git.md#git-pull)
* [git diff (Versiyon Farkı)](https://github.com/GrkmAyarkan/NOTLAR/blob/main/Git.md#git-diff)
* [.gitignore](https://github.com/GrkmAyarkan/NOTLAR/blob/main/Git.md#gitignore)
  - [Nasıl Oluşturulur?](https://github.com/GrkmAyarkan/NOTLAR/blob/main/Git.md#nas%C4%B1l-olu%C5%9Fturulur)
  - [Nasıl çalışır, nasıl kullanılmalı?](https://github.com/GrkmAyarkan/NOTLAR/blob/main/Git.md#nas%C4%B1l-%C3%A7al%C4%B1%C5%9F%C4%B1r-nas%C4%B1l-kullan%C4%B1lmal%C4%B1)
  - [Neye dikkat etmeliyim?](https://github.com/GrkmAyarkan/NOTLAR/blob/main/Git.md#neye-dikkat-etmeliyim)
* [Ekstralar](https://github.com/GrkmAyarkan/NOTLAR/blob/main/Git.md#ekstralar)
  - [Yapılan commit üzerinde değişiklik yapmak](https://github.com/GrkmAyarkan/NOTLAR/blob/main/Git.md#yap%C4%B1lan-commit-%C3%BCzerinde-de%C4%9Fi%C5%9Fiklik-yapmak)
  - [Branch İşlemleri ve Stash Kavramı](https://github.com/GrkmAyarkan/NOTLAR/blob/main/Git.md#branch-i%CC%87%C5%9Flemleri-ve-stash-kavram%C4%B1)
  - [Merge, Rebase, Confict](https://github.com/GrkmAyarkan/NOTLAR/blob/main/Git.md#merge-rebase-confict)
## **git init**
Henüz versiyon kontrolü altında olmayan bir projenin dizininde, boş bir git deposu oluşturmak için kullanılır.
* untracked (izlenmeyen): GIT tarafından henüz takip edilmeyen, yani yeni oluşturulmuş dosyaları ifade eder.
* unstaged (hazırlanmamış): Güncellenmiş ancak commit’lenmek için hazırlanmamış dosyaları ifade eder.
* staged (hazırlanmış): Commit’lenmeye hazır olan dosyaları ifade eder.
* deleted (silinmiş): Projeden silinmiş ama GIT üzerinden kaldırılmamış dosyaları ifade eder.

## **git config**
GIT’in bir çok konfigürasyon ve ayarı vardır, bunlardan ikisi user.name ve user.email olanıdır. Bu ayarları yapılandırmak için aşağıdaki komutları kullanırız. Ayrıca bu ayarlar global yani sistem genelinde geçerli ayarlardır. Proje bazlı bu ayarlar değiştirilebilir.
```
$ git config --global user.name "Name Surname"
$ git config --global user.email "test@email.com"
```
Bu ayarların bütününü görüntülemek için:
```
$ git config --list
```
Not: Eğer windows işletim sistemi kullanıyorsanız, böyle bir hata ile karşılaşabilirsiniz.
```
warning: LF will be replaced by CRLF in kaynak/dosya/yolu
```
Bu hatanın çözümü için aşağıdaki komutu kullanabilirsiniz.
````
$ git config core.autocrlf true
````

## **git add**
Yeni eklenen veya üzerinde değişiklik yapılan dosyaları **staged** ortamına göndermek için kullanılır. **staged** (hazırlanmış): Commit’lenmeye hazır olan dosyaları ifade eder.
````
$ git add <dosya veya klasör_adı>
````
Tek seferde bütün dosyaları eklemek için ise:
````
$ git add .  veya  $ git add *  veya   $ git add -A .
````
Buradaki **-A** (all) tümü anlamındadır. **.** ise tüm dosya uzantılarını ifade eder.

## **git rm**
Staged ortamına eklenmiş bir dosyanın takibinin bırakılması yani **untracked** (izlenmeyen) hale getirilmesi sağlayan komuttur. **untracked** (izlenmeyen): GIT tarafından takip edilmeyen, genelde yeni oluşturulmuş dosyaları ifade eder.
````
$ git rm  --cached <dosya veya klasor_name>
````
Dosyayı klasörden silmek istiyorsak eğer, aşağıdaki komutu kullanılırız.
````
$ git rm <dosya veya klasor_name>
````

## **git status**
Üzerinde çalışılan projenin o anki durumu hakkında bilgi verir. Yapılan değişiklikler, eklenen ve silinen dosyalar gibi bilgiler listelenir.
* On branch main -> Main branch'ınde olduğumuzu,
* Changes to be commited -> Commit'lenmeye hazır değişiklikler olduğunu,
* Modified: index.html -> Index.html dosyasında değişiklik yaptığımızı,
* Deleted: styles.css -> styles.css dosyasını sildiğimizi,
* Changes not staged for commit -> Üzerinde değişiklik yapılan ama staged ortamına gönderilmemiş dosyaları ifade eder.
* Untracked files -> takibi yapılmayan dosyaları ifade eder.

## **git commit**
Commit, **staged** ortamına alınan dosyaların Local Repository’e gönderilmesidir. Her commit benzersiz bir kimliğe (**unique ID**) sahip olur. Bu sayede eski bir commit'e geri dönebilirsiniz.
````
$ git commit -m "ilk commit mesajı"
````
Buradaki **-m** (message) mesaj anlamındadır ve commit sırasında yapılan değişikliği açıklamak için kullanılır. 

## **git log**
Projedeki commit geçmişini görüntülememizi sağlar. Bütün commit'ler, id'si, yazarı, tarihi ve mesajı ile beraber listelenir.

## **git branch**

Local veya remote repository üzerinde yeni bir **branch** (dal) eklemek, silmek veya listelemek için kullanılır.\
Projenize yeni bir branch eklemek için;
````
$ git branch <branch_name>
````
Tüm uzak ve yerel branch'lari listelemek için;
````
$ git branch -a
````
Bir branch'ı silmek için;
````
$ git branch -d <branch_name>
````

## **git checkout** 
Branch’ler arası veya commit'ler arası geçiş yapmak istediğimizde kullanılır. \
Mevcutta var olan branch'a geçiş yapmak için;
````
$ git checkout <branch_name>
````
Yeni bir branch oluşturup, bu branch'a geçiş yapmak için;
````
$ git checkout -b <branch_name>
````
Commitler arası geçiş yapmak için: (Eski bir versiyona dönmek istediğimiz zaman)
````
$ git checkout <commit_ID>
````

## **git merge** 
Başka bir branch'da olan değişiklikleri, bulunduğumuz branch ile birleştirmek istediğimizde kullanılır.
````
$ git merge <branch_name>
````

## **git clone** 
Mevcut bir Remote Repository'de bulunan dosyaların bilgisayarımızda bir kopyasının oluşturulmasını sağlar.
````
$ git clone <remote_URL>
````

## **git push**
Projemizde aldığımız commit'leri, remote repository'e gönderir.
````
$ git push origin master
````
Burada bahsi geçen **origin**, **remote repository**’nin kök dizinini belirtir ve sabit bir isimdir. **master** ise sizin çalıştığınız **branch** (dal)’ı belirtir.\
Henüz remote repository’niz yoksa aşağıdaki komut ile local deponuzu uzak sunucudaki depoya bağlayabilirsiniz.
````
$ git remote add origin http://uzak_deponun_adresi.git
````

## **git pull**
**git pull** aslında iki ayrı Git komutunun birleşimidir:
````
1. git fetch
````
Uzak depodaki değişiklikleri yerel bilgisayara indirir (ör. yeni commit'ler, dallar veya güncellemeler). Ancak bu değişiklikleri yerel çalışma diziniyle birleştirmez. Eğer doğrudan uzak branch'in son halini almak istiyorsanız (yerel branch'te birleştirme yapmak yerine), birleştirme işlemi yapmadan sadece değişiklikleri indirebilirsiniz.
````
2. git merge
````
İndirilen değişiklikleri, aktif olan yerel branch (dal) ile birleştirir.
### Kullanımı:
````
git pull [remote] [branch]
````
**remote** (isteğe bağlı): Uzak depo adı. Varsayılan olarak genelde **origin** kullanılır.
**branch** (isteğe bağlı): Çekmek istedğiniz dal (Ör. **main** veya **master**). Eğer bir dal adı verilmezse, mevcut branch'le ilişkili olan uzak branch çekilir.\
1. Varsayılan Remote ve Branch ile çekme:
````
git pull
````
2. Belirli bir Remote ve Branch ile çekme:
````
git pull origin main
```` 

## **git diff**
Repository üzerinde yapılan değişikliklerden sonra dosyalar arasında oluşan farklılıkları gösterir.\
Çalışma dizini ile repository (HEAD) arasındaki farklılıkları görmek için:
````
$ git diff HEAD
````
İki commit arasındaki farklılıkları görmek için:
````
$ git diff <commit_id_1>..<commit_id_2>
````
Çalışma dizini ve staged ortamı arasındaki farkları görmek için:
````
$ git diff --staged
````

# **.gitignore** 
 .gitignore dosyası projemizin kök dizinine oluşturulan düz bir metin dosyasıdır. Adından anlaşıldığı gibi diyor ki beni göz ardı et. Daha doğrusu göz ardı etmek istediğin, local çalışma alanındaki takip edilmesini istemediğin, takım arkadaşların için gerekmeyen dosyaların varsa veya bu dosyaların boyutu reponuza atmanıza gerek olmayacak kadar büyük ölçekli ise buyur beni kullan diyor.

Bu dosyaları .gitignore dosyasına koy ki GIT de senin bu dosyalarını artık takip etmesin. Üstelik bu işlemler yapılırken senin halihazırdaki dosyalarını da hiç bir şekilde etkilemesin.
## **Nasıl oluşturulur?**
Reponuzu oluştururken verilen seçeneklerde add gitignore file dosyasına tıklayarak reponuzla beraber oluşturabilirsiniz. Aynı şekilde editörünüzde .gitignore şeklinde de oluşturabilirsiniz.
### Terminal İçin
Windows;
````
$ echo some-text or nothing > .gitignore
````
Buradaki some-text or nothing kısmı .gitignore dosyasına yazılmasını istediğiniz metini ekler. Hiçbir şey de yazmayabilirsiniz.\
MacOS/Unix için;
````
$ touch .gitignore
````
## **Nasıl çalışır, nasıl kullanılmalı?**
.gitignore dosyasının her satırına takip edilmesini istemediğimiz dosyaları veya dizinleri yazarak göz ardı edebiliriz.\
Bu dosyaları yazarken bize kolaylık sağlayan bazı formatlar var.\
**.env** dosyası genellikle API anahtarları, veritabanı bağlantı bilgileri, gizli anahtarlar gibi gizli veya hassas bilgilerin saklandığı bir dosyadır. Bu komut **.env** adlı dosyanın Git tarafından izlenmesini ve depolanmasını engeller.
````
.env
````
* Dizinleri ise klasörün sonuna `/` işareti ekleyerek  belirtiriz.
````
node-modules/ dist/ logs/
````
* `*` yıldız karakteriyle ise belirtilen örnekte **.log** uzantısına sahip dosyaların tümünü izlemeyi bırakacaktır.
````
*.log
````
`*` joker karakteri, herhangi bir dosya adı anlamına gelir.\
.log uzantısıyla biten tüm dosyaları hedef alır.

* Bu örnekte ise adı files ile biten tüm dosyaları izlemeyi bırakır.
````
*files/
````
yani bu komuta göre adı **myfiles/**, **logfiles**, **tempfiles** gibi isminin sonun fales ile biten tüm dosyaları hedef alır ve izlemeyi bırakır. **files/** klasörü ile doğrudan eşleşmez.\
Sadece adı **files/** olan dosyayı izlemeyi bırakması için şu komut kullanılır;
````
files/
````
*  Eğer ki bir klasörümüzü içerisindeki bir dosya haricinde izlenmesini istemiyorsak **!** işareti ile bunu sağlayabiliriz. Bu örnekte **files** klasörü içerisindeki **example.txt** haricindeki dosyalar izlenmeyecektir. Files klasörü içerisindeki sadece **example.txt** git akışında görülecektir. Ancak daha önce **files/** ignore işlemi gerçekleştirilmiş ise bu işlem **işe yaramaz**.
````
!files/example.txt
````
* **.gitignore** dosyasında yorum satırı oluşturmak için ise **#** karakteri kullanılır.

## Neye dikkat etmeliyim?

- Eğer projenizi **git add .** veya **git commit** etmişseniz sonrasında  **.gitignore**  dosyasına eklemek istediğiniz dosyayı ekleseniz de bu işlem gerçekleşmeyecektir ve o dosyanız reponuzda hala GIT ile takip edilecektir.
````
bash $ git rm --cached FILENAME
````
Bu komut ile belirttiğiniz dosya (FILENAME), Git'in takip ettiği dosyalar listesinden çıkartılır.\
Belli dosyaları yeni bir projede her seferinde **.gitignore** dosyasına eklemek istemiyorsanız ve Windows kullanıcısı iseniz C:\Users\{myusername}\ adresine giderek .gitignore_global dosyası oluşturup içerisine global olmasını istediğiniz dosyaları ekledikten sonra git bash terminalinizi açarak aşağıdakı komut ile konfigürasyon sağlayabilirsiniz.
````
$ git config --global core.excludesfile "%USERPROFILE%\.gitignore"
````
Dosyanızın doğru çalıştığını kontrol etmek için ise aşağıdaki komutu çalıştırarak aşağıdaki çıktıyı aldığınızda sorunsuz çalıştırabilmişsinizdir. (Aşağıdaki kodu kopyala yapıştır yapmadan önce kullanıcı adını değiştirin.)
````
$ git config --global core.excludesfile
> C:/Users/user-name/.gitignore_global
````

### Kaynaklar
* https://medium.com/fedeveloper/git-bash-ile-komut-komut-versiyonlama-a354efd3063f
* https://www.jrebel.com/blog/git-cheat-sheet
* http://guides.beanstalkapp.com/version-control/common-git-commands.html

# Ekstralar
## Yapılan commit üzerinde değişiklik yapmak.
Son yapılan commit için aşşağıdaki komut ile düzenleme yapılabilir.
````
git commit --amend
````
Eğer bir commit'i tamemen geri almak isterseniz.
````
git revert commitID
````
Komutu ile commit geri alınır ve yerine bu commitin geri alındığına dair bilgi veren yeni bir commit oluşturur. \
Commit ID yi bulmak için [git log](https://github.com/GrkmAyarkan/NOTLAR/blob/main/Git.md#git-log) kullanılır. \
Commit'ler arasındaki farkları görebilmek için:
````
git diff CommitID1..CommitID2 dosyaAdı
````
Eğer tek bir dosya değil de tüm dosyalar için bakmak isterseniz dosya adını kaldırarak komutu `git diff CommitID1..CommitID2` şeklinde kullanabiliriz. \
Eski commitlerden birine dönmek isterseniz: 
````
git reset --hard commitID
````

## Branch İşlemleri ve Stash Kavramı
[Branch](https://github.com/GrkmAyarkan/NOTLAR/blob/main/Git.md#git-branch)'leri listelemek içim:
````
git branch
````
Komutunu kullanırız. Bu bize oluşturulmuş tüm **Branch**'leri listeler ve hangisinin aktif olduğunu belirtir.
````
git branch branchAdı
````
Komutu ile istediğimiz isimde **branch** oluşturuz fakat hala **eski** branch aktif halde olur.
````
git checkout branchAdı
````
Komutu ile istediğimiz branch'e geçiş yapabiliriz. \
Bunu daha kısa yoldan yapmak için;
````
git checkout -b branchAdı
````
Komutunu kullanarak **yeni** bir branch oluşturur ve ona geçiş yapmış oluruz. \
Oluşturulan branch'i silmek için:
````
git branch -D branchAdı
````

Bir dosyada yapılan değişikleri projede kaydetmek istemiyor ama aynı zamanda da bu değişiklikleri saklamak istiyorsak **stash** komutunu kullanırız.
````
git stash
````
Değişiklik projede kaydedilmez ama son commit'te geçici olarak saklanır. 
````
git stash list
````
Komutu ile tüm kaydedilenlerin bir listesini görürüz. \
Listeyi temizlemek için `git stash clear` kullanılır.
Yapılan kayda geri döndemk için 1. yol `git stash pop` kullanabiliriz. Bu bize en son yapılan **stash**'i getirir ve o stash'i siler. \
2. Yol ise `git stash apply stash@{stashNumarası}` şeklinde istediğimiz stash'i belirterek yapılabilir ve o stash listede kalır, 1. yolda olduğu gibi silinmez. StashID'si diyebileceğimiz numarakay `stash list` ile ulaşabiliriz.

## Merge, Rebase, Confict
2 farklı branch üzerinde çalışırken bu branch’lerin birleştirilmesi için yapabileceğimiz 2 farklı yöntem bulunmaktadır. Bunlardan birisi merge diğeri ise rebase. \

Örnek bir senaryoda başta A branch'imiz olsun ve `dosyaA.md` adında bir dosya oluşturmuş olalım. \
Daha sonra biz A branch'indeyken `git checkout -b B` ile B branch'i oluşturup ona geçiş yapalım. Daha sonra bu branch'te `dosyaB.md` adında bir dosya oluşturalım ve üzerinde işlemler yapıp commitler göndermiş olalım. \
Bu durumda B branch'i A dan türetildiği için B tüm dosyaları görebilecek ancak A branch'i `dosyaB.md` yi göremeyecek. \
Bu durumda kullanabileceğimiz ilk yöntem **Merge**'tir. A branch'indeyken;
````
git merge B
````
Komutunu kullanırsak, A branch'i le B yi merge et (birleştir) demiş oluruz ve `dosyaB.md` ve tüm commitler A branch'ine geçmiş olur. \
Bu durumda herhangi bir commit gönderilmemiş olur ve dışarıdan biri commit'leri incelediğinde bu birleştirme işleminin yapıldığını anlayamayabilir. \
Bu durumda;
````
git merge --squash B
````
Komutunu kullanarak git'e bu iki branch'in birleştiğine dair otomatik bir commit gider yapılan değişiklikler birleştirilmiş olur ancak B branch'inin commitleri A'ya geçmez.

İkinci kullanabileceğimiz yöntem ise **Rebase**'tir.
````
git rebase B
````
Merge'in squash olmadan kullanımı ile aynı şekilde sonuç verir.

### Confict
İki farklı branch'te aynı yerde yapılan iki farklı değişiklik olduğunda branchlerin birleştirilmesi esnasında git bize bu değişikliklerin çakıştığına dair bir uyarı verecektir. Bu durumda doğu olan kod bloğuna bizim karar verip diğer kod bloğunu silip tekrardan add ve commit işlemi yaparak bu sorunu hallederiz. \
Bu hatayı alıp tekrar birleşme öncesine dönmek istersek şu komutu kullanabiliriz;
````
git merge --abort
````
