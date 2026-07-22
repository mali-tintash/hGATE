# Architecture Review Checklist

## Status Integrity

- [ ] Every material statement is Observed, Assumed, Proposed, Decided, Open, Excluded, or Superseded.
- [ ] Every Decided item records the decision owner and rationale.
- [ ] Agent recommendations are not presented as stakeholder agreement.
- [ ] Open details remain visible in the executive summary and diagrams when material.

## Evidence and Flows

- [ ] At least one representative journey is traced end to end.
- [ ] Authoritative state owners are identified.
- [ ] Async events, queues, retries, webhooks, and provider callbacks are included.
- [ ] Current behavior and target behavior are separated.
- [ ] Critical assumptions include a disconfirming check.

## Architecture Coherence

- [ ] Business promise, supported journeys, and topology agree.
- [ ] Diagrams and prose show the same call and event directions.
- [ ] Identity propagation and authorization are explicit.
- [ ] Data ownership and mutation boundaries are explicit.
- [ ] Provisioning, reset, migration, and deletion cover non-database state.
- [ ] External-provider simulation does not bypass required internal domain behavior.

## Claim Discipline

- [ ] “Isolated” names the enforceable boundaries.
- [ ] “Parity” names included and excluded dimensions.
- [ ] “Real time” has a measurable latency expectation.
- [ ] “Atomic” states the actual transaction or visibility boundary.
- [ ] “Exactly once” is replaced by concrete idempotency and deduplication semantics unless formally guaranteed.
- [ ] “Same code” does not imply same configuration or behavior without validation.

## Security and Operations

- [ ] Credentials, secrets, network paths, egress, and trust registration are covered.
- [ ] Customer-controlled endpoints and external systems are treated as separate trust domains.
- [ ] Privacy, retention, audit, and redaction are addressed.
- [ ] Noisy-neighbor and capacity controls have owners.
- [ ] Support, incident response, and observability ownership are clear.

## Business and Governance

- [ ] Alternatives include technical and organizational cost.
- [ ] Rejected alternatives include reasons.
- [ ] Non-goals and release exclusions are explicit.
- [ ] Open decisions have owners or a resolution path.
- [ ] The architecture document does not silently become an implementation backlog.

## Adversarial Review Prompts

- What production or privileged resource can this design still accidentally reach?
- What happens if configuration is incomplete or wrong?
- Which identifier is treated as globally unique but is not?
- Which state survives reset, retry, redeploy, or failover unexpectedly?
- Which team can mint more authority than it should possess?
- Which customer-visible promise depends on an external provider?
- What breaks when two services deploy different contract versions?
- Which claim sounds stronger than the mechanism can enforce?
