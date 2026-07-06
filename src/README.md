# src

Folder sumber utama aplikasi React. Berisi seluruh kode logika, komponen, styling, dan konfigurasi internal aplikasi.

## Struktur Folder

```
src/
├── assets/       # Gambar, ikon, dan aset yang diimpor oleh bundler
├── components/   # Komponen UI yang dapat digunakan ulang (reusable)
├── pages/        # Halaman-halaman utama aplikasi (routing)
├── services/     # Service layer untuk komunikasi API/eksternal
├── types/        # Definisi tipe TypeScript (interfaces, types)
├── utils/        # Fungsi-fungsi helper dan utilitas
├── App.tsx       # Komponen root aplikasi
├── App.css       # Styling khusus App
├── main.tsx      # Entry point aplikasi React
└── index.css     # Styling global (Tailwind CSS imports)
```

## Teknologi

- **React 19** — Library UI
- **TypeScript 6** — Type safety
- **Tailwind CSS 4** — Utility-first CSS
- **Vite 8** — Build tool dan dev server
- **Zustand** — State management
- **Axios** — HTTP client
- **Lucide React** — Icon library

## Development

```bash
npm run dev       # Menjalankan dev server
npm run build     # Build untuk production
npm run lint      # Jalankan ESLint
npm run preview   # Preview hasil build
```
