---
layout: post
title:  "git pull request"
date:   2018-05-08 16:00:00 +0800
categories: git
---

在平时项目开发中，经常需要提交代码，并审核后合并到主分支。

目前，我使用的方法是，本地新建分支，完成开发后，推送并新建远程分支，然后网页上提一个pull request，但是我发现这样做的问题是，会在远程仓库新建很多分支，目前没想到其他方法。

具体操作指令

`git checkout -b xxx` 在某分支的基础上，新建一个本地分支

some coding...

`git add .` 添加要提交的文件

`git commit -m 'xxx'` 添加提交注释

`git push --set-upstream origin xxx` 将本地分支推送到远程，并新建xxx分支

然后网页端操作，选择要merge到分支，提交pull request

待仓库作者同意合并后，清理分支

`git branch -D xxx` 删除本地分支，D强制删除，d不强制

`git push origin --delete xxx` 删除远程分支
