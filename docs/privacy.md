# Privacy and data handling

[العربية](privacy.ar.md) · [Main guide](../README.md)

## What is published here

Only the reusable skill instructions, supporting resources, blank templates, documentation and, where present, helper code with synthetic test fixtures. The public signature is limited to `eyoussef-builds`, `hello@eyoussef.me` and `eyoussef.me`.

The package excludes the creator's personal profile, source conversations, real project names/results, real report images, local usernames, device names, private absolute paths, account/project IDs, credentials and private research. Standard generic locations such as `~/.agents/skills/` and `~/.codex` describe installation/runtime conventions; they are not the creator's computer paths.

## What happens when you use it

Your installed agent uses its own tools, permissions and model/service settings. A Markdown skill is not a separate security boundary. Instructions or local helpers do not grant new account access.

For Idea to MVP, your new product brief, research, preview and generated project files may contain your private business idea. Keep them in your own project and decide its repository visibility separately. The skill does not send them to this repository or to its author.

For Daily Progress Report, authorized history is read to prepare your report. The local collector opens the index read-only, does not modify source chat logs, and writes a new evidence folder. It contains no network-upload or telemetry code. It does not crawl unrelated apps or other users' accounts. The evidence can still contain private message text, titles, identifiers and paths. Its token-pattern redaction does not anonymize everything.

The model receives whatever evidence your agent reads into its context. Image-generation services receive the infographic prompt. Use only relevant, non-sensitive highlight facts there; do not include raw chats, credentials or private customer details. The provider's own processing/retention rules still apply. This repository does not promise that using a cloud model keeps data exclusively on your computer.

## Before you share your own output

1. Read the report, product files or images yourself. Remove private people, customer data, internal URLs, account IDs, machine paths and secrets.
2. Keep raw history, scratch evidence, local preferences and `.env` files outside public commits. The included `.gitignore` helps but cannot protect files already committed or explicitly force-added.
3. Check the exact staged file list and the full Git history, not just the visible README. Use a fresh clean export when publishing a reusable skill.
4. Do not attach private evidence when reporting a bug. Describe the format with an invented example instead.

## Reporting a privacy issue

Email [hello@eyoussef.me](mailto:hello@eyoussef.me) with the affected public file and a minimal description. Do not put a secret into a public issue. If a live credential was exposed, revoke/rotate it through its provider; deleting a file alone does not invalidate the credential or erase copies.

---

Created by [eyoussef-builds](https://github.com/eyoussef-builds) · [hello@eyoussef.me](mailto:hello@eyoussef.me) · [eyoussef.me](https://eyoussef.me)
