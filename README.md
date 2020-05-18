# FAQ of OpenVINO
持续更新中。。。。。
## demo_security_barrier_camera.bat 出错
![](https://github.com/caohuiyan/ov_faq/blob/master/screenshots/vs_version_Q.jpg)
### 可能原因：  
安装 visual studio 的时候修改了默认路径，demo_security_barrier_camera.bat中没有找到相应的 visual studio 版本  
### 解决办法：  
在demo_security_barrier_camera.bat中加上visual studio版本信息  
![](https://github.com/caohuiyan/ov_faq/blob/master/screenshots/vs_version_A.jpg)  
## bad conversion 错误
![](https://github.com/caohuiyan/ov_faq/blob/master/screenshots/bad_conversio_Q.jpg)
### 可能原因：  
加载的模型路径中有中文  
### 解决办法：  
确保模型文件的路径中没有中文  
## 在Windows上配置环境变量  
参考：https://www.intel.cn/content/www/cn/zh/support/articles/000033440/boards-and-kits/neural-compute-sticks.html  
设置过程中参考 C:\Program Files (x86)\IntelSWTools\openvino\bin\setupvars.bat  
