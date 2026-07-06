# Components

Folder untuk menyimpan komponen-komponen UI yang dapat digunakan ulang (*reusable components*).

## Panduan

- Komponen di sini harus bersifat **reusable** dan tidak terikat pada halaman tertentu.
- Setiap komponen sebaiknya memiliki folder tersendiri dengan file komponennya.
- Komponen yang kompleks sebaiknya dipecah menjadi sub-komponen.

## Contoh Struktur

```
components/
├── Button/
│   └── index.tsx
├── Modal/
│   └── index.tsx
├── Navbar/
│   ├── index.tsx
│   └── NavbarItem.tsx
└── Card/
    └── index.tsx
```

## Konvensi Penamaan

- Gunakan **PascalCase** untuk nama file komponen: `Button.tsx`, `Navbar.tsx`
- Ekspor komponen utama lewat `index.tsx` agar import lebih bersih
- Simpan props type di file yang sama atau buat file `.types.ts` terpisah
