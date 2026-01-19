# Binary Search Algorithm

İkili arama algoritması, elimizde bulunan **veri dizisini sıralı olduğunu** varsayıyor, bu durumu değiştirerek sonuca varmak istiyor.

- İkili arama algoritması, **diziyi her seferinde ikiye bölerek ikili arama yapar**. Sıralı bir listem var ise benim Big-o logn olarak karşımıza çıkıyor.
- Aradığım sayı 15 ve benim değer kümem [10,15,20,16,22,36,23] diyelim. Binary Search bu diziyi manipüle ederek şu ifadeye dönüştürüyor. [10,15,16,20,22,23,36]. 36 sayısını en yüksek sayı, 10 sayısını en düşük sayı ilan ediyor. Benim aradığım sayı ile ortada kalan sayıyı kıyaslıyor eğer benim sayım büyükse kendinden küçük bütün sayıları siliyor. Ve kendine yeni bir ortanca belirliyor. Böylelikle gereksiz arama yapmaktan kurtarıyor.

<img width="1799" height="884" alt="Screenshot 2026-01-19 173533" src="https://github.com/user-attachments/assets/e2b424bf-cbfe-48a0-a029-96b25f27cdf4" />

Time complexity: logn adimda istenilen degere ulasilabilir.
Buyuk input size li islemlerde cok avantajlidir

<img width="1600" height="630" alt="image" src="https://github.com/user-attachments/assets/0ccbdfa3-2fd4-4c81-827e-58fe718502f7" />


## Example:

<img width="809" height="614" alt="image" src="https://github.com/user-attachments/assets/8b177001-bbc9-46e9-80d9-4da87bfe0d93" />

- En basta iki deger belirlenir lower & higher index olarak middle a bakilir.
- orta noktayi aliyoruz aradigimiz ile orta noktayi karsialstirip gereksiz tarafi atiyoruz. problem size i -> n/2 oldu
- sonra elde kalan listenin orta noktasi alinip eldeki aranan deger ile karsilastirilir, eleyerek devam edilir.

## References:

1. [binary-search](https://www.khanacademy.org/computing/computer-science/algorithms/binary-search/a/binary-search)
2. [what-is-the-binary-search](https://www.mobilhanem.com/algoritma-dersleri-binary-search/)
3. [binary-search-algorthims](https://www.programiz.com/dsa/binary-search)
