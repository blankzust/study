# git

git学习总结

### 初始化
> git init

### 将改动的文件添加到版本管理库 
  "*" 代表全部文件    
>git add <文件名或者 “*”> 

### 将代码提交到版本管理库
> git commit -m "提交信息"

### 查看当前仓库状态
  也就是那些文件修改过，但是看不到修改的内容
> git status

### 查看当前仓库修改内容
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

###查看命令历史
>git reflog

###