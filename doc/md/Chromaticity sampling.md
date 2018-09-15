
# 色度采样
彩色图像，则为RGB图像(也可以是CMYK)，有三个通道的信息，这也是当代最常见的彩色图像。首先，我们要知道一个像素具有两个信息：明度值表示像素的亮度；色度值表示像素的色彩。如果把一个画面里面的像素的明度值去掉，则会获得一张黑色的照片；如果把色度值去掉，则获得了一个黑白的画面，这也是彩色照片变为黑白照片的原理。  
因此彩色图像转换为黑白图像极其简单，属于有损压缩数据；反之则很难，因为数据不会凭空增多。但其实，彩色图像需要保留明度值信息，但不一定要保留色度值信息，可以由多个像素来共享一个色度值，来呈现同样的颜色，这样可以大大减少数据量，同时也方便我们的算法、模型设计。
首先，我们单独分离画面的明度Y，然后预测得到两个色度通道Cr和Cb。最后，我们把这些信息结合一起，我们仍可以得到一张与RGB图像没有差别的彩色图片。YCrCb就是色度采样中最常用的色度模式。
