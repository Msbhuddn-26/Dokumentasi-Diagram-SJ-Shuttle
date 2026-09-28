# 🚌 Dokumentasi-Diagram-SJ-Shuttle (TelePort UNPAM)

Repositori ini berisi kumpulan dokumentasi **System Analysis & Design (SAD)** untuk proyek perangkat lunak **SJ Shuttle (Telemetry Pamulang Orbit Transportation)**. 

Dokumentasi ini memetakan seluruh arsitektur sistem, interaksi aktor, alur proses (*workflow*), komunikasi antar-objek (MVC), hingga logika komputasi di peladen (*backend*) sebelum diimplementasikan ke dalam kode pemrograman. Seluruh diagram telah dibungkus ke dalam antarmuka presentasi HTML statis yang interaktif dan mudah dibaca.

---

## 🚀 Fitur Utama Sistem yang Dimodelkan
Dokumentasi ini merancang arsitektur untuk ekosistem *shuttle bus* dengan standar *Enterprise*, meliputi:
1. **Self-Ticketing & Dynamic QR:** Pembuatan token QR sekali pakai dengan batasan waktu (TTL 5 Menit).
2. **Geo-Validation Boarding:** Pemotongan saldo otomatis (*cashless*) yang diwajibkan melalui validasi jarak spasial (<15 meter) menggunakan **Algoritma Trigonometri Haversine** guna mencegah indikasi *Fake GPS*.
3. **Automated E-Wallet:** Integrasi pendanaan dompet digital mandiri via *Webhook* **Midtrans Payment Gateway**.
4. **Real-time Telemetry:** Pelacakan armada bus secara langsung (detik-per-detik) menggunakan infrastruktur **WebSocket (Laravel Reverb)**.
5. **Auto-Scheduler (Hibernation):** Efisiensi beban peladen menggunakan *Cron Job* yang secara otomatis menidurkan transmisi GPS saat armada sedang tidak beroperasi di luar jam masuk/pulang kampus.
6. **Emergency Chain-Reaction:** Protokol sistem mitigasi terpadu (SOS Alert) saat armada mengalami kerusakan teknis.

---

## 📂 Struktur Direktori (*Folder Structure*)
Proyek dokumentasi ini disusun dengan sangat rapi dan modular:

```text
📁 Dokumentasi-SJ-Shuttle/
├── 📁 activity/         # Kumpulan gambar Activity Diagram (.png)
├── 📁 flowchart/        # Kumpulan gambar Flowchart Diagram (.png)
├── 📁 sequence/         # Kumpulan gambar Sequence Diagram (.png)
├── 📄 index.html        # Halaman Dashboard Navigasi Utama (Start Here!)
├── 📄 use_case.html     # Halaman Presentasi Skenario Use Case
├── 📄 activity.html     # Halaman Presentasi Activity Diagram
├── 📄 sequence.html     # Halaman Presentasi Sequence Diagram
├── 📄 flowchart.html    # Halaman Presentasi Algoritma & Flowchart
├── 📄 use_case.png      # Master File Use Case Diagram
└── 📄 README.md         # Dokumentasi Repositori
