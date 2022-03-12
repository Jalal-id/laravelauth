# Aplikasi Laravel Sederhana Dengan Autentikasi

Ini adalah contoh aplikasi Laravel sederhana dengan autentikasi (register, login, verifikasi email, lupa password) menggunakan bootstrap 5.

**Persiapan:**

-   Webserver (xampp)
-   Git Bash
-   Composer
-   Akun pengiriman email (mailtrap, mailgun dsb)

## Mulai

Arahkan direktori dimana anda akan menyimpan folder project, buka git bash lalu clone project ini menggunakan perintah:

```bash
git clone https://github.com/Jalal-id/simpleauthlaravel.git
```

Masuk direktori project:

```bash
cd simpleauthlaravel
```

Copy file `.env`

```bash
cp .env.example .env
```

Setting konfigurasi database & provider pengiriman email (tergantung akun masing-masing) pada file `.env`

```bash
DB_CONNECTION=mysql
DB_HOST=127.0.0.1
DB_PORT=3306
DB_DATABASE=db_tutorial
DB_USERNAME=root
DB_PASSWORD=

MAIL_MAILER=smtp
MAIL_HOST=smtp.mailtrap.io
MAIL_PORT=2525
MAIL_USERNAME=
MAIL_PASSWORD=
MAIL_ENCRYPTION=tls
MAIL_FROM_ADDRESS="hello@example.com"
MAIL_FROM_NAME="${APP_NAME}"
```

Install dependencies:

```bash
composer install
```

Set up database:

```bash
php artisan migrate
```

Jalankan aplikasi:

```bash
php artisan serve
```

Buka http://localhost:8000 atau http://127.0.0.1:8000 pada browser favorit anda.

## Routes yang tersedia

-   `/home`
-   `/login`
-   `/register`
-   `/password/reset`
-   `/verify-email/{id user}/{token}`
-   `/email/verify`

## License

The Laravel framework is open-sourced software licensed under the [MIT license](https://opensource.org/licenses/MIT).
