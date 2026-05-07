# :file_folder: Organization

## :book: Table of Contents

- [:file_folder: Organization](./#file_folder-organization)
  - [:telescope: Overview](./#telescope-overview)
  - [:building_construction: Structure](./#building_construction-structure)
  - [:toolbox: Tools](./#toolbox-tools)
  - [:books: References](./#books-references)

## :telescope: Overview

<!-- <llm prompt="Organization.Overview" applied> -->

This repository is organized as a central template workspace for Chimera Lab. It combines top-level documentation and automation with a curated set of template repositories so contributors can maintain shared standards, documentation patterns, and template inheritance from one place.

<!-- </llm> -->

## :building_construction: Structure

<!-- <llm prompt="Organization.Structure" applied> -->

The root groups repository-wide governance, contributor guidance, and automation files. Supporting configuration lives in `.chimera-lab/` and `.github/`, while `docs/` contains the explanatory documentation for structure, architecture, organization, and planning.

Template content is separated into dedicated submodule directories such as `repository.template/`, `topic.template/`, `project.template/`, `app.template/`, and other specialized variants. This keeps each template self-contained while allowing the root repository to coordinate shared conventions and updates across the template family.

<!-- </llm> -->

## :toolbox: Tools

<!-- <llm prompt="Organization.Tools" applied> -->

Organization work in this repository is supported primarily by the CMR CLI, Git submodules, GitHub Actions, and pre-commit hooks. The `Makefile` provides a consistent entry point for common maintenance tasks such as rendering documentation, validating metadata, checking template sync status, and running the full CMR pipeline.

In practice, contributors use `make help` to discover targets, `make cmr-render` and `make cmr-check` for documentation and repository validation, `make cmr-template-status` or `make cmr-template-diff` for inheritance review, and `pre-commit run --all-files` for local hygiene checks.

<!-- </llm> -->

## :books: References

- [:page_facing_up: STRUCTURE.md](STRUCTURE.md)
- [:page_facing_up: ../../README.md](../../README.md)
