本配置用于快速启动应用服务，利用docker compose可以非常方便的在任意操作系统上启动应用，不论开发还是生产部署。

需要注意的是，启动应用前请先将`config.php`放于app/app目录下，并请修改docker-compose.yaml中的/var/app/backend对应的宿主机路径为你的项目路径。

官方PHP镜像未安装或启动一些依赖的插件，php/dockerfile用于重构应用安装这些插件，首次执行docker compose up时会自动构建，无需你手动处理，仅需稍作等待。

启动应用及其他依赖的容器：
```bash
docker compose up

# 上述非以守护进程启动，首次启动可用上述方式，方便你观察容器就绪状态，后续启动可用下述指令以守护进程启动
docker compose up -d
```

应用启动成功后可至浏览器访问<http://127.0.0.1:5000/>测试是否正常，一般来说新拉的项目未安装php vendor插件，需按下述步骤安装：
```bash
# 进入php容器终端
docker exec -it sidefs-php sh

# 安装composer vendor
php composer.phar install
```

至此应用应该已能正常访问，你可以在宿主机目录下开发项目，文件是映射到docker容器的，即改动代码后直接刷新浏览器即可看到效果。

最后可以通过下述指令停止应用：
```bash
docker compose down
```
