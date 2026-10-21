# Idea to MVP

[العربية](README.ar.md) · [Install for 15 agents](docs/agent-installation.md) · [Privacy](docs/privacy.md) · [MIT license](LICENSE)

**Tell your AI a rough software idea. Let it research, ask useful questions, write the plan, and guide an approved build.**

Imagine building a toy house. First you decide who it is for. Then you draw it. Then you choose the pieces. Only then do you build and check that the doors open. This skill teaches a coding assistant to work in that order, so you do not have to explain the same process every time.

## What is a skill?

A skill is a folder containing an instruction book called `SKILL.md`, plus useful templates and notes. Your AI reads the book when you ask for this kind of work. It is not a separate AI, subscription, or website. You still need a coding agent with an account and suitable tools.

**MVP** means the first useful version of a product: a small complete experience people can actually use. It does not mean a page of buttons that do nothing. Your approved scope decides what must be built.

## Start here: the easiest installation

If your agent can download files and install skills, paste this into its chat:

```text
Install the idea-to-mvp skill from https://github.com/eyoussef-builds/idea-to-mvp.
Read its installation guide and inspect the skill before installing.
Install the complete skills/idea-to-mvp folder in the supported personal skill
directory for this agent. Preserve any existing customized copy.
Tell me the installed location and how to invoke it. Do not start a project yet.
```

The agent may ask for permission to download or write to your skill directory. Read that request. If it cannot install files, follow the [step-by-step guide for your agent](docs/agent-installation.md), including a no-terminal download method and Windows instructions.

## Your first project, step by step

1. Open a folder where you want the new project to live. Start your coding agent there.
2. Ask it to use the skill. In Codex, paste:

   ```text
   Use $idea-to-mvp. Let's start a new project.
   My rough idea is an app that helps people plan meals from ingredients they have.
   Please research it, then interview me with recommendations before building.
   ```

3. Add any websites, screenshots, audience details or rough notes you already have. Messy notes are fine. The meal-planning example is fictional; replace it with your idea.
4. Answer the questions. Each question should come with a recommendation and a short reason. You can say “all recommended, except…” to accept the current suggestions while changing anything you dislike.
5. Review `project.md`. Think of it as the picture on the toy box: what you are making, who uses it, how it works, and what counts as finished. The assistant also prepares a small screen/output preview unless you skip it.
6. Correct anything missing. The interview usually uses small batches of questions, but there is no fixed total. A material unanswered question still needs an answer.
7. When you want implementation, give a clear handoff. For example:

   ```text
   The plan is approved. Use official GitHub Spec Kit, set a goal if supported,
   and build the MVP described in project.md. Implement and test the complete
   agreed scope. Ask me about missing ownership, deployment or budget decisions
   before using external services. Do not invent account access or credentials.
   ```

8. Review the delivered application, checks and activation instructions. A real payment or email integration is only verified when the required real checks have actually happened.

Other agents use their own invocation syntax; see the installation guide. A natural request such as “let's start a new project” may select the skill automatically, but explicitly naming it is the clearest way to check.

## What the assistant does behind the scenes

| Stage | Plain explanation | What you get |
| --- | --- | --- |
| Research | Looks at the problem, references, alternatives and important current facts. | Cited findings in `research/`. |
| Interview | Asks about the customer, journey, product rules, design, price and operations. | Accepted choices, reasons and unresolved questions. |
| Product definition | Turns those decisions into a clear description and a useful preview. | `project.md` and a core screen/output example. |
| Setup check | Checks the real tools, accounts, delivery target and spending limits. | Explicit setup decisions instead of guessed access. |
| Official Spec Kit | Uses GitHub's toolkit to turn the agreed product into requirements and tasks. | Constitution, specifications, plan, checks and tasks. |
| Build and verify | Implements the agreed journeys, tests important behavior and checks the UI where tools allow. | Working implementation and honest verification evidence. |
| Authorized release | Finishes the agreed repository/deployment work and explains provider activation. | Usable output, handoff and any explicitly deferred checks. |

The workflow state lives in `docs/workflow-state.md`, so a later session can continue from the current phase rather than asking everything again. A native persistent goal is used only when authorized and supported; a state file is not a background scheduler.

## What is GitHub Spec Kit?

It is an official, separate toolkit from GitHub for building from written specifications. Think of this skill as the guide who helps you decide what to build, and Spec Kit as the organized instruction sheets for building it. This repository does not bundle Spec Kit or impersonate its commands.

Your assistant checks the installed version and the actual integration for your agent. It should follow the [official quickstart](https://github.github.io/spec-kit/quickstart.html), not blindly copy an old command. Installation may require separate tooling. See the [Spec Kit handoff](skills/idea-to-mvp/references/spec-kit.md).

## Choose what “finished” means

- **Credential-ready:** the agreed independent work is finished, with secure setup instructions for specifically accepted missing provider credentials/checks. Those checks remain clearly pending.
- **Fully activated:** the required providers are configured and the agreed real end-to-end checks are completed.

Choose this with the assistant. It must not silently change a fully activated target into credential-ready just because an integration is difficult.

## What you need, and what installation does not do

You need an agent that can read files. Research needs browsing; building needs file and terminal tools; visual checks need browser tools. Cloud deployment and paid providers need your own accounts, access and spending decisions. The assistant should inspect existing authorized access before asking you to repeat setup.

Installing this instruction folder does not buy services, create a schedule, grant access to accounts, approve public releases, or make every agent support the same tools. You can stop at research or planning. Accepting interview recommendations alone does not start a new build phase. Never paste secret keys into chat or commit them.

## Customize it and keep it updated

You may privately add `references/local-profile.md` inside your installed copy for your preferred language, stack or style. It is optional. Keep it out of public commits; the repository ignores that filename. A preference is not permission to spend money or proof that you own an account.

To update, download the new version and compare it with your installed folder. Preserve your changes before replacing it. To remove it, delete only the installed `idea-to-mvp` skill folder or use your agent's documented uninstall control. See [troubleshooting](docs/agent-installation.md#troubleshooting).

## Inside the box

- `skills/idea-to-mvp/SKILL.md`: the main workflow.
- `references/`: interview, Spec Kit and delivery guidance.
- `assets/`: blank templates for the product, project instructions and workflow state.
- `agents/openai.yaml`: Codex display and invocation metadata.

The shared files contain instructions and blank templates, not the creator's projects, personal setup or chat history. [Read the privacy guide](docs/privacy.md) before sharing output from your own future use.

---

Created by [eyoussef-builds](https://github.com/eyoussef-builds) · [hello@eyoussef.me](mailto:hello@eyoussef.me) · [eyoussef.me](https://eyoussef.me)
