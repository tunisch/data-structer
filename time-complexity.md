# Time Complexity
**Algoritmanın verimli olması için belli kurallar vardır.**
- Örnek: Raflara kitap yerleştirmek.
- Kitapları, gelişigüzel raflara dağıtırsak aradığımız kitabı daha fazla zamanda bulabiliriz. Aslında bu bir worst case'dir. Kitapları filtrelememiz gerekir. Kalın olanları bir rafa, ince olanları bir rafa, küçük boyutta olanları bir rafa koyduğumuz zaman aradığımız şeyi daha rahat bulabiliriz. Algoritma, en kötü senaryoya ne kadar hazırsa, bizi o kadar memnun edebilir.
- Algoritmalar için genellikle sık kullanılan average case'dir. Kitapların bölümüne göre kaç tane olduğunu biliyorsak average case kullanabiliriz. En büyük rafı miktarı fazla olana ayırabiliriz. Input yoksa average zordur!!!!
- Bir diğer senaryomuz ise best case'dir. Beklediğimiz en iyi durum. Kitap örneğine devam edecek olursak, bütün kitapların ayrı raflarda olması, alfabeye göre sıralanması best case olarak ifade edilebilir. Çünkü aradığımızı rahatlıkla bulabiliyoruz.
- Kullanacağımız algoritmayı analiz etmek istiyoruz. Problem ayıı olsa da farklı inputlar için algoritmamız farklı performans senaryoları üretebilir.
- Diyelim ki bir kelimenin anlamını sözlükte arıyorum. Arama için sayfalara tek tek bakıyorum. Burada algoritmam sayfalara tek tek bakmak, input da aradığım kelime.
- Aradığım kelimenin boyutu ayn ıolsa da hangi harfle başladığına göre yapacağım işlem (sayfa çevirme) sayısı değişebilir. Yani input algoritmamın yapacağı işlem sayısını etkileyebiliyor.

**Bu yüzden analizimizi 3 ana başlık altında yapabiliriz: Worst case, average case, best case**

    1) Worst Case: Verecegimiz inputun algoritmamizi en yavaş (en fazla işlem yapacak) şekilde çalıştırdığı durum. Aradığımız kelimenin "z" ile başlaması gibi.
       - Her algoritmaya gore worst case farklı. Sözlüğe baştan değil sondan bakmaya başlasaydım "z" ile başlaması worst case olmazdı.
    2) Average Case: Genel olarak beklediğim durum.
    3) Best Case: Vereceğimiz inputun algoritmamızi en hizl şekilde çalıştırdığı durum.
- Algoritmamızın çalışmasını en iyi yansıtan average case, ama bu durumu analiz etmek diğerlerine göre çok daha zor. İnputların geldiği dağılımı bilip ona göre analiz etmek gerekiyor.
- Worst case'e gore analiz yaparsak, performansımız için üst sınır çizmiş oluruz. Böylece worst case için bizi tatmin eden bir algoritmamız varsa, average case zaten bundan daha iyi (veya ayni) performans vereceği için o da bizi tatmin edecektir.

**Input (girdi) nedir?**
- Algoritmanın çalışması için verdiğin her şey input’tur.

**Java’dan düşünelim:**
- Bir dizi → input
- Dizinin uzunluğu → input’un boyutu
- Kullanıcının girdiği sayı → input
- Okunan dosyadaki satırlar → input

**Yani: algoritmanın “üzerinde çalıştığı veri” = input**
- Aynı algoritmayı yazarsın ama verdiğin veri değişir.
- Veri değişince, algoritmanın çalışması da değişir.

**1️⃣ En iyi durum (Best Case)**
```java
arr = {7, 2, 3, 4, 5};
target = 7;
```
**İlk elemanda bulur.**
- → 1 adımda biter

**2️⃣ En kötü durum (Worst Case)**
```java
arr = {1, 2, 3, 4, 5};
target = 7;
```
**Hiç yok.**
- → tüm diziyi dolaşır (n adım)

**Bu yüzden analiz yaparken:**

> “Bu algoritma n elemanlı input için ne kadar çalışır?”
diye sorarız.




## References:
1. [why-and-what-time-complexity](https://www.mygreatlearning.com/blog/why-is-time-complexity-essential/)
