maven安装（前提需要下载好jdk）

首先在maven官网https://maven.apache.org/download.cgi下载安装包。

在终端解压 tar -zxvf ****

配置环境变量
在/etc/profile添加

export MAVEN_HOME=/home/zyj/idea_maven/apache-maven-3.9.1
#
export PATH=$MAVEN_HOME/bin:$PATH

执行source /etc/profile保存生效
最后mvn --version 查看是否安装成功

配置本地仓库和阿里云镜像
新建一个repo文件夹，把其路径放在localRepository当做仓库。

然后找到<mirror>在其下面配置镜像(在3.8以上好像都有配置镜像，删除后再添加）
镜像在https://developer.aliyun.com/mvn/guide有配置指南
  
每次重新开终端时都要重新source ，好烦啊，还为解决~
