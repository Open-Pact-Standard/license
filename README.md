# Open-Pact License v1.3.1 (OPL-1.3.1)

**A fair-source license**: free for personal use, paid for commercial use. The Maintainer decides how.

> [v1.3.1 release](https://github.com/Open-Pact-Standard/license/releases/tag/v1.3.1) \u00b7 [CHANGELOG](CHANGELOG.md) \u00b7 [LICENSE](LICENSE.md)

## What this is

OPL-1.3.1 is a fair-source license. It lets anyone use, modify, and share the Work freely for **personal** purposes. **Commercial** use requires payment to the Maintainer per the **Standard Terms** they publish at a URL declared in `NOTICE`. The Maintainer chooses the payment mechanism \u2014 a smart contract, a Stripe link, a bank transfer, an \u201cemail me\u201d line \u2014 whatever is simplest.

This is the **Polyform Mixed** model: free Personal Use, paid Commercial Use, Maintainer-controlled pricing. v1.3.1 supersedes v1.2 (Reciprocity) and v1.1.

OPL-1.3.1 is not \u201copen source\u201d as defined by the Open Source Initiative. It restricts commercial use unless the Maintainer has published Standard Terms and you comply with them. That is the trade-off, and it is intentional.

## Quick start

To apply OPL-1.3.1 to a Work:

1. **Copy [LICENSE.md](LICENSE.md)** into your repository root.
2. **(Optional) Copy [OPL-AI.md](OPL-AI.md)** if you want AI training restricted. By default, the OPL-AI addendum is **not** incorporated; the Maintainer must opt in via `NOTICE`.
3. **Create a `NOTICE` file** using [NOTICE.example](NOTICE.example) as a template. At minimum you need:
   - `OPL Version: 1.3.1`
   - `Maintainer: <name and reachable contact>`
   - `Governing Jurisdiction: <state/province, country>`
   - `Standard Terms URL: <URL where your commercial-use pricing lives>`
   - `OPL-AI: opted in.` (or `opted out.` \u2014 default is opt-out)
4. **Add `SPDX-License-Identifier: OPL-1.3.1`** to each source file.
5. **Reference the license** from your package manifest (`pyproject.toml`, `Cargo.toml`, `package.json`, etc.) using the SPDX identifier.

That\u2019s it. No registry, no on-chain fee collection, no framework required. The license is the contract.

## The 3 v1.3.1 patches (vs. v1.3)

v1.3.1 is a clarification release on top of v1.3. The substance of v1.3 is preserved; only 3 open ambiguities are resolved:

1. **Standard Terms URL validity (LICENSE \u00a73.3).** A \u201cValid\u201d URL now satisfies **7 criteria**: HTTPS, redirect-following, HTML, no-authentication, no-JavaScript-only rendering, reasonable stability, and substantive content. A rebuttable-presumption rule with burden allocation applies in disputes (User shows failure, Maintainer shows satisfaction).

2. **Wind-down of Commercial Use (LICENSE \u00a73.7, new).** If a Maintainer revokes Commercial Use or materially changes the Standard Terms, existing commercial users are granted a **90-day wind-down period** to negotiate, migrate, or stop using the Work. The \u00a75 abandonment clock and the \u00a73.7 wind-down clock **run in parallel**.

3. **OPL-AI opt-in syntax (OPL-AI \u00a78.1\u2013\u00a78.3, new).** A canonical syntax for declaring AI training restrictions: `OPL-AI: opted in.` (or `opted out.`). Six parsing rules, a versioning rule, and 16+ examples.

See [CHANGELOG.md](CHANGELOG.md) for the full release notes.

## Files in this repo

- [LICENSE.md](LICENSE.md) \u2014 the v1.3.1 license text
- [OPL-AI.md](OPL-AI.md) \u2014 the v1.3.1 AI training addendum (incorporated only if Maintainer opts in)
- [NOTICE.example](NOTICE.example) \u2014 template for the required `NOTICE` file
- [CHANGELOG.md](CHANGELOG.md) \u2014 release notes for v1.1, v1.3, and v1.3.1

## Status

OPL-1.3.1 is **published** — see the [v1.3.1 release](https://github.com/Open-Pact-Standard/license/releases/tag/v1.3.1) — and now awaits broader community and legal review for the 1.4 cycle. The license is functional and complete; refinements are tracked in [CHANGELOG.md](CHANGELOG.md).

For questions or feedback, open an issue on this repo.

<!-- CI test marker 2026-06-11T17:52:06Z -->
