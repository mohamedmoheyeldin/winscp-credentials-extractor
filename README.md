# WinSCP Credentials Extractor

PowerShell tool to extract, decrypt, and export WinSCP session credentials (host, username, password) from `WinSCP.ini` into JSON format.

---

## 🚀 Features

- Reads WinSCP.ini from local directory
- Parses all stored sessions
- Extracts:
  - Host
  - Username
  - Encrypted Password
- Decrypts passwords into plaintext
- Exports structured JSON output
- Lightweight and easy to run

---

## 📦 Project Structure

```
winscp-credentials-extractor/
│
├── decrypt-winscp.ps1
├── README.md
├── docs/
│   └── WinSCP_Decryption_Documentation.pdf
├── sample/
│   └── output-example.json
└── .gitignore
```

---

## ⚙️ Requirements

- Windows OS
- PowerShell 5.1+ or PowerShell 7+
- WinSCP installed (for generating WinSCP.ini)

---

## 📂 Usage

### 1. Prepare Files

Place the following in the same directory:

- `decrypt-winscp.ps1`
- `WinSCP.ini`

---

### 2. Run Script

```powershell
.\decrypt-winscp.ps1
```

---

### 3. Output

The script generates a JSON file containing decrypted credentials.

#### Example:

```json
{
  "sessions": [
    {
      "host": "example.com",
      "username": "admin",
      "password": "plaintext_password"
    }
  ]
}
```

---

## 🔄 Workflow

1. Load `WinSCP.ini`
2. Parse session entries
3. Extract relevant fields
4. Decrypt stored passwords
5. Build structured JSON
6. Export output file

---

## 🛠 Use Cases

- Credential migration
- Automation reuse
- System auditing
- Integration with other tools

---

## ⚠️ Security Warning

This tool exposes **plaintext credentials**.

### DO NOT:
- Commit output JSON files to GitHub
- Share exported credentials
- Store output in insecure locations

### Recommended:
- Use in a secure environment
- Delete output file after use
- Restrict access to authorized users only

---

## ⚖️ Disclaimer

This tool is intended for **authorized use only**.

Unauthorized access to credentials may violate security policies and laws.

Use responsibly.

---

## 👨‍💻 Author

Mohamed Moheyeldin (Eldin)
QA Automation Engineer | SDET | DevOps
