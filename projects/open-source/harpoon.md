# harpoon

- refresh projects before update
- autocmd stores offset when closing buffer

## config

## data

```yaml
projects:
  projectPathAsKey:
    mark:
      marks:
        - col: 16
          row: 254
          filename: "rel/path/to/file"
    term:
      cmds:
        - "test cmd 1"
        - "test cmd 2"
  anotherProjectPathAsKey: ...
  yetAnotherProjectPathAsKey: ...
global_settings:
  mark_branch: false
  save_on_toggle: false
  excluded_filetypes:
    - "harpoon"
  enter_on_sendcmd: true
  save_on_change: true
  tmux_autoclose_windows: false
```

if mark_branch is true, the git branch is appended to the project path key

```yaml
projects:
    "/Users/tim/src/playground/git/play-main"
      ...
    "/Users/tim/src/playground/git/play-test2"
      ...
```

## features

- branch key

## code

- expand
  expand_dir reads directories and expands their path using plenary. the directory may contain ~ or $HOME and plenary will expand it. the function also deletes the unexpanded key. (replaces the key)
- merge

## init.lua

- get_mark_config
  - gets the current marks of the current project

## utils

- normalize_path

  - normalize relative to root of project

- ensure correct config
  - get mark config key
