# wireguard_ipv4_ipv6


#### 此脚本支持 ipv4 和 ipv6   转发所有流量，一般只有把 VPN 当做武当纵云梯来用时，才会需要转发所有流量，不多说，点到为止。


####  同样如果想连上本地连上 云服务器的内网ip地址 修改脚本 这部分内容内的 AllowedIPs 

```bash

	# Create client file and add the server as a peer
	echo "[Interface]
PrivateKey = ${CLIENT_PRIV_KEY}
Address = ${CLIENT_WG_IPV4}/32,${CLIENT_WG_IPV6}/128
DNS = ${CLIENT_DNS_1},${CLIENT_DNS_2}

[Peer]
PublicKey = ${SERVER_PUB_KEY}
PresharedKey = ${CLIENT_PRE_SHARED_KEY}
Endpoint = ${ENDPOINT}
AllowedIPs = 0.0.0.0/0,::/0
PersistentKeepalive = 30" >>"${HOME_DIR}/${SERVER_WG_NIC}-client-${CLIENT_NAME}.conf"


```


### 此处关于 ipv6 的 AllowedIPs  修改未经验证， 本处只是提示可以如此修改