Git kata: Amending commits
When we are working, we make a lot of commits. Sometimes we just forget something obvious that we want to fix quickly.

git commit --amend allows us to do that - tinker with the last commit we made.

You can use git log -p or git show to inspect the contents of commits and file changes that were added to the commits.

Setup:
Run source setup.sh (or .\setup.ps1 in PowerShell)
The task
What does git status tell us?
What does git log -p tell us?
Stage the addition of bar.txt
Run git commit --amend
What happened? What does git log -p tell us?
What happens if you run git commit --amend again?
Useful commands
git add
git log --oneline --graph
git log -p
git show
git commit --amend