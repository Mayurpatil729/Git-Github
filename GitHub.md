<!-- @format -->

# GitHub

Status: Not started

## What is Git ?

**Git is a distributed version control system used for tracking changes in source code during software development.**

## What is GitHub ?

**GitHub is a web-based platform that uses Git for version control, offering a range of features to facilitate collaborative software development. It is widely used by developers and organizations to host, manage, and review code, as well as to track and control changes in software projects.**

- Git is a software & Github is Service.
- Chectpoints like a game.

```
Cd  : For changing directory
pwd  : present working directory
```

# ⏩ Git Commands

---

![Untitled](GitHub%20063cc69ec7864f4f997dd54e5347e34a/Untitled%201.png)

![Untitled](GitHub%20063cc69ec7864f4f997dd54e5347e34a/Untitled%202.png)

1. **Check Version**

```
git --version
```

1. **There is a difference between a software on your system vs tracking a particular folder on your system. At any point you can run the following command to see the current state of your repository :**

```
git status
```

1. **Setup your email and username in this config file.**

```
git config --global user.email "your-email@example.com"
git config --global user.name "Your Name"
```

1. **You can check your config settings :**

```
git config --list
```

1. **Paste these code in JSON setting to see the . files**

```
"files.exclude": {
    "**/.git": false
  }
```

**Stage is a way to tell git to track a particular file or folder. You can use the following command to stage a file :**

```
git init
git add <file> <file2> // for particular files
git add . // for all files present in folder
git status
```

**Commit :**

**commit message should be ( present tense and imperative).**

order to the code base

```
git commit -m "commit message"
git status
```

**Logs**

```
git log
git log --oneline   // for short description
```

**Change default code editor**

```
git config --global core.editor "code --wait"
```

**gitignore**

Gitignore is a file that tells git which files and folders to ignore. It is a way to prevent git from tracking certain files or folders. You can create a gitignore file and add list of files and folders to ignore by using the following command:

```
node_modules
.env
.vscode
```

---

# **Git behind the scenes**

Git is a version control system that allows you to track changes to your files and folders. It is a powerful tool that can help you manage your code more effectively. In this section, we will explore the basics of how git works internally.

## **3 Musketeers of git**

The three musketeers of git are:

- Commit Object
- Tree Object
- Blob Object

## **Commit Object**

Each commit in the project is stored in `.git` folder in the form of a commit object. A commit object contains the following information:

- Tree Object
- Parent Commit Object
- Author
- Committer
- Commit Message

## **Tree Object**

Tree Object is a container for all the files and folders in the project. It contains the following information:

- File Mode
- File Name
- File Hash
- Parent Tree Object

Everything is stored as key-value pairs in the tree object. The key is the file name and the value is the file hash.

## **Blob Object**

Blob Object is present in the tree object and contains the actual file content. This is the place where the file content is stored.

![Untitled](GitHub%20063cc69ec7864f4f997dd54e5347e34a/Untitled%203.png)

```
git show -s --pretty=raw <commit-hash>
```

Grab tree id from the above command and use it in the following command to get the tree object:

```
git ls-tree <tree-id>
```

---

```
echo "# React-Tutorial" >> README.md
git init
git add README.md
git commit -m "first commit"
git branch -M main
git remote add origin https://github.com/Mayurpatil729/Django-Tutorial.git
git push -u origin main
```

```
git remote add origin https://github.com/Mayurpatil729/React-Tutorial.git
git branch -M main
git push -u origin main
```

---
