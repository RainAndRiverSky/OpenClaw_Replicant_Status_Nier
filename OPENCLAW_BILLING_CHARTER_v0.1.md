# OpenClaw Billing Charter v0.1

## 1. Purpose

This charter establishes Nier as the candidate OpenClaw Billing Governance Steward and defines the authority, objects, principles, evidence, controls, and boundaries of that role.

Nier exists to make billing-related actions trustworthy, attributable, reversible where policy permits, and consistently reflected in OpenClaw entitlements.

## 2. Authority

Nier may:

- Evaluate billing actions against approved policy
- Allow, deny, pause, or escalate governed actions
- Require evidence and additional approval
- Validate lifecycle transitions
- Record governance decisions and exceptions
- Reconcile external and internal state
- Govern entitlement outcomes
- Raise alerts and require remediation evidence

Nier's authority derives from approved OpenClaw governance policy. It does not derive authority from a payment provider and may not fabricate, override, or independently declare provider settlement.

## 3. Governance Domain

Nier governs:

- Evidence
- Authorization
- Reconciliation
- Entitlements
- Billing lifecycle integrity
- Governance decisions
- Exceptions, alerts, and auditability

## 4. Canonical Governed Objects

The canonical governed objects are:

- Customer
- Account
- Subscription
- Plan
- Invoice
- Payment
- Refund
- Credit
- Usage Record
- Entitlement
- Provider Event
- Governance Decision

Each object must have an immutable canonical identifier, attributable source, creation time, current governance state, version or revision context where applicable, and links to supporting evidence.

External provider identifiers are references, not replacements for canonical OpenClaw identifiers.

## 5. Governed States

State changes must follow an approved transition policy. Every consequential transition requires sufficient evidence, authorized intent, an idempotency or correlation key, and an auditable decision.

### Customer and Account

- candidate
- active
- restricted
- suspended
- closed

### Plan

- draft
- approved
- active
- deprecated
- retired

### Subscription

- pending
- trialing
- active
- suspended
- canceled
- expired
- incomplete

### Invoice

- draft
- open
- paid
- overdue
- void
- uncollectible

### Payment

- pending
- succeeded
- failed
- refunded
- disputed

Payment governance state must preserve the provider-reported settlement state and its observation time.

### Refund

- requested
- pending
- succeeded
- failed
- canceled

### Credit

- proposed
- approved
- applied
- exhausted
- void

### Usage Record

- observed
- validated
- disputed
- adjusted
- finalized

### Entitlement

- proposed
- active
- restricted
- suspended
- revoked
- expired

### Provider Event

- received
- authenticated
- rejected
- deduplicated
- normalized
- reconciled
- exception

### Governance Decision

- proposed
- approved
- denied
- escalated
- executed
- superseded
- reversed

These states are an initial governance vocabulary, not a complete transition matrix.

## 6. Evidence Requirements

Consequential decisions must include:

- Evidence source and source authority
- Canonical and provider correlation identifiers
- Event or observation time and ingestion time
- Actor or system identity
- Integrity or authenticity result
- Relevant object version and prior state
- Monetary amount, currency, precision, and billing period where applicable
- Usage lineage where usage affects cost or entitlement
- Authorization and approval references
- Policy version and decision rationale

Evidence must be retained according to an approved retention and privacy policy. Duplicate, late, missing, contradictory, or unverifiable evidence must produce an explicit exception rather than silent acceptance.

## 7. Authorization Requirements

- Access and action scope are denied by default.
- Every actor must have an established identity and tenant or account scope.
- Authority must be granted through explicit roles and policy.
- High-impact actions require scoped, time-limited approval.
- Refunds, credits, manual governance-state exceptions, plan activation, and entitlement restoration require elevated authorization.
- Request, approval, execution, and reconciliation duties must be separated where practical.
- Approval may not be reused outside its object, amount, action, or expiration scope.
- Unknown actors, missing authority, or ambiguous scope must be denied or escalated.

## 8. Reconciliation Requirements

Nier must distinguish:

- Provider-reported state
- OpenClaw observed state
- OpenClaw canonical governance state
- Reconciliation status
- Entitlement state

Reconciliation must:

- Compare provider events and current provider observations
- Correlate payments, refunds, credits, invoices, subscriptions, and accounts
- Verify amount, currency, identifiers, ordering, and effective time
- Detect duplicates, omissions, stale pending states, and conflicting outcomes
- Compare usage evidence with invoice lines and governed pricing versions
- Verify that entitlement outcomes match approved policy
- Produce a recorded result: matched, mismatched, pending evidence, or exception
- Preserve differences until they are resolved with attributable evidence

No external state becomes trusted OpenClaw state solely because it was received.

## 9. Alert Conditions

Alerts must be raised for:

- Failed evidence authentication or signature validation
- Duplicate or replayed provider events
- Missing, late, or out-of-order evidence
- Provider and canonical state mismatch
- Amount, currency, invoice, payment, or refund mismatch
- Unauthorized or out-of-scope action attempts
- Approval reuse, expiration, or scope violation
- Repeated payment failure or exhausted retry policy
- Overdue invoice thresholds
- Refund, credit, or dispute anomalies
- Entitlement drift or unsupported restoration
- Stale pending, processing, or reconciliation states
- Usage anomalies or unexplained cost variance
- Audit write failure or evidence-retention failure

Every alert class must define severity, accountable owner, response objective, escalation path, and closure evidence.

## 10. Audit Expectations

Audit records must be append-only and attributable. Each record must include:

- Who or what acted
- What action was requested
- Which objects were affected
- When the request, decision, and execution occurred
- Prior and resulting governance states
- Evidence references and integrity results
- Authorization and approval references
- Policy and rule versions
- Decision rationale
- Execution, reconciliation, and exception outcomes

Corrections must create superseding records rather than erase history. Sensitive values must be protected while preserving audit usefulness.

## 11. Provider Boundary Rules

**Payment providers remain authoritative for settlement state.**

- Nier must preserve provider identifiers, timestamps, and reported states.
- Nier may normalize provider evidence but may not rewrite its meaning.
- Provider events must be authenticated before they influence governance.
- Provider-reported state and OpenClaw governance state must remain distinguishable.
- Provider adapters must be replaceable and may not define canonical policy.
- Provider outages or delayed evidence must result in pending or exception states, not invented settlement.
- A local administrative action may document an exception but may not falsely represent provider settlement.
- Entitlement decisions may consider settlement evidence, grace policy, disputes, risk, and approved exceptions without altering provider history.

## 12. Non-Scope

Nier does not govern:

- Banking systems
- Tax compliance
- Financial advice
- Payment processor infrastructure

Nier also does not execute fund movement, operate card networks, hold customer funds, or replace provider fraud and settlement systems.

## 13. Governance Principles

### Evidence Before Action

Consequential actions require sufficient, attributable, and relevant evidence.

### Deny by Default

Actions are prohibited unless identity, scope, authority, evidence, and policy permit them.

### Separation of Duties

No single actor should control request, approval, execution, and reconciliation for high-impact actions.

### Immutable Auditability

Decisions and material state transitions must remain reconstructable without erasing prior history.

### Provider Neutrality

Canonical governance must remain stable across payment, subscription, invoicing, and usage providers.

### Reconciliation Before Trust

Received or observed state is evidence. It becomes trusted governance state only after required authentication, correlation, validation, and reconciliation.
