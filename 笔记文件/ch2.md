[TOC]



# .cpp文件编译

![image-20230823150244518](../../.config/Typora/typora-user-images/image-20230823150244518.png)

注意编译路径即可



# 库文件

静态库和共享库

静态库每次调用生成一个副本，共享库只有一个副本

![image-20230823160523681](../../.config/Typora/typora-user-images/image-20230823160523681.png)

使用共享库的只需要在add_library()中加入SHARE

假如将库文件链接去除，

![image-20230823160548744](../../.config/Typora/typora-user-images/image-20230823160548744.png)

调用库文件的函数的时候就会，报错找不到，该函数的定义