# 🛡️ Month 1 – Networking, Linux & Security Foundations

Repository ini berisi dokumentasi perjalanan belajar selama 1 bulan membangun pondasi kuat di bidang:

- 🌐 Networking Fundamental
- 🐧 Linux Administration
- 🔐 Basic Security & OWASP Awareness
- 🧪 Hands-on Lab & Mini Pentest Simulation

Target utama dari project ini adalah membangun fundamental skill yang siap naik ke level pentesting & cybersecurity lebih lanjut.

---

# 🎯 OUTPUT AKHIR BULAN 1

Setelah menyelesaikan seluruh materi dan lab di repository ini, saya mampu:

- ✅ Melakukan subnetting manual tanpa kalkulator
- ✅ Melakukan scanning Nmap dan memahami hasilnya
- ✅ Menghubungkan SSH antar VM (termasuk key authentication)
- ✅ Memahami dan menjelaskan OWASP Top 10
- ✅ Menyelesaikan OverTheWire Bandit (0–10+)
- ✅ Membuat 1 Mini Pentest Report dalam bentuk PDF

---

# 📅 STRUCTURE PEMBELAJARAN

## 📘 Week 1 – Networking Fundamental

Fokus membangun pondasi jaringan.

Materi yang dipelajari:

- OSI Model vs TCP/IP Model
- IPv4 Addressing
- Subnetting manual
- CIDR notation
- DNS workflow
- HTTP vs HTTPS
- TCP vs UDP
- 3-Way Handshake
- Port & Service concept
- Basic Nmap scanning

Contoh praktik:

```bash
nmap -sS 192.168.1.10
nmap -sC -sV 192.168.1.10
```

Memahami:
- Open / Closed / Filtered port
- Service detection
- Version detection

---

## 🐧 Week 2 – Linux & Bash Practice

Fokus pada penggunaan Linux sebagai environment utama cybersecurity.

Materi:

- Struktur filesystem Linux
- File permission (chmod, chown)
- Process management (ps, top, kill)
- User management
- Networking commands:
  - ss
  - netstat
  - curl
  - telnet
- Basic Bash scripting
- Setup SSH server
- SSH key-based authentication

Contoh SSH:

```bash
ssh user@192.168.1.20
ssh -i id_rsa user@192.168.1.20
```

---

## 🔐 Week 3 – Security & OWASP Awareness

Mulai masuk ke konsep keamanan.

Materi:

- CIA Triad (Confidentiality, Integrity, Availability)
- Hashing vs Encryption
- Firewall dasar (UFW)
- Packet sniffing HTTP
- OWASP Top 10 overview
- Nmap advanced scan
- Netcat basic usage

Contoh:

```bash
nmap -sC -sV -O -p- 192.168.1.30
nc -lvnp 4444
```

Memahami:
- Service fingerprinting
- Banner grabbing
- Risk exposure dari open port

---

## 🧪 Week 4 – Mini Pentest Simulation & Report

Simulasi penetration testing sederhana pada lab environment.

Target yang digunakan:

- TryHackMe Lab (VPN)
- OverTheWire Bandit
- Metasploitable 2

Tahapan yang dilakukan:

### 1️⃣ Reconnaissance

```bash
nmap -sC -sV -p- 192.168.100.30
```

Contoh temuan:
- 21 (FTP)
- 22 (SSH)
- 23 (Telnet)
- 80 (HTTP)
- 139/445 (SMB)
- 3306 (MySQL)

---

### 2️⃣ Exploitation

- Login Telnet menggunakan default credential
- Akses sebagai root
- Enumerasi user & service

---

### 3️⃣ Post-Exploitation

- Cek SUID binary
- Enumerasi konfigurasi sistem
- Identifikasi service yang tidak perlu aktif

---

### 4️⃣ Security Findings

Contoh temuan:

- Telnet aktif tanpa enkripsi
- Default credential masih digunakan
- Banyak port terbuka tanpa pembatasan firewall

---

### 5️⃣ Recommendations

- Disable Telnet
- Gunakan SSH key-based authentication
- Implementasi firewall (UFW)
- Tutup port yang tidak diperlukan
- Update & patch sistem

---

## 📄 Mini Pentest Report

Week 4 menghasilkan 1 laporan mini pentest berbentuk PDF berisi:

- Scope
- Methodology
- Findings
- Risk Analysis
- Recommendation
- Conclusion

File laporan tersedia di repository.

---

# 🧰 Tools yang Digunakan

## Networking & Recon
- nmap
- netstat
- ss
- tcpdump

## Linux Administration
- chmod
- chown
- ps
- top
- kill

## Security Tools
- netcat
- telnet
- UFW
- SSH

## Lab Environment
- Kali Linux
- Metasploitable 2
- VirtualBox
- TryHackMe VPN

---

# 🚀 Cara Menggunakan Repository Ini

Clone repository:

```bash
git clone https://github.com/Dryex-yo/Month1-Networking-Linux-Security.git
cd Month1-Networking-Linux-Security
```

Baca file per minggu dan praktikkan langsung di lab VM.

Disarankan:
- Gunakan minimal 2 VM
- Dokumentasikan setiap percobaan
- Jangan hanya baca — praktikkan

---

# 🎓 Goal Selanjutnya (Month 2)

- Web exploitation deeper
- Privilege escalation
- Active Directory basic
- CTF challenge lebih kompleks

---

# 📌 Tentang Project Ini

Project ini dibuat sebagai dokumentasi perjalanan belajar cybersecurity dari nol dengan pendekatan:

Theory + Lab + Documentation + Reporting

Tujuan akhirnya bukan hanya bisa "scan", tapi bisa:

- Memahami apa yang terjadi
- Menjelaskan hasil scan
- Menganalisis risiko
- Memberikan rekomendasi keamanan

---

# 👨‍💻 Author

Dryex  
Cybersecurity learner – documenting the journey from zero to professional.
