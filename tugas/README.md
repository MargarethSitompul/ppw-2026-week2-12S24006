# Portofolio Web — ppw-2026-week2-12S24006

Halaman web portofolio profil profesional tunggal (*single page showcase webpage*) yang dibuat untuk memenuhi Tugas Mandiri Mahasiswa (Individual Assignment) minggu ke-2 mata kuliah Pemrograman Web.

**Judul Tugas:** Pengembangan Halaman Web Portofolio & Layanan Interaktif *Accessible* Berbasis HTML5 dan Modern CSS

## Identitas

| Keterangan | Isi |
|---|---|
| Nama | (ganti dengan nama lengkap Anda)* |
| NIM | 12S24006 |
| Program Studi | Sistem Informasi (Computer Information Systems) |
| Institusi | Institut Teknologi Del |

## Demo Live

Situs ini dipublikasikan melalui GitHub Pages di:
`https://<username-github-anda>.github.io/ppw-2026-week2-12S24006/`

*(Tautan aktif setelah repositori dipublikasikan — lihat panduan deployment di bawah.)*

## Struktur Berkas

```
ppw-2026-week2-12S24006/
├── index.html      # Struktur & konten halaman
├── style.css       # Seluruh styling (CSS eksternal)
└── README.md        # Dokumen ini
```

## Ringkasan Fitur & Pemenuhan Kriteria

**1. Struktur Semantik HTML5**
Halaman menggunakan `<header>` (logo & navigasi), `<nav>`, `<main>` dengan tiga `<section>` (`#tentang`, `#portofolio`, `#layanan`), `<aside>` (kartu "Sekilas Fakta"), dan `<footer>`. Elemen `<div>` hanya dipakai sebagai pembungkus tata letak, bukan pengganti elemen bermakna.

**2. Data Tabular & Lists**
Tabel riwayat proyek pada bagian "Portofolio Karya" memuat `<caption>`, `<thead>`, `<tbody>`, `<tfoot>`, serta atribut `scope="col"` dan `scope="row"`. Bagian ini juga memuat dua jenis daftar HTML: `<ol>` (alur kerja proyek, karena memang berurutan) dan `<ul>` (daftar kompetensi dan bidang peminatan).

**3. Formulir Interaktif & Accessible**
Formulir pada bagian "Formulir Layanan" dikelompokkan dalam dua `<fieldset>` dengan `<legend>` ("Data Pemohon" dan "Detail Permintaan"), dan memuat delapan tipe kontrol input: `text`, `email`, `tel`, `number`, `radio`, `checkbox`, `select`, dan `textarea`. Setiap kontrol memiliki `<label for="...">` eksplisit, dan seluruh isian wajib memakai atribut `required`.

**4. Estetika & Tata Letak CSS Modern**
`style.css` menerapkan *universal box-sizing reset*, palet warna dengan proporsi 60% netral, 30% teks/struktur gelap, dan 10% aksen teal, tipografi modern (Fraunces untuk judul, Inter untuk isi), sudut membulat, bayangan lembut, tata letak CSS Grid dan Flexbox, serta *media query* `@media (max-width: 768px)` agar tetap responsif di layar ponsel.

**5. Pengelolaan Git & GitHub Pages**
Lihat panduan deployment di bawah untuk mengunggah proyek ini ke repositori `ppw-2026-week2-12S24006` dan mengaktifkan GitHub Pages.

## Panduan Deployment ke GitHub Pages

1. Buat repositori publik baru di GitHub dengan nama persis `ppw-2026-week2-12S24006`.
2. Di folder proyek ini (berisi `index.html`, `style.css`, `README.md`), jalankan:
   ```bash
   git init
   git add .
   git commit -m "Inisialisasi portofolio tugas mandiri"
   git branch -M main
   git remote add origin https://github.com/<username-github-anda>/ppw-2026-week2-12S24006.git
   git push -u origin main
   ```
3. Buka repositori di GitHub, masuk ke **Settings > Pages**.
4. Pada bagian **Source**, pilih branch `main` dan folder `/ (root)`, lalu klik **Save**.
4. Tunggu beberapa menit, situs akan aktif di alamat yang ditampilkan GitHub Pages, lalu tempelkan alamat tersebut ke bagian "Demo Live" pada README ini.

## Catatan

- Ganti seluruh data contoh (nama, email, tautan GitHub) pada `index.html` dan README ini dengan data Anda yang sebenarnya sebelum dikumpulkan.
- Formulir pada halaman ini bersifat demonstratif (belum terhubung ke backend sungguhan); atribut `action="/api/submit"` dapat diarahkan ke endpoint nyata jika diperlukan pada tugas lanjutan.