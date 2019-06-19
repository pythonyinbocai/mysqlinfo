MySQL的Linux系统下安装
• 下载MySQL的安装包
– 在MySQL官网上下载最新版的Ubuntu Linux专用的MySQL 
– https://dev.mysql.com/downloads/mysql/
– mysql-server_5.7.17-1ubuntu16.04_amd64.deb-bundle.tar
• 解压文件,命令为：
– root@ubuntu:/fly/mysql# tar -xvf mysql-server_5.7.17-
1ubuntu16.04_amd64.deb-bundle.tar
– 解压开来后，一共有11个deb包
• 用sudo dpkg -i [包名]命令逐个安装
– 因为包与包中间存在依赖关系，这里安装有个先后顺序。

• 安装的顺序是： 
1.mysql-common_5.7.17-1ubuntu16.04_amd64.deb 
2.libmysqlclient20_5.7.17-1ubuntu16.04_amd64.deb 
3.libmysqlclient-dev_5.7.17-1ubuntu16.04_amd64.deb 
4.libmysqld-dev_5.7.17-1ubuntu16.04_amd64.deb
 5.mysql-community-client_5.7.17-1ubuntu16.04_amd64.deb 
6.mysql-client_5.7.17-1ubuntu16.04_amd64.deb 
7.mysql-community-source_5.7.17-1ubuntu16.04_amd64.deb
• 这里需要再安装一个依赖包叫libmecab2，安装好后，继续安装最
后一个： 
8.mysql-community-server_5.7.17-1ubuntu16.04_amd64.deb 
安装过程中需要设置数据库密码。 
• 到这里，所有的已经安装完毕。输入Mysql -u root -p可以登陆数
据了。

MySQL的Linux系统下安装
• 文件默认位置
– /usr/bin 客户端程序和脚本 
– /usr/sbin mysqld 服务器 
– /var/lib/mysql 日志文件，数据库
– /usr/share/doc 文档 
– /usr/include/mysql 包含( 头) 文件 
– /usr/lib/mysql 库 
– /usr/share/mysql 错误消息和字符集文件

• 安装MySQL后，默认情况下，服务器是启动的
• 停止服务
  /etc/init.d/mysql stop
MySQL的Linux系统下安装

![1560925841860](C:\Users\HUAWEI\AppData\Roaming\Typora\typora-user-images\1560925841860.png)



启动服务

![1560925862377](C:\Users\HUAWEI\AppData\Roaming\Typora\typora-user-images\1560925862377.png)

输入如下格式的命令登录数据库
mysql -u user –p
– -h后面MySQL数据库服务器
– -u后面用户名
– -p用于指定用户名对应的密码
– 如果-p后面没有输入密码，系统会提示用户输入

![1560925884263](C:\Users\HUAWEI\AppData\Roaming\Typora\typora-user-images\1560925884263.png)