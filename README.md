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
