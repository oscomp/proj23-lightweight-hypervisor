# proj23-lightweight-hypervisor
### 项目描述

本项目试图在RISC-V处理器上实现一个轻量级的Hypervisor。目前在RISC-V的Hypervisor规范一直没成型，主要在M模式下实现一套轻量级的Hypervisor，在QEMU模拟的RV64 virt上，让其支持RT-Thread Smart、Linux做为一个或多个GuestOS运行。

### 所属赛道

2021全国大学生操作系统比赛的“OS功能设计”赛道



### 参赛要求

- 以小组为单位参赛，最多三人一个小组，且小组成员是来自同一所高校的本科生（2021年春季学期或之后本科毕业的大一~大四的学生）
- 如学生参加了多个项目，参赛学生选择一个自己参加的项目参与评奖
- 请遵循“2021全国大学生操作系统比赛”的章程和技术方案要求



### 项目导师

**Jesven**

* github [jesven](https://github.com/jesven)

* email shaojinchun@rt-thread.com



### 难度

难



### 特征

Hypervisor支持qemu仿真，同时运行RT-Thread Smart与Linux的一个或多个GuestOS。



### 参考实现

https://github.com/RT-Thread/rt-thread/tree/rt-smart

### License

* [Apache-2.0](https://opensource.org/licenses/Apache-2.0)



## 预期目标

### 注意：下面的内容是建议内容，不要求必须全部完成。选择本项目的同学也可与导师联系，提出自己的新想法，如导师认可，可加入预期目标

### 第一题：Hypervisor基本功能在qemu上的实现

在RISC-V的M态实现Hypervisor支持，期望支持S态多操作系统的同时运行，实现S态操作系统的总物理内存分配，可选支持虚拟内存分配，实现串口设备及中断管理机制的虚拟化，并最终可同时在不同的串口终端上同时运行rt-smart与Linux。

### 第二题：Hypervisor控制台在qemu上的实现

在第一题实现的基础上，实现一个运行于独立的串口终端的控制台，该控制台可以对当前所有的虚拟机进行资源和运行管理，实现包括但不限于虚拟机的启动和结束、虚拟物理内存的分配等功能。

### 第三题：为Hypervisor增添SMP环境支持

为Hypervisor增添SMP环境支持，同时要求控制台支持相关的CPU核心分配操作，完成CPU核心虚拟化，使得各个操作系统可以使用指定数量和指定的CPU核心。

