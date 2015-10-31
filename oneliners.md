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
- Dump git configs
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
- Sync fork with upstream repository
```bash
    cd ~/Workspaces/GitHub
    #clone the fork repo locally
    git clone https://github.com/jedatu/upstream-repo-name.git upstream-repo-fork
    cd upstream-repo-fork
    #add the upstream repo
    git remote add upstream https://github.com/UpstreamCorp/upstream-repo-name.git
    git fetch 
    git fetch upstream
    #updating a develop branch
    git checkout develop
    git merge --no-ff upstream/develop
    git commit –m “Updated develop with upstream”
    git push
    #updating a master branch
    git checkout -b master origin/master
    git merge --no-ff upstream/master
    git commit –m “Updated master with upstream”
    git push
```
