这是一个构建VPN的脚本集合。来源都是基于网上的脚本，或者经过自己微调。作为程序猿一名，这方面以实用为主。

> 以下提到脚本均在Bandwagon Host上验证过

## 脚本列表

#### cisco_ipsec.sh 

适用于CentOS6和Ubuntu系统，已在CentOS 6.5 x86上验证过，在mac上使用时，`Share Secret`中填入`ipsec.secrets`的PSK的值。

#### pptp.sh

适用于CentOS6和Ubuntu系统，在CentOS 6.5 x86上验证过

#### ikev2\_cisco\_ipsec.sh

安装后可以连接ikev1/ikev2/以及Cisco IPSec，适用于CentOS6和Ubuntu系统，在CentOS 6.5 x86上验证过，但是x64系统有问题未能成功。并且发现在部分公司内网无法连上服务器。

此脚本源于[这里](https://github.com/quericy/one-key-ikev2-vpn)

安装完成后，如果要连接`Cisco IPSec`, 无需像IKEv2那样导入密钥，在mac上使用时，`Share Secret`中填入`ipsec.secrets`的PSK的值。

Mac系统如果要连接`IKEv2`，需要安装证书，下载`my_key/ca.cert.pem`证书文件，改名为`ca.cert.cer`, 在钥匙串上导入到系统证书里。remote id请填写服务器IP地址。这个值对应于`ipsec.secret`文件中的`leftid`的值。

#### l2tp_ipsec.sh

这个脚本包含了L2TP/IPSec, IKEV1, IKEV2, 以及 Cisci IPSec在内的几个VPN方案，实用StrongSwan原理上支持Bandwagon，我还没有尝试过。源于[这里](https://github.com/philpl/setup-strong-strongswan)

## 注意

Bandwagon Host基于OpenVZ，IPSec方法必须使用Strongswan，OpenSwan方案需要内核支持，所以目前未能用在Bandwagong的机器上。

X64系统上的ikev2.sh脚本未能成功安装配置，另外发现家里电信内网和移动4G网络都可以穿透正常使用，但是未能穿透公司内网。
