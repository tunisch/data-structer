# Ram modeli (Random Access Machine) =/ Pc deki Ram degil ❌

- Bir algoritmayı farklı cihazlarda denemek bize pek fazla bir sonuç çıkarmıyordu. Çünkü kaynaklar değişebiliyordu. Bu probleme genel bir çözüm getirebilmek için hayalî bir cihaz düşünelim. Bu cihaz üzerinde bütün algoritmaları çalıştırdıktan sonra bize bir sonuç veriyor.
- Bu hayalî cihaza RAM (Random Access Machine) diyoruz. Ram, algoritmalar arasındaki farkları belirlemek için kullanacağımız bir araç olacak.
- Her işlemin birim zamanı var. Döngüler, kaç defa işlem yapıyorsa, (işlem sayısı * kaç kere tekrar edeceği) kadar birim zaman alır. Toplama, Çıkarma, and, or gibi aritmetik işlemler, 1 birim zaman alır.
- Genellenebilir bir analiz gapmak icin, her algoritmayi aynı bilgisayar ile test ediyor gibi yapacağız.
- Bu hayali makineye RAM (Random Access Machine) diyeceğiz.

**Ram in Ozellikleri:**
1. Her basit islem (+, -, and, or gibi) 1 birim zaman alır.
2. Döngüler 1 birim zaman değil, icerisinde kaç defa işlem oluyorsa iterasyon sayısı * işlem sayısı kadar birim zaman alır.
3. Hafızadan her okuma işlemi 1 birim zaman alır.

## References:
1. [ram-random-access-machine]()
2. [ram-model]()
