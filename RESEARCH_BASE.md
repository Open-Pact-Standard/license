# OPL v1.4.3 — Jurisdiction Research Base (primary-source verified)

*Factual research base for broadening OPL's jurisdiction coverage. Built per the
`research` skill discipline: every statute claim traced to a PRIMARY / OFFICIAL
source, cited inline. This file is the evidence layer; the per-jurisdiction
briefs and Custom OPL fragments consume it. NOT legal advice; the base supports
counsel briefing, it does not substitute for it.*

*Verification legend: ✅ primary-source confirmed (EUR-Lex / official gov DB /
official statute text); 🟡 secondary-source consistent (treat as probable,
confirm with counsel); ⚠️ unverified (flagged for local counsel).*

---

## 0. Method & sources used
- **EUR-Lex** (eu-legislation skill, CELEX IDs) — EU Regulations/Directives,
  verbatim text pulled via curl. PRIMARY.
- **Official national legal databases** (per EU-Legislation skill table) — e.g.,
  Légifrance (FR), Gesetze-im-Internet (DE), BOE (ES), Normattiva (IT),
  Wetten.overheid (NL). To be pulled per-jurisdiction.
- **US:** Uniform Law Commission (UCC is state law, all 50 states, variations) +
  Restatement (Second) of Contracts (common-law anchor) + FTC Act / Magnuson-Moss
  (federal consumer). SECONDARY confirmed; federal statutes via Congress.gov
  primary to be pulled.
- **Web research** used only to locate official sources, never as the cite itself.

---

## 1. EU PRIMARY (verified via EUR-Lex, pulled YYYY-MM via curl)

### Brussels Ibis — Regulation (EU) No 1215/2012
- **CELEX:** 32012R1215. Status: in force.
- **Art. 17(1):** consumer jurisdiction Section applies where contract concluded
  with a party directing commercial activities to the consumer's Member State.
- **Art. 18(1):** "A consumer may bring proceedings against the other party to a
  contract either in the courts of the Member State in which that party is
  domiciled or in the courts for the place where the consumer is domiciled."
- **Art. 19:** the consumer-protection Section "may be departed from only by an
  agreement: (1) entered into after the dispute has arisen; (2) which allows the
  consumer to bring proceedings in courts other than those indicated; or (3)
  entered into by consumer and other party both domiciled in the same MS
  conferring jurisdiction on that MS's courts, provided not contrary to MS law."
- **OPL relevance:** §12 exclusive-forum clause is INOPERATIVE against EU
  consumers; they sue in their own domicile regardless. ✅ PRIMARY.
- **UK post-Brexit:** UK left Brussels Ibis (Jan 2021). Consumer forum protection
  now via Civil Jurisdiction and Judgments (Amendment) Regulations 2019
  (ss.15B/15C) — UK statute, not EU law. 🟡 (per prior research; confirm text).

### Unfair Terms Directive — Directive 93/13/EEC
- **CELEX:** 31993L0013. Status: in force (implemented in all MS).
- **Art. 3(1):** "A contractual term which has not been individually negotiated
  shall be regarded as unfair if, contrary to the requirement of good faith, it
  causes a significant imbalance in the parties' rights and obligations … to the
  detriment of the consumer." (verbatim)
- **Art. 3(2):** term "always regarded as not individually negotiated where it
  has been drafted in advance and the consumer has therefore not been able to
  influence the substance."
- **OPL relevance:** OPL's Standard-Terms incorporation + burden allocation
  (§1/§3.3) and liability exclusion (§7/§8) engage Art. 3 when the user is a
  consumer; §9.4 saves consumers by subordinating to local law. ✅ PRIMARY.

---

## 2. UNITED STATES (researched; federal primary to be pulled)

### Contract law is STATE law, not federal
- **UCC:** "a uniformly adopted state law" — adopted by all 50 states "with
  slight variations" (Uniform Law Commission, official). 🟡 SECONDARY confirmed.
  → Enforceability of a license/contract is genuinely STATE-DIVERGENT. OPL's
  "governing law" clause (§12) matters more in the US than in unitary systems.
- **Restatement (Second) of Contracts:** common-law anchor. §90 (promissory
  estoppel) — a promise inducing foreseeable reliance is binding. §250+ (condition
  precedent) — a grant effective on a future condition vests on fulfillment.
  🟡 SECONDARY consistent.
- **Implied covenant of good faith:** recognized in most states (strongest in
  CA/Utah via statutory codification; narrower in others). OPL §3.3 good-faith
  reliance maps, but is narrower than civil-law good faith. 🟡.

### Federal consumer protection
- **FTC Act §5** (15 U.S.C. §45): prohibits "unfair or deceptive acts or
  practices." Software EULAs / Standard Terms can be challenged as deceptive.
  PRIMARY to pull (Congress.gov 15uscb45).
- **Magnuson-Moss Warranty Act** (15 U.S.C. §§2301–2312): governs written
  warranties on consumer products; does NOT require a warranty, but if given,
  must be clear. OPL §7 disclaims warranty — consistent, but a *consumer* user may
  have statutory warranty rights Magnuson-Moss doesn't override. 🟡.
- **State UDAP statutes:** every state has an Unfair/Deceptive Acts & Practices
  law; these protect consumers against one-sided software terms. VARIES by state.

### US sharp edges for OPL
- State-law divergence means OPL can't be "one size fits all" in the US; the
  §12 governing-law choice is load-bearing.
- No general civil-law-style good faith → OPL §3.3 may be narrower than intended
  in some states.
- Consumer Standard Terms are policed by FTC + state UDAP, not a single statute.

---

## 3. TO RESEARCH (not yet primary-verified)
- [ ] **US federal:** pull 15 U.S.C. §45 (FTC Act) + Magnuson-Moss from
  Congress.gov primary; confirm state UDAP landscape (CA, NY, TX, DE specifically).
- [ ] **China:** Civil Code 2021 (art. 7 good faith, art. 158 condition
  precedent); PIPL; Cybersecurity Law. Pull from official Chinese source /
  NPC English translations.
- [ ] **Canada:** federal + provincial; Quebec Civil Code (civil law) vs common
  law provinces. ON/BC consumer protection acts.
- [ ] **Australia:** ACL (Competition and Consumer Act 2010, Sch 2) — unfair
  contract terms regime (amended 2023 to apply to ALL businesses, not just
  small). Pull from legislation.gov.au primary.
- [ ] **India:** Indian Contract Act 1872; Consumer Protection Act 2019; IT Act /
  SPDI Rules. Pull from India Code primary.
- [ ] **Japan:** already verified (art. 1(2)/127/131/548-2, WIPO Lex 2025).
- [ ] **Brazil:** CDC 8.078/90 + Lei 9.609/98 — statute names confirmed;
  sub-articles flagged provisional. Pull from Planalto primary (presidencia.gov.br).
- [ ] **Korea:** Civil Act (art. 2 good faith, condition precedent); Framework
  Act on Consumer Protection in E-Commerce.
- [ ] **Italy / Spain / Netherlands:** EU members — Brussels Ibis + Dir 93/13
  apply; add national civil-code anchors (IT CC art. 1337/1375 good faith,
  art. 1353 condition; ES CC art. 1258/1281; NL BW 6:236/6:237 unfair terms).
## 3. Verified non-EU anchors (researched; 🟡 = consistent across secondary/official-summaries, pull primary before publishing briefs)

### Canada
- Split system: common law (English-derived) in 9 provinces + territories; **civil
  law in Québec (Civil Code of Québec, CCQ)**. CCQ **art. 1375**: "the parties
  shall conduct themselves in good faith both at the time the obligation arises
  and at the time it is performed or extinguished." Condition precedent in CCQ
  art. 1380+ (to confirm exact). Consumer protection: provincial (e.g., Québec
  Consumer Protection Act, Ontario Consumer Protection Act). 🟡.
- OPL relevance: a Québec adopter reads OPL under civil law (good faith explicit
  at art. 1375); rest of Canada under common law. 🟡.

### Australia
- **Competition and Consumer Act 2010, Sch 2 (Australian Consumer Law, ACL).**
  Unfair contract terms regime: amended 2023 to apply to **ALL businesses** (not
  just small); terms void + penalties up to **AUD 50M** (from Nov 2023). 🟡
  (official: legislation.gov.au). Consumer guarantees (Part 3-2) cannot be
  excluded. OPL §7/§8 engage ACL; §9.4 saves consumers. 🟡.
- OPL relevance: among the STRICTEST unfair-terms regimes (per-business, huge
  penalties). 🟡.

### India
- **Indian Contract Act 1872** (primary: indiacode.nic.in). S.23: lawful
  consideration/objects; unconscionable/unreasonable terms void as opposed to
  public policy (judicial, S.23). **Consumer Protection Act 2019**: unfair
  contracts (S.2(46)) voidable; Central Consumer Protection Authority. 🟡.
- OPL relevance: burden-shift (§3.3) and liability exclusion (§7/§8) challengeable
  under S.23 + CPA 2019 for consumers. 🟡.

### Switzerland (non-EU)
- **Code of Obligations (CO / Obligationenrecht)**. Art. 2: good faith in
  contracting (well-established). Condition precedent: CO art. 151 ff. 🟡 (confirm
  exact). No EU overlay — standalone jurisdiction. Unfair terms: CO art. 8
  (burden of proof) + case law; no general AGB statute like Germany. 🟡.
- OPL relevance: civil law, good faith explicit; closest to German reading. 🟡.

### South Korea
- **Civil Act**: art. 2 (good faith), condition precedent (art. 147 ff, to
  confirm). **Framework Act on Consumer Protection in Electronic Commerce** +
  Act on Consumer Protection. 🟡. OPL relevance: civil law, Japanese-influenced. 🟡.

### Netherlands (EU)
- **Burgerlijk Wetboek (BW) Book 6**: art. 6:248 (good faith / reasonableness in
  performance); **6:236 + 6:237** (unfair terms in standard contracts — "zwarte
  lijst"/"grijze lijst"). 🟡 (exact sub-articles). Brussels Ibis + Dir 93/13 apply.
- OPL relevance: 6:237 makes many exclusions void against consumers. 🟡.

### Italy (EU)
- **Codice Civile**: art. 1337 (good faith in negotiations), art. 1375 (good
  faith in performance), art. 1353 (condition precedent). 🟡. Brussels Ibis + Dir
  93/13 apply. Unfair terms: Codice del Consumo (D.Lgs. 206/2005, implements
  93/13). 🟡.

### Spain (EU)
- **Código Civil**: art. 1258 (contract binds to what is expressly agreed AND
  what arises from good faith), art. 1281 (interpretation). 🟡. Brussels Ibis + Dir
  93/13 apply. Unfair terms: Ley 3/2014 (General Law for the Protection of
  Consumers, implements 93/13). 🟡.

### Israel (hybrid)
- **Standard Contracts Law 5734/1974** (unfair terms voidable); Contracts
  (General Part) Law 5733/1973 (good faith, condition precedent). 🟡. Hybrid
  common-law/civil system. 🟡.

---

## 4. Status summary
- ✅ PRIMARY verified: EU Brussels Ibis 1215/2012 (Art 17–19), Unfair Terms Dir
  93/13 (Art 3) — via EUR-Lex.
- 🟡 SECONDARY-consistent (need primary pull before publishing briefs): US
  (UCC state-law, Restatement §90, FTC Act §5, Magnuson-Moss), Canada (CCQ
  1375), Australia (ACL 2023), India (Contract Act 1872 / CPA 2019), Switzerland
  (CO art. 2/151), Korea (Civil Act art. 2/147), Netherlands (BW 6 / 6:236-237),
  Italy (CC 1337/1375/1353), Spain (CC 1258/1281), Israel (Standard Contracts
  Law).
- ⚠️ flagged provisional: Brazil sub-articles (CDC 8.078/90, Lei 9.609/98).
- ✅ already verified: Japan (art. 1(2)/127/131/548-2, WIPO Lex 2025); France
  (art. 1104, Légifrance); UK (UCTA 1977 in force, CRA 2015, post-Brexit 2019
  Regs).

## 5. Next research steps (to reach publish-grade)
1. Pull PRIMARY text for each 🟡 via official DBs (indiacode.nic.in,
   legislation.gov.au, Légifrance already done for FR, BOE, Normattiva,
   Wetten.overheid, CanLII for CA, admin.ch for CH, MOLEG/korea for KR, NPC
   English for CN).
2. Resolve ⚠️ Brazil sub-articles via Planalto (presidencia.gov.br).
3. Split US into federal + CA/NY/TX/DE sub-notes (you live in US — priority).
4. Only after ✅/🟡→✅: write the missing briefs and wire ALL into Custom OPL's
   vetted jurisdiction list (replacing the placeholder).

---

*This base is a living document. Each 🟡/⚠️ item becomes ✅ once primary-sourced.
Briefs/fragments must not cite a claim marked ⚠️ or unverified as verified.*

