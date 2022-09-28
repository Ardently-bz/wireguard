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
如果遇到不明白的，可以参考这篇文章的注解：

WireGuard 教程：WireGuard 的搭建使用与配置详解  https://icloudnative.io/posts/wireguard-docs-practice/
剩下这几篇文章是可选的，有兴趣就看看：

我为什么不鼓吹 WireGuard  https://icloudnative.io/posts/why-not-wireguard/
Why not “Why not WireGuard?”  https://icloudnative.io/posts/why-not-why-not-wireguard/
WireGuard 教程：使用 DNS-SD 进行 NAT-to-NAT 穿透   https://icloudnative.io/posts/wireguard-endpoint-discovery-nat-traversal/   

WireGuard 教程：使用 Prometheus 监控 WireGuard   https://icloudnative.io/posts/monitoring-wireguard-using-prometheus/

