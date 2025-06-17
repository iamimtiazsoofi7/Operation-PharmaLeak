# Operation-PharmaLeak

# 🕵️‍♂️ Digital Forensics Case Study: Pharmaceutical Data Breach

## 📌 Problem Statement

A leading pharmaceutical company was on the verge of launching a groundbreaking drug when sensitive research data was stolen and leaked to a competitor. A digital forensics expert was brought in to investigate the breach, recover the stolen data, and identify the culprit. The investigation revealed an **insider threat** — a disgruntled employee who executed a sophisticated attack involving **phishing**, **privilege escalation**, and **data exfiltration to the cloud**.

---

## 👨‍💻 Project Team
- **Sudipto Das** – 2022BCY0007  
- **Imtiaz** – 2022BCY0006  
- **Mokshith** – 2022BCY0004  

---

## 📖 Project Overview

This project simulates a real-world digital forensics investigation using **Magnet AXIOM** to analyze multiple digital artifacts.

### 🧩 Phases of Investigation

#### Phase 1: Initial Discovery of the Breach
- Anomalous database queries discovered in Splunk logs at **2:03 AM**.
- Access was made using employee account `jsmith` from an unauthorized IP `192.168.1.100`.
- Logs suggested the breach occurred internally.

#### Phase 2: Tracing the Insider Threat
- Forensic analysis of John Smith’s workstation revealed a **deleted ZIP file** containing the stolen data.
- Windows Registry revealed a script `elevate_privileges.ps1` executed via phishing.
- Email forensics showed a **malicious Word document** as a phishing attachment.

#### Phase 3: Reconstructing the Data Exfiltration
- Network forensics uncovered large HTTPS transfers to `competitorcorp.sharepoint.com`.
- DNS and NetFlow logs aligned with the data theft time frame.

#### Phase 4: Following the Data to the Cloud
- SharePoint cloud logs revealed the upload of `drug_trials_data.zip` from John Smith’s home IP.
- MD5 hash matched the stolen file on his workstation.
- API access logs confirmed the upload was **scripted**, indicating premeditation.

---

## 🔍 Tools & Techniques Used

- **Magnet AXIOM**: Core forensics tool for timeline analysis, registry parsing, file carving, and email/network analysis.
- **Autopsy**: Used for deep workstation image analysis.
- **Wireshark**: For inspecting PCAPs and HTTPS traffic.
- **RegRipper**: Registry analysis.
- **NetFlow & DNS logs**: Correlated with activity timeline.
- **Cloud Forensics**: SharePoint API and audit log analysis.

---

## 🧠 Key Skills Demonstrated

- Log Analysis  
- File System Forensics  
- Registry and Email Artifact Analysis  
- Network Forensics  
- Cloud and API Forensics  
- Hashing and Integrity Validation  
- Chain of Custody Documentation  

---

## 🎯 Capture The Flag (CTF) Challenge

The project includes **25 CTF-style questions** designed to test understanding of forensic techniques and use of Magnet AXIOM.

👉 Explore questions across:
- Unauthorized access detection
- Email and registry analysis
- PCAP inspection and DNS correlation
- Cloud API usage and IP geolocation
- Cryptanalysis and chain of custody

> 📁 Access the challenge dataset and documentation:
> - [🔗 Images & Logs](https://drive.google.com/drive/folders/1_w6jbBnqehmoQaVC5jXNhk9WJdiS6oNy?usp=drive_link)
> - [📄 Final Report](https://drive.google.com/drive/folders/1pSu3OHHVV6uJwfvFVGZ5u5rQOAiFRH4R?usp=drive_link)

---

## 📦 Repository Contents

- `/docs/` – Case files, images, and reports  
- `/CTF_Questions.md` – 25 CTF challenges with solutions  
- `/scripts/` – PowerShell phishing script and parsing tools  
- `/reports/` – Detailed findings and PDF report  
- `README.md` – You are here!

---

## 📚 How to Use

1. Clone the repository:
   ```bash
   git clone https://github.com/<your-username>/digital-forensics-case-study.git
