# French-Law Practitioner Brief — OPL v1.4.3 Pre-Publication Confirmation

*Prepared for: qualified French IP & contract counsel.*
*Purpose: confirm whether OPL v1.4.3 (draft, OPL-1.4 SPDX id) is enforceable and
travels correctly under French law, where a Work's NOTICE declares "Governing
Jurisdiction: France" (or a French adopter applies OPL under French law). One of
several per-jurisdiction briefs; broader cross-system analysis in
REGIONAL_REVIEW.md. Pre-forms questions so counsel can confirm/correct
efficiently. NOT a legal opinion; a question list with texts and statutory
anchors.*

*Statute anchors verified by web research (Aug 2026): Code civil art. 1104
(Légifrance — in force 1/10/2016, unchanged); Code de la consommation L212-1
(implements ex-Dir 93/13); Brussels Ibis Reg. (EU) 1215/2015 (France is an EU
member).*

---

## 0. Scope & framing

- **Governing law declared:** France → Code civil + Code de la consommation + EU
  regulations (France is EU member).
- **License type:** unilateral copyright license with a commercial-use payment
  tier (Standard Terms URL) and automatic abandonment→Apache-2.0 conversion (§5
  standing conditional grant).
- **User typology:** OPL's "You" spans consumers, solo developers, businesses.
  French consumer law (Code de la consommation) protects *consummateurs*; B2B is
  governed by Code civil. Counsel should confirm treatment per type.

---

## 1. Conditional grant (§5) — Code civil art. 1304-1 ff (condition suspensive)

**OPL text (§5):** "the Maintainer hereby grants each recipient a license under
the Apache License 2.0, effective automatically on abandonment … a standing
conditional grant."

**Question 1a:** Is a license grant subject to a future, objectively determinable
condition (Maintainer unreachable for the NOTICE-declared period) valid and
self-executing under French law as a **condition suspensive** (art. 1304-1 ff,
formerly art. 1181)? Does the grant vest in the licensee without a formal
relicensing act by the Maintainer?

**Consequence if wrong:** if French law requires a formal act for the grant to
vest, the "no actor required" design fails for French adopters.

**Likely (predicted):** condition suspensive is recognized; vests on event
without formality between parties. Confirm.

---

## 2. "Conclusive evidence" (§5) — preuve

**OPL text (§5):** a Designated Successor "may record … conclusive evidence of
the conversion; not a precondition."

**Question 2a:** Under French evidence law (art. 1353 ff C. civ., freedom of
proof for non-consumer matters; admissibility of a private writing such as a
LICENSE commit), can parties stipulate a private act as "conclusive evidence"? Or
is "conclusive" (irréfragable) reserved to specific statutory cases?

**Consequence if wrong:** cosmetic — the standing grant (§5) is operative
regardless.

---

## 3. Standard Terms incorporation + burden (§1, §3.3) — C. consom. L212-1

**OPL text (§1/§3.3):** incorporates Standard Terms "at time of access,"
subject to §3.7 wind-down; a **rebuttable presumption** with **User bears
initial burden** of showing URL failure.

**Question 3a (consumers):** Under **C. consom. L212-1** (ex-Dir 93/13), are
OPL's burden-shifting and the "current at time of access" incorporation
challengeable as unfair terms? Note: French law exempts "core" price/subject
terms from the unfairness test but scrutinizes opacity and surprise. Does OPL's
Standard-Terms incorporation engage L212-1?

**Question 3b (B2B):** Under **C. civ. art. 1104 / 1110** (good faith;
sanctions of unfair/trapping clauses under art. 1164 / 1171 for standard terms),
is the burden allocation enforceable between professionals?

**Consequence if wrong:** core mechanism (rebuttable presumption) may be
inoperative vs consumers; B2B posture needs confirmation.

---

## 4. Liability exclusion (§7/§8) — C. civ. art. 1231-5; C. consom.

**OPL text (§8):** "IN NO EVENT … LIABLE."

**Question 4a:** Under **C. civ. art. 1231-5** (exoneration clauses) and
consumer provisions, is a total liability exclusion void against consumers?
Restricted against businesses (particularly for fault/obligation de
sécurité)?

**Consequence if wrong:** partial void vs consumers; §9.4 saves consumers.

---

## 5. Forum selection + arbitration (§12) — Brussels Ibis; C. consom.

**OPL text (§12):** exclusive jurisdiction of NOTICE courts; arbitration
permitted. **§9.4 (v1.4.3):** consumer's mandatory rights + local forum not
limited.

**Question 5a (consumers):** Under **Brussels Ibis Reg. 1215/2015 Art. 18–19**
(France bound as EU member), may a consumer sue in their home court regardless of
§12? Does OPL's §9.4 carve-out correctly preserve this?

**Question 5b (B2B):** Is a French exclusive-forum clause enforceable between
professionals? Is arbitration (arbitrage) permitted and confined to "specific
dispute" as OPL states?

**Consequence if wrong:** §12 inoperative vs consumers; B2B forum enforceable.

---

## 6. "Urgent court relief" (§12.1) — référé (CPC art. 808)

**OPL text (§12.1, v1.4.3):** "injunctive or other urgent court relief."

**Question 6a:** Does "urgent court relief" adequately anchor the **référé**
(art. 808 CPC — judge des référés) remedy? Or should OPL reference it explicitly?

**Consequence if wrong:** cosmetic.

---

## 7. Good faith (§3.3) — C. civ. art. 1104

**OPL text (§3.3):** "honors it in good faith."

**Question 7a:** Maps to **art. 1104** ("les contrats doivent être négociés,
formés et exécutés de bonne foi" — explicitly at formation since 2016 reform).
Confirm no additional formalism needed; note art. 1104's formation-stage
good-faith duty is broader than the US implied covenant.

---

## 8. Summary table

| # | OPL clause | French statute | Question | If wrong | Substance |
|---|---|---|---|---|---|
| 1 | §5 standing grant | C. civ. 1304-1 ff | self-executing condition? | abandonment robustness fails | 🔴 high |
| 2 | §5 conclusive evidence | C. civ. 1353 ff | evidentiary stipulation valid? | cosmetic | 🟢 low |
| 3 | §1/§3.3 incorporation+burden | C. consom. L212-1; C. civ. 1104/1171 | unfair-terms exposure? | core mechanism void (B2C) | 🔴 high |
| 4 | §7/§8 liability | C. civ. 1231-5 | void vs consumers/B2B? | partial void; §9.4 saves | 🟡 med |
| 5 | §12 forum/arb | Brussels Ibis 18–19 | consumer override handled? | §12 inoperative B2C | 🟡 med |
| 6 | §12.1 urgent relief | CPC 808 (référé) | label adequate? | cosmetic | 🟢 low |
| 7 | §3.3 good faith | C. civ. 1104 | implied duty present? | no conflict | 🟢 low |

---

## 9. What we need back from counsel

Confirm/enforce for #1–#7 with controlling authority. Specifically:
- Is the §5 standing grant self-executing under French condition-suspensive law?
- Does OPL's AGB-style burden allocation (§3.3) survive L212-1 for B2C / art.
  1171 for B2B?
- Is §9.4's consumer carve-out sufficient for Brussels Ibis Art. 18–19?

On receipt, OPL v1.4.3 can move Draft → Published (per release discipline: full
audit + maintainer sign-off on timing and content; no tag/release without
explicit approval).

---

*Prepared by: Hermes (agent), using ported legal skills as drafting aids. Not a
substitute for the qualified French legal opinion this brief elicits. Companion
files: LEGAL_REVIEW.md, REGIONAL_REVIEW.md, GERMAN_LAW_BRIEF.md.*
