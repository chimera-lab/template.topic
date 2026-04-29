# :file\_folder: Architecture

## :book: Table of Contents

- [:file\_folder: Architecture](./#file_folder-architecture)
  - [:telescope: Overview](./#telescope-overview)
  - [:building\_construction: Structure](./#building_construction-structure)
    - [:building\_construction: Architectural Layers](./#building_construction-architectural-layers)
    - [:building\_construction: Responsibilities Per Layer](./#building_construction-responsibilities-per-layer)
    - [:building\_construction: Documentation Boundaries](./#building_construction-documentation-boundaries)
    - [:building\_construction: Template Inheritance Impact](./#building_construction-template-inheritance-impact)
  - [:triangular\_ruler: Technologies](./#triangular_ruler-technologies)
    - [:triangular\_ruler: Core Toolchain](./#triangular_ruler-core-toolchain)
    - [:triangular\_ruler: Validation Tooling](./#triangular_ruler-validation-tooling)
    - [:triangular\_ruler: Publication Readiness](./#triangular_ruler-publication-readiness)
  - [:books: References](./#books-references)

## :telescope: Overview

<!-- <llm prompt="Architecture.Overview" applied> -->

This repository is organized as a template library for topic-oriented project documentation. Each top-level `*.template/` directory represents a reusable documentation module or scaffold, while the repository root contains shared governance, contribution, and maintenance files used across all templates.

The structure follows a simple separation of concerns:

- Template packages such as `app.template/`, `project.template/`, `repository.template/`, and `topic.template/` define distinct documentation building blocks.
- Specialized variants such as `laravel_app.template/`, `typescript_app.template/`, and Docker-related templates adapt the same approach for specific technology stacks.
- `docs/` contains supporting reference material and repository-level design artifacts.
- Root files such as `README.md`, `DEVELOPMENT.md`, and `Makefile` provide repository guidance and operational entry points.

In practice, the architecture favors modularity over a single monolithic template: common documentation concepts are split into focused template directories so they can be combined, extended, and maintained independently.

<!-- </llm> -->

This document defines the technical architecture baseline for repositories derived from this template. It explains structural boundaries, integration points, and quality controls so implementations remain consistent across inherited templates.

## :building\_construction: Structure

<!-- <llm prompt="Architecture.Structure" applied> -->

This repository is organized as a template library, with each top-level `*.template/` directory representing a self-contained documentation or project scaffold variant. Shared repository metadata and contributor guidance live at the root, while cross-cutting reference material is grouped under `docs/`.

The structure follows a clear separation of concerns:

- Root files such as `README.md`, `DEVELOPMENT.md`, `CONTRIBUTING.md`, `SECURITY.md`, and `CHANGELOG.md` define project-wide usage, maintenance, and governance.
- Template directories such as `app.template/`, `project.template/`, `repository.template/`, `topic.template/`, and related variants contain the actual reusable template content.
- `docs/` holds supporting documentation and reference assets for understanding and maintaining the template system.
- `Makefile` provides repository-level automation for common maintenance workflows.

This layout keeps template content isolated from repository operations and documentation, making each template easier to evolve independently while preserving consistent project-wide standards.

<!-- </llm> -->

### :building\_construction: Architectural Layers

```text
Repository Architecture
├── Governance Layer
│   ├── LICENSE
│   ├── SECURITY.md
│   ├── CODE_OF_CONDUCT.md
│   └── CONTRIBUTING.md
├── Configuration Layer
│   ├── .chimera-lab/meta.json
│   └── .chimera-lab/settings.json
├── Automation Layer
│   └── .github/{agents,prompts,skills,workflows}
├── Documentation Layer
│   ├── README.md
│   ├── docs/{ARCHITECTURE,ORGANIZATION,ROADMAP,STRUCTURE}.md
│   └── docs/knowledge/*.knowledge.md
└── Implementation Layer
  ├── src/
  ├── tests/
  └── tooling/config files
```

### :building\_construction: Responsibilities Per Layer

- Governance layer defines legal and contribution constraints for public distribution.
- Configuration layer stores metadata and template-level behavior used by CMR workflows.
- Automation layer is reserved for GitHub concerns only; no human documentation should be stored here.
- Documentation layer hosts human-facing guides and LLM-oriented knowledge with explicit cross-references.
- Implementation layer contains runtime code and test assets according to repository type.

### :building\_construction: Documentation Boundaries

- Human documentation: detailed explanations and operational context in `docs/*.md`.
- LLM knowledge: concise concept maps in `docs/knowledge/*.knowledge.md` with links to detailed docs.
- Structural rule: `.github/` contains GitHub automation artifacts; documentation content belongs in `docs/`.

### :building\_construction: Template Inheritance Impact

- `repository.template` is the architecture root for downstream templates.
- Child templates may extend architecture details but should not break baseline layer boundaries.
- Shared changes must be performed at the highest suitable template level to reduce duplication and drift.

## :triangular\_ruler: Technologies

<!-- <llm prompt="Architecture.Technologies" applied> -->

This repository is documentation- and template-driven rather than application-runtime driven. Its architecture relies on portable text assets, organized scaffold directories, and lightweight automation to support repeatable repository and project generation workflows.

- **Markdown** is the primary authoring format for documentation and reusable template content.
- **Template directories** such as `topic.template/`, `project.template/`, `package.template/`, `app.template/`, and framework-specific variants provide structured, composable scaffolds.
- **Template variables/placeholders** enable organization- or project-specific customization without changing the base template layout.
- **Make** is used for lightweight repository automation and repeatable maintenance tasks.
- **GitHub-native repository conventions** are part of the operating model, including standard community, contribution, and security documentation.

The stack is intentionally minimal and text-first, which keeps the repository easy to maintain, review, version, and adapt across different project types.

<!-- </llm> -->

### :triangular\_ruler: Core Toolchain

- Git for source control and submodule orchestration.
- CMR CLI for documentation validation, template synchronization, and structural checks.
- GitHub Actions for CI validation and publication pipelines.

### :triangular\_ruler: Validation Tooling

- `cmr docs check` for full documentation compliance.
- `cmr docs check --tags` for LLM/CMR render directive validation.
- `cmr docs fix -r toc -r header-emoji` for standardized formatting repair.
- `cmr config headers list` for typed-header vocabulary verification.

### :triangular\_ruler: Publication Readiness

- Repository should be publishable under Apache-2.0 with required notices preserved.
- Documentation and metadata must be consistent before release tagging.
- CI should fail on structural violations to prevent drift from template architecture.

## :books: References

- [:page\_facing\_up: ../../README.md](../../README.md)
- [:page\_facing\_up: STRUCTURE.md](STRUCTURE.md)
- [:page\_facing\_up: ORGANIZATION.md](ORGANIZATION.md)
- [:page\_facing\_up: ROADMAP.md](ROADMAP.md)
- [:page\_facing\_up: knowledge/repository.knowledge.md](knowledge/repository.knowledge.md)
- [:page\_facing\_up: knowledge/validating.knowledge.md](knowledge/validating.knowledge.md)
