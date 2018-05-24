# CVDL_course_project
A CVPR PKU course project

小组成员：大逸子、狗神、白哥、杨海欣

## 奋斗精神

不说太多，这个项目是10000个大作业，我们要一起**把它做好**！

## 任务说明

- 任务是遥感图像的分割。

- 目前所用模型是U-Net （[arXiv:1505.04597](https://arxiv.org/abs/1505.04597), 2015）和 Hourglass ([arXiv:1603.06937](https://arxiv.org/abs/1603.06937), 2016)。

- 数据集地址在[这里](https://files.inria.fr/aerialimagelabeling/NEW2-AerialImageDataset.zip)，包含了奥斯丁等地区的建筑物图像分割。

## 目标计划

- 在这个数据集上达到一个不错的结果。

- 如果能有时间处理一下其他数据集更好。

- 想办法得到国土规划局的土地规划方案，利用模型将其与中国目前的遥感卫星图片做对比，试图找出违反了规划要求的地方，标出地理位置和挪用土地面积。

- 写报告、做ppt…

## 现存问题

- 目前第一个模型已经在训练中，但训练速度比较缓慢，主要原因在计算资源**严重匮乏**。我们急需更强力的计算资源，如果哪位同学的实验室有深度学习相关的资源，赶快**老实交代**；如果没有，大逸子跟李老师交涉一下，看能不能用一下他们实验室的GPU。

- 模型loss的可视化做得还不是特别好，cuda还存在memory不够而导致程序崩溃的问题，希望同志们**帮助修改**。

- 估计简单用U-Net分割效果不会特别好，之后很可能还要改进。如果有同学了解图像处理相关知识（比如预处理、传统方法进行分割），或者很懂深度网络调参（逸子和狗神经验不足），麻烦**喊一嗓子**，方便之后的讨论。

- 在获得国土规划分布上面的工作还没有开始开展，要求目前不高，不用上来就全国，从某个地方区县开始就可以。需要证明我们“能做”就够。

## 阶段任务

- 想办法做一下正负样本均衡，然后多训几个epoch，看效果能不能变好…

- 在有了一定的准确率后，我们打算借鉴一下DeepLab，用空洞卷积来搭建网络，然后借助Graphcut之类的算法进行后处理。这样就可以宣布计划中第一条完成了。

![Lena镇楼](https://github.com/Barak123748596/CVDL_course_project/blob/master/lena.jpg)