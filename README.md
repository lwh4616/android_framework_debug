# android_framework_debug
调试android java层源码

1 首先建立代码层库
repo init -u https://android.googlesource.com/platform/manifest -b android-6.0.0_r1

国内镜像 repo init -u http://mirrors.ustc.edu.cn/aosp/platform/manifest -b android-6.0.0_r1

2 同步子木块 我们只需要framework代码就可以了
  repo sync platform/frameworks/base
  如果想看cpp代码 同步 repo sync platform/frameworks/native
3 使用Genymotion创建相对应的模拟器 6.0 nexus5

4 使用android studio带入framework源码 点击 attach  debugger to android process 
  如果想debug anroid server层的代码 选择system_server 进程 在相应的地方打断点.
  
  我主要用来调试AMS 在ActivityManagerService 的方法里面打断点。 上层的主要断点Activity ActivityStack Instumentation等一些关键方法
