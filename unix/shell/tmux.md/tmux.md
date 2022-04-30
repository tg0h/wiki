# tmux

## unique ids

the internal id of the session, window or pane remains unchanged and is different from the numbers when in tree mode (normally activated with the prefix s or prefix w commands), which merely show the ordinal numbers of the item

```tmux
tmux list-windows -F '${#window-id}'
```

## select-pane

merely makes the pane active in its window, does not go to the pane if the pane belongs in another session. eg if `tmux select pane -t ''$1:@2.%3'`. Instead, use `tmux switch-client`

```zsh
# select next tmux pane
tmux select-pane -t +
```

```zsh
# select tmux pane below
tmux select-pane -t {down-of}
```

```zsh
# select tmux pane with id 3
tmux select-pane -t 3
```
