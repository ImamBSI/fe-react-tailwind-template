# Utils

Folder untuk menyimpan fungsi-fungsi utilitas dan helper yang digunakan di seluruh aplikasi.

## Panduan

- Fungsi di folder ini harus bersifat **pure** (tidak memiliki side effects) dan dapat diuji secara mandiri.
- Pisahkan berdasarkan kategori (contoh: `format.ts`, `validation.ts`, `date.ts`).
- Hindari menaruh logika yang berhubungan langsung dengan UI atau API di sini.
- Selalu sertakan tipe parameter dan return value.

## Contoh Struktur

```
utils/
├── index.tsx          # Re-export semua utilitas
├── format.ts          # Fungsi format (tanggal, angka, currency)
├── validation.ts      # Fungsi validasi (email, phone, dll)
├── storage.ts         # Helper untuk localStorage/sessionStorage
├── constants.ts       # Konstanta yang digunakan di aplikasi
└── helpers.ts         # Fungsi helper umum
```

## Contoh Penggunaan

```tsx
// utils/format.ts
export const formatCurrency = (amount: number): string => {
  return new Intl.NumberFormat('id-ID', {
    style: 'currency',
    currency: 'IDR',
  }).format(amount)
}

export const formatDate = (date: string | Date): string => {
  return new Intl.DateTimeFormat('id-ID', {
    dateStyle: 'long',
  }).format(new Date(date))
}
```
