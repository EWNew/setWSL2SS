# setWSL2SS
# 设置WSL2代理



# 配置代理
export hostip=$(cat /etc/resolv.conf |grep -oP '(?<=nameserver\ ).*')

alias setss='export https_proxy="http://${hostip}:7890";export http_proxy="http://${hostip}:7890";'

alias unsetss='unset http_proxy;unset https_proxy'


参考：https://solidspoon.xyz/2021/02/17/%E9%85%8D%E7%BD%AEWSL2%E4%BD%BF%E7%94%A8Windows%E4%BB%A3%E7%90%86%E4%B8%8A%E7%BD%91/