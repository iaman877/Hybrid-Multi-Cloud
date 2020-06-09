# Topic  : log | matrix

there are many uses of log 
*  It contain all the history of login 
*  it is also used for data analysis for company 
```
# cd /var/log
# ls
# cat secure {here ssecure is the default folder}
# cat /var/log/secure  {it will show all the login attempt}
# tail -2 /var/log/secure  {only show last two line }
# cd httpd  {open httpd folder, and it have two files (1) acesslog (2) error log}
# cat acess_log {it will show all the web services which have logged}
# tail -5 access_log  {it will only show last 5 lines of log}
# tail -f access_log  { it will only real time login success attempt}
```
