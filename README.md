# 🛡️ DeXJS: Secure Payload Decryptor

Otomasi berbasis GitHub Actions untuk mendekripsi dan menjalankan payload PowerShell secara aman menggunakan Python. Repositori ini dirancang untuk menjaga kerahasiaan script utama Anda dengan menggunakan enkripsi AES dan GitHub Secrets.

---

## 🚀 Fitur Utama
* **Single-File Decryptor**: Mengunduh script dekripsi secara dinamis (tidak tersimpan di repo).
* **Environment Security**: Menggunakan GitHub Secrets (`API_KEY`) untuk kunci dekripsi.
* **PowerShell Optimized**: Kompatibel dengan Windows Runner di GitHub Actions.

## 🛠️ Persiapan (Prerequisites)

Sebelum menjalankan workflow, pastikan Anda telah menyiapkan hal berikut:

1.  **GitHub Secrets**: 
    * Buka tab **Settings** > **Secrets and variables** > **Actions**.
    * Tambahkan New repository secret dengan nama `API_KEY` (Berisi kunci dekripsi Anda).
2.  **Encrypted File**: 
    * Pastikan file `database_i4x.dexenc` sudah ada di root direktori repositori ini.
