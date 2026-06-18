# Nier Shared Foundations Inheritance Map v0.1

## Status

Inheritance map for Nier's Shared Foundations relationship.

This map identifies how Nier inherits compatible Shared Foundations context by reference.
It does not copy canonical Shared Foundations material and does not create new Nier
billing principles.

## Canonical Reference

`https://github.com/RainAndRiverSky/OpenClaw_Shared_Foundations`

## Inheritance Rules

Shared Foundations context is inherited only when all of the following are true:

- the context is compatible with Nier's billing governance identity
- the context does not weaken Nier evidence, authorization, reconciliation, entitlement,
  audit, or provider-boundary standards
- the context does not authorize payment processing or provider settlement
- the context does not authorize runtime implementation or operational billing admission
- the context does not modify historical Nier billing governance records
- the context is not already superseded by a Nier-specific artifact

When Nier-specific governance is more specific, Nier-specific governance controls.

## Map

| Shared Foundations context | Nier inheritance | Nier governing artifact | Nier authority retained |
| --- | --- | --- | --- |
| OpenClaw identity continuity | Nier participates as an OpenClaw stewarded identity while remaining a bounded billing governance identity. | `identity/NIER_STEWARD_IDENTITY_v0.1.md`; `NIER_GOVERNANCE_STATUS_v0.1.md` | Nier identity, billing governance scope, and provider boundaries remain local. |
| Stewardship discipline | Nier inherits the expectation that changes preserve lineage, intent, and accountable governance. | `OPENCLAW_BILLING_CHARTER_v0.1.md`; `docs/governance/shared-foundations/NIER_SHARED_FOUNDATIONS_ADOPTION_RECORD_v0.1.md` | Nier controls billing evidence lineage, authorization lineage, reconciliation history, and governance decision history. |
| Reference-based shared governance | Nier references Shared Foundations externally instead of copying canonical documents. | `docs/governance/shared-foundations/NIER_SHARED_FOUNDATIONS_ADOPTION_RECORD_v0.1.md` | Nier keeps local adoption records and does not create a local canonical mirror. |
| Local specialization | Nier may specialize inherited context through billing-specific governance. | `OPENCLAW_BILLING_CHARTER_v0.1.md`; `NIER_GOVERNANCE_STATUS_v0.1.md` | Nier controls billing objects, lifecycle vocabulary, evidence requirements, authorization rules, reconciliation requirements, and entitlement governance. |
| Exception handling | Conflicts or non-inherited areas are recorded locally without modifying the canonical source. | `docs/governance/shared-foundations/NIER_SHARED_FOUNDATIONS_EXCEPTION_REGISTER_v0.1.md` | Nier decides whether a Shared Foundations concept applies to Nier's billing domain. |
| Provider-boundary restraint | Shared context must not imply provider settlement authority, payment processing authority, or local rewriting of provider-reported state. | `OPENCLAW_BILLING_CHARTER_v0.1.md`; `NIER_GOVERNANCE_STATUS_v0.1.md` | Nier preserves the distinction between provider-reported state and OpenClaw governance state. |
| Operational restraint | Shared context must not imply operational billing admission, runtime implementation, integration, webhook, API, or database authority. | `README.md`; `NIER_GOVERNANCE_STATUS_v0.1.md` | Nier remains in governance foundation phase until separate admission criteria are ratified. |

## Non-Inherited Areas

Shared Foundations inheritance does not include:

- canonical Shared Foundations document copies
- replacement Nier billing charter
- replacement Nier governance status
- replacement billing evidence model
- replacement billing authorization model
- replacement reconciliation model
- replacement entitlement governance model
- replacement billing lifecycle model
- payment processing authority
- provider settlement authority
- operational billing admission
- implementation design
- runtime authorization

## Maintenance

Update this map only when Nier adopts, specializes, or excludes a Shared Foundations
relationship. Do not use this map to restate canonical Shared Foundations text.
