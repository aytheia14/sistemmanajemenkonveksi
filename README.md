# 🧵 Konveksi — Sistem Manajemen Produksi

Aplikasi web berbasis **Google Apps Script** untuk mencatat dan memantau aktivitas produksi harian usaha konveksi secara digital — menggantikan pencatatan manual di kertas yang rentan hilang dan susah dilacak.

---

## 🎯 Tujuan

Membantu pengelola konveksi dalam mencatat barang masuk, hasil jahitan per penjahit, barang keluar, serta memantau produktivitas secara real-time — semua tersimpan aman di Google Spreadsheet.

---

## ⚙️ Teknologi yang Digunakan

| Komponen | Teknologi |
|---|---|
| Frontend | HTML, CSS, JavaScript |
| Backend | Google Apps Script (JavaScript) |
| Database | Google Spreadsheet |
| Hosting | Google Apps Script Web App (gratis) |

> Tidak memerlukan server khusus atau biaya hosting — cukup akun Google.

---

## 🔐 Fitur Login

Saat pertama dibuka, pengguna wajib login dengan username dan password. Sistem hanya bisa diakses oleh admin yang berwenang. Tersedia tombol **Keluar** di pojok kanan atas.

---

## 📦 Fitur Utama

### 1. Barang Masuk
Mencatat setiap bahan baku atau barang yang masuk ke gudang, lengkap dengan nama barang, jumlah, satuan, dan keterangan supplier. Riwayat bisa dilihat per hari maupun keseluruhan.

### 2. Hasil Jahitan
Mencatat output produksi dari masing-masing penjahit. Setiap entri dilengkapi **jam pengambilan** (pilihan per jam, 00:00–23:00) sehingga bisa diketahui produktivitas penjahit per sesi kerja. Ada juga ringkasan visual per penjahit dalam bentuk kartu dengan progress bar.

### 3. Barang Keluar
Mencatat barang yang dikirim atau dijual, dengan waktu otomatis dan riwayat lengkap.

### 4. Master Penjahit
Database daftar penjahit aktif beserta spesialisasi dan nomor telepon. Hanya penjahit yang terdaftar di sini yang bisa dipilih saat input hasil jahitan.

### 5. Log Aktivitas
Rekam jejak otomatis semua aksi yang dilakukan di sistem — siapa mencatat apa dan kapan. Berguna untuk audit dan kontrol. Menyimpan 100 aktivitas terakhir.

---

## 📊 Dashboard Real-time

Di bagian atas halaman terdapat **5 kartu statistik** yang terupdate otomatis setiap ada transaksi baru:

- Masuk Hari Ini
- Catatan Jahitan
- Item Dijahit
- Keluar Hari Ini
- Penjahit Aktif

---

## 💾 Penyimpanan Data

Semua data tersimpan langsung ke Google Spreadsheet dengan 5 sheet terpisah:

| Sheet | Isi |
|---|---|
| `MasterPenjahit` | Data penjahit aktif |
| `BarangMasuk` | Riwayat barang masuk |
| `HasilJahitan` | Catatan hasil jahitan per penjahit |
| `BarangKeluar` | Riwayat barang keluar |
| `LogAktivitas` | Rekam jejak semua aksi |

Data bisa dilihat, dicetak, atau diekspor ke Excel kapan saja.

---

## 🖥️ Tampilan Sistem

### Halaman Login
![Login](screenshots/login.png)
> Setiap pengguna wajib login sebelum mengakses sistem. Tampilan bersih dengan form username, password, dan tombol Masuk.

### Dashboard & Navigasi
![Dashboard](screenshots/dashboard.png)
> Sidebar kiri berisi menu navigasi. Bagian atas menampilkan 5 kartu statistik real-time aktivitas hari ini.

### Barang Masuk — Form Input
![Barang Masuk Form](screenshots/barang_masuk_form.png)
> Form pencatatan barang masuk dengan validasi otomatis. Dilengkapi field nama barang, jumlah, satuan (dropdown), dan keterangan.

### Barang Masuk — Riwayat
![Barang Masuk Riwayat](screenshots/barang_masuk_riwayat.png)
> Tabel riwayat transaksi hari ini dan semua histori. Badge hijau (+angka) menandakan jumlah barang masuk.

### Hasil Jahitan — Form Input
![Hasil Jahitan Form](screenshots/hasil_jahitan_form.png)
> Form input dengan dropdown penjahit aktif dan jam pengambilan otomatis sesuai jam saat ini.

### Hasil Jahitan — Ringkasan & Riwayat
![Hasil Jahitan Ringkasan](screenshots/hasil_jahitan_ringkasan.png)
> Ringkasan produktivitas per penjahit dalam bentuk kartu + progress bar. Tabel riwayat bisa difilter per hari atau semua data.

### Barang Keluar — Form Input
![Barang Keluar Form](screenshots/barang_keluar_form.png)
> Form pencatatan barang keluar. Waktu tercatat otomatis saat disimpan. Badge merah (-angka) untuk jumlah keluar.

### Barang Keluar — Riwayat
![Barang Keluar Riwayat](screenshots/barang_keluar_riwayat.png)
> Tabel keluar hari ini dan semua riwayat. Data ditampilkan dari terbaru ke terlama.

### Master Penjahit
![Master Penjahit](screenshots/master_penjahit.png)
> Database penjahit aktif dengan kode unik (PNJ001, dst), nama, telepon, spesialisasi, dan status Aktif.

### Log Aktivitas
![Log Aktivitas](screenshots/log_aktivitas.png)
> Rekam jejak otomatis semua aksi. Badge berwarna per kategori: Hijau = Barang Masuk, Ungu = Hasil Jahitan, Merah = Barang Keluar.

---

*Dibangun dengan Google Apps Script · Disimpan di Google Spreadsheet*
