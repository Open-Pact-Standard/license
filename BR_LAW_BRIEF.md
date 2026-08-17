# Brazilian-Law Practitioner Brief — OPL v1.4.3 Pre-Publication Confirmation

*Prepared for: qualified Brazilian IP & contract counsel.*
*Purpose: confirm whether OPL v1.4.3 (draft, OPL-1.4 SPDX id) is enforceable and
travels correctly under Brazilian law, where a Work's NOTICE declares "Governing
Jurisdiction: Brazil" (or a Brazilian adopter applies OPL under Brazilian law).
One of several per-jurisdiction briefs; broader cross-system analysis in
REGIONAL_REVIEW.md. Pre-forms questions so counsel can confirm/correct
efficiently. NOT a legal opinion; a question list with texts and statutory
anchors.*

*Statute anchors — VERIFICATION STATUS: the statute NAMES are confirmed by
research (CDC 8.078/90 — Código de Defesa do Consumidor; Lei 9.609/98 — Software
Law). Specific SUB-ARTICLE numbers cited below are PROVISIONAL and must be
confirmed by Brazilian counsel — web research returned non-authoritative sources
for sub-articles. Treat all article sub-numbers as flagged-unverified.*

---

## 0. Scope & framing

- **Governing law declared:** Brazil → Código Civil (CC) + Código de Defesa do
  Consumidor (CDC, Lei 8.078/90) + Lei 9.609/98 (Software Law).
- **License type:** unilateral copyright license with commercial-use payment tier
  (Standard Terms URL) and automatic abandonment→Apache-2.0 conversion (§5).
- **User typology:** OPL's "You" spans consumers and businesses. CDC protects
  *consumidores*; B2B under CC. **Brazil's consumer protection is among the
  STRONGEST** — CDC art. 51 voids unconscionable clauses broadly.

---

## 1. Conditional grant (§5) — Código Civil art. 135 (condição suspensiva)

**OPL text (§5):** "standing conditional grant … effective automatically on
abandonment."

**Question 1a:** Under **CC art. 135** (condição suspensiva — "the effect of the
juridical act is suspended until the condition is fulfilled"), is a license grant
conditional on a future, objectively determinable event (Maintainer unreachable)
valid and self-executing? Does the Apache-2.0 grant vest without a formal act?
*(art. 135 number provisional — confirm.)*

**Consequence if wrong:** abandonment robustness fails for Brazilian adopters.

**Likely (predicted):** condição suspensiva recognized; vests on event. Confirm
article number.

---

## 2. "Conclusive evidence" (§5) — Código de Processo Civil (CPC)

**OPL text (§5):** successor recording "conclusive evidence … not a precondition."

**Question 2a:** Under the **CPC** evidence rules (parties may agree on
evidentiary weight; a private document such as a LICENSE commit is admissible),
can parties stipulate a private act as "conclusive evidence" (irrefutável)? Or is
that reserved? *(CPC article provisional — confirm.)*

**Consequence if wrong:** cosmetic — standing grant operative regardless.

---

## 3. Standard Terms incorporation + burden (§1, §3.3) — CC art. 423; CDC art. 51

**OPL text (§1/§3.3):** incorporates Standard Terms "at time of access," subject
to §3.7; **rebuttable presumption**, **User bears initial burden** of showing URL
failure.

**Question 3a (consumers):** Under **CDC art. 51** (void clauses — e.g.,
exoneration of fault, unilateral waiver of rights, burden-shift to consumer),
does OPL's "User bears initial burden" and "current at time of access"
incorporation engage art. 51? Brazilian CDC is interpreted BROADLY against the
supplier. *(art. 51 confirmed; sub-items provisional — confirm.)*

**Question 3b (B2B):** Under **CC art. 423** (interpretation contra proferentem
for ambiguous standard terms) and good-faith principles, is the burden allocation
enforceable between businesses?

**Consequence if wrong:** core mechanism likely VOID vs consumers under CDC art.
51; B2B posture needs confirmation. **Brazil is the highest consumer-exposure
system.**

---

## 4. Liability exclusion (§7/§8) — CDC art. 24–25; CC art. 14

**OPL text (§8):** "IN NO EVENT … LIABLE."

**Question 4a:** Under **CDC art. 24–25** (strict/objective liability for consumer
damage; cannot be excluded) and **CC art. 14** (fault liability), is a total
liability exclusion void against consumers? *(arts. 24–25 confirmed; confirm.)*

**Consequence if wrong:** blanket exclusion VOID vs consumers under CDC; §9.4
saves consumers but Brazilian courts are especially protective.

---

## 5. Forum selection + arbitration (§12) — CDC art. 101; CPC

**OPL text (§12):** exclusive jurisdiction of NOTICE courts; arbitration
permitted. **§9.4 (v1.4.3):** consumer's mandatory rights + local forum not
limited.

**Question 5a (consumers):** Under **CDC art. 101**, a consumer may sue in their
OWN DOMICILE regardless of any forum clause — forum clauses are VOID vs consumers
for consumer matters. Does OPL's §9.4 carve-out correctly preserve this? *(art.
101 confirmed; confirm.)*

**Question 5b (B2B):** Is a Brazilian exclusive-forum clause enforceable between
businesses (CPC art. 63)? Is arbitration permitted (Lei 9.307/96 — Arbitration
Law) as OPL states?

**Consequence if wrong:** §12 is VOID vs consumers under CDC art. 101 (strongest
consumer-forum protection of all surveyed systems); B2B forum enforceable.

---

## 6. "Urgent court relief" (§12.1) — tutela provisória (CPC art. 300)

**OPL text (§12.1, v1.4.3):** "injunctive or other urgent court relief."

**Question 6a:** Does "urgent court relief" adequately anchor **tutela provisória
de urgência** (CPC art. 300) / liminar? Or should OPL reference it explicitly?
*(CPC art. 300 confirmed; confirm.)*

**Consequence if wrong:** cosmetic.

---

## 7. Good faith (§3.3) — Código Civil art. 422

**OPL text (§3.3):** "honors it in good faith."

**Question 7a:** Maps to **CC art. 422** ("the parties are bound by good faith
obligations in contract formation and performance"). Confirm no additional
formalism needed.

---

## 8. Summary table

| # | OPL clause | Brazilian statute | Question | If wrong | Substance |
|---|---|---|---|---|---|
| 1 | §5 standing grant | CC art. 135 (cond. susp.) | self-executing? | abandonment robustness fails | 🔴 high *(art# prov.)* |
| 2 | §5 conclusive evidence | CPC evid. | stipulation valid? | cosmetic | 🟢 low |
| 3 | §1/§3.3 incorporation+burden | CDC art. 51; CC art. 423 | void vs consumers? | core mechanism VOID (B2C) | 🔴 high *(art# prov.)* |
| 4 | §7/§8 liability | CDC art. 24–25; CC art. 14 | void vs consumers? | VOID vs consumers | 🔴 high *(art# prov.)* |
| 5 | §12 forum/arb | CDC art. 101 | forum VOID vs consumers? | §12 VOID B2C | 🔴 high *(art# prov.)* |
| 6 | §12.1 urgent relief | CPC art. 300 (tutela) | label adequate? | cosmetic | 🟢 low |
| 7 | §3.3 good faith | CC art. 422 | duty present? | no conflict | 🟢 low |

**Brazil-specific sharp edge:** CDC art. 51 (clause voiding) + art. 101 (consumer
forum at home) make Brazil the MOST consumer-protective system surveyed. OPL's §9.4
carve-out is essential here; the B2C mechanisms (burden allocation, liability
exclusion, forum) are likely VOID against Brazilian consumers as a matter of
course. **This is expected and correct** — OPL subordinates to local law via §9.4.

---

## 9. What we need back from counsel

Confirm/enforce for #1–#7, and **CRITICALLY: verify every article sub-number
cited above** (web research was non-authoritative for Brazilian sub-articles).
Specifically:
- Confirm CC art. 135 (condição suspensiva) wording/number for the §5 grant.
- Confirm CDC arts. 51 / 24–25 / 101 applicability to OPL's B2C mechanisms.
- Confirm CPC article numbers for evidence (§5) and tutela provisória (§12.1).
- Confirm §9.4 carve-out is sufficient under CDC.

On receipt, OPL v1.4.3 can move Draft → Published (per release discipline).

---

*Prepared by: Hermes (agent), using ported legal skills as drafting aids. Brazilian
article sub-numbers are PROVISIONAL and flagged for local-counsel verification;
the statute names (CDC 8.078/90, Lei 9.609/98) are confirmed. Not a substitute
for the qualified Brazilian legal opinion this brief elicits. Companion files:
LEGAL_REVIEW.md, REGIONAL_REVIEW.md, GERMAN/FR/UK/JP_LAW_BRIEF.md.*
