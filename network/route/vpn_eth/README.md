Ref : TODO
Date : 2020.02.09
SRC : note/tools/network/route/vpn_eth.txt
OS : **Windows 10**(1909)

#### 1. vpn_eth.txt


```
# Problem : Cannot access internet after connecting to VPN.
# Fix	: Delete the default route automatically configured when adding the VPN,
#	  and add policy route.
route DELETE 0.0.0.0 mask 0.0.0.0 47.94.224.171
route add 172.0.0.0 mask 255.0.0.0 47.94.224.171
```

#### 2. 补充说明vpn_eth.txt

问题：连接VPN后，无法访问外部网络
修复：删除在添加VPN时自动添加的静态路由，添加需要的路由


连接VPN时取消添加默认路由的步骤
```
属性
网络
Internet 协议版本4
高级
[去勾选]在远程网络上使用默认网关
```

