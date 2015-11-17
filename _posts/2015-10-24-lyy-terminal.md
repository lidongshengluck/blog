---
layout: post
title:  'linux termine study'
date:   '2015-10-24 23:21:20'
categories: linux
---
# 2015-10-24
## terminal键入技巧
- shift+insert粘贴
- ctrl++字变大，ctrl+字变小
- ctrl+p上一条指令，ctrl+n下一条指令
- gdb ./～调式～
- ctrl+r寻找以前打开过的文件，可以输入关键字寻找
- vi ~/.vim/mydoc/index/doc/REANME.txt是打开vim参考手册
- vi ~/.vim/conf.d/.vim-leadermap.vimrc看
- 当/var/run/yum.pid已锁定pid运行，此时无法进行新的yum。解决方案：rm -f /var/run/yum.pid将文件删除，再运行yum
- 解xxx.tar压缩文件的指令为：tar -xf xxx.tar
- rm为删除指令
- ctrl+c 清除停止当前指令并开始新的一条指令
- #while killall -USR1-dd; do sleep 5; done。此指令可以看dd转载文件时的时间进程
- 格式化u盘：mkfs.vfat /dev/xxx,其中xxx是yongfdisk -l指令先查出usb所在设备位置的名称
- root下用fdisk -l看硬盘情况
- mount装载，umont卸载
- 文件转载 #dd if=xxx of=/dev/xxx。其中if是inputfile后接目录下的文件，of是outputfile后接目标设备
- alt+i当前屏幕最大最小切换
- alt+o水平分出一新屏
- alt+e垂直分出一新平
