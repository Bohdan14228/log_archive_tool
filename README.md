# log_archive_tool

# 🧾 log-archive — Simple Log Archiver and Mail Sender

This Bash script creates a compressed archive (`.tar.gz`) of any log directory  
and optionally sends it to your email via **Gmail SMTP** using `msmtp` and `mail`.

---

## ⚙️ Features
- Archives any specified log directory  
- Automatically names archives by date and time  
- Saves archives locally  
- Optionally emails the archive to a recipient  
- Works with Gmail via `msmtp`

---

## 🧩 Requirements

- Ubuntu 20.04+ or any Debian-based system  
- Gmail account with **App Password** enabled  
- Installed packages: `msmtp`, `msmtp-mta`, `mailutils`, `tar`

---

Create App Password for .msmtprc
https://myaccount.google.com/apppasswords

---

## 🚀 Installation

### 1️⃣ Install dependencies
```bash
sudo apt update
sudo apt install msmtp msmtp-mta mailutils -y
nano ~/.msmtprc
chmod 600 ~/.msmtprc
sudo cp ~/.msmtprc /root/.msmtprc
sudo chmod 600 /root/.msmtprc
sudo cp log-archive /usr/local/bin/
sudo chmod +x /usr/local/bin/log-archive
mkdir -p ~/log_archive_tool/backup(Create a folder for storing backups)
log-archive /var/log/ exemple@gmail.com



