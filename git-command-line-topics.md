# Git command line topics

[![Official dicumentation](https://img.icons8.com/material/24/000000/link--v1.png)Official Documentation](https://git-scm.com/docs)



## 1. Resolving merge conflict with vimdiff



```bash
$ git mergetool
```



![Example](https://camo.githubusercontent.com/f9cc945fe7fdfa06222d1ed3939a96168f1adf16/68747470733a2f2f6170702e626f782e636f6d2f726570726573656e746174696f6e2f66696c655f76657273696f6e5f33373636313934383539342f696d6167655f323034382f312e706e673f7368617265645f6e616d653d7773393269753166746a69623870636d71306238686c79306877776e62316a68)

![vimdiff](https://www.rosipov.com/images/posts/three-way-merge-with-vimdiff.png)

From left to right, top to the bottom:

`LOCAL` – this is file from the current branch

 `BASE` – common ancestor, how file looked before both changes

 `REMOTE` – file you are merging into your branch 

`MERGED` – merge result, this is what gets saved in the repo

Let’s assume that we want to keep the “octodog” change (from REMOTE). For that, move to the MERGED file (`Ctrl + w, j`), move your cursor to a merge conflict area and then:

```bash
:diffget RE
```

```bash
Ctrl w + h   # move to the split on the left 
Ctrl w + j   # move to the split below
Ctrl w + k   # move to the split on top
Ctrl w + l   # move to the split on the right
```

This gets the corresponding change from `REMOTE` and puts it in `MERGED` file. You can also:

```bash
:diffg RE  " get from REMOTE
:diffg BA  " get from BASE
:diffg LO  " get from LOCAL
```

Save the file and quit (a fast way to write and quit multiple files is `:wqa`).



## 2.  Other `vimdiff` keyboard shortcuts

```bash
]c - Jump to the next change.
[c - Jump to the previous change.
```



## 3. Resolving conflict from a `git pull`

If you were trying to do a `git pull` when you ran into `merge` conflicts, follow all steps in the previous section for using the `mergetool`, then do:

```bash
$ git rebase –continue
```

This command will

> Forward-port local commits to the updated upstream HEAD.

according to the documentation, meaning your local commits will be pushed to the `upstream remote branch` as a new forward commit that doesn't interfere with previous commits. Hooray now you can claim that you can collaborate with others with Git without messing up with your collaborators' commits.

