# DB-Integrity-Validation Suite

Repositori ini berisi infrastruktur pengujian otomatis untuk memvalidasi integritas dan keamanan aset database yang terenkripsi. Sistem ini memanfaatkan GitHub Actions untuk melakukan dekripsi sementara dan menjalankan prosedur validasi dalam lingkungan runtime yang terisolasi.

---

## Deskripsi Operasional
Sistem ini dirancang untuk memastikan aset database tetap aman selama siklus pengembangan. Dengan memisahkan kunci enkripsi ke dalam GitHub Secrets dan menggunakan mesin validasi dinamis, risiko kebocoran data sensitif dalam repositori publik dapat diminimalisir.

## Fitur Teknis
* **Dynamic Validation Engine**: Mengunduh modul validasi inti secara runtime untuk mencegah penyimpanan logika sensitif dalam repositori.
* **Secret-Key Integration**: Memanfaatkan enkripsi tingkat industri dengan kunci yang dikelola melalui GitHub Secrets (AES-256).

## Persiapan Konfigurasi

Untuk mengaktifkan suite validasi ini, langkah-langkah berikut harus dipenuhi:

1. **GitHub Secrets Configuration**:
    * Navigasi ke **Settings** > **Secrets and variables** > **Actions**.
    * Masukkan Secret baru dengan nama `API_KEY`. Secret ini berfungsi sebagai kunci dekripsi utama untuk aset database.

2. **Asset Deployment**:
    * Pastikan file `namafile.dexenc` (aset terenkripsi) tersedia di direktori root repositori ini.

## Struktur Kerja (Workflow)
Proses meliputi:
1. Inisialisasi lingkungan Python 3.12 pada Windows Runner.
2. Pengunduhan validator internal (`internal_validator.py`).
3. Dekripsi aset database menjadi file sementara `db_schema_update.ps1`.
4. Eksekusi prosedur validasi internal melalui PowerShell.

---
**Status Proyek:** Aktif - Internal Security Testing Only
