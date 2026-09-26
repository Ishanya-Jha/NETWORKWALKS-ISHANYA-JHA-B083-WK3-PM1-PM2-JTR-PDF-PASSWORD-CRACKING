# 🔐 Networkwalks Week 03 | Password Security Assessment

**Password Cracking • PDF Security Analysis • Hash Extraction • Evidence-Based Validation**

**Author:** Ishanya Jha
**Program:** Networkwalks Cybersecurity Internship
**Batch:** B083-Networkwalks
**Assessment Theme:** Password Security • PDF Hash Extraction • Password Recovery

> **Authorized Laboratory Assessment:** This repository documents practical password-security activities performed on the three assigned laboratory PDF files within the authorized Networkwalks internship environment. Recovered passwords and sensitive hash values are not published.

---

## 📌 Overview

Week 03 focused on understanding **password-protected PDF files, hash extraction, password cracking, and password verification**.

The same three assigned PDF files were tested using multiple password-recovery workflows:

* **W3-PM1:** JTR GUI and PDF hash extraction
* **W3-PM1:** John the Ripper on Kali Linux
* **W3-PM2:** Networkwalks Hash Calculator
* **W3-PM2:** Networkwalks Password Cracker

The practical workflow was:

```text
Password-Protected PDF
        ↓
PDF Hash Extraction
        ↓
PDF Password Hash
        ↓
Password Cracking
        ↓
Recovered Password
        ↓
PDF Verification
```

---

# 🎯 Objectives

* Understand password-protected PDF security.
* Extract PDF password hashes.
* Use JTR through a graphical interface.
* Use John the Ripper on Kali Linux.
* Use browser-based Networkwalks password-security tools.
* Compare different password-recovery workflows.
* Verify recovered passwords against the assigned PDFs.
* Document the practical work using screenshots and evidence.
* Understand the importance of strong and unique passwords.

---

# 🔬 W3-PM1 | John the Ripper

## 1. JTR GUI

The JTR GUI environment was installed and used to understand the graphical password-cracking workflow.

### Workflow

```text
JTR GUI Installation
        ↓
Load Password Hash
        ↓
Configure Attack
        ↓
Start Recovery
        ↓
Verify Result
```

### 📸 Evidence

![JTR GUI Installation](./W3-PM1-JTR/JTR-GUI/screenshots/01-jtr-gui-installation.png)

![JTR GUI](./W3-PM1-JTR/JTR-GUI/screenshots/02-jtr-gui-open.png)

---

## 2. PDF Hash Extraction

The three assigned PDFs were converted into PDF-compatible password hashes.

PDF hash extraction was performed using the PDF hash extraction workflow and the resulting hashes were used with John the Ripper.

Example:

```bash
/usr/share/john/pdf2john.pl "My Locked PDF1.pdf" > pdf1.hash
```

The same process was performed for PDF2 and PDF3.

### Generated hash files

```text
pdf1.hash
pdf2.hash
pdf3.hash
```

The extracted hashes use the PDF hash format recognized by John the Ripper.

### 📸 Evidence

![PDF1 Hash Extraction](./W3-PM1-JTR/PDF-HASH-EXTRACTION/screenshots/01-pdf1-hash-extraction.png)

![PDF2 Hash Extraction](./W3-PM1-JTR/PDF-HASH-EXTRACTION/screenshots/02-pdf2-hash-extraction.png)

![PDF3 Hash Extraction](./W3-PM1-JTR/PDF-HASH-EXTRACTION/screenshots/03-pdf3-hash-extraction.png)

---

## 3. John the Ripper on Kali Linux

Kali Linux includes John the Ripper.

Installation was verified using:

```bash
which john
```

Output:

```text
/usr/sbin/john
```

### Password Recovery

Each PDF hash was processed individually.

```bash
john pdf1.hash
john pdf2.hash
john pdf3.hash
```

The recovered state was verified using:

```bash
john --show pdf1.hash
john --show pdf2.hash
john --show pdf3.hash
```

### Results

| PDF  | JTR Result  | Verification |
| ---- | ----------- | ------------ |
| PDF1 | ✅ Recovered | ✅ Verified   |
| PDF2 | ✅ Recovered | ✅ Verified   |
| PDF3 | ✅ Recovered | ✅ Verified   |

### 📸 Evidence

![John Installation](./W3-PM1-JTR/KALI-JOHN/screenshots/01-john-installed.png)

![PDF1 JTR](./W3-PM1-JTR/KALI-JOHN/screenshots/02-pdf1-john-crack.png)

![PDF2 JTR](./W3-PM1-JTR/KALI-JOHN/screenshots/03-pdf2-john-crack.png)

![PDF3 JTR](./W3-PM1-JTR/KALI-JOHN/screenshots/04-pdf3-john-crack.png)

---

# 🌐 W3-PM2 | Networkwalks Tools

## 1. Networkwalks Hash Calculator

The assigned PDFs were processed using the Networkwalks Hash Calculator.

**Tool:** Networkwalks Hash Calculator

The workflow was:

```text
Protected PDF
      ↓
Hash Calculator
      ↓
Generated PDF Hash
      ↓
Copy Hash
```

The same process was performed for all three assigned PDFs.

### 📸 Evidence

![PDF1 Hash Calculator](./W3-PM2-NETWORKWALKS/HASH-CALCULATOR/screenshots/01-pdf1-hash-calculator.png)

![PDF2 Hash Calculator](./W3-PM2-NETWORKWALKS/HASH-CALCULATOR/screenshots/02-pdf2-hash-calculator.png)

![PDF3 Hash Calculator](./W3-PM2-NETWORKWALKS/HASH-CALCULATOR/screenshots/03-pdf3-hash-calculator.png)

---

## 2. Networkwalks Password Cracker

The generated PDF hashes were submitted to the Networkwalks Password Cracker.

The tool processed the hashes and attempted password recovery using its available password candidates.

### Workflow

```text
PDF Hash
    ↓
Networkwalks Password Cracker
    ↓
Password Recovery
    ↓
Recovered Password
```

### 📸 Evidence

![PDF1 Password Cracker](./W3-PM2-NETWORKWALKS/PASSWORD-CRACKER/screenshots/01-pdf1-password-cracker.png)

![PDF2 Password Cracker](./W3-PM2-NETWORKWALKS/PASSWORD-CRACKER/screenshots/02-pdf2-password-cracker.png)

![PDF3 Password Cracker](./W3-PM2-NETWORKWALKS/PASSWORD-CRACKER/screenshots/03-pdf3-password-cracker.png)

---

# 📄 PDF Verification

After password recovery, the recovered passwords were used to access the corresponding assigned PDFs.

Successful access confirmed that the recovered credentials were valid for the laboratory files.

### 📸 Evidence

![PDF1 Verification](./W3-PM2-NETWORKWALKS/PDF-VERIFICATION/screenshots/01-pdf1-opened.png)

![PDF2 Verification](./W3-PM2-NETWORKWALKS/PDF-VERIFICATION/screenshots/02-pdf2-opened.png)

![PDF3 Verification](./W3-PM2-NETWORKWALKS/PDF-VERIFICATION/screenshots/03-pdf3-opened.png)

---

# 📊 Overall Results

| PDF                | JTR / Kali  | Networkwalks Tools | PDF Verification |
| ------------------ | ----------- | ------------------ | ---------------- |
| My Locked PDF1.pdf | ✅ Completed | ✅ Completed        | ✅ Verified       |
| My Locked PDF2.pdf | ✅ Completed | ✅ Completed        | ✅ Verified       |
| My Locked PDF3.pdf | ✅ Completed | ✅ Completed        | ✅ Verified       |

---

# 🛠️ Tools Used

* **John the Ripper (JTR)**
* **JTR GUI**
* **Kali Linux**
* **PDF Hash Extraction**
* **Networkwalks Hash Calculator**
* **Networkwalks Password Cracker**
* **GitHub**

---

# 🧠 Key Learning Outcomes

Through this practical, I gained hands-on experience in:

* PDF password security
* Hash extraction
* Password-cracking workflows
* John the Ripper
* Kali Linux command-line tools
* GUI-based password-cracking workflows
* Browser-based security tools
* Password verification
* Evidence collection and documentation
* Secure handling of recovered credentials

---

# 🔐 Security & Ethical Considerations

All activities were performed on the **assigned laboratory PDF files within the authorized internship scope**.

Sensitive information has intentionally been excluded from this public repository.

The following should not be published:

* Recovered passwords
* Complete sensitive hashes
* Protected source PDFs
* Decrypted laboratory files
* Credential-bearing screenshots

The techniques demonstrated here should only be used against systems or files for which appropriate authorization has been provided.

---

# 📁 Repository Structure

```text
WEEK-3-CYBERSECURITY-PROJECT/
│
├── README.md
│
├── W3-PM1-JTR/
│   ├── JTR-GUI/
│   │   └── screenshots/
│   │
│   ├── PDF-HASH-EXTRACTION/
│   │   └── screenshots/
│   │
│   └── KALI-JOHN/
│       └── screenshots/
│
└── W3-PM2-NETWORKWALKS/
    ├── HASH-CALCULATOR/
    │   └── screenshots/
    │
    ├── PASSWORD-CRACKER/
    │   └── screenshots/
    │
    └── PDF-VERIFICATION/
        └── screenshots/
```

---

# 📌 Conclusion

Week 03 provided practical exposure to **password security, PDF hash extraction, password recovery, and credential verification**.

Using the same three assigned PDF files, I worked with both **John the Ripper/Kali Linux** and **Networkwalks password-security tools**, gaining practical understanding of different password-recovery workflows and evidence-based verification.

---

**👤 Ishanya Jha**
**Networkwalks Cybersecurity Internship | B083-Networkwalks**
**MCA 3rd Semester | Cybersecurity & Web Development Intern**
