# :file_folder: Architecture

## :book: Table of Contents

- [:file_folder: Architecture](./#file_folder-architecture)
  - [:telescope: Overview](./#telescope-overview)
  - [:building_construction: Structure](./#building_construction-structure)
    - [:building_construction: Architectural Layers](./#building_construction-architectural-layers)
    - [:building_construction: Responsibilities Per Layer](./#building_construction-responsibilities-per-layer)
    - [:building_construction: Documentation Boundaries](./#building_construction-documentation-boundaries)
    - [:building_construction: Template Inheritance Impact](./#building_construction-template-inheritance-impact)
  - [:triangular_ruler: Technologies](./#triangular_ruler-technologies)
    - [:triangular_ruler: Core Toolchain](./#triangular_ruler-core-toolchain)
    - [:triangular_ruler: Validation Tooling](./#triangular_ruler-validation-tooling)
    - [:triangular_ruler: Publication Readiness](./#triangular_ruler-publication-readiness)
  - [:books: References](./#books-references)

## :telescope: Overview

<!-- llm<Architecture.Overview> -->

This document defines the technical architecture baseline for repositories derived from this template. It explains structural boundaries, integration points, and quality controls so implementations remain consistent across inherited templates.

## :building_construction: Structure

<!-- llm<Architecture.Structure> -->

### :building_construction: Architectural Layers

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

### :building_construction: Responsibilities Per Layer

- Governance layer defines legal and contribution constraints for public distribution.
- Configuration layer stores metadata and template-level behavior used by CMR workflows.
- Automation layer is reserved for GitHub concerns only; no human documentation should be stored here.
- Documentation layer hosts human-facing guides and LLM-oriented knowledge with explicit cross-references.
- Implementation layer contains runtime code and test assets according to repository type.

### :building_construction: Documentation Boundaries

- Human documentation: detailed explanations and operational context in `docs/*.md`.
- LLM knowledge: concise concept maps in `docs/knowledge/*.knowledge.md` with links to detailed docs.
- Structural rule: `.github/` contains GitHub automation artifacts; documentation content belongs in `docs/`.

### :building_construction: Template Inheritance Impact

- `repository.template` is the architecture root for downstream templates.
- Child templates may extend architecture details but should not break baseline layer boundaries.
- Shared changes must be performed at the highest suitable template level to reduce duplication and drift.

## :triangular_ruler: Technologies

<!-- llm<Architecture.Technologies> -->

### :triangular_ruler: Core Toolchain

- Git for source control and submodule orchestration.
- CMR CLI for documentation validation, template synchronization, and structural checks.
- GitHub Actions for CI validation and publication pipelines.

### :triangular_ruler: Validation Tooling

- `cmr docs check` for full documentation compliance.
- `cmr docs check --tags` for LLM/CMR render directive validation.
- `cmr docs fix -r toc -r header-emoji` for standardized formatting repair.
- `cmr config headers list` for typed-header vocabulary verification.

### :triangular_ruler: Publication Readiness

- Repository should be publishable under Apache-2.0 with required notices preserved.
- Documentation and metadata must be consistent before release tagging.
- CI should fail on structural violations to prevent drift from template architecture.

## :books: References

- [:page_facing_up: ../../README.md](../../README.md)
- [:page_facing_up: STRUCTURE.md](STRUCTURE.md)
- [:page_facing_up: ORGANIZATION.md](ORGANIZATION.md)
- [:page_facing_up: ROADMAP.md](ROADMAP.md)
- [:page_facing_up: knowledge/repository.knowledge.md](knowledge/repository.knowledge.md)
- [:page_facing_up: knowledge/validating.knowledge.md](knowledge/validating.knowledge.md)
