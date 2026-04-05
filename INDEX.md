# 📦 Open-Pact Release Manifest (v1.1)

This document serves as the master index for the **Open-Pact License v1.1 (OPL-1.1)** release package.

## 1. File Directory

| File | Description | Target Audience |
| :--- | :--- | :--- |
| **LICENSE.md** | The canonical legal text of OPL-1.1. | Legal Teams, Compliance Tools |
| **README.md** | The "Pitch." Explains the Tiers, the Guild, and why we built this. | Developers, Public Visitors |
| **RATIONALE.md** | The philosophy behind the license (The "AI Tax" and sustainability). | Journalists, Policy Makers |
| **NOTES.md** | Section-by-section commentary in plain English. | Reviewers, curious developers |
| **FAQ.md** | Answers to hard questions (Commercial rights, AI training, Forking). | CTOs, Legal Counsel |

## 2. Repository Setup Checklist

When creating the `open-pact/license` repository, follow these steps:

- [x] **1. Upload all .md files** from this folder to the root.
- [x] **2. Set Description:** "Source-Available Software for the Age of AI. Governed by Guilds."
- [x] **3. Set Topics:** `license`, `software-licensing`, `ai-safety`, `fair-source`, `open-pact`.
- [x] **4. License:** Select "Custom License" in GitHub's settings and point it to `LICENSE.md`.
- [ ] **5. Pin Repo:** Pin the repository to the top of the "open-pact" organization profile.

## 3. Versioning Status

*   **Current Version:** 1.1
*   **Status:** **Soft Launch Candidate.** Ready for public review.
*   **Major Changes from v1.0:** 
    *   Added "Internal Evaluation" rights (Section 2.3).
    *   Added "Stewardship Sunset" (Section 16) - auto-converts to Apache 2.0 after 3 years of inactivity.
    *   Enhanced "Derivative Works" definition to include Code Integrations (Section 1.8).
    *   Added "Whistleblower Fund" and "Automated Auditing" permissions (Section 11 & 17).

## 4. Integration Guide

### For Framework/Contracts Repos:
1.  In your project's `README.md`, add:
    > "This project is licensed under the **Open-Pact License v1.1**. See [open-pact/license](https://github.com/open-pact/license) for full terms."
2.  In your `package.json` or `cargo.toml` or `pyproject.toml`:
    ```toml
    license = "OPL-1.1"
    ```

### For Compliance Bots:
The **Royalty Registry** is not located in this repository. It is located in the [open-pact/framework](https://github.com/open-pact/framework) repository. Compliance bots should scan the on-chain registry to verify if a user holds a "License Record."

---

*Generated for the Open-Pact Guild.*
