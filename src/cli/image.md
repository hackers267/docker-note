# Image命令

`docker image`命令是对`docker`中镜像信息的查看。

## 查看镜像列表

在`docker`中存在一个或多个镜像，当我们要查看有哪些镜像的时候，可以使用下面的命令：
```shell
docker images
docker image ls
```

上面的命令都可以列出docker中存在的镜像，其信息包括：

- Repository  镜像仓库名称
- TAG  镜像标签
- Image Id  镜像id
- Created  镜像创建时间
- Size  镜像占用大小

如果想要查看某个镜像的更加详细的信息可以参考下面的[命令](##查看某个镜像的详细信息)

## 查看某个镜像的详细信息

当我们要查看某个镜像的详细信息的时候，我们可以使用下面的命令：
```shell
docker image inspect imageId
```

如果你不知道镜像id，可以使用`docker images`查看镜像列表，在其中找到镜像id。