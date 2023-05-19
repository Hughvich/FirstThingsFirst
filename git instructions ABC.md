#### 远程仓库命令：
$ git clone + url(新建的仓库地址）  
一般加gitclone.com/github.com/...  
然后clone的本地仓库就和远程仓库关联上了

$ git remote add skeleton https://github.com/Berkeley-CS61B/skeleton-sp18.git  
在本地仓库添加远程仓（关联）并给远程仓库取名为skeleton

$ git remote -v   
查看当前仓库所连接的远程仓库

$ git pull skeleton master  
本地仓库拉取skeleton远程仓库的数据 master为分支名称  
如果本地仓库不是从远程克隆，而是本地创建的仓库且其中存在文件，此时再pull会报错，可以通过--allow-unrelated-histories合并

$ git push origin master  
push 本地仓库origin 到远程仓库master分支

----
#### 本地仓库命令：
$git init 创建本地仓库（会默认创建一个master分支）

$ git add lab1/*  
$ git commit -m "completed first part of lab1"
修改本地文件后，将修改的内容commit到本地仓库
举例子比如说这周我们在lab1中进行作业

$ git reset 将暂存区的文件取消暂存，
	或切换到指定版本（尾部加版本号）：git reset --hard  31d6035a6a5bda99e96ff57a5ca9524024d997e7

$ git log 查看版本标识commit  31d60...（一长串字符），作者，时间，备注-m

本地文件修改后，先git add到暂存区，然后git commit -m到本地仓库，再git push origin master到远程仓库

---
#### 分支：
$ git branch 查看分支 -r 远程分支 -a 所有本地+远程分支  
$ git branch [branch-name] 创建分支  
$ git checkout [branch-name] 切换分支  
$ git push [repo-name] [branch-name] 推送至远程仓库分支  
$ git merge[branch-name]合并分支到当前分支

合并冲突：  
两个分支下都修改过同一文件

---
#### 标签：
某个分支某个特定时间点的状态  
$ git tag 查看所有标签  
$ git tag[tag-name] 创建标签  
$ git push[repo-name] [tag-name] 标签push到远程repo  
$ git checkout -b [branch] [tag-name] 检出标签，将标签状态下载下来，拿到当时状态代码，需要创建新分支  


****分支和标签的区别：****  
分支会发生变化（副本），标签为静态的快照，正在成长的人和照片里的人的区别

---
### 在IDEA中使用git
* 从本地初始化仓库：VCS - Create Git Repository...
* 从远程仓库克隆：VCS - Get from Version Control ...

.gitignore文件：不用交给git管理的，如.iml,.idea,target/的.class文件

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

