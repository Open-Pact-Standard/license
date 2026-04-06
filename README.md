# Open-Pact License v1.1 (OPL-1.1)

> **Source-Available Software for the Age of AI.**

The Open-Pact License is a four-tier licensing framework designed to bridge the gap between permissive open source and closed proprietary software. It guarantees source availability and individual freedom while establishing fair compensation when code is used for commercial profit or AI model training.

**Current Status:** [Soft Launch](#soft-launch) · [Read the Legal Text](LICENSE.md) · [Submit Feedback](https://github.com/open-pact/license/issues/1)

---

## At a Glance

| Tier | Who | Cost | Rights |
| :--- | :--- | :--- | :--- |
| **1. Personal Use** | Individuals, Students, Researchers | **Free** | Full access, modification, redistribution, and security research. |
| **2. Commercial** | Businesses, SaaS, Enterprise | **Dynamic** | Defined by Project Registry (Flat, Usage, or Revenue Share). |
| **3. AI Training Use** | LLMs, Model Training, AI Companies | **Premium** | Training access with mandatory model card disclosure. |
| **4. Reciprocity** | Derivative Works, Forks | **10% Revenue Share** | Build on our code, share royalties back. |

---

## Why Open-Pact?

Every major open-source project built today faces the same problem: **extractive consumption without reciprocity.**

| Use Case | MIT/Apache | GPL | BSL/SSPL | **OPL-1.1** |
| :--- | :--- | :--- | :--- | :--- |
| **Free for individuals** | Yes | Yes | Yes | **Yes** |
| **Free for commercial use** | Yes | Yes | No | **Fee (fair, scaled)** |
| **AI training allowed freely** | Yes | Unclear | Yes | **Premium + Disclosure** |
| **Creator compensated** | No | No | Only originator | **Yes (Community Guild)** |
| **Abandonware protection** | No | No | Time-delay | **36-month Apache 2.0** |

### The Three Principles

1. **Humans First.** Individuals can always learn, build, and share freely.
2. **Fair Compensation.** When code creates commercial value, the creators share in it.
3. **AI Transparency.** If you train on our code, you disclose it. If you clone it, you reciprocate.

---

## Key Features

### Stewardship Sunset
No one controls this license forever. If a project has no active stewardship for **36 months** and fewer than **3 active participants**, the code automatically converts to [Apache 2.0](https://www.apache.org/licenses/LICENSE-2.0). You are never trapped by abandonware.

### The License Steward
The Steward governs the license, sets fees, and maintains the Project Registry. A Steward can be a **solo developer** or a **Guild** (a community governance body). Solo Stewards can transition to Guild governance at any time by publishing notice.

### Community Accountability
If a Steward goes rogue, **20% of active Contributors** can petition for removal. If the Steward doesn't cure within 90 days, stewardship transfers to the community.

### AI Agent Definition
The license explicitly defines AI Agents -- including AGI -- and their legal status. AI cannot hold copyright, vote in governance, or exercise any rights under this license. The human or entity operating the Agent bears legal responsibility.

### Canary Token Enforcement
To prevent invisible code theft, Stewards embed unique identifiers in software distributions. Discovery of a Canary Token in unauthorized use is **non-rebuttable evidence** of infringement.

### International Arbitration
Disputes involving companies with >$1M annual revenue are resolved through **binding arbitration** enforceable under the **[New York Convention](https://en.wikipedia.org/wiki/New_York_Convention)** in 170+ jurisdictions worldwide.

---

## How to Use This License

### For Projects
1. Add `LICENSE.md` to your repository root.
2. Add a reference in your `package.json`, `Cargo.toml`, or `pyproject.toml`:
   ```json
   { "license": "OPL-1.1" }
   ```
3. Register with the [Project Registry](https://open-pact.dev) to publish your fee schedule.

### For Individuals
Clone, fork, test, and share. Personal Use is always **free and permissionless**.

### For Companies
1. Determine your **Total Workforce** (employees + contractors + autonomous AI agents).
2. Register with the License Steward and pay the applicable fee.
3. If training AI models on our code, disclose it in your Model Card.

---

## Repository Structure

| File | Description |
| :--- | :--- |
| [**`LICENSE.md`**](LICENSE.md) | The canonical legal text of OPL-1.1. |
| [**`RATIONALE.md`**](RATIONALE.md) | The philosophy -- why we built this, and why existing licenses fail. |
| [**`NOTES.md`**](NOTES.md) | Section-by-section commentary in plain English. |
| [**`FAQ.md`**](FAQ.md) | Frequently asked questions for developers and legal teams. |
| [**`INDEX.md`**](INDEX.md) | Master index and release checklist for the OPL-1.1 package. |

---

## Soft Launch

This license is currently in **Soft Launch**. We are inviting projects, developers, and legal scholars to review the text and provide feedback before our formal release.

### What We're Looking For
- **Enforceability** of the "AI Training Disclosure" requirement (Section 4).
- **Fairness** of the Commercial Tiers and Total Workforce calculation (Section 3).
- **Compatibility** with existing dependency ecosystems (Section 18).
- **Clarity** of the governance model for Guild and solo Stewards.

### Adversarial Testing
OPL-1.1 has survived **7 rounds** of automated adversarial stress testing (48 findings, all patched). See the [Final Report](FINAL_REPORT.md) for the complete audit trail.

### How to Contribute
- 📝 [Submit Feedback](https://github.com/open-pact/license/issues/1)
- 🔍 [Review the Text](LICENSE.md)
- 💬 [Discuss on the OPL Forum](https://open-pact.dev)

---

> **Note:** The Open-Pact License is a **source-available** license. It is not an "Open Source" license as defined by the Open Source Initiative (OSI), as it places restrictions on fields of endeavor (commercial and AI use) to ensure creator compensation.
