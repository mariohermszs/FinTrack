# 💰 FinTrack

**FinTrack** adalah aplikasi web inovatif yang berfungsi sebagai platform pencatatan keuangan personal (*personal finance tracker* & *financial diary*). Website ini dirancang untuk membantu pengguna melacak arus kas harian serta membangun target finansial dengan tampilan yang modern dan interaktif.

🔗 **Live Demo:** [fin-track-five-rho.vercel.app](https://fin-track-five-rho.vercel.app)
📦 **Repository:** [github.com/mariohermszs/FinTrack](https://github.com/mariohermszs/FinTrack)

---

## 📖 Deskripsi

Berbeda dengan aplikasi pencatatan keuangan konvensional yang rumit, FinTrack mengadopsi standar akuntansi formal nasional berupa **Sistem Laporan Arus Kas Metode Langsung (Direct Method Cash Flow Statement)** yang disederhanakan secara otomatis oleh sistem di balik layar.

Transaksi dikelompokkan secara terstruktur ke dalam dua pilar utama keuangan:
- **Cash Inflows** (Arus Kas Masuk / Pendapatan)
- **Cash Outflows** (Arus Kas Keluar / Pengeluaran)

---

## 🛠️ Tech Stack

- **HTML5**
- **Tailwind CSS**
- **Chart.js**

---

## ✨ Fitur Utama

### 1. Input Nominal Transaksi dengan Auto-Comma
Sistem otomatisasi UI akan memisahkan angka ribuan dengan koma secara langsung saat pengguna mengetik nominal (misalnya `5000000` akan terformat otomatis menjadi `5,000,000`). Fitur ini berfungsi untuk meminimalkan human error.

### 2. Timestamp Otomatis
Untuk memenuhi standar akuntansi audit, setiap mutasi kas keuangan yang disimpan akan direkam secara otomatis oleh JavaScript, mencatat waktu penginputan data secara presisi (tanggal, bulan, tahun, jam, menit, dan detik).

### 3. Analisis Keuangan Berdasarkan Kategori
FinTrack menampilkan infografis dalam bentuk diagram bulat (*Doughnut Chart*) menggunakan library Chart.js. Pengguna dapat mengklik salah satu irisan kategori pengeluaran/pemasukan pada grafik untuk langsung melihat data tabel riwayat transaksi pada kategori tersebut.

### 4. Financial Health Alert
FinTrack memiliki algoritma khusus yang akan otomatis mendeteksi rasio kesehatan finansial. Jika total pengeluaran (*Cash Outflows*) telah menembus batas kritis (80%) dari total pemasukan (*Cash Inflows*), sistem akan memunculkan *Alert Card* berwarna merah di halaman depan.

### 5. Export Data Ledger dalam Format CSV
FinTrack menyediakan fungsionalitas ekspor data yang dapat mengubah seluruh basis data lokal menjadi file *spreadsheet* dengan format `.csv`, sehingga memudahkan pengguna ketika mengolah data pada software seperti Microsoft Excel.

### 6. Persistent Local Memory
FinTrack menggunakan memori browser `localStorage` dalam pengoperasiannya, sehingga seluruh data pembukuan kas harian dan progress target tabungan tersimpan secara permanen dan tidak hilang ketika halaman web direfresh.

---

## 🎯 Target Pengguna

### 1. Mahasiswa dan Pelajar
FinTrack dapat membantu mahasiswa dan pelajar dalam mengelola uang saku bulanan atau pendapatan dari magang. Kelompok ini membutuhkan platform yang simpel dan mudah digunakan tanpa harus memahami teori akuntansi pembukuan yang membingungkan.

### 2. Freelancer dan Pelaku Usaha Mikro
FinTrack dapat membantu para pelaku usaha dalam mencatat pendapatan dari berbagai proyek (seperti bisnis rumahan ataupun jasa freelance). Fitur kategori dan ekspor CSV dapat membantu mereka dalam mengevaluasi kas masuk dan keluar setiap bulannya.

### 3. Personal Budgeter (Masyarakat Umum)
FinTrack juga dapat membantu pengguna yang ingin disiplin menabung demi mencapai target tertentu (misalnya menabung untuk membeli gadget baru, dana kesehatan, dana darurat, hingga persiapan studi) serta pengguna yang ingin mengetahui pos-pos pengeluaran mereka setiap bulannya.

---

## 🎨 Desain UI/UX

Desain antarmuka FinTrack disusun dengan memperhatikan prinsip-prinsip dasar UI/UX, yaitu:

### 1. Gaya Visual & Estetika (Liquid Glassmorphism)
Tampilan website ini mengadopsi gaya **Apple Liquid Glass UI**. Latar belakangnya menggunakan warna biru tua yang identik dengan tema perbankan, ditambah efek *Aurora Ambient Backdrop* berupa cahaya lembut yang bergerak perlahan di belakang konten. Komponen form dan tabel dibuat transparan dengan efek blur (*glassmorphism*) serta garis tepi putih tipis, menghasilkan tampilan yang bersih, modern, dan terasa premium seperti antarmuka khas Apple.

### 2. Konsistensi Desain
Konsistensi visual dijaga dengan menerapkan bentuk kelengkungan sudut yang seragam pada seluruh komponen di setiap halaman (`rounded-[2rem]`). Font yang digunakan juga konsisten, yaitu **Inter**, dan palet warna diterapkan sesuai fungsinya: biru untuk navigasi utama, hijau emerald untuk kas masuk, dan merah rose untuk kas keluar.

### 3. Navigasi yang Jelas
Navigasi pada website ini menggunakan sistem **Single Page Application (SPA)** melalui sidebar di sebelah kiri. Dengan sistem ini, pengguna dapat berpindah antar-halaman (Dashboard, Financial Diary, Financial Targets) secara instan tanpa perlu memuat ulang halaman. Menu yang sedang aktif juga akan otomatis berubah warna untuk menandai posisi navigasi pengguna saat itu.

### 4. Tata Letak & Hirarki Visual
Tata letak disusun secara *top-down* dengan susunan yang seimbang dan simetris. Form input dibuat *full-width* agar selebar tabel di bawahnya, sehingga informasi penting seperti tanggal, deskripsi, dan nominal transaksi dapat ditampilkan secara rapi dan tidak terpotong.

### 5. Affordance & Feedback Visual
Setiap tombol interaktif diberikan efek *hover*, yaitu sedikit membesar saat didekati kursor, sebagai penanda bahwa elemen tersebut dapat diklik. Selain itu, sistem juga dilengkapi dengan *toast notification* di pojok kanan bawah yang akan muncul secara otomatis sebagai bentuk feedback setiap kali pengguna berhasil menambah atau menghapus data.

### 6. Responsivitas Layar
Tampilan website ini dapat menyesuaikan ukuran layar secara otomatis. Ketika diakses melalui laptop, komponen akan memanfaatkan ruang horizontal secara maksimal. Sementara itu, ketika diakses melalui perangkat HP, tata letak akan berubah menjadi satu kolom vertikal dengan ukuran tombol yang lebih besar agar mudah dijangkau oleh jempol pengguna.

### 7. Optimalisasi Performa
Untuk mencegah efek patah-patah akibat beban render dari efek kaca transparan, website ini memanfaatkan *hardware acceleration* melalui properti CSS `transform: translate3d` dan `will-change`. Dengan demikian, proses animasi dapat dibantu oleh GPU, sehingga perpindahan antar halaman terasa lebih ringan dan mulus.

---

## 🚀 Cara Menjalankan

1. Clone repository ini:
   ```bash
   git clone https://github.com/mariohermszs/FinTrack.git
   ```
2. Buka file `index.html` menggunakan browser, atau
3. Akses langsung melalui live demo: [fin-track-five-rho.vercel.app](https://fin-track-five-rho.vercel.app)

---

## 📄 Lisensi

Proyek ini dibuat untuk keperluan tugas kuliah.
