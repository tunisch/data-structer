# Algoritma Analizi

- Algoritma analizi, var olan kaynaklara göre en uygun algoritmayı seçmek için uygulanır. Peki algoritma analizi en iyi nasıl yapılır? Kulağa karmaşık geliyor ama çok basit. Programlama dillerinden ve donanımlardan bağımsız bir şekilde Algoritma analizi yapılmalıdır. Aksi taktirde en uygun sonuç alınamayabilir.
- Donanımlar veya programlama dilleri farklı cihazlarda aynı performansı vermeyebilir. Örnek verecek olursak, cep telefonları için uygulama tasarladığımızı varsayalım. Bu uygulamanın performansı Apple telefonlar için farklı, Android telefonlar için farklı, arasında donanım farklı olanlar için ayrı olacaktır. Donanım ve diller ile algoritma analizi pek sağlıklı değildir.
- Algoritma analizi, bir algoritmanın çalışabilmesi için gerekli koşulların sağlanıp sağlanamadığını gösteren bir parametredir.

- Aslında belli bir makinede çalıştırılabilir algoritmaların performansı için dikkat etmemiz gereken kriterler arasında ‘programlama dili seçiminin’ yanı sıra birçok teknoloji detayı vardır ki bunlar; derleyici seçimi, kodu hangi hızda çalıştırdığımız, belleğin ne kadar hızlı olduğu ve hatta önbelleğe alma işleminin miktarı olarak sıralanabilir.

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
