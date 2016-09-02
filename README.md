这是一个构建VPN的脚本集合。来源都是基于网上的脚本，或者经过自己微调。作为程序猿一名，这方面以实用为主。

> 以下提到脚本均在Bandwagon Host上验证过

## 脚本列表

- cisco_ipsec.sh, 适用于CentOS6和Ubuntu系统，在CentOS 6.5 x86上验证过
- pptp.sh, 适用于CentOS6和Ubuntu系统，在CentOS 6.5 x86上验证过
- ikev2.sh, 适用于CentOS6和Ubuntu系统，在CentOS 6.5 x86上验证过，但是x64系统有问题未能成功。部分公司内网不能正常使用。
- l2tp_ipsec.sh, 这个脚本包含了L2TP/IPSec, IKEV1, IKEV2, 以及 Cisci IPSec在内的几个VPN方案，实用StrongSwan原理上支持Bandwagon，我还没有尝试过。

## 注意

Bandwagon Host基于OpenVZ，IPSec方法必须使用Strongswan，OpenSwan方案需要内核支持，所以目前未能用在Bandwagong的机器上。

X64系统上的ikev2.sh脚本未能成功安装配置，另外发现家里电信内网和移动4G网络都可以穿透正常使用，但是未能穿透公司内网。
