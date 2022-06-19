# solve problem on yolov4+cmake+cuda v11.6(v11.7bug)+cudnn v11.x+opencv+darknet

# **環境建置**
 opencv download網址:https://opencv.org/releases/

cuda toolkit網址(要下載別的版本只要改網址):https://developer.nvidia.com/cuda-11-6-0-download-archive?target_os=Windows&target_arch=x86_64&target_version=10&target_type=exe_local

cudnn網址(需登入):https://developer.nvidia.com/cudnn


![Image](https://user-images.githubusercontent.com/74455348/172022402-84b2321e-1558-4945-821f-ae7e245f68d2.png)


darknet網址:https://github.com/AlexeyAB/darknet

git網址:https://git-scm.com/

### **參考影片**

https://www.youtube.com/watch?v=PVf16gIhnek&ab_channel=%E6%9F%AF%E6%9F%AF 

### **遇到問題**

1. darknet建置時所遇到問題:
類似
![Image](https://user-images.githubusercontent.com/74455348/172022510-6c8d6cb1-c093-491d-ab80-0b02e879b57b.png)

遇到MSB372且有寫compute_xx,sm_xx等....
這時就要改darknet屬性中的
CUDA C/C++ ->Device -> Code Generation
改成你顯示卡的運算能力(改成以下應該都可)

![Image](https://user-images.githubusercontent.com/74455348/172022727-0c784936-325d-465c-9fc5-f1a1c602e706.png)

**你顯示卡的運算能力看這!!**:https://zh.wikipedia.org/wiki/CUDA
<br>在此表下找自己顯卡型號
![Image](https://upload.cc/i1/2022/06/16/xZwSLz.png)
