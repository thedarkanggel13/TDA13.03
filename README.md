<div align="center">

<img src="https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEg37CcA4Uz64b1cOt_C-yCMmenmwVwn_S5BQ9lP-YM-_KQ52PSZ_KdbAlinDxJ0I6rXjBGXizroZjJ6Fnbmf9JFoYwV1wJ60KsgmzQp2GvSCiLUof87dh6fVIXTsGnDGKq9BwX2piPoybBthFtWpRD5LevxlLepgapAALjLGGWkUcOzug/s1600/image1788458552" width="560" alt="TDA GEN 13">

# TDA13.03

## Social Media Security Research & Awareness Repository

**TDA GEN 13 — THE DARK ANGEL 13**

OSINT • Phishing Awareness • Web Security • Defensive Research • Cybersecurity Education

</div>

---

## 📌 About

**TDA13.03** merupakan repository penelitian dan edukasi keamanan siber yang berisi kumpulan materi, contoh halaman, dokumen, serta referensi mengenai keamanan akun media sosial dan serangan berbasis social engineering.

Repository ini dapat digunakan untuk mempelajari:

- phishing awareness;
- social engineering indicators;
- web login page analysis;
- OSINT;
- XSS awareness;
- IP logging concepts;
- persistence/backdoor concepts;
- port forwarding concepts;
- security awareness training;
- defensive cybersecurity research.

Materi dalam repository ini hanya boleh digunakan untuk:

- perangkat milik sendiri;
- akun milik sendiri;
- lab internal;
- sandbox;
- capture-the-flag;
- security awareness simulation dengan izin;
- sistem yang secara eksplisit memberikan izin pengujian.

---

# 📂 Repository Structure

```text
TDA13.03/
│
├── Hacking-Social_Media-Accounts-main.zip
│
└── Hacking-Social_Media-Accounts-main/
    │
    ├── README.md
    │
    ├── Deface-Web-by-exploiting-xss.md
    ├── Google_Dorks.md
    ├── IP-Logger.php
    ├── MSF-Persistence-Backdoor.md
    ├── Shell_Port-Forwarding.md
    ├── Tracking_IP_Address.md
    ├── Social_media_OSINT.pdf
    ├── Stupid.mp3
    │
    ├── Fack-reCaptcha-Phishing/
    │   └── recaptcha-phish/
    │       └── README.md
    │
    ├── Landing-Login-Page/
    │   ├── Basic-fix-Login-form-for-GoPhish.txt
    │   ├── Free_Internet_Landing_Page.html
    │   └── Instagarm-page-with-same-logo2.html
    │
    └── Phishing-Mail/
        ├── Free_Internet_mail.html
        ├── Google-Account-Login-Attempt-mail.html
        ├── Instagram-Login-Attempt-by-Someone-mail.html
        ├── Instagram_Landing_Page.html
        ├── LinkedIn-Password-reset-Attempt-Mail.html
        └── System_is_Out_of_Date.html
```

---

# 🧩 Main Materials

| File / Directory | Purpose |
|---|---|
| `Google_Dorks.md` | Search-query research and OSINT concepts |
| `Social_media_OSINT.pdf` | Social-media OSINT reference |
| `Tracking_IP_Address.md` | IP tracking concepts |
| `IP-Logger.php` | Source sample for IP logging analysis |
| `Deface-Web-by-exploiting-xss.md` | XSS-related web-security notes |
| `MSF-Persistence-Backdoor.md` | Persistence/backdoor research notes |
| `Shell_Port-Forwarding.md` | Network forwarding concepts |
| `Landing-Login-Page/` | Login-page examples for awareness analysis |
| `Phishing-Mail/` | Phishing email examples for awareness training |
| `Fack-reCaptcha-Phishing/` | Fake reCAPTCHA phishing example for analysis |

---

# 🎯 Research Focus

Repository ini cocok untuk mempelajari bagaimana serangan social engineering dapat terlihat dari sisi defender.

Contoh topik analisis:

```text
Suspicious Login Pages
Fake CAPTCHA
Credential Harvesting Indicators
Phishing Email Indicators
OSINT Footprints
IP Logging Concepts
XSS Awareness
Persistence Concepts
Port Forwarding Concepts
Social Engineering Techniques
```

---

# 📱 Installation on Termux

Termux dapat digunakan untuk clone repository, membaca dokumen, memeriksa HTML/PHP secara statis, dan melakukan analisis offline.

---

## 1. Update Termux

```bash
pkg update
pkg upgrade -y
```

---

## 2. Install Paket Dasar

```bash
pkg install -y   git   curl   wget   grep   sed   findutils   file   unzip   python
```

Verifikasi:

```bash
git --version
python --version
file --version
```

---

## 3. Clone Repository

```bash
cd ~

git clone https://github.com/thedarkanggel13/TDA13.03.git

cd ~/TDA13.03
```

Jika repository sudah tersedia:

```bash
cd ~/TDA13.03

git pull --ff-only origin main
```

---

## 4. Masuk ke Project

```bash
cd ~/TDA13.03/Hacking-Social_Media-Accounts-main
```

Periksa isi:

```bash
find . -maxdepth 3 -type f | sort
```

---

## 5. Periksa Jenis File

```bash
find . -maxdepth 3 -type f -exec file {} \;
```

Ini membantu mengidentifikasi:

```text
HTML
PHP
Markdown
PDF
Audio
Text
Other Files
```

---

## 6. Review README Upstream

```bash
sed -n '1,260p' README.md
```

---

## 7. Review Dokumen Markdown

Daftar semua dokumen:

```bash
find . -type f -name "*.md" -print
```

Contoh membaca:

```bash
sed -n '1,220p' Google_Dorks.md
```

```bash
sed -n '1,220p' Tracking_IP_Address.md
```

```bash
sed -n '1,220p' Shell_Port-Forwarding.md
```

---

## 8. Review HTML Secara Offline

Daftar semua halaman HTML:

```bash
find . -type f -name "*.html" -print
```

Lihat source:

```bash
sed -n '1,220p' Landing-Login-Page/Free_Internet_Landing_Page.html
```

atau:

```bash
sed -n '1,220p' Phishing-Mail/Google-Account-Login-Attempt-mail.html
```

---

## 9. Cari Form HTML

Untuk mengidentifikasi halaman yang mempunyai form:

```bash
grep -Rni "<form" .   --include="*.html"   --include="*.php"
```

Cari field password:

```bash
grep -Rni 'type=["'\"']password' .   --include="*.html"   --include="*.php"
```

---

## 10. Cari URL Eksternal

```bash
grep -RniE 'https?://|action=|fetch\(|XMLHttpRequest|location\.href' . --include="*.html" --include="*.php" --include="*.js"
```

Gunakan hasil ini untuk review sebelum membuka halaman apa pun.

---

## 11. Review PHP Secara Statis

Periksa:

```bash
sed -n '1,260p' IP-Logger.php
```

Cari fungsi sensitif:

```bash
grep -nE 'REMOTE_ADDR|HTTP_USER_AGENT|file_put_contents|fopen|curl|header\(|mail\(|exec\(|system\(' IP-Logger.php
```

---

## 12. Security Keyword Scan

```bash
grep -RniE 'password|username|credential|login|cookie|session|token|REMOTE_ADDR|webhook|telegram|discord|mail\(|curl|fetch\(|action=' . --exclude-dir=.git
```

---

## 13. Periksa File Sensitif

```bash
find . -type f   \(     -name ".env"     -o -iname "*.pem"     -o -iname "*.key"     -o -iname "*token*"     -o -iname "*secret*"     -o -iname "*password*"     -o -iname "*cookie*"     -o -iname "*session*"   \)   -not -path "./.git/*"   -print
```

---

# 🐉 Installation on Kali Linux

Kali Linux cocok untuk defensive source review, static analysis, dan isolated lab work.

---

## 1. Update Kali

```bash
sudo apt update
```

Opsional:

```bash
sudo apt upgrade -y
```

Jika menggunakan root:

```bash
apt update
apt upgrade -y
```

---

## 2. Install Paket Analisis Dasar

```bash
sudo apt install -y   git   curl   wget   unzip   file   grep   sed   python3   php-cli
```

Jika shell sudah root, hilangkan `sudo`.

---

## 3. Clone Repository

```bash
cd ~

git clone https://github.com/thedarkanggel13/TDA13.03.git

cd ~/TDA13.03/Hacking-Social_Media-Accounts-main
```

Jika sudah tersedia:

```bash
cd ~/TDA13.03
git pull --ff-only origin main

cd Hacking-Social_Media-Accounts-main
```

---

## 4. Periksa Struktur

```bash
find . -maxdepth 3 -type f | sort
```

---

## 5. Periksa File Type

```bash
find . -maxdepth 3 -type f -exec file {} \;
```

---

## 6. PHP Syntax Check

Tanpa menjalankan file:

```bash
php -l IP-Logger.php
```

Command tersebut hanya melakukan pemeriksaan syntax PHP.

---

## 7. HTML Static Review

Daftar HTML:

```bash
find . -type f -name "*.html" -print
```

Cari form:

```bash
grep -Rni "<form" .   --include="*.html"   --include="*.php"
```

---

## 8. Cari Form Action

```bash
grep -RniE '<form|action=|method=' . --include="*.html" --include="*.php"
```

Ini berguna untuk mengidentifikasi ke mana sebuah form mencoba mengirim data.

---

## 9. Cari External Network Reference

```bash
grep -RniE 'https?://|webhook|telegram|discord|curl|fetch\(|XMLHttpRequest' . --include="*.html" --include="*.php" --include="*.js" --include="*.md"
```

---

## 10. Credential-Handling Review

```bash
grep -RniE 'username|password|credential|login|token|cookie|session' . --exclude-dir=.git
```

---

# 🔎 Defensive Analysis Workflow

Gunakan alur berikut:

```text
Repository
   │
   ▼
Inventory Files
   │
   ▼
Read Documentation
   │
   ▼
Inspect HTML / PHP
   │
   ▼
Check External URLs
   │
   ▼
Check Form Destinations
   │
   ▼
Check Credential Handling
   │
   ▼
Static Security Analysis
   │
   ▼
Isolated Lab Review
```

---

# 🧪 Safe Testing Environment

Direkomendasikan menggunakan:

```text
Disposable Virtual Machine
Offline VM
Sandbox
Isolated Kali Linux Lab
Owned Android Device
Local Security Awareness Lab
Capture-the-Flag Environment
Authorized Training Environment
```

---

# 🛡️ Phishing Awareness Indicators

Beberapa indikator yang perlu diperhatikan ketika menganalisis halaman login atau email:

- domain yang menyerupai layanan asli;
- form login yang mengirim data ke domain berbeda;
- halaman mendesak pengguna untuk segera login;
- URL yang disamarkan;
- halaman CAPTCHA palsu;
- field username/password yang mengirim data ke endpoint tidak resmi;
- email dengan link login tidak dikenal;
- attachment mencurigakan;
- permintaan OTP atau token;
- permintaan credential di luar domain resmi.

---

# 🌐 OSINT Notes

OSINT harus dilakukan hanya menggunakan informasi yang:

- tersedia secara publik;
- diperoleh secara sah;
- digunakan sesuai ketentuan layanan;
- tidak digunakan untuk impersonation;
- tidak digunakan untuk harassment;
- tidak digunakan untuk unauthorized account access.

---

# ⚠️ Important Security Notice

Beberapa file di repository ini menggambarkan teknik yang dapat digunakan dalam serangan phishing, credential harvesting, persistence, tracking, atau web exploitation.

Repository ini tidak boleh digunakan untuk:

```text
Credential Theft
Unauthorized Account Access
Impersonation
Unauthorized Tracking
Malicious Phishing Campaigns
Unauthorized Persistence
Unauthorized Exploitation
Stealing Sessions or Tokens
```

---

# 🔑 Sensitive Information

Jangan commit:

```text
Passwords
API Keys
Access Tokens
Cookies
Sessions
SSH Private Keys
Personal Credentials
Webhook Secrets
Database Credentials
Victim Data
Private Logs
```

Sebelum push:

```bash
find . -type f   \(     -name ".env"     -o -iname "*.pem"     -o -iname "*.key"     -o -iname "*token*"     -o -iname "*secret*"     -o -iname "*password*"     -o -iname "*cookie*"     -o -iname "*session*"   \)   -not -path "./.git/*"   -print
```

---

# 📦 Archive Information

Repository menyertakan archive:

```text
Hacking-Social_Media-Accounts-main.zip
```

Versi extracted tersedia di:

```text
Hacking-Social_Media-Accounts-main/
```

Archive dapat dipertahankan sebagai source snapshot.

---

# 📚 Recommended Use

Repository ini cocok untuk:

```text
Cybersecurity Education
Security Awareness Training
Phishing Detection Training
Defensive Web Analysis
Source Code Review
OSINT Education
Social Engineering Awareness
Static Analysis
Incident Response Training
```

---

# ⚖️ Disclaimer

Seluruh dokumentasi, source code, HTML, PHP, dan materi lain di repository ini disediakan untuk tujuan pendidikan, penelitian defensif, security awareness, dan authorized security testing.

Pengguna bertanggung jawab memastikan penggunaan sesuai:

- hukum yang berlaku;
- kebijakan organisasi;
- terms of service;
- scope pengujian;
- izin pemilik sistem;
- privasi pihak lain.

---

# 📜 License

Periksa ketentuan lisensi dari source project upstream sebelum mendistribusikan atau memodifikasi ulang materi.

---

# 👤 Repository Information

| Information | Value |
|---|---|
| Owner | `thedarkanggel13` |
| Repository | `TDA13.03` |
| Project | `Hacking-Social_Media-Accounts-main` |
| Content | HTML / PHP / Markdown / PDF |
| Focus | Security Research & Awareness |

---

<div align="center">

<img src="https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEg37CcA4Uz64b1cOt_C-yCMmenmwVwn_S5BQ9lP-YM-_KQ52PSZ_KdbAlinDxJ0I6rXjBGXizroZjJ6Fnbmf9JFoYwV1wJ60KsgmzQp2GvSCiLUof87dh6fVIXTsGnDGKq9BwX2piPoybBthFtWpRD5LevxlLepgapAALjLGGWkUcOzug/s1600/image1788458552" width="340" alt="TDA GEN 13">

## TDA GEN 13

### THE DARK ANGEL 13

**Research • Analyze • Learn • Defend • Secure**

</div>
