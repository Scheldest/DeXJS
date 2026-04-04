# Kebijakan Keamanan (Security Policy)

Kami menganggap serius keamanan infrastruktur pengujian ini. Sebagai proyek yang berfokus pada validasi integritas database dan teknik enkripsi, kami berkomitmen untuk mengikuti standar industri dalam menangani temuan kerentanan.

## Versi yang Didukung

Hanya versi terbaru dari cabang `main` yang secara aktif menerima pembaruan keamanan dan perbaikan integrasi.

| Versi | Didukung |
| :--- | :--- |
| 1.2.x | ✅ Ya |
| 1.1.x | ❌ Tidak |
| < 1.0 | ❌ Tidak |

## Pelaporan Kerentanan

Jika Anda menemukan celah keamanan dalam mekanisme dekripsi atau alur kerja otomatisasi kami, mohon untuk tidak melaporkannya melalui *Public Issue*. Kami menghargai pengungkapan yang bertanggung jawab demi melindungi pengguna aset terenkripsi kami.

Silakan laporkan temuan Anda melalui salah satu jalur berikut:

1.  **GitHub Private Reporting**: Gunakan fitur "Report a vulnerability" pada tab Security di repositori ini.
2.  **Email Kontak**: Kirimkan detail teknis ke [Email Anda atau Email Samaran] dengan subjek: `SECURITY VULNERABILITY - DB-Integrity-Validation`.

### Informasi yang Dibutuhkan
Untuk membantu kami memvalidasi laporan Anda, mohon sertakan:
* Deskripsi mendetail tentang potensi celah.
* Langkah-langkah untuk mereproduksi (Proof of Concept).
* Dampak yang mungkin terjadi pada integritas data.

## Proses Respons

* **Konfirmasi**: Kami akan memberikan konfirmasi tanda terima laporan dalam waktu 48-72 jam kerja.
* **Investigasi**: Tim akan melakukan audit internal terhadap modul `internal_validator.py` dan konfigurasi runner.
* **Perbaikan**: Jika valid, perbaikan akan segera dirilis melalui commit resmi, dan pelapor akan diberikan atribusi jika diinginkan.

---
*Kebijakan ini terakhir diperbarui pada: 4 April 2026.*
