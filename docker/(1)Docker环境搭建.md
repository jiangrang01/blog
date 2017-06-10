Docker 下载与安装
=================
系统版本 

 -  Centos
 -  Kernel Version

Installation--------->yum install docker-io
查找docker信息和版本命令：docker info /docker -v

修改映像配置：/etc/docker/daemon.jason
添加如下："registry-mirror":["https://docker.mirrors.ustc.edu.cn"]

在docker index中搜索image：docker search redis

从docker registry server 中下拉image或repository:docker pull [OPTIONS] NAME[:TAG]


启动命令：sudo systemctl start docker／sudo service docker start

查看所有镜像的列表:   docker images

学习过镜像是存储在Docker registry。在registry中的镜像可以使用以下命令查找到：docker search

- 容器生命周期管理 — docker [run|start|stop|restart|kill|rm|pause|unpause]
- 容器操作运维 — docker [ps|inspect|top|attach|events|logs|wait|export|port]
- 容器rootfs命令 — docker [commit|cp|diff]
- 镜像仓库 — docker [login|pull|push|search]
- 本地镜像管理 — docker [images|rmi|tag|build|history|save|import]
- 其他命令 — docker [info|version]


# 使用网络
-----------
容器中可以运行一些网络应用，要让外部也可以访问这些应用，可以通过 -P 或 -p 参数来指定端口映射。
当使用 -P 标记时，Docker 会随机映射一个 49000~49900 的端口到内部容器开放的网络端口。
使用 docker ps 可以看到，本地主机的 49155 被映射到了容器的 5000 端口。此时访问本机的 49155 端口即可访问容器内 web 
-p（小写的）则可以指定要映射的端口，并且，在一个指定端口上只可以绑定一个容器。支持的格式有 ip:hostPort:containerPort | ip::containerPort | hostPort:containerPort。

## 映射所有接口地址

使用 hostPort:containerPort 格式本地的 5000 端口映射到容器的 5000 端口，可以执行

$ sudo docker run -d -p 5000:5000 training/webapp python app.py
此时默认会绑定本地所有接口上的所有地址。

## 映射到指定地址的指定端口

可以使用 ip:hostPort:containerPort 格式指定映射使用一个特定地址，比如 localhost 地址 127.0.0.1

$ sudo docker run -d -p 127.0.0.1:5000:5000 training/webapp python app.py
## 映射到指定地址的任意端口

使用 ip::containerPort 绑定 localhost 的任意端口到容器的 5000 端口，本地主机会自动分配一个端口。

$ sudo docker run -d -p 127.0.0.1::5000 training/webapp python app.py
还可以使用 udp 标记来指定 udp 端口

$ sudo docker run -d -p 127.0.0.1:5000:5000/udp training/webapp python app.py

reference
- https://yeasy.gitbooks.io/docker_practice/content/network/port_mapping.html
- http://kuga.me/2016/07/22/docker-redis-cluster/

docker ps 查询本地运行哪些镜像
netstat -na |grep 8080 查询8080有木有被监听

Happy Writing!