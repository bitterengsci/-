
考察C++、数据结构

多线程的了解
stl有什么？
vector扩充方式，size与capacity区别
顺序存储结构有哪些？
左值引用与右值引用
map与unordered map区别
const与static、const在函数前与函数后区别
虚函数与纯虚函数区别，虚函数关键字
函数memcpy 、memset的实现，手撕代码
一行代码求平方根
各种排序时间空间复杂度（快排，归并，桶排，堆排），手撕代码
二叉树排序、堆排序、希尔排序、桶排序时间复杂度（重要！因此重复）
最长公共子串、最长公共子序列，手撕代码
树的DFS与BFS、树的遍历，手撕代码
对于n个实例的k维数据，建立kd tree的时间复杂度
哈夫曼树带权路径长度、哈夫曼编码
长度为n的list，删除、插入与随机访问的计算复杂度
字符串子串数目
三维空间最近邻搜索的常用数据结构（八叉树、kd tree）
HashMap和Hashtable的比较
在一个二维数组中，每一行都按照从左到右递增的顺序排序，每一列都按照从上到下递增的顺序排序。请完成一个函数，输入这样的一个二维数组和一个整数，判断数组中是否含有该整数
10的答案（张同学的同学很给力）。放到10下面11就变成1了=_=，因此放到最后。
import math
print([n for n in range(2,X) if 0 not in [n%d for d in range(2,int(math.sqrt(n))+1)]])
如果import不算的话…
二：数学基础

考察概率论、线性代数、矩阵分析、数值优化

一层楼共有n级台阶，一次可以上至少一级但不超过m级台阶，求有多少种不同的上楼方案数。由于结果可能很大，你只需要输出结果对10007取模的值即可
拟合二维平面中的带噪声直线，其中有不超过20%的样本点远离了直线，另外80%的样本点可能有高斯噪声的偏移，要求输出为ax+by+c=0的形式，其中a>0且a^2+b^2=1
切比雪夫不等式、协方差与相关系数、各种分布、多元高斯分布
线性回归推导回归系数（y=kx，y=kx+b）
甲乙两人约好在某地碰面，时间段为10点到11点。若甲先到，最多会等待10分钟，10分钟内乙未出现则离开；若乙先到，最多会等待15分钟，15分钟内甲未出现则离开，请问两人见面的概率是多少？
ABCDE5个人互相传球，由A开始第一次传球，经5次传球最后回到A的手上，其中A与B不会互相传球，C只会传给D，E不会传给C，共有多少种传球方法？
MLE、MAP和贝叶斯估计
MLE，MAP，EM 和 point estimation 之间的关系是怎样的？
如何求解Ax=b (非迭代Cholesky分解、QR分解，迭代)
最小二乘封闭解与迭代解的取舍
梯度下降法、牛顿法、GN、LM，推导、优缺点
如何判断点在多边形内
一阶、二阶优化，Jacobian、hessian矩阵
1000个数的阶乘，求有多少个0
递推法求数学期望，反证法，数学归纳法等


三：SLAM

landmark参数化方式、对比，逆深度参数化；点线面因子图优化
滤波+回环（Trifo-VIO）
outlier+鲁棒核、RANSAC
EKF更新方程
AR系统如何实现
介绍下VO
Gridmap（网格标0、1）给定起点和终点，求最优路径（A*或其他路径规划算法）
相似变换、仿射变换、射影变换的区别
E和F的区别，自由度计算
单应矩阵H的求取
PNP算法、ICP算法（二维码、手眼标定）
闭环检测常用方法（orb、lsd、深度学习）
单目的初始化（拓展：双目，RGBD，VIO的初始化及传感器标定），其他：
https://github.com/frobelbest/GSLAM
简述一下Bundle Adjustment的过程
SVO、LSD中深度滤波器原理
说一说某个SLAM框架的工作原理（svo、orb、lsd）及其优缺点，如何改进？
RANSAC的框架
位姿不同表示间的相互转化、旋转矩阵特征值和特征向量物理意义
真实世界到相机照片的变换可看成射影变换
直接法与特征点法的优缺点对比
常见滤波方法的对比（KF、EKF、IEKF、UKF、PF）
双目测距范围Z=fb/d。问题： 640*480，fov＝90°，zmax＝10m，最小视差为2，求使zmax稳定的最小基线长度（6.25cm）
特征点法与直接法误差模型、Jacobian推导
光流的假设、仿射变换、4种方法，svo采取的方法，优势何在
MSCKF与ROVIO、MSCKF与预积分
边缘化方式原理
grid_map 
https://github.com/ANYbotics/grid_map
四：传统图像处理

图像平滑算子、边缘检测算子
图像去噪滤波算法（高斯、均值、双边、Guide filter）
三个度量patch相似度的方法（SSD、SAD、NCC）
二进制描述子
计算描述子距离函数
描述一下SIFT或者SURF特征检测、匹配
SIFT的4个不变性
特征点、描述子ORB、SIFT、SURF、BRIEF等等 。geometric invariance：平移，旋转，尺度……; photometric invariance：亮度，曝光……
Mat实现、Mat类指针引用复制函数
颜色直方图统计，手撕代码
形态学操作，手撕代码
积分图，手撕代码
连通区域算法，给二值图，求出最大联通区域（用深度优先和广度优先算法，手撕代码）
Mser、Swt检测
图像分割（Grabcut）
目标跟踪（相关滤波KCF）
五：机器学习以及深度学习

这部分会很随意，根据项目

IOU、NMS，手撕代码
Kmeans伪代码
SVM的优缺点
随机森林的训练过程
优化方法SGD、Batch GD、Adadelta、Momentum对超参数的敏感程度
CNN中feature map维度计算、图中每一个特征点在原图的感受野大小
Segmatch
目标分割、目标检测（one stage、two stage），YOLO三代的发展，小目标检测
模型压缩与加速 mobilenet v1、mobilenet v2、shufflenet
https://github.com/memoiry/Awesome-model-compression-and-acceleration

六：参考资料

大疆算法工程师笔试（计算机视觉部分）

https://wenku.baidu.com/view/9aacf48ea21614791611282a.html

网易3D视觉方向

https://www.nowcoder.com/test/10780247/summary

谢晓佳学长“SLAM求职经验帖”

http://paopaorobot.org/bbs/read.php?tid=87&fid=7

http://paopaorobot.org/bbs/read.php?tid=88&fid=7

VO、SLAM、VIO基础论文

VO
rpg.ifi.uzh.ch/visual_o

《VO_Part_I_Scaramuzza》、《VO_Part_II_Scaramuzza》

光流
《Lucas-Kanade 20 Years On: A Unifying Framework》

图优化SLAM
《A Tutorial on Graph-Based SLAM》

《g2o: A General Framework for Graph Optimization》

参数化
《Impact of Landmark Parametrization on Monocular EKF-SLAM with Points and Lines》

边缘化
《Null-Space-based Marginalization》

VIO
《Quaternion kinematics for the error-state Kalman filter》

《Information Sparsification in Visual-Inertial Odometry》

其他常见SLAM、VIO系统相关论文（结合自己研究方向）

综述性质论文

下面第一篇论文总结了如下几点，感觉总结的很好

数据关联
初始化
位姿估计
地图生成
地图维护
失效恢复
回环检测
《Keyframe-based monocular SLAM: design, survey, and future directions》

《Past, Present, and Future of Simultaneous Localization And Mapping: Towards the Robust-Perception Age》

《Visual Place Recognition: A Survey》

《Simultaneous Localization and Mapping: A Survey of Current Trends in Autonomous Driving》

《Visual SLAM and Structure from Motion in Dynamic Environments: A Survey》

《A Benchmark Comparison of Monocular Visual-Inertial Odometry Algorithms for Flying Robots》

《GSLAM: A General SLAM Framework and Benchmark》

https://github.com/zdzhaoyong/GSLAM

《Survey on Computer Vision for UAVs: Current Developments and Trends》

《Semantic mapping for mobile robotics tasks: A survey》

《A Review on Deep Learning Techniques Applied to Semantic Segmentation》

《Deep Learning for Generic Object Detection: A Survey》

轨迹评估算法

https://github.com/MichaelGrupp/evo

https://github.com/raulmur/evaluate_ate_scale

ROVIO

SVO

《A Tutorial on Quantitative Trajectory Evaluation for Visual(-Inertial) Odometry》

VO、SLAM、VIO参考书籍

《SLAM十四讲》、《因子图在SLAM中的应用》

《state estimation for robotics》

《An Invitation to 3D Vision》、《Multi View Geometry》

深度学习参考

《解析卷积神经网络——深度学习实践手册》 lamda.nju.edu.cn/weixs/

《神经网络与深度学习》 nndl.github.io/

Shirley Snow 刘同学总结

https://zhuanlan.zhihu.com/p/42807023

《AI算法工程师手册》
https://zhuanlan.zhihu.com/p/63638229


1、视觉SLAM方法一般分为特征点法和直接法。请简述一下特征点法和直接法的概念，以及对应的优缺点。

特征点法，根据提取、匹配 特征点来估计相机运动，优化的是重投影误差，对光照变化不敏感 ，是比较成熟的方案。常见的开源方案 比如ORBSLAM
优点：
（1）特征点本身对光照、运动、旋转比较不敏感，所以比较稳定
（2）相机运动较快（相对直接法来说）也能跟踪成功，鲁棒性好一些
（3）研究时间较久，方案比较成熟
缺点：
（1）关键点提取、描述子、匹配耗时长
（2）特征点丢失场景无法使用
（3）只能构建稀疏地图
直接法，根据相机的亮度信息估计相机的运动，可以不需要计算关键点和描述子，优化的是光度误差，根据使用像素数量可分为稀疏、半稠密、稠密三种。常见开源方案有SVO, LSD-SLAM
优点：
（1）速度快，可以省去计算特征点、描述子时间
（2）可以用在特征缺失的场合（比如白墙），特征点法在该情况下会急速变差
（3）可以构建半稠密乃至稠密地图
缺点：
（1）因为假设了灰度不变，所以易受光照变化影响
（2）要求相机运动较慢或采样频率较高（可以用图像金字塔改善）
（3）单个像素或像素块区分度不强，采用的是数量代替质量的策略
2、视觉SLAM常用的相机包括，单目，双目，RGB-D相机，请分别说说它们本身的优缺点、常用的相机型号等。

以下是我使用时的一些总结，可能有疏漏错误，欢迎补充指正。
单目相机：
常用型号：有非常多的种类可以选择
优点：
1、应用最广，成本可以做到非常低。
2、体积小，标定简单，硬件搭建也简单。
3、可以用于室内和室外（有适当光照条件下）。
缺点：
1、具有纯视觉传感器的通病：在光照变化较大，纹理特征缺失、快速运动导致模糊的情况下无法使用（睁眼瞎）。
2、SLAM过程使用单目相机有尺度不确定性，需要专门初始化。
3、必须通过运动才能估计深度（帧间匹配三角化）
双目相机：
常用型号：Indemind，小觅，ZED等
优点：
1、相比于单目，在静止时就能够根据左右相机视差图计算深度。
2、可测量距离可以根据基线调节。基线距离越大，测量距离越远。
3、可以用于室内和室外（有适当光照条件下）。
缺点：
1、双目相机标定相对复杂
2、用视差计算深度比较消耗资源
3、具有纯视觉传感器的通病：在光照变化较大，纹理特征缺失、快速运动导致模糊的情况下无法使用（睁眼瞎）。
RGB-D相机：
常用型号：Kinect系列、Realsense系列、Orbbec、Pico等
优点：
1、使用物理测距方法测量深度，所以避免了纯视觉传感器的通病，在没有光照的情况下、快速运动的情况下都可以测距。这是非常大的优势。
2、相对双目，输出帧率较高，更适合运动场景。
3、输出深度值比较准，结合RGB信息，容易实现手势识别、人体姿态估计等应用。
缺点：
1、测量范围窄，易受日光干扰，通常只能用于室内场景
2、在遇到透射材料、反光表面、黑色物体情况下表现不好，造成深度图缺失
3、通常分辨率无法做到很高，目前主流分辨率VGA（640x480）
4、标定比较复杂。
3、关键帧在SLAM里应用非常多，很多知名的开源算法都使用了关键帧。请你用自己的语言描述一下关键帧是什么？有什么用？如何选择关键帧？

关键帧目前是一种非常常用的方法，可以减少待优化的帧数，并且可以代表其附近的帧。可以理解为一个学校里有100个班级，每个班的班长就是一个关键帧，他可以代表他班里的人，那么如何选取关键帧呢？
选取的指标主要有：
（1）距离上一关键帧的帧数是否足够多（时间）。比如我每隔固定帧数选择一个关键帧，这样编程简单但效果不好。比如运动很慢的时候，就会选择大量相似的关键帧，冗余，运动快的时候又丢失了很多重要的帧。
（2）距离最近关键帧的距离是否足够远（空间）/运动
比如相邻帧我根据pose计算运动的相对大小，可以是位移也可以是旋转或者两个都考虑，运动足够大（超过一定阈值）就新建一个关键帧，这种方法比第一种好。但问题是如果对着同一个物体来回扫就会出现大量相似关键帧。
（3）跟踪质量（主要根据跟踪过程中搜索到的点数和搜索的点数比例）/共视特征点
这种方法就是记录当前视角下的特征点数，或者视角，当相机离开当前场景时才会新建关键帧，避免了第2种方法的问题。缺点是比较复杂
打个比方，关键帧相当于slam的骨架，是在局部一系列普通帧中选出一帧作为局部帧的代表，记录局部信息。举例来说，摄像头放在原处不动，普通帧还是要记录的，但关键帧因为总看到原场景，所以不会增加。
三角化需要一定程度的共视区域，所以普通帧每2帧之间会存在大量的信息冗余，如果所有帧全部参与计算，不仅浪费了算力，对内存也是极大的考验，这一点在前端vo递归处理方式中表现不明显，但在后端优化里是一个大问题，所以关键帧主要作用是面向后端优化的算力与精度的折中。此外，关键帧选择时还会对图片质量、特征点质量等进行考察，一定程度上也发挥了滤波的作用，防止无用的或错误的信息进入优化过程而破坏定位建图的准确性。
选择关键帧主要从关键帧自身和关键帧与其他关键帧的关系2方面来考虑。一方面，关键帧自身质量要好，例如不能是非常模糊的图像、特征点数量要充足、特征点分布要尽量均匀等等；另一方面，关键帧与其他关键帧之间的关系，需要和局部地图中的其他关键帧有少量的共视关系，但大部分特征点是新特征点，以达到既存在约束，又尽量少的信息冗余的效果，例如局部地图点投影到此帧的点数低于一个阈值或前一个关键帧的特征点在此帧里已经有90%观测不到等等。
在关键帧的运用上，我认为orbslam做的非常好，尤其是在回环检测中使用了以关键帧为代表的帧“簇”的概念，回环筛选中有一步将关键帧前后10帧为一组，计算组内总分，以最高分的组的0.75为阈值，滤除一些组，再在剩下的组内各自找最高分的一帧作为备选帧，这个方法非常好地诠释了“关键帧代表局部”的这个理念。
4、按照你的理解讲解一下什么是极线约束？这个约束能带来什么好处？

极线约束也叫对极约束。这个约束的意思就是说，假设相机在不同位置拍摄了两幅图像，如果一个空间点P在两幅图上分别有两个成像点，已知左图成像点为p1，那么右图成像点p2一定在相对于p1的极线上。

（以上过程面试的时候最好画图解释一下，见附图，面试官会感觉你很专业）
极线约束的好处：从上面的描述我们可以看到，我们在做特征点匹配时，左图成像点p1的待匹配点p2一定在相对于p1的极线上，那么我们在做搜索时就可以在极线附近（考虑实际可能 会有一点误差）进行搜索，相对暴力匹配极大减少待匹配的点的数量。
极线约束可以简洁的给出匹配点的空间位置关系，使得相机位姿估计问题变的简单。
限于篇幅，只列举以上几个问题及解答，以下所有问题《从零开始学习SLAM》知识星球里都有参考解答，并且会持续发布。欢迎交流讨论

5、SLAM后端一般有两种方法：滤波方法和非线性优化方法，这两种方法有什么优缺点？

6、单目视觉slam中尺寸漂移是怎么产生的？有什么解决办法

7、直接法估计相机位姿时，并不需要 提取特征点，而是通过优化匹配点的像素值误差（也称光度误差）估计位姿，但也会面临快速运动，光照变化等的挑战，如果让你改善该问题，你会采用哪些方法来提高跟踪质量(精度，速度，鲁棒性等)？

8、什么是PnP算法？请用你的语言描述一下原理，它一般用在什么场景，解决什么问题？


此外，我们平时在SLAM的学习工作中也会遇到一些问题，我总结了一些常见的问题，也一并列在这里，并给出了答案（见知识星球）

9、 我们知道相机的内参有 fx, fy, cx, cy, 畸变参数(只考虑k1, k2)，相对世界坐标原点外参T。如果我们现在对相机拍摄的图片进行2倍的下采样，那么这些参数会如何变化？

10、我们知道双目相机两个相机光心的间距我们 称之为 baseline。如果双目相机baseline比较大，我们称之为wide baseline.现在某代码中使用一个单目相机进行SLAM过程，在特征匹配时资料中提到了wide baseline，请问这个wide baseline怎么理解？

11、RGB-D相机我们知道可以直接输出 RGB + depth两张图比如我们常见的Kinect 是结构光原理，包括一个彩色相机，一个红外发射器，一个红外接收器。另外，Intel的Realsense系列RGB-D相机也非常常用，比如下面Realsense D415，官网说是Active IR stereo，也就是双目深度相机，这个双目和我们平时说的双目有何不同？为什么有如下四个孔？

12、我们在阅读文献或者代码中误差相关时，经常可以看到一个概念，叫逆深度（inverse depth）。也就是深度的倒数，那么同学们有没有想过，为什么使用逆深度误差而不是深度误差？

13、我们在看SLAM相关论文的时候，会遇到一个词“kidnap”， 直译过来就是“绑架”，不了解的同学可能感觉怪怪的。你知道这个“绑架”是什么意思吗？可以用哪些方法解决这样的问题？

14、我们知道（不知道的话，去查一下十四讲）用g2o和ceres库都能用来进行BA优化，这两者在使用过程中有什么不同？

15、SLAM中回环检测（闭环检测）的目的是什么？简述一下SLAM中可以使用的回环检测方法？

16、SLAM中为什么要引入李群李代数？

17、为什么SLAM中常用LM算法而不是高斯牛顿求解优化问题？

18、讨论一下SLAM应用场景及落地的问题。大家觉得SLAM技术最适合的应用场景是什么？在哪个场景能够最快技术落地呢？

19、大家都是SLAM方向的研究者，不管是学生还是已经工作，以后都面临找（换）工作的问题，那么你知道哪些做SLAM技术的公司？

20、什么是ICP 算法？简述一下算法原理，SLAM中一般什么情况下会使用该算法？



如何对匹配好的点做进一步的处理，更好保证匹配效果
（1）确定匹配最大距离，汉明距离小于最小距离的两倍

（2）使用KNN-matching算法，令K=2。则每个match得到两个最接近的descriptor，然后计算最接近距离和次接近距离之间的比值，当比值大于既定值时，才作为最终match。

（3）RANSAC（使用RANSAC找到最佳单应性矩阵。由于这个函数使用的特征点同时包含正确和错误匹配点，因此计算的单应性矩阵依赖于二次投影的准确性）


1. 单目相机，F和H矩阵有何不同，E和F矩阵有何不同，只旋转不平移能不能求F，只旋转不平移能不能求H

E=t^R

[公式]

H=R-t*nT/d

在相机只有旋转而没有平移的情况，此时t为0，E也将为0，导致无法求解R，这时可以使用单应矩阵H求旋转，但仅有旋转，无法三角化求深度。


3. 描述BA

BA的本质是一个优化模型，其目的是最小化重投影/光度误差，用于优化相机位姿和世界点。局部BA用于优化局部的相机位姿，提高跟踪的精确度；全局BA用于全局过程中的相机位姿，使相机经过长时间、长距离的移动之后，相机位姿还比较准确。BA是一个图优化模型，一般选择LM(Levenberg-Marquardt)算法并在此基础上利用BA模型的稀疏性进行计算；可以直接计算，也可以使用g2o或者Ceres等优化库进行计算。

Bundle Adjustment : 从视觉重建中提炼出最优的3D模型和相机参数（内参和外参），好似每一个特征点都会反射几束光线，当把相机位姿和特征点位置做出最优的调整后，这些光线都收束到相机相机光心。也就是根据相机的投影模型构造构造代价函数，利用非线性优化（比如高斯牛顿或列文伯格马夸而尔特）来求最优解，利用雅克比矩阵的稀疏性解增量方程，得到相机位姿和特征点3D位置的最优解。

BA可以分为基于滤波器的BA和基于迭代的BA


4. 描述PnP

Perspective-n-Points, PnP(P3P)提供了一种解决方案，它是一种由3D-2D的位姿求解方式，即需要已知匹配的3D点和图像2D点。目前遇到的场景主要有两个，其一是求解相机相对于某2维图像/3维物体的位姿；其二就是SLAM算法中估计相机位姿时通常需要PnP给出相机初始位姿。

在场景1中，我们通常输入的是物体在世界坐标系下的3D点以及这些3D点在图像上投影的2D点，因此求得的是相机坐标系相对于世界坐标系(Twc)的位姿

在场景2中，通常输入的是上一帧中的3D点（在上一帧的相机坐标系下表示的点）和这些3D点在当前帧中的投影得到的2D点，所以它求得的是当前帧相对于上一帧的位姿变换，如图所示：

两种情况本质上是相同的，都是基于已知3D点和对应的图像2D点求解相机运动的过程。


5. 描述下GN、LM方法

（1） GN：线搜索

将f（x）进行一节泰勒展开，最后求解

线性方程H△x=b；

用JT*J近似H矩阵，省略H复杂的计算

过程；

稳定性差，可能不收敛；

（2） LM：信赖区域；

求解线性方程(H+λI)△x=b；

提供更稳定，更准确的增量


6. 如何处理关键帧

关键帧选取的指标主要有：

（1）跟踪质量（主要根据跟踪过程中搜索到的点数和搜索的点数比例）/共视特征点

（2）距离最近关键帧的距离是否足够远（空间）/运动

（3）距离上一关键帧的帧数是否足够多（时间）


7. 为什么要引入李群李代数

旋转矩阵自身是带有约束的，正交且行列式为1，他们作为优化变量时，会引入额外的约束，时优化变的困难，通过李群李代数的转换关系，把位姿估计变成无约束的优化问题。


8. 什么是极限约束

所谓极线约束就是说同一个点在两幅图像上的映射，已知左图映射点p1，那么右图映射点p2一定在相对于p1的极线上，这样可以减少待匹配的点数量。（画图解释）


9. 单目视觉slam中尺寸漂移是怎么产生的

单目相机根据一张图片无法得出一张图片中物体的实际大小，同理也就无法得出运动的尺度大小，这是产生尺度漂移的根源。而在优化过程中，单目相机使用对极几何中的三角测量原理，而三角测量中，极小的角度误差在累积之后深度不确定都会变得很大，从而无法保证尺度一致性。


10. SLAM中的绑架问题

绑架问题就是重定位，是指机器人在缺少之前位置信息的情况下，如何去确定当前位姿。例如当机器人被安置在一个已经构建好地图的环境中，但是并不知道它在地图中的相对位置，或者在移动过程中，由于传感器的暂时性功能故障或相机的快速移动，都导致机器人先前的位置信息的丢失，在这种情况下如何重新确定自己的位置。


Behaviour Trees, Finite State Machines, Petri-Nets



Dear Recruiter, I will complete all my study at Imperial College this September but the official graduation is May 2020. I am eligible to work in Canada and currently looking for opportunities commencing this September. Thank you.

adaptive learning methods: deep learning (neural networks), reinforcement learning, semisupervised learning, time-series prediction and anomaly detection


* 相似变换、仿射变换、射影变换的区别
* Homography和Fundamental Matrix的区别，包括二者区别，几个自由度，为什么是这么多自由度，怎么计算，这些在多视图几何那本书中都有
* 视差与深度的关系。在相机完成校正后，则有d/b=f/z,其中d表示视差，b表示基线，f是焦距，z是深度
* PNP算法
* 闭环检测常用方法
* 给一个二值图，求出最大联通区域（可以用深度优先和广度优先算法，现场手写代码）
* 说一说梯度下降法、牛顿法、高斯-牛顿法区别
* 边缘检测算子
* BA算法
* SVO中的深度滤波器原理
* 说一说某个SLAM的工作原理（orb,lsd,svo,ptam）及其优缺点，如何改进
上面说的都是SLAM这个方向要掌握的一些基础知识，其实还有一点非常非常重要，SLAM是一个大方向，它不可能单独落地，一定要和其他技术结合。我觉得目前来讲可以分为三个方向：三维重建，增强现实，移动机器人，一定要先想好自己想搞哪个方向，了解这个方向大概是什么样的
三维重建：选择这个方向，需要对SFM比较熟悉，SFM不追求速度，更追求精度，一般可以考虑大疆、百度
增强现实：这个方向需要懂IMU和视觉的融合，比如MSCKF,VINS这些系统，还要了解底层的opengl编程，对工程能力要求高，这个方向需求量很大，各个大厂的AI LAB都招增强现实方面的人才
移动机器人：这个我自己了解的不多，大概需要懂导航、路径规划这些，主要是大疆、百度及一些初创公司在做
最主要的就是基础要扎实，论文是附加项，没有也没什么，有了也不要忘了基础，希望大家都能找到满意的工作！

１.连通区域算法（可以将 图像简化为二值图来考虑
http://blog.csdn.net/icvpr/article/details/10259577）
2. 实现RANSAC的框架（MRPT写得是比较好的，注意每次此迭代后需要更新迭代次数。见libs/base/src/math/ransac.cpp）
3. Homography和Fundamental matrix的性质与区别
4. 简单实现cv::Mat()
5. 简述一下GN、LM等优化方法的区别
6. 推导一下卡尔曼滤波，描述一下粒子滤(http://blog.csdn.net/heyijia0327）
7. 描述一下SIFT或者SURF特征检测，匹配
8. 如何求解Ax=b (非迭代、迭代，其中非迭代的方法可以参考eigen手册，上面 列了一些(http://eigen.tuxfamily.org/dox/group__TutorialLinearAlgebra.html)
9. 简述一下Bundle Adjustment的过程
10. 对熟悉的某一个开源SLAM，简述其流程

1.ORBSLAM的初始化方式
2.ORB特征点与SIFT、SURF的区别
3.简述EPnP算法的大致步骤
4.vins中是如何将IMU数据与camera融合到一起的？简述一下vins的大致框架
5.vins初始化是如何完成的？
6.简述一下ORBSLAM和vins的区别，如果你是开发者，你觉得这两个算法还有哪些可以改进的地方（选择其中一个也可）
7.刚才提到你使用了一种名叫kalibr的相机内参标定工具，你提到这个工具也能进行camera-imu联合标定，能简述一下其思想吗？（此题没答上来，因为只会用没有深究其内部原理）
8.简述堆和栈的区别（接下来是编程题，不过问的很少）
9.虚函数和纯虚函数的区别
10.你用过容器吗（具体指vector），你觉得他有哪些特点？

1.ORB特征点的特性（回答围绕旋转、尺度不变性，还有消耗时间三个方面）
2.牛顿法、GN、LM的区别
3.你知道哪些非线性优化库？（回答g2o）追问ORBSLAM中如何使用g2o进行优化？
4.你了解c++各种设计模式吗？
5.const在不同位置的含义

1.特征点法与直接法的区别（以ORBSLAM和vins为例）
2.你了解深度学习吗？你觉得深度学习和SLAM有哪些结合点？
3.介绍一下各种传感器的特点（单目、双目、RGBD、激光）追问单目SLAM的缺陷以及如何解决
4.你了解激光SLAM吗？能不能简述一下ICP算法的原理
5.如何解决SLAM环境中动态对象的问题（具体事例为，餐厅来来往往的行人，这个时候送餐机器人估计的位姿受行人影响，会变得不够准确）

1.你了解激光和视觉传感器的联合标定吗？有没有使用过相关的工具？
2.你在简历中提到过一种轨迹误差评测工具（rpg_trajectory_evaluation）,能具体介绍一下原理吗？
3.你了解ROS吗？能不能介绍一下你做过的项目
4.请你讲一下对极几何的知识以及基础矩阵的求解

1.详细讲述一下vins中预计分的推导过程（这个问题有点要命，幸好之前自己亲手推导过）
2.你了解卡尔曼滤波吗？
3.SLAM中为什么用李群李代数？
4.你了解图优化吗？能简单介绍一下吗？

深度和视差的关系

1.你了解ORBSLAM吗？能否具体介绍一下，你作为一名工程师，打算从那几个方面去优化它呢？或者有哪些可以创新的地方？
2.你刚才提到vins的最新版本是vins_fusion，能具体介绍一下这个方案吗？
3.static关键字的作用
4.你用过智能指针吗？分别都有什么特点呢？





https://www.zhihu.com/question/532565032/answer/2483264411

作者：半闲居士
链接：https://www.zhihu.com/question/532565032/answer/2483264411
来源：知乎
著作权归作者所有。商业转载请联系作者获得授权，非商业转载请注明出处。

写一个求两点的距离函数。要求支持常见的2维、3维至任意有限高维点。

pose的时间插值是常见需求。写一个6自由度pose的插值函数。pose和时间戳是自定义的结构体，例如 std::vector<TimedPose> 之类。TimedPose.time_stamp为时间，TimedPose.pose是位姿。

让2的函数支持其他的常见有序容器，如std::list<TimedPose>和std::map<double, TimedPose>。

让2的函数支持自定义取时间戳的方式和取pose的方式，因为其他的结构体中时间戳变量和pose变量名称可能不同，例如TimedPose里的时间戳字段是time_stamp，而TimedPose2里的则是time_。

不用库写一个并行的for循环。输入两个迭代器和一个lambda，例如for_each(begin, end, [](int i){cout<<i;});

用你熟悉的优化库写一个自定的edge/factor/residual function。

写一个读取程序，从rosbag中读取给定消息并执行某个回调函数。回调函数由用户定义。

在7的基础上，把读到的消息进行转换，写入另一个bag包。

在8的基础上，把某种常见的操作在一个通用函数内实现。例如，某个msg含有ros标准header的，将它的header.timestamp转成输出消息的timestamp字段。

写一个三维点的operator < 函数。

如何对空间栅格进行hash？写一个存储空间栅格的hash容器。

把一个同步的ros消息处理函数改成异步的。

在10的基础上，支持任意的消息类型和异步回调函数。

用最小二乘写一个由3D点拟合平面参数的函数。

写一个计算某个数组均值和方差的函数。

在14的基础上，支持高维的矢量数组。

在15的基础上，还能支持对任意结构体的某个字段计算均值和方差。



Transformer面试题
1. Transformer为何使用多头注愈力机击U?（为什么不使用一个头） 
2. Transfonner为什么Q和K使用不同的权重矩阵生成，为何不能使用同一个值 进行自身的点乘？ 
3. Transformer计算attention的时候为何选择点乘而不是加法？两者计算复杂 度和效果上有什么区别？ 
4. 为什么在进行sof teas之前需要对attention进行scaled（为什么除以处的 平方根），并使用公式推导进行讲解 
5. 在计算attention 500re的时候如何对padding做mask操作？ 
6. 为什么在进行多头注惫力的时候需要对每个head进行降维？ 
7. 大概讲一下Transformer的Encoder模块？ 
8. 为何在获取输入词向量之后需要对矩阵乘以embedding size的开方？ 
9. 简单介绍一下Transformer的位置编码？有什么惫义和优缺点？ 
10. 你还了解哪些关于位置编码的技术，各自的优缺点是什么？ 
11. 简单讲一下Transformer中的残差结构以及惫义。 
12. 为什么transformer块使用细幽srm而不是助“迎即衅！公e塑塑飞在 Transformer的位置是哪里？ 
13. 简答讲一下BatchNorr技术，以及它的优缺点。 
14. 简单描述一下Trarsf orrer中的前馈神经网络？使用了什么激活函数？相关 优缺点？ 
15. Ercoder端和Deco der端是如何进行交互的？ 
16. Decoder阶段的多头自注意力和ercoder的多头自注意力有什么区别？ 
17. Trarsf orrer的并行化提现在哪个地方？ 
18. Decoder端可以做井行化吗？ 
19. 简单描述一下熙互幽然Ce rodel和byt epalrerco dlrg，有实际应用过吗？ 
20. 简单描述一下熙互幽然Ce rodel和byt epalrerco dlrg，有实际应用过吗？ 
21. Trarsf orrer训练的时候学习率是如何设定的？Dropout是如何设定的，位置 在哪里？Dropout在测试的需要有什么需要注意的吗？ 21h熙文的。ask为何不学习transforoer在attentlon处进行屏蔽score配 巧？ 



Transformer为伺使用多头注意力机制？（为什么不使用一个头） 
答：多头可以使参数矩阵形成多个子空间，矩阵整体的slze不变，只是改变了 每个head对应的维度大小，这样做使矩阵对多方面信息进行学习，但是计算量 和单个head差不多。 2. Transformer为什么Q和K使用不同的权重矩阵生成，为何不能使用同一个值 进行自身的点乘？ 答：请求和键值初始为不同的权重是为了解决可能输入句长与输出句长不一致的 问题。并且假如1K维度一致，如果不用K，直接拿K和K点乘的话，你会发现 att er or score矩阵是一个对称矩阵。因为是同样一个矩阵，都投影到了同样 一个空间，所以泛化能力很差 3. Transfo～计算at七est non的时候为f卿）择点乘而不是加法？两者计算复杂 度和效果上有什么区别？ 答：K和K的点乘是为了得到一个attentlon score矩阵，用来对V进行提纯。 K和Q使用了不同的tk,t K来计算，可以理解为是在不同空间上的投影。正 因为有了这种不同空间的投影，增加了表达能力，这样计算得到的attentlon score矩阵的泛化能力更高。 4为什么在进行softmaa之前需要对attention进行scaled（为什么除以熊的 平方振），井使用公式推导讲行翻涌l 
答：假设Q和K的均值为O，方差为1。它们的矩阵乘积将有均值为O,,J~ 
为dk，因此使用业的平方报被用于缩放，因为，Q和K的矩阵乘积的为值本 应该为O方差本应该为1，这样可以获得更平缓的nof tans。当维度很大时，
 
17. Transformer的并行化提现在哪个地方？ 答：Transforoer的并行化主要体现在：cif att erl or模块，在En co der端 Trarsf orirer可以并行处理整个序列，并得到整个输入序列经过irc der端的输 出，但是工县焦只能从前到后的执行 18. Deroder端可以做并行化吗？ 训练的时候可以，但是交互的时候不可以 19简单描述一下wor热iece model和byte pair enroding，有实际应用过吗？ 答“传统词表示方法无法很好的处理未知或罕见的词汇（toy问题） 传统词tokeniz热on)法不利于模型学习词缀之间的关系” BPE〔字节对编码）或二元编码是一种简单的数据压缩形式，其中最常见的一对 连续字节数据被替换为该数据中不存在的字节后期使用时需要一个替换表来重 建原始数据 优点：可以有效地平衡词汇表大小和步数（编码句子所需的token次数）。 缺点：基于贪婪和确定的符号替换，不能提供带概率的多个分片结果 20. Transformer训练的时候学习菊堤如何设定的？Dropout是如何设定的，位 置在哪里？Dropout在测试的需要有什么需要注意的吗？ L\是为了解决梯度消失的问题，dropout是为了解决过拟合的问题在erbe 1二 后面加LN有利于erbeddlrg rat rl0的收敛。 21. bert的mash为何不学习transformer在attention处讲行屏蔽score的技 
