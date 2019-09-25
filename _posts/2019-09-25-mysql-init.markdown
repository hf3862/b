---
layout: post
title:  "MySQL 5.6 in CentOS 7"
date:   2019-09-25 11:52:00 +0800
categories: 
---

{% highlight bash %}
[root@localhost ~]# rpm -Uvh http://dev.mysql.com/get/mysql-community-release-el7-5.noarch.rpm
[root@localhost ~]# yum repolist enabled | grep "mysql.*-community.*"
[root@localhost ~]# yum install mysql-community-server
[root@localhost ~]# service mysqld start
[root@localhost ~]# mysql_secure_installation

[root@localhost ~]# mysql -h localhost -u root -p
mysql> create schema test default character set utf8 collate utf8_general_ci;
mysql> create user 'tt'@'%' identified by 'tt123';
mysql> grant all privileges on `test`.* to 'tt'@'%';
mysql> flush privileges;
{% endhighlight %}
