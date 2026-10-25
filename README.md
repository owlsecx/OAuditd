# 🦉 OAuditd

<p align="center">
  <img src="https://img.shields.io/badge/Platform-Linux-0a0c10?style=flat-square"/>
  <img src="https://img.shields.io/badge/Category-OForensics-blue?style=flat-square"/>
  <img src="https://img.shields.io/badge/License-MIT-green?style=flat-square"/>
  <img src="https://img.shields.io/badge/Part%20of-OwlSec%20Toolkit-7b5ea7?style=flat-square"/>
  <img src="https://img.shields.io/badge/Version-1.0.0-cyan?style=flat-square"/>
</p>

> **OAuditd** — Offline auditd Rules & Config Auditor

---

> ⚠️ **AUTHORISED USE ONLY** — Use only on systems you own or have explicit written permission to test. Unauthorised use is illegal.

---

## 📌 Overview

OAuditd is an offline, read-only auditor for the Linux audit daemon, reviewing auditd.conf and audit rules (rules.d, audit.rules) against CIS and DISA STIG expectations. Tolerant parsers mean malformed configs or rule syntax never crash the audit, and it can inspect a live host or a mounted image via --root. Findings are mapped to CIS / NIST AU-* / CWE with ready-to-paste remediation rules and a generated rules file.

---

## ✨ Features

- Tolerant parsers for auditd.conf and auditctl-syntax rule files
- Storage and failure-mode review (disk_full_action, space_left, log perms)
- Immutable mode, failure flag, backlog and rate-limit checks
- CIS Linux and DISA STIG coverage across identity, time, MAC, logins and more
- Duplicate/conflicting rule detection and rules.d ↔ audit.rules drift
- CIS/NIST/CWE mapping, remediation rules and export TXT/MD/JSON/CSV/SARIF

---

## ⚙️ Requirements

- **Linux**
- **No Python installation needed** — runs as a standalone executable

---

## 🚀 Usage

```bash
./OAuditd --scan
./OAuditd --rules /etc/audit/rules.d/ --baseline stig --fail-on high
./OAuditd --root /mnt/image --scan --format json -o report.json
./OAuditd --help
```

---

## 📦 Part of OwlSec Toolkit

This tool is part of the **OwlSec** suite — a collection of 300+ security and privacy tools.

🔗 [owlsec.org](https://owlsec.org)

---

## ©️ License

MIT License — © Khaled S. Haddad

*Tools are distributed as pre-built executables. Source code is proprietary.*
