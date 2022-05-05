# worktrees

- https://levelup.gitconnected.com/git-worktrees-the-best-git-feature-youve-never-heard-of-9cd21df67baf
- rabbit hole
  - vim/plenary strdisplaywidth - unicode, tabs zz

```bash
# get status from outside a worktree
# note that this is also affected by the GIT_DIR and GIT_WORKTREE env vars
git --git-dir /Users/tim/src/playground/git/worktrees/bare/.bare/worktrees/feat1 --work-tree ./feat1 status
```

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

## telescope extension

- create a telescope picker and call find
  - take in the opts that telescope passes in
  - in the picker, configure
    - prepare results
    - finder
    - sorter
    - attach mappings
      - define what selection does
      - define other mappings in i, n mode
- return require("telescope").register_extension

- results

```lua
results = {
  {
  branch: '[feat1]',
  path: '/Users/.../path/to/feat1',
  sha: 'abcd'
  },
  ...
}
```
