# Static Analysis Laboratory Reports

Repositori ini berisi kumpulan laporan laboratorium mengenai analisis statis (*static analysis*) terhadap berbagai file binary berformat Portable Executable (PE). Analisis statis dilakukan dengan memeriksa karakteristik file, informasi *header*, tabel fungsi yang diimpor (*Import Address Table*), serta *strings* yang tertanam tanpa mengeksekusi program tersebut.

## Identitas Mahasiswa
* **Nama:** Richard Jeavin Anggana
* **NIM:** 24.83.1073

## Daftar Laporan Analisis Statis
Minimal menganalisis 2 binary PE disertai dengan laporan singkat:
* **[Laporan 01] Analisis Statis Struktur Header & IAT Sample-A.exe**
  * Memeriksa arsitektur target (32-bit/64-bit), stempel waktu kompilasi, serta fungsi sensitif dari `KERNEL32.dll` dan `USER32.dll`.
  * **Status:** Selesai ([Lihat Dokumen](laporan-analisis-01.md))
* **[Laporan 02] Analisis String & Deteksi Karakteristik Sample-B.exe**
  * Melakukan ekstraksi string tersembunyi untuk mengidentifikasi indikasi alamat IP, domain, atau pesan eror tertentu.
  * **Status:** Selesai ([Lihat Dokumen](laporan-analisis-02.md))

## Kebijakan Keamanan Lab
1. **Lingkungan Terisolasi:** Semua file sampel binary dianalisis menggunakan Virtual Machine (VM) yang terisolasi dari jaringan utama demi keamanan sistem host.
2. **Larangan Malware Aktif:** **TIDAK ADA** file malware aktif atau kode berbahaya berbahaya yang diunggah ke repositori publik ini. Repositori ini hanya memuat teks dokumentasi berupa laporan (`.md`).

---
*Disusun sebagai bukti proses belajar dan praktikum mandiri Reverse Engineering.*

<<<<<<< HEAD

=======
* [Log Commit Tambahan 05] Perbaikan format teks dan tipografi laporan laboratorium.
* [Log Commit Tambahan 06] Sinkronisasi metadata hash MD5 berkas biner sampel A.
* [Log Commit Tambahan 07] Perapian susunan daftar string yang diekstraksi dari sampel B.
* [Log Commit Tambahan 08] Pembaruan klausul keamanan dan etika laboratorium virtual.
* [Log Commit Tambahan 09] Penyesuaian tata letak tabel fungsi impor Windows API.
* [Log Commit Tambahan 10] Finalisasi dokumen portofolio praktikum analisis statis dasar.

>>>>>>> 207f6e52849292010f456d66d03ceb6368725e5f

