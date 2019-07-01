1.安装完git之后，在开始菜单里找到“Git”->“Git Bash”，蹦出一个类似命令行窗口的东西，就说明Git安装成功！
2.设置名字和email地址，
$ git config --global user.name "Your Name"
$ git config --global user.email "email@example.com"
注意git config命令的--global参数，用了这个参数，表示你这台机器上所有的Git仓库都会使用这个配置，当然也可以对某个仓库指定不同的用户名和Email地址。
3.创建一个版本库
$ mkdir learngit
$ cd learngit//打开目录
$ pwd //显示一下目录路径
通过git init命令把这个目录变成Git可以管理的仓库：$ git init

4.$ git status  //看下当前版本库的状态

  $ git diff readme.txt //看一下修改的区别 
  $ git add readme.txt //添加或修改文件
  $ git commit -m "add distributed" //提交文件，后面是描述
  
  版本回退
  $ git log //先看下提交日志    
  $ git log --pretty=oneline //让日志在一行显示，更清晰
  
  $ git reset --hard HEAD^//回退到上一个版本
  $ cat readme.txt //查看文件内容
  $ git reset --hard 1094a 回退到指定版本1094a.....
5.$ git checkout -- file可以丢弃工作区的修改

  $git checkout -- readme.txt
  命令git checkout -- readme.txt意思就是，把readme.txt文件在工作区的修改全部撤销，这里有两种情况：

一种是readme.txt自修改后还没有被放到暂存区，现在，撤销修改就回到和版本库一模一样的状态；

一种是readme.txt已经添加到暂存区后，又作了修改，现在，撤销修改就回到添加到暂存区后的状态。

总之，就是让这个文件回到最近一次git commit或git add时的状态。

6 $ rm test.txt //删除文件
 $ git rm test.txt //提交删除文件
7.$ git push -u origin master //本地文件上传到远程文件

8.$ git remote -v //查看远程分支
origin  git@github.com:username/Animations.git (fetch)
origin  git@github.com:username/Animations.git (push)
 $ git fetch origin master:temp //使用如下命令可以在本地新建一个temp分支，并将远程origin仓库的master分支代码下载到本地temp分支
 $ git diff temp //用如下命令来比较本地代码与刚刚从远程下载下来的代码的区别
 $ git merge temp //对比区别之后，如果觉得没有问题，可以使用如下命令进行代码合并
 
 $ git branch -d temp //如果temp分支不想要保留，可以使用如下命令删除该分支
 
9.git branch -a //查看远程分支，带有“*”号的表示当前分支
  git branch //查看本地分支
  git checkout master // 切换分支命令
  
  $ git branch -d //删除本地分支
  $ git push origin --delete // 删除远程分支
git clone git@github.com:martin-meng/yyy-2.git//远程仓库导入到本地

10.批量删除
先手动删除文件
$ git add .
$ git commit -m "clear"
$ git push