# git-basics

## branches

**git branch** - show current branch and local branches

**git branch --all** - show all branches

**git branch <branch_name>** - create local branch without changing branches list

**git branch -d <branch-name>** - delete branch

**git checkout <branch_name>** - switch to specified branch if branch exists

**git checkout -b <branch_name>** - create and switch to created branch (short for git branch <branch_name> and git checkout <branch_name>)

## Pulling changes

**git pull** - merge changes from remote branch if upstream is set. (git pull under the hood is git fetch and git merge)

**git pull origin <remote_branch_name>** - helps when no upstream is set

**git pull --rebase origin <remote_branch_name>** - pull with rebase when required to pretiffy log. ( Without to much details what happens: rebase squashes the commits to one "patch" and then merges into target branch. Rebase is very much debatable stuff mostly because it requres to force push changes into branch and some other problems could arise)


## Git add

**git add <file_name>** - stage file to be tracked

**git add .** - stage all files

**git add <folder_path>** - stage all untracked files in folder
## Git commit

**git commit -m 'commit-message-here'** - create commit with message files should be staged to commit

**git commit --amend** - make changes to latest commit before they were pushed to remote. (change commit message, add files to commit etc.)

## Git reset

**git reset HEAD~<number_of_commits_to_reset>** - Revert lates commit. (git does soft reset by default keeping staged files unmodified: git reset --soft HEAD~1)

**git reset --hard HEAD~<number_of_commits>** - Revert <n> of latest commits. (also does git restore removing all changes made to the files)

## Git push

**git push**  - Send your changes to the tracked remote branch (in other word to upstream branch)

**git push -u origin <branch_name>** - Send your local changes to remote branch. (-u sets upstream)

**git push -f origin <branch_name>** - Send your local changes to remote branch overwriting the changes (used to change undesired commit after it was pushed)


## Git stash

**git stash** - Save your current changes in stash so you can pull or checkout.

**git stash list** - Shows list of all stashes

**git stash apply** - Applies last stashed files. git stash apply <stash_name> - use to apply specific stash name.

**git stash pop** - Applies and removes last stash

**git stash drop <stash_name>** - Remove stash. Without name remove last stash in stack.

**git stash clear** - Remove all stashes.

## Utility commands

**git status** - shows status of current branch. Unstaged files etc.

**git checkout <file_name>** - revert changes to unstaged file. (accepts folders, path, all)
