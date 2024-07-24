# Check it out

## Restore First Snapshot:
### Revert the working tree to its initial state, as captured in the first snapshot, and then print the content of the hello.sh file.
````bash
 git rev-list --max-parents=0 HEAD
 git revert 9ccf66b
 cat hello.sh
````
## Restore Second Recent Snapshot:
### Revert the working tree to the second most recent snapshot and print the content of the hello.sh file.
````bash
 git revert HEAD~1
 cat hello.sh
````
## Return to Latest Version:
### Ensure that the working directory reflects the latest version of the hello.sh file present in the main branch, without referring to specific commit hashes.
````bash
 git revert HEAD
````