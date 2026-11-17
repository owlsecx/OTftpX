# 🦉 OTftpX

<p align="center">
  <img src="https://img.shields.io/badge/Platform-Linux-0a0c10?style=flat-square"/>
  <img src="https://img.shields.io/badge/Category-ONetwork-blue?style=flat-square"/>
  <img src="https://img.shields.io/badge/License-MIT-green?style=flat-square"/>
  <img src="https://img.shields.io/badge/Part%20of-OwlSec%20Toolkit-7b5ea7?style=flat-square"/>
  <img src="https://img.shields.io/badge/Version-1.0.0-cyan?style=flat-square"/>
</p>

> **OTftpX** — TFTP & PXE Network-Boot Server Config Auditor

---

> ⚠️ **AUTHORISED USE ONLY** — Use only on systems you own or have explicit written permission to test. Unauthorised use is illegal.

---

## 📌 Overview


OTftpX is an offline, read-only TFTP and PXE network-boot server configuration auditor covering tftpd-hpa, atftpd, inetd/xinetd in.tftpd and dnsmasq TFTP/PXE directives. It analyses iPXE scripts, PXELINUX/GRUB menus and kickstart/preseed/autoinstall files for plaintext credentials, unauthenticated repos and post-install shell scripts, and walks TFTP roots for world-writable images and keys. Secrets are masked and findings export to TXT, Markdown, JSON, CSV or SARIF.

---

## ✨ Features


- in.tftpd option engine (tftpd-hpa defaults, xinetd server_args, inetd.conf): --create, --secure, --user, remap, scope
- atftpd and dnsmasq TFTP/PXE directives (enable-tftp, tftp-root, tftp-secure, dhcp-boot, pxe-service)
- iPXE script checks: plaintext chainloading, missing imgverify, embedded credentials, boot-time shell
- PXELINUX/GRUB menu checks (MENU MASTER PASSWD, password_pbkdf2, root-shell cmdlines, check_signatures)
- Kickstart/preseed/autoinstall review for plaintext/weak hashes, sshpw and unauthenticated repos
- TFTP root walk for world-writable images, keys and symlinks; secrets masked with TXT/MD/JSON/CSV/SARIF export

---

## ⚙️ Requirements

- **Linux**
- **No Python installation needed** — runs as a standalone executable

---

## 🚀 Usage


```bash
./OTftpX --scan -f sarif -o tftp.sarif
./OTftpX -i /etc/default/tftpd-hpa -i /srv/tftp
./OTftpX -r /mnt/image --fail-on high --json
./OTftpX --demo
./OTftpX --help
```

---

## 📦 Part of OwlSec Toolkit

This tool is part of the **OwlSec** suite — a collection of 300+ security and privacy tools.

🔗 [owlsec.org](https://owlsec.org)

---

## ©️ License

MIT License — © Khaled.s.Haddad

*Tools are distributed as pre-built executables. Source code is proprietary.*
