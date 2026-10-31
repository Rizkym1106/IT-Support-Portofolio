# Project 01 — Windows Installation & Configuration

## 🎯 Tujuan
Membuktikan kemampuan dan keterampilannya dalam melakukan instalasi serta konfigurasi sistem operasi Windows pada perangkat pengguna secara bersih, aman, dan siap pakai.

---

## 🖼️ Dokumentasi Visual Proyek

### 1. Mengubah Boot Priority (BIOS/UEFI)
> Mengatur urutan *booting* pada BIOS/UEFI agar sistem membaca media instalasi USB/Flashdisk terlebih dahulu.

![Mengubah Boot Priority](Mengubah%20Boot%20Priority.jpg)

### 2. Berhasil Melakukan Install Ulang
> Proses instalasi sistem operasi Windows selesai dengan sukses dan siap untuk tahap konfigurasi driver serta aplikasi dasar.

![Berhasil Melakukan Install Ulang](Berhasil%20melakukan%20install%20ulang.jpg)

---

## 📚 Materi Praktik
- **Persiapan Instalasi**: Pembuatan media instalasi (Bootable USB) dan pengaturan boot priority pada BIOS/UEFI.
- **Instalasi Ulang Windows**: Proses *clean install* sistem operasi hingga ke tampilan *desktop*.
- **Instalasi Driver**: Pemasangan driver perangkat keras (LAN, Wi-Fi, Display, Audio).
- **Instalasi Aplikasi Dasar**: Pemasangan perangkat lunak standar (Browser, Office, PDF Reader, Utility).
- **Pemeriksaan Device Manager**: Memastikan seluruh komponen perangkat keras terdeteksi tanpa kendala/ikon peringatan (*yellow exclamation*).
- **Pengujian Fungsi Perangkat**: Verifikasi jaringan, suara, layar, dan fungsi dasar setelah instalasi.

---

## 🔍 Bukti & Hasil Pengujian

### Checklist Pengujian Setelah Instalasi

| Komponen Perangkat | Item Pengujian | Hasil Pengujian | Status |
| :--- | :--- | :--- | :---: |
| **Sistem Operasi** | Aktivasi & Sistem Informasi | Windows terinstal dan terdeteksi dengan benar | ✅ PASS |
| **Jaringan** | Koneksi Wi-Fi & Ethernet | Dapat terhubung ke internet tanpa masalah | ✅ PASS |
| **Pengoperasian Layar** | Resolusi & Driver Grafis | Display menyesuaikan resolusi native monitor | ✅ PASS |
| **Audio** | Speaker & Microphone | Suara keluar dengan jernih dan mic merespons | ✅ PASS |
| **Input Devices** | Keyboard & Touchpad/Mouse | Seluruh tombol dan fungsi navigasi berjalan normal | ✅ PASS |
| **Device Manager** | Status Pengenal Hardware | Tidak ada peringatan *Unknown Device* / Driver bentrok | ✅ PASS |

---

## 📝 Catatan Tambahan
> **⚠️ Penting**: Sebelum melakukan instalasi ulang pada komputer atau laptop utama, pastikan seluruh data penting telah di-*backup* ke media penyimpanan eksternal atau *cloud storage*, serta persiapkan media instalasi dengan benar. Pada lingkungan latihan, praktik dapat dilakukan di dalam mesin virtual (VMware/VirtualBox) atau perangkat uji coba.
