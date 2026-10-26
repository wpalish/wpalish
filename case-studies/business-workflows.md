# Workflow engineering: approvals, retries and imports

Alisher Nursain · reviewed 26 October 2026

These three small Node.js/SQLite projects explore business rules that are easy to hide behind an interface. Each reuses a shared local cabinet and authentication core. The useful comparison is the mutation boundary: what must remain true when someone applies a change, retries a step or confirms an import.

## BekitChange: approval belongs to a version

Two requests, A and B, can both be approved against record v1. Once A creates v2, applying B must stop. B's reviewers evaluated a different source state.

A saved request freezes its original RU/KK record, proposed texts and review policy. Two assigned reviewer accounts must differ from the author and each other. After their ordered approvals, the original author explicitly applies the change. The server compares the saved base to the current card again. Both language fields, the new version and the application record commit in one SQLite transaction with audit.

The shared workspace revision is conservative. Even an unrelated edit can make an old command stale, trading convenience for an explicit conflict. Distinct accounts do not independently establish distinct humans, and the request digest is not an electronic signature.

[Reviewed domain rules](https://github.com/wpalish/bekit-change/blob/24b631888ddf3a4541cd9971da7c55fd0d8eee01/module.js#L10) · [Workflow tests](https://github.com/wpalish/bekit-change/blob/24b631888ddf3a4541cd9971da7c55fd0d8eee01/tests/workflow.test.js)

## KadamRun: continue from a saved checkpoint

A published recipe freezes a sequence of literal text operations and its retry policy. The owner explicitly advances the run. Events preserve the intermediate value and expected sequence.

A synthetic example adds a prefix, then simulates a temporary failure in a later operation. Continuing must not add the prefix again. The implementation reconstructs state from the event sequence, checks the owner, expected event number and allowed retry time, then records the next transition. A successful checkpoint survives a SQLite file restart.

Time passing does not execute a step. This is a local, inspectable state model, not a background worker or proof of exactly-once external API effects. Real connectors would need their own implementation and evaluation.

[State transitions](https://github.com/wpalish/kadam-run/blob/0e6af4d1dbc296f6ddb9a4f6ed1a1adca9476a44/module.js#L13) · [Restart/continuation test](https://github.com/wpalish/kadam-run/blob/0e6af4d1dbc296f6ddb9a4f6ed1a1adca9476a44/tests/workflow.test.js#L24)

## KoshiMap: check an import at the write boundary

A preview can describe a correct import plan and still be stale when its author confirms. KoshiMap preserves the original JSON batch and a published mapping for a bounded set of flat string rows.

The plan distinguishes insert, skip-identical, duplicate source and conflict. Archived records continue to reserve their code. Confirmation checks the revision and recomputes the plan inside the SQLite transaction. Any conflict refuses every insertion; the copy record, entries and audit commit together. A zero-new-entry batch still has an explicit record.

Values retain their exact case, whitespace and Unicode. This makes comparisons explainable; fuzzy cleanup and general CSV/Excel migration are separate scope.

[Planning rules](https://github.com/wpalish/koshi-map/blob/fd22ccc94556ee526b6f8eebde518c09b972e377/module.js#L66) · [Confirmation/revalidation](https://github.com/wpalish/koshi-map/blob/fd22ccc94556ee526b6f8eebde518c09b972e377/module.js#L108) · [Workflow tests](https://github.com/wpalish/koshi-map/blob/fd22ccc94556ee526b6f8eebde518c09b972e377/tests/workflow.test.js)

## Verification and scope

On 26 October 2026, the complete workflow.test.js suites passed locally for these three projects: 24 tests each, 72 total, on Node 24.15.0 with synthetic data, SQLite and local HTTP. A separate QaitaCycle suite passed 24 tests, bringing that review to 96. The runs included domain refusals, stale commands and persistence/restart behavior; exact cases are in each repository.

These results do not establish real customer outcomes, production load/security readiness or external integration behavior. No performance or revenue improvement is claimed.

## Discuss a product

I work on paid, fully remote web MVPs, APIs and internal workflows. A useful brief defines the user journey, data boundaries, integrations and acceptance criteria. [Contact](mailto:alisher.nursain@gmail.com) · [Profile](../README.md)
