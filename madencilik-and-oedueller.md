# Madencilik & Ödüller

### Madencilik & Ödüller

Meson Network için en uygun madenciler kimlerdir?

* Devamlı ağ kullanan bant genişliği kullanıcıları
* Ev kullanıcıları için Statik IP
* IoT cihazlarının sahipleri
* Adanmış sunucuların sahipleri
* IDC sunucularının (kurum/kuruluş/okullar) sahipleri.

En istikrarlı hizmet sağlayıcılarımız olmaya davetliler. Sonuç olarak bu boşta kalan kaynaklardan en iyi şekilde yararlanmamız ile birlikte, Meson Network Projesi'nin planına ve konumlandırmasına göre ekonomik ve sağlıklı bir model haline gelir.

### Ön koşul

* Statik (Genel) IP veya A DHCP ön koşulu
* Güvenlik duvarının portunun açılması (varsayılan: 443, özel sunucu portları için destek)
* Yeterli miktarda depolama sağlamak ( varsayılan minimum gereksinim: 20 GB)

### Madencilik kuralları

Lütfen detaylar için "mining rules" 'u kontrol edin.

Madencilik Puanı = Bant Genişliği Puanı \* Depolama Puanı \* Kredi Puanı

Temel olarak, bant genişliği, Bant genişliği puanı ile ilgili en önemli unsurdur.

Ayrıca, depolama alanı dosyaları önbelleğe almak için gereklidir karşılığında depolama puanı kazanılır.

Ek olarak, sabit ve istikrarlı sunucular daha yüksek Kredi puanına sahip olacaktır.

Ayrıca, farklı bölgelerdeki sunucular için bazı ödül ayarlamaları olacak.

| Ağ                                         | Test Ağı                                                                                                                                                                                                                                                                                                                                       |
| ------------------------------------------ | ---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Öğe                                        | Değer                                                                                                                                                                                                                                                                                                                                          |
| Madencilik puanı                           | Madencilik Puanı = Bant Genişliği Puanı \* Depolama Puanı \* Kredi Puanı                                                                                                                                                                                                                                                                       |
| Bazı madencilik nodelarının kazanç yüzdesi | ![](https://docs.meson.network/assets/percentage.cbded1c4.svg)                                                                                                                                                                                                                                                                                 |
| Bant genişliği puanı                       | ![](https://docs.meson.network/assets/bandwidth-score.822a3b3e.svg)                                                                                                                                                                                                                                                                            |
| Bant genişliği üst sınırı                  | Bant genişliği puanı, bant genişliği 1500 Mb/s'ye ulaştıktan sonra artmaz                                                                                                                                                                                                                                                                      |
| Depolama puanı                             | ![](https://docs.meson.network/assets/storage-score.3a4dfe1b.svg)                                                                                                                                                                                                                                                                              |
| Minimum depolama gereksinimi               | 20 GB                                                                                                                                                                                                                                                                                                                                          |
| Credit Score                               | ![](https://docs.meson.network/assets/credit-score.9b760e1e.svg) Eğer node'unuz çevrimiçi ve devamlı olarak çalışıyorsa kredi maksimum 10000000 değerine kadar kademeli olarak artacaktır. Node'unuz çevrimdışı olduğunda ise, kredi 0'a kadar kademeli olarak azalacaktır. Bu node'unuzu daha fazla token almak için istikrarlı hale getirir. |
| Örnek                                      | Bant genişliğiniz 200Mb/s ise, "Bant genişliği puanı" 200 olacaktır. Depolamayı 60 GB olarak ayarlarsanız "Depolama puanı" 0,85 olur. Krediniz 500000 ise, "Kredi puanı" 0,7 olacaktır. Madencilik puanı = 200 \* 0.85 \* 0.7 = 119                                                                                                            |

Tüm TestAğı Tokenleri, Ana ağ tokenlerinin %1 i ile eşleştirilecektir. FAQ-Token'e göre başlangıçta 100,000,000 Meson Token'i olacak ve bunun 1.000.000 Token'i Ana Ağ Tokenlerinin değişimi olarak kullanılacak.

Ana Ağ Tokenleriniz = (TestAğı Tokenleriniz / Tüm TestAğı Tokenleri) \* (%1 \* Tüm Ana Ağ Tokenleri) = (Ana ağ Tokenleriniz / Tüm TestAğı Tokenleri) \* 1.000.000

Örneğin, en sonunda toplam 160.000.000 TestAğı Tokeni olacağını ve o zaman 2.000.000 TestAğı Tokenine sahip olduğunuzu varsayalım. Bu durumda (2.000.000 / 160.000.000) \* 1.000.000 = 125.000 Ana Ağ Tokeni elde edeceksiniz.
