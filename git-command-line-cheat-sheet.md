# Git command line notes

[![Official dicumentation](https://img.icons8.com/material/24/000000/link--v1.png)Official Documentation](https://git-scm.com/docs)

---



![Git workflow](https://res.cloudinary.com/practicaldev/image/fetch/s--QNbMdq1B--/c_limit%2Cf_auto%2Cfl_progressive%2Cq_auto%2Cw_880/https://thepracticaldev.s3.amazonaws.com/i/fgviyzh10boel5s7rwfb.png)



## Setup and Config 



```bash
git --version
```

[![Official dicumentation](https://img.icons8.com/material/24/000000/link--v1.png)**Config**](https://git-scm.com/docs/git-config)

```bash
git config --list
```

```bash
git config --global user.name "Ivan Avila"
```

```bash
git config --global user.email "ivelaval@gmail.com"
```

[![Official dicumentation](https://img.icons8.com/material/24/000000/link--v1.png)**Help**](https://git-scm.com/docs/git-help)

```bash
git help <verb>
```

```bash
git <verb> --help 
```

[![Official dicumentation](https://img.icons8.com/material/24/000000/link--v1.png)**Init**](https://git-scm.com/docs/git-help)

```bash
git init
```



## Basic commands



**Status**

```bash
git status
```

**Add**

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

**Commit**

```bash
git commit -m "<message>"
```

```bash
git commit -a -m "<message>"
```

> Commit the staged snapshot recursively

**Log**

```bash
git log
```

**Diff**

```bash
git diff
```

> Show  unstaged changes between your inbox and working directory



## Branches



**Branch**

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

**Checkout**

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



## Undoung changes



**Reset**

```bash
git reset <file>
```

```bash
git reset
```

> Remove all files from staging area

**Revert**

```bash
git revert <commit>
```

> Create a new commit that undoes all of the changes  made in <commit>

**Clean**	

```bash
git clean <flag>
```

> Shows which files would be removed from working directory. Use the *-f* flag in place of the *-n* flag to excute the clean.









## Git Flow

![Git-flow](https://i.stack.imgur.com/TBHkD.png)