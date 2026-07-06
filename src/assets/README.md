# Assets

Folder untuk menyimpan aset statis yang diimpor langsung oleh kode, seperti gambar, ikon, SVG, dan font.

## Cara Penggunaan

File di folder ini akan di-bundle oleh Vite dan diberi hash pada nama file-nya saat production build (contoh: `hero-abc123.png`).

```tsx
// Contoh import gambar
import heroImage from './assets/hero.png'

// Di JSX
<img src={heroImage} alt="Hero" />
```

## Perbedaan dengan `public/`

| Aspek | `src/assets/` | `public/` |
|-------|---------------|-----------|
| Diproses bundler | ✅ Ya | ❌ Tidak |
| Diimpor di kode | ✅ Ya | ❌ Tidak (pakai path absolut) |
| Hash pada filename | ✅ Ya | ❌ Tidak |
| Tree-shaking | ✅ Ya | ❌ Tidak |

Gunakan folder ini untuk aset yang digunakan di dalam komponen. Gunakan `public/` untuk file seperti `favicon.ico` atau `manifest.json`.
