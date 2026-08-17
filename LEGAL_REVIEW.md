# OPL v1.4.2 — Legal-Skills Review (real-adopter red-team)

*Reviewer: Hermes, applying ported legal skills as drafting/validation aids.*
*Method: `ambiguity-stress-test` (contract profile) + `contract-risk-analyzer`
(5-clause lens). Document read on its four corners; no external case-law research
(OPL is a private license instrument, not a statute). Outcomes predicted on a
US interpretive frame; the reference adoption (origin-canary) now declares
**United States** (maintainer is US-based), and OPL remains a template license
so any adopter declares their own jurisdiction in NOTICE — German
doctrine would differ, noted where material.*

*This is analysis, not legal advice. The adopter (Ikaros Digital LLC) should
still obtain qualified counsel before any high-exposure commercial deployment.*

---

## PART A — Ambiguity Stress-Test (contract profile)

Scanned against the six universal families + the contract "characterization
conflict" family. Newest clauses (§5 standing grant, §4.4 optional successor)
re-tested specifically.

### Scenario 1 — "Standard Terms as incorporated-by-reference, current-at-access"
**Anchors:** §1 "Standard Terms" def; §3.3 (changes, 90-day notice); §3.7.1(b).
**Family:** C (definitional boundary) + D (standardless discretion).
**Narrative:** A User integrated origin-canary commercially in 2025 under Standard
Terms pricing EUR 49/mo. In 2026 the Maintainer changes the URL content to EUR
499/mo and asserts the new user rate applies to *all* users "as they exist at
time of access." The User points to §3.7.1(b): a >100% increase triggers the
90-day wind-down, so the old rate holds for 90 days. The Maintainer points to
§1: "The License incorporates the Standard Terms as they exist at the URL at the
time of access by the user (i.e., the *current* Standard Terms)." Both cite real
text. **Likely outcome:** harmonization + implied covenant of good faith
favors the User — §3.7.1(b) is the *specific* provision controlling rate changes
and explicitly contemplates >100% increases as wind-down triggers, so it governs
over the general "current terms at access" language. But the tension is real and
admissible. **Redraft:** in §1, qualify "current Standard Terms" with "subject
to the wind-down protections in §3.7 for existing commercial users." Closes the
characterization conflict.
**Severity:** 🟡 Medium (internal tension, not a void; resolves against drafter
via specific-governs-general, but a German court might read §1 literally).

### Scenario 2 — "Conclusive evidence" vs "not a precondition" (the successor seam)
**Anchors:** §5 optional successor; §1 "Designated Successor" def.
**Family:** A (internal contradiction) / F (cross-clause).
**Narrative:** Maintainer vanishes; a named Successor publishes an Apache-2.0
LICENSE. A downstream adopter later relies on that recorded LICENSE. Separately,
a skeptic argues the "standing grant" already applied on day 1 of abandonment,
so the Successor's recording is mere evidence. The text says the recording is
"conclusive evidence" but "not a precondition" and the grant "holds regardless."
**Likely outcome:** no genuine contradiction — the two sentences are drafted to
reconcile, and they do. The "conclusive evidence" language slightly
over-weights the recording but "regardless" governs. Low litigation risk.
**Severity:** 🟢 Low (we already stress-tested this in v1.4.2; holds up).
**Note:** §1 defines "Designated Successor" as requiring "a signed statement
from the prior Maintainer," but §5/§4.4 say it's named "in NOTICE." Minor
internal mismatch in *how* a successor is established (signed statement vs NOTICE
entry). **Redraft:** align §1 to "identified in NOTICE by the prior Maintainer"
to match §4.4/§5. (Cosmetic but a real cross-clause inconsistency.)

### Scenario 3 — "Reachable" is undefined (the known soft term)
**Anchors:** §4.1; §5 trigger ("no Maintainer is reachable at the contact").
**Family:** B (vague operative term).
**Narrative:** Maintainer's NOTICE email bounces; User claims abandonment started.
Maintainer says they responded via a GitHub issue comment (same project). Is a
project comment "reachable at the contact published in NOTICE"? "Reachable" has
no definition and no measurement baseline. **Likely outcome:** contra
proferentem (construed against drafter, since OPL is adhesive to users) + the
implied duty of good faith push toward a reasonable-contact standard; a bouncing
listed email with no alternative response is likely "unreachable." But genuinely
contestable. **Redraft:** define "reachable" as "the contact in NOTICE returns a
human response within the §4.2 60-day window." Closes the gap.
**Severity:** 🟡 Medium (this is the single biggest abandonment-trigger ambiguity;
worth fixing even though OPL is adhesive).

### Scenario 4 — Hosted Service "primary functionality" boundary
**Anchors:** §1 "Hosted Service" def; §3.3 integration clause.
**Family:** C (definitional boundary).
**Narrative:** A SaaS embeds origin-canary as a *minor* forensic feature inside a
much larger product. Is the product's "primary functionality ... the Work or a
Derivative"? Arguably in (it offers the Work as a hosted service) and arguably
out (the Work is incidental). **Likely outcome:** the definition says "whose
primary functionality IS the Work" — a minor feature is likely OUT, so Personal
Use + no payment. But a Maintainer could argue any hosted offering of the Work
counts. Contestable. **Redraft:** add "a Hosted Service that offers the Work or
a Derivative as a distinct, separately-marketed capability," narrowing "primary
functionality" so incidental embedding is clearly Personal Use.
**Severity:** 🟡 Medium (commercial-revenue-bearing ambiguity).

### Scenario 5 — "Derivative" + §3.2 light copyleft interaction
**Anchors:** §1 "Derivative"; §3.2.
**Family:** C + F.
**Narrative:** User creates a Derivative but relicenses it under MIT, keeping §3.3
payment protection "applied to the protections themselves" (§3.2). A second party
takes the MIT Derivative and strips the §3.3 payment. §3.2 says you "may not
distribute ... under terms that remove ... §3.3." Does the MIT relicensee violate
§3.2 by distributing freely? **Likely outcome:** §3.2 binds the *first*
Distributor (who relicensed under MIT but promised to keep §3.3 applied to the
protections). The downstream party who strips §3.3 likely breaches §3.2
construed against them. But "applied to the protections themselves" is
metaphysical — it's unclear what a court enforces. **Redraft:** state plainly
that a Derivative distributed under other terms must still require payment for
Commercial Use per §3.3 (the protection travels with the Work).
**Severity:** 🟡 Medium (the "light copyleft propagates protections not code"
metaphor is elegant but legally under-specified).

### Scenario 6 — DOSP "first public release date" for a pre-existing version
**Anchors:** §5.1 (Version, first public release date).
**Family:** E (gap/silence) — already partially closed in v1.4.1.
**Narrative:** Maintainer adopts OPL in 2026 but a Version was first released in
2024 (before OPL). When does the DOSP clock start? The definition says "first
made available to the public" — which could be 2024 (already past) or 2026 (OPL
adoption). **Likely outcome:** the definition is forward-looking by context
(OPL can't convert a version released before OPL existed on a schedule it didn't
declare), but the text doesn't say so. **Redraft:** "first public release date
on or after the OPL adoption date declared in NOTICE." Closes the gap.
**Severity:** 🟢 Low (v1.4.1 tightened this; residual ambiguity is minor).

---

## PART B — 5-Clause Risk Lens (`contract-risk-analyzer`)

| Clause | OPL posture | Risk | Note |
|---|---|---|---|
| **Limitation of Liability** | §7 Disclaimer + §8 Limitation (AS-IS, no liability). One-sided *in the Maintainer's favor* — users get no recourse. | 🟢 Low for adopter (you're the Maintainer); 🔴 for downstream commercial users (no liability cap protects them, but they also pay you). Adhesive but standard for OSS/fair-source. | Acceptable; mirrors Apache-2.0 posture. |
| **Indemnities** | None provided either way. | 🟢 Low. No mutual indemnity; the "no indemnity" row in the Kit is accurate. | Fine. |
| **IP Ownership** | §2 grants; §3.2 light copyleft; patent grant §6. | 🟡 Medium. The "Derivative may be relicensed ... as long as protections continue to apply" (§3.2) is the soft spot — see Scenario 5. Maintainer retains copyright; users get a license, not ownership. Clean for the adopter. | Tighten §3.2 per Scenario 5. |
| **Data Protection** | N/A — OPL governs software licensing, not data processing. origin-canary itself collects no data (verified offline). | 🟢 Low. The license correctly says nothing about data; a separate DPA would only arise if a Maintainer's Standard Terms collected user data (yours at ikaros.dev/terms might). | Out of scope of OPL; flag for your Standard Terms, not the license. |
| **Termination** | §3.7 wind-down (90-day, automatic, not extendable by Maintainer); §5 abandonment. | 🟢 Low for users (strong wind-down + auto-Apache escape). 🟢 for Maintainer (you control Commercial Use termination via §3.7.1). | This is OPL's *strongest* clause set — genuinely adopter-and-user friendly. |

---

## PART C — Coverage report (what the scan surfaced)

Defect-dense areas: **§3.3/§1 Standard Terms incorporation** (Scenarios 1),
**§5 successor mechanics** (Scenario 2 — minor §1/§5 mismatch), **§4.1 "reachable"**
(Scenario 3), **§1 Hosted Service** (Scenario 4), **§3.2 Derivative copyleft**
(Scenario 5), **§5.1 DOSP clock** (Scenario 6).

Cross-clause tensions found: §1 "current Standard Terms" vs §3.7 wind-down
(Scenario 1); §1 "signed statement" successor vs §4.4/§5 "in NOTICE" (Scenario 2).

No validity/ enforceability opinion rendered (out of scope per skill); OPL's
Berlin governing law means a German court applies different doctrines
(esp. the "conclusive evidence" and "standing grant" constructs would be read
under BGB, not US canons). Recommend a German-law pass before publishing v1.4.2
as final.

---

## PART D — Recommended fixes (priority order)

1. **§4.1 "reachable"** — define it (Scenario 3). Highest-value, lowest-risk fix.
2. **§1 "Standard Terms"** — qualify "current at access" with §3.7 wind-down
   carve-out (Scenario 1). Removes the characterization conflict.
3. **§3.2** — state the payment protection travels with the Derivative plainly
   (Scenario 5).
4. **§1 "Designated Successor"** — align "signed statement" → "identified in
   NOTICE" to match §4.4/§5 (Scenario 2 cosmetic).
5. **§1 "Hosted Service"** — narrow with "distinct, separately-marketed
   capability" (Scenario 4).
6. **§5.1 DOSP clock** — "on or after OPL adoption date" (Scenario 6).

All six are clarifications (v1.4.3), same SPDX id. Items 1–3 are the ones worth
doing before any external adoption; 4–6 are nice-to-have hardening.

---

*Sources note: contract profile — instrument read on its four corners; no
external legal-research step (OPL is a private license, not a statute). Outcomes
predicted on a US interpretive frame; Berlin governing law noted as a divergence
requiring a separate German-law pass.*
