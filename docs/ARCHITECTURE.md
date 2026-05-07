# :file_folder: Architecture

## :book: Table of Contents

- [:file_folder: Architecture](./#file_folder-architecture)
  - [:telescope: Overview](./#telescope-overview)
  - [:triangular_ruler: Technologies](./#triangular_ruler-technologies)
  - [:building_construction: Structure](./#building_construction-structure)
  - [:jigsaw: Components](./#jigsaw-components)
  - [:books: References](./#books-references)

## :telescope: Overview

<!-- <llm prompt="Architecture.Overview" applied> -->

This repository is a documentation-centric template hub rather than a single deployable application. Its architecture centers on coordinating repository metadata, documentation rendering, validation workflows, and a family of template repositories managed together through Git submodules and CMR automation.

<!-- </llm> -->

## :triangular_ruler: Technologies

<!-- <llm prompt="Architecture.Technologies" applied> -->

The core technologies are Git for source and submodule management, Markdown for repository documentation, Make for task orchestration, pre-commit for local quality checks, GitHub Actions for CI automation, and the Chimera Lab `cmr` CLI for documentation rendering, metadata validation, template synchronization, and GitHub resource checks.

Supporting configuration is defined through standard repository files such as `.editorconfig`, `.gitattributes`, `.gitignore`, YAML workflow files, and Chimera Lab metadata under `.chimera-lab/`.

<!-- </llm> -->

## :building_construction: Structure

<!-- <llm prompt="Architecture.Structure" applied> -->

The architecture is layered around a small set of clear responsibilities. Root-level files define contributor guidance, governance, and automation entry points; `docs/` captures human-readable structure and operational context; `.github/` contains GitHub-native automation assets; and `.chimera-lab/` stores template linkage and repository metadata consumed by CMR.

Alongside those layers, each `*.template/` directory acts as an independent template unit with its own files and documentation. The root repository ties these units together, making it possible to review, render, validate, and upgrade shared template behavior from a central workspace.

<!-- </llm> -->

## :jigsaw: Components

<!-- <llm prompt="Architecture.Components" applied> -->

The main architectural components are:

- **Repository governance layer**: root Markdown files such as `README.md`, `CONTRIBUTING.md`, `DEVELOPMENT.md`, and related policy documents.
- **Documentation layer**: the `docs/` directory, which describes architecture, organization, structure, and planning.
- **Automation layer**: `Makefile`, `.pre-commit-config.yaml`, and `.github/workflows/` for local and CI-driven maintenance.
- **CMR metadata layer**: `.chimera-lab/` for repository metadata and template tracking.
- **Template catalog layer**: submodule directories such as `repository.template/`, `topic.template/`, `project.template/`, `app.template/`, and other specialized templates managed from this repository.

<!-- </llm> -->

## :books: References

- [:page_facing_up: ../../README.md](../../README.md)
- [:page_facing_up: STRUCTURE.md](STRUCTURE.md)
- [:page_facing_up: ORGANIZATION.md](ORGANIZATION.md)
- [:page_facing_up: ROADMAP.md](ROADMAP.md)
