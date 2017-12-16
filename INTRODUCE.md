# 内容介绍

Secure shell (SSH)

Red Hat 企业版 Linux 7 (RHEL 7) 在某些方面与 RHEL 6 相比有明显改进。两者之间的主要区别有：

- 新的服务管理器 systemd 提供了新功能，并且相比 Upstart 和原来的 SysVinit 系统，引导速度更快。
- RHEL 7 的默认文件系统是 XFS 文件系统，支持最高 500TB 的文件系统。
- firewalld 守护进程配置一个基于区域的防火墙。
- GNOME 3 是默认的桌面环境。
- 可从 RHEL 6 直接升级。

在生产系统上，以 root 用户账户身份登录到系统是一个非常危险的做法，但是它是管理 RHEL 的最快捷方法。

命令提示假定用户使用 root 用户账户。当登录到 root 账户时，则会看到如下所示的命令行提示：

    [root@server1 root]#

由于这个提示的长度可能会导致文中的代码换行或断行，因此这里把这个 root 账户的提示简化为：

    #

特别需要注意，哈希标记 (#) 在 Linux 脚本和程序里用作注释字符。

当我们以普通用户登录到 Linux 系统时，就会看到稍微不同的提示。
假设采用 michael 用户登录到系统，则通常情形下系统的提示如下所示：

    [michael@server1 michael]$

同样，我们把上面的提示简化为

    $

有些命令会超出一行的长度，例如：

    # virt-install -n outsider1.example.org -r 1024 --disk
    path=/var/lib/libvirt/images/outsider1.example.org.img,size=16
    -l ftp://192.168.122.1/pub/inst -x ks=ftp://192.168.122.1/pub/ks1.cfg

除非这个命令经过精心排列，否则换行符可能会出现在错误的位置，如出现在 --disk 开关前面的两个短划线之间。
解决这个问题的方法之一是使用反斜杠符号 (\) ，它转义表示其后的回车符(反斜杠也可以转义空格，因此可以方便地使用长文件名)。
这样，<red>虽然下面的内容看起来在4个不同的行里，但是根据反斜杠符号的作用， Linux 会把它当作一个命令来处理</red>。

    # virt-install -n outsider1.example.org -r 1024 --disk \
    > path=/var/lib/libvirt/images/outsider1.example.org.img,size=16 \
    > -l ftp://192.168.122.1/pub/inst \
    > -x ks=ftp://192.168.122.1/pub/ks1.cfg

下面的命令列出所有已安装在本地系统上的程序包：

    # rpm --query --alll

当我们在自己的 RHEL 7 系统上执行这个命令时，它列出了 1300 个程序包。

相反，下面的命令列出本地系统上所有程序包里的文件：

    # rpm --query -all

当我们在自己的 RHEL 7 系统里执行上述命令时，它列出 143 000 个文件。这个结果完全不同于前一个命令的结果。因此，必须注意短划线。

