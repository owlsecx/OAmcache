# 🦉 OAmcache

<p align="center">
  <img src="https://img.shields.io/badge/Platform-Linux-0a0c10?style=flat-square"/>
  <img src="https://img.shields.io/badge/Category-Security-blue?style=flat-square"/>
  <img src="https://img.shields.io/badge/License-MIT-green?style=flat-square"/>
  <img src="https://img.shields.io/badge/Part%20of-OwlSec%20Toolkit-7b5ea7?style=flat-square"/>
  <img src="https://img.shields.io/badge/Version-1.0-cyan?style=flat-square"/>
</p>

> **OAmcache** — part of the OwlSec Toolkit.

---

> ⚠️ **AUTHORISED USE ONLY** — Use only on systems you own or have explicit written permission to test. Unauthorised use is illegal.

---

## 📌 Overview

OAmcache analyzes the Windows Amcache.hve registry hive, which records evidence of programs that ran or were installed. It includes its own REGF hive parser and extracts files with SHA-1 hashes, installed applications, drivers and shortcuts from Windows 7 to 11. A triage engine flags suspicious entries and maps them to MITRE ATT&CK.

---

## ✨ Features

- Native Windows registry (REGF) parser with checksum validation, big-data values and ASCII/UTF-16 names
- Amcache extraction for Windows 10/11 and the legacy 7/8 layout: files with SHA-1, path, publisher, version and link date; apps; drivers; shortcuts
- Triage: masquerading system binaries, renamed tools, offensive and remote-access tools, temp/download paths, double extensions, BYOVD drivers, future link dates
- Timeline with date and keyword filters, search, SHA-1 export and IOC hash matching
- Generic Hive Explorer for any hive (NTUSER, SYSTEM and others) and a demo hive generator
- Reports in TXT / JSON / Markdown / CSV / SARIF

---

## ⚙️ Requirements

- **Linux**
- **No Python installation needed** — runs as a standalone executable

---

## 🚀 Usage

```bash
./OAmcache                                   # interactive menu
./OAmcache --file Amcache.hve
./OAmcache --file Amcache.hve --timeline --from 2026-01-01
./OAmcache --file Amcache.hve --ioc bad_sha1.txt
./OAmcache --file Amcache.hve --drivers
```

Run `./OAmcache --help` for the full list of options.

---

## 📦 Part of OwlSec Toolkit

This tool is part of the **OwlSec** suite — a collection of 300+ security and privacy tools.

🔗 [owlsec.org](https://owlsec.org)

---

## ©️ License

MIT License — © Khaled S. Haddad

*Tools are distributed as pre-built executables. Source code is proprietary.*
