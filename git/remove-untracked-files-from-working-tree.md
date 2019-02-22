# Remove untracked files from the working tree using `git clean`

`git clean` allows you to _recursively_ remove files and directories from the working tree that aren't under version control.

Generally, only untracked files are removed. However, you can remove ignored files too by passing in `-x` as a flag.

```
git clean -[flags]
```

**Tip**: Passing the `-n` flag will perform a dry-run and show you what will be removed before you perform the command.

#### Further reading
[Git Docs - Git Clean](https://git-scm.com/docs/git-clean)
