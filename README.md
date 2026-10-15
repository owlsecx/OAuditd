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

Offline Linux auditd rules & configuration auditor (CIS/STIG coverage)

---

## ✨ Features

- Tolerant auditd.conf parser — duplicates, typos, invalid values, unknown keys never crash the audit
- Tolerant audit rule parser (auditctl syntax) for rules.d/*.rules, audit.rules and --root trees
- Storage & failure-mode review — disk_full_action, space_left/admin_space_left, max_log_file_action, num_logs, flush/freq, write_logs, log permissions
- Immutable mode (-e 2), failure flag (-f), backlog (-b), backlog_wait_time and rate-limit (-r) checks
- CIS Linux & DISA STIG coverage engine — identity, time-change, MAC policy, network env, logins, sessions, perm_mod, access, delete, mounts, modules, sudoers, privileged commands, audit-tool tamper
- Syscall arch coverage (b64/b32), unknown syscalls, never-vs-always ordering, exclude-list blind spots
- Duplicate / conflicting rule detection, key tags, rules.d ↔ audit.rules drift detection
- Setuid/setgid binary discovery for --root trees
- CIS / NIST AU-* / CWE mapping + remediation with ready-to-paste rule lines and a generated rules file
- Exports TXT / Markdown / JSON / CSV / SARIF 2.1.0
- Built-in --demo self-test, CI gates (--fail-on)
- Read-only by design — never modifies the system

---

## ⚙️ Requirements

- **Linux**
- **No Python installation needed** — runs as a standalone executable

---

## 🚀 Usage

```bash
./OAuditd
```

---

## 📦 Part of OwlSec Toolkit

This tool is part of the **OwlSec** suite — a collection of 300+ security and privacy tools.

🔗 [owlsec.org](https://owlsec.org)

---

## ©️ License

MIT License — © Khaled S. Haddad

*Tools are distributed as pre-built executables. Source code is proprietary.*
