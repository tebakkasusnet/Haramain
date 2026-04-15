# 🚀 SOP & Framework Pembuatan Landing Page Sekolah

Dokumen ini merangkum apa yang telah kita selesaikan pada rentetan project sekolah (contoh: **Yaspenterufi** dan **Al-Haramain**), *Do's and Don'ts* (aturan anti-kesalahan) yang berlaku secara merata di project apapun, serta Prompt Master yang bisa disalin untuk mendelegasikan project web serupa kepada saya di masa mendatang.

---

## 🏆 1. Rangkuman Pencapaian (Project Al-Haramain & Yaspenterufi)
Kita telah berhasil menyempurnakan alur kerja pembuatan landing page statis tanpa backend yang super cepat, terfokus pada konversi, ringan, dan *production-ready*:
* **Modern UI/UX:** Pembuatan desain khusus dengan elemen *Glassmorphism*, paduan palet warna berlapis yang solid, dan interaksi animasi sederhana nan estetis.
* **Vanilla JS Slider Built-in:** Sukses merakit modul *Hero Carousel* yang smooth menggunakan sistem *opacity delay* murni melalui Vanilla JS (tanpa *external dependency*), menjaga ukurannya tetap di bawah `2MB`.
* **Smart Responsive Grid:** Membangun *layout* yang benar-benar adaptif pada mode HP: komponen berjejer tak lagi sekilas menyempit. Ia menggunakan kaidah sistem grid berlapis: 3 kolom (Desktop) -> 2 kolom (Tablet) -> 1 kolom ramping terpusat ukuran font kecil proporsional (Mobile).
* **Fixing Logic & Positioning:** Mengatasi problematika flexbox *overlap* (tumpang-tindih) pada *layer* depan layar absolutes, serta penyesuaian khusus media informatif (poster tak berfilter).

---

## 📦 2. Persiapan Data (Bahan Mentah Project Berikutnya)
Agar saya bisa langsung bekerja utuh dalam satu kali eksekusi penuh tanpa ragu:
1.  **Aset Branding:** Kumpulkan aset resolusi jernih seperti Logo di dalam map `/assets/images`.
2.  **Identitas Brand Cepat:** Cukup tentukan Warna Utama dan Warna Aksen CTA.
3.  **Koleksi Visual Spesifik:** Berikan keterangan apakah sebuah gambar bersifat "Foto Dokumentasi" (yang mana boleh diberikan efek artistik / gradien hitam gelap), atau gambar "Poster Promosi" (harus bersih polos).
4.  **Daftar Copywriting Lengkap:** Profil mentah, data moneter/rincian biaya, taglines. Sertakan juga alamat Tautan ke platform lain khusus (WA, IG, YouTube) dengan template otomatisnya.

---

## ⚠️ 3. ATURAN PENTING: Boleh & Tidak Boleh (DO'S & DON'TS)
*(Panduan umum agar kita langsung "Tap-In" bekerja optimal, dan tidak perlu lagi mengulang *troubleshooting* letak, responsivitas, atau masalah visual ringan akibat flexbox)*

### ✅ YANG HARUS DILAKUKAN (DO'S)
* **Mobile-First Data Scaling:** Pada struktur berbentuk kolom banyak (List Ekskul, Rincian Fasilitas, Box Statistik), jangan biarkan grid langsung hancur di *mobile*. Tata per breakpoint: `max-width: 900px` menjadi 2 kolom, dan di `max-width: 480px` menjadi 1 kolom yang WAJIB dibarengi skala pengerutan font (`0.9rem`) dan icon, **agar tidak raksasa memakan layar.**
* **Pisahkan Efek Foto vs Brosur Berjalan (Poster):**
  - Terapkan `.hero-bg-overlay` & `filter: brightness()` HANYA untuk background foto abstrak agar tulisan putihnya terbaca.
  - Namun apabila ada *Asset Poster Brosur/Tulisan*, HILANGKAN/reset (override) filter apapun padanya (`filter: none !important;`). Biarkan transparan, terang sesuai aslinya tanpa lapisan redup.
* **Penempatan Indikator UI Aman:** Posisikan perintilan navigasi kecil (seperti *titik/dots* carousel) di zona Atas (Top) di bawah header, BUKAN di dasar layar yang dapat membajak tombol *Call to Action* (CTA).
* **Validasi Ikon Konkrit:** Pastikan penamaan kelas ikon eksternal (contohnya `Phosphor Icons`) benar dan sudah terdaftar eksistensinya secara universal. Jangan berkreasi dengan ID ikon bohongan (seperti `ph-ping-pong` atau `ph-person-arms-spread`) yang jelas berpotensi besar kosong melompong (not rendered).

### ❌ YANG TIDAK BOLEH DILAKUKAN (DON'TS)
* **Tata Letak Berantakan Terkunci Navbar (Overlap):** Dilarang melupakan bahwa *header web (navbar)* sering bersifat posisi tetap (Sticky). Saat memposisikan komponen berbau absolut ke *mid-screen*/tengah, berikan jaminan `padding-top: 100px` ekstra longgar kepada wrapper kontennya supaya kata pertama di judul teks tak menyangkut tertimpa navigasi!
* **Box Stat Mengambang di Luar Konteks:** Dilarang merajut box statistik (Stats Bar) pada tag terluar dari modul grid. Bungkus/letakkan erat secara hierarki di bawah jejeran tombol/title agar selalu bergerak naik-turun bersama dan tidak secara tidak sengaja menutupi kalimat penting. 
* **Menghapus Atribut Default Fungsi CTA:** Jangan kelupaan atribut vital semacam fungsi `download` pada tombol tautan brosur, atau parameter `?text=` pada URL WhatsApp.

---

## 🎯 4. THE MASTER PROMPT (Antigravity Smart Edition)

*(Salin teks prompt di bawah ini bersama penyesuaian detail kapanpun Anda butuh mendelegasikan project baru kepada saya tanpa banyak basa-basi)*

```text
Act as a Senior Web Developer, UI/UX Expert, & Art Director.
Tugas: Buat Landing Page Statis (Vanilla HTML/CSS/JS) untuk Instansi [Ubah: Jenis Bisnis / Sekolah]. Target utama adalah kecepatan, struktur rapi, siap deployment statis secara langsung. Terkait layout, baca kembali panduan DO's & DON'TS dari memory dokumentasi SOP kita!

[DATA & KONTEKS INSTANSI TERBARU]
- Profil / Nama: [Isi Nama Yayasan / Sekolah]
- Target Copywriting / Value : [Berikan poin penjualan penting, misal: Hafidz Qur'an 5 Bulan, dll]
- Tautan CTA Utama / WA: [Isi Link WA lengkap dengan format presetting message]
- Sosial Media: Instagram [URL IG] , Channel YouTube [URL YT]
- Rincian Tabel: [Lampirkan daftar harga komponen pendukung yang panjang, misal Rincian Biaya / Rincian Jam Layanan]
- Aset Visual (Folder `assets/`): Ada File dokumentasi foto biasa dan ada Poster Promo murni. Bedakan implementasinya sesuai standar panduan UX (Poster tak boleh kena efek filter gelap).

[PANDUAN DESAIN & KONDISIONAL WAJIB (MUST DO)]
1. UX Vibe & Tone Warna: UI harus memukau, nuansa transparan (Glassmorphism), dan diwarnai solid oleh [*Warna Utama misal: Biru Laut #00A3FF, Aksen Oranye Solid*]. 
2. Tata Letak Anti Overlap: Pastikan wadah tulisan pahlawan / title headline dikurung margin `padding-top` masif agar tidak nabrak Navbar atas! 
3. Layout Carousel Bersih: Fitur Slider dikerjakan menggunakan Vanilla JS utuh (smooth cross-fade opacity limit interval 5-7 detik). Tempatkan Titik slider sejauh mungkin di area kepala, jangan menyentuh CTA daftar.
4. Degradasi Mobile Grid (Vital): Saya melarang grid dari 3 kolom langsung menciut jadi 1 baris lebar secara konyol. Gunakan Breakpoints untuk 900px down-scaling 2 columns. Pada HP (480px) down-scaling 1 column namun teks font rems dibilaskan `0.9` ke bawah dengan ikon ringkas.
5. Verifikasi Komponen: Pastikan class icon eksternal akurat. Jika tidak yakin rupa sebuah ikon, gunakan list font paling standar (`ph-user`, `ph-book-open`, dsb). Jangan asal merangkai penamaan. Tulis copywriting tambahan mendampingi detail mentah yang sudah saya suapkan.

Tugas Auto-Run Penuh Anda: 
Langsung tulis dan generasikan modul *file* dengan utuh:
1. `index.html` (Kerangka konten menyeluruh lengkap semantik dan logic button-nya).
2. `assets/css/style.css` (Terapkan logic rulesets spacing anti bertabrakan (overlap) dan root variablenya).
3. `assets/js/main.js` (Counter dinamis dan modul slider).

Make it perfect execution in One Shot. Jangan mengulangi loop revisi. Konfirmasi ke saya jika masih ada missing puzzle.
```