<div align="center">

```text
 ██▓    ▓█████ ██▒   █▓ ██▓ ▄▄▄     ▄▄▄█████▓ ██░ ██  ▄▄▄       ███▄    █    ▒██   ██▒
▓██▒    ▓█   ▀▓██░   █▒▓██▒▒████▄   ▓  ██▒ ▓▒▓██░ ██▒▒████▄     ██ ▀█   █    ▒▒ █ █ ▒░
▒██░    ▒███   ▓██  █▒░▒██▒▒██  ▀█▄ ▒ ▓██░ ▒░▒██▀▀██░▒██  ▀█▄  ▓██  ▀█ ██▒   ░░  █   ░
▒██░    ▒▓█  ▄  ▒██ █░░░██░░██▄▄▄▄██░ ▓██▓ ░ ░▓█ ░██ ░██▄▄▄▄██ ▓██▒  ▐▌██▒    ░ █ █ ▒ 
░██████▒░▒████▒  ▒▀█░  ░██░ ▓█   ▓██▒ ▒██▒ ░ ░▓█▒░██▓ ▓█   ▓██▒▒██░   ▓██░   ▒██▒ ▒██▒
░ ▒░▓  ░░░ ▒░ ░  ░ ▐░  ░▓   ▒▒   ▓▒█░ ▒ ░░    ▒ ░░▒░▒ ▒▒   ▓▒█░░ ▒░   ▒ ▒    ▒▒ ░ ░▓ ░
░ ░ ▒  ░ ░ ░  ░  ░ ░░   ▒ ░  ▒   ▒▒ ░   ░     ▒ ░▒░ ░  ▒   ▒▒ ░░ ░░   ░ ▒░   ░░   ░▒ ░
  ░ ░      ░       ░░   ▒ ░  ░   ▒    ░       ░  ░░ ░  ░   ▒      ░   ░ ░     ░    ░  
    ░  ░   ░  ░     ░   ░        ░  ░         ░  ░  ░      ░  ░         ░     ░    ░  
                   ░                                                                   
```

### ⚡ Offensive Security Researcher & Security Tooling Engineer ⚡
**Founder, Leviathan X** · Reverse Engineering · Attack Surface Management (Failed ASM Lol) · Vulnerability Research

[![Location](https://img.shields.io/badge/Location-Kuala%20Lumpur-red?style=for-the-badge&logo=googlemaps&logoColor=white)](https://github.com/cyeezy08)
[![Domain](https://img.shields.io/badge/Platform-leviathan.ac-00ffcc?style=for-the-badge&logo=firefox&logoColor=black)](https://offsec.leviathan.ac/)
[![X/Twitter](https://img.shields.io/badge/Twitter-%40cpioh8bm-1DA1F2?style=for-the-badge&logo=x&logoColor=white)](https://x.com/cpioh8bm)
[![Email](https://img.shields.io/badge/Contact-chinyeezy08%40gmail.com-D14836?style=for-the-badge&logo=gmail&logoColor=white)](mailto:chinyeezy08@gmail.com)

</div>

---

### 💻 `$ cat /etc/motd`

```bash
> whoami        : Chin Yi Zhe (@cyeezy08)
> role          : Offensive Security Researcher · Systems & Tools Developer
> focus         : Firmware/Binary Reverse Engineering · Attack Surface Intelligence · Protocol Dissection
> platform      : Leviathan Stack (High-Concurrency Go Engines + Passive Threat Analytics)
> primary node  : Custom ARM64 Cluster (Raspberry Pi 5 tuned for 24/7 low-footprint recon)
> philosophy    : "Just Doing What Iam Doing Lol"
```

---

### 🛡️ Selected Vulnerability Research & Advisories

| Target / Advisory | Severity | Vulnerability Class | Impact & Scope |
|---|---|---|---|
| **[HiSilicon SoC DVR OEM Fleet](https://github.com/cyeezy08)** | **CVSS 9.8 (Critical)** | CWE-494 / CWE-78 · CWE-321 | **0-Day Root RCE**: Unsigned firmware boot upgrade hijack (`tar -zxvf`) + hardcoded AES-256 keys (`dvr1234567`). **28,006 internet-facing devices** mapped globally via Shodan hash `1901075043`. Coordinated via CERT/CC. |
| **[`decompress-CWE-59`](https://github.com/cyeezy08/decompress-CWE-59-PoC)** | **High** | CWE-59 (Arbitrary File Write) | Symlink escape and hardlink write bypass in `decompress@4.2.1` (**17.6M weekly downloads**). |
| **[`Kimai-CVE-2026-49865`](https://github.com/cyeezy08/Kimai-CVE-2026-49865-POC)** | **High** | CWE-287 (Authentication Bypass) | Default `APP_SECRET` authentication bypass enabling administrative session forge in Kimai instances $\le 2.57.0$. |
| **[`Tianwen-ERP-Upload`](https://github.com/cyeezy08/Tianwen-ERP-Upload-PoC)** | **Critical** | CWE-434 (Unrestricted File Upload) | Unauthenticated arbitrary file upload in Tianwen Property Management ERP; authored benign reproducible TUI PoC. |
| **[`DoS-Braces-3.03`](https://github.com/cyeezy08/DoS-Braces-3.03)** | **Medium** | CWE-400 (Denial of Service) | Incomplete patch analysis of CVE-2024-4068 via comma-separated brace expansion. |

---

### ⚡ The Leviathan Offensive Arsenal

Specialized offensive tools built in Go and Python designed for speed, low footprint, and zero dependency hell:

```
                  ┌──────────────────────────────────────────────┐
                  │                 LEVIATHAN X                  │
                  └──────┬───────────────────────┬───────────────┘
                         │                       │
           ┌─────────────▼─────────────┐   ┌─────▼─────────────────────────┐
           │        RECON & ASM        │   │       CORRELATION & INTEL     │
           ├───────────────────────────┤   ├───────────────────────────────┤
           │ • HostageLVX (Go)         │   │ • leviathan-core (Python)     │
           │   Dangling DNS & Takeover │   │   Explainable KEV/EPSS engine │
           │ • FenrirLVX (Go)          │   │ • leviathan-intel (FastAPI)   │
           │   Fast WordPress/CMS audit│   │   Multi-tenant exposure API   │
           │ • SurfaceDiff (Python)    │   │ • agy-mcp (Python/FastMCP)    │
           │   Surface delta tracking  │   │   Antigravity Agent bridge    │
           └───────────────────────────┘   └───────────────────────────────┘
```

* 🚀 **[HostageLVX](https://github.com/cyeezy08/HostageLVX)** — Lightning-fast dangling-DNS & subdomain takeover engine in Go. CNAME verification against AWS S3, GitHub Pages, Azure, and 30+ cloud providers.
* W **[FenrirLVX](https://github.com/cyeezy08/FenrirLVX)** — Low-footprint Go CLI for WordPress/CMS testing: plugin fingerprinting, local CVE correlation (`vuln_db.json`), and Shodan facet queries.
* 🤖 **[agy-mcp](https://github.com/cyeezy08/agy-mcp)** — Path-traversal-hardened FastMCP server bridging AI agents with bug bounty orchestration tools.

---

### 🛠️ Technical Stack & Weaponry

```text
Core Languages   :: Go · Python (FastAPI, AsyncIO) · C/C++ · Bash · SQL
Offensive Focus  :: Firmware Reverse Engineering · Binary Protocol Auditing · Attack Surface Management · Supply-Chain AppSec
Reverse Eng      :: Ghidra · GDB · radare2 · binwalk · chroot emulation
Recon & Intel    :: Shodan API (197k+ Query Analytics) · ProjectDiscovery Suite · DNS Records · FIRST EPSS · CISA KEV
Hardware Lab     :: ARM64 SoC Architecture (Raspberry Pi 5 Node, 65k ulimit, tuned concurrency) · Kali Linux
```

---

<div align="center">

### 📊 GitHub Activity & Metrics

<img src="https://github-readme-stats.vercel.app/api?username=cyeezy08&show_icons=true&theme=radical&hide_border=true&count_private=true" width="48%" />
<img src="https://github-readme-stats.vercel.app/api/top-langs/?username=cyeezy08&layout=compact&theme=radical&hide_border=true" width="48%" />

<br>

```text
"The ASN-scale lane needs scanning infrastructure; this lane needs none.
 Pure intelligence correlation against declared assets. Triage is not a scan."
```

**[🌐 offsec.leviathan.ac](https://offsec.leviathan.ac)** · **[🐦 @cpioh8bm](https://x.com/cpioh8bm)** · **[📧 chinyeezy08@gmail.com](mailto:chinyeezy08@gmail.com)**

</div>
