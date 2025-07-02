Cara Menjalankan Aplikasi
Clone repository ini

bash

git clone https://github.com/username/user-management-api.git
cd user-management-api
Install dependencies

bash

npm install
Siapkan database

Jalankan file setup.sql di MySQL Workbench:

Buat database user_management

Buat tabel users dan isi data awal

Jalankan server

bash

node app.js
Akses API di browser

Dokumentasi Swagger:
http://localhost:3000/api-docs

Get All Users:
GET http://localhost:3000/api/users

Endpoint API
Method	Endpoint	Deskripsi
POST	/api/users	Tambah user baru
GET	/api/users	Ambil semua user
PUT	/api/users/:id	Perbarui data user by ID
DELETE	/api/users/:id	Hapus user by ID


Tools
Node.js + Express

MySQL + mysql2

Joi (validasi)

Swagger UI


Berikut ini adalah **dokumentasi singkat tentang API User Management** yang telah kamu buat:

---

📄 Dokumentasi Singkat API: User Management

🔧 Base URL (lokal):

```
http://localhost:3000/api
```

---

📌 Endpoint & Penjelasan

1. **POST /users** – Tambah Pengguna

Deskripsi: Menambahkan pengguna baru
Body (JSON):

```json
{
  "name": "John Doe",
  "email": "john@example.com",
  "phone": "081234567890",
  "is_active": true,
  "department": "IT"
}
```

Validasi:

  * Email harus valid dan unik
  * Nomor telepon minimal 10 digit angka

---

 2. **GET /users** – Ambil Semua Pengguna

Deskripsi: Mengambil daftar seluruh pengguna dalam database
Response:

```json
[
  {
    "id": 1,
    "name": "John Doe",
    "email": "john@example.com",
    "phone": "081234567890",
    "is_active": true,
    "department": "IT"
  }
]
```

---

### 3. **PUT /users/\:id** – Perbarui Pengguna

* **Deskripsi**: Memperbarui data pengguna berdasarkan ID
* **Parameter URL**:

  * `id` → ID dari pengguna yang ingin diperbarui
* **Body (JSON)**:

```json
{
  "name": "Jane Doe",
  "email": "jane@example.com",
  "phone": "081298765432",
  "is_active": false,
  "department": "HR"
}
```

---

### 4. **DELETE /users/\:id** – Hapus Pengguna

* **Deskripsi**: Menghapus pengguna berdasarkan ID
* **Parameter URL**:

  * `id` → ID pengguna

---

## ✅ Format Data Pengguna

| Field        | Tipe    | Keterangan                    |
| ------------ | ------- | ----------------------------- |
| `name`       | string  | Nama lengkap pengguna         |
| `email`      | string  | Harus format email & unik     |
| `phone`      | string  | Hanya angka, min. 10 karakter |
| `is_active`  | boolean | Status aktif (`true/false`)   |
| `department` | string  | Nama departemen pengguna      |

---

## 🧪 Testing & Dokumentasi Interaktif

* Swagger UI tersedia di:

```
http://localhost:3000/api-docs
```

---



