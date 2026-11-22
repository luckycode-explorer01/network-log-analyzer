# network-log-analyzer
# 🛡️ Network Log Analyzer & Parser (Advanced Version)

An automated Python script designed to process, parse, and analyze network logs, perform validation and categorization, and automate reporting for cyber forensic and network administration tasks.

---

## 📌 Problem Statement
Dalam administrasi jaringan dan monitoring keamanan, pengelola sistem menangani ribuan data log setiap hari. Memilih IP valid, memisahkan trafik internal (privat) dari koneksi luar (publik), dan menemukan data rusak secara manual membutuhkan waktu lama dan rawan kesalahan. Selain itu, analis membutuhkan laporan siap pakai yang mudah dibaca oleh atasan.

## 💡 Solution & Features
Script Python otomatis ini bertugas untuk:
1. **Fleksibilitas Sumber Data:** Membaca file log asli (`.log` / `.txt`) dari server jika tersedia, atau beralih ke data simulasi (*fallback*) jika file tidak ditemukan.
2. **Validasi Otomatis:** Memvalidasi kelayakan format IPv4 dan menyaring data rusak (`try-except`).
3. **Kategorisasi IP:** Memisahkan IP Privat (Lokal) vs IP Publik sesuai standar RFC 1918.
4. **Analisis Anomali:** Menghitung frekuensi akses tiap IP untuk mengidentifikasi potensi anomali/serangan trafik berulang.
5. **Otomasi Laporan & Export:** Meng-export rekapitulasi data langsung ke file `.csv` (Excel) dan menyediakan fitur *auto-download* laporan.

---

## 🛠️ Tech Stack
* **Bahasa:** Python 3.x
* **Library Utama:** `ipaddress` (validasi IP), `csv` (export data), `os` (manajemen file sistem), `google.colab` (auto-download)
* **Environment:** Google Colab Mobile

---

## 📥 Cara Mengunduh Hasil Laporan (.csv)
Hasil rekapitulasi yang diexport (`rekap_log_jaringan.csv`) dapat diunduh dengan dua cara:
1. **Manual:** Buka panel folder 📁 di sebelah kiri Google Colab > Klik titik tiga `⋮` pada file `rekap_log_jaringan.csv` > Pilih **Download**.
2. **Otomatis:** Menggunakan modul `google.colab.files.download()` di akhir eksekusi program.
