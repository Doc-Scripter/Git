# History
## Show the history of the working directory.
````bash
git log
````
##  Show One-Line History for a condensed view showing only commit hashes and messages.
````bash
 git log --oneline
````
## Controlled Entries:
### You need to customize the log output by specifying the number of entries or a time range. Customize it to display the last 2 entries and to view the commits made within the last 5 minutes.
````bash
 git log --oneline -n 2
 git log --since="5 minutes ago" -n 2 
````
## Personalized Format:
### Show logs in a personalized format, including the commit hash, date, message, branch information, and author name, resembling * e4e3645 2023-06-10 | Added a comment (HEAD -> main) [John Doe]
````bash
 git log --since="30 minutes ago" -n 2 --pretty=format:"* %h %ad | %s (%d) [%an]" --date=short
````
 