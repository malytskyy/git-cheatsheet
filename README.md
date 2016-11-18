# Git Cheatsheet
## Getting information
Show short status  
 ``` 
 git status -s 
 ```
View outstanding commits for upstream
``` 
git diff --cached [path] 
```
Show outstanding commits for upstream
```
git log --stat @{u}..
```
Go grab all of the stuff from the upstream, and then compare my current branch against the upstream master branchgit branchShow all branches
```
git fetch && git log ..@{u}
```
List only conflicted files 
```
git diff --name-only --diff-filter=U
```
List all untracked files in text-processing friendly mode
```
git ls-files --others --exclude-standard
```
## Make changes
Commit with message that will be provided via editor 
```
git commit
```
Template loaded up with the last commit message
```
git commit -c HEAD
```
Add all changed files to staging area
```
git add .
```
Add all changes and commit. Message still will be entered
```
git commit –a
```
Creates .rej files when can't automatically detect how to apply a patch 
```
git apply --reject --whitespace=fix [patchfile]
```
## Undo changes
To get rid of untracked files and directories in your working copy
```
git clean -fd
```
Unstages file, but reserves changes
```
git reset [file]
```
The working tree and staging area are reset to the tip of the current branch or HEAD.
```
git reset --hard HEAD
```
Undo changes locally to modified unstaged file [file]
```
git checkout -- [file]
```
Undo a commit
```
git reset --soft HEAD~1
```

## Branches
Get newest state from upstream without changing any local data  
```
git fetch
``` 
Do a ```git fetch && git merge``` on current branch
```
git pull
```
Publish current branch
```
git push
```
Switch to branch [branch]
```
git checkout [branch]
```
Delete branch [branch]
```
git branch –d [branch]
```
Create a new branch [branch] and switch to it
```
git checkout –b [branch]
```
Integrate branch [branch] into current branch
```
git rebase [branch]
```
Create public remote branch from current. Call this to set default:```$ git config --global push.default current```
```
git push -u
```
Delete remote branch [branch]
```
git push origin --delete [branch]
```



