### @cyeezy08

**Offensive Security Researcher | Systems & Tooling Developer | Founder, Leviathan Offsec**

Vulnerability Research · Firmware & Reverse Engineering · Attack Surface Engineering

[![Website](https://img.shields.io/badge/Platform-leviathan.ac-00ffcc?style=flat-square&logo=firefox)](https://leviathan.ac)
[![Organization](https://img.shields.io/badge/GitHub-leviathan--offsec-181717?style=flat-square&logo=github)](https://github.com/leviathan-offsec)
[![Email](https://img.shields.io/badge/Contact-chinyeezy08%40gmail.com-D14836?style=flat-square&logo=gmail)](mailto:chinyeezy08@gmail.com)

---

```bash
> whoami        : @cyeezy08
> focus         : Vulnerability Research · Embedded Protocol Analysis · Attack Surface Delta Tracking
> platform      : Leviathan Stack (Concurrent Go Utilities + Standard-Library Python Tools)
> node          : Custom ARM64 Recon Cluster (Raspberry Pi 5)
> doctrine      : "Zero Packets When Possible, Pure Intel Always. Explainable Scoring Over Black-Box Vibes."
```

---

### Public Vulnerability Research & Advisories

| Advisory / Target | Severity | Class | Scope & Impact |
|---|---|---|---|
| **[`decompress-CWE-59`](https://github.com/cyeezy08/decompress-CWE-59-PoC)** | High | CWE-59 (Arbitrary File Write) | Symlink escape and hardlink write bypass in `decompress@4.2.1` (**17.6M weekly downloads**). |
| **[`Kimai-CVE-2026-49865`](https://github.com/cyeezy08/Kimai-CVE-2026-49865-POC)** | High | CWE-287 (Authentication Bypass) | Default `APP_SECRET` authentication bypass enabling administrative session forge in Kimai instances $\le 2.57.0$. |
| **[`Tianwen-ERP-Upload`](https://github.com/cyeezy08/Tianwen-ERP-Upload-PoC)** | Critical | CWE-434 (Unrestricted File Upload) | Unauthenticated arbitrary file upload in Tianwen Property Management ERP; paired with terminal demo PoC. |
| **[`DoS-Braces-3.03`](https://github.com/cyeezy08/DoS-Braces-3.03)** | Medium | CWE-400 (Denial of Service) | Incomplete patch analysis of CVE-2024-4068 via comma-separated brace expansion. |

---

### Tooling Suite: Leviathan OffSec

Production security tools built in Go and Python, developed under [`@leviathan-offsec`](https://github.com/leviathan-offsec):

```text
                  ┌──────────────────────────────────────────────┐
                  │                 LEVIATHAN X                  │
                  └──────┬───────────────────────┬───────────────┘
                         │                       │
           ┌─────────────▼─────────────┐   ┌─────▼─────────────────────────┐
           │        RECON & ASM        │   │       CORRELATION & INTEL     │
           ├───────────────────────────┤   ├───────────────────────────────┤
           │ • HostageLVX (Go)         │   │ • leviathan-core (Python)     │
           │   Dangling DNS & Takeover │   │   Explainable KEV/EPSS engine │
           │ • FenrirLVX (Go)          │   │ • agy-mcp (Python/FastMCP)    │
           │   Fast WordPress/CMS audit│   │   Agent Orchestration Bridge  │
           │ • surfacediff (Python)    │   │                               │
           │   Surface delta tracking  │   │                               │
           └───────────────────────────┘   └───────────────────────────────┘
```

* **[HostageLVX](https://github.com/leviathan-offsec/HostageLVX)** — High-speed dangling DNS and subdomain takeover engine in Go. CNAME verification against 30+ cloud and edge providers.
* **[FenrirLVX](https://github.com/leviathan-offsec/FenrirLVX)** — Low-footprint Go CLI for WordPress/CMS testing, local CVE correlation (`vuln_db.json`), and Shodan facet queries.
* **[surfacediff](https://github.com/leviathan-offsec/surfacediff)** — Attack surface snapshotting and field-by-field delta diffing utility. Standard library only, zero dependencies.
* **[leviathan-core](https://github.com/leviathan-offsec/leviathan-core)** — Contract-enforced risk scoring kernel correlating CVSS, EPSS, CISA KEV, and PoC availability.
* **[agy-mcp](https://github.com/leviathan-offsec/agy-mcp)** — Path-traversal-hardened FastMCP server bridging autonomous AI coding assistants with security tooling.

---

### Threat Intelligence & Background
* **4+ years of OSINT** tracking closed cybercrime forums, Initial Access Brokers (IABs), and 1-day exploit trade flows.
* Focus on operationalizing underground adversary intelligence into passive attack surface management rules.

---

### Technical Capabilities
* **Languages:** Go, Python (AsyncIO, FastAPI), C/C++, Bash, SQL
* **Reverse Engineering:** Ghidra, GDB, radare2, binwalk, Linux ARM64/x86_64
* **Security & Intel:** Shodan API, CISA KEV, FIRST EPSS, DNS Protocol Analysis, Supply-Chain Auditing

---

*"Build. Break. Understand. Secure."*
