- Create local branch based on origin and switch to it
    git checkout -b feature/1-Commands origin/feature/1-Commands

- Commit all changes with comment
    git add .
    git commit -a -m 'in-line comment'
    
- Clone Github project into a specific folder
    git clone https://github.com/AmwayCorp/MyBiz.git local-you-git
    
- Create branch and switch to it
    git checkout -b feature/mybranch
    
- Push branch to Github
    git push --set-upstream origin feature/mybranch
    
- Dumb git configs
    git config --list