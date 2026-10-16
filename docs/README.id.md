# Vexland_Manhunt

[English](../README.md) | [日本語](README.ja.md) | [فارسی](README.fa.md) | [Deutsch](README.de.md) | [Français](README.fr.md) | [Español](README.es.md) | [Português (Brasil)](README.pt-BR.md) | [Italiano](README.it.md) | [Nederlands](README.nl.md) | [Polski](README.pl.md) | [Українська](README.uk.md) | [Türkçe](README.tr.md) | [Русский](README.ru.md) | [简体中文](README.zh-CN.md) | [繁體中文](README.zh-TW.md) | [한국어](README.ko.md) | [हिन्दी](README.hi.md) | [Bahasa Indonesia](README.id.md)

**Pengalaman Minecraft Runner melawan Hunter yang lengkap, dibuat bersama oleh [Bardiya Alizadeh (Kabir) · Farland_game](https://github.com/FarlandGame) dan [Ali · Alivexor](https://github.com/Alivexor).**

Vexland_Manhunt menyatukan persiapan pertandingan, peran tim, pengejaran awal, pelacakan, progres, hadiah, hasil, dan administrasi dalam satu plugin server Paper. Runner berusaha mengalahkan Ender Dragon, sedangkan Hunter berusaha mengeliminasi Runner terakhir. Plugin ini mendukung beberapa Runner dan menjaga pengejaran tetap berlangsung saat pemain mati, respawn, berpindah dimensi, dan terhubung kembali. Pusat kendali `/mhgui` memungkinkan administrator mengelola pertandingan melalui menu, dengan pesan dan buku panduan yang dilokalkan untuk pemain.

## Unduhan dan kompatibilitas

| Berkas / versi | Unduh | Kegunaan |
|---|---|---|
| **1.13.1 — terkini** | [VexLandManhunt-1.13.1.jar](https://github.com/FarlandGame/Vexland_Manhunt/releases/download/v1.13.1/VexLandManhunt-1.13.1.jar) | Plugin Manhunt buatan Bardiya dan Ali |
| **GrimAC 2.3.73 — wajib** | [grimac-bukkit-2.3.73.jar](https://github.com/FarlandGame/Vexland_Manhunt/releases/download/v1.13.1/grimac-bukkit-2.3.73.jar) | Dependensi antikecurangan pihak ketiga yang terpisah |
| 1.9.11 — arsip | [VexLandManhunt-1.9.11-.jar](https://github.com/FarlandGame/Vexland_Manhunt/releases/download/v1.9.11/VexLandManhunt-1.9.11-.jar) | Build Manhunt sebelumnya |
| 1.6.4 — arsip | [VexLandManhunt-1.6.4.jar](https://github.com/FarlandGame/Vexland_Manhunt/releases/download/v1.6.4/VexLandManhunt-1.6.4.jar) | Build Manhunt yang lebih lama |

**Target: Paper 1.21.11, Java 21.** Angka 1.6.4, 1.9.11, dan 1.13.1 adalah rilis plugin, bukan versi Minecraft yang didukung. Pada 1.13.1, GrimAC merupakan dependensi wajib dan penghubungnya memerlukan API 2.3.73. Unduh **kedua JAR terkini**. Keduanya adalah plugin server; pemain tidak memasangnya di folder mods klien.

Ini adalah build asli untuk server pribadi dengan akses administratif tingkat tinggi khusus pembuat, dipertahankan persis seperti yang diberikan. Panduan ini membahas kontrol publik Manhunt.

## Pengalaman Manhunt

- **Tim Runner dan Hunter:** tetapkan pemain yang sedang online ke salah satu pihak. Pertandingan membutuhkan setidaknya satu Runner serta satu Hunter atau seorang pemain online yang belum diberi peran. Runner yang masih hidup melanjutkan permainan jika rekan timnya mati; Runner yang mati menjadi Hunter kecuali kematian tersebut mengakhiri pertandingan.
- **Awal pertandingan sinematik:** inventaris dan mode permainan disiapkan, tim diperkenalkan, dan sebuah roulette memilih waktu keunggulan awal Runner. Hunter dibekukan selama hitung mundur tersebut, disertai umpan balik berupa judul di layar dan suara. Waktu keunggulan awal dipilih secara acak; administrator dapat melepaskan Hunter lebih awal.
- **Kompas pelacak dengan pemilihan target:** Hunter menerima kompas khusus. Klik kanan untuk memilih Runner dari menu target dan mengubah target selama pengejaran. Saat melintasi dimensi, pelacakan mengikuti rute portal yang sesuai sampai pelacakan langsung memungkinkan. Hunter menerima kembali pelacaknya setelah respawn.
- **Tampilan progres:** bossbar dan informasi pertandingan mengikuti perlengkapan Runner serta progres melalui sumber daya Nether, blaze rod, pearl, Eye of Ender, stronghold, dan End. Build yang lebih baru menambahkan tahap yang lebih terperinci dan visual progres yang menyesuaikan kesehatan naga.
- **Hadiah untuk kill oleh Runner:** ketika Runner membunuh Hunter saat pertandingan aktif, digunakan kumpulan hadiah berbobot berisi 50 entri yang mempertimbangkan progres. Termasuk animasi pengundian, hadiah ganda/tripel, pengumuman rangkaian kill, dan perayaan item langka.
- **Kemenangan dan hasil:** kematian Runner terakhir memberikan kemenangan kepada Hunter; mengalahkan Ender Dragon memberikan kemenangan kepada Runner. Termasuk judul akhir pertandingan, perayaan, informasi kill/kematian, dan pembersihan item sementara. Build yang lebih baru juga melaporkan MVP serta hasil kerusakan dan jarak.
- **Komunikasi tim dan utilitas:** pesan pribadi untuk rekan tim dengan `/teammsg`, inventaris sampah 54 slot untuk membuang item dengan `/trash`, dan penglihatan malam pribadi dengan `/nv`.
- **Administrasi melalui menu:** peran, mulai/reset, pelepasan Hunter lebih awal, friendly fire, penguncian server, teleportasi semua pemain, pemulihan kesehatan/makanan, bahasa, pengaturan perlindungan, status, dan buku panduan tersedia melalui pusat kendali. Pembekuan dan reset penuh membantu menyiapkan pertandingan berikutnya.
- **Panduan yang dilokalkan:** buku Runner, Hunter, dan administrator menjelaskan tujuan, penggunaan pelacak, kematian, persiapan, dan perintah. Versi 1.9.11 memberi pemain panduan sesuai peran melalui `/mhhelp`.
- **Integrasi Paper Anti-Xray:** kontrol menu mengonfigurasi perlindungan Paper pada tingkat dunia; perubahan membutuhkan restart server agar berlaku.

## Apa yang baru di 1.13.1?

Dibandingkan dengan build 1.9.11 yang diberikan:

- **Penonton hantu:** peran terpisah, penetapan oleh administrator, penerbangan terlindungi, pemain tersembunyi, penyimpanan/pemulihan status, dan menu teleportasi peserta dengan beberapa halaman.
- **Pusat kontrol yang didesain ulang:** menu berkategori, pilihan empat peran secara eksplisit, pemilih target berdasarkan nama, pemilih durasi sambung ulang, preset Classic/Fast/Hardcore/Custom, dan layar konfirmasi khusus dengan batas 30 detik.
- **Integrasi GrimAC:** GrimAC 2.3.73 yang wajib menggantikan jalur pengaktifan VexAC yang aktif. Sakelar utama, lima kelompok pemeriksaan, peringatan, serta kontrol pemantauan/penindakan tersedia di GUI. Paper Anti-Xray tetap terpisah.
- **Perencana Smart Hunter Kit baru:** menyesuaikan perlengkapan dan persediaan dengan perlengkapan/enchantment Runner, Runner terdekat, jumlah anggota tim, jarak, dimensi, dan medan. Perencana ini mempertahankan perlengkapan yang sudah lebih kuat, menghindari alat ganda, serta membatasi pengisian barang habis pakai menggunakan riwayat 30 detik. Ini tidak menjamin selisih perlengkapan tetap atau keseimbangan yang telah diukur.
- **Pemulihan tervalidasi:** snapshot bersegel SHA-256, pemeriksaan skema/status, dan cadangan valid sebagai alternatif; snapshot yang tidak valid atau berformat lebih baru dipertahankan tanpa ditimpa. Status penonton memiliki penyimpanan persistennya sendiri.
- **Pesan yang diperluas:** kunci terjemahan bertambah dari 683 menjadi 762 untuk setiap terjemahan bawaan, tetap dalam sepuluh bahasa dalam game yang sama. Dua perintah publik baru didaftarkan: `/mspectator <player>` dan `/mhspectate`.
- **Alternatif saat reset:** jika tidak ada permukaan aman di dekat titik spawn Overworld, reset dapat melewati teleportasi tersebut alih-alih memaksanya.

## Penyiapan dan penggunaan lengkap dengan `/mhgui`

Hentikan server dan cadangkan dunia serta data plugin. Masukkan kedua JAR terkini ke `plugins/`, dengan hanya menyisakan satu JAR Manhunt dan satu JAR GrimAC di sana. Pertahankan pengaturan/data `plugins/VexLandManhunt/` yang sudah ada saat memperbarui. Jalankan server Paper 1.21.11 / Java 21 hingga selesai memulai; lakukan restart penuh saat mengganti build. GrimAC harus berhasil dimuat. Nama internal plugin tetap `VexLandManhunt`.

Panduan ini menjelaskan rilis plugin **1.13.1** menggunakan label bahasa Inggris. Label mengikuti bahasa server secara keseluruhan. Posisi menghitung baris dari atas ke bawah dan kolom dari kiri ke kanan. Gunakan klik kiri biasa kecuali disebutkan tindakan khusus. Panduan ini berasal dari pemeriksaan statis; tidak ada server Minecraft yang dijalankan.

### Menyiapkan pertandingan

1. Gunakan `/mhgui` dengan `vexland.admin` (bawaan: OP).
2. Buka **Player Roles**, klik petak bernama pemain, lalu pilih **Runner**, **Hunter**, **Spectator**, atau **No Team**. Ini membuka pemilih peran yang pasti; mengeklik pemain tidak menggilir perannya.
3. Tetapkan setidaknya satu Runner dan satu Hunter. Pemain online yang belum ditetapkan dapat menjadi Hunter saat pertandingan dimulai; penonton tidak mengisi slot wajib salah satu tim.
4. Tinjau **Match Settings**, **GrimAC Security**, dan **Global Language**. Matikan Server Freeze sebelum memulai.
5. Buka **Match Controls → Start Match**. Inventaris peserta disiapkan/dikosongkan, pengantar dimainkan, dan roulette memilih waktu tunggu Hunter.

### Beranda: `/mhgui` (lima baris)

| Posisi | Tombol | Tindakan |
|---|---|---|
| R2 C2 | Match Controls | Memulai, menjeda/melanjutkan, melepas, dan mereset. |
| R2 C4 | Player Roles | Membuka daftar peran pemain online. |
| R2 C6 | Match Settings | Serangan sesama tim, kit, spawn, sambung ulang, dan preset. |
| R2 C8 | Player Management | Memilih target serta menggunakan alat pemain/dunia. |
| R4 C2 | GrimAC Security | Membuka pengaturan perlindungan. |
| R4 C4 | Global Language | Memilih bahasa yang digunakan semua orang. |
| R4 C6 | Administrator Guide | Menambahkan buku admin terlokalisasi ke inventaris Anda. |
| R5 C5 | Close | Menutup menu. |

Beacon di R1 C5 melaporkan status pertandingan dan jumlah Runner/Hunter.

### Match Controls (lima baris)

| Posisi | Tombol | Tindakan |
|---|---|---|
| R2 C2 | Start Match | Memulai seluruh rangkaian. |
| R2 C4 | Pause Match / Resume Match | Menjeda atau melanjutkan permainan dan penghitung waktu pertandingan; tersedia untuk pertandingan RUNNING. |
| R2 C6 | Release Hunters | Mengakhiri waktu tunggu Hunter saat ini lebih awal. |
| R2 C8 | Reset Match | Membuka konfirmasi, lalu mereset pertandingan sepenuhnya. |
| R4 C2 | Server Freeze | Mengaktifkan/menonaktifkan pembekuan global pemain non-OP. |
| R4 C4 | Teleport Everyone | Membuka konfirmasi, lalu membawa semua pemain online kepada Anda. |
| R4 C6 | Match Info | Mengirim laporan pertandingan dan tim. |

**Back** berada di R5 C1; **Close** di R5 C9. Server Freeze terpisah dari Pause Match: gunakan Pause jika waktu dan sistem permainan harus berhenti bersamaan.

### Player Roles

Daftar pemain enam baris menampilkan hingga 45 petak peran bernama, diurutkan berdasarkan nama pemain, dalam lima baris pertamanya. Runner menggunakan beton hijau limau, Hunter beton merah, Spectator Eye of Ender, dan No Team beton abu-abu. Baris bawah memiliki **Previous Page** di C1, informasi halaman/online di C3, **Back to Control Center** di C5, serta **Next Page** di C9.

Klik pemain untuk membuka **Choose Player Role** (tiga baris):

| Posisi | Peran yang pasti |
|---|---|
| R2 C2 | Runner |
| R2 C4 | Hunter |
| R2 C6 | Spectator |
| R2 C8 | No Team |

Nama/peran pemain saat ini muncul di R1 C5; **Back** di R3 C1 dan **Close** di R3 C9. Peran dapat berubah selama pertandingan. Mengubah Runner terakhir yang ditetapkan menjadi peran lain selama RUNNING membuka konfirmasi **Last Runner: the match will end**. Menerapkannya dapat memberikan kemenangan kepada Hunter. Perintah peran langsung berlaku seketika, jadi gunakan dengan sengaja. No Team dapat ditetapkan di sini; sinkronisasi awal/masuk biasa dapat menjadikan pemain yang belum ditetapkan sebagai Hunter saat pertandingan aktif.

### Penonton

Administrator menetapkan melalui `/mspectator <player>` atau memilih **Spectator** dalam Player Roles. Perintah memeriksa akses administrator meskipun deskriptornya tidak memiliki baris izin. Pemain tidak mendaftarkan dirinya sendiri dengan menjalankan `/mhspectate`.

Penonton menerima kompas **Spectator teleport** di slot hotbar pertama. Pegang di tangan utama dan klik kanan, atau gunakan `/mhspectate`, untuk membuka menu teleportasi enam baris. Menu hanya berfungsi selama pemain memiliki peran Spectator. Lima baris pertamanya berisi hingga 45 Runner/Hunter online yang masih hidup, diurutkan menurut nama; klik petak peran bernama untuk teleportasi ke lokasi pemain saat ini, termasuk di dunia lain. Baris bawah memiliki **Previous Page** di C1, **Close** di C5, serta **Next Page** di C9. Jika tidak ada peserta yang sesuai, R3 C5 menampilkan **No players available**. Menutup menu ini tidak mengakhiri peran penonton.

Penonton dapat terbang, tersembunyi dari pemain lain, tidak bertabrakan, dan terlindungi dari kerusakan. Implementasinya menggunakan mode Adventure dengan penerbangan; tidak menyediakan kamera Spectator vanilla atau gerak menembus blok. Serangan, penghancuran/penempatan blok, interaksi blok/entitas biasa, mengambil/menjatuhkan barang, penukaran tangan kedua, klik/seret inventaris, manipulasi armor stand, serta pengambilan/perolehan pengalaman diblokir. Mob tidak dapat menargetkan mereka dan perubahan rasa lapar dibatalkan. `/teammsg <message>` menjangkau pemain lain dengan peran Spectator. Jangan sampaikan lokasi peserta atau bantuan luar lainnya kepada peserta pertandingan.

Untuk keluar, administrator menetapkan **Runner**, **Hunter**, atau **No Team**, atau menggunakan `/mrunner <player>` atau `/mhunter <player>`. Tidak ada perintah/tombol khusus untuk keluar sendiri. Keluar memulihkan inventaris/barang pada kursor, lokasi, mode game, penerbangan, tabrakan, dan status kekebalan yang tersimpan, lalu menerapkan perilaku pertandingan peran baru. Status penonton disimpan untuk masuk kembali. Match Reset penuh memulihkan status penonton, menghapus peran, dan memindahkan pemain online ke spawn Overworld yang aman jika tersedia. Pembersihan akhir pertandingan normal tidak menyertakan penonton dalam penanganan barang/penerbangan peserta.

### Match Settings (lima baris)

| Posisi | Tombol | Tindakan |
|---|---|---|
| R2 C2 | Friendly Fire | Mengaktifkan/menonaktifkan kerusakan sesama tim. |
| R2 C4 | Smart Hunter Kit | Mengaktifkan/menonaktifkan kit respawn Hunter adaptif. |
| R2 C6 | Auto World Spawn | Membuka pilihan interval. |
| R2 C8 | Reconnect Grace | Membuka pilihan durasi sambung ulang Runner. |
| R4 C2 | Match Preset | Memilih Classic, Fast, Hardcore, atau Custom. |
| R4 C4 | Reset Settings | Mengonfirmasi pengaturan seimbang: Kit ON, Spawn 15m, Reconnect 15m. |
| R4 C6 | Random Head Start | Petak informasi; roulette tetap memilih penundaan. |

**Back** di R5 C1; **Close** di R5 C9.

Pemilih **Reconnect Grace** tiga baris menawarkan **1, 5, 10, 15, 20, 30 menit** di R2 C2–C7, secara berurutan. Mengeklik menyimpan nilainya dan mempertahankan pemilih tetap terbuka. Back di R3 C1; Close di R3 C9.

Pemilih **Match Preset** tiga baris menempatkan **Classic**, **Fast**, **Hardcore**, **Custom** di R2 C2, C4, C6, C8. Classic: Kit ON, Spawn 15m, Reconnect 15m. Fast: ON, 5m, 10m. Hardcore: OFF, OFF, 5m. Custom mempertahankan pengaturan manual saat ini. Preset mempertahankan waktu keunggulan awal acak. Pemilihan mempertahankan menu tetap terbuka; Back di R3 C1, Close di R3 C9.

**Auto World Spawn** menawarkan OFF, 5m, 10m di R2 C2, C3, C4 dan 15m, 20m, 30m di R2 C6, C7, C8. Back di R3 C5. Pilih interval atau gunakan `/mhspawn <off|5|10|15|20|30|status>`. Ini memindahkan spawn Overworld ke dekat Runner Overworld yang sesuai; pemindahan dapat dilewati jika tidak ada yang sesuai. `/mhkit <on|off|toggle|status>` mengontrol kit secara langsung.

### Player Management (enam baris)

| Posisi | Tombol | Berlaku untuk |
|---|---|---|
| R1 C5 | Target Player | Membuka pemilih pemain berdasarkan nama. |
| R2 C2 | Full Heal | Semua pemain online. |
| R2 C4 | Full Hunger | Semua pemain online. |
| R2 C6 | Clear Effects | Semua pemain online. |
| R2 C8 | Freeze Target | Pemain terpilih. |
| R4 C2 | Clear Target Inventory | Pemain terpilih; perlu konfirmasi. |
| R4 C4 | Kill Target | Pemain terpilih; perlu konfirmasi dan hasil pertandingan normal berlaku. |
| R4 C6 | Set Day | Dunia Anda saat ini. |
| R4 C8 | Clear Weather | Dunia Anda saat ini. |
| R5 C2 | Clear Dropped Items | Dunia Anda saat ini; perlu konfirmasi. |
| R5 C4 | Emergency Sync | Menyegarkan sistem peran/runtime untuk pemain online. |
| R5 C6 | Freeze Team | Kiri: Runner; kanan: Hunter; Shift+klik: menghapus pembekuan tim/individu ini. |

Back di R6 C1; Close di R6 C9. Pemilihan target tidak mengubah peran. Pemilihnya menawarkan 28 pemain online lain per halaman, pada baris 2–5, kolom 2–8; klik nama untuk memilih dan kembali. Previous/Back/Next di R6 C1/C5/C9. Periksa kembali target yang ditampilkan sebelum menerapkan tindakan.

### Layar konfirmasi

Reset Match, Teleport Everyone, Reset Settings, Clear Target Inventory, Kill Target, Clear Dropped Items, dan perubahan Runner terakhir melalui GUI menggunakan layar **Confirm Action** terpisah dengan tiga baris. Baca tindakan/target di R1 C5, lalu klik **Confirm** hijau di R2 C3 atau **Cancel** merah di R2 C7. Konfirmasi kedaluwarsa setelah **30 detik**. Target berubah/offline atau peran berubah memerlukan pemilihan ulang. Ini menggantikan petunjuk klik berulang lima/delapan detik dalam panduan lama untuk jalur menu baru ini.

### GrimAC Security dan bahasa

Menu Grim enam baris memiliki status di R1 C5; sakelar di R2 C2 **GrimAC Master**, C4 **Movement**, C6 **Combat**, C8 **Packets**; R4 C2 **Velocity / AntiKB**, C4 **World / Scaffold**, C6 **Anti X-Ray**, C8 **Admin Alerts**; serta R5 C5 **Monitor mode**. Back di R6 C1 dan Close di R6 C9. Monitor mode memilih antara peringatan/bukti dan penindakan. Paper Anti-Xray terpisah dan memerlukan restart setelah perubahan. Ini adalah kontrol GrimAC; uraian menu VexAC/AutoClick yang lama tidak menggambarkan rilis ini.

Global Language berlaku bagi semua orang dan menyegarkan menu/barang. Klik bahasa yang tercantum; Back di R3 C5. `/mhlang` membuka pemilih yang sama, dan `/mhhelp` memberikan panduan pemain/admin terlokalisasi.

### Nilai bawaan terkini, sambung ulang, dan moderasi

Nilai cadangan konfigurasi baru di `plugins/VexLandManhunt/config.yml` adalah:

```yaml
features:
  adaptive-hunter-kit: true
  auto-world-spawn-minutes: 0
  custom-reconnect-minutes: 15
```

`0` berarti perpindahan spawn otomatis dimatikan. Reset Settings dan Classic justru memilih 15 menit. Selama jendela sambung ulang Runner, slotnya dipertahankan; kembali tepat waktu memberikan perlindungan sepuluh detik. Waktu server mati yang tersimpan tidak dihitung. Berakhirnya batas waktu dapat mengubah Runner menjadi Hunter atau mengakhiri pertandingan dengan kemenangan Hunter. Pause/Resume membekukan sistem permainan dan menyesuaikan waktu pertandingan aktif. Berkas pemulihan dikelola plugin.

Pengaturan penghubung Grim disimpan di `plugins/VexLandManhunt/grim-settings.yml`. Nilai bawaan baru adalah Master ON, kelima kelompok ON, Admin Alerts ON, dan **Monitor mode OFF: penindakan diaktifkan**. Monitor mode mengantrekan bukti/peringatan dan membatalkan laporan pelanggaran yang memenuhi syarat. Dalam mode penindakan, penghubung dapat mengubah perintah kick Grim menjadi pemutusan terlokalisasi yang mengizinkan sambung ulang; ini tidak menetapkan kebijakan ban permanen. Ambang sebenarnya juga bergantung pada konfigurasi Grim. Bukti diantrekan ke `plugins/VexLandManhunt/anticheat/grim-evidence.log`; antrean terbatas dapat membuang entri saat beban tinggi. Penghubung mengecualikan penonton, permainan yang dijeda/dibekukan, serta konteks kendaraan tertentu, dengan kelonggaran tiga detik setelah masuk, teleportasi, dan respawn. Tidak ada klaim tolok ukur akurasi atau kinerja antikecurangan.

## Referensi perintah publik — 1.13.1

Akses administrator berarti OP atau `vexland.admin` (bawaan OP). Handler `/mspectator <player>` memeriksanya walaupun tidak memiliki baris izin dalam deskriptor. Perintah peran langsung diterapkan seketika; mengubah Runner terakhir saat RUNNING dapat mengakhiri pertandingan. GUI memberikan konfirmasi untuk situasi itu.

| Perintah | Kegunaan | Akses |
|---|---|---|
| `/mhgui` | Membuka pusat kontrol berkategori | Administrator |
| `/mhstart` | Memulai rangkaian pertandingan penuh | Administrator |
| `/mhreset` | Mereset pertandingan sepenuhnya | Administrator |
| `/mhrelease` | Melepas Hunter yang menunggu | Administrator |
| `/mrunner <player>` | Menetapkan Runner | Administrator |
| `/mhunter <player>` | Menetapkan Hunter | Administrator |
| `/mspectator <player>` | Menetapkan Spectator | Administrator; baru |
| `/mhspectate` | Membuka menu teleportasi peserta | Spectator saat ini; baru |
| `/teammsg <message>` | Mengirim ke peran/tim sendiri | Pemain |
| `/trash` | Inventaris sekali pakai dengan 54 slot; alias `/mhtrash`, `/vextrash` | Pemain |
| `/nv` | Mengaktifkan/menonaktifkan penglihatan malam pribadi | Pemain |
| `/mhlang` | Membuka pemilih bahasa global | Administrator |
| `/mhkit <on\|off\|toggle\|status>` | Mengatur kit Hunter adaptif | Administrator |
| `/mhspawn <off\|5\|10\|15\|20\|30\|status>` | Mengatur perpindahan spawn | Administrator |
| `/mhhelp` | Menerima panduan peran/admin terlokalisasi | Pemain / administrator |
| `/mhpause` | Menjeda pertandingan yang berjalan | Administrator |
| `/mhresume` | Melanjutkan pertandingan yang dijeda | Administrator |
| `/mhdebug` | Diagnostik internal | Administrator |

`/mhnone` tidak didaftarkan dalam rilis ini; gunakan peran No Team dalam GUI. Hunter mengeklik kanan kompas pelacak untuk memilih Runner; ini terpisah dari teleportasi penonton dan pemilih target administrator. Runner menang dengan mengalahkan Ender Dragon; Hunter menang ketika tidak ada Runner tersisa. Runner yang gugur menjadi Hunter jika Runner lain masih tersisa.

## Bahasa, riwayat, dan kredit pihak ketiga

Plugin asli menyediakan **10 bahasa dalam game**: Inggris, Persia, Arab, Spanyol, Prancis, Jerman, Rusia, Tionghoa Sederhana, Hindi, dan Portugis. `/mhlang` memilih satu bahasa untuk seluruh server, disimpan dalam `language.txt`. Panduan GitHub memiliki **18 bahasa**, tidak termasuk edisi dokumentasi bahasa Arab. Bahasa Jepang dan bahasa README tambahan lainnya tidak menambahkan terjemahan dalam game ke JAR yang tidak diubah.

[Riwayat versi](https://github.com/FarlandGame/Vexland_Manhunt/blob/main/CHANGELOG.md) mencatat setiap build yang diberikan. Panduan lengkap 1.9.11 / 1.6.4 yang lama disimpan dalam [arsip berversi](archive/1.9.11/README.id.md). Build khusus penonton kini telah diberikan dan diterbitkan sebagai 1.13.1; fiturnya tidak boleh dianggap tersedia pada unduhan lama.

**GrimAC adalah proyek independen para kontributor GrimAC, didistribusikan dengan GPL-3.0.** Bardiya dan Ali membuat Vexland_Manhunt beserta integrasinya; mereka tidak disebut sebagai pembuat GrimAC. JAR Grim yang diberikan cocok dengan SHA-512 dan SHA-1 artefak Bukkit 2.3.73 resmi di Modrinth. Commit sumber yang tertanam cocok dengan [upstream v2.3.73](https://github.com/GrimAnticheat/Grim/releases/tag/v2.3.73). Rilis mencakup biner tanpa perubahan, checksum, snapshot sumber upstream, lisensi, dan [pemberitahuan pihak ketiga](../THIRD_PARTY_NOTICES.md). Pemberitahuan komponen ini tidak menetapkan lisensi untuk proyek Manhunt yang terpisah.

## Tantangan bercanda untuk Dream

Sedikit candaan Minecraft dari Bardiya 😄

> "Huh... Ali dan aku membuat plugin Manhunt seratus kali lebih baik daripada punya Dream, tetapi Dream takut dan tidak mau memainkan punya kami!"

## Pembuat dan cakupan proyek

**Dibuat bersama oleh [Bardiya Alizadeh (Kabir) · Farland_game](https://github.com/FarlandGame) dan [Ali · Alivexor](https://github.com/Alivexor).** Kedua nama pengguna tersebut juga tercatat sebagai penulis dalam deskriptor plugin asli.

Repositori ini menyajikan rilis asli yang telah dikompilasi, dokumentasinya, dan catatan versi sebagai proyek portofolio bersama. Deskripsi fitur didasarkan pada pemeriksaan statis terhadap JAR yang disediakan. Kompatibilitas server langsung, kinerja pemulihan, keseimbangan, dan akurasi anti-cheat belum diuji dalam proses publikasi ini.

[Portofolio GitHub Bardiya](https://github.com/FarlandGame) · [GitHub Ali](https://github.com/Alivexor) · [Semua rilis](https://github.com/FarlandGame/Vexland_Manhunt/releases)
