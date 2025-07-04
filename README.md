# 🕷️ Dynamic Application Security Testing (DAST) – CI/CD Pipeline with Wapiti & GitHub Actions

This project demonstrates the integration of **Dynamic Application Security Testing (DAST)** into a secure CI/CD pipeline using **Wapiti**, **Cloudflare Tunnel**, and **GitHub Actions**. A vulnerable Node.js web application is dynamically scanned at runtime to detect real-world web vulnerabilities before deployment.

---

## 🧾 Project Overview

A deliberately insecure Express.js application is exposed temporarily to the public internet using Cloudflare Tunnel. On every code push, **GitHub Actions** triggers a **Wapiti** scan against the live instance. This helps identify runtime vulnerabilities such as reflected XSS, open redirects, and missing security headers. The goal is to embed dynamic vulnerability detection directly into the CI/CD lifecycle to promote secure development practices.

---

## 🧰 Tech Stack

| Layer             | Technology                   |
|------------------|-------------------------------|
| Language          | JavaScript (Node.js)         |
| Framework         | Express.js                   |
| Security Tool     | Wapiti (DAST)                |
| CI/CD Platform    | GitHub Actions               |
| Tunneling Tool    | Cloudflare Tunnel            |
| Development OS    | Windows 11                   |
| Version Control   | Git & GitHub                 |
| Code Editor       | Visual Studio Code           |

---

## 🔧 Tools Used

- **Wapiti** – A dynamic web application vulnerability scanner  
- **Cloudflare Tunnel** – Securely exposes localhost to the public internet  
- **GitHub Actions** – Automates scanning on every commit  
- **Node.js + Express** – Vulnerable web application for testing  
- **VS Code** – IDE used to develop the Node.js app  

---

## ⚙️ How It Works

1. The Node.js server is run locally on port 3000.  
2. Cloudflare Tunnel exposes the server to the internet.  
3. The tunnel’s public URL is used as the Wapiti scan target.  
4. On every push, GitHub Actions runs a Wapiti scan against the public URL.  
5. Scan reports are generated and stored as HTML artifacts in GitHub.

---

## 🧪 Vulnerability Detection

The following real-world issues were detected using Wapiti:

- Reflected **Cross-Site Scripting (XSS)**  
- **Open Redirects** via user-controlled parameters  
- **Missing HTTP Headers**:
  - Content-Security-Policy  
  - X-Frame-Options  
  - X-Content-Type-Options  

These are common web vulnerabilities often missed without runtime testing.

---

## 📜 Report Output

- Wapiti outputs a full **HTML report**  
- Lists discovered vulnerabilities by type and severity  
- Contains request/response examples and affected URLs  
- Available as downloadable artifacts via GitHub Actions

---

## 📌 Key Features

- 🔄 End-to-end automated dynamic scanning in CI/CD  
- 🔍 Simulates attacker behavior to discover runtime flaws  
- ✅ Real-time feedback loop for developers  
- 🧪 Complements SAST tools with runtime security visibility

---

## 🎯 Learning Outcomes

- Gained hands-on experience with DAST tools in DevSecOps  
- Learned how to expose local apps securely for CI pipelines  
- Understood GitHub Actions as a trigger mechanism for automated scanning  
- Practiced interpreting and acting on security scan reports

---

## 🔮 Future Improvements

- Add Slack/Discord notifications for high severity findings  
- Schedule nightly/weekly scans using GitHub cron triggers  
- Correlate Wapiti results with SAST scan outputs  
- Extend scanning to APIs and GraphQL endpoints  
- Centralize reports via dashboards or GitHub Pages

---

## 👨‍💻 Author

**Abhinav Srivastava**  
[GitHub](https://github.com/abhisri073)
