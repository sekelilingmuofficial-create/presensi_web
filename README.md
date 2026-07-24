# Presensi — Landing Page

Landing page statis untuk **Presensi**, aplikasi absensi karyawan dengan verifikasi foto selfie dan lokasi GPS real-time. Dibangun murni dengan HTML, CSS, dan vanilla JavaScript — tanpa framework, tanpa build step — supaya mudah di-*host* di mana saja, termasuk GitHub Pages.

Desain dan tangkapan layar diambil langsung dari mockup aplikasi mobile & dashboard admin Presensi.

## Struktur folder

```
presensi-landing/
├── index.html              # Halaman utama (satu halaman, semua section)
├── css/
│   └── style.css           # Design tokens, layout, responsive rules
├── js/
│   └── script.js           # Menu mobile + animasi scroll reveal
├── assets/
│   ├── img/
│   │   ├── logo.png             # Logo Presensi
│   │   ├── favicon-32.png       # Favicon
│   │   ├── favicon-192.png      # Ikon apple-touch
│   │   ├── dashboard.png        # Screenshot dashboard web admin
│   │   └── promo-poster.png     # Poster promosi (referensi/arsip)
│   └── screens/
│       ├── login.png
│       ├── beranda.png
│       ├── presensi_lokasi.png
│       ├── presensi_foto.png
│       ├── verifikasi.png
│       ├── berhasil.png
│       ├── riwayat.png
│       └── profil.png
└── README.md
```

## Menjalankan secara lokal

Tidak perlu instalasi apa pun. Cukup buka `index.html` langsung di browser, atau jalankan server statis sederhana agar path relatif berjalan mulus:

```bash
# Python
python3 -m http.server 8000

# atau Node
npx serve .
```

Lalu buka `http://localhost:8000`.

## Deploy ke GitHub Pages

1. Push folder ini sebagai repo baru di GitHub.
2. Buka **Settings → Pages**.
3. Pada **Source**, pilih branch `main` dan folder `/ (root)`.
4. Simpan — halaman akan tersedia di `https://<username>.github.io/<nama-repo>/` dalam beberapa menit.

## Kustomisasi

Semua warna, tipografi, dan ukuran radius diatur sebagai custom property CSS di bagian atas `css/style.css` (`:root { ... }`), jadi mengganti palet atau font cukup dilakukan di satu tempat:

```css
:root{
  --ink:  #17181C;
  --red:  #E31E2B;
  --green:#1FAE5C;
  --font-display: 'Sora', sans-serif;
  --font-body:    'Inter', sans-serif;
  --font-mono:    'JetBrains Mono', monospace;
}
```

Teks tombol "Unduh di Google Play / App Store" pada bagian CTA sengaja dibuat sebagai tombol teks generik (bukan logo resmi Google Play / App Store) — ganti dengan tautan unduh sebenarnya begitu aplikasi sudah tayang di toko, dan pertimbangkan memakai badge resmi sesuai brand guideline masing-masing platform.

## Lisensi aset

Logo, tangkapan layar aplikasi, dan poster promosi adalah milik proyek Presensi. Sesuaikan lisensi kode (mis. MIT) sesuai kebutuhan sebelum repo dipublikasikan.
