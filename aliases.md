##Useful aliases

```
        purge-h = "!f() { echo \"Removes all folders and files not in source control\"; }; f"
        purge = !git clean -fdx
        update-from-h = "!f() { echo \"git update-from <remote> <branch-name>\"; }; f"
        update-from = "!f() { git fetch $1 --prune; git merge --ff-only $1/$2 || git rebase --preserve-merges $1/$2; }; f"
        branches = !git branch
        branches-all = !git branch -a
	branches-find = "!f() { git branch -a | grep $1; }; f"
        co = checkout
        lga = log --graph --oneline --all --decorate
        pretty = log --graph --oneline --all --decorate
        ec = config --global -e
        update = !git pull --rebase --prune $@ && git submodule update --init --recursive
        fullmerge = !git merge --no-ff $@
        cob = checkout -b
        cm = "!f() { git add -A | git commit -m \"$1\"; }; f"
        cmp = "!f() { git add -A | git commit -m \"$1\" | git push; }; f"
        save = !git add -A && git commit -m 'SAVEPOINT'
        undo = reset HEAD~1 --mixed
        amend = commit -a --amend
        wipe = !git add -A && git commit -qm 'WIPE SAVEPOINT' && git reset HEAD~1 --hard
        bclean = "!f() { git branch --merged ${1-develop} | grep -v \" ${1-develop}$\" | xargs -r git branch -d; }; f"
        bdone = "!f() { git checkout ${1-develop} && git up && git bclean ${1-develop}; }; f"
        files = "!f() { git diff --name-status $1^ $1; }; f"
        lclone = "!f() { git checkout -b $1 origin/$1; }; f"
        initbranch = "!f() { git checkout -b $1 | git push --set-upstream origin $1; }; f"
        delbranch = "!f() { git branch -D $1; }; f"
        dumpconfigs = !git config --list
```
