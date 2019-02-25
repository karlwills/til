# Compile all commits from a branch into a single commit when merging branches using `git merge --squash`

Adding the `--squash` flag to a `git merge` command will allow you to squash all commits within the branch being merged into a single commit. 

This will also allow you to add your own commit message as part of the merge.

#### Example

```
git merge --squash feature/branchname
```


#### Further Reading

[Git - Merge --squash](https://git-scm.com/docs/git-merge#git-merge---squash)
