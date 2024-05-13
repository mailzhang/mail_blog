

```
docker ps -a
docker rm
docker images
docker rmi

docker exec -it [name]  /bin/bash

docker build -t [镜像名称]:[标签] [Dockerfile所在目录的路径]
docker build -f Dockerfile  -t media_centos_base:v1 .

docker run -d  --name m1 --rm media_centos_base:v1 tail -f /dev/null
    
# 清理未运行的容器
docker container prune

# 用于清理悬空的镜像、未使用的容器、网络和卷
docker system prune

# 挂在数据卷
-v /path/on/host:/path/in/container

```

开源存放位置
```shell
docker login ccr.ccs.tencentyun.com --username=xxxx

docker tag [imageId] ccr.ccs.tencentyun.com/mail_base/ubuntu_py37_media_base:[tag]
docker push ccr.ccs.tencentyun.com/mail_base/ubuntu_py37_media_base:v1
```


mac编译linux运行
```angular2html
--platform linux/amd64
docker build -f Dockerfile --platform linux/amd64  -t media_centos_base:v1 .
```