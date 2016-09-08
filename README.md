##  git 入门
+ 创建版本库  ``` git init ```
+ 把文件添加到版本库 ``` git add filename.txt ```  PS:先有文件才能添加 ,注意文件名称的大小写
+ 把文件提交到仓库 ``` git commit  -m "wrote a readme file" ```  
+ 版本控制 :继续修改filenam之后
   * 现在，运行 ``` git status ``` 命令看看结果 
   * 用``` git diff ``` 这个命令看看修改的内容 
   * 提交修改和提交新文件是一样的两步，第一步是```git add ```
   * 在执行第二步``` git commit```之前，我们再运行```git status``` 看看当前仓库的状态,git status告诉我们，将要被提交的修改包括readme.txt，下一步，就可以放心地提交了。
   * 然后继续执行 ``` git  commit  -m "add something "  ``` 
   * 提交后，我们再用git status命令看看仓库的当前状态  ```  nothing to commit(working directory clean) ```



首先，登陆GitHub，然后，在右上角找到“Create a new repo”按钮，创建一个新的仓库：


在Repository name填入gitskills，其他保持默认设置，点击“Create repository”按钮，就成功地创建了一个新的Git仓库：


目前，在GitHub上的这个learngit仓库还是空的，GitHub告诉我们，可以从这个仓库克隆出新的仓库，也可以把一个已有的本地仓库与之关联，然后，把本地仓库的内容推送到GitHub仓库。


现在，我们根据GitHub的提示，在本地的learngit仓库下运行命令：

```
$ git remote add origin git@github.com:yunxileo/learngit.git
```

然后，发现报错：
```
“fatal: remote origin already exists”
```
修改命令为：```git remote add github git@github.com:yunxileo/learngit.git ```

接着push依然报错：

```
git push github master

```

之后可以用 ``` -fu ``` 命令：

```
$ git push -fu github master
```


请千万注意，把上面的yunxileo替换成你自己的GitHub账户名，否则，你在本地关联的就是我的远程库，关联没有问题，但是你以后推送是推不上去的，因为你的SSH Key公钥不在我的账户列表中。

添加后，远程库的名字就是```origin```，这是Git默认的叫法，也可以改成别的，但是```origin```这个名字一看就知道是远程库。


下一步，就可以把本地库的所有内容推送到远程库上：

