# Services

Folder untuk menyimpan service layer yang menangani komunikasi dengan API eksternal atau layanan pihak ketiga.

## Panduan

- Gunakan folder ini untuk semua pemanggilan HTTP (REST API, GraphQL, dll).
- Manfaatkan **Axios** yang sudah terinstall sebagai HTTP client.
- Pisahkan service berdasarkan domain/modul (contoh: `auth.service.ts`, `user.service.ts`).
- Selalu definisikan tipe return di setiap service function.

## Contoh Struktur

```
services/
├── index.tsx            # Re-export semua service
├── api.client.ts        # Instance Axios yang sudah dikonfigurasi
├── auth.service.ts      # Service untuk autentikasi
├── user.service.ts      # Service untuk data user
└── product.service.ts   # Service untuk data produk
```

## Contoh Penggunaan

```tsx
// services/api.client.ts
import axios from 'axios'

const apiClient = axios.create({
  baseURL: import.meta.env.VITE_API_URL,
  headers: { 'Content-Type': 'application/json' },
})

export default apiClient

// services/user.service.ts
import apiClient from './api.client'
import { User } from '../types'

export const userService = {
  getAll: () => apiClient.get<User[]>('/users'),
  getById: (id: string) => apiClient.get<User>(`/users/${id}`),
}
```
