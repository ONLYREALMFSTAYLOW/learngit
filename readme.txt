Git is a versdistributed versionion control system.
Git is free software distributed under the GPL.
Git has a mutable index called stage.
Git tracks changes of files.


lesson 1 添加文件到 Git 仓库：
现在总结一下今天学的两点内容：
1.初始化一个Git仓库，使用git init命令。
2.添加文件到Git仓库，分两步：
使用命令git add <file>，注意，可反复多次使用，添加多个文件；
使用命令git commit -m <message>，完成。
笔记：
1.第二次 git 的时候还是需要重新添加的
2.messagee 是更新备注


lesson 2 查看工作区状态：
要随时掌握工作区的状态，使用git status命令。
如果git status告诉你有文件被修改过，用git diff可以查看修改内容。


lesson 3 查看历史版本:
现在总结一下：
HEAD指向的版本就是当前版本，因此，Git允许我们在版本的历史之间穿梭，使用命令git reset --hard commit_id。
穿梭前，用git log可以查看提交历史，以便确定要回退到哪个版本。
要重返未来，用git reflog查看命令历史，以便确定要回到未来的哪个版本。


lesson 4 提交的具体过程:
前面讲了我们把文件往Git版本库里添加的时候，是分两步执行的：
第一步是用git add把文件添加进去，实际上就是把文件修改添加到暂存区；
第二步是用git commit提交更改，实际上就是把暂存区的所有内容提交到当前分支。
因为我们创建Git版本库时，Git自动为我们创建了唯一一个master分支，所以，现在，git commit就是往master分支上提交更改。
你可以简单理解为，需要提交的文件修改通通放到暂存区，然后，一次性提交暂存区的所有修改。


lesson 5 本地操作回退:
场景1：当你改乱了工作区某个文件的内容，想直接丢弃工作区的修改时，用命令git checkout -- file。
场景2：当你不但改乱了工作区某个文件的内容，还添加到了暂存区时，想丢弃修改，分两步，第一步用命令git reset HEAD <file>，就回到了场景1，第二步按场景1操作。
场景3：已经提交了不合适的修改到版本库时，想要撤销本次提交，参考版本回退一节，不过前提是没有推送到远程库。

lesson 6 文件删除恢复：
命令git rm用于删除一个文件。如果一个文件已经被提交到版本库，那么你永远不用担心误删，但是要小心，你只能恢复文件到最新版本，你会丢失最近一次提交后你修改的内容。
使用 git checkout 恢复，其实是用版本库里的版本替换工作区的版本，无论工作区是修改还是删除，都可以“一键还原”。

lesson 7 链接到 github：
使用公钥
ssh 文件夹在系统中不可见，可以直接用 $ open ~/.ssh 命令直接打开

lesson 8 在 github 关联远程库：
$ git remote add origin git@github.com:ONLYREALMFSTAYLOW/learngit.git
要关联一个远程库，使用命令git remote add origin git@server-name:path/repo-name.git；
关联一个远程库时必须给远程库指定一个名字，origin是默认习惯命名；
关联后，使用命令git push -u origin master第一次推送master分支的所有内容；
此后，每次本地提交后，只要有必要，就可以使用命令git push origin master推送最新修改；

lesson 9 从 github 克隆远程库：
$ git clone git@github.com:ONLYREALMFSTAYLOW/gitskills.git
然后可以进入查看一下
$ cd xxx
$ ls

try again

这条用以说明 vs 自动 commit and push 成功

check 一下是不是非要用 request 插件

基本可以确认是非要用到那个插件才会更新

再次尝试自动提交

为什么 vscode 自动提交就是不行呢

再试试，找原因

问题出在更新没有写说明