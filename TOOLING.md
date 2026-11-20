# Leviathan X | Open-source security tooling

**Discover. Verify. Compare. Explain.**

Leviathan X is the umbrella identity for a small, maintained set of security-engineering tools. Each utility works independently. The eventual unified investigation API is a separate integration project, not a feature already shipped.

## Flagship lineup

| Project | Primary question | Result or coverage boundary |
| --- | --- | --- |
| [FenrirLVX](https://github.com/cyeezy08/FenrirLVX) | Which observed WordPress components match a local advisory? | Observed version, candidate advisory, data coverage and unknown versions |
| [HostageLVX](https://github.com/cyeezy08/HostageLVX) | Does an authorized hostname show evidence of a dangling provider configuration? | Provider fingerprints and classification with false-positive caveats |
| [surfacediff](https://github.com/cyeezy08/surfacediff) | What changed between two authorized asset inventories? | Reproducible snapshots, field-level deltas and missing-history limitations |

The tools are not bulk target discovery services. Use only with permission for network checks. Uncertain observations must never be presented as confirmed exploitation or absence of risk.

## Consistent visual identity

All flagship repositories use a common **Leviathan X** banner in their own `assets/leviathan-x-header.svg` files and keep meaningful screenshots or real CLI recordings when available.

- Palette: near-black `#07090E`, mint `#00FFCC`, cyan `#38BDF8`, pale slate.
- Density: technical, readable, restrained. Avoid large decorative dashboards and fake metrics.
- Type: plain sans for labels; monospace for data and code.
- Evidence states: **verified**, **unverified**, **not evaluated**, **excluded**. Unknown does not equal safe.
- Public claims must reference code, fixtures, workflow runs or documented source data.

## Integration contract (proposed, not implemented)

A future Leviathan X Tools API can adapt standalone tool outputs to an immutable, evidence-backed observation envelope.

```json
{
  "schema_version": "1.0",
  "tool": "fenrir",
  "asset_id": "authorized-asset-id",
  "observation_type": "component_advisory_candidate",
  "observed_at": "ISO-8601 UTC timestamp",
  "source": {
    "provider": "tool_or_permitted_feed",
    "reference": "source reference or null"
  },
  "evidence": {
    "detected_version": "1.2.3",
    "advisory_id": "example-id",
    "range": "source-defined"
  },
  "coverage": {
    "evaluated": true,
    "not_evaluated_reason": null
  },
  "status": "candidate"
}
```

The payload is an **interface example**, not a real finding. No automated network scanning, cross-repository tool invocation, webhook ingestion or customer API is claimed to exist from this document.

## Repository hygiene

- Keep the three flagship tools public and individually installable.
- Keep [homebrew-tap](https://github.com/cyeezy08/homebrew-tap) as a distribution repository, not a fourth scanner.
- Keep AI benchmark and model experiments separate from the Leviathan X security product identity.
- Do not force unrelated projects into a single monorepo or delete/privatize repositories without a deliberate migration.
- Preserve release names and import paths until compatible packages and upgrade paths are tested.

## Proposed GitHub profile pins

**1. FenrirLVX  2. HostageLVX  3. surfacediff**

Those three give reviewers a coherent evidence-first story. The remaining profile slots can demonstrate independent systems engineering only if the repositories are maintained and have verified tests. GitHub pins require a separate profile action; a Markdown recommendation does not change them.

## Collaboration

For platform design-partner conversations, contact **admin@leviathanx.org**. A separate partnership brief is being reviewed and is not yet part of the published profile.

This page describes the public tooling strategy. It does not assert production deployment, approved provider partnerships, or commercial availability.
