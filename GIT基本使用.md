### 1.文件添加到版本库中    
(1)通过命令 git ini把当前目录变成git可以管理的仓库  
(2)使用“git add 文件名”添加到暂存区  
   如果想将当前目录下及子目录内容全部加入暂存区，使用 git add  
(3)使用命令 git commit -m “注释” 把文件提交到仓库  
(4)如果临时修改文件，但`并未提交`，如果想看修改内容，使用 git diff文件名  
### 2.版本回退
(1)查看文件修改的历史记录,使用git log，如果嫌显示信息太多，使用git log --pretty=online.  
(2)如果想回退上个版本,使用git reset --hard HEAD^,如果想退回两个版本，使用git reset --hard HEAD^^.  
(3)查看仓库的各个版本号，使用git reflog.  
(4)想退回某个版本,使用git reset --hard 版本号。 
(5)如果在工作区修改了文件但还没有提交，如果想恢复修改前版本，用git checkout --(空格)文件名  
 ### 3.删除文件
 (1)在工作目录中删除文件：rm 文件名   
 (2)如果已经提交了，除了rm命令以外，还要再commit一下才能在版本库中删除
### 4.远程仓库
 (1)本地Git仓库和github仓库间是通过SSH加密的,查看密钥指令：cat ~/.ssh/id_rsa.pub
 (2)查看远程仓库用户信息，查看用户名git config user.name,查看用户注册邮箱git config user.email  
 (3)把本地仓库与远程仓库分支关联：git remote add origin(空格)+github对应的推送地址   
 (4)把本地库内容推送到远程库：git push -u origin master  
    如果是第一次推送，需要加-u，git不但会把本地master分支内容推送到远程master分支，还会把本地的master分支和远程master分支关联，因此以后的推送或者拉取时可以简化。  
 (5)[问题]如何解决failed to push some refs to git  
 出现错误的主要原因是在建立本地仓库后，与远程仓库的内容不一致导致的。因此在向远程库推送的时候，要先进行pull，让本地新建的库和远程同步：  
 git pull origin master,然后再push命令
