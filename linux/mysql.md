# 目录
- [目录](../readme.md)

- 有可能你的系统没有 safe_mysqld 程序(比如我现在用的 ubuntu操作系统, apt-get安装的mysql) , 下面方法可以恢复
-1. 停止mysqld； 
/etc/init.d/mysql stop
(您可能有其它的方法,总之停止mysqld的运行就可以了)
-2. 用以下命令启动MySQL，以不检查权限的方式启动； 
mysqld start --skip-grant-tables &
-3. 然后用空密码方式使用root用户登录 MySQL； 
mysql -u root
-4. 修改root用户的密码； 
mysql> update mysql.user set password=PASSWORD('newpassword') where User='root'; 
mysql> flush privileges; 
mysql> quit 
重新启动MySQL
/etc/init.d/mysql restart
就可以使用新密码 newpassword 登录了。