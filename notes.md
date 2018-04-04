# Python-Web-Application

安装nginx的时候报错

> $ sudo apt-get install nginx
> Failed to start A high performance web server and a revers p...
照屏幕上的指令
> $ systemctl status nginx.service
返回同样的错误，检查nginx的的状态？
> $ nginx -t
显示正常
> nginx: the configuration file /etc/nginx/nginx.conf syntex is ok
> nginx: configuration file /etc/nginx/nginx.conf test is successful

在网上搜，或许是端口被占用, 检查一下
> $ nginx
> nginx: [emerg] bing() to 0.0.0.0:80 failed (98: Address already in use)
确实如此，那看一下现在是谁在用那个端口呢
> $ netstat -ltunp
> Active Internet connections (only servers)
> Proto    Recv-Q    Send-Q    Local Address    Foreign Address    State    PID/Program
> tcp           0         0    0.0.0.0:80       0.0.0.0:*          LISTEN   838/apache2
就是PID 838了，关闭进程吧
> $ kill 838
再试一下安装nginx
> $ sudo apt-get install nginx
进入公网ip, 出现nginx欢迎界面, 阶段性胜利!
