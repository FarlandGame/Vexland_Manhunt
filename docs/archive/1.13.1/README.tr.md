# Vexland_Manhunt — 1.13.1

> Arşiv sürüm kılavuzu · [2.0.0 →](../../README.tr.md)

[English](README.md) | [日本語](README.ja.md) | [فارسی](README.fa.md) | [Deutsch](README.de.md) | [Français](README.fr.md) | [Español](README.es.md) | [Português (Brasil)](README.pt-BR.md) | [Italiano](README.it.md) | [Nederlands](README.nl.md) | [Polski](README.pl.md) | [Українська](README.uk.md) | [Türkçe](README.tr.md) | [Русский](README.ru.md) | [简体中文](README.zh-CN.md) | [繁體中文](README.zh-TW.md) | [한국어](README.ko.md) | [हिन्दी](README.hi.md) | [Bahasa Indonesia](README.id.md)

**[Bardiya Alizadeh (Kabir) · Farland_game](https://github.com/FarlandGame) ve [Ali · Alivexor](https://github.com/Alivexor) tarafından birlikte geliştirilen, eksiksiz bir Minecraft Kaçan–Avcı deneyimi.**

Vexland_Manhunt; maç kurulumu, takım rolleri, ilk kovalamaca, takip, ilerleme, ödüller, sonuçlar ve yönetimi tek bir Paper sunucu eklentisinde birleştirir. Kaçanlar (Runner) Ender Dragon'u yenmeye çalışırken Avcılar (Hunter) son Kaçanı ortadan kaldırmaya çalışır. Eklenti birden fazla Kaçanı destekler; ölümler, yeniden doğmalar, boyut değişiklikleri ve yeniden bağlantılar sırasında kovalamacanın sürmesini sağlar. `/mhgui` kontrol merkezi, yöneticilerin menüler üzerinden maç yönetmesini sağlar; oyuncular için yerelleştirilmiş mesajlar ve rehber kitapları bulunur.

## İndirmeler ve uyumluluk

| Dosya / sürüm | İndir | Amaç |
|---|---|---|
| **1.13.1 — güncel** | [VexLandManhunt-1.13.1.jar](https://github.com/FarlandGame/Vexland_Manhunt/releases/download/v1.13.1/VexLandManhunt-1.13.1.jar) | Bardiya ve Ali tarafından geliştirilen Manhunt eklentisi |
| **GrimAC 2.3.73 — gerekli** | [grimac-bukkit-2.3.73.jar](https://github.com/FarlandGame/Vexland_Manhunt/releases/download/v1.13.1/grimac-bukkit-2.3.73.jar) | Ayrı, üçüncü taraf hile önleme bağımlılığı |
| 1.9.11 — arşiv | [VexLandManhunt-1.9.11-.jar](https://github.com/FarlandGame/Vexland_Manhunt/releases/download/v1.9.11/VexLandManhunt-1.9.11-.jar) | Önceki Manhunt derlemesi |
| 1.6.4 — arşiv | [VexLandManhunt-1.6.4.jar](https://github.com/FarlandGame/Vexland_Manhunt/releases/download/v1.6.4/VexLandManhunt-1.6.4.jar) | Daha eski Manhunt derlemesi |

**Hedef: Paper 1.21.11, Java 21.** 1.6.4, 1.9.11 ve 1.13.1 sayıları desteklenen Minecraft sürümleri değil, eklenti sürümleridir. 1.13.1 sürümünde GrimAC zorunlu bir bağımlılıktır ve köprü 2.3.73 API'sini gerektirir. **Her iki güncel JAR dosyasını** indirin. Bunlar sunucu eklentileridir; oyuncular bunları istemcinin mods klasörüne yüklemez.

Bunlar, belirli geliştiricilere özgü yükseltilmiş yönetici erişimi içeren ve sağlandıkları biçimde aynen korunan özgün kişisel sunucu derlemeleridir. Bu kılavuz Manhunt'ın herkese açık kontrollerini kapsar.

## Manhunt deneyimi

- **Kaçan ve Avcı takımları:** çevrimiçi oyuncuları iki taraftan birine atayın. Bir maç için en az bir Kaçan ve bir Avcı ya da henüz rol atanmamış çevrimiçi bir oyuncu gerekir. Bir takım arkadaşı ölürse hayatta kalan Kaçanlar devam eder; bu ölüm maçı bitirmiyorsa ölen Kaçan Avcı olur.
- **Sinematik maç başlangıcı:** envanterler ve oyun modları hazırlanır, takımlar tanıtılır ve bir rulet Kaçanların önden kaçma süresini belirler. Bu geri sayımda Avcılar dondurulur; ekrandaki başlıklar ve seslerle geri bildirim verilir. Önden kaçma süresi rastgeledir; yöneticiler Avcıları erken serbest bırakabilir.
- **Hedef seçilebilen takip pusulası:** Avcılara özel bir pusula verilir. Hedef menüsünden Kaçan seçmek ve kovalamaca sırasında hedef değiştirmek için pusulaya sağ tıklayın. Farklı boyutlarda doğrudan takip mümkün olana kadar ilgili portal rotası izlenir. Avcılar yeniden doğunca takip pusulalarını tekrar alır.
- **İlerleme göstergeleri:** bossbar'lar ve maç bilgileri Kaçanların ekipmanını; Nether kaynakları, blaze çubukları, inciler, Ender Gözleri, stronghold ve End aşamalarındaki ilerlemelerini takip eder. Yeni yapı daha ayrıntılı aşamalar ve ejderhanın canını dikkate alan ilerleme görselleri ekler.
- **Kaçanların öldürmelerine ödül:** etkin maç sırasında bir Kaçan bir Avcıyı öldürürse, ilerlemeye göre değişen ve 50 girdiden oluşan ağırlıklı ödül havuzu kullanılır. Animasyonlu çekilişler, ikili/üçlü ödüller, seri duyuruları ve nadir eşya kutlamaları dahildir.
- **Zafer ve sonuçlar:** son Kaçanın ölümü Avcılara, Ender Dragon'un yenilmesi Kaçanlara zafer kazandırır. Maç sonu başlıkları, kutlamalar, öldürme/ölüm bilgileri ve geçici eşyaların temizlenmesi bulunur. Yeni yapı ayrıca MVP, hasar ve mesafe sonuçlarını bildirir.
- **Takım iletişimi ve yardımcı araçlar:** `/teammsg` ile takım arkadaşlarına özel mesaj, `/trash` ile 54 yuvalı tek kullanımlık çöp envanteri ve `/nv` ile kişisel gece görüşü.
- **Menülerle yönetim:** roller, başlatma/sıfırlama, Avcıları erken salma, dost ateşi, sunucu kilidi, herkesi ışınlama, iyileştirme/doyurma, dil, koruma ayarları, durum ve rehberler kontrol merkezinden kullanılabilir. Dondurma ve tam sıfırlama, sonraki maçı hazırlamaya yardımcı olur.
- **Yerelleştirilmiş rehberler:** Kaçan, Avcı ve yönetici kitapları hedefleri, pusula kullanımını, ölümleri, kurulumu ve komutları açıklar. 1.9.11 sürümü, `/mhhelp` üzerinden oyuncunun rolüne uygun rehber verir.
- **Paper Anti-Xray entegrasyonu:** menü kontrolleri Paper'ın dünya düzeyindeki korumasını yapılandırır; değişikliklerin uygulanması için sunucu yeniden başlatılmalıdır.

## 1.13.1 sürümündeki yenilikler

Sağlanan 1.9.11 derlemesine kıyasla:

- **Hayalet izleyiciler:** ayrı bir rol, yönetici tarafından atama, korumalı uçuş, gizli oyuncular, durumun kaydedilip geri yüklenmesi ve sayfalı katılımcıya ışınlanma menüsü.
- **Yenilenmiş kontrol merkezi:** kategorili menüler, dört rolden açık seçim, isimli hedef seçici, yeniden bağlanma süresi seçicisi, Classic/Fast/Hardcore/Custom ön ayarları ve 30 saniyelik özel onay ekranları.
- **GrimAC entegrasyonu:** zorunlu GrimAC 2.3.73, etkin VexAC başlangıç yolunun yerini alır. Ana anahtar, beş denetim grubu, uyarılar ve izleme/yaptırım kontrolleri GUI'de sunulur. Paper Anti-Xray bağımsız kalır.
- **Yeni Smart Hunter Kit planlayıcısı:** ekipman ve malzemeleri Runner ekipmanına/büyülerine, en yakın Runner'a, takım sayılarına, uzaklığa, boyuta ve araziye uyarlar. Mevcut daha güçlü ekipmanı korur, yinelenen araçlardan kaçınır ve 30 saniyelik geçmişle tüketilebilir eşya takviyesini sınırlar. Bu, sabit ekipman farkı veya ölçülmüş denge garantisi değildir.
- **Doğrulanmış kurtarma:** SHA-256 ile mühürlenmiş anlık görüntüler, şema/durum denetimleri ve geçerli yedeğe dönüş; geçersiz veya daha yeni biçimdeki görüntüler üzerlerine yazılmadan saklanır. İzleyici durumu ayrı olarak kalıcılaştırılır.
- **Genişletilmiş mesajlar:** paketlenmiş her çeviride çevrilen anahtar sayısı 683'ten 762'ye çıkar; oyun içindeki aynı on dil korunur. İki yeni herkese açık komut kaydedilmiştir: `/mspectator <player>` ve `/mhspectate`.
- **Sıfırlama alternatifi:** Overworld doğma noktası yakınında güvenli yüzey bulunamazsa sıfırlama, ışınlanmayı zorlamak yerine atlayabilir.

## `/mhgui` ile tam kurulum ve kullanım

Sunucuyu durdurun ve dünyaların ve eklenti verilerinin yedeğini alın. Her iki güncel JAR'ı `plugins/` içine koyun; burada yalnızca bir Manhunt JAR'ı ve bir GrimAC JAR'ı bırakın. Yükseltirken mevcut `plugins/VexLandManhunt/` ayarlarını/verilerini koruyun. Paper 1.21.11 / Java 21 sunucusunu tamamen başlatın; derlemeleri değiştirirken tam yeniden başlatma yapın. GrimAC başarıyla yüklenmelidir. Eklentinin dahili adı `VexLandManhunt` olarak kalır.

Bu kılavuz **1.13.1** eklenti sürümünü İngilizce etiketlerle açıklar. Etiketler sunucu genelindeki dile uyar. Konumlarda satırlar yukarıdan aşağıya, sütunlar soldan sağa sayılır. Özel işlem belirtilmedikçe normal sol tıklamayı kullanın. Bu kılavuz statik incelemeye dayanır; Minecraft sunucusu çalıştırılmamıştır.

### Maç kurma

1. `vexland.admin` izniyle (varsayılan: OP) `/mhgui` kullanın.
2. **Player Roles** menüsünü açın, isimli oyuncu kutucuğuna tıklayın ve **Runner**, **Hunter**, **Spectator** veya **No Team** seçin. Bu, kesin rol seçicisini açar; oyuncuya tıklamak rolünü sırayla değiştirmez.
3. En az bir Runner ve bir Hunter atayın. Atanmamış çevrimiçi oyuncular maç başladığında Hunter olabilir; izleyiciler iki takımın da gerekli kontenjanını doldurmaz.
4. **Match Settings**, **GrimAC Security** ve **Global Language** ayarlarını gözden geçirin. Başlamadan önce Server Freeze'i kapatın.
5. **Match Controls → Start Match** açın. Katılımcı envanterleri hazırlanır/temizlenir, giriş oynatılır ve rulet Hunter'ların bekleme süresini seçer.

### Ana sayfa: `/mhgui` (beş satır)

| Konum | Düğme | İşlem |
|---|---|---|
| R2 C2 | Match Controls | Başlatma, duraklatma/sürdürme, serbest bırakma ve sıfırlama. |
| R2 C4 | Player Roles | Çevrimiçi oyuncuların rol listesini açar. |
| R2 C6 | Match Settings | Dost ateşi, kitler, doğma noktası, yeniden bağlanma ve ön ayarlar. |
| R2 C8 | Player Management | Hedef seçimi ve oyuncu/dünya araçları. |
| R4 C2 | GrimAC Security | Koruma ayarlarını açar. |
| R4 C4 | Global Language | Herkes için kullanılacak dili seçer. |
| R4 C6 | Administrator Guide | Yerelleştirilmiş yönetici kitabını envanterinize ekler. |
| R5 C5 | Close | Menüyü kapatır. |

R1 C5 konumundaki işaretçi maç durumunu ve Runner/Hunter sayılarını bildirir.

### Match Controls (beş satır)

| Konum | Düğme | İşlem |
|---|---|---|
| R2 C2 | Start Match | Tam diziyi başlatır. |
| R2 C4 | Pause Match / Resume Match | Oynanışı ve maç sayaçlarını duraklatır veya sürdürür; RUNNING durumundaki maçta kullanılabilir. |
| R2 C6 | Release Hunters | Geçerli Hunter bekleme süresini erken bitirir. |
| R2 C8 | Reset Match | Onay ekranını açar, ardından maçı tamamen sıfırlar. |
| R4 C2 | Server Freeze | OP olmayan oyuncular için genel dondurmayı açar/kapatır. |
| R4 C4 | Teleport Everyone | Onay ekranını açar, ardından tüm çevrimiçi oyuncuları yanınıza getirir. |
| R4 C6 | Match Info | Maç ve takım raporunu gönderir. |

**Back**, R5 C1; **Close**, R5 C9 konumundadır. Server Freeze, Pause Match'ten ayrıdır: saat ve oynanış sistemlerinin birlikte durması gerektiğinde Pause kullanın.

### Player Roles

Altı satırlı oyuncu listesi, ilk beş satırında oyuncu adına göre sıralanmış en fazla 45 isimli rol kutucuğu gösterir. Runner açık yeşil beton, Hunter kırmızı beton, Spectator Ender Gözü, No Team gri beton kullanır. Alt satırda C1'de **Previous Page**, C3'te sayfa/çevrimiçi bilgisi, C5'te **Back to Control Center** ve C9'da **Next Page** bulunur.

**Choose Player Role** ekranını (üç satır) açmak için oyuncuya tıklayın:

| Konum | Kesin rol |
|---|---|
| R2 C2 | Runner |
| R2 C4 | Hunter |
| R2 C6 | Spectator |
| R2 C8 | No Team |

Oyuncunun adı/geçerli rolü R1 C5'te görünür; **Back**, R3 C1 ve **Close**, R3 C9 konumundadır. Maç sırasında roller değişebilir. RUNNING sırasında son atanmış Runner'ı başka role geçirmek, **Last Runner: the match will end** onayını açar. Uygulamak Hunter'lara galibiyet verebilir. Doğrudan rol komutları hemen uygulanır; bu nedenle bilinçli kullanın. Burada No Team atanabilir; normal başlangıç/katılma eşitlemesi, etkin maçta atanmamış oyuncuyu Hunter'a dönüştürebilir.

### İzleyiciler

Yönetici `/mspectator <player>` ile atar veya Player Roles içinde **Spectator** seçer. Komut, tanımlayıcısında izin satırı bulunmasa da yönetici erişimini denetler. Oyuncular `/mhspectate` çalıştırarak kendilerini kaydedemez.

İzleyici, hızlı erişim çubuğunun ilk yuvasında **Spectator teleport** pusulası alır. Altı satırlı ışınlanma menüsünü açmak için ana elde tutup sağ tıklayın veya `/mhspectate` kullanın. Menü yalnızca oyuncunun Spectator rolü varken çalışır. İlk beş satırda ada göre sıralanmış, yaşayan en fazla 45 çevrimiçi Runner/Hunter bulunur; başka bir dünyada olsa bile o oyuncunun güncel konumuna ışınlanmak için isimli rol kutucuğuna tıklayın. Alt satırda C1'de **Previous Page**, C5'te **Close**, C9'da **Next Page** vardır. Uygun katılımcı yoksa R3 C5'te **No players available** yazar. Menüyü kapatmak izleyicilikten çıkarmaz.

İzleyiciler uçar, diğer oyunculardan gizlenir, çarpışmaz ve hasardan korunur. Uygulama uçuşlu Adventure modunu kullanır; vanilla Spectator kamerasını veya blokların içinden geçmeyi sağlamaz. Saldırıları, blok kırma/yerleştirmeyi, olağan blok/varlık etkileşimlerini, eşya alma/atmayı, ikinci el değiştirmeyi, envanter tıklama/sürüklemelerini, zırh askısı kullanımını ve deneyim alma/kazanmayı engeller. Yaratıklar onları hedefleyemez ve açlık değişimleri iptal edilir. `/teammsg <message>`, Spectator rolündeki diğer oyunculara ulaşır. Yarışmacılara katılımcı konumlarını veya başka dış yardımları aktarmayın.

Çıkmak için yönetici **Runner**, **Hunter** veya **No Team** atar ya da `/mrunner <player>` veya `/mhunter <player>` kullanır. Kişinin kendi çıkışı için özel komut/düğme yoktur. Çıkış, kayıtlı envanter/imleç eşyasını, konumu, oyun modunu, uçuşu, çarpışmayı ve bağışıklık durumunu geri yükler; ardından yeni rolün maç davranışını uygular. İzleyici durumu yeniden katılma için kaydedilir. Tam Match Reset, izleyici durumunu geri yükler, rolleri temizler ve çevrimiçi oyuncuları mevcutsa güvenli bir Overworld doğma noktasına taşır. Normal maç sonu temizliği, izleyicileri katılımcı eşya/uçuş işlemlerinin dışında tutar.

### Match Settings (beş satır)

| Konum | Düğme | İşlem |
|---|---|---|
| R2 C2 | Friendly Fire | Takım arkadaşına hasarı açar/kapatır. |
| R2 C4 | Smart Hunter Kit | Uyarlanabilir Hunter yeniden doğma kitlerini açar/kapatır. |
| R2 C6 | Auto World Spawn | Aralık seçimini açar. |
| R2 C8 | Reconnect Grace | Runner yeniden bağlanma süresi seçimini açar. |
| R4 C2 | Match Preset | Classic, Fast, Hardcore veya Custom seçer. |
| R4 C4 | Reset Settings | Dengeli ayarları onaylar: Kit ON, Spawn 15m, Reconnect 15m. |
| R4 C6 | Random Head Start | Bilgi kutucuğu; gecikmeyi hâlâ rulet seçer. |

**Back**, R5 C1; **Close**, R5 C9 konumundadır.

Üç satırlı **Reconnect Grace** seçicisi R2 C2–C7'de sırayla **1, 5, 10, 15, 20, 30 dakika** sunar. Tıklamak değeri kaydeder ve seçiciyi açık tutar. Back, R3 C1; Close, R3 C9 konumundadır.

Üç satırlı **Match Preset** seçicisi **Classic**, **Fast**, **Hardcore**, **Custom** seçeneklerini R2 C2, C4, C6, C8'e koyar. Classic: Kit ON, Spawn 15m, Reconnect 15m. Fast: ON, 5m, 10m. Hardcore: OFF, OFF, 5m. Custom mevcut elle yapılan ayarları korur. Ön ayarlar rastgele başlangıç avantajını korur. Seçim menüyü açık tutar; Back, R3 C1; Close, R3 C9'dadır.

**Auto World Spawn**, R2 C2, C3, C4'te OFF, 5m, 10m ve R2 C6, C7, C8'de 15m, 20m, 30m sunar. Back, R3 C5'tedir. Aralık seçin veya `/mhspawn <off|5|10|15|20|30|status>` kullanın. Overworld doğma noktasını uygun bir Overworld Runner'ının yakınına taşır; uygun oyuncu yoksa atlayabilir. `/mhkit <on|off|toggle|status>` kitleri doğrudan kontrol eder.

### Player Management (altı satır)

| Konum | Düğme | Uygulandığı hedef |
|---|---|---|
| R1 C5 | Target Player | İsimli oyuncu seçicisini açar. |
| R2 C2 | Full Heal | Tüm çevrimiçi oyuncular. |
| R2 C4 | Full Hunger | Tüm çevrimiçi oyuncular. |
| R2 C6 | Clear Effects | Tüm çevrimiçi oyuncular. |
| R2 C8 | Freeze Target | Seçilen oyuncu. |
| R4 C2 | Clear Target Inventory | Seçilen oyuncu; onay gerekir. |
| R4 C4 | Kill Target | Seçilen oyuncu; onay gerekir ve normal maç sonuçları uygulanır. |
| R4 C6 | Set Day | Bulunduğunuz dünya. |
| R4 C8 | Clear Weather | Bulunduğunuz dünya. |
| R5 C2 | Clear Dropped Items | Bulunduğunuz dünya; onay gerekir. |
| R5 C4 | Emergency Sync | Çevrimiçi oyuncuların rol/çalışma sistemlerini yeniler. |
| R5 C6 | Freeze Team | Sol: Runner'lar; sağ: Hunter'lar; Shift+tıklama: bu takım/bireysel dondurmalarını kaldırır. |

Back, R6 C1; Close, R6 C9'dadır. Hedef seçimi rolleri değiştirmez. Seçici, her sayfada 2–5. satırlar ve 2–8. sütunlarda diğer 28 çevrimiçi oyuncuyu sunar; seçip dönmek için ada tıklayın. Previous/Back/Next, R6 C1/C5/C9'dadır. İşlemi uygulamadan önce gösterilen hedefi tekrar kontrol edin.

### Onay ekranları

Reset Match, Teleport Everyone, Reset Settings, Clear Target Inventory, Kill Target, Clear Dropped Items ve GUI'de son Runner rolünü değiştirme işlemi, ayrı üç satırlı **Confirm Action** ekranını kullanır. R1 C5'te işlem/hedefi okuyun, ardından R2 C3'te yeşil **Confirm** veya R2 C7'de kırmızı **Cancel** seçeneğine tıklayın. Onay **30 saniye** sonra sona erer. Değişen/çevrimdışı hedefler veya değişen roller yeni seçim gerektirir. Bu yeni menü yolları için eski kılavuzdaki beş/sekiz saniyelik tekrar tıklama talimatlarının yerini bu alır.

### GrimAC Security ve dil

Altı satırlı Grim menüsünde durum R1 C5'tedir; anahtarlar R2 C2 **GrimAC Master**, C4 **Movement**, C6 **Combat**, C8 **Packets**; R4 C2 **Velocity / AntiKB**, C4 **World / Scaffold**, C6 **Anti X-Ray**, C8 **Admin Alerts** ve R5 C5 **Monitor mode** konumlarındadır. Back, R6 C1; Close, R6 C9'dadır. Monitor mode, uyarı/kanıt ile yaptırım arasında seçim yapar. Paper Anti-Xray bağımsızdır ve değişikliklerden sonra yeniden başlatma gerektirir. Bunlar GrimAC kontrolleridir; eski VexAC/AutoClick menü açıklaması bu sürümü anlatmaz.

Global Language herkese uygulanır ve menüleri/eşyaları yeniler. İsimli dile tıklayın; Back, R3 C5'tedir. `/mhlang` aynı seçiciyi açar, `/mhhelp` ise yerelleştirilmiş oyuncu/yönetici kılavuzunu verir.

### Güncel varsayılanlar, yeniden bağlanma ve moderasyon

`plugins/VexLandManhunt/config.yml` içindeki yeni yapılandırmanın yedek varsayılanları şunlardır:

```yaml
features:
  adaptive-hunter-kit: true
  auto-world-spawn-minutes: 0
  custom-reconnect-minutes: 15
```

`0`, doğma noktasının otomatik taşınmasının kapalı olduğunu belirtir. Reset Settings ve Classic ise 15 dakika seçer. Runner'ın yeniden bağlanma penceresinde yeri korunur; zamanında dönmesi on saniye koruma sağlar. Kaydedilen sunucu kapalı kalma süresi sayılmaz. Sürenin dolması Runner'ı Hunter'a dönüştürebilir veya maçı Hunter'ların galibiyetiyle bitirebilir. Pause/Resume oynanış sistemlerini dondurur ve etkin maç zamanlamasını ayarlar. Kurtarma dosyalarını eklenti yönetir.

Grim köprü ayarları `plugins/VexLandManhunt/grim-settings.yml` içinde saklanır. Yeni varsayılanlar Master ON, beş grubun tamamı ON, Admin Alerts ON ve **Monitor mode OFF: yaptırım etkindir** şeklindedir. Monitor mode kanıt/uyarıları kuyruğa alır ve uygun ihlal bildirimlerini iptal eder. Yaptırım modunda köprü, Grim atma komutunu yeniden bağlanmaya izin veren yerelleştirilmiş bağlantı kesmeye dönüştürebilir; kalıcı yasaklama politikası oluşturmaz. Gerçek eşikler Grim yapılandırmasına da bağlıdır. Kanıtlar `plugins/VexLandManhunt/anticheat/grim-evidence.log` dosyasına kuyruğa alınır; sınırlı kuyruklar yük altında kayıt düşürebilir. Köprü, izleyicileri, duraklatılmış/dondurulmuş oyunu ve belirli araç durumlarını muaf tutar; katılma, ışınlanma ve yeniden doğmadan sonra üç saniyelik tolerans sağlar. Hile önleme doğruluğu veya performans ölçümü iddia edilmez.

## Herkese açık komut başvurusu — 1.13.1

Yönetici erişimi OP veya `vexland.admin` anlamına gelir (varsayılan OP). `/mspectator <player>` işleyicisi, tanımlayıcı izin satırı olmasa da bunu kontrol eder. Doğrudan rol komutları hemen uygulanır; RUNNING sırasında son Runner'ı değiştirmek maçı bitirebilir. GUI bu durumda onay sunar.

| Komut | Amaç | Erişim |
|---|---|---|
| `/mhgui` | Kategorili kontrol merkezini açar | Yönetici |
| `/mhstart` | Tam maç dizisini başlatır | Yönetici |
| `/mhreset` | Maçı tamamen sıfırlar | Yönetici |
| `/mhrelease` | Bekleyen Hunter'ları serbest bırakır | Yönetici |
| `/mrunner <player>` | Runner atar | Yönetici |
| `/mhunter <player>` | Hunter atar | Yönetici |
| `/mspectator <player>` | Spectator atar | Yönetici; yeni |
| `/mhspectate` | Katılımcıya ışınlanma menüsünü açar | Mevcut Spectator; yeni |
| `/teammsg <message>` | Kendi rolünüze/takımınıza gönderir | Oyuncu |
| `/trash` | Tek kullanımlık 54 yuvalı envanter; takma adlar `/mhtrash`, `/vextrash` | Oyuncu |
| `/nv` | Kişisel gece görüşünü açar/kapatır | Oyuncu |
| `/mhlang` | Genel dil seçicisini açar | Yönetici |
| `/mhkit <on\|off\|toggle\|status>` | Uyarlanabilir Hunter kitlerini yapılandırır | Yönetici |
| `/mhspawn <off\|5\|10\|15\|20\|30\|status>` | Doğma noktası taşınmasını yapılandırır | Yönetici |
| `/mhhelp` | Yerelleştirilmiş rol/yönetici kılavuzunu verir | Oyuncu / yönetici |
| `/mhpause` | Devam eden maçı duraklatır | Yönetici |
| `/mhresume` | Duraklatılmış maçı sürdürür | Yönetici |
| `/mhdebug` | Dahili tanılama | Yönetici |

`/mhnone` bu sürümde kayıtlı değildir; GUI'deki No Team rolünü kullanın. Hunter'lar Runner seçmek için takip pusulalarına sağ tıklar; bu, izleyici ışınlanmasından ve yöneticinin hedef seçicisinden ayrıdır. Runner'lar Ender Ejderhası'nı yenerek kazanır; Hunter'lar hiç Runner kalmadığında kazanır. Başka Runner'lar kalmışsa düşen Runner, Hunter olur.

## Diller, geçmiş ve üçüncü taraf katkıları

Özgün eklenti **10 oyun içi dil** sunar: İngilizce, Farsça, Arapça, İspanyolca, Fransızca, Almanca, Rusça, Basitleştirilmiş Çince, Hintçe ve Portekizce. `/mhlang` tüm sunucu için tek dil seçer ve `language.txt` içinde saklar. GitHub kılavuzu, Arapça belge sürümü hariç **18 dil** içerir. Japonca ve diğer ek README dilleri, değiştirilmemiş JAR'lara oyun içi çeviri eklemez.

[Sürüm geçmişi](https://github.com/FarlandGame/Vexland_Manhunt/blob/main/CHANGELOG.md) sağlanan her derlemeyi kaydeder. Eski 1.9.11 / 1.6.4 kılavuzunun tamamı [sürümlü arşivde](../1.9.11/README.tr.md) korunur. Özel izleyici derlemesi artık sağlanmış ve 1.13.1 olarak yayımlanmıştır; özellikleri eski indirmelere atfedilmemelidir.

**GrimAC, GrimAC katkıcılarının GPL-3.0 altında dağıtılan bağımsız projesidir.** Bardiya ve Ali, Vexland_Manhunt'ı ve entegrasyonunu geliştirmiştir; GrimAC'nin yazarları olarak gösterilmezler. Sağlanan Grim JAR'ı, resmi Modrinth 2.3.73 Bukkit dosyasının SHA-512 ve SHA-1 değerleriyle eşleşir. Gömülü kaynak commit'i [upstream v2.3.73](https://github.com/GrimAnticheat/Grim/releases/tag/v2.3.73) ile eşleşir. Sürüm; değiştirilmemiş ikili dosyaları, sağlama toplamlarını, upstream kaynak anlık görüntüsünü, lisansı ve [üçüncü taraf bildirimlerini](../../../THIRD_PARTY_NOTICES.md) içerir. Bu bileşen bildirimleri, ayrı Manhunt projesine bir lisans atamaz.

## Dream'e eğlenceli bir meydan okuma

Bardiya'dan biraz Minecraft şakalaşması 😄

> "Ah... Ali'yle Dream'inkinden yüz kat daha iyi bir Manhunt eklentisi yaptık ama Dream korkuyor, bizimkini oynamıyor!"

## Geliştiriciler ve proje kapsamı

**[Bardiya Alizadeh (Kabir) · Farland_game](https://github.com/FarlandGame) ve [Ali · Alivexor](https://github.com/Alivexor) tarafından birlikte geliştirildi.** Her iki kullanıcı adı da özgün eklenti tanımlarında yazar olarak kayıtlıdır.

Bu depo; özgün derlenmiş sürümleri, belgelerini ve sürüm notlarını ortak bir portföy projesi olarak sunar. Özellik açıklamaları sağlanan JAR'ların statik incelemesine dayanır. Canlı sunucu uyumluluğu, kurtarma performansı, denge ve hile algılama doğruluğu bu yayımlama sürecinde test edilmemiştir.

[Bardiya'nın GitHub portföyü](https://github.com/FarlandGame) · [Ali'nin GitHub'ı](https://github.com/Alivexor) · [Tüm sürümler](https://github.com/FarlandGame/Vexland_Manhunt/releases)
