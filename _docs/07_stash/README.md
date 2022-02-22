# Stash

- Create a new local branch with `git branch` command:

```shell
git branch stash-test
```

- Create a new file in directory

```shell
touch test-file-for-stash
```

- Put current changes in your working directory into stash for later use with `git stash`

```shell
git stash
```

- Add one more file to your project directory

```shell
touch test-file-pop
```

- Run `git stash` command to add it to stash

```
git stash
```

- changes added to stash, we can check the list of currently created stashes with `git stash list` command:

```shell
git stash list
```

- apply stored stash content into working directory, and clear stash with `git stash pop`

```shell
git stash pop
```

> `test-file-pop` file is in working directory and the latest stash removed from stash list

- Delete a specific stash from all stashes with `git stash drop` command:

```shell
git stash drop
```

## Navigation

[<<< git rebase](../06_rebase/README.md) 


