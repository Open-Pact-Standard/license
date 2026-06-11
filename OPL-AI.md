# OPL-AI Addendum v1.3.1 (DRAFT)

> **Status:** Draft for review. Companion to OPL-1.3 / OPL-1.3.1. This addendum is incorporated into OPL-1.3 §3.5 **only if** the Maintainer has affirmatively opted in via `NOTICE`. **Default: not incorporated.** v1.3.1 is a clarification release that adds a canonical syntax for the opt-in/opt-out declaration (see §8.1–§8.3 below). The substance of v1.3 (the default flip and the §2–§7 restrictions) is preserved.
>
> **Note on the v1.3 change:** OPL-AI v1.0 (for OPL-1.2) was incorporated by reference and required the Maintainer to opt out. OPL-AI v1.3 (for OPL-1.3) flips the default: the addendum is **not** incorporated unless the Maintainer affirmatively opts in via `NOTICE`. The change is consistent with OPL-1.3's broader shift from "default restrictions" to "default permissions, with per-work opt-ins." A Maintainer who wants AI training restricted must now declare that in `NOTICE` (e.g., `OPL-AI: opted in.`); a Maintainer who does nothing has a license that permits AI training under the same terms as any other use. The substantive restrictions in §2–§7 are unchanged. Only the default, the mechanism (§8), the version reference in OPL-1.3 §3.5, and one cross-reference in §3.2 (OPL-1.2 §3.3 "Hosted Service restriction" → OPL-1.3 §3.3 "Commercial Use requires Standard Terms payment") are affected. Note that OPL-1.3 §3.3 is a payment mechanism, not a prohibition, so the "may not" in §3.2 still works when the Maintainer has not granted a separate written agreement.
>
> **Honest disclosure up front:** enforcement of any AI training restriction is imperfect. The mechanisms in this addendum are best-effort, not bulletproof. The standard's bet is that reasonable actors will comply when caught, and that the mechanisms make non-compliance detectable. We make no claim that this is a complete solution.

---

---

## 1. What this addendum does

OPL-AI defines the term **"AI System"** and the **restricted uses** of the Work in the context of artificial intelligence. It also describes the **detection and attestation mechanisms** by which compliance is verified.

This addendum is incorporated into the OPL-1.3 license **only if** the Maintainer has affirmatively opted in via `NOTICE` (see §8). The default is opt-in. The Maintainer must declare in `NOTICE` that this addendum applies. It does not modify any other term of OPL-1.3.

---

## 2. Definition of "AI System"

For the purposes of this addendum, an **"AI System"** is any system — model, agent, tool, service, or product — that:

- Has been trained, fine-tuned, aligned, evaluated, or distilled using the Work, a Derivative, or any output of the Work; or
- Generates outputs that are materially derived from the structure, organization, non-public interfaces, or substantial functional units of the Work; or
- Is marketed, documented, or reasonably understood to provide functionality substantially similar to the Work.

This includes foundation models, fine-tuned derivatives, multi-modal models, agent systems, retrieval-augmented generation systems, and any system that uses a model's outputs as training signal for further models.

---

## 3. Restricted uses

The following are restricted under OPL-1.3 §3.5 when this addendum is incorporated:

### 3.1 Training and fine-tuning

You may not use the Work, a Derivative, or any output of the Work as:

- Pre-training data for an AI System.
- Fine-tuning data for an AI System.
- Alignment or reinforcement-learning data.
- Evaluation or benchmarking data (where the result is used to improve a model).
- Distillation data (training a smaller model to mimic a larger one).
- Synthetic data generation seed.

### 3.2 Operational use

You may not:

- Operate an AI System whose outputs are materially derived from the Work as a Hosted Service under OPL-1.3 §3.3.
- Embed the Work, a Derivative, or an AI System trained on them, in a product that automates decisions or actions that the Work itself was used to make.
- Use the Work as the knowledge base, retrieval corpus, or context source for an AI System, where the AI System's primary value is derived from the Work.

### 3.3 Distillation

You may not train an AI System to mimic the outputs of another AI System that was itself trained on the Work in violation of this addendum.

---

## 4. Permitted uses

The following are **not** restricted:

- Using the Work to inform human-written code or documentation.
- Using the Work as a reference (read by humans) during the development of an AI System.
- Using the Work as a test fixture for an AI System, where the test result is not used to improve a model.
- Citing the Work in academic research, where the citation is in the paper and the Work itself is not used as training data.
- Using the Work to build a system that the Maintainer has explicitly licensed for that purpose under a separate written agreement.

---

## 5. Attestation

A commercial user of an AI System that may have been trained on the Work is encouraged to publish an annual attestation confirming:

- Whether the Work was used in any restricted use as defined in §3.
- If yes, the date of the restricted use, the AI System involved, and whether a separate agreement with the Maintainer is in place.

**Default venue:** A public post in the project's official communication channel (GitHub Discussions, mailing list, or equivalent), or — if the OPL Registry exists at the time of attestation — to the Registry.

This is an attestation, not a notarization. It is intended as a baseline signal of good faith.

---

## 6. Detection and best-effort mechanisms

The following mechanisms may be used by the Maintainer to detect restricted uses. None are perfect. None are required. All are best-effort.

### 6.1 Canary tokens

The Maintainer may embed unique, semantically innocuous identifiers ("canary tokens") in source files. Discovery of a canary token in a published model or training dataset is evidence that the Work was used in a restricted use. The burden is then on the alleged infringer to demonstrate lawful access.

### 6.2 Registry fingerprinting

The Maintainer may publish cryptographic fingerprints of releases. A model whose outputs include content derivable from a fingerprinted release is evidence of restricted use.

### 6.3 Audit agents

The OPL framework provides an optional audit agent (`audit_agent.py`) that scans public endpoints and published model outputs for canary-token matches and fingerprint derivations. The audit agent is opt-in for the Maintainer; it is not deployed by default.

### 6.4 Voluntary disclosure

The Maintainer may request, and AI System operators are encouraged to provide, voluntary disclosure of training-data composition. The OPL framework may publish a public registry of compliant AI Systems.

### 6.5 Suspension during abandonment

If no Maintainer is reachable for the period specified in OPL-1.3.1 §5, the mechanisms in §6.1, §6.2, and §6.3 are suspended. They resume on re-assumption of stewardship. Canary tokens that were embedded in source prior to abandonment remain in the source; the suspension applies to the *act of monitoring and asserting them*, not to their presence in the codebase.

---

## 7. Enforcement reality check

The OPL-AI mechanisms are best-effort. The following limits are honest:

- **Canary tokens can be stripped.** Sophisticated actors with access to the source can remove them. Detection of stripping is itself imperfect.
- **Good-faith discovery-and-removal is permitted.** A model operator who discovers a canary token in their training data, or who notices that the Work was incidentally included in a large web-crawl snapshot (e.g., a Common Crawl snapshot), and who removes the Work from their training data before training, has not violated this addendum. Operators are encouraged to publish a public note describing the discovery and removal.
- **Fingerprinting requires compute.** A model that uses a fraction of the Work's tokens may not produce fingerprint-derivable outputs. The threshold for "materially derived" is a judgment call.
- **False positives happen.** A model trained on a large corpus that incidentally included the Work (e.g., a Common Crawl snapshot that happened to include the project's GitHub repository) may be flagged. A model operator can demonstrate compliance by showing that the Work was not the primary training signal and that the model does not produce outputs materially derived from the Work's substantial functional units. A cure mechanism is available: the operator submits a written explanation to the Maintainer; if the Maintainer does not object within 30 days, the matter is considered resolved.
- **Cross-border enforcement is hard.** An AI System operated by a defendant outside the Maintainer's jurisdiction may be practically unenforceable. See `REVIEW.md` §9.
- **The audit agent is observational, not enforcement.** It generates signals; humans adjudicate disputes.

OPL-AI does not promise a complete solution. It promises a **detectable, attestable, negotiable** mechanism that raises the cost of non-compliance relative to the cost of compliance.

---

## 8. Opting in

The Maintainer opts in to this addendum in `NOTICE` with a single line:

```
OPL-AI: opted in. AI training is restricted under the OPL-AI addendum (v1.3).
```

When opted in, OPL-1.3 §3.5 incorporates this addendum by reference, and the restrictions in §2–§7 apply. The Maintainer may revoke the opt-in at any time by updating `NOTICE` (e.g., `OPL-AI: opted out.`); the revocation is not retroactive, and prior acts in reliance on the opt-in remain subject to the addendum.

The default in OPL-1.3 / OPL-1.3.1 is **not** to opt in. A Maintainer who does nothing has a license that permits AI training under the same terms as any other use.

Opting in is intended for Maintainers who:

- Consider AI training a concern worth restricting for their Work.
- Operate in an ecosystem where the restriction is a competitive or ethical advantage.
- Have decided, after consideration, that the trade-off benefits the Work.

**8.1 Canonical syntax**

The canonical forms are:

```
OPL-AI: opted in. [optional human-readable text]
OPL-AI: opted out. [optional human-readable text]
```

**Parsing rules.**

1. The line must begin with the literal string `OPL-AI:` (case-sensitive — only this exact casing is recognized).
2. The prefix may be followed by **any amount of ASCII whitespace** (spaces or tabs), including zero.
3. The value must be exactly one of:
   - `opted in.`
   - `opted out.`

   The value is **case-insensitive** — `Opted In.`, `OPTED OUT.`, and `opted in.` are all recognized. (The case-insensitivity is a usability concession; the prefix remains case-sensitive to prevent false matches with non-OPL metadata.)
4. After the value, the line may continue with optional human-readable text. **A parser may ignore** any text after the value. The text is documentation, not part of the syntax.
5. The line may be **commented out** (preceded by `#` or `//` per the NOTICE file's comment convention) — a commented line is treated as if absent. The default (line absent or commented) is opt-out, per OPL-1.3 §3.5.
6. If **multiple** `OPL-AI:` lines appear in the NOTICE (e.g., from a copy-paste error or a poorly-merged update), the **last uncommented occurrence wins**. A parser should warn if multiple lines are present.

**8.2 Versioning**

The version reference (e.g., `(v1.3.1)`) in the optional text is **documentation only**. The currently-published version of the OPL-AI addendum (referenced from OPL-1.3.1 §3.5) applies regardless of the version reference in the NOTICE line. A Maintainer who specifies a different version (e.g., `(v1.4)` before v1.4 is published) is treated as opting in to the **currently-published version**, not a future version. To bind a specific historical version, the Maintainer should reference it via a different mechanism (e.g., an explicit version field in `NOTICE`).

**8.3 Examples**

Valid opt-in lines:

```
OPL-AI: opted in.
OPL-AI: opted in. AI training is restricted under the OPL-AI addendum (v1.3.1).
OPL-AI: OPTED IN.
OPL-AI:  opted  in.
OPL-AI: Opted In.   (note: case-insensitive value)
```

Valid opt-out lines:

```
OPL-AI: opted out.
OPL-AI: opted out. AI training is permitted under the same terms as other use.
OPL-AI: OPTED OUT.
```

Invalid lines (parser should treat as absent; default = opt-out):

```
OPL-AI: yes.                         # missing the canonical "opted in" verb
OP-LAI: opted in.                    # typo in the prefix
OPL AI: opted in.                    # missing colon
OPL-AI: opted in (v1.3).             # missing the trailing period
OPLAI: opted in.                     # missing the dash in the prefix
AI training: opted in.               # wrong prefix
```

Treated-as-absent lines (parser should ignore, fall back to default = opt-out):

```
# OPL-AI: opted in.                  # commented out
// OPL-AI: opted in.                 # commented out (alt convention)
```

---

## 9. Compatibility with other licenses

OPL-AI v1.3.1 is compatible, by design, with:

- **MIT, Apache 2.0, BSD-2/3, MPL-2.0:** A Work may be dual-licensed OPL-1.3 + OPL-AI and any of these, at the Maintainer's discretion.
- **GPL-3.0, AGPL-3.0:** Compatible, subject to the no-stripping provision in OPL-1.3 §3.2.
- **OPL-1.2 → OPL-1.3.1:** A Work migrating from OPL-1.2 to OPL-1.3.1 may adopt OPL-AI v1.3.1; the conversion is not retroactive to prior versions. Note that OPL-1.2's OPL-AI v1.0 used an opt-out default; OPL-1.3 / OPL-1.3.1's OPL-AI v1.3.1 uses an opt-in default.

OPL-AI v1.3.1 is not currently compatible with BUSL, FSL, or SSPL. Cross-license work is an area for future work.

---

*End of OPL-AI addendum draft v1.3.*
