# 🕵️‍♀️ Wireshark Exercise —  Download From Fake Software Site

## 📌 Description
The purpose of this exercise was to review a pcap file using Wireshark and create a incident report. The user downloaded a suspicious file after searching for Google Authenticator.

---

## 🛠 Tools Used

![image](https://img.shields.io/badge/Wireshark-1679A7?style=for-the-badge&logo=Wireshark&logoColor=white)
![image](https://img.shields.io/badge/VirtualBox-21416b?style=for-the-badge&logo=VirtualBox&logoColor=white)

---

## 🔗 Exercise link

[Link to exercise](https://www.malware-traffic-analysis.net/2025/06/13/index.html)

## 🗂 The 5 W's

**Who (Observed Hosts / Actors)**  
- Infected host IP: `<!-- INSERT IP -->`  
- Attacker IP(s): `<!-- INSERT IP(s) -->`  
- Hostnames / MAC addresses: `<!-- INSERT hostnames or MACs -->`

**What (Activity Observed)**  
- Description of activity (e.g., file upload, C2 beaconing, data exfiltration):  
  `<!-- INSERT concise description -->`

**When (Timestamps & Timezone)**  
- First seen: `<!-- INSERT datetime -->`  
- Last seen:  `<!-- INSERT datetime -->`  
- Timezone: `<!-- INSERT timezone e.g., UTC or EST -->`

**Where (Network / Ports / Protocols)**  
- Source / destination subnets or environments: `<!-- INSERT -->`  
- Protocols & ports observed: `<!-- INSERT (e.g., HTTP port 80, TLS 443, SMB 445) -->`

**Why (Impact / Likely Purpose)**  
- Likely intent (e.g., credential theft, data exfiltration, lateral movement): `<!-- INSERT -->`  
- Business impact / severity: `<!-- INSERT -->`

---

## 🔎 Methodology (How I Investigated)
1. Loaded pcap: `<!-- INSERT file name -->`  
2. Initial triage: used `Statistics → Conversations` and `Statistics → Endpoints`.  
3. Applied filters (examples):  
   - `http`  
   - `ip.src == x.x.x.x && tcp.port == 80`  
   - `tls.handshake`  
4. Followed relevant streams: `Follow → TCP Stream` or `Follow → HTTP Stream`.  
5. Extracted artifacts and corroborated with OSINT / threat intel (if applicable).

*(Replace steps with the exact commands/filters you used.)*

---

## 🧾 Evidence / Screenshots
<!-- Add screenshots of Wireshark filters, TCP stream, HTTP contents, DNS queries, etc. -->
<p align="center">
  <img src="<!-- INSERT IMAGE URL -->" alt="Wireshark Screenshot 1" width="80%" />
</p>

---

## ⚠️ Indicators of Compromise (IOCs)
- **IP addresses:**  
  - `<!-- ip1 -->`  
  - `<!-- ip2 -->`
- **Hostnames / Domains:**  
  - `<!-- domain1 -->`  
  - `<!-- domain2 -->`
- **MAC addresses:**  
  - `<!-- mac1 -->`
- **Suspicious URIs / File names:**  
  - `<!-- URI or filename -->`
- **Hashes (if extracted):**  
  - `<!-- sha256 / md5 -->`
- **Other artifacts:**  
  - `<!-- e.g., User-Agent string, unique cookie, HTTP POST fields -->`

---

## 🧾 Findings Summary
- Key takeaways (3–5 bullets):  
  - `<!-- INSERT finding 1 -->`  
  - `<!-- INSERT finding 2 -->`  
  - `<!-- INSERT finding 3 -->`

---

## ✅ Conclusion & Next Steps
- Short conclusion: `<!-- INSERT -->`  
- Recommended next steps (e.g., block IPs, update detections, run host scans):  
  - `<!-- INSERT -->`

---

## 📚 References & Notes
- PCAP source: `<!-- INSERT source or link to exercise -->`  
- Useful commands/filters:  
  ```text
  # Example filters
  ip.addr == x.x.x.x
  http.request.method == "POST"
  tls.handshake.type == 1




---

## 🖼 Screenshots  

<details close>
<summary>Click to View</summary>

<p align="center">
  <img src="https://github.com/user-attachments/assets/35cfef17-215a-4847-8726-1ae48e2e0fc3" width="80%" alt="Wireshark Conversations" />  
  <br><br>
  <img src="https://github.com/user-attachments/assets/5ec759a6-d883-4094-91cf-ad464590ce95" width="80%" alt="HTTP Stream Analysis" />  
  <br><br>
  <img src="https://github.com/user-attachments/assets/e00c9388-0d78-4bc1-8eb2-1a207c07af7b" width="80%" alt="DNS Query Example" />  
  <br><br>
  <img src="https://github.com/user-attachments/assets/1fab2148-6a84-41c0-932e-521afad8db0e" width="80%" alt="DNS Query Example" />
  <br><br>
  <img src="https://github.com/user-attachments/assets/a17aad5b-91c6-4944-a0ef-a4fcb306602c" width="80%" alt="DNS Query Example" />
</p>

</details>

---

🔗 This project is part of my **learning path toward becoming a SOC Analyst**, focusing on **packet analysis and malware investigation**.
