---
name: fix-context
agent: prompt-engineer
description: Validate and improve agents, prompts, and knowledge files
---

# :file_folder: Fix Context

## :book: Table of Contents

- [:file\_folder: Fix Context](./#file_folder-fix-context)
  - [:book: Table of Contents](./#book-table-of-contents)
  - [:world\_map: Guides](./#world_map-guides)
    - [:compass: Information Gathering](./#compass-information-gathering)
      - [:compass: Discover Files](./#compass-discover-files)
    - [:compass: Validation](./#compass-validation)
      - [:compass: Check Names](./#compass-check-names)
      - [:compass: Check Content](./#compass-check-content)
      - [:compass: Check References](./#compass-check-references)
    - [:compass: Check Quality](./#compass-check-quality)
    - [:compass: Output](./#compass-output)

## :world_map: Guides

### :compass: Information Gathering

#### :compass: Discover Files

- List agents with `cmr docs {agents|prompts|knowledge} list`
- Document purposes and relationships

### :compass: Validation

#### :compass: Check Names

- Agents: `lowercase-with-hyphens.agent.md`
- Prompts: `lowercase-with-hyphens.prompt.md`
- Knowledge: `lowercase-with-hyphens.knowledge.md`

#### :compass: Check Content

- Automated content check with `cmr docs validate`

#### :compass: Check References

- Agents: Reference only knowledge files
- Prompts: Reference only knowledge files
- Knowledge: Reference knowledge and docs files
- No agent-to-agent or prompt-to-prompt references

### :compass: Check Quality

- Clear structure and headers
- Focused on development guidance
- References knowledge files correctly
- No duplication of knowledge content between docs and knowledge files
- Apply automated fixes with `cmr docs fix`
- Validate again with `cmr docs validate`

### :compass: Output

- List of changes made
- Deleted files
- Improved documentation
- Reference updates
