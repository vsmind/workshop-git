# Git merge

- Checkout remote branch `02-merge-practice`

```shell
git checkout -b 02-merge-practice origin/02-merge-practice
```

> This branch has a simple "Hello world app"
> You can check content of the `main.go` file

- Checkout remote branch `02-merge-practice-target`

```shell
git checkout -b 03-merge-practice-target origin/03-merge-practice-target
```

> This branch has the same `main.go` file, but it prints something strange

- Merge `02-merge-practice` branch into `03-merge-practice-target` and apply code from `02-merge-practice` branch

```shell
git merge 02-merge-practice
```

Resolve conflicts

## Navigation

[<<< git commit](../02_commit/README.md) |
[git reset/revert >>>](../04_reset_revert/README.md)