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


## 第一次执行脚本安装出现这个报错  重启下服务器即可
```bash
WARNING: WireGuard does not seem to be running.
You can check if WireGuard is running with: systemctl status wg-quick@wg0
If you get something like "Cannot find device wg0", please reboot!
```
