# 目录
- [目录](../readme.md)

-1.查看定时任务日志
	tail -f /var/log/cron
-2.查看定时任务
	crontab -l
-3.新加定时伤务
	crontab -e

-4.redis 关闭
	cd /data/redis/bin
	./redis-cli shutdown
	
-redis启动
	./redis-server  ../conf/redis.conf

-5.查看磁盘：
 	df -h
	 文件  du -h 文件path   du -h  / |sort -n
	du  /data    -sh  总的大小
-6.find
	find  /   -type f -size +1G  在目录 / 下查找大于1G的文件

-7.ssh登陆
	ssh -l git 192.168.0.103
	ssh git@192.168.0.103

-8.ldd命令的介绍
	在制作自己的发行版时经常需要判断某条命令需要哪些共享库文件的支持，以确保指定的命令在独立的系统内可以可靠的运行；

	在Linux环境下通过ldd命令即可实现，在终端下执行：
	ldd /bin/ls

	在启动nginx时，提示没有找到libprce.so.1 用如下命令
	ldd $(which /usr/local/nginx/sbin/nginx)

-9 tar 命令
 tar.gz 解压 tar -zxvf xx.tar.gz
 tar.bz2 解压 tar -jxvf xx.tar.bz2

 -10 查看系
    cat /etc/issue
    uname -a
 - 11 创建用户
    useradd testuser 创建用户testuser
    passwd testuser 给已创建的用户testuser设置密码
    说明：新创建的用户会在/home下创建一个用户目录testuser
	usermod --help 修改用户这个命令的相关参数
	userdel testuser 删除用户testuser
	rm -rf testuser 删除用户testuser所在目录
