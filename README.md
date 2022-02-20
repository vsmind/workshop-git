# workshop-git

## Commit

Create a new file in a project folder for example with `touch` command

```shell
touch test
```

Run `git status` 

```shell
touch test
```

![img.png](_docs/images/part_1.png)

Stage created untracked file to git with `git add` command:

```shell
git add test
```

Check operation with `git status`

![img.png](_docs/images/part_2.png)

Save changes in repository with `git commit` command:

```shell
git commit
```

Default text edit will be open, you need to add a commit message and save the file to perform commit:

![img.png](_docs/images/part_3.png)

Use `git status` to check the operation result:

![img.png](_docs/images/part_4.png)

Push commit to the remote repository

```shell
git push
```

![img.png](_docs/images/part_5.png)

Add 2 new files to the project folder

```shell
touch test_file_1
touch test_file_2
```

Created files are not added to git, check it with `git status`

```shell
git status                                                                                                                                     
```

![img.png](_docs/images/part_6.png)

Add both files to git, this time we will add all files 

```shell
git add .
```

![img.png](_docs/images/part_7.png)

> We can use `git add --all` or `git add -A`

```
git commit -m "Added test files"
```

Both files committed 

![img.png](_docs/images/part_8.png)

Push files to remote repository

```shell
git push
```

### Commit without staging

Create files test files

```shell
touch file_no_stage_1
touch file_no_stage_2
touch file_no_stage_3
```

Try to run git commit without adding files to staging

```shell
git commit -m "Stage files"
```

![img.png](_docs/images/part_9.png)

Files was not committed

We can add all files and commit at once

```shell
git commit -a -m "Added no stage file"
```

Check that files was committed



### TO_DO

```shell
git commit --amend -m "new message"
```