# Open-Pact License v1.2 (DRAFT v2)

> **Status:** Draft for review. Not yet published. This is a redesign of OPL-1.1 with the goal of doing one thing well, instead of doing everything poorly.
>
> **Headline:** *Open work, get paid if it grows.*

---

## What this license is

OPL-1.2 is a fair-source license. It lets you use, modify, and share the Work freely. It asks that anyone who builds a business on top of the Work share a small part of the value back with the people who made it. If you want to use the Work to run a paid hosted service, talk to the Maintainer first — they're easy to reach, and the conversation is short.

OPL-1.2 is not "open source" as defined by the Open Source Initiative. It restricts certain fields of endeavor to protect the people who make the Work. That is the trade-off, and it is intentional.

---

## 1. Definitions

- **"Work"** means the software (including source code, build scripts, configuration, and accompanying documentation) made available under this license.
- **"You"** means any individual or entity exercising rights under this license.
- **"Maintainer"** means the person or legal entity named in the project's `NOTICE` file, or their designated successor.
- **"Derivative"** means any work that includes a substantial portion of the Work, modified or unmodified.
- **"Functional Equivalent"** has the meaning given in §3.6. The term captures works that are not textually derived from the Work but are substantially similar in function and were developed with access to the Work.
- **"Hosted Service"** means a service operated by You, accessible to third parties over a network, whose primary functionality is the Work, a Derivative, or a Functional Equivalent.
- **"Revenue"** means gross income received by You from a Hosted Service or Derivative, net of refunds, chargebacks, payment-processing fees, and sales taxes. Revenue "attributable to" a Derivative means the Revenue of the product or service whose primary functionality is the Derivative.
- **"AI System"** has the meaning given in the **OPL-AI addendum**, incorporated by reference.
- **"Contributor"** means any individual who has submitted a merged change to the Work, as recorded in the project's contribution history.
- **"Designated Successor"** means a person or entity identified as the Maintainer's successor by a signed statement from the prior Maintainer in an updated `NOTICE` file. If no such statement exists, succession follows the abandonment procedure in §5.

---

## 2. Grant of rights

Subject to the conditions in §3, and to the Reciprocity obligation in §3.4, You may, without prior permission:

- Use the Work for any purpose, including commercial purposes.
- Modify the Work and create Derivatives.
- Distribute the Work, modifications, or Derivatives, in source or object form.
- Sublicense the Work, modifications, or Derivatives, provided that any sublicensee is bound by the conditions in §3.
- Embed the Work in a larger product or service.

This grant is intentionally broad. The conditions in §3 are the only limits. Reciprocity in §3.4 is an obligation of payment, not a restriction on the grant itself.

---

## 3. Conditions

The following conditions apply to the rights granted in §2.

### 3.1 Attribution and notice

If You distribute the Work or a Derivative, You must:

- Preserve the copyright notice.
- Include a copy of this license.
- Include the `NOTICE` file (or, if You do not distribute source, equivalent notice in your distribution).
- Clearly mark any modifications You have made.

### 3.2 No stripping

You may not distribute the Work or a Derivative under terms that remove, weaken, or fail to enforce the conditions in §3.3, §3.4, and §3.5.

This is light copyleft. It propagates the protections, not the code. A Derivative may be relicensed for any other terms as long as the protections in this section continue to apply to the protections themselves.

### 3.3 Hosted Service restriction

You may not operate a Hosted Service and receive direct compensation primarily for the Hosted Service, without a separate written agreement with the Maintainer.

The following are **not** restricted by this section:

- Internal use within a single legal entity (or an affiliated group under common control treated as a single employer under the tax law of the Maintainer's jurisdiction).
- Use that does not involve third parties as users of the Hosted Service.
- Non-commercial use, including educational, research, and personal projects.
- Small-scale use: Hosted Services that receive less than USD $5,000 in direct annual compensation from the service, OR that have fewer than 10,000 monthly active users, are exempt from this restriction. The Maintainer may lower or remove this carve-out in `NOTICE`.

### 3.4 Reciprocity

If You distribute a Derivative, You owe the Maintainer a share of the Revenue attributable to that Derivative. The default rate is **5%**. The Maintainer may set a different rate in `NOTICE`, or waive Reciprocity entirely.

Reciprocity is calculated and paid at intervals of no less than annually. The Maintainer must publish a payment address in `NOTICE`.

> **Fallback:** If You have made a written request to the Maintainer for a payment address and the Maintainer has not provided one within 90 days, Reciprocity for that Derivative is permanently waived. For the purposes of this paragraph, a "written request" means an email, posted letter, or public GitHub issue or Discussion post sent to the contact in `NOTICE`, with a verifiable timestamp. A waiver under this paragraph does not affect any other obligation under this license.

This fallback exists so that downstream users are not trapped by an unresponsive Maintainer.

### 3.5 AI training restriction

You may not use the Work, a Derivative, or any output of the Work for the training, fine-tuning, alignment, evaluation, or distillation of any AI System, and You may not operate an AI System whose outputs are materially derived from the Work, without a separate written agreement with the Maintainer.

The full definition of "AI System," the scope of restricted uses, and the available exceptions are specified in the **OPL-AI addendum** (current version: OPL-AI-1.0). The Maintainer may opt out of the OPL-AI addendum in `NOTICE`; if the Maintainer has not done so, OPL-AI is incorporated by reference.

### 3.6 Functional Equivalent Work

You may not create or distribute a **Functional Equivalent** of the Work under terms more permissive than this license, and you may not operate a Hosted Service whose primary functionality is a Functional Equivalent, without a separate written agreement with the Maintainer.

A **"Functional Equivalent"** is a work whose primary functional purpose is substantially the same as the Work's, and that was developed with access to the Work or a Derivative. Access is presumed if the Functional Equivalent is publicly released within 36 months of the Work's first public release and addresses a problem domain that the Work addresses. Independent creation evidence rebuts the presumption of access.

This section does not restrict independent development that arrives at substantially similar functionality without access to the Work. The "Functional Equivalent" test is a contractual analog to the fair-use analysis in *Sega Enterprises Ltd. v. Accolade, Inc.*, 977 F.2d 1510 (9th Cir. 1992), adapted for a private license. The contractual nature of this section means that case-law developments in fair use do not automatically extend to or from this test; the section operates on its own terms.

---

## 4. Maintainer obligations

The Maintainer must:

- Be reachable at the contact published in `NOTICE`.
- Respond to written licensing inquiries within 60 days.
- Maintain the Work, or designate a Designated Successor and update `NOTICE` accordingly.

These are not aspirations. Failure to satisfy §4.1 or §4.3 for the period specified in §5 is a condition for abandonment.

---

## 5. Abandonment

If no Maintainer is reachable at the contact in `NOTICE` for **24 consecutive months**, the Work converts to the **Apache License 2.0**.

The conversion procedure is:

1. A Contributor, a group of at least three Contributors, or the OPL Standard's designated fiscal sponsor (default: **Software in the Public Interest, Inc.**, or any successor designated by the project's Contributors) may publish a public notice of intent to convert, citing documented attempts to contact the Maintainer at the contact in `NOTICE` over the prior 24 months with no response.
2. The Maintainer has **30 days** from publication of the notice to file a public counter-notice. A counter-notice must include a current, reachable contact and a statement of intent to resume stewardship. The counter-notice contact is verified by a test message from the conversion-initiator within 7 days of the counter-notice; if the Maintainer does not respond to the test message, the counter-notice is treated as not filed.
3. If no counter-notice is filed within the 30-day period, the conversion is effective on the 31st day. The license under which the Work is distributed becomes the Apache License 2.0.
4. If a counter-notice is filed, the conversion is paused. A second conversion procedure may not be initiated for 12 months from the date of the counter-notice, unless the Maintainer again becomes unreachable.

A Maintainer may voluntarily relinquish stewardship at any time by publishing a public statement and designating a successor in `NOTICE`. If no successor is named, abandonment is deemed to have begun on the date of the relinquishment.

---

## 6. Patent grant

Each Contributor grants You a perpetual, worldwide, non-exclusive, royalty-free patent license to make, use, sell, offer for sale, and import the **Work as contributed by that Contributor**. Modifications You make are not covered by this grant unless You own the relevant patents.

This grant terminates against any party that files a patent infringement claim alleging that the Work contributed by that Contributor infringes a patent.

---

## 7. Disclaimer

THE WORK IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY, FITNESS FOR A PARTICULAR PURPOSE, AND NONINFRINGEMENT. THE ENTIRE RISK AS TO THE QUALITY AND PERFORMANCE OF THE WORK IS WITH YOU.

---

## 8. Limitation of liability

IN NO EVENT SHALL ANY CONTRIBUTOR OR MAINTAINER BE LIABLE FOR ANY CLAIM, DAMAGES, OR OTHER LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT, OR OTHERWISE, ARISING FROM, OUT OF, OR IN CONNECTION WITH THE WORK OR THE USE OR OTHER DEALINGS IN THE WORK.

---

## 9. Interpretation

**9.1** This license is to be interpreted according to its express terms. Where a term is undefined, the plain meaning applies.

**9.2** If any provision is held unenforceable, the remaining provisions remain in effect.

**9.3** The Maintainer may publish a **clarification** of an existing term in `NOTICE`, but a clarification: (a) may not impose a new restriction, (b) may not expand the scope of any existing restriction, (c) is not retroactive, and (d) is subject to a 30-day public-comment period before taking effect. A "clarification" that violates (a), (b), or (c) is null and void.

**9.4** This license does not supersede any applicable law. Where the law requires more, the law controls. Where this license requires more and the law allows, this license controls.

---

## 10. Trademark

This license does not grant You any right to use the Maintainer's trademarks, trade names, logos, or service marks, except as required to describe the origin of the Work (for example, "this product is derived from FooBar" or "powered by FooBar").

If the Work is distributed under a name that includes the Maintainer's trademark, You must include the `NOTICE` file's trademark notice (if any) in your distribution.

---

## 11. No endorsement

You may not use the Maintainer's name, the name of the Work, the name of any Contributor, or the names of any of their products or services, to endorse or promote products or services derived from the Work, without prior written permission from the relevant party.

---

## 12. Governing law and forum

This license is governed by the laws of the jurisdiction specified in the project's `NOTICE` file under "Governing Jurisdiction" (or, if no jurisdiction is specified, the jurisdiction in which the Maintainer is located; or, if the Maintainer is an entity, the jurisdiction of its primary place of business), without regard to conflict-of-laws principles. The parties consent to the exclusive jurisdiction of the courts of that jurisdiction for any dispute arising under this license, subject to §9.4.

Nothing in this section prevents the parties from agreeing to binding arbitration for a specific dispute.

**12.1 Injunctive relief.** Notwithstanding §12, either party may seek injunctive or other equitable relief in a court of competent jurisdiction to prevent irreparable harm, including but not limited to infringement of the Work. The Maintainer's ability to seek such relief is not conditioned on the parties' agreement to arbitrate, and is not waived by any other provision of this license.

---

## 13. How to apply this license

To apply OPL-1.2 to a Work:

1. Place the full text of this license in a file named `LICENSE` in the repository root.
2. Create a `NOTICE` file containing:
   - The Maintainer's name and reachable contact.
   - **Governing Jurisdiction:** the jurisdiction whose laws govern this license, per §12. If unspecified, the Maintainer's location applies.
   - The Reciprocity rate (or a statement that the default 5% applies, or a waiver).
   - A Reciprocity payment address.
   - An opt-in or opt-out of the OPL-AI addendum, if You wish to change the default.
   - Any trademark notice You wish to assert.
   - Any small-scale carve-out override under §3.3, if You wish to lower or remove the exemption.
3. Add `SPDX-License-Identifier: OPL-1.2` to each source file.
4. Reference the license from your package manifest (`pyproject.toml`, `Cargo.toml`, `package.json`, etc.) using the SPDX identifier.

That's it. No registry required. No on-chain anything. No Guild. No Custodial Steward. No on-chain fee collection. Those are options in the optional `Open-Pact-Standard/framework` repository, available to Maintainers who want them; none of them are required by this license.

---

## What changed from OPL-1.1

| | OPL-1.1 | OPL-1.2 |
|---|---|---|
| Length | ~64 KB | ~7 KB |
| Default restrictions | Four pre-defined tiers (Personal/Commercial/AI/Reciprocity) | One restriction (Hosted Service) + default Reciprocity + default AI + no-stripping |
| "Total Workforce" definition | Required, complex | Removed |
| Reciprocity tier | Separate tier, opt-in to configure | Default-on at 5%, Maintainer can override in NOTICE; 90-day written-request → permanent waiver fallback |
| AI training clause | Embedded in main license, canary-token enforcement | Reference to separate OPL-AI addendum; opt-out available |
| Governance (Guild, Custodial Steward) | Required, complex | Removed; successor designation is a NOTICE update |
| Registry / smart contracts | Required for enforceability | Optional, lives in separate framework repo |
| Abandonment → Apache 2.0 | 36 months of unresponsiveness | 24 months + 30-day cure period + counter-notice verification + SPI as fiscal sponsor default |
| Terminology | "Steward" | "Maintainer" (OSS-native) |
| SaaS companion license (OPL-SaaS 1.0) | Required for hosted services | Not required; §3.3 covers it directly, with a small-scale ($5K / 10K MAU) carve-out |
| Trademark, no-endorsement, choice-of-forum | Absent or unclear | Added (§10, §11, §12); §12.1 injunctive-relief carve-out |
| Functionally Equivalent Work / clean-room defense | Present in v1.1 (Round 8 fix) but dropped in early v1.2 drafts | Restored in §3.6 with a Sega-v.-Accolade "starting point" test and a 36-month access presumption |

---

*End of OPL-1.2 draft v2.*
