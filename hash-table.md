# Hash Function/ Hash Table

**Indexleme**
- Arraylerde 0 bazlı bir indexleme vardır. Bazı programlama dillerin 1 bazlı indexlemeler olsa da genel olarak 0 bazlı indexleme kullanılır.

<img width="518" height="431" alt="image" src="https://github.com/user-attachments/assets/54ae5282-db97-4286-94da-26881bda8711" />

**Hash Function/ Hash Table**
- Hash Table, key value prensibine dayanan bir array kümesidir. Key olarak çağırdığınız elemanın değerini (value) yansıtır.
- Hash Table yerine dizileri kullanabilirdik. Fakat her ürünü ve fiyatını tek tek aramak istemediğimiz için hash table kullanıyoruz. Peki bu süreç nasıl işliyor? Hemen bir örnek yapalım. Örneğimiz bir kuru yemiş dükkanından gelecek.

<img width="518" height="431" alt="image" src="https://github.com/user-attachments/assets/f97f6848-5137-4fc1-a868-89889b41f7de" />

- Bu kısımda ilk olarak bulunan ürün sayımız kadar değeri olan bir Array oluşturduk.
- Daha sonra hash fonksiyonundan ürünleri geçirerek index değerlerine ulaştık.

<img width="518" height="431" alt="image" src="https://github.com/user-attachments/assets/e9f8c890-c4df-48ae-8b65-302c53961bfb" />

- Şifrelendiği için artık her badem keyi gönderildiğinde 85TL, fıstık keyi gönderildiğinde ise 69 sonucu verecektir.
- Özetle, elimizde var olan verileri bir fonksiyondan geçirip indexliyoruz. Bu fonksiyona hash function, bu fonksiyon ile birleştiğimiz dizi yapısına ise Hash Table diyoruz.

## References:
1. [hash-table-nedir](https://www.youtube.com/watch?v=_TCkO3DnVs4)
2. [hash-table-full-definition](https://www.hackerearth.com/practice/data-structures/hash-tables/basics-of-hash-tables/tutorial/)
