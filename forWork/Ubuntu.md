## 命令行连接
`ssh  远程机器名@192.168.67.128`
`telnet 192.168.67.128 22`
## 启动端口
### //安装后需要重启
`sudo apt-get install openssh-server openssh-client`

`service ssh start`

`ssh localhost`

`lsof -i:22`