# Quick Sort

İlk olarak bir pivot belirler bu pivota göre pivottan küçük ve eşitler sol kısmına, pivottan büyük ve eşitler sağ kısmına yazılır. Parçalanmış kısımlar yeni bir pivot belirlenerek parça pinçik edilir.

- `Pivot` ile merge sorttaki gibi soldan ve sagdan bolerek karsilastirip birlestiriyoruz.
- n-1 islem yapilir (her asamada)
- **pivot guzel bolmeler yaparsa daha hizli olur Ama pivot en kucuk deger ya da en buyuk olursa worst case olusur, bu durumda insertion sort daha hizli ve mantikli kabul edilir.**

<img width="577" height="410" alt="image" src="https://github.com/user-attachments/assets/37449870-53c4-4187-9d83-d5975dcf5e32" />

- Quick Sortta pivot ortadan bolerse en hizli durum diagrami; **Average Case Durumu**

<img width="1214" height="482" alt="image" src="https://github.com/user-attachments/assets/0e6061e9-0324-424e-961d-bbc39373b063" />

    - x : kac kere islem yapildi sayisi , n dizi sayisi , 2 = her islemde 2 ye bolerek gittigimiz icin.

- Quick Sortta pivot en kucuk ya da en buyuk olursa dizide; **Worst Case Durumu** 

<img width="891" height="536" alt="image" src="https://github.com/user-attachments/assets/0065c6c9-a0d9-4850-8d02-80e77bbd2f31" />

Hızlı sıralama günümüzde çok yaygın olarak kullanılan bir sıralama algoritmasıdır. N tane sayıyı average case e göre big-o nlogn, worst case e göre big-o n^2 karmaşıklığı ile sıralanır.

- Quick Sort Merge Sorttan daha hizli olabilir
- Merge Sortun worst case i nlogn ,
- Quick Sortun average case i nlogn,
**Peki diyleim ki Quick Sortun Average case nlogn , Merge Sortunda Average Case nlogn o zaman hangisi daha hizli olur?**
> Quick Sort daha hizli olur cunku  **Katsayidan dolayi** daha hizlidir. Quick Sort Katsayisi Merge Sorttan az oldugu icin daha hizli olur.

<img width="580" height="420" alt="image" src="https://github.com/user-attachments/assets/69936d06-eb85-4a59-b4fa-626d905dcd38" />

Yukardaki Gorselde Time complexleri karsialstiriyoruz, normalde hepsinin Big-O notion u O(n^2), Ama Katsayisi 1/2 olan daha hizli calisir Cunku yarisi zamanda calisir ve bu yuzden daha hizli calisir diyebiliriz.

## Example

1) Aşağıdakilerden hangisi Quick Sort'un özellikleri arasında yer almaz?

- Günümüzde çok yaygın olarak kullanılır.
- Bir pivot belirler, pivota göre diziyi parçalar.
- Average case'in time complexity'si nlogn'dir.
- Worst case'in time complexity'si n'dir.

**Cevap**
>  Worst case'in time complexity'si n'dir.

### Referance:

1.  [quick-sort](https://www.mobilhanem.com/algoritma-dersleri-quick-sort/)
2.  [quick-sort-nedir](https://tr.wikipedia.org/wiki/H%C4%B1zl%C4%B1_s%C4%B1ralama)
