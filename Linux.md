# 多进程
### 0、1、2号进程
idle进程：系统创建的第一个进程，加载系统。
systemd进程：系统初始化，是所有其他用户进程的祖先。init
kthreadd进程：负责所有内核进程的调度和管理。
### 进程标识
每个进程都有一个非负整数表示的唯一进程ID。

查看进程：```ps -ef |grep 进程名```

```getpid(void)```，获取进程ID。

```getppid(void)```，获取父进程ID。
### fork函数
一个现有的进程调用函数fork创建一个新的进程。

子进程和父进程继续执行fork函数后的代码。

fork函数调用一次，返回两次。

子进程返回0，父进程返回子进程的进程ID。

子进程是父进程的副本。

子进程获得了父进程的数据空间、堆和栈的副本，不是共享。
