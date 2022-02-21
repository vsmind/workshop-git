# Git reset / git revert

## Git reset

- Checkout remote branch `04-reset-practice`

```shell
git checkout -b 04-reset-practice origin/04-reset-practice
```

- edit file `reset_test` in project root
- commit file and check log

```
git commit -am "Changed test file"
```

- Reset the latest commit and keep changes

```shell
git reset --soft HEAD^
```

```shell
git reset HEAD filename
```

## Git revert

- Revert the latest commit by using the head alias in `git revert` command:

```shell
git revert HEAD
```

- We can revert specified commit by passing commit sha to the `git revert` command:

```shell
git revert COMMIT_ID
```

## Next steps

[<<< git merge](../03_merge/README.md)
[git cherry-pick >>>](../05_cherry_pick/README.md)