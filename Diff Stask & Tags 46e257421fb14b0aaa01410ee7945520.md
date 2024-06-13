# Diff Stask & Tags

---

# **Git diff**

The `git diff` is an informative command that shows the differences between two commits. It is used to compare the changes made in one commit with the changes made in another commit. Git consider the changed versions of same file as two different files. Then it gives names to these two files and shows the differences between them.

## **How to read the diff**

- a -> file A and b -> file B
- --- indicates the file A
- +++ indicates the file B
- @@ indicates the line number

Here the file A and file B are the same file but different versions.

Git will show you the changes made in the file A and file B. It will also show you the line number where the change occurred along with little preview of the change.

---

# **Comparing Working Directory and Staging Area**

This command shows the unstaged changes in your working directory compared to the staging area. This command alone will not show you the changes made in the file A and file B, you need to provide options to show the changes.

```
git diff
```

This command shows the changes between your last commit and the staging area (i.e., changes that are staged and ready to be committed).

```
git diff --staged
```

## **Comparing between branches**

This command compares the difference between two branches.

```
git diff <branch-name-one> <branch-name-two>
```

Another way to compare the difference between two branches is to use the following command:

```
git diff branch-name-one..branch-name-two
```

**Comparing Specific Commits:**

```
git diff <commit-hash-one> <commit-hash-two>
```

---

## **Git Stash**

Stash is a way to save your changes in a temporary location. It is useful when you want to make changes to a file but don’t want to commit them yet. You can then come back to the file later and apply the changes.

> Conflicting changes will not allow you to switch branches without committing the changes. Another alternative is to use the git stash command to save your changes in a temporary location.
> 

```
git stash
```

### **Naming the stash**

You can also name the stash by using the following command:

```
git stash save "work in progress on X feature"
```

### **View the stash list**

```
git stash list
```

**Apply the stash**

```
git stash apply
```

**Apply the specific stash**

```
git stash apply stash@{0}
```

**Applying and dropping the stash**

```
git stash pop
```

**Drop the stash**

```
git stash drop
```

**Applying stash to a specific branch**

```
git stash apply stash@{0} <branch-name>
```

**Clearing the stash**

```
git stash clear
```

---

# **Git Tags**

Tags are a way to mark a specific point in your repository. They are useful when you want to remember a specific version of your code or when you want to refer to a specific commit. Tags are like sticky notes that you can attach to your commits.

### **Creating a tag**

```
git tag <tag-name>
```

**Create an annotated tag**

```
git tag -a <tag-name> -m "Release 1.0"
```

**List all tags**

```
git tag
```

**Tagging a specific commit**

```
git tag <tag-name> <commit-hash>
```

**Push tags to remote repository**

```
git push origin <tag-name>
```

**Delete a tag**

```
git tag -d <tag-name>
```

**Delete tag on remote repository**

```
git push origin :<tag-name>
```

---