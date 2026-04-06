# ROUND 10 ADVERSARIAL ANALYSIS — OPL-1.1 (Post-Round-9-Patches)

## Analyst: Adversarial Legal Analyst
## Date: April 6, 2026
## Target: OPL-1.1 license text, MINIMAL_SETUP.md, REGISTRY_TEMPLATE.json

---

## SCENARIO 1: The "Clear and Convincing" Burden-of-Proof Trap (Section 3.2.4)

SCENARIO:
AcmeCorp, a 500-employee company, incorporates a small OPL-licensed utility library
(200 lines of code) into its $50M/year SaaS platform. The Project Registry for that
library publishes a fee of $10,000/year (Tier3_Organization). AcmeCorp believes this
is disproportionate since the library represents perhaps 0.05% of their product's
functional value. In any enforcement action, AcmeCorp must rebut the presumption
of proportionality.

LOOPHOLE: Section 3.2.4 states: "the Licensee bears the burden of demonstrating that
the published compensation is NOT proportionate... by clear and convincing evidence."
"Clear and convincing evidence" is a legal evidentiary standard significantly higher
than the ordinary "preponderance of the evidence" standard used in civil contract
disputes. In most U.S. jurisdictions, "clear and convincing" requires evidence that
the fact-finder have a "firm belief or conviction" in the truth of the allegation —
roughly 75% certainty vs. 51% for preponderance. This is typically reserved for
fraud, patent invalidity, or termination of parental rights. A standard commercial
fee dispute almost never carries this burden.

A corporate lawyer would argue that: (a) the "clear and convincing" standard is
contractually unconscionable when unilaterally imposed via an adhesive license;
(b) no court would enforce an evidentiary burden higher than the statutory standard
for the cause of action; OR (c) even if the standard is upheld, the Licensee can
simply concede the fee is proportionate under the 3.2.4 factors (Total Workforce,
integration extent, market rates) and instead argue the fee isn't owed at all under
a different theory — such as the license conditions being unenforceable — thereby
sidestepping the proportionality framework entirely.

Moreover, the text says: "The presumption of proportionality does not apply where
the Licensee has never received a copy of the Registry-published fee schedule."
(Section 3.2.4, last sentence). A corporation can argue it never "received" the
fee schedule merely because the Registry URL was only in a LICENSE.md file it
cloned via git — the corporation never affirmatively viewed it. This creates an
all-or-nothing escape hatch: if you never saw the Registry, there's no presumption,
and the Steward must prove proportionality from scratch.

PRINCIPLE_VIOLATION: Principle 2 (Fair Compensation) — The fee structure is designed
to ensure fair compensation, but the "clear and convincing" language is so extreme
that a court may strike the entire proportionality clause as unconscionable, leaving
no mechanism to determine what a fair fee actually is. Alternatively, Principle 4
(Dynamic Pricing) is undermined because the "never received" carve-out lets any
company claim ignorance and avoid the Registry's authority entirely.

SEVERITY: HIGH

FIX RECOMMENDATION:
- Replace "by clear and convincing evidence" with "by a preponderance of the evidence"
  which is the standard for civil disputes and would hold up in court.
- Replace "never received a copy" with "could not reasonably have discovered the
  Registry-published fee schedule through publicly available means" — this closes
  the clone-without-viewing escape hatch while protecting against genuinely hidden
  registries.
- Add: "The burden of demonstrating proportionality shall not require evidence
  exceeding the standard applicable in civil proceedings in the governing jurisdiction."

---

## SCENARIO 2: The Fallback JSON Registry Authenticity Void (Section 1.19 + REGISTRY_TEMPLATE.json)

SCENARIO:
DataMine Inc. is training an AI model using code from "QuickUtil," a solo-developer
project that has no smart contract and only a REGISTRY.json file in its GitHub repo.
The Steward of QuickUtil is a pseudonymous developer "dev@example.com" who hasn't
responded to email in 8 months. DataMine checks the REGISTRY.json, finds an
AI training fee of $10,000, but notes that: (a) the JSON file has no cryptographic
signature or attestation; (b) anyone could edit this file and commit it (the Steward's
GitHub account could be compromised); (c) there is no canonical identifier linking
the person who controls the repo to the Steward identity in the file.

DataMine argues that REGISTRY.json does not satisfy the "Project Registry" requirement
because Section 1.19 requires "tamper-evident records" and the JSON file offers no
tamper evidence — anyone with push access to the repo can silently edit it. Furthermore,
without a smart contract or cryptographic signature, DataMine can claim no reasonable
reliance on the published fee because the fee could have been changed without notice
or proof. DataMine pays nothing and waits for enforcement. When sued, they argue
that the Steward failed to maintain a valid Project Registry (Section 1.19), meaning
no fee schedule was ever lawfully published, and Section 3.2.3's good-faith negotiation
requirement cannot be triggered because there's no authoritative fee to negotiate against.

This is amplified because MINIMAL_SETUP.md (Tier 1) explicitly states that the JSON
file "Satisfies OPL-1.1's 'Project Registry' requirement." But the LICENSE.md itself
(Section 1.19) requires "tamper-evident records." A plain text JSON file in a git
repo — without hash pinning or signatures — is not genuinely tamper-evident outside
the context of git history, which is not referenced by the license.

PRINCIPLE_VIOLATION: Principle 4 (Dynamic Pricing) — The Registry is supposed to be
the authoritative source for fees, but if its authenticity can be challenged for
JSON-only projects, then the Registry's authority collapses for the vast majority
of solo/small projects that cannot or will not deploy smart contracts. This creates
a fundamental contradiction: the license says the Registry is authoritative, but
the fallback mechanism doesn't meet the technical requirements the license itself
specifies.

SEVERITY: HIGH

FIX RECOMMENDATION:
- In Section 1.19, add explicit language that a file published in the canonical
  source repository (e.g., REGISTRY.json in the repository root) constitutes a
  tamper-evident record through the version control system's commit history.
  Language: "For projects not using on-chain infrastructure, a Registry file
  published in the canonical source repository with accessible version-control
  history (e.g., git) shall be deemed tamper-evident for purposes of this License."
- Require the REGISTRY.json template to include a GPG signature field or similar
  cryptographic attestation from the Steward.
- Add a notice provision: the Steward must sign registry changes, or the previous
  version remains effective for any Licensee who registered under it.

---

## SCENARIO 3: The "De Minis" Revenue Attribution Shell Game (Section 4.3(d) + Section 5.2)

SCENARIO:
MegaMind AI Corp trains a foundation model on 10,000 open-source projects, including
47 OPL-licensed projects. The model generates $100M in annual API revenue. MegaMind's
legal team structures the product so that the OPL-influenced domains (code generation)
are described as "experimental features" in the model card. They attribute the
$100M revenue to: (a) enterprise subscriptions for general AI chat ($60M), (b) image
generation features ($30M), and (c) the code completion feature ($10M). They then
argue that only the $10M code completion revenue is "attributable to the model or
its outputs" in the "relevant domain" mentioned in Section 4.3(d).

The de minimis threshold in the REGISTRY_TEMPLATE.json is $100/year for derivative
works (Section 5.2 references this). But Section 4.3(d) uses a different standard:
"generating more than the de minimis threshold defined in Section 5.2 in annual
revenue attributable to the model or its outputs." The problem is that "revenue
attributable to the model or its outputs" is narrower than the Section 5.2 definition
of "revenue derived from that Derivative Work." A model company can argue their
subscription revenue is attributable to the platform, the brand, the infrastructure —
not specifically to the model's outputs. The specific $10M from code completion
is still well above the $100 de minimis, but the model company can then argue that
the SOFTWARE's specific contribution (a single 200-line utility library among 10,000
training sources) is not "substantial" under 4.3(d) because the language says:
"'trained substantially' means that the Software's code, patterns, or structures
contributed to the model's capabilities in the relevant domain." The company argues
the contribution is not demonstrated — the training logs don't track per-source
contribution, and the model card only lists the project name as required by 4.3(a).

Even worse: Section 4.3(d) triggers Section 5.2 obligations, which say "if You
distribute a Derivative Work... and collect royalties." But a model company
does not "distribute" a model in many cases — they offer API access. While
Section 1.14's definition of Royalties includes "hosted or managed service,"
Section 5.2's trigger is specifically about "distribut[ing] a Derivative Work."
An API endpoint does not clearly constitute "distribution" of the derivative
(the weights-trained model itself). The model is accessed, not distributed.
This is a fundamental ambiguity: Section 5.2 was written for software
derivatives, not trained models.

PRINCIPLE_VIOLATION: Principle 3 (AI Transparency — "Train on code = disclose it;
clone it = reciprocate") and Principle 2 (Fair Compensation). The language fails
to capture the revenue model of API-based model providers who never "distribute"
their models, and the "trained substantially" standard has no operational definition
for multi-source training scenarios.

SEVERITY: CRITICAL

FIX RECOMMENDATION:
- Add explicit language in Section 4.3(d): "For the avoidance of doubt, offering
  access to a trained model via API, SaaS, or any hosted service constitutes
  'distribution' for purposes of Section 5.2."
- Define "trained substantially" with a measurable threshold, e.g., "The Software
  appears in the training dataset for the model (as evidenced by the Licensee's
  training records), and: (a) the model includes capabilities in a domain for
  which the Software provides non-trivial functionality, and (b) the Licensee
  has not explicitly excluded the Software from its training data."
- Create a specific revenue attribution formula for multi-source AI training:
  when OPL code is among multiple training sources, each Steward is entitled to
  a pro-rata share based on lines-of-code, file count, or the Licensee's own
  documented proportional contribution metric. Require the Licensee to declare
  the methodology used.

---

## SCENARIO 4: The Abandoned-Project Derivative Deadlock (Section 5.2(a))

SCENARIO:
"WebToolkit" was an OPL-licensed project whose solo Steward, "Jane Doe," passed
away in 2024 without transferring stewardship. No estate has come forward. The
project hasn't been updated since 2024 and no one has updated its Project Registry.
BobCorp finds WebToolkit, creates a Derivative Work called "WebToolkit Pro," and
generates $2M in revenue from it. Under Section 5.2(a), BobCorp must pay the
original Steward a proportional share of royalties "as defined in the Project
Registry of the ORIGINAL Software."

Here's the problem: the last line of Section 5.2(a) states: "Where no rate is
published in either Registry, the Derivative Work may not be distributed
commercially until a rate is established." If the original Steward is dead and
no one is maintaining the Registry, no rate can be newly established or confirmed.
Even if an old rate exists in the old Registry, BobCorp may argue:
- the Steward is no longer valid (Section 15.6 transfer hasn't occurred),
- no one has authority to receive payments,
- therefore the condition "derivative royalty percentage is NOT fixed by this License
  document" means there is no mechanism to pay anyone.

But the critical deadlock is narrower: if the original Registry published a rate
BUT the Steward is unreachable, BobCorp technically cannot register or pay because
there's no functioning recipient. Section 5.3 says the Derivative Work must
"register its link to the original Software's Project Registry" — but the link
is to a dead project. Section 15.6 covers steward transfer on death, but only
if a successor assumes stewardship within 90 days. If we're past that, Section 15.6(iv)
says "stewardship and all associated obligations shall transfer to the community
of Contributors." But if there are active Contributors, they must elect an interim
Steward within 30 days. If they don't, there's a governance vacuum.

During this vacuum, BobCorp argues Section 5.2(a) prevents commercial distribution
because "the Project Registry of the ORIGINAL Software" has no functioning Steward
to validate or receive payments. The "may not be distributed commercially" language
is an absolute prohibition without a time limit, sunset clause, or escrow mechanism.

Section 16.2 (Sunset) requires 36 months of inactivity AND fewer than 3 Active
Participants. If BobCorp itself becomes an Active Participant (as a Collaborator
filing bugs/issues), they could trigger the "below 3 Participants" count to go UP
rather than down, ironically preventing sunset. Or, if there are 2+ other active
participants, sunset never triggers.

BobCorp simply sits on its Derivative Work, generates $2M/year, pays nobody, and
dares anyone to enforce. Any enforcement action faces the problem that the Steward
is dead, the Contributors haven't organized, and Section 5.2 says "may not be
distributed commercially until a rate is established."

PRINCIPLE_VIOLATION: Principle 2 (Fair Compensation) — Paradoxically, the provision
designed to ensure fair compensation for the original Steward also prevents
ANYONE from being compensated, because no functioning mechanism exists to
establish a rate when the Steward is dead and the Contributor community hasn't
organized. Nobody gets paid, and the public gets no commercial product either.
Principle 1 (Humans First) — This prevents individuals from building on dead
projects commercially, which is the opposite of what the license intends.

SEVERITY: CRITICAL

FIX RECOMMENDATION:
- Add a "Steward Vacuum" clause to Section 5.2: "Where the original Steward is
  unreachable for a period exceeding twelve (12) months, or where a successor
  has not assumed stewardship within the period specified in Section 15.6, and
  no rate is published in the original Software's Project Registry: (a) the
  Derivative Work may be distributed commercially at a rate of the smallest
  fee tier published in the Derivative Work's own Registry, or ten percent (10%)
  of gross revenue derived from the Derivative Work, whichever is less, paid
  into an escrow account designated for the original Steward or community;
  (b) such escrow funds shall be released to the successor Steward upon
  assumption of stewardship, or after thirty-six (36) months shall be distributed
  to the Contributors of the original Software in proportion to their accepted
  Contributions."
- Section 16.2 sunset should be triggered by the absence of a reachable Steward,
  not just inactivity of the repository.

---

## SCENARIO 5: The Two-Tier Registry Enforcement Asymmetry (Section 1.19 + Section 3.2.1 + MINIMAL_SETUP.md)

SCENARIO:
Two competing OPL projects exist:
- Project A (smart contract): A well-funded project with a RoyaltyRegistry smart
  contract on Ethereum. Fees are immutable on-chain. License Records are published
  automatically. Canary tokens are embedded. Full enforcement stack (Tier 3).
- Project B (JSON fallback): A solo developer's utility library with only a
  REGISTRY.json file in the repo. No smart contract. The Steward is responsive
  but lacks infrastructure. Tier 1 setup.

BigCorp Inc. wants to use both. For Project A, BigCorp pays because the smart
contract automatically detects non-compliance via canary tokens, and enforcement
is automatic and forensically provable. For Project B, BigCorp simply doesn't pay.
Why? Because:
  1. The REGISTRY.json has no automated collection mechanism.
  2. BigCorp argues they never received the fee schedule ("never received a copy"
     — Section 3.2.4 last sentence).
  3. Even if they did, the JSON file could have been modified at any time by
     someone with write access (Section 1.19's "tamper-evident" requirement is
     arguably unmet by a plain JSON file as discussed in Scenario 2).
  4. There is no License Record to verify or refute — the JSON Registry doesn't
     maintain a list of Licensees.
  5. BigCorp argues the Steward of Project B didn't "designate" the Registry
     properly — the URL was in LICENSE.md but not in a prominent README notice
     as suggested in MINIMAL_SETUP.md.

BigCorp pays for Project A (on-chain, automated, expensive to evade) and ignores
Project B (JSON-only, hard to prove non-compliance). This creates a two-tier
enforcement system where the license's protections are effectively nullified
for all projects that cannot afford smart-contract deployment — precisely the
small and solo projects the license was designed to protect.

More specifically, Section 3.2.1 says: "If the License Steward publishes the
Registry URL in the Software's repository (e.g., in LICENSE.md, README, or
package metadata), that URL shall be presumed canonical." But "presumed"
canonical doesn't mean "is" canonical — it just creates a presumption. A
corporate lawyer can rebut this presumption by arguing the Steward didn't
formally "designate" the Registry (note that 3.2.1 says "designated by the
License Steward at the time of registration" as the primary standard, while
publishing in LICENSE.md is just a presumption). If the Steward is a solo dev
who just dropped LICENSE.md and REGISTRY.json in their repo without an explicit
designation statement, the corporation argues no valid designation occurred.

PRINCIPLE_VIOLATION: Principle 2 (Fair Compensation) — The fallback Registry
creates a de facto two-tier system where small/solo projects cannot actually
enforce compensation despite the text promising they can. Principle 5 (Community
Compensation) — Royalties cannot flow to contributors if the enforcement
mechanism for smaller projects is practically non-existent, meaning those
projects' contributors receive nothing. Principle 1 (Humans First) — This
effectively punishes individual developers by making their projects easier
to exploit without paying than well-funded projects with enforcement
infrastructure.

SEVERITY: HIGH

FIX RECOMMENDATION:
- Add to Section 1.19: "A REGISTRY.json (or REGISTRY.md) file published in the
  root of the Software's canonical source repository, by the repository owner or
  a person with documented write access, shall constitute a valid designation
  of the Project Registry for purposes of this License."
- Add a minimum compliance requirement for Licensees: "A Licensee engaged in
  Commercial Use or AI Training Use of the Software has an affirmative duty to
  locate the Project Registry by checking (i) LICENSE.md, (ii) README.md, and
  (iii) package metadata files. Failure to check these locations does not
  constitute a defense against enforcement."
- Add to Section 3.2.4: "The presumption of proportionality also applies to
  fee schedules published via the fallback JSON Registry mechanism. The Licensee
  cannot challenge the authenticity of a fallback Registry solely on the basis
  that it is not an on-chain smart contract."

---

## SCENARIO 6: The Truncated Section 11.3 and the Incomplete Personal Use Exception

SCENARIO:
Section 11.3 "Personal Use Exception" on lines 825-826 reads:
  "### 11.3 Personal Use Exception
   This License expressly does not restrict the ability of any person or"
That's it. The section is truncated — it ends mid-sentence with "any person or"
and then immediately jumps to "## SECTION 12: VERSIONS AND UPDATES."

A corporate lawyer reviewing this license would immediately spot the truncated
section and argue: (a) the license is internally contradictory or incomplete;
(b) any ambiguity in an adhesive license should be construed against the
drafter (contra proferentem doctrine); (c) the apparent intent was to create
a broad personal use exception, and the fact that it's truncated means the
exception's scope cannot be determined, making the entire clause unenforceable
under the doctrine of severability; (d) if Section 11.3 is unenforceable, it
may create a cascade effect on Sections 2, 9, and 10, all of which reference
Personal Use definitions and exceptions.

More concretely, a defendant in an enforcement action could file a motion to
strike all sections referencing or depending on Section 11.3, arguing the
license is materially incomplete and therefore the agreement was never fully
formed. While this is a weaker legal argument, it creates litigation leverage:
the Steward must either (1) concede the truncation and explain what was omitted,
which gives the defendant discovery into draft versions and drafting intent,
or (2) litigate over an obviously broken section, which makes the entire
license appear sloppy and unprofessional to a judge.

This is not just a documentation bug — it's an active vulnerability. Every
enforcement action can weaponize this as a "the license is broken" defense,
delaying proceedings and undermining the Steward's credibility. The fact that
the license has been published in this state for weeks means it can be argued
the Steward is effectively abandoning the attempt to maintain a complete
license document.

PRINCIPLE_VIOLATION: Principle 1 (Humans First) — The Personal Use Exception was
intended to guarantee individual freedoms, but its truncation makes the scope
of those freedoms ambiguous, chilling legitimate personal use (individuals may
fear the exception doesn't apply to them). Principle 4 (Dynamic Pricing) —
An incomplete license undermines confidence in the entire Registry system,
as parties will question whether other sections are similarly truncated or
broken.

SEVERITY: MEDIUM (because the intended content can likely be reconstructed
from context, but the litigation leverage it creates is non-trivial)

FIX RECOMMENDATION:
- Complete Section 11.3 with the intended text immediately. Based on the
  surrounding context, this appears to have been cut off during editing.
  A plausible completion: "This License expressly does not restrict the ability
  of any person or entity to engage in activities that would otherwise be
  permitted under applicable law, including but not limited to fair use,
  first sale doctrine, and independent development. No provision of this
  License shall be construed to limit rights that cannot be waived or
  contracted away under applicable law."
- After completing the section, add a verification step to the release process:
  a script that validates all sections are complete (no trailing "or" or "and"
  at section ends, all subsections have content).

---

## ADDITIONAL FINDING: Section 5.4 (Multi-Project Aggregation) Numbering Anomaly

The section numbering at line 572 jumps from 5.2 to 5.4, skipping 5.3.
Section 5.3 actually appears later at line 592, creating two issues:
(a) the numbering is out of order (5.4 appears before 5.3), and
(b) a lawyer could argue Section 5.4 is a typographical error and shouldn't
bind the parties, or should be interpreted according to its position (as
5.2.1 or as part of 5.2 rather than as a standalone section).

This isn't a standalone loophole but compounds the credibility problem when
combined with the truncated Section 11.3. A pattern of structural errors in
a legal document gives a judge reason to be skeptical of the drafter's
precision on more substantive provisions.

---

## SUMMARY OF FINDINGS

| #  | Scenario | Severity | Stated Principle(s) Violated |
|----|----------|----------|------------------------------|
| 1  | "Clear and Convincing" Burden-of-Proof Trap | HIGH | Principles 2, 4 |
| 2  | Fallback JSON Registry Authenticity Void | HIGH | Principle 4 |
| 3  | "Trained Substantially" Revenue Attribution Shell Game | CRITICAL | Principles 2, 3 |
| 4  | Abandoned-Project Derivative Deadlock | CRITICAL | Principles 1, 2 |
| 5  | Two-Tier Registry Enforcement Asymmetry | HIGH | Principles 1, 2, 5 |
| 6  | Truncated Section 11.3 Personal Use Exception | MEDIUM | Principles 1, 4 |
| +1 | Section 5.4 numbering anomaly (compounding factor) | LOW | — |

These 6 scenarios (+ 1 compounding factor) represent NEW vulnerabilities not
identified in Rounds 1-9, arising specifically from the post-Round-9 changes:
the rebuttable presumption language (1), the JSON fallback (2, 5), the new
Section 4.3(d) AI training trigger (3), and the Section 5.2 derivative
distribution ban (4).
