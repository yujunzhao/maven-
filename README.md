maven安装（前提需要下载好jdk）

首先在maven官网https://maven.apache.org/download.cgi下载安装包。

在终端解压 tar -zxvf ****

配置环境变量
在/etc/profile添加

export MAVEN_HOME=/home/zyj/idea_maven/apache-maven-3.9.1
export PATH=$MAVEN_HOME/bin:$PATH

执行source /etc/profile保存生效
最后mvn --version 查看是否安装成功

配置本地仓库和阿里云镜像
新建一个repo文件夹，把其当做仓库里
<localRepository>/home/zyj/idea_maven/apache-maven-3.9.1/repo</localRepository>

然后找到<mirror>在其下面配置镜像(在3.8以上好像都有配置镜像，删除后再添加）
  
<mirror>
  <id>aliyunmaven</id>
  <mirrorOf>*</mirrorOf>
  <name>阿里云公共仓库</name>
  <url>https://maven.aliyun.com/repository/public</url>
</mirror>
  
最后就完成了
  
中途出现了一些错误，也不太清楚原因，只是在bash下执行了一遍source /etc/profile就OK了。
