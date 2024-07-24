# Move it

## Moving hello.sh:
### Using Git commands, move the program hello.sh into a lib/ directory, and then commit the move.
````bash
mkdir -p lib
git mv hello.sh lib/
git add hello.sh 
git commit -m "file organisation:moved hello.sh to lib"
````
### Create a Makefile in the root directory of the repository with the provided content and commit it to the repository.
````bash
nano Makefile
git add Makefile 
git commit -m "file org:created Makefile"
````