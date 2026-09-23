## Branching:
A `branch` is a small movable pointer that refers to a commit.

* Branching means creating a seperate line of development from the main line.

* For example you  need to add a feature to your project:
  You can create a branch for that
```SH
  $  git branch payment-feature
```

**The main purpose of branching is isolation**:
→ The stable code remains undisturbed
→ You can experiment safely
→ You can work on several tasks independently
→ You can later combine the work through mergin.


* To create a new branch
```sh
    $ git branch testing
```
It creates a branch but it doesnt switch to automatically, use this to do it
```sh
    $ git switch -c testing
```
And if you already have a branch but not switch to it yet, 
```sh
  $ git checkout testing
```
#### Viewing all branches and divergence
```sh
    $ git log --oneline --decorate --graph --all
```

→ `--oneline` displays each commit compactly
→ `--decorate` displays branch names and `HEAD`
→ `--graph` draws an ASCII graph showing relationships
→ `all` includes commits reachable from all local branches.


#### The complete mental model is:
`HEAD → current branch → latest commit → parent commit → earlier commit`

**When you:**
* Create a branch, Git creates another pointer to a commit.
* Switch branches, Git moves `HEAD` and updates your working directory.
* Commit, the current branch pointer moves forwad.
* Work on two branches independently, their histories diverge
* View the graph, Git shows how those pointers and commits relate
* Merge later, Git uses the record parent relationships to combine the lines development.


## Basic Branching and Merching:

