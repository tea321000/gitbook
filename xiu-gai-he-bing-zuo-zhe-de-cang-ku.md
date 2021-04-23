# 修改&合并作者的仓库

## 修改仓库

1.首先把作者的仓库fork到自己的账号下

2.使用

```text
git clone xxx.git
```

把自己的仓库clone到本地（最好使用.git而不是http，这样在后面update的时候可以免输账号密码）

3.（可选）参考

{% page-ref page="chuang-jian-bing-lian-jie-yuan-cheng-cang-ku.md" %}

一节来配置ssh公私钥

4.修改完成后先添加新增或进行修改的文件，再commit后push到远端

```bash
git add .
git commit -m "xxx"
git push
```

## 合并仓库

当作者更新了自己的仓库后，想把自己fork的仓库更新到作者update的版本，需要先建立一个branch，然后把作者的远端pull到自己的那个branch中，再把那个branch与master进行merge：

```bash
#-b创建并切换分支
git checkout -b test
#为要pull的远端分支起别名upstream
git remote add upstream https://location/of/generic.git
#拉取upstream的master分支
git pull upstream master
#切换回本地主分支
git checkout master
#与test分支合并
git merge test
#最后可以删掉新增加的分支test
git branch -d test
```

