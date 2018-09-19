# ZJU 有线网+ss配置 for Mac

## step
1. 玉泉申请IP（24小时生效，mac地址为以太网mac地址）
2. 插入网线后，在设置->网络中配置有线网
   1. ipv4手动
   2. 路由器即网关
   3. 其他信息根据申请的ip填写
3. 设置->网络中新建L2TP类型的VPN
   1. 服务器地址为10.5.2.9
   2. 账号为学号，密码在“鉴定设置”中填写
   3. 高级：点选“通过VPN发送所有流量”
      1. 代理点选自动代理配置：
         1. 命令行开启Mac本地webserver
         2. 将ss自带的pac文件（或为js格式）复制到webserver根目录
         3. 在设置中代理配置文件url填写url，例如http://localhost/proxy.pac

## 可能遇到的问题
   1. 可以上外网，不能上内网，且网速慢
      solution：可能是设置中配置了全局代理，需要在VPN中设置pac
