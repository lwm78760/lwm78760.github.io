---
layout:     post                    # 使用的布局（不需要改）
title:      github+typora+PicGo建立实时上传图片的图床               # 标题 
subtitle:   Hello typora, Hello PicGo     #副标题
date:       2020-04-15              # 时间
author:     lwm78760                      # 作者
header-img: img/post-bg-2015.jpg    #这篇文章标题背景图片
catalog: true                       # 是否归档
tags:                               #标签
    - github
    - typora
    - PicGo
    - 图床
---



参考

[manjaro19.0.2+typora+PicGo](https://www.cnblogs.com/Justdocument/p/12552317.html)

[手把手教你用Typora自动上传到picgo图床【教程与排坑】](https://www.jianshu.com/p/4cd14d4ceb1d)

[PicGo踩坑记（上传失败，服务端出错，请重试）](https://blog.csdn.net/TalesOV/article/details/104450037)

### 一、下载

##### 下载PicGo

**[作者github的release地址](https://github.com/Molunerfinn/PicGo/releases)**

![img](https://raw.githubusercontent.com/lwm78760/github-picgo-typora/master/imgs/qoHNTIx3OtV1Cr7-1586942379084.png)

​		或者听从[作者建议](https://github.com/Molunerfinn/PicGo)

​		**还可以使用 [Scoop](https://scoop.sh/) 来安装 PicGo: `scoop bucket add helbing https://github.com/helbing/scoop-bucket` & `scoop install picgo`。 感谢 @helbing 的贡献！**

​		**还可以使用 [Chocolatey](https://chocolatey.org/) 来安装 PicGo: `choco install picgo`。 感谢 @iYato 的贡献！**

##### 下载typora

[进入官网](https://www.typora.io/)下载typora

![image-20200415172706373](https://raw.githubusercontent.com/lwm78760/github-picgo-typora/master/imgs/image-20200415172706373.png)

### 二、建立github图床仓库

##### 1.创建GitHub图床之前，需要注册/登陆GitHub账号

##### 2. 创建Repository，点击"New repository"按钮，进行设置

![image-20200415174228662](https://raw.githubusercontent.com/lwm78760/github-picgo-typora/master/imgs/image-20200415174228662.png)

> 为repository初始化一个README.md文件可以根据需求选择，非必选

##### 3.生成一个Token用于操作GitHub repository

点击settings

进入页面后，点击"Developer settings"按钮

进入页面后，点击"Personal access tokens"按钮

![image-20200415174402787](https://raw.githubusercontent.com/lwm78760/github-picgo-typora/master/imgs/image-20200415174402787.png)



创建新的Token

![img](https://raw.githubusercontent.com/lwm78760/github-picgo-typora/master/imgs/3146329-2cddeffa8fe35933.png)

填写描述，选择"repo",然后点击"Generate token"按钮

> 注：创建成功后，会生成一串token，这串token之后不会再显示，所以第一次看到的时候，就要好好保存。我的token有时会失效，所以有时不能上传可以看看token。

### 三、 配置图床

##### 1.打开PicGo，点击github图床进行配置

![image-20200415175029649](https://raw.githubusercontent.com/lwm78760/github-picgo-typora/master/imgs/image-20200415175029649.png)

+ 设定仓库名的时候，是按照“账户名/仓库名的格式填写”
+ 分支名统一填写“master”,即github的主分支
+ 将之前的Token黏贴在这里
+ 存储的路径可以按照我这样子写，就会在repository下创建一个“imgs”文件夹
+ 自定义域名的作用是，在上传图片后成功后，PicGo会将“自定义域名+上传的图片名”生成的访问链接，放到剪切板上`https://raw.githubusercontent.com/用户名/RepositoryName/分支名，`，自定义域名需要按照这样去填写

##### 2.快捷键及相关配置

![image-20200415175400066](https://raw.githubusercontent.com/lwm78760/github-picgo-typora/master/imgs/image-20200415175400066.png)

注：可以将快捷键设置为`ctrl+shift+c`

### 四、如何在typora中设置拖入图片自动上传

这篇文章讲的很详细，还有动图，但是这是在windows上的。

[手把手教你用Typora自动上传到picgo图床【教程与排坑】](https://www.jianshu.com/p/4cd14d4ceb1d)

打开typora，点开左上角文件，选择**偏好设置**

1. 设置插入图片时为【上传图片】
2. 勾选【对本地位置的图片应用上述规则】
3. 在上传服务中选择“PicGo(app)”
4. 在路径中选择picgo安装目录**PicGo.exe**

![image-20200415175850187](https://raw.githubusercontent.com/lwm78760/github-picgo-typora/master/imgs/image-20200415175850187.png)

上传的方法也很简单，将图片复制进去typora就会自动帮你上传了，你也可以右键点击上传图片。

![img](https://raw.githubusercontent.com/lwm78760/github-picgo-typora/master/imgs/20524049-bfad2dcc0c1060df.gif)

改为复制到指定路径

![image-20200415200325429](https://raw.githubusercontent.com/lwm78760/github-picgo-typora/master/imgs/image-20200415200325429.png)

我的复制，会自动到复制到指定目录，会有提示上传图像

![image-20200415200048080](https://raw.githubusercontent.com/lwm78760/github-picgo-typora/master/imgs/image-20200415200048080.png)

上传后的路径

![image-20200415200157626](https://raw.githubusercontent.com/lwm78760/github-picgo-typora/master/imgs/image-20200415200157626.png)

可以在【格式】->【图像】->【上传所有图片】

![img](https://raw.githubusercontent.com/lwm78760/github-picgo-typora/master/imgs/20524049-51b15429b5affad8.png)



### 常见错误

##### 1.typora错误

1. **`Failed to fetch`**

![img](https://raw.githubusercontent.com/lwm78760/github-picgo-typora/master/imgs/20524049-f35b8bff8320b838.webp)

> 这个错误一般是由端口设置错误造成的。
>
> ***解决办法：*** 打开picgo设置，点击设置Server选项，**将端口改为36677端口**，这是picgo推荐的默认端口号，然后保存，成功。
>
> 有的时候端口会变成366771，问题在于你打开了多个picgo程序，picgo会自动帮你把36677端口改为366771端口。

1. **`{"success",false}`**

![img](https://raw.githubusercontent.com/lwm78760/github-picgo-typora/master/imgs/20524049-f13e449f45c83bb8.webp)

> 这个错误相信也有很多小伙伴遇到了，原因是**文件名冲突**了，如果你上传过一张image1.jpg的图片，再上传名称一样的图片就会失败，康康log文件(感谢日志！)里也写到了。
>
> *解决办法*：办法也很简单，打开picgo设置，将**【时间戳重命名】打开**。

ps:整个过程的bug非常多，让我非常痛苦。最后完成的效果：可以拖进typora上传，但是图片地址依然是本地地址，无法自动变成网络地址。
 所以文章中的图片还是我拖入PicGo之后再进入typora粘贴链接地址（上传成功会自动复制进粘贴板）。

如果你有问题可以在评论中和我交流。希望尽我所能向你提供帮助，亦或从你这学习到如何修复这个bug。

##### 2.图床设置的问题

1. 首先在确保你的GitHub图床设置路径准确无误的情况下：

   + 再次检查你的仓库名是否正确
   + 仓库名不能出现空格！！如果一定要有空格请用 **-** 来代替（因为GitHub中的空格默认换成-）
   + 不要出现一些奇怪的符号！
   + 我的token有时会失效，所以有时不能上传可以看看token。

2. 上传文件的问题

   + 同上，文件名不要包含空格！

   + 文件名不要包含奇怪的字符（**加**乘百分号等等）

3. 间歇性上传失败

   这种情况是以上都没问题，并且之前成功上传过，突然就不能上传了。

   打开PicGo的**设置-设置server**

   ![img](https://raw.githubusercontent.com/lwm78760/github-picgo-typora/master/imgs/20200222203320.png)

   把这个开关，开换成关，关换成开（别问为什么，问就是不知道反正有效。。）

   ![img](https://raw.githubusercontent.com/lwm78760/github-picgo-typora/master/imgs/20200222203337.png)

4. 仍然没有解决

   这种情况，咱就只能依靠玄学了

   - 重启应用
   - 重启电脑
   - 如果使用代理了，全局或直连试一下

### 五、使用smms图床

1. **首先你需要在插件设置中下载 `smms-user` 的插件**

    ![img](https://raw.githubusercontent.com/lwm78760/github-picgo-typora/master/imgs/C51bhKfY7m3qXHP.png)

2. **点击图标，会把你引向这个插件的github主页 [picgo-plugin-smms-user](https://github.com/xlzy520/picgo-plugin-smms-user#readme)**

    **详细阅读文档后你需要：**

```shell
Copy# 1.进入 ~/.config/picgo/ 目录
cd ~/.config/picgo/

# 2.克隆该项目(我是用了proxychains)
proxychains git clone https://github.com/lwm78760/picgo-plugin-smms-user.git

# 3.安装这个插件
npm install ./picgo-plugin-smms-user
```

- 重启应用 你会获得一个**新的图床设置**，这里的Auth需要你去 [sm.ms](http://sm.ms) 注册一个账号并获得一个

  `secret token `

![img](https://raw.githubusercontent.com/lwm78760/github-picgo-typora/master/imgs/Vu6xdcjXsSARGDv.png)