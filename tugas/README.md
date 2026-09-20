# Portofolio mrgrt

Halaman web portofolio tunggal (single page) untuk tugas mandiri **Pengembangan Halaman Web Portofolio & Layanan Interaktif Accessible Berbasis HTML5 dan Modern CSS** (PPW minggu ke-2).

Struktur bagian halaman (Tentang Saya, Keahlian, Portofolio Karya, Formulir Layanan) mengikuti pola portofolio pengembang pada repositori acuan [rchll-16/my-portfolio](https://github.com/rchll-16/my-portfolio), tetapi dibuat dengan HTML5 dan CSS murni sesuai aturan modul.

**Demo langsung:** `https://USERNAME.github.io/ppw-2026-week2-12S24006/`

---

## Identitas

| Keterangan | Isi |
| --- | --- |
| Nama panggilan | mrgrt |
| NIM | 12S24006 |
| Program studi | Sistem Informasi (Computer Information Systems) |
| Kampus | Institut Teknologi Del, Balige |

---

## Teknologi

- HTML5 semantik (tanpa `<div>`)
- CSS3 modern: custom properties, Grid, Flexbox, `:user-invalid`, `prefers-color-scheme`
- Tanpa JavaScript dan tanpa framework

---

## Struktur berkas

```
ppw-2026-week2-12S24006/
├── index.html    # Halaman utama
├── style.css     # CSS eksternal
├── README.md     # Dokumentasi ini
└── LICENSE       # Lisensi MIT
```

---

## Kesesuaian dengan spesifikasi modul

| No | Persyaratan | Penerapan |
| --- | --- | --- |
| 1 | Struktur semantik HTML5 | `<header>` (logo dan `<nav>`), `<main>`, 5 `<section>` (termasuk Tentang Saya, Portofolio Karya, Formulir Layanan), 2 `<aside>`, `<footer>`. Tidak ada `<div>`. |
| 2 | Tabel dan daftar | Satu tabel lengkap (`<caption>`, `<thead>`, `<tbody>`, `<tfoot>`, `scope="col"` dan `scope="row"`), plus `<ul>` (navigasi, keahlian, kegiatan) dan `<ol>` (alur layanan). |
| 3 | Formulir accessible | 3 `<fieldset>` dengan `<legend>`; 8 tipe kontrol: text, email, tel, number, radio, checkbox, select, textarea; semua memakai `<label for>` dan `required`. |
| 4 | CSS modern | `style.css` eksternal, reset `box-sizing`, palet 60-30-10, tipografi Bricolage Grotesque dan Public Sans, `border-radius`, `box-shadow`, Grid dan Flexbox, `@media (max-width: 768px)`. |
| 5 | Git dan GitHub Pages | Repositori publik `ppw-2026-week2-12S24006`, dipublikasikan lewat GitHub Pages. |

### Palet warna 60-30-10

| Porsi | Peran | Warna terang | Warna gelap |
| --- | --- | --- | --- |
| 60% | Latar dan kartu | `#f3f6f5`, `#ffffff` | `#0c181d`, `#132228` |
| 30% | Header, footer, kartu identitas, kepala tabel | `#12404f` | `#1a5468` |
| 10% | Tombol dan sorotan (merah pita tenun) | `#b8322a` | `#ff8577` |

### Fitur aksesibilitas (WCAG 2.2 AA)

- Tautan "Lewati ke konten utama" di awal halaman
- Bahasa halaman ditetapkan (`lang="id"`) dan urutan judul (h1 sampai h4) berurutan
- Kontras teks dan komponen antarmuka memenuhi rasio AA pada mode terang dan gelap
- Indikator fokus keyboard yang jelas di semua tautan dan kontrol
- Ukuran target sentuh minimal 44 px pada tombol dan tautan navigasi
- Setiap kolom formulir punya label eksplisit, petunjuk (`aria-describedby`), dan atribut `autocomplete`
- Tabel dibungkus area yang bisa digulir dengan keyboard
- Animasi gulir halus hanya aktif jika pengguna tidak meminta pengurangan gerak
- Mode gelap otomatis mengikuti pengaturan sistem

---

## Menjalankan secara lokal

```bash
git clone https://github.com/USERNAME/ppw-2026-week2-12S24006.git
cd ppw-2026-week2-12S24006
```

Buka `index.html` di peramban. Tidak perlu instalasi apa pun.

---

## Deploy ke GitHub Pages

```bash
git init
git add .
git commit -m "feat: tambah halaman portofolio HTML5 dan CSS"
git branch -M main
git remote add origin https://github.com/USERNAME/ppw-2026-week2-12S24006.git
git push -u origin main
```

Lalu di GitHub: **Settings > Pages > Build and deployment > Source: Deploy from a branch > Branch: `main` / `(root)` > Save**. Tunggu satu sampai dua menit, lalu buka `https://USERNAME.github.io/ppw-2026-week2-12S24006/`.

---

## Catatan tentang formulir

Karena GitHub Pages hanya menyajikan berkas statis, formulir memakai validasi bawaan peramban dan menampilkan pesan konfirmasi lewat `:target` CSS. Data belum dikirim ke server. Untuk pengembangan lanjutan, ganti `action` dengan alamat layanan formulir (misalnya Formspree) dan ubah `method` menjadi `post`.

---

## Ide pengembangan

- Menambahkan tombol mode terang/gelap manual
- Menambahkan tautan demo langsung pada tiap karya unggulan
- Menambahkan sertifikat dan penghargaan pada bagian Tentang Saya

---

## Penulis

**mrgrt**, mahasiswa Sistem Informasi, Institut Teknologi Del.

## Lisensi

Proyek ini berlisensi **MIT**. Lihat berkas `LICENSE`.