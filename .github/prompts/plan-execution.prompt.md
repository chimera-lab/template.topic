---
name: plan-execution
agent: project-manager
description: Create executable task lists from GitHub issues
---

# :file_folder: Plan Execution

## :book: Table of Contents

- [:file\_folder: Plan Execution](./#file_folder-plan-execution)
  - [:book: Table of Contents](./#book-table-of-contents)
  - [:world\_map: Guides](./#world_map-guides)
    - [:compass: Issue Analysis](./#compass-issue-analysis)
      - [:compass: Fetch Issues](./#compass-fetch-issues)
      - [:compass: Analyze Each](./#compass-analyze-each)
      - [:compass: Validate Decomposition](./#compass-validate-decomposition)
    - [:compass: Task Planning](./#compass-task-planning)
      - [:compass: Create Task List](./#compass-create-task-list)
      - [:compass: Order Tasks](./#compass-order-tasks)
    - [:compass: Output](./#compass-output)

## :world_map: Guides

### :compass: Issue Analysis

#### :compass: Fetch Issues

- Single: `gh issue view <number>`
- Milestone: `gh issue list --milestone "v0.x.0"`
- Extract: title, body, labels, milestone

#### :compass: Analyze Each

- Clear acceptance criteria?
- Technical requirements specified?
- Module/component identified?
- Dependencies documented?

#### :compass: Validate Decomposition

- Single focused objective?
- Actionable steps clear?
- No ambiguous requirements?

### :compass: Task Planning

#### :compass: Create Task List

- Use `manage_todo_list` tool
- Format: `#<issue>: <action> - @<agent>`
- Include: issue, module, goal, steps, dependencies

#### :compass: Order Tasks

- Foundation first: models, utilities
- Implementation: commands, modules
- Validation: tests, error handling
- Documentation: knowledge, docs
- Integration: workflows, releases

### :compass: Output

- Complete task list with dependencies
- Execution order
- Success criteria
