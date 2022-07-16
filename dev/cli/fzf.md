# fzf

##preview

```zsh
# --highlight-line
#   this is a bat feature
# --preview window ~8,+{1}-5
#   this is a fzf feature
#   ~8 - show first 8 lines (header)
#   +{1} - fzf delimits the input piped in to it and provides access via index variables {n}.
#   the default delimiter fzf uses is space but can be specified via --delimiter <delimiter>
#   pass the first index variable from bat (which is the line number)
#   the number is signed, you can show eg the +n row or the -n row (the nth row from the bottom)
#   -5 subtract 5 rows (go up 5 rows) so that you don't show the highlighted line as the first line
#   since you want to provide context by showing the rows above the highlighted line

bat --style=numbers --color always $configFile | fzf --preview 'bat --style=numbers --color=always '"$configFile"' --highlight-line {1}' --preview-window ~8,+{1}-5
```

## actions

- change multiple actions with +
  - edit file, then abort to exit fzf

## presentation

1. demo
2. search file dir history

- apply filters
- preview - file vs dir

3. text search
4. app integration - get something and pass to app

- cw
- pass otp

5. search command output

- git
- candy cognito list users
- gr function

6. apply commands to entries

- go to dir, delete, edit file, copy text

7. search text file content

- search package.json

8. function, alias
9. dir switcher

- config
  - nvim config
- aliases
  - global alias for fzf
- tmp folder
- downloads folder
- eg notes

how long did this take?
