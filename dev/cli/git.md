# git

I just found out this cool thing about git.
## tactics

- using git commits just for console.log statements and then quickly dropping them

## moving around

```bash
# move main branch backwards by 3 commits
git branch -f main HEAD~3
```

## rebase

```bash
# put another ref on top of base ref
git rebase <base ref> (@) # (current ref is implied)
```

```bash
# put another ref on top of base ref
git rebase <base ref> <another ref>
```

```bash
# if main is behind feat1 to 'fast forward main'
git rebase feat1 main
```

## git push

colon refspec

```bash
# source can be foo~1
# destation does not need to exist in origin, git will create destination
# git push origin main:newBranch
git push origin <source>:<destination>
git push <remote> <place>
git push

```

## git diff

```bash
# search for strings that begin with capital letter and word boundary
git log --name-status main.. | grep -E '^[A-Z]\b'
```
