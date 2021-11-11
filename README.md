# Git CLI Workshop

Learn the basics of Git through an interactive workshop.

## Instructions

### Getting started

1. Fork this repository to your personal Github account
2. Download or `git clone` your personal fork to your local computer
3. Add this repo as `upstream`: `git remote add upstream <repo-url>`
4. Review the commit log: `git log`
5. Review the reference log: `git reflog`

### Fix spelling error

1. Create a new "fix" branch: `git checkout -b fix_name-spelling`
2. Find your name within the `team.txt` file and correct its spelling
3. Save your changes
4. Review your Git status: `git status`
5. "Stage" your change to be committed: `git add team.txt`
6. Review your Git status: `git status`
7. Commit your changes: `git commit`
8. Push your changes to `origin`: `git push origin fix_name-spelling`
9. PR your new branch to `upstream/main`

### Fix conflicts

1. Main has been updated, you can no longer merge your PR
2. Switch your local `main` branch: `git checkout main`
3. Pull updates from `upstream`: `git pull upstream main`
4. Switch back to your "fix" branch: `get checkout -`
5. Rebase your "fix" branch with `main`: `git rebase main`
6. Your `rebase` will halt and ask you to fix the conflict
7. Before you move on, familiarize yourself with the CLI instructions
8. Now, view the commit log: `git log` (Notice your commit is gone!)
9. Fix the conflicts manually (there are other ways, but let's keep it simple)
10. Once the conflicts are fixed, print the status: `git status`
11. Stage the modified file for commit: `git add team.txt`
12. Continue the rebase: `git rebase --continue`
13. View the commit log once again: `git log`
14. Push your changes to `origin`: `git push origin fix_name-spelling`
15. Notice the error
16. Now, try again, but force push: `git push -f origin fix_name-spelling`
17. Check your PR and ensure it can be merged without conflicts
18. Once it's ready to merge, I'll merge it

### Collaborating

1. Justin has started the work on each member's details, but needs help
2. Add Justin's fork as another remote: `git remote add justin <repo-url>`
3. Fetch a branch from Justin's repo: `git fetch justin feat_add-member-details`
4. Notice the printout from this fetch
5. Now, checkout the branch: `git checkout feat_add-member-details`
6. Now, checkout the other branch: `git checkout justin/feat_add-member-details`
7. Notice you are now in Detached HEAD Mode
8. Jump back into the non-detached branch: `git checkout -`
9. Add your role and location data to your member file
10. Add and commit your changes: `git add .` & `git commit`
11. Push your changes to `origin`: `git push origin feat_add-member-details`
12. PR your new branch to `upstream/main`

### Ammending Additions

1. You member detail feature has a new request: add the year you joined ForeRock
2. Open your member detail file, and add `year: <year joined>` at the bottom
3. Save your file
4. Stage your changes: `git add .`
5. View your commit history: `git log`
6. Amend your previous commit: `git commit --amend`
7. Push your changes to `origin`: `git push origin feat_add-member-details`
8. Oops, notice the error
9. Try again, but now force push: `git push -f origin feat_add-member-details`
10. Review your PR once again for correctness
11. Notice the two commits on your PR: one from me, and the other from you
12. Once it's ready, I will merge it
