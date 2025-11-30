# 🛡️ DPSG CyberX: Digital Privacy & Security Guardian (Android)

**Platform:** Android (Java / XML)  
**Package Name:** `com.dpsg.cyberx`  
**Status:** MVP Complete (Structural integrity achieved, API context needs final runtime tuning)

DPSG CyberX is a high-assurance, native Android security application designed to give users complete visibility and proactive control over app permissions, resource usage, and background security risks. It acts as a **digital privacy guardian** by auditing apps that use sensitive system APIs.

---

## 🎯 Project Overview & Core Features

The application is structured into **four main functional modules**, all accessible from the central **MainActivity Dashboard**.

---

# I. Core Application Structure

### User-facing app/permission management features.

| Component | Function | Implementation Details |
|----------|----------|-------------------------|
| **Phase 3: App Permission Manager** | Lists installed apps and audits dangerous permissions (Camera, Mic, Storage, Location). Direct link to OS Settings provided. | Uses `PackageManager.getPackageInfo()` with `GET_PERMISSIONS` executed on a background thread. |
| **Phase 4: Real-Time Monitoring** | Tracks last usage time of sensitive hardware (Camera/Mic/Location) for each app over 7 days. | Powered by `UsageStatsManager` (foreground/background logs). |

---

# II. System Reporting & Security Auditing

### Background metrics collection and risk evaluation.

| Metric / Section | Function | Android API Used |
|------------------|----------|------------------|
| **Phase 5: Privacy Reports** | Generates system health summary: RAM/CPU load, Top 5 Network Hogs, DPSG Security Score. | `ActivityManager`, `Debug.MemoryInfo`, `TrafficStats` |
| **Phase 6: AI Behavioral Alerts** | Shows alerts triggered by rule-based analysis of CPU/RAM spikes or abnormal activity. | Internal Java logic (Mock data supported) |

---

# 📐 DPSG Security Score Logic (0–100%)

| Rule | Metric Checked | Deduction |
|------|----------------|-----------|
| **R1 (High CPU Hogs)** | App processes with CPU > 10% | –5 points per hog |
| **R2 (System Overload)** | Running processes > 50 | –10 points |
| **R3 (RAM Risk)** | RAM usage > 85% | –20 points |
| **R4 (Network Risk)** | Top network hog > 50MB | –15 points |

---

# 🚀 Getting Started

## Prerequisites
- Android Studio (Latest)
- Android SDK Platform 29+ (Android 10+)
- Java + XML support

---

## Installation

1. **Clone the Repository**
   ```
   git clone https://github.com/PERARASU10/CyberX--Digital-Privacy-Security-Guardian.git
   cd CyberX
   ```
## ▶️ Run Instructions

### **Open the Project**
- Open in **Android Studio**
- Allow **Gradle** to complete syncing

### **Run the App**
- Use a **Physical Android Device**  
  **OR**
- Use an **Android 10+ Emulator (API 29 or higher)**

---

## 🔐 Mandatory Runtime Permission (Critical)

Required for **Real-Time Monitoring** to function.

### Steps:
1. Open the app.
2. Navigate to the **Real-Time Monitoring** screen.
3. Tap **Grant Usage Access**.
4. In Android **Settings**, enable:
   **Permit usage access → DPSG CyberX**
5. Return to the app → The status becomes **Granted**.

---

## 💻 Expected Output

### **Dashboard**
A clean UI with the following 4 primary modules:
- **App Permissions**
- **Real-Time Monitoring**
- **Alerts**
- **Reports**

---

### **App Permissions**
- Shows all installed apps  
- Selecting an app displays all **dangerous permissions**  
- A **Manage** button opens the OS settings for that app  

---

### **Reports**
Displays all major device security metrics:
- **Security Score**
- **RAM Usage**
- **CPU Usage**
- **Network Usage**
- **Top 5 Network/Data Hogs**
- **Memory-Sorted Process List**

---

## 🖼️ Output Screenshot





## 🤝 Contributing

Contributions are welcome!

### Steps to Contribute:

1. **Fork this repository**

2. **Create a Feature Branch**
   ```
   git checkout -b feature/AmazingFeature
   ```
3.Commit your changes
  ```
  git commit -m "Add AmazingFeature"
  ```
4.Push the branch
  ```
  git push origin feature/AmazingFeature
  ```
5.Open a Pull Request
  Provide a clear explanation of what you changed and why.

##⚖️ License

  Distributed under the MIT License.
  See LICENSE.md for more information.
   
