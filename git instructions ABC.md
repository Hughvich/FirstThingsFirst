#### 远程仓库命令：
$ git clone + url(新建的仓库地址）  
一般加gitclone.com/github.com/...  
然后clone的本地仓库就和远程仓库关联上了

$ git remote add skeleton https://github.com/Berkeley-CS61B/skeleton-sp18.git  
在本地仓库添加远程仓（关联）并给远程仓库取名为skeleton

$ git remote -v   
查看当前仓库所连接的远程仓库

$ git pull skeleton master  
拉取skeleton远程仓库的数据，和本地仓库合并

$ git push origin master  
本地仓库push到远程仓库

----
#### 本地仓库命令：

$ git add lab1/*  
$ git commit -m "completed first part of lab1"
修改本地文件后，将修改的内容commit到本地仓库
举例子比如说这周我们在lab1中进行作业

$ git reset 将暂存区的文件取消暂存，
	或切换到指定版本（尾部加版本号）：git reset --hard  31d6035a6a5bda99e96ff57a5ca9524024d997e7

$ git log 查看版本标识commit  31d60...（一长串字符），作者，时间，备注-m

本地文件修改后，先git add到暂存区，然后git commit -m到本地仓库，再git push origin master到远程仓库

---
* git clone [remote-repo-URL]: Makes a copy of the specified repository, but on your local computer. Also creates a working directory that has files arranged exactly like the most recent snapshot in the download repository. Also records the URL of the remote repository for subsequent network data transfers, and gives it the special remote-repo-name “origin”.
* git remote add [remote-repo-name] [remote-repo-URL]: Records a new location for network data transfers.
* git remote -v: Lists all locations for network data transfers.* 
* git pull [remote-repo-name] master: Get the most recent copy of the files as seen in remote-repo-name
* git push [remote-repo-name] master: Pushes the most recent copy of your files to the remote-repo-name.

---
### 概念
工作区 -> git add -> 暂存区index/stage -> git commit -> 版本库

untracked：未跟踪：没被纳入版本控制（add 前）

tracked：已跟踪：被纳入版本控制（add 后）：  

1. Unmodified：未修改状态
2. Modified：已修改状态
3. Staged：已暂存状态

红色字体：没放到暂存区  
绿色字体：已放到暂存区  

