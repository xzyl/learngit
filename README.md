1.创建版本库
新建一个git仓库
mkgir learngit 
进入git仓库
cd learngit 
查看路径
pwd  
变成Git可以管理的仓库
git init

（查看.git   ls -ah ）

编写一个readme.txt的文件

Git is a version control system.
Git is free software.
放到leargit的目录下

用命令告诉git 将文件添加到GIT仓库
git add readme.txt

用命令告诉告诉GIT 将文件添加到git仓库

git commint -m "wrote a readme.txt"
(简单解释一下git commit命令，-m后面输入的是本次提交的说明，可以输入任意内容，当然最好是有意义的，这样你就能从历史记录里方便地找到改动记录)


2.时光机穿梭
修改readme.txt文件

然后使用git status命令查看结果  出来的命令 有一行红色的字体  告诉我们文件被修改 但尚未提交

git diff 可以查看修改内容

git 可以允许我们在版本的历史之间穿梭   git reset --hard commit_id

穿梭前可以使用 git log 查看提交历史

穿梭回未来 git reflog查看命令历史，里边确定回到哪个版本
  明白

暂存区
第一步 将文件添加到git 的仓库但是未修改到分支

第二步 将文件添加到master的分支
3.管理修改
每次修改如果不add到暂存区 就不会加入到commit中	

撤销修改

当你乱改了工作区的某文件内容，想直接丢弃工作区的修改用命令   git checkout -- file

当你乱改了工作区额某文件内容 并且提交到了暂存区想丢弃修改  分两步 第一步 git reset HEAD file 然后按照第一步操作
删除文件
命令git rm用于删除一个文件。如果一个文件已经被提交到版本库，那么你永远不用担心误删，但是要小心，你只能恢复文件到最新版本，你会丢失最近一次提交后你修改的内容。



