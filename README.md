# snell-install

apt update && apt install wget unzip curl socat -y

# 二进制文件下载界面

https://manual.nssurge.com/others/snell.html

# ARM

wget https://dl.nssurge.com/snell/snell-server-v4.0.0-linux-aarch64.zip

# 解压到指定路径

unzip snell-server-v4.0.0-linux-aarch64.zip -d /usr/local/bin

# AMD

wget https://dl.nssurge.com/snell/snell-server-v4.0.0-linux-amd64.zip

# 解压到指定路径

unzip snell-server-v4.0.0-linux-amd64.zip -d /usr/local/bin

# 下载启动文件

curl -Lo /etc/systemd/system/snell.service https://raw.githubusercontent.com/fqnpc/snell-install/main/snell.service

# 生成配置文件

snell-server --wizard -c /etc/snell-server.conf

# 管理命令

# 重载服务

systemctl daemon-reload

# 开机运行 Snell

systemctl enable snell

# 开启 Snell

systemctl start snell

# 关闭 Snell

systemctl stop snell

# 重启 Snell

systemctl restart snell

# 查看 Snell 状态

systemctl status snell

# 关闭开机运行Snell

systemctl disable snell


