
强烈建议开启bbr加速，可大幅加快节点reality和vmess节点的速度

# 简介
- Reality Hysteria2 （vmess ws）一键安装脚本
  
## 功能

- 无脑回车一键安装或者自定义安装
- 完全无需域名，使用自签证书部署hy2，（使用argo隧道支持vmess ws优选ip（理论上比普通优选ip更快））
- 支持修改reality端口号和域名，hysteria2端口号
- 无脑生成sing-box，clash-meta，v2rayN，nekoray等通用链接格式


## 使用教程

### reality和hysteria2 vmess ws三合一脚本

```bash
bash <(curl -fsSL https://github.com/sscles/sing-box-reality-hysteria2/raw/main/beta.sh)
```

### reality hysteria2二合一脚本

```bash
bash <(curl -fsSL https://github.com/sscles/sing-box-reality-hysteria2/raw/main/install.sh)
```

### 安装完成后终端输入 mianyang 可再次调用本脚本


|项目||
|:--|:--|
|程序|**/root/sbox/sing-box**|
|服务端配置|**/root/sbox/sbconfig_server.json**|
|重启|`systemctl restart sing-box`|
|状态|`systemctl status sing-box`|
|查看日志|`journalctl -u sing-box -o cat -e`|
|实时日志|`journalctl -u sing-box -o cat -f`|

warp解锁v4 v6等操作自行使用warp-go脚本
具体操作就不说了

```
wget -N https://gitlab.com/fscarmen/warp/-/raw/main/warp-go.sh && bash warp-go.sh
```

Linux-NetSpeed是一键安装BBR原版、BBRplus版、BBR魔改版和LotServer(锐速)版内核的网络加速脚本。
1）安装wget下载工具，则执行命令：
```
yum -y install wget #CentOS/RedHat
apt-get install wget #Debian/Ubuntu
```
2）执行一键安装Linux-NetSpeed网络加速脚本命令：
```
wget -N --no-check-certificate "https://raw.githubusercontent.com/sscles/Linux-NetSpeed/master/tcp.sh"
chmod +x tcp.sh
./tcp.sh
```
本脚本已不更新，推荐使用5.5以上内核自带的BBR速度最佳。
BBR加速哪个好？
如果你在生产环境中使用，夫子推荐你直接开启BBR原版进行网络加速，而不推荐使用一键脚本开启BBR加速；
否则，你可以随意使用一键脚本开启BBR/BBRplus/BBR2/BBR3/BBR魔改版/LotServer加速模式，折腾无极限。

## Credit
- [sing-reality-box](https://github.com/deathline94/sing-REALITY-Box)
- [sing-box](https://github.com/SagerNet/sing-box)
