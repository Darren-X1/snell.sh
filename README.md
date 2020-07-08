# 此脚本仅用于远程连接家中局域网内机器，请勿用于任何非法行为！
## 适用于64位Linux系统。
## 运行完毕后屏幕显示psk，默认端口号~~13254~~ 9889（我随手那么一按( ̀⌄ ́)，按照标准填入Surge即可。
## 原作者停止更新，此版本已更新snell-server-v2.0.3
# 请使用root用户运行
---
MTProxyTLS

```
mkdir /home/mtproxy && cd /home/mtproxy
curl -s -o mtproxy.sh https://raw.githubusercontent.com/ellermister/mtproxy/master/mtproxy.sh && chmod +x mtproxy.sh && bash mtproxy.sh
```
开启bbr

```
wget --no-check-certificate -O /opt/bbr.sh https://github.com/teddysun/across/raw/master/bbr.sh
chmod 755 /opt/bbr.sh
/opt/bbr.sh
```
Debian & Ubuntu 用户请运行

```
wget --no-check-certificate -O snell.sh https://raw.githubusercontent.com/Darren-X1/snell.sh/master/snell.sh
chmod +x snell.sh
./snell.sh
```

Centos & RedHat 用户请运行

```
wget --no-check-certificate -O snell.sh https://raw.githubusercontent.com/Darren-X1/snell.sh/master/snell.centos.sh
chmod +x snell.sh
./snell.sh
```

首次安装默认端口号13254，如需修改请
在所有脚本运行结束后运行

```
nano /etc/snell/snell-server.conf
systemctl restart snell
```

自行修改。

当然你也可以用vi ^o^

查看运行状态：

```
systemctl status snell
```

卸载方法：

```
wget --no-check-certificate -O uninstall-snell.sh https://raw.githubusercontent.com/Darren-X1/snell.sh/master/uninstall-snell.sh
chmod +x uninstall-snell.sh
./uninstall-snell.sh
```
