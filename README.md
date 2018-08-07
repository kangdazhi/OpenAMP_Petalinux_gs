# OpenAMP_Petalinux_gs
该文档主要讲解如何使用OpenAMP框架实现多核处理器核间通信，包括开发环境的搭建、工程的建立和编译等，并在需要的时候介绍所涉及的Virtio、RPMsg组件的工作原理。由于xilinx提供的基于OpenAMP框架的内核模块需要在Linux系统上电启动完成后对其中一个处理器核心进行reset，然后初始化软件运行环境，从而实现双核心的独立工作；基于实际项目需求，需要在上电的时候两个处理器就处于完全独立状态，分别启动执行自己的程序，所以需要对内核模块程序进行重新设计，具体代码见/src/demo_without_using_remoteproc/
