# 📋 Dokumentasi Aplikasi Penghitung Mundur & Detik Tersisa

## 🎯 Fungsi Aplikasi

Aplikasi ini adalah **alat penghitung mundur dua kolom** yang berfungsi untuk:

1. **Menentukan waktu target** (tanggal dan jam spesifik) yang ingin dicapai
2. **Menampilkan hitung mundur** lengkap dalam format hari, jam, menit, dan detik di kolom kiri
3. **Menampilkan detik tersisa** secara real-time di kolom kanan (dalam angka besar yang mudah dibaca)
4. **Memberikan visualisasi** status apakah waktu target sudah diatur, aktif, atau sudah terlewati
5. **Memungkinkan pengaturan ulang** waktu target kapan saja untuk memulai hitung mundur baru

Aplikasi ini cocok untuk:
- Menghitung mundur menuju acara penting (ulang tahun, pernikahan, peluncuran produk)
- Timer deadline proyek
- Penghitung waktu menuju akhir promo/diskon
- Alat bantu manajemen waktu

---

## 🛠️ Teknologi yang Digunakan

| Teknologi | Versi | Fungsi |
|-----------|-------|--------|
| **HTML5** | - | Struktur halaman, elemen form, dan tata letak semantik |
| **CSS3** | - | Styling responsif, efek glassmorphism, animasi hover, layout flexbox, media queries untuk mobile |
| **JavaScript (ES6+)** | - | Logika penghitung mundur, manipulasi DOM real-time, event handling, interval timer |
| **Google Fonts (system-ui)** | - | Tipografi modern dan bersih |
| **Local Browser API** | `datetime-local` | Input tanggal dan waktu native browser |
| **JavaScript Date API** | `Date()` | Parsing waktu, perhitungan selisih, format lokal Indonesia |

### Fitur Teknis Unggulan:
- ✅ **Real-time update setiap 1 detik** menggunakan `setInterval`
- ✅ **Deteksi zona waktu lokal** pengguna secara otomatis
- ✅ **Responsive design** - bekerja optimal di desktop, tablet, dan smartphone
- ✅ **Validasi input** - menolak format waktu tidak valid
- ✅ **Auto-cleanup interval** saat halaman ditutup atau target diubah

---

## 📖 Cara Menggunakan

### Langkah 1: Buka Halaman
- Simpan kode HTML sebagai file dengan ekstensi `.html` (contoh: `countdown.html`)
- Buka menggunakan browser modern (Chrome, Firefox, Edge, Safari)

### Langkah 2: Atur Waktu Target
1. **Di kolom kiri**, cari kotak bertuliskan "Pilih Waktu Target"
2. Klik pada **input datetime-local** (format: `YYYY-MM-DD HH:MM`)
3. Pilih **tanggal** dan **jam** yang diinginkan (misal: 2026-12-31 23:59)
4. Klik tombol **🚀 SET & MULAI HITUNG MUNDUR**

### Langkah 3: Lihat Hasil Perhitungan

**Kolom Kiri (Hitung Mundur Lengkap):**
- Menampilkan sisa waktu dalam format: `Hari : Jam : Menit : Detik`
- Contoh: `02 : 14 : 35 : 22` (berarti 2 hari, 14 jam, 35 menit, 22 detik lagi)

**Kolom Kanan (Detik Tersisa):**
- Menampilkan **total detik** dalam angka besar
- Contoh: `187.522` detik
- Dilengkapi keterangan real-time status

### Langkah 4: Mengganti Waktu Target
- Ulangi **Langkah 2** - cukup pilih waktu baru dan klik tombol SET
- Penghitung mundur akan **otomatis reset** dan mulai menghitung ke waktu baru

### Contoh Skenario Penggunaan:

| Tujuan | Cara Setting |
|--------|---------------|
| Menghitung mundur 30 menit dari sekarang | Pilih waktu sekarang + 30 menit di datetime picker |
| Menghitung mundur ke hari raya | Pilih tanggal 1 Syawal (misal) pukul 00:00 |
| Deadline tugas besok jam 08:00 | Pilih besok pukul 08:00 di kalender |

### Tips Penting:
- ⏰ **Waktu menggunakan zona lokal komputer Anda** (WIB/WITA/WIT otomatis)
- 🔄 **Halaman akan terus berjalan** meskipun target sudah lewat (menampilkan 0)
- 🎯 **Status badge** akan berubah warna:
  - 🟢 Hijau = Aktif menghitung mundur
  - 🟠 Oranye = Waktu sudah lewat / peringatan
  - ⚪ Abu-abu = Belum ada target

---

## ⚙️ Fitur Khusus

### 1. **Mode Demo Otomatis**
Saat pertama kali dibuka, aplikasi akan otomatis mengatur waktu target **10 menit dari sekarang** sebagai contoh, sehingga Anda langsung bisa melihat cara kerjanya.

### 2. **Validasi Cerdas**
- Jika memilih waktu yang sudah lewat, akan muncul peringatan
- Jika input kosong saat klik SET, akan muncul notifikasi
- Format tanggal otomatis disesuaikan dengan bahasa Indonesia

### 3. **Responsif Mobile**
Di layar sempit (<780px), kedua kolom akan ditumpuk vertikal agar mudah dibaca di HP.

---

## 🐛 Troubleshooting

| Masalah | Solusi |
|---------|--------|
| Angka tidak berubah | Refresh halaman, pastikan JavaScript diaktifkan |
| Waktu tidak sesuai | Cek zona waktu komputer Anda sudah benar |
| Tombol SET tidak bereaksi | Pastikan memilih tanggal & jam terlebih dahulu |
| Tampilan berantakan | Gunakan browser modern (Chrome/Firefox/Edge terbaru) |

---

## 📝 Catatan Teknis

- **Akurasi**: Setiap detik timer melakukan sinkronisasi dengan waktu sistem, sehingga akurat dengan jam komputer Anda.
- **Performa**: Menggunakan satu `setInterval` global untuk efisiensi, dibersihkan otomatis saat target diubah.
- **Kompatibilitas**: Mendukung semua browser yang mengimplementasikan `datetime-local` input (Chrome 20+, Firefox 57+, Edge 12+, Safari 14.1+)

---

**Selamat mencoba!** 🎉 Jika ada pertanyaan, cukup setel ulang waktu target kapan saja untuk memulai hitungan baru.
