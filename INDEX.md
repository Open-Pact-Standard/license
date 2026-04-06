     1|# 📦 Open-Pact Release Manifest (v1.1)
     2|
     3|This document serves as the master index for the **Open-Pact License v1.1 (OPL-1.1)** release package.
     4|
     5|## 1. File Directory
     6|
     7|| File | Description | Target Audience |
     8|| :--- | :--- | :--- |
     9|| **LICENSE.md** | The canonical legal text of OPL-1.1. | Legal Teams, Compliance Tools |
    10|| **README.md** | The "Pitch." Explains the Tiers, the Guild, and why we built this. | Developers, Public Visitors |
    11|| **RATIONALE.md** | The philosophy behind the license (The "AI Tax" and sustainability). | Journalists, Policy Makers |
    12|| **NOTES.md** | Section-by-section commentary in plain English. | Reviewers, curious developers |
    13|| **FAQ.md** | Answers to hard questions (Commercial rights, AI training, Forking). | CTOs, Legal Counsel |
| **MINIMAL_SETUP.md** | Setup tiers: Text-Only to Full Enforcement. What's required vs optional. | Solo Devs, Small Projects |
| **REGISTRY_TEMPLATE.json** | Fallback Project Registry (JSON) for projects not using smart contracts. | All Projects using Tier 1 (Basic Registry) |
    14|
    15|## 2. Repository Setup Checklist
    16|
    17|When creating the `open-pact/license` repository, follow these steps:
    18|
    19|- [x] **1. Upload all .md files** from this folder to the root.
    20|- [x] **2. Set Description:** "Source-Available Software for the Age of AI. Governed by Guilds."
    21|- [x] **3. Set Topics:** `license`, `software-licensing`, `ai-safety`, `fair-source`, `open-pact`.
    22|- [x] **4. License:** Select "Custom License" in GitHub's settings and point it to `LICENSE.md`.
    23|- [ ] **5. Pin Repo:** Pin the repository to the top of the "open-pact" organization profile.
    24|
    25|## 3. Versioning Status
    26|
    27|*   **Current Version:** 1.1
    28|*   **Status:** **Soft Launch Candidate.** Ready for public review.
    29|*   **Major Changes from v1.0:** 
    30|    *   Added "Internal Evaluation" rights (Section 2.3).
    31|    *   Added "Stewardship Sunset" (Section 16) - auto-converts to Apache 2.0 after 3 years of inactivity.
    32|    *   Enhanced "Derivative Works" definition to include Code Integrations (Section 1.8).
    33|    *   Added "Whistleblower Fund" and "Automated Auditing" permissions (Section 11 & 17).
    34|
    35|## 4. Integration Guide
    36|
    37|### For Framework/Contracts Repos:
    38|1.  In your project's `README.md`, add:
    39|    > "This project is licensed under the **Open-Pact License v1.1**. See [open-pact/license](https://github.com/open-pact/license) for full terms."
    40|2.  In your `package.json` or `cargo.toml` or `pyproject.toml`:
    41|    ```toml
    42|    license = "OPL-1.1"
    43|    ```
    44|
    45|### For Compliance Bots:
    46|The **Royalty Registry** is not located in this repository. It is located in the [open-pact/framework](https://github.com/open-pact/framework) repository. Compliance bots should scan the on-chain registry to verify if a user holds a "License Record."
    47|
    48|---
    49|
    50|*Generated for the Open-Pact Guild.*
    51|