---
name: code
description: Execute development tasks, commit changes, and verify completion
---

# :file_folder: Code

## :book: Table of Contents

- [:file_folder: Code](./#file_folder-code)
  - [:book: Table of Contents](./#book-table-of-contents)
  - [:telescope: Overview](./#telescope-overview)
  - [:world_map: Guides](./#world_map-guides)
    - [:world_map: Implementation](./#world_map-implementation)
    - [:world_map: Task Closure](./#world_map-task-closure)
    - [:world_map: Output](./#world_map-output)
  - [:books: References](./#books-references)

## :telescope: Overview

Execute coding tasks. Follow project conventions and keep changes surgical.

## :world_map: Guides

### :world_map: Implementation

- Understand the organization's standards, conventions, and best practices from knowledge files and existing code.
- Understand scope from issue or request before coding.
- Follow project language/framework conventions.
- Make focused, minimal changes aligned with the objective.
- Run tests and linters before committing.

### :world_map: Task Closure

- Check git status: `git status`.
- Stage changes: `git add .`.
- Conventional commit: `{type}: {description}` with `Closes #{number}`.
- Commit types: feat, fix, docs, style, refactor, test, chore.
- Push: `git push`.
- Verify: `gh issue view {number}`.
- Update progress: `manage_todo_list`.

### :world_map: Output

- Commit hash and message.
- Issue status (if applicable).

## :books: References

- [:page_facing_up: ../../../docs/knowledge/operating.knowledge.md](../../../docs/knowledge/operating.knowledge.md)
- [:page_facing_up: ../../../docs/knowledge/automation.knowledge.md](../../../docs/knowledge/automation.knowledge.md)
- [:page_facing_up: ../../../docs/knowledge/deployment.knowledge.md](../../../docs/knowledge/deployment.knowledge.md)
