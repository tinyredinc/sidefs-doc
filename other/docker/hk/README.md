hk服务以docker部署，根目录位于：
```
cd /var/docker
```

重启服务：
```
sudo docker compose down && sudo docker compose up -d
```


### 部署前端测试应用

1. 打包你的前端代码

2. 将打包后代码推到测试服务器
```bash
# pc
scp -r .\dist\* fe_deploy@hk-fs-plt-api.sideai.com:/var/docker/app/frontend/pc/
# or mobile
scp -r .\dist\* fe_deploy@hk-fs-plt-api.sideai.com:/var/docker/app/frontend/mobile/

# 然后输入密码即进入文件上传过程
```

3. 打开浏览器验证
```
# pc
http://hk-fs-plt-api.sideai.com:10081/
# mobile
http://hk-fs-plt-api.sideai.com:10082/
```