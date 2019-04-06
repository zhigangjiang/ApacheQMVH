# 脚本说明
本脚本为本人大学期间网络服务器课程作业，平时觉得使用频繁，因此分享。
# 功能说明
## 主菜单
### 1.	显示apache网页服务器状态、虚拟主机配置和firewall防火墙状态
### 2.	添加虚拟主机
输入添加的主机域名和目录 输入jzg.com 目录 /var/www/html3/
添加成功 重启服务器
访问成功 /var/www/html3/index.html
### 3.	移除虚拟主机
输入需要移除的主机域名
输入不存在配置文件中的域名会提示重新输入
输入正确，移除成功 重启服务器
移除后 以第一个虚拟主机的目录为默认根目录
 
### 4.	修改虚拟主机
输入需要修改的主机域名
 选择修改域名还是文档目录
 
修改域名成功修改为www.niuini.com
 
修改文档目录为 /var/www/html/
 
访问成功
 
### 5.	打开防火墙并且添加http服务永久生效
 
如果已经添加http服务则提示
 
客户端 访问
 
### 6.	打开防火墙并且移除http服务永久生效
 
客户端访问
 
### 7.	退出脚本

# 安装说明
bash 运行
# 注意
配置apache基于域名的虚拟主机，应配置dns，使多个域名指向相同apache服务器，当apache服务器接受浏览器发送的不同头文件，其中包括用户输入的域名，来选择虚拟主机，指向不同目录，从而完成1台web服务器绑定多个域名。当客服端浏览器输入不在虚拟主机目录中的域名，而该域名又指向apache服务器，测试显示：会访问第一个虚拟主机的文档目录作为默认目录，而不会访问httpd.conf中的DocumentRoot。因为设置了NameVirtualHost *:80 。
# 展望：
虚拟主机的使用越来越频繁，一台主机可以绑定多个域名，符合当前一些用户的需求，该脚本功能比较简单，但是用户体验较好，会检测用户的输入，当用户输入为空，或者输入不存在，或者重复的内容时会提示。以后进一步完善脚本功能。
