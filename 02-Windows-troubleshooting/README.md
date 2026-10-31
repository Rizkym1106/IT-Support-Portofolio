# Project 02 — Windows Troubleshooting

## 🎯 Tujuan
Menganalisis, mendiagnosis, dan menyelesaikan masalah konektivitas jaringan pada sistem operasi Windows menggunakan alat bantu baris perintah (*Command Line Interface*).

---

## 🖼️ Dokumentasi Visual Proyek

### Menguji Koneksi Menggunakan Command Prompt (`ping`)
> Pengujian koneksi jaringan secara langsung menggunakan perintah `ping` untuk memeriksa respons dan latensi ke *gateway* maupun alamat server luar.

![Menguji Koneksi Menggunakan Ping](Menguji%20koneksi%20menggunakan%20ping.jpg)

---

## 📋 Kasus Troubleshooting
**Permasalahan**: Komputer pengguna tidak dapat mengakses internet atau jaringan lokal.

---

## 🛠️ Langkah-Langkah Praktik & Analisis

1. **Memeriksa Konfigurasi Jaringan (`ipconfig /all`)**
   - Memeriksa apakah komputer mendapatkan Alamat IP (DHCP) atau terkonfigurasi secara statis.
   - Memastikan status adapter (*Ethernet* / *Wi-Fi*) dalam keadaan *Enabled*.

2. **Memeriksa Alamat IP & Default Gateway**
   - Memastikan Alamat IP berada dalam subnet yang sama dengan jaringan lokal.
   - Mengecek apakah Alamat *Default Gateway* dan *DNS Server* sudah terisi dengan benar (tidak berawalan `169.254.x.x` / APIPA).

3. **Menguji Koneksi (`ping`)**
   - Perintah `ping 127.0.0.1` untuk menguji *loopback* (TCP/IP stack).
   - Perintah `ping [Alamat_IP_Gateway]` untuk memeriksa koneksi ke router/gateway lokal.
   - Perintah `ping 8.8.8.8` untuk menguji konektivitas keluar menuju internet.
   - Perintah `ping google.com` untuk memastikan resolusi nama domain (DNS) berjalan lancar.

4. **Traceroute Jalur Koneksi (`tracert`)**
   - Menggunakan perintah `tracert 8.8.8.8` untuk melacak lompatan (*hop*) paket data dan menemukan titik kegagalan (*bottleneck* / rute terputus).

5. **Menganalisis Hasil & Diagnosis Masalah**
   - Menganalisis *output* pesan kesalahan seperti `Request timed out`, `Destination host unreachable`, atau `DNS probe finished bad config`.

6. **Perbaikan & Pengujian Ulang**
   - Melakukan *reset* IP & DNS menggunakan perintah `ipconfig /release`, `ipconfig /renew`, serta `ipconfig /flushdns` (atau perbaikan pada lapisan fisik/adapter).
   - Melakukan pengujian ulang `ping` dan membuka browser untuk memastikan akses internet telah pulih.

---

## 📊 Ringkasan Diagnosis & Hasil Perbaikan

| Perintah CMD | Fungsi Utama | Hasil Sebelum Perbaikan | Hasil Setelah Perbaikan |
| :--- | :--- | :--- | :--- |
| `ipconfig /all` | Cek IP, Gateway, & Subnet | Alamat IP bernilai APIPA (`169.254.x.x`) | Mendapatkan IP DHCP valid (`192.168.1.x`) |
| `ping [Gateway]` | Cek koneksi ke router | `Request timed out` | `Reply from 192.168.1.1: bytes=32 time=2ms` |
| `ping 8.8.8.8` | Cek koneksi ke internet | `Destination host unreachable` | `Reply from 8.8.8.8: bytes=32 time=18ms` |
| `ping google.com` | Cek resolusi nama DNS | `Ping request could not find host` | `Reply from 142.250.x.x: bytes=32 time=20ms` |
| `tracert 8.8.8.8` | Analisis rute paket | Terhenti pada hop pertama (*Gateway*) | Berhasil mencapai server tujuan melalui 8-10 hop |
