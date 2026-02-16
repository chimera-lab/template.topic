---
name: fix-docs
agent: technical-writer
description: Validate and improve documentation files
---

# :file_folder: Fix Docs

## :book: Table of Contents

- [:file\_folder: Fix Docs](./#file_folder-fix-docs)
  - [:book: Table of Contents](./#book-table-of-contents)
  - [:world\_map: Guides](./#world_map-guides)
    - [:compass: Documentation Review](./#compass-documentation-review)
      - [:compass: Discover Files](./#compass-discover-files)
      - [:compass: Validate Content](./#compass-validate-content)
      - [:compass: Check Quality](./#compass-check-quality)
    - [:compass: Output](./#compass-output)

## :world_map: Guides

### :compass: Documentation Review

#### :compass: Discover Files

- List all documentation files using `cmr docs list`
- Identify: core, supporting, temporary
- Check documentation validation with `cmr docs validate`

#### :compass: Validate Content

- Core docs: architecture, workflows, guidelines
- Supporting docs: reference, examples
- Temporary: status reports (should delete)

#### :compass: Check Quality

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
