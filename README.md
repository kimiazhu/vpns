这是一个构建VPN的脚本集合。

包括：

- cisco_ipsec.sh, 适用于CentOS6和Ubuntu系统，在CentOS 6.5 x86上验证过，支持Bandwagon host
- pptp.sh, 适用于CentOS6和Ubuntu系统，在CentOS 6.5 x86上验证过，支持Bandwagon host
- ikev2.sh, 适用于CentOS6和Ubuntu系统，在CentOS 6.5 x86上验证过，但是x64系统有问题未能成功，支持Bandwagon host

## 注意

Bandwagon Host基于OpenVZ，IPSec方法必须使用Strongswan，OpenSwan方案需要内核支持，所以目前未能用在Bandwagong的机器上。
