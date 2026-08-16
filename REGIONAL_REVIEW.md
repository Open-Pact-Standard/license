# OPL v1.4.3 — Regional / Jurisdictional Discrepancy Scan

*Follow-on to LEGAL_REVIEW.md. The first review assumed a US interpretive frame
and flagged that OPL's stated governing law is Berlin, Germany. This scan asks a
sharper question: **does OPL's drafting silently assume US/common-law doctrine in
ways that break or shift meaning under other legal systems a real adopter might
be in?** Because OPL is a *template* license — adopters declare their own
governing jurisdiction in NOTICE — the license must not carry hidden US-specific
constructs that misfire when an adopter in, say, France, Japan, or Brazil applies
it under their own law.*

*Method: read the text for Anglo-American legal constructs; map each against
German/BGB (OPL's own stated law), EU-overlay (Berlin = EU member), other
civil-law systems, and common-law. Flag where the construct (a) is void/voidable,
(b) flips meaning, or (c) is simply inoperative under local law. Severity =
adopter-exposure if they rely on the clause under that law. Not legal advice;
qualified local counsel needed before publishing v1.4.3 as final.*

---

## A. Constructs that assume US/common-law doctrine

### R1 — "standing conditional grant" (§5)
**US frame:** a grant "hereby granted, effective automatically on condition" is a
familiar equitable/contractual mechanism; enforceable as written.
**German/BGB:** a license grant triggered by a *future condition* (unreachability)
is valid as a befristete/bedingte Einräumung (conditional grant), but German law
has **no doctrine of "automatic conversion" by operation of the license's own
terms** the way Anglo systems imply. Under BGB §158, a condition precedent is
recognized, so the grant *can* be conditional — but the *automatic* quality
rests on contract freedom (§305 ff), which is fine between the parties. **Low
risk, but** the "standing grant" vocabulary is US; a German court reads it as a
bedingte Lizenzgewährung, which is fine. **Verdict: operative, no fix needed, but
rename-risk if you want German-native phrasing.**
**EU/civil-law generally:** conditional grants are recognized across civil law.
**Verdict: ✅ portable.**

### R2 — "conclusive evidence" (§5 successor recording)
**US frame:** "conclusive evidence" is a standard evidentiary label.
**German/BGB:** "conclusive" (unwiderleglich) evidence is recognized (§292 ZPO
for certain statutory cases; by agreement parties can agree evidentiary weight),
but a *private* recording being "conclusive" is unusual — German procedural law
treats such agreements as to evidentiary effect as generally permissible between
parties (dispositiv). **Low risk.** The bigger issue: the recording is a GitHub
commit of an Apache LICENSE — under German law that's a simple declaration, not a
formal act. **Verdict: ✅ operative, semantic only.**

### R3 — "incorporated by reference" + "rebuttable presumption" (§1, §3.3)
**US frame:** incorporation by reference and rebuttable presumptions are routine.
**German/BGB:** "incorporation by reference" of external terms (the Standard Terms
URL) triggers **§305c BGB (überraschende Klauseln — surprising clauses are void)**
and the **AGB-Kontrolle (standard-terms review)**. If the Maintainer's Standard
Terms are "general business terms" (AGB) under BGB, they are subject to
judicial content control — and a *consumer* or *small-business* user gets
heightened protection. **MEDIUM risk for German adopters:** the "current Standard
Terms at time of access" + "rebuttable presumption, User bears initial burden"
language could be read as an AGB clause shifting burden of proof — German courts
are skeptical of burden-shifting and surprise. **This is the most jurisdiction-
sensitive clause for OPL's own stated law.**
**EU overlay:** Directive 93/13 (unfair terms in consumer contracts) + the new
**Directive (EU) 2019/770** (supply of digital content/services) mean a *consumer*
adopting-or-using OPL software gets mandatory rights OPL cannot waive (§9.4
correctly says "this license does not supersede applicable law" — good, that
saves it). **Verdict: ✅ saved by §9.4, but the AGB-control exposure for German
B2B-via-AGB remains; note it.**

### R4 — "implied covenant of good faith and fair dealing"
**US frame:** implied in every contract (esp. NY/CA).
**German/BGB:** **§242 BGB** is the civil-law equivalent (Treu und Glauben) and is
*stronger/more explicit* than the US implied covenant. So OPL's "honors it in
good faith" (§3.3) maps cleanly onto §242. **Verdict: ✅ German law is MORE
protective here; no conflict.**
**Civil-law generally:** good faith is a general principle (art. 1134 Fr. civ.,
etc.). **✅ portable.**

### R5 — "Limitation of liability" / "AS IS" disclaimer (§7, §7/§8)
**US frame:** standard, enforceable against commercial users.
**German/BGB:** **§309 Nr. 7–8 BGB** voids certain liability exclusions in AGB;
**§276/§278** set mandatory fault standards. A *total* liability exclusion (§8
"IN NO EVENT ... LIABLE") is **void against consumers** under §309, and
**restricted against businesses** if it excludes gross negligence (§309 Nr. 7a).
**Verdict: 🟡 for German adopters** — the blanket §8 exclusion is fine
B2B if negotiated, but if the Standard Terms are AGB, the total exclusion is
partially void. **Saved for consumers by §9.4 (law controls).** Note for B2B AGB.
**EU:** same consumer-protective direction. **✅ §9.4 saves consumers.**

### R6 — "Governing law and forum" (§12) — exclusive jurisdiction clause
**US frame:** routine forum-selection clause.
**German/BGB / EU:** **Brussels Ibis Regulation (EU) 1215/2015** overrides
private forum choices **for consumers** — a consumer can sue in their own
home court regardless of §12 (Art. 18–19). **Verdict: ✅ §12 is inoperative
against EU consumers** (they sue locally), but valid B2B. OPL doesn't contemplate
consumer-users distinctly — it treats "You" broadly. **Minor gap: OPL should
state that consumer statutory rights/fora are unaffected** (rely on §9.4, but
explicit is better).

### R7 — "arbitration" (§12 last line)
**US frame:** fine.
**German/BGB:** consumer arbitration agreements are restricted (**§§1033–1041a
ZPO**; a consumer can challenge). B2B arbitration is fine. **Verdict: ✅ fine for
B2B; consumer carve-out needed (same as R6).**

### R8 — "injunctive relief / equitable relief" (§12.1)
**US frame:** "equitable relief" is a US-specific remedy label (equity court).
**German/BGB:** no "equity" split; injunctive relief is **§935 ff ZPO**
(einstweilige Verfügung). The *concept* (prevent irreparable harm) exists but the
*label* "equitable relief" is meaningless in Germany. **Verdict: ✅ operative in
substance (injunction exists), but the US label is a translation artifact.**
Cosmetic for German; **potentially confusing in civil-law systems without an
equity tradition (e.g., France, Japan).**

---

## B. Cross-system summary table

| Construct | US/common-law | German/BGB | EU overlay | Other civil-law | Adopter risk |
|---|---|---|---|---|---|
| R1 standing grant (§5) | ✅ native | ✅ bedingte Gewährung | ✅ | ✅ | 🟢 none |
| R2 conclusive evidence (§5) | ✅ | ✅ (party agreement) | ✅ | ✅ | 🟢 none |
| R3 incorporation + rebuttable presumption (§1/§3.3) | ✅ | 🟡 AGB-control / §305c | 🟡 Dir.93/13, 2019/770 | 🟡 | 🟡 medium (German B2B AGB) |
| R4 good faith (§3.3) | ✅ implied | ✅ §242 (stronger) | ✅ | ✅ | 🟢 none |
| R5 liability exclusion (§7/§8) | ✅ | 🟡 void vs consumers per §309 | 🟡 | 🟡 | 🟡 medium (if AGB) |
| R6 exclusive forum (§12) | ✅ | ✅ B2B / ⚠️ consumer override | ⚠️ Brussels Ibis | ⚠️ | 🟡 consumer carve-out |
| R7 arbitration (§12) | ✅ | 🟡 consumer-restricted | 🟡 | 🟡 | 🟡 consumer carve-out |
| R8 "equitable relief" (§12.1) | ✅ native label | ⚠️ label meaningless | ⚠️ | ⚠️ | 🟢 cosmetic |

---

## C. Discrepancies that actually need attention

**1. Consumer-user blind spot (R3, R5, R6, R7).** OPL's "You" is broad and
includes consumers, but the license never distinguishes consumer vs business
users. Under German/EU law, consumers get mandatory rights OPL cannot waive —
§9.4 ("does not supersede applicable law") saves enforceability, but the license
*reads* as if it binds consumers like businesses. **Recommended fix (low-risk
clarification, v1.4.4 or a NOTICE note):** add a sentence to §9.4 or §12 that
"nothing limits mandatory consumer rights or the consumer's right to bring
proceedings in their local court." This is pure hardening, no right changed.

**2. AGB-control exposure for German Maintainer's Standard Terms (R3, R5).** If
the Maintainer's Standard Terms are AGB (almost always true for a published
pricing page), German courts can void surprising/exclusion clauses. OPL can't fix
the Maintainer's *own* Standard Terms, but OPL's own "rebuttable presumption,
User bears initial burden" (§3.3) could itself be challenged as AGB if OPL is
treated as the Maintainer's standard terms. **Recommended fix:** the §3.3 burden
allocation is fine B2B; for safety, note in guidance (not the license) that
German Maintainers should have Standard Terms reviewed for AGB-compliance. **No
license-text change required** — this is advisor guidance.

**3. "Equitable relief" label (R8).** Cosmetic but a real translation artifact for
civil-law adopters (France, Japan, Brazil). **Recommended fix (trivial):** in
§12.1, say "injunctive or other urgent court relief" instead of "equitable
relief." Removes the US-equity assumption.

**4. The US interpretive frame itself (meta).** LEGAL_REVIEW.md and this scan were
reasoned on US doctrine. OPL's stated law is Berlin. **The single highest-value
action before publishing final:** have a German-law practitioner confirm R1–R8,
especially R3/R5 AGB exposure. The license is *draft*; do not publish as final
without that pass.

---

## D. What is NOT a discrepancy (good news)

- **§5 standing grant, §4.1 reachable, §3.2 copyleft, §5.1 DOSP** — all portable
  to civil law; conditional grants, good faith, and versioning are universal.
- **§9.4 ("does not supersede applicable law")** — the single most important
  clause for regional safety; it correctly subordinates OPL to mandatory local
  law, which neutralizes most consumer/EU conflicts automatically.
- **Patent grant (§6)** — standard, portable; termination-for-assertion is
  recognized broadly.

---

## E. Recommended regional-hardening set (optional v1.4.4 or advisor note)

1. **§12 / §9.4 consumer carve-out sentence** — "Mandatory consumer rights and the
   consumer's right to proceedings in their local court are not limited by this
   license." (Closes R6/R7 consumer blind spot; pure hardening.)
2. **§12.1 "equitable relief" → "injunctive or urgent court relief".** (Closes R8
   label artifact.)
3. **Advisor guidance (not license text):** German Maintainers should AGB-review
   their Standard Terms (R3/R5).

None of these change OPL's substance; they make it travel cleanly across the
jurisdictions a real adopter might declare in NOTICE.

---

*Sources note: no external legal-research step (OPL is a private license
instrument). Analysis predicts outcomes on US doctrine and maps to German/BGB and
EU frameworks by analogy; it is not a substituted local-legal opinion. A
qualified German/EU practitioner should confirm R3/R5/R6 before v1.4.3 is
published as final.*
