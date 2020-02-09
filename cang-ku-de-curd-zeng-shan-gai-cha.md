# 仓库的CURD（增删改查）

按照前面的步骤我们已经获得了远程仓库的本地克隆，接下来进行增删改查操作。首先我们尝试**新建**一个txt文件并提交到本地git索引中：

```text
me@DESKTOP-02FTDM3 MINGW64 ~/OneDrive - email.szu.edu.cn/git/repo (master)
$ echo "hello world" > hello.txt && git add hello.txt
```

这里我们在该文件夹下新建了写有hello world内容的hello.txt，并且**git add**将这个文件添加到了本地git的文件索引中，git的文件索引保存了目录工作树的快照，之后每次该文件内容发生改变（SHA值发生改变），文件索引都会将改动记录下来。在远程提交前可以进行多次**git add**并将内容一次性进行远程提交。

要想从本地git索引中删除文件，则使用**git rm**指令：

```text
$ git rm hello.txt
```

在本地索引添加了新文件之后，我们需要在推送到远程仓库前先进行**git commit**本地提交，在提交注释中简要说明本次提交所做的更改，然后再进行**git push**远程推送：

```text
$ git commit -m "提交注释"
$ git push -u origin master
```

第一次执行git push远程推送时必须加上-u参数，后面接远程仓库的short name以及分支名，在这里是**origin**以及**master**。仓库刚建立的时候只有**master**主分支，一般完整的仓库版本迭代需要稳定版**master**主分支，带有比较激进特性的**dev**分支，以及**dev**分支开发过程中一些出现bug还没修好的中间分支。在中间分支完成后合并到dev分支，经过一段时间后再合并到master分支完成一次更新。详情可见如下链接，里面的图非常生动形象。

{% embed url="https://nvie.com/posts/a-successful-git-branching-model/" %}



