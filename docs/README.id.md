# Vexland_Manhunt


[English](../README.md) | [日本語](README.ja.md) | [فارسی](README.fa.md) | [Deutsch](README.de.md) | [Français](README.fr.md) | [Español](README.es.md) | [Português (Brasil)](README.pt-BR.md) | [Italiano](README.it.md) | [Nederlands](README.nl.md) | [Polski](README.pl.md) | [Українська](README.uk.md) | [Türkçe](README.tr.md) | [Русский](README.ru.md) | [简体中文](README.zh-CN.md) | [繁體中文](README.zh-TW.md) | [한국어](README.ko.md) | [हिन्दी](README.hi.md) | [Bahasa Indonesia](README.id.md)

<!-- PLAYFUL_INTRO_START -->
<p><img src="https://raw.githubusercontent.com/FarlandGame/Vexland_Manhunt/main/assets/portfolio-sticker.svg" width="88" height="88" alt=""></p>

> Hunter membawa kompas. Runner membawa rencana… dan alasan cadangan untuk berjaga-jaga. 🎮🧭

[Kenalan dengan Kabir: kisahku, awal perjalanan kreatif, dan rencana ke Jepang](https://github.com/FarlandGame/FarlandGame/blob/main/docs/story.id.md)
<!-- PLAYFUL_INTRO_END -->

**Pengalaman Minecraft Runner melawan Hunter yang lengkap, dibuat bersama oleh [Bardiya Alizadeh (Kabir) · Farland_game](https://github.com/FarlandGame) dan [Ali · Alivexor](https://github.com/Alivexor).**

Vexland_Manhunt menyatukan persiapan pertandingan, peran tim, pengejaran awal, pelacakan, progres, hadiah, hasil, dan administrasi dalam satu plugin server Paper. Runner berusaha mengalahkan Ender Dragon, sedangkan Hunter berusaha mengeliminasi Runner terakhir. Plugin ini mendukung beberapa Runner dan menjaga pengejaran tetap berlangsung saat pemain mati, respawn, berpindah dimensi, dan terhubung kembali. Pusat kendali `/mhgui` memungkinkan administrator mengelola pertandingan melalui menu, dengan pesan dan buku panduan yang dilokalkan untuk pemain.

## Unduhan dan kompatibilitas

| Rilis yang disediakan | Unduhan | Instalasi |
|---|---|---|
| **2.0.0 — paket gabungan** | [VexLandManhunt-2.0.0.jar](https://github.com/FarlandGame/Vexland_Manhunt/releases/download/v2.0.0/VexLandManhunt-2.0.0.jar) | **Satu JAR**, termasuk GrimAC 2.3.73 terintegrasi |
| **1.13.1 — cabang spectator** | [Rilis dan kedua JAR](https://github.com/FarlandGame/Vexland_Manhunt/releases/tag/v1.13.1) | Manhunt ditambah GrimAC 2.3.73 terpisah |
| 1.9.11 / 1.6.4 — versi lama | [Semua rilis](https://github.com/FarlandGame/Vexland_Manhunt/releases) | Build mandiri terdahulu |

**Paper 1.21.11 / Java 21.** Ini adalah plugin server, bukan mod klien. Nama berkas yang disediakan dan rilis publiknya adalah **2.0.0**, tetapi deskriptor yang tidak diubah melaporkan **`1.9.11-grim.1`** dan menetapkan dasar permainan sebagai 1.9.11. Paket gabungan ini **tidak** memuat peran khusus Spectator, `/mspectator <player>`, `/mhspectate`, menu berkategori, atau tambahan 1.13.1 lainnya. Tetap gunakan cabang 1.13.1 yang dicantumkan secara terpisah jika Anda membutuhkan fitur tersebut.

Build server pribadi asli dengan akses administratif yang ditingkatkan khusus untuk pembuat dipertahankan sebagaimana disediakan. Panduan ini membahas kontrol publik.

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

## Apa yang berubah dalam paket 2.0.0 yang disediakan?

- **Satu JAR terintegrasi:** Manhunt, GrimAC 2.3.73 yang dimodifikasi, dan PacketEvents yang disertakan berbagi satu instans plugin Bukkit. Paket ini tidak memerlukan instalasi GrimAC atau PacketEvents terpisah. Deskriptor menyediakan `GrimAC`; arsip telah diratakan, bukan JAR Grim tanpa perubahan yang disarangkan.
- **Status modul:** perintah administrator `/vexintegration` melaporkan Grim ACTIVE/INACTIVE, pemilik Bukkit, status VexAC, status PacketEvents, dan jumlah pemain yang dilacak. Perintah bawaan `/grim` dan `/grimac` didaftarkan oleh modul terintegrasi.
- **Proses mulai terkendali:** pemuat memerlukan API konfigurasi Paper dan tepat Minecraft 1.21.11. Pemuat menolak pemuatan saat server berjalan dengan pemain daring dan instans GrimAC terpisah. Jika proses mulai terintegrasi gagal, plugin dinonaktifkan dan mencatat bahwa perlindungan Grim tidak aktif; server itu sendiri dapat terus berjalan. Verifikasi status sebelum memulai pertandingan.
- **Migrasi data yang ada:** pada pemuatan terintegrasi pertama, migrasi mencadangkan kedua pohon data plugin lama dan menyalin data GrimAC lama hanya jika tujuan terintegrasi belum ada. Data terintegrasi yang ada diutamakan jika keduanya ada; tidak dilakukan penggabungan/penimpaan. Data asli dipertahankan.
- **Penanggung jawab koreksi gerakan:** `plugins/VexLandManhunt/integration.properties` secara default menggunakan `movement-correction-owner=legacy`. Alternatif yang didukung adalah `grim`; nilai lain membatalkan proses mulai. Memilih grim menekan jalur koreksi pengembalian/teleportasi VexAC, sementara pemeriksaan, peringatan, dan bukti VexAC tetap ada. Ini tidak menonaktifkan semua hukuman sistem lama.
- **Dasar permainan:** menu datar `/mhgui`, pergiliran peran Runner/Hunter, kontrol VexAC, Smart Hunter Kit V3, jeda/lanjutkan, pemulihan, dan 683 kunci terjemahan mengikuti 1.9.11. Ini adalah rilis pengemasan/integrasi gabungan, bukan kumpulan fitur 1.13.1 yang mendukung spectator.

## Permainan yang dipertahankan dari fondasi 1.9.11

Sistem berikut ditambahkan ke fondasi 1.9.11 dan dipertahankan oleh paket gabungan ini. Ini adalah fitur permainan yang diwarisi, bukan fitur spectator baru 2.0.0.

| Penambahan atau perubahan | Perilaku di 1.9.11 |
| --- | --- |
| **Smart Hunter Kit V3** | Kit respawn adaptif mempertimbangkan perlengkapan Runner, tim, dan konteks pertandingan. Sistem ini bertujuan menjaga kit Hunter di bawah rata-rata perlengkapan Runner dan dapat diaktifkan/dinonaktifkan melalui `/mhkit` atau GUI. |
| **Spawn Overworld otomatis** | Memindahkan spawn dunia ke dekat Runner Overworld yang memenuhi syarat pada interval pilihan: mati, 5, 10, 15, 20, atau 30 menit. Sistem memilih kandidat permukaan yang aman dan melewati situasi yang tidak sesuai. |
| **Jeda dan lanjutkan** | `/mhpause` membekukan permainan serta timer terkait pertandingan, pelacakan, dan perpindahan spawn; `/mhresume` melanjutkannya. Waktu jeda dikompensasikan dalam perhitungan waktu pertandingan aktif. |
| **Pemulihan setelah restart/crash** | Lapisan pemulihan mengembalikan status pertandingan, peran, target pelacak, progres, timer hadiah/kematian, dan status koneksi ulang dengan snapshot utama/cadangan, penyimpanan berkala, dan penyimpanan saat shutdown. |
| **Pengaturan koneksi ulang Runner** | Batas waktu koneksi ulang yang dapat dikonfigurasi menggantikan batas tetap 60 menit sebelumnya. Default instalasi baru: 15 menit, dengan perlindungan 10 detik saat bergabung kembali. Waktu server tidak aktif tidak dihitung; habisnya batas waktu dapat mengubah Runner menjadi Hunter atau mengakhiri pertandingan. |
| **Administrasi diperluas** | Ubah peran saat pertandingan berlangsung sambil mempertahankan Runner terakhir; tindakan pada pemain terpilih, teleportasi/pembekuan tim, sinkronisasi ulang runtime, dan pintasan meningkatkan pengelolaan pertandingan. |
| **Reset pengaturan dengan konfirmasi** | Dua klik dalam delapan detik menerapkan Smart Kit ON, spawn otomatis setiap 15 menit, dan koneksi ulang 15 menit. Ini berbeda dari default spawn otomatis OFF pada instalasi baru. |
| **VexAC 3.0** | Pemeriksaan pergerakan, pertarungan, AutoClick, velocity/knockback, dan pembangunan dunia; kontrol grup/utama, pencatatan bukti, peringatan administrator, dan pengecualian lingkungan/lag. |
| **Ultra Deep Debug v4** | `/mhdebug` menyediakan diagnostik mesin status, GUI, kit sintetis/stress, placeholder bahasa, siklus simpan-pulih, dan integritas. |
| **Tampilan diperluas** | Detail progres lebih banyak, visual kesehatan naga, hasil MVP/kerusakan/jarak, dan informasi ping pada TAB. |
| **Perubahan perintah** | Menambahkan `/mhkit`, `/mhspawn`, `/mhpause`, `/mhresume`, dan `/mhdebug`; menghapus `/mhnone`; membuat `/mhhelp` menyesuaikan pemain/administrator dan menambahkan alias `/trash`. |
| **Lebih banyak pesan yang dilokalkan** | Sumber daya terjemahan bertambah dari 446 kunci pesan per bahasa menjadi 683. |

Pemeriksaan VexAC yang disertakan mencakup Fly, Speed, Timer, Phase, Step, NoSlow, GroundSpoof, Reach, KillAura, AimAssist, pukulan menembus dinding, BadPackets, pola waktu AutoClick, knockback yang diubah, Scaffold, Tower, FastPlace, Nuker, dan jangkauan blok. UI-nya memakai label hanya memantau, sementara kode yang dikompilasi juga memiliki jalur kick; pastikan perilaku moderasi yang sebenarnya di server uji sebelum mengandalkan label tersebut. Build sebelumnya berisi kontrol Anti AutoClick dan Anti Fly lama sebagai gantinya.

## Persiapan dan penggunaan lengkap dengan `/mhgui`

### 1. Instal build gabungan

1. Hentikan sepenuhnya server **Paper 1.21.11 / Java 21** dan cadangkan dunia serta data plugin.
2. Tempatkan hanya `VexLandManhunt-2.0.0.jar` dari rilis ini di `plugins/`. Pindahkan JAR Manhunt lama dan GrimAC mandiri keluar dari direktori plugin aktif. Pertahankan folder datanya; jangan menghapusnya. Pemain tidak menginstal JAR ini pada klien.
3. Mulai secara normal alih-alih menggunakan `/reload`. Pemuat terintegrasi mengelola siklus hidup Grim dan PacketEvents.
4. Sebagai OP atau dengan `vexland.admin`, jalankan `/vexintegration`. Periksa `Grim=ACTIVE` dan `PacketEvents=true` sebelum melanjutkan ke `/mhgui`. Perlindungan yang tidak aktif adalah masalah proses mulai, bukan instalasi terintegrasi yang berhasil.

Konfigurasi Grim berada di `plugins/VexLandManhunt/grim/` (`config.yml`, `messages.yml`, `punishments.yml`, `discord.yml`), dengan riwayat opsional `violations.sqlite`. Cadangan migrasi pertama ditempatkan di `plugins/VexLandManhunt-integration-backups/`; `plugins/VexLandManhunt/integration-migration-v1.txt` menandai penyelesaian. Jika data Grim lama dan terintegrasi sama-sama ada, tujuan terintegrasi dipertahankan dan peringatan dicatat. Migrasi menolak tautan simbolis.

Tinjau penanggung jawab koreksi gerakan di `plugins/VexLandManhunt/integration.properties`; pertahankan pengaturan lainnya. Nilai default instalasi baru:

```properties
movement-correction-owner=legacy
```

Panduan menu publik lengkap di bawah mengikuti dasar permainan 1.9.11 paket ini. Cabang spectator memiliki panduan arsipnya sendiri.

### 2. Buka pusat kendali

Bergabunglah ke server sebagai administrator dengan **OP** atau izin **`vexland.admin`**, lalu masukkan:

```text
/mhgui
```

Instruksi di bawah membahas antarmuka publik dalam rilis plugin **2.0.0**, menggunakan label tombol bahasa Inggris. Label mengikuti bahasa server yang dipilih. Untuk menggunakan seluruh GUI, gunakan akun **OP** yang tepercaya: izin dalam deskriptor memungkinkan membuka perintah, sedangkan beberapa handler GUI yang disertakan menerapkan pemeriksaan OP yang lebih ketat. Inventaris utama memiliki lima baris dengan sembilan slot per baris. Arahkan kursor ke tombol untuk membaca deskripsi dan pengaturan saat ini. Sebagian besar tombol menggunakan klik biasa; tindakan mouse khusus dan konfirmasi dijelaskan di bawah. Menu 1.6.4 yang lebih kecil dibahas di bagian akhir.

#### Siapkan pertandingan pertama Anda

1. Buka **Player Roles**. Klik kepala pemain setiap peserta sampai peran yang ditampilkan benar. Di 2.0.0, peran berganti antara **Runner** dan **Hunter**; peserta yang sebelumnya belum diberi peran menjadi Runner pada klik pertama. Klik kiri/kanan/shift bukan pintasan terpisah untuk memilih peran. Gunakan **Previous Page**, **Next Page**, dan **Back to Control Center** bila diperlukan.
2. Tetapkan setidaknya satu Runner dan setidaknya satu Hunter. Prosedur mulai dapat mengubah pemain online lain yang belum diberi peran menjadi Hunter, jadi menetapkan setiap peserta secara eksplisit membuat susunan tim jelas.
3. Klik **Friendly Fire** untuk memilih apakah rekan satu tim dapat saling melukai. Periksa indikator ON/OFF setelah mengklik.
4. Klik **Language** untuk memilih bahasa seluruh server. Pengaturan ini memengaruhi pesan, antarmuka, pemberitahuan, dan buku panduan untuk semua orang, bukan hanya pemain Anda sendiri.
5. Tinjau **Smart Hunter Kit**, **Auto World Spawn**, dan **Anti-Cheat**. Baca panduan administrator dari tombol buku jika Anda membutuhkan penjelasan di dalam game.
6. Pastikan **Server Freeze** mati, lalu klik **Start Match**. Memulai pertandingan menyiapkan pemain dan inventaris mereka, menjalankan pengenalan dan roulette waktu keunggulan awal acak bagi Runner sebelum Hunter dilepaskan, lalu memulai perburuan. Simpan apa pun yang Anda perlukan di luar inventaris peserta sebelum memulai.

#### Tombol pusat kendali utama

Posisi di bawah menghitung baris dari atas ke bawah dan kolom dari kiri ke kanan. Posisi ini menggambarkan tata letak akhir 2.0.0 yang telah dihias.

| Posisi | Tombol bahasa Inggris | Fungsinya |
|---|---|---|
| Baris 2, kolom 2 | Player Roles | Membuka menu kepala pemain Runner/Hunter dengan beberapa halaman. |
| Baris 2, kolom 3 | Target Player | Berganti di antara pemain online lain untuk tindakan admin pada target terpilih. Periksa nama target saat ini. |
| Baris 2, kolom 4 | Friendly Fire | Mengaktifkan/menonaktifkan kerusakan antar rekan tim. |
| Baris 2, kolom 5 | Match Info | Mengirim laporan singkat tentang status pertandingan, tim, friendly fire, dan target terpilih. |
| Baris 2, kolom 6 | Start Match | Menjalankan awal pertandingan normal dan rangkaian keunggulan awal acak. |
| Baris 2, kolom 7 | Full Heal | Memulihkan kesehatan semua pemain online. |
| Baris 2, kolom 8 | Reset Match | Melakukan reset pertandingan penuh. Ini berbeda dari Reset Settings. |
| Baris 3, kolom 2 | Full Hunger | Memulihkan makanan dan saturasi semua pemain online. |
| Baris 3, kolom 3 | Release Hunters | Melepaskan Hunter yang menunggu sebelum waktu keunggulan awal berakhir. |
| Baris 3, kolom 4 | Clear Effects | Menghapus efek potion dari semua pemain online. |
| Baris 3, kolom 5 | Server Freeze | Mengaktifkan/menonaktifkan pembekuan server global; pemain biasa tanpa OP dibekukan. |
| Baris 3, kolom 6 | Clear Target Inventory | Mengosongkan inventaris, armor, dan tangan sekunder pemain terpilih setelah konfirmasi. |
| Baris 3, kolom 7 | Teleport Everyone | Membawa semua pemain online ke posisi Anda saat ini. |
| Baris 3, kolom 8 | Kill Target | Membunuh pemain terpilih setelah konfirmasi; aturan kematian normal dapat memengaruhi pertandingan. |
| Baris 4, kolom 2 | Anti-Cheat | Membuka kontrol VexAC Security. |
| Baris 4, kolom 3 | Freeze Target | Mengaktifkan/menonaktifkan pembekuan individual pemain terpilih. |
| Baris 4, kolom 4 | Emergency Restore | Memulihkan kesehatan, makanan, dan saturasi semua pemain online. |
| Baris 4, kolom 5 | Freeze Team | Klik kiri mengaktifkan/menonaktifkan pembekuan Runner; klik kanan melakukan hal yang sama untuk Hunter; shift-klik menghapus pembekuan individual/tim. |
| Baris 4, kolom 6 | Set Day | Mengubah dunia Anda saat ini menjadi siang hari. |
| Baris 4, kolom 7 | Clear Weather | Menghentikan hujan dan petir di dunia Anda saat ini. |
| Baris 4, kolom 8 | Language | Membuka pemilih bahasa global. |
| Baris 5, kolom 2 | Smart Hunter Kit | Mengaktifkan/menonaktifkan kit respawn Hunter adaptif; menampilkan ON/OFF. |
| Baris 5, kolom 3 | Clear Dropped Items | Menghapus entitas item yang jatuh di dunia Anda saat ini. |
| Baris 5, kolom 4 | Pause Match / Resume Match | Menghentikan atau melanjutkan permainan aktif dan timer pertandingan. |
| Baris 5, kolom 5 | Emergency Sync | Menyinkronkan ulang peran pemain, pelacak, dan status runtime terkait. |
| Baris 5, kolom 6 | Reset Settings | Memulihkan pengaturan seimbang setelah konfirmasi dua klik. |
| Baris 5, kolom 7 | Close | Menutup pusat kendali. |
| Baris 5, kolom 8 | Auto World Spawn | Membuka pemilih interval spawn Overworld otomatis. |
| Baris 5, kolom 9 | Manhunt Administrator Guide | Memberikan buku panduan administrator yang dilokalkan. |

Kaca dekoratif dan item judul/status bukan tombol permainan.

#### Peran dan target terpilih

**Player Roles** mengubah tim Manhunt peserta yang sebenarnya. Klik kepala mereka dan baca peran yang diperbarui. Selama STARTING/RUNNING, antarmuka mengizinkan perubahan Runner/Hunter tetapi menolak mengubah Runner terakhir menjadi Hunter. Ini mempertahankan pihak Runner dalam pertandingan yang berlangsung. Lakukan perubahan peran dengan sengaja karena runtime tim dan pelacak disinkronkan setelah perubahan.

**Target Player** adalah pilihan terpisah: tombol ini memilih seseorang untuk tindakan seperti Freeze Target, Clear Target Inventory, atau Kill Target tanpa mengubah timnya. Terus ganti pilihan sampai nama pemain online yang dimaksud ditampilkan. Jika target yang disimpan tidak lagi tersedia, kode dapat beralih ke pemain online lain yang pertama ditemukan, jadi selalu pastikan namanya tepat sebelum melakukan tindakan pada target terpilih. Jika tidak ada orang lain yang online, antarmuka melaporkan bahwa target tidak tersedia.

**Clear Target Inventory** dan **Kill Target** mengharuskan Anda mengklik tindakan yang sama untuk target yang sama dua kali dalam **lima detik**. Klik pertama menyiapkan konfirmasi dan mengidentifikasi target; klik kedua menjalankan tindakan. Mengganti target atau menunggu terlalu lama membutuhkan konfirmasi baru. Mengosongkan inventaris menghapus isinya; membunuh Runner dapat mengakhiri atau mengubah pertandingan sesuai aturan kematian normal.

**Freeze Team** memiliki satu-satunya pintasan mouse khusus tim dalam menu ini: klik kiri biasa memilih tim Runner, klik kanan biasa memilih tim Hunter, dan shift-klik menghapus semua pembekuan individual/tim yang dikelola oleh alat ini. Sakelar Server Freeze global merupakan kontrol terpisah dan harus dimatikan secara terpisah jika pemain masih dibekukan.

#### Smart Hunter Kit

Klik **Smart Hunter Kit** untuk mengaktifkan atau menonaktifkan kit respawn Hunter adaptif. Tombol menampilkan status saat ini. Ketika aktif, Hunter yang respawn dapat menerima kit yang disesuaikan dengan perlengkapan Runner dan konteks pertandingan; panduan pemain yang disertakan menggambarkan kit ini lebih lemah dari rata-rata Runner. Ketika mati, Hunter tidak mendapat kit otomatis setelah kematian. Ini tidak menonaktifkan kompas pelacak.

Untuk menetapkan pengaturan secara langsung alih-alih mengganti statusnya, gunakan `/mhkit on`, `/mhkit off`, atau `/mhkit status`. Nilai fallback konfigurasi baru yang diperiksa adalah ON.

#### Auto World Spawn

Klik **Auto World Spawn**, lalu pilih **OFF**, **5 minutes**, **10 minutes**, **15 minutes**, **20 minutes**, atau **30 minutes**. Memilih opsi menyimpannya dan mengembalikan Anda ke `/mhgui`; **Back** kembali tanpa memilih interval baru.

Ketika aktif, sistem secara berkala mencari permukaan Overworld yang aman di dekat Runner Overworld aktif dan memindahkan spawn dunia ke sana. Perpindahan dilewati jika tidak ada Runner di Overworld atau tidak ditemukan kandidat yang aman. Nilai fallback konfigurasi baru adalah OFF. Untuk kontrol yang sama melalui perintah, gunakan `/mhspawn off`, `/mhspawn 15`, atau `/mhspawn status`, dengan interval yang didukung sebagai pengganti 15.

#### Jeda, koneksi ulang, dan pemulihan

**Pause Match** tersedia ketika pertandingan berstatus RUNNING. Tombol ini membekukan sistem permainan, pergerakan/interaksi, timer pertandingan, pelacakan, dan perpindahan spawn. **Resume Match** melanjutkan sistem tersebut dan mengompensasi waktu jeda. Server Freeze hanya membekukan pemain dan tidak boleh digunakan sebagai pengganti ketika Anda perlu menghentikan jam pertandingan.

Batas waktu koneksi ulang Runner dapat dikonfigurasi, dengan nilai fallback instalasi baru **15 menit**. Bergabung kembali tepat waktu memulihkan status Runner dan memberikan perlindungan sepuluh detik saat bergabung kembali. Waktu server tidak aktif tidak mengurangi waktu koneksi ulang yang disimpan. Slot Runner yang kedaluwarsa menjadi Hunter; habisnya batas waktu Runner terakhir dapat memberikan kemenangan kepada Hunter.

**Tidak ada pemilih durasi koneksi ulang terpisah dalam GUI 2.0.0 yang disediakan.** Untuk menyesuaikannya, hentikan server, edit `plugins/VexLandManhunt/config.yml`, pertahankan pengaturan lainnya, dan tetapkan:

```yaml
features:
  custom-reconnect-minutes: 15
```

Restart setelah mengedit. Nilai di bawah satu menit dibatasi menjadi satu menit. **Reset Settings** mengembalikan nilai ini ke 15 menit. Build yang dikompilasi juga menyimpan status pertandingan/koneksi ulang dan snapshot cadangan untuk pemulihan setelah restart/crash server; biarkan plugin mengelola berkas tersebut alih-alih mengeditnya saat permainan berlangsung.

#### Reset Settings dan Reset Match

**Reset Settings** mengharuskan tombol diklik dua kali dalam **delapan detik**. Klik pertama menyiapkan konfirmasi; klik kedua memulihkan **Smart Kit ON**, **Auto Spawn setiap 15 menit**, **Reconnect 15 menit**, dan **keunggulan awal acak**. Ini berbeda dari instalasi baru, ketika Auto World Spawn memiliki fallback OFF. Tindakan ini mengubah konfigurasi; tidak menggantikan reset pertandingan penuh.

**Reset Match** melakukan reset pertandingan yang sudah ada, membersihkan status/item pertandingan sementara, dan mengembalikan pemain ke spawn Overworld untuk ronde berikutnya. Tombol utamanya tidak menggunakan konfirmasi dua klik Reset Settings. **Start Match** dapat menyiapkan/mengosongkan inventaris peserta. Periksa kontrol reset/mulai yang hendak Anda gunakan sebelum mengklik.

#### Kontrol bahasa dan anti-cheat

**Language** membuka pemilih global. Klik nama bahasa yang Anda inginkan. Kedua build yang disediakan berisi bahasa Inggris, Persia, Arab, Spanyol, Prancis, Jerman, Rusia, Tionghoa Sederhana, Hindi, dan Portugis. Bahasa yang dipilih digunakan bersama oleh seluruh server dan disimpan. Dokumentasi README bahasa Jepang tidak menambahkan bahasa Jepang ke pemilih dalam game plugin.

**Anti-Cheat** membuka **VexAC Security**. Klik **VexAC Master** untuk mengaktifkan/menonaktifkan mesin internal, atau klik **Movement**, **Combat**, **AutoClick**, **Velocity / AntiKB**, atau **World / Scaffold** untuk mengaktifkan/menonaktifkan grup tersebut. **Anti X-Ray** mengaktifkan/menonaktifkan Anti-Xray yang dikonfigurasi di Paper; restart server untuk menerapkan perubahan tersebut. Item status, log bukti, dan model deteksi menjelaskan sistem saat ini. **Back to Control Center** kembali ke menu utama.

Antarmuka build menggambarkan moderasi yang hanya memantau, tetapi pemeriksaan statis tetap menemukan jalur kick berbasis ambang batas. Perlakukan keterangan menu yang menyatakan tidak ada kick sebagai perbedaan antara implementasi dan dokumentasi, lalu pastikan perilaku moderasi di server yang terkendali sebelum mengandalkannya.

#### GrimAC terintegrasi dan VexAC lama

GUI **VexAC Security** yang ada mengontrol mesin VexAC lama; tombol Master/grupnya bukan panel kontrol Grim baru. GrimAC terintegrasi berjalan berdampingan dengannya. Gunakan `/vexintegration` untuk status modul dan perintah bawaan `/grim` atau `/grimac` untuk perintah Grim sendiri serta alat yang dikontrol oleh izin. Pengaturan Grim dan aturan hukumannya berada di `plugins/VexLandManhunt/grim/`.

Menu pemantau/grup GrimBridge 1.13.1 dan `grim-settings.yml` tidak mendeskripsikan paket ini. Jangan menganggap bahwa mematikan VexAC juga menonaktifkan GrimAC terintegrasi, atau bahwa label pemantau menetapkan kebijakan tanpa pengeluaran pemain. Paper Anti-Xray tetap merupakan pengaturan independen yang memerlukan mulai ulang.

#### Panduan dalam game dan pemecahan masalah

Klik **Manhunt Administrator Guide** atau gunakan `/mhhelp` untuk mendapatkan buku panduan yang dilokalkan. Pemain dapat menggunakan `/mhhelp` untuk mendapatkan panduan sesuai peran di 2.0.0. Hunter mengklik kanan kompasnya untuk memilih Runner; antarmuka pelacak ini terpisah dari pemilih Target Player milik administrator.

Jika peran atau pelacak tampak tidak sinkron, **Emergency Sync** menyegarkan status runtime terkait. **Match Info** membantu memeriksa tim dan status saat ini. Jika upaya memulai gagal, periksa bahwa pertandingan siap, pembekuan server mati, dan tim Runner/Hunter tersedia. Setelah mengganti JAR, gunakan restart server penuh alih-alih `/reload`. `/mhdebug` adalah perintah diagnostik administrator yang disertakan dalam 2.0.0; keberadaannya bukan klaim bahwa rilis ini telah lulus pengujian di server langsung.

#### Menggunakan pusat kendali 1.6.4 yang lebih lama

1.6.4 tetap memiliki **Player Roles**, **Friendly Fire**, **Start Match**, **Reset Match**, **Release Hunters Now**, **Server Lock**, **Teleport Everyone To Me**, **Heal & Feed Everyone**, **Match Status**, pemilihan bahasa, **Anti Cheat**, dan panduan administrator. Perannya berganti dalam urutan **None → Runner → Hunter**, dan perubahan peran dikunci saat pertandingan sedang dimulai/berlangsung.

Menu anti-cheat-nya berisi **Anti AutoClick** lama (aturan 30-CPS dengan penanganan peringatan/kick), **Anti Fly**, dan Paper **Anti X-Ray**. Batas waktu koneksi ulang Runner ditetapkan pada **60 menit**. Sakelar Smart Hunter Kit V3 yang baru, pemilih Auto World Spawn, jeda/lanjutkan, konfirmasi Reset Settings, serta alat target terpilih/dunia yang diperluas sebagaimana dijelaskan di atas merupakan fitur 2.0.0 dan tidak dapat diharapkan ada dalam menu lama.

Panduan ini disusun dari metadata JAR yang disediakan, teks bahasa/bantuan yang dibundel, dan disassembly statis. Antarmuka tidak dijalankan di server Minecraft langsung selama pemeriksaan ini.

### 3. Mainkan pengejaran

Runner melarikan diri selama waktu keunggulan awal acak dan berprogres menuju tujuan mengalahkan Ender Dragon. Hunter menunggu pelepasan, lalu mengklik kanan kompas pelacaknya untuk memilih Runner. Target dapat diubah selama permainan, termasuk ketika pengejaran melintasi dimensi. Gunakan `/teammsg <message>` untuk berbicara hanya kepada tim Anda dan `/mhhelp` untuk panduan peran yang dilokalkan di 2.0.0.

Jika Runner mati, Runner lain tetap bermain dan pemain yang mati menjadi Hunter. Hunter dapat respawn dan melanjutkan pelacakan. Kematian Runner terakhir atau habisnya batas waktu setelah Runner terputus dapat mengakhiri pertandingan dengan kemenangan Hunter; kekalahan Ender Dragon mengakhirinya dengan kemenangan Runner.

### 4. Jeda, akhiri, dan siapkan pertandingan berikutnya

Di 2.0.0, jeda dengan `/mhpause` dan lanjutkan dengan `/mhresume`. Gunakan `/mhrelease` jika Hunter perlu dilepaskan sebelum hitung mundur keunggulan awal berakhir. Untuk pertandingan baru, gunakan reset penuh pusat kendali atau `/mhreset`; reset membersihkan status dan item pertandingan sementara serta mengembalikan pemain ke spawn Overworld. Mengubah pengaturan Paper Anti-Xray membutuhkan restart.

## Pengaturan default dalam paket gabungan 2.0.0

Nilai fallback konfigurasi baru yang diperiksa adalah:

```yaml
features:
  adaptive-hunter-kit: true
  auto-world-spawn-minutes: 0
  custom-reconnect-minutes: 15
```

`0` berarti perpindahan spawn otomatis mati. Tindakan reset pengaturan yang dikonfirmasi dalam GUI menetapkan interval spawn menjadi 15 menit sebagai gantinya. Gunakan GUI atau `/mhkit` dan `/mhspawn` untuk pengaturan yang sesuai.

## Referensi perintah publik — gabungan 2.0.0

Perintah administrator memerlukan OP atau `vexland.admin` (default OP). Obrolan tim, tempat sampah, dan penglihatan malam adalah utilitas pemain; `/mhhelp` memberikan panduan sesuai peran. Tabel ini mencantumkan 17 perintah Manhunt/integrasi; perintah bawaan Grim memiliki izinnya sendiri. `/mhnone` tidak didaftarkan di sini.

| Perintah | Tujuan |
| --- | --- |
| `/vexintegration` | Laporkan status Grim terintegrasi, VexAC, PacketEvents, dan pemilik Bukkit bersama |
| `/mhgui` | Membuka pusat kendali |
| `/mhstart` | Menjalankan rangkaian awal pertandingan penuh |
| `/mhreset` | Mereset pertandingan saat ini sepenuhnya |
| `/mhrelease` | Melepaskan Hunter lebih awal |
| `/mrunner <player>` | Menetapkan Runner |
| `/mhunter <player>` | Menetapkan Hunter |
| `/teammsg <message>` | Mengirim pesan pribadi kepada rekan tim |
| `/trash` | Membuka inventaris 54 slot untuk membuang item |
| `/nv` | Mengaktifkan/menonaktifkan penglihatan malam pribadi |
| `/mhlang` | Membuka pemilih bahasa global |
| `/mhhelp` | Menerima buku panduan yang dilokalkan |
| `/mhkit <on\|off\|toggle\|status>` | Mengonfigurasi kit Smart Hunter |
| `/mhspawn <off\|5\|10\|15\|20\|30\|status>` | Mengonfigurasi perpindahan spawn otomatis |
| `/mhpause` | Menjeda pertandingan yang berlangsung |
| `/mhresume` | Melanjutkan pertandingan yang dijeda |
| `/mhdebug` | Menjalankan diagnostik internal |

## Bahasa dalam game dan dokumentasi

Paket ini mempertahankan **10 bahasa game**: Inggris, Persia, Arab, Spanyol, Prancis, Jerman, Rusia, Mandarin Sederhana, Hindi, dan Portugis. Setiap terjemahan yang disertakan memiliki **683 kunci**, mengikuti 1.9.11. `/mhlang` menetapkan satu bahasa untuk seluruh server, yang disimpan di `language.txt`.

Dokumentasi proyek tersedia dalam **18 bahasa**, tanpa edisi dokumentasi berbahasa Arab. Terjemahan ini tidak menambahkan bahasa Jepang atau bahasa dalam game tambahan lainnya ke biner yang tidak diubah.

## Riwayat versi, sumber, dan kredit

[CHANGELOG.md](../CHANGELOG.md) mencatat setiap rilis yang disediakan. [Panduan spectator 1.13.1](archive/1.13.1/README.id.md) lengkap dan [panduan lama 1.9.11 / 1.6.4](archive/1.9.11/README.id.md) tetap tersedia. Setiap versi yang disediakan mempertahankan unduhan dan checksum-nya sendiri.

**Manhunt dibuat bersama oleh Bardiya / Farland_game dan Ali / Alivexor. GrimAC adalah proyek terpisah oleh GrimAC / DefineOutside dan para kontributor.** Artefak terintegrasi ini memodifikasi tiga kelas Grim; ini bukan biner resmi Grim tanpa perubahan dari rilis lama yang terdiri dari dua berkas. [Paket sumber](https://github.com/FarlandGame/Vexland_Manhunt/releases/download/v2.0.0/VexLandManhunt-2.0.0-source.zip) pendamping mempertahankan sumber, skrip build, input dependensi, dan pemberitahuan yang disediakan, dengan bukti pengujian/runtime dihilangkan dan kode sumber tidak diubah. Rilis ini juga menyertakan teks GPLv3, checksum, dan [pemberitahuan pihak ketiga](../THIRD_PARTY_NOTICES.md). Tidak ada pengujian server langsung atau build yang dapat direproduksi yang dilakukan selama publikasi ini.

## Tantangan bercanda untuk Dream

Sedikit candaan Minecraft dari Bardiya 😄

> "Huh... Ali dan aku membuat plugin Manhunt seratus kali lebih baik daripada punya Dream, tetapi Dream takut dan tidak mau memainkan punya kami!"

## Pembuat dan cakupan proyek

**Dibuat bersama oleh [Bardiya Alizadeh (Kabir) · Farland_game](https://github.com/FarlandGame) dan [Ali · Alivexor](https://github.com/Alivexor).** Kedua nama pengguna tersebut juga tercatat sebagai penulis dalam deskriptor plugin asli.

Repositori ini menyajikan rilis asli yang telah dikompilasi, dokumentasinya, dan catatan versi sebagai proyek portofolio bersama. Deskripsi fitur didasarkan pada pemeriksaan statis terhadap JAR yang disediakan. Kompatibilitas server langsung, kinerja pemulihan, keseimbangan, dan akurasi anti-cheat belum diuji dalam proses publikasi ini.

[Portofolio GitHub Bardiya](https://github.com/FarlandGame) · [GitHub Ali](https://github.com/Alivexor) · [Semua rilis](https://github.com/FarlandGame/Vexland_Manhunt/releases)
