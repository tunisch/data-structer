# Big-O Notation
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
  

**Big-O Notation grafikleri :**

<img width="518" height="431" alt="image" src="https://github.com/user-attachments/assets/7b38e2ac-a0d0-4a7d-be4c-2b59a306e1e4" />

- İki farklı arama yöntemimiz var. Bunlardan A algoritması sayfa sayfa, B algoritması yarıya bölüp tarıyor. Sizce hangisi daha hızlı çalışır? Tabii ki B algoritması. Peki neden? Sürekli tarayacağı alan azalıyor. A algoritması daha işlemini bile yarılamamışken, B algoritması sonuca ulaşıyor.
- N tane işlem üzerinden big-o gösterimi yapalım. A algoritması input olarak kaç sayfa varsa o kadar işlem yapıyor. B algoritması ise sayfa sayısını azaltmak için alfabetik sıraya göre sağ ve sol olarak yarıya indiriyor.

<img width="518" height="431" alt="image" src="https://github.com/user-attachments/assets/dca433db-e431-4974-aa89-f1fa141570e6" />

## References:
1. [big-o-nedir](https://medium.com/kodcular/nedir-bu-big-o-notation-b8b9f1416d30)
