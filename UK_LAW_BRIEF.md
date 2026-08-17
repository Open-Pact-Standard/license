# UK-Law Practitioner Brief — OPL v1.4.3 Pre-Publication Confirmation

*Prepared for: qualified English IP & contract counsel.*
*Purpose: confirm whether OPL v1.4.3 (draft, OPL-1.4 SPDX id) is enforceable and
travels correctly under the law of England & Wales, where a Work's NOTICE
declares "Governing Jurisdiction: United Kingdom" (or an English adopter applies
OPL under English law). One of several per-jurisdiction briefs; broader
cross-system analysis in REGIONAL_REVIEW.md. Pre-forms questions so counsel can
confirm/correct efficiently. NOT a legal opinion; a question list with texts and
statutory anchors.*

*Statute anchors verified by web research (Aug 2026): Unfair Contract Terms Act
1977 (legislation.gov.uk — "no known outstanding effects", still in force);
Consumer Rights Act 2015 (consumer unfair terms, Part 2); post-Brexit — UK left
Brussels Ibis (Jan 2021); consumer forum protection now rests on the Civil
Jurisdiction and Judgments (Amendment) Regulations 2019 (ss.15B/15C), not EU law.*

---

## 0. Scope & framing

- **Governing law declared:** England & Wales (or "United Kingdom" — note: UK is
  not a single jurisdiction for private law; clarify England/Wales vs Scotland).
- **License type:** unilateral copyright license with commercial-use payment
  tier (Standard Terms URL) and automatic abandonment→Apache-2.0 conversion (§5
  standing conditional grant).
- **User typology:** OPL's "You" spans consumers and businesses. UK protects
  consumers under CRA 2015; B2B under UCTA 1977 + common law.
- **Brexit note:** Brussels Ibis no longer binds the UK. Consumer forum override
  now derives from UK statute (2019 Regs), not EU regulation.

---

## 1. Conditional grant (§5) — condition precedent (common law)

**OPL text (§5):** "standing conditional grant … effective automatically on
abandonment … requires no further act."

**Question 1a:** Is a license grant conditional on a future, objectively
determinable event (Maintainer unreachable for the NOTICE period) valid and
self-executing as a **condition precedent** at English common law? Does the
Apache-2.0 grant vest in the licensee without a formal relicensing act?

**Consequence if wrong:** abandonment robustness fails for English adopters.

**Likely (predicted):** condition precedent recognized; vests on event. Confirm.

---

## 2. "Conclusive evidence" (§5) — evidence law

**OPL text (§5):** successor recording "conclusive evidence … not a precondition."

**Question 2a:** Under the Civil Evidence Act 1995 and common-law evidentiary
principles, can parties stipulate a private act (LICENSE commit) as "conclusive
evidence" between themselves? Or is "conclusive" weight reserved?

**Consequence if wrong:** cosmetic — standing grant operative regardless.

---

## 3. Standard Terms incorporation + burden (§1, §3.3) — UCTA 1977; CRA 2015

**OPL text (§1/§3.3):** incorporates Standard Terms "at time of access," subject
to §3.7; **rebuttable presumption**, **User bears initial burden** of showing URL
failure.

**Question 3a (consumers):** Under **CRA 2015 Part 2 (ss.62–63, 64–65)**, is the
burden-shifting and "current at time of access" incorporation an **unfair term**
(unfair if contrary to good faith / causing significant imbalance)? Note: CRA
exempts "core" price/subject terms from the fairness test if transparent — does
OPL's Standard-Terms incorporation engage s.62?

**Question 3b (B2B):** Under **UCTA 1977 s.3**, does OPL's burden allocation
(imposed by a "business" Maintainer on another business) fail the
**reasonableness** test (s.11)? Is OPL treated as the Maintainer's standard
terms engaging UCTA?

**Consequence if wrong:** core mechanism inoperative vs consumers; B2B posture
needs reasonableness assessment.

---

## 4. Liability exclusion (§7/§8) — UCTA 1977 s.2–3

**OPL text (§8):** "IN NO EVENT … LIABLE … IN AN ACTION OF CONTRACT, TORT, OR
OTHERWISE."

**Question 4a:** Under **UCTA 1977 s.2(1)** (negligence liability) and **s.3**
(contractual liability when dealing on own standard terms), is the blanket
exclusion valid? Note: s.2(1) **absolutely prohibits** excluding liability for
death/personal injury caused by negligence; other negligence needs reasonableness
(s.11). Does OPL's "action of … tort" language engage s.2?

**Question 4b (consumers):** Under **CRA 2015**, is the exclusion an unfair term
vs consumers regardless of UCTA?

**Consequence if wrong:** blanket exclusion fails reasonableness / is void vs
consumers; §9.4 saves consumers but B2B needs a reasonableness note.

---

## 5. Forum selection + arbitration (§12) — post-Brexit

**OPL text (§12):** exclusive jurisdiction of NOTICE courts; arbitration
permitted. **§9.4 (v1.4.3):** consumer's mandatory rights + local forum not
limited.

**Question 5a (consumers):** Post-Brexit, under the **Civil Jurisdiction and
Judgments (Amendment) Regulations 2019 (ss.15B/15C)**, may a consumer sue in
their home court regardless of §12? Does OPL's §9.4 carve-out preserve this?

**Question 5b (B2B):** Is an English exclusive-jurisdiction clause enforceable
under the 2019 Regs / common law? Is the "binding arbitration for a specific
dispute" carve-out valid (Arbitration Act 1996)?

**Consequence if wrong:** §12 inoperative vs consumers (UK statute overrides);
B2B forum enforceable.

---

## 6. "Urgent court relief" (§12.1) — injunctive relief

**OPL text (§12.1, v1.4.3):** "injunctive or other urgent court relief."

**Question 6a:** "Urgent court relief" adequately anchors **injunctions** (Senior
Courts Act 1981 s.37) / interim injunctions? Adequate for English counsel?

**Consequence if wrong:** cosmetic.

---

## 7. Good faith (§3.3) — common law (narrower)

**OPL text (§3.3):** "honors it in good faith."

**Question 7a:** English common law has **no general implied duty of good faith**
(unlike civil law), but recognizes it in **relational contracts** (post-2019
*BrailSF*) and in specific contexts. Does OPL's §3.3 good-faith reliance find a
hook, or is it narrower than civil-law systems? Does this create any
enforceability gap vs the French/German readings?

**Consequence if wrong:** good-faith duty may be narrower in England — flag for
drafting consistency across jurisdictions.

---

## 8. Summary table

| # | OPL clause | UK statute | Question | If wrong | Substance |
|---|---|---|---|---|---|
| 1 | §5 standing grant | common law (condition precedent) | self-executing? | abandonment robustness fails | 🔴 high |
| 2 | §5 conclusive evidence | Civil Evidence Act 1995 | stipulation valid? | cosmetic | 🟢 low |
| 3 | §1/§3.3 incorporation+burden | CRA 2015 s.62; UCTA s.3 | unfair/reasonableness? | core mechanism void (B2C) | 🔴 high |
| 4 | §7/§8 liability | UCTA s.2–3 | reasonableness / void? | fails s.2(1) death/injury; §9.4 saves B2C | 🔴 high (strictest) |
| 5 | §12 forum/arb | 2019 Regs ss.15B/15C | consumer override handled? | §12 inoperative B2C | 🟡 med |
| 6 | §12.1 urgent relief | SCA 1981 s.37 | label adequate? | cosmetic | 🟢 low |
| 7 | §3.3 good faith | common law (relational) | duty present/narrower? | possible gap vs civil law | 🟡 med |

**UK-specific sharp edge:** UCTA's reasonableness test (s.11) is the STRICTEST
B2B regime among the surveyed systems — English B2B users relying on OPL's
liability exclusion should expect a reasonableness assessment. Flag in advisor
guidance.

---

## 9. What we need back from counsel

Confirm/enforce for #1–#7. Specifically:
- Is the §5 standing grant self-executing at English common law?
- Does OPL's burden allocation survive CRA 2015 (B2C) and UCTA s.3 reasonableness
  (B2B)?
- Is the blanket §8 exclusion valid under UCTA s.2, or void for death/personal
  injury / failed reasonableness?
- Is §9.4's consumer carve-out sufficient post-Brexit (2019 Regs ss.15B/15C)?

On receipt, OPL v1.4.3 can move Draft → Published (per release discipline).

---

*Prepared by: Hermes (agent), using ported legal skills as drafting aids. Not a
substitute for the qualified English legal opinion this brief elicits. Companion
files: LEGAL_REVIEW.md, REGIONAL_REVIEW.md, GERMAN_LAW_BRIEF.md, FR_LAW_BRIEF.md.*
