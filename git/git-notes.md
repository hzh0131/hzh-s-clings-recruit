# Git Learning Notes

GitHub Username: <hzh0131>

## Course Repositories

Introduction to Git:
https://github.com/<hzh0131>/<hzh-s-clings-recruit>

Introduction to GitHub:
https://github.com/<hzh0131>/<hzh-s-clings-recruit>

## Git and GitHub
1. Git：本地软件工具，安装在自己电脑，不用联网。可以做记录代码修改、保存版本、回退代码，负责版本控制等等的事。

2. GitHub：互联网网站平台，必须联网。本身不会做版本记录，只用来存放 Git 导出的代码仓库。

3. 核心区别：Git 是工具，干版本管理的活；GitHub 是线上存储空间，用来存放 Git 管理好的代码。Git 可以脱离 GitHub 单独使用，但 GitHub 离不开 Git 来上传代码。


## Basic Workflow

### Commit

Commit 就是把当前代码改动保存在本地，是 Git 最基础的保存操作。每次写完一部分功能，我就可以 commit，写上简短说明记录改了什么。它不会把代码上传到网上，只是存在本地电脑。后续代码写崩的时候，就能通过 commit 记录，回退到之前没问题的版本，方便追踪每一步修改，避免改动丢失。

### Branch

Branch 也就是分支，可以理解成代码的副本。主分支一般存放稳定能运行的代码，我开发新功能时，新建分支在上面修改，不会破坏原本的主代码。不同分支互不干扰，适合小组开发。功能调试完成后，再把分支合并回主分支，这样就不会因为写新代码把原本能跑的程序搞坏。


### Pull Request

Pull Request 简称 PR，是 GitHub 平台的功能，本地 Git 没有这个功能。我在自己分支改完代码后，通过 PR 向项目主仓库申请把我的修改合并进去。队友可以在这里查看我的代码、提出修改意见，审核通过之后，代码才会并入主项目。团队做课程大作业时，可以靠它实现多人协作审核代码。

## Commands and Operations

1. git status 查看仓库当前状态，能看到哪些文件被修改、哪些还没暂存，哪些准备提交。不会改动代码，相当于"查看仪表盘"，写代码前后经常敲它，确认自己改了哪些文件，防止误操作。

2. git add 文件名 把修改后的文件加入暂存区。改动完代码不会直接保存版本，git add告诉Git：我要把这些文件纳入下一次提交。可以指定单个文件，也可以用git add .把全部改动文件加入暂存，只是临时存放，还没有生成版本。

3. git commit -m "描述文字" 把暂存区的改动，生成本地版本快照。‑m后面写这次改了什么的备注。执行完，改动就永久记录在本地Git里，可以回退，此时代码还只在自己电脑，没有传到GitHub。

4. git push 将本地已经commit完成的版本，推送到远程GitHub仓库。把电脑上的版本上传到网上，云端就同步了我的代码，队友也能拉取到我的修改，完成本地到线上的同步。

## What I Learned

1. 我一开始不知道git add与git commit -m的区别，后来自己尝试了几次就清楚了前者只是暂存，后者则是生成本地版本，在本地保存了改动。而要上传到云端则还需要git push。即git add--git commit -m--git push。

