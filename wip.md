
*Handling Work in Progress*

**Stash**

- Stash uncommitted changes, get latest and restore WIP

```
    git stash save "Uncommitted changes before update operation at 9/18/2014 9:25 AM"
    git merge --no-stat -v origin/develop
    git stash pop
``` 
