# # WireGuard installer

**This project is a bash script that aims to setup a [WireGuard](https://www.wireguard.com/) VPN on a Linux server, as easily as possible!**

## Requirements

Supported distributions:

- Ubuntu >= 16.04
- Debian >= 10
- Fedora
- CentOS
- Arch Linux
- Oracle Linux

## Usage

   bash wireguard-install-ipv4.sh
    
  IPv4 or IPv6 public address:    输入服务公网ip地址或者域名
  Public interface:   可回车直接使用默认
  WireGuard interface name:   可回车直接使用默认  
  Server's WireGuard IPv4:    vip虚拟机网段可以使用默认 只要不跟服务端 客户端网段冲突即可
  Server's WireGuard port [1-65535]:  WireGuard 服务所使用的 UDP 端口
  First DNS resolver to use for the clients:  DNS 根据自己情况来设置 我设置的是 233.5.5.5
  Second DNS resolver to use for the clients (optional):  DNS 根据自己情况来设置 我设置的是 114.114.114.114  

  Client name: test    客户端文件的名称
  Client's WireGuard IPv4:   客户端vpn 虚拟ip地址 可以直接默认使用




It will install WireGuard (kernel module and tools) on the server, configure it, create a systemd service and a client configuration file.

Run the script again to add or remove clients!


## 第一次执行脚本安装出现这个报错 提示wg-quick 启动失败  reboot重启下服务器即可
```bash
WARNING: WireGuard does not seem to be running.
You can check if WireGuard is running with: systemctl status wg-quick@wg0
If you get something like "Cannot find device wg0", please reboot!
```


# # WireGuard 参考文档 

WireGuard 教程：WireGuard 的工作原理     https://icloudnative.io/posts/wireguard-docs-theory/

WireGuard 快速安装教程   https://icloudnative.io/posts/configure-wireguard-using-wg-gen-web/

WireGuard 配置教程：使用 wg-gen-web 来管理 WireGuard 的配置 https://icloudnative.io/posts/wireguard-full-mesh/ 

Wireguard 全互联模式（full mesh）配置指南 https://icloudnative.io/posts/wireguard-full-mesh/


### 如果遇到不明白的，可以参考这篇文章的注解：

WireGuard 教程：WireGuard 的搭建使用与配置详解  https://icloudnative.io/posts/wireguard-docs-practice/


### 剩下这几篇文章是可选的，有兴趣就看看：

我为什么不鼓吹 WireGuard  https://icloudnative.io/posts/why-not-wireguard/

Why not “Why not WireGuard?”  https://icloudnative.io/posts/why-not-why-not-wireguard/

WireGuard 教程：使用 DNS-SD 进行 NAT-to-NAT 穿透   https://icloudnative.io/posts/wireguard-endpoint-discovery-nat-traversal/  


WireGuard 教程：使用 Prometheus 监控 WireGuard   https://icloudnative.io/posts/monitoring-wireguard-using-prometheus/

