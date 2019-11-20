---
title: 301服务器使用指南
date: 2019-11-20 12:01:00
categories: Technology
tags: linux 
---

2017 王沛正

# 301服务器使用指南

## 可用环境(其他需要可自行安装)

MATLAB, Mathematica, Python,Jupyter,Fortran, C/C++

## 远程连接服务器

参见

[使用putty远程连接linux](https://blog.csdn.net/qq_18297675/article/details/52566194)

[使用Xshell远程连接Linux服务器](https://blog.csdn.net/jam_fanatic/article/details/83754814)



**内网! 内网! 内网!**

比如在一教连上CQUNET后就是内网，插上网线也是内网

IPaddress: 10.250.113.17

Port: 5013/5015

--------------------

## linux基础

### 如何切换目录

比方说有目录:/home/username/local/c

当前目录:/home/username

    cd local    #进入local文件夹

当前目录:/home/username/local

    cd .. #返回上一级目录

当前目录:/home/username

### 如何新建文件(文件夹)

    mkdir dirname #建立一个名字为dirname的文件夹

    cd dirname #进入文件夹dirname

    touch filename #建立一个名字为filename的文件

例:

    mkdir c

    cd c

    touch test.c

### 如何打开文件

* 如果是文件夹，直接cd即可打开

* 编辑(打开)文本文件:

        vi test.c #vi 如何使用参见下条

* 程序文件:

        ./filename #打开当前目录下的filename

### 如何使用VIM

参见：[linux-vim](https://www.runoob.com/linux/linux-vim.html)

-----------

## MATLAB(Mathematica)

直接在命令行输入MATLAB，Xshell+Xmanager会显示MATLAB图形化界面

## Fortran(C/C++)

在合适的位置创建一个文件夹作为存放***.f90的文件夹

    touch ***.f90 #建立f90文件
    vi ***.f90 #用vim打开文件
    gfortran ***.f90 -o ***    #第二个***是输出文件名称
    ./***

C语言同理，将上面第三行编译语句换为下面的就好

    gcc helloworld.c -o helloworld
