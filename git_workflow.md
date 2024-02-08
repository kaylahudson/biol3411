# General Git Workflow 
Optional First Step: change the name and email associated with your Git commits. These are *not* the same as your GitHub username and email.<br>
`git config --global user.name <username>`<br>
`git config --global user.email <email>`<br>

1. `git pull`<br>
   Updates your local main branch with any changes in the remote repository.
2. `git branch <branch>`<br>
   Creates a new branch. You can make changes in this branch without affecting the main branch.
3. `git checkout <branch>`<br>
   Changes your current branch to the one you just created. You can now add/edit/remove files.
4. `git add <filename>` or `git add --all`<br>
   Add file(s) to the Staging Environment. Add files to the Staging Environment whenever you hit a milestone or complete a portion of work.
5. `git commit -m "<concise, informative commit message here>"`<br>
   Adds a commit of any staged files. The commit message should describe the changes made and why.
6. `git checkout main`<br>
    Changes back to the main branch in your local repository.
7. `git pull`<br>
    Updates your local main branch with any changes that have been pushed to the remote repository since you first pulled and starting working in your branch.
8. `git checkout <branch>`<br>
    `git rebase main`<br>
    Changes the base of <branch> to the most up-to-date main branch (that you just got through step 7).
9. Review of the proposed changes by anyone with access to the branch. Once approved, continue to next step.
10. `git checkout main`<br>
    `git merge <branch>`<br>
    Changes back to your local main branch. Merges the commits in `<branch>` to main branch (the current branch). This should be a fast forward merge.
11. `git push`<br>
    Pushes the changes you've made to the remote repository (aka GitHub). May fail if your local main branch is not up to date. If this occurs, reset your local main branch to the version prior to merging your new commits, then go back to step 6.
12. `git branch -d <branch>`<br>
    Deletes the branch that you created to make changes.
