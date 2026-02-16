---
name: update-team
agent: prompt-engineer
description: Update architecture diagram with agents, prompts, and knowledge
---

# :file_folder: Update Team

## :book: Table of Contents

- [:file\_folder: Update Team](./#file_folder-update-team)
  - [:book: Table of Contents](./#book-table-of-contents)
  - [:world\_map: Guides](./#world_map-guides)
    - [:compass: Resources Discovery](./#compass-resources-discovery)
    - [:compass: Read Content](./#compass-read-content)
      - [:compass: Process Agents](./#compass-process-agents)
      - [:compass: Process Prompts](./#compass-process-prompts)
      - [:compass: Process Knowledge](./#compass-process-knowledge)
    - [:compass: Update Diagram](./#compass-update-diagram)
      - [:compass: Update PlantUML](./#compass-update-plantuml)
      - [:compass: Validate](./#compass-validate)

## :world_map: Guides

### :compass: Resources Discovery

- `cmr docs list`

### :compass: Read Content

#### :compass: Process Agents

- Read each agent file
- Extract name, description, role and references

#### :compass: Process Prompts

- Read each prompt
- Identify target agent
- Note relationships

#### :compass: Process Knowledge

- Read knowledge files
- Document purpose
- Map references

### :compass: Update Diagram

#### :compass: Update PlantUML

- Update `.github/copilot-team-components.plantuml`
- Add actual agents, prompts, knowledge
- Update relationships
- Maintain valid PlantUML syntax

#### :compass: Validate

- All agents represented
- All prompts shown
- All knowledge files included
- Relationships correct
- Syntax valid
