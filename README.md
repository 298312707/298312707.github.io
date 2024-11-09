# Mysql篇

1.主机连接linux虚拟机mysql服务，报错2003

[windows下用navicat链接虚拟机MySQL数据库的过程和问题解决 - brankoliu_liu - 博客园 (cnblogs.com)](https://www.cnblogs.com/brankoliu/p/10845491.html)

# Redis篇

1.安装yum仓库出错，提示

>        错误：依赖检测失败：
>                         epel-release = 7 被 remi-release-7.9-6.el7.remi.noarch 需要

 [安装rpm包时提示错误：依赖检测失败的解决方法_错误:依赖检测失败:erlang-asn1(x86-64) = 20.1-1.el7.centos -CSDN博客](https://blog.csdn.net/qq_45556655/article/details/115634195)

2.安装redis出错,提示

> 没有可用软件包 redis-7.0.13。
> 错误：无须任何处理

把命令改为yum --enablerepo=remi -y install redis-7.2.5 

# Minio篇

1.console页面主机无法访问

> 使用systemctl stop firewalld关闭防火墙即可

# Nginx篇

1.nginx网页无法访问

> 关闭防火墙即可[【Nginx】启动成功无法访问网页（完整的排除方案）_nginx启动成功但是无法访问-CSDN博客](https://blog.csdn.net/yujing1314/article/details/105225325)

2.部署完成后，访问页面提示网关错误

> [查看SELinux状态及关闭SELinux-CSDN博客](https://blog.csdn.net/javazhouchon/article/details/119428372)

# ChatGpt

> cmd输入ipconfig /flushdns
