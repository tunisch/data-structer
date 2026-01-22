# Insertion Sort Algorithms

## İnsertion Sort Nasıl Çalışır?
Bastan sonra arama yapilir en kucugu bulunup en basa yazilir (n arama) sonra (n-1) arama, boylelikle 1 aramaya kadar gider. n n-1 n-2 1 -> n.(n+1)/2 = O(n2) 

Algoritmada döngümüz her bir tur döndüğünde sıradaki elemanı sondan başa doğru karşılaştırarak yerine yerleştirme esaslı çalışmaktadır.

<img width="768" height="543" alt="image" src="https://github.com/user-attachments/assets/75389498-64c4-487f-8408-a53ddf0203d7" />

Pseduo kodu verdikten sonra açıklamaya devam edelim:

```
for (i = 1; i < n; i++)
   {
       deger = arr[i];
       j = i-1;
 
       while (j >= 0 && arr[j] > deger)
       {
           arr[j+1] = arr[j];
           j--;
       }
       arr[j+1] = deger;
   }
```

Az önce de dediğim gibi üstteki for döngüsü her bittiğinde dizideki i. elemanı yani ‘deger‘ değişkeni doğru yerini bulmuştur. Doğru derken kastettiğim 0 ile i arasındaki doğru yerini bulmuştur. Döngü en sona geldiğinde 0 dan n-1 e kadar herkes doğru yerini bulduğu için dizi sıralanmıştır.

Hemen bir örnek vererek daha rahat kavramaya çalışalım.

Not: ‘[‘ ve ‘]’ ayraçlarıyla ayrılmış kısım halihazırda sıralanmış aralığı temsil eder.

Başlangıç
[10] 3 9 2 1

1. Adım
[3 10] 9 2 1

2. Adım
[3 9 10] 2 1

3. Adım
[2 3 9 10] 1

4. Adım
[1 2 3 9 10]

### Karmaşıklık Hesabı

Gördüğünüz üzere her adımda yeni bir eleman sıralanmış kısıma dahil olmaktadır. Karmaşıklık hesabı yaparsak her adımda bütün elemanları gezdiği için en kötü ihtimalde O(N^2)‘dir. Bu algoritma için en iyi ihtimalle başlangıçta dizinin sıralı olmasıdır. Böylelikle hiç yer değiştirme yapmadan sıralama bitecektir.

En kötü durum ise tersten yani bu örnek için büyükten küçüğe sıralanmış bir diziyi girdi olarak vermektir. Her eleman için en başa kadar karşılaştırma yapacağı için yaklaşık N^2 işlem gerçekleşecektir.

### İnsertion Sort kodu:

```java
void sort(int arr[])
    {
        int n = arr.length;
        for (int i=1; i<n; ++i)
        {
            int deger = arr[i];
            int j = i-1;
 
            while (j>=0 && arr[j] > deger)
            {
                arr[j+1] = arr[j];
                j = j-1;
            }
            arr[j+1] = deger;
        }
    }
```
