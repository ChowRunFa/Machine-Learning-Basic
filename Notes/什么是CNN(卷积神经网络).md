## 什么是卷积神经网络

卷积神经网络(Convolutional Neural Network)，在一个个填充着数字的正方形小格子，它们被称为卷积核。

<img src="https://img-blog.csdnimg.cn/aabbcc53f4c24064825a89ab3abb2fdf.png" alt="请添加图片描述" style="zoom:50%;" />

原始图片经过输入层后，会变为灰度或是RGB数值填充的矩阵

<img src="https://img-blog.csdnimg.cn/8cafb44fb29b4cabb04da26828f2a253.png" alt="请添加图片描述" style="zoom:50%;" />

将卷积核与图片矩阵对齐，对应格子中的数字相乘后再相加，再将得到的数字填入新矩阵，这就是卷积。

<img src="https://img-blog.csdnimg.cn/623c9e55a2264cab87f77d214379e30e.png" alt="请添加图片描述" style="zoom:50%;" />

卷积核以一定的距离在图像上移动运算，这被称为步长，得到的新矩阵能反映图像的部分特征，因此被称为特征图。它们既是这一层的输出，也是下一层的输入。

<img src="https://img-blog.csdnimg.cn/e01ad40ed33c4454a3b795640b5bfba0.png" alt="请添加图片描述" style="zoom:50%;" />

设置不同的卷积核，我们就能找到各种各样的特征。要如何设计它们？还记得训练吗？对于**CNN**来说，训练就是让网络根据已有的数据和它们的标签，自动确定卷积核中的数字。

以拥有5个卷积层的AlexNet为例，边缘、纹理、组成...，以人眼的角度观察，越靠后的卷积层提取出的特征越抽象。

<img src="https://img-blog.csdnimg.cn/8e25a736ddab4f2091ba07c9ed63dfdf.png" alt="请添加图片描述" style="zoom:50%;" />

除了卷积层，CNN还有两个重要的配件，池化层和全连接层。池化层能选取图像的主要特征，常用的Maxpooling是保留窗口覆盖区域的最大数值，矩阵被池化后，参数会大量减少。

<img src="https://img-blog.csdnimg.cn/bb4e65112285480baa6c1b07b3b0be88.png" alt="请添加图片描述" style="zoom:50%;" />

全连接层通常在网络的最后，能将提取到的特征集合在一起，给出图片可能是某种事物的概率。

<img src="https://img-blog.csdnimg.cn/b2becde4f9254aec94c30f1274337c41.png" alt="请添加图片描述" style="zoom:50%;" />

CNN非常擅长处理图像，正是它在各类比赛中的优异表现引领了深度学习潮流，不仅如此，将声音当作图谱处理可以完成语音识别，将词语作为向量处理可以完成机器翻译...总而言之，CNN是个不可多得的好工具。