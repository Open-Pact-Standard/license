# Open-Pact License v1.4 (OPL-1.4)

**A fair-source license**: free for personal use, paid for commercial use. The Maintainer decides how.

> [v1.4 draft](LICENSE.md) · [CHANGELOG](CHANGELOG.md) · [LICENSE](LICENSE.md)

## What this is

OPL-1.4 is a **fair-source** license with two tiers:

- **Personal Use — free.** Use, modify, and share the Work for study, personal projects, education, research, and internal non-revenue tooling. No gate, no permission, no fee, no registry.
- **Commercial Use — paid at the Maintainer's price.** When someone profits from the Work, they pay the Maintainer per the Standard Terms the Maintainer publishes. The Maintainer sets the price, chooses the payment mechanism, and chooses whether to restrict AI training. The license does not prescribe a rate.

This is the **Polyform Mixed** model. v1.3.1 supersedes v1.2 (Reciprocity) and v1.1.

**No chain. No system token. No DAO. No registry required.** The license is the contract. The only external dependency is the Standard Terms URL — an HTTPS HTML page where the Maintainer publishes their pricing and payment mechanism. The Maintainer can use Stripe, a bank transfer, an email address, a smart contract address (for documentation), or any other mechanism they choose. x402-style crypto payments are supported as an optional payment mechanism via the adoption tools.

OPL-1.3.1 is not "open source" as defined by the Open Source Initiative. It restricts commercial use unless the Maintainer has published Standard Terms and you comply with them. That is the trade-off, and it is intentional.

## What is NOT part of this license

- **No on-chain registry.** The license does not require deploying smart contracts, registering on a chain, or paying gas.
- **No system token.** There is no $OPL token and no token economics in this license.
- **No DAO or guild governance.** The Maintainer is the steward. There is no governance layer.
- **No registry requirement.** The framework repository (if it exists) is an optional, separate product. It is not required by this license.

These things may exist as separate products or optional tools, but they are not part of OPL-1.3.1. A creator can adopt this license in under an hour with three Python commands and a Standard Terms page. See [SYSTEM_DESIGN.md](SYSTEM_DESIGN.md) for the full architecture.

## Quick start

To apply OPL-1.4 to a Work:

1. **Copy [LICENSE.md](LICENSE.md)** into your repository root.
2. **(Optional) Copy [OPL-AI.md](OPL-AI.md)** if you want AI training restricted. By default, the OPL-AI addendum is **not** incorporated; the Maintainer must opt in via `NOTICE`.
3. **Create a `NOTICE` file** using [NOTICE.example](NOTICE.example) as a template. At minimum you need:
   - `OPL Version: 1.4`
   - `Maintainer: <name and reachable contact>`
   - `Governing Jurisdiction: <state/province, country>`
   - `Standard Terms URL: <URL where your commercial-use pricing lives>`
   - `OPL-AI: opted in.` (or `opted out.` — default is opt-out)
   - *(Optional)* `DOSP period: <months>` — declare to opt into scheduled conversion to Apache 2.0 (recommended 24-60; silent = no scheduled conversion).
   - *(Optional)* `Commercial Terms file: COMMERCIAL_TERMS.md` — pin immutable per-Version commercial terms.
4. **Add `SPDX-License-Identifier: OPL-1.4`** to each source file.
5. **Reference the license** from your package manifest (`pyproject.toml`, `Cargo.toml`, `package.json`, etc.) using the SPDX identifier.

That's it. No registry, no on-chain fee collection, no framework required. The license is the contract.

## Adoption tools

Free CLI tools for adopting OPL-1.4 — automate every step of the quick start above:

| Tool | What it does |
|------|-------------|
| [`opl_init.py`](https://github.com/Open-Pact-Standard/tools/blob/main/tools/opl_init.py) | Generate a valid `NOTICE` file (interactive or `--non-interactive`) |
| [`opl_spdx_inject.py`](https://github.com/Open-Pact-Standard/tools/blob/main/tools/opl_spdx_inject.py) | Add `SPDX-License-Identifier: OPL-1.4` to every source file (60+ languages) |
| [`opl_check.py`](https://github.com/Open-Pact-Standard/tools/blob/main/tools/opl_check.py) | Validate compliance: LICENSE, NOTICE, SPDX headers, Standard Terms URL |
| [`opl_registry_gen.py`](https://github.com/Open-Pact-Standard/tools/blob/main/tools/opl_registry_gen.py) | Generate `REGISTRY.json` for Tier 1 adopters with structured fee schedules |
| [`opl_migrate.py`](https://github.com/Open-Pact-Standard/tools/blob/main/tools/opl_migrate.py) | Migrate from MIT/Apache/GPL/BSD — auto-detect license, generate report |

```bash
# Quick start with tools (run from your project root):
git clone https://github.com/Open-Pact-Standard/tools.git .opl-tools
python3 .opl-tools/tools/opl_init.py --non-interactive   --maintainer "Your Name <you@example.com>"   --jurisdiction "California, United States"   --terms-url "https://example.com/standard-terms"
python3 .opl-tools/tools/opl_spdx_inject.py .
python3 .opl-tools/tools/opl_check.py . --skip-remote
```

See the [tools repo](https://github.com/Open-Pact-Standard/tools) for full documentation.

## The 3 v1.3.1 patches (vs. v1.3)

v1.3.1 is a clarification release on top of v1.3. The substance of v1.3 is preserved; only 3 open ambiguities are resolved:

1. **Standard Terms URL validity (LICENSE \u00a73.3).** A "Valid" URL now satisfies **7 criteria**: HTTPS, redirect-following, HTML, no-authentication, no-JavaScript-only rendering, reasonable stability, and substantive content. A rebuttable-presumption rule with burden allocation applies in disputes (User shows failure, Maintainer shows satisfaction).

2. **Wind-down of Commercial Use (LICENSE \u00a73.7, new).** If a Maintainer revokes Commercial Use or materially changes the Standard Terms, existing commercial users are granted a **90-day wind-down period** to negotiate, migrate, or stop using the Work. The \u00a75 abandonment clock and the \u00a73.7 wind-down clock **run in parallel**.

3. **OPL-AI opt-in syntax (OPL-AI \u00a78.1\u2013\u00a78.3, new).** A canonical syntax for declaring AI training restrictions: `OPL-AI: opted in.` (or `opted out.`). Six parsing rules, a versioning rule, and 16+ examples.

See [CHANGELOG.md](CHANGELOG.md) for the full release notes.

## Files in this repo

- [LICENSE.md](LICENSE.md) — the v1.3.1 license text
- [OPL-AI.md](OPL-AI.md) — the v1.3.1 AI training addendum (incorporated only if Maintainer opts in)
- [NOTICE.example](NOTICE.example) — template for the required `NOTICE` file
- [CHANGELOG.md](CHANGELOG.md) — release notes for v1.1, v1.3, and v1.3.1

## Status

OPL-1.3.1 is **published** — see the [v1.3.1 release](https://github.com/Open-Pact-Standard/license/releases/tag/v1.3.1) — and now awaits broader community and legal review for the 1.4 cycle. The license is functional and complete; refinements are tracked in [CHANGELOG.md](CHANGELOG.md).

For questions or feedback, open an issue on this repo.

<!-- ci-test-2 2026-06-11T18:10:43Z -->
