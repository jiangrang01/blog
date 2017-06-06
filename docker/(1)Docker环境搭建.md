Docker 下载与安装
=================
系统版本 

 -  Centos
 -  Kernel Version

Installation--------->yum install docker-io

修改映像配置：/etc/docker/daemon.jason
添加如下："registry-mirror":["https://docker.mirrors.ustc.edu.cn"]

在docker index中搜索image：docker search redis

从docker registry server 中下拉image或repository:docker pull [OPTIONS] NAME[:TAG]


启动命令：sudo systemctl start docker／sudo service docker start

Happy Writing!