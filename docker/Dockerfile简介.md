##Dockerfile

FROM hub.c.163.com/bingohuang/debian:163

MAINTAINER bingohuang <me@bingohuang.com>

RUN apt-get update && apt-get install -y nginx

COPY docker-mario /usr/share/nginx/www

EXPOSE 80

ENTRYPOINT ["nginx", "-g", "daemon off;"]
Dockerfile 解析：

以下对 Dockerfile 做逐句解析

- 关键字 FROM，选用包含163更新源的Debian镜像，版本7.9
- 关键字 MAINTAINER，添加作者信息和联系方式（有任何问题或反馈欢迎发邮件沟通）
- 关键字 RUN，运行命令，这里是更新程序列表并安装 Nginx 程序
- 关键字 COPY，将 docker-mario 源码拷贝到容器的 /usr/share/nginx/www 目录下（这是第三步安装好 Nginx 程序后自动生成的目录
- 关键字 EXPOSE，暴露端口，这里是 Nginx 的默认端口：80
- 关键字 ENTRYPOINT，指定容器运行的默认指令（不会被用户指令覆盖）