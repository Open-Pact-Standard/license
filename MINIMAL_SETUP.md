# Minimum Viable Setup for OPL-1.1

## Does OPL-1.1 require smart contracts to work?

**No.** OPL-1.1 is a copyright license. It is legally enforceable through traditional
copyright law regardless of whether you deploy any smart contracts or other infrastructure.

The smart contracts and tools we provide are **enforcement enhancers**, not requirements.
They automate royalty collection, provide technical evidence of infringement, and enable
frictionless payments -- but the license text alone establishes your rights.

## Setup Tiers

### Tier 0: Text-Only (Solo Devs)
**What you need:**
- The `LICENSE.md` file in your repository
- Copyright headers in your source files

**What works:**
- ✅ Copyright protection against unauthorized use
- ✅ Legal basis for cease-and-desist claims
- ✅ Individual contributors retain their rights
- ✅ Abandonware protection (36-month sunset)

**What's missing:**
- ❌ No automated royalty collection
- ❌ No technical enforcement evidence
- ❌ No frictionless payments
- ❌ Manual fee negotiation required

### Tier 1: Basic Registry (Small Projects)
**What you need:**
- Everything in Tier 0
- `REGISTRY.md` or `REGISTRY.json` published in your repository (see below)
- Email or wallet address for receiving inquiries

**What works:**
- ✅ Published fee schedule (establishes "Registry" per OPL-1.1)
- ✅ Clear pricing for commercial users
- ✅ Derivative reciprocity obligations published
- ✅ Good-faith compliance for users who want to pay

**What's missing:**
- ❌ Manual invoicing required
- ❌ No automated enforcement
- ❌ No canary tokens

### Tier 2: Smart Contract Automation (Growing Projects)
**What you need:**
- Everything in Tier 1
- RoyaltyRegistry smart contract deployed (mainnet or L2)
- Project Registry URL pointing to the contract address
- LicenseIssuer interface for user-facing purchases

**What works:**
- ✅ Automated royalty collection
- ✅ Immutable fee schedule (tamper-proof)
- ✅ Contributor distribution automation
- ✅ On-chain License Records for compliance verification

**What's missing:**
- ❌ No canary enforcement tokens
- ❌ No x402 frictionless payments

### Tier 3: Full Enforcement Stack (Professional/Enterprise)
**What you need:**
- Everything in Tier 2
- Canary Token Embedding Tool (canary embedding in distributions)
- CanaryRegistry on-chain registration
- x402 payment facilitator (optional, for micro-payments)
- Guild governance (optional, for multi-contributor projects)

**What works:**
- ✅ Automated royalty collection
- ✅ Technical evidence of infringement (canary tokens)
- ✅ Frictionless x402 payments
- ✅ Community governance
- ✅ Full enforcement pipeline

---

## The Fallback Registry (Tier 1)

If you don't deploy smart contracts, you can satisfy the "Project Registry" requirement
by publishing a simple JSON file. This satisfies the license's requirement that fees be
"defined in the Project Registry" without requiring on-chain infrastructure.

### REGISTRY.json Template

Create a file named `REGISTRY.json` in your repository root:

```json
{
  "$schema": "https://open-pact.org/schemas/registry-v1.json",
  "project": {
    "name": "Your Project Name",
    "repository": "https://github.com/your-org/your-project",
    "license_version": "OPL-1.1"
  },
  "steward": {
    "type": "solo",
    "contact": "steward@your-email.com",
    "ens_or_wallet": "0x1234567890abcdef",
    "last_updated": "2026-04-06"
  },
  "commercial_fees": [
    {
      "tier": "Tier1_Individual",
      "type": "flat",
      "amount": 100,
      "currency": "USDC",
      "conditions": {
        "description": "Individuals and small teams",
        "max_revenue": 100000
      }
    },
    {
      "tier": "Tier3_Organization",
      "type": "flat",
      "amount": 1000,
      "currency": "USDC",
      "conditions": {
        "description": "Organizations",
        "max_revenue": 5000000
      }
    },
    {
      "tier": "Tier4_LargeOrg",
      "type": "revenue_share",
      "percentage": 2.5,
      "currency": "USDC",
      "conditions": {
        "description": "Large organizations",
        "min_revenue": 5000000
      }
    }
  ],
  "ai_training": {
    "type": "custom",
    "base_fee": 5000,
    "currency": "USDC",
    "disclosure_required": true
  },
  "derivative_reciprocity": {
    "percentage": 20,
    "description": "Original Steward receives 20% of Derivative Work revenues (per Section 5.2)"
  },
  "payment_instructions": {
    "method": "email",
    "details": "Email steward@your-email.com with your project details and totalWorkforce count. You will receive an invoice with payment instructions.",
    "accepted_currencies": ["USDC", "USDT", "ETH"]
  },
  "registry_metadata": {
    "version": "2026-04-06",
    "canonical_url": "https://github.com/your-org/your-project/blob/main/REGISTRY.json",
    "ipfs_hash": "QmXYZ..."
  }
}
```

### How to Use the Fallback Registry

1. **Create** `REGISTRY.json` in your repository root using the template above
2. **Customize** the fee tiers to match your project's needs
3. **Reference** it in your `README.md`:
   ```
   This project is licensed under OPL-1.1.
   Fee schedule: https://github.com/your-org/your-project/blob/main/REGISTRY.json
   Contact: steward@your-email.com
   ```
4. **Update** it when you want to change pricing (the file is your Registry)

### What the Fallback Registry Provides

- ✅ **Satisfies OPL-1.1's "Project Registry" requirement** — fees are published and discoverable
- ✅ **Establishes clear pricing** — users know what they owe
- ✅ **Contact information** — users can initiate good-faith negotiations
- ✅ **No infrastructure needed** — just a JSON file on GitHub

### Limitations of the Fallback Registry

- ❌ **Manual enforcement** — you must track compliance yourself
- ❌ **No automatic royalty collection** — users must email you to pay
- ❌ **No technical evidence** — you can't prove which distribution a derived work came from
- ❌ **Versioning** — you must manually track which version of the Registry applied when

---

## How Enforcement Works Without Smart Contracts

OPL-1.1 is a **copyright license**. Enforcement relies on copyright law, not smart contracts.

### Your Legal Rights (Text-Only Setup)
1. **Copyright ownership** — you own the code, users need your license to use it
2. **Cease-and-desist** — if they violate the license, you can demand they stop
3. **Damages** — if they refuse, you can sue for copyright infringement
4. **Registry as evidence** — your published REGISTRY.json proves what fees were published

### How Registry Enhances Enforcement
1. **Smart contracts** — automate collection, provide immutable on-chain records
2. **Canary tokens** — provide technical evidence that code was derived from yours
3. **x402 payments** — make payment frictionless (easier to comply than to evade)

### The Analogy
- **License text** = the law
- **Registry** = the published fee schedule
- **Smart contracts** = the automated tax collection system
- **Canary tokens** = forensic evidence for investigators

You need the first two to have a working system. The rest are nice-to-have automation.
