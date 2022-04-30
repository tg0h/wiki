# worktrees

- https://levelup.gitconnected.com/git-worktrees-the-best-git-feature-youve-never-heard-of-9cd21df67baf

```bash
md worktree
git clone --bare git@github.com:tg0h/worktree.git .git
gwl
gwa main
gwa feat1
gwr feat1
```

GIT_DIR
GIT_WORKTREE can be env vars

```bash
# https://git-scm.com/docs/git-rev-parse

git rev-parse --is-inside-work-tree

git rev-parse --absolute-git-dir
# git rev-parse --git-dir vs --absolute-git-dir
# Show $GIT_DIR if defined. Otherwise show the path to the .git directory. The path shown, when relative, is relative to the current working directory.
# points to the bare git repo dir or the worktree dir

git rev-parse --show-toplevel
# Show the (by default, absolute) path of the top-level directory of the working tree. If there is no working tree, report an error

git rev-parse --is-bare-repository
```

## init.lua

- first check if inside worktree
- then find the git directory with git rev parse absolute git dir
