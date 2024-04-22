<h1 align="center">Proyek praujikom-main hadiyanfikran 👋</h1>

![Landing Page](https://github.com/hadiyanfikran/praujikom/assets/140688425/47bd94d3-b367-4391-ab1c-7cf56694ed0a)

---

<h2 id="tentang">🤔 Apa Konsep web yang saya buat?</h2>

Aplikasi digital perpustakaan dengan tata letak yang modern dan bersih, halaman ini menampilkan hero section yang mencolok, bersama dengan deskripsi layanan, ulasan, dan bagian lokasi yang mudah diakses.

<h2 id="fitur">🤨 Fitur apa aja sih yg ada di proyek ini?</h2>

-   [Mazer Bootstrap Template](https://github.com/zuramai/mazer)
    -   Mode gelap dan mode terang 
    -   Dashboard UI
-   Halaman Awal (Landing Page)
    -   Halaman home
    -   data buku
    -   data anggota
    -   data petugas
    -   data peminjam
    -   logout
-   Authentication
    -   Pendaftaran (register)
    -   Login
-   Multi User
    -   Admin
        -   Pengguna yang dapat dikelola 
        -   Buku yang dapat dikelola
        -   Genre (Kategori) buku yang dapat dikelola
        -   Melihat semua data secara keseluruhan (widget ui)
        -   Generate Laporan (EXCEL, CSV, HTML, PDF)
    -   Petugas
        -   Menangani penerimaan / peminjaman buku
        -   Generate Laporan (EXCEL, CSV, HTML, PDF)
    -   Peminjam / Pembaca
        -   Mencari buku
        -   Memberikan Rating dan Ulasan buku
        -   Daftar keinginan buku (whislist / bookmark)
        -   Melihat peminjaman buku mereka sendiri
        -   Register (membuat akun sebagai peminjam)
    -   Semua
        -   Mengulas buku di Halaman Awal
        -   Login
        -   Logout
-   Pencarian Halaman Awal (Landing Page)
    -   Buku
    -   Genre (kategori) Buku

<h2 id="testing-account">👤 Akun Default untuk Pengujian</h2>

### 🧖 Petugas

-   Nama Pengguna: adminal group
-   Kata Sandi: password

### 🧗 Peminjam

-   Nama Pengguna: zoro
-   Kata Sandi: password

<h2 id="demo">🏦 ERD & Relasi antar tabel</h2>

![ERD](https://github.com/hbtw25/perpus-v2/blob/main/erd.png?raw=true)

![RAT](https://github.com/hbtw25/perpus-v2/blob/main/relasiantartabel.png?raw=true)

Tabel Failed_Jobs, Personal_access_tokens, Password_reset_tokens, migrations abaikan saja karna bawaan dari Laravel.


<h2 id="demo">🏦 UML Diagram Use Case</h2>

![UML](https://github.com/hbtw25/perpus-v2/blob/main/uml.jpeg?raw=true)


<h2 id="demo">🏠 Halaman Demo</h2>

<p>Halaman demo saat ini tidak tersedia. Oleh karena itu, disarankan untuk mencobanya secara lokal dengan mengikuti langkah-langkah instalasi di bawah ini.</p>

<h2 id="pre-requisite">💾 Prasyarat</h2>

<p>Berikut adalah prasyarat yang diperlukan untuk menginstal dan menjalankan aplikasi.</p>

-   PHP 8.2.8 & Web Server (Apache, Lighttpd, atau Nginx)
-   Database (MariaDB dengan v11.0.3 atau PostgreSQL)
-   Web Browser (Firefox, Safari, Opera, dll)

<h2 id="installation">💻 Instalasi</h2>

<h3 id="develop-yourself">🏃‍♂️ Mengembangkan Sendiri</h3>
1. Klona repositori

```bash
git clone https://github.com/hbtw25/perpus-v2.git
cd perpus-v2
composer install
npm install
cp .env.example .env
```

2. Konfigurasi database melalui file `.env`

```conf
APP_DEBUG=true
DB_DATABASE=autodidak
DB_USERNAME=root
DB_PASSWORD=
```

3. Migrasi dan symlink

```bash
php artisan key:generate
php artisan storage:link
php artisan migrate --seed
```

4. Mulai situs web

```bash
npm run dev
# Jalankan di terminal yang berbeda
php artisan serve
```

<h3 id="develop-docker">🐳 Mengembangkan dengan Docker</h3>

-   Klona repositori:

```bash
git clone https://github.com/hbtw25/perpus-v2.git
cd autodidak
```

-   Salin file `.env.example` dengan `cp .env.example .env` dan konfigurasikan database:

```conf
APP_DEBUG=true
DB_HOST=mariadb
DB_DATABASE=autodidak
DB_USERNAME=root
DB_PASSWORD=
```

-   Pastikan Anda telah menginstal Docker dan jalankan:

```bash
docker compose up --build -d
```

-   Instal dependensi:

```bash
docker compose run --rm composer install
docker compose run --rm npm install
```

-   Setup Laravel:

```bash
docker compose run --rm laravel-setup
```

-   Jalankan secara lokal:

```bash
docker compose run --rm --service-ports npm run dev
```

-   Halaman
-   -   PhpMyAdmin: `http://127.0.0.1:8000`

<h4 id="docker-commands">🔐 Perintah</h4>

-   Composer
-   -   `docker-compose run --rm composer install`
-   -   `docker-compose run --rm composer require laravel/breeze --dev`
-   -   Dsb

-   NPM
-   -   `docker-compose run --rm npm install`
-   -   `docker-compose run --rm --service-ports npm run dev`
-   -   Dsb

-   Artisan
-   -   `docker-compose run --rm artisan serve`
-   -   `docker-compose run --rm artisan route:list`
-   -   Dsb

