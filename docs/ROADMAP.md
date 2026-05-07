# :file_folder: Roadmap

## :book: Table of Contents

- [:file_folder: Roadmap](./#file_folder-roadmap)
  - [:telescope: Overview](./#telescope-overview)
  - [:memo: To-Do List](./#memo-to-do-list)
  - [:books: References](./#books-references)

## :telescope: Overview

<!-- <llm prompt="Roadmap.Overview" applied> -->

This roadmap focuses on keeping the template repository coherent, maintainable, and easy to extend. Priorities center on tightening documentation coverage, aligning placeholder automation with real project workflows, and improving the consistency of the template family managed from this workspace.

<!-- </llm> -->

## :memo: To-Do List

<!-- <llm prompt="Roadmap.ToDoList" applied> -->

1. Replace remaining placeholder sections in root and submodule documentation with repository-specific guidance.
2. Specialize the root `Makefile` targets that are still stubs (`install`, `test`, `lint`, `format`, `build`, and `docs`) where concrete behavior is required.
3. Bring `.github/workflows/ci.yml` in line with the documented local workflow so CI checks reflect actual repository expectations.
4. Continue refining CMR-based validation and rendering flows to reduce manual documentation upkeep.
5. Review template submodule versions regularly and apply upstream template updates in a controlled way.
6. Expand contributor-facing guidance where repository conventions are implicit today, especially around template synchronization and GitHub resource management.

<!-- </llm> -->

## :books: References

- [:page_facing_up: ../CHANGELOG.md](../CHANGELOG.md)
- [:page_facing_up: ../CONTRIBUTING.md](../CONTRIBUTING.md)
- [:page_facing_up: ../README.md](../README.md)
