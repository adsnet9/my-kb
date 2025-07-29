# ❓ FAQ – Pertanyaan Umum Aplikasi MCS

Berikut adalah daftar pertanyaan umum dan solusi yang sering ditemui oleh tim IPM, Developer, dan SME terkait aplikasi MCS.

---

### 🔧 Q: Bagaimana cara mengetahui apakah insiden berasal dari sisi backend?

**A:**
- Periksa log API atau service utama di server.
- Gunakan tools monitoring (contoh: Grafana, ELK).
- Bandingkan dengan status komponen lainnya (misal: database, network).

---

### 🔌 Q: Apa yang harus dilakukan jika user tidak bisa login?

**A:**
- Cek koneksi ke database pengguna.
- Pastikan tidak ada error pada service authentication.
- Pastikan data user tidak expired atau diblokir.

---

### 📤 Q: Bagaimana cara export log untuk investigasi?

**A:**
- Masuk ke server aplikasi.
- Jalankan perintah: `journalctl -u nama_service --since "1 hour ago" > log.txt`
- Kirim file `log.txt` ke tim yang menangani.

---

### 🧪 Q: Apakah ada environment staging/test untuk replikasi insiden?

**A:**
- Ya, environment staging tersedia di `http://staging.mcs.local`
- Data sudah disamakan dengan production (tanpa data sensitif)

---

### 📆 Q: Di mana saya bisa lihat insiden-insiden sebelumnya?

**A:**
- Buka halaman [Kumpulan Insiden](usage/overview.md)
- Di sana tersedia daftar insiden dan akar masalahnya
