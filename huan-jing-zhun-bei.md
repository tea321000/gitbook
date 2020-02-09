---
description: 系统的准备
---

# 环境准备

1. 首先我们需要一个linux发行版，常用的linux distribution包括Ubuntu，Centos，RedHat等，国内也有一些例如deepin的比较有特色的发行版，建议尽量使用国际上比较常用的发行版，这样在遇到问题Google时可以比较容易能找到解决方案。本教程基于Ubuntu 18.04.3进行讲解，最新的Ubuntu版本可以从[https://ubuntu.com/download](https://ubuntu.com/download) 中进行下载。
2. 假如需要使用GPU的CUDA或者NVIDIA-doker进行神经网络相关训练的话，建议以实机方法进行系统安装而不要使用虚拟机，暂时windows还不能通过hyper-V等方式虚拟化GPU资源，原因不明，推测可能与windows没有开放相关API权限有关。实机的安装需要单独给Ubuntu划分一个磁盘分区，Ubuntu官方推荐使用rufus进行U盘系统安装：[https://rufus.ie/](https://rufus.ie/)
3. 假如需要在虚拟机中进行安装，建议使用Oracle甲骨文公司的virtualBox VM：[https://www.virtualbox.org/](https://www.virtualbox.org/)，不需要像VMware进行额外的破解。此外，可以通过1.的链接下载镜像后安装系统，也可以Google一些别人安装好后上传的虚拟镜像文件直接导入从而节省安装的时间，类似：[https://www.osboxes.org/ubuntu/](https://www.osboxes.org/ubuntu/)



