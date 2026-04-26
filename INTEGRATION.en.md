# ai-dev-os Integration Guide

Chinese version: [INTEGRATION.md](INTEGRATION.md)

This document explains how to integrate ai-dev-os into another repository as a Git submodule and how to point `AGENTS.md` and `CLAUDE.md` to the correct entry path.

## Recommended Setup

The recommended setup is to mount this repository as a Git submodule under `.ai-dev-os/` in the consuming repository.

```bash
git submodule add <your-repo-url> .ai-dev-os
git submodule update --init --recursive
```

If you do not want to use a hidden directory, you can mount it under `ai-dev-os/` instead. In that case, all entry paths must be updated from `.ai-dev-os/00_README.md` to `ai-dev-os/00_README.md`.

## Example Layout After Integration

```text
your-project/
  AGENTS.md
  CLAUDE.md
  .ai-dev-os/
    00_README.md
    00-overview/
    01-general/
    02-frontend/
    ...
    11-ai-engineering/
    README.md
    LICENSE
```

Notes:

- Keeping `README.md`, `LICENSE`, `AGENTS.md`, and `CLAUDE.md` at the submodule root is normal.
- These files do not interfere with submodule usage.
- The actual rule entry point for the consuming repository is `.ai-dev-os/00_README.md`.

## Suggested AGENTS.md Template For The Consuming Repository

If the consuming repository uses `.ai-dev-os/` as the submodule directory, it can use the following template:

```md
# AGENTS.md

This project uses ai-dev-os as its AI software engineering operating system.
Before working on a task, the AI must read .ai-dev-os/00_README.md and then continue with the project's own documentation, code, and constraints.

If the task involves technology selection, framework selection, component library selection, architecture selection, or template selection, ask the user first and wait for confirmation before continuing.

## Language Requirement

- Use Simplified Chinese for replies, documentation, comments, and explanations.
```

If your directory name is `ai-dev-os/` instead of `.ai-dev-os/`, replace the path accordingly.

## Suggested CLAUDE.md Template For The Consuming Repository

```md
# CLAUDE.md

This repository treats AGENTS.md as the primary and authoritative instruction file.

When working in this repository, read and follow AGENTS.md first.

Additional constraints:

- If CLAUDE.md conflicts with AGENTS.md, AGENTS.md takes precedence.
- This file should stay intentionally minimal and only serve as a compatibility entry point.
```

## Updating The Submodule

To pull the latest rules in the consuming repository:

```bash
git submodule update --remote --recursive
```

If your team prefers to pin the submodule to a specific commit, commit the updated submodule pointer through the normal Git workflow.

## Developing ai-dev-os Itself

If the current repository root directly contains `00_README.md`, `00-overview/`, `01-general/` through `11-ai-engineering/`, then you are developing ai-dev-os itself.

In that case:

- The repository root is the rule library root.
- The entry path is the root `00_README.md`.
- You should not write it as `.ai-dev-os/00_README.md`, because that is the external integration path, not the internal repository path.