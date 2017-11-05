# Transmission
系统为：centos6 64位

python：2.7.13

工作目录：/root

一、Transmission
1.安装
wget http://github.itzmx.com/1265578519/transmission/master/2.84/transmissionbt.sh -O transmissionbt.sh;sh transmissionbt.sh
1.1.使用事项

1.访问地址为http://IP：9091，默认用户名和密码均为itzmx.com，文件下载位置:/home/transmission/Downloads/

2.修改端口、用户名和密码 请务必停止服务后修改

service transmissiond stop
vi /home/transmission/.config/transmission/settings.json
rpc-username 帐号
rpc-password 密码
rpc-port 端口
rpc-authentication-required 是否开启使用账号密码加密访问

/usr/share/transmission/web/  替换美化包

设置完成后重启服务：
service transmissiond start

3.重启进程
service transmissiond restart

4.卸载Transmission
service transmissiond stop
rm -rf /home/transmission
rm -rf /usr/share/transmission

二、Transmission的美化

默认的Transmission其实挺丑的，我们可以美化汉化一下
特别注意因为项目不稳定，一键脚本最近安装后找不到网页文件，造成404问题，推荐手动下载完整包安装！

项目地址：https://github.com/ronggang/transmission-web-control

2.1.手动安装

CentOS版目录：/usr/share/transmission/web/

Debian版目录：/var/lib/transmission-daemon/web

完整包下载：https://github.com/ronggang/transmission-web-control/raw/master/release/transmission-control-full.tar.gz

2.2.一键脚本

wget https://github.com/ronggang/transmission-web-control/raw/master/release/tr-control-easy-install.sh
bash tr-control-easy-install.sh
如果需要http而不是https，请使用以下命令：

wget https://github.com/ronggang/transmission-web-control/raw/master/release/tr-control-easy-install-en-http.sh --no-check-certificate
bash tr-control-easy-install-en-http.sh
如果需要安装到群晖downloadstation,请下载下列安装脚本并运行：

wget https://github.com/ronggang/transmission-web-control/raw/master/release/ds-control-easy-install.sh
bash ds-control-easy-install-en-http.sh
至此Transmission的安装教程结束！


