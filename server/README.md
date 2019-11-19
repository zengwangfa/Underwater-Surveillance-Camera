
- rc.local 
	- 以自启动服务方式开启python服务端（用于收发指令、传递数据）
	- 以自启动服务方式开启MJPG-Streamer推送视频流
	
# 1.MJPG-Streamer安装
[MJPG-Streamer安装与推流](https://blog.csdn.net/qq_39492932/article/details/84671345)
	
	

## 2.1 系统脚本式自启动

- 1.将/etc/rc.local中的rc.local替换掉（如果需要多个摄像头，）
- 2.server.py 放 /home/pi 下

- 3.shell输入：
`
sudo chmod +x /etc/rc.local
`
使脚本生效（可执行）

---
- 当发现rc.local中的服务**并未自启动**，输入命令： `sudo systemctl status rc-local` 可以检查服务状态（正常状态如下图），如未启动可根据提示的**报错信息**进行相应的修改

![rc.local服务状态](../docs/pictures/status_rc-local.jpg "rc.local服务状态")


