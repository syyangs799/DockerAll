## docker 安装部署redis
### 下载镜像
```
docker pull redis
```
### 启动镜像
```
docker run --name redis --privileged=true -p 6379:6379 -d redis
```