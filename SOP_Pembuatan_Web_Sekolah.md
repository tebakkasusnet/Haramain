# 🚀 SOP & Framework Pembuatan Landing Page Sekolah

Dokumen ini merangkum apa yang telah kita selesaikan di **Project Yaspenterufi**, apa saja yang dibutuhkan untuk membuat project serupa di sekolah lain dengan sangat cepat, serta Prompt Master yang bisa kamu *"Copy-Paste"* ke saya (Antigravity) di masa depan.

---

## 🏆 1. Rangkuman Pencapaian (Project Yaspenterufi)
Kita telah berhasil membangun landing page statis tanpa backend yang sangat ringan, super cepat, terfokus pada konversi pendaftaran (PPDB), dan *production-ready*:
* **Modern UI/UX:** Desain khusus dengan *Glassmorphism*, palet warna spesifik (Medical Blue/Energetic Orange), tipografi modern (Google Fonts), dan hover animasi interaktif.
* **Layout Adaptif:** Grid bersistem untuk aktivitas (model strip 2 baris x 6 kolom yang stabil), dan sangat responsif ke ukuran tablet/HP.
* **Performa Bebas Kendala:** Dibuat menggunakan Vanilla HTML/CSS/JS murni. Memanfaatkan `IntersectionObserver` agar elemen muncul (fade-in) mulus saat di-scroll tanpa library eksternal.
* **Konversi Optimal:** Semua CTA pendaftaran diarahkan secara "Hardcode" via URL menuju WhatsApp CS dan unduhan tombol brosur *(download via <a> attribute)*, menihilkan kebutuhan server atau database tambahan.
* **Siap Deploy (Vercel-ready):** Struktur aset yang sudah disanitasi (`assets/images/`, `assets/css/`, `assets/js/`), menjadikan repositori sangat teratur dan proses naik *live* di Vercel semudah memencet tombol *import*.

---

## 📦 2. Persiapan Data untuk Project Sekolah Selanjutnya
Sebelum memulai chat/project sekolah baru berikutnya dengan saya, siapkan bahan peluru ini agar pengerjaan tuntas dalam sekali *Prompt*:

1.  **Aset Branding Asli:** File Logo Sekolah dalam format `PNG Transparan` (tanpa *background* putih).
2.  **Identitas Warna Khusus:** 1 Warna Utama (Primary) dan 1 Warna Aksen (Secondary/CTA). *(Misal: Emerald Forest & Sunrise Yellow).*
3.  **Koleksi Foto:** Jangan masukkan foto *low-res*. Kumpulkan minimal 6-12 foto jernih dokumentasi kegiatan siswa atau lingkungan belajar. Buatkan folder `assets/images` dan taruh semuanya di sana agar saya bisa langsung *mapping* namanya.
4.  **Aset Brosur:** File brosur PDF atau bentuk JPEG tunggal (`brosur.pdf` atau `.jpeg`).
5.  **Daftar Informasi Mentah / Copywriting Dasar:**
    * Sebutkan secara eksplisit "Nama Yayasan" dan "Nama Sekolah".
    * Tahun Berdiri, Akreditasi, dan Angka penting lainnya untuk statistik hero.
    * Daftar Jurusan Spesifik atau Unit pendidikan yang disediakan dengan deksripsi minimalis(1-2 kalimat).
    * Target URL WhatsApp penerimaan siswa lengkap.

---

## ⚙️ 3. Alur Kerja Replikatif Saya (The Antigravity Playbook)
Jika kamu memicu *Master Prompt* nanti, ini adalah langkah otomatis yang masuk ke "otak" saya sebagai standard framework:
1.  **[SCAFFOLDING]:** Inisiasi `index.html` dengan *boilerplates* yang matang, injeksi Google Fonts, dan penyematan *Phosphor Icons* CDN.
2.  **[DESIGN SYSTEM]:** Membangun `style.css` dengan mematok CSS Variables dasar (Warna brand baru, layout spacing, typography modern).
3.  **[SECTIONING]:** Pembangunan modular -> Beranda *Full Width* -> Info Sekolah Modular -> Panel Jurusan -> *Gallery Strip CSS-Grid* -> Footer navigasi cepat.
4.  **[WIRING]:** Menyambungkan logikal `main.js`. Khususnya logika `IntersectionObserver` untuk animasi kemunculan elemen.
5.  **[TESTING]:** Agent otomatis memastikan tidak ada masalah *overlap* posisi absolut/relatif antar layout menggunakan Browser Testing mandiri.

---

## 🛡️ 4. Aturan Validasi Khusus (Instruksi Tambahan)
*(Aturan wajib ini ditambahkan untuk memastikan fungsionalitas dan layout web tetap sempurna tanpa revisi berulang)*
* **Fungsi Autodownload:** Tombol unduh brosur WAJIB menggunakan atribut `download` pada tag `<a>` sehingga file langsung tersimpan ke perangkat pengguna, bukan sekadar membuka tab baru.
* **Integrasi Pesan WA Otomatis:** URL WhatsApp harus selalu menyertakan pre-filled text (parameter `?text=`).
* **Optimalisasi Resolusi Foto:** Jika foto buram, aplikasikan penyesuaian via CSS (seperti filter brightness/contrast). Diperbolehkan menduplikasi foto yang sama jika stok aset foto kurang.
* **Pengembangan Konten Estetik:** Diizinkan mengembangkan data valid yang ada menjadi *copywriting* tambahan yang menarik agar website terlihat lebih profesional.
* **Keamanan Margin & Spacing:** Perhatikan ekstra pada margin/padding kanan-kiri. Jangan sampai ada elemen, *assets*, atau teks yang saling tumpang tindih atau terlalu mepet ke ujung layar.
* **Optimalisasi Handphone (Mobile-First):** Wajib mengutamakan tampilan UI di layar HP.
* **Validasi Link Eksternal:** Pastikan tombol media sosial (Instagram dan YouTube) terhubung ke link yang tepat dan aktif.
* **Zero Mistake / Ask First:** Jika ada keraguan terkait tata letak atau data pendukung, agen (saya) diwajibkan bertanya terlebih dahulu untuk konfirmasi sebelum menyusun kode.

---

## 🎯 5. THE MASTER PROMPT (Copy-Paste Ini Sesuka Hati)

Simpan teks (kotak di bawah) ini pada catatanmu. Kapanpun kamu siap membuat project landing page untuk instansi/sekolah lain, sediakan satu folder kosong berisi foto-foto dan jalankan Prompt ini kepada saya:

```text
Act as a Senior Web Developer, UI/UX Expert, & Art Director.
Saya mau kamu buatkan Landing Page Statis (Vanilla HTML/CSS/JS) untuk PPDB Sekolah baru. Hindari Tailwind/React, buat strukturnya siap deploy Vercel (semua gambar sudah ada di assets/images).

[DATA & KONTEKS SEKOLAH]
- Nama Yayasan: [Isi Nama Yayasan]
- Instansi/Unit: [Isi Nama Sekolah/Banyak Jenjang]
- WhatsApp PPDB: [Isi No WA penuh]
- Template Pesan WA: [Contoh: "Assalamu'alaikum, saya ingin bertanya terkait Pendaftaran..."]
- Link Instagram: [Isi URL IG]
- Link YouTube: [Isi URL YT]
- File Unduhan Brosur: [Contoh: assets/brosur.pdf]
- Tagline Spesifik: [Misal: "Cerdas, Mandiri, dan Berakhlak Mulia"]
- Ciri Khas/Target: [Misal: Modern Islamic Boarding School / Vocational Engineering]

[PANDUAN DESAIN & FUNGSI WAJIB]
- UI Vibe: Highly Premium, Bersih, Dinamis, Modern. Terapkan Micro-animations saat hover, efek Glassmorphism untuk navbar/cards statis, dan border-radius/bayangan.
- Warna Primary (Kode HEX/Nama): [Contoh: Biru Muda #3B82F6]
- Warna Secondary/CTA: [Contoh: Oranye Solid]
- Tipografi: Padukan Outfit (Heading) & Inter (Body) atau kombinasi selaras lain dari Google Fonts.
- Layout Safety: Perhatikan margin kanan-kirinya! Beri padding/margin yang proporsional agar tidak terlalu dekat/mepet layar dan mencegah informasi tertimpa. Wajib optimalisasi sempurna untuk handphone.
- Handling Aset: Kembangkan tampilan sedemikian rupa, gunakan filter/enhance jika foto resolusinya kurang bagus. Gunakan foto duplikat jika stok kurang.
- Copywriting: Kembangkan poin informasi valid yang ada menjadi teks tambahan yang memikat.
- Validasi: Jangan sampai ada kesalahan. Jikalau ragu, kamu wajib bertanya ke saya untuk konfirmasi.

[STRUKTUR SEKSI]
1. Header/Navbar: Sticky dengan efek Glass. Pastikan link sosial media (Instagram & YouTube) terhubung dengan benar.
2. Hero Banner: Sangat atraktif. Heading besar, tombol CTA ganda. Tombol 1 terhubung WA dengan auto-template message. Tombol 2 bersifat Autodownload file brosur. Tambahkan "Stats Bar" mengambang rapi persis di bawahnya (Tahun, Akreditasi, Total Jurusan).
3. Tentang Instansi: Dua kolom -> 1 Foto resolusi tinggi (dengan frame modern) vs Text deksriptif poin keunggulan instansi.
4. Program Jenjang / Jurusan: Kartu-kartu Grid bersusunan rapi.
5. Galeri Ekstrakurikuler: Wajib gunakan arsitektur "CSS Grid Strip Layout" padat (horizontal menyambung rapat seperti dokumentasi sebelumnya) berjejer 2 baris.
6. Penutup (PPDB Banner & Footer Minimalist). Pastikan tautan IG dan YT sudah sinkron.

Kamu sepenuhnya diizinkan auto-run. Langsung generasikan file:
1. `index.html` (Terintegrasi utuh dengan atribut download dan WA url params)
2. `assets/css/style.css` (Lengkap variables, layout margin aman, intersection observer classes, responsif max 480px, grid layout stabil)
3. `assets/js/main.js` (Logika smooth-scroll & scroll listener)
Analisis dan sesuaikan nama-nama path gambar sesempurna mungkin!