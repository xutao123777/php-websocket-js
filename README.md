# php-websocket-js
PHP操作websocket




Step #1：只能通过命令行调用PHP.exe开启websocket程序服务
Step #2：能否通过web开启websocket服务
不建议使用web开启websocket服务, 原因有下：
1、因为端口不能重复打开, 所以你必须保证 websocket.php 只会被运行一次

2、web 方式下的 php 是超时设置有效的, 当然你需要设置成永不超时

3、web 服务器是有超时限制的, 虽然时间比较长。应用程序长时间无数据输出, 将会被挂起或中断

4、如果 websocket.php 间歇的做标准输出的话, 可以解决 3 的问题。但会引发下一个问题

5、php 在向标准输出写的时候, 会检查到请求源的连接是否畅通。如果请求源被关闭了, 就会终止程序的运行
