# :file_folder: <!-- <var key="repository.name"> --><!-- </var> -->

Repository template providing the standard structure, docs, and contribution workflow for <!-- <var key="org.name" applied> -->chimera-lab<!-- </var> --> projects.

## :book: Table of Contents

- [:file_folder: <!-- <var key="repository.name"> --><!-- </var> -->](./#file_folder-var-keyrepositoryname-var)
  - [:telescope: Overview](./#telescope-overview)
  - [:clipboard: Requirements](./#clipboard-requirements)
  - [:inbox_tray: Installation](./#inbox_tray-installation)
  - [:keyboard: Usage](./#keyboard-usage)
  - [:books: References](./#books-references)
  - [:scroll: License](./#scroll-license)

## :telescope: Overview

<!-- <llm prompt="Overview" applied> -->

This repository provides the shared topic template set for the Chimera Lab documentation system. It contains reusable templates for common repository and project surfaces, including organization, repository, project, package, scaffold, application, and framework-specific layouts, so teams can create consistent documentation with a common structure and terminology.

The repository is intended to standardize how documentation is organized across related projects, reduce duplication, and make template maintenance easier. Each `*.template/` directory represents a template variant that can be reused or adapted when scaffolding documentation for a specific software repository or topic.

<!-- </llm> -->

## :clipboard: Requirements

<!-- <llm prompt="Requirements" applied> -->

- Git and a GitHub account for cloning the repository, creating branches, and opening pull requests.
- A Unix-like shell with `make` available if you plan to use the repository automation.
- A text or Markdown editor that preserves HTML comments, because the templates use comment-based variable markers.
- Basic familiarity with Markdown and the repository's template layout before modifying files in the `*.template/` directories.

<!-- </llm> -->

## :inbox_tray: Installation

<!-- <llm prompt="Installation" applied> -->

No package or binary installation is required to use these templates.

1. Clone the repository:

   ```bash
   git clone https://github.com/chimera-lab/template.topic.git
   cd template.topic
   ```

2. Choose the template directory that matches your use case, such as `topic.template/`, `project.template/`, `repository.template/`, or `package.template/`.

3. Copy the relevant template content into your target repository and replace placeholder values with your organization, project, or topic-specific details.

If you want to work with the repository locally, make sure these standard tools are available:

- `git`
- `make`

For best results, customize templates in a feature branch so changes can be reviewed before publishing.

<!-- </llm> -->

## :keyboard: Usage

<!-- <llm prompt="Usage" applied> -->

Use this repository as a source of reusable documentation templates. Each `*.template/` directory provides a focused skeleton for a specific documentation scope, such as repositories, projects, packages, apps, scaffolds, and topics.

1. Select the template directory that matches your documentation target.
2. Copy its contents into the destination repository or documentation workspace.
3. Replace template variables and placeholder content with project-specific values.
4. Remove sections that do not apply, then expand the remaining sections with concrete documentation.
5. Keep the established header hierarchy so the generated documentation stays consistent across repositories.

Example workflow:

```bash
cp -R repository.template/ ../my-repo/docs/
```

When working across multiple documentation layers, start with higher-level templates such as `overview.template/`, `org.template/`, or `topic.template/`, then add lower-level templates like `project.template/`, `package.template/`, or `repository.template/` as needed.

Use the templates as a structured starting point, not as final content. Tailor them to the actual system, ownership model, delivery process, and maintenance expectations of the target repository.

<!-- </llm> -->

## :books: References

- [:page_facing_up: CODE_OF_CONDUCT.md](CODE_OF_CONDUCT.md)
- [:page_facing_up: CONTRIBUTING.md](CONTRIBUTING.md)
- [:page_facing_up: SECURITY.md](SECURITY.md)
- [:page_facing_up: ./docs/STRUCTURE.md](./docs/STRUCTURE.md) - Project Structure
- [:page_facing_up: ./docs/ORGANIZATION.md](./docs/ORGANIZATION.md) - Managing entity

## :scroll: License

- Licensed under the terms specified in [:link: LICENSE](LICENSE). Review before distributing or reusing this template.

<!-- <llm prompt="tags:topic.template" applied> -->

- template
- topic
<!-- </llm> -->