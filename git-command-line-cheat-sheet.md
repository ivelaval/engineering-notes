# Git command line notes

[![Official dicumentation](https://img.icons8.com/material/24/000000/link--v1.png)Official Documentation](https://git-scm.com/docs)

---



![Git workflow](https://res.cloudinary.com/practicaldev/image/fetch/s--QNbMdq1B--/c_limit%2Cf_auto%2Cfl_progressive%2Cq_auto%2Cw_880/https://thepracticaldev.s3.amazonaws.com/i/fgviyzh10boel5s7rwfb.png)



## Setup and Config 



```bash
git --version
```

[**Config**](https://git-scm.com/docs/git-config)

```bash
git config --list
```

```bash
git config --global user.name "Ivan Avila"
```

```bash
git config --global user.email "ivelaval@gmail.com"
```

[**Help**](https://git-scm.com/docs/git-help)

```bash
git help <verb>
```

```bash
git <verb> --help 
```

[**Init**](https://git-scm.com/docs/git-help)

```bash
git init
```



## Basic commands



[**Status**](https://git-scm.com/docs/git-status)

```bash
git status
```

[**Add**](https://git-scm.com/docs/git-add)

```bash
git add .
```

```
git add <directory/file>
```

```bash
git add -A
```

> Force to add everything changes

[**Commit**](https://git-scm.com/docs/git-commit)

```bash
git commit -m "<message>"
```

```bash
git commit -a -m "<message>"
```

> Commit the staged snapshot recursively

[**Log**](https://git-scm.com/docs/git-log)

```bash
git log
```

[**Diff**](https://git-scm.com/docs/git-diff)

```bash
git diff
```

> Show  unstaged changes between your inbox and working directory



## Branches



[**Branch**](https://git-scm.com/docs/git-branch)

```bash
git branch -a
```

> List all branches (Local and remote branches)

```bash
git branch <branch-name>
```

> Create a new branch

```bash
git branch -d <branch-name>
```

> Delete <branch-name>

[**Checkout**](https://git-scm.com/docs/git-checkout)

```bash
git checkout -b <branch-name>
```

> Create and check out a new <branch-name>

```bash
git checkout -- <file-name>	
```

> Discard file changes (<file-name>)

[**Switch**](https://git-scm.com/docs/git-switch)

```bash
git switch <branch-name>
```

> Switch to a specified branch

[**Stash**](https://git-scm.com/docs/git-stash)

```bash
git stash list
```

```bash
git stash apply
git stash apply <stash@{<number>}>
```

> Apply stash ID on 0 position ***stash@{0}*** if It's not has specified the position

```bash
git stash save "<name>"
```

```bash
git stash drop 
git stash drop <stash@{<number>}>
```

> Delete stash ID on 0 positon ***stash@{0}*** if It's not has specified the position

```bash
git stash show
git stash show <stash@{<number>}> 
```

> Show changes of stash ID on 0 positon ***stash@{0}*** if It's not has specified the position

```bash
git stash pop 
git stash pop <stash@{<number>}>
```

> Apply last stash and delete it if It's not has specified the position

```bash
git stash branch <branch-name> <stash@{<number>}>
```

> Create a new branch from stash ID



## Undoing changes



[**Reset**](https://git-scm.com/docs/git-reset)

```bash
git reset <file>
```

```bash
git reset
```

> Remove all files from staging area

[**Revert**](https://git-scm.com/docs/git-revert)

```bash
git revert
git revert <commit>
```

> Create a new commit that undoes all of the changes  made in <commit>

[**Clean**](https://git-scm.com/docs/git-clean)	

```bash
git clean <flag>
```

> Shows which files would be removed from working directory. Use the *-f* flag in place of the *-n* flag to excute the clean.



## Sharing and Updating Projects



[**Remote**](https://git-scm.com/docs/git-remote)

```bash
git remote -v
```

```bash
git remote add <name> <destination-url> 
```

```bash
git remote rename <new-name> <destination-url>
```

```bash
git remote show <name>	
```

```bash
git remote set-url <name> <new-destination-url>
```

[**Fetch**](https://git-scm.com/docs/git-fetch)

```bash
git fetch <remote> <branch>
```

> get last changes info

[**Pull**](https://git-scm.com/docs/git-pull)

```bash
git pull <remote> <branch>
git pull <remote/branch>
```

```bash
git pull --rebase <origin> <branch>
```

[**Push**](https://git-scm.com/docs/git-push)

```bash
git push <remote> <branch>
git push <remote/branch>
```

```bash
git push -u <remote> <branch>
```

> Push to <remote> any exist branch

```bash
git push <remote> --delete <branch>
```

> Delete remote branch



## Git Flow



![Git-flow](https://i.stack.imgur.com/TBHkD.png)