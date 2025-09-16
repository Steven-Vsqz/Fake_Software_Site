# 🕵️ Wireshark Exercise — Malware Traffic Analysis

<p align="center">
 <img src="https://github.com/user-attachments/assets/a40a99f3-a464-4ec6-bb06-7363a7cd54a8" width="75%" alt="Cover" /> 
</p>

## 📌 Description
The purpose of this exercise was to review a packet capture (pcap) file using Wireshark and produce an incident report.  
During the analysis, it was identified that the user searched for *Google Authenticator* and downloaded a suspicious file, which led to malicious activity on the host.

---

## 🛠️ Tools Used
- [**Wireshark**](https://www.wireshark.org) – network packet analysis  
- [**VirusTotal**](https://www.virustotal.com/gui/home/upload) – malware hash analysis  
- [**UrlScan.io**](https://urlscan.io) – domain/URL reputation check  
- [**VirtualBox**](https://www.oracle.com/virtualization/technologies/vm/downloads/virtualbox-downloads.html) – virtualized lab environment  

---

## 🔗 Exercise link

[Link to exercise](https://www.malware-traffic-analysis.net/2025/01/22/index.html)

---

## 🗂️ The 5 W’s of the Incident

**Who caused the incident?**  
- User account: `shutchenson`  
- Host name: `Desktop-L8C5GSJ`  
- MAC address: `00:d0:b7:26:4a:74`  
- IP address: `10.1.17.215`  

**What happened?**  
- User searched for Google Authenticator and downloaded a suspicious file.  

**When did the incident occur?**  
- January 22, 2025 – 11:45:56 AM  

**Where did the incident happen?**  
- On a Windows workstation (`Desktop-L8C5GSJ`).  

**Why did the incident happen?**  
- The user accessed a fraudulent site (`Authenticatoor.org`) and executed malicious downloads.

---

## 🔎 Findings Summary
- The fake site `Authenticatoor.org` was visited.  
- Three suspicious files were downloaded:  
  - `264872`  
  - `29842.ps1`  
  - `pas.ps1`  
- Command and Control (C2) traffic was established over **port 80** to IP: `5.252.153.241`.  
- Malicious PowerShell and CMD commands executed to download and hide files within system directories.  
- File hashes submitted to **VirusTotal** — categorized as a **Trojan**.  

---

## ⚠️ Indicators of Compromise (IOCs)

**IP Address**  
- `5.252.153.241` (C2 server)  

**Domain**  
- `Authenticatoor.org` (malicious site)  

**Files / Scripts**  
- `264872`  
- `29842.ps1`  
- `pas.ps1`  

**Hash Values**  
- SHA-256: `a833f27c2bb4cad31344e70386c44b5c221f031d7cd2f2a6b8601919e790161e`  

---

## 📊 Screenshots / Evidence

<details close>
<summary>Click to View</summary>

<p align="center">
  <img src="https://github.com/user-attachments/assets/287fd61c-ac56-4481-a623-a509d30082da" width="80%" alt="Image_1" />  
  <br><br>
  <img src="https://github.com/user-attachments/assets/85e949a6-566b-4b3c-9076-89ce4bbc993b" width="80%" alt="Image_2" />  
  <br><br>
  <img src="https://github.com/user-attachments/assets/1bc62517-e54e-44fb-a900-caf78d0e78f6" width="80%" alt="Image_3" />  
  <br><br>
  <img src="https://github.com/user-attachments/assets/ba447e00-2b43-454c-a326-a6a1b2d39849" width="80%" alt="Image_4" />  
</p>

</details>

---

🔗 This project is part of my **learning path toward becoming a SOC Analyst**, focusing on **packet analysis and malware investigation**.
