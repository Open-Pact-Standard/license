# Changelog

All notable changes to the Open-Pact License will be documented in this file.

The format is based on [Keep a Changelog](https://keepachangelog.com/en/1.0.0/),
and this project adheres to [Semantic Versioning](https://semver.org/spec/v2.0.0.html).

## [1.4.3] - 2026-08-18 (Published)

OPL-1.4.3 is the first **published** release of the OPL-1.4 series. It supersedes
v1.3.1 and carries the same `OPL-1.4` SPDX identifier. v1.4.3 incorporates the
complete legal-skills-review pass (ambiguity stress-test + 5-clause risk scan +
regional discrepancy scan) on top of the v1.4 major revision.

The v1.4 series (v1.4 → v1.4.1 → v1.4.2 → v1.4.3) is a **substantive,
adoption-focused revision** of OPL from the published v1.3.1:

### Changed (v1.4 vs v1.3.1)
- **§5.1 Version-Based DOSP (new, opt-in).** A Maintainer may declare a DOSP
  period in `NOTICE`, after which each Version's source converts to Apache
  License 2.0 on a scheduled date (recommended 24-60 months). Silent `NOTICE` =
  no scheduled conversion. Aligns with the Fair Source movement's DOSP
  expectation *for adopters who opt in* while preserving creator autonomy.
- **§3.6 Functional Equivalent — REMOVED.** The functional-equivalence
  restriction (and clean-room-rewrite coverage) was deleted. Removes the "code
  taint" anxiety that discouraged adoption. Actual copying remains protected by
  copyright law.
- **§13 NOTICE shape (extended).** Added two optional fields: **DOSP period**
  (enables §5.1) and **Commercial Terms file** (a per-Version immutable
  `COMMERCIAL_TERMS.md` pinning pricing/payment/scope).
- **§5 abandonment — robust.** Replaced the vague "converts to Apache-2.0" with
  an explicit **standing conditional grant** effective automatically on
  abandonment (no actor, successor, or registry required); added an optional,
  strictly-bounded Designated Successor who may *record* the conversion but holds
  no other power.
- **SPDX identifier** bumped to `OPL-1.4`.

### Notes
- v1.4.1 / v1.4.2 / v1.4.3 are successive tightening passes; no rights or
  obligations were added beyond the v1.4 revision. Keeping the `OPL-1.4` SPDX
  identifier stable across them.

## [1.3.1] - 2026-06-11 (Published)

OPL-1.3.1 is a clarification release on top of OPL-1.3. The substance of v1.3 is preserved; only the 3 open design questions (ODQs) from the v1.3 PR (#3) checklist are resolved.

### Changed

- **Standard Terms URL validity (LICENSE \u00a73.3).** Expanded from 4 criteria to **7 criteria**: HTTPS, redirect-following, HTML, no-authentication, no-JavaScript-only rendering, reasonable stability, and substantive content. Added a **rebuttable-presumption** rule with burden allocation: User bears the initial burden of showing the URL failed a criterion; Maintainer bears the burden of showing the URL satisfied the criteria at the time of access.
- **Wind-down of Commercial Use (LICENSE \u00a73.7, new).** Added a new section with 6 sub-sections covering: triggers (revocation or material change), 90-day wind-down period, who is an "existing commercial user", what the wind-down does NOT cover, Maintainer unreachable during wind-down, and cure of an invalid URL. The \u00a75 abandonment clock and the \u00a73.7 wind-down clock **run in parallel**. Old "\u00a73.7 Reserved" renumbered to \u00a73.8.
- **OPL-AI opt-in syntax (OPL-AI \u00a78.1\u2013\u00a78.3, new).** Added a **canonical syntax** for the opt-in/opt-out declaration with 6 parsing rules (case-sensitive prefix, case-insensitive value, whitespace-tolerant, trailing text ignored, commented lines treated as absent, last uncommented occurrence wins), a versioning rule (version reference is documentation only), and 16+ examples (5 valid opt-in, 3 valid opt-out, 6 invalid, 2 commented-as-absent).

### Notes

- v1.3.1 is a clarification release; no substantive changes from v1.3. PR #4 carries the patches on top of release/v1.3.

## [1.3] - 2026-06-11 (Draft)

OPL-1.3 is a major redesign of the Open-Pact License. It supersedes OPL-1.2 (PR #2) and the OPL-1.1 series. The redesign replaces the v1.2 Reciprocity mechanism with a **Polyform Mixed** model: free Personal Use, paid Commercial Use per the Maintainer\u2019s published Standard Terms URL.

### Changed

- **Commercial Use requires Standard Terms payment (LICENSE \u00a73.3, new mechanism).** Replaces the v1.2 Hosted Service restriction with a **Polyform Mixed** default: Personal Use is free; Commercial Use requires payment to the Maintainer per the Standard Terms published at the URL declared in `NOTICE`. The Maintainer chooses the payment mechanism. Default when `NOTICE` is silent: Commercial Use is not permitted (with a 30-day cure window). 90-day grace period for existing commercial users if the URL becomes invalid.
- **Reciprocity removed (LICENSE \u00a73.4, reserved).** The v1.2 5% Reciprocity mechanism is removed. Payment for Commercial Use is now a per-work commercial term set via Standard Terms, not a License mechanism. This section is reserved for future use.
- **OPL-AI opt-in (LICENSE \u00a73.5).** The OPL-AI addendum is **not** incorporated by default. The Maintainer must affirmatively opt in via `NOTICE` (e.g., `OPL-AI: opted in.`). This is a **default flip** from OPL-AI v1.0 (which was incorporated by default; opt-out was required). The OPL-AI v1.3 substance (\u00a72\u2013\u00a77) is unchanged from v1.0.
- **Functional Equivalent (LICENSE \u00a73.6).** Triggered by **Commercial Use** context (not Reciprocity context). Integrated with \u00a73.3 via the Hosted Service restriction.
- **Abandonment (LICENSE \u00a75).** Simplified from v1.2: **36 months** of Maintainer unresponsiveness (range 12\u201360, default 36) **automatically** converts the Work to **Apache License 2.0**. No third-party authorization, no fiscal sponsor, no counter-notice process, no public-notice requirement.
- **NOTICE shape (LICENSE \u00a713).** Replaces the v1.2 Reciprocity fields with: **OPL Version** (required), **Maintainer** (required), **Governing Jurisdiction** (required), **Standard Terms URL** (required for Commercial Use), **OPL-AI opt-in/opt-out** (required), **Abandonment period** (optional, 12\u201360 months), **Trademark notice** (optional).
- **Standard Terms change notice.** 90 days\u2019 notice required for existing commercial users when the Maintainer changes the Standard Terms (URL or content).
- **Removed entirely:** OPL-Standard framework references (registry, smart contracts, fiscal sponsor, Guild, Custodial Steward). OPL-Standard does not act as steward; the Maintainer is the steward. OPL-Standard provides free open-source example tools (smart-contract templates, payment integrations) but does not process payments or take a cut.

### Removed

- **\u00a73.4 Reciprocity mechanism (v1.2).** The 5%-of-Revenue Reciprocity + 90-day written-request waiver is removed.
- **\u00a73.3 small-scale carve-out (v1.2).** The built-in $5K/yr or 10K MAU threshold is removed; Maintainer sets any threshold in Standard Terms.
- **OPL-Standard framework dependency.** No registry, no smart contracts, no on-chain fee collection, no Guild, no Custodial Steward. None required by this license.

### Notes

- The v1.3 PR (#3) was opened as a draft on `release/v1.3` targeting `main`. v1.3.1 (PR #4) layers 3 patches on top of v1.3. Both PRs were published as v1.3.1 on 2026-06-11.

## [1.1] - 2026-04-05 (Soft Launch)

### Structural
- License Steward pattern introduced; Functionally Equivalent Work definition added.
- Total Workforce metric defined for Reciprocity calculation.
- Project Registry-based fees and royalties operationalized.

### Enforcement
- Canary Token Enforcement: unique identifiers embedded in source, discovery in published models = evidence of restricted use.
- Binding Arbitration: parties consent to binding arbitration for disputes.
- Disgorgement damages available for willful infringement.
- Whistleblower provisions: third parties may report suspected AI-training violations.

### Dependencies (Section 18)
- Separation of licenses: each dependency has its own license; OPL does not impose a single license on the dependency graph.
- Shadow Dependency Prohibition: Maintainers must disclose all material dependencies.
- Anti-Poisoning clause: dependencies must not contain malicious code targeting the OPL ecosystem.
- Good Faith Declaration: parties must act in good faith when interpreting ambiguous terms.

### Governance
- Steward Removal: a Steward may be removed by 2/3 vote of active Maintainers.
- Guild Membership rights: any Contributor to an OPL Work is a Guild Member with voting rights on Guild matters.
- Human-only voting: AI Systems may not vote in Guild matters.
- Copyright survival: copyright in the Work survives termination of the license.

### Adversarial Testing
- 7 rounds of automated stress testing performed.
- 48 patches applied in response to adversarial findings.
- See `FINAL_REPORT.md` for the full audit trail.

[Unreleased]: https://github.com/Open-Pact-Standard/license/compare/v1.3.1...HEAD
[1.3.1]: https://github.com/Open-Pact-Standard/license/pull/4
[1.3]: https://github.com/Open-Pact-Standard/license/pull/3
