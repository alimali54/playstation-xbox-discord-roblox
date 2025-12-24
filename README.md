Bu araç Playstation trafiğini PC üzerinden geçirerek internete çıkarır. Böylece PC'de GoodbyeDPI ile erişim engelini aştığınızda Playstation'da da aşmış olursunuz.

GoodbyeDPI'ı sadece Roblox ve Discord domainleri etkileyecek şekilde yapılandırdım. Playstation'un tüm trafiği PC'den geçse de sadece Roblox ve Discord domainleri DPI bypass işleminden etkilenir, normal trafik etkilenmez.

| Trafik Türü | İşlem (DPI Bypass) | Sonuç |
| :--- | :---: | :--- |
| **Discord (Sesli Sohbet & API)** | ✅ AKTİF | Bağlantı sorunları çözülür. |
| **Roblox (Web & Oyun)** | ✅ AKTİF | Erişim engeli aşılır. |
| **PSN Servisleri (Store, Güncelleme)** | ❌ PASİF | Orijinal hızda ve doğrudan bağlanır. |
| **Online Oyun Trafiği (Ping/Lag)** | ❌ PASİF | Paketler ellenmez, gecikme yaşanmaz. |
| **Video Akış (Youtube, Netflix)** | ❌ PASİF | Bypass işlemine girmeden standart akar. |

> [!NOTE]
> **Gecikme Hakkında:** Trafik bilgisayarınız üzerinden köprülenerek geçtiği için, bilgisayarınızın donanım performansına ve ağ kalitesine bağlı olarak çok minimal bir gecikme (ping) artışı yaşanabilir. En iyi performans için hem PC'nin hem de konsolun kablolu (Ethernet) bağlantı veya 5 Ghz Wi-Fi kullanması önerilir. 

PC ve Playstation'un aynı ağda olması yeterlidir. PC'yi kablo ile PS'e bağlama veya PC'den hotspot açma gibi işlemlere ihtiyaç yoktur.
Playstation'da NAT tipi bozulmaz. Kendi denemelerimde normalde NAT 2 alırken işlemler sonrasında da NAT 2 alıyorum.


<img width="502" height="527" alt="Ekran Alıntısı" src="https://github.com/user-attachments/assets/58027d21-c7b2-4138-8dbf-cd6a79489e5e" />


Gereksinimler
1.  **PC:** 64 Bit Windows işletim sistemi.
2.  **Sürücü:** [Npcap](https://npcap.com/) yüklü olmalıdır.

Kullanım Talimatları

1.  Programı **Yönetici Olarak** çalıştırın.
2.  Güvenlik duvarı uyarıları gelirse "Erişime İzin Ver" butonuna tıklayın.
3.  Program "SİSTEM ÇALIŞIYOR" mesajını verene kadar bekleyin.
4.  Konsolunuzun (PS/Xbox) ağ ayarlarına gidin ve **Manuel** kurulumu seçin:

| Ayar | Değer |
| :--- | :--- |
| **IP Adresi** | `172.24.2.10` (veya 172.24.2.2 - 255 arası herhangi bir sayı) |
| **Alt Ağ Maskesi** | `255.255.0.0` |
| **Ağ Geçidi** | `172.24.2.1` |
| **Birincil DNS** | *Programın sonunda verilen Local IP* |
| **İkincil DNS** | *Programın sonunda verilen Local IP* |

Kurulum (Geliştiriciler İçin)

Kaynak kodundan derlemek isterseniz:
1. [AutoIt v3](https://www.autoitscript.com/site/autoit/) indirin ve kurun.
2. `.au3` dosyasını `Compile Script to .exe` seçeneği ile derleyin.


## 📜 Credits & Acknowledgments

Bu proje, aşağıdaki harika açık kaynaklı araçları bir araya getirerek çalışmaktadır:

* **[GoodbyeDPI](https://github.com/ValdikSS/GoodbyeDPI)** - ValdikSS tarafından geliştirilen pasif DPI engelleyici.
* **[dnscrypt-proxy](https://github.com/DNSCrypt/dnscrypt-proxy)** - DNS trafiğini şifrelemek ve güvenli DNS kullanmak için.
* **[go-pcap2socks](https://github.com/DaniilSokolyuk/go-pcap2socks)** - Pcap trafiğini SOCKS vekillere yönlendiren ağ köprüsü.
* **[Npcap](https://npcap.com/)** - Windows için paket yakalama kütüphanesi.

Bu araçların her biri kendi lisansları altında korunmaktadır. Onların emeği olmadan bu proje mümkün olmazdı.
