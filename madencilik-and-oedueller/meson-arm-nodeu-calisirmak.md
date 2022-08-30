# Meson ARM nodeu çalışırmak

#### Meson ARM Node'u çalıştırmak

#### Konuşlandırma gereksinimleri

* Statik (Genel) IP veya A DHCP ön koşulu
* ARM tabanlı cihazlar (Raspberry Pi/Soft Router/Jetson Nano etc.)
* Güvenlik duvarının portunun açılması (varsayılan: 443, özel sunucu portları için destek)
* Yeterli miktarda depolama sağlamak (varsayılan minimum gereksinim: 20 GB)

#### Desteklenen Unix/Linux işletim sistemleri

| OS              | Website                                |
| --------------- | -------------------------------------- |
| Ubuntu          | https://ubuntu.com/download/server/arm |
| Debian          | https://www.debian.org/ports/arm       |
| Raspberry Pi OS | https://www.raspberrypi.com/software   |
| Fedora          | https://arm.fedoraproject.org          |
| OpenWrt         | https://openwrt.org                    |
| Armbian         | https://www.armbian.com                |
| DietPi          | https://dietpi.com                     |
| Manjaro         | https://manjaro.org/download/#ARM      |
| Arch Linux      | https://archlinuxarm.org               |
| openSUSE        | https://get.opensuse.org               |
| Asahi Linux     | https://asahilinux.org                 |

#### Kayıt

https://dashboard.meson.network/register

![](https://docs.meson.network/assets/run-meson-node-01.523c807a.png)

"Nodes" butonuna tıklayın ve bu sayfada token ve kurulum eğitimini bulabilirsiniz.

![](https://docs.meson.network/assets/run-meson-node-02.9bf14d62.png)

#### ARM üzerine Meson nasıl kurulur? (Linux)

#### 1. İndirmek & Kurmak

#### Linux ARM 64-bit

`wget 'https://staticassets.meson.network/public/meson_cdn/v3.1.18/meson_cdn-linux-arm64.tar.gz' && tar -zxf meson_cdn-linux-arm64.tar.gz && rm -f meson_cdn-linux-arm64.tar.gz && cd ./meson_cdn-linux-arm64 && sudo ./service install meson_cdn`

#### Linux ARM 32-bit

`wget 'https://github.com/daqnext/meson-terminal/releases/download/v3.1.18/meson_cdn-linux-arm.tar.gz' && tar -zxf meson_cdn-linux-arm.tar.gz && rm -f meson_cdn-linux-arm.tar.gz && cd ./meson_cdn-linux-arm && sudo ./service install meson_cdn`

uname -m çıktısını kontrol edin. Sonuç aarch32 ise, ARM Linux çekirdeğini 32 bit'te çalıştırıyorsunuz ve eğer sonuç aarch64 veya arm64 ise de çekirdeği 64 bit modunda çalıştırıyorsunuz. ARM işlemci [listesine](https://en.wikipedia.org/wiki/List\_of\_ARM\_processors) göz atın.

#### 2. Token ayarlama ve yapılandırma

`sudo ./meson_cdn config set --token=your token --https_port=443 --cache.size=30`

İnternet servis sağlayıcınız Statik IP sağlamadığında 443 dışında başka portlar ayarlamanız gerekebilir. Geçerli değerler 1 ile 65535 arasındadır.

`sudo ./meson_cdn config set --token=your token --https_port=1943 --cache.size=30`

#### Parametre listesi:

`-token=your token # you can find out your token in nodes page -https_port=443 # default is 443, support for custom server ports -cache.size=30 # minimum: 20G, default: 30G -cache.folder=xxxx # string, cache folder path, could be an absolute path`

#### 3. Hizmeti başlatmak

`sudo ./service start meson_cdn`

Router'ınızdaki portlar nasıl yönlendirilir?

Port yönlendirme ayarlamalarını öğrenmek için [https://portforward.com/](https://portforward.com/router.htm?utm\_source=meson.network) adresine ya da Router'ınızın talimatlarına göz atın.

#### Örneğin Cisco DPC3941T XFINITY router'ını ele alalım, port yönlendirme için temel süreç:

**1. Cisco DPC3941T XFINITY router'ınıza giriş yapın.**

Varsayılan IP Adresi: `10.0.0.1` Varsayılan Kullanıcı Adı: `admin` Varsayılan Şifre: `password`

**2. Port yönlendirme bölümüne gidin.**

Şimdi router'ınızda port yönlendirme bölümünü bulmamız gerekiyor. Nasıl yapacağınız aşağıda. Router'ınızdaki ilk sayfadan başlayarak:

![](https://docs.meson.network/assets/run-meson-arm-nodes-01.feb2414d.png)

Sayfanın solundaki "Advanced" bağlantısına tıklayın.

Şimdi yeni bir menü görmelisiniz. Bu yeni menüde, "Port Forwarding" 'e tıklayın.

![](https://docs.meson.network/assets/run-meson-arm-nodes-02.efae9b34.png)

Sayfanın ortasına yakın bir yerde bulunan "Add service" düğmesini tıklayın.

![](https://docs.meson.network/assets/run-meson-arm-nodes-03.9f1a8a66.png)

#### 3. Port yönlendirme girdisi oluşturun.

"Common service" açılır kutusundan, "Other" 'ı seçin.

Bu yönlendirmeyi neden kurduğunuzu hatırlayabilmeniz için "Service name" kutusuna bu yönlendirme için bir ad girin.

Yönlendirdiğiniz portların protokol türünü seçmek için "Service Type" açılır kutusunu kullanın.

Portları yönlendirdiğiniz IP adresini "Server IP Adress Box" 'a girin.

Tek bir port yönlendiriyorsanız bu port numarasını "Start Port" ve "End Port" kutularına girin.

Örnekte, varsayılan ortu `1943` olarak değiştirdim.

TCP Portları : `1943` UDP Portları : `1943`

İşiniz bittiğinde Save butonuna tıklayın.

Portlarınız şimdi açık olmalıdır. Portlarınızın açık olup olmadığını test edin.

2-3 dakika sonra yeni node'da açılan terminallerde yeni bir terminal kaydınız olur.

![](https://docs.meson.network/assets/run-meson-node-03.5107cf26.png)
