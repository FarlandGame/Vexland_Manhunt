# Vexland_Manhunt


[English](../README.md) | [日本語](README.ja.md) | [فارسی](README.fa.md) | [Deutsch](README.de.md) | [Français](README.fr.md) | [Español](README.es.md) | [Português (Brasil)](README.pt-BR.md) | [Italiano](README.it.md) | [Nederlands](README.nl.md) | [Polski](README.pl.md) | [Українська](README.uk.md) | [Türkçe](README.tr.md) | [Русский](README.ru.md) | [简体中文](README.zh-CN.md) | [繁體中文](README.zh-TW.md) | [한국어](README.ko.md) | [हिन्दी](README.hi.md) | [Bahasa Indonesia](README.id.md)

<!-- PLAYFUL_INTRO_START -->
<p><img src="https://raw.githubusercontent.com/FarlandGame/Vexland_Manhunt/main/assets/portfolio-sticker.svg" width="88" height="88" alt=""></p>

> Avcılar pusula getirir. Kaçanlar ise bir plan… ve her ihtimale karşı bir bahane. 🎮🧭
<!-- PLAYFUL_INTRO_END -->

**[Bardiya Alizadeh (Kabir) · Farland_game](https://github.com/FarlandGame) ve [Ali · Alivexor](https://github.com/Alivexor) tarafından birlikte geliştirilen, eksiksiz bir Minecraft Kaçan–Avcı deneyimi.**

Vexland_Manhunt; maç kurulumu, takım rolleri, ilk kovalamaca, takip, ilerleme, ödüller, sonuçlar ve yönetimi tek bir Paper sunucu eklentisinde birleştirir. Kaçanlar (Runner) Ender Dragon'u yenmeye çalışırken Avcılar (Hunter) son Kaçanı ortadan kaldırmaya çalışır. Eklenti birden fazla Kaçanı destekler; ölümler, yeniden doğmalar, boyut değişiklikleri ve yeniden bağlantılar sırasında kovalamacanın sürmesini sağlar. `/mhgui` kontrol merkezi, yöneticilerin menüler üzerinden maç yönetmesini sağlar; oyuncular için yerelleştirilmiş mesajlar ve rehber kitapları bulunur.

## İndirmeler ve uyumluluk

| Sunulan sürüm | İndirme | Kurulum |
|---|---|---|
| **2.0.0 — birleşik paket** | [VexLandManhunt-2.0.0.jar](https://github.com/FarlandGame/Vexland_Manhunt/releases/download/v2.0.0/VexLandManhunt-2.0.0.jar) | Entegre GrimAC 2.3.73 içeren **tek JAR** |
| **1.13.1 — spectator dalı** | [Sürüm ve iki JAR](https://github.com/FarlandGame/Vexland_Manhunt/releases/tag/v1.13.1) | Manhunt ve ayrı GrimAC 2.3.73 |
| 1.9.11 / 1.6.4 — eski | [Tüm sürümler](https://github.com/FarlandGame/Vexland_Manhunt/releases) | Geçmiş bağımsız derlemeler |

**Paper 1.21.11 / Java 21.** Bunlar istemci modları değil, sunucu eklentileridir. Sunulan dosyanın adı ve yayımlanan sürüm **2.0.0** olsa da, değiştirilmemiş tanımlayıcı **`1.9.11-grim.1`** değerini bildirir ve oynanış temelini 1.9.11 olarak belirtir. Bu birleşik paket, özel Spectator rolünü, `/mspectator <player>`, `/mhspectate`, kategorilere ayrılmış menüleri veya diğer 1.13.1 eklemelerini **içermez**. Bu özelliklere ihtiyacınız varsa ayrıca listelenen 1.13.1 dalını kullanmaya devam edin.

Oluşturucuya özel yükseltilmiş yönetici erişimi içeren özgün kişisel sunucu derlemeleri, sunuldukları haliyle korunmuştur. Bu kılavuz herkese açık kontrolleri kapsar.

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

## Sunulan 2.0.0 paketinde neler değişti?

- **Tek entegre JAR:** Manhunt, değiştirilmiş GrimAC 2.3.73 ve pakete dahil PacketEvents tek bir Bukkit eklenti örneğini paylaşır. Bu paket için ayrı GrimAC veya PacketEvents kurulumu gerekmez. Tanımlayıcı `GrimAC` sağlar; arşiv düzleştirilmiştir, içinde değiştirilmemiş ayrı bir Grim JAR barındırmaz.
- **Modül durumu:** yönetici komutu `/vexintegration`, Grim ACTIVE/INACTIVE durumunu, Bukkit sahibini, VexAC durumunu, PacketEvents durumunu ve izlenen oyuncu sayısını bildirir. Yerel `/grim` ve `/grimac` komutları entegre modül tarafından kaydedilir.
- **Kontrollü başlatma:** yükleyici Paper yapılandırma API'sini ve tam olarak Minecraft 1.21.11 sürümünü gerektirir. Çevrimiçi oyuncular varken çalışırken yüklemeyi ve ayrı bir GrimAC örneğini reddeder. Entegre başlatma başarısız olursa eklenti devre dışı bırakılır ve Grim korumasının etkin olmadığı günlüğe yazılır; sunucunun kendisi çalışmaya devam edebilir. Maç başlatmadan önce durumu doğrulayın.
- **Mevcut veri aktarımı:** ilk entegre yüklemede, aktarım her iki eski eklenti veri ağacını yedekler ve eski GrimAC verilerini yalnızca entegre hedef mevcut değilse kopyalar. Her ikisi de varsa mevcut entegre veriler önceliklidir; birleştirme veya üzerine yazma yapılmaz. Özgün veriler korunur.
- **Hareket düzeltme yetkisi:** `plugins/VexLandManhunt/integration.properties` varsayılan olarak `movement-correction-owner=legacy` kullanır. Desteklenen alternatif `grim` değeridir; diğer değerler başlatmayı durdurur. grim seçildiğinde VexAC'nin geri alma/ışınlama düzeltme yolları bastırılır; VexAC kontrolleri, uyarıları ve kanıtları korunur. Bu, eski sistemin tüm cezalarını devre dışı bırakmaz.
- **Oynanış temeli:** düz `/mhgui`, Runner/Hunter rol döngüsü, VexAC kontrolleri, Smart Hunter Kit V3, duraklatma/sürdürme, kurtarma ve 683 çevrilmiş anahtar 1.9.11 sürümünü izler. Bu, spectator destekli 1.13.1 özellik kümesi değil, birleşik paketleme/entegrasyon sürümüdür.

## 1.9.11 temelinden korunan oynanış

Aşağıdaki sistemler 1.9.11 temeline eklenmiş olup bu birleşik pakette korunmaktadır. Bunlar yeni 2.0.0 spectator özellikleri değil, devralınan oynanış özellikleridir.

| Eklenen veya değişen özellik | 1.9.11 sürümündeki davranış |
| --- | --- |
| **Smart Hunter Kit V3** | Uyarlanabilir yeniden doğma kitleri; Kaçan ekipmanını, takımları ve maçın bağlamını dikkate alır. Sistem Avcı kitlerini Kaçanların ortalama ekipmanının altında tutmayı amaçlar; `/mhkit` veya arayüzle açılıp kapatılır. |
| **Otomatik Overworld doğma noktası** | Dünya doğma noktası, uygun bir Overworld Kaçanının yakınına seçilen aralıkta taşınır: kapalı, 5, 10, 15, 20 veya 30 dakika. Sistem güvenli bir yüzey adayı seçer ve uygun olmayan durumları atlar. |
| **Duraklatma ve sürdürme** | `/mhpause`; oynanışı, maça bağlı sayaçları, takibi ve doğma noktası hareketini dondurur; `/mhresume` devam ettirir. Duraklatılmış süre etkin maç süresinden düşülür. |
| **Yeniden başlatma/çökme kurtarma** | Kurtarma katmanı; ana/yedek anlık görüntüler, periyodik kayıtlar ve kapanış kayıtlarıyla maç durumunu, rolleri, pusula hedeflerini, ilerlemeyi, ödül/ölüm sayaçlarını ve yeniden bağlantı durumunu geri yükler. |
| **Kaçanın yeniden bağlantı ayarları** | Yapılandırılabilir süre, önceki sabit 60 dakikalık sürenin yerini alır. Yeni kurulum varsayılanı 15 dakika ve geri dönüşte 10 saniyelik korumadır. Sunucunun kapalı kaldığı süre sayılmaz; sürenin dolması Kaçanı Avcıya dönüştürebilir veya maçı bitirebilir. |
| **Genişletilmiş yönetim** | Son Kaçanı koruyarak devam eden maçta rol değiştirme; seçilen oyuncu işlemleri, takım ışınlama/dondurma, çalışma zamanı durumunu yeniden eşitleme ve kısayollar maç yönetimini geliştirir. |
| **Onaylı ayar sıfırlama** | Sekiz saniyede iki tıklama; Smart Kit AÇIK, otomatik doğma noktası 15 dakikada bir ve yeniden bağlantı 15 dakika ayarlarını uygular. Bu, yeni kurulumdaki otomatik doğma noktası KAPALI varsayılanından farklıdır. |
| **VexAC 3.0** | Hareket, savaş, AutoClick, hız/geri tepme ve dünya inşası denetimleri; grup/ana kontroller, kanıt kaydı, yönetici uyarıları ve ortam/gecikme istisnaları. |
| **Ultra Deep Debug v4** | `/mhdebug`; durum makinesi, arayüz, sentetik kit/yük, dil yer tutucuları, kurtarma kaydetme/geri yükleme döngüsü ve bütünlük tanılama araçları sağlar. |
| **Genişletilmiş göstergeler** | Daha ayrıntılı ilerleme, ejderha canı görselleri, MVP/hasar/mesafe sonuçları ve TAB ping bilgisi. |
| **Komut değişiklikleri** | `/mhkit`, `/mhspawn`, `/mhpause`, `/mhresume` ve `/mhdebug` eklenir; `/mhnone` kaldırılır; `/mhhelp` oyuncu/yöneticiye uygun hâle gelir ve `/trash` için takma adlar eklenir. |
| **Daha çok yerelleştirilmiş mesaj** | Çeviri kaynakları dil başına 446 mesaj anahtarından 683'e çıkar. |

VexAC'ın paketlenmiş denetimleri Fly, Speed, Timer, Phase, Step, NoSlow, GroundSpoof, Reach, KillAura, AimAssist, duvar arkasından vurma, BadPackets, AutoClick zamanlama örüntüleri, değiştirilmiş geri tepme, Scaffold, Tower, FastPlace, Nuker ve blok erişimini kapsar. Arayüz yalnızca izleme etiketi kullanırken derlenmiş kodda oyuncuyu sunucudan atma yolları da vardır; bu etikete güvenmeden önce gerçek moderasyon davranışını test sunucusunda doğrulayın. Eski yapı bunun yerine eski Anti AutoClick ve Anti Fly kontrollerini içerir.

## `/mhgui` ile eksiksiz kurulum ve kullanım

### 1. Birleşik derlemeyi kurun

1. **Paper 1.21.11 / Java 21** sunucusunu tamamen durdurun; dünyaları ve eklenti verilerini yedekleyin.
2. Bu sürümden yalnızca `VexLandManhunt-2.0.0.jar` dosyasını `plugins/` içine koyun. Eski Manhunt ve bağımsız GrimAC JAR dosyalarını etkin eklenti dizininin dışına taşıyın. Veri klasörlerini koruyun; silmeyin. Oyuncular bu JAR dosyasını istemciye kurmaz.
3. `/reload` kullanmak yerine normal şekilde başlatın. Entegre yükleyici, Grim ve PacketEvents yaşam döngüsünü yönetir.
4. OP olarak veya `vexland.admin` izniyle `/vexintegration` çalıştırın. `Grim=ACTIVE` ve `PacketEvents=true` değerlerini kontrol ettikten sonra `/mhgui` aşamasına geçin. Etkin olmayan koruma, başarılı bir entegre kurulum değil, bir başlatma sorunudur.

Grim yapılandırması `plugins/VexLandManhunt/grim/` içinde bulunur (`config.yml`, `messages.yml`, `punishments.yml`, `discord.yml`); isteğe bağlı geçmiş `violations.sqlite` dosyasındadır. İlk aktarım yedekleri `plugins/VexLandManhunt-integration-backups/` konumuna gider; `plugins/VexLandManhunt/integration-migration-v1.txt` tamamlanmayı işaretler. Hem eski hem entegre Grim verileri varsa entegre hedef korunur ve bir uyarı günlüğe yazılır. Aktarım sembolik bağlantıları reddeder.

`plugins/VexLandManhunt/integration.properties` içinde hareket düzeltme yetkisini gözden geçirin; diğer ayarları koruyun. Yeni kurulum varsayılanı:

```properties
movement-correction-owner=legacy
```

Aşağıdaki eksiksiz herkese açık menü kılavuzu bu paketin 1.9.11 oynanış temelini izler. Spectator dalının kendine ait arşivlenmiş kılavuzu vardır.

### 2. Kontrol merkezini açın

Sunucuya **OP** veya **`vexland.admin`** iznine sahip yönetici olarak katılıp şunu girin:

```text
/mhgui
```

Aşağıdaki açıklamalar, **2.0.0** eklenti sürümünün herkese açık arayüzünü İngilizce düğme adlarıyla anlatır. Etiketler sunucunun seçilen dilini izler. Arayüzün tamamını kullanmak için güvendiğiniz bir **OP** hesabı kullanın: tanım dosyasındaki izin komutu açmaya izin verse de sağlanan bazı arayüz işleyicileri daha sıkı OP denetimleri uygular. Ana envanter, dokuz yuvalı beş satırdan oluşur. Açıklamasını ve mevcut ayarını okumak için düğmenin üzerine gelin. Çoğu düğme normal tıklamayla çalışır; özel fare işlemleri ve onaylar aşağıda açıklanır. Daha küçük 1.6.4 menüsü sonunda anlatılır.

#### İlk maçınızı kurun

1. **Player Roles** (Oyuncu Rolleri) menüsünü açın. Görünen rol doğru olana kadar her katılımcının oyuncu kafasına tıklayın. 2.0.0'de rol **Runner** ve **Hunter** arasında değişir; henüz rolü olmayan katılımcı ilk tıklamada Kaçan olur. Sol/sağ/shift tıklama ayrı rol seçme kısayolları değildir. Gerektiğinde **Previous Page** (Önceki Sayfa), **Next Page** (Sonraki Sayfa) ve **Back to Control Center** (Kontrol Merkezine Dön) düğmelerini kullanın.
2. En az bir Kaçan ve bir Avcı atayın. Başlatma işlemi kalan rolsüz çevrimiçi oyuncuları Avcıya dönüştürebilir; bu yüzden tüm katılımcıları açıkça atamak takımları netleştirir.
3. Takım arkadaşlarının birbirlerine zarar verip veremeyeceğini seçmek için **Friendly Fire** (Dost Ateşi) düğmesine tıklayın. Ardından ON/OFF göstergesini kontrol edin.
4. Sunucunun tamamı için dil seçmek üzere **Language** (Dil) düğmesine tıklayın. Bu ayar yalnızca sizin oyuncunuzu değil, herkesin mesajlarını, arayüzlerini, bildirimlerini ve rehberlerini etkiler.
5. **Smart Hunter Kit**, **Auto World Spawn** ve **Anti-Cheat** ayarlarını inceleyin. Oyun içi açıklama gerekiyorsa kitap düğmesinden yönetici rehberini okuyun.
6. **Server Freeze** (Sunucuyu Dondur) kapalı olsun, ardından **Start Match** (Maçı Başlat) düğmesine tıklayın. Başlatma, oyuncuları ve envanterlerini hazırlar; tanıtımı ve Avcıların bekleme süresini belirleyen rastgele ruleti çalıştırır, sonra av başlar. Başlatmadan önce saklamak istediğiniz eşyaları katılımcı envanterlerinin dışında tutun.

#### Ana kontrol merkezi düğmeleri

Aşağıdaki konumlarda satırlar yukarıdan aşağıya, sütunlar soldan sağa sayılır. Bunlar 2.0.0'in son süslenmiş düzenini anlatır.

| Konum | İngilizce düğme | İşlevi |
|---|---|---|
| Satır 2, sütun 2 | Player Roles | Sayfalı Kaçan/Avcı oyuncu kafası menüsünü açar. |
| Satır 2, sütun 3 | Target Player | Seçili hedefe yönetici işlemleri uygulamak için diğer çevrimiçi oyuncular arasında geçer. Mevcut hedef adını kontrol edin. |
| Satır 2, sütun 4 | Friendly Fire | Takım arkadaşları arasında hasarı açıp kapatır. |
| Satır 2, sütun 5 | Match Info | Maç durumu, takımlar, dost ateşi ve seçilen hedef hakkında kısa rapor gönderir. |
| Satır 2, sütun 6 | Start Match | Normal maç başlangıcını ve rastgele önden kaçma dizisini çalıştırır. |
| Satır 2, sütun 7 | Full Heal | Tüm çevrimiçi oyuncuların canını yeniler. |
| Satır 2, sütun 8 | Reset Match | Maçı tamamen sıfırlar. Reset Settings ile farklıdır. |
| Satır 3, sütun 2 | Full Hunger | Tüm çevrimiçi oyuncuların açlık ve doygunluğunu yeniler. |
| Satır 3, sütun 3 | Release Hunters | Bekleyen Avcıları önden kaçma süresi dolmadan serbest bırakır. |
| Satır 3, sütun 4 | Clear Effects | Tüm çevrimiçi oyunculardan iksir etkilerini kaldırır. |
| Satır 3, sütun 5 | Server Freeze | Genel sunucu dondurmasını açıp kapatır; sıradan OP olmayan oyuncular donar. |
| Satır 3, sütun 6 | Clear Target Inventory | Onaydan sonra seçilen oyuncunun envanterini, zırhını ve ikinci elini temizler. |
| Satır 3, sütun 7 | Teleport Everyone | Tüm çevrimiçi oyuncuları bulunduğunuz konuma getirir. |
| Satır 3, sütun 8 | Kill Target | Onaydan sonra seçilen oyuncuyu öldürür; normal ölüm kuralları maçı etkileyebilir. |
| Satır 4, sütun 2 | Anti-Cheat | VexAC Security kontrollerini açar. |
| Satır 4, sütun 3 | Freeze Target | Seçilen oyuncunun bireysel dondurmasını açıp kapatır. |
| Satır 4, sütun 4 | Emergency Restore | Çevrimiçi herkesin canını, açlığını ve doygunluğunu yeniler. |
| Satır 4, sütun 5 | Freeze Team | Sol tıklama Kaçanları, sağ tıklama Avcıları dondurur/çözer; shift tıklama bireysel/takım dondurmalarını temizler. |
| Satır 4, sütun 6 | Set Day | Mevcut dünyanızı gündüz yapar. |
| Satır 4, sütun 7 | Clear Weather | Mevcut dünyanızdaki yağmuru ve gök gürültüsünü durdurur. |
| Satır 4, sütun 8 | Language | Genel dil seçicisini açar. |
| Satır 5, sütun 2 | Smart Hunter Kit | Uyarlanabilir Avcı yeniden doğma kitlerini açıp kapatır; ON/OFF gösterir. |
| Satır 5, sütun 3 | Clear Dropped Items | Mevcut dünyanızda yere düşmüş eşya varlıklarını kaldırır. |
| Satır 5, sütun 4 | Pause Match / Resume Match | Etkin oynanışı ve maç sayaçlarını durdurur veya sürdürür. |
| Satır 5, sütun 5 | Emergency Sync | Oyuncu rollerini, pusulaları ve ilgili çalışma zamanı durumunu yeniden eşitler. |
| Satır 5, sütun 6 | Reset Settings | İki tıklamalı onaydan sonra dengeli ayarları geri yükler. |
| Satır 5, sütun 7 | Close | Kontrol merkezini kapatır. |
| Satır 5, sütun 8 | Auto World Spawn | Otomatik Overworld doğma noktası aralığı seçicisini açar. |
| Satır 5, sütun 9 | Manhunt Administrator Guide | Yerelleştirilmiş yönetici rehberini verir. |

Dekoratif camlar ve başlık/durum eşyaları oynanış düğmeleri değildir.

#### Roller ve seçili hedefler

**Player Roles**, katılımcının gerçek Manhunt takımını değiştirir. Kafasına tıklayıp güncellenen rolü okuyun. STARTING/RUNNING sırasında arayüz Kaçan/Avcı değişikliklerine izin verir, ancak son Kaçanı Avcıya çevirmeyi reddeder. Böylece devam eden maçın Kaçan tarafı korunur. Değişiklikten sonra takımın çalışma zamanı durumu ve pusulalar eşitlendiği için rolleri bilinçli değiştirin.

**Target Player** ayrıdır: oyuncunun takımını değiştirmeden Freeze Target, Clear Target Inventory veya Kill Target gibi işlemler için onu hedef seçer. İstediğiniz çevrimiçi oyuncunun adı görünene kadar ilerleyin. Kayıtlı hedef kullanılamaz olursa kod diğer ilk çevrimiçi oyuncuya dönebilir; bu yüzden hedefe yönelik işlemden hemen önce adı mutlaka doğrulayın. Başka kimse çevrimiçi değilse hedef bulunmadığını bildirir.

**Clear Target Inventory** ve **Kill Target**, aynı hedef için aynı işleme **beş saniye** içinde iki kez tıklamayı gerektirir. İlk tıklama onayı hazırlar ve hedefi belirtir; ikinci işlem uygular. Hedefi değiştirmek veya fazla beklemek yeni onay gerektirir. Envanteri temizlemek içeriğini siler; bir Kaçanı öldürmek normal ölüm kuralları uyarınca maçı bitirebilir veya değiştirebilir.

**Freeze Team**, bu menüde takıma özel fare kısayollarının bulunduğu tek düğmedir: normal sol tıklama Kaçan takımını, normal sağ tıklama Avcı takımını seçer; shift tıklama bu aracın yönettiği tüm bireysel/takım dondurmalarını temizler. Genel Server Freeze ayrı bir kontroldür; oyuncular hâlâ donmuşsa ayrıca kapatılmalıdır.

#### Smart Hunter Kit

Uyarlanabilir Avcı yeniden doğma kitlerini açıp kapatmak için **Smart Hunter Kit** düğmesine tıklayın. Düğme mevcut durumu gösterir. Açıkken yeniden doğan Avcı, Kaçan ekipmanına ve maçın bağlamına uyarlanmış bir kit alabilir; sağlanan oyuncu rehberi kitin Kaçan ortalamasından zayıf olduğunu açıklar. Kapalıyken Avcılar ölümden sonra otomatik kit almaz. Bu, takip pusulasını kapatmaz.

Açıp kapatmak yerine doğrudan ayarlamak için `/mhkit on`, `/mhkit off` veya `/mhkit status` kullanın. İncelenen yeni yapılandırmanın yedek varsayılanı ON'dur.

#### Auto World Spawn

**Auto World Spawn** düğmesine tıklayın, ardından **OFF**, **5 minutes**, **10 minutes**, **15 minutes**, **20 minutes** veya **30 minutes** seçin. Bir seçenek ayarı kaydedip `/mhgui` menüsüne döner; **Back** yeni aralık seçmeden geri döner.

Etkin olduğunda sistem, Overworld'deki etkin bir Kaçanın yakınında güvenli bir Overworld yüzeyi arayıp dünya doğma noktasını oraya taşır. Overworld'de Kaçan yoksa veya güvenli aday bulunmazsa taşıma atlanır. Yeni yapılandırmanın yedek varsayılanı OFF'tur. Aynı kontroller için `/mhspawn off`, `/mhspawn 15` veya `/mhspawn status` kullanın; 15 yerine desteklenen herhangi bir aralığı yazabilirsiniz.

#### Duraklatma, yeniden bağlantı ve kurtarma

**Pause Match**, maç RUNNING durumundayken kullanılabilir. Oynanış sistemlerini, hareket/etkileşimleri, maç sayaçlarını, takibi ve doğma noktası hareketini dondurur. **Resume Match** bunları sürdürür ve duraklatılmış süreyi telafi eder. Server Freeze yalnızca oyuncuları dondurur; maç saatini duraklatmak gerektiğinde onun yerine kullanılmamalıdır.

Kaçanın yeniden bağlantı süresi yapılandırılabilir; yeni kurulumdaki yedek varsayılan **15 dakikadır**. Zamanında yeniden katılmak Kaçan durumunu geri yükler ve on saniyelik geri dönüş koruması verir. Sunucunun kapalı kaldığı süre kayıtlı yeniden bağlantı süresini tüketmez. Süresi dolan Kaçan yerleri Avcı olur; son Kaçanın süresinin dolması Avcılara zafer kazandırabilir.

**Sağlanan 2.0.0 arayüzünde ayrı bir yeniden bağlantı süresi seçicisi yoktur.** Özelleştirmek için sunucuyu durdurun, `plugins/VexLandManhunt/config.yml` dosyasını diğer ayarları koruyarak düzenleyin ve şunu ayarlayın:

```yaml
features:
  custom-reconnect-minutes: 15
```

Düzenledikten sonra yeniden başlatın. Bir dakikanın altındaki değerler bire çıkarılır. **Reset Settings** bu değeri 15 dakikaya getirir. Derlenmiş yapı, yeniden başlatma/çökme sonrasında kurtarma için maç/yeniden bağlantı durumunu ve yedek anlık görüntüleri de kaydeder; oyun sırasında dosyaları düzenlemek yerine eklentinin yönetmesine izin verin.

#### Reset Settings ve Reset Match

**Reset Settings**, **sekiz saniye** içinde iki tıklama gerektirir. İlk tıklama onayı hazırlar; ikincisi **Smart Kit ON**, **Auto Spawn her 15 dakikada**, **Reconnect 15 dakika** ve **rastgele önden kaçma süresi** ayarlarını geri getirir. Bu, Auto World Spawn'ın yedek varsayılanı OFF olan yeni kurulumdan farklıdır. Yapılandırmayı değiştirir; maçın tam sıfırlanmasının yerini almaz.

**Reset Match**, mevcut maç sıfırlamasını yapar; geçici maç durumunu/eşyalarını temizler ve oyuncuları yeni tur için Overworld doğma noktasına döndürür. Ana düğmesi Reset Settings'in iki tıklamalı onayını kullanmaz. **Start Match**, katılımcı envanterlerini hazırlayabilir/temizleyebilir. Tıklamadan önce hangi sıfırlama/başlatma kontrolünü kullanmak istediğinizi inceleyin.

#### Dil ve hile koruması kontrolleri

**Language** genel seçiciyi açar. İstediğiniz dilin adına tıklayın. Sağlanan iki yapı da İngilizce, Farsça, Arapça, İspanyolca, Fransızca, Almanca, Rusça, Basitleştirilmiş Çince, Hintçe ve Portekizce içerir. Seçilen dil sunucunun tamamında paylaşılır ve kaydedilir. Japonca README belgesi, eklentinin oyun içi seçicisine Japonca eklemez.

**Anti-Cheat**, **VexAC Security** menüsünü açar. Dahili motoru açıp kapatmak için **VexAC Master** düğmesine; grubunu açıp kapatmak için **Movement**, **Combat**, **AutoClick**, **Velocity / AntiKB** veya **World / Scaffold** düğmesine tıklayın. **Anti X-Ray**, Paper'ın yapılandırılmış Anti-Xray korumasını açıp kapatır; bu değişiklik için sunucuyu yeniden başlatın. Durum, kanıt kaydı ve algılama modeli kutucukları mevcut sistemleri açıklar. **Back to Control Center** ana menüye döner.

Yapının arayüzü yalnızca izleme yapan moderasyon anlatır, ancak statik incelemede eşik tabanlı sunucudan atma yolu vardır. Menüdeki oyuncu atmama ifadesini uygulama/belgeleme tutarsızlığı olarak ele alın; ona güvenmeden önce kontrollü bir sunucuda moderasyon davranışını doğrulayın.

#### Entegre GrimAC ve eski VexAC

Mevcut **VexAC Security** arayüzü eski VexAC motorunu kontrol eder; Master/grup düğmeleri yeni bir Grim kontrol paneli değildir. Entegre GrimAC onunla birlikte çalışır. Modül durumu için `/vexintegration`, Grim'in kendi komutları ve izinlerle denetlenen araçları için yerel `/grim` veya `/grimac` kullanın. Grim ayarları ve ceza kuralları `plugins/VexLandManhunt/grim/` içindedir.

1.13.1 GrimBridge izleme/gruplar menüsü ve `grim-settings.yml` bu paketi tanımlamaz. VexAC'yi kapatmanın entegre GrimAC'yi de devre dışı bıraktığını veya bir izleme etiketinin oyuncu atmama politikası oluşturduğunu varsaymayın. Paper Anti-Xray, yeniden başlatma gerektiren bağımsız bir ayar olmaya devam eder.

#### Oyun içi rehber ve sorun giderme

Yerelleştirilmiş rehber almak için **Manhunt Administrator Guide** düğmesine tıklayın veya `/mhhelp` kullanın. Oyuncular 2.0.0'de kendi rollerine uygun rehber için `/mhhelp` kullanabilir. Avcılar Kaçan seçmek için pusulalarına sağ tıklar; bu takip arayüzü, yöneticinin Target Player seçicisinden ayrıdır.

Bir rol veya pusula eşleşmiyor görünüyorsa **Emergency Sync** ilgili çalışma zamanı durumunu yeniler. **Match Info** mevcut takımları ve durumu kontrol etmeye yardım eder. Başlatma isteği başarısızsa maçın hazır olduğunu, sunucu dondurmasının kapalı olduğunu ve Kaçan/Avcı takımlarının bulunduğunu kontrol edin. JAR değişikliğinden sonra `/reload` yerine sunucuyu tamamen yeniden başlatın. `/mhdebug`, 2.0.0'de bulunan yönetici tanılama komutudur; varlığı bu sürümlerin canlı sunucu testlerini geçtiği anlamına gelmez.

#### Eski 1.6.4 kontrol merkezini kullanma

1.6.4; **Player Roles**, **Friendly Fire**, **Start Match**, **Reset Match**, **Release Hunters Now**, **Server Lock**, **Teleport Everyone To Me**, **Heal & Feed Everyone**, **Match Status**, dil seçimi, **Anti Cheat** ve yönetici rehberini korur. Roller **None → Runner → Hunter** şeklinde döner ve maç başlarken/çalışırken rol değişiklikleri kilitlenir.

Hile koruması menüsü eski **Anti AutoClick** (uyarı/sunucudan atma işlemleriyle 30 CPS kuralı), **Anti Fly** ve Paper **Anti X-Ray** içerir. Kaçanın yeniden bağlantı süresi sabit **60 dakikadır**. Yukarıdaki yeni Smart Hunter Kit V3 anahtarı, Auto World Spawn seçicisi, duraklatma/sürdürme, Reset Settings onayı ve genişletilmiş seçili hedef/dünya araçları 2.0.0'e aittir; eski menüde beklenmemelidir.

Bu rehber, sağlanan JAR meta verileri, paketlenmiş dil/yardım metinleri ve statik ayrıştırmadan elde edilmiştir. İnceleme sırasında arayüz canlı Minecraft sunucusunda çalıştırılmamıştır.

### 3. Kovalamacayı oynayın

Kaçanlar rastgele önden kaçma süresinde uzaklaşıp Ender Dragon'u yenmeye ilerler. Avcılar serbest bırakılmayı bekler, sonra Kaçan seçmek için takip pusulalarına sağ tıklar. Takip boyutları geçse bile oyun sırasında hedefler değiştirilebilir. Yalnızca takımınızla konuşmak için `/teammsg <message>`, 2.0.0'de yerelleştirilmiş rol rehberi için `/mhhelp` kullanın.

Bir Kaçan ölürse kalan Kaçanlar devam eder ve ölen oyuncu Avcı olur. Avcı yeniden doğup takibi sürdürebilir. Son Kaçanın ölümü veya bağlantısı kesilen Kaçanın süresinin dolması Avcılara maçı kazandırabilir; Ender Dragon'un yenilmesi Kaçanlara kazandırır.

### 4. Duraklatın, bitirin ve yeni maçı hazırlayın

2.0.0'de `/mhpause` ile duraklatıp `/mhresume` ile sürdürün. Avcılar bekleme geri sayımı dolmadan salınacaksa `/mhrelease` kullanın. Yeni maç için kontrol merkezinin tam sıfırlamasını veya `/mhreset` kullanın; sıfırlama geçici maç durumunu/eşyalarını temizler ve oyuncuları Overworld doğma noktasına döndürür. Paper Anti-Xray ayarlarını değiştirmek yeniden başlatma gerektirir.

## Birleşik 2.0.0 paketindeki varsayılan ayarlar

İncelenen yeni yapılandırmanın yedek varsayılan değerleri:

```yaml
features:
  adaptive-hunter-kit: true
  auto-world-spawn-minutes: 0
  custom-reconnect-minutes: 15
```

`0`, otomatik doğma noktası hareketinin kapalı olduğunu belirtir. Arayüzün onaylı ayar sıfırlaması aralığı bunun yerine 15 dakikaya getirir. İlgili ayarlar için arayüzü veya `/mhkit` ve `/mhspawn` kullanın.

## Herkese açık komut başvurusu — birleşik 2.0.0

Yönetici komutları OP veya `vexland.admin` gerektirir (varsayılan OP). Takım sohbeti, çöp ve gece görüşü oyuncu araçlarıdır; `/mhhelp` role uygun kılavuzu gösterir. Tablo, 17 Manhunt/entegrasyon komutunu listeler; yerel Grim komutlarının kendi izinleri vardır. `/mhnone` burada kayıtlı değildir.

| Komut | Amaç |
| --- | --- |
| `/vexintegration` | Entegre Grim, VexAC, PacketEvents ve paylaşılan Bukkit sahibi durumunu bildirir |
| `/mhgui` | Kontrol merkezini açar |
| `/mhstart` | Tam maç başlangıcını çalıştırır |
| `/mhreset` | Mevcut maçı tamamen sıfırlar |
| `/mhrelease` | Avcıları erken serbest bırakır |
| `/mrunner <player>` | Kaçan atar |
| `/mhunter <player>` | Avcı atar |
| `/teammsg <message>` | Takım arkadaşlarına özel mesaj gönderir |
| `/trash` | 54 yuvalı tek kullanımlık envanteri açar |
| `/nv` | Kişisel gece görüşünü açıp kapatır |
| `/mhlang` | Genel dil seçicisini açar |
| `/mhhelp` | Yerelleştirilmiş rehber verir |
| `/mhkit <on\|off\|toggle\|status>` | Akıllı Avcı kitlerini yapılandırır |
| `/mhspawn <off\|5\|10\|15\|20\|30\|status>` | Otomatik doğma noktası hareketini yapılandırır |
| `/mhpause` | Devam eden maçı duraklatır |
| `/mhresume` | Duraklatılmış maçı sürdürür |
| `/mhdebug` | Dahili tanılama çalıştırır |

## Oyun içi diller ve belgeler

Bu paket **10 oyun dilini** korur: İngilizce, Farsça, Arapça, İspanyolca, Fransızca, Almanca, Rusça, Basitleştirilmiş Çince, Hintçe ve Portekizce. Paketteki her çeviri **683 anahtar** içerir ve 1.9.11 sürümünü izler. `/mhlang`, `language.txt` içine kaydedilen ve sunucu genelinde kullanılan tek bir dil ayarlar.

Proje belgeleri, Arapça belge sürümü hariç **18 dilde** sunulur. Bu çeviriler değiştirilmemiş ikili dosyaya Japonca veya başka ek oyun içi diller eklemez.

## Sürüm geçmişi, kaynak ve katkıda bulunanlar

[CHANGELOG.md](../CHANGELOG.md), sunulan her sürümü kaydeder. Tam [1.13.1 spectator kılavuzu](archive/1.13.1/README.tr.md) ve [eski 1.9.11 / 1.6.4 kılavuzu](archive/1.9.11/README.tr.md) erişilebilir durumdadır. Sunulan her sürüm kendi indirmesini ve sağlama toplamını korur.

**Manhunt, Bardiya / Farland_game ve Ali / Alivexor tarafından birlikte oluşturulmuştur. GrimAC, GrimAC / DefineOutside ve katkıda bulunanların ayrı bir projesidir.** Bu entegre ürün üç Grim sınıfını değiştirir; önceki iki dosyalı sürümdeki değiştirilmemiş resmî Grim ikili dosyası değildir. Eşlik eden [kaynak paketi](https://github.com/FarlandGame/Vexland_Manhunt/releases/download/v2.0.0/VexLandManhunt-2.0.0-source.zip), test/çalışma zamanı kanıtları çıkarılmış ve kaynak kodu değiştirilmemiş olarak sunulan kaynakları, derleme betiklerini, bağımlılık girdilerini ve bildirimleri korur. Sürüm ayrıca GPLv3 metni, sağlama toplamları ve [üçüncü taraf bildirimleri](../THIRD_PARTY_NOTICES.md) içerir. Bu yayımlama sırasında canlı sunucu veya yeniden üretilebilir derleme testi yapılmamıştır.

## Dream'e eğlenceli bir meydan okuma

Bardiya'dan biraz Minecraft şakalaşması 😄

> "Ah... Ali'yle Dream'inkinden yüz kat daha iyi bir Manhunt eklentisi yaptık ama Dream korkuyor, bizimkini oynamıyor!"

## Geliştiriciler ve proje kapsamı

**[Bardiya Alizadeh (Kabir) · Farland_game](https://github.com/FarlandGame) ve [Ali · Alivexor](https://github.com/Alivexor) tarafından birlikte geliştirildi.** Her iki kullanıcı adı da özgün eklenti tanımlarında yazar olarak kayıtlıdır.

Bu depo; özgün derlenmiş sürümleri, belgelerini ve sürüm notlarını ortak bir portföy projesi olarak sunar. Özellik açıklamaları sağlanan JAR'ların statik incelemesine dayanır. Canlı sunucu uyumluluğu, kurtarma performansı, denge ve hile algılama doğruluğu bu yayımlama sürecinde test edilmemiştir.

[Bardiya'nın GitHub portföyü](https://github.com/FarlandGame) · [Ali'nin GitHub'ı](https://github.com/Alivexor) · [Tüm sürümler](https://github.com/FarlandGame/Vexland_Manhunt/releases)
