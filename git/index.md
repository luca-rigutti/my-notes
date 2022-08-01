# GIT

Git is a version control system

## Commands list

`git init`

`git status`

`git add file`

`git commit -m "Message"`

`git stash`

`git checkout branch-name`

## Hooks

Hooks are script that are running in some event.

They come from `/git-core/templates/` files.

### Typology:

- pre
- post

### An usefull example

To prevent commit on a branch, you can setup the pre-commit hook to block based on the actual branch.

[The example](https://stackoverflow.com/questions/40462111/prevent-commits-in-master-branch)
