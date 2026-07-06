# SIPESTISIDA - Sistem Informasi Persediaan Pestisida

Sistem informasi manajemen persediaan (inventory management) berbasis web untuk **PT. Ridho Agro Jaya**, perusahaan distribusi pestisida dan bahan kimia pertanian di Palembang, Sumatera Selatan.

🔗 **Live Demo:** [sipestisida.my.id](https://sipestisida.my.id)

---

## 📋 Tentang Proyek

SIPESTISIDA dikembangkan sebagai Tugas Akhir untuk membantu PT. Ridho Agro Jaya mengelola persediaan pestisida secara lebih efisien dan akurat. Sistem ini menangani **115 SKU produk** dengan fitur peramalan stok, klasifikasi prioritas produk, dan pelacakan batch untuk mencegah kerugian akibat produk kedaluwarsa.

## ✨ Fitur Utama

- **📊 Peramalan Stok (SMA Forecasting)** — Prediksi kebutuhan stok bulanan menggunakan metode Simple Moving Average, dievaluasi dengan MAPE (Mean Absolute Percentage Error)
- **📦 FEFO Batch Tracking** — Pelacakan batch produk dengan prinsip First Expired First Out untuk meminimalkan risiko kedaluwarsa
- **🔤 ABC Analysis** — Klasifikasi produk berdasarkan tingkat kepentingan (Kategori A: 47 produk, B: 38 produk, C: 30 produk)
- **📱 QR Code Integration** — Setiap produk memiliki QR code unik untuk mempercepat proses input dan pengecekan stok
- **📝 Stock Opname** — Modul pencatatan dan penyesuaian stok fisik secara berkala
- **📈 Laporan & Dashboard** — Visualisasi data persediaan, tren penjualan, dan performa stok secara real-time

## 🛠️ Teknologi yang Digunakan

| Kategori | Teknologi |
|---|---|
| Backend | Laravel 11, PHP 8.4 |
| Database | MySQL |
| Frontend | Blade Templating, Bootstrap |
| Build Tool | Vite |
| Version Control | Git & GitHub |

## 📂 Struktur Proyek

```
sipestisida/
├── app/
│   ├── Http/Controllers/    # Logika kontroler (produk, stok, laporan, dll)
│   ├── Models/               # Model Eloquent
│   └── Services/              # Logika bisnis (forecasting, ABC analysis)
├── database/
│   └── migrations/            # Struktur tabel database
├── resources/
│   └── views/                 # Tampilan Blade
├── routes/
│   └── web.php                 # Definisi routing
└── public/                     # Asset publik (CSS, JS, QR code)
```

## ⚙️ Instalasi Lokal

1. Clone repository ini
   ```bash
   git clone https://github.com/[username]/sipestisida.git
   cd sipestisida
   ```

2. Install dependency PHP
   ```bash
   composer install
   ```

3. Install dependency JavaScript
   ```bash
   npm install
   ```

4. Salin file environment dan sesuaikan konfigurasi database
   ```bash
   cp .env.example .env
   php artisan key:generate
   ```

5. Jalankan migrasi database
   ```bash
   php artisan migrate
   ```

6. Build asset frontend
   ```bash
   npm run build
   ```

7. Jalankan server lokal
   ```bash
   php artisan serve
   ```

## 📊 Ringkasan Analisis

- **Total produk dikelola:** 115 SKU
- **Periode data forecasting:** November 2025 – April 2026
- **Klasifikasi ABC:** 47 produk Kategori A, 38 produk Kategori B, 30 produk Kategori C

## 👤 Pengembang

Dikembangkan oleh **[Nama Kamu]** sebagai proyek Tugas Akhir, Program Studi Manajemen Informatika, Politeknik Negeri Sriwijaya.

## 📄 Lisensi

Proyek ini dibuat untuk keperluan akademik (Tugas Akhir) dan studi kasus pada PT. Ridho Agro Jaya.
