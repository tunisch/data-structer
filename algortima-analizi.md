# Algoritma Analizi

- Algoritma analizi, var olan kaynaklara göre en uygun algoritmayı seçmek için uygulanır. Peki algoritma analizi en iyi nasıl yapılır? Kulağa karmaşık geliyor ama çok basit. Programlama dillerinden ve donanımlardan bağımsız bir şekilde Algoritma analizi yapılmalıdır. Aksi taktirde en uygun sonuç alınamayabilir.
- Donanımlar veya programlama dilleri farklı cihazlarda aynı performansı vermeyebilir. Örnek verecek olursak, cep telefonları için uygulama tasarladığımızı varsayalım. Bu uygulamanın performansı Apple telefonlar için farklı, Android telefonlar için farklı, arasında donanım farklı olanlar için ayrı olacaktır. Donanım ve diller ile algoritma analizi pek sağlıklı değildir.
- Algoritma analizi, bir algoritmanın çalışabilmesi için gerekli koşulların sağlanıp sağlanamadığını gösteren bir parametredir.

- Aslında belli bir makinede çalıştırılabilir algoritmaların performansı için dikkat etmemiz gereken kriterler arasında ‘programlama dili seçiminin’ yanı sıra birçok teknoloji detayı vardır ki bunlar; derleyici seçimi, kodu hangi hızda çalıştırdığımız, belleğin ne kadar hızlı olduğu ve hatta önbelleğe alma işleminin miktarı olarak sıralanabilir.
- **Algoritma analizinde biz şunu merak ederiz:**
> “Girdi büyüdükçe bu algoritma ne kadar daha yavaşlıyor?”

- **Buradaki kilit fikir şu:**
  - Bilgisayarın hızı, kullanılan dil, RAM, işlemci… bunların hiçbiriyle ilgilenmiyoruz. Çünkü onlar değişkendir. Bugün var, yarın yok. Ama algoritmanın davranışı kalıcıdır.
  - Bu yüzden çalışma süresini zaman (saniye) olarak değil, girdi boyutuna bağlı bir fonksiyon olarak ifade ederiz.
```java
Mesela:
Girdi boyutu: n (dizideki eleman sayısı gibi düşün)
Çalışma süresi: T(n)
```
**Şimdi örnekle netleştirelim.**

Diyelim ki bir dizide en büyük sayıyı buluyorsun:
```java
for (int i = 0; i < n; i++) {
    // tek bir karşılaştırma
}
```
- Bu döngü n kez çalışır.
- Bilgisayar hızlı mı yavaş mı önemli değil.
- Her durumda iş sayısı n ile doğru orantılıdır.

**Bunu şöyle yazarız:**

```java
T(n) = n
```
- Bu, büyüme hızı (rate of growth) demektir.
- Yani girdi 2 katına çıkarsa, iş de 2 katına çıkar.

**Şimdi daha ilginç bir örnek:**
```java
for (int i = 0; i < n; i++) {
    for (int j = 0; j < n; j++) {
        // işlem
    }
}
```
- Burada iç içe iki döngü var.
**İş sayısı:**
```java
 n * n = n²
```
**Yani:**
```r
T(n) = n²
```
- Bu algoritma, girdi büyüdükçe çok daha hızlı yavaşlar.
**İşte cümlede söylenen şey tam olarak bu:**
> “Programa verdiğimiz input boyutu ile çalışma zamanını fonksiyonel olarak birbirine bağlarsak…”

**Yani:**
- Zamanı → T(n)
- Girdiyi → n
- Aralarındaki ilişkiyi → matematiksel fonksiyon
> “…bilgisayarlara ve programlama dillerine bağlı olmayan bir yapı oluştururuz.”

**Çünkü:**
- Java mı, C mi → umurumuzda değil
- Bilgisayar hızlı mı → önemsiz
- Önemli olan → algoritmanın büyüme davranışı

**Bu yüzden algoritma analizinde:**
- saniye ölçmeyiz
- Big-O kullanırız

**Özetle tek cümlelik özü şu:**

> Algoritma analizi, “bu kod kaç saniyede çalışır?” değil,
“girdi büyüdükçe iş miktarı nasıl büyür?” sorusunu sorar.

## Bu analizi nasil yapabilirim?
- **Calısma Süresi(Execution Time):** Programlama dilinden ve kullanılan bilgisayarın özelliklerinden
etkileniyor o guzden genellenebilir değil.❌
- **Ifade Sagısı:** Programda kac tane ifadenin calıstığı(Bunu gap, bunları topla vs gibi.). Programlama
diline göre aynı işlem icin calışan ifade sagısı değisebilir.
genellenebilir değil.❌
- **Büyüme Hızı (Rate of Growth):** Programa verdiğimiz
input (girdi) boyutu ile çalışma zamanını fonksiyonel
olarak birbirine bağlarsak bilgisayarlara ve programlama
dillerine bağlı olmayan bir yapı oluşturmus oluruz.✅

### References:
1. [derinlemesine-algoritma-analizi](https://birhankarahasan.com/algoritma-analizi-nedir-zaman-karmasikligi-big-o-gosterimi)
2. [algoritma-analiz-wiki](https://tr.wikipedia.org/wiki/Algoritma_analizi)
