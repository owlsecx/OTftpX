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

TFTP / PXE network-boot server configuration security auditor

---

## ✨ Features

- in.tftpd option engine (tftpd-hpa defaults file, xinetd server_args, inetd.conf): --create, --secure, --user, --permissive, --umask, remap files, listen address scope, tcp_wrappers
- atftpd OPTIONS, dnsmasq TFTP / PXE directives only (enable-tftp, tftp-root, tftp-secure, dhcp-boot, pxe-service) — DHCP scopes are left to ODhcpX
- iPXE scripts — plaintext chainloading, imgverify, embedded credentials, boot-time shell
- PXELINUX / GRUB menus — MENU MASTER PASSWD, superusers / password_pbkdf2, root-shell cmdlines, check_signatures, auto-reinstall defaults
- Kickstart / preseed / autoinstall — plaintext and weak password hashes, sshpw, unauthenticated repos, curl | sh post-install scripts
- TFTP root walk — world-writable boot images, keys, tokens, leftovers, escaping symlinks, Secure Boot (unsigned EFI) hints, loader version info
- Secrets masked everywhere; --root offline images
- Export TXT / Markdown / JSON / CSV / SARIF 2.1.0
- Self-test --demo, CI gates --fail-on / --min-severity

---

## ⚙️ Requirements

- **Linux**
- **No Python installation needed** — runs as a standalone executable

---

## 🚀 Usage

```bash
./OTftpX
```

---

## 📦 Part of OwlSec Toolkit

This tool is part of the **OwlSec** suite — a collection of 300+ security and privacy tools.

🔗 [owlsec.org](https://owlsec.org)

---

## ©️ License

MIT License — © Khaled S. Haddad

*Tools are distributed as pre-built executables. Source code is proprietary.*
