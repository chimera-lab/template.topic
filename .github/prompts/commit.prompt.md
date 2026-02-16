---
name: commit
agent: repository-manager
description: Execute git operations with SSH setup and submodule sync
---

# :file_folder: Git Commit

## :book: Table of Contents

- [:file\_folder: Git Commit](./#file_folder-git-commit)
  - [:book: Table of Contents](./#book-table-of-contents)
  - [:world\_map: Guides](./#world_map-guides)
    - [:compass: SSH Setup](./#compass-ssh-setup)
      - [:compass: Verify SSH Access](./#compass-verify-ssh-access)
      - [:compass: Setup SSH Key](./#compass-setup-ssh-key)
    - [:compass: Git Operations](./#compass-git-operations)
      - [:compass: Check Changes](./#compass-check-changes)
      - [:compass: Sync Remote](./#compass-sync-remote)
      - [:compass: Commit Changes](./#compass-commit-changes)
      - [:compass: Push](./#compass-push)
    - [:compass: Output](./#compass-output)

## :world_map: Guides

### :compass: SSH Setup

#### :compass: Verify SSH Access

- Test: `ssh -T git@github.com`
- If fails, setup SSH key

#### :compass: Setup SSH Key

- Eval agent: `eval "$(ssh-agent -s)"`
- Add key: `ssh-add ~/.ssh/*github.com`

### :compass: Git Operations

#### :compass: Check Changes

- `git status`
- `git submodule foreach --recursive 'git status'`
- Skip submodule ops if no changes

#### :compass: Sync Remote

- Fetch: `git fetch --prune`
- Pull: `git pull`
- Submodule: `git submodule foreach --recursive 'git fetch --prune && git pull'`

#### :compass: Commit Changes

- Group related changes logically
- Create commits: conventional format
- Each group gets its own commit

#### :compass: Push

- `git push`
- `git submodule foreach --recursive 'git push'`

### :compass: Output

- SSH confirmation
- Git status for all repos
- Commit hashes
- Push results
