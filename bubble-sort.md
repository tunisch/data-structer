# Bubble Sort Algorithm

## Sıralama Algoritmaları Arasındaki Farklar

Sıralama algoritmaları arasındaki temel farklar **zaman karmaşıklığı (time complexity)** ve **hafıza karmaşıklığı (space complexity)** üzerinden değerlendirilir.

* **Verimli algoritmalar** genellikle `O(N log N)` zamanında çalışır.
* **Verimsiz algoritmalar** ise `O(N²)` zaman karmaşıklığına sahiptir.

Bubble Sort, bu ikinci gruba giren klasik ve öğretici bir algoritmadır.

![Bubble Sort vs Others](https://github.com/user-attachments/assets/c52cb397-b136-434e-939d-7a90581fd73f)

---

## Bubble Sort Hakkında

Bubble Sort, komşu elemanları karşılaştırarak çalışan basit bir sıralama algoritmasıdır. Mantık şudur:

* Dizi baştan sona gezilir.
* Yan yana duran iki eleman karşılaştırılır.
* Sıralama koşuluna uymuyorsa yerleri değiştirilir.
* Her turda **en küçük (veya en büyük) eleman** doğru konumuna biraz daha yaklaşır.

### Temel Pseudo Kod

```c
for (i = 1; i <= n; i++)
    for (j = n; j > i; j--)
        if (dizi[j] < dizi[j - 1]) {
            tmp = dizi[j - 1];
            dizi[j - 1] = dizi[j];
            dizi[j] = tmp;
        }
```

Bu örnekte algoritma diziyi **küçükten büyüğe** doğru sıralar.

> Büyükten küçüğe sıralamak için `if (dizi[j] > dizi[j - 1])` yazmak yeterlidir.

---

## Çalışma Mantığı (Adım Adım)

Örnek dizi:

```
56  3  96  -2  1
```

### Başlangıç

```
56  3  96  -2  1
```

### 1. Döngü

```
-2  56  3  96  1
```

### 2. Döngü

```
-2  1  56  3  96
```

### 3. Döngü

```
-2  1  3  56  96
```

### 4. Döngü

```
-2  1  3  56  96
```

### 5. Döngü

```
-2  1  3  56  96
```

Dikkat edilirse **3. döngüden sonra dizi zaten sıralıdır**, ancak algoritma bunu bilmediği için çalışmaya devam eder.

---

## Neden Gereksiz Döngüler Var?

Bubble Sort ve benzeri temel algoritmalar, **en kötü senaryoya göre** tasarlanmıştır.

* En kötü senaryo: Dizi tamamen ters sıralı
* Bu durumda algoritma tüm döngüleri çalıştırmak zorundadır

Ancak dizi erken sıralanırsa, bunu fark edecek bir mekanizma eklenebilir.

---

## İyileştirilmiş Bubble Sort (Early Exit)

Her turda dizinin sıralı olup olmadığı kontrol edilirse, gereksiz döngüler engellenebilir.

```c
for (i = 1; i <= n; i++) {
    int sirali = 1;

    for (j = n; j > i; j--) {
        if (dizi[j] < dizi[j - 1]) {
            tmp = dizi[j - 1];
            dizi[j - 1] = dizi[j];
            dizi[j] = tmp;
            sirali = 0;
        }
    }

    if (sirali == 1)
        break;
}
```

Bu versiyon, **en iyi senaryoda O(N)** zamanda çalışabilir.

---

## Bubble Sort Zaman Karmaşıklığı Analizi

* Dış döngü: En kötü durumda `N` kez
* İç döngü: `N + (N-1) + ... + 1`

Toplam işlem sayısı yaklaşık olarak:

```
N × (N - 1)
```

### Big-O Gösterimi

```
O(N²)
```

Bu nedenle Bubble Sort **büyük veri setleri için önerilmez**.

---

## Java ile Bubble Sort Kodu

```java
void bubbleSort(int[] arr) {
    int n = arr.length;

    for (int i = 0; i < n - 1; i++) {
        for (int j = 0; j < n - i - 1; j++) {
            if (arr[j] > arr[j + 1]) {
                int temp = arr[j];
                arr[j] = arr[j + 1];
                arr[j + 1] = temp;
            }
        }
    }
}
```

---

## Ne Zaman Kullanılır?

* Algoritma mantığını öğrenmek için
* Küçük veri setleri için
* Eğitim ve görselleştirme amaçlı

Gerçek sistemlerde genellikle **Merge Sort**, **Quick Sort** veya **Tim Sort** tercih edilir.
