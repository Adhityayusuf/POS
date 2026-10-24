# POS

Belajar **routing dan controller** pada Laravel lewat simulasi etalase
toko (point of sale). Tiap kategori produk punya halaman sendiri,
dipisah per controller dan view Blade.

## Fitur

- Halaman utama (`/`) dari `HomeController`
- Katalog produk per kategori:
  - `/category/food-beverage` — makanan & minuman
  - `/category/beauty-health` — kecantikan & kesehatan
  - `/category/home-care` — perawatan rumah
  - `/category/baby-kid` — ibu & anak
- Halaman penjualan (`/sales`) dari `SalesController`
- Contoh route dengan parameter ganda: `/user/{id}/name/{name}`
  dari `UserController`

## Struktur

```
app/Http/Controllers/
├── HomeController.php
├── ProductController.php   # 4 kategori produk
├── SalesController.php
└── UserController.php
resources/views/
├── home.blade.php
├── products/*.blade.php    # 1 view per kategori
├── sales/index.blade.php
└── user/profile.blade.php
```

## Instalasi

```bash
composer install
cp .env.example .env
php artisan key:generate
php artisan serve
```

## Tech Stack

- PHP ^8.2, Laravel, Blade

## Konteks

Praktikum Pemrograman Web Lanjut, Politeknik Negeri Malang (Polinema).
