# test_udp

测试比较 kcp 、 raknet、enet、tcp 等库

## test1

- 测试内容

  服务器以 `一定频率` 发送 400 字节的数据包 (如 66 毫秒)，查看客户端前后2个包的时间间隔

- 参考意义

  帧同步游戏，服务器会定时广播数据包给客户端，因此能考察服务器的每帧其他玩家指令包到达本机的时间。

- 详细文档

  [test1/README.md](test1/README.md)

- 测试结果

  参见：<https://blog.csdn.net/u013272009/article/details/81430262>

## test2

- 测试内容

  回显测试，查看客户端发送 1 个包到服务会发该包的时间间隔（即 RTT 测试）

- 参考意义

  帧同步游戏，客户端发送战斗指令到服务器下帧回发战斗指令，因此能考察操作的流畅度

- 相比 test1

  本测试仅测试 Kcp，测试其他的已无意义

- 详细文档

  [test2/README.md](test2/README.md)

- 测试结果

  [test2/README.md](test2/README.md)
