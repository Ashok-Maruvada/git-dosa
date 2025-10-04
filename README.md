                                # Important #

someone from your team made changes to your feature branch in github and merged the changes to main.
But you are working in your feature branch in local 
they told that the main branch is moved. now you need to pull the changes to your local main and feature branches.

first switch to main branch >git checkout main
pull the changes from remote >git pull origin main
then switch to your feature branch >git checkout feature
to make feature branch up to date with main >git rebase main (if team using rebase model)
