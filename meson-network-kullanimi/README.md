# Meson Network Kullanımı

#### Tüm websiteyi hızlandırın

Meson Network tarafından hızlandırılacak herhangi bir şey, URL'yi değiştirmek kadar basit olabilir.&#x20;

#### Meson CDN'e Kaydolun

Meson CDN kontrol paneline kaydolun ve oturum açın.

https://dashboard.meson.network/register

![](https://docs.meson.network/assets/using-01.039eee42.png)

#### Pull zone oluştur

Pull zones'a tıkla ve Pull Zone List'e göz at.

![](https://docs.meson.network/assets/using-02.f6e4be40.png)

Create pull zone' a tıkla ve hızlandırmak istediğiniz Web Sitesi Domain'ini girin.

![](https://docs.meson.network/assets/using-03.48eb0d77.png)

Kaynak url sekmesiz belirtilmelidir. örneğin, https://www.domain.com/

#### Örnek: Meson, IPFS'yi geliştirir.

IPFS'e, sık sık çağırılan dosyaları Meson'a depolayan bir önbellek katmanı (diğer bir deyişle ikinci katman) ekledik. İçerik teslimi için hızı optimize etmek ve temel depolama katmanında (IPFS) maliyet/baskıdan tasarruf etmek faydalı olabilir.

Kaynak URL'yi tanımla (e.g. https://ipfs.io)

![](https://docs.meson.network/assets/using-04.c894583c.png)

"Add" butonuna tıkla, "Pull zone URL"yi alın.

![](https://docs.meson.network/assets/using-05.45306885.png)

Orijinal sekmeyi yenisiyle değiştirin.

`https://ipfs.io/ipfs/QmXoypizjW3WknFiJnKLwHCnL72vedxjQkDDP1mXWo6uco/wiki/ => https://pz-rlhgrj.meson.network/ipfs/QmXoypizjW3WknFiJnKLwHCnL72vedxjQkDDP1mXWo6uco/wiki/`

Şimdi bu yeni url'yi isteyin. Meson'un dosyayı küresel olarak dağıtılmış terminallere dağıtması için biraz zamana ihtiyacı var.

`https://spec00-bfhkcefkbefkfxx-06-rlhgrj.mesontracking.com/ipfs/QmXoypizjW3WknFiJnKLwHCnL72vedxjQkDDP1mXWo6uco/wiki/_m_access_key_caavymwyao`

Bağlantı, isteği yerine getirmek için belirli bir node'a atlar,spec00-bfhkcefkbefkfxx-06-rlhgrj node'un kısaltılmış ve sabit değeridir.

![](https://docs.meson.network/assets/using-06.436f95f6.png)
