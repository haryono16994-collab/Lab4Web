# Lab 4 - Box Element

Halaman HTML sederhana untuk latihan properti CSS `float` dan `clear` pada elemen `div`. Empat kotak berwarna ditampilkan untuk melihat bagaimana elemen mengambang (float) dan bagaimana `clear` memindahkannya ke baris berikutnya.

## File

| File | Keterangan |
|------|------------|
| `lab4box.html` | Halaman tunggal berisi HTML dan CSS (internal `<style>`) |

## Cara Menjalankan

1. Simpan `lab4box.html` di komputer.
2. Buka file tersebut di browser (klik dua kali atau gunakan Live Server di VS Code).

Tidak memerlukan instalasi atau koneksi internet.

## Struktur HTML

```
<body>
├── <header>   → judul "Box Element"
└── <section>
    ├── div.div1  (Div 1)
    ├── div.div2  (Div 2)
    ├── div.div3  (Div 3)
    └── div.div4  (Div 4)
```

## Penjelasan CSS

| Elemen | Warna | Properti penting |
|--------|-------|------------------|
| semua `div` | - | `float: left`, `padding: 10px` |
| `.div1` | Merah | mengikuti aturan `div` |
| `.div2` | Kuning | mengikuti aturan `div` |
| `.div3` | Hijau | mengikuti aturan `div` |
| `.div4` | Biru | `clear: left`, `float: none` |

## Hasil yang Diharapkan

- **Div 1, Div 2, dan Div 3** mengambang ke kiri sehingga tersusun berjajar secara horizontal (merah, kuning, hijau). Lebar masing-masing mengikuti isi teksnya ditambah padding 10px.
- **Div 4** tidak lagi mengambang (`float: none`) dan memakai `clear: left`, sehingga turun ke bawah barisan kotak sebelumnya dan tampil sebagai blok selebar penuh.

## Konsep yang Dipelajari

- `float: left` membuat elemen mengambang ke kiri dan elemen berikutnya mengalir di sampingnya.
- `clear: left` memaksa elemen berada di bawah elemen yang mengambang ke kiri.
- `padding` menambah ruang di dalam kotak.
- Pemilihan elemen dengan selector tag (`div`) dan selector class (`.div1` dst.).

## Catatan

- Tag `<style>` diletakkan setelah `</body>`. Browser tetap menampilkannya dengan benar, tetapi praktik yang baik adalah menaruhnya di dalam `<head>` atau memisahkannya ke file `.css`.
- Meta viewport sudah ada, tetapi halaman ini hanya demonstrasi layout dasar dan belum memuat gaya responsif.
