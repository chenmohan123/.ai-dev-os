# ai-dev-os Release and Collaboration Guide

Chinese version: [RELEASE.md](RELEASE.md)

This document defines the recommended branching strategy, release guidance, and first-release checklist for ai-dev-os.

## Recommended Branching Strategy

The recommended setup is one stable branch plus one long-lived development branch:

- `main`: stable branch for external consumption. Repositories using ai-dev-os as a submodule should normally reference this branch or a tagged release.
- `develop`: long-lived integration branch for day-to-day changes such as rule updates, index backfills, and documentation adjustments.
- `feature/*`: short-lived branches for new rule sets, examples, templates, or structural additions.
- `docs/*`: short-lived branches for README, integration, release, and other supporting documentation updates.
- `fix/*`: short-lived branches for path drift, broken links, inconsistent entries, and other focused fixes.

If the repository is maintained by one person only, `main + feature/*` can still work. Once maintenance becomes continuous, keeping `develop` is recommended.

## Recommended Collaboration Flow

1. Create a short-lived branch from `develop`.
2. Complete the change and run focused self-checks.
3. Merge back into `develop` and confirm that entries, indexes, and example navigation are still aligned.
4. When `develop` reaches a stable milestone, merge it into `main`.
5. Tag the release on `main` so consuming repositories can pin to a stable version.

## Suggested Branch Names

- `develop`: long-lived development branch.
- `feature/root-entry-cleanup`: entry or directory structure improvements.
- `feature/integration-guide`: new integration guide or templates.
- `docs/readme-polish`: README or documentation refinement.
- `fix/path-drift`: outdated paths, broken references, or navigation drift fixes.

## Versioning Guidance

If you intend to make the repository consumable by other projects, use semantic version tags:

- `v0.x.y`: still evolving quickly; structure and directory conventions may continue to change.
- `v1.x.y`: root entries, main directory structure, and integration model are relatively stable.

At the current stage, starting from `v0.1.0` is the most reasonable choice.

## First Release Checklist

### Repository Structure

- The repository root directly contains `00_README.md`, `00-overview/`, and the topic directories through `11-ai-engineering/`.
- Old `.ai-dev-os/` internal path wording has been cleaned up where necessary.
- [AGENTS.md](AGENTS.md) and [CLAUDE.md](CLAUDE.md) clearly state that this repository is developing ai-dev-os itself.

### Entries and Navigation

- [00_README.md](00_README.md) remains the single root entry.
- [00-overview/00_README.md](00-overview/00_README.md) and [00-overview/library-index.md](00-overview/library-index.md) still perform their routing roles correctly.
- Any new directory or document has already been backfilled into the relevant entries and indexes.

### External-Facing Documentation

- [README.en.md](README.en.md) or [README.md](README.md) explains the project positioning, quick start path, integration model, and related documents.
- [INTEGRATION.en.md](INTEGRATION.en.md) or [INTEGRATION.md](INTEGRATION.md) is sufficient for consuming repositories to complete submodule integration.
- The selected open-source license is already confirmed in `LICENSE`.

### Release Policy

- `main` is clearly defined as the stable consumption branch and `develop` as the daily development branch.
- The first public tag, such as `v0.1.0`, is agreed.
- It is clear whether consuming repositories should pin to `main`, a tag, or a specific commit.

## Recommendations For Consuming Repositories

- If stability matters, pin to a tag or an explicit commit instead of following `develop`.
- Only let consuming repositories track the latest `main` if you are comfortable exposing them to ongoing rule changes.
- Do not recommend consuming repositories reference `develop` directly.

## What Can Be Added Later

- A sample repository demonstrating submodule-based integration.

This repository already provides [CONTRIBUTING.en.md](CONTRIBUTING.en.md) for contribution workflow and [CHANGELOG.md](CHANGELOG.md) for user-facing change tracking.