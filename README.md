maven安装（前提需要下载好jdk）

首先在maven官网https://maven.apache.org/download.cgi下载安装包。

在终端解压 tar -zxvf ****

配置环境变量
在/etc/profile添加

export MAVEN_HOME=/home/zyj/idea_maven/apache-maven-3.9.1
export PATH=$MAVEN_HOME/bin:$PATH

执行source /etc/profile保存生效
最后mvn --version 查看是否安装成功
