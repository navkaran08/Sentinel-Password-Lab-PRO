# 🔐 Sentinel Password Lab PRO

> **Sentinel Password Lab PRO** is a privacy-focused cybersecurity password analysis tool built with **HTML, CSS, and JavaScript**. It analyzes password strength, character composition, predictable patterns, search-space estimates, Shannon entropy, common-password indicators, optional breach exposure, and provides secure password and passphrase generation.

---

## ✨ Features

* 🔒 Real-time password strength analysis
* 📊 Password strength score with visual indicator
* 🧮 Search-space estimation
* 🧠 Shannon entropy calculation
* 🔍 Character analysis

  * Lowercase letters
  * Uppercase letters
  * Numbers
  * Symbols
  * Spaces
  * Unique characters
* ⚠️ Common and weak password detection
* 🔄 Repeated-character detection
* 🔢 Numeric sequence detection
* 🔤 Alphabetic sequence detection
* ⌨️ Keyboard-pattern detection
* 📅 Predictable word and base-pattern detection
* 🛡️ Optional Pwned Passwords exposure checking
* 🔐 k-anonymous breach lookup
* 🎲 Web Crypto API password generation
* 📝 Secure passphrase generation
* 👁️ Show / hide password control
* 📋 Copy password and generated password
* 💡 Security weakness detection
* 💡 Password improvement recommendations
* 🎨 Premium cybersecurity interface
* ⚡ Fast client-side processing
* 📱 Responsive mobile design
* ♿ Reduced-motion support
* 📦 Standalone HTML application
* 🚫 No private backend required for core analysis

---

## 🛠️ Requirements

### 🌐 Modern Web Browser

The application works with modern browsers such as:

* Google Chrome
* Microsoft Edge
* Mozilla Firefox
* Apple Safari
* Chromium-based browsers

### Optional Network Access

Network access is only required for the optional **Pwned Passwords exposure check**.

> **Node.js, npm, databases, and backend servers are not required for the core application.**

---

# 📦 Installation

## 1. Clone the Repository

```bash
git clone https://github.com/navkaran08/Sentinel-Password-Lab-PRO.git
```

Enter the project directory:

```bash
cd Sentinel-Password-Lab-PRO
```

---

# ▶️ Run the Application

The application is a standalone HTML file.

Open:

```text
Sentinel-Password-Lab-Pro.html
```

You can simply double-click the file and open it in a modern browser.

No installation is required for the core password analysis features.

---

# 🪟 Windows CMD

## Clone + Open

```cmd
git clone https://github.com/navkaran08/Sentinel-Password-Lab-PRO.git && cd Sentinel-Password-Lab-PRO && start Sentinel-Password-Lab-Pro.html
```

## Run with Python HTTP Server

```cmd
cd Sentinel-Password-Lab-PRO
python -m http.server 8000
```

Then open:

```text
http://localhost:8000/Sentinel-Password-Lab-Pro.html
```

---

# ⚡ Windows PowerShell

## Clone + Open

```powershell
git clone https://github.com/navkaran08/Sentinel-Password-Lab-PRO.git
cd Sentinel-Password-Lab-PRO
Start-Process '.\Sentinel-Password-Lab-Pro.html'
```

## Run Local Server

```powershell
cd Sentinel-Password-Lab-PRO
python -m http.server 8000
```

Open:

```text
http://localhost:8000/Sentinel-Password-Lab-Pro.html
```

---

# 🐧 Linux

## Clone + Open

```bash
git clone https://github.com/navkaran08/Sentinel-Password-Lab-PRO.git && cd Sentinel-Password-Lab-PRO && xdg-open 'Sentinel-Password-Lab-Pro.html'
```

## Run Local Server

```bash
cd Sentinel-Password-Lab-PRO
python3 -m http.server 8000
```

Open:

```text
http://localhost:8000/Sentinel-Password-Lab-Pro.html
```

---

# 🍎 macOS

## Clone + Open

```bash
git clone https://github.com/navkaran08/Sentinel-Password-Lab-PRO.git && cd Sentinel-Password-Lab-PRO && open 'Sentinel-Password-Lab-Pro.html'
```

## Run Local Server

```bash
cd Sentinel-Password-Lab-PRO
python3 -m http.server 8000
```

Open:

```text
http://localhost:8000/Sentinel-Password-Lab-Pro.html
```

---

# 📂 Manual Run

Already downloaded the repository?

Simply open:

```text
Sentinel-Password-Lab-Pro.html
```

in a modern web browser.

> No installation is required for local password analysis.

---

# 🧪 Testing

For testing and demonstrations, use **disposable example passwords only**.

Examples:

```text
password123
Welcome2026!
aaaaaaaaaaaaaaaa
Correct-Horse-Battery-Test
```

You can also test the built-in generators:

```text
Secure password
Secure passphrase
20-character password
32-character password
4-word passphrase
```

> ⚠️ **Never enter a password that you currently use for an important account.**

---

# 🔍 Analysis Engine

Sentinel Password Lab PRO evaluates multiple password-security signals.

## Character Profile

The analyzer can examine:

```text
Lowercase letters
Uppercase letters
Digits
Symbols
Spaces
Unique characters
Password length
```

---

## ⚠️ Pattern Detection

The analyzer looks for predictable characteristics such as:

```text
Repeated characters
1234
2345
3456
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

The built-in common-password list is intentionally limited and embedded inside the HTML.

> It should **not** be interpreted as a complete leaked-password database.

---

# 🧮 Entropy & Search-Space Estimates

The application displays two different security measurements.

## Search-Space Estimate

The search-space estimate is an idealized calculation based on:

* Password length
* Detected character categories
* Estimated character pool

## Shannon Entropy

Shannon entropy provides a statistical measurement based on the observed distribution of characters in the password.

> ⚠️ These values are **informational models**. They are not guarantees of real-world password security.

Real password security also depends on password construction, attacker strategy, password reuse, hashing configuration, and authentication controls.

---

# ⏱️ Crack-Time Model

The application provides an **illustrative offline guessing estimate** based on its calculated search-space model.

This value is not a prediction of an actual attack.

Actual password resistance can vary depending on:

* Password hashing algorithm
* Hash work factor
* Attacker hardware
* Candidate-generation techniques
* Password reuse
* Previously compromised credentials
* Rate limiting
* Multi-factor authentication
* Passkeys
* Authentication architecture

---

# 🛡️ Breach / Exposure Checking

When enabled and network access is available, Sentinel Password Lab PRO can use the **Pwned Passwords range API** to check whether a password hash appears in known compromised-password data.

The intended flow is:

```text
Password
   ↓
Local SHA-1 hash
   ↓
First 5 hash characters
   ↓
Pwned Passwords range request
   ↓
Returned hash suffixes
   ↓
Local comparison
   ↓
Exposure result
```

The complete password is not sent to the external service.

Possible results include:

```text
Found
No Match
Unavailable
```

### Important

A **No Match** result does not prove that a password has never been exposed.

An **Unavailable** result means the external lookup could not be completed and should not be treated as a clean security result.

---

# 🔐 Secure Password Generation

Password generation uses the browser's **Web Crypto API**.

The application uses:

```javascript
crypto.getRandomValues()
```

rather than:

```javascript
Math.random()
```

The generator supports features such as:

* 20-character passwords
* 32-character passwords
* Secure random character selection
* Similar-character exclusion
* Secure passphrase generation
* Multi-word passphrases

---

# 🔒 Privacy

Sentinel Password Lab PRO is designed with a local-first approach.

Core password analysis is performed directly in the browser.

The application does not send the complete password to a private application server.

The application also does not implement password-analysis history storage.

### Important Privacy Limitation

A browser-based application cannot protect sensitive input from a compromised device or software that can observe browser activity.

Potential examples include:

* Malware
* Malicious browser extensions
* Screen-recording software
* Compromised operating systems
* Untrusted proxies
* Other software with access to browser activity

For real accounts, use:

* Unique passwords
* A reputable password manager
* Multi-factor authentication
* Passkeys where supported

---

# 🎨 Interface

The project provides a premium cybersecurity-style interface containing features such as:

* 🔐 Security Dashboard
* 📊 Password Strength Meter
* 🧮 Entropy Analysis
* 🔍 Character Profile
* ⚠️ Weakness Detection
* 🛡️ Breach Exposure Panel
* 🎲 Secure Password Generator
* 📝 Passphrase Generator
* 💡 Security Recommendations
* 📱 Responsive Mobile Layout
* 🌙 Dark Cybersecurity Design

---

# 🎯 Purpose

Sentinel Password Lab PRO is designed for:

* 🎓 Cybersecurity education
* 🔐 Password security awareness
* 🛡️ Defensive security testing
* 🧪 Security demonstrations
* 📚 Learning password-security concepts
* 👨‍💻 Authorized security testing

Use the application only with passwords and data you are authorized to test.

---

# ⚠️ Responsible Use

This project is intended for **defensive, educational, and authorized security testing**.

Do not use the application to collect, expose, distribute, or publish:

* Real passwords
* Leaked credentials
* Authentication tokens
* Session cookies
* API keys
* Recovery codes
* Private keys
* Other sensitive secrets

Never place real credentials in:

* GitHub issues
* Screenshots
* Pull requests
* Documentation
* Demonstration videos
* Public repositories

---

# 📁 Project Structure

The current repository structure is:

```text
Sentinel-Password-Lab-PRO/
│
├── Sentinel-Password-Lab-Pro.html
├── README.md
├── usage.txt
└── LICENSE
```

---

# 🚀 Quick Commands

## Clone

```bash
git clone https://github.com/navkaran08/Sentinel-Password-Lab-PRO.git
```

## Enter Project

```bash
cd Sentinel-Password-Lab-PRO
```

## Open Application

### Windows

```cmd
start Sentinel-Password-Lab-Pro.html
```

### Linux

```bash
xdg-open Sentinel-Password-Lab-Pro.html
```

### macOS

```bash
open Sentinel-Password-Lab-Pro.html
```

---

# 🌐 Local HTTP Server

## Python

```bash
python -m http.server 8000
```

or:

```bash
python3 -m http.server 8000
```

Open:

```text
http://localhost:8000/Sentinel-Password-Lab-Pro.html
```

## Node.js

If Node.js is installed:

```bash
npx serve .
```

## PHP

If PHP is installed:

```bash
php -S localhost:8000
```

Stop a running local server with:

```text
CTRL + C
```

---

# 👨‍💻 Author

**Navkaran Singh**

Cybersecurity / Penetration Testing

---

# 📄 License

This project is licensed under the **MIT License**.

See the [`LICENSE`](LICENSE) file for details.

---

# ⭐ Project

**Sentinel Password Lab PRO**

A privacy-focused browser-based password security analyzer designed for education, awareness, defensive security testing, and authorized security research.

If you find the project useful, consider giving the repository a ⭐ on GitHub.

**Repository:**
`https://github.com/navkaran08/Sentinel-Password-Lab-PRO`
