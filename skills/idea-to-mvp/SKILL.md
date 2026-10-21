---
name: idea-to-mvp
description: "Start a new software project or SaaS idea: research references and competitors, interview the founder with recommendations, write project.md, then use official GitHub Spec Kit and an authorized goal to build, test, and deploy the MVP. Use for requests such as 'let's start a new project', 'shape this idea', or 'interview me before building', and to resume this workflow. Do not restart discovery for an ordinary feature or bug fix in an existing product."
---

# Idea to MVP

Guide a founder from a rough idea to a complete agreed product. Own research and recommendations; let the founder choose the business and product. Preserve their chosen scope, prioritize a useful end-to-end customer journey, and make the experience unusually simple.

## Start or resume

1. Read applicable project instructions and existing `project.md`, `research/`, `docs/workflow-state.md`, and Spec Kit artifacts if present. Resume the current phase; do not overwrite an existing product definition or repeat settled questions.
2. If `references/local-profile.md` exists beside this skill, read it. It supplies this user's preferences only; it does not establish account access, budgets, ownership, credentials, or authorization. With no profile, use the founder's stated stack or research suitable options.
3. Start in the user's chosen project folder. If none is clear, establish a suitable location before creating files. Use existing paths and naming conventions when available.
4. If the request is only “let's start a new project,” ask for a rough brain dump, any working name, audience, and references. Recommend starting with the problem and desired customer result; accept messy notes. Do not demand a completed brief or a large questionnaire before helping.
5. Explain the immediate phase briefly. Create/update `docs/workflow-state.md` from [the state template](assets/workflow-state.template.md) as meaningful decisions accumulate. Record the next unresolved questions and the exact scope of any approval.

This skill's invocation authorizes discovery and planning. Application implementation begins when the founder explicitly asks to build, such as “approved, build” or “run Spec Kit, set a goal, and implement.” If that authorization already exists, preserve it. “Go with recommended” accepts the current proposed decisions, subject to exceptions; by itself it does not authorize a new build phase.

## 1. Investigate before the main interview

Inspect the supplied references and relevant alternatives. Research the actual problem, customer, differentiation, complete workflow, pricing/economics, implementation feasibility, integrations, and consequential edge cases. Prefer direct product pages, documentation and available source code. Check current prices, API capabilities, terms or policies when they materially affect the idea.

Save findings under `research/` as concise, cited Markdown with URLs, dates, findings, implications, and evidence limits. Maintain an index and a decision/interview record. Distinguish observed behavior, a vendor's claim, inference, and your recommendation. Do not label self-reported revenue as audited profit or a feature comparison as proven demand.

Return a coherent product hypothesis and the important gaps before interviewing. Make a substantial initial pass, then research specific questions as they arise. Stop broad research once the agreed scope can be responsibly defined; do not add arbitrary source quotas, paid pilots, validation programs, or prototypes as launch prerequisites unless the founder adopts them. Explain genuine feasibility constraints and seek a decision instead of silently substituting another business.

## 2. Interview until material questions are resolved

Read [the interview guide](references/interview.md). Cover the foundation, customer journeys, product rules, UX and scope, then commercial model and operations as relevant. Choose the next questions from unresolved decisions rather than reciting a fixed questionnaire.

**Every question must include a concrete recommendation and a short reason.** Usually group 3–5 related questions for comfortable pacing, but this is never a quota, maximum, total interview limit, or reason to stop. Ask fewer or more when useful. Keep asking follow-up questions whenever a material gap, contradiction, dependency, or new answer requires it—even after a draft or an earlier approval. Do not close the interview because a preset number of rounds has elapsed.

Treat “recommendations are good,” “all recommended,” or similar as acceptance of the recommendations just presented, honoring every exception. Record accepted choices and their rationale. It does not invent factual values that the founder has not supplied: legal identity, account ownership, budget, access or personal goals. Mark those unknown, retrieve them from authorized sources where appropriate, or ask specifically.

Challenge weak value, unnecessary friction, unsupported claims and conflicting rules. Recommend improvements without overriding the founder. When they choose a broader V1, build that scope; propose tradeoffs and never quietly reduce it to your preferred pilot. Recommend a small complete journey where it fits the founder's goal, with clear optional future work.

## 3. Consolidate the product and preview

Write `project.md` using [the project template](assets/project.template.md), adapting the headings to the product. It must contain the agreed customer value, real journeys, free/paid boundaries, exact business rules, UX, scope, architecture direction, meaningful edge cases, acceptance criteria, and unresolved dependencies. Separate accepted decisions, proposals, assumptions and unknown facts. Include decision rationale and links to supporting research.

Include the public marketing experience in launch scope unless the founder excludes it. Where applicable, cover responsive/mobile UX, accessibility, navigation, pricing, transactional communications, support/admin needs, privacy and indexability. Translate SEO/AEO/GEO into concrete public content, metadata, canonical URLs, useful structured data, sitemap and robots rules. Consider `llms.txt` when relevant; never imply a file guarantees visibility or rankings. Private surfaces require explicit indexability/access decisions.

As part of this planning review, produce a lightweight key-screen or clickable preview and a realistic example of the main product output. Focus on the core journey, important states, and whether the result is actually useful. Clearly label synthetic examples. This is planning work, not a reason to start production implementation early. The founder may skip the preview; if they explicitly approve building now, do not impose a new preview approval gate. Use their design references and direction; favor clear hierarchy and simple interactions over decorative generic layouts.

Review contradictions and calculations. Present the product definition, preview, remaining material questions and proposed delivery boundary together. If build authorization is absent, invite one “approved, build” decision once the package is reviewable. If they already authorized building, continue after resolving material blockers without demanding the same authorization again. Approval does not freeze discovery of consequential gaps; ask if a new answer is needed.

## 4. Preflight, Spec Kit and explicit goal

Read [the Spec Kit handoff](references/spec-kit.md) and [delivery guidance](references/delivery.md). Verify actual tools and authorized access before asking the founder to perform setup. Resolve owner decisions that cannot be inferred: cloud/billing target and spending bounds, repository target/visibility, permanent locations, domain ownership/DNS, legal/support/admin identity, provider dependencies and deployment scope. Do not assume another user's profile, organization, logged-in browser, or a historical project grants access.

After build authorization, run the genuine official GitHub Spec Kit workflow supported by the installed version and host: initialize safely; establish the constitution; specify, clarify, plan, check requirements, generate tasks, and analyze consistency. Inspect each stage's outputs and fix meaningful gaps before implementation. Preserve the founder's research and `project.md`; Spec Kit translates the agreed definition into implementation artifacts.

When the founder explicitly authorizes setting a goal (including the workflow's “approved, build” handoff), create one native persistent goal if the host offers it. Do not replace an unrelated unfinished goal. Include the full agreed product, marketing site, infrastructure, tests, deployment, documentation, spending constraints and chosen activation boundary. A goal may begin after initialization and encompass the remaining Spec Kit work. Without native goals, write the same objective and acceptance criteria into workflow state and execute with the available host; do not claim a native goal exists.

One authorization to proceed covers the remaining approved sequence; do not ask to rerun every stage. Further questions are for actual unresolved decisions, new scope/impact, missing facts or host-required approvals. The skill cannot authorize destructive changes, new spending targets or external communications outside the user's instruction.

## 5. Build and deliver the agreed whole

Implement dependency-ordered tasks and keep specs, decisions and evidence current. Use an appropriate isolated checkout/worktree when needed, without discarding local work. Build the actual application journeys and product outputs, public marketing, required operations and integrations. Resolve routine implementation details autonomously within the approved constraints.

Test important state changes, permissions, failures, money/entitlements and provider boundaries. Check real browser journeys and relevant mobile layouts, not just isolated units. Review for meaningful regressions and unresolved severe defects. Use Spec Kit convergence or its supported equivalent to reconcile code against requirements, and repair actual gaps. Do not substitute test counts, empty checkboxes, skeletons, or simulated provider results for complete customer value.

For credential-ready delivery, finish every credential-independent task and provide secure activation/configuration steps for the specifically deferred services. Keep live-provider verification visibly pending. For fully activated delivery, the required real checks remain acceptance work. Never silently convert a fully activated target to credential-ready to mark a goal complete. See the delivery reference for the exact distinction.

Add the applicable rules from [the project guidance template](assets/project-guidance.template.md) to the project's agent instructions without overwriting existing guidance: research consequential new work; explain major cross-module impact before approval; maintain specs, decisions and module contracts from code; preserve verification evidence. These requirements continue with future development.

Where authorized, finish the repository workflow and deploy all affected surfaces, verify the running version, and remove disposable test fixtures. Report the usable result, verification, remaining gaps and exact next steps. Mark a goal complete only against its agreed acceptance boundary. Do not claim proven business demand, measured ROI, flawless software or live integrations without evidence.

## Durable project artifacts

Use the project's existing organization; these are defaults, not additional bureaucracy:

- `research/`: source findings, options and interview/decision record.
- `project.md`: accepted product definition, scope and launch boundary.
- `docs/workflow-state.md`: phase, decisions, pending questions, authorization, goal and next action.
- Spec Kit's own generated paths: constitution, feature specifications, plan, contracts and tasks.
- `docs/`: architecture/module interactions, decisions, product walkthrough, verification and provider activation as needed.

Keep private identity, account data and raw conversations out of shared skill packages. The optional local profile is installed separately. This skill works with host capabilities; it does not require a particular connector, native goal tool, browser, multi-agent runtime or external account.

For explanatory infographics about this skill, use [the infographic brand style](references/brand-style.md). Software products being built retain the founder's own approved design direction.
