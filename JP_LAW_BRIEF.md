# Japanese-Law Practitioner Brief — OPL v1.4.3 Pre-Publication Confirmation

*Prepared for: qualified Japanese IP & contract counsel.*
*Purpose: confirm whether OPL v1.4.3 (draft, OPL-1.4 SPDX id) is enforceable and
travels correctly under Japanese law, where a Work's NOTICE declares "Governing
Jurisdiction: Japan" (or a Japanese adopter applies OPL under Japanese law). One
of several per-jurisdiction briefs; broader cross-system analysis in
REGIONAL_REVIEW.md. Pre-forms questions so counsel can confirm/correct
efficiently. NOT a legal opinion; a question list with texts and statutory
anchors.*

*Statute anchors verified by web research (Aug 2026): Civil Code art. 1(2) (good
faith), art. 127 / 131 (condition precedent) — Japanese Law Translation / WIPO
Lex (2025 version). Consumer protection via the Act on Specified Commercial
Transactions (特定商取引法) and the Consumer Contract Act (消費者契約法).*

---

## 0. Scope & framing

- **Governing law declared:** Japan → Civil Code (民法) + consumer statutes.
- **License type:** unilateral copyright license with commercial-use payment tier
  (Standard Terms URL) and automatic abandonment→Apache-2.0 conversion (§5
  standing conditional grant).
- **User typology:** OPL's "You" spans consumers and businesses. Japanese
  consumer law (Consumer Contract Act) protects consumers; B2B under Civil Code.

---

## 1. Conditional grant (§5) — Civil Code art. 127 / 131

**OPL text (§5):** "standing conditional grant … effective automatically on
abandonment."

**Question 1a:** Under **Civil Code art. 127** ("a juridical act subject to a
condition precedent becomes effective upon fulfillment of the condition") and
art. 131, is a license grant conditional on a future, objectively determinable
event (Maintainer unreachable) valid and self-executing? Does the Apache-2.0
grant vest without a formal relicensing act?

**Consequence if wrong:** abandonment robustness fails for Japanese adopters.

**Likely (predicted):** condition precedent explicit in art. 127; vests on event.
Confirm.

---

## 2. "Conclusive evidence" (§5) — evidence (民事証拠)

**OPL text (§5):** successor recording "conclusive evidence … not a precondition."

**Question 2a:** Under Japanese civil evidence principles (parties may agree on
evidentiary weight; a private document such as a LICENSE commit is admissible
under art. 317 ff), can parties stipulate a private act as "conclusive evidence"?
Or is "conclusive" (立証責任の転換) reserved?

**Consequence if wrong:** cosmetic — standing grant operative regardless.

---

## 3. Standard Terms incorporation + burden (§1, §3.3) — Civil Code art. 548-2; Consumer Contract Act

**OPL text (§1/§3.3):** incorporates Standard Terms "at time of access," subject
to §3.7; **rebuttable presumption**, **User bears initial burden** of showing URL
failure.

**Question 3a (consumers):** Under the **Consumer Contract Act (消費者契約法)** and
**Civil Code art. 548-2** (incorporation of standard terms by reference), is
OPL's burden-shift and "current at time of access" incorporation challengeable?
Note: art. 548-2 requires the standard terms to be "indicated" to the other
party; surprise/unreasonable terms may be invalid. Does OPL's Standard-Terms
incorporation engage art. 548-2 / the Consumer Contract Act?

**Question 3b (B2B):** Under **Civil Code art. 548-2** (standard terms between
businesses), is the burden allocation enforceable? Japanese law scrutinizes
unreasonable standard terms even B2B (art. 548-2 三号/四号 — grossly
unreasonable clauses void).

**Consequence if wrong:** core mechanism inoperative vs consumers; B2B posture
needs confirmation.

---

## 4. Liability exclusion (§7/§8) — Civil Code art. 415; Consumer Contract Act

**OPL text (§8):** "IN NO EVENT … LIABLE."

**Question 4a:** Under **Civil Code art. 415** (liability for non-performance /
tort) and the **Consumer Contract Act**, is a total liability exclusion void
against consumers? Restricted against businesses (Japanese courts limit
exclusion of liability for willful/material negligence)?

**Consequence if wrong:** partial void vs consumers; §9.4 saves consumers.

---

## 5. Forum selection + arbitration (§12) — Civil Code art. 11-2; consumer statutes

**OPL text (§12):** exclusive jurisdiction of NOTICE courts; arbitration
permitted. **§9.4 (v1.4.3):** consumer's mandatory rights + local forum not
limited.

**Question 5a (consumers):** Under the **Consumer Contract Act** and **Civil Code
art. 11-2** (agreed jurisdiction; consumer may sue in their own domicile under
the Act on Specified Commercial Transactions), may a consumer sue locally
regardless of §12? Does OPL's §9.4 carve-out preserve this?

**Question 5b (B2B):** Is a Japanese exclusive-forum clause (合意管轄) enforceable
between businesses? Is arbitration (arbitration clause under the Arbitration Act)
permitted as OPL states?

**Consequence if wrong:** §12 inoperative vs consumers; B2B forum enforceable.

---

## 6. "Urgent court relief" (§12.1) — provisional disposition (民事保全)

**OPL text (§12.1, v1.4.3):** "injunctive or other urgent court relief."

**Question 6a:** Does "urgent court relief" adequately anchor **provisional
disposition (仮処分)** / injunction under the Civil Preservation Act
(民事保全法)? Or should OPL reference it explicitly?

**Consequence if wrong:** cosmetic.

---

## 7. Good faith (§3.3) — Civil Code art. 1(2)

**OPL text (§3.3):** "honors it in good faith."

**Question 7a:** Maps to **art. 1(2)** ("the exercise of rights and performance
of duties must be done in good faith"). Confirm no additional formalism needed;
note art. 1(2) is a constitutional-level principle in Japan.

---

## 8. Summary table

| # | OPL clause | Japanese statute | Question | If wrong | Substance |
|---|---|---|---|---|---|
| 1 | §5 standing grant | CC art. 127/131 | self-executing condition? | abandonment robustness fails | 🔴 high |
| 2 | §5 conclusive evidence | CC art. 317 ff | stipulation valid? | cosmetic | 🟢 low |
| 3 | §1/§3.3 incorporation+burden | CC art. 548-2; Consumer Contract Act | unfair-terms exposure? | core mechanism void (B2C) | 🔴 high |
| 4 | §7/§8 liability | CC art. 415; Consumer Contract Act | void vs consumers/B2B? | partial void; §9.4 saves | 🟡 med |
| 5 | §12 forum/arb | CC art. 11-2; consumer statutes | consumer override handled? | §12 inoperative B2C | 🟡 med |
| 6 | §12.1 urgent relief | Civil Preservation Act (民事保全) | label adequate? | cosmetic | 🟢 low |
| 7 | §3.3 good faith | CC art. 1(2) | duty present? | no conflict | 🟢 low |

---

## 9. What we need back from counsel

Confirm/enforce for #1–#7. Specifically:
- Is the §5 standing grant self-executing under art. 127/131?
- Does OPL's burden allocation survive art. 548-2 (B2B) and the Consumer Contract
  Act (B2C)?
- Is §9.4's consumer carve-out sufficient under the consumer forum statutes?

On receipt, OPL v1.4.3 can move Draft → Published (per release discipline).

---

*Prepared by: Hermes (agent), using ported legal skills as drafting aids. Not a
substitute for the qualified Japanese legal opinion this brief elicits. Companion
files: LEGAL_REVIEW.md, REGIONAL_REVIEW.md, GERMAN/FR/UK_LAW_BRIEF.md.*
