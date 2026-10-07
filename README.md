# Laporan Praktikum Pemrograman Web: HTML5 Semantik & CSS3 Layout Responsif

**Mata Kuliah:** Pengembangan Aplikasi Web / Pemrograman Web  
**Tugas:** Pertemuan 02 & 03 (HTML5 Semantik dan CSS3 Layout Responsif: Flexbox & Grid)  
**Nama Mahasiswa:** Al-Bukhari Insan Kamil  
**NIM:** 20240140270  
**Topik:** Website Biografi Pahlawan Nasional (Ir. Soekarno)  

---

## 📌 Deskripsi Proyek
Proyek ini merupakan halaman profil dan biografi interaktif pahlawan nasional Republik Indonesia, **Ir. Soekarno**. Website ini dibangun dengan mengutamakan standar *semantic web* murni, aksesibilitas (*web accessibility/a11y*), performa ringan, serta layout responsif berbasis CSS Flexbox dan CSS Grid modern tanpa efek dekoratif berlebih (*formal-modern style*).

---

## 🖥️ Dokumentasi Tampilan Layar Desktop

Tampilan desktop menggunakan sistem layout **CSS Grid 2 Kolom** pada `.layout-wrapper` yang membagi area konten utama (`<main>`) dan kolom samping (`<aside>`), serta **Flexbox 1D** pada header dan navigasi horizontal.

### 1. Desktop - Header, Navigasi, Profil Tokoh & Sidebar Atas
![Desktop 1](screenshot/dekstop%201.png)
* **Penjelasan Singkat:**
  * Landmark `<header>` menampilkan badge pahlawan nasional, judul utama (`<h1>`), dan deskripsi singkat tokoh dengan latar marun formal.
  * Menu `<nav>` horizontal disusun menggunakan Flexbox dengan efek hover halus dan transisi fokus aksesibel.
  * Seksi `<section id="profil">` memuat potret tokoh menggunakan tag semantik `<figure>`, `<img>` dengan `alt` deskriptif, dan `<figcaption>`.
  * Kolom samping `<aside>` di sisi kanan menampilkan blok `<blockquote>` kutipan bersejarah serta informasi ringkas tokoh.

---

### 2. Desktop - Linimasa Jejak Perjuangan
![Desktop 2](screenshot/dekstop%202.png)
* **Penjelasan Singkat:**
  * Bagian `<section id="perjuangan">` memanfaatkan Ordered List (`<ol>`) dengan *custom counter badge* melingkar bernomor urut 1 sampai 5.
  * Setiap butir peristiwa dilengkapi tag semantik `<time>` untuk penanggalan terstruktur (1927, 1930, 1 Juni 1945, 17 Agustus 1945, 1955).
  * Di sebelah kanan, sidebar fakta singkat tokoh tetap tersusun berdampingan secara proporsional.

---

### 3. Desktop - Gagasan Besar (CSS Grid 3 Kolom) & Artikel Refleksi
![Desktop 3](screenshot/dekstop%203.png)
* **Penjelasan Singkat:**
  * Bagian `<section id="gagasan">` menampilkan 3 kartu pemikiran besar (Pancasila, Konsep Trisakti, dan Gerakan Non-Blok) menggunakan CSS Grid 2D: `repeat(3, minmax(0, 1fr))` dengan jarak `gap` yang presisi.
  * Di bawahnya terdapat landmark `<article id="refleksi">` yang berisi kajian reflektif relevansi nilai kepahlawanan Bung Karno di era digital dengan aksen border sebelah kiri.

---

### 4. Desktop - Form Buku Tamu Aksesibel & Footer
![Desktop 4](screenshot/dekstop%204.png)
* **Penjelasan Singkat:**
  * Bagian `<section id="buku-tamu">` dirancang memenuhi standar aksesibilitas WCAG: pasangan `<label for="...">` dan input `<input id="...">` saling terhubung eksplisit.
  * Kategori pengunjung dikelompokkan rapi menggunakan elemen `<fieldset>` dan `<legend>`.
  * Tombol submit memenuhi standar ukuran sentuh ramah pengguna (`min-height: 44px`).
  * Landmark `<footer>` di bagian bawah menyajikan informasi hak cipta dan keterangan tugas praktikum mahasiswa.

---

## 📱 Dokumentasi Tampilan Layar Mobile (Responsif $\le$ 768px)

Pada layar ponsel pintar (diuji hingga resolusi sempit 360px), layout 2-kolom otomatis bertransformasi menjadi **1 kolom vertikal** tanpa menyisakan *horizontal scrollbar*.

### 1. Mobile - Header, Navigasi & Profil Awal
![Mobile 1](screenshot/mobile%201.png)
* **Penjelasan Singkat:**
  * Tipografi judul pada `<header>` mengecil secara proporsional dan teks menu navigasi melakukan *flex-wrap* agar tetap terbaca nyaman.
  * Foto tokoh pada `<figure>` menyesuaikan lebar layar secara adaptif (`max-width: 100%`).

---

### 2. Mobile - Teks Profil & Awal Linimasa
![Mobile 2](screenshot/mobile%202.png)
* **Penjelasan Singkat:**
  * Paragraf biografi mengalir vertikal dengan spasi pembatas yang nyaman dibaca (*comfortable line-height: 1.65*).
  * Linimasa sejarah mulai ditampilkan dengan penanda nomor urut rapi di sisi kiri.

---

### 3. Mobile - Kelanjutan Linimasa Sejarah
![Mobile 3](screenshot/mobile%203.png)
* **Penjelasan Singkat:**
  * Rangkaian peristiwa (Pledoi 1930 hingga KAA 1955) tetap runtut dan jelas tanpa terpotong batas layar.

---

### 4. Mobile - Transformasi Grid Kartu Gagasan
![Mobile 4](screenshot/mobile%204.png)
* **Penjelasan Singkat:**
  * Fitur 3 kolom kartu gagasan secara otomatis ditransformasikan oleh media query menjadi **1 kolom vertikal stacked** (`grid-template-columns: 1fr`).
  * Setiap kartu mempertahankan padding dan keterbacaan teks yang optimal.

---

### 5. Mobile - Akhir Kartu Gagasan & Artikel Refleksi
![Mobile 5](screenshot/mobile%205.png)
* **Penjelasan Singkat:**
  * Kartu Gerakan Non-Blok tersaji utuh, diikuti kartu `<article>` refleksi era digital dengan garis aksen marun di sebelah kiri.

---

### 6. Mobile - Formulir Buku Tamu Ramah Sentuh
![Mobile 6](screenshot/mobile%206.png)
* **Penjelasan Singkat:**
  * Seluruh input teks, email, dan textarea membentang penuh (100% lebar kontainer) untuk memudahkan pengisian formulir di perangkat bergerak.
  * Tombol submit memenuhi lebar kontainer (*full-width touch target*) sehingga nyaman ditekan oleh jari.

---

### 7. Mobile - Sidebar Berpindah ke Bagian Bawah
![Mobile 7](screenshot/mobile%207.png)
* **Penjelasan Singkat:**
  * Sesuai hierarki DOM semantik, elemen `<aside>` berpindah ke urutan bawah konten `<main>`.
  * Kutipan inspiratif Bung Karno dan daftar awal fakta singkat tersaji rapi dalam kotak tersendiri.

---

### 8. Mobile - Lanjutan Fakta Singkat & Footer
![Mobile 8](screenshot/mobile%208.png)
* **Penjelasan Singkat:**
  * Daftar fakta singkat tokoh ditampilkan secara terstruktur per baris.
  * Area `<footer>` menutup halaman dengan susunan teks tengah yang rapi dan bebas dari kebocoran horizontal (*no horizontal overflow*).

---

## 🛠️ Ringkasan Pemenuhan Spesifikasi Praktikum
1. **HTML5 Semantik:** Menggunakan landmark `<header>`, `<nav>`, `<main>`, `<section>`, `<article>`, `<aside>`, dan `<footer>`.
2. **Aksesibilitas (A11y):** Form memiliki asosiasi eksplisit antara `<label>` dan `<input>`, pengelompokan `<fieldset>`/`<legend>`, serta outline fokus keyboard yang kontras (`:focus-visible`).
3. **CSS Layout Modern:**
   * **Flexbox:** Digunakan untuk menu navigasi horizontal dan perataan header.
   * **CSS Grid:** Digunakan untuk sistem 2-kolom desktop dan kartu 3-kolom gagasan besar.
4. **Desain Formal & Bersih:** Palet warna konsisten (`--primary-color: #7b1113`, putih, slate netral), tanpa bayangan tebal, tanpa animasi berat, dan 100% responsif pada layar ponsel $\ge 360\text{px}$.
