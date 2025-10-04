                                # Important #

someone from your team made changes to your feature branch in github and merged the changes to main.
But you are working in your feature branch in local 
they told that the main branch is moved. now you need to pull the changes to your local main and feature branches.

Since your team uses squash and merge, here’s the clean fix to stop repeated conflicts:

Switch to the main branch locally.
>git checkout main
Fetch the latest remote updates but doesn’t merge or rebase them yet.
>git fetch origin
Get the latest commits from origin/main and merge them into your local main
>git pull origin main

Switch to your working feature branch.
>git checkout feature/<your-feature-name>
Fetch the latest remote updates but doesn’t merge or rebase them yet.
>git fetch origin
Reapply your local commits on top of the latest origin/dev (or origin/main)
>git rebase origin/dev
Stage all modified and resolved files (especially after conflicts).
>git add .
Continue the rebase after fixing conflicts.
>git rebase --continue
See the current state of your repo.
>git status
Show a concise commit history.
>git log --oneline