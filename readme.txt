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
  dfs

