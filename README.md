Windows Pentest Toolkit Installer

This PowerShell script automates the installation and setup of a comprehensive penetration testing environment on Windows, tailored for internal assessments, O365/Azure AD testing, post-exploitation, and more.

🚀 Features

Installs popular tools via Chocolatey

Downloads latest GitHub releases for offensive and recon tooling

Extracts tools to a centralized folder: ~/PentestTools/bin

Automatically adds each tool’s path to the user’s PATH environment variable

Skips tools that are already installed or downloaded

📆 Tools Installed
🔍 Recon & Enumeration

BloodHound

ROADtools

PingCastle

Sysinternals Suite

🔓 Credential Access & Abuse

Mimikatz

Rubeus

Seatbelt

LaZagne

🛠 Post-Exploitation / Network Tools

CrackMapExec (CME)

Fiddler

Wireshark

7-Zip

Postman

📝 Documentation

Notepad++

Draw.io

Optional: Markdown editors like Obsidian or Typora (manual install)

🧰 Requirements

Windows 10 or higher

Administrator privileges

Chocolatey (auto-installs if missing)

PowerShell 5+ or PowerShell Core

📂 Folder Structure
~/PentestTools/
├── bin/         → Extracted tools, each in its own folder
├── zips/        → Downloaded GitHub release archives
└── Install-PentestToolkit.ps1

All folders inside bin/ are automatically added to your user PATH.

⚙️ How to Use

Run PowerShell as Administrator

Execute the script:

Set-ExecutionPolicy Bypass -Scope Process -Force
.\Install-PentestToolkit.ps1

💡 On first use, the script will install Chocolatey if not already installed.

Restart your PowerShell window to use CLI tools globally.

✏️ Customization

Add or remove tools from the $chocoPackages or $githubTools arrays in the script.

You can also add support for Git-based clones (e.g., PowerView) or precompiled binaries.

🛡️ Warning

This toolkit includes dual-use security tools intended for authorized, ethical penetration testing and security research. Do not use without explicit permission.
