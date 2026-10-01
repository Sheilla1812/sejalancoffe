# Sejalan Coffee POS

Sistem POS sederhana PHP Native + MySQL untuk Sejalan Coffee.

## Fitur
- Customer scan QR meja, tanpa login.
- Pilih menu, quantity, Normal/Less/Non Sugar, catatan, nama.
- Pesanan masuk ke dashboard kasir.
- Kasir wajib login.
- Status order dan pembayaran Cash/QRIS/Debit.
- Dashboard kasir, laporan, dan export Excel.
- Export Excel dari browser menggunakan SheetJS.
- Logo Sejalan Coffee sudah disertakan.

## Instalasi XAMPP
1. Salin folder `sejalan-coffee` ke `C:/xampp/htdocs/`.
2. Jalankan Apache dan MySQL.
3. Buka phpMyAdmin dan import `database/sejalan_coffee.sql`.
4. Pastikan `config/database.php` sesuai username/password MySQL.
5. Buka `http://localhost/sejalan-coffee/`.
6. Customer demo: `http://localhost/sejalan-coffee/customer/order.php?table=01`.
7. Login: `http://localhost/sejalan-coffee/login.php`.

Demo account:
- kasir / password

## QR meja
Setiap QR meja cukup mengarah ke URL seperti:
`http://alamat-domain/sejalan-coffee/customer/order.php?table=01`

Untuk produksi, gunakan HTTPS dan domain hosting. QR Code bisa dibuat dari URL tersebut menggunakan generator QR pilihan café.

## Catatan QRIS
Upload/kelola gambar QRIS asli café sebelum pembayaran QRIS dipakai. Prototype ini sengaja tidak membuat QRIS palsu.

## Catatan produksi
Untuk real-time yang lebih instan, polling 10 detik pada dashboard kasir dapat diganti WebSocket. Untuk café kecil/menengah, polling sudah cukup sederhana.
