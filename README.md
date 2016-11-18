# Git Cheatsheet
## Overview
- [Getting information](#getting-information)
- [Make changes](#make-changes)
- [Undo changes](#undo-changes)
- [Branches](#branches)

## Getting information
|Command|Description|
|---|---|
|``` git status -s ```|Show short status|
|``` git diff --cached [path] ```|View outstanding commits for upstream|
|```git log --stat @{u}..```|Show outstanding commits for upstream|
|```git fetch && git log ..@{u}```|Go grab all of the stuff from the upstream, and then compare my current branch against the upstream master branch|
|```git branch```|Show all branches|
|```git diff --name-only --diff-filter=U```|List only conflicted files |
|```git ls-files --others --exclude-standard```|List all untracked files in text-processing friendly mode|

## Make changes
|Command|Description|
|---|---|
|```git commit```|Commit with message that will be provided via editor|
|```git commit -c HEAD```|Template loaded up with the last commit message|
|```git add .```|Add all changed files to staging area|
|```git commit –a```|Add all changes and commit. Message still will be entered|
|```git apply --reject --whitespace=fix [patchfile]```|Creates `.rej` files when can't automatically detect how to apply a patch|

## Undo changes
|Command|Description|
|---|---|
|```git clean -fd```|To get rid of untracked files and directories in your working copy|
|```git reset [file]```|Unstages file, but reserves changes|
|```git reset --hard HEAD```|The working tree and staging area are reset to the tip of the current branch or `HEAD`|
|```git checkout -- [file]```|Undo changes locally to modified unstaged file `[file]`|
|```git reset --soft HEAD~1```|Undo a commit|


## Branches
|Command|Description|
|---|---|
|```git fetch``` |Get newest state from upstream without changing any local data|
|```git pull```|Do a ```git fetch && git merge``` on current branch|
|```git push```|Publish current branch|
|```git checkout [branch]```|Switch to branch `[branch]`|
|```git branch –d [branch]```|Delete branch `[branch]`|
|```git checkout –b [branch]```|Create a new branch `[branch]` and switch to it|
|```git rebase [branch]```|Integrate branch `[branch]`  into current branch|
|```git push -u```|Create public remote branch from current. Call this to set default:```$ git config --global push.default current```|
|```git push origin --delete [branch]```|Delete remote branch `[branch]`|




