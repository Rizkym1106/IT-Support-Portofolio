# Project 03 — Printer Installation & Troubleshooting

## 🎯 Tujuan
Mengkonfigurasi, menginstal driver, dan menangani masalah operasional pencetakan (*printer troubleshooting*) agar perangkat printer siap digunakan dalam lingkungan kerja harian.

---

## 🖼️ Dokumentasi Visual Proyek

### Penginstalan Driver Printer
> Proses menginstal driver printer secara manual maupun melalui paket driver resmi perangkat agar printer terdeteksi secara optimal di dalam sistem operasi.

![Melakukan Penginstalan Driver Printer](Melakukan%20penginstalan%20driver%20printer.jpg)

---

## 📋 Kasus Troubleshooting
**Permasalahan**: Pengguna tidak dapat mencetak dokumen dari komputer (*Printer Not Responding / Offline*).

---

## 📚 Materi Praktik
- **Menambahkan Printer**: Menghubungkan perangkat printer via USB / Network Printer (IP Address).
- **Instalasi Driver Printer**: Pemasangan driver yang sesuai dengan tipe dan seri printer.
- **Mengatur Default Printer**: Menentukan printer utama yang otomatis terdepan saat pengguna melakukan cetak dokumen.
- **Memeriksa Antrean Cetak (*Print Queue*)**: Membersihkan atau membatalkan dokumen yang tertahan (*stuck*) pada antrean cetak.
- **Mengatasi Masalah Printer Offline**: Mereset layanan *Print Spooler* dan memeriksa koneksi kabel/jaringan printer.
- **Pengujian Cetak (*Test Print*)**: Melakukan pencetakan halaman pengujian (*Print Test Page*) untuk memastikan fungsi pencetakan normal.

---

## 🛠️ Catatan Penanganan Masalah & Solusi

### 1. Masalah Antrean Cetak Macet (*Stuck Print Queue*)
- **Penyebab**: Terdapat dokumen rusak (*corrupt*) dalam antrean yang menghalangi dokumen berikutnya.
- **Solusi**:
  1. Buka `services.msc`, cari layanan **Print Spooler**, lalu pilih **Stop**.
  2. Hapus berkas temporary cetak pada folder `C:\Windows\System32\spool\PRINTERS`.
  3. Jalankan kembali (*Start*) layanan **Print Spooler**.

### 2. Status Printer Offline
- **Penyebab**: Kabel USB longgar, masalah alamat IP pada printer jaringan, atau opsi *"Use Printer Offline"* aktif pada Windows.
- **Solusi**:
  1. Periksa sambungan kabel dan pastikan daya printer menyala.
  2. Buka menu **Devices and Printers** -> Klik kanan printer -> Pilih **See what's printing**.
  3. Buka menu **Printer** dan hilangkan centang pada opsi **Use Printer Offline**.

---

## ✅ Checklist Hasil Konfigurasi
- [x] Driver printer terpasang dengan versi terbaru dan kompatibel.
- [x] Perangkat printer diset sebagai **Default Printer**.
- [x] Antrean cetak berfungsi dengan lancar tanpa ada dokumen terhenti.
- [x] *Print Test Page* berhasil dicetak dengan hasil yang bersih dan jelas.
