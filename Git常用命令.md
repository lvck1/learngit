# Git常用命令

`git init`初始化一个仓库

`git add <file>`添加文件到暂存区

`git commit -m <message>`提交暂存区文件至仓库

`git status`查看仓库状态

`git diff`

`git restore <file>`丢弃工作区修改

`git restore --staged <file>`丢弃暂存区修改

`git reset --hard <commit_id>`回退到指定版本

`git rm <file>`删除版本库文件

`ssh-keygen -t rsa -C "youremail@example.com"`生成ssh私钥和公钥

`git remote add origin git@github.com:lvck1/learngit.git`将本地仓库关联到远程仓库

`git push -u origin master`将本地仓库内容推送到远程仓库

`git pull <remote> <branch>`拉取远程仓库最新代码

如果是两个不相关的提交记录，可能会报错`fatal: refusing to merge unrelated histories`
加一条`--allow-unrelated-histories`

`git remote`

* `-v` 查看远程仓库信息
* `rm` 删除远程仓库，即解除本地仓库与远程仓库的关联，不是物理删除

`git clone git@github.com:lvck1/learngit.git`克隆远程仓库到本地

`git branch`查看当前分支

* `git branch <branch_name>`创建分支
* `-d` 删除分支
* `-D` 强制删除分支

`git checkout <branch_name>`或`git switch <branch_name>`切换分支

* `git checkout -b <branch_name>`创建并切换分支

`git merge <branch_name>` 合并分支到当前分支(提交到版本库才能进行合并操作，工作区和暂存区是不能合并的)

* `git merge --no-ff -m "merge with no-ff" dev` 禁用Fast forward

`git stash` 保存当前现场，供以后恢复现场继续使用

* `list` 查看保存的现场
* `git stash apply` 恢复现场，但不删除stash内容
* `git stash drop` 删除stash内容
* `git stash pop` 恢复现场并删除stash内容

`git cherry-pick` 复制特定的提交到当前分支

`git push origin master`推送分支到对应的远程分支上

git push origin <tagname> 推送标签到远程

git push origin --tags 推送所有标签到远程仓库

`git rebase`可以把本地未push的分叉提交历史整理成直线

`git tag <name>`创建标签

`git tag`查看所有标签

* -d 删除标签
