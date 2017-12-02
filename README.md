# git

git学习总结

### 初始化
> git init

### 将改动的文件添加到版本管理库
  "*" 代表全部文件
>git add <文件名或者 * >

### 将代码提交到版本管理库
> git commit -m "提交信息"

### 查看当前仓库状态
  也就是那些文件修改过，但是看不到修改的内容
> git status

### 查看版本仓库与工作区的不同内容
  文件名可以不加 ，不加为全部
> git diff <文件名>

### 查看git提交历史
> git log
  如果查看自己的提交历史时嫌信息过多
>git log --pretty=oneline
### 版本回退
  HEAD版,HEAD^代表上一个版本 ，HEAD^^代表上上一个版本，HEAD~10 代表前推十个版本
> git reset --hard HEAD^  //回退到上个版本
> git reset --hard HEAD~10 //回退到前十个版本
> git reset --hard <commit_id> //回退到固定的版本

### 查看命令历史
>git reflog

### 撤销修改
*  checkout 与 -- 与 文件名之间都必须有空格<br />
  语句有两次含义：<br />
  1. 当你没有执行git add 的时候，将工作区的代码撤销到你最后一次commit的版本库里，
  2. 当你执行了 git add 的时候， 将你工作区的代码撤销到你最后一次git add 的暂存区里
> git checkout -- < 文件名称 >
* 将暂存区的修改撤销掉
>git reset HEAD < 文件名称 >

### 文件删除
  此操作是从版本库里删除
> git rm < 文件名称 >

### 查看当前分支
> git branch

### 创建新分支
> git branch < 分支名称 >

### 切换新分支 
> git checkout < 分支名称 >

### 创建新的分支并且切换过去
> git checkout -b < 分支名称 > 

### 合并分支
  合并指定分支到当前分支
  * 普通模式 走的是快速前进 merge之后是直接将 master的指针指向 dev 的提交上的  
> git merge < 分支名称 >
  * 禁用 快速前进模式 merge之后master 需要重新commit
> git merge --no-ff -m "< message >" < 分支名称 >

### 删除分支
> git branch -d < 分支名称 >