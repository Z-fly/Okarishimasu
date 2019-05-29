# 租借女友
**彼女、お借りします**

### 92话起同步更新
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
## 使用方法
1. 安装Python3
https://www.python.org/downloads/
2. 命令行执行pip install opencv-python
3. 安装SDK Platform Tools
https://developer.android.google.cn/studio/releases/platform-tools.html
下载解压至$PATH目录<br>Linux&Mac OS X：/usr/local/bin/<br>Windows ：C:\WINDOWS\
4. 连接安卓手机，在任意目录执行本脚本
