# handygit
## Usefull day to day git - for when I cannot remember

### Easy merging
Merge code without doing the commit with review opportunity.

* ```git merge dev --no-ff --no-commit```
Once there is no conflicts, you can commit the merge or aborting with ```git merge --abort``` but it seems that the abort command will not remove newly created files. Files which will considered as untracked for the current branch.

### Delete a remote branch
```git push --delete (remote) (branch)``` like ```git push --delete origin dev```
