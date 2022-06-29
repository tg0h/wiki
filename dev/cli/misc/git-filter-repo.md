# git filter repo

- https://github.com/newren/git-filter-repo
- https://htmlpreview.github.io/?https://github.com/newren/git-filter-repo/blob/docs/html/git-filter-repo.html

```bash
# remove .DS_STORE files in git repo
git filter-repo --invert-paths --path '.DS_Store' --use-base-name

# remove folder from git repo
git filter-repo --invert-paths --path 'lib/zsh/candy'
```

```bash
# in expressions.txt enter strings you want to replace with ***REMOVED***
git filter-repo --replace-text expressions.txt

```
