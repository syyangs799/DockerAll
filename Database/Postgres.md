docker 安装部署postgres
```
docker run --name postgres -e POSTGRES_PASSWORD=postgres -p 5432:5432 -d postgres:9.4
```
说明：
```
设置环境变量，
指定数据库的登录口令为postgres;
postgres镜像默认的用户名为postgres;
```