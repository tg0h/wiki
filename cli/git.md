# git

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
