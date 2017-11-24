操作环境：CentOS 6.2 32bit

服务器地址：美国

 

1.准备VPS

2.安装sshd，设置sshd开机启动，允许root远程登录（可忽略，一般服务商会帮你预配置好）

3.使用root用户远程xshell工具登录主机。

4.进行系统更新
```
yum -y update
```

5.安装wget下载器
```
yum -y install wget
```

6.下载ss安装脚本
```
git clone https://github.com/hxwang1024/shadowsocks.git
```

7.使上述脚本属性可执行

```
chmod +x shadowsocks.sh
```

8.执行脚本
```
./shadowsocks.sh 2>&1 | tee shadowsocks.log
```

9.控制台会依次询问ss访问密码，访问端口，加密方式（选择端口后不需要你另外开放防火墙规则）

10.请尽情使用吧！


Reference
1.[teddysun](https://raw.githubusercontent.com/teddysun/shadowsocks_install/master/shadowsocks.sh)