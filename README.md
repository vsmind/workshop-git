# workshop-git

## Clone project to local filesystem

```shell
git clone __SSH__PATH__ 
```

## Commits

Create a new file in a project folder for example with `touch` command

```shell
touch test
```

Run `git status` 

```shell
touch test
```

![img.png](_docs/images/part_1.png)

Add created untracked file to git

```shell
git add test
```

Check operation with `git status`

![img.png](_docs/images/part_2.png)

Commit the file with `git commit` command

```shell
git commit
```

Default text edit will be open, you need to add a commit message and save the file to perform commit

![img.png](_docs/images/part_3.png)

You can check the `git status`

![img.png](_docs/images/part_4.png)

Push commit to the remote repository

```shell
git push
```

