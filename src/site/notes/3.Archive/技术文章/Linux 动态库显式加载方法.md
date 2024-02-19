---
{"dg-publish":true,"dg-path":"技术文章/Linux 动态库显式加载方法.md","permalink":"/技术文章/Linux 动态库显式加载方法/","updated":"2024-01-30T09:45:21.263+08:00"}
---

#Technomous #Compile 

通过包含 `<dlfcn.h>` 头文件我们便可使用 Linux 上的动态库操作函数。以下介绍其中常用的函数。

# dlopen


``` c
void * dlopen(const char* pathname, int mode)
```

dlopen 函数以指定模式打开指定的动态链接库，并返回一个句柄给调用进程。
# dlsym

``` c
void * dlsym(void* handle, const char* symbol)
```

dlsym 根据动态链接库操作句柄（pHandle）与符号（symbol），返回符号对应地址。使用这个函数不但可以获取函数地址，也可以获取变量地址。

# dlclose

``` c
int dlclose(void *handle)
```

dlclose 用于关闭指定句柄的动态链接库，只有当此动态链接库的使用计数为 0 时，才会真正被系统卸载。

# dlerror

``` c
const char *dlerror(void) 
```

当动态链接库操作函数失败时，dlerror 可以返回出错信息，返回值为 NULL 时表示操作函数执行成功。
