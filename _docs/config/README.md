# Git config

## Basic configuration commands

- check git configuration:

```shell
git config -l
```

- setup username

```shell
git config --global user.name "Ola"
```

- setup email

```shell
git config --global user.email "ola.nordmann@cegal.com"
```

- Cache login credentials

```shell
git config --global credential.helper cache
```

## Useful tips

Git uses basic editor as a pager for git result, sometimes this can be unpractical, we can change this behavior and use `cat`
Use `cat` as pager for git command:

```shell
git config --global core.pager cat
```