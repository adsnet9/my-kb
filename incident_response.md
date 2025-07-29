# 🛠️ SOP Penanganan Insiden Aplikasi MCS

Dokumen ini berisi panduan langkah demi langkah dalam menangani insiden yang terjadi pada sistem aplikasi MCS.

---

## 🚨 1. Deteksi Insiden

- Sumber notifikasi: monitoring, pengguna, ticketing
- Cek log error / alert dashboard
- Verifikasi dampak dan scope

---

## 🧭 2. Klasifikasi & Prioritas

| Level | Deskripsi | Contoh |
|-------|-----------|--------|
| P1 | Sistem total down, layanan tidak bisa digunakan | Semua transaksi gagal |
| P2 | Fitur penting terganggu tapi sistem masih berjalan | Delay respon API |
| P3 | Bug minor, tidak mengganggu proses utama | Salah label UI |

---

## 👥 3. Koordinasi Tim

- Notifikasi via grup insiden
- Catat PIC yang menangani
- Update status secara berkala

---

## 🔧 4. Penanganan Teknis

- Langkah mitigasi sementara
- Rollback jika diperlukan
- Patching / fix final

---

## 📝 5. Dokumentasi Insiden

- Kronologi
- Tindakan yang diambil
- Root Cause Analysis (RCA)
- Link ke log, screenshot, atau hasil investigasi

---

## ✅ 6. Evaluasi & Post-Mortem

- Laporan insiden ditinjau ulang
- Update ke SOP jika dibutuhkan
