# Branching

## Create a new branch

We are going to create and checkout branch from GitHub web interface first

### Create branch from GitHub

![img.png](images/branching_01.png)

- Press the branch selector
- Write a name `new-branch` for the new branch
- Press `Create branch: new-branch`
- Run `git fetch` to get list of changes from the remote

```shell
git fetch
```

- Check the list of remote branches with `git branch` command:

```shell
git branch -a
```

![img.png](images/branching_02.png)

You will see the list of your local and remote branches

- checkout created remote branch with `git checkout` command:

```shell
git checkout -b LOCAL_BRANCH_NAME origin/BRANCH_NAME
```

This command will do the following:
> - Pull changes from the remote
> - Creates a new local branch
> - Checkout this local branch
> - Pull changes from remote branch 

### Create branch locally and push to remote

- Create a new local branch with help of `git checkout`:

```shell
git checkout -b branch-from-local-pc
```

- Check that created branch exists only locally with `git branch -a`:

```shell
git branch -a
```

![img.png](images/branching_03.png)

- push branch to remote with `git push` the `HEAD` shortcut allows us to push the branch to remote with the same name

```shell
git push -u origin HEAD 
```

> `git push -u origin branch-from-local-pc`

- run `git branch` command to confirm remote branch created:

![img_1.png](images/branching_04.png)

- this can be done in GitHub web interface:

![img.png](images/branching_05.png)

## Remove branch

- check the local branches first with `git branch`:

```shell
git branch
```

![img.png](images/branching_06.png)

- remove branch locally with `git branch` command:

```shell
git branch -d branch-from-local-pc
```

- you can confirm deletion with `git branch`:

![img.png](images/branching_07.png)

- at the same time branch still exists on remote

```shell
git branch -a
```

![img_1.png](images/branching_08.png)

- remove remote branch with `git push` command 

```shell
git push origin --delete branch-from-local-pc
```

- confirm deletion with `git branch`

```shell
git branch -a
```

![img_2.png](images/branching_09.png)

## Next step

[<<<workshop start](../00_workshop_start/README.md) |
[git commit >>>](../02_commit/README.md)
