# :package: topic.template

This repository **is a template** for topic repositories. It extends `repository.template` with structure for domain knowledge collections.

## :book: Table of Contents

- [:package: topic.template](./#package-topictemplate)
  - [:telescope: Overview](./#telescope-overview)
  - [:inbox_tray: Installation](./#inbox_tray-installation)
  - [:building_construction: Structure](./#building_construction-structure)
    - [:building_construction: Inherited verbatim from `repository.template`](./#building_construction-inherited-verbatim-from-repositorytemplate)
    - [:building_construction: Extended from `repository.template`](./#building_construction-extended-from-repositorytemplate)
    - [:building_construction: New in `topic.template`](./#building_construction-new-in-topictemplate)
  - [:books: References](./#books-references)

## :telescope: Overview

A repository skeleton for **topic repositories** — curated domain knowledge collections, reference material, and thematic content areas. Extends `repository.template` with:

- Topic-specific `DEVELOPMENT.md` placeholders using the `Topic.Development.*` LLM namespace.
- Topic-specific `docs/ARCHITECTURE.md` with a `:jigsaw: Components` section.
- This `TEMPLATE.md` documenting what distinguishes a topic repo from the base.

## :inbox_tray: Installation

```bash
cmr repo init --template topic.template <new-topic-name>
```

Or use GitHub's "Use this template" button. Updates from this template can be pulled later with:

```bash
cmr repo template upgrade
```

## :building_construction: Structure

### :building_construction: Inherited verbatim from `repository.template`

All root governance files (`LICENSE`, `CHANGELOG.md`, `CONTRIBUTING.md`, `CODE_OF_CONDUCT.md`, `SECURITY.md`, `AGENTS.md`, `Makefile`), `docs/` baseline, `.github/` baseline, and tooling files (`.editorconfig`, `.gitattributes`, `.gitignore`, `.pre-commit-config.yaml`).

### :building_construction: Extended from `repository.template`

| File                   | Change                                                                                        |
| ---------------------- | --------------------------------------------------------------------------------------------- |
| `DEVELOPMENT.md`       | Sections specialised for topic repos using the `Topic.Development.*` LLM namespace            |
| `docs/ARCHITECTURE.md` | Adds `:jigsaw: Components` h2 with pending `<llm prompt="Architecture.Components">` directive |

### :building_construction: New in `topic.template`

| File          | Purpose                                                                  |
| ------------- | ------------------------------------------------------------------------ |
| `TEMPLATE.md` | This file — documents the template's purpose and differences from parent |

## :books: References

- Parent template: [:page_facing_up: repository.template](https://github.com/chimera-lab/repository.template)
- [:page_facing_up: docs/ARCHITECTURE.md](docs/ARCHITECTURE.md) - Architectural overview
