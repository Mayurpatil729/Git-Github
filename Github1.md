# Github

---

# **What is Github?**

Github is a web-based Git repository hosting service. It is a popular platform for developers to collaborate on projects and to share code. Github provides a user-friendly interface for managing and tracking changes to your code, as well as a platform for hosting and sharing your projects with others.

Some other alternative of Github are:

- Gitlab
- Bitbucket
- Azure Repos
- Gitea

## **Configure your config file**

```
git config --global user.email "your-email@example.com"
git config --global user.name "Your Name
```

### check your config settings :

```
git config --list
```

---

# **Setup ssh key and add to github**

## **Step 1: Generate a new SSH key**

```
ssh-keygen -t ed25519 -C "your-email@chaicode.com"=
```

## **Save the key**

1. **Add key to your ssh-agent**
2. **Add key to github**
3. **Adding code to remote repository**

```
git init
git add <files>
git commit -m "commit message"
```

## **Check remote url setting**

```
git remote -v
```

## **Add remote repository**

```
git remote add origin https://github.com/
```

## **Push code to remote repository**

```
git push origin main
```

## **Setup an upstream remote**

```
git remote add upstream <remote-url>
```

```
git remote add -u <remote-url>
```

```
git push -u origin main
```

---

## **Get code from remote repository**

There are two ways to get code from a remote repository:

- fetch the code
- pull the code

Fetch the code means that you are going to download the code from the remote repository to your local repository. Pull the code means that you are going to download the code from the remote repository and merge it with your local repository.

![Untitled](Github%20a5dbaa5f706c4d0aa5908ece0e31ec30/Untitled.png)

### **Fetch code**

```
git fetch <remote-name>
```

### **Pull code**

```
# git pull <remote-name> <branch-name>
git pull origin main
```

Here `<remote-name>` is the name of the remote repository that you want to pull from and `<branch-name>` is the name of the branch that you want to pull.

---

## Git Clone

```
git clone link
```