# OPL v1.4.3 — Multi-Jurisdiction Discrepancy Scan

*Follow-on to LEGAL_REVIEW.md (adversarial ambiguity review). LEGAL_REVIEW assumed
a US interpretive frame and flagged that OPL's stated governing law is Berlin,
Germany. This scan goes further: **OPL is a template license — adopters declare
their OWN governing jurisdiction in NOTICE.** So the license must not carry
hidden US-specific constructs that misfire when an adopter in France, the UK,
Japan, Brazil, or elsewhere applies it under their law. We scan the most likely
adopter jurisdictions plus the common-law/civil-law split.*

*Method: read the text for Anglo-American legal constructs; map each against
German/BGB (OPL's own stated law), France (Code civil), UK (UCTA/CRA), Japan
(Civil Code), Brazil (Lei 9.609/CDC), and EU overlay. Flag where a construct is
void/voidable, flips meaning, or is inoperative. Severity = adopter-exposure if
they rely on the clause under that law. Not legal advice; qualified local counsel
needed before publishing v1.4.3 as final. Anchors verified by web search where
marked; Brazil article-level claims are flagged unverified.*

---

## 0. The template-license problem

OPL's §12 lets the adopter name any "Governing Jurisdiction" in NOTICE. OPL v1.4.3
is therefore simultaneously:
- a **German-law instrument** (origin-canary declares Berlin), AND
- a **French / UK / Japanese / Brazilian / etc. instrument** for other adopters.

The license text uses US-equity and US-contract vocabulary throughout ("standing
grant," "conclusive evidence," "equitable relief" [fixed in v1.4.3 → "urgent
court relief"], "incorporated by reference," "rebuttable presumption"). Each must
survive translation into the adopter's system. This scan tests that.

---

## 1. The constructs, system by system

### C1 — Conditional / "standing" grant (§5 abandonment → Apache-2.0)
| System | Treatment | Risk |
|---|---|---|
| US/common-law | Condition precedent; self-executing. ✅ | 🟢 |
| **Germany (BGB §158)** | Bedingte Rechtsgeschäfte — condition precedent valid; grant vests on condition without formal act (see GERMAN_LAW_BRIEF #1). ✅ | 🟢 (confirm) |
| **France (C. civ.)** | Condition suspensive (art. 1304-1 ff, formerly 1181) — valid; vests on event. ✅ | 🟢 |
| **UK** | Condition precedent under common law; enforceable. ✅ | 🟢 |
| **Japan (Civil Code art. 127)** | "A juridical act subject to a condition precedent becomes effective upon fulfillment." Explicit. ✅ | 🟢 |
| **Brazil (CC art. 135)** | Condição suspensiva recognized. *(CC art. 135 unverified — flag.)* | 🟡 unverified |

**Verdict:** the §5 standing grant is the MOST PORTABLE clause — every major
system recognizes conditional grants. Low risk everywhere. Germany needs the
formal-act confirmation (brief #1); Brazil needs article verification.

### C2 — "Conclusive evidence" (§5 successor recording)
| System | Treatment | Risk |
|---|---|---|
| Germany (ZPO §292) | Evidentiary weight by agreement permissible between parties. ✅ | 🟢 |
| France | Preuve — parties may agree probative weight; a private writing (LICENSE commit) is admissible. ✅ | 🟢 |
| UK | Evidence Act 1995 — evidence is for the tribunal; "conclusive" stipulations between parties generally upheld. ✅ | 🟢 |
| Japan | Evidence rules dispositive between parties. ✅ | 🟢 |
| Brazil | Same. ✅ | 🟢 |

**Verdict:** the standing grant (C1) is the operative mechanism; "conclusive
evidence" is label-only. Cosmetic everywhere.

### C3 — Incorporation by reference + burden allocation (§1, §3.3)
| System | Treatment | Risk | Verified |
|---|---|---|---|
| Germany (BGB §305c, §307, §309) | AGB-control: burden-shifting/surprise clauses scrutinized. 🟡 (brief #3) | 🟡 | ✅ |
| France (C. consom. L212-1; ex-Dir 93/13) | Unfair terms void against consumers; "core" price terms exempt but opacity/surprise attacked. 🟡 | 🟡 | ✅ |
| UK (UCTA 1977 s.2–3; CRA 2015 s.62) | Business liability exclusions need *reasonableness*; consumer terms must be *fair*. A burden-shift on a consumer likely fails. 🟡 | 🟡 | ✅ (UCTA 1977 in force, no outstanding effects; CRA 2015 live) |
| Japan (CCA art. 1(2) good faith; consumer statutes) | Good faith + consumer protection; one-sided terms challengeable. 🟡 | 🟡 | ✅ (art.1(2), 127/131 current per WIPO Lex 2025) |
| Brazil (CDC 8.078/90 art. 51; Lei 9.609/98) | Unconscionable/one-sided clauses void (art. 51); software protected by Lei 9.609/98. 🟡 | 🟡 | ⚠️ statute names verified; specific article sub-numbers unverified |

**Verdict:** the SAME AGB/unfair-terms exposure appears in EVERY system — not
just Germany. OPL's "User bears initial burden" (§3.3) and its Standard-Terms
incorporation face consumer-protection challenge universally. §9.4 ("does not
supersede applicable law") saves consumers in all systems; the B2B posture needs
per-system confirmation. **This is the cross-jurisdiction headline finding.**

### C4 — Good faith "honors in good faith" (§3.3)
| System | Treatment | Risk |
|---|---|---|
| Germany (§242) | Treu und Glauben — explicit, stronger than US. ✅ | 🟢 |
| France (art. 1104) | "Contracts must be negotiated, formed AND performed in good faith" — post-2016 reform, explicit at formation. ✅ | 🟢 |
| UK | Implied duty of good faith in some contexts (not universal, but relational contracts recognized post-2019). ⚠️ narrower than civil law | 🟢 (operative) |
| Japan (art. 1(2)) | "Exercise of rights and performance of duties must be in good faith." Explicit. ✅ | 🟢 |
| Brazil (CC art. 422) | "The parties are bound by good faith obligations in contract formation and performance." Explicit. ✅ | 🟢 |

**Verdict:** good faith is a NEAR-UNIVERSAL civil-law principle and increasingly
UK/common-law too. OPL's §3.3 maps cleanly everywhere. Lowest-risk clause.

### C5 — Liability exclusion "IN NO EVENT" (§7/§8)
| System | Treatment | Risk | Verified |
|---|---|---|---|
| Germany (BGB §309 Nr.7–8) | Total exclusion void vs consumers; restricted vs businesses (gross negligence). 🟡 | 🟡 | ✅ |
| France (C. consom. art. L212-1; CC art. 1231-5) | Exclusions of liability void vs consumers; limited vs businesses. 🟡 | 🟡 | ✅ |
| UK (UCTA s.2–3) | Business liability exclusion needs *reasonableness* (s.11 test); cannot exclude death/personal-injury negligence at all. 🟡 | 🟡 | ✅ (UCTA 1977 in force) |
| Japan | Tort/contract liability limits scrutinized; consumer protection. 🟡 | 🟡 | ✅ |
| Brazil (CDC art. 24–25) | Liability for consumer damage cannot be excluded; relative/initial liability. 🟡 | 🟡 | ⚠️ art. refs unverified |

**Verdict:** blanket liability exclusion is ATTACKED IN EVERY SYSTEM against
consumers, and restricted against businesses. OPL's §9.4 saves consumers
everywhere; the B2B posture varies (UK reasonableness test is the strictest).
**OPL should note that B2B users in the UK need a reasonableness assessment.**

### C6 — Forum selection + arbitration (§12)
| System | Treatment | Risk | Verified |
|---|---|---|---|
| Germany / EU (Brussels Ibis Art.18–19) | Consumer may sue locally regardless of §12. 🟡 (brief #5) | 🟡 | ✅ |
| France (ex-Dir 93/13; Brussels Ibis) | Same consumer override. 🟡 | 🟡 | ✅ |
| UK (post-Brexit: CJJA 2019 Regs, not Brussels Ibis) | UK left Brussels Ibis (Jan 2021). The Civil Jurisdiction and Judgments (Amendment) Regulations 2019 retain consumer protective forum rules (sections 15B/15C) — UK consumers still sue locally; B2B forum clauses enforceable if reasonable. 🟡 | 🟡 | ✅ (nuanced — Brussels Ibis no longer binds UK) |
| Japan | Forum selection enforceable; consumer mandatory-forum rights under consumer statute. 🟡 | 🟡 | ✅ |
| Brazil (CDC art. 101) | Consumer may sue in their own domicile; forum clause void vs consumer. 🟡 | 🟡 | ⚠️ art. ref unverified |

**Verdict:** consumer forum override is UNIVERSAL (Brazil art. 101 is the
strongest — consumer sues at home). OPL's v1.4.3 §9.4 consumer carve-out handles
it; confirm wording covers all systems. UK-specific note: post-Brexit the
override rests on UK statute (2019 Regs), not EU law.

### C7 — "Urgent court relief" (§12.1) [was "equitable relief"]
| System | Treatment | Risk |
|---|---|---|
| Germany (§935 ff ZPO, einstweilige Verfügung) | Exists. ✅ | 🟢 |
| France (référé, art. 808 CPC) | Exists. ✅ | 🟢 |
| UK (injunctive relief) | Exists. ✅ | 🟢 |
| Japan (shihō rensai / provisional disposition) | Exists. ✅ | 🟢 |
| Brazil (tutela provisória, CPC art. 300) | Exists. ✅ | 🟢 |

**Verdict:** v1.4.3's "urgent court relief" wording travels cleanly; the old
"equitable relief" US-equity label is gone. Cosmetic-only fix, now portable.

---

## 2. Cross-jurisdiction synthesis

**Clauses that travel cleanly everywhere (no action):** C1 standing grant, C2
conclusive evidence, C4 good faith, C7 urgent relief. These are universal.

**Clauses with UNIVERSAL consumer/B2B exposure (the real finding):** C3
(incorporation + burden), C5 (liability exclusion), C6 (forum). Every system
protects consumers against these and scrutinizes B2B. OPL's §9.4 is the
cross-system safety valve — it correctly subordinates OPL to mandatory local law
in ALL systems, so consumers are protected by operation of §9.4 alone.

**The genuine license-text question (not just advisor):** does OPL's B2B
posture need per-system tailoring? Answer: NO for consumers (§9.4), but OPL could
add a one-line note that B2B users should assess local AGB/unfair-terms/
reasonableness rules. This is advisor guidance, not a text change — OPL stays
jurisdiction-neutral by design.

**UK-specific sharp edge:** UCTA's *reasonableness test* (s.11) is stricter than
continental AGB-control for B2B — a UK B2B user relying on OPL's liability
exclusion should know it's subject to reasonableness. Worth a UK-specific advisor
note.

---

## 3. Recommended multi-jurisdiction hardening (all clarification, no substance)

1. **§9.4 consumer carve-out (DONE v1.4.3)** — covers DE/FR/UK/JP/BR consumers via
   §9.4 + explicit sentence. Universal fix.
2. **§12.1 "urgent court relief" (DONE v1.4.3)** — portable label.
3. **Advisor note (new, recommend adding to OPL guidance, not the license):**
   "B2B users should assess OPL's liability exclusion and Standard-Terms
   incorporation against local unfair-terms / AGB / reasonableness rules
   (e.g., Germany §307 BGB, UK UCTA s.11, France L212-1, Brazil art. 51)."
4. **Brazil article verification** — the CC/CDC/Lei 9.609 article numbers cited
   above are unverified; a Brazilian practitioner should confirm before any
   Brazil-specific claim is published.

---

## 4. Per-jurisdiction practitioner briefs

The German brief exists (GERMAN_LAW_BRIEF.md). For full multi-jurisdiction
coverage before publishing final, parallel briefs for **France, UK, Japan,
Brazil** should confirm the C3/C5/C6 exposures under local statutes. This scan
provides the clause→statute mapping; the briefs turn it into confirm/correct
questions per system.

---

*Sources — cross-referenced by web research (Aug 2026), not merely recalled:
- **France:** Code civil art. 1104 (Légifrance — in force since 1/10/2016, no
  subsequent change); consumer unfair terms via Code de la consommation L212-1
  (implements ex-Dir 93/13). ✅ verified current.
- **UK:** UCTA 1977 (legislation.gov.uk — "no known outstanding effects", still
  in force); CRA 2015 (consumer unfair terms, Part 2). Post-Brexit: UK left
  Brussels Ibis (Jan 2021); Civil Jurisdiction and Judgments (Amendment)
  Regulations 2019 retain consumer forum protection (ss.15B/15C). ✅ verified,
  with the Brexit nuance noted.
- **Japan:** Civil Code art. 1(2) (good faith), art. 127/131 (condition
  precedent) — Japanese Law Translation / WIPO Lex (2025 version). ✅ verified
  current.
- **Brazil:** CDC 8.078/90 art. 51 (void unconscionable terms) + art. 101
  (consumer forum); Lei 9.609/98 (software). ⚠️ statute names verified; specific
  article sub-numbers should be confirmed by a Brazilian practitioner (web search
  returned non-authoritative sources for sub-articles).
- **Germany:** BGB §§158, 242, 305c, 307, 309, 309 Nr.7–8, ZPO §§292, 935 ff;
  Brussels Ibis Art.18–19 — per GERMAN_LAW_BRIEF.md (to be confirmed by German
  counsel).

No external legal-research step on the license text itself (read on four
corners); statute anchors confirmed by web search and marked ✅/⚠️ above. This is
analysis to inform counsel, not a substituted local-legal opinion.*
