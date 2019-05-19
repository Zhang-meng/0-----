# Linux命令记录

# 1、基本命令

查看当前目录下的文件和文件夹：ls

查看当前目录：pwd

创建文件：touch file

复制文件：cp file1 file2 ()

移动文件：mv file1 file2 (结果为将file1重命名为file2)

删除文件：rm file1

创建目录：mkdir dir

复制目录：cp -r dir1 dir2

移动目录： mv dir1 dir2(如果dir2存在，则结果为移动，否则结果重命名)

删除目录：rm -r dir1

# 2、其他命令

## 1、sshd服务相关

1、Ubuntu下安装sshd服务：先输入命令sshd回车，如果没装按照提示进行命令输入：sudo apt-get install openssh-server

2、CentOS7中使用:yum install openssh-server进行安装，

3、  打开sshd服务：service sshd start

​		关闭sshd服务 ：service sshd stop

​		重启命令:	service sshd restart

​		查看当前sshd状态：service sshd status

​		查看本机IP：ifconfig

# 3、用户操作命令

## 		在root权限下可以进行用户的增加、删除、修改密码等操作：

## 1、创建用户： adduser zmm1

## 2、修改当前用户的密码：passwd zmm1

## 2、查看当前用户：whoami

## 3、删除当前用户：userdel -f zmm1

​	删除时userdel后的参数有 -f :(强制删除用户，不管他在不在线)和-r（删除用户的工作目录）





# 4、linux下的安装与卸载软件相关

​		yum(全称Yellow dog Updater ,Modeified)是一个在fedora和RedHat以及CentOS中的shell前端软件包管理器。基于RPM包管理，能够从指定的服务器自动下载RPM包并且安装，可以自动处理依赖关系，并且一次安装所有依赖包的软件包，无需繁琐的一次次的下载按装。

## 常用的yum命令

1、显示已经安装的软件包列表：yum list installed

2、查找可以安装的软件包：yum list git(以git为例)

3、安装软件包：yum install git（以git为例）

4、卸载软件包：yum remove git

5、列出软件包的依赖：yum deplist  git

6、显示软件包的描述信息和概要信息：yum info git

7、升级软件包：yum update(所有安装包)，yum update git(某个安装包)，yum check-update(检查可更新的软件包)

8、查找安装软件所在路径：whereis git（是通过本地架构好的数据库索引查找会比较快。如果没有更新到数据库里面的文件或命令则无法查找到信息） ，which git(通过PATH环境变量查找可执行文件路径，用于查找指向这个命令所在的文件夹)

## Ubantu下

6、常用apt命令
apt-cache search # ------(package 搜索包)
apt-cache show #------(package 获取包的相关信息，如说明、大小、版本等)
sudo apt-get install # ------(package 安装包)
sudo apt-get install # -----(package - - reinstall 重新安装包)
sudo apt-get -f install # -----(强制安装?#"-f = 
--fix-missing"当是修复安装吧...)
sudo apt-get remove #-----(package 删除包)
sudo apt-get remove - - purge # ------(package 删除包，包括删除配置文件等)
sudo apt-get autoremove --purge # ----(package 
删除包及其依赖的软件包+配置文件等（只对6.10有效，强烈推荐）)
sudo apt-get update #------更新源
sudo apt-get upgrade #------更新已安装的包
sudo apt-get dist-upgrade # ---------升级系统
sudo apt-get dselect-upgrade #------使用 dselect 升级
apt-cache depends #-------(package 了解使用依赖)
apt-cache rdepends # ------(package 
了解某个具体的依赖?#当是查看该包被哪些包依赖吧...)
sudo apt-get build-dep # ------(package 安装相关的编译环境)
apt-get source #------(package 下载该包的源代码)
sudo apt-get clean && sudo apt-get autoclean # --------清理下载文件的存档 
&& 只清理过时的包
sudo apt-get check #-------检查是否有损坏的依赖



# 5、SecureCRT远程登录软件客户端功能



## 1、远程登录服务器，可以在客户端操控服务器端。

## 2、zmodem功能，客户机和服务器之间的文件上下载功能。

​	在服务器linux系统命令行用**rz**（对服务那边来说是接收）；sz file（对服务那边来说是发送file是要发送的文件名）；