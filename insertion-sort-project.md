Bu dosya [Insertion Sort Projesinin](https://github.com/tunisch/data-structer/tree/project/insertion-sort) çözümünü içermektedir.

**Project 1**

## Stages
- [22,27,16,2,18,6]
- [16,22,27,2,18,6]
- [2,16,22,27,18,6]
- [2,16,18,22,27,6]
- [2,6,16,18,22,27]

## Big-O Notation

n n-1 n-2... 1 = n.(n+1)/2 = n^2 -> O(n^2)

## Time Comlexity: Dizi siraliyken 18 sayisinin case durumu
Average case: Aradığımız sayının ortada olması

Worst case: Aradığımız sayının sonda olması

Best case: Aradığımız sayının dizinin en başında olması.
- [2,6,16,18,22,27]

**Yanıt:** Sonuca bakildiginda aranan sayi (18) ortada yer almaktadir. Bu durum bir **Average casedir**.

**Project 2**

[7,3,5,8,2,9,4,15,6] 

**Selection Sort a gore ilk 4 adimi:**

- [2,7,3,5,8,9,4,15,6]
- [2,3,7,5,8,9,4,15,6]
- [2,3,4,7,5,8,9,15,6]
- [2,3,4,5,7,8,9,15,6]

Selection Sort’ta her turda sadece 1 eleman doğru yerine kesin olarak yerleşir.

Ara elemanlar “tam sıralı” görünse bile bu tesadüf; algoritma onların düzeniyle ilgilenmez.
