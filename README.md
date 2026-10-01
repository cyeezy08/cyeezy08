Offensive security researcher working on IoT firmware reverse engineering, attack
surface tooling, and published CVE proofs of concept. Founder of
[Leviathan OffSec](https://github.com/leviathan-offsec).

[![leviathan.ac](https://img.shields.io/badge/leviathan.ac-00ffcc?style=flat-square)](https://leviathan.ac)
[![Leviathan OffSec](https://img.shields.io/badge/GitHub-leviathan--offsec-181717?style=flat-square&logo=github)](https://github.com/leviathan-offsec)
[![Bugcrowd](https://img.shields.io/badge/Bugcrowd-h%2Fcyeezy08-171717?style=flat-square)](https://bugcrowd.com/h/cyeezy08)
[![ORCID](https://img.shields.io/badge/ORCID-0009--0008--6789--5538-a6ce21cb?style=flat-square&logo=orcid&logoColor=white)](https://orcid.org/0009-0008-6789-5538)

---

### Firmware Research

**[80 Days Reverse Engineering an IoT DVR](https://leviathan.ac/posts/80-days-reversing-iot-dvr.html)**

HiSilicon ARM32 surveillance firmware across 28,006 internet-facing units. Three
findings proven at the binary level:

- Protocol authentication bypass from a hardcoded AES-256 key
- Unsigned root firmware upgrade chain, executes as uid 0 at boot
- Command injection behind a two-character blocklist, backticks and dollar signs
  filtered, semicolons pipes and redirects not

The writeup includes the disassembly and a Unicorn emulation transcript that captures
the argument at the `system()` call site. No bounty. Written as a post-mortem,
including the parts that did not work.

**Dahua IPC firmware**

Command injection primitive in `libpdi.so`. `NetSetDNSHostName` interpolates its
argument into `system("hostname %s")` with no sanitisation. Confirmed in two product
classes across two separate library builds, from an unstripped binary. Reachability
from a network handler is not established and is not claimed.

---

### Published CVE PoCs

| Target | Severity | Class | Detail |
|---|---|---|---|
| [WordPress_Exploit_Directory](https://github.com/cyeezy08/WordPress_Exploit_Directory) | Critical | CWE-434 | `CVE-2026-32475`, unauthenticated arbitrary file upload in Elementor Pro 4.2.1 and earlier, CVSS 9.0. Fixed in 4.2.2 |
| [Tianwen-ERP-Upload](https://github.com/cyeezy08/Tianwen-ERP-Upload-PoC) | Critical | CWE-434 | Unauthenticated arbitrary file upload in Tianwen Property Management ERP |
| [Kimai-CVE-2026-49865](https://github.com/cyeezy08/Kimai-CVE-2026-49865-POC) | High | CWE-287 | Default `APP_SECRET` allows admin session forgery in Kimai up to 2.57.0 |
| [decompress-CWE-59](https://github.com/cyeezy08/decompress-CWE-59-PoC) | Medium | CWE-59 | Symlink escape and hardlink write bypass in the PyPI `decompress` package, 0.0.5, unpatched. Low install volume |
| [DoS-Braces-3.03](https://github.com/cyeezy08/DoS-Braces-3.03) | Medium | CWE-400 | Incomplete patch analysis for CVE-2024-4068 via comma-separated brace expansion |

---

### Tooling

Built and maintained under [Leviathan OffSec](https://github.com/leviathan-offsec):

| Tool | Language | What it does |
|---|---|---|
| [HostageLVX](https://github.com/leviathan-offsec/HostageLVX) | Go | Dangling DNS and subdomain takeover detection, CNAME verified against 21 cloud services across 28 patterns |
| [FenrirLVX](https://github.com/leviathan-offsec/FenrirLVX) | Go | WordPress and CMS attack surface mapping, plugin fingerprinting, offline CVE correlation |
| [leviathan-core](https://github.com/leviathan-offsec/leviathan-core) | Python | Risk scoring correlating CVSS, FIRST EPSS, CISA KEV and PoC availability |
| [surfacediff](https://github.com/leviathan-offsec/surfacediff) | Python | Content-addressed attack surface snapshots and deterministic field diffs. Zero dependencies |

Tools under active development, not yet released:

| Project | Language | What it is |
|---|---|---|
| agy-mcp | Python | Hardened Model Context Protocol server for AI coding assistants. Repository not public yet |

---

### Approach

For firmware work, the order that actually mattered:

1. Read the vendor's own JavaScript to find unauthenticated download APIs, so every
   image can be MD5-verified against a published hash.
2. Carve using binwalk offsets, then peel container layers structurally until the data
   stops changing. Vendors ship u-boot `comp` bytes that do not match the actual
   codec, so detect by magic and never trust the header.
3. Gate on entropy before attempting extraction. A Shannon entropy of 8.0 means
   encrypted, and it is worth saying so rather than burning a day.
4. Use `objdump -T` for exports and `objdump -d` with an xref filter for
   PLT-resolved call sites. On a stripped ARM PIE this beats running full recursive
   disassembly, which can take an hour on a large binary.
5. Resolve the format string before deciding a sink is exploitable. A `%s` fed by
   request data is a finding. A fixed template is not. This is the step that
   separates the two, and the one most often skipped.

### Background

Previously tracked closed cybercrime forums, initial access brokers, and
one-day exploit trade flows on OSINT work. Currently heads-down on firmware
research and the tooling above.

Skills: Go, Python, C, Bash, SQL. Tools: Ghidra, radare2, binwalk, Unicorn, GDB,
across ARM32, ARM64 and x86_64.

---

Work here is against assets I own or have written authorisation to assess.
Get in touch by email, on GitHub, or via [bugcrowd.com/h/cyeezy08](https://bugcrowd.com/h/cyeezy08).
