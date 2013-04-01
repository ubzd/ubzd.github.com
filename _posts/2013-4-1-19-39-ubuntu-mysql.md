---
layout: post
title: ubuntu下安装mysql
category: ubuntu
tags: [ubuntu]
---
{% include JB/setup %}

1. 下载mysql-5.5.30-linux2.6-i686.tar.gz
2. 放到`/usr/local`下,可以在support-files下面的mysql.server文件中修改路径
3.  创建用户组： `sudo groupadd mysql`
4. 在创建的用户组中创建一个用户： `sudo useradd -r -g mysql mysql`
5. `cd /usr/local/msyql`
6. 修改目录的拥有者： `sudo chown -R mysql .` `sudo chgrp -R mysql .`
7. 安装libaio依赖库 `sudo apt-get install libaio-dev`
8. 生成mysql的数据库运行的系统数据库 `sudo scripts/mysql_install_db --user=mysql`
9. 把mysql目录的拥有者改为root用户，并将生成的系统依赖数据赋给mysql用户，执行如下命令： `chown -R root .` `chown -R mysql data`
10. 安好之后可以执行`sudo ./support-files/mysql.server start`
11. 将mysql的配置文件安装到/etc目录下：`sudo cp support-files/my-medium.cnf /etc/my.cnf`
12. 解决中文乱码, 在[mysqld]加入`character-set-server=utf8`
13. 然后`cp /usr/local/mysql/support-files/mysql.server /etc/init.d/mysqld`
