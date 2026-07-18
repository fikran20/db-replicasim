# DB-ReplicaSim 🖥️🔋
> **Project Simulasi Replikasi Database Interaktif**  
> Tugas 4 - Mata Kuliah Scalable Systems Design(2026)
> Nama: Fikran
> Nim: 105841119623
> Kelas: RPL-6B

**DB-ReplicaSim** adalah sebuah aplikasi simulator berbasis web interaktif yang dirancang untuk memvisualisasikan bagaimana mekanisme **Database Replication** bekerja pada sistem terdistribusi. Alat peraga edukatif ini mensimulasikan aliran data secara *real-time*, waktu respons (latensi), dampak gangguan jaringan (*replication lag*), hingga skenario kegagalan server (*node crash*).

---

## 🚀 Fitur Utama

Simulator ini mendukung 3 arsitektur replikasi utama sesuai dengan materi kuliah Sistem Terdistribusi:

1. **Master-Slave (Synchronous)**  
   Simulasi penjaminan *Strong Consistency*. Transaksi tulis dari klien akan ditahan oleh Master sampai server Slave memberikan konfirmasi (*ACK*). Jika Slave mati, transaksi otomatis ditolak.
2. **Master-Slave (Asynchronous)**  
   Simulasi *Eventual Consistency*. Master merespons klien secara instan demi latensi rendah, sementara proses push data ke Slave berjalan di latar belakang (*background*), memunculkan efek penundaan data (*replication lag*).
3. **Master-Master (Asynchronous)**  
   Simulasi arsitektur *Multi-Write Node* untuk mencapai *High Availability*. Kedua master dapat menerima operasi baca-tulis sekaligus dan saling mensinkronkan data di latar belakang.

### 🕹️ Kontrol Interaktif yang Tersedia:
* **Slider Replication Lag:** Mengatur jeda waktu sinkronisasi (0.2 hingga 5.0 detik).
* **Hardware Failure Switch:** Mematikan atau menghidupkan server secara paksa (*Crash Simulation*).
* **Live Logs Terminal:** Konsol internal dengan *timestamp* untuk merekam kronologi proses data.

---

## 🛠️ Tech Stack

Aplikasi ini dibangun menggunakan arsitektur *client-side (zero-dependency)* sehingga sangat ringan dan portabel:
* **HTML5 & JavaScript (ES6+):** Logika *state machine* database dan pemrograman asinkron.
* **Tailwind CSS:** Desain antarmuka modern dengan tema *Dark Mode*.
* **Dynamic SVG:** Untuk memvisualisasikan jalur kabel jaringan yang dinamis dan beranimasi saat sinkronisasi data terjadi.
* **FontAwesome:** Ikonografi server dan perangkat komputer.

---

## 💻 Cara Menjalankan Project

Project ini tidak memerlukan proses instalasi server lokal (seperti XAMPP, Node.js, atau Docker). Anda bisa langsung menjalankannya langsung di browser:

### Cara Cepat:
1. Unduh atau clone repository ini ke komputer Anda.
2. Cari file `simulasi.html`.
3. Klik dua kali (*double-click*) file tersebut untuk membukanya di Google Chrome, Edge, Firefox, atau Safari.

---
*Project ini dibuat untuk memenuhi tugas akademik pada Program Studi Teknik Informatika.*
