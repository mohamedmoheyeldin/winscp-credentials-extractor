# WinSCP Credentials Extractor

PowerShell script to extract and decrypt stored WinSCP session credentials from `WinSCP.ini` and export them into JSON format.

---

## 🚀 Features

- Reads WinSCP.ini
- Extracts:
  - Host
  - Username
  - Encrypted Password
- Decrypts passwords to plaintext
- Outputs structured JSON

---

## 📂 Usage

1. Place `decrypt-winscp.ps1` in the same directory as:
   - WinSCP.ini

2. Run:

```powershell
.\decrypt-winscp.ps1
