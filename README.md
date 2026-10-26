<picture>
  <source media="(prefers-color-scheme: dark)" srcset="assets/header-dark.svg">
  <source media="(prefers-color-scheme: light)" srcset="assets/header-light.svg">
  <img alt="Alisher Nursain — Technical Lead and Software Developer. Architecture, APIs and business workflows. Astana, Kazakhstan." src="assets/header-light.svg" width="100%">
</picture>

<p align="center">
  <a href="#selected-work">Selected work</a> &nbsp; / &nbsp;
  <a href="case-studies/business-workflows.md">Workflow engineering</a> &nbsp; / &nbsp;
  <a href="https://www.linkedin.com/in/alisher-nursain-80873a326/">LinkedIn</a> &nbsp; / &nbsp;
  <a href="mailto:alisher.nursain@gmail.com">Contact</a>
</p>

## Technical Lead & Software Developer

I take technical responsibility for **architecture, task planning, delivery coordination and releases**. My project experience includes initiatives with 20–30 participants and, in one case, around 50. I also build projects independently.

I build **APIs and business workflows** where the rules behind an action matter: who may approve a change, which version was reviewed, what survives a restart, and how conflicting actions are handled. My work combines implementation, architectural explanations and reproducible checks.

Based in **Astana, Kazakhstan**. Three years of programming experience. Computing at **Coventry University Kazakhstan** (2025–2029 expected, in progress).

**Open to paid, fully remote projects.** Total availability: 20–30 hours/week. For a complete web MVP, API or internal tool, we can agree the user journeys, integrations, acceptance criteria and delivery stages before implementation.

## Selected work

| Project | Engineering problem | Implementation and evidence |
| :--- | :--- | :--- |
| **[BekitChange](https://github.com/wpalish/bekit-change)** | Two approved requests must not overwrite a newer record. | Two assigned reviews, exact base-version check, author-only application and an atomic SQLite write with audit. [Domain rules](https://github.com/wpalish/bekit-change/blob/24b631888ddf3a4541cd9971da7c55fd0d8eee01/module.js#L10) · [24 local workflow tests](https://github.com/wpalish/bekit-change/blob/24b631888ddf3a4541cd9971da7c55fd0d8eee01/tests/workflow.test.js). |
| **[KadamRun](https://github.com/wpalish/kadam-run)** | A retry should preserve an already successful intermediate result. | Recipe snapshots, saved events and explicit owner-driven retries. [State transitions](https://github.com/wpalish/kadam-run/blob/0e6af4d1dbc296f6ddb9a4f6ed1a1adca9476a44/module.js#L13) · [24 local workflow tests](https://github.com/wpalish/kadam-run/blob/0e6af4d1dbc296f6ddb9a4f6ed1a1adca9476a44/tests/workflow.test.js). |
| **[KoshiMap](https://github.com/wpalish/koshi-map)** | An import preview can become stale before the write. | Exact duplicate/conflict rules, server-side plan recalculation and whole-batch atomic application. [Import planning](https://github.com/wpalish/koshi-map/blob/fd22ccc94556ee526b6f8eebde518c09b972e377/module.js#L66) · [24 local workflow tests](https://github.com/wpalish/koshi-map/blob/fd22ccc94556ee526b6f8eebde518c09b972e377/tests/workflow.test.js). |
| **[ASHYQ Apply](https://github.com/wpalish/ashyq-apply)** | Admissions workflows need explicit evidence states and background-job ownership. | Collaborative Python/React work with requirement states, job leases, retries and cancellation. [Architecture and scope](case-studies/ashyq-apply.md). |

On **26 October 2026**, 96 local workflow tests passed across BekitChange, KadamRun, KoshiMap and [QaitaCycle](https://github.com/wpalish/qaita-cycle), 24 per project, on Node 24.15.0. These runs used synthetic data, SQLite and local HTTP. They establish the checked local behavior; external integrations and production operation need separate validation. The operational projects reuse a shared cabinet/authentication core.

### More engineering notes

- [Context Platform](case-studies/context-platform.md): calculation modules, invalid inputs and horizon boundaries.
- [Alēm Expert Router](case-studies/alem-expert-router.md): skill/capacity constraints and explainable assignment.
- [Petrel RAG](case-studies/petrel-rag.md): retrieval pipeline exploration and validation limits.
- [Yummy](https://github.com/wpalish/yummy) and [BudgetGate](https://github.com/wpalish/budgetgate): order/stock transitions and expense-approval rules.

## Engineering approach

**Define the result → model the rules → compare options → implement → verify → document the handover.**

I make the important boundaries visible: rejected actions, stale data, ownership, restart behavior and the scope of tests. [Workflow engineering notes](case-studies/business-workflows.md) explain three current examples.

**Toolkit:** Python/FastAPI · React/TypeScript · Node.js · SQLite · SQLAlchemy · Git · pytest. Technologies vary by project; follow the source and case notes for the reviewed scope.

I use AI tools in development and review. Tool permissions, private-data handling and acceptance criteria are agreed for each client brief. Project leadership is described at portfolio level; participant counts do not describe the contributors to every repository or a verified number of direct reports.

## Writing and contact

I publish short engineering explanations about architecture, reliable state transitions and business workflows.

[LinkedIn](https://www.linkedin.com/in/alisher-nursain-80873a326/) · [X / @wpalish](https://x.com/wpalish) · [Astana Hub](https://astanahub.com/account/v2/user/832790/profile/about/) · [Engineering notes](case-studies/README.md) · [Email](mailto:alisher.nursain@gmail.com)

[Concept Work / Synthetic Data portfolio](https://wpalish.github.io/ai-studio/) is labelled separately from repository work. Public projects include collaborative and AI-assisted development; the case notes distinguish local checks from client delivery and production outcomes.
