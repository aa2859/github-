# github-
github使用文档(待改进)


git常用命令
设置git的user name和email
git config --global user.name ""
git config --global user.email""
设置本地秘钥
cd ~/.ssh                           如果没有秘钥就没有文件显示,有则备份删除
ssh-keygen -t rsa -C "邮箱"         按回车 选择y 按回车,复制公钥到github的ssh中
ssh -T git@github.com               测试是否连接上
git init                            本地库初始化
git clone  IP网址                   克隆远程库
git clone  IP网址 -b 分支名称       克隆远程库具体分支
git status                          查看状态
git add .                           增加所有修改文件
git add -A                          增加所有(当需要提交的数据过多时)
git reset head .                    撤销git add的内容 
git commit -a                       提交所欲改动的文件
git commit -m '说明'                提交时并加说明
git push                            推送到github
git log                             查看所有的commit记录
git branch                          列出本地分支
git branch -v                       查看远程和本地的所有分支
git checkout 分支名字               切换分支

git rm 文件名                       删除了物理文件(慎用)
git rm --cache -r                   只把特定文件从暂存区删除(实际文件没有删除)
git merge 分支名aa                  将aa分支合并到当前分支

git pull                            拉取远程库
git merge origin/master             将远程主分支合并到本地当前分支

git reset --hard commitId号         本地回滚
touch .gitignre                     创建忽略文件
git diff -w +文件名                 来确认代码自动合并的情况
git checkout HEAD file/to/restore   git reset是针对版本,如果想针对文件回退本地修改
git stash                           git pull时本地与远程发生冲突时,本地的所有修改就都被暂时存储起来
git stash list                      可以看到保存的信息
