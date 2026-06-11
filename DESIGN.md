# Open-Pact License: Design Evolution (v1.2 → v1.3 → v1.3.1)

> **Purpose:** This document preserves the *rationale* behind the design decisions that produced OPL-1.3.1. The license text lives in [`LICENSE.md`](LICENSE.md) and the release notes in [`CHANGELOG.md`](CHANGELOG.md). This file explains *why* the design evolved the way it did, so a future reviewer of a hypothetical OPL-1.4 understands the constraints the current design is operating under.

## At a glance

| Version | Date | Headline | Status |
|---|---|---|---|
| v1.1 | 2026-04-05 | Soft launch: License Steward, Reciprocity, Canary Token, Guild | Superseded |
| **v1.2** | (proposed; never merged) | Reciprocity + Hosted Service restriction, OPL-AI opt-out default | **Superseded before merge** |
| **v1.3** | 2026-06-11 | Polyform Mixed: free Personal Use, paid Commercial Use per Standard Terms | Active base |
| **v1.3.1** | 2026-06-11 | 3 clarifications on top of v1.3 (Standard Terms URL 7-criteria, §3.7 wind-down, OPL-AI canonical syntax) | Active |

## The v1.2 design (Reciprocity model)

**Headline:** *A Reciprocity-based fair-source license.*

The v1.2 design (drafted in PR #2) used a **Reciprocity** mechanism as its core commercial-use gate:

- **§3.3 — Hosted Service restriction.** Operating a Hosted Service derived from the Work *and* receiving direct compensation triggered a 5% of net revenue obligation.
- **§3.4 — Reciprocity mechanism.** Default 5% of Revenue on distributed Derivatives, with a 90-day written-request waiver if the Maintainer was unresponsive.
- **§3.5 — OPL-AI opt-out (default-on).** OPL-AI addendum incorporated by default; the Maintainer had to opt out via `NOTICE`.
- **§5 — Abandonment.** 24 months of Maintainer unresponsiveness, with a 30-day cure window, a counter-notice process, and a SPI fiscal-sponsor step.
- **§13 — NOTICE shape.** Required the Reciprocity rate, a Payment Address, and the AI opt-in.
- **OPL-Standard framework.** License + framework: a registry, smart contracts, a Guild, and a Custodial Steward. The framework processed payments and took a cut.

The v1.2 design closed the gap that open-source licensing cannot enforce commercial-use terms by tying the obligation to *revenue*, not *use*. A small developer who made a side project could ship under v1.2 and never trigger the 5% obligation; a large SaaS company that built a hosted product from a v1.2 Work would owe 5% of net revenue to the Maintainer.

The design was the foundation of the project for ~2 months. PR #2 was opened and reviewed.

## The course correction: why Reciprocity → Polyform Mixed

**Headline:** *The Reciprocity default was the wrong level of abstraction.*

During v1.2 review, the founder identified that a hardcoded 5% Reciprocity default is the wrong level of abstraction for a license that aims to span calculators to neural networks:

1. **Heterogeneous commercial value.** A calculator script and a foundation model do not have the same commercial value. A 5% rate that makes sense for a calculator generates millions for a foundation-model Maintainer; a 5% rate that works for a foundation model is ruinous for an indie developer who is trying to keep a side project alive. The license was conflating *enforceability* with *fairness*: a single rate cannot be both.

2. **Maintainer agency.** The Reciprocity mechanism had the *license* setting the commercial term, when the right place for the commercial term is the *Maintainer–user negotiation*. The Maintainer knows the value of the Work, the market for it, and the right price; the license author (working upstream of any specific Work) does not.

3. **Framework dependency.** The Reciprocity mechanism required the OPL-Standard framework — a registry, smart contracts, a Custodial Steward — to process payments. This added a *gatekeeper* between the Maintainer and the user, which is exactly the kind of dependency the v1.1 era had been trying to escape. The framework could charge fees, take a cut, or go down; all three were unacceptable.

4. **Per-work pricing vs. universal pricing.** The Polyform Mixed model lets a Maintainer publish *zero* pricing (free Commercial Use, sponsorship-only), *tiered* pricing (ARR bands), *flat* pricing ($/month), or *negotiated* pricing (contact email). The Reciprocity model forced all Maintainers into the same 5% shape.

The course correction was intentional and total: the v1.3 PR replaced the Reciprocity mechanism with the Polyform Mixed model, removed the framework dependency, simplified abandonment, and flipped the OPL-AI default to opt-in. v1.2 was closed in favor of v1.3.1; the v1.2 work is preserved in the [`release/v1.2`](https://github.com/Open-Pact-Standard/license/tree/release/v1.2) branch for historical reference.

## The v1.3 design (Polyform Mixed)

**Headline:** *Free for personal use. Paid for commercial use. The Maintainer decides how.*

The v1.3 design (merged in PR #3) replaces the Reciprocity mechanism with a **Polyform Mixed** default:

- **§3.3 — Commercial Use requires Standard Terms payment.** Personal Use is free; Commercial Use requires payment to the Maintainer per the Standard Terms published at the URL declared in `NOTICE`. The Maintainer chooses the payment mechanism. Default when `NOTICE` is silent: Commercial Use is not permitted, with a 30-day cure window for the Maintainer to fix a blank or unresolving URL.
- **§3.4 — Reciprocity removed (reserved).** The Reciprocity mechanism is removed. The section is reserved for future use.
- **§3.5 — OPL-AI opt-in (default-off).** The OPL-AI addendum is *not* incorporated by default. The Maintainer must affirmatively opt in via `NOTICE`. This is a **default flip** from OPL-AI v1.0 (which was incorporated by default; opt-out was required).
- **§3.6 — Functional Equivalent.** Triggered by Commercial Use context (not Reciprocity context), integrated with §3.3.
- **§5 — Abandonment.** Simplified: 36 months of Maintainer unresponsiveness (range 12–60, default 36) **automatically** converts the Work to **Apache License 2.0**. No third-party authorization, no fiscal sponsor, no counter-notice process, no public-notice requirement.
- **§13 — NOTICE shape.** Replaces the v1.2 Reciprocity fields with: **OPL Version**, **Maintainer**, **Governing Jurisdiction**, **Standard Terms URL** (required for Commercial Use), **OPL-AI opt-in/opt-out**, optional **Abandonment period** and **Trademark notice**.
- **OPL-Standard role.** License + free open-source tools (smart-contract templates, payment integrations). No payment processing, no fees, no framework. The Maintainer is the steward.

The full v1.2 → v1.3 comparison table is at the bottom of [`LICENSE.md`](LICENSE.md). The CHANGELOG entry for v1.3 is in [`CHANGELOG.md`](CHANGELOG.md).

## The v1.3.1 design (3 clarifications)

**Headline:** *No substantive changes from v1.3. Three open ambiguities resolved.*

v1.3.1 (merged in PR #4) is a clarification release on top of v1.3. The substance of v1.3 is preserved; only 3 open design questions (ODQs) from the v1.3 PR checklist are resolved.

### Patch 1: Standard Terms URL validity (LICENSE §3.3)

**Problem in v1.3.** A “Valid Standard Terms URL” was defined in v1.3 with 4 criteria (HTTPS, 2xx response, HTML, no authentication). This was under-specified: a URL that returns a 1-line “Pay me $1M” page, a URL that 302-redirects off the Maintainer’s domain, and a URL that requires JavaScript to render all satisfy the 4 criteria but are clearly broken in spirit.

**Resolution in v1.3.1.** The criteria are expanded to **7 criteria**:

1. **HTTPS scheme** (no plaintext).
2. **Returns 2xx** after following redirects within the Maintainer’s domain.
3. **HTML webpage** (not PDF, not plain text, not image).
4. **Human-readable in a major browser without authentication** (no login, no paywall, no IP gating, no cookie gating beyond a standard consent banner).
5. **Not behind JavaScript-only rendering** (the Standard Terms must be in the HTML source, visible with JavaScript disabled).
6. **Reasonably stable** (a persistent URL on a domain the Maintainer controls, not a transient post or one-time link).
7. **Substantive content** (publishes the commercial-use pricing, payment mechanism, and scope of permitted Commercial Use in clear human-readable language).

A **rebuttable-presumption** rule with burden allocation applies in disputes: the User bears the initial burden of showing the URL failed a criterion; the Maintainer bears the burden of showing the URL satisfied the criteria at the time of access. This is a fair allocation: the User is the one with access to the URL as it was at the time of their use, and the Maintainer is the one who controls the URL’s state.

### Patch 2: Wind-down of Commercial Use (LICENSE §3.7, new)

**Problem in v1.3.** §3.3 specified a 90-day *grace period* for existing commercial users if the Standard Terms URL becomes invalid, but did not address the more general case where the Maintainer *intentionally* revokes Commercial Use or *materially* changes the Standard Terms. The 90-day grace period for an invalid URL is a one-time transition; a Maintainer who wanted to revoke Commercial Use had no obligation to give existing users any wind-down time.

**Resolution in v1.3.1.** A new **§3.7** (6 sub-sections) is added:

- **Triggers:** revocation of Commercial Use, or material change to the Standard Terms.
- **90-day wind-down period** for existing commercial users.
- **Who is an “existing commercial user”** — defined by the date the URL was last Valid and the User had a paid relationship.
- **What the wind-down does NOT cover** — new users are bound by the new Standard Terms; the wind-down only applies to users who were in good standing at the time of the change.
- **Maintainer unreachable during wind-down** — if the Maintainer becomes unreachable *during* the wind-down, the wind-down still applies; the §5 abandonment clock runs in parallel.
- **Cure of an invalid URL** — distinct from a wind-down: a Maintainer who lets the URL lapse can cure within 30 days without triggering the wind-down clock.

The §5 abandonment clock and the §3.7 wind-down clock **run in parallel**. The old “§3.7 Reserved” is renumbered to §3.8.

### Patch 3: OPL-AI opt-in syntax (OPL-AI §8.1–§8.3, new)

**Problem in v1.3.** The §3.5 opt-in was described as “the Maintainer must affirmatively opt in via `NOTICE`”, but did not specify a canonical syntax. Without a canonical syntax, a parser reading a `NOTICE` file has to guess whether `OPL-AI: opted in.`, `OPL-AI: opted in`, `OPL-AI: OPTED IN.`, `OPL-AI:opt-in.`, `Opl-Ai: opted in.`, etc. all mean the same thing.

**Resolution in v1.3.1.** A canonical syntax with 6 parsing rules:

1. **Case-sensitive prefix:** the prefix `OPL-AI:` is case-sensitive (must be uppercase).
2. **Case-insensitive value:** the value `opted in.` / `opted out.` is case-insensitive (`OPTED IN.`, `Opted In.`, `opted IN.` all work).
3. **Whitespace-tolerant:** any amount of whitespace between the prefix and the value is allowed.
4. **Trailing text ignored:** anything after the value (e.g., `opted in. AI training is restricted.`) is treated as human-readable commentary.
5. **Commented lines treated as absent:** lines beginning with `#` are comments and ignored.
6. **Last uncommented occurrence wins:** if multiple uncommented `OPL-AI:` lines exist, the last one is authoritative.

A **versioning rule** is added: the version reference (e.g., `OPL-AI: opted in. (v1.3.1)`) is documentation only; the parser uses the version of the OPL-AI addendum bundled with the Work. This avoids the chicken-and-egg of needing to fetch the latest OPL-AI version to know whether the declaration is valid.

**16+ examples** in the OPL-AI v1.3.1 addendum cover 5 valid opt-in, 3 valid opt-out, 6 invalid, and 2 commented-as-absent cases.

## What v1.3.1 preserves from v1.3

The substance of v1.3 is preserved. The Polyform Mixed default, the §3.5 OPL-AI opt-in, the §3.6 Functional Equivalent test, §5 abandonment, and §13 NOTICE shape are all unchanged. The 3 patches in v1.3.1 are *clarifications*, not *changes*; they resolve ambiguities that existed in the v1.3 text without altering the substantive license obligations.

## The v1.2 historical reference

The v1.2 design is preserved in the [`release/v1.2`](https://github.com/Open-Pact-Standard/license/tree/release/v1.2) branch for historical reference. The v1.2 PR (#2) was closed in favor of the v1.3.1 work; the [closing comment](https://github.com/Open-Pact-Standard/license/pull/2#issuecomment-4682881009) explains the course correction in detail.

## Open design questions for v1.4

Three design questions remain open and may be addressed in v1.4:

- **Reciprocity reservation (§3.4).** The Reciprocity mechanism is *removed* from v1.3.1, but the section is *reserved* for future use. Whether to leave it reserved, repurpose it (e.g., for a Maintainer-level Reciprocity default), or remove the reservation entirely is an open question.
- **OPL-AI v2.0.** The OPL-AI v1.3.1 addendum is a clarification of v1.0/v1.3 syntax. Substantive changes to the AI training restrictions (e.g., covering inference, retrieval-augmented generation, model distillation) are deferred to OPL-AI v2.0.
- **Standard Terms URL stability (§3.3 criterion (f)).** The 7-criterion test says a URL must be “reasonably stable” but does not quantify the stability period. v1.4 may add a specific timeframe (e.g., “stable for at least 12 months after first declaration”) and a procedure for change-of-URL that does not require re-validation.

## See also

- [`LICENSE.md`](LICENSE.md) — the v1.3.1 license text (includes a v1.2 → v1.3 comparison table)
- [`OPL-AI.md`](OPL-AI.md) — the v1.3.1 AI training addendum
- [`CHANGELOG.md`](CHANGELOG.md) — release notes for v1.1, v1.3, and v1.3.1
- [`NOTICE.example`](NOTICE.example) — template for the required `NOTICE` file
- [`README.md`](README.md) — Quick start
- [PR #2 (v1.2, closed)](https://github.com/Open-Pact-Standard/license/pull/2) — the v1.2 design, closed in favor of v1.3.1
- [PR #3 (v1.3, merged)](https://github.com/Open-Pact-Standard/license/pull/3) — the v1.3 design
- [PR #4 (v1.3.1, merged)](https://github.com/Open-Pact-Standard/license/pull/4) — the v1.3.1 design
- [`release/v1.2` branch](https://github.com/Open-Pact-Standard/license/tree/release/v1.2) — v1.2 historical reference
