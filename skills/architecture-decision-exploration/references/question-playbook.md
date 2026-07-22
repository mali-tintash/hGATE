# Question Playbook

Ask questions in dependency order. Skip clusters already answered by evidence or explicit constraints.

## 1. Business Promise

- Who uses this capability, and what must they be able to prove or accomplish?
- What business risk exists if the capability is incomplete or inaccurate?
- What is explicitly not being promised?
- Is this exploration, certification, production readiness, compliance, or operational enablement?

## 2. Representative Journeys

- What is the primary happy path?
- Which failure or recovery paths materially affect the architecture?
- What irreversible or externally visible side effects occur?
- Which system is authoritative at each state transition?

## 3. Identity and Ownership

- Who is the caller, and on whose behalf does it act?
- Which system issues credentials and owns revocation?
- What tenant, organization, member, environment, and client identities exist?
- Which team owns the customer contract, domain decision, and operational support?

## 4. Data and Isolation

- What data is shared, copied, synthesized, retained, or prohibited?
- What is the effective resource namespace?
- Which stores, queues, caches, secrets, and providers form the isolation boundary?
- What prevents untrusted input from selecting a more privileged environment?

## 5. Fidelity and Compatibility

- Which real domain logic must execute?
- Which external boundaries may be simulated?
- What does parity include and explicitly exclude?
- How are fixtures or scenarios versioned and kept compatible across services?

## 6. Lifecycle and Failure

- How are resources provisioned, activated, reset, expired, migrated, and deleted?
- What happens to in-flight requests, jobs, events, caches, and callbacks?
- What state is preserved during reset or migration?
- What is externally visible during partial failure?

## 7. Operations and Business Cost

- Who supports this capability and with what service expectation?
- What observability is available to customers and operators?
- Who owns commercial quotas versus protective service ceilings?
- What are the infrastructure, provider, retention, and support costs?
- What abuse or noisy-neighbor behavior must be contained?

## 8. Decision Closure

- Which alternatives remain viable?
- What evidence would change the preferred option?
- Which items are architecture invariants versus detailed design?
- Who has authority to decide each open item?
- What review date or trigger should revisit the decision?

## Question Quality Test

A strong question does at least one of the following:

- Eliminates an architecture alternative
- Establishes an invariant
- Resolves ownership
- Exposes a hidden business or operational cost
- Distinguishes current behavior from desired behavior
- Identifies evidence needed for a material assumption

Avoid questions whose answer merely selects a low-level mechanism before the requirement is known.
