# 3D Gaussian Splatting 模型训练和可视化学习



## 数据集

### 标准数据集

   Tanks&Temples 和 Deep Blending 的 SfM 数据集

### 自制数据集

    参考`https://blog.csdn.net/fluoxetine_drug/article/details/146329939`和`https://www.cnblogs.com/milton/p/18904741`

    1. 拍摄一段视频
    2. 使用脚本`从视频提取帧序列.py`文件提取帧序列，或采用`ffmpeg`将视频转为连续图片
    3. 使用3dgs自带的convert.py脚本将连续图片帧转点云。此处需要安装`COLMAP`，注意会输出三个重要文件：`points3D.bin`（重建的点云信息）、`cameras.bin`（相机参数）和`images.bin`（每张图片的位姿和关键点）。详细介绍见`https://colmap.github.io/format.html`。
   
    
## 训练

### 实验运行环境

    1. 运行平台信息

        autoDL（云服务平台）
        租用的硬件资源：1 张 RTX3090

    2. 环境配置（software environment / runtime environment

       系统：Ubuntu 20.04
       Python 版本：3.8
       PyTorch 版本：2.0.0
       CUDA 版本：11.8

### 训练方法

    1. 训练方法采用`train.py`脚本

## 可视化方法

    1. 三维可视化采用`https://superspl.at/editor`

    2. ply文件数据查看采用`脚本\ply文件查看器.html`