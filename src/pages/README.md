# Pages

Folder untuk menyimpan halaman-halaman utama aplikasi yang mewakili setiap route/rute.

## Panduan

- Setiap halaman seharusnya mewakili satu route yang bisa diakses pengguna.
- Nama file sebaiknya sesuai dengan nama halaman (contoh: `Home.tsx`, `Login.tsx`, `Dashboard.tsx`).
- Halaman sebaiknya hanya mengatur komposisi komponen dari `components/` dan menangani data untuk route tersebut.
- Hindari menulis logika bisnis kompleks langsung di halaman — gunakan `services/` dan `utils/`.

## Contoh Struktur

```
pages/
├── index.tsx        # Re-export semua halaman
├── Home.tsx
├── Login.tsx
├── Dashboard.tsx
└── NotFound.tsx
```

## Contoh Penggunaan

```tsx
// pages/index.tsx
export { default as Home } from './Home'
export { default as Login } from './Login'
export { default as Dashboard } from './Dashboard'
```
