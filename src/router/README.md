# Router

Folder untuk menyimpan konfigurasi routing aplikasi menggunakan **React Router**.

## Cara Kerja

File `index.tsx` di folder ini adalah **pusat deklarasi semua route** aplikasi. Setiap halaman yang dibuat di `src/pages/` harus didaftarkan di sini agar bisa diakses.

## Struktur

router/
├── README.md # Dokumentasi ini
└── index.tsx # Konfigurasi semua route


## Cara Menambah Route Baru

1. Buat halaman baru di `src/pages/`, contoh: `About.tsx`
2. Import halaman tersebut di `src/router/index.tsx`
3. Tambahkan route baru di array `createBrowserRouter`

**Contoh:**

```tsx
// 1. Buat src/pages/About.tsx
export default function About() {
  return <h1>About Page</h1>
}

// 2. Di src/router/index.tsx, import dan tambahkan:
import About from '../pages/About'

const router = createBrowserRouter([
  { path: '/', element: <Home /> },
  { path: '/about', element: <About /> },  // ← Tambah di sini
  { path: '*', element: <NotFound /> },
])

Fitur yang Didukung
Lazy Loading — Gunakan React.lazy() untuk code-splitting
Route Guards — Tambahkan wrapper untuk proteksi route
Nested Routes — Gunakan <Outlet /> untuk layout bertingkat
Dynamic Routes — Gunakan :id untuk parameter dinamis