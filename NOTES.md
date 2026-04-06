# Open-Pact License v1.1 (OPL-1.1) — Section Notes

## Overview
This document explains the intent, mechanics, and rationale behind each section of the Open-Pact License (OPL-1.1). It is not a substitute for the legal text, but it is designed to make the legal text accessible to developers, lawyers, and business leaders.

**Core Philosophy:** "Fair compensation for extraction, permissionless access for humans."

---

### Preamble
**The Intent:** The software world is broken. Traditional licenses either give everything away for free (MIT/Apache) or lock everything down (BSL/CC-NC). OPL sits in the middle: it allows individuals to use code freely, but requires businesses and AI companies to pay for the value they extract.
**The Mechanism:** A tiered system governed by a "License Steward" (either a Guild of contributors or a solo developer).

### Section 1: Definitions
*   **1.2 License Steward:** The entity in charge. Can be a Guild (community) or a Solo dev. This means OPL works for a 1-person project just as well as a 10,000-person open source foundation.
*   **1.4 - 1.4.3 The People Map:** We distinguish between:
    *   **Contributor:** Someone with accepted code.
    *   **Collaborator:** Someone who helps (tests, docs) but has no IP claim.
    *   **Guild Member:** Someone with voting power on royalties and policy.
*   **1.4.1 AI Agent:** AI is explicitly defined. It cannot hold copyright or vote. If an AI generates code, the *human or company* running it is responsible. This closes the "AI ghostwriter" loophole.
*   **1.5 Total Workforce:** We count everyone who works: employees, contractors, gig workers, and autonomous AI agents. We *don't* count tools like Copilot or linters. This prevents companies from firing staff to hire "AI agents" to dodge fees.
*   **1.22 Functionally Equivalent Work:** You can't just copy the exact behavior of our software and release it under MIT to avoid paying. If you build a clone to displace us, you still pay.

### Section 2: Personal Use (Tier 1)
*   **Rights:** Full access, modification, redistribution.
*   **Cost:** Free.
*   **Internal Evaluation:** Companies can test the software for 90 days before buying. This removes the friction of "try before you buy."
*   **Security Research:** Allowed for everyone, even if paid. You can hunt bugs in our code without fear of a lawsuit.

### Section 3: Commercial Use (Tier 2)
*   **Rights:** Use in business, SaaS, internal tools.
*   **Cost:** Fees are **NOT fixed** in this legal text. They are set by the License Steward and published in a **Project Registry** (a public URL or Smart Contract). This allows flexible pricing (flat fee, usage-based, revenue share) tailored to the software's specific value.
*   **Key Safeguards:**
    *   **Canonical Registry (3.2.1):** You can only use the Steward's official registry.
    *   **Per-Project (3.2.2):** One fee covers one project.
    *   **Temporal (3.2.3):** Prices change prospectively, not retroactively. If no price is listed, you must negotiate in good faith within 30 days.
    *   **Proportionality (3.2.4):** Fees must be reasonable based on your company size and how much you use the code.
*   **Payment:** Stablecoins (USDC), Crypto, or Fiat.
*   **Escrow:** If the Steward disappears (ghosts you), you can pay into escrow and you are considered valid.

### Section 4: AI Training Use (Tier 3)
*   **Rights:** Training models on our code.
*   **Cost:** Higher premium than Commercial.
*   **Disclosure:** You must list us in your Model Card.
*   **Anti-Competitive:** You can't train a model specifically to replace our product using our own code.

### Section 5: Derivative Works (Tier 4)
*   **Reciprocity:** If you build a business on our code and make over a minimum amount (the "de minimis" threshold), you must share at least 10% of the revenue with the original Stewards.
*   **5.2 Anti-Evasion:** No revenue slicing, bundling, or transfer pricing games. If OPL is the primary value, all revenue counts.
*   **5.5 Version Certification:** Every version of a Derivative Work must be "certified" as clean. This prevents bad actors from sneaking stolen GPL code into one specific version to poison the ecosystem.

### Section 10: Termination
*   **10.4 Damages & Disgorgement:** We don't use fixed fines (which are just taxes). If you steal the software, we can claim all profits you made from it.
*   **10.5 No Safe Harbor:** Just because we didn't put a specific penalty for a specific violation doesn't mean you can get away with it.

### Section 11: Enforcement
*   **Canary Tokens:** Each download of the software contains unique, invisible identifiers. If we find your company's "unique" code in the wild with a Token that matches a download you took but didn't pay for, that is non-rebuttable evidence of theft.
*   **Registry:** We maintain a public record of who is licensed. This allows anyone to verify that you are allowed to use the code.

### Section 15: Miscellaneous
*   **15.6 Succession:** If a solo Steward dies, the community can eventually take over if the heir doesn't step up.
*   **15.7 Steward Removal:** If a Steward goes rogue (stealing royalties), the community (20% of contributors) can vote them out.
*   **15.1 Arbitration:** For disputes involving companies with >$1M revenue, we agree to Binding Arbitration. This means we can enforce this license in 170+ countries (via the New York Convention) without relying on local courts that might ignore foreign IP laws.

### Section 16: Sunset
*   **36-Month Rule:** If a project is abandoned for 36 months AND has fewer than 3 active participants, it automatically becomes **Apache 2.0**. This ensures we never become "zombie software" that holds code hostage.

### Section 17: Whistleblower
*   **Bounty:** 5% of all royalties go to a bounty pool.
*   **Anonymity:** You can report violations anonymously.
*   **Anti-Harassment:** False reports are penalized. No one can use the whistleblower system as a weapon against competitors. Only material violations (unlicensed commercial use) result in registry entries, with a 6-month cap per subject.

### Section 18: Third-Party Dependencies
*   **Separation:** Dependencies (MIT, Apache, GPL, etc.) keep their own licenses. They are not "infected" by OPL. 
*   **Definition:** A real Dependency must be (a) independently created and (b) have a verifiable license. You cannot use this to hide your own code.
*   **Anti-Poisoning:** The Steward is responsible for ensuring dependencies aren't incompatible (e.g., GPL code in a commercial tool). Deliberate "poisoning" of a project's license status is illegal.
*   **Shadow Dependencies:** If a product tries to hide OPL code inside a "Dependency" folder to avoid paying royalties, the law treats it as part of the main Software.
*   **Good Faith Declaration:** All dependencies must be declared in a machine-readable file. Errors must be cured within 30 days.
