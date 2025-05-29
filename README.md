# docker
docker-compose学习，并整理一些自己常用的docker-compose脚本文件

docker-compose 安装及设置命令，基于Ubuntu，懒得用 docker compose
```
sudo apt update

sudo apt install docker.io

# 安装docker-compose
mkdir -p ~/.docker/cli-plugins/

# 下载二进制 https://github.com/docker/compose 访问查看最新版本
curl -SL https://github.com/docker/compose/releases/download/v2.29.1/docker-compose-linux-x86_64 -o ~/.docker/cli-plugins/docker-compose

# 授权可执行
chmod +x ~/.docker/cli-plugins/docker-compose

# 验证
docker compose version

# 调整别名
echo 'alias docker-compose="docker compose"' >> ~/.bashrc

# 重新加载
source ~/.bashrc

#验证是否别名成功
docker-compose --version

# 设置为开机自动启动
systemctl enable docker
```

常用命令
```
# 1、启动应用
docker-compose up

# 2、后台启动应用
docker-compose up -d

# 3、停止应用
docker-compose stop

# 4、停止并删除应用
docker-compose down

# 5、重新创建服务
docker-compose up --build

# 6、查看服务状态
docker-compose ps

# 7、查看服务日志
docker-compose logs

# 8、查看指定服务日志
docker-compose logs <service_name>

# 9、列出所有运行的服务
docker-compose ls

# 10、删除服务的容器
docker-compose rm <service_name>

# 11、列出服务环境变量
docker-compose config

# 12、执行服务器内的命令
docker-compose exec <service_name> <command>
```
