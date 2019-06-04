# 租借女友
**彼女、お借りします**<br>
正版地址：https://manga.bilibili.com/m/detail/mc26446


### 92话起同步更新
91话之前的可以去bika看，百度一搜能直接下APP的。<br>
整话打包见Releases，页面短网址：http://vurl.cn/zjny1

### QQ群：239120775
加群连接：https://dwz.cn/WPAooGMb

```python
#!/usr/bin/env python3
from os import path, popen, remove
from cv2 import imread, imwrite, IMWRITE_JPEG_QUALITY

while input() != "q":
    for i in range(1, 100):
        if not path.isfile(f"{i:0>2d}.jpg"):
            popen("adb exec-out screencap -p > " + str(i) + ".png").read()
            im = imread(str(i) + ".png")
            imwrite(f"{i:0>2d}.jpg", im[190:1730, 0:1920], [int(IMWRITE_JPEG_QUALITY), 80])
            remove(str(i) + ".png")
            print(f"{i:0>2d}.jpg")
            break
else:
    exit(0)

```
## 使用说明
此脚本用于把漫画资源截图导出到脚本运行目录，并裁剪压缩，对其它漫画同理，更改[190:1730, 0:1920]裁剪参数即可。
运行时按回车键顺序截图，按q回车退出，也可按Ctrl+C快速退出。

## 使用方法
1. 安装Python3<br>
https://www.python.org/downloads/
2. 命令行执行pip install opencv-python
3. 安装SDK Platform Tools<br>
https://developer.android.google.cn/studio/releases/platform-tools.html
<br>下载解压至$PATH目录<br>Linux&Mac OS X：/usr/local/bin/<br>Windows ：C:\WINDOWS\
4. 连接安卓手机，手机上打开USB调试，在任意目录执行本脚本

## 使用举例
新建目录，打开命令行，CD至此目录，打开手机，用数据线连接电脑，手机上打开漫画APP，点击阅读漫画某话的第1页，执行脚本，按下回车键，出现01.jpg，然后翻页，按下回车键，出现02.jpg，依此类推，直到这话翻完。<br>输入q回车退出，之后可使用压缩命令`7z -mx=9 a filename.7z *`打包，至此一个流程结束，上传到网站。
