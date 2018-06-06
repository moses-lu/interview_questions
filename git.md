git的常用命令整理

0： 新建开发文件夹 git init 初始化项目，并形成.git的文件

1：git clone 克隆项目

2：进入项目

3：创建本地分支test，并拉取test分支上的代码，git checkout -b test orgin/test 

4：创建本地开发分支,切换到本地开发分支，同步测试代码  git checkout -b yexiao 

5: 在本地分支开发，提交   git add .       git commit -m 'message'

6:切分支到test上 ， 拉取最新代码  git pull， 合并yexiao分支的代码  有冲突时解决冲突后再提交  git merge yexiao 

7:查看状态 ,提交测试代码  git push

以我的github项目为例: 

url:https://github.com/moses-lu/interview_questions

项目名：interview_questions

#### 1：拉取项目： 

git clone 项目的url

cd  项目名

ls 查看一级目录  ls -a 查看所有目录

##### 2：创建分支  （开发时需要新开一个本地分支）

git branch 查看本地分支

git branch -r 查看远程分支

git branch branchName 创建分支

git checkout branchName 切换到相应的分支

git checkout -b branchName 创建本地分支并切换分支

git checkout -b branchName origin/branchName 创建本地分支并切换分支并拉取在远程分支上的数据

创建远程分支

git checkout yexiao

git push --set-upstream origin yexiao

#### 3：提交修改：

git status 查看状态

git  add . 所有文件

git commit -m '备注'

git status

#### 4: 提交到远程分支

git push 提交到当前的远程分支

提交到测试分支

git checkout test  git pull   git status   git merge branchName    git status  git push

#### 5：查看历史记录和提交的文件：

git log 查看

git log --author=userName 查看某个人提交的内容

git show commitId 查看某次提交的信息

#### 6：合并分支：假定当前分支为test

git merge yexiao   把yexiao分支合并到test了

git push  origin:barnchName  提交到远程分支  简写成 git push 

#### 7：删除：

git branch -r -D branchName  删除远程分支

git branch -D branchName 删除本地分支

rm fileName 删除本地文件

git rm fileName 删除远程文件

#### 8：配置和修改和查看用户名和邮箱
配置

git config –global user.name yexiao

git config –global user.email 15002171839@163.com

查看：

git config user.name

git config user.email

修改：

git config --global user.name "username"

git config --global user.email "email"