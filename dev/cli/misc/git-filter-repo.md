# git filter repo

- https://github.com/newren/git-filter-repo
- https://htmlpreview.github.io/?https://github.com/newren/git-filter-repo/blob/docs/html/git-filter-repo.html

```bash
# remove .DS_STORE files in git repo
git filter-repo --invert-paths --path '.DS_Store' --use-base-name
```
