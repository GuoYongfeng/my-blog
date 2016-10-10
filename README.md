# 使用Git和Github来拉近和大牛的距离

## 介绍

- GitHub 是一个面向开源及私有软件项目的托管平台，因为只支持 Git 作为唯一的版本库格式进行托管，故名 GitHub。
- Git是一款免费、开源的分布式版本控制系统，用于敏捷高效地处理任何或小或大的项目。
- 和大家一起熟悉github和git的基本使用
- 使用git快速参与项目开发

## 跳上github这艘大船

- 基本的账号注册
- 找到一些流行的开源项目、获取第一手资料
- follow一些技术牛人，持续关注他们的动态，以及关注一些感兴趣的项目
- 创建仓库，以及github上可对项目的基本操作
- 未来是否你也有兴趣参与开源

## git安装和基本使用

- 下载：http://git-scm.com/downloads
	- windows用户下载安装后可以直接打开git bash客户端使用
- 基本的config，还有很多
	- username & email
- 创建仓库
	- init or clone
- git 基本操作
![enter image description here](http://www.ruanyifeng.com/blogimg/asset/2015/bg2015120901.png)

## remote 远程操作

在管理Git项目上，很多时候都是直接使用https url克隆到本地，当然也有有些人使用SSH url克隆到本地。这两种方式的主要区别在于：
- 使用https url克隆对初学者来说会比较方便，复制https url然后到git Bash里面直接用clone命令克隆到本地就好了，但是每次fetch和push代码都需要输入账号和密码，这也是https方式的麻烦之处。
- 而使用SSH url克隆却需要在克隆之前先配置和添加好SSH key，因此，如果你想要使用SSH url克隆的话，你必须是这个项目的拥有者。否则你是无法添加SSH key的，另外ssh默认是每次fetch和push代码都不需要输入账号和密码，如果你想要每次都输入账号密码才能进行fetch和push也可以另外进行设置。

公钥、私钥

### 解决问题

- git remote
```
# 查看remote
git remote -v
# 删除remote
git remote rm origin
# 添加remote

```
- ssh keys
查看本地是否有SSH Key
```
cd ~/.ssh
ls
```
如果没有就生成一个
```
ssh-keygen -t rsa -C "guoyff@yonyou.com"
```
- 在github上，settings->ssh keys->add

## git 分支操作

有人把 Git 的分支模型称为“必杀技特性”，而正是因为它，将 Git 从版本控制系统家族里区分出来。Git 有何特别之处呢？Git 的分支可谓是难以置信的轻量级，它的新建操作几乎可以在瞬间完成，并且在不同分支间切换起来也差不多一样快。和许多其他版本控制系统不同，Git 鼓励在工作流程中频繁使用分支与合并，哪怕一天之内进行许多次都没有关系。

理解分支的概念并熟练运用后，你才会意识到为什么 Git 是一个如此强大而独特的工具，并从此真正改变你的开发方式。

```
# 创建分支
git branch branch_name
# 本地切换到这个分支
git checkout branch_name
```

```
# 创建并且直接切换到这个新分支
git checkout -b branch_name
```

```
# 分支合并，比如将分支develop合并到master分支
git checkout master
git merge master develop
```

![enter image description here](http://image.beekka.com/blog/201207/bg2012070506.png)
