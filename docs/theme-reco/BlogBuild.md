---
title: blog的搭建
date: 2022-06-15
sidebar: 'auto'
publish: true
typora-root-url: ..\img
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

![1](W:\vuepress-reco\vuepress-theme-reco-demo-demo-1.x\my-blog\docs\img\blog\1.png)

![1655285964223](W:\vuepress-reco\vuepress-theme-reco-demo-demo-1.x\my-blog\docs\img\blog\2.png)

![3](W:\vuepress-reco\vuepress-theme-reco-demo-demo-1.x\my-blog\docs\img\blog\3.png)

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

![1655286550601](/blog/4.png)

密钥生成在c盘用户目录的.ssh文件夹中

![1655286728933](/blog/5.png)



## blog上传

```
#目录中启动git
git status #查看被修改过的文件

git add -A #将所有修改过的文件添加到暂存区中

git commit -m 备注 #添加到本地仓库中
```

### 使用ssh将本地仓库推送到远程

![1655287302235](/blog/6.png)



因为ssh比较长，所以需要起一个别名

```
git remote add origin_ssh ssh地址 #origin_ssh是别名
```

进行push

```
git push 别名 分支
```

## 写blog

```
# 新建一个 markdown 文件
echo '# Hello VuePress!' > README.md	# Hello VuePress! 内容 ，README.md 文件名，类型

# 开始写作
vuepress dev .

# 构建静态文件
npm run build
```

