# :file_folder: Chimera-lab - README Documents Syntax Rules

## :book: Table of Contents

<!-- toc -->

## :book: Repositoryepository

### :book: Name

- Repository should always have a suffix name, use an appropriated organization template to name it.

### :book: Projects

#### :book: Stages

| Stage | Goal | Exit Criteria Questions |
|---|---|---|
| **Ideating** | Generate ideas | Is there a clear problem and a viable solution idea? |
| **Planning** | Define direction | Is there a basic roadmap with tasks and time estimates? |
| **Building** | Create MVP | Are the main features working without critical crashes? |
| **Presenting** | Make it usable | Can someone use or demo the basic interface with guidance? |
| **Sharing** | Show to the world | Is it published with clear info and a way to get feedback? |
| **Polishing** | Refine | Is the code clean, modular, and the infra/configs stable? |
| **Releasing** | Launch as product | Is it ready for public use with support and monetization? |

### :book: Commits

### :book: Issues

#### :book: Milestones

#### :book: Labels

##### :book: Common

- **bug** — Something isn't working `#d73a4a`
- **documentation** — Improvements or additions to documentation `#0366d6`
- **duplicate** — This issue or pull request already exists `#7e7e7e`
- **enhancement** — New feature or request `#22863a`
- **good first issue** — Good for newcomers `#7057ff`
- **help wanted** — Extra attention is needed `#ff7f50`
- **invalid** — This doesn't seem right `#e4e669`
- **question** — Further information is requested `#ff69b4`
- **wontfix** — This will not be worked on `#4b0000`

##### :book: General

- **logic** — Business or application logic `#af52fd`
- **performance** — Performance related `#fbca04`
- **testing** — Tests and quality assurance `#a4cc83`
- **security** — Security concerns `#b31d28`
- **logging** — Handling, storing, or visualizing logs `#5319e7`
- **configuration** — Managing system configurations `#f6f8fa`
- **authentication** — Verifying user or system identity `#8a2be2`
- **authorization** — Controlling access permissions `#ff1493`

##### :book: Infrastructure

- **software** — General-purpose software project `#00bfff`
- **infrastructure** — System infrastructure provisioning or configuration `#1d76db`
- **containerization** — Use of containers to package and deploy software `#d93f0b`
- **orchestration** — Managing container lifecycle and deployments `#e36209`
- **automation** — Automating infrastructure `#006b75`
- **load-balancing** — Distributing traffic across systems `#c1440e`
- **monitoring** — Observing system performance and health `#7e7e7e`
- **cicd** — Continuous integration and deployment pipelines `#0052cc`
- **observability** — Visibility into system operations and metrics `#ff7f50`
- **storage** — Projects using databases or storage solutions `#22863a`
- **frontend** — Client-side applications, UI, or user interaction `#0e8a16`
- **backend** — Server-side services or infrastructure `#6f42c1`
- **microservice** — Microservice architecture components `#f9d0c4`

##### :book: Interface

- **ui** — Related to user interface design `#e11d21`
- **ux** — Related to user experience and usability `#ffa07a`
- **desktop** — Web-based applications with user-facing interfaces `#0366d6`
- **mobile** — Projects targeting iOS or Android platforms `#f66a0a`
- **cli** — Command-line interface applications `#e99695`

##### :book: Embedded

- **hardware** — Related to physical components or electronics `#9370db`
- **firmware** — Embedded software running on hardware devices `#20b2aa`
- **operating-system** — OS-level projects or dependencies `#40e0d0`

##### :book: Study

- **terminology** — Related to glossary, terms, definitions `#4f9f04`
- **configuration** — Setup, environment, or files configuration `#aacb0c`
- **guides** — Step-by-step tutorials or instructions `#9bb611`
- **chapters** — Content divided by chapters or sections `#c1440e`
- **problems** — Known issues or troubleshooting notes `#af52fd`
- **appendix** — Supplemental notes, references, or credits `#f39abe`
- **exercise** — Practice tasks or exercises `#758981`
- **example** — Code or content examples `#9cbea5`
- **review** — Content or code needing review or feedback `#a4cc83`

### :book: Branchs

### :book: Templates

- Version must be present as `<!--(version=a.b.c)-->`.
  - 'a' - changes require revision.
  - 'b' - changes can be resolved.
  - 'c' - changes can be ignored.
- Any change to the template that modifies the document structure should have its version updated.
- Every header should have an emoji prefix as documented in [Document Headers](#document-headers)

#### :book: List of Templates

- [:open_file_folder: chimera-lab/repository.template](https://github.com/chimera-lab/repository.template)
  - [:open_file_folder: chimera-lab/topic.template](https://github.com/chimera-lab/topic.template)
  - [:open_file_folder: chimera-lab/overview.template](https://github.com/chimera-lab/overview.template)
  - [:open_file_folder: chimera-lab/diy.template](https://github.com/chimera-lab/diy.template)
  - [:open_file_folder: chimera-lab/app.template](https://github.com/chimera-lab/app.template)
    - [:open_file_folder: chimera-lab/laravel_app.template](https://github.com/chimera-lab/laravel_app.template)
  - [:open_file_folder: chimera-lab/project.template](https://github.com/chimera-lab/project.template)
  - [:open_file_folder: chimera-lab/scaffold.template](https://github.com/chimera-lab/scaffold.template)
    - [:open_file_folder: chimera-lab/docker_scaffold.template](https://github.com/chimera-lab/docker_scaffold.template)
  - [:open_file_folder: chimera-lab/org.template](https://github.com/chimera-lab/org.template)

#### :book: Child MarkDown Documentation

Child documents should be presented in the template prefixed with "README.".

#### :book: Document Headers

Document's main headers should be prefixed with `:file_folder:`, example `# :file: Chimera-lab`.

Document headers must always have an emoji, must match the following terms or the parent header emoji.

##### :paperclip: Appendix

##### :book: {doc.chapter}

##### :hammer_and_wrench: Common problems

##### :wrench: Configuration

##### :busts_in_silhouette: Contributing

##### :medal_military: Credits

##### :control_knobs: Customization

##### :page_facing_up: Files

##### :book: {doc.guide}

##### :book: {doc.step}

##### :inbox_tray: Installation

##### :loudspeaker: Introduction

##### :package: Material

##### :notebook: Notes

##### :telescope: Overview

##### :puzzle_piece: Components

##### :books: References

##### :clipboard: Requirements

##### :link: See also

##### :gear: Software

##### :building_construction: Structure

##### :newspaper: Sources

##### :card_file_box: Submodules

##### :book: Table of Contents

##### :triangular_ruler: Technologies

##### :mag: Terminology

##### :memo: To-do list

##### :toolbox: Tools

##### :keyboard: Usage

##### :scroll: License

##### :warning: Warnings

##### :file_folder: {Chimera LAB's repository name}

#### :book: Link prefixes

##### :globe_with_meridians: External link

##### :file_folder: Chimera LAB's repositories

##### :file_cabinet: Other repositories

##### :mag: Terms

#### :book: Links

- External link names shoud be prefixed with `:globe_with_meridians:` :globe_with_meridians:.

  - Example: `:globe_with_meridians: [Wikipedia](https://www.wikipedia.org/)` [:globe_with_meridians: Wikipedia](https://www.wikipedia.org/)

- Link associated to Organization repositories shoud have their name prefixed with `:open_file_folder:` :open_file_folder:.

  - Example chimera-lab: `[:open_file_folder: Chimera-lab](https://github.com/chimera-lab/chimera-lab)` [:open_file_folder: chimera-lab/chimera-lab](https://github.com/chimera-lab/chimera-lab)
  - Example others: `[:file_folder: github/docs](https://github.com/github/docs)` [:file_folder: github/docs](https://github.com/github/docs)

- Links related to Organization Terms should have their name prefixed with `:mag:` :mag:.

  - Example: `[:mag: Term](https://github.com/chimera-lab/template.topic?tab=readme-ov-file#repository)` [:mag: Term](https://github.com/chimera-lab/template.topic?tab=readme-ov-file#repository)

- Links related to the document should have their name prefixed with their icon as documented in [Document Headers](#document-headers).

  - Example: `[:paperclip: Appendix](#paperclip-appendix)` [:paperclip: Appendix](#paperclip-appendix)
  - Example: `[:notebook: Notes](#notebook-notes)` [:notebook: Notes](#notebook-notes)
