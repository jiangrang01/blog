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

Happy Writing!