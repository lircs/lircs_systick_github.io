---
title: aupe_note.md
date: 2018-01-18 14:33:31
tags:
---

linux 文件IO函数

> 本文介绍的函数被称为不带缓存的IO(unbuffered IO)，不带缓存是指每一个read、write函数都调用内核中的一个系统调用。
这些不带缓存的IO函数不是ANSIC C的组成部分，但是是POSIX.1和XPG3的组成部分。
> 文件描述符： 对于内核而言，所有打开的文件都由文件描述符引用，文件描述符是一个*非负整数*。按照惯例，UNIX shell
使文件描述符0与进程的标准输入(STDIN_FILENO)相结合，文件描述符1与进程的标准输出(STDOUT_FILENO)相结合，文件描述符2
与进程的标准错误输出(STDERR_FILENO)相结合。

## open函数

```c
#include <sys/types.h>
#include <sys/stat.h>
#include "fcntl.h"

//返回：若成功为文件描述符，若出错为-1
int open(const char *pathname, int oflag, .../*, mode_t mode */);
```

- read
- write
- lseek
- close


