# Jcat-server
jib-registry 启动
jcat-jib-build配置
            <image>192.168.56.101:5000/jcatserver:${project.version}</image>

docker运行jcat服务
docker run --rm -it --name mje  -v /opt/config:/opt/config  -v /home/shaojun/aat.properties:/app/resources/aat.properties --net host  localhost:5000/arts:1.4.0-0518


docker run --rm -it  -p 9111:8088-v /opt/config:/opt/config  -v /home/shaojun/Documents/projects/config/aat.properties:/app/resources/aat.properties -v /home/shaojun/Documents/projects/config/arts.properties:/app/resources/arts.properties  -e JAVA_TOOL_OPTIONS="-agentlib:jdwp=transport=dt_socket,server=y,suspend=n,address=5005"   --net host  localhost:5000/arts:R6A0001

docker run -it --entrypoint bash 192.168.56.101:5000/jcatserver:1.0.111-SNAPSHOT 

aat.FATNumber=FAT1023773/2009 

<username>jcatcie</username>
<password>Iomdqguk@a8i7zv&</password>
 
ehaehss
Sj@931016

docker 登录
docker login armdocker.rnd.ericsson.se
拉取aat 的镜像
docker pull armdocker.rnd.ericsson.se/proj-jcatfw/aat-solution/aat-core:2.3 
 
启动AAT
docker run -p 8080:8080 -p 9090:9090 {imageId}


Docker 开启远程debug
docker run -e "JAVA_TOOL_OPTIONS=-agentlib:jdwp=transport=dt_socket,server=y,suspend=n,address=localhost:8888" -p 8888:8888  --net=host  9d36693adc36