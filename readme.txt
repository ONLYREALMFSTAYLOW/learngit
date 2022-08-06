Git is a versdistributed versionion control system.
Git is free software distributed under the GPL.

lesson 1：
现在总结一下今天学的两点内容：
1.初始化一个Git仓库，使用git init命令。
2.添加文件到Git仓库，分两步：
使用命令git add <file>，注意，可反复多次使用，添加多个文件；
使用命令git commit -m <message>，完成。
笔记：
1.第二次 git 的时候还是需要重新添加的
2.messagee 是更新备注

lesson 2：
要随时掌握工作区的状态，使用git status命令。
如果git status告诉你有文件被修改过，用git diff可以查看修改内容。

lesson 3:
现在总结一下：
HEAD指向的版本就是当前版本，因此，Git允许我们在版本的历史之间穿梭，使用命令git reset --hard commit_id。
穿梭前，用git log可以查看提交历史，以便确定要回退到哪个版本。
要重返未来，用git reflog查看命令历史，以便确定要回到未来的哪个版本。

