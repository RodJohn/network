
外网ip和内网ip
宽带




子网掩码/ping通


1.用网线直接连接或通过HUB或普通交换机间连接的计算机之间要能够相互通，它们的网络地址必须相同

2.IP地址=网络地址+主机地址

3.网络地址=IP地址*子网掩码
将IP地址和子网掩码都换算成二进制，然后进行与运算，结果就是网络地址。
255.255.255.0 换算成二进制为 11111111·11111111·11111111·00000000 




网关
网关实质上是一个网络通向其他网络的IP地址。
比如有网络A和网络B，网络A的IP地址范围为“192.168.1.1~192. 168.1.254”，子网掩码为255.255.255.0；网络B的IP地址范围为“192.168.2.1~192.168.2.254”，子网掩码为255.255.255.0。在没有路由器的情况下，两个网络之间是不能进行TCP/IP通信的，即使是两个网络连接在同一台交换机(或集线器)上，TCP/IP协议也会根据子网掩码(255.255.255.0)判定两个网络中的主机处在不同的网络里。而要实现这两个网络之间的通信，则必须通过网关。如果网络A中的主机发现数据包的目的主机不在本地网络中，就把数据包转发给它自己的网关，再由网关转发给网络B的网关，网络B的网关再转发给网络B的某个主机



子网掩码

ip地址后边加个/8(16,24,32)
是掩码的位数，
A类IP地址的默认子网掩码为255.0.0.0（由于255相当于二进制的8位1，所以也缩写成“/8”，表示网络号占了8位）;
B类的为255.255.0.0（/16）;
C类的为255.255.255.0(/24)
/30就是255.255.255.252
/32就是255.255.255.255




