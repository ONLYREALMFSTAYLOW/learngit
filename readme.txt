Git is a versdistributed versionion control system.
Git is free software distributed under the GPL.
Git has a mutable index called stage.
Git tracks changes of files.


lesson 1 添加文件到 Git 仓库：
git init：为当前所在文件夹初始化一个Git仓库
git add <file>：添加文件到暂存区，可反复添加多个文件
git commit -m <message>：提交更新，messagee是更新备注，不可为空


lesson 2 查看工作区状态：
git status：查看工作区状态
git diff：查看修改内容


lesson 3 查看历史版本:
git log：查看提交历史
git reset --hard commit_id：回退到指定提交版本
git reflog：查看命令历史


lesson 4 提交的具体过程:
因为我们创建Git版本库时，Git自动为我们创建了唯一一个master分支，所以，现在，git commit就是往master分支上提交更改。
你可以简单理解为，需要提交的文件修改通通放到暂存区，然后，一次性提交暂存区的所有修改。


lesson 5 本地操作回退:
场景1：当你改乱了工作区某个文件的内容，想直接丢弃工作区的修改时，用命令git checkout -- file。
场景2：当你不但改乱了工作区某个文件的内容，还添加到了暂存区时，想丢弃修改，分两步，第一步用命令git reset HEAD <file>，就回到了场景1，第二步按场景1操作。
场景3：已经提交了不合适的修改到版本库时，想要撤销本次提交，参考版本回退一节，不过前提是没有推送到远程库。

lesson 6 文件删除恢复：
git rm：删除一个文件。如果一个文件已经被提交到版本库，那么你永远不用担心误删，但是要小心，你只能恢复文件到最新版本，你会丢失最近一次提交后你修改的内容。
使用 git checkout 恢复，其实是用版本库里的版本替换工作区的版本，无论工作区是修改还是删除，都可以“一键还原”。

lesson 7 链接到 github：
使用公钥
ssh 文件夹在系统中不可见，可以直接用 $ open ~/.ssh 命令直接打开

lesson 8 在 github 关联远程库：
$ git remote add origin git@github.com:ONLYREALMFSTAYLOW/learngit.git
关联一个远程库时必须给远程库指定一个名字，origin是默认习惯命名；
关联后，使用命令git push -u origin master第一次推送master分支的所有内容；
此后，每次本地提交后，只要有必要，就可以使用命令git push origin master推送最新修改；

lesson 9 从 github 克隆远程库：
$ git clone git@github.com:ONLYREALMFSTAYLOW/gitskills.git
然后可以进入查看一下
$ cd xxx
$ ls

lesson 10 vscode 自动同步到远程库：
更新说明不能为空
