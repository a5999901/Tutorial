### 1.文件添加到版本库中    
(1)通过命令 git ini把当前目录变成git可以管理的仓库  
(2)使用“git add 文件名”添加到暂存区  
   如果想将当前目录下及子目录内容全部加入暂存区，使用 git add .
(3)使用命令 git commit -m “注释” 把文件提交到仓库  
(4)如果临时修改文件，但`并未提交`，如果想看修改内容，使用 git diff文件名  
### 2.版本回退
(1)查看文件修改的历史记录,使用git log，如果嫌显示信息太多，使用git log --pretty=online.  
(2)如果想回退上个版本,使用git reset --hard HEAD^,如果想退回两个版本，使用git reset --hard HEAD^^.  
(3)查看仓库的各个版本号，使用git reflog.  
(4)想退回某个版本,使用git reset --hard 版本号

 
