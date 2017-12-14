# 序

Linux 是一个<red>多用户</red>、<red>多任务</red>的开源操作系统，其低成本和高安全性等特点是其得到青睐的重要原因。

RHCSA 和 RHCE 是两个不同的考试，有各自的侧重点，然而二者之间也有重叠之处。Red Hat 提供了多种认证，而 RHCSA 和 RHCE 是这些
认证的<red>基础</red>，也就是说，必须先通过 RHCSA 和 RHCE ，Red Hat 才允许参加其他认证考试。

Red Hat 认证系统管理员考试 (Red Hat Certified System Administrators, RHCSA)

Red Hat 认证工程师考试 (Red Hat Certified Engineers, RHCE)

Red Hat 企业版 Linux (Red Hat Enterprise Linux, RHEL)

有了 KVM ，能在单台物理计算机上安装多个虚拟的、相互独立的 RHEL 系统 (及其他操作系统)。

许多公司已把众多塞满各种物理系统的房间转换为只包含有限几个系统的小机柜。在每个系统里都安装了许多虚拟机。

重构版本是由第三方根据相同的源代码生成得到的软件。另一方面，克隆版本是由不同源代码生成得到的软件。

安全是许多公司选择 Linux 的另一个理由。美国国家安全局已经开发出自己的 Linux 内核版本，
它在名为安全增强型 Linux (Security-Enhanced Linux, SELinux) 的系统里提供了基于上下文的安全。

RHEL 已经把 SELinux 当作分层安全策略的一个重要组成部分。

为准备 Red Hat 认证考试，需要准备一个至少由 3 台 Linux 计算机组成的网络。由于 RHCSA 考试的重点是虚拟机，因此
建议把其中两台 Linux 计算机用作 KVM 系统。配置了网络服务后，可通过另一台计算机检查操作结果。

## 如何获得 Red Hat 企业版 Linux 操作系统

RHEL 7 使用基于内核的虚拟机 (Kernel-based Virtual Machine, KVM)。

Red Hat 只支持64位CPU物理计算机上的 KVM 虚拟主机。

你可能需要在此64位硬件系统上安装两个或两个以上的虚拟机。虚拟机在多 CPU 系统或多核 CPU 系统上运行起来可能更好。建议64位硬件系统
至少要有 8GB 的 RAM ，16GB 的 RAM 也许会更好。

对于 Red Hat 企业版 Linux 7 ，Red Hat 修改为以下几个不同的版本：
- RHEL 服务器版本为3种不同类型的 CPU 架构提供了不同级别的技术支持：
    - 基于 AMD 和 Intel CPU 的 32 位和 64 位系统。其价格取决于 CPU 插槽数和支持虚拟访客的数量。
    - IBM POWER7 系统，其价格取决于 CPU 插槽数。
    - IBM z 系统。
- RHEL 桌面 (RHEL Desktop) 系统，它为工作站提供了各个级别的技术支持。
- RHEL 开发人员套件提供了 RHEL 7 和几个增件软件的下载访问，但只能将这些软件用于开发目的。
- RHEL 增件可用于高可用性、弹性存储和负载均衡及其他领域。




