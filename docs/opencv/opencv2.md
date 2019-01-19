# python中opencv的使用教程
在之前的文章中，已经介绍了Anaconda的使用，并安装tensorflow作为示例，opencv模块的安装也是一样的，这里不做过多介绍。以下是学习过程中的代码。

#### 图片的加载
```python
import cv2
img = cv2.imread("logo.png",1)
cv2.imshow("image",img)
cv2.waitKey(0)
```

#### 图片的写入
```python
import cv2
img = cv2.imread("logo.png",1)
cv2.imwrite("test.png",img)
```

#### 图片质量有损压缩
```python
import cv2
img = cv2.imread("logo.png",1)
cv2.imwrite("imageText1.png",img,[cv2.IMWRITE_JPEG_QUALITY,50])
```

#### 图片无损压缩
```python
import cv2
img = cv2.imread("logo.png",1)
cv2.imwrite("imageText.png",img,[cv2.IMWRITE_PNG_COMPRESSION,0])
```

#### 图片像素的获取和写入
```python
import cv2
img = cv2.imread("logo.png",1)
(b,g,r) = img[100,100]
print(b,g,r)
for i in range(1,100):
    img[10+i,100]=[255,0,0]

cv2.imshow("image",img)
cv2.waitKey(0)
```