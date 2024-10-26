# ubuntu-kurulum
Neden Ubuntu?

Ubuntu, kullanıcı dostu arayüzü, geniş yazılım deposu ve güçlü topluluğu ile öne çıkan popüler bir Linux dağıtımıdır. Açık kaynak kodlu olması, kişiselleştirme seçeneklerinin zenginliği ve güvenliğiyle de tercih sebebidir.

Gerekli Malzemeler:

Ubuntu ISO Dosyası: Ubuntu'nun resmi web sitesinden en güncel sürümü indirin.
USB Bellek (En az 4 GB): Belleğin tüm içeriği silineceği için önemli verilerinizi yedeklemeyi unutmayın.
Rufus veya Ventoy: ISO dosyasını USB'ye yazdırmak için kullanacağımız ücretsiz bir araç.
Adım 1: Bootable USB Hazırlama

Windows Kullanıcıları:

Rufus'u İndirin ve Çalıştırın: Rufus'u resmi web sitesinden indirip bilgisayarınıza kurun.
USB Belleği ve ISO Dosyasını Seçin: Rufus'u açtıktan sonra, sol taraftaki listeden USB belleğinizi seçin. Sağ taraftaki "Açılış Yöntemi" bölümünden indirdiğiniz Ubuntu ISO dosyasını seçin.
Yazdırma Yöntemini Belirleyin: Yazdırma yöntemini "ISO" olarak seçin.
Başlat'a Tıklayın: İşlemi onaylayarak USB belleğinizi Ubuntu yükleme diski haline getirin.
Ventoy'u İndirin ve Çalıştırın: Ventoy'un resmi web sitesinden indirip bilgisayarınıza kurun.

Linux Kullanıcıları:

Terminal'i açın ve aşağıdaki komutu çalıştırın:

Bash
sudo dd bs=4M if=/path/to/ubuntu.iso of=/dev/sdX status=progress oflag=sync


Bu komutta:

/path/to/ubuntu.iso: İndirdiğiniz ISO dosyasının tam yolunu belirtin.
/dev/sdX: USB belleğinizin sürücü adını belirtin. lsblk komutu ile USB belleğinizin doğru sürücü adını öğrenebilirsiniz.

Ventoy:
Ventoy’u İndirin Öncelikle, Ventoy’un en güncel sürümünü resmi web sitesinden indirin. İndirdiğiniz dosya .tar.gz uzantılı olacaktır. Bilgisayarınıza kaydedin.

Dosyayı Çıkartın Terminal’i açın ve indirdiğiniz dosyanın bulunduğu dizine gidin:



cd /indirilenler
tar -xzf ventoy-x.x.x-linux.tar.gz
Bu işlem, aynı dizinde 'ventoy' adında bir klasör oluşturur.

Ventoy’u USB’ye Kurma USB belleğinizi bilgisayarınıza takın ve terminalden lsblk komutunu kullanarak aygıt adını bulun (örneğin /dev/sdX). Bu adı not edin ve Ventoy'u USB’ye kurmak için terminalde şu komutu çalıştırın:

sudo ./Ventoy2Disk.sh -i /dev/sdX
Adım 2: Bilgisayarı USB'den Başlatma

Bilgisayarı Yeniden Başlatın: Bilgisayarınızı yeniden başlatın.
BIOS/UEFI Ayarlarına Girin: Bilgisayarınızın marka ve modeline göre değişen bir tuşa (F2, F12, Del, Esc gibi) basarak BIOS/UEFI ayarlarına girin.
Boot Sırasını Değiştirin: Boot (Önyükleme) sekmesinden USB belleğini ilk sıraya taşıyın.
Veya bilgisyarın boot menüsünden önyükleme usb'sini bulun ve bilgisayarı önyüklükelenebilir usb den başlatın.
Değişiklikleri Kaydedin: Değişiklikleri kaydedip çıkın.
![Screenshot 2024-10-26 171625](https://github.com/user-attachments/assets/d83f674c-82c2-4bfd-ac3c-d351c964d530)
![Screenshot 2024-10-26 171852](https://github.com/user-attachments/assets/3e9dc4d7-f3ce-400b-9093-70d781ac3bb6)
![Screenshot 2024-10-26 171929](https://github.com/user-attachments/assets/2d18ba4a-1e7f-4da8-9ea9-54208b667566)
![Screenshot 2024-10-26 171958](https://github.com/user-attachments/assets/45e75cfb-5e7c-4d7e-a4e7-fba75ac8dfc2)

Adım 3: Ubuntu Kurulumu
![Screenshot 2024-10-26 172015](https://github.com/user-attachments/assets/0284366d-6ae6-4b83-b9d8-a40917772777)

Kurulum Ekranı: Bilgisayarınız USB'den başlatıldığında Ubuntu kurulum ekranı gelecektir. "Ubuntu'yu Kur" seçeneğini seçin.
Dil ve Klavye Düzeni: Kurulum dilini ve klavye düzeninizi seçin.
Güncellemeler ve Yazılımlar: Normal veya minimal kurulum seçeneklerinden birini tercih edin. Güncellemeleri kurulum sırasında indirmek isterseniz ilgili seçeneği işaretleyin.
Disk Bölümlendirme: Diski tamamen Ubuntu için kullanacaksanız "Diskin tamamını sil ve Ubuntu'yu kur" seçeneğini seçebilirsiniz. Daha gelişmiş bir bölümleme yapmak isterseniz "Daha Fazla Seçenek" seçeneğini kullanın.
Kullanıcı Bilgileri: Bilgisayar adı, kullanıcı adı ve şifre gibi bilgileri girin.
Kurulumu Başlatın: Kurulum işlemi başlayacaktır. Bu süre birkaç dakika sürebilir.
![Screenshot 2024-10-26 172404](https://github.com/user-attachments/assets/e5f04585-c177-4825-81eb-478b31a5044b)
![Screenshot 2024-10-26 172458](https://github.com/user-attachments/assets/ce5894cd-8257-409f-bb6a-8362edbe7ee2)

Kurulum Sonrası Adımlar

Sistem Güncellemeleri: Kurulum tamamlandıktan sonra sisteminizi güncellemek için aşağıdaki komutu terminalde çalıştırın:

sudo apt update && sudo apt upgrade
