# 🛠️ Windows Pentest Toolkit Installer

This PowerShell script automates the installation and setup of a **comprehensive penetration testing environment on Windows**, tailored for internal assessments, O365/Azure AD testing, post-exploitation, and more.

---

## 🚀 Features

- Installs popular tools via [Chocolatey](https://chocolatey.org/)
- Downloads latest GitHub releases for offensive and recon tooling
- Extracts tools to a centralized folder: `~/PentestTools/bin`
- Automatically adds each tool’s path to the user’s `PATH` environment variable
- Skips tools that are already installed or downloaded

---

## 📆 Tools Installed

### 🔍 Recon & Enumeration
- [BloodHound](https://github.com/BloodHoundAD/BloodHound)
- [ROADtools](https://github.com/dirkjanm/ROADtools)
- [PingCastle](https://github.com/vletoux/pingcastle)
- [Sysinternals Suite](https://learn.microsoft.com/en-us/sysinternals/downloads/)

### 🔓 Credential Access & Abuse
- [Mimikatz](https://github.com/gentilkiwi/mimikatz)
- [Rubeus](https://github.com/GhostPack/Rubeus)
- [Seatbelt](https://github.com/GhostPack/Seatbelt)
- [LaZagne](https://github.com/AlessandroZ/LaZagne)

### 🛠 Post-Exploitation / Network Tools
- [CrackMapExec (CME)](https://github.com/byt3bl33d3r/CrackMapExec)
- [Fiddler](https://www.telerik.com/fiddler)
- [Wireshark](https://www.wireshark.org/)
- [7-Zip](https://www.7-zip.org/)
- [Postman](https://www.postman.com/)

### 📝 Documentation
- [Notepad++](https://notepad-plus-plus.org/)
- [Draw.io](https://github.com/jgraph/drawio-desktop/releases)
- Optional: Markdown editors like Obsidian or Typora (manual install)

---

## 🧰 Requirements

- **Windows 10 or higher**
- **Administrator privileges**
- [Chocolatey](https://chocolatey.org/install) (auto-installs if missing)
- PowerShell 5+ or PowerShell Core

---

## 📂 Folder Structure

```
~/PentestTools/
├── bin/         → Extracted tools, each in its own folder
├── zips/        → Downloaded GitHub release archives
└── Install-PentestToolkit.ps1
```

All folders inside `bin/` are automatically added to your user `PATH`.

---

## ⚙️ How to Use

1. **Run PowerShell as Administrator**
2. **Execute the script:**

```powershell
Set-ExecutionPolicy Bypass -Scope Process -Force
.\Install-PentestToolkit.ps1
```

> 💡 On first use, the script will install Chocolatey if not already installed.

3. **Restart your PowerShell window** to use CLI tools globally.

---

## ✏️ Customization

- Add or remove tools from the `$chocoPackages` or `$githubTools` arrays in the script.
- You can also add support for Git-based clones (e.g., PowerView) or precompiled binaries.

---

## 🛡️ Warning

This toolkit includes dual-use security tools intended for authorized, ethical penetration testing and security research. **Do not use without explicit permission.**

---

## 📘 License

MIT License — use at your own risk.

---

## 🙋 Support

Need help adding more tools or modifying the script for your organization? [Open an issue or request a feature](#).

