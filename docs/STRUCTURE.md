# :file_folder: Repository Structure

## :book: Table of Contents

- [:file_folder: Repository Structure](./#file_folder-repository-structure)
  - [:telescope: Overview](./#telescope-overview)
  - [:building_construction: Structure](./#building_construction-structure)
    - [:building_construction: Root Level](./#building_construction-root-level)
    - [:building_construction: `.chimera-lab/` Directory](./#building_construction-chimera-lab-directory)
    - [:building_construction: `.github/` Directory](./#building_construction-github-directory)
    - [:building_construction: `docs/` Directory](./#building_construction-docs-directory)
    - [:building_construction: Documentation Hierarchy](./#building_construction-documentation-hierarchy)
    - [:building_construction: Configuration Hierarchy](./#building_construction-configuration-hierarchy)
    - [:building_construction: Documentation Patterns & Conventions](./#building_construction-documentation-patterns-conventions)
      - [:building_construction: Knowledge Files Frontmatter](./#building_construction-knowledge-files-frontmatter)
      - [:building_construction: Canonical Knowledge Inventory](./#building_construction-canonical-knowledge-inventory)
      - [:building_construction: Semantic Header Vocabulary](./#building_construction-semantic-header-vocabulary)
      - [:building_construction: Render Tag Mappings](./#building_construction-render-tag-mappings)
      - [:building_construction: CMR Directive Catalog](./#building_construction-cmr-directive-catalog)
      - [:building_construction: Layer Separation Rules](./#building_construction-layer-separation-rules)
      - [:building_construction: GitHub Automation Structure](./#building_construction-github-automation-structure)
  - [:books: References](./#books-references)

## :telescope: Overview

<!-- <llm prompt="Structure.Overview" applied> -->

This repository is organized as a template collection for documentation topics. The root contains shared project metadata and contributor guidance such as `README.md`, `DEVELOPMENT.md`, `CONTRIBUTING.md`, `CHANGELOG.md`, `SECURITY.md`, `CODE_OF_CONDUCT.md`, `LICENSE`, and `Makefile`, while `docs/` holds supporting reference material and diagrams.

The main content lives in `*.template/` directories. Each template directory represents a documentation scope or delivery target, including general structures such as `overview.template/`, `topic.template/`, `project.template/`, `repository.template/`, `package.template/`, `org.template/`, and `scaffold.template/`, alongside implementation-oriented variants such as `app.template/`, `typescript_app.template/`, `laravel_app.template/`, `docker_scaffold.template/`, and `laravel_docker_scaffold.template/`. This keeps each template self-contained while preserving a consistent repository-wide layout.

<!-- </llm> -->

## :building_construction: Structure

### :building_construction: Root Level

```text
repository/
├── .chimera-lab/           # Repository metadata and configuration
├── .github/                # GitHub-specific files
├── docs/                   # Additional documentation (project-specific)
├── src/                    # Source code (if applicable)
├── tests/                  # Test files (if applicable)
├── README.md               # Main documentation
├── CHANGELOG.md            # Version history
├── CONTRIBUTING.md         # Contribution guidelines
├── CODE_OF_CONDUCT.md      # Community guidelines
├── SECURITY.md             # Security policy
└── LICENSE                 # License terms
```

### :building_construction: `.chimera-lab/` Directory

Configuration and metadata:

```text
.chimera-lab/
├── meta.json               # Repository metadata
│   ├── description         # Short description
│   ├── tags                # Category tags
│   ├── template            # Template name
│   └── remote_template     # Template repository info
└── settings.json           # Configuration
    ├── custom_variables    # Template variables
    └── validation_rules    # Documentation rules
```

### :building_construction: `.github/` Directory

GitHub workflows and automation:

```text
.github/
├── agents/                 # AI agent definitions
│   ├── *.agent.md          # Agent files
│   └── README.md           # Agents overview
├── prompts/                # Prompt templates
│   └── *.prompt.md         # Prompt files
└── workflows/              # GitHub Actions (if applicable)
    └── *.yml               # Workflow definitions
```

### :building_construction: `docs/` Directory

Documentation and knowledge base:

```text
docs/
├── ARCHITECTURE.md         # Technical architecture
├── ORGANIZATION.md         # Organization structure
├── ROADMAP.md              # Project roadmap
├── STRUCTURE.md            # Repository structure (this file)
├── diagrams/               # Diagrams and visual assets
└── knowledge/              # Knowledge base
    └── *.knowledge.md      # Knowledge files
```

### :building_construction: Documentation Hierarchy

```text
README.md (entry point)
├── docs/knowledge/*.knowledge.md (concepts)
└── docs/*.md (detailed guides)
    ├── ARCHITECTURE.md
    ├── ORGANIZATION.md
    ├── ROADMAP.md
    └── STRUCTURE.md
```

### :building_construction: Configuration Hierarchy

```text
.chimera-lab/meta.json (metadata)
└── .chimera-lab/settings.json (configuration)
    └── custom_variables (template overrides)
```

### :building_construction: Documentation Patterns & Conventions

#### :building_construction: Knowledge Files Frontmatter

All knowledge files (`.knowledge.md`) require YAML frontmatter at the top:

```yaml
---
name: {filename-stem}
description: {one-line-summary}
---
```

**Example**:
```yaml
---
name: cmr
description: CMR CLI tool reference and command patterns
---
```

#### :building_construction: Canonical Knowledge Inventory

The repository defines 9 required knowledge files covering core domains:

| File | Description | Max Lines | Purpose |
|------|-------------|-----------|---------|
| `automation.knowledge.md` | CI/CD workflows and automation | 250 | Deployment, versioning, release patterns |
| `cmr.knowledge.md` | CMR CLI reference and commands | 250 | Complete command reference (most detailed) |
| `deployment.knowledge.md` | Release and environment management | 250 | Versioning, environments, verification |
| `operating.knowledge.md` | Git operations and workflows | 250 | Git commands, workflow execution, repository context |
| `planning.knowledge.md` | Task decomposition and milestones | 250 | Execution order, issue analysis, planning |
| `repository.knowledge.md` | Repository structure and templates | 250 | Structure conventions, naming patterns, metadata |
| `researching.knowledge.md` | Context discovery and analysis | 250 | Codebase exploration, issue analysis, discovery |
| `reviewing.knowledge.md` | Validation and quality gates | 250 | Code review, documentation review, context validation |
| `validating.knowledge.md` | Structure validation and header types | 250 | Header vocabulary, naming rules, structure validation |

**Constraint**: All knowledge files ≤250 lines per file to maintain LLM-first focus. See [:page_facing_up: validating.knowledge.md](knowledge/validating.knowledge.md) for validation rules.

#### :building_construction: Semantic Header Vocabulary

All headers must use emoji prefixes from the standardized vocabulary:

| Emoji | Category | Usage | Examples |
|-------|----------|-------|----------|
| `:file_folder:` | Structure | Main heading, file role, directory | "Repository Structure", "Files Directory" |
| `:book:` | Navigation | Table of contents | Always used for "Table Of Contents" |
| `:telescope:` | Discovery | Overview/summary | "Overview" sections |
| `:clipboard:` | Specification | Requirements, checklist | "Requirements", configuration items |
| `:inbox_tray:` | Input | Installation, setup | "Installation", input workflows |
| `:keyboard:` | Execution | Usage, commands, workflow | "Usage", step-by-step guides |
| `:books:` | Reference | Documentation links | Always for "References" section |
| `:scroll:` | Legal | License, terms, policies | License sections |
| `:building_construction:` | Architecture | Structure, design, hierarchy | STRUCTURE, ORGANIZATION sections |
| `:triangular_ruler:` | Technology | Tech stack, tools | "Technologies", implementation details |
| `:world_map:` | Navigation | Guides, workflows | Multi-step procedures, routing |
| `:toolbox:` | Tools | Utilities, CLI | CLI references, tool descriptions |
| `:warning:` | Alert | Warnings, cautions | Important notices, gotchas |
| `:wrench:` | Configuration | Settings, parameters | Configuration sections |
| `:compass:` | Direction | Steps, waypoints | Step-by-step guides |
| `:hammer_and_wrench:` | Remediation | Troubleshooting | Problem-solving, fixes |
| `:memo:` | Plan | To-Do lists, milestones | Tasks, planned work |
| `:notebook:` | Documentation | Notes, annotations | Remarks, observations |
| `:dart:` | Skills | Agent capabilities | Skill references, capabilities |

**Rule**: All typed headers must include emoji. See [:page_facing_up: validating.knowledge.md](knowledge/validating.knowledge.md) for complete typed header list.

#### :building_construction: Render Tag Mappings

Documentation placeholders for LLM-guided content generation:

**Patterns**:

- `<!-- <llm prompt="SectionName" applied> -->

Describe the purpose, scope, and expected usage of this part of the repository. Focus on the key context a contributor or reader needs to understand it quickly, including any important constraints, dependencies, and links to related templates, guides, or source files. Keep the content specific, actionable, and limited to information that helps someone navigate or maintain this repository effectively.

<!-- </llm> -->` for README sections such as `Overview` or `Usage`
- `<!-- <llm prompt="Namespace.Section" applied> -->

Use `Namespace.Section` for a stable, scoped section name that is easy to read, sort, and reuse across the repository.

- `Namespace` identifies the broader domain, component, or document family.
- `Section` identifies the specific topic inside that namespace.
- Prefer clear, reusable names such as `Repository.Overview`, `Project.Setup`, or `Topic.References`.
- Reuse an existing namespace when the content belongs to an established area; create a new one only when it introduces a distinct domain.
- Keep names concise, descriptive, and consistently formatted.

This convention improves discoverability, reduces naming collisions, and makes cross-document structure easier to maintain.

<!-- </llm> -->` for documentation pages such as `Architecture.Overview`

**Active mappings by file**:

```text
README.md:
  llm<Overview>
  llm<Requirements>
  llm<Installation>
  llm<Usage>

STRUCTURE.md:
  llm<Structure.Overview>

ORGANIZATION.md:
  llm<Organization.Overview>

ROADMAP.md:
  llm<Roadmap.Overview>

ARCHITECTURE.md:
  llm<Architecture.Overview>
  llm<Architecture.Structure>
  llm<Architecture.Technologies>
```

**Validation**: Run `cmr docs check --tags` to validate all render directives map to active header prompts.

**Resolution policy**:

- Default location: repository `.chimera-lab/settings.json` under `llm.headerPrompts`
- Optional shared location: organization-level settings when the same prompt set is reused across multiple templates or repositories
- Override rule: keep repository-specific overrides minimal and only for genuinely divergent wording or structure

#### :building_construction: CMR Directive Catalog

CMR directives are reserved for generated repository and organization inventories. They should be used only when the content is expected to be refreshed by `cmr docs render`.

**Syntax**:

```html
<!-- <cmr cmd="group.command[key=value,...]"> --><!-- </cmr> -->
<!-- <cmr cmd="group.command" applied> -->...content...<!-- </cmr> -->
```

**Supported baseline directives in current workspace**:

```text
project.list
org.list
org.list[suffix=app]
org.list[suffix=scaffold]
org.topic
org.submodules
org.types
org.inheritance
org.stats
```

**Usage by repository type**:

- `topic.template`: prefer `org.submodules` in README-level overview pages listing contained subrepositories.
- `project.template`: prefer `project.list` when a repository acts as an aggregate of project entries.
- `org.template`: allow `org.list[...]`, `org.topic`, `org.types`, `org.inheritance`, and `org.stats` for organization-wide inventories.
- `app.template`, `package.template`, `scaffold.template`: avoid CMR directives by default unless the repository is explicitly acting as an index or generated registry.

**Rules**:

- Use LLM directives for narrative content.
- Use CMR directives only for generated tables, lists, or aggregate inventories.
- Do not invent new directives in templates without first verifying resolver support in CMR knowledge and implementation.
- Preserve `;applied` only for rendered output; source templates should keep the unresolved directive form.

#### :building_construction: Layer Separation Rules

Documentation organization follows strict layer boundaries to maintain clarity and reusability:

```text
prompts (frontmatter: agent, skills)
├── agents (`:dart: Skills` section)
├── skills (`:books: References` to knowledge)
├── knowledge (`:books: References` to docs)
└── docs (`:books: References` to external)
```

**Allowed references**:
| From | To | Via | Allowed |
|------|-----|------|---------|
| Knowledge | docs/ | `:books: References` | ✅ YES |
| Knowledge | sibling knowledge | `:books: References` | ✅ YES |
| Skill | Knowledge | `:books: References` in SKILL.md | ✅ YES |
| Agent | Skill | `:dart: Skills` section | ✅ YES |
| Prompt | Agent | Frontmatter `agent:` | ✅ YES |
| Prompt | Skill | Content references | ✅ YES |

**Forbidden references**:
| From | To | Reason |
|------|-----|--------|
| Agent | Agent | No horizontal coupling |
| Skill | Skill | No horizontal coupling |
| Prompt | Prompt | No horizontal coupling |
| Knowledge | Agent | Breaks layer boundary |
| Docs | Knowledge | One-way flow only |

#### :building_construction: GitHub Automation Structure

`.github/` reserved for GitHub-specific automation **only**. No documentation content in `.github/docs/` or `.github/`.

**Directories**:
- `agents/`: AI agent definitions (`*.agent.md` with frontmatter)
- `prompts/`: Prompt templates (`*.prompt.md` with frontmatter)
- `skills/`: Agent skills (referenced by agents, not duplicated here)
- `workflows/`: GitHub Actions (`.yml` files)
- `ISSUE_TEMPLATE/`: GitHub issue templates

**Constraint**: All agents/prompts/skills reference documentation via knowledge, never vice versa.

## :books: References

- [:page_facing_up: ORGANIZATION.md](ORGANIZATION.md)
- [:page_facing_up: ../../README.md](../../README.md)
- [:page_facing_up: knowledge/validating.knowledge.md](knowledge/validating.knowledge.md)
- [:page_facing_up: knowledge/reviewing.knowledge.md](knowledge/reviewing.knowledge.md)
