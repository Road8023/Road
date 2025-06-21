## 一键安装
```
bash <(curl -sL https://raw.githubusercontent.com/Road8023/Road/OVO/V/docker-install-xray/install_xray_without_ssl.sh)
```
## Shadowsocks 一键部署
```
bash -c "$(curl -L https://raw.githubusercontent.com/Road8023/Road/refs/heads/OVO/V/docker-install-xray/shadowsocks-auto.sh))"
```
## 卸载
```
docker rm -f xray && rm -rf /etc/xray
```
