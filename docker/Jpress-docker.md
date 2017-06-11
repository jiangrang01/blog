- docker run -d -p 8888:8080 jpress
- Dockerfile

 from ......
 MAINTAINER jiangrang 240264462@qq.com

 copy jpress/wars/...  /usr/local/tomcat/webapps
 -  docker build -t jpress:latest .

 - netstat -na|grep 8888

 docker run -d -p 9999:3063 -e MYSQL_ROOT_PASSWORD = 000000 -e MYSQL_DATABASE = jpress hub.c.163.com/lobrary/mysql:latest