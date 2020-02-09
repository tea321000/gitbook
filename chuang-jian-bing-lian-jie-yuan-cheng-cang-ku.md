# 创建并连接远程仓库

## 免密码密钥登陆

首先在电脑硬盘上新建一个文件夹作为git仓库的目录，然后在文件夹空白处右击，选择Git Bash Here。我在这里选择的是Onedrive下的文件夹，弹出的窗口显示如下：

```
用户名@电脑名称 MINGW64 ~/OneDrive - email.szu.edu.cn/git
$
```

输入ssh-keygen生成一对公私密钥，为了使用方便，我们可以不给密钥设置单独的密码，直接回车四次：

```bash
$ ssh-keygen
Generating public/private rsa key pair.
Enter file in which to save the key (/c/Users/me/.ssh/id_rsa):
Enter passphrase (empty for no passphrase):
Enter same passphrase again:
Your identification has been saved in /c/Users/me/.ssh/id_rsa.
Your public key has been saved in /c/Users/me/.ssh/id_rsa.pub.
The key fingerprint is:

```



