# Nier

## OpenClaw Billing Governance Steward

Nier governs billing evidence, authorization, reconciliation, entitlements, and lifecycle integrity across the OpenClaw ecosystem.

## Mission Statement

Nier provides a durable, provider-neutral governance layer for billing-related decisions. Its mission is to ensure that consequential billing actions are authorized, evidence-backed, reconciled, auditable, and reflected correctly in customer entitlements.

## Governance Domain

Nier's governance domain includes:

- Billing identities, actors, roles, and delegated authority
- Customers, accounts, plans, subscriptions, and trials
- Invoices, payments, refunds, credits, and usage records
- Provider events and normalized governance states
- Entitlement grants, changes, suspensions, restorations, and revocations
- Evidence provenance, retention, and decision traceability
- Reconciliation, exception handling, alerts, and audit records

Payment providers remain authoritative for settlement state. Nier observes provider evidence and governs how OpenClaw authorizes, reconciles, records, and acts on that evidence.

## Current Phase

**Governance Foundation Phase**

The current work establishes Nier's identity, authority boundaries, canonical governed objects, principles, and readiness criteria. This repository does not yet contain billing integrations or operational billing services.

## Shared Foundations

Nier references Shared Foundations by Reference + Inheritance only from the canonical
public repository:

`https://github.com/RainAndRiverSky/OpenClaw_Shared_Foundations`

Canonical Shared Foundations documents are not copied into this repository. Nier retains
authority over billing governance, billing evidence, authorization, reconciliation,
entitlements, provider boundaries, billing lifecycle integrity, and billing audit
expectations.

## Core Responsibilities

- Require evidence before consequential billing actions
- Apply deny-by-default authorization and scoped approvals
- Validate governed lifecycle transitions
- Reconcile provider, local, usage, invoice, and entitlement evidence
- Detect mismatches, stale states, duplicates, and policy violations
- Govern entitlement outcomes derived from billing evidence
- Preserve immutable, attributable decision history
- Escalate exceptions and high-risk actions to accountable reviewers
- Maintain provider-neutral governance rules and object definitions

## Relationship to OpenClaw Runtime

Nier is intended to operate as a governance control plane for billing-related activity across OpenClaw Runtime, agents, MCP-connected services, and supporting operational systems.

Future runtime integration should enforce governance before actions execute and record outcomes afterward. Runtime components may supply identity, usage, provider, and operational evidence, but they do not replace Nier's policy, authorization, reconciliation, or audit responsibilities.

## Provider-Neutral Philosophy

Nier governs billing behavior independently of any specific payment or subscription provider. Provider adapters may report external identifiers, events, and settlement states, while canonical governance objects and policies remain stable.

Provider-specific state must never silently become trusted OpenClaw state. It must be authenticated, correlated, normalized, reconciled, and retained as evidence.

## Future Roadmap

1. Ratify the billing governance charter and canonical object definitions.
2. Define complete lifecycle state models and allowed transitions.
3. Define evidence schemas, provenance rules, and retention expectations.
4. Define authorization roles, approval thresholds, and separation of duties.
5. Define reconciliation policies, exception classes, and alert severity.
6. Define entitlement governance and restoration requirements.
7. Design provider-neutral integration contracts.
8. Validate runtime and MCP integration boundaries.
9. Implement governance controls only after foundation approval.

No payment processing, provider integration, API, webhook, or database implementation is included in this phase.

## Repository Structure

```text
.gitignore
README.md
LICENSE
OPENCLAW_BILLING_CHARTER_v0.1.md
identity/
  NIER_STEWARD_IDENTITY_v0.1.md
docs/
  governance/
    shared-foundations/
      NIER_GOVERNANCE_STATUS_v0.1.md
      NIER_SHARED_FOUNDATIONS_ADOPTION_RECORD_v0.1.md
      NIER_SHARED_FOUNDATIONS_INHERITANCE_MAP_v0.1.md
      NIER_SHARED_FOUNDATIONS_EXCEPTION_REGISTER_v0.1.md
  handoffs/
    Published milestone handoff records
evidence/
  PORTABILITY-AUDIT-20260621/
    audit_notes.md
```

## Documentation

Primary governance documents:

- `OPENCLAW_BILLING_CHARTER_v0.1.md`
- `docs/governance/shared-foundations/NIER_GOVERNANCE_STATUS_v0.1.md`
- `identity/NIER_STEWARD_IDENTITY_v0.1.md`
- `docs/governance/shared-foundations/NIER_SHARED_FOUNDATIONS_ADOPTION_RECORD_v0.1.md`
- `docs/governance/shared-foundations/NIER_SHARED_FOUNDATIONS_INHERITANCE_MAP_v0.1.md`
- `docs/governance/shared-foundations/NIER_SHARED_FOUNDATIONS_EXCEPTION_REGISTER_v0.1.md`

Published milestone handoffs:

- `docs/handoffs/✨🌊 COMPLETE — OPENCLAW BILLING GOVERNANCE STEWARD NIER FOUNDATION + FIRST ADMISSION CHECKPOINT HANDOFF 🌊✨.md`
- `docs/handoffs/✨🌊 COMPLETE — NIER SHARED FOUNDATIONS ADOPTION + GOVERNANCE ALIGNMENT HANDOFF 🌊✨.md`
- `docs/handoffs/✨🌊 COMPLETE — NIER BILLING GOVERNANCE AUTHORITY INVESTIGATION + ROOT AUTHORITY DISCOVERY HANDOFF 🌊✨.md`
- `docs/handoffs/✨🌊 COMPLETE — NIER FOUNDATION PROMOTION + BILLING DECISION AUTHORITY VALIDATION + GITHUB PUBLICATION COMPLETION HANDOFF 🌊✨.md`
- `docs/handoffs/✨🌊 COMPLETE — NIER PUBLIC READINESS VALIDATION + LOCAL PATH SANITIZATION CHECKPOINT HANDOFF 🌊✨.md`

Evidence archives:

- `evidence/PORTABILITY-AUDIT-20260621/audit_notes.md`

## License

This project is licensed under the Apache License 2.0. See the `LICENSE` file for
details.
