Linux Command
=================
- find / -name filename.txt 根据名称查找/目录下的filename.txt文件。

- find . -name "*.xml" 递归查找所有的xml文件

- find . -name "*.xml" |xargs grep "hello world" 递归查找所有文件内容中包含hello world的xml文件


- grep -H 'spring' *.xml 查找所以有的包含spring的xml文件

- find ./ -size 0 | xargs rm -f & 删除文件大小为零的文件

- ls -l | grep '.jar' 查找当前目录中的所有jar文件

- grep 'test' d* 显示所有以d开头的文件中包含test的行。

- grep 'test' aa bb cc 显示在aa，bb，cc文件中匹配test的行。

- grep '[a-z]\{5\}' aa 显示所有包含每个字符串至少有5个连续小写字符的字符串的行。

- ps –ef|grep tomcat 查看所有有关tomcat的进程

- ps -ef|grep --color java 高亮要查询的关键字

- kill -9 19979 终止线程号位19979的进程

- ls -al  查看文件，包含隐藏文件

- cp source dest 复制文件

- cp -r sourceFolder targetFolder 递归复制整个文件夹

- scp sourecFile romoteUserName@remoteIp:remoteAddr 远程拷贝

- rmdir deleteEmptyFolder 删除空目录 rm -rf deleteFile 递归删除目录中所有内容

- 移动文件mv /temp/movefile /targetFolder

- 重命令mv oldNameFile newNameFile

- 查看文件头10行head -n 10 example.txt

- 查看文件尾10行tail -n 10 example.txt

- tail -f exmaple.log //这个命令会自动显示新增内容，屏幕只显示10行内容的（可设置）。

- netstat -tln | grep 8080 查看端口8080的使用情况

- lsof -i :8080  查看端口属于哪个程序

- ps aux|grep java 查看java进程

- ps aux 查看所有进程




Happy Writing!