Setup
Run source setup.sh (or .\setup.ps1 in PowerShell)
Task
Reorder the history such that it actually makes sense - add the files in the order that matches their name.

Use git log --oneline --graph to view the commits
Also try git reflog to view the commits. git reflog defaults to git reflog show and this is an alias for git log -g --abbrev-commit --pretty=oneline
Use git rebase -i <after-this-commit> to reorder the commits. There are commments in the file you edit that explain the commands available.
Use git log --oneline --graph to view the result
useful commands
git rebase -i <after-this-commit>
git log --oneline --graph
git reflog