# Public

Folder untuk aset statis yang tidak perlu diproses oleh Vite/bundler.

File yang ada di folder ini akan disalin langsung ke folder `dist/` saat build dan bisa diakses secara publik dari root path (`/`).

## Contoh Penggunaan

- `favicon.ico`
- `robots.txt`
- `manifest.json`
- Gambar atau file statis lainnya yang dirujuk tanpa import

## Catatan

Jangan pindahkan file yang perlu diimpor oleh kode (seperti gambar yang dipakai di komponen) ke folder ini. Gunakan `src/assets/` untuk file yang harus di-bundle.
