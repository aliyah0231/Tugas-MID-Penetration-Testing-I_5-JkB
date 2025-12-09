# Tugas-MID-Penetration-Testing-I_5-JkB

**Mata Kuliah:** Ethical Hacking and Penetration Testing

**Topik:**  Information Gathering (Passive & Active Reconnaissance)

**Semester:**  5

---

## 👤 Identitas Mahasiswa
| Atribut | Detail |
| :--- | :--- |
| **Nama** | NUR ALIYAH AMALIANI |
| **NIM** | 105841106923 |
| **Jurusan** | Informatika / Jaringan Komputer |

---

## 📂 Unduh Dokumen (Download)

### 1. 📄 [Skenario (Klik untuk Unduh)](SKENARIO_ETHICAL_HACKING.pdf)
Dokumen ini berisi **alur tahapan teknis** yang dilakukan dari awal hingga akhir, termasuk konfigurasi laboratorium dan perintah-perintah yang dijalankan.

### 2. 📊 [Laporan (Klik untuk Unduh)](LAPORAN_ETHICAL_HACKING_UTS.PDF)
Dokumen ini berisi **hasil analisis**, bukti tangkapan layar (*screenshots*), dan kesimpulan mengenai kerentanan yang ditemukan pada target.

---

## 📝 Ringkasan Eksekutif (*Executive Summary*)

Audit ini mensimulasikan serangan *Black-Box* yang dibagi menjadi dua fase:

### 🔹 Fase 1: Passive Reconnaissance (Target: Tokopedia)
Pengumpulan intelijen publik tanpa interaksi langsung.
* **Metode:** Google Dorking, LinkedIn OSINT, BuiltWith.
* **Temuan Kunci:**
    * Sub-domain kritis (`accounts`, `seller`) terekspos.
    * Format email internal teridentifikasi (`nama.nama@tokopedia.com`).
    * Identifikasi personil kunci (*High Value Targets*) untuk simulasi *Whaling*.
    * Teknologi server: Tengine & React.

### 🔹 Fase 2: Active Reconnaissance (Target: VulnOS)
Pemindaian jaringan internal di laboratorium virtual (`192.168.56.20`).
* **Metode:** Nmap Scanning, Service Detection, Wireshark Analysis.
* **Temuan Kunci:**
    * **Port 22 (SSH):** Versi OpenSSH 6.6 (Usang/Vulnerable).
    * **Port 80 (HTTP):** Apache 2.4.7 (Usang).
    * **Port 6667 (IRC):** Layanan tidak lazim (Indikasi Backdoor).
    * **OS Fingerprinting:** Linux Ubuntu (Kernel 3.x/4.x).

---

## 🗂️ Struktur Folder Repositori

Dokumentasi bukti pengerjaan disimpan dalam folder terstruktur:

```text
/
├── 📄 README.md                <-- (Halaman Utama ini)
├── 📄 SKENARIO_PENGERJAAN.pdf  <-- (File Dokumen Skenario)
├── 📄 LAPORAN_LENGKAP.pdf      <-- (File Dokumen Laporan)
│
├── 📂 dokumentasi_gambar/      <-- (Kumpulan Bukti Screenshot)
│   ├── 📂 1_passive_recon/
│   │   ├── subdomain_dork.png
│   │   ├── linkedin_search.png
│   │   ├── builtwith_tech.png
│   │   └── github_leak.png
│   │
│   └── 📂 2_active_recon/
│       ├── nmap_tcp_scan.png
│       ├── nmap_udp_scan.png
│       ├── dhcp_fix_config.png
│       └── wireshark_analysis.png
