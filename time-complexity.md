# Time Complexity Nedir?
- Time complexity bir algoritmanın çalışması için gerekli olan süredir. Ancak buradaki süre, saniyeleri hesaplayarak değil, kaç tane işlem gerçekleştirdiğine göre hesaplanmaktadır. Uygulama tarafından gerçekleştirilen işlem sayısı, veri setinin büyüklüğüne ve o veri setindeki elemanlarına sırasına göre belirlenir.
**Örneğin bir dizinin en küçük elemanını bulma işlemine bakalım:**
```java
1 public class MinFinder {
2    public static int getMin(int[] arr) {
3        int min = arr[0]; // Java'da undefined yok, ilk elemanı referans alırız
4
5        for (int element : arr) {
6            if (element < min) {
7                min = element;
8            }
9        }
10        return min;
    }

    public static void main(String[] args) {
        int[] numbers = {4, 5, 9, 32, 1, 5, 35, 3124, -10, 21, 321, 41};
        System.out.println(getMin(numbers));
    }
}
```
```r
Satır 2: 1 işlem
(Basit bir atama işlemi olduğu için karmaşıklığı 1 kabul edilir)
Satır 3: 1 işlem
(Döngünün başlangıç tanımı sabit maliyetlidir)
Satır 5–9:
Bir döngü işlemi gerçekleşir ve dizinin boyutu olan n kadar çalışır
→ O(n)
Satır 6: 1 işlem
(Karşılaştırma operatörleri if koşulu gibi sabit zamanda çalışır)
Satır 7: 1 işlem
(Atama işlemi sabit maliyetlidir)
Satır 10: 1 işlem
(return işlemi sabit zamanlıdır)
```
**Toplam Zaman Karmaşıklığı**

- Döngü dışındaki işlemler sabittir (O(1)), döngü ise n kez çalışır.
- Bu nedenle algoritmanın toplam zaman karmaşıklığı:

`O(n)` = Linear Complexity’e eşittir. 

**Algoritmanın verimli olması için belli kurallar vardır.**
- Örnek: Raflara kitap yerleştirmek.
- Kitapları, gelişigüzel raflara dağıtırsak aradığımız kitabı daha fazla zamanda bulabiliriz. Aslında bu bir worst case'dir. Kitapları filtrelememiz gerekir. Kalın olanları bir rafa, ince olanları bir rafa, küçük boyutta olanları bir rafa koyduğumuz zaman aradığımız şeyi daha rahat bulabiliriz. Algoritma, en kötü senaryoya ne kadar hazırsa, bizi o kadar memnun edebilir.
- Algoritmalar için genellikle sık kullanılan average case'dir. Kitapların bölümüne göre kaç tane olduğunu biliyorsak average case kullanabiliriz. En büyük rafı miktarı fazla olana ayırabiliriz. Input yoksa average zordur!!!!
- Bir diğer senaryomuz ise best case'dir. Beklediğimiz en iyi durum. Kitap örneğine devam edecek olursak, bütün kitapların ayrı raflarda olması, alfabeye göre sıralanması best case olarak ifade edilebilir. Çünkü aradığımızı rahatlıkla bulabiliyoruz.
- Kullanacağımız algoritmayı analiz etmek istiyoruz. Problem ayıı olsa da farklı inputlar için algoritmamız farklı performans senaryoları üretebilir.
- Diyelim ki bir kelimenin anlamını sözlükte arıyorum. Arama için sayfalara tek tek bakıyorum. Burada algoritmam sayfalara tek tek bakmak, input da aradığım kelime.
- Aradığım kelimenin boyutu aynı olsa da hangi harfle başladığına göre yapacağım işlem (sayfa çevirme) sayısı değişebilir. Yani input algoritmamın yapacağı işlem sayısını etkileyebiliyor.

**Bir başka örnek olarak; Elimizde bir algoritmanın Time complexity değerinin T(n) =(n^2 + 3n + 4) olduğunu düşünelim. n değerinin çok büyük olması durumunda, 3n+4 kısmı, n^2 kısmı ile karşılaştırıldığında önemsiz hale gelecektir.**

<img width="481" height="271" alt="image" src="https://github.com/user-attachments/assets/23a5719b-6015-4429-881e-072f9f6fe7cd" />
- n = 1000 için n^2, 1000000 değerine sahip olurken 3n + 4, 3004 değerine sahip olur. Bu yüzden bu sabit kısımları yok sayabiliriz.
- Time complexity bize bir algoritma için 3 durum sunar. Best-case, average-case ve worst-case.

**Elimizde sıralı olmayan bir dizi olduğunu düşünelim. Örneğin [5,1,4,2,6,3,7]**

- Bu dizi de aradığınız bir değeri bulabilmek için dizideki tüm index değerleri ile aradığınız değerin eşleşmesi gerekmektedir (Linear Search). Bu örneğin case’lerine bir bakalım:

```
Best-case: Aradığınız değerin 5 olması bu algoritmanın best-case’dir. Çünkü daha ilk iterasyonda aradığımız değere ulaşmış oluruz.
_Average-case Bu case, verilen input setindeki değerlerin dizi içerisindeki dağılımına göre belirlenir. Bu örnek için average-case aradığımız değerin, dizi’nin tam ortasındaki, yani 2 değerinin olması olabilir.
Worst-case: Bu örneğimiz için worst-case, yani en kötü durum senaryosu, aradığımız değerin dizinin en sondaki değer olması durumudur. Bu örnek için bu değer 7'dir.
Worst-case: Aradığımız değerin dizi içerisinde bulunmaması durumu da worst-case'e örnektir.
```

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




### References:
1. [why-and-what-time-complexity](https://www.mygreatlearning.com/blog/why-is-time-complexity-essential/)
