# ai-dev-os

Chinese version: [README.md](README.md)

ai-dev-os is a rule library and operating system for AI-driven software engineering. It is designed to standardize task intake, repository routing, minimal-change execution, validation loops, and governance practices.

This repository is the ai-dev-os source repository itself. The rule content lives directly at the repository root. When working inside this repository, start from [00_README.md](00_README.md) and then follow the index into the relevant topic directory.

Note: the authoritative rule content and examples are currently maintained in Chinese. English documentation is provided first for project overview, integration, and collaboration entry points.

## What It Is For

- Providing a consistent operating model for AI coding agents.
- Reusing one shared engineering rule system across multiple repositories.
- Making practices such as minimal changes, early validation, failure recovery, and auditability explicit and reusable.

## Repository Structure

- [00_README.md](00_README.md): the single root entry for the rule library.
- [00-overview](00-overview): global overview, navigation, and maintenance conventions.
- [01-general](01-general) to [11-ai-engineering](11-ai-engineering): topic-specific rule directories.
- [AGENTS.md](AGENTS.md) and [CLAUDE.md](CLAUDE.md): instructions for working on ai-dev-os itself.

## Quick Start

If this is your first time entering the repository, read in this order:

1. [00_README.md](00_README.md)
2. [00-overview/00_README.md](00-overview/00_README.md)
3. [00-overview/library-index.md](00-overview/library-index.md)
4. The relevant topic directory's `00_README.md`

## Using It As a Git Submodule

The recommended setup is to add this repository to another project as a Git submodule under `.ai-dev-os/`.

```bash
git submodule add <your-repo-url> .ai-dev-os
git submodule update --init --recursive
```

Example layout:

```text
your-project/
  AGENTS.md
  CLAUDE.md
  .ai-dev-os/
    00_README.md
    00-overview/
    01-general/
    ...
    11-ai-engineering/
```

Keeping `README.md`, `LICENSE`, `AGENTS.md`, and `CLAUDE.md` at the submodule root is normal and does not interfere with submodule usage. The actual rule entry point for the consuming repository is `.ai-dev-os/00_README.md`.

For full integration steps and templates, see [INTEGRATION.en.md](INTEGRATION.en.md).

## Development vs Integration

There are two different path perspectives:

- Inside this repository: the root entry is [00_README.md](00_README.md).
- Inside a consuming repository that mounts ai-dev-os as a submodule: the entry path is `.ai-dev-os/00_README.md`.

Do not mix these two perspectives when writing instructions.

## Support

If this project is helpful to you, you are welcome to support its ongoing maintenance.

See [SUPPORT.en.md](SUPPORT.en.md).

## Related Documents

- [INTEGRATION.en.md](INTEGRATION.en.md): submodule integration guide and templates.
- [CONTRIBUTING.en.md](CONTRIBUTING.en.md): contribution workflow, index backfill rules, and pre-submit checks.
- [RELEASE.en.md](RELEASE.en.md): branching strategy, release recommendations, and first-release checklist.
- [CHANGELOG.md](CHANGELOG.md): user-facing changes and upgrade impact summaries.
- [SUPPORT.en.md](SUPPORT.en.md): support and sponsorship options.