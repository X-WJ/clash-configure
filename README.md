clash-configure

1,download clash_linux64.gz
2,gunzip clash_linux64.gz
3,chmod +x clash_linux64
4,configure configure.yaml

'''
# HTTP 代理端口
port: 7890 

# SOCKS5 代理端口

# Linux 和 macOS 的 redir 代理端口
redir-port: 7892 

# 允许局域网的连接
allow-lan: true

# 规则模式：Rule（规则） / Global（全局代理）/ Direct（全局直连）
mode: Rule

# 设置日志输出级别 (默认级别：silent，即不输出任何内容，以避免因日志内容过大而导致程序内存溢出）。
# 5 个级别：silent / info / warning / error / debug。级别越高日志输出量越大，越倾向于调试，若需要请自行开启。
log-level: silent
# Clash 的 RESTful API
external-controller: '0.0.0.0:9090'


'''

5,configure Country.mmdb  manual  (it will fail if your network is poor )
6,test run 
./clash -d ./  
in my computer likes :
/export/software/clash -d /export/software/ 
7,configure at http://clash.razord.top/#/rules 
8,configure loacl proxy
以 Ubuntu 19.04 為例，打開系統設置，選擇網絡，點擊網絡代理右邊的 ⚙ 按鈕，選擇手動，填寫 HTTP 和 HTTPS 代理為 127.0.0.1:7890，填寫 Socks 主機為 127.0.0.1:7891，即可啟用系統代理。

