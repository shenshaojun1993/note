# Docker
## Mac
brew services start mongodb-community@4.2
brew services stop mongodb-community@4.2
mongod --config /usr/local/etc/mongod.conf --fork


## Docker加速
在/etc/docker下添加或修改 docker daemon.json配置
```
{
  "registry-mirrors" : [
    "http://docker.mirrors.ustc.edu.cn",
    "http://hub-mirror.c.163.com",
    "registry.docker-cn.com"
  ],
  "insecure-registries" : [
    "armdocker.rnd.ericsson.se",
    "docker.mirrors.ustc.edu.cn"
  ],
  "debug" : true,
  "experimental" : true
}
```
然后执行"systemctl restart docker"重载镜像配置。

## Docker配置mongo
docker pull mongo:latest
docker run  -d --restart always --name mongo -p 27017:27017 mongo
docker run --rm -p 8080:8080 192.168.56.101:5000/demo:0.0.0.1

## Docker配置Registry

```docker run -d --restart always -p 5000:5000 -v /home/art3mis/registry/:/var/lib/registry/ --name registry registry```

添加docker权限给当前用户，使docker命令免sudo
sudo groupadd docker 
sudo gpasswd -a ${USER} docker 
sudo service docker restart 
然后再重启电脑或者重新打开会话。

```docker run -e JAVA_TOOL_OPTIONS="-agentlib:jdwp=transport=dt_socket,server=y,suspend=n,address=8888" -p 8080:8080  -p 8888:8888  localhost:5000/hello:0.0.2-SNAPSHOT```

## aliyun镜像加速地址
```
{
  "registry-mirrors": ["https://tmaz9u3e.mirror.aliyuncs.com"]
}
```

## Docker 运行MySQL
```docker run -d --name myMysql -v /data/mysql:/var/lib/mysql -e MYSQL_ROOT_PASSWORD=123456 -p 3306:3306 mysql```

## Docker 运行draw.io

```docker pull fjudith/draw.io
docker run -dit --restart=always --name=draw -p 8080:8080 fjudith/draw.io
```