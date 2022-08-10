Disco-Diffusion-Local V3.0 | [Disco-Diffusion-Local V2.0 +](./README.md)


# Disco-Diffusion-Local V3.0

基于 https://github.com/alembics/disco-diffusion  pyside2做了界面（持续更新），Windows 系统电脑可以，推荐6GB以上独显，30系列、20系列N卡最佳，AMD显卡不支持。

# 1、下载

## V3.0下载

## 提供多种方式下载

（1）百度网盘链接：链接：https://pan.baidu.com/s/1B0g4MPFe_drP_hRjgEnKGg 提取码：95kh

（2）天翼网盘链接：https://cloud.189.cn/t/ZZ7vuyZrMvmm (访问码:7dn8)

（3）谷歌网盘链接：https://drive.google.com/drive/folders/1mBtw3oz9rCsQflt5xzDw08Z9VRMDoB_T?usp=sharing

## 后续更新将网盘里的V3.1或V3.2或更新版本的exe文件拷贝到解压的主目录，运行对应版本exe就是最新版本了。

### 另外请注意：自己的C:\Users\User\AppData\Local\CrashDumps这个目录，有时候爆显存崩溃会遗留很大文件，删除即可，C:\Users\User\不同电脑不一样。


# 联系我解决问题

 ![image](https://github.com/zhaoyun0071/Disco-Diffusion-Local/blob/main/contact.png)


# 2、更新记录

## V3.0版本：2022-05-14

1、相比V2.0版本，引入新的内核架构，测试性能提升5%~10%；

2、上个版本爆显存的弹窗指示不够完善，删掉此功能，爆显存依然通过黑窗CUDA OUT OF MEMORY查看；

3、启动时，黑窗的引起误会的warning去除掉了；

4、简化V2.0版本的安装要求，将移动到C盘用户文件夹下的vgg16-397923af.pth模型，也归属到models文件夹，现在安装就很简单了，两部操作：解压到pic_disco文件夹；models文件夹移动到pic_disco文件夹即可完成安装。


# 3、安装
## 解压
解压pic_disco.zip，生成pic_disco目录，不要解压到C盘。
## 模型文件移动到指定目录
网盘里的models文件夹移动到pic_disco目录中；

## 打开软件
进入软件目录pic_disco，双击打开DD5_V3.0程序即可，软件界面如下所示
：
 ![image](https://github.com/zhaoyun0071/Disco-Diffusion-Local/blob/main/images/1.png)
 
## 软件配置

拥有详细的界面化设置，仅针对静图。
 ![image](https://github.com/zhaoyun0071/Disco-Diffusion-Local/blob/main/images/set1.png)
  ![image](https://github.com/zhaoyun0071/Disco-Diffusion-Local/blob/main/images/set2.png)
   ![image](https://github.com/zhaoyun0071/Disco-Diffusion-Local/blob/main/images/set3.png)
    ![image](https://github.com/zhaoyun0071/Disco-Diffusion-Local/blob/main/images/set4.png)

## 输出图片目录
pic_disco\images_out。

## 过程图片目录
pic_disco\progress.png，每几个step（频率可配置）更新一次图片。

# 4、显卡配置需求
可能需要至少6GB显存，以下为测试情况：

（1）	RTX2060 6G独显，图片尺寸256x512可行；

（2）	RTX1070 8G独显，250steps耗时预估2小时，图片尺寸1280x720；

（3）	RTX2070S 8G独显，450steps耗时预估16分钟，图片尺寸960x448；

（4）	RTX3090 24G独显，450steps耗时预估10分钟，图片尺寸1280x720。


注：默认参数因为选了3个CLIP模型，如果想要尺寸更大，少选几个模型即可，但效果肯定有所影响，诸如6G独显的2060显卡，之选如下第一个模型，尺寸768×512都没问题：

  ![image](https://github.com/zhaoyun0071/Disco-Diffusion-Local/blob/main/images/clip.png)

# 5、常见错误
下面这些都是图片设置过大导致的爆显存，或者6GB以下的显卡：

（1）	Unable to find a valid cuDNN algorithm to run convolution


（2）	CUDA out of memory


（3） 生成的图是黑色的，目前发现的1060、1660、1660ti都有问题，原因是中途生成NAN数据，解决方案正在寻找。



# 6、离线版生成图展示

下均是网友利用离线版V2.0+版本生成的图，供各位参考：

（1）默认参数下，仅尺寸改为1280×720，RTX3090生成

  ![image](https://github.com/zhaoyun0071/Disco-Diffusion-Local/blob/main/images/1.jpg)
  
（2）默认参数下，仅尺寸改为768×448，RTX3070-8G独显笔记本版生成

  ![image](https://github.com/zhaoyun0071/Disco-Diffusion-Local/blob/main/images/12.jpg)


（3）默认参数下，仅尺寸改为1280×512，RTX3090生成

  ![image](https://github.com/zhaoyun0071/Disco-Diffusion-Local/blob/main/images/122.jpg)

（4）默认参数下，仅尺寸改为1280×512，RTX3090生成

  ![image](https://github.com/zhaoyun0071/Disco-Diffusion-Local/blob/main/images/3.jpg)


