
- 1 安装
	 ansible-galaxy install mescanef.zabbix-server

	安装脚本
	hosts: localhost
 
  	become: yes
  	roles:
    	- { role: geerlingguy.apache }
    	#如果要安装数据库
	#    - { role: geerlingguy.mysql } 
     	- { role: mescanef.zabbix-server }

 zabbix_vhost= false

 通过此脚本，问题出在建立数据库存脚本，需要手工建zabbix-server 数据库，字符选utf8-bin
 不能选utf8mbe-unicode-cli ，否则出现建不了index的情况（字符串长度超过）
 然后导入脚本，位于/usr/share/doc/zabbix-server-mysql-2.4.8/create/

 ip/zabbix 登陆 用户Admin 密码zabbix

 进入后可能出现红色提示时区没有设置，administration中的installation进行检查
 在/etc/php.ini date.timezone = Asia/Shanghai


