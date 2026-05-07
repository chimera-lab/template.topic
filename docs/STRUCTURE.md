# :file_folder: Repository Structure

## :book: Table of Contents

- [:file_folder: Repository Structure](./#file_folder-repository-structure)
  - [:telescope: Overview](./#telescope-overview)
  - [:building_construction: Structure](./#building_construction-structure)
    - [:building_construction: Layer Separation Rules](./#building_construction-layer-separation-rules)
      - [:building_construction: Semantic Header Vocabulary](./#building_construction-semantic-header-vocabulary)
      - [:building_construction: GitHub Automation Structure](./#building_construction-github-automation-structure)
  - [:books: References](./#books-references)

## :telescope: Overview

<!-- <llm prompt="Structure.Overview" applied> -->

This repository is organized as a documentation-first template workspace. The root combines governance files, developer tooling, CMR metadata, and a set of template repositories tracked as submodules, while the `docs/` directory holds the narrative documentation that explains how the repository is structured and maintained.

The layout favors clear separation between repository-wide policy, automation, rendered documentation, and reusable template content so contributors can update one concern without obscuring the others.

<!-- </llm> -->

## :building_construction: Structure

<!-- <llm prompt="Structure.Structure" applied> -->

At the top level, the repository contains standard governance and contributor-facing files such as `README.md`, `CONTRIBUTING.md`, `DEVELOPMENT.md`, `CHANGELOG.md`, `SECURITY.md`, and `CODE_OF_CONDUCT.md`. Tooling and automation live alongside them in `Makefile`, `.pre-commit-config.yaml`, `.editorconfig`, `.gitattributes`, `.gitignore`, `.github/`, and `.chimera-lab/`.

The `docs/` directory is reserved for structured project documentation, including architecture, organization, roadmap, and structure references. Reusable repository templates are stored as Git submodules in directories such as `repository.template/`, `topic.template/`, `project.template/`, `app.template/`, and related variants, allowing this repository to act both as documentation and as a template catalog.

<!-- </llm> -->

### :building_construction: Layer Separation Rules

<!-- <llm prompt="Structure.LayerSeparation" applied> -->

Keep repository concerns separated by intent. Root-level governance files describe policy and contribution flow, `docs/` explains the system and its conventions, `.github/` contains GitHub-facing automation and issue metadata, and `.chimera-lab/` stores Chimera Lab configuration and template metadata.

Template repositories should remain self-contained inside their own directories rather than leaking implementation details into the root. When changing shared behavior, prefer updating the relevant template or automation surface directly instead of duplicating the same rule across multiple documentation files.

<!-- </llm> -->

#### :building_construction: Semantic Header Vocabulary

<!-- <llm prompt="Structure.SemanticHeaders" applied> -->

Documentation in this repository follows a semantic heading style that pairs an emoji with a short noun phrase, for example `:telescope: Overview`, `:building_construction: Structure`, `:toolbox: Tools`, and `:books: References`. The goal is consistency and fast scanning rather than decoration alone.

Use overview sections for purpose and scope, structure sections for layout and relationships, tools or configuration sections for operational details, and references sections for onward navigation. Keep heading names stable across documents so generated tables of contents, CMR checks, and cross-document reading patterns remain predictable.

<!-- </llm> -->

#### :building_construction: GitHub Automation Structure

<!-- <llm prompt="Structure.GitHubAutomation" applied> -->

GitHub-specific automation is grouped under `.github/`. `workflows/` contains CI and pre-commit workflow definitions, `ISSUE_TEMPLATE/` holds repository issue forms, and adjacent prompt or skill directories provide structured inputs for automation-assisted maintenance and writing flows.

This separation keeps repository automation declarative and discoverable. Operational logic that runs on GitHub belongs in workflows and templates here, while local developer commands remain anchored in the `Makefile` and repository configuration files.

<!-- </llm> -->

## :books: References

<!-- <llm prompt="Structure.References" applied> -->

- [:page_facing_up: ../../README.md](../../README.md) - Repository entry point and high-level context.
- [:page_facing_up: ../ARCHITECTURE.md](../ARCHITECTURE.md) - Architectural view of the repository and its components.
- [:page_facing_up: ../ORGANIZATION.md](../ORGANIZATION.md) - How repository content is grouped and managed.
- [:page_facing_up: ../ROADMAP.md](../ROADMAP.md) - Planned maintenance and future improvements.
- [:page_facing_up: ../../DEVELOPMENT.md](../../DEVELOPMENT.md) - Local setup, tooling, and validation workflow.

<!-- </llm> -->
