# 1.Anaconda下载配置

[最新版最详细Anaconda新手安装+配置+环境创建教程_anaconda配置-CSDN博客](https://blog.csdn.net/qq_44000789/article/details/142214660)

# 2.CUDA+Pytorch安装配置

[2024年Pytorch + CUDA配置教程（Windows版）手把手教学，详细讲解_windows pytorch cuda-CSDN博客](https://blog.csdn.net/m0_65482549/article/details/141195825)

[CUDA与CUDNN在Windows下的安装与配置（超级详细版）_cudnn安装windows-CSDN博客](https://blog.csdn.net/YYDS_WV/article/details/137825313)

# 3.Pytorch安装配置

[Conda虚拟环境管理（创建、删除、进入、退出）详细教程_conda退出虚拟环境-CSDN博客](https://blog.csdn.net/m0_74738450/article/details/135827553)

## 遇到的最严重的问题：

![image-20241025182347251](C:\Users\17541\AppData\Roaming\Typora\typora-user-images\image-20241025182347251.png)

明明已经安装上pytorch了，但是：

![image-20241025204127852](C:\Users\17541\AppData\Roaming\Typora\typora-user-images\image-20241025204127852.png)



问题！！！！！！！

为什么找不到，因为是在

![image-20241025182512449](C:\Users\17541\AppData\Roaming\Typora\typora-user-images\image-20241025182512449.png)

在windows 的power shell中怎么可能找到呢，我在虚拟环境（mypy1)中安装的，自然要去虚拟环境中去import torch呀，宋提到这个问题我才恍然大悟，一直在找什么别的问题啊啊啊，应该早点去问的，（又印证了那句话：学计算机遇到一些问题赶紧找个懂的人问一问，人家的两句话就能解决你几个小时解决不了的问题。前提是你已经独立解决了很久了，实在是找不到办法了。）

在虚拟环境中python下不久一下子搞定了嘛，真是两行教程搞了一下午。

![image-20241025204142250](C:\Users\17541\AppData\Roaming\Typora\typora-user-images\image-20241025204142250.png)

此次教训，铭记于心！！！

## 配PyCharm本地conda环境+解释器

[[已解决\] pycharm添加本地conda虚拟环境 + 配置解释器 - pycharm找不到conda可执行文件_pytharm添加conda环境找不到可执行文件-CSDN博客](https://blog.csdn.net/weixin_57972634/article/details/143037457)



终于成了woc！

![image-20241025204027531](C:\Users\17541\AppData\Roaming\Typora\typora-user-images\image-20241025204027531.png)
