# Evidence Guide

Use this guide while exploring current behavior and validating architectural claims.

## Evidence Hierarchy

Prefer evidence in this order, while accounting for freshness:

1. Runtime behavior, tests, traces, metrics, and production-safe diagnostics
2. Executable contracts: schemas, API definitions, migrations, policies, state machines
3. Owning code paths that compute, mutate, authorize, route, or publish
4. Configuration and deployment definitions
5. Runbooks and maintained architecture documentation
6. Authoritative domain or operational owner statements
7. Call sites, comments, names, and inferred conventions

Names and diagrams are leads, not proof.

## Evidence Record

For each material claim, record:

| Field | Description |
|---|---|
| Claim | Precise statement being evaluated |
| Status | Observed or Assumed |
| Source | File/symbol, command, trace, document, or stakeholder |
| Confidence | High, medium, or low |
| Freshness | When the evidence was produced or last verified |
| Disconfirming check | Cheapest check that could prove the claim wrong |
| Decision impact | Which decision changes if the claim is false |

## Journey Trace

For each representative journey, capture:

| Hop | Caller | Callee | Auth/context | Contract | State owner | Side effect | Async/retry | Evidence |
|---|---|---|---|---|---|---|---|---|

Include callbacks and events that occur after the initiating HTTP response.

## Common Evidence Errors

- Treating a stub, mock, or test fixture as runtime behavior
- Inferring a dependency from a domain label such as `wallet`, `points`, or `identity`
- Reading only the platform edge and missing downstream state machines or queues
- Treating an environment enum as proof of environment isolation
- Treating a schema suffix as the entire tenant or security boundary
- Assuming a configuration option is enabled in deployed environments
- Describing a likely flow as the actual current flow
- Ignoring caches, object storage, queues, outboxes, analytics, and external providers

## Current vs Target

Maintain separate diagrams or columns:

- **Current:** evidence-backed behavior today
- **Target:** proposed or decided future behavior
- **Gap:** capability needed to move from current to target

Never silently repair the current-state diagram to make it match the proposal.
