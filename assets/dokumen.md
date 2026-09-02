# MANAJEMEN PROYEK INFORMATIKA
### Pengembangan Ekosistem Sistem Informasi Terpadu Pelayanan, Pengaduan, & Konsultasi ASN (BKPSDM Banjarnegara)
**Framework:** PMBOK (*Project Management Body of Knowledge*) | **Fokus Presentasi:** Project Scope & Project Schedule

---

### 1. Project Overview
Proyek ini bertujuan mengembangkan ekosistem sistem informasi digital terpadu berbasis Web dan Mobile (Android) pada **Badan Kepegawaian dan Pengembangan Sumber Daya Manusia (BKPSDM) Pemerintah Kabupaten Banjarnegara**. Sistem ini mengintegrasikan Buku Tamu Digital (Kios Lobi), Pengaduan Masyarakat, Layanan Konsultasi Online ASN dengan Live Chat, Survei Indeks Kepuasan Masyarakat (IKM), Gateway Notifikasi WhatsApp otomatis, Firebase Cloud Messaging (FCM), serta Aplikasi Mobile Android **SAPA BKPSDM** untuk staf dan pimpinan.

---

### 2. Project Scope

#### In-Scope
| No. | Fitur / Komponen Pekerjaan | Deskripsi Realisasi Kode |
|:---:|---|---|
| **1** | **Autentikasi & Multi-Role Authorization** | Login & hak akses multi-level: *Super Admin*, *Kepala Badan*, *Admin Bidang I–IV*, dan *Staf PIC*. |
| **2** | **Kios Self-Service Buku Tamu (Port 8003)** | Portal check-in mandiri di lobi (*web-kiosk*): input identitas, instansi, NIK/NIP, keperluan, bidang tujuan, serta foto/tanda tangan. |
| **3** | **Pengelolaan Buku Tamu & Disposisi (Port 8000)** | Verifikasi kedatangan tamu, penugasan ke PIC bidang, penerimaan tamu, riwayat kunjungan, dan pencatatan notulensi. |
| **4** | **Sistem Pengaduan Masyarakat** | Pengajuan aduan publik, kategorisasi berdasarkan bidang, upload bukti/lampiran, tracking status, verifikasi admin, dan tanggapan resmi. |
| **5** | **Portal Layanan Online & Live Chat ASN (Port 8002)** | Pengajuan konsultasi kepegawaian antar-ASN, ruang live chat interaktif staf-pemohon, serta pertukaran dokumen pendukung. |
| **6** | **Survei Indeks Kepuasan Masyarakat / IKM (Port 8001)** | Form kuesioner publik penilaian pelayanan sesuai standar PermenPAN-RB, perhitungan skor otomatis, dan agregasi mutu pelayanan (A/B/C/D). |
| **7** | **Aplikasi Mobile "SAPA BKPSDM" (Flutter Android)** | Aplikasi mobile untuk Pimpinan & Staf: monitoring buku tamu, rekap aduan, balas chat konsultasi, dan notifikasi instan. |
| **8** | **Push Notification Gateway (Firebase FCM)** | Pengiriman push notification *real-time* ke smartphone Android saat ada tamu penting, aduan masuk, atau pesan chat baru. |
| **9** | **WhatsApp Notification Gateway (Node.js/Baileys Port 3000)** | Pengiriman pesan WA otomatis konfirmasi ke pengunjung, notifikasi tugas ke PIC bidang, dan pemberitahuan disposisi ke pimpinan. |
| **10** | **Executive Dashboard & Rekap Statistik** | Grafik analitik tren kunjungan, distribusi pengaduan, skor IKM per bidang, dan waktu respon layanan. |
| **11** | **Ekspor Laporan & Dokumen** | Cetak rekapitulasi data buku tamu, pengaduan, dan rekap survei IKM dalam format **PDF** dan **Excel (XLSX)**. |
| **12** | **Shared Storage & Microservice Launcher** | Penataan folder penyimpanan file bersama (*shared_storage*) dan script automasi satu-klik (`jalankan_semua.bat`). |

#### Out-of-Scope
| No. | Fitur / Pekerjaan yang Tidak Termasuk |
|:---:|---|
| **1** | Pengembangan aplikasi mobile berbasis **iOS (Apple App Store)** (fokus saat ini eksklusif Android APK). |
| **2** | Integrasi API langsung ke database nasional BKN (seperti SIASN / MyASN BKN). |
| **3** | Integrasi perangkat keras biometrik khusus (seperti mesin *fingerprint* / scanner retina fisik di lobi). |
| **4** | Chatbot berbasis AI / Large Language Model (LLM) untuk menjawab pengaduan & konsultasi secara otomatis tanpa staf. |
| **5** | Fitur pelacakan lokasi (*GPS Real-time Tracking*) staf di lapangan. |
| **6** | Sistem pembayaran atau transaksi retribusi keuangan (*Payment Gateway*). |
| **7** | SMS Gateway GSM / SMS OTP reguler (notifikasi fokus pada WhatsApp & FCM). |

---

### 3. Work Breakdown Structure (WBS)

```text
1. Pengembangan Ekosistem Terpadu BKPSDM
   ├── 1.1 Analisis & Perancangan Sistem
   │   ├── 1.1.1 Analisis alur birokrasi & matriks kewenangan 4 Bidang BKPSDM
   │   ├── 1.1.2 Perancangan skema database terpadu (MySQL) & shared storage
   │   ├── 1.1.3 Perancangan arsitektur multi-port & RESTful API Gateway
   │   └── 1.1.4 Perancangan UI/UX (Admin Tailwind, Kios Lobi, & Mobile SAPA Flutter)
   ├── 1.2 Pengembangan Backend Utama & Portal Admin (Port 8000)
   │   ├── 1.2.1 Autentikasi multi-role & manajemen user/bidang
   │   ├── 1.2.2 Modul manajemen buku tamu & alur disposisi
   │   ├── 1.2.3 Modul penanganan pengaduan masyarakat & tindak lanjut
   │   ├── 1.2.4 Dashboard analitik, rekap IKM, & ekspor laporan (PDF/Excel)
   │   └── 1.2.5 REST API Gateway untuk integrasi Mobile & Web Kios
   ├── 1.3 Pengembangan Modul Web Khusus (Port 8001, 8002, 8003)
   │   ├── 1.3.1 Portal Form Kios Tamu Mandiri (Lobi Onsite - Port 8003)
   │   ├── 1.3.2 Portal Layanan Konsultasi Online ASN & Live Chat (Port 8002)
   │   └── 1.3.3 Portal Publik Survei IKM PermenPAN-RB (Port 8001)
   ├── 1.4 Pengembangan Integrasi & Mobile App
   │   ├── 1.4.1 Microservice WhatsApp Gateway Bot (Node.js/Baileys - Port 3000)
   │   ├── 1.4.2 Integrasi Firebase Cloud Messaging (FCM Service)
   │   └── 1.4.3 Pengembangan Aplikasi Android "SAPA BKPSDM" (Flutter)
   ├── 1.5 Testing & Penjaminan Kualitas
   │   ├── 1.5.1 Unit testing & API endpoint testing
   │   ├── 1.5.2 Integration testing multi-service & shared storage
   │   ├── 1.5.3 User Acceptance Testing (UAT) bersama pegawai BKPSDM
   └── 1.6 Deployment, Integrasi LAN, & Dokumentasi
       ├── 1.6.1 Konfigurasi local server IP, batch automation (jalankan_semua.bat)
       ├── 1.6.2 Penyusunan PANDUAN_IMPLEMENTASI.md & README teknis
       └── 1.6.3 Pelatihan admin & serah terima sistem
```

---

### 4. Project Schedule (3 Bulan / 12 Minggu)

| No. | Aktivitas | Durasi | Bulan | Minggu |
|:---:|---|:---:|:---:|:---:|
| **1** | Analisis kebutuhan bisnis, alur disposisi, dan SOP pelayanan 4 Bidang BKPSDM | 5 Hari | Bulan 1 | Minggu 1 |
| **2** | Perancangan arsitektur database MySQL, API contracts, dan shared storage | 5 Hari | Bulan 1 | Minggu 2 |
| **3** | Perancangan UI/UX & Prototyping (Admin Tailwind, Kios Lobi, Survei, & Mobile) | 6 Hari | Bulan 1 | Minggu 2–3 |
| **4** | Setup Environment, Core Backend Laravel, Autentikasi Multi-Role, & Seeder | 6 Hari | Bulan 1 | Minggu 3–4 |
| **5** | Development Modul Manajemen Buku Tamu, Pengaduan, dan Disposisi Admin (Port 8000) | 6 Hari | Bulan 2 | Minggu 5 |
| **6** | Development Kios Form Tamu Onsite (Port 8003) & Portal Survei IKM (Port 8001) | 5 Hari | Bulan 2 | Minggu 6 |
| **7** | Development Portal Layanan Online ASN & Live Chat Realtime (Port 8002) | 6 Hari | Bulan 2 | Minggu 7 |
| **8** | Development Microservice WhatsApp Gateway Bot (Node.js/Baileys Port 3000) & Queue | 5 Hari | Bulan 2 | Minggu 8 |
| **9** | Development REST API Gateway & Integrasi Push Notification Firebase (FCM) | 5 Hari | Bulan 3 | Minggu 9 |
| **10** | Development Aplikasi Mobile Android SAPA BKPSDM (Flutter) & Ekspor PDF/Excel | 8 Hari | Bulan 3 | Minggu 9–10 |
| **11** | System Integration Testing, Security Testing, & Stress Test Multi-Service | 5 Hari | Bulan 3 | Minggu 11 |
| **12** | User Acceptance Testing (UAT) bersama pegawai BKPSDM & Revisi Feedback | 4 Hari | Bulan 3 | Minggu 11–12 |
| **13** | Deployment Jaringan Lokal (LAN), Setup Batch Runner, Pelatihan & Serah Terima | 4 Hari | Bulan 3 | Minggu 12 |

---

### 5. Milestone

| Milestone | Target | Kriteria Keberhasilan |
|---|:---:|---|
| **M1: Analisis Kebutuhan & SRS Disetujui** | Akhir Minggu 1 | Dokumen kebutuhan fungsional & SOP 4 bidang disepakati bersama stakeholder. |
| **M2: Perancangan Arsitektur & UI/UX Selesai** | Akhir Minggu 3 | Desain database ERD, API schema, dan mockup antarmuka siap diimplementasikan. |
| **M3: Core Backend & Fitur Tamu/Aduan Selesai** | Akhir Minggu 5 | Autentikasi multi-role, buku tamu, dan modul aduan berfungsi di server admin. |
| **M4: Seluruh Sub-Portal Web & WA Bot Selesai** | Akhir Minggu 8 | Form Kios Tamu, Survei IKM, Live Chat ASN, dan WA Gateway aktif terhubung. |
| **M5: REST API, Push Notif FCM, & Mobile App Selesai** | Akhir Minggu 10 | Aplikasi Android Flutter terhubung penuh ke backend dan menerima push notif FCM. |
| **M6: Testing Multi-Service & UAT Selesai** | Akhir Minggu 11 | Seluruh modul lolos functional/integration testing dan disetujui dalam uji UAT. |
| **M7: Deployment, Pelatihan & Project Handover** | Akhir Minggu 12 | Sistem siap operasional via `jalankan_semua.bat`, dokumentasi & pelatihan tuntas. |

---

### 6. Kesimpulan
Proyek **Ekosistem Sistem Informasi BKPSDM Kabupaten Banjarnegara** memiliki cakupan terpadu yang mencakup pengelolaan Buku Tamu Digital, Pengaduan Masyarakat, Konsultasi ASN, Survei IKM, Gateway Notifikasi (WhatsApp & FCM), serta Aplikasi Android SAPA BKPSDM. Seluruh batasan pekerjaan (*In-Scope* & *Out-of-Scope*) telah diterjemahkan ke dalam struktur WBS terperinci dan dijadwalkan secara bertahap selama **3 bulan (12 minggu)**, mulai dari tahap analisis kebutuhan, perancangan arsitektur, development multi-layanan, integrasi mobile/microservice, pengujian, hingga *deployment* dan dokumentasi operasional.
