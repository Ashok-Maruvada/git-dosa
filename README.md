                                # Important #

someone from your team made changes to your feature branch in github and merged the changes to main.
But you are working in your feature branch in local 
they told that the main branch is moved. now you need to pull the changes to your local main and feature branches.

Since your team uses squash and merge, here’s the clean fix to stop repeated conflicts:

git fetch origin
git checkout main
git pull origin main

git checkout feature/<your-feature-name>
git reset --hard origin/main   # aligns your branch with main after squash merge


Then start fresh commits on this branch.

After a squash merge:
Always reset your local feature branch to main instead of rebasing it again.
Never rebase an old feature branch that’s already merged (even squashed) — it just repeats history and causes fake conflicts.
