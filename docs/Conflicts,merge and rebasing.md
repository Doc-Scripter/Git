# Conflicts, merging and rebasing

## Merge Main into Greet Branch:
### Start by merging the changes from the main branch into the greet branch.
````bash
git checkout greet 
git merge main 
````
### Switch to main branch and make the changes below to the hello.sh file, save and commit the changes.
````bash
git checkout main 
nano hello.sh 
git add hello.sh 
git commit -m "updated:changed content in hello.sh"
````

## Merging Main into Greet Branch (Conflict):
### Attempt to merge the main branch into greet. Bingooo! There you have it, a conflict.
````bash
git checkout greet 
git merge main
````
### Resolve the conflict (manually or using graphical merge tools), accept changes from main branch, then commit the conflict resolution.
````bash
git status
````
#### i used vs-code to fix the conflicts
```bash
git add hello.sh 
git commit -m "fix:resolved conflicts"
````
## Rebasing Greet Branch:
### Go back to the point before the initial merge between main and greet.
````bash
 git reset --hard 51b660c1973b17
````
### Rebase the greet branch on top of the latest changes in the main branch.
````bash
 git checkout greet 
 git rebase main 
````
## Merging Greet into Main:
### Merge the changes from the greet branch into the main branch.
```bash
git checkout main 
git merge greet 
```
## Understanding Fast-Forwarding and Differences:
###  Explain fast-forwarding and the difference between merging and rebasing.
Fast-Forward Merge:

    A fast-forward merge occurs when the target branch is simply updated to point to the same commit as the source branch because there are no diverging commits.

Merging:

    Merging combines the changes from different branches into one. It can create a merge commit if there are divergent commits.

Rebasing:

    Rebasing re-applies commits on top of another base commit. This keeps the commit history linear but can rewrite commit history.
 