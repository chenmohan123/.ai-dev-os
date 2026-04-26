# ai-dev-os Contribution Guide

Chinese version: [CONTRIBUTING.md](CONTRIBUTING.md)

This document explains how to contribute new rules, navigation updates, examples, templates, and supporting documentation to ai-dev-os in a way that stays stable, traceable, and maintainable.

## Before You Start

Before making changes, read in this order:

1. [00_README.md](00_README.md)
2. [00-overview/00_README.md](00-overview/00_README.md)
3. [00-overview/library-index.md](00-overview/library-index.md)
4. [00-overview/library-maintenance.md](00-overview/library-maintenance.md)
5. The target directory's `00_README.md`

If you are changing AI software engineering workflow content, also read [11-ai-engineering/00_README.md](11-ai-engineering/00_README.md).

## What Contributions Are Welcome

Good contributions include:

- Adding missing `00_README.md` files, navigation pages, examples, or templates.
- Improving entry guidance, boundaries, reading order, or validation expectations in existing documents.
- Fixing broken links, outdated paths, drifted directory references, or clear wording issues.
- Adding supporting documents such as integration, release, or collaboration guides.

Avoid mixing all of the following into one change set:

- Large-scale directory renames.
- Open-ended repository-wide rewrites.
- New rules, historical cleanup, directory migration, and wording polish all at once.

## Core Collaboration Principles

- Prefer minimal changes: solve one clear problem at a time.
- Entry first: when adding a directory or section, add the entry point before expanding the body content.
- Backfill indexes: if you add a directory, entry page, or high-frequency path, update the relevant navigation files as well.
- Keep paths stable: do not rename widely referenced files casually.
- Converge wording first: align wording before considering file or directory renames.
- Chinese remains authoritative: rule text and examples are primarily maintained in Simplified Chinese.

## Branching Suggestions

Follow the strategy described in [RELEASE.md](RELEASE.md):

- `develop`: long-lived development branch.
- `feature/*`: new rule sets, templates, examples, or directory capabilities.
- `docs/*`: README, integration, contribution, and other documentation updates.
- `fix/*`: path drift, broken links, entry inconsistencies, and other focused fixes.

Example:

```bash
git checkout develop
git pull
git checkout -b docs/contributing-guide-en
```

## Rules For Updating The Rule Library

### Adding A Top-Level Directory

- Use a two-digit numeric prefix plus a topic name.
- Create that directory's `00_README.md` first.
- Backfill [00_README.md](00_README.md) and [00-overview/00_README.md](00-overview/00_README.md).
- If the change affects common reading paths, also update [00-overview/library-index.md](00-overview/library-index.md).

### Adding A Section Within A Topic

- Use names like `NN_topic-rule.md` or `NN_topic-template.md`.
- Let numbering express reading order or responsibility order.
- Update that topic directory's `00_README.md`.
- If the new section affects cross-directory reading paths, update the relevant index or navigation page.

### Editing Historical Content

- Prefer fixing wording and entry guidance first.
- If you must change a path, identify all references and update them together.
- Do not combine structural refactors with large content expansions in one round.

## Pre-Submission Checklist

Before submitting, check at least the following:

- [00_README.md](00_README.md) is still the single root entry.
- Any new directory has its own `00_README.md`.
- The relevant directory entry, overview entry, or global index has been backfilled.
- No outdated paths, broken links, or conflicting wording were introduced.
- Temporary conclusions were not accidentally turned into long-term rules.
- Multiple unrelated topics were not mixed into one submission.

## Suggested Commit Messages

Commit messages do not need to be complicated, but they should state the main purpose clearly:

- `docs: add contributing and integration guides`
- `docs: align root entry and submodule entry wording`
- `feat: add 11-ai-engineering example navigation`
- `fix: remove old .ai-dev-os path references`

## Suggested Pull Request Description

When opening a pull request, explain at least:

- What problem this change solves.
- Which entries, directories, or examples were updated.
- Whether indexes and navigation were backfilled.
- Whether there are structural or path changes that need extra review.

## What To Avoid

- Expanding body content without updating entries and indexes.
- Updating only README while leaving the real navigation inside the rule library inconsistent.
- Renaming directories or files broadly before checking references.
- Treating temporary conclusions from the current task as long-term project facts.

## Related Documents

- [README.en.md](README.en.md): project overview and quick understanding.
- [INTEGRATION.en.md](INTEGRATION.en.md): integration guide for consuming repositories.
- [RELEASE.md](RELEASE.md): branching strategy and release guidance.
- [00-overview/library-maintenance.md](00-overview/library-maintenance.md): directory structure and naming conventions.