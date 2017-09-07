##    阿里云环境

日志文件  
cd /var/log/  

查看磁盘容量  
du -h --max-depth=1 ./  

查看端口  
lsof -Pni +M -i4|grep  

运行jar  
(java -jar  --spring.profiles.active=demo &)  

检查nignx  
/usr/local/nginx/sbin/nginx  -t -c conf/nginx.conf  

重启nginx  
/usr/local/nginx/sbin/nginx -s reload

启动nginx  
/usr/local/nginx/sbin/nginx -c /usr/local/nginx/conf/nginx.conf  

maven启动  
mvn spring-boot:run -D spring.profiles.active=demo

查看nginx访问记录  
tail -200f /usr/local/nginx/logs/access.log

查看nginx错误信息  
tail -200f /usr/local/nginx/logs/error.log  

进入redis客户端  
/data/redis-3.2.3/src/redis-cli -a foobared  

net连接数  
netstat -n | awk '/^tcp/ {++S[$NF]} END {for(a in S) print a, S[a]}'

监控端口TCP状态
netstat -anc|grep 3999  

