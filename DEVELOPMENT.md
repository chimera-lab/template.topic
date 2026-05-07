# :file_folder: Development Environment Setup

## :book: Table of Contents

- [:file_folder: Development Environment Setup](./#file_folder-development-environment-setup)
  - [:clipboard: Requirements](./#clipboard-requirements)
  - [:inbox_tray: Installation](./#inbox_tray-installation)
    - [:inbox_tray: Clone the repository](./#inbox_tray-clone-the-repository)
    - [:inbox_tray: Create development environment](./#inbox_tray-create-development-environment)
    - [:inbox_tray: Install dependencies](./#inbox_tray-install-dependencies)
    - [:inbox_tray: Install pre-commit hooks (optional but recommended)](./#inbox_tray-install-pre-commit-hooks-optional-but-recommended)
  - [:keyboard: Usage](./#keyboard-usage)
  - [:toolbox: Tools](./#toolbox-tools)
    - [:toolbox: Running Tests](./#toolbox-running-tests)
    - [:toolbox: Code Quality](./#toolbox-code-quality)
    - [:toolbox: CMR Pipeline](./#toolbox-cmr-pipeline)
    - [:toolbox: Pre-commit Hooks](./#toolbox-pre-commit-hooks)
  - [:wrench: Configuration](./#wrench-configuration)
  - [:control_knobs: Customization](./#control_knobs-customization)
  - [:hammer_and_wrench: Common Problems](./#hammer_and_wrench-common-problems)

## :clipboard: Requirements

<!-- <llm prompt="Development.Requirements" applied> -->

- Git and GNU Make.
- Node.js with the Chimera Lab `cmr` CLI available on your `PATH`.
- `pre-commit` installed for local quality checks.
- GitHub CLI (`gh`) authenticated if you plan to run GitHub-backed CMR commands.
- Access to the repository submodules; this repository depends on template submodules being initialized.

<!-- </llm> -->

## :inbox_tray: Installation

### :inbox_tray: Clone the repository

<!-- <code lang="bash"> -->

<!-- <data name="REPO_REMOTE"> -->

<!-- <var key="repo.remote" applied> -->git@github.com:chimera-lab/template.topic.git<!-- </var> -->

<!-- </data name="REPO_REMOTE"> -->

<!-- <data name="REPO_NAME"> -->

<!-- <var key="repo.name" applied> -->template.topic<!-- </var> -->

<!-- </data name="REPO_NAME"> -->

```bash
REPO_REMOTE=git@github.com:chimera-lab/repository.template.git
REPO_NAME=repository.template

git clone $REPO_REMOTE
cd $REPO_NAME
```

<!-- </code> -->

### :inbox_tray: Create development environment

<!-- <llm prompt="Development.Installation" applied> -->

After cloning, initialize submodules and ensure the local TypeScript tooling is available in your shell.

```bash
git submodule update --init --recursive
npm install
```

If the CLI is managed from another local checkout or shared toolchain, make sure `cmr` and `pre-commit` are available from your shell before continuing.

<!-- </llm> -->

### :inbox_tray: Install dependencies

<!-- <llm prompt="Development.InstallDependencies" applied> -->

This repository does not define a full root application workflow. Install the developer tooling you need for the TypeScript-based CLI and then verify that the CMR CLI is available.

```bash
npm install
cmr --help
```

If `cmr` is provided from a separate local checkout or shared toolchain, make sure it is on your `PATH` before continuing.

<!-- </llm> -->

### :inbox_tray: Install pre-commit hooks (optional but recommended)

<!-- <llm prompt="Development.PreCommitHooks" applied> -->

Install the Git hooks once per clone so basic formatting and file checks run automatically before each commit.

```bash
make setup
```

That target currently installs the repository pre-commit hooks. You can also run `pre-commit install` directly inside an active environment.

<!-- </llm> -->

## :keyboard: Usage

<!-- <llm prompt="Development.Usage" applied> -->

Most work in this repository follows a short loop: update templates or documentation, render generated content, then run the CMR checks. When you touch inherited files or submodule-backed content, review template status before opening a pull request.

A typical session is:

```bash
make cmr-render
make cmr-check
```

Use `make help` to see the full command set, including template-sync and resource-sync targets.

<!-- </llm> -->

## :toolbox: Tools

### :toolbox: Running Tests

<!-- <llm prompt="Development.Tests" applied> -->

No project-specific unit or integration test suite is wired at the root yet; `make test` is a placeholder target intended for downstream specialization. For this repository, the practical verification baseline is the CMR validation targets and, when you change a specific submodule template, that template's own checks in its directory.

<!-- </llm> -->

### :toolbox: Code Quality

<!-- <llm prompt="Development.CodeQuality" applied> -->

Code quality at the root is centered on documentation and repository hygiene rather than language-specific linting. `make lint` and `make format` are placeholders, while the active checks come from pre-commit and the CMR validation targets.

For day-to-day work, use:

```bash
pre-commit run --all-files
make cmr-check
```

This catches common file issues, Markdown formatting drift, YAML problems, metadata gaps, and documentation/header validation.

<!-- </llm> -->

### :toolbox: CMR Pipeline

<!-- <llm prompt="Development.CmrPipeline" applied> -->

The CMR targets are the main automation surface for this repository. `make cmr-render` normalizes tags and renders directives into tracked Markdown files, `make cmr-check` validates configuration, metadata, documentation, template sync, and GitHub resource definitions, and `make cmr-pipeline` runs both in sequence.

Use `make cmr-template-status` or `make cmr-template-diff` when checking inheritance changes, and `make cmr-template-upgrade` only when you intend to pull updates from the parent template.

<!-- </llm> -->

### :toolbox: Pre-commit Hooks

<!-- <llm prompt="Development.PreCommitTools" applied> -->

The configured hooks focus on repository hygiene:

- `pre-commit-hooks` for whitespace, line endings, merge-conflict markers, large files, and JSON/TOML/YAML validation.
- `mdformat` with GitHub Flavored Markdown support for Markdown formatting.
- `prettier` for YAML formatting.

Run everything locally with `pre-commit run --all-files`, or target a single hook while iterating on a specific file type.

<!-- </llm> -->

## :wrench: Configuration

<!-- <llm prompt="Development.Configuration" applied> -->

Core repository metadata lives in `.chimera-lab/meta.json`, while template inheritance is tracked through `.chimera-lab/.template` and the checked-in Git submodules. Formatting defaults are defined in `.editorconfig`, `.gitattributes`, and `.gitignore`, and CI expectations are outlined in `.github/workflows/`.

When adjusting repository behavior, keep those files aligned so local tooling, generated docs, and GitHub automation continue to agree.

<!-- </llm> -->

## :control_knobs: Customization

<!-- <llm prompt="Development.Customization" applied> -->

This template is intentionally opinionated but not rigid. Common customization points are the placeholder `install`, `test`, `lint`, `format`, `build`, and `docs` targets in `Makefile`, the workflow stubs in `.github/workflows/ci.yml`, the hook set in `.pre-commit-config.yaml`, and the prompt, agent, and skill definitions under `.github/`.

If you specialize the repository for a concrete runtime or delivery workflow, update those surfaces together so the documented commands, CI jobs, and local developer setup stay consistent.

<!-- </llm> -->

## :hammer_and_wrench: Common Problems

<!-- <llm prompt="Development.CommonProblems" applied> -->

Common setup issues usually come down to a small set of causes:

- **`cmr: command not found`**: activate the correct environment or install the Chimera Lab CLI before running Make targets.
- **Missing template content**: run `git submodule update --init --recursive` after cloning.
- **GitHub-backed checks fail**: confirm `gh auth login` or your token-based CMR authentication is in place before running sync or resource checks.
- **Rendered docs keep changing**: run `make cmr-render` before committing so generated tags, variables, and tables of contents are up to date.
- **Pre-commit rewrites files**: review the changes, re-stage them, and rerun the hooks until the tree is clean.

<!-- </llm> -->
