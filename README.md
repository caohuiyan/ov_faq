# FAQ of OpenVINO
持续更新中。。。。。
## 运行脚本出错  
2020.2版本的demo中使用opencv读取video出错：CvCapture_MSMF::initStream Failed to set mediaType (stream 0, (0x0 @ 1) MFVideoFormat_RGB32 (unsupported media type)
![](https://github.com/caohuiyan/ov_faq/blob/master/screenshots/failed_to_set_media_type_Q.jpg)  
### 解决办法：
2020.1版本没有问题，2020.2需进一步调查...  
## 运行脚本出错  
此时不应有xxx：  
![](https://github.com/caohuiyan/ov_faq/blob/master/screenshots/%E6%AD%A4%E6%97%B6%E4%B8%8D%E5%BA%94%E6%9C%89_Q.jpg)
### 解决办法：  
检查环境变量Path的值，删掉有问题的值（后面可以重新添加）  
https://software.intel.com/en-us/forums/intel-distribution-of-openvino-toolkit/topic/849044?language=en-us&https=1#  
This problem in OpenVINO 2020.2 release being considered as a bug. Problem is related to media files with audio streams and MSMF backend.  
Meanwhile, you can use one of the following workarounds:  
1. Install FFmpeg as VideoCapture backend (on Windows you need to download OpenCV community plugin. There's downloader script in the package: openvino\opencv\ffmpeg-download.ps1. Right click on it - Run with PowerShell).  
2. Use hot fix available in upstream https://github.com/opencv/opencv/pull/17406  
3. Use media file without audio stream  

## demo_security_barrier_camera.bat 出错
CMake Error: Could not create named generator Visual Studio  
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
