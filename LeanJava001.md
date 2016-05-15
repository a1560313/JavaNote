#一、Java开发环境配置 （centos）

##JDK 下载安装
1.JDK下载[http://www.oracle.com/technetwork/java/javase/downloads/jdk8-downloads-2133151.html](http://www.oracle.com/technetwork/java/javase/downloads/jdk8-downloads-2133151.html)

2.jdk-8u91-linux-x64.rpm

3.安装配置

- 安装

	``` 
	yum localinstall jdk-8u91-linux-x64.rpm
	```
	
	正常情况下会安装到/usr/java/jdk1.8.0_91/bin/java
	
- 配置
      
      `vim /etc/profile`
      
      append code under in end of profile:
       
		JAVA_HOME=/usr/java/jdk1.8.0_91
		
		PATH=$JAVA_HOME/bin:$PATH
		
		CLASSPATH=.:$JAVA_HOME/lib/dt.jar:$JAVA_HOME/lib/tools.jar
		
		export JAVA_HOME
		
		export PATH
		
		export CLASSPATH
		
##tomcat 安装
- 下载tomcat zip 包
- copy 到任意项目目录下 并解压
- `chmod a+x *.sh`
- `./startup.sh`
- 127.0.0.1:8080 就可以访问（若无法访问看下面）

## 防火墙配置
- `vim /etc/sysconfig/iptables`
- append code under in end of iptables:

	`A INPUT -m state --state NEW -m tcp -p tcp --dport 8080 -j ACCEPT`