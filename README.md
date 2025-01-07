# github_web_application

一、 github上新建仓库，本地上传初始代码
1.在github上创建仓库

2. 打开 Git Bash
  首先进入你的master文件夹下，右键打开“Git Bash Here” ，弹出命令窗口 ，输入如下语句进行上传
  首先找到你想创建的目录文件通过git init创建本地git仓库
  比如我在本地路径：E:/1github/0_git_chinese_dog
  右键Git Bash Here

3. git init  初始化本地仓库（若未初始化）
  //  在此文件夹生成一个.git隐藏文件
  $ git init    
  
  init我们已经做了
  git add README.md
  git commit -m "first commit"
  git branch -M main
  git remote add origin https://github.com/xiaoluoshan/2024_chinese_readdog.git
  git push -u origin main

4. 将本地代码添加到暂存区

  路径下新建一个log.txt
  // 将文件添加到缓存区( 注意这个"."，是有空格的，
  "."代表这个test这个文件夹下的目录全部都提交，
  也可以通过git add 文件名 提交指定的文件)
  $ git add . 
  
  //  查看现在的状态，可以看到picture文件夹里面的内容都提交上去了；
  $ git status  
  
  //  提交本地代码到本地仓库
  $ git commit -m "Initial commit"
  
  //  添加远程仓库地址
  //  添加新的git方式的origin, github上创建好的仓库和本地仓库进行关联
  $ git remote add origin git@github.com:xiaoluoshan/2024_chinese_readdog.git
  
  // 把本地库的所有内容推送到远程仓库（github）上
  将本地仓库的代码推送到 GitHub 远程仓库的 master 分支
  （如果想推送到其他分支，把 master 替换成相应分支名即可）
  $ git push origin master

二、下载、修改并提交代码到仓库

1）克隆 或 拉取最新代码
  //克隆
  git clone http://xxx
  //拉取
  git pull http://xxx

2）修改后，添加
  git add xxx

3）描述信息
  git commit -m "提交"

4）推送到远程
  git push origin master


三、 常见命令
  git branch -r  //查看远程所有分支
  
  git branch //查看本地所有分支
  
  git branch -a //查看本地及远程的所有分支
  
  git fetch  //将某个远程主机的更新，全部取回本地
  
  git remote -v //查看仓库关联情况
  
  git status //查看git状态



注意事项：
上传文件还要注意的是github上传文件限制了100.00MB以内，超过50.00MB小于100.00MB会进行warning，超过100.00MB会进行error错误，如果上传大型数据集需要注意查找上传大文件的方式，因为没有报错，所以我也没尝试。
