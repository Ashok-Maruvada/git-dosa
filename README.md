                                # Important #

someone from your team made changes to your feature branch in github and merged the changes to main.
But you are working in your feature branch in local 
they told that the main branch is moved. now you need to pull the changes to your local main and feature branches.

Since your team uses squash and merge, here’s the clean fix to stop repeated conflicts:

git checkout main
git fetch origin
git pull origin main


git checkout feature/<your-feature-name>
git fetch origin
git rebase origin/dev
git add .
git rebase --continue
git status
git log --oneline