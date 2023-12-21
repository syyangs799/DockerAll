## docker 安装部署mysql
### 下载镜像
```
docker pull mysql
```
### 启动镜像
```
docker run -p 3306:3306 --name syyang-mysql \
-v $PWD/conf:/etc/mysql/conf.d \
-v $PWD/logs:/logs \
-v $PWD/data:/var/lib/mysql \
-e MYSQL_ROOT_PASSWORD=123456 \
-d mysql
```
## docker安装MYSQLCDC
### 下载镜像
```
docker pull debezium/example-mysql
```
### 启动镜像
```
docker run -it --rm --name mysql-cdc \
-p 3306:3306 \
-e MYSQL_ROOT_PASSWORD=debezium \
-e MYSQL_USER=mysqluser \
-e MYSQL_PASSWORD=mysqlpw -d debezium/example-mysql```