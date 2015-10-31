- Create local branch based on origin and switch to it
```bash
    git checkout -b feature/1-Commands origin/feature/1-Commands
```
- Commit all changes with comment
```bash
    git add .
    git commit -a -m 'in-line comment'
``` 
- Clone Github project into a specific folder
```bash    
    git clone https://github.com/AmwayCorp/MyBiz.git local-you-git
```
- Create branch and switch to it
```bash
    git checkout -b feature/mybranch
```
- Push branch to Github
```bash 
    git push --set-upstream origin feature/mybranch
```
- Dumb git configs
```bash 
    git config --list
```
- Display a concise history of commits
```bash 
    git log --graph --oneline --all --decorate
```
- Reset Hard
```bash
    git reset --hard origin/develop
    git clean -f -d
```
- Display the reflog
```bash
    git reflog
```
    
