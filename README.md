     1|# Open-Pact License v1.1 (OPL-1.1)
     2|
     3|> **Source-Available Software for the Age of AI.**
     4|
     5|The Open-Pact License is a four-tier licensing framework designed to bridge the gap between permissive open source and closed proprietary software. It guarantees source availability and individual freedom while establishing fair compensation when code is used for commercial profit or AI model training.
     6|
     7|**Current Status:** [Soft Launch](#soft-launch) · [Read the Legal Text](LICENSE.md) · [Submit Feedback](https://github.com/open-pact/license/issues/1)
     8|
     9|---
    10|
    11|## At a Glance
    12|
    13|| Tier | Who | Cost | Rights |
    14|| :--- | :--- | :--- | :--- |
    15|| **1. Personal Use** | Individuals, Students, Researchers | **Free** | Full access, modification, redistribution, and security research. |
    16|| **2. Commercial** | Businesses, SaaS, Enterprise | **Dynamic** | Defined by Project Registry (Flat, Usage, or Revenue Share). |
    17|| **3. AI Training Use** | LLMs, Model Training, AI Companies | **Premium** | Training access with mandatory model card disclosure. |
    18|| **4. Reciprocity** | Derivative Works, Forks | **Dynamic (Registry)** | Build on our code, share royalties back. |
    19|
    20|---
    21|
    22|## Why Open-Pact?
    23|
    24|Every major open-source project built today faces the same problem: **extractive consumption without reciprocity.**
    25|
    26|| Use Case | MIT/Apache | GPL | BSL/SSPL | **OPL-1.1** |
    27|| :--- | :--- | :--- | :--- | :--- |
    28|| **Free for individuals** | Yes | Yes | Yes | **Yes** |
    29|| **Free for commercial use** | Yes | Yes | No | **Fee (fair, scaled)** |
    30|| **AI training allowed freely** | Yes | Unclear | Yes | **Premium + Disclosure** |
    31|| **Creator compensated** | No | No | Only originator | **Yes (Community Guild)** |
    32|| **Abandonware protection** | No | No | Time-delay | **36-month Apache 2.0** |
    33|
    34|### The Three Principles
    35|
    36|1. **Humans First.** Individuals can always learn, build, and share freely.
    37|2. **Fair Compensation.** When code creates commercial value, the creators share in it.
    38|3. **AI Transparency.** If you train on our code, you disclose it. If you clone it, you reciprocate.
    39|
    40|---
    41|
    42|## Key Features
    43|
    44|### Stewardship Sunset
    45|No one controls this license forever. If a project has no active stewardship for **36 months** and fewer than **3 active participants**, the code automatically converts to [Apache 2.0](https://www.apache.org/licenses/LICENSE-2.0). You are never trapped by abandonware.
    46|
    47|### The License Steward
    48|The Steward governs the license, sets fees, and maintains the Project Registry. A Steward can be a **solo developer** or a **Guild** (a community governance body). Solo Stewards can transition to Guild governance at any time by publishing notice.
    49|
    50|### Community Accountability
    51|If a Steward goes rogue, **20% of active Contributors** can petition for removal. If the Steward doesn't cure within 90 days, stewardship transfers to the community.
    52|
    53|### AI Agent Definition
    54|The license explicitly defines AI Agents -- including AGI -- and their legal status. AI cannot hold copyright, vote in governance, or exercise any rights under this license. The human or entity operating the Agent bears legal responsibility.
    55|
    56|### Canary Token Enforcement
    57|To prevent invisible code theft, Stewards embed unique identifiers in software distributions. Discovery of a Canary Token in unauthorized use is **non-rebuttable evidence** of infringement.
    58|
    59|### International Arbitration
    60|Disputes involving companies with >$1M annual revenue are resolved through **binding arbitration** enforceable under the **[New York Convention](https://en.wikipedia.org/wiki/New_York_Convention)** in 170+ jurisdictions worldwide.
    61|
    62|---
    63|
    64|## How to Use This License
    65|
    66|### For Projects
    67|1. Add `LICENSE.md` to your repository root.
    68|2. Add a reference in your `package.json`, `Cargo.toml`, or `pyproject.toml`:
    69|   ```json
    70|   { "license": "OPL-1.1" }
    71|   ```
    72|3. Register with the [Project Registry](https://open-pact.dev) to publish your fee schedule.
    73|
    74|### For Individuals
    75|Clone, fork, test, and share. Personal Use is always **free and permissionless**.
    76|
    77|### For Companies
    78|1. Determine your **Total Workforce** (employees + contractors + autonomous AI agents).
    79|2. Register with the License Steward and pay the applicable fee.
    80|3. If training AI models on our code, disclose it in your Model Card.
    81|
    82|---
    83|
    84|## Repository Structure
    85|
    86|| File | Description |
    87|| :--- | :--- |
    88|| [**`LICENSE.md`**](LICENSE.md) | The canonical legal text of OPL-1.1. |
    89|| [**`RATIONALE.md`**](RATIONALE.md) | The philosophy -- why we built this, and why existing licenses fail. |
    90|| [**`NOTES.md`**](NOTES.md) | Section-by-section commentary in plain English. |
    91|| [**`FAQ.md`**](FAQ.md) | Frequently asked questions for developers and legal teams. |
    92|| [**`INDEX.md`**](INDEX.md) | Master index and release checklist for the OPL-1.1 package. |
    93|
    94|---
    95|
---

### Setting Up Your Project with OPL-1.1

Not every project needs smart contracts. See [MINIMAL_SETUP.md](MINIMAL_SETUP.md) for
setup tiers from Text-Only to Full Enforcement, including a fallback JSON Registry template.

---
## Soft Launch
    97|
    98|This license is currently in **Soft Launch**. We are inviting projects, developers, and legal scholars to review the text and provide feedback before our formal release.
    99|
   100|### What We're Looking For
   101|- **Enforceability** of the "AI Training Disclosure" requirement (Section 4).
   102|- **Fairness** of the Commercial Tiers and Total Workforce calculation (Section 3).
   103|- **Compatibility** with existing dependency ecosystems (Section 18).
   104|- **Clarity** of the governance model for Guild and solo Stewards.
   105|
   106|### Adversarial Testing
   107|OPL-1.1 has survived **7 rounds** of automated adversarial stress testing (48 findings, all patched). See the [Final Report](FINAL_REPORT.md) for the complete audit trail.
   108|
   109|### How to Contribute
   110|- 📝 [Submit Feedback](https://github.com/open-pact/license/issues/1)
   111|- 🔍 [Review the Text](LICENSE.md)
   112|- 💬 [Discuss on the OPL Forum](https://open-pact.dev)
   113|
   114|---
   115|
   116|> **Note:** The Open-Pact License is a **source-available** license. It is not an "Open Source" license as defined by the Open Source Initiative (OSI), as it places restrictions on fields of endeavor (commercial and AI use) to ensure creator compensation.
   117|