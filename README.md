# FinTrack - Advanced Cash Flow & Dynamic Target Hub

FinTrack adalah aplikasi web pencatatan keuangan personal (*personal finance tracker*) modern yang dirancang secara individual untuk memenuhi Tugas Akhir mata kuliah **Desain Antar Muka Pengguna (Semester Genap 2025/2026)**. 

Aplikasi ini berhasil mengintegrasikan prinsip akuntansi formal (Laporan Arus Kas Metode Langsung / *Direct Method Cash Flow Statement*) ke dalam sebuah antarmuka intuitif beraliran **Apple Liquid Glass UI (Glassmorphism)** yang sangat *user-friendly* bagi masyarakat awam.

## Tautan Aplikasi & Repositori
* **Live Website Deployment:** https://fin-track-five-rho.vercel.app
* **GitHub Repository URL:** https://github.com/mariohermszs/FinTrack/

---

## Target Pengguna (Target User)
* **Mahasiswa & Pelajar:** Membantu mengelola uang saku atau pendapatan magang secara mandiri tanpa harus pusing memahami istilah Debit/Kredit akuntansi konvensional.
* **Pekerja Lepas (*Freelancer*) & Pelaku Usaha Mikro:** Menyediakan jurnal mutasi kas yang rapi untuk memisahkan dana operasional dan alokasi tabungan masa depan.
* **Masyarakat Awam:** Siapa saja yang membutuhkan platform pembukuan harian yang estetik, cepat, aman, dan bisa diakses kapan saja melalui *smartphone* maupun laptop.

---

## Fitur Utama & Keunggulan Sistem (Fungsionalitas Tinggi)
1. **Automated Accounting Standards (Jurnal Kas Mutasi):** Mengadopsi standar formal akuntansi pembukuan arus kas pendek. Mengotomatisasi pencatatan kas masuk (*Cash Inflows*) dan kas keluar (*Cash Outflows*) secara kronologis.
2. **Real-time Input Masking (Auto-Comma):** UI cerdas yang otomatis memisahkan angka ribuan dengan koma secara langsung saat pengguna mengetik nominal (misal: mengetik `1000000` langsung terformat menjadi `1,000,000`), meminimalkan kesalahan input data (*human error*).
3. **High-Precision Audit Trail (Auto-Timestamp):** Setiap riwayat transaksi dilengkapi dengan rekaman waktu otomatis yang presisi hingga satuan detik (`Tanggal, Bulan, Tahun, hh:mm:ss`) demi validitas jejak audit pembukuan keuangan.
4. **Drill-Down Charts Analytics:** Dilengkapi dengan sepasang grafik diagram bulat interaktif (*Doughnut Chart*) dari Chart.js. Pengguna dapat mengklik salah satu irisan kategori grafik untuk langsung dialihkan dan melakukan penyaringan (*auto-filter*) data secara otomatis di tabel riwayat.
5. **Smart Budget Outflow Guardrail (Sistem Alert Cerdas):** Algoritma sistem akan memicu munculnya banner peringatan (*Budget Danger Zone Alert*) secara dinamis jika rasio pengeluaran pengguna telah menembus batas aman 80% dari total pemasukan.
6. **Data Ledger Export (.CSV File):** Pengguna dapat mengekspor seluruh basis data pembukuan kas kronologis ke dalam format spreadsheet file `.csv` hanya dengan satu kali klik untuk keperluan pelaporan eksternal.
7. **Persistent Client-Side Storage:** Seluruh data transaksi dan target kustom disimpan secara aman di dalam `localStorage` browser pengguna, sehingga data tidak akan hilang saat halaman web dimuat ulang (*refresh*).

---

## Penerapan Prinsip UI/UX & Estetika (Evaluasi Rubrik)

### 1. Konsistensi Desain (*Design Consistency*)
Menggunakan skema warna korporat perbankan modern yang solid (kombinasi Deep BCA Blue, Emerald Green untuk Inflow, dan Rose Red untuk Outflow). Desain komponen di seluruh halaman menerapkan asas simetri visual yang konsisten menggunakan sudut melengkung halus (*rounded corners* 32px) khas Apple.

### 2. Navigasi yang Jelas (*Clear Navigation*)
Menerapkan arsitektur *Single Page Application* (SPA) dengan bantuan menu *sidebar navigasi* interaktif di sisi kiri. Pengguna dapat berpindah halaman (*Dashboard*, *Financial Diary*, *Financial Targets*) secara instan dengan efek transisi yang mulus tanpa perlu memuat ulang seluruh halaman web (*zero reload*).

### 3. Tata Letak Rapi & Hirarki Visual (*Visual Hierarchy & Layout*)
Penyajian informasi diatur dengan struktur atas-bawah (*top-down symmetric grid*) yang lapang untuk mencegah kepadatan visual (*clutter-free*). Penggunaan ukuran tipografi font *Inter* yang proporsional memandu mata pengguna untuk langsung membaca informasi terpenting terlebih dahulu (seperti nominal metrik arus kas).

### 4. Komponen Affordance & Feedback
Setiap tombol interaktif dilengkapi dengan efek transisi mikro hover yang responsif. Ditambah dengan sistem *Toast Notification* di pojok kanan bawah yang muncul secara instan untuk memberikan umpan balik (*feedback*) visual yang jelas setiap kali pengguna berhasil menambah atau menghapus data pembukuan.

### 5. Responsivitas Penuh (*Mobile-Friendly Design*)
Aplikasi web ini 100% responsif berkat optimasi grid fleksibel dari Tailwind CSS. Saat diakses via desktop, elemen akan tersusun secara horizontal yang megah, dan otomatis bertransformasi menjadi 1 kolom vertikal yang *thumb-friendly* saat dibuka melalui layar *smartphone* (HP).

---

## Struktur Folder Projek
```text
fintrack-project/
├── index.html          # File tunggal aplikasi utama (Struktur UI, Styling, & Core Logic)
├── README.md           # Berkas dokumentasi resmi repositori
└── (assets)            # Dokumen pendukung infografis dan icon aset tambahan
