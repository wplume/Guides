# GitGuide
Git命令行指南

- `git status` 可以查看什么文件有改动
- `git diff` 可以查看改动了哪里，按`q`退出
- `git init`
- `git clone`
- `git add [file name]`
- `git commit`
- `git commit -m '[message]'`
- `git log` 查看提交历史
- `git reflog `“后悔药”
- `git branch`
- `git branch [new branch name]`
- `git branch -d [branch name]`
- `git branch -D [branch name]`
- `git checkout [branch name]` 切换分支
- `git checkout -b [branch name]` 新建并切换分支
- `git merge [branch name]` 在master下合并指定分支
- `git tag`
- `git checkout [file path]` 在没有add的情况下，可以撤销更改
- `git reset HEAD [file path]` 这个指令可以取消add，HEAD表示当前版本
- `git reset --hard HEAD`
- `git reset --hard [version number]` 前7位
- `git push [remote repo name] [branch name]`
- `git pull [remote repo name] [branch name]`
- `git fetch [remote repo name] [branch name]` 这个只是下载不merge，之后可以查看diff，再merge
- `git remote add [remote repo name] http/ssh`添加到远程仓库
- `git remote -v `查看当前有哪些远程仓库
- `git remote update [remote repo name] --prune` 更新远程仓库列表
- `git config --global user.name "[user name]"`
- `git config --global user.email "[user email]"`

删除`.git`目录，或者删除整个目录
解决冲突

## 撤销已推送的提交

1. 第一步
`git log`查看提交历史
2. 第二步
`git reset --soft [回滚到指定版本号]`重置到指定版本号
3. 第三步
`git push [remote repo name] [branch name] --force`强制推送