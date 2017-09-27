# handygit
## Usefull day to day git - for when I cannot remember

### Easy merging
Merge code without doing the commit with review opportunity.

* ```git merge dev --no-ff --no-commit```
Once there is no conflicts, you can commit the merge or aborting with ```git merge --abort``` but it seems that the abort command will not remove newly created files. Files which will considered as untracked for the current branch.

### Delete a remote branch
```git push --delete (remote) (branch)``` like ```git push --delete origin dev```

### To stop tracking a file you need to remove it from the index. This can be achieved with this command.
```git rm --cached <file>```

### To assume that a file has not modified
```git update-index --assume-unchanged```

### CRLF & LF

Git can handle this by auto-converting CRLF line endings into LF when you add a file to the index, and vice versa when it checks out code onto your filesystem. You can turn on this functionality with the core.autocrlf setting. 

If you’re on a Windows machine, set it to true – this converts LF endings into CRLF when you check out code:
* git config --global core.autocrlf true

If you’re on a Linux or Mac system that uses LF line endings, then you don’t want Git to automatically convert them when you check out files; however, if a file with CRLF endings accidentally gets introduced, then you may want Git to fix it. You can tell Git to convert CRLF to LF on commit but not the other way around by setting core.autocrlf to input:
* git config --global core.autocrlf input

If you’re a Windows programmer doing a Windows-only project, then you can turn off this functionality, recording the carriage returns in the repository by setting the config value to false:
* git config --global core.autocrlf false
