# Hash Collision
- Hash Function farklı iki değerden aynı sayı üretilirse bu duruma Collison (çarpışma) denir. Bu olay istediğimiz bir durum değildir.
    - Hash Function'lar bazen farklı durumlar için farklı sonuçlar üretemeyebilir. Örnek olarak araçları bir hash function dan geçirelim. Bu fonksiyonumuz son harflerine göre bir değer atıyor. Örneğin, motor ve tır için aynı değerleri ataması collision'a neden oluyor.
    - Collision sorunuyla az karşılaşabilmek için kaliteli bir hash function olmalı. Bu sayede verimli bir Hash Table elde etmiş oluyoruz.
    - Çarpışma sayısı arttıkça aradığımız şeyi bulma hızı azalır.
    - Collision oldugunda ya array boyutu arttirilir ya da her bir input farkli degerlere map edilir(array boyutu arttirmak)
    - Ya da `linked list` kullanarak da collision cozulebilir(node ile referanslar verilir) ama bu performans acisindan ve karmasik projelerde tercih edilmez cunku index cakismasi cok olacak zaten bu durum collision .
## References:
1. [Wiki](https://en.wikipedia.org/wiki/Hash_collision)
2. [Detail-collision](https://freemanlaw.com/hash-collisions-explained/)
