# Laporan Lab 01: Analisis Statis Struktur Header & IAT Sample-A.exe

## 1. Identitas Analisis
* **Analis:** Richard Jeavin Anggana
* **NIM:** 24.83.1073
* **Objek Target:** Sample-A.exe (Aplikasi PE 64-bit)

## 2. Informasi Dasar & Metadata File
Menggunakan perangkat **Detect It Easy (DIE)** dan **HxD Hex Editor**, diperoleh informasi dasar sebagai berikut:
* **Magic Header:** `MZ` (0x4D 0x5A) -> Mengonfirmasi format Portable Executable Windows.
* **File Size:** 42.5 KB
* **MD5 Hash:** `bc3a1982f6e7b7ad839ef41132aa9211`
* **Subsystem:** Windows Command Line / Console Application

## 3. Analisis Import Address Table (IAT)
Melalui pembacaan tabel fungsi impor, ditemukan beberapa pustaka dinamis (`.dll`) eksternal yang mencerminkan kapabilitas program ini:
* **`KERNEL32.dll`**: Memanggil fungsi `CreateFileW`, `WriteFile`, dan `CloseHandle`. Ini mengindikasikan program memiliki kapabilitas untuk membuat dan menulis file baru ke dalam sistem komputer.
* **`USER32.dll`**: Memanggil fungsi `MessageBoxA`. Ini mengindikasikan program dapat memicu pop-up grafis interaktif ke layar monitor pengguna.

## 4. Kesimpulan Perilaku (Hipotesis)
Berdasarkan analisis statis terhadap IAT, program `Sample-A.exe` ini diprediksi merupakan utilitas penulisan log sederhana yang akan memunculkan notifikasi grafis (`MessageBox`) setelah berhasil menuliskan suatu data ke dalam file lokal di harddisk.
