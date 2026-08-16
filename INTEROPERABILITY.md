# OPL Interoperability — Independently Governed, Fair-Source-Aligned

**Status:** Positioning note for OPL-1.4. Non-normative.

## The position in one sentence

Open-Pact License (OPL) is **independently governed** by the Open-Pact-Standard
org (Ikaros Digital LLC) and is **not** a submission to, nor under the
stewardship of, the Fair Source movement or any other external registry. At the
same time, OPL is **designed to be interoperable** with fair-source norms *in
case* a downstream user, customer, or tooling ecosystem wants that bridge — the
interoperability is structural, not opt-in paperwork.

You do your own thing. The bridge is already built.

## Why this is the right position

- **Sovereignty.** OPL's red lines (no forced rolling conversion, creator
  autonomy paramount, zero-infra, no registry required) are enforced by the
  license text itself, not by an external org's approval. Submitting to a
  registry would dilute that.
- **Interop without subordination.** Fair-source compatibility is expressed
  *through* OPL's own mechanics (see below), so a user who needs fair-source
  posture gets it without OPL ceasing to be its own standard.
- **Tooling already speaks the bridge.** The conversion target is Apache
  License 2.0 — the most widely parsed license identifier on earth. The moment
  a Version converts, every scanner, registry, and compliance tool understands
  it natively.

## The structural interop bridges

### 1. Apache-2.0 conversion (the universal bridge)

Both OPL conversion triggers land on **Apache License 2.0**:

- **§5 Abandonment** — if no Maintainer is reachable for the declared period
  (default 36 months), the Work converts to Apache-2.0 (§5, line 162).
- **§5.1 DOSP (opt-in)** — if the Maintainer affirmatively declares a DOSP
  period in `NOTICE`, each Version converts to Apache-2.0 on schedule
  (§5.1, line 174).

> The conversion is **automatic**. No third-party authorization, fiscal
> sponsor, or public notice is required.

**Interop consequence:** an OPL work is, by construction, a *deferred*
Apache-2.0 work. Anyone who needs Apache-2.0 compatibility can either (a) wait
for the trigger, or (b) — if the Maintainer opted into DOSP — rely on the
scheduled conversion. No relicensing negotiation is ever required.

### 2. SPDX identifier

OPL emits a valid SPDX-style identifier: `OPL-1.4`. The `opl-adopt` tooling
writes it into every source file (`SPDX-License-Identifier: OPL-1.4`) and the
package manifest. Tooling that recognizes SPDX can *name* the license even
before it understands the semantics; tooling that doesn't can still scan for the
string.

### 3. Fair-source concepts, expressed in OPL terms

| Fair-Source concept | OPL equivalent | Notes |
|---|---|---|
| Delayed open-source publication | §5.1 DOSP (opt-in) | Silent `NOTICE` = no scheduled conversion. OPL is fair-source *by choice*, not by force. |
| Abandonment → open source | §5 abandonment | Same intent, simplified: no fiscal sponsor, no public-notice burden on a solo Maintainer. |
| Commercial use permitted with terms | §3.3 Valid Standard Terms URL | Maintainer publishes their own pricing; no central marketplace. |
| Patent grant | §6 | Mirrors Apache-2.0 / standard fair-source patent terms. |
| Converted form is a known OSS license | Apache-2.0 | Universal interop target. |
| Non-commercial / source-available variant | Custom OPL "Source-Available" variant | Honestly *not* fair-source; documented as such (see below). |

### 4. Custom OPL variants and the boundary

The Custom OPL configurator (in `Open-Pact-Standard/tools`) produces two
families:

- **Fair-Source-compatible Custom OPL** — DOSP kept (or abandonment kept),
  commercial terms permitted. This is interoperable with the fair-source
  posture: a downstream consumer gets eventual Apache-2.0 + fair commercial
  terms.
- **Source-Available Custom OPL** — conversion disabled (e.g. "freeze-forever").
  This is **deliberately not fair-source** and is labeled as such by the
  configurator's hard-block. It remains interoperable at the *tooling* level
  (SPDX string, NOTICE format) but does not promise a future open-source
  conversion.

> Honesty rule: a Source-Available Custom OPL variant must **not** be described
> as "fair source." OPL's interop story is real precisely because it does not
> overclaim.

## For tooling authors

If you build license scanners, registries, or compliance tooling and want to
support OPL:

1. **Treat `OPL-1.4` as a deferred-Apache-2.0 identifier.** The simplest
   correct interpretation: an OPL-licensed work will, on its conversion trigger
   (§5 and/or §5.1), become Apache-2.0.
2. **Read `NOTICE`** to determine if DOSP is opted in (scheduled conversion) and
   the abandonment period (default 36 months).
3. **Do not assume forced conversion.** A silent `NOTICE` means no scheduled
   conversion — the work is source-available for its life unless abandoned.
4. **Patent + disclaimer** terms mirror standard OSS expectations; no special
   handling required.

## For downstream users who need fair-source compliance

You can adopt OPL *as* a fair-source license by simply **opting into DOSP** in
your `NOTICE` (declare a DOSP period). That single field makes your OPL work
express the fair-source delayed-publication posture, while keeping OPL's
sovereignty guarantees (no registry, no fiscal sponsor, your own commercial
terms). If you later need literal Apache-2.0, the conversion arrives on
schedule or on abandonment — automatically.

---

*OPL is its own standard. The fair-source bridge is a feature, not a dependency.*
