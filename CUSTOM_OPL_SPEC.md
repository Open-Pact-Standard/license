# Custom OPL — Clause-Library Configurator Spec (DRAFT)

**Status:** Design draft. Depends on OPL-1.4 (opt-in DOSP + Commercial Terms file). Not yet implemented.

## 1. The idea

OPL-1.4 is one license with fixed clauses. Projects differ. **Custom OPL** lets a
Maintainer author a *bespoke variant* of OPL for their project by choosing
parameters, and the service emits a coherent, legally-structured license
document. Examples a user might want:

- **DOSP = 120 months** (10-year horizon) instead of the 24-60 recommended range.
- **Abandonment = freeze-forever** — the Work stays source-available even if the
  Maintainer vanishes; no automatic Apache 2.0 conversion. An immutable contract
  that never frees the code.
- **Fixed commercial rate, immutable even on abandonment** — the price cannot be
  raised by a future steward; the COMMERCIAL_TERMS.md is binding for the version's
  life.
- General "curtail your own license needs as you want" — a dial-a-license over a
  vetted clause set.

This is the **"license as a service"** layer: OPL-the-base-license stays
local-first and free; Custom OPL is the optional value-add that authors the
variant.

## 2. Non-negotiable design constraints (keep OPL's trust)

1. **Parameterized from vetted fragments ONLY.** The configurator assembles the
   license from a fixed library of pre-approved clause fragments. It does **not**
   allow free-form clause editing. Every output is a known-good combination.
   This is what makes "service generates your license" *trustworthy* rather than
   *reckless*. (Free-form AI-written licenses = unlimited liability; we do not do
   that.)
2. **Base OPL stays the no-account path.** Adoption must never *require* the
   service. A developer can still hand-write a NOTICE and use OPL-1.4 directly.
   Custom OPL is opt-in convenience.
3. **Local-first generation.** The configurator can run locally (same as
   `opl_init.py`); hosting/accounts are a later, optional layer. No required
   server, no required registry.
4. **Transparency.** Every generated Custom OPL embeds a machine-readable
   "provenance block" listing the exact parameters chosen and the fragment IDs
   used, so any output is reproducible and auditable.

## 3. The parameter surface (v1 of the configurator)

Each parameter maps to one or more vetted fragment slots in the license:

| Parameter | Options | Emits clause |
|---|---|---|
| **Commercial model** | Paid (Standard Terms) / Free-for-all / Personal-only | §3.3 variant |
| **DOSP** | Off (default) / N months (any value, incl. >60) / Forever-frozen (no conversion) | §5.1 variant |
| **Abandonment** | Convert-to-Apache (default) / Freeze-forever (no conversion) / Custom period (12-60) | §5 variant |
| **OPL-AI** | Out (default) / In | §3.5 + OPL-AI addendum toggle |
| **Rate stability** | Changeable / Immutable-per-version (binding COMMERCIAL_TERMS) | §13 + Commercial Terms fragment |
| **Jurisdiction** | from vetted list / custom | §12 + NOTICE |
| **Derivative light-copyleft** | On (default) / Off | §3.2 variant |
| **Trademark** | None / Asserted | §10 fragment |

## 4. Fair.io boundary (must be explicit)

Fair Source *requires* Delayed Open Source Publication. Therefore Custom OPL
splits into two labeled tiers:

- **Fair-Source (Custom OPL):** the variant keeps a DOSP conversion (any N,
  including >60). Eligible for Fair.io listing as an OPL variant.
- **Source-Available (Custom OPL):** the variant sets DOSP = Forever-frozen or
  Abandonment = Freeze-forever (no conversion). NOT Fair Source. Marketed
  honestly as "Source-Available (Custom OPL)", never as Fair Source.

The configurator **refuses to label a no-conversion variant as Fair Source** and
warns the user at generation time.

## 5. Liability & safety

- Output is labeled "generated from vetted fragments; not legal advice."
- Every fragment carries a stability rating; the configurator only combines
  fragments whose interaction matrix is pre-validated (e.g. "Forever-frozen +
  Fair.io submission = incompatible" is a hard block, not a soft warning).
- A changelog of fragment versions is kept so a generated license's provenance
  block can be re-validated later.

## 6. Implementation sketch (phased)

- **Phase A (local, now):** Extend `opl_init.py` / `opl-adopt` skill to accept the
  parameter surface above and assemble the license from fragment templates held
  in a `custom-opl/fragments/` directory. Emit LICENSE + NOTICE + COMMERCIAL_TERMS
  + provenance block. Local-only.
- **Phase B (validation):** Use the ported legal skills (`legal/ambiguity-stress-test`,
  `legal/contract-risk-analyzer`) as an automated pre-publish check on each
  generated combination.
- **Phase C (optional hosted):** A web front-end over Phase A/B, accounts optional,
  for users who want a hosted generator. Does NOT store user code; only the
  parameter set + emitted files.

## 7. Open questions for the Maintainer

1. Fragment library scope: start with the ~8 parameters above, or narrower?
2. Do we allow **free-form** editing of a generated variant (max flexibility, max
   liability) or **parameter-only** (safe)? **Recommendation: parameter-only.**
3. Branding: is "Custom OPL" the right name, or "OPL Studio" / "OPL Forge"?
4. Does a generated Custom OPL need its own SPDX-style identifier (e.g.
   `OPL-1.4-CUSTOM-<hash>`) for tooling/validation?

---
*This spec is a design draft. Nothing here changes OPL-1.4's text. The base
license remains the local-first, no-account path; Custom OPL is an optional
authoring layer built on top of it.*
