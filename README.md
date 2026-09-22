 # 🕵️ NetworkWalks — Week 2 | Project Module 3: Footprinting with Maltego



## 📌 Overview

**Footprinting** is the reconnaissance phase of ethical hacking / penetration testing where publicly available information about a target (domain, email addresses, infrastructure, employees, etc.) is gathered using OSINT (Open Source Intelligence) techniques — without directly interacting with the target's systems.

**Maltego** is a graphical link-analysis tool that automates this process using "Transforms" — modules that query public data sources (search engines, DNS, WHOIS, social media, etc.) and visualize the relationships as an interactive graph.

---

## 🎯 Tasks Covered

| Task | Description |
|------|-------------|
| **Task 1** | Download & install Maltego on a Windows computer |
| **Task 2** | Find all email addresses related to the target organization domain `networkwalks.com` (with due permission) |

---

## 🛠️ Tools Used

- **Maltego Graph (Community Edition)** — v4.11.3
- **Java Runtime (Eclipse Temurin / Adoptium JRE 17)** — bundled prerequisite
- **Target domain:** `networkwalks.com` *(used with explicit permission for training purposes)*

---

## 🚀 Lab Walkthrough

### Task 1 — Install Maltego

1. Go to [maltego.com](https://maltego.com) → **Resources → Download Maltego**.
2. Download **Maltego Graph for Windows** (`.exe + Java (x64)`).
3. Run `MaltegoSetup.exe` **as Administrator**.
4. Allow installation of the required Java Runtime (Eclipse Temurin JRE 17) when prompted.
5. Complete the setup wizard (`Next → Install → Finish`), keeping **Create Desktop Shortcut** checked.
6. Launch Maltego (**Run as Administrator**) and complete first-run configuration:
   - Activation option: **Maltego ID**
   - Activation method: **Online Activation (Default)**
   - Accept the End User License Agreement
   - Create a free **Maltego ID** (email, first name, last name) and verify via **Browser Login**
   - On successful authentication, Maltego redirects back automatically
   - Install Transforms: **Utilities** (default)
   - Web Browser: `<Default System Browser>` | Privacy Mode: **Normal**
7. Click **Finish** — Maltego is now ready to run Transforms.

![Purpose]()
![Purpose]()
![Purpose]()
![Purpose]()

### Task 2 — Footprint `networkwalks.com` for email addresses

1. In the **Entity Palette**, search for **Domain** and drag it onto the graph canvas.
2. Double-click the entity and rename it to `networkwalks.com`.
3. Right-click the entity → filter Transforms by typing **email** → run:
  ![Purpose]()
![Purpose]()
![Purpose]()
5. Maltego queries public sources and returns discovered email entities linked to the domain — e.g. `info@networkwalks.com`.
6. Results (graph + transform logs) can be exported to **XLSX, CSV, images, or PDF** for reporting.

> 💡 **Other useful Transforms to explore:** DNS from Domain, Domain owner detail [Whois], Person from Domain, Explore Historical Snapshots, Search Web, Domain Name System (DNS) Lookup.

---



## ⚠️ Why This Matters (Attacker Perspective)

Information gathered this way (emails, subdomains, technologies) is often the **first step** in a real-world attack chain. Threat actors use footprinting results to:
- Identify likely usernames/email formats for phishing or credential-stuffing
- Fingerprint the technology stack (e.g., CMS platform) and search for known CVEs/exploits
- Map organizational structure and social-engineering targets

Understanding this phase helps defenders reduce their **digital footprint** and anticipate reconnaissance-driven attacks.

---

## 📚 Maltego Facts

- Created by **Paterva** in **2008** in Pretoria, South Africa.
- Has powered **over 1 million investigations** worldwide since launch.
- Used by major organizations including the **FBI**, **INTERPOL**, and roughly half of the **DOW 30** companies.
- Available as a free **Community Edition (CE)** with limited results, plus paid commercial tiers.
- Also available for **Kali Linux** and other platforms.

---

# 👤 Author


**KANISHKA M** Cybersecurity Intern B083

LinkedIn: [https://www.linkedin.com/in/kanishka-m525](https://www.linkedin.com/in/kanishka-m525)
