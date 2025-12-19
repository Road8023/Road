# 📚 部署教程
# 第一步：准备工作
您需要准备：
 * 中转机 (Master)：一台拥有公网 IP 的服务器，用于部署控制面板。
 * 节点机 (Agent)：一台或多台用于实际转发流量的服务器（可以是那台中转机自己，也可以是其他国内/国外机器）。
# 第二步：两种方式
## 1.一键安装脚本（方式）
```
curl -o go_relay.sh https://raw.githubusercontent.com/Road8023/Road/refs/heads/OVO/V/relay/go_relay.sh && chmod +x go_relay.sh && ./go_relay.sh
```
## 2.编译与安装 (Master端方式)

假设您已经在 Master 服务器上。

 * 编译项目 (如果您没有 Go 环境，请先安装 Go 1.20+)：
 * 
###  下载代码并保存为 main.go
### 编译为 Linux 64位可执行文件
```
CGO_ENABLED=0 GOOS=linux GOARCH=amd64 go build -o relay main.go
```
### 赋予执行权限
```
chmod +x relay
```
 * 首次运行与配置：
   首次运行请直接启动，它会自动进入安装引导模式。
```
   ./relay -mode master
```
   此时终端会显示：面板启动: http://localhost:8888
