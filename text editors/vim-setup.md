---
title: vim setup
---

# vim setup

- runtimepath
- lua folder
- init.vim

vim runtime folder is in homebrew cellar - /opt/homebrew/Cellar/neovim/0.6.0/share/nvim/runtime

## lsp

tsserver - https://github.com/typescript-language-server/typescript-language-server
jsconfig.json - https://code.visualstudio.com/docs/languages/jsconfig

``` vim
:LspInfo
:LspStart <config_name>
:LspStop <client id>
```

set up nvim-cmp after setting up lsp to set up auto completion (as opposed to manual completion via nvim's omnifunc)


## lua

```lua
lua <lua code> 
```

runs 1 line of lua script directly in init.vim

### requires

see lua-package-path. 

``` lua
lua require('basic')
``` 

- neovim searches runtimepath for a lua folder and searches for basic.lua. 
- neovim also searches for a basic folder with init.lua.

Neovim runs last script that meets condition.


### functions

Before you say anything, yes, all of that is valid lua. If a function only recieves a single argument, and that argument is a string or a table, you can omit the parenthesis.

