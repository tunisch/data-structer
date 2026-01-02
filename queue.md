# QUEUE

- Queue (Kuyruk), FIFO (First in First out) (İlk giren ilk çıkar) prensibine dayanan, girişlerde ve çıkışlarda belirli bir kurala göre çalışan yapıdır. Stack de verdiğimiz örneği kuyruğa göre uyarlayalım. Biz örnekte Örneğin sinema bileti almak için sıraya girmiş kişileri düşünebiliriz. İlk önce gelen kişi bileti daha önce alacaktır.
- Queue (Kuyruk)'da eleman eklemesi yaparken enqueue methodunu kullanıyoruz. Eleman silerken ise dequeue methodunu kullanıyoruz. Siradaki elemani getirmek icin ise peek methodunu kullaniyoruz.
- Queue veri yapısında, verilere iki uçtan erişim vardır. Bir uçtan eleman ekleme (enqueue), diğer uçtan eleman çıkarma (dequeue) işlemleri yapılır. Siradaki elemani getir (peek) islemleri ile yapilir.
- Queue tasarımı dizi veya bağlı liste ile yapılabilir. Bağlı liste kullanarak boyutu sabit olmayan bir queue oluşturabiliriz. Dizi kullanmak için ise sabit bir boyut belirlemeliyiz.

## Öncelikli Kuyruk (Priority Queue)
- Bazı problemlerin çözümünde doğrudan kuyruk oluşturamayız. Örneğin uçakların inişi sırasında, acil inmesi gereken uçaklar bulunabilir. Veya muayene sırasında bekleyen hastalar için farklı bir öncelik belirlenebilir.
- Bu gibi senaryolarda öncelikli kuyruk ile çözüm üretilir. Öncelik sırası belirlenir ve program sırasında uygulanır.

<img width="254" height="84" alt="image" src="https://github.com/user-attachments/assets/f9ebd15b-0439-4d69-85fd-dc3d67d7539f" />

- Sıradaki eleman, front olarak tuttuğumuz düğüm demektir. Dolayısıyla front düğümünün değerini return ile döndürürsek, silme işlemi uygulamadan sıradaki elemanı elde ederiz.

**Avantajları:**

- Geliş sırasına göre hizmet verilmesi gereken senaryolarda avantajlıdır.
- Üretici-tüketici problemlerinde fayda sağlar.
- Hastanelerde, uçakların inişinde, araç geçişlerinde öncelikli kuyruk kullanılabilir.

**Dezavantajları:**
 
- Üzerinde arama yapmak zahmetlidir. En baştan başlanıp ilerlemek gerekir.
- Kuyruğun aralarına eleman eklemek karmaşıktır.

**Kullanım Alanları:**

- İşletim sistemlerinde çalışma önceliği kuyruk ile yapılır.
- Ağ yazıcılarında, belgeler öncelikli kuyruk ile çalışır.
- Asansör yazılımı kuyruk ile yapılabilir.

<img width="518" height="431" alt="image" src="https://github.com/user-attachments/assets/6bd77f83-631f-4d81-aa09-e8157b4a5170" />

### References:

1. [queue-kod-ile-anlatım](https://medium.com/@tolgahan.cepel/do%C4%9Frusal-veri-yap%C4%B1lar%C4%B1-4-kuyruk-queue-dcbd07e8ba77)
2. [queue-short-definition](https://www.educative.io/edpresso/what-is-a-queue)
3. [queue-detail-definition](https://www.studytonight.com/data-structures/queue-data-structure)
