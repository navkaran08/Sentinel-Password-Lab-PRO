# 🔐 Sentinel Password Lab PRO

> An advanced **Cyber Security password analysis tool** built with **HTML, CSS, and JavaScript**. Sentinel Password Lab PRO analyzes password strength using character analysis, security scoring, search-space estimation, Shannon entropy, common-password detection, predictable pattern detection, optional breach/exposure checking, secure password generation, and practical security recommendations.

## ✨ Features

- 🔒 **Real-time password strength analysis**
- 📊 **Password strength score** with visual indicator
- 🧮 **Search-space estimate & Shannon entropy**
- 🔍 **Character analysis** — lowercase, uppercase, digits, symbols & spaces
- ⚠️ **Built-in common/weak password detection**
- 🔄 **Repeated-character detection**
- 🔢 **Numeric and alphabetic sequence detection**
- ⌨️ **Keyboard-pattern detection**
- 📅 **Predictable password/base-word pattern detection**
- 🛡️ **Optional Pwned Passwords exposure checking**
- 🔐 **k-anonymous breach lookup**
- 🎲 **Web Crypto secure password generator**
- 📝 **Secure passphrase generator**
- 👁️ **Show / Hide password option**
- 📋 **Copy password / generated password**
- 💡 **Security weakness & improvement recommendations**
- 🎨 **Premium Cyber Security / glassmorphism interface**
- ⚡ **Fast client-side analysis**
- 📱 **Responsive mobile interface**
- ♿ **Reduced-motion support**
- 📦 **Standalone HTML application**
- 🚫 **No private application server required for core analysis**

## 🛠️ Requirements

🌐 **Modern Web Browser**

- Google Chrome
- Microsoft Edge
- Mozilla Firefox
- Safari
- Chromium-based browsers

### Optional

For the live Pwned Passwords exposure check, the browser needs network access to the external service.

> **No Node.js, npm, database, or backend server is required for the core application.**

## 📦 Installation or ▶️ Run

Clone the repository:

```bash
git clone https://github.com/navkaran08/Password-Strength-Analyzer-Pro-2026.git
cd Password-Strength-Analyzer-Pro-2026
```

Then open:

```text
Sentinel-Password-Lab-Pro(1).html
```

> If you rename the file to `Sentinel-Password-Lab-Pro.html`, use that filename in the commands below.

## 🪟 Windows CMD

### Clone + Open

```cmd
git clone https://github.com/navkaran08/Password-Strength-Analyzer-Pro-2026.git && cd Password-Strength-Analyzer-Pro-2026 && start Sentinel-Password-Lab-Pro(1).html
```

### Run with Python HTTP Server

```cmd
cd Password-Strength-Analyzer-Pro-2026
python -m http.server 8000
```

Open:

```text
http://localhost:8000/Sentinel-Password-Lab-Pro(1).html
```

## ⚡ Windows PowerShell

### Clone + Open

```powershell
git clone https://github.com/navkaran08/Password-Strength-Analyzer-Pro-2026.git; cd Password-Strength-Analyzer-Pro-2026; Start-Process '.\Sentinel-Password-Lab-Pro(1).html'
```

### Run Local Server

```powershell
cd Password-Strength-Analyzer-Pro-2026
python -m http.server 8000
```

Open:

```text
http://localhost:8000/Sentinel-Password-Lab-Pro(1).html
```

## 🐧 Linux

### Clone + Open

```bash
git clone https://github.com/navkaran08/Password-Strength-Analyzer-Pro-2026.git && cd Password-Strength-Analyzer-Pro-2026 && xdg-open 'Sentinel-Password-Lab-Pro(1).html'
```

### Run Local Server

```bash
cd Password-Strength-Analyzer-Pro-2026
python3 -m http.server 8000
```

Open:

```text
http://localhost:8000/Sentinel-Password-Lab-Pro(1).html
```

## 🍎 macOS

### Clone + Open

```bash
git clone https://github.com/navkaran08/Password-Strength-Analyzer-Pro-2026.git && cd Password-Strength-Analyzer-Pro-2026 && open 'Sentinel-Password-Lab-Pro(1).html'
```

### Run Local Server

```bash
cd Password-Strength-Analyzer-Pro-2026
python3 -m http.server 8000
```

Open:

```text
http://localhost:8000/Sentinel-Password-Lab-Pro(1).html
```

## 📂 Manual Run

Already downloaded the project?

Simply open:

```text
Sentinel-Password-Lab-Pro(1).html
```

with a modern web browser.

> **No installation is required for local password analysis.**

## 🧪 Test the Application

You can use disposable examples such as:

```text
password123
Welcome2026!
aaaaaaaaaaaaaaaa
Correct-Horse-Battery-Test
```

Or use the built-in generator:

```text
Generate secure password
Generate passphrase
20 characters
32 characters
4-word passphrase
```

> Do not enter a password that you currently use for an important account.

## 🔍 Analysis Engine

The application evaluates multiple signals.

### Character Profile

It measures:

```text
Lowercase
Uppercase
Digits
Symbols
Spaces
Unique characters
```

### Pattern Detection

It checks for examples of:

```text
Repeated characters
1234 / 2345 / 3456
9876
abcd
qwer
asdf
zxcv
password
admin
welcome
letmein
qwerty
```

The built-in common-password list is intentionally small and embedded in the HTML. It is **not represented as a claim of a large leaked-password database**.

## 🧮 Entropy & Search Estimate

The tool displays two different concepts.

### Search Estimate

An idealized character-pool estimate based on the detected character classes and password length.

### Shannon Entropy

A statistical calculation based on the observed character distribution.

> These measurements are informative models. They are not guarantees of real-world password security.

## ⏱️ Crack-Time Model

The application provides an illustrative offline-fast guessing estimate based on the calculated search estimate.

The result is a **model estimate**, not a prediction of an actual attack.

Real-world password resistance can depend on:

- Password hashing algorithm
- Hash work factor
- Attacker hardware
- Candidate-generation strategy
- Password reuse
- Known compromises
- Rate limiting
- MFA
- Passkeys
- Other authentication controls

## 🛡️ Breach / Exposure Checking

When network access is available, Sentinel Password Lab PRO can query the **Have I Been Pwned Pwned Passwords** range endpoint.

The browser:

```text
Password
   ↓
Local SHA-1 hash
   ↓
First 5 hash characters
   ↓
Pwned Passwords range request
   ↓
Response searched locally
   ↓
Exposure result
```

The complete password is not sent to the service.

Possible results include:

```text
Found
No match
Unavailable
```

A **No match** result does not prove that a password has never been exposed.

An **Unavailable** result means the external lookup could not be completed and is not treated as a clean result.

## 🔐 Secure Password Generation

Password generation uses the browser's Web Crypto API:

```javascript
crypto.getRandomValues()
```

The application does not use `Math.random()` for password generation.

The generator supports:

- 20-character passwords
- 32-character passwords
- Secure random character selection
- Similar-character exclusion
- Secure multi-word passphrases

## 🔒 Privacy

Core password scoring and analysis are performed locally in the browser.

The application does not send the full password to a private application server.

The page also does not implement password-analysis history storage.

### Important Privacy Note

A browser-based application cannot protect input from a compromised computer, malicious browser extension, malware, screen recorder, proxy, or other software that can observe browser activity.

For sensitive accounts, prefer:

- A reputable password manager
- Unique passwords
- MFA
- Passkeys where supported

## 🎨 Interface

The project includes:

🔐 **Security Dashboard**  
📊 **Strength Meter**  
🧮 **Entropy Analysis**  
🔍 **Character Profile**  
⚠️ **Weakness Detection**  
🛡️ **Breach Exposure Panel**  
🎲 **Secure Generator**  
📝 **Passphrase Generator**  
💡 **Security Recommendations**  
📱 **Responsive Mobile Layout**  
🌙 **Premium Dark Cyber Security Design**

## 🎯 Purpose

Sentinel Password Lab PRO is designed for:

🎓 **Cybersecurity Education**  
🔐 **Password Security Awareness**  
🛡️ **Defensive Security Testing**  
🧪 **Security Demonstrations**  
📚 **Learning Password Security Concepts**  
👨‍💻 **Authorized Security Testing**

Use the tool only with passwords and data you are authorized to test.

## ⚠️ Responsible Use

This project is intended for defensive and educational purposes.

Do not use it to collect, expose, distribute, or publish:

- Real passwords
- Leaked credentials
- Authentication tokens
- Session cookies
- API keys
- Other secrets

Never place real credentials in GitHub issues, screenshots, pull requests, documentation, or demonstrations.

## 📁 Project Structure

```text
Password-Strength-Analyzer-Pro-2026/
│
├── Sentinel-Password-Lab-Pro(1).html
├── README.md
├── LICENSE
└── Usage.txt
```

## 🚀 Quick Commands

### Clone

```bash
git clone https://github.com/navkaran08/Password-Strength-Analyzer-Pro-2026.git
```

### Enter Project

```bash
cd Password-Strength-Analyzer-Pro-2026
```

### Start Local Server

```bash
python -m http.server 8000
```

### Python 3

```bash
python3 -m http.server 8000
```

### Node.js

```bash
npx serve .
```

### PHP

```bash
php -S localhost:8000
```

Stop a running local server with:

```text
CTRL + C
```

## 👨‍💻 Author

**Navkaran Singh**

*Penetration Tester & Ethical Hacker & Cybersecurity Analyst*

## 📄 License

This project is licensed under the **MIT License**.

See [`LICENSE`](LICENSE) for details.

---

<div align="center">

🔐 **Sentinel Password Lab PRO**

**Analyze Smarter. Build Stronger. Protect Better.**

</div>
