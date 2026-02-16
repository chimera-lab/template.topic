---
name: research
description: Discover and gather project context, issues, and codebase information
---

# :file_folder: Research

## :book: Table of Contents

- [:file_folder: Research](./#file_folder-research)
  - [:book: Table of Contents](./#book-table-of-contents)
  - [:telescope: Overview](./#telescope-overview)
  - [:world_map: Guides](./#world_map-guides)
    - [:world_map: Context Discovery](./#world_map-context-discovery)
    - [:world_map: Issue Gathering](./#world_map-issue-gathering)
    - [:world_map: Codebase Exploration](./#world_map-codebase-exploration)
    - [:world_map: Output](./#world_map-output)
  - [:books: References](./#books-references)

## :telescope: Overview

Research gathers and validates context before action. Start from project metadata, expand through issues and documentation, then explore code. Prefer structured discovery over broad reading.

## :world_map: Guides

### :world_map: Context Discovery

- Read README and ORGANIZATION docs for project scope.
- Use `cmr docs list` to enumerate documentation by category.
- Use `cmr repo status` to check repository state.

### :world_map: Issue Gathering

- Use `gh issue list` to discover open issues.
- Use `gh issue view <number>` for full issue context.
- Use `cmr repo issues list` for organization-level views.
- Extract labels, milestones, and dependencies.

### :world_map: Codebase Exploration

- Search with semantic search or grep for relevant files.
- Read referenced documentation before modifying code.
- Validate assumptions against existing conventions.

### :world_map: Output

- Structured summary of findings.
- Relevant files and their purposes.
- Identified issues and context.

## :books: References

- [:page_facing_up: ../../../docs/knowledge/researching.knowledge.md](../../../docs/knowledge/researching.knowledge.md)
