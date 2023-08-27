# webdav_fuse
挂载webdav到本地磁盘

## 安装
1、选择适合自己的版本，下载rclone.exe，放在RCLONE-GG-W.exe同级目录

2、请先安装winfsp-1.8.20304.msi，然后打开RCLONE-GG-W.exe

![image](https://github.com/xieyuhua/webdav_fuse/assets/29120060/69ff8d1f-07b4-4f13-bbe8-b8b67825584e)

3、确定挂载成功

![image](https://github.com/xieyuhua/webdav_fuse/assets/29120060/00e148b7-45ab-4d78-99e2-0e9e604fc59c)

4、取消挂载点击STOP

![image](https://github.com/xieyuhua/webdav_fuse/assets/29120060/7b04a572-d663-4d6f-8234-f2ffdc547daa)

# 注意

1.生成文件WEBDAV.bat
```
rclone.exe mount WEBDAV: H: --cache-dir C:\go\rclonewebdav\Temp --allow-other --vfs-cache-mode writes --allow-non-empty
```
2.rclone配置文件
```
[s3]
type = s3
provider = Alibaba
access_key_id = LTAdqd20kqdqQKk
secret_access_key = Z29ff8hmgtcewqddqwdj5eY
endpoint = oss-cn-shanghai.aliyuncs.com

[WEBDAV]
type = webdav
url = http://47.68.55.32:5645/dav/
user = 1
pass = sr5Wx-0rT81n452bejsIOyY
```
