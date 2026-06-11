# Changelog

All notable changes to the Open-Pact License are documented in this file. The format is based on [Keep a Changelog](https://keepachangelog.com/), and this project adheres to [Semantic Versioning](https://semver.org/) for license revisions.

## [1.2] - 2026-06-11 — "Open work, get paid if it grows."

**Status:** Recommended. This is the current version of the Open-Pact License.

### Added
- **Minimal, opt-in design.** A single Hosted-Service restriction, default-on Reciprocity, default-on AI training restriction (via OPL-AI addendum), and a no-stripping clause. The four-tier prescriptive structure of v1.1 is replaced by a single condition set with Maintainer-customizable defaults.
- **OPL-AI addendum** (`OPL-AI.md`). The AI training restriction is moved into a companion document that can be layered onto OPL-1.2 or any other license. Maintainers may opt out with a single line in `NOTICE`.
- **Reciprocity waiver fallback** (§3.4). If the Maintainer is unreachable for 90 days after a written request, Reciprocity is permanently waived for that Derivative. Downstream users are not trapped by an unresponsive Maintainer.
- **Small-scale carve-out** for the Hosted Service restriction (§3.3). Services under USD $5,000 in direct annual compensation, or under 10,000 monthly active users, are exempt. Maintainer can override in `NOTICE`.
- **Trademark clause** (§10). Standard, prevents derivative work from implying Maintainer endorsement or trademark misuse.
- **No-endorsement clause** (§11). Standard, prevents use of Maintainer or Contributor names to promote derivatives without permission.
- **Governing law and forum** (§12). Specifies the Maintainer's jurisdiction as default, allows explicit override in `NOTICE`.
- **30-day cure period** for abandonment (§5). A Maintainer has 30 days to file a verified counter-notice before conversion to Apache 2.0 takes effect.
- **Counter-notice verification** (§5). The counter-notice contact is verified by a test message within 7 days; an unreachable contact invalidates the counter-notice.
- **SPI (Software in the Public Interest, Inc.)** designated as the default fiscal sponsor for the abandonment procedure (§5).
- **§3.3 carve-out for affiliated groups** under common control (tax-law-aligned definition).
- **§6 patent grant narrowed** to "the Work as contributed by that Contributor." Third-party modifications are not covered.
- **§9.3 four-part clarification constraint** with a 30-day public-comment period. Clarifications cannot impose new restrictions, cannot expand existing ones, are not retroactive, and require public notice.

### Changed
- **Terminology:** "License Steward" → "Maintainer" throughout. "Designated Successor" formalized in §1.
- **Patent retaliation clause** retained; cure period not added (consistent with Apache 2.0 practice).
- **Reciprocity default** is now on-by-default at 5%, with explicit Maintainer override or waiver available in `NOTICE`.

### Removed
- The four-tier prescriptive structure (Personal / Commercial / AI Training / Reciprocity) is replaced by a single condition set.
- The "Total Workforce" definition (which had no judicial precedent) is removed.
- Guild model, Custodial Steward, and Beneficiary role are removed. Succession is a NOTICE-file update.
- On-chain registry, smart-contract enforcement, and tokenized mechanisms are removed from the license text. They are available as optional infrastructure in the `Open-Pact-Standard/framework` repository.
- OPL-SaaS 1.0 companion license is no longer required. The Hosted Service restriction in §3.3 covers SaaS directly.
- The Trademark clause, no-endorsement clause, and choice-of-forum are explicit and standard; they were implicit or absent in v1.1.

### Preserved (with provenance)
- All 10 rounds of adversarial stress testing documented in `ROUND10_ANALYSIS.md` apply to v1.1. The vulnerability findings remain valid for v1.1; the v1.2 design explicitly addresses the critical issues identified.

## [1.1] - 2026-04-05 — Soft Launch

**Status:** **DEPRECATED.** Superseded by OPL-1.2. Preserved at `LICENSE-OPL-1.1.md` for existing adopters. No further changes will be made to v1.1.

### Summary
The first public release of the Open-Pact License. A four-tier source-available framework (Personal / Commercial / AI Training / Reciprocity) designed to protect small developers from corporate extraction of their OSS work, particularly from cloud-wrapping and AI training.

### Structural
- License Steward pattern.
- Definitions of "Functionally Equivalent Work" and "Total Workforce."
- Project Registry for fee publication.
- Stewardship Sunset: 36 months of unresponsiveness → Apache 2.0.

### Enforcement
- Canary Token integration.
- Binding arbitration under the New York Convention for entities over $1M revenue.
- Disgorgement damages and whistleblower protections.

### Dependencies
- Separation of license from project.
- Prohibition of Shadow Dependencies.
- Anti-poisoning clause.

### Governance
- Steward removal rules.
- Guild membership.
- Copyright survival.

### Testing
- 7 rounds of adversarial stress testing.
- 48 patches applied.

### Notes for v1.1 adopters
You may continue to use OPL-1.1 indefinitely. There is no forced migration. The new OPL-1.2 is recommended for new projects and for existing v1.1 projects where the Maintainer is willing to migrate. Migration is a single PR (replace `LICENSE.md` with the v1.2 text; update `NOTICE` per v1.2 §13). Existing v1.1 adopters do not need to take any action.
