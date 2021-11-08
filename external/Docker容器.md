### [Docker容器](https://zhuanlan.zhihu.com/p/92889072)

[Docker —— 从入门到实践](https://yeasy.gitbook.io/docker_practice/image/pull)

#### 容器操作

```bash
docker ps  #查看正在运行的容器状态
docker ps -a # 查看所有容器的状态
docker version #查看client和server端版本，并可以查看是否开启体验功能
```

##### inspect

```text
docker inspect [container-id] # 查看容器详情
```

##### start/stop/restart/kill/rm/

```shell
docker start [container-id] # 启动容器

docker restart [container-id] # 重启容器

docker kill [container-id] # 强制关闭容器(默认发送SIGKILL信号, 加-s参数可以发送其他信号)

docker rm [容器名 或 container-id] # 删除容器

docker inspect [container-id] # 查看容器详情
```

##### exec在运行的容器中运行命令

```text
docker exec [OPTIONS] CONTAINER COMMAND [ARG...] 

docker exec container-name  ls /  # 在正在运行的容器中使用 ls命令

docker exec -it container-name /bin/bash  # 进入容器

docker attach container-name
```

#### 镜像IMG操作

##### search/images/rmi/inspect/save/load

```bash
docker search [条件]

docker images # 查看本地镜像

docker rmi [镜像名 或 镜像ID] # 删除本地镜像

docker inspect [镜像名 或 镜像ID]

docker save [镜像名] > [文件路径] # 打包本地镜像，使用压缩包来完成迁移

docker load < [文件路径] # 导入镜像压缩包
```

#### 常见命令&&使用场景

##### 创建容器docker

` docker run -it -v /宿主机绝对路径目录:/容器内目录 镜像名 `

