# Laporan Lab 02: Analisis String & Deteksi Karakteristik Sample-B.exe

## 1. Identitas Analisis
* **Analis:** Richard Jeavin Anggana
* **NIM:** 24.83.1073
* **Objek Target:** Sample-B.exe

## 2. Metodologi Analisis
Analisis statis dasar ini berfokus pada teknik **Strings Extraction** menggunakan utilitas CLI *Strings* dari Sysinternals guna melihat teks polos yang berada di dalam section berkas biner tanpa menjalankannya secara langsung.

## 3. Temuan Teks / String Penting
Berikut adalah daftar string mencurigakan dan bernilai penting yang berhasil diekstraksi dari ruang memori file:
* `http://malicious-domain-amikom.local/login.php` -> Sebuah URL domain eksternal. Ini mengindikasikan adanya fungsi komunikasi jaringan.
* `C:\Users\Developer\Documents\SecretProject\Release\target.pdb` -> Path direktori kompilasi lokal milik developer asli program.
* `SOFTWARE\Microsoft\Windows\CurrentVersion\Run` -> Alamat registri Windows yang biasa digunakan malware untuk mengaktifkan fitur *Persistence* (berjalan otomatis setiap kali PC dihidupkan).

## 4. Rekomendasi Keamanan
Karena ditemukan indikasi modifikasi registri startup dan alamat URL luar, sampel ini disarankan untuk diisolasi dalam jaringan virtual sandbox internal dan dilanjutkan ke tahap analisis dinamis menggunakan debugger demi keamanan.
