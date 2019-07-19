# Git教程

## Git相关概念解释

工作区 --> 暂存区 --> 版本库 --> 远程仓库

|名称|解释|
| ---- | ---- |
|工作区|本地文件存放的工作目录，尚未做标记|
|暂存区|将修改后本地文件标记为暂存，准备一起提交|
|版本库|标记暂存的文件提交后，正式标记为版本控制状态|
|远程仓库|将本地版本库与服务器上的版本库进行同步|

## Git常用命令解释

```bash
# 初始化当前目录为工作区
git init
# 添加test.txt文件到暂存区
git add test.txt
# 提交暂存区所有的变更到master版本库
git commit -m "add test.txt."
# 查看当前库状态
git status
# 查看test.txt文件修改的内容
git diff test.txt
# 查看仓库的修改日志
git log
# 回退到上一个版本
git reset --hard HEAD^
# 查看刚才的commit id
git reflog
# 指定当前HEAD指向的版本(eb68237为commit id)
git reset --hard eb68237
# 撤回还未添加到暂存区的变更(将版本库内的文件覆盖工作区的文件)
git checkout -- test.txt
# 撤回已添加到暂存区的变更
git reset HEAD test.txt
# 从版本库里删除文件并提交
git rm test.txt
git commit -m "remove test.txt."

# 将本地工作区关联到github
git remote add origin git@github.com:jarlcox/sharing.git
# 第一次将本地版本库与远程仓库关联
git push -u origin master
# 更新到远程仓库
git push origin master
# 从远程仓库克隆项目
git clone git@github.com:jarlcox/sharing.git

# 创建并切换到dev分支
git checkout -b dev
# 查看分支
git branch
```
