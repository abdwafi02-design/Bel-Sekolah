# 🔔 Bel Sekolah Otomatis Modern (4 Bahasa & Multi-Platform)

Aplikasi **Bel Sekolah Otomatis Offline-First** berbasis web (PWA) yang dirancang khusus untuk operasional sekolah di Chromebook Zyrex, PC Windows, Linux, Android, dan macOS. Dilengkapi pengumuman narasi multi-bahasa otomatis (Indonesia, Inggris, Arab, Mandarin), lonceng digital High Definition V2, timeline visual D3, dan integrasi Google Drive.

---

## 🌟 Fitur Utama

1. **Pengumuman Suara Otomatis 4 Bahasa**:
   - 🇮🇩 **Bahasa Indonesia**: Narasi jernih dan santun.
   - 🇬🇧 **Bahasa Inggris**: Aksen standar internasional.
   - 🇸🇦 **Bahasa Arab**: Dilengkapi mesin fonetik cerdas otomatis (tajwid presisi) sehingga tetap bersuara lancar di Chromebook Zyrex / PC yang tidak memiliki paket bahasa Arab native.
   - 🇨🇳 **Bahasa Mandarin**: Pengucapan pinyin standar.
2. **Koleksi Suara Bel Versi Baru (V2.0)**:
   - Melodi lonceng sekolah modern Asia (*Kin-Kon-Kan-Kon* glockenspiel)
   - Lonceng Carillon Tabung Katedral (*Tubular Bells*)
   - Jingle Celesta Arpeggio Ceria
   - Sentuhan Etnik Gamelan Perunggu Nusantara
   - Jingle Siaran Pengumuman Bandara / Stasiun
   - Westminster Chimes klasik dentang ganda
3. **Timeline Visual Interaktif (D3.js)**:
   - Memantau status seluruh bel harian (Selesai, Sedang Berlangsung, Menunggu, Dilewati).
4. **Google Drive Cloud Sync**:
   - Cadangkan seluruh jadwal dan pengaturan ke Google Drive pribadi.
   - Impor rekaman bel kustom (.mp3, .wav) langsung dari Google Drive.
5. **Keamanan Sandi & Mode Kiosk**:
   - Kunci menu dengan PIN Operator untuk mencegah perubahan tidak disengaja.
   - **Privasi Terjamin**: Sandi tidak pernah tersimpan di repositori GitHub publik.
6. **Offline-First & Screen Wake Lock**:
   - Berjalan 100% tanpa internet setelah dimuat.
   - Layar tidak akan mati/tidur otomatis (*Screen Wake Lock*).

---

## 🔒 Keamanan Sandi & Privasi Akun

> **PENTING: Sandi Anda Aman & Dirahasiakan!**
> 
> Saat repositori ini dipublikasikan ke GitHub (baik publik maupun privat), **sandi atau PIN Anda TIDAK AKAN PERNAH terunggah ke GitHub**.

### Bagaimana Sistem Melindungi Kerahasiaan Anda?
1. **Penyimpanan Lokal (Zero-Knowledge Repo)**:
   - Sandi/PIN yang Anda ubah disimpan secara eksklusif di penyimpanan browser lokal komputer Anda (`localStorage`).
   - Kode sumber di GitHub hanya berisi nilai awal bawaan pabrik (`1234`).
2. **Filter Berkas Sensitif (`.gitignore`)**:
   - Berkas cadangan (`*.backup.json`), kunci rahasia, dan variabel lingkungan (`.env*`) telah otomatis diabaikan oleh Git sehingga tidak akan terunggah.
3. **Kontrol Hak Akses**:
   - Anda bebas memilih repositori GitHub dalam mode **Private** (hanya Anda yang dapat melihat kode) atau **Public**.

---

## 🚀 Panduan Publish ke GitHub

Ikuti langkah-langkah di bawah ini untuk mengunggah proyek ini ke akun GitHub Anda:

### 1. Buat Repositori Baru di GitHub
1. Masuk ke akun GitHub Anda di [https://github.com](https://github.com).
2. Klik tombol **"+"** di pojok kanan atas, lalu pilih **New repository**.
3. Beri nama repositori, misalnya: `bel-sekolah-otomatis`.
4. Pilih opsi:
   - **Private** (Direkomendasikan jika ingin kode hanya dapat diakses oleh Anda/pihak sekolah), atau
   - **Public** (Jika ingin dibagikan secara terbuka; ingat bahwa data jadwal dan sandi lokal Anda tetap aman).
5. Jangan centang *Initialize this repository with a README* (karena berkas README sudah ada di proyek ini).
6. Klik **Create repository**.

### 2. Unggah Kode dari Komputer / Terminal
Buka terminal pada folder proyek ini, lalu jalankan perintah berikut:

```bash
# Inisialisasi Git lokal (jika belum)
git init

# Tambahkan seluruh berkas proyek ke staging area
git add .

# Buat commit pertama
git commit -m "Rilis Awal Sistem Bel Sekolah Otomatis 4 Bahasa"

# Ubah nama branch utama menjadi main
git branch -M main

# Hubungkan dengan repositori GitHub Anda (ganti USERNAME dengan akun GitHub Anda)
git remote add origin https://github.com/USERNAME/bel-sekolah-otomatis.git

# Unggah berkas ke GitHub
git push -u origin main
```

---

## 🌐 Panduan Deploy Online Gratis

Setelah kode berada di GitHub, Anda dapat meng-hosting aplikasi ini secara gratis agar bisa dibuka dari peramban (browser) di perangkat sekolah mana pun:

### Opsi A: Deploy dengan Vercel (Paling Mudah & Cepat - 1 Menit)
1. Kunjungi [https://vercel.com](https://vercel.com) dan masuk dengan akun GitHub Anda.
2. Klik **Add New** > **Project**.
3. Pilih repositori `bel-sekolah-otomatis` dari daftar GitHub Anda.
4. Framework Preset akan otomatis terdeteksi sebagai **Vite**.
5. Klik tombol **Deploy**.
6. Selesai! Anda akan mendapatkan URL HTTPS publik gratis (contoh: `https://bel-sekolah-otomatis.vercel.app`).

### Opsi B: Deploy dengan GitHub Pages
1. Pastikan script build di `vite.config.ts` menggunakan base path yang sesuai (`base: './'`).
2. Jalankan:
   ```bash
   npm run build
   ```
3. Buka tab **Settings** di repositori GitHub Anda > menu **Pages**.
4. Di bagian **Build and deployment**, pilih sumber **GitHub Actions** atau deploy cabang `dist`/`gh-pages`.

---

## 💻 Cara Menjalankan di Komputer Lokal

```bash
# 1. Pasang dependensi
npm install

# 2. Jalankan server pengembangan
npm run dev

# 3. Buka di peramban
# http://localhost:3000
```

---

## 🛠️ Konfigurasi PIN Operator

- **Default PIN Bawaan**: `1234`
- **Cara Mengubah**:
  1. Masuk ke menu **Pengaturan** (ikon gear di navigasi atas).
  2. Gulir ke bagian **Keamanan & Proteksi PIN Admin**.
  3. Aktifkan **Proteksi Menu dengan PIN**.
  4. Masukkan 4-6 digit angka baru pilihan Anda.
  5. Klik tombol **Simpan Pengaturan**.
  6. PIN baru Anda tersimpan aman di browser perangkat tersebut!

---

## 📄 Lisensi
Didistribusikan di bawah lisensi Apache-2.0. Bebas digunakan dan disesuaikan untuk satuan pendidikan di seluruh Indonesia.
