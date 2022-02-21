# Git reset / git revert

## Git reset

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