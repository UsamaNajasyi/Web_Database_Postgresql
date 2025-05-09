
# 📊 Web Data Streaming (Node.js + Socket.IO + PostgreSQL)

Aplikasi web ini menampilkan data dari database PostgreSQL secara real-time menggunakan Socket.IO dan Express. Cocok untuk dashboard data atau monitoring live.

## 🚀 Fitur
- Streaming data real-time dari tabel `users`.
- Koneksi database PostgreSQL yang otomatis reload saat `.env` berubah.
- Status koneksi database dikirim ke klien secara live.

## 📦 Teknologi
- Node.js + Express
- PostgreSQL (dengan `pg`)
- Socket.IO
- dotenv

## 🔧 Instalasi

1. **Clone repository:**

```bash
git clone https://github.com/username/namaproject.git
cd namaproject
```

2. **Install dependencies:**

```bash
npm install
```

3. **Siapkan file `.env`:**

```env
DB_USER=postgres
DB_HOST=localhost
DB_NAME=postgres
DB_PASS=yourpassword
DB_PORT=5432
```

> Pastikan database `users` dan tabel `users` sudah tersedia.

4. **Jalankan server:**

```bash
npm start
```

Akses di: [http://localhost:3000](http://localhost:3000)

## 📂 Struktur Proyek

```
/public          # File frontend (jika ada)
/server.js       # Server utama
/.env            # Konfigurasi koneksi database
```

## 📝 Catatan

- Aplikasi ini secara otomatis memeriksa perubahan pada file `.env` setiap 10 detik.
- Data dari tabel `users` diambil dan dikirim ke klien setiap 2 detik.
