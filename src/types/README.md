# Types

Folder untuk menyimpan semua definisi tipe TypeScript yang digunakan di seluruh aplikasi.

## Panduan

- Definisikan `interface` atau `type` di sini agar mudah ditemukan dan digunakan ulang.
- Pisahkan berdasarkan domain/modul (contoh: `user.types.ts`, `auth.types.ts`).
- Gunakan `export` agar bisa diimpor di file lain.
- Hindari menaruh logika bisnis — folder ini hanya untuk definisi tipe.

## Contoh Struktur

```
types/
├── index.tsx          # Re-export semua tipe
├── user.types.ts      # Tipe terkait user
├── auth.types.ts      # Tipe terkait autentikasi
├── api.types.ts       # Tipe umum untuk response API
└── common.types.ts    # Tipe umum yang sering dipakai
```

## Contoh Penggunaan

```tsx
// types/user.types.ts
export interface User {
  id: string
  name: string
  email: string
  role: 'admin' | 'user'
}

export type CreateUserPayload = Pick<User, 'name' | 'email' | 'role'>

// types/api.types.ts
export interface ApiResponse<T> {
  data: T
  message: string
  status: number
}
```
