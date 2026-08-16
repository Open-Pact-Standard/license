# German-Law / EU Practitioner Brief — OPL v1.4.3 Pre-Publication Confirmation

*Prepared for: qualified German/EU intellectual-property & contract counsel.*
*Purpose: confirm whether OPL v1.4.3 (draft, OPL-1.4 SPDX id) is enforceable and
travels correctly under German law (BGB) and the EU overlay, where the Work's
NOTICE declares "Governing Jurisdiction: Berlin, Germany" (as the origin-canary
reference adoption does). This brief pre-forms the questions so counsel can
confirm or correct efficiently. It is NOT a legal opinion; it is a question list
with the relevant texts and statutory anchors.*

*Source texts: OPL v1.4.3 LICENSE.md (open-pact-license repo, commit 7827c1d);
the companion REGIONAL_REVIEW.md (cross-system scan) and LEGAL_REVIEW.md
(adversarial ambiguity review). OPL remains marked "Draft … Not yet published";
this brief is the gate before that status changes.*

---

## 0. Scope & framing

- **Governing law declared:** Berlin, Germany → BGB + EU directives as applicable.
- **License type:** a public, unilateral, copyright-based license with a
  commercial-use payment tier (Standard Terms URL) and an automatic
  abandonment→Apache-2.0 conversion (§5 standing conditional grant).
- **Two distinct legal objects must be separated:**
  1. **OPL itself** — the license text the Maintainer offers to users.
  2. **The Maintainer's Standard Terms** (published at the NOTICE URL) — the
     Maintainer's *own* commercial contract, distinct from OPL.
  German AGB-control (§305 ff BGB) may attach to **either or both** depending on
  whether each is "general business terms." This brief separates them.
- **User typology OPL does not distinguish:** OPL's "You" spans consumers,
  solo developers, and businesses. German/EU mandatory protections differ by
  user type. Counsel should confirm treatment for each.

---

## 1. Abandonment "standing conditional grant" (§5) — BGB §158

**OPL text (§5):** "the Maintainer hereby grants each recipient a license under
the Apache License 2.0, effective automatically on abandonment … a standing
conditional grant … requires no further act by the Maintainer."

**Question 1a:** Is a license grant conditional on a future, objectively
determinable event (Maintainer unreachable for the NOTICE-declared period) valid
and self-executing under **BGB §158 (Bedingte Rechtsgeschäfte)**? Does German
law require any formal act (e.g., a written relicensing) for the Apache-2.0
rights to vest, or does the condition-precedent suffice?

**Question 1b:** OPL states the conversion "requires no third-party
authorization … no fiscal sponsor … no public notice." Under BGB, is a
condition precedent that vests rights in the absence of any recording or
registry enforceable against the Maintainer's successors and assigns? (I.e., can
a downstream licensee rely on the Apache-2.0 grant without a recorded instrument?)

**Consequence if wrong:** if BGB requires a formal act for the grant to vest, the
"no actor required" design fails and OPL's abandonment robustness collapses for
German adopters — the single feature v1.4.2 was built to secure.

**Likely (predicted, not advised):** BGB §158 recognizes conditions precedent; a
grant that vests on condition should be valid without a formal recording between
the parties. Confirm.

---

## 2. "Conclusive evidence" — successor recording (§5)

**OPL text (§5):** a Designated Successor "is authorized — but not required — to
record the abandonment conversion by publishing an Apache License 2.0 LICENSE …
Such a recording is conclusive evidence of the conversion; it is not a
precondition."

**Question 2a:** Can parties by agreement (OPL) stipulate that a private act
(publishing a LICENSE file) is "conclusive evidence" of a legal status
(conversion to Apache-2.0)? Under **ZPO** (procedural law), is such an
evidentiary agreement permissible between the contracting parties, or is
"conclusive" (unwiderleglich) reserved to statutory cases (§292 ZPO)?

**Consequence if wrong:** the recording's "conclusive" weight is a label only;
the standing grant (§5) is the operative mechanism regardless, so failure here is
cosmetic. Low risk. Confirm for cleanliness.

---

## 3. Standard Terms incorporation + burden allocation (§1, §3.3) — BGB §305c, §309, AGB-Kontrolle

**OPL text (§1 "Standard Terms"):** "The License incorporates the Standard Terms
as they exist at the URL at the time of access by the user … subject to the
wind-down protections in §3.7." **§3.3:** a **rebuttable presumption** that a
Valid Standard Terms URL satisfies 7 criteria; "the **User bears the initial
burden** of showing the URL failed a criterion; the Maintainer bears the burden
of showing it satisfied the criteria."

**Question 3a (OPL as AGB):** If OPL is treated as the Maintainer's general
business terms (AGB) under **BGB §305 ff**, does the "User bears the initial
burden" allocation survive AGB-content control? German courts scrutinize
burden-shifting and surprise clauses. Is **§305c (überraschende Klauseln —
surprising clauses void)** or **§309 (klauselverbote ohne Wertungsmöglichkeit)**
engaged?

**Question 3b (Maintainer's Standard Terms as AGB):** The Maintainer's *own*
Standard Terms (published at the URL) are almost certainly AGB. Does OPL's
"current at time of access" + 90-day-change model (§3.3) create AGB-risk for the
Maintainer (e.g., one-sided price-change power under **§307 BGB**)?

**Consequence if wrong:** if OPL's burden allocation is void as AGB, the
rebuttable-presumption machinery (a central OPL mechanism) is unenforceable
against German business users, and the Maintainer's Standard Terms face
content-control challenge. **This is the highest-substance exposure.**

**Mitigation already present:** OPL §9.4 subordinates to applicable law, and the
Maintainer can negotiate bespoke terms. But the *default* AGB posture should be
confirmed.

---

## 4. Liability exclusion (§7 Disclaimer, §8 Limitation) — BGB §309 Nr. 7–8, §276

**OPL text (§8):** "IN NO EVENT SHALL ANY CONTRIBUTOR OR MAINTAINER BE LIABLE FOR
ANY CLAIM, DAMAGES, OR OTHER LIABILITY … ARISING FROM … THE WORK."

**Question 4a:** Under **BGB §309 Nr. 7 (Haftungsausschluss bei
Grobfahrlässigkeit/ Vorsatz)** and **§309 Nr. 8 (Haftung für Sach-/Körperschäden)**,
is a *total* liability exclusion void as against **consumers**? Against
**businesses**, does it fail for gross negligence / intentional breach?

**Question 4b:** OPL §2 grants broad Personal Use rights to "any individual."
If a consumer uses the Work personally and suffers damages, does **§309**
override OPL's §8 entirely for that consumer (leaving OPL's liability regime
inoperative)? Does **§9.4** (law controls) handle this correctly, or should OPL
state the consumer carve-out explicitly? *(Note: v1.4.3 already added a §9.4
consumer carve-out sentence — confirm it is drafted broadly enough.)*

**Consequence if wrong:** the blanket §8 is partially void vs consumers and
restricted vs businesses under AGB. OPL's §9.4 saves consumers, but the B2B AGB
posture needs confirmation.

---

## 5. Forum-selection & arbitration (§12, §12.1) — Brussels Ibis, BGB §§1033–1041a

**OPL text (§12):** exclusive jurisdiction of the NOTICE-declared courts;
arbitration permitted. **§12.1:** injunctive/"urgent court relief" permitted
notwithstanding §12. **§9.4 (v1.4.3):** consumer's mandatory rights and local
forum not limited.

**Question 5a (consumers):** Under **Brussels Ibis Regulation (EU) 1215/2015,
Art. 18–19**, can a consumer be bound by OPL's exclusive forum clause, or may
they sue in their home court regardless? Does OPL's §9.4 consumer carve-out
correctly preserve this, or is an explicit Brussels-Ibis acknowledgment needed?

**Question 5b (arbitration):** Under **BGB §§1033–1041a ZPO**, are consumer
arbitration agreements restrictable? Does OPL's "parties may agree to binding
arbitration for a specific dispute" survive for B2B? For consumers?

**Consequence if wrong:** §12 is inoperative against EU consumers (they sue
locally) — OPL's §9.4 carve-out should handle it; confirm wording is sufficient
and that B2B arbitration is clean.

---

## 6. "Urgent court relief" label (§12.1) — terminology

**OPL text (§12.1, v1.4.3):** changed from "equitable relief" to "injunctive or
other urgent court relief." German equivalent: **einstweilige Verfügung (§935 ff
ZPO)**.

**Question 6a:** Is "urgent court relief" an adequate translation anchor for the
§935 ff ZPO remedy, or should OPL reference it explicitly for German adopters?

**Consequence if wrong:** cosmetic only — the remedy exists; the label is a
translation aid.

---

## 7. Good-faith / "honors in good faith" (§3.3) — BGB §242

**OPL text (§3.3):** "the Maintainer honors it [the payment mechanism] in good
faith."

**Question 7a:** This maps to **BGB §242 (Treu und Glauben)**. Confirm German law
provides the implied duty OPL relies on, and that no additional formalism is
needed. *(Predicted: §242 is broader than the US implied covenant — no conflict.)*

---

## 8. Summary table for counsel

| # | OPL clause | German statute | Question | If wrong | Substance |
|---|---|---|---|---|---|
| 1 | §5 standing grant | BGB §158 | self-executing condition? | abandonment robustness fails | 🔴 high |
| 2 | §5 conclusive evidence | ZPO §292 | evidentiary agreement valid? | cosmetic | 🟢 low |
| 3 | §1/§3.3 incorporation + burden | BGB §305c, §307, §309 | AGB-control of burden alloc? | core mechanism void (B2B) | 🔴 high |
| 4 | §7/§8 liability exclusion | BGB §309 Nr.7–8, §276 | void vs consumers/business? | partial void; §9.4 saves consumers | 🟡 med |
| 5 | §12 forum / arbitration | Brussels Ibis Art.18–19; ZPO §§1033–1041a | consumer override handled? | §12 inoperative vs consumers | 🟡 med |
| 6 | §12.1 urgent relief | ZPO §935 ff | label adequate? | cosmetic | 🟢 low |
| 7 | §3.3 good faith | BGB §242 | implied duty present? | no conflict | 🟢 low |

**Must-fix-in-text candidates (if counsel agrees):** #1 (confirm self-executing
grant — if BGB needs formalism, OPL needs a recording fallback), #3 (AGB posture
of OPL's own burden allocation). #4/#5 already mitigated by §9.4 + v1.4.3
consumer carve-out; confirm sufficiency.

**Advisor-only (Maintainer's Standard Terms, not OPL):** #3b (Maintainer's own
AGB), #4b (Maintainer's liability stance). OPL cannot fix these; the Maintainer
obtains separate AGB review.

---

## 9. What we need back from counsel

For each of #1–#7: confirm / correct / flag, with the controlling authority.
Specifically:
- Is OPL v1.4.3 **enforceable as written** under BGB for (a) business users,
  (b) consumer users?
- Does the §5 standing grant **vest without a formal act**, or must OPL add a
  recording mechanism for German adopters?
- Does OPL's AGB exposure (its own burden allocation, #3) require **text changes**,
  or is §9.4 + negotiation sufficient?
- Is the **§9.4 consumer carve-out** (v1.4.3) drafted broadly enough to satisfy
  Brussels Ibis + §309?

On receipt of counsel's confirmation (or required text changes), OPL v1.4.3 can
move from **Draft** to **Published** per the project's release discipline
(full audit + maintainer sign-off on timing and content; no tag/release without
explicit approval).

---

*Prepared by: Hermes (agent), using ported legal skills as drafting aids. Not a
substitute for the qualified German/EU legal opinion this brief is designed to
elicit. Companion files: LEGAL_REVIEW.md, REGIONAL_REVIEW.md.*
