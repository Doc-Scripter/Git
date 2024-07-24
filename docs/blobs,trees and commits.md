# blobs, trees and commits

## Exploring .git/ Directory:
### Navigate to the .git/ directory in your project and examine its contents.You will have to explain the purpose of each subdirectory, including objects/, config, refs, and HEAD in the audit.
````bash
  cd .git
  ls -R
````
## Latest Object Hash:
### Find the latest object hash within the .git/objects/ directory using Git commands and print the type and content of this object using Git commands.
````bash
git log -1 --format="%H"
current_hash=$(git log -1 --format="%H")
git cat-file -t $current_hash
git cat-file -p $current_hash
git log -1 --format="%T"
tree_hash=$(git log -1 --format="%T")
git ls-tree $tree_hash
````
## Dumping Directory Tree:
### Use Git commands to dump the directory tree referenced by this commit.
```bash
lib_hash=$(git ls-tree $tree_hash lib|awk '{print $3}')
git ls-tree $lib_hash
````
### Dump the contents of the lib/ directory and the hello.sh file using Git commands.
````bash
hello_hash=$(git ls-tree $lib_hash hello.sh | awk '{print $3}')
git cat-file -p $hello_hash
````
