## 1.docker search registry 
## 2.docker pull registry 
## 3.docker run -d -p 5000:5000 --name registry registry:0:9:1(镜像名称)
## 4.docker ps -a 
## docker exec -it website(images name) /bin/bash   通过exec命令进入后台启动的交互模式中  supervisorctl查看有没有启动，通过exit命令退出
##docker run -d -p 3306:3306 -v host_dir:container_dir(宿主机目录与容器目录映射volume)
## Mac中是ifconfig en0 命令
## docker tag registry 10.12.49.14:5000/csphere/csphere:0.11.1
##jenkins 挂载需要以下命令：docker run -d -p 8080:8080 --name jenkins -v host_dir:container_dir -v /var/run/docker.sock:/var/run/docker.sock
-v /root/maven-tar:/root csphere/jenkins:1.609
