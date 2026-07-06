# Hooks

Folder untuk menyimpan custom hook React yang berisi logika reusable dan dapat dipakai oleh beberapa komponen.

## Tujuan

- Memisahkan logika dari tampilan UI.
- Mengurangi duplikasi kode antar komponen.
- Membuat logika lebih mudah dipelihara dan diuji.

## Kapan Menggunakan Hook

Gunakan custom hook ketika:

- ada logika stateful yang dipakai di lebih dari satu komponen;
- ingin mengelola efek samping seperti fetching data, local storage, atau event listener;
- ingin memecah logika kompleks agar komponen tetap sederhana.

## Konvensi Penamaan

- Nama file sebaiknya diawali dengan `use`, contoh: `useAuth.ts`, `useLocalStorage.ts`.
- Satu hook biasanya menangani satu tanggung jawab tertentu.
- Hook sebaiknya mengembalikan nilai yang jelas dan mudah dipakai oleh komponen.
- Hindari menaruh logika bisnis yang terlalu kompleks langsung di dalam komponen.

## Contoh Struktur

```text
hooks/
├── useAuth.ts
├── useLocalStorage.ts
└── useDebounce.ts
```

## Contoh Sederhana

```tsx
import { useState } from 'react'

export function useCounter() {
  const [count, setCount] = useState(0)

  const increment = () => setCount((prev) => prev + 1)
  const decrement = () => setCount((prev) => prev - 1)

  return { count, increment, decrement }
}
```

Folder ini saat ini masih kosong dan siap untuk diisi dengan custom hook sesuai kebutuhan aplikasi.
