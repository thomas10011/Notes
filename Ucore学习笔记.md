# Ucore学习笔记

## lab1

### make的执行过程

以下代码摘自make命令的输出。

```shell
+ cc kern/init/init.c
gcc -Ikern/init/ -march=i686 -fno-builtin -fno-PIC -Wall -ggdb -m32 -gstabs -nostdinc  -fno-stack-protector -Ilibs/ -Ikern/debug/ -Ikern/driver/ -Ikern/trap/ -Ikern/mm/ -c kern/init/init.c -o obj/kern/init/init.o
#编译kern/init/init.c 输出obj/kern/init/init.o
+ cc kern/libs/stdio.c
gcc -Ikern/libs/ -march=i686 -fno-builtin -fno-PIC -Wall -ggdb -m32 -gstabs -nostdinc  -fno-stack-protector -Ilibs/ -Ikern/debug/ -Ikern/driver/ -Ikern/trap/ -Ikern/mm/ -c kern/libs/stdio.c -o obj/kern/libs/stdio.o
+ cc kern/libs/readline.c
gcc -Ikern/libs/ -march=i686 -fno-builtin -fno-PIC -Wall -ggdb -m32 -gstabs -nostdinc  -fno-stack-protector -Ilibs/ -Ikern/debug/ -Ikern/driver/ -Ikern/trap/ -Ikern/mm/ -c kern/libs/readline.c -o obj/kern/libs/readline.o
#编译kern/libs/stdio.c readlin.c
#输出obj/kern/libs/stdio.o readline.o
+ cc kern/debug/panic.c
gcc -Ikern/debug/ -march=i686 -fno-builtin -fno-PIC -Wall -ggdb -m32 -gstabs -nostdinc  -fno-stack-protector -Ilibs/ -Ikern/debug/ -Ikern/driver/ -Ikern/trap/ -Ikern/mm/ -c kern/debug/panic.c -o obj/kern/debug/panic.o
+ cc kern/debug/kdebug.c
gcc -Ikern/debug/ -march=i686 -fno-builtin -fno-PIC -Wall -ggdb -m32 -gstabs -nostdinc  -fno-stack-protector -Ilibs/ -Ikern/debug/ -Ikern/driver/ -Ikern/trap/ -Ikern/mm/ -c kern/debug/kdebug.c -o obj/kern/debug/kdebug.o
+ cc kern/debug/kmonitor.c
gcc -Ikern/debug/ -march=i686 -fno-builtin -fno-PIC -Wall -ggdb -m32 -gstabs -nostdinc  -fno-stack-protector -Ilibs/ -Ikern/debug/ -Ikern/driver/ -Ikern/trap/ -Ikern/mm/ -c kern/debug/kmonitor.c -o obj/kern/debug/kmonitor.o
#编译kern/debug/panic.c kdebug.c kmonitor.c
#输出obj/kern/debug/panic.o kdebug.o kmonitor.o
+ cc kern/driver/clock.c
gcc -Ikern/driver/ -march=i686 -fno-builtin -fno-PIC -Wall -ggdb -m32 -gstabs -nostdinc  -fno-stack-protector -Ilibs/ -Ikern/debug/ -Ikern/driver/ -Ikern/trap/ -Ikern/mm/ -c kern/driver/clock.c -o obj/kern/driver/clock.o
+ cc kern/driver/console.c
gcc -Ikern/driver/ -march=i686 -fno-builtin -fno-PIC -Wall -ggdb -m32 -gstabs -nostdinc  -fno-stack-protector -Ilibs/ -Ikern/debug/ -Ikern/driver/ -Ikern/trap/ -Ikern/mm/ -c kern/driver/console.c -o obj/kern/driver/console.o
+ cc kern/driver/picirq.c
gcc -Ikern/driver/ -march=i686 -fno-builtin -fno-PIC -Wall -ggdb -m32 -gstabs -nostdinc  -fno-stack-protector -Ilibs/ -Ikern/debug/ -Ikern/driver/ -Ikern/trap/ -Ikern/mm/ -c kern/driver/picirq.c -o obj/kern/driver/picirq.o
+ cc kern/driver/intr.c
gcc -Ikern/driver/ -march=i686 -fno-builtin -fno-PIC -Wall -ggdb -m32 -gstabs -nostdinc  -fno-stack-protector -Ilibs/ -Ikern/debug/ -Ikern/driver/ -Ikern/trap/ -Ikern/mm/ -c kern/driver/intr.c -o obj/kern/driver/intr.o
#编译kern/driver/clock.c console.c  picirq.c intr.c
#输出obj/kern/driver/clock.o console.o picirq.o intr.o
+ cc kern/trap/trap.c
gcc -Ikern/trap/ -march=i686 -fno-builtin -fno-PIC -Wall -ggdb -m32 -gstabs -nostdinc  -fno-stack-protector -Ilibs/ -Ikern/debug/ -Ikern/driver/ -Ikern/trap/ -Ikern/mm/ -c kern/trap/trap.c -o obj/kern/trap/trap.o
+ cc kern/trap/vectors.S
gcc -Ikern/trap/ -march=i686 -fno-builtin -fno-PIC -Wall -ggdb -m32 -gstabs -nostdinc  -fno-stack-protector -Ilibs/ -Ikern/debug/ -Ikern/driver/ -Ikern/trap/ -Ikern/mm/ -c kern/trap/vectors.S -o obj/kern/trap/vectors.o
+ cc kern/trap/trapentry.S
gcc -Ikern/trap/ -march=i686 -fno-builtin -fno-PIC -Wall -ggdb -m32 -gstabs -nostdinc  -fno-stack-protector -Ilibs/ -Ikern/debug/ -Ikern/driver/ -Ikern/trap/ -Ikern/mm/ -c kern/trap/trapentry.S -o obj/kern/trap/trapentry.o
#编译kern/trap/文件夹下的trap.c vectors.S trapentry.S
#生成obj/kern/trap/trap.o vectors.o trapentry.o

+ cc kern/mm/pmm.c
gcc -Ikern/mm/ -march=i686 -fno-builtin -fno-PIC -Wall -ggdb -m32 -gstabs -nostdinc  -fno-stack-protector -Ilibs/ -Ikern/debug/ -Ikern/driver/ -Ikern/trap/ -Ikern/mm/ -c kern/mm/pmm.c -o obj/kern/mm/pmm.o
#编译kern/mm/pmm.c
#生成obj/kern/mm/pmm.o

+ cc libs/string.c
gcc -Ilibs/ -march=i686 -fno-builtin -fno-PIC -Wall -ggdb -m32 -gstabs -nostdinc  -fno-stack-protector -Ilibs/  -c libs/string.c -o obj/libs/string.o
+ cc libs/printfmt.c
gcc -Ilibs/ -march=i686 -fno-builtin -fno-PIC -Wall -ggdb -m32 -gstabs -nostdinc  -fno-stack-protector -Ilibs/  -c libs/printfmt.c -o obj/libs/printfmt.o
#编译libs/string.c printfmt.c
#生成libs/printfmt.c

+ ld bin/kernel
ld -m    elf_i386 -nostdlib -T tools/kernel.ld -o bin/kernel  obj/kern/init/init.o obj/kern/libs/stdio.o obj/kern/libs/readline.o obj/kern/debug/panic.o obj/kern/debug/kdebug.o obj/kern/debug/kmonitor.o obj/kern/driver/clock.o obj/kern/driver/console.o obj/kern/driver/picirq.o obj/kern/driver/intr.o obj/kern/trap/trap.o obj/kern/trap/vectors.o obj/kern/trap/trapentry.o obj/kern/mm/pmm.o  obj/libs/string.o obj/libs/printfmt.o
#链接成可执行文件bin/kernel

+ cc boot/bootasm.S
gcc -Iboot/ -march=i686 -fno-builtin -fno-PIC -Wall -ggdb -m32 -gstabs -nostdinc  -fno-stack-protector -Ilibs/ -Os -nostdinc -c boot/bootasm.S -o obj/boot/bootasm.o
+ cc boot/bootmain.c
gcc -Iboot/ -march=i686 -fno-builtin -fno-PIC -Wall -ggdb -m32 -gstabs -nostdinc  -fno-stack-protector -Ilibs/ -Os -nostdinc -c boot/bootmain.c -o obj/boot/bootmain.o
#编译boot/bootasm.S bootmain.c
#输出obj/boot/bootasm.o bootmain.o

+ cc tools/sign.c
gcc -Itools/ -g -Wall -O2 -c tools/sign.c -o obj/sign/tools/sign.o
gcc -g -Wall -O2 obj/sign/tools/sign.o -o bin/sign
#编译tools/sign.c 生产sign.o 转化为库文件sign

+ ld bin/bootblock
ld -m    elf_i386 -nostdlib -N -e start -Ttext 0x7C00 obj/boot/bootasm.o obj/boot/bootmain.o -o obj/bootblock.o
#链接生成二进制文件bin/bootblock

'obj/bootblock.out' size: 492 bytes
build 512 bytes boot sector: 'bin/bootblock' success!
#obj/bootblock.out大小为492字节，提示构建512字节的bin/bootblock文件成功

#先解释一下dd命令
#dd是linux下强大的数据复制工具。
#if = FILE 表示从FILE中读取数据。
#of = FILE 表示写入数据到FILE中。
#ibs = BYETS 表示读取数据时，一次性读BYTES大小的块。不指定默认512字节。
#obs = BYETS 表示写入数据时，一次性写BYTES大小的块。不指定默认512字节。
#count = N 表示总共读取或者写入N * ibs(obs)字节数的数据。
dd if=/dev/zero of=bin/ucore.img count=10000
10000+0 records in
10000+0 records out
5120000 bytes (5.1 MB, 4.9 MiB) copied, 0.0195807 s, 261 MB/s
#从/dev/zero文件(“零”设备，无限提供0x00)中读取数据
#写入到bin/ucore.img文件中
#count=10000表示读取10000*512字节的数据
#即ucore.img大小为5,120,000字节。

#拓展
#/dev/null “空设备”，任何输入到这个设备的数据都被丢弃。
#/dev/random 随机数设备，依赖系统中断不断产生随机字节流。产生速度较慢，但随机性好。
#/dev/urandom 不依赖系统中断，速度快，随机性较低。

#conv = notrunc 表示如果目的文件已经存在，那么不要截断文件内容。默认会截断成0字节大小。一般配合oflag = append使用，不截断并且以追加的方式写入数据。
dd if=bin/bootblock of=bin/ucore.img conv=notrunc
1+0 records in
1+0 records out
512 bytes copied, 5.4334e-05 s, 9.4 MB/s
#将bootblock写入ucore.img的第一个块

#seek = 1 表示从输出文件ucore.img跳过一个块再开始复制。
#skip = blocks 表示从输入文件跳过blocks个块再开始复制。
dd if=bin/kernel of=bin/ucore.img seek=1 conv=notrunc
146+1 records in
146+1 records out
74816 bytes (75 kB, 73 KiB) copied, 0.000374306 s, 200 MB/s
#将kernel复制到ucore.img中。

```



### i8086的启动过程

i8086有20根地址总线，实模式下内存空间布局如下：

| 起始    | 结束    | 大小           | 用途                                                         |
| ------- | ------- | -------------- | ------------------------------------------------------------ |
| 0xFFFF0 | 0xFFFFF | 16B            | BIOS入口地址，此地址也属于BIOS代码，同样属于顶部64KB。这里的16字节的内容是长跳转指令jmp F000:E05B |
| 0xF0000 | 0xFFFEF | 64KB-16B       | BIOS范围是F0000～FFFFF共64KB，最上面的16字节是BIOS入口地址。 |
| 0xC8000 | 0xEFFFF | 160KB          | 映射硬件适配器的ROM或者内存映射式I/O。                       |
| 0xC0000 | 0xC7FFF | 32KB           | 显示适配器BIOS。                                             |
| 0xB8000 | 0xBFFFF | 32KB           | 用于文本模式显示适配器。                                     |
| 0xB0000 | 0xB7FFF | 32KB           | 用于黑白显示适配器。                                         |
| 0xA0000 | 0xAFFFF | 64KB           | 用于彩色显示适配器。                                         |
| 0x9FC00 | 0x9FFFF | 1KB            | EBDA(Extended BIOS Data Area)扩展BIOS数据区。                |
| 0x07E00 | 0x9FBFF | 622080B约608KB | 可用区域。                                                   |
| 0x07C00 | 0x07DFF | 512B           | MBR被BIOS加载到此处，共512字节。                             |
| 0x00500 | 0x07BFF | 30464B约30KB   | 可用区域。                                                   |
| 0x00400 | 0x004FF | 256B           | BIOS Data Area(BIOS数据区)。                                 |
| 0x00000 | 0x003FF | 1KB            | Interrupt Vector Table(中断向量表)。                         |

- 从低地址向高地址看，0到0x9FFFF为DRAM，有640KB。

- 顶部的0xF0000到0xFFFFF为ROM，有64KB，储存BIOS代码。

- PC加电后，CS寄存器初始化为**0xF000**，IP寄存器初始化为**0xFFF0**，于是CPU执行的第一条指令的地址是**CS:IP = 0xFFFF0**，是一条跳转指令**jmp F000:E05B**。开始BIOS执行过程。

- BIOS主要做两件事：初始化硬件和建立中断向量表。建立中断向量表，其他程序就能通过中断调用BIOS已经实现的硬件控制函数。

- BIOS的最后一项工作是校验0盘0道1扇区的内容，如果BIOS发现这个扇区最后两个字节是0x55AA，那么BIOS就会将这个扇区的内容加载到内存0x7C00处，用的是命令**jmp 0:7C00**。之后的工作便交给BOOTLoader(MBR)。

> 拓展
>
> 到了32位的80386 CPU时代，内存空间扩大到了4G，多了段机制和页机制，但Intel依然很好地保证了80386向后兼容8086。
>
> 地址空间的变化导致无法直接采用8086的启动约定。如果把BIOS启动固件编址在0xF000起始的64KB内存地址空间内，就会把整个物理内存地址空间隔离成不连续的两段，一段是0xF000以前的地址，一段是1MB以后的地址，这很不协调。
>
> 为此，intel采用了一个折中的方案：默认将执行BIOS ROM编址在32位内存地址空间的最高端，即位于4GB地址的最后一个64KB内。在PC系统开机复位时，CPU进入实模式，并将CS寄存器设置成0xF000，将它的shadow register的Base值初始化设置为0xFFFF0000，EIP寄存器初始化设置为0x0000FFF0。所以机器执行的第一条指令的物理地址是0xFFFFFFF0。
>
> 80386的BIOS代码也要和以前8086的BIOS代码兼容，故地址0xFFFFFFF0处的指令还是一条长跳转指令`jmp F000:E05B`。注意，这个长跳转指令会触发更新CS寄存器和它的shadow register，即执行`jmp F000 : E05B`后，CS将被更新成0xF000。表面上看CS其实没有变化，但CS的shadow register被更新为另外一个值了，它的Base域被更新成0x000F0000，此时形成的物理地址为Base+EIP=0x000FE05B，这就是CPU执行的第二条指令的地址。
>
> 此时这条指令的地址已经是1M以内了，且此地址不再位于BIOS ROM中，而是位于RAM空间中。由于Intel设计了一种映射机制，将内存高端的BIOS ROM映射到1MB以内的RAM空间里，并且可以使这一段被映射的RAM空间具有与ROM类似的只读属性。所以PC机启动时将开启这种映射机制，让4GB地址空间的最高一个64KB的内容等同于1MB地址空间的最高一个64K的内容，从而使得执行了长跳转指令后，其实是回到了早期的8086 CPU初始化控制流，保证了向下兼容。



### BootLoader执行过程

BIOS将通过读取硬盘主引导扇区到内存，并转跳到对应内存中的位置执行bootloader。bootloader完成的工作包括：

- 切换到保护模式，启用分段机制
- 读磁盘中ELF执行文件格式的ucore操作系统到内存
- 显示字符串信息
- 把控制权交给ucore操作系统

对应其工作的实现文件在lab1中的boot目录下的三个文件asm.h、bootasm.S和bootmain.c。



### BootLoader进入保护模式的过程

#### 全局描述符表

和一个段有关的信息需要8个字节（64）位来描述，所以称为段描述符（Segemnt Descriptor）。每个段需要一个描述符，为了存放这些描述符，需要在内存中开辟一段空间。这段空间里，所有的描述符都是挨在一起，集中存放的，这就构成一个段描述符。

主要的段描述符表是**全局描述符表**（Global Descriptor Table, GDT）。所谓全局，意味着是为整个软硬件系统服务的。在进入保护模式前，必须定义全局描述符表。

处理器内部有一个48位的寄存器，称为**全局描述符表寄存器**（GDTR），用于跟踪全局描述符表。寄存器分为32位的线性地址和16位的边界。32位的线性基地址保存的是全局描述符表在内存中的起始地址，16位边界部分保存的是全局描述符表的边界（界限），在数值上等于表的大小减一。

由于GDT的界限是16位的，所以该表最大2^16^字节，也就是65536字节（64KB）。而一个段描述符大小8字节，故最多可以定义2^13^也就是8192个段描述符。

