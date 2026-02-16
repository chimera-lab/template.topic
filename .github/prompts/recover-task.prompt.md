---
name: recover-task
agent: project-manager
description: Recover and restore todo list from previous context
---

# :file_folder: Recover Task

## :book: Table of Contents

- [:file\_folder: Recover Task](./#file_folder-recover-task)
  - [:book: Table of Contents](./#book-table-of-contents)
  - [:world\_map: Guides](./#world_map-guides)
    - [:compass: Recovery](./#compass-recovery)
      - [:compass: Analyze Context](./#compass-analyze-context)
      - [:compass: Validate Structure](./#compass-validate-structure)
      - [:compass: Restore](./#compass-restore)
    - [:compass: Report](./#compass-report)
      - [:compass: Confirm Recovery](./#compass-confirm-recovery)
    - [:compass: Recovery Sources](./#compass-recovery-sources)

## :world_map: Guides

### :compass: Recovery

#### :compass: Analyze Context

- Review conversation history
- Find previous todo list states
- Identify last valid configuration

#### :compass: Validate Structure

- Check id, title, description, status
- Ensure valid: not-started, in-progress, completed
- Identify incomplete or corrupted entries

#### :compass: Restore

- Use `manage_todo_list` with operation="write"
- Include all recovered todos with original status
- Preserve progress and context

### :compass: Report

#### :compass: Confirm Recovery

- List todos by status
- Completed count
- In-progress count
- Not-started count
- Flag items needing attention

### :compass: Recovery Sources

- Last `manage_todo_list` in conversation
- Explicit mentions in recent messages
- Inferred from completed work
