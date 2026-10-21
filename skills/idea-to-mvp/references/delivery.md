# End-to-end delivery and evidence

Read at operational preflight and during implementation/release. Adapt to the approved stack and the host's tools; these instructions do not require a particular cloud provider.

## Operational preflight

Inspect available connectors/CLIs, repository state, authenticated identities and actual access. Use existing authorized sources before asking for facts. Avoid exposing token values, environment dumps or verbose credential-bearing diagnostics. Distinguish a sandbox/config-write/network error from expired credentials before telling the founder to log in again.

Record the correct repository target/visibility, cloud project, billing account, spending bounds, region/data residency, domain/DNS, legal/support/admin identity and provider readiness. Identify existing resources before creating duplicates. A profile recommends technology but cannot approve a billable target, grant ownership or authorize destructive changes. Explain permanence or operational impact only when it materially affects an owner choice.

Clarify deployment/commit/push/merge authority in the handoff using the founder's existing instructions. “Approved, build” under this workflow may authorize the presented end-to-end delivery scope; do not expand it to unrelated repositories, services, external messages or production resets. Use a safe isolated checkout/worktree when appropriate and preserve other work. Existing approvals persist; do not repeatedly ask for the same permission.

## Define the acceptance boundary

| Target | Required to deliver | Explicitly pending |
| --- | --- | --- |
| Credential-ready | All agreed independent implementation, real configured services, public/app UX, deployment within granted scope, suitable tests and browser QA, operational docs, secure provider adapters and complete activation procedure. | Only the named credential/account-dependent setup and real checks accepted as deferred. |
| Fully activated | The above plus actual configured provider/account integrations and the required real end-to-end checks. | Anything deferred requires an explicit change of scope; otherwise the goal remains unfinished. |

Adopt credential-ready at planning review when it fits the founder's request. Do not silently choose it after discovering an integration is difficult. Missing credentials do not excuse unrelated unfinished tasks. Explicitly distinguish implementation readiness, deployed behavior, activated integrations and business validation.

Prepare activation beyond an empty key field: secret names and secure entry method, runtime access/configuration, products/prices and webhooks where needed, signing-secret handling, OAuth/account connection, sender/domain readiness, resumable setup and verification steps. Use provider-specific official documentation and current configuration. Never request secrets in chat or commit them. Label adapter/emulator/synthetic checks honestly; they do not establish real delivery, payment or publication.

## Build for the real product journey

Implement vertical journeys that finish the user's task, with relevant empty/error/loading, retry/recovery and access states. A generator must create the useful output agreed in `project.md`; a dashboard containing disconnected generators is insufficient when an integrated recurring workflow was approved.

Maintain requirement/task coverage as work proceeds. Update specs and decisions when accepted changes affect behavior. Document meaningful module dependencies, source-of-truth boundaries, provider contracts and state transitions. Do not invent operating status from code alone.

For the public site, implement the agreed positioning, navigation, product/pricing/support content, mobile presentation and discoverability. Check actual metadata, canonical URLs, structured-data validity, sitemap/robots behavior, public/private indexing and redirects. Never generate fake testimonials or unsupported revenue/quality claims to fill a design.

## Verify against the accepted result

Use checks proportional to the change. Prioritize meaningful state transitions and boundaries: access isolation, entitlements/money, retries/idempotency, concurrency where relevant, privacy and deletion/export, realistic provider responses, and failure recovery. Avoid tests that only mirror implementation or exist to inflate counts.

Walk through the complete core product in a real browser with realistic data where tools permit. Compare the actual useful output to the approved example and intended customer outcome. Inspect relevant desktop/mobile layouts, keyboard access, contrast, content fit and the states that users will encounter. Record what was observed and what the tools could not test. Do not report a rendered UI or a working external service based on source inspection alone.

Run the installed Spec Kit convergence workflow and reconcile every in-scope requirement with code and verification evidence. Correct actual omissions and severe defects, then run affected checks. Do not broaden/repeat testing without a remaining concern. Review for regressions before release; report known material issues and do not claim an impossible guarantee of bug-free software.

For deployment, use the authorized repository/release process, verify all affected web/worker/job/data-config surfaces, and check the running version and core deployed journey. Clean up disposable fixtures and private test media/accounts where safe and authorized; preserve real customer and financial records. If verification itself needs an external action not granted by the founder, obtain the narrow necessary authorization while completing independent work.

## Maintainable handoff

Create only useful documentation, fitted to the project's organization:

- An architecture/module map with interactions and important decisions.
- A product walkthrough explaining what users do, outputs, stack/providers and material limitations. For AI products, include actual production prompts or a precise source/version map, with secrets excluded.
- A verification report mapping requirements to observed checks and the exact release, with pending items.
- An activation/runbook covering named provider dependencies, recovery and verification.

Merge the [project guidance template](../assets/project-guidance.template.md) into the applicable project instructions; do not overwrite unrelated rules. Major future edits need an impact explanation and approval before implementing newly proposed changes, unless the exact change and impact were already authorized. Routine implementation decisions within approved scope do not require repeated approval.

Report the usable URL/artifacts, completed scope, material verification, pending integrations and concise instructions for checks the founder must perform. Keep the objective intact when blocked, follow the host's native goal-state rules, and mark it complete only against the accepted boundary.
