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

