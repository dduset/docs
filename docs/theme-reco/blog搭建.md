---
title: blog的搭建
date: 2022-06-15 17:45
---



# Blog的搭建

## 下载官方的安装包vuepress-reco

> https://github.com/vuepress-reco/vuepress-theme-reco-demo/tree/demo/1.x

下载后解压到目录



## 项目初始化

### 安装npm

```
npm install
```

### 创建博客工程

```
#安装脚手架工具
npm install @vuepress-reco/theme-cli -g
#创建项目
theme-cli init my-blog #my-blog 可替换成自己需要的项目名称
```

输入后会出现一些信息配置：

![1655284492727](C:\Users\Administrator\AppData\Roaming\Typora\typora-user-images\1655284492727.png)

![1655284441352](C:\Users\Administrator\AppData\Roaming\Typora\typora-user-images\1655284441352.png)



![1655285964223](C:\Users\Administrator\AppData\Roaming\Typora\typora-user-images\1655285964223.png)

### 创建好后进入工程目录，启动项目

```
#接入项目目录
cd my-blog #my-blog替换为之前你填入的项目名称

#安装npm
npm install

#运行测试环境
npm run dev
```



## 连接github

### 创建一个新的仓库（公开）

根据提示的代码进行连接

```
git init 

git add .

后面的复制
```



## 进入vercel新建项目

> https://vercel.com/

进行同步github仓库，里面会检查github的更新，然后给你一个域名进行访问



## 配置ssh远程密钥

```
#在目录页git命令行中
ssh-keygen
（一直回车，使用默认值）
```

![1655286550601](C:\Users\DELL\AppData\Roaming\Typora\typora-user-images\1655286550601.png)

密钥生成在c盘用户目录的.ssh文件夹中

![1655286728933](C:\Users\DELL\AppData\Roaming\Typora\typora-user-images\1655286728933.png)



## blog上传

```
#目录中启动git
git status #查看被修改过的文件

git add -A #将所有修改过的文件添加到暂存区中

git commit -m 备注 #添加到本地仓库中
```

