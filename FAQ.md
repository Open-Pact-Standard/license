# Open-Pact License v1.1 (OPL-1.1) — Frequently Asked Questions

## General Questions

### Is OPL Open Source?
No. OPL-1.1 is a **Source-Available** or **Fair Source** license. It allows you to read, modify, and share the code, but it restricts certain commercial and AI uses to ensure creators are compensated. It is more permissive than "Proprietary" but more restrictive than "MIT" or "Apache."

### Does this mean I can't use OPL-licensed software for free?
Not at all. If you are an individual using the software for personal projects, education, research, or hobby development, it is **100% free** (Tier 1). We only charge for commercial use (Tier 2) and AI training (Tier 3).

### What if I run out of money?
The license is designed to be fair. If a project goes abandonware (no update in 36 months), the software automatically becomes **Apache 2.0**. You will never be held hostage by an abandoned license.

## For Businesses

### How much do I have to pay?
Fees are set by the **License Steward** (the project owner or the Guild) and published in the **Project Registry** (usually a simple webpage or on-chain contract). We use stablecoins (USDC), crypto, or fiat. The fees are tiered based on your Total Workforce (employees + contractors).

### Can we test the software before paying?
Yes! **Internal Evaluation** is free for up to 90 days. You can integrate, test, and prototype to see if the software fits your needs. You only need to pay when you move to production.

### What is the "Public Blacklist"?
If a company consistently refuses to pay for commercial use or AI training, the License Steward may publish a **Violation Record** in the Project Registry. Other OPL projects and the community can see this record. It is a mechanism to enforce the ecosystem, but we have strict due process (verification, cure periods) to prevent abuse.

### Can we use this in our internal enterprise tool?
Yes, but that falls under **Commercial Use** (Tier 2). You will need to register and pay the applicable fee for your organization size.

### What is a "Canary Token"?
To prevent "invisible" theft (like copying code into a closed-source binary), the Steward may embed unique, verifiable identifiers (Canary Tokens) in specific downloads of the software. If these tokens appear in any unauthorized product, they serve as evidence of which specific download was misused.

## For AI Companies

### Can I use OPL code to train my model?
Yes, but you must purchase an **AI Training License** (Tier 3). This costs more than a standard commercial license because AI extraction provides compounding, long-term value. 

### Do I have to disclose my training data?
Yes. Under **Section 4.3**, you must disclose the use of OPL-licensed material in your Model Cards or public documentation. We believe in transparency so that users know where their AI's knowledge comes from.

### What if I accidentally use OPL code?
The license includes a **3-Day Amnesty Window** (Section 17.4) for good faith errors. If you find it and cure the error (pay the fee or remove the code) immediately, there are no penalties.

## For Developers and Forkers

### Can I fork this project and change the license?
**No.** Section 10.1(f) explicitly prohibits re-licensing OPL code as MIT, Apache, GPL, or any other license. If you fork the code, you must maintain the OPL restrictions. This ensures the work stays within the "compensate the creator" ecosystem.

### What if my fork makes less than $1,000/year?
If your derivative is below the "de minimis" threshold (set by the Steward), you are exempt from paying royalties. You still must license your derivative under OPL (so others can use it for free), but you don't owe the original author a cut.

### I wrote a "Clean Room" clone. Can I license it as MIT?
**No.** OPL covers **Functionally Equivalent Works** (Section 1.22). If you create a clone to displace the original project in a commercial offering, you cannot escape the reciprocity requirements simply by rewriting the code from scratch. You must still license your work under OPL.

## Governance

### Who is the "License Steward"?
Either the original creator (Solo Steward) or a collective of contributors called a **Guild**. Solo creators have the same legal power as a Guild, making OPL perfect for indie devs.

### What is a "Guild"?
A Guild is an organized collective of Contributors that manages royalties and enforces the license. It operates as a governance convention, not a specific legal entity. It can be backed by an LLC, a Cooperative, or a DAO.

### What if the Steward steals the money?
Section 15.7 allows **20% of active Contributors** to petition for the removal of a malicious Steward. If the Steward refuses to step down after 90 days, stewardship automatically transfers to the community.
