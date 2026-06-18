# Nier Governance Status v0.1

## Status

**Governance Foundation Phase**

Nier is a candidate OpenClaw Billing Governance Steward. Its identity and initial scope are established, but its policies, state models, evidence contracts, and operational admission controls still require ratification.

## Mission

Govern billing evidence, authorization, reconciliation, entitlements, and lifecycle integrity across the OpenClaw ecosystem without assuming responsibility for payment processing or provider settlement.

## Shared Foundations Relationship

Nier acknowledges Shared Foundations by reference and inheritance from the canonical
public repository:

`https://github.com/RainAndRiverSky/OpenClaw_Shared_Foundations`

This relationship is recorded locally through:

- `identity/NIER_STEWARD_IDENTITY_v0.1.md`
- `docs/governance/shared-foundations/NIER_SHARED_FOUNDATIONS_ADOPTION_RECORD_v0.1.md`
- `docs/governance/shared-foundations/NIER_SHARED_FOUNDATIONS_INHERITANCE_MAP_v0.1.md`
- `docs/governance/shared-foundations/NIER_SHARED_FOUNDATIONS_EXCEPTION_REGISTER_v0.1.md`

Shared Foundations are used by Reference + Inheritance only. Canonical Shared
Foundations documents are not copied into this repository.

Shared Foundations inheritance does not replace Nier-specific billing governance,
billing evidence requirements, billing authorization, reconciliation requirements,
entitlement governance, provider boundary rules, billing lifecycle integrity, billing
charter authority, or operational admission requirements.

## Governance Domain

Nier governs:

- Identity, role, scope, and approval requirements for billing actions
- Canonical billing objects and their lifecycle transitions
- Evidence provenance, correlation, sufficiency, and retention
- Reconciliation between provider, local, usage, invoice, and entitlement state
- Entitlement decisions and their supporting evidence
- Exceptions, alerts, escalations, overrides, and audit history
- Provider-neutral policy and integration boundaries

Payment providers remain authoritative for settlement state. Nier governs whether and how provider-reported state may affect OpenClaw records, decisions, and entitlements.

## Reconnaissance Findings Summary

The OpenClaw ecosystem and reviewed governance layers demonstrate several recurring patterns:

- Effective governance is enforced before execution rather than left to agent discretion.
- Deny-by-default scope, explicit identity, rate limits, and human approval are established action-governance patterns.
- Append-only records, version lineage, provenance, structured metadata, and visible evidence support trustworthy decisions.
- Mature billing systems use explicit state machines for subscriptions, invoices, payments, refunds, retries, and overdue handling.
- Provider state and local domain state must remain distinct and be reconciled.
- Idempotency and immutable correlation identifiers are essential for retries, duplicate events, and re-imports.
- Entitlements are a governed outcome of billing evidence, not a direct synonym for payment status.
- Operational practice requires defined alert thresholds, accountable responders, transparent timelines, and closure evidence.
- Existing token accounting can support attribution and forecasting but does not constitute a settlement ledger.
- Existing authentication and credential patterns are fragmented, creating an integration risk for future billing governance.

## Current Governance Layers

### 0. Shared Foundations Reference and Inheritance

**Artifacts:**

- `identity/NIER_STEWARD_IDENTITY_v0.1.md`
- `docs/governance/shared-foundations/NIER_SHARED_FOUNDATIONS_ADOPTION_RECORD_v0.1.md`
- `docs/governance/shared-foundations/NIER_SHARED_FOUNDATIONS_INHERITANCE_MAP_v0.1.md`
- `docs/governance/shared-foundations/NIER_SHARED_FOUNDATIONS_EXCEPTION_REGISTER_v0.1.md`

Shared Foundations provide compatible baseline OpenClaw stewardship context by external
reference. Nier-specific governance remains authoritative for billing evidence,
authorization, reconciliation, entitlements, provider boundaries, billing lifecycle
integrity, and operational admission boundaries.

### 1. Billing Charter

**Artifact:** `OPENCLAW_BILLING_CHARTER_v0.1.md`

Enduring governance layer for Nier's billing authority, governed objects, state
vocabulary, evidence requirements, authorization requirements, reconciliation
requirements, alerts, audit expectations, and provider boundary rules.

### 2. Governance Status

**Artifact:** `NIER_GOVERNANCE_STATUS_v0.1.md`

Current governance snapshot for Nier's foundation phase, mission, domain, risks,
unknowns, milestones, and admission readiness.

## Canonical Governed Objects

### Customer

The party receiving a product, service, invoice, or entitlement.

### Account

The governance and billing boundary that groups customers, identities, subscriptions, balances, and provider references.

### Subscription

A time-bounded agreement connecting an account to a plan and its governed lifecycle.

### Plan

A versioned commercial definition of price, billing cadence, limits, trial terms, and entitlement policy.

### Invoice

A demand or record of amounts due, including line evidence, currency, period, adjustments, and status.

### Payment

A provider-linked attempt or result associated with settling an invoice or balance.

### Refund

A governed reversal request or provider-reported reversal of a prior payment.

### Credit

A governed value adjustment applicable to an account, balance, or invoice.

### Usage Record

An attributable, time-bound measurement used for cost accounting, limits, or billing calculation.

### Entitlement

A governed right to access a feature, resource, capacity, or service for a defined scope and period.

### Provider Event

Authenticated external evidence describing a provider-side occurrence or state observation.

### Governance Decision

An attributable policy outcome containing the action, authority, evidence, rationale, prior state, resulting state, and policy version.

## Current Risks

- No ratified canonical state model or transition matrix
- No evidence schema, provenance classification, or retention policy
- No approved identity, role, or separation-of-duties model
- No reconciliation frequency, tolerance, or exception taxonomy
- No entitlement precedence or restoration policy
- No formal alert severity, ownership, or response objectives
- No provider adapter trust contract
- Fragmented authentication and credential-management patterns in the surrounding ecosystem
- Potential confusion between estimated token cost and billable settlement evidence
- No operational mechanism yet for immutable audit retention

## Current Unknowns

- Which OpenClaw service will own canonical account and customer identity
- Which runtime identities may request or approve billing actions
- Required approval thresholds for refunds, credits, overrides, and entitlement restoration
- Required evidence retention periods and privacy classifications
- Supported currencies, precision rules, and rounding policy
- Usage metering authority and dispute-resolution procedure
- Entitlement behavior during provider outages or reconciliation delays
- Expected reconciliation cadence and acceptable mismatch tolerances
- Initial provider and subscription-system integration order
- Operational ownership for alerts, incidents, and manual review queues

## Future Milestones

1. Charter review and formal admission approval
2. Canonical object schema and identifier policy
3. State-transition and lifecycle policy
4. Evidence, provenance, and retention standard
5. Authorization and separation-of-duties matrix
6. Reconciliation and exception-management standard
7. Entitlement governance policy
8. Alerting, incident, and audit operating model
9. Provider-neutral adapter contract
10. OpenClaw Runtime and MCP boundary design
11. Controlled implementation readiness review

## Admission Readiness Assessment

**Assessment: Foundation established; not ready for operational admission.**

Nier has a clear mission, governance domain, provider boundary, canonical object set, and initial risk register. It is ready for charter review and policy design.

Nier is not ready to authorize or execute billing actions. Operational admission requires ratified state models, evidence requirements, role definitions, reconciliation rules, entitlement policy, alert ownership, audit controls, and tested integration boundaries.
