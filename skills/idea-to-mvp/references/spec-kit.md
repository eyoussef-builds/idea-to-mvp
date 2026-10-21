# Official GitHub Spec Kit handoff

Read after the product definition is ready and the founder authorizes the build/Spec Kit phase. The workflow must use the actual installed toolkit, not files merely named to resemble it.

## Sources and version awareness

Official sources checked 2026-10-21:

- [Repository](https://github.com/github/spec-kit)
- [SDD quickstart](https://github.github.io/spec-kit/quickstart.html)
- [Integrations](https://github.github.io/spec-kit/integrations/index.html)
- [Codex integration](https://github.github.io/spec-kit/integrations/codex.html)

Inspect `specify --version`, `specify --help` and relevant subcommand help. Read current official instructions and the project's installed/generated skills. Flags, invocation syntax and paths can differ across versions and hosts. Do not silently upgrade a working project integration or overwrite its customizations. If a required capability is unavailable, establish whether a compatible installed workflow suffices; otherwise explain the gap and use an approved official installation/upgrade path.

Do not replace the founder's research/interview process with Spec Kit's separate idea-assessment extension unless requested. Do not install unrelated extensions or turn every task into GitHub issues by default.

## Safe initialization

Inspect the existing checkout, `.specify/`, agent integrations and local changes. Preserve `project.md`, research, agent instructions and any established constitution. Initialize in the correct folder only once, or use the supported adoption/integration commands for an existing project. Do not use `--force` by habit or treat historical initialization flags as universally safe.

Illustrative commands, to be verified against the installed CLI:

```sh
specify --version
specify init --help
specify init --here --integration codex
```

Use the integration key appropriate to the actual host. Codex's documented skill layout is `.agents/skills/speckit-<command>/SKILL.md`, invoked with `$speckit-...`. Other integrations use their own syntax. Native skill invocations belong in the agent, not the shell. If the host lacks a dispatch mechanism, read and execute the installed skill's instructions with its prescribed scripts and inputs; do not claim dispatch occurred. A genuine unavailable capability is a reported blocker, not a reason to fabricate a successful official workflow.

Verify which files were generated and review the diff for unintended changes. Record the toolkit version, integration and paths in workflow state. Keep project-specific rules in supported project instructions/overrides rather than editing toolkit-generated commands without a supported customization mechanism.

## Full project path

The documented production path at the source check date is:

| Stage | Input and outcome to inspect |
| --- | --- |
| Constitution | Accepted quality, usability, maintainability, scope and verification principles. Establish once; amend deliberately. |
| Specify | Product behavior and acceptance criteria from `project.md`; preserve what/why and the complete approved scope. |
| Clarify | Resolve material underspecification. Use existing accepted answers; ask the founder when a new product decision is needed. |
| Plan | Approved stack, architecture, interactions, data, provider boundaries and deployment approach. Record rationale and real dependencies. |
| Checklist | Requirements-quality review, with evidence for whether each criterion is satisfied. This does not prove implementation. |
| Tasks | Dependency-ordered work spanning product, public site, infrastructure, integrations, verification and documentation. |
| Analyze | Check contradictions, omissions and coverage across the generated artifacts; fix the source and recheck meaningful findings. |
| Implement | Execute accepted tasks and required checks without silently shrinking scope. |
| Converge | Reconcile working code with requirements; fix genuine gaps and repeat relevant checks until the agreed boundary is satisfied. |

Follow the actual installed command sequence where it differs; preserve these outcomes. Inspect results between stages. This review is the agent's work and does not require asking the founder to approve every generated artifact. Ask when a finding changes a material product decision, scope, spending or previously granted authority.

Keep checklist ownership and state truthful. Read each generated gate's instructions; review requirement quality before marking its criteria satisfied. Do not blanket-check items to bypass implementation gates. Fix unclear requirements or obtain an informed decision for a real exception. Do not report a task done solely because the code file exists.

Use one or multiple feature specifications according to the product's real boundaries. Maintain coverage of every accepted requirement and cross-module contract; avoid splitting the whole MVP into disconnected demonstrations. Do not assume a branch selects the active feature: inspect the installed version's feature-selection mechanism before issuing commands in a multi-feature project.

## Goal and scope continuity

After explicit goal/build authorization, use the native goal tool if available. A goal may cover initialization through deployment; it need not wait for every generated task. Do not create it during an interview-only request, add a token budget without an explicit request, or replace an unrelated unfinished goal. Without native support, persist the objective and acceptance criteria in `docs/workflow-state.md`.

Example objective to adapt to accepted facts:

> Build the approved product in project.md using official GitHub Spec Kit. Finish the complete agreed customer journeys and outputs, public marketing, authorized cloud/repository setup, integrations, maintainable documentation, relevant automated/browser/mobile verification, and authorized deployment. Preserve approved scope and spending constraints. Deliver against the chosen credential-ready or fully activated boundary. Complete all independent work, report actual blockers, and keep explicitly deferred activation checks visible. Continue through verification rather than stopping at a scaffold or passing unit suite.

Use the native host's goal-status rules. Mark completion only when the chosen objective is achieved; pending activation can coexist with a completed credential-ready implementation goal only when that boundary was explicitly adopted. Do not call the whole system fully verified when provider checks are pending.
