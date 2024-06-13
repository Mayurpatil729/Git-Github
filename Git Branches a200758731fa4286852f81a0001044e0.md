# Git Branches

---

# **Branched in git**

Branches are a way to work on different versions of a project at the same time. They allow you to create a separate line of development that can be worked on independently of the main branch. This can be useful when you want to make changes to a project without affecting the main branch or when you want to work on a new feature or bug fix.

![Untitled](Git%20Branches%20a200758731fa4286852f81a0001044e0/Untitled.png)

> the Default branch used to be **master**, but it is now called **main**. There is nothing special about main, it is just a convention.
> 

## **Creating a new branch**

create a new branch, you can use the following command:

```
git branch
git branch bug-fix   // Create a new Branch 
git switch bug-fix
git log
git switch master
git switch -c dark-mode    // Switch & Create branch
git checkout orange-mode     // To check branch exist or not
```

Some points to note:

- `git branch` - This command lists all the branches in the current repository.
- `git branch bug-fix` - This command creates a new branch called `bug-fix`.
- `git switch bug-fix` - This command switches to the `bug-fix` branch.
- `git log` - This command shows the commit history for the current branch.
- `git switch master` - This command switches to the `master` branch.
- `git switch -c dark-mode` - This command creates a new branch called `dark-mode`. the `c` flag is used to create a new branch.
- `git checkout orange-mode` - This command switches to the `orange-mode` branch.

> Commit before switching to a branchGo to .git folder and checkout to the HEAD file
> 

---

# **Merging branches**

```
git checkout main
git merge bug-fix
```

![Untitled](Git%20Branches%20a200758731fa4286852f81a0001044e0/Untitled%201.png)

### Note :

- `git checkout main` - This command switches to the `main` branch.
- `git merge bug-fix` - This command merges the `bug-fix` branch into the `main` branch.

This is a fast-forward merge. It means that the commits in the `bug-fix` branch are directly merged into the `main` branch. This can be useful when you want to merge a branch that has already been pushed to the remote repository.

---

### **Not fast-forward merge :**

![Untitled](Git%20Branches%20a200758731fa4286852f81a0001044e0/Untitled%202.png)

 

```
git checkout main
git merge bug-fix
```

![Untitled](Git%20Branches%20a200758731fa4286852f81a0001044e0/Untitled%203.png)

---

## **Managing conflicts**

There is no magic button to resolve conflicts. You have to manually resolve the conflicts. Decide, what to keep and what to discard. VSCode has a built-in merge tool that can help you resolve the conflicts. I personally use VSCode merge tool. Github also has a merge tool that can help you resolve the conflicts but most of the time I handle them in VSCode and it gives me all the options to resolve the conflicts.

## **Rename a branch**

```
git branch -m <old-branch-name> <new-branch-name>
```

## Delete Branch

```
git branch -d <branch-name>
```

## **Checkout a branch**

```
git checkout <branch-name>
```

## **List all branches**

```
git branch
```