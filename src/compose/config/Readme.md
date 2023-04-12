# 配置文件


设置开机启动：`restart: always`

## 示例文件

```dockerfile
version: '3.7'
services:
  qdrant-local:
    image: qdrant/qdrant
    container_name: qdrant
    restart: always
    volumes:
      - /opt/qdrant/data:/qdrant/storage
    ports:
      - "6333:6333"
      - "6334:6334"
    environment:
      QDRANT__SERVICE__GRPC_PORT: 6333
```

- `image`: 容器镜像
- `container_name`: 容器名称
- `restart`: 重启策略，默认为`always`
- `volumes`: 容器挂载的文件系统，默认为`/opt/qdrant/data:/qdrant/storage`
- `ports`: 容器端口映射，默认为`6333:6333`
- `environment`: 容器环境变量，默认为`QDRANT__SERVICE__GRPC_PORT=6333`
