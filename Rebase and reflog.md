# Rebase and reflog

---

## **Rebase in git**

Git rebase is a powerful Git feature used to change the base of a branch. It effectively allows you to move a branch to a new starting point, usually a different commit, by “replaying” the commits from the original base onto the new base. This can be useful for keeping a cleaner, linear project history.

Some people like to use rebase over the merge command because it allows you to keep the commit history cleaner and easier to understand. It also allows you to make changes to the code without affecting the original branch.

## **Merge commits**

A merge commit is a commit that combines two or more commits into one. It is created when you merge two or more branches into a single branch. The merge commit contains all the changes from the original branches, and it is used to keep the project history clean and easy to understand.

![Untitled](Rebase%20and%20reflog%20f9a931e356224dd59dd2e94475f76861/Untitled.png)

![Untitled](Rebase%20and%20reflog%20f9a931e356224dd59dd2e94475f76861/Untitled%201.png)

Rebase is a powerful tool in Git that allows you to move a branch to a new starting point. It effectively replays the commits from the original base onto the new base. This can be useful for keeping a cleaner, linear project history.

Suppose you have a feature branch called feature-branch that you want to rebase onto the main branch.

### **Ensure you are on the branch you want to rebase:**

```
git checkout feature-branch
git rebase main
```

### **Resolve any conflicts:**

```
git add <resolved-files>
git rebase --continue
```

## **Git reflog**

Git reflog is a command that shows you the history of your commits. It allows you to see the changes that you have made to your repository over time. This can be useful for debugging and understanding the history of your project.

**View the reflog:**

```
git reflog
```

**Find specific commit**

```
git reflog <commit-hash>
```

**Recover lost commits or changes**

```
git reflog <commit-hash>
git reset --hard <commit-hash>
```

```
git reflog <commit-hash>
git reset --hard HEAD@{1}
```

---