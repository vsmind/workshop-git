# Git worktree

- Checkout remote branch `08-worktree`

```shell
git checkout -b 17-worktree origin/17-worktree
```

- Add some changes in worktree.txt in project folder

- Create a new worktree for `master` branch, use `git worktree` command

> Best practice for `git`, is to put worktree outside your main repository folder

```shell
git worktree add ../worktree/master
```

- Check existing worktrees

```shell
git worktree list
```

- Navigate to created worktree

```shell
cd ../worktree/master
```

- Create a new file in a project folder with `touch` command if you are running **Linux/Mac-OS**

```shell
touch worktreefile
```

- If you are using **Windows command prompt** you can create an empty file with `copy` command:

```powershell
copy NUL worktreefile
```

- If you are using **Windows powershell** you can create an empty file with `New-Item` command:

```powershell
New-Item -Path './worktreefile' -ItemType File
```

- Add files to git index, commit file and push it to the master branch:

```shell
git add .
git commit -m "Worktree fix"
git push
```

- Navigate back to you working directory

```shell
cd ../../workshop-git
```

- Remove created worktree from file system
> Git suggests to remove worktree entries after work is done

```shell
git worktree remove ../worktree/master
```

- Check changes you done in the `worktree.txt` are still there

```shell
git status
```

- Commit changes to branch

```shell
git commit -am "Worktree.txt changed"
```

- Merge `master branch` to you feature branch

```shell
git fetch
git merge origin/master
```

- Check file you added in master worktree are added to you current branch

## Navigation

[<<< git stash](../07_stash/README.md)
