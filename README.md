<!-- cyeezy08 GitHub profile. Workflow badges come from GitHub Actions. -->



[Projects](#selected-projects) · [Leviathan X tooling](TOOLING.md) · [Engineering principles](#how-i-build) · [Collaboration](#collaboration)

</div>

## Selected projects

These are independent repositories with separate development timelines. A linked project is not a claim that a new release has shipped recently.

| Project | Focus | Source / status |
| :-- | :-- | :-- |
| **[FenrirLVX](https://github.com/cyeezy08/FenrirLVX)** | WordPress component discovery and local vulnerability-advisory correlation. Tracks detected versions, range confidence and advisory coverage. | [Code](https://github.com/cyeezy08/FenrirLVX) · [CI](https://github.com/cyeezy08/FenrirLVX/actions/workflows/ci.yml) |
| **[HostageLVX](https://github.com/cyeezy08/HostageLVX)** | Dangling-DNS verification with fingerprint-based classification and checks designed to reduce false positives. | [Code](https://github.com/cyeezy08/HostageLVX) · [CI](https://github.com/cyeezy08/HostageLVX/actions/workflows/ci.yml) |
| **[surfacediff](https://github.com/cyeezy08/surfacediff)** | Normalized asset snapshots and field-level change reports for authorized inventories. | [Code](https://github.com/cyeezy08/surfacediff) · [CI](https://github.com/cyeezy08/surfacediff/actions/workflows/ci.yml) |
| **[TyrLVX](https://github.com/cyeezy08/TyrLVX)** | Offline comparison of two authorized API-session captures. Distinguishes meaningful cross-tenant evidence from harmless status and body differences. | [Code](https://github.com/cyeezy08/TyrLVX) |
| **[LLM-bullshit](https://github.com/cyeezy08/LLM-bullshit)** | Experiments in evaluating AI-assisted security review workflows. | [Code](https://github.com/cyeezy08/LLM-bullshit) |

### Repository health (live GitHub signals)

[![FenrirLVX CI](https://github.com/cyeezy08/FenrirLVX/actions/workflows/ci.yml/badge.svg)](https://github.com/cyeezy08/FenrirLVX/actions/workflows/ci.yml)
[![HostageLVX CI](https://github.com/cyeezy08/HostageLVX/actions/workflows/ci.yml/badge.svg)](https://github.com/cyeezy08/HostageLVX/actions/workflows/ci.yml)
[![surfacediff CI](https://github.com/cyeezy08/surfacediff/actions/workflows/ci.yml/badge.svg)](https://github.com/cyeezy08/surfacediff/actions/workflows/ci.yml)

These badges reflect GitHub Actions when available; they are not manually assigned success claims. See each repository's CI logs and release history for current verification.

## How I build

- **Proof before claims.** A successful HTTP response is not automatically a vulnerability, and a successful build is not a security assessment.
- **Coverage is part of the result.** Unknown versions, untested paths, missing advisories and stale feeds must be visible.
- **Reproducible output.** Prefer structured results, fixtures, regression tests, and documented failure conditions to opaque scores.
- **Authorization by design.** Active assessments belong on systems I own or have explicit permission to test.

**Working stack:** Go, Python, Linux, HTTP/API engineering, software supply-chain analysis, automated testing and security data normalization.

## Leviathan X

The [**Leviathan X tooling suite**](TOOLING.md) connects the three public CLI projects through a shared evidence-first design, while keeping each repository independently usable.

**[Leviathan X](https://leviathanx.org)** is an independently developed exposure-intelligence platform in progress. Its intended workflow brings together verified public vulnerability feeds, source provenance, authorized asset inventory, explainable correlation and historical change tracking.

The platform is distinct from the individual CLI tools above. Its full customer-facing deployment and integrations are **not represented as complete** by this profile.

> Research, code and historical datasets are not a substitute for validated production telemetry.

## Collaboration

I welcome thoughtful bug reports, reproducible test cases, documentation improvements, and research discussions through the relevant repository's [issues](https://github.com/cyeezy08?tab=repositories).

For Leviathan X business inquiries: **admin@leviathanx.org**.

Security research and active testing are conducted within documented authorization. Private projects and confidential data are not published through this profile.
