# HOWTO - Git Usage

## What is Git

> Git is a software for tracking changes in any set of files, usually used for corrdinating work among programmers collaboratively developing source code during software development.
> 
> *from [wikipedia](https://en.wikipedia.org/wiki/Git)*

Thus, with Git, we can collaborate within group and between group. [GitHub](https://github.com) is a company which provide a tools/website which intergrate with git. There are many other alternatives to GitHub, suc has [GitLab](https://gitlab.com/), [Bitbucket](https://bitbucket.org/) and [Gitee](https://gitee.com).

## Basic Knowledge of Git

NOTICE: in this document, we only introduce the git usage on UNIX-like platforms (e.g. macOS and Linux), for Windows, the usage of git are similar but the usage of bash/cmd are not. What's more, we will not introduce the installation of Git.

### create a local git repository(repo)
To begin, first you need to open up a terminal and move to the path that you want to place the proejct on.
```bash
cd ~/development/
mkdir template
cd tempalte
```
Then, to initialize a git repository in the root of the folder, run the `git init` command:
```bash
git init
```
Here, you have initilzed a git repo on the local machine.

### add a news file to the repo

After the coding, you produce a multiple files that want to upload to the git server, then, you need let the git know which file you want to update
```bash
touch helloworld.c   # <- create a file called helloworld.c
git add helloworld.c # <- include the "helloworld.c" in 
```

Usually, you need to check and add one-by-one, however, if you want to upload all the files(and folders) under the root path(or specific path), you can just use `git add .`
```bash
git add .
```

### create a commit
The git commit command captures a snapshot of the project's currently staged changes.
```bash
git commit -m"This is my first commit"
```

### push the commit
The git push command is used to upload local repository content to a remote repository.
```bash
git push
```

### pull the commit 
The git pull command is used to fetch and download content from a remote repository and immediately update the local repository to match that content. Thus, please do the `git pull` before you start changing you local code
```bash
git pull
```

## Reference

1. [The documentation of Git](https://git-scm.com/doc)
2. [troubleshooting documentation](https://ohshitgit.com/)
