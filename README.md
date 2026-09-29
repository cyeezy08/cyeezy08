### 👋 Hi, (@cyeezy08)

**Offensive Security Researcher | Threat Intel & Tooling Developer | Founder, Leviathan Offsec**

I'm a security researcher based in Kuala Lumpur. I build high-concurrency offensive tools in Go and Python, hunt for vulnerabilities in open-source software and firmware, and track underground cybercrime ecosystems to understand how threat actors operate.

[![LinkedIn](https://img.shields.io/badge/LinkedIn-Connect-0077B5?style=flat-square&logo=linkedin)](https://www.linkedin.com/in/chin-yi-zhe-38a0753b3/)
[![Website](https://img.shields.io/badge/Website-leviathan.ac-00ffcc?style=flat-square&logo=firefox)](https://leviathan.ac)
[![Organization](https://img.shields.io/badge/GitHub-leviathan--offsec-181717?style=flat-square&logo=github)](https://github.com/leviathan-offsec)
[![Email](https://img.shields.io/badge/Email-chinyeezy08%40gmail.com-D14836?style=flat-square&logo=gmail)](mailto:chinyeezy08@gmail.com)

---

### 💻 `$ cat /etc/motd`

```bash
> whoami        : Chin Yi Zhe (@cyeezy08)
> role          : Offensive Security Researcher · Systems & Tools Developer
> focus         : Firmware/Binary Reverse Engineering · Attack Surface Intelligence · Protocol Dissection
> platform      : Leviathan Stack (High-Concurrency Go Engines + Passive Threat Analytics)
> primary node  : Custom ARM64 Cluster (Raspberry Pi 5 tuned for 24/7 low-footprint recon)
> philosophy    : "Zero Packets When Possible, Pure Intel Always. Explainable Scoring Over Black-Box Vibes."
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

* 🚀 **[HostageLVX](https://github.com/leviathan-offsec/HostageLVX)** — Lightning-fast dangling-DNS & subdomain takeover engine in Go. CNAME verification against AWS S3, GitHub Pages, Azure, and 30+ cloud providers.
* 🐺 **[FenrirLVX](https://github.com/leviathan-offsec/FenrirLVX)** — Low-footprint Go CLI for WordPress/CMS testing: plugin fingerprinting, local CVE correlation (`vuln_db.json`), and Shodan facet queries.
* 🔍 **[SurfaceDiff](https://github.com/leviathan-offsec/surfacediff)** — Diff your attack surface, not your vanity metrics. Tracks perimeters and highlights newly exposed assets.
* ⚖️ **[leviathan-core](https://github.com/leviathan-offsec/leviathan-core)** — The audited Leviathan risk kernel: $\min(100, \text{CVSS}\le40 + \text{EPSS}\le40 + \text{KEV }15 + \text{PoC }5)$ with full reason logging.
* 🤖 **[agy-mcp](https://github.com/leviathan-offsec/agy-mcp)** — Path-traversal-hardened FastMCP server bridging AI agents with bug bounty orchestration tools.

---

### 🧠 Threat Intelligence Background
* **4+ years of OSINT** within closed cybercrime ecosystems.
* Tracked 1-day exploit distribution, IAB (Initial Access Broker) activity, and threat actor TTPs.
* Experienced in translating underground chatter into actionable defensive intelligence.

---

### 🛠️ Tech Stack & Weaponry
`Go` · `Python (FastAPI, AsyncIO)` · `Ghidra` · `GDB` · `radare2` · `binwalk` · `Shodan API` · `CISA KEV` · `FIRST EPSS` · `Docker` · `Linux / ARM64`

---

*"Build. Break. Understand. Secure."*
