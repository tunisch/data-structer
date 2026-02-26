# Merge Sort 

Algoritmanın çalışması kavramsal olarak şöyledir:

- Sıralı olmayan listeyi ortadan eşit olarak iki alt listeye ayırır.
- Alt listeleri kendi içinde sıralar.
- Sıralı iki alt listeyi tek bir sıralı liste olacak şekilde birleştirir.

Insertion Sort'da, Big-O gösteriminden dolayı input'um arttığında n2 olduğunda dolayı çalışma zamanı artıyor.

- Peki daha hızlı bir şekilde sıralama yapılabilir mi? Evet, Merge Sort burada yardımımıza koşuyor. Bir listeyi her adımda parçaya ayırıp tek eleman kalıncaya kadar bölüyor. Böldükten sonra sıralı bir şekilde bize sunuyor (Performans).

<img width="518" height="431" alt="image" src="https://github.com/user-attachments/assets/5224c793-c8a4-489e-954d-bb1e81956a50" />

<img width="518" height="431" alt="image" src="https://github.com/user-attachments/assets/f2e1b2a4-1e31-4f7b-82a2-c47812160211" />

- **Insertion sort'da, time complexity n2 olduğundan ötürü çalışma zamanımız artıyordu. Merge sort'da ise nlogn olduğu için açık ara performans olarak daha iyi diyebiliriz.**

## Referans: 

1. [merge-sort-wiki](https://tr.wikipedia.org/wiki/Birle%C5%9Ftirmeli_s%C4%B1ralama)
2. [merge-sort-detail-with-code](https://www.programiz.com/dsa/merge-sort)
