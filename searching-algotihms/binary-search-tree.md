# Binary Search Tree 
Ram de Binary Search e gore farkli depolandigi icin bu yuzden yeni veri eklemede O(n) time complex durumu olusmaz. bos olan node a eklenerek sistem devam eder.
- BST bir veri yapısıdır.

**[7, 5, 1, 8, 3, 6, 0, 9, 4, 2]**

> ilk gelen root tur, Burada root: 7 dir
- Kuralı basit:

Sol alt ağaç < kök

Sağ alt ağaç > kök

```
      5
     / \
    3   8
   / \   \
  2   4   9
```
- BST’de arama

> Ortalama durumda: O(log n)
> Ağaç dengeliyse süper.

- BST’de ekleme

Yeni elemanı alırsın:

Kökten başlarsın, Sağ mı sol mu diye karar verirsin ,Yaprakta eklenir.Kaydırma yok. Taşıma yok. Sadece aşağı doğru yürüyüş.

- Ortalama durumda ekleme: O(log n)

Ama burada evrenin küçük bir şakası var.

> Eğer ağacı dengesiz kurarsan:

```
1
 \
  2
   \
    3
     \
      4
```
Bu artık ağaç değil, utanmadan liste olmuş bir şeydir.

- Arama: O(n)
- Ekleme: O(n)

| Yapı                          | Arama    | Ekleme   | Gerçeklik         |
| ----------------------------- | -------- | -------- | ----------------- |
| Sıralı dizi + Binary Search   | O(log n) | **O(n)** | Kaydırma yüzünden |
| Binary Search Tree (ortalama) | O(log n) | O(log n) | Yapısal           |
| Dengesiz BST                  | O(n)     | O(n)     | Liste kılığı      |


<img width="1362" height="733" alt="image" src="https://github.com/user-attachments/assets/ee2d3fa5-ddf0-40cb-8d8d-f174a3f9cae0" />

Dizilerde (Array) Ekleme ve Arama Performansı Sıralı bir dizide arama yapmak log n zaman alırken, bu diziye yeni bir elemanı sıralı bir şekilde eklemek O(n) zaman alır. Bunun sebebi, yeni bir eleman eklendiğinde dizideki diğer elemanların yer değiştirmek (taşınmak) zorunda kalmasıdır. Bu maliyetten kurtulmak için Binary Search Tree (İkili Arama Ağacı) yapısı kullanılır.
Binary Search Tree (BST) Yapısı ve Mantığı BST'de veriler, bağlı listelerdeki (linked list) gibi referanslar aracılığıyla tutulur; ancak burada her düğümün sağ ve sol olmak üzere iki referansı vardır,. 

Temel kural şudur:
- Bir düğümün sağ tarafında kendisinden büyük elemanlar bulunur.
- Bir düğümün sol tarafında kendisinden küçük elemanlar bulunur.

Yeni Eleman Ekleme Süreci Yeni bir eleman (örneğin 18) eklenirken en baştaki düğümden başlanarak "bu eleman büyük mü küçük mü?" sorusu sorulur. Eleman büyükse sağa, küçükse sola gidilerek uygun yer bulunur. Bu yöntemle, her soruda ağacın bir tarafı elendiği için problem sürekli yarıya iner. Eğer ağaç iyi dağılmış (dengeli) ise, bir eleman eklemek log n zamanda tamamlanır.

**Zaman Karmaşıklığı:En İyi ve En Kötü Durumlar**

- Average Case (Ortalama Durum): Ağaç dengeli ve elemanlar sağa-sola eşit dağılmışsa, arama ve ekleme işlemleri log n karmaşıklığındadır.
- Worst Case (En Kötü Durum): Eğer ağaç dengesizse (örneğin sadece sol tarafa yığılmışsa), eleman eklemek veya aramak için neredeyse tüm elemanlara bakmak gerekebilir. Bu durumda zaman karmaşıklığı O(n) olur,.
- BST ve Diziler Arasındaki Fark Dizilerin aksine, Binary Search Tree yapısında "random access" (rastgele erişim) yoktur; yani "bana beşinci elemanı getir" gibi doğrudan bir erişim yapılamaz. Ancak dengeli bir ağaçta hem arama hem de yeni eleman ekleme işlemleri log n süresinde yapılabildiği için dizilere göre çok daha hızlı sonuç verir
- Binary searchte bu islemi yapmak time complex te O(logn) zaman aliyor ama diyelim ki yeni eleman eklemek istersek bu arrray[] e bunuda sirali olarak tut yine aramalarda kulalncam dersek bunu yapmam time complex te O(n) islem oluyor (butun elemanlar tasindigi icin bir yere tasinirken n tane islem yapmis oluyoruz yani )

Burada yapacagimiz sey;

Bir düğüm her iki tarafa da referans verebiliyor. Sağ ve sol olarak. Sağ tarafından kendinden büyük elemanlar, sol tarafında ise kendinden küçük elemanlar bulunacak.

<img width="1194" height="614" alt="image" src="https://github.com/user-attachments/assets/35c52c7c-2342-408a-8993-c86718190f79" />

- Tree'ye eleman eklemek istediğimde root'dan başlıyorum. Örnek olarak ben 26 sayısını ağaç yapısına eklemek istiyorum. Root'a soruyorum senin değerin ne 56. Baştaki açıklamamızı hatırlayalım. Sağ tarafında kendinden büyük, sol tarafında kendinden küçük elemanlar var. O yüzden sırasıyla 56 ve 30 a kadar ilerliyorum. 30 bana benim sol tarafıma geçmelisin çünkü sen benden küçüksün diyor. Karşıma 22 değerinde olan düğüm çıkıyor ve 22 den büyük olduğum için sağ tarafına bir köşe çekiyorum ve 26 sayısını bağlıyorum.

## References:
1. [binary-search-tree-nedir](https://tsafaelmali.medium.com/binary-search-tree-nedir-2e6fb0621d9)
2. [binary-search-anlamak](https://www.buraksenyurt.com/post/Binary-Search-Tree-yi-Anlamak)
3. [binary-search-tree-english-detail](https://www.geeksforgeeks.org/dsa/binary-search-tree-data-structure/)
