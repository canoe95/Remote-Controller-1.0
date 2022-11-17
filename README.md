## 基于Java Socket 的远程控制程序

Listener.jar：本地端用套接字不断连接服务器的 8088 端口（死循环），实际上这里的套接字从某种意义上来说像是一个服务器

Server.jar：服务器上跑一个 socket 服务器，用于和远端的客户通信和接受网页 socket 的请求，当在网页上输入密码正确时，将创建一个 socket 并向服务器的 8088 端口（即远端的 socket 服务器）发送一串字符

Remote-Controller.war：提供网页服务，向 Server.jar 发出请求，Listener.jar 监听 Server.jar 对相应请求作出反应
