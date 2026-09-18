# QR 3D - GitHub Pages (Rp0)

Project statis untuk:
QR Code -> scan HP -> viewer model 3D interaktif.

Tidak memakai PHP, MySQL, hosting berbayar, atau database.

## Isi
- index.html = daftar objek
- viewer.html = viewer model 3D
- qr.html = generator QR otomatis
- models/ = file GLB
- assets/ = CSS + konfigurasi daftar model

Model contoh:
- CPU
- RAM
- GPU
- SSD

## Cara pasang di GitHub Pages

1. Login ke GitHub.
2. Buat repository PUBLIC, contoh: `qr-3d-informatika`.
3. Upload seluruh ISI folder project ini ke root repository.
   Pastikan `index.html` berada langsung di root repository.
4. Buka repository -> Settings -> Pages.
5. Pada Build and deployment:
   - Source: Deploy from a branch
   - Branch: main
   - Folder: / (root)
6. Save.
7. Setelah Pages aktif, buka URL yang diberikan GitHub.

Contoh alamat project:
https://USERNAME.github.io/qr-3d-informatika/

## Membuat QR

Setelah website sudah aktif:
1. Buka website GitHub Pages.
2. Pilih `QR Code` pada objek.
3. Klik `Download QR PNG`.
4. Cetak/tempel QR tersebut.

PENTING:
Buat/download QR dari website GitHub Pages yang sudah online,
bukan dari file lokal di komputer, supaya URL yang masuk ke QR benar.

## Mengganti model

Ganti file `.glb` pada folder models, atau tambahkan model baru.
Daftar objek ada di `assets/models.js`.

Contoh tambah:
printer: {
  name: "Printer",
  file: "models/printer.glb",
  desc: "Model printer."
}

Lalu upload `printer.glb` ke folder models.

## Catatan
Viewer memakai Google <model-viewer> melalui CDN dan generator QR memakai qrcodejs melalui CDN,
jadi HP membutuhkan koneksi internet ketika membuka viewer.
