# telescope

## useful apis

```lua
local output = utils.get_os_command_output({"git", "worktree", "list"})
```

## vim api

- vim.tbl_extend
  - vim.tbl_extend("keep", table1, table2 ...) - keep leftmost table
  - vim.tbl_extend("force", table1, table2 ...) - keep rightmost table
- vim.F.if_nil
