---
layout:     post                    # 使用的布局（不需要改）
title:      GithHub Desktop管理GitHub仓库               # 标题 
subtitle:   Hello world, Hello GithHub Desktop     #副标题
date:       2020-04-15              # 时间
author:     lwm78760                      # 作者
header-img: img/post-bg-2015.jpg    #这篇文章标题背景图片
catalog: true                       # 是否归档
tags:                               #标签
    - github
    - GithHub Desktop
---

参考

https://www.jianshu.com/p/06a960d991aa

### 利用GithHub Desktop管理GitHub仓库

​		[GithHub Desktop](https://desktop.github.com/) 是 **GithHub** 推出的一款管理GitHub仓库的桌面软件，换句话说就是将你在**Github**上的文件同步到本地电脑上，并将修改后的文件同步到**Github**远程仓库。

##### 1.下载

进入[下载](https://desktop.github.com/)页面，选择对应的平台进行下载，安装，登录，输入你的**GitHub**账号和密码进行登录，一路Continue。

![image-20200415202120311](https://raw.githubusercontent.com/lwm78760/github-picgo-typora/master/imgs/image-20200415202120311.png)

##### 2.现在选择仓库

![image-20200415203107406](https://raw.githubusercontent.com/lwm78760/github-picgo-typora/master/imgs/image-20200415203107406.png)

之间建立好的项目仓库远程克隆，复制地址，

也可以点击下载zip到本地进行本地添加

![image-20200415203324856](https://raw.githubusercontent.com/lwm78760/github-picgo-typora/master/imgs/image-20200415203324856.png)

选择URL仓库地址及本地保存地址

![image-20200415203609125](https://raw.githubusercontent.com/lwm78760/github-picgo-typora/master/imgs/image-20200415203609125.png)

导入后也可以在软件里导入

![image-20200415211106653](https://raw.githubusercontent.com/lwm78760/github-picgo-typora/master/imgs/image-20200415211106653.png)

##### 3.界面介绍

如果你打开这个软件后，会发现应该如下所示。 左边的是可以切换添加进来的仓库，再也不需要cd来cd去了，白色框内是改变提醒，下面是提交修改。所以整个工作流程是有修改直接commit就行了。

![image-20200415210521513](https://raw.githubusercontent.com/lwm78760/github-picgo-typora/master/imgs/image-20200415210521513.png)

##### 4.提交改变

当你对仓库文件夹的文件下进行修改、添加或删除时，都可以在 **GitHub Desktop** 中看到改变，提示提交，提交后可以看到提交历史history

![image-20200415214914949](https://raw.githubusercontent.com/lwm78760/github-picgo-typora/master/imgs/image-20200415214914949.png)

##### 5.同步

点击按钮进行远程推送，看到了吧，现在显示本地没有改变，但是上面push origin显示了1，代表的是我们与远程的github不同步，本地有一个更新，就是我们新加的本地改变，但是github并没有更新，推送远程分支我之后会讲。

![image-20200415215033304](https://raw.githubusercontent.com/lwm78760/github-picgo-typora/master/imgs/image-20200415215033304.png)

##### 6.完成

打开你的GitHub上的仓库，你就可以看到已经和本地同步了

##### 7.更新本地仓库

比如说现在远程仓库已经被更新了，有可能是你的同事提交了他的一部分，但是在你的本地仓库并没有更新，现在怎么办呢？ 很简单，一键fetch

![image-20200415220816205](https://raw.githubusercontent.com/lwm78760/github-picgo-typora/master/imgs/image-20200415220816205.png)

好啦～点击pull origin就可以把远程的更新到本地了~ 看看里面的history就知道干了些什么了。

![image-20200415221000505](https://raw.githubusercontent.com/lwm78760/github-picgo-typora/master/imgs/image-20200415221000505.png)

##### 8.版本回退

有很多时候我们在当前这一步骤做了一些不可挽回的错误，比如说删除了重要的文件以后再也找不到了，这时候使用版本回退可以回退到任何一个commit过的状态。

打开history你会发现有很多commit后的历史记录,其中有我们之前的update。所以右键它会显示revet this commit

![image-20200415221142260](https://raw.githubusercontent.com/lwm78760/github-picgo-typora/master/imgs/image-20200415221142260.png)

好了，现在看看你的文件夹吧 :> 是不是回来了呢？

##### 9.创建分支、合并分支

我们尝试创建一个新的分支，点击new，创建一个分支，如果你现在仔细观察的话会发现原来的master分支变成了新分支

![image-20200415221412413](https://raw.githubusercontent.com/lwm78760/github-picgo-typora/master/imgs/image-20200415221412413.png)

现在我想把它合并到我原来的master分支，那怎么做呢？ 首先打开branch选项，点击其中的merge into curren branch(当前处于master分支,永远都是把其他分支merge到当前！) ，然后选择一个新分支

![image-20200415221734431](https://raw.githubusercontent.com/lwm78760/github-picgo-typora/master/imgs/image-20200415221734431.png)



##### 注意

​		你在 **GitHub** 网站上进行 **Commit** 操作后，需要在**GitHub Desktop**上按一下 **同步按键** 才能同步网站上的修改到你的本地。

