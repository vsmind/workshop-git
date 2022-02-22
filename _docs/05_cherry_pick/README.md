# Cherry-pick

- Checkout remote branch `06-cherry-pick`

```shell
git checkout -b 06-cherry-pick origin/06-cherry-pick
```

- get commit from another branch to our with help of `git cherry-pick`
- check git log on target branch

```shell
git log --pretty=oneline -n 6 origin/07-cherry-pick-source
```

- copy commit SHA for "cherry-pick basic" commit and use it in `git cherry-pick` command:

```shell
git cherry-pick dddf3a4cc5504bb4b8ee213b57129dfb1f48b732
```

- check the current log and see that you have cherry-pick commit on top of log

```shell
git log --pretty=oneline -n 2
```

- copy commit SHA for "cherry-pick with edit" commit
- use `git cherry-pick -edit` command to get commit but change commit message:

```shell
git cherry-pick --edit c0b6e4f84eebcef41a5bafaf3684d9229894c2db 
```

> Default editor will be open where you can change the commit message

- check the current log and see that you have cherry-pick commit with the new message

```shell
git log --pretty=oneline -n 2
```

- copy commit SHA for "cherry-pick without commit" commit
- use `git cherry-pick --no-commit` command to move content of the target commit into the working directory:

```shell
git cherry-pick --no-commit f0e6abdae0cde91a8a6b1717471969fdfd5fb609
```

- check the current log and see that cherry-pick have not created a new commit in your branch

```shell
git log --pretty=oneline -n 2
```

- Use git status, you will se a new file created by cherry-pick

```shell
git status
```

## Navigation

[<<< git reset/revert](../04_reset_revert/README.md) |
[git rebase >>>](../06_rebase/README.md)


