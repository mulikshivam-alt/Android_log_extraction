
# 📱 Android Log Extraction and Reporting Tool (Forensic Utility)

## 📌 Overview

This project is a **desktop-based Android Log Extraction and Reporting Tool** designed for **digital forensic investigation**.
The tool connects an **Android device via USB** to a laptop and uses **ADB (Android Debug Bridge)** to extract system and user activity logs. Extracted logs are **parsed, analyzed, hashed, and compiled into a forensic report**.

The application provides a **GUI interface** and supports extraction of:

* Call logs
* SMS logs
* Browser activity logs
* System / debug logs

This tool is intended for **educational, research, and forensic investigation purposes**.

---

## 🎯 Key Features

* USB-based Android device connection
* ADB-powered log extraction
* Modular log extraction (Call, SMS, Browser, Debug)
* Hash generation for forensic integrity
* Automated forensic report generation
* GUI-based desktop application
* Temporary raw log preservation
* Suitable for evidence documentation

---

## 🏗️ Project Architecture

```
Final Project V1/
│
├── main.py                     # Main GUI application (Tkinter)
├── requirements.txt            # Python dependencies
│
├── usermodules/                # Core forensic modules
│   ├── Call_Logs.py             # Call log extraction
│   ├── sms_Logs.py              # SMS log extraction
│   ├── Browser_Logs.py          # Browser history/log extraction
│   ├── debug_Logs.py            # System & debug logs extraction
│   ├── hash.py                  # Hash generation for integrity
│   └── generatereport.py        # Forensic report generation
│
├── tmp/                         # Temporary extracted raw logs
│   ├── call_logs.txt
│   ├── sms_logs.txt
│   └── raw_debug_*.txt
│
├── dist/                        # Packaged / compiled modules
│
├── build/                       # Build artifacts (PyInstaller)
│
├── *.png                        # Screenshots & output visuals
│
└── README.md
```

---

## ⚙️ Technology Stack

* **Programming Language:** Python 3
* **GUI Framework:** Tkinter
* **Android Interface:** ADB (Android Debug Bridge)
* **Packaging:** PyInstaller
* **Operating System:** Windows (tested)

---

## 🔌 Prerequisites

* Python 3.x installed
* ADB installed and added to system PATH
* USB Debugging enabled on Android device
* USB cable for device connection
* Required Python libraries (see `requirements.txt`)

---

## 🚀 Installation & Setup

### 1️⃣ Clone the Repository

```bash
git clone https://github.com/your-username/android-log-extraction-tool.git
cd android-log-extraction-tool
```

### 2️⃣ Install Dependencies

```bash
pip install -r requirements.txt
```

### 3️⃣ Verify ADB Connection

```bash
adb devices
```

Ensure the Android device is listed.

---

## ▶️ How to Run the Tool

```bash
python main.py
```

The GUI window will open, allowing you to:

* Connect device
* Extract logs
* Generate reports

---

## 🧪 Log Extraction Workflow

1. Android device connected via USB
2. ADB session established
3. Logs extracted using shell commands
4. Raw logs saved in `/tmp`
5. Hash values generated
6. Structured forensic report created

---

## 📄 Forensic Report

The generated report includes:

* Device interaction timestamp
* Extracted log summaries
* Hash values for integrity verification
* Structured log sections for analysis

This ensures **chain-of-custody support** and **evidence integrity**.

---

## 🔐 Forensic Integrity

* Hashing ensures logs are **unaltered**
* Raw logs preserved separately
* Report generation is automated and repeatable

---

## ⚠️ Limitations

* Requires USB debugging enabled
* Root access may be required for deeper logs
* Tested primarily on Android devices with ADB support
* Windows-focused deployment

---

## 📚 Use Cases

* Academic forensic projects
* Android system analysis
* Digital evidence collection
* Law enforcement training simulations
* Security research

---

## 👨‍💻 Author

**Shivam Mulik**
M.Tech – Cyber / Digital Forensics
Academic Project

---

## ⚖️ Disclaimer

This tool is developed **strictly for educational and forensic research purposes**.
Unauthorized access to devices without permission may be illegal.

---

## ⭐ Future Enhancements

* SQLite database log parsing
* Cloud-based report storage
* Support for more Android versions
* Advanced timeline reconstruction
* Encrypted report export (PDF)
