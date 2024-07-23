---
title: hexo博客搭建教程(1)
date: 2024-07-23 12:15:05
categories: 技术
tags:
  - 博客搭建
cover: https://r2.haier-mail.com/imghost/2024/07/v2-7827197bfa0023932d428633d41372fd_180x120.jpg
---
你是否想拥有一个属于自己的博客？你是否还在为部署博客网站需要服务器而发愁？这里是一篇教程，讲述了如何免服务器，仅使用少量指令，就能搭建一个属于自己的博客网站。
<!--more-->
# 前言
这篇教程主要讲述了你所看到的这个我自己的博客网站的搭建过程。也包括了我在搭建过程中遇到的一些问题和解决方法。博客采用的是Hexo框架配合github的pages功能，从而免去了购买服务器的麻烦。但是这种方法搭建的博客为静态网站([静态网站和动态网站的差异](https://www.bilibili.com/read/cv27216434/))，因此编辑文章等操作，均需要在本地进行。
以下是Hexo官网
>[hexo](https://hexo.io/zh-cn/)

博客会部署在github pages上，关于github pages的介绍请看下面链接。
>[2023年最新 Github Pages 使用手册-CSDN博客](https://blog.csdn.net/SiShen654/article/details/132471133)

如果你之前从来没听说过这两个东西，怎么办？没关系，只需要按照下面操作步骤操作，最后，也可以轻松的创建一个自己的博客网站。
如果你觉得下方教程太过于复杂，可以去Hexo官网参照[官方的教程](https://hexo.io/zh-cn/docs/)来进行博客配置。

# 博客部署教程
本文主要介绍hexo框架的安装，初始化，以及如何部署到GitHub pages
更换主题，博客简单配置，请见后续教程。

## Hexo简介
本博客的搭建是依靠Hexo完成的，那么什么是Hexo呢？借用官网的话来说，Hexo是一个快速、简洁且高效的博客框架。Hexo使用Markdown来解析博客文章，能很高效快速的生产一个博客网页，更重要的是，Hexo框架支持第三方主题，你可以在他的[主题网站](https://hexo.io/themes/)寻找自己喜欢的主题，来个性化自己的博客。

## Hexo框架的安装

### Git的安装

本博客由于会部署到github上，因此，在部署过程中会用到Git这个软件，那么Git是什么呢？Git是一个分布式的版本控制软件，通俗点来说，就是一个帮你备份、管理源代码或文本文档的软件，同时，它还支持把代码推送到远程服务器，以及从远程服务器拉取代码，从而实现云同步的功能。当然，Git的功能远不止这些。有关Git更详细的介绍，以及Git的使用教程，请看廖雪峰大大的教程：
> [Git教程](https://www.liaoxuefeng.com/wiki/896043488029600)

这里以Windows系统为例：
在Windows上使用Git，可以从Git官网直接[下载安装程序](https://git-scm.com/downloads)，然后按默认选项安装即可。

**1.进入Git官网，选择windows版本**
![image.png](https://r2.haier-mail.com/imghost/2024/07/202407021639742.png)

**2.点击下载链接**
![image.png](https://r2.haier-mail.com/imghost/2024/07/202407021622169.png)

**3.一路next，默认安装即可。**
![image.png](https://r2.haier-mail.com/imghost/2024/07/202407021642812.png)

**4.初次使用的配置**
在安装完Git后，还需要进行一些简单的配置，这里还需要配置本地电脑的用户名和邮箱，用来区分不同机器。可以在任意目录下右键选择Open Git Bash here 或者在开始菜单里找到Git->Git Bash，打开Git的命令行。然后输入以下指令：
```bash
git config --global user.name "Your Name"
git config --global user.email "email@example.com"
```
（注意将Your Name 和 email@example.com换成你自己想取的名字和自己的邮箱）

输入完后可以执行以下命令检查配置是否正确
```bash
git config user.name
git config user.email
```


其他系统安装可以参考上面[Git教程](https://www.liaoxuefeng.com/wiki/896043488029600/896067074338496)中的安装步骤。

### Node.js的安装

[nodejs官网](https://nodejs.cn/download/)也为大多数系统提供了官方的安装包，这里还是以Windows为例：

**1.进入[官网](https://nodejs.cn/download/)，下载Windows版本。**
![image.png](https://r2.haier-mail.com/imghost/2024/07/202407081546569.png)

**2.运行安装程序，点击Next，接受协议，然后点击Next。**
![image.png](https://r2.haier-mail.com/imghost/2024/07/202407081547418.png)
![image.png](https://r2.haier-mail.com/imghost/2024/07/202407081553630.png)

**3.选择安装路径，可以自己在其他盘创建一个文件夹（路径最好是全英文），然后点击next**
![image.png](https://r2.haier-mail.com/imghost/2024/07/202407081555048.png)

**4.这里一定要选择Add to Path，随后点击Next，默认安装即可**。
![image.png](https://r2.haier-mail.com/imghost/2024/07/202407081625859.png)

**5.验证Node.js**
我们可以在任意路径下点击鼠标右键，选择Open Git Bash here，打开Git的终端。
![image.png](https://r2.haier-mail.com/imghost/2024/07/202407081602305.png)
然后在终端里输入以下指令：
```Bash
node -v
npm -v
```
能够看到版本号就说明安装配置成功了，如果不行，请重新安装Node.js，并检查是否选择了Add to Path。
![image.png](https://r2.haier-mail.com/imghost/2024/07/202407081621788.png)

### Hexo的安装
在上述步骤都完成后，我们就可以正式安装Hexo框架了，我们在Git Bash中执行以下命令，即可安装Hexo
```bash
npm install -g hexo-cli
```
安装完还可以执行以下命令，查看是否成功安装
```bash
hexo -v
```
能够输出版本号就说明安装成功。
![image.png](https://r2.haier-mail.com/imghost/2024/07/202407111641835.png)

## 博客的搭建

### 初始化Hexo
Hexo在安装完成后，要使用他需要先初始化，这里你可以在一个喜欢的位置创建一个文件夹，然后打开文件夹，打开Git Bash，输入以下指令，等待一小段时间后，博客就完成了初始化，文件夹内也会多出来很多博客的配置文件。

```bash
hexo init
```
![image.png](https://r2.haier-mail.com/imghost/2024/07/202407111652163.png)

项目文件说明：

| 项目文件         | 说明        |
| ------------ | --------- |
| node_modules | 依赖包       |
| source       | 用来存放你的文章  |
| themes       | 主题        |
| _config.yml  | 博客的配置文件   |
| public       | 存放生成的页面   |
| scaffolds    | 生成文章的一些模板 |

### Hexo的基本使用

#### 常用指令
首先，这里先介绍几个hexo常用的指令。
启动本地服务器，可以用来预览当前博客网站。
```bash
hexo s
```
生成博客网站的文件
```bash
hexo g
```
部署博客网站
```bash
hexo d
```
生成博客文件并推送
```bash
hexo g -d
```
清理生成的博客网站文件
```bash
hexo clean
```
创建文章或页面
```bash
hexo new post 文章名
hexo new page 页面名
```

#### 网站预览
初始化完成后，输入如下指令,然后浏览器输入网址http://localhost:4000/就可以预览当前博客网站了。
```bash
hexo g
hexo s
```
![image.png](https://r2.haier-mail.com/imghost/2024/07/202407222326422.png)
![image.png](https://r2.haier-mail.com/imghost/2024/07/202407222326980.png)
在终端中按下ctrl+c 可以关闭本地服务器。

#### 简单配置
博客的文章放在source/_posts文件夹里

要修改博客网站的信息，可以修改博客目录下的_config.yml文件
要修改主题的配置，有两种方法
第一种方法是参照对应主题的配置，将配置内容直接写在博客目录的_config.主题名.yml文件内，这样，主题会自动合并配置文件内容，从而更改主题配置。
第二种方法是找到主题的存放目录，然后修改主题目录下_config.yml文件的内容。
目前来说，更推荐第一种方法来修改主题配置，这样可以防止主题出现问题。

关于主题配置，请更具自己选择的主题的官方介绍来进行配置。
在下一篇文章中，我也会介绍我所使用的主题的安装方法和一些简单配置。
这里推荐一些大佬关于其他主题的配置教程。
[Hexo + GitHub史上最全搭建个人blog教程_hexo+github博客搭建教程 gao-CSDN博客](https://blog.csdn.net/qq_42000293/article/details/132377152)
（next主题）
[【Hexo】Hexo搭建Butterfly主题并快速美化_hexo butterfly-CSDN博客](https://blog.csdn.net/mjh1667002013/article/details/129290903?ops_request_misc=&request_id=&biz_id=102&utm_term=hexo%E4%B8%BB%E9%A2%98%E8%AE%BE%E7%BD%AE&utm_medium=distribute.pc_search_result.none-task-blog-2~all~sobaiduweb~default-0-129290903.142^v100^control&spm=1018.2226.3001.4187)
（Butterfly主题）

### 博客的部署
这里以部署到github pages为例，如果你需要部署到其他地方，大体流程也是相似的。

GitHub pages部署博客也有两种方式，一种是从分支部署，另一种是通过GitHub Actions部署。
第一种方法部署相对来说较为简单，而第二种方法则可以实现博客部署的自动化。
这里先讲解从分支部署的方法，另一种方法我也会在下一篇教程的最后讲解。

#### 1.创建Github仓库
打开github网站，创建一个GitHub仓库，注意仓库名是：用户名.github.io
![image.png](https://r2.haier-mail.com/imghost/2024/07/202407231215039.png)
![image.png](https://r2.haier-mail.com/imghost/2024/07/202407231218363.png)

#### 2.添加SSH keys
任意目录下打开Git Bash，输入以下指令(注意请换成自己Git配置的邮箱)
```bash
ssh-keygen -t rsa -C "youremail@youremail.com"
```
一路回车，然后执行以下指令，终端会输出你的密钥，复制密钥
```bash
cat ~/.ssh/id_rsa.pub
```
在Github上，点击右上角头像，选择settings，点击SSH and GPG keys
![image.png](https://r2.haier-mail.com/imghost/2024/07/202407231236448.png)
点击右边绿色的New SSH key按钮，填写密钥信息，最后点击Add SSH key，即可添加密钥
![image.png](https://r2.haier-mail.com/imghost/2024/07/202407231240817.png)
执行以下命令，可以查看设置是否成功。
```bash
ssh -T git@github.com
```

#### 3.从分支部署
首先修改站点配置文件，也就是博客目录下的_config.yml文件，可以在Github的仓库复制自己刚创建的仓库地址，然后填到对应位置。
```yaml
# Deployment
## Docs: https://hexo.io/docs/one-command-deployment
deploy:
  type: git
  repo: git@github.com:username/reponame.git
  branch: main
```
repo 填写ssh格式的仓库地址，branch填写要部署到的分支名，例如部署到默认分支main
![image.png](https://r2.haier-mail.com/imghost/2024/07/202407231315058.png)
![image.png](https://r2.haier-mail.com/imghost/2024/07/202407231320079.png)

在修改完配置文件后，还需要安装一个模块，用于部署网站。
在博客根目录下打开Git Bash，输入如下指令
```bash
npm install hexo-deployer-git --save
```
在完成上述操作后，在博客根目录打开Git Bash输入如下指令就可以上传网站文件了
```bash
hexo clean
hexo g -d
```
最后，打开GitHub仓库，点击Settings，下滑找到Github Pages，source选择Deploy from a branch，branch选择你刚刚填写的分支，这里以设置的为main分支为例。
![image.png](https://r2.haier-mail.com/imghost/2024/07/202407231333887.png)
之后，你就会得到一个 用户名.github.io 的域名，通过这个GitHub子域名，就可以访问你的博客网站了。
#### 4.设置个人域名
如果你有自己的个人域名，也可以将网站的域名设置为你的个人域名，这里简述设置的方法。
1.在你的域名的管理平台中，选择域名解析，为你的域名添加一条cname记录，记录内容为刚刚得到的GitHub的子域名。这里以阿里云为例。
![image.png](https://r2.haier-mail.com/imghost/2024/07/202407231342301.png)
2.添加完解析记录后，回到Github pages的设置页面，在Custom domain上填写自己的域名，也可以勾选下方强制使用HTTPS，增加网站的安全性。
![image.png](https://r2.haier-mail.com/imghost/2024/07/202407231344884.png)
3.最后等待配置完成，完成后，设置的上面域名变成自己的域名，就代表配置成功了。
![image.png](https://r2.haier-mail.com/imghost/2024/07/202407231347983.png)

#### 5.文章更新
部署完博客网站后，后续自己的文章可以在写完后，放在source/_posts文件夹内
然后，在博客根目录打开Git Bash，输入如下指令，完成网站文章的更新。
```bash
hexo g -d
```
有时，如果出现问题，也可以先执行以下命令，清除旧的生成文件，再进行更新。
```bash
hexo clean
```

# 结语
博客搭建和部署的基础教程到此就结束了。而我目前使用的主题的安装和配置，还有主题配置时，我遇到的一些问题和解决方法，以及使用Github Actions自动化部署博客，我将会在下一篇文章进行介绍。
敬请期待我的下一篇博客搭建教程。
![1.png](https://r2.haier-mail.com/imghost/2024/07/1.png)

