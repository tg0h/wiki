# vim lua

https://github.com/nvim-telescope/telescope.nvim/issues/592#issuecomment-789023039

```lua 
M.my_fd = function(opts)
  opts = opts or {}
  opts.cwd = vim.fn.systemlist("git rev-parse --show-toplevel")[1]
  if vim.v.shell_error ~= 0 then
    -- if not git then active lsp client root
    -- will get the configured root directory of the first attached lsp. You will have problems if you are using multiple lsps 
    opts.cwd = vim.lsp.get_active_clients()[1].config.root_dir
  end
  require'telescope.builtin'.find_files(opts)
end
```
