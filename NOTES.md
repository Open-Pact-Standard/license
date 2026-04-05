# Open-Pact License v1.1 (OPL-1.1) -- Notes & Commentary

## Overview

This document provides plain-English commentary on the [Open-Pact License v1.1 (OPL-1.1)](LICENSE-OPL-1.1.md). It explains the intent behind each section and how it applies to different types of users.

**This document is informative only. It does not supersede the license text. if there is a conflict, the license text in LICENSE-OPL-1.1.md controls.**

---

## Preamble

**What it says:**
We are making a deal. You get access to the code for free. If you use it to make money or build AI, you pay the creators. The "Guild" (the community of contributors) manages this deal using on-chain transparency.

**Why it's important:**
Traditional licenses like MIT assume everyone is a developer sharing code at a university. They don't account for corporations extracting billions of dollars in value, or AI companies training models on code for free. The Preamble sets the intent: **This is a reciprocity agreement, not a public domain.**

---

## Section 1: Definitions

This is the dictionary. If a word here isn't defined here, it has its standard legal meaning (usually US Copyright Law).

*   **Guild:** Defined as the collective of Contributors. This is unique. It means no single person owns the "rights" to enforce the license or change fees. It's a decentralized governance body.
*   **Personal Use:** The "Free" tier. If you are a student, a hobbyist, or doing security research, this is you. **Key distinction:** You cannot use the code if it supports a commercial operation, even if you personally aren't making money from it.
*   **Commercial Use:** The "Business" tier. If this code helps you make money, save money, or run a business, you pay.
*   **AI Training Use:** The "AI" tier. This is broad on purpose. It covers feeding code to LLMs, using outputs as training data, and fine-tuning. It explicitly separates AI extraction from standard "running" of the software.
*   **Legal Entity:** Standard corporate definition (control, 50% ownership, etc).

---

## Section 2: Personal Use License

**For:** Students, Hobbyists, Researchers, Open Source Developers.

**The Deal:**
*   **Cost:** $0.
*   **Rights:** Perpetual, worldwide, royalty-free. You can modify, share, and build anything you want, as long as it's not for Commercial or AI Training use.
*   **Obligations:** Keep the license file. Don't pretend you are a commercial licensee.

---

## Section 3: Commercial Use License

**For:** Startups, SaaS Companies, Enterprise Internal Tools.

**The Deal:**
*   **Cost:** Tiered by company size (e.g., $100/yr for Micro, $50k/yr for Enterprise).
*   **Rights:** Full commercial rights to use, modify, and deploy.
*   **Mechanism:** You buy a license via the Guild registry (smart contract). You get a License Record on-chain.
*   **Obligation:** Be honest about your size. If you lie about being "Micro" when you are "Enterprise," you breach the license and lose your rights.

**FAQ: Can I use this in a closed-source product?**
Yes, as long as you hold a valid Commercial License. Unlike GPL, OPL does not "infect" your proprietary code. You buy the right to use it.

---

## Section 4: AI Training Use License

**For:** AI Companies, Model Labs, Agentic Frameworks.

**The Deal:**
*   **Cost:** Higher than commercial (e.g., $25k+).
*   **Rights:** Training models, fine-tuning, evaluation.
*   **The "Sticker":** You **must** disclose that you trained on this software. If your model spits out code that looks like this software, your user needs to know they might need a license too.
*   **Anti-Competitive Clause:** You cannot train a model *specifically* to replace the Software using the Software's own code. (e.g., you can't train a model to replace this exact codebase using this codebase).

**Why this is needed:**
Standard licenses grant the right to "reproduce." AI companies argue training a model isn't reproduction, it's "fair use" or "inspiration." This clause closes that loophole by defining AI Training as a specific, licensable activity.

---

## Section 5: Reciprocity (The "Network Effect")

**For:** Forks, Plugin Authors, Derivative Products.

**The Deal:**
If you fork this code and make money from the fork:
1.  You must use OPL-1.1 for your fork.
2.  You must share at least 10% of your revenue with the original Guild.
3.  Users of your fork also have to pay for Commercial/AI use.

**Why this is needed:**
This creates a network. If you build a successful business on top of this, you support the original creators. It prevents "leeching" where someone takes the code, modifies it slightly, and starts selling a better version without giving back.

---

## Section 6 & 7: Copyright & Patent Grants

**Legal Core:**
These are standard "Apache-style" grants.
*   **Copyright:** You give me permission to use the code.
*   **Patent:** You (Contributor) give me permission to use any patents *I specifically need to use your contribution*. If I sue you for patent infringement later, I lose my license. This prevents "open source patent ambushes."

---

## Section 8: Trademark

**The Brand:**
Just because you can use the code, doesn't mean you can use the **name**. You cannot call your fork "Project X" if the original is "Project X," and you can't use the logo.

---

## Section 10: Termination

**The "Three Strikes" Clause:**
If you break the rules (e.g., use it commercially without paying), your license ends.
*   **Grace Period:** You have 30 days to fix it. If you pay up within 30 days, you get your rights back. This is fairer than "one mistake and you're dead forever."

---

## Section 11: Enforcement

**The Guild Power:**
Usually, "enforcement" implies a company sending letters. Here, the Guild *is* the enforcer. The Guild can vote to ban a user or sue. Because the registry is on-chain, proving "you didn't pay" is as easy as checking a blockchain address. There is no "I didn't get the email" excuse.

---

## Section 12: Versions

**Future-Proofing:**
If we release OPL-2.0, you aren't forced to upgrade. You can stay on OPL-1.1 terms. This ensures stable, long-term legal certainty.

---

## Section 15: Smart Contract Integration

**The Bridge:**
Most licenses assume paper contracts. We assume smart contracts. This clause says: "If the smart contract code says you paid, you paid. If the text says something different, the text wins." It bridges the gap between human law and machine execution.
