
With curl:
```
curl -fsSL https://hacdias.github.io/filemanager/get.sh | bash
```
Or using wget:
```
wget -qO- https://hacdias.github.io/filemanager/get.sh | bash
```
If you’re on Windows, you can use PowerShell to install File Manager too. You should run the following command as administrator since it needs permissions to add the executable to the PATH:
```
iwr -useb https://hacdias.github.io/filemanager/get.ps1 | iex

```
So, if you wanted to run File Manager on port 80, with the database on /etc/fm.db and the default scope to /root, you would run:
```
filemanager --port 80 --database /usr/local/bin/filemanager.db --scope /root
```








==============
其他方案：
```
chmod +x /usr/local/bin/filemanager

mkdir /etc/filemanager

mkdir /srv ##这步报错可忽略

wget -O /etc/filemanager/config.json https://github.com/malaohu/ruyo-shell/raw/master/FileManager/config.json

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
