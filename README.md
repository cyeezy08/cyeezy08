# ⚡ CHIN YEEZY (`@cyeezy08`)
### Systems Architect • Autonomous Threat Intelligence • Applied Cybersecurity
> **Founder & Core Architect:** [Leviathan Exposure Intelligence (`leviathan.ac`)](https://leviathan.ac)  
> **Telemetry Lake:** **93,088,005+** Derived Exposure Records • ClickHouse Cloud Postgres • AWS Edge

---

```
┌─────────────────────────────────────────────────────────────────────────────┐
│  LEVIATHAN LIVE THREAT LAKE // CURRENT TELEMETRY                            │
├────────────────────────────────┬────────────────────────────────────────────┤
│  TOTAL INDEXED ASSETS          │  93,088,005 records                        │
│  Darkweb & Stealer Leaks       │  82,481,596 records (Masked + SHA256)      │
│  Open Server & Cloud Files     │  8,579,388 records                         │
│  Live Internet Assets          │  1,624,805 records                         │
│  CISA KEV & CVE Correlations   │  402,216 records                           │
└────────────────────────────────┴────────────────────────────────────────────┘
```

---

## 🛠️ The Custom Recon & Exposure Fleet (Beyond PDTM)
Generic scanners hit rate limits and produce noisy text dumps. I design and build high-throughput, purpose-built Go and Python micro-engines that pipe directly into analytical backends:

* **[`HostageLVX`](https://github.com/cyeezy08/HostageLVX)** — High-speed concurrent dangling DNS and orphaned cloud resource takeover verifier.
* **[`FenrirLVX`](https://github.com/cyeezy08/FenrirLVX)** — Ultra-low latency network asset reconnaissance and port mapper written in pure Go.
* **[`surfacediff`](https://github.com/cyeezy08/surfacediff)** — Immutable, content-addressed attack surface tracker for detecting stealth infrastructure shifts.
* **[`cve-watch`](https://github.com/cyeezy08/security-research)** — Real-time CISA Known Exploited Vulnerabilities (KEV) and zero-day blast radius evaluator.
* **`leviathan-ingest`** — High-concurrency ARM64 ingestion engine streaming >30k records/sec into Postgres with native SHA-256 deduplication.

---

## 🏗️ Systems Architecture & Core Stack
* **Languages:** Go (`pgx`, concurrent network primitives), Python 3.12 (`httpx`, `asyncio`), TypeScript, SQL (ClickHouse / PostgreSQL).
* **Cloud Infrastructure:** AWS (`ap-southeast-2` Lambda, API Gateway, DynamoDB, S3), Cloudflare Edge Workers & Rulesets.
* **Analytical Engines:** ClickHouse Cloud (OLAP clusters) & PostgreSQL 18 (Managed HA Sync).
* **Edge Nodes:** Native Linux PRoot environments (aarch64), Tor SOCKS5 routing, residential/ISP proxy pooling.
* **Model Inference:** NVIDIA NIM (`nemotron-3.5`, `deepseek-v4`), OpenAI API drop-in pipelines.

---

## 🌐 Public Verification & Intel Feeds
* **Live Product & API:** [leviathan.ac](https://leviathan.ac) | [api.leviathan.ac/stats/summary](https://api.leviathan.ac/stats/summary)
* **X (Twitter):** [@LeviathanXCDN](https://x.com/LeviathanXCDN)
* **ORCID:** [0009-0008-6789-5538](https://orcid.org/0009-0008-6789-5538)
* **Direct Contact:** `admin@leviathan.ac`
