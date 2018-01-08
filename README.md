
With curl:
```
curl -fsSL https://henriquedias.com/filemanager/get.sh | bash
```
Or using wget:
```
wget -qO- https://henriquedias.com/filemanager/get.sh | bash
```
If you’re on Windows, you can use PowerShell to install File Manager too. You should run the following command as administrator since it needs permissions to add the executable to the PATH:

iwr -useb https://henriquedias.com/filemanager/get.ps1 | iex

或者
put filemanager  to  usr/local/bin

```
chmod +x /usr/local/bin/filemanager
```
```
mkdir /etc/filemanager
```
```
mkdir /srv ##这步报错可忽略
```
```
wget -O /etc/filemanager/config.json https://github.com/malaohu/ruyo-shell/raw/master/FileManager/config.json
```
```
nohup filemanager -c /etc/filemanager/config.json >/dev/null 2>&1 &
```

后台启动服务
```
nohup filemanager -c /etc/filemanager/config.json >/dev/null 2>&1 &
```

关闭后台服务
```
eval $(ps -ef | grep filemanager | grep -v grep | awk '{print "kill "$2}')
```
