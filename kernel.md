# 1、Linux内核准备
## 1.1 获取内核源码
- Linux内核官方网站：http://www.kernel.org
- git：
``` shell
git clone https://github.com/torvalds/linux.git
```
- - - - -
## 1.2 安装内核源码
``` shell
$ cd /usr/src/kernel
$ tar xzvf linux-2.6.32.tar.gz
```
- - - - -
## 1.3 使用补丁
``` shell
diff -Nur newfile oldfile
patch -p1 < ../patch-x.y.z
```
``` shell
for i in `ls ../patch`; \ 
do patch -p1 < ../patch/"$i";done
```
- - - - -
## 1.4 内核源码树

| 目录 | 描述 |
| :---: | :---: |
| arch | 特定体系结构的源码 |
| block | 块设备I/O层 |
| crypto | 加密API |
| Documention | 内核源码文档 |
| drivers | 设备驱动程序 |
| firmware | 使用某些驱动程序而需要的设备固件 |
| fs | VFS和各种文件系统 |
| include | 内核头文件 |
| init | 内核引导和初始化 |
| ipc | 进程间通信 |
| kernel | 像调度程序这样的核心子系统 |
| lib | 管理内核函数 |
| mm | 内核管理子系统和VM |
| net | 网络子系统 |
| samples | 实例，实例代码 |
| scripts | 编译内核使用的脚本 |
| security | Linux安全模块 |
| sound | 语音子系统 |
| usr | 早期用户空间代码（initramfs）|
| tools | 在Linux开发中有用的工具 |
| virt | 虚拟化基础结构 |
- - - - -
## 1.5 编译内核
内核配置
- `make menuconfig`
- `make config`
- `make xconfig`
- `make defconfig`

- `make clean`
- `make distclean`

配置之后会产生.config文件  
内核编译：
- `make`
- `make modules`
- `make modules_install`
- `make install`
- `/sbin/depmod 2.6.31.8`
- `make -jn`

模块安装到 `/lib/modues`
- - - - -
## 1.6 内核开发的特点
- 内核编程时既不能访问`C`库也不能访问标准的`C`头文件；
- 内核编程时必须使用`GNU C`；
- 内核编程时缺乏想用户空间那样的内存保护机制；
- 内核编程时难以执行浮点运算；
- 内核给每个进程只有一个很小的定长堆栈；
- 由于内核支持异步中断、抢占和`SMP`，因此必须时刻注意同步和并发；
- 要考虑可移植性的重要性。

- 查看内核打印消息：`dmesg`或`cat /var/log/message`
- 清空当前内核消息：`dmesg -c`
- 插入内核模块：`insmod HelloWorld.ko`
- 查看内核模块：`lsmod`
- 删除内核模块：`rmmod HelloWorld.ko`
- - - - -
## 1.7 第一个内核模块程序
`HelloWord.c`
``` C
#Include <linux/init.h>
#Include <linux/module.h>
MODULE_LICENSE("Dual BAD/GPL")
static int hello_init(void) {
    printk(KERN_INFO "Hello, world!\n");
    printk("Hello: module loaded at 0x%p", hello_init);
    printk("HZ = %d\n", HZ);
}
static void hello_exit(void) {
    printk(KERN_INFO "Goodbye, cruel word!\n"); 
    printk("By: module loaded at 0x%p\n", hello_exit);
}
module_init(hello_init);
module_exit(hello_exit);
MODULE_AUTHOR("harlonxl@gmail.com");
MODULE_DESCRIPTION("Hello world, first kernel module");
```
- - - - -
# 2、进程管理
## 2.1 进程
- 进程就是处于运行期的程序以及相关资源的总称，是操作系统进行资源分配和调度的基本单位，进程通常包含一些资源，例如打开的文件描述符，挂起的信号，内核内部数据，处理器状态，一个或者多个具有内存映射的内存地址空间及一个或多个执行线程，还有用来存放全局变量的数据段等。
- 执行线程是在进程中的活动对象，是`CPU`调度的最小单位，每个线程拥有独立的程序计数器，进程栈和一组进程寄存器。
- linux系统下查看进程：
``` shell
# ps aux
USER       PID %CPU %MEM    VSZ   RSS TTY      STAT START   TIME COMMAND
root         1  0.0  0.1  43272  3672 ?        Ss   Jun07   0:26 /usr/lib/systemd/systemd --switched-root --system --deserialize 21
root         2  0.0  0.0      0     0 ?        S    Jun07   0:00 [kthreadd]
root         3  0.0  0.0      0     0 ?        S    Jun07   0:21 [ksoftirqd/0]
root         5  0.0  0.0      0     0 ?        S<   Jun07   0:00 [kworker/0:0H]
root         7  0.0  0.0      0     0 ?        S    Jun07   0:00 [migration/0]
root         8  0.0  0.0      0     0 ?        S    Jun07   0:00 [rcu_bh]
root         9  0.0  0.0      0     0 ?        R    Jun07   2:29 [rcu_sched]
root        10  0.0  0.0      0     0 ?        S    Jun07   0:10 [watchdog/0]
root        12  0.0  0.0      0     0 ?        S    Jun07   0:00 [kdevtmpfs]
root        13  0.0  0.0      0     0 ?        S<   Jun07   0:00 [netns]
root        14  0.0  0.0      0     0 ?        S    Jun07   0:00 [khungtaskd]
root        15  0.0  0.0      0     0 ?        S<   Jun07   0:00 [writeback]
root        16  0.0  0.0      0     0 ?        S<   Jun07   0:00 [kintegrityd]
root        17  0.0  0.0      0     0 ?        S<   Jun07   0:00 [bioset]
root        18  0.0  0.0      0     0 ?        S<   Jun07   0:00 [kblockd]
root        19  0.0  0.0      0     0 ?        S<   Jun07   0:00 [md]
root        25  0.0  0.0      0     0 ?        S    Jun07   0:00 [kswapd0]
root        26  0.0  0.0      0     0 ?        SN   Jun07   0:00 [ksmd]
...
```
`ps`命令参数含义：
- `a`：打印所有进程
- `u`：以用户为主打印进程
- `x`：显示所有进程，不区分终端
- - - - -
## 2.2 进程描述符及任务结果
进程描述符`task_struct`，该结构定义在`<linux/sched.h>`中，放在一个双向循环循环链表。
``` C
struct task_struct {
    /** 进程状态 */
    volatile long state;	 /* -1 unrunnable, 0 runnable, >0 stopped */
    ...
    /** 进程描述符链表 */
    struct list_head tasks;
	struct plist_node pushable_tasks;
    /** 虚拟内存结构 */
	struct mm_struct *mm, *active_mm;
    ...
    /** 进程PID */    
    pid_t pid; 
    /** 线程组的领导线程ID */    
	pid_t tgid;
	...
	struct task_struct *real_parent; /* real parent process */
	/** 父进程进程描述符 */
	struct task_struct *parent;
	/** 子进程链表 */
	struct list_head children;
	...
	/** 文件系统信息 */
	struct fs_struct *fs;
    /** 进程打开文件的信息 */
	struct files_struct *files;
    /** 命名空间 */
	struct nsproxy *nsproxy;
    ...
}
```
查看linux系统中`pid`的最大值：
``` shell
# cat /proc/sys/kernel/pid_max 
32768
```
- - - - -
### 2.2.1 分配进程描述符
linux是通过`slab`分期器来分配 `task_struct`结构，这样能达到对象复用和缓存着色`(cache coloring)`的目的。
- - - - -
### 2.2.2 进程描述符的存放
在内核中，访问任务通常要获得指向task_struct的指针，可以通过`current`宏查找当前正在运行进程的进程描述符。硬件体系不同，这个宏的实现是不同的，例如：`PowerPC`中，专门有一个寄存器来存放该宏，而对于`x86`这种寄存器比较缺的体系结构，只能在栈的尾端创建`thread_info`结构，通过计算偏移间接地查找 `task_struct`结构。
在`x86`系统中，`current`把栈指针的后13个有效位屏蔽掉，用来计算`thread_info`的偏移，该操作是通过`current_thread_info()`函数来完成的。
```C
static inline struct thread_info *current_thread_info(void)
{
	return (struct thread_info *)
		(current_stack_pointer & ~(THREAD_SIZE - 1));
}
```
`thread_info`结构体如下：
``` C
struct thread_info {
	struct pcb_struct	pcb;		/* palcode state */

	struct task_struct	*task;		/* main task structure */
	unsigned int		flags;		/* low level flags */
	unsigned int		ieee_state;	/* see fpu.h */

	struct exec_domain	*exec_domain;	/* execution domain */
	mm_segment_t		addr_limit;	/* thread address space */
	unsigned		cpu;		/* current CPU */
	int			preempt_count; /* 0 => preemptable, <0 => BUG */

	int bpt_nsaved;
	unsigned long bpt_addr[2];		/* breakpoint handling  */
	unsigned int bpt_insn[2];

	struct restart_block	restart_block;
};
```
`thread_info`的地址在栈顶，如下图所示：
<div align=center><img width="500" src="https://github.com/Harlonxl/Learning-Note/blob/master/image/thread_info.png"/></div>

- - - - -

### 2.2.3 进程状态
进程描述符`state`域描述了当前进程的状态，系统中的每个进程必然处于五种进程状态中的一种：
- `TASK_RUNING`：运行状态，进程时可运行的，它或者正在执行，或者在运行队列找那个等待运行。
- `TASK_INTERRUPTIBLE`：可中断，进程正在睡眠，等待某些条件的达成。一旦条件达成，内核就会把进程状态置为运行，处于此状态的进程也会因为接收到信号而提前被唤醒并随时准备投入运行。
- `TASK_UNINTERRUPTIBLE`：不可屏蔽，除了就算接收到信号也不会被唤醒或准备投入运行外，这个状态与可中断状态相同。
- `_TASK_TRACED`：被其他进程跟踪的进程，例如通过`ptrace`对调试程序进行跟踪。
- `_TASK_STOPPED`：停止状态，进程停止运行。
<div align=center><img width="800" src="https://github.com/Harlonxl/Learning-Note/blob/master/image/task_state.jpeg"/></div>
<div align=center>进程状态转化图</div>

- - - - -
### 2.2.4 设置当前进程状态
通过函数`set_task_state(task, state)`函数来设置，必要的时候设置内存屏障来强制其他处理器作重新排序。否则，等同于：
``` C
task->state = state;
```
- - - - -
### 2.2.5 进程上下文
当一个程序执行了系统调用或者触发了某个异常，就陷入了内核空间，此时，我们称内核“代表进程执行”并处于进程上下文中，在此上下文中`current`宏是有效的。
- - - - -
### 2.2.6 进程创建
Unix进程创建是通过两个函数来执行的：`fork()`函数和`exec()`函数。
- `fork()`：拷贝当前进程创建一个子进程，子进程与父进程的区别仅仅在于`PID`、`PPID`和某些资源和统计量（如，挂起的信号）。linux的`frok()`使用写时拷贝实现的，`fork()`创建子进程时，并不会复制父进程的地址空间，而是共享父进程的地址空间，只有对需要写入的时候，数据才会被复制，这种延迟拷贝的机制提高了`exec()`函数的效率。
- `exec()`：负责读取可执行文件并将其载入地址空间开始运行。
- - - - -
### 2.2.7 fork()函数调用过程
`fork()`函数的实际开销就是拷贝父进程的页表以及为子进程创建唯一的进程描述符。`fork()`、`vfork()`和`__clone()`库函数都是根据自己需要的参数标记去调用`clone()`函数，然后由`clone()`调用`do_fork()`，`clone()`声明如下：
``` C
int clone(int (*proc)(void *), void *sp, int flags, void *data);
```
`clone()`函数也是linux用来创建线程的函数，其参数含义如下：
- `proc`：线程调用的函数；
- `sp`：线程使用的堆栈；
- `flags`：用于控制进程的行为，例如共享打开文件等
- `data`：线程函数的参数

`do_fork()`函数调用`copy_process()`函数完成创建工作：
- 调用`dup_task_struct()`为新进程创建一个内核栈、`thread_info`结构和`task_struct`，这些值与当前的进程的值相同。此时，子进程与父进程的描述符是完全相同的；
- 检查并确保创建这个子进程后，当前用户所拥有进程数目没有超出给它分配的资源的限制；
- 子进程设置自己的`task_struct`中的一些字段；
- 子进程的状态设置为`TASK_UNINTERRUPTIBLE`；
- 调用`alloc_pid()`为新进程分配一个有效`pid`；
- 之后根据`clone()`函数的参数，拷贝或者共享打开的文件、文件状态信息、信号处理函数、进程地址空间和命名空间等。
- - - - -
### 2.2.8 vfork()
`vfork()`函数不会拷贝进程表项，子进程不能写地址空间，并且`vfork()`会让子进程先执行，子进程和父进程共享堆栈、数据段，`vfork()`函数存在的意义就是创建子进程之后调用`exec()`函数族，现在由于`fork()`函数有了写时拷贝机制，`vfrok()`的意义并不大，最好不要使用`vfork()`函数。  
- - - - -
## 2.3 线程在linux中的实现
linux内核并不区分线程和进程，每个线程都拥有唯一隶属于自己的`task_struct`，只不过与另一个进程（父进程）共享某些资源。  
其他操作系统的实现可能是提供了专门支持线程的机制，通常称作为轻量级进程（`LWP`）。  
### 2.3.1 线程创建
线程创建的调用过程如下：
``` C
clone(CLONE_VM | CLONE_FS | CLONE_FILES | CLONE_SIGHAND, 0);
```
线程共享地址空间、文件系统资源、打开的文件描述符和信号处理程序等。
`fork()`的创建如下：
``` C
clone(CLONE_SIGHAND, 0);
```
`vfork()`的创建如下：
``` C
clone(CLONE_VFORK | CLONE_VM | CLONE_SIGHAND, 0);
```
`clone()`函数的这些参数是在`<linux/sched.h>`中定义的。
- - - - -
### 2.3.2 内核线程
内核线程是用来在后台执行一些操作，内核线程与普通线程的区别在于内核线程没有独立的地址空间，其`task_struct`的`mm`为`NULL`，只在内核空间运行，内核线程和普通线程一样，可以被调度，也可以被抢占。  
内核线程只能由内核线程来创建，linux是通过`kthreadd`内核进程找中衍生出所有新的内核线程，接口定义在`<linux/kthread.h>`中。
``` C
truct task_struct *kthread_create(int (*threadfn)(void *data),
				   void *data,
				   const char namefmt[], ...)
	__attribute__((format(printf, 3, 4)));
```
`threadfn`是内核线程运行的函数，`data`是传递的参数，`namefmt`是内核线程的参数，创建的内核线程不会自动运行，要通过`wake_up_process()`函数唤醒它并运行，这两个操作可以通过`kthread_run()`来完成：
``` C
#define kthread_run(threadfn, data, namefmt, ...)			   \
({									   \
	struct task_struct *__k						   \
		= kthread_create(threadfn, data, namefmt, ## __VA_ARGS__); \
	if (!IS_ERR(__k))						   \
		wake_up_process(__k);					   \
	__k;								   \
})
```
内核线程会一直运行直到调用`do_exit()`，或者内核的其他部分调用`kthread_stop()`函数：
``` C
int kthread_stop(struct task_struct *k);
```
- - - - -
# 2.4 进程终结
虽然有些伤感，但进程始终还是要终结的，内核必须释放它所占有的资源，并把这一不幸进一步告知父进程。
进程可能会调用`exit()`函数终结，也有可能接受到了不可处理也不能忽略的信号，不管进程怎么终结的，该任务大部分会通过`do_exit()`来完成，定义在`kernel/exit.c`中：
- 将`task_struct`中的标志成员设置为`PF_EXITING`；
- 调用`acct_update_integrals()`函数输出记账信息；
- 调用`exit_mm()`释放占用的`mm_struct`，如果没有其他进程共享，就彻底释放它们；
- 接着调用`exit_sem()`函数，如果进程排队等候`IPC`信号，则离开队列；
- 调用`exit_files()`和`exit_fs()`，分别递减文件描述符、文件系统数据的引用计数，如果某个引用计数为零，就释放其资源；
- 设置`task_struct`中的`exit_code`成员；
- 调用`exit_notify()`函数向父进程发送信号；
- 调用`schedule()`切换到新的进程。

此时进程不可运行，并处于`EXIT_ZOMBIE`退出状态，它所占用的内存就是内核栈、`thread_info`结构和`task_struct`结构，此时进程存在的唯一目的就是向进程提供信息。
- - - - -
### 2.4.1 删除进程描述符
进程退出时的清理工作和进程描述符的删除被分开执行的，通过`wait()`函数，调用`wait4()`系统调用来实现的，他的标准动作是，挂起调用他的进程，直到其中一个子进程退出，此时函数会返回该子进程的`PID`，此时调用该函数提供的指针会包含子进程的退出代码。  
最终释放进程描述符时，`release_task()`函数被调用：
- 调用`__exit_signal()`函数，该函数调用`_unhash_process()`，后者又调用`detach_pid()`从`pidhash`上删除该进程，同事也从任务列表中删除该进程；
- `_exit_signal()`释放目前僵死进程所用的所有剩余资源，并进行最终统计和记录；
- 如果该进程是进程组中最后一个进程，那么就要通知僵死的零头进程的父进程；
- 调用`put_task_struct()`释放进程内核栈和`thread_info`结构所占的页，并释放`task_struct`所占的`slab`高速缓存。
- - - - -
### 2.5.2 孤儿进程
如果父进程在子进程之前退出，子进程必须要找到一个新的父亲，不然子进程会一直处于僵死状态，白白耗费内存，对于这个问题，解决办法是子进程在当前进程组内找一个线程作为父亲，如果不行，就让`init`做他们的父进程。
- - - - -
# 3、进程调度
进程调度程序可看做在可运行态进程之间分配有限的处理器时间资源的内核子系统。
## 3.1 多任务
多任务操作系统就是能同时并发地交互执行多个进程的操作系统。多任务系统可以分为两类：
- 非抢占式多任务：让步
- 抢占式多任务：抢占、时间片
- - - - - 
## 3.2 Linux的进程调度
`2.5`之前：`O(1)`调度器
`2.6`之后：完全公平调度算法`CFS`
- - - - - 
## 4.3策略
### 4.3.1 I/O消耗型和处理器消耗型的进程
进程可以被分为I/O消耗型和处理器消耗型，前者是指处理器大多数时间都是再提交IO请求或者等待IO请求，而后者大多数都再运行代码，除非被抢占，这类任务通常会不停的运行，占用大量的`CPU`时间，调度器应该减少他们的执行频率。  
调度策略通常要在两个矛盾的目标中寻找平衡：响应时间和吞吐量，Unix系统的调度程序更倾向于`I/O`消耗程序，以提供更好的程序响应时间，Linux为了保证交互式应用和桌面系统的性能，所以对进程的响应做了优化（缩短响应时间），更倾向于`I/O`消耗进程。  
- - - - - 
### 4.3.2 进程优先级
Linux提供了两种优先级策略：  
- `nice`值：范围是`-20`到`19`，默认是`0`，值越大表示优先级越低，优先级越高会获得更多的处理器时间，Linux系统中，`nice`值代表时间片的比例，而Mac OS X中，进程的`nice`值代表分配给进程的时间片的绝对值。  
- 实时优先级：其值是可配置的，默认情况下从`0~99`，越高优先级越大，任何实时进程的优先级都高于普通进程。  
- - - - - 
### 4.3.3 时间片
时间片是一个数值，它表明进程在抢占前能够持续运行的时间。时间片的设置有很大的问题，如果时间片太长，导致有些任务无法及时调度， 如果太短，会明显增大进程切换的开销，前面提到的`I/O`消耗型进程希望时间片越小越好，这样能够及时的处理响应，而处理器消耗型希望时间片越长越好，尽可能多的占用处理器时间，能够明显的提高高速缓存的命中率。  
Linux的`CFS`并没有直接分配时间片到进程，而是将处理器的使用比例划分到进程，这样的话，进程获得的处理器时间和系统负载有密切的关系，这个比例还会受到`nice`值的影响。  
Linux中的`CFS`调度器，其抢占时机取决于新的可运行程序消耗了多少处理器使用比，如果消耗的使用比比当前进程小，则新进程立刻投入运行中，抢占当前进程，否则，推迟其执行。
- - - - - 
## 4.4 Linux调度算法
### 4.4.1 调度器类
Linux调度器是以模块的方式提供的，称作为调度器类，它允许多种不同的可动态添加的调度算法并存，调度属于自己的进程，每个调度器都有一个优先级，基础的调度器的代码位于`kernel/sched.c`文件中，它会按照优先级顺序遍历调度类，拥有一个可执行进程的最高优先级的调度器类生出，去选择下面要执行的一个程序。  
完全公平调度`(CFS)`是一个针对普通进程的调度类，在Linux中被称为`SCHED_NORMAL`，`CFS`算法实现定义在文件`kernel/sched_fair.c`中。


