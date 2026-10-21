## Product decisions, specifications and delivery

Merge these rules into the project's existing agent instructions at build handoff, adapting document paths. Preserve existing rules and scope.

- Read `project.md`, the current specs and relevant source before changing product behavior. Resume accepted decisions and current workflow state rather than restarting discovery.
- For consequential new features, investigate suitable practices, actual provider capabilities and relevant edge cases. Explain what fits this product and why; distinguish evidence, recommendation and assumption.
- Before implementing a newly proposed major change, explain current behavior, proposed behavior, affected modules/contracts/data, user and operational impact, migration/compatibility needs and meaningful verification. Obtain the founder's decision where it changes scope or behavior. If that exact change/impact is already authorized, proceed without asking again. Routine implementation choices within approved scope do not need another approval.
- Keep product/spec/plan/task documentation, decision rationale, architecture and module interactions aligned with the actual code in the same change. Distinguish code capability, deployed configuration and behavior verified in operation. Never backfill documentation using unsupported assumptions.
- Preserve the whole approved product and UX scope. Suggest improvements and tradeoffs; do not silently remove features or replace the intended business.
- Verify important changed journeys and boundaries, review regressions, and record evidence and material limitations. Passing unit tests alone does not prove a complete useful product or a live integration.
- Keep requirement-quality checklists distinct from implementation and verification state. Complete tasks only with evidence appropriate to their acceptance criteria.
- For AI behavior, keep production prompt/version references, real input/output contracts, claim/source rules and relevant quality checks current. Synthetic results remain labeled.
- Prepare secure, documented provider activation and keep intentionally deferred real payment/email/publishing checks explicit. Never equate configured secret containers or simulated adapters with activated integrations.
- Keep `docs/workflow-state.md` current at material transitions: phase, pending questions, accepted decisions, authorization, goal, evidence and next action. Do not reset a goal or its acceptance boundary because a turn ends.
- At release, reconcile requirements against code and observed checks, deploy all authorized affected surfaces, verify the running version, clean disposable test fixtures safely and report unresolved items with practical next steps.
