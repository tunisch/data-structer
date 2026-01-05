# Big-O Notation
- Yazılan bir algoritmanın performansını ölçebilmemiz için kullanacağımız en önemli araçlardan biri ise Big-O notation’dır. Big-O notation bir algoritmanın performansını veya time complexity’sini hesaplamak için kullanılır.
- Big O Notationda katsayilar onemli degil, Dominant faktorler alinir. -> n^2 nin 3n e gore daha dominant olmasi gibi bu yuzden Time complex degeri :`O(n^2)` alinir
- Iki farklı arama yöntemi düşünelim.
- A algoritması tek tek sayfalara bakıyor.
- B algoritması sozlujun alfabetik sıralanmış olduğundan yararlanarak en başta en ortadaki sayfayı açıyor, eğer bu bu sayfadaki harfler aradığım kelimeden alfabetik olarak daha ilerideyse sol tarafa aynısını yoksa sağ tarafa aynısını yapıyor.
- Böylece problem her seferinde yari boyutuna inmis oluyor.
- Birkaç durum üzerinden konuşalım. Diyelimki 100 sayfalık bir sözlüğüm var. A algoritması en kötü durumda (aradığım en son sayfadaysa) kaç islem yapacak ? **(100 işlem)**
- B algoritmasi en kotu durumda kac islem yapar? **(2^n = 100)**
- Bu ornege bakarak B algoritmasının A algoritmasında daha hižli olduğunu görebiliyoruz. **(100 / 7 den yaklaşık 15 katı hızında diyebilir miyiz ? bu genellenebilir bir sey midir ?)**
- Pek diyemiyoruz. Soyle düşünelim, sozluğum 10.000 elemanlı olsa, A algoritması en kötü durumda 10.000 islem yapar ama B algoritması 2^x=10.000 yaklaşık 13 islem yapar. 10.000 / 13 yaklaşık 770 katı hızında gözűkuyor !
- Bu yuzden algoritmalarin sadece 1 input boyutuna göre karşılaştırmalarına bakıp karar veremeyiz. Genel yapısını bize gösterecek bir analize ihtiyacımız var, iste burada Big O Notation devrege giriyor.
- Big O notation algoritmanin ne kadar surede çalışacağını söylemeyecek. Bize algoritmamızın çalışma zamanının inputun boyutu ile nasıl değiseceğini söyleyecek.
- Mesela sözlük örneğimiz de input size'imiza n dersek algoritmamızi en kötü durumda n işlem yaptığını söyleyebiliriz. Inputum n boyutunda olunca calısma süremin de en kötü durumda n olmasıni `O(n)` diye göstereceğim. Aynı sekilde B algoritması icin `O(logn)`
- Big o notation'da yapilacak toplam islem sayısinin input size ile nasıl scale(sistem yuk altindayken performansi olcmek) olacağına bakıyoruz, Benim için bu fonksiyonun yapısı önemli.
- Islem sayısı input size ile linear mi artiyor, karesi ile mi orantili artıyor, logaritmik mi ?
- Karakteristiği onemsediğimiz icin 2n islem yapan algoritmaya da n islem yapan algoritmaya da O(n) diyoruz, ikisi de linear bir sekilde artıyor.Big O Notation bakarken katsayılar önemli değil.
- Burada n^2 özel bir durum değil aynısı 2n, 3n, 1/2n için de geçerli, onların da Big O Notation'ı O(n). Yapı ne olursa olsun katsayı yazılmıyor.
- Analizimin sonucu `2n^2+3n+2` gibi bir sey cıktı diyelim. `n` büyüdükce, `3n+2` nin etkisi `2n^2` in yanında önemsiz kalacak. O yuzden dominant olanı Big O notation olarak yazabiliriz `O(n^2)`.
**2n^2+3n+2 -> 2n^2 -> O(n^2)
**Big-O Terimleri ve Senaryoları**
- O(1) -> Constant
- O(N) -> Linear
- O(N^ 2) → Quadratic
- O(log N) → Logarithmic
- O(N log N) → Linearithmic
- O(c^N)→ Exponential
- O(N!) → Factorial

(N = veri setinin büyüklüğü || eleman sayısı, c — sabit bir değer)

<img width="1100" height="692" alt="image" src="https://github.com/user-attachments/assets/3b11247c-d94b-4217-a034-55d80f3dfd47" />

**Yukarıdaki chart’ta, veri setine ve yapılan işleme göre algoritmanın Big-O sınıflandırması yer almaktadır.**

**Aşağıdaki tabloda ise en çok kullanılan Big-O terimlerinin farklı büyüklüklerdeki input setlerine göre karşılaştırmaları yer almaktadır.**

<img width="1100" height="401" alt="image" src="https://github.com/user-attachments/assets/6115d025-e90e-454c-accc-bc278059c4ab" />

- Bu terimleri, örnekler ile beraber daha net anlamaya çalışalım.

**O(1) — Constant Complexity**
  - **Constant complexity’de** elinizde bulunan veri seti ne kadar büyük olursa olsun, çalıştırılma süresi ve kullanılan kaynak her zaman **sabittir**.

<img width="416" height="312" alt="image" src="https://github.com/user-attachments/assets/a21ac335-0183-464d-8bc4-4b10d56d6514" />

**Örneğin:**
```java
public class Main {

    public static void getLastItem(int[] items) {
        System.out.println(items[items.length - 1]);
    }

    public static void main(String[] args) {
        int[] numbers = {10, 2, 20, 11000, 32, 123, 241312, 32142, 32131};
        getLastItem(numbers);
    }
}
```
- Fonksiyona argüman olarak yazılan array ne kadar büyük olursa olsun, çalıştırılma süresi hep sabit olacaktır çünkü bizim istediğimiz array’in son elemanıdır.

**O(N) — Linear Complexity**

- **Linear complexity’de**, elimizdeki veri seti arttıkça, çalıştırılma süreside doğru orantılı şekilde artış gösterir.
- Günlük yaşantımızdan bir örnek verecek olursak eğer, gün içerisinde okuduğunuz bir kitab’ı veya izlediğiniz bir filmi ele alalım. Sizin ne kadar süre kitap okuduğunuz veya filmi izlediğiniz, kitabın sayfa sayısına veya filmin süresine bağlı olarak değişir. Eğer bir film 2 saat ise, siz 2 saatinizi filmi izlemek için harcamış olursunuz. Eğer kitap 100 sayfa ise ve siz 50 sayfasını 1 saatte okuduysanız, tüm kitabı okumak için 2 saat harcamanız gerekecektir.

<img width="463" height="316" alt="image" src="https://github.com/user-attachments/assets/0281b964-c962-443f-98b3-0c5e65395b35" />

**Örneğin bir dizinin tüm elemanlarını yazdırma işlemi Linear Complexity’e örnektir çünkü array’in eleman sayısı arttıkça, fonksiyonun çalışma süresi de artacaktır.**

```java
1 public class Main {
2
3    public static void displayArrayElements(int[] array) {
4        for (int value : array) {   // n kez döner
5            System.out.println(value); // her döngüde 1 işlem
        }
    }

    public static void main(String[] args) {
        int[] numArray = {
            21, 23, 12321, 312, 312, 312, 3, 14, 12, 4,
            32, 53, 5, 234, 1, 32, 13, 12, 41, 321, 4, 124
        };

        displayArrayElements(numArray);
    }
}
```
- Bu fonksiyonun time complexity’sine bakalım:
```
Satır 4: n boyutunda bir döngü gerçekleşir
Satır 5: For döngüsü içerisinde 1 işlem gerçekleşir.
```
- Böylelikte Complexity olarak (N) + 1 değerini elde ederiz. 1 değerini, n arttıkça önemi azalacağı için yok sayabiliriz. O(n) 

**O(N²) — Quadratic Complexity Time Algorithm**

- **Quadratic Complexity** input büyüklüğünün karesi ile doğru orantılıdır.
- Eğer input büyüklüğü 2 ise, 4 işlem gerçekleşir. Eğer input büyüklüğü 8 ise, 64 işlem gerçekleşir ve bu şekilde devam eder. Genellikle sıralama (sorting) algoritmalarında bu complexity görülür.

<img width="382" height="322" alt="image" src="https://github.com/user-attachments/assets/a5bd85b8-c603-43f1-a11c-1cb089015d79" />

- Örneğin bir array içerisindeki her elemanı, array’in diğer elemanları ile yazdırma işleminde, iç içe for döngüleri kullanırız. Tek for kullanımında O(N) bir işlem gerçekleştiriz. Bu işlemi iç içe yaptığımızdan, N * N sonucu ile O(N²) Time complexity değerini elde etmiş oluruz.

```java
public class QuadraticCalculation {

    static void quadraticCalculation(int[] arr) {
        int count = 0;

        for (int i = 0; i < arr.length; i++) {
            for (int j = 0; j < arr.length; j++) {
                System.out.println("i: " + i + " and j: " + j);
                count++;
            }
        }

        System.out.println(arr.length); // 6
        System.out.println(count);      // 36
    }

    public static void main(String[] args) {
        int[] arr = {3, 1, 2, 5, 6, 71};
        quadraticCalculation(arr);
    }
}
```
**Şimdi asıl önemli kısım: neden 36?**

- arr.length = 6

**Dış döngü:**

`i → 0,1,2,3,4,5 → 6 kez`

**İç döngü:**

`Her i için j → 0,1,2,3,4,5 → 6 kez`

**Toplam:**

`6 × 6 = 36`
> **count** değişkeni aslında algoritma analizinde yaptığımız şeyi simüle ediyor:
“Kaç kere çalıştı?”

`count = n * n → O(n²)`

**O(log N) — Logarithmic Complexity**

- Logarithmic time complexity, genelde her seferinde problemi ikiye bölen algoritmalarda kullanılır. Örneğin sözlükten bir kelime baktığımızı düşünelim. Sözlüklerde, her kelimenin alfabetik olarak sıralı olduğunu biliyoruz. Kelimeyi bulabilmek için yapılabilecek olanlar:
- A algoritması:
  - Kitabın en başından başlayarak sırasıyla kelimeyi bulana kadar gitmek.
- B algoritması:
  - Kitabın ortasından açıp ilk kelimeye bakmak.

- Eğer aranan kelime alfabetik olarak kitabın ortasında bulunan ilk kelimeden büyükse kitabın sağ tarafına, değilse sol tarafına bakmaya devam etmek.

A algoritmasında kelime kelime gideceğimizden dolayı Time complexity değeri O(N)’dir. B algoritmasının Time Complexity’si O(logN)’dir. Her iterasyonda problemi ikiye böler. B algoritması aynı zamanda Binary search’e örnektir.

<img width="472" height="328" alt="image" src="https://github.com/user-attachments/assets/fa0f64e5-d094-432d-b381-4739e40edaaf" />

**Big-O Notation grafikleri :**

<img width="518" height="431" alt="image" src="https://github.com/user-attachments/assets/7b38e2ac-a0d0-4a7d-be4c-2b59a306e1e4" />

- İki farklı arama yöntemimiz var. Bunlardan A algoritması sayfa sayfa, B algoritması yarıya bölüp tarıyor. Sizce hangisi daha hızlı çalışır? Tabii ki B algoritması. Peki neden? Sürekli tarayacağı alan azalıyor. A algoritması daha işlemini bile yarılamamışken, B algoritması sonuca ulaşıyor.
- N tane işlem üzerinden big-o gösterimi yapalım. A algoritması input olarak kaç sayfa varsa o kadar işlem yapıyor. B algoritması ise sayfa sayısını azaltmak için alfabetik sıraya göre sağ ve sol olarak yarıya indiriyor.

<img width="518" height="431" alt="image" src="https://github.com/user-attachments/assets/dca433db-e431-4974-aa89-f1fa141570e6" />

## References:
1. [big-o-nedir](https://medium.com/kodcular/nedir-bu-big-o-notation-b8b9f1416d30)
2. [big-o-cheatsheet](https://www.bigocheatsheet.com/)
