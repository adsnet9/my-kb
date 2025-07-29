# 📋 Kumpulan Insiden & Akar Masalah

Halaman ini berfungsi sebagai arsip insiden-insiden penting yang pernah terjadi, beserta akar masalah dan langkah penyelesaiannya.

---

## 🗓️ Insiden Terdokumentasi

| Tanggal | Ringkasan | Level | Status | RCA |
|---------|-----------|-------|--------|-----|
| 2025-07-10 | API Gateway Timeout | P1 | Selesai | Network congestion |
| 2025-06-18 | Data gagal sync ke DB | P2 | Selesai | Deadlock saat batch |
| 2025-05-30 | Error login user | P3 | Selesai | Kesalahan validasi input |

---

## 🔍 Detail Format RCA

Contoh format:

### 🆘 Insiden: API Gateway Timeout
- 📅 Tanggal: 2025-07-10
- 🧭 Level: P1
- 👤 PIC: Developer A
- 🕵️ Ringkasan:
  Sistem tidak bisa diakses selama 15 menit akibat timeout dari API Gateway.

- 🔎 Root Cause:
  Terjadi lonjakan traffic mendadak tanpa scaling otomatis.

- 🛠️ Solusi:
  - Clear antrean API Gateway
  - Implementasi auto-scaling instance

- ✅ Status: Selesai

