# Git reset / git revert

## Git reset

### Soft reset

- Checkout remote branch `04-reset-practice`

```shell
git checkout -b 04-reset-practice origin/04-reset-practice
```

- edit file `reset_test` in project root
- commit file and check log

```shell
git commit -am "Changed test file"
```

- Check latest commit

```shell
git log --pretty=oneline -n 1 
```

- Reset the latest commit and keep changes

```shell
git reset --soft HEAD^
```

- Check `git log` to confirm that latest commit removed

```shell
git log --pretty=oneline -n 2
```

- If you open `reset_test` file, you will see that changes is there ready to be committed 

### Hard reset

- Now lets see on hard reset
- Add a new line to `reset_test` file and commit it:

```shell
git commit -am "reset_test one"
```

- Let repeat the previous step and add new line and commit:

```shell
git commit -am "reset_test two"
```

- And one more time:

```shell
git commit -am "reset_test three"
```

- Check the git log for the last 3 commits:

```shell
git log --pretty=oneline -n 3
```

- Lets run hard reset and remove 2 last commits:

```
git reset --hard HEAD~2
```

- Check the command result with `git log`:

```shell
git log --pretty=oneline -n 3
```

> you can see that commits are removed and file reverted to "reset_test one" commit


```shell
git reset HEAD filename
```

## Git revert

- Checkout remote branch `05-revert-practice`

```shell
git checkout -b 05-revert-practice origin/05-revert-practice
```

- Check git history for the last 5 commits

```shell
git log --pretty=oneline -n 5
```

- Revert the latest commit by using the head alias in `git revert` command:

```shell
git revert HEAD
```

- Check the git log, you will see new revert commit

```shell
git log --pretty=oneline -n 6
```

- We can revert specified commit by passing commit sha to the `git revert` command:

```shell
git revert COMMIT_ID
```

> Write revert message and save it to complete commit

- Check the git log, you will see new revert commit as a latest commit in git history:

```shell
git log --pretty=oneline -n 5
```

## Next steps

[<<< git merge](../03_merge/README.md) |
[git cherry-pick >>>](../05_cherry_pick/README.md)