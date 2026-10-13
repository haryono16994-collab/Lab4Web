# Layout Sederhana

Website statis multi-halaman yang dibuat dengan HTML dan CSS murni sebagai bagian dari tugas praktikum web. Proyek ini menunjukkan dasar pembuatan layout: header, navigasi, hero panel, konten utama, sidebar, dan footer.

## Daftar Halaman

| File | Halaman | Isi |
|------|---------|-----|
| `home.html` | Home | Hero panel, tiga kotak fitur dengan gambar bulat, dan dua artikel singkat, dilengkapi sidebar |
| `artikel.html` | Artikel | Dua entri artikel (gambar di kiri dan di kanan) dengan sidebar widget |
| `about.html` | About | Profil singkat, portofolio, dan daftar keahlian (HTML & CSS, JavaScript, Figma & Photoshop) |
| `kontak.html` | Kontak | Formulir kontak (nama, email, pesan) |
| `style.css` | - | Stylesheet yang dipakai bersama oleh semua halaman |

## Struktur Proyek

```
.
├── home.html
├── artikel.html
├── about.html
├── kontak.html
└── style.css
```

## Cara Menjalankan

Tidak perlu instalasi atau build. Cukup:

1. Simpan semua file dalam satu folder yang sama.
2. Buka `home.html` di browser (klik dua kali atau gunakan Live Server di VS Code).
3. Gunakan menu navigasi untuk berpindah antarhalaman.

> Koneksi internet diperlukan agar font Google Fonts dan gambar placeholder dari `dummyimage.com` dapat dimuat.

## Struktur Layout

Semua halaman memakai kerangka yang sama:

```
#container (980px, di tengah)
├── header          → judul situs
├── nav             → menu navigasi (link aktif diberi class "active")
├── #hero           → hanya di Home
├── #wrapper
│   ├── #main       → konten utama (640px)
│   └── #sidebar    → widget (260px)
└── footer
```

Halaman About dan Kontak tidak memakai sidebar, sehingga `#main` diberi `width: 100%`.

## Detail CSS

- **Font:** Open Sans (Google Fonts).
- **Reset:** `margin` dan `padding` semua elemen di-nol-kan.
- **Layout:** berbasis `float` dengan clearfix (`.row:after`, `.entry:after`) dan `footer { clear: both }`.
- **Navigasi:** latar biru `#1f5faa`, warna `#2b83ea` untuk link aktif dan saat di-hover.
- **Komponen:**
  - `.box`: kolom tiga sama lebar (33,33%) untuk fitur di Home
  - `.image-circle`: gambar berbentuk lingkaran
  - `.entry` dan `.right-img`: artikel dengan gambar di kiri atau kanan
  - `.widget-box`: kotak widget sidebar dengan header biru `#428bca`
  - `.btn`: tombol (`btn-large`, `btn-default`)
  - `.contact-form`: gaya input dan textarea dengan efek fokus
  - `.divider`: garis pemisah antarbagian

## Catatan dan Saran Pengembangan

- **Belum responsif.** Lebar `#container` tetap 980px meskipun sudah ada meta viewport. Pertimbangkan media query atau `max-width` agar nyaman di perangkat mobile.
- **Formulir kontak belum berfungsi.** Atribut `action="#"` belum terhubung ke backend atau layanan pengiriman email.
- **Gaya inline.** Beberapa halaman (About dan Kontak) memakai atribut `style` langsung di HTML. Sebaiknya dipindahkan ke `style.css`.
- **Aturan CSS ganda.** Selector seperti `.entry h2`, `.entry img`, dan `hr.divider` didefinisikan lebih dari sekali di `style.css` sehingga bisa dirapikan.
- **Font tidak terpakai.** `Open Sans Condensed` di-import tetapi belum digunakan.
- **Konten placeholder.** Teks Lorem ipsum dan gambar `dummyimage.com` perlu diganti dengan konten asli.
- Kelas `.btn`, `.btn-large`, dan `.btn-default` dipakai di HTML tetapi belum didefinisikan di `style.css`.

## Lisensi dan Kredit

&copy; 2021 - Universitas Pelita Bangsa
