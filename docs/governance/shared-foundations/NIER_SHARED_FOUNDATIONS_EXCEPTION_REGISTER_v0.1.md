# Nier Shared Foundations Exception Register v0.1

## Status

Exception register for Nier's Shared Foundations inheritance.

This register records where Shared Foundations context is limited, specialized, or not
inherited by Nier. It does not modify the canonical Shared Foundations repository and
does not replace Nier-specific billing governance.

## Canonical Reference

`https://github.com/RainAndRiverSky/OpenClaw_Shared_Foundations`

## Current Exceptions

No active conflict exceptions are recorded at adoption.

## Standing Nier Reservations

The following reservations are not conflicts. They are Nier-specific boundaries that
govern all Shared Foundations inheritance:

| Reservation | Rule | Nier authority |
| --- | --- | --- |
| Billing governance | Shared Foundations context cannot replace Nier's billing charter, billing domain, canonical objects, lifecycle integrity requirements, or governance decisions. | `OPENCLAW_BILLING_CHARTER_v0.1.md`; `NIER_GOVERNANCE_STATUS_v0.1.md` |
| Evidence and audit | Shared Foundations context cannot lower Nier's billing evidence, provenance, retention, attribution, decision-traceability, or append-only audit expectations. | `OPENCLAW_BILLING_CHARTER_v0.1.md` |
| Authorization | Shared Foundations context cannot weaken deny-by-default scope, actor identity, approval, elevated authorization, or separation-of-duties requirements for billing actions. | `OPENCLAW_BILLING_CHARTER_v0.1.md` |
| Reconciliation and entitlements | Shared Foundations context cannot replace Nier's provider, local, usage, invoice, reconciliation, or entitlement governance requirements. | `OPENCLAW_BILLING_CHARTER_v0.1.md`; `NIER_GOVERNANCE_STATUS_v0.1.md` |
| Provider boundary | Shared Foundations context cannot authorize payment processing, provider settlement declarations, provider-state rewriting, or silent trust in external provider state. | `OPENCLAW_BILLING_CHARTER_v0.1.md` |
| Runtime implementation | Shared Foundations context cannot create implementation authority while Nier remains in governance foundation phase. | `README.md`; `NIER_GOVERNANCE_STATUS_v0.1.md` |

## Exception Record Format

Future exceptions should use this format:

```text
Exception ID:
Date:
Shared Foundations reference:
Nier artifact affected:
Conflict or limitation:
Decision:
Rationale:
Review requirement:
```

## Review Rule

If a future Shared Foundations update appears to affect Nier billing governance,
authorization, evidence, reconciliation, entitlement governance, provider boundaries,
audit expectations, runtime authority, or operational billing admission, the issue must
be recorded here before Nier treats the inherited context as applicable.
