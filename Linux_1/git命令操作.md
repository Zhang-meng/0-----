# Linux下的git命令意义

# 1、git的安装

## a、在Ubuntu系统下使用:sudo apt install git命令安装，

## b、在CentOs7系统下使用：yum install git 命令进行安装

## .其他版本的安方式具体参考git官网；

## https://git-scm.com/download/linux

![1557833310020](C:\Users\ZMM\AppData\Roaming\Typora\typora-user-images\1557833310020.png)

# 2 、git的使用命令

## 1、安装完成后用命令：git --version 查看是否安装成功，

例如：git version 2.20.1

## 2、进行账户信息的配置：

### git config --global user.name "Zang-meng"
git config --global user.email 1352055936@qq.com

配置完后输入下面命令进行查看是否正确

git config --list

user.name=Zang-meng

user.email=1352055936@qq.com



## 3、从github上克隆某个项目：git colone http://github.com/Zhang-meng/xml_Pro1.git

## 其中后面的链接是从想要克隆下来的项目的链接，克隆下来之后便可以进行正常的操作。![1557833924853](C:\Users\ZMM\AppData\Roaming\Typora\typora-user-images\1557833924853.png)

## 4、查看克隆下来的项目的提交版本的

详细信息：git log

简略信息：git log --oneline

## 5、查看固定作者更新的

详细信息：git log --author=*Zhang-meng*

简略信息：git log --author=*Zhang-meng* --oneline

其中“Zhang-meng”为作者的github名

## 6、查看与之前版本的不同：git --patch-with-stat

