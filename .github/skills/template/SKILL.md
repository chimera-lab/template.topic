---
name: template
description: Structure and manage documentation templates and header hierarchies
---

# :file_folder: Template

## :book: Table of Contents

- [:file_folder: Template](./#file_folder-template)
  - [:book: Table of Contents](./#book-table-of-contents)
  - [:telescope: Overview](./#telescope-overview)
  - [:world_map: Guides](./#world_map-guides)
    - [:world_map: Structure Design](./#world_map-structure-design)
    - [:world_map: Template Inheritance](./#world_map-template-inheritance)
    - [:world_map: Validation](./#world_map-validation)
    - [:world_map: Output](./#world_map-output)
  - [:books: References](./#books-references)

## :telescope: Overview

Design and maintain documentation structure skeletons using semantic headers. Manage template inheritance hierarchies. Create only table of contents and headers — do not write content under headers.

## :world_map: Guides

### :world_map: Structure Design

- Create table of contents listings with semantic emoji headers.
- Use `cmr docs headers list-typed` to understand available header types.
- Plan documentation hierarchy and organization.
- Maintain consistency across the organization.

### :world_map: Template Inheritance

- Templates inherit from parent: child → parent → `repository.template`.
- Modify at the highest appropriate level to avoid duplication.
- Use `cmr repo template validate` to check synchronization.
- Use `cmr repo template update` to apply upstream changes.
- Propagate changes: `cp` from parent to child templates.

### :world_map: Validation

- Run `cmr docs validate` to check all documentation.
- Check that all files follow naming conventions.

### :world_map: Output

- Header skeleton with table of contents.
- Updated template files.
- Validation results.

## :books: References

- [:page_facing_up: ../../../docs/knowledge/validating.knowledge.md](../../../docs/knowledge/validating.knowledge.md)
