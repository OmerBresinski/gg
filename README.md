# ggw

Interactive git worktree session launcher. Pick or create a branch via fzf, then launch your preferred editor(s).

## Installation

```bash
npm install -g @omerbres/gg
```

## Requirements

- macOS (uses AppleScript for window management)
- [git](https://git-scm.com/)
- [fzf](https://github.com/junegunn/fzf)
- One or more of:
  - [Cursor](https://cursor.sh/)
  - [OpenCode](https://opencode.ai/)
  - [Claude Code](https://claude.ai/code)
- [Ghostty](https://ghostty.org/) (for terminal-based tools)

## Usage

Run `ggw` from any git repository:

```bash
ggw
```

1. **Select a branch** - Use fzf to pick an existing branch or type a new branch name
2. **Select editor(s)** - Use Tab to select one or more tools (Cursor, OpenCode, Claude), then Enter to launch

The script will:
- Reuse an existing worktree if the branch is already checked out
- Create a new worktree at `<repo>/.worktrees/<branch>` otherwise
- Launch your selected tools and tile windows automatically

## Configuration

Set `GG_BASE_BRANCH` to customize the base branch for new branches (defaults to detecting from `origin/HEAD`, then `main`, then `master`):

```bash
export GG_BASE_BRANCH=develop
```

## License

MIT
