# Python-Web-Application

>     $ sudo apt-get install nginx
Failed to start A high performance web server and a revers p...`

`$ systemctl status nginx.service`

returns the same

`$ nginx =t`

returns

`nginx: the configuration file /etc/nginx/nginx.conf syntex is ok`

`nginx: configuration file /etc/nginx/nginx.conf test is successful`

`$ nginx`

returns

`nginx: [emerg] bing() to 0.0.0.0:80 failed (98: Address already in use)`

`$ netstat -ltunp`

returns

`Active Internet connections (only servers)`

`Proto    Recv-Q    Send-Q    Local Address    Foreign Address    State    PID/Program`

`tcp           0         0    0.0.0.0:80       0.0.0.0:*          LISTEN   838/apache2`

`$ kill 838`
