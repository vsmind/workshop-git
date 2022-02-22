# Stash

- Create a new local branch with `git branch` command:

```shell
git branch stash-test
```

- Create a new file in directory

```shell
touch test-file-for-stash
```

- Add created file to the index

```shell
git add .
```

- Put current changes in your working directory into stash for later use with `git stash`

```shell
git stash
```

- Add one more file to your project directory

```shell
touch test-file-pop
```

- Add new file to git index:

```shell
git add test-file-pop
```

- Run `git stash save` command to add file to stash with predefined message

```
git stash save "stash to pop"
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
git stash drop 0
```

- We removed the first created stash from the list: 

```shell
git stash list
```

## Navigation

[<<< git rebase](../06_rebase/README.md) 


