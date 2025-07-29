# 🧭 Panduan Identifikasi Insiden

Halaman ini berisi langkah-langkah sistematis untuk membantu tim IPM, developer, dan SME dalam mengidentifikasi dan menelusuri insiden yang terjadi pada aplikasi MCS.

---

## 🎯 Tujuan

Membantu tim melakukan investigasi awal terhadap insiden yang dilaporkan oleh pengguna, monitoring, atau alert system, sehingga penanganan bisa dilakukan dengan cepat dan tepat.

---

## 🛠️ Langkah Identifikasi Awal

### 1. Kumpulkan Informasi Awal
- Waktu kejadian insiden
- Nama pengguna yang terdampak
- Modul atau fungsi aplikasi yang bermasalah
- Pesan error atau screenshot (jika ada)
- Log aktivitas terakhir sebelum kejadian

### 2. Cek Monitoring & Log
- Buka dashboard monitoring (Grafana, Prometheus, atau lainnya)
- Cek log dari service terkait (gunakan `journalctl`, `docker logs`, atau ELK stack)

    ```bash
    journalctl -u nama_service --since "30 minutes ago"
    ```

- Perhatikan error yang muncul di backend/API atau database

### 3. Validasi dari UI / UX
- Replikasi langkah pengguna jika memungkinkan
- Cek apakah error muncul konsisten
- Bandingkan antara user yang terdampak dan user yang normal

### 4. Konfirmasi Status Dependency
- Apakah ada service lain yang sedang down?
- Cek status koneksi ke database, API eksternal, atau autentikasi

---

## 🔍 Alat Bantu Identifikasi

| Tools         | Fungsi                                               |
|---------------|------------------------------------------------------|
| Grafana       | Monitoring performa aplikasi & resource              |
| ELK Stack     | Log centralization & search (Elasticsearch + Kibana)|
| Postman       | Testing endpoint API secara manual                   |
| ping/curl     | Cek koneksi antar komponen                           |

---

## ✅ Checklist Sebelum Eskalasi

- [ ] Informasi awal lengkap
- [ ] Log error ditemukan
- [ ] Replikasi berhasil dilakukan
- [ ] Status dependency sudah dicek
- [ ] Estimasi dampak disiapkan

---

## 👥 PIC Penanganan Insiden

| Role   | Nama            | Kontak         |
|--------|------------------|----------------|
| IPM    | Dini Kurniawati  | 0813-1074-3741 |
| DevOps | Ahmad R.         | 0812-xxxx-xxxx |
| SME    | Raka S.          | 0812-xxxx-xxxx |

---

## 📚 Referensi Terkait

- [SOP Penanganan Insiden](sop/incident_response.md)
- [Kumpulan Insiden Sebelumnya](usage/overview.md)
