# ROBIO 2019 会议总结

## 1.会议简介

这是充满血泪史的一次会议经历，发着烧坐了一天飞机，吐了一天，还熬夜做ppt，真的是全靠意志活着。

ROBIO会议已经是第2次参加（上次是硕士期间，在澳门举办），这次会议在云南大理举行，时间是12.6-12.9。首先不得不吐槽一下去大理有多么麻烦，北京飞大理只有早晨6:30的2趟，根本赶不过去，火车时间又太久，我还是请假参加会议的。花了一晚上研究去的路线，最后决定到昆明转机。然后会议方提供的酒店太贵了，700多一晚已经超了清华的出差标准684元，所以我只能在附近找了个民宿，看了看评价还可以，离酒店400米。

IEEE系列的会议注册提前先申请一个IEEE student membership会比较划算（27美元），论文超了2页，最后算下来注册费交了4900人民币。

ROBIO号称是机器人三大会议之三，不过水文很多，挑一些质量好的看看就行。绝大部分都是中国人，这英语是真的不行，根本听不懂在讲啥，全靠看ppt自己领悟。

## 2.文章
ROBIO会议是multi-track，所以只能找一些相关方向的听一听。

### SLAM 1
我在这个session 第一个讲，讲完了我就留在这个session听了一下SLAM的工作。没啥好工作，逻辑上自洽都费劲。
1. 哈尔滨工业大学 工作是：3D lidar and 双目摄像的外参标定 用了一个feature-point 约束。
2. 中科院+香港大学 工作：low-light SLAM  做了一个相机$\gamma$矫正，camera 20HZ+IMU 200HZ 对比了几个实验，有实际的实验，相机用的小蜜 还有一个lidar用来做真值--这就不咋个合理，很不严谨。
3. 广东工业大学 工作：深度估计 半监督
   1. dense depth
   2. semi-supervised encoder-decoder结构
   3. depth loss + nearbyloss + smooth loss
   4. 用稀疏depth+single image 构建dense depth
   在现场直接有人就问了你这工作意义是啥，有很多工作一张图就可以恢复深度，作者自己也答不出来。不知道作者没调研到还是故意不对比。
   不过作者的英语很好，唯一一个听懂的。
4. 中科院深圳先进技术研究院 工作：multi-task CNN to 估计 6D pose 不通过 pnp，然而看起来就是MASK RCNN用了一遍，没什么创新。

### navigation 1
第一天的下午在这个session听了一下。

1. 江苏南京Science and Technology（不知道是中文的哪所大学） 做单目VO的，方法是先做edge enhancement，然后接一个有LSTM的CNN，比deep vo好。
2. curiosity driven deep reinforcement learning for motion planning in multi-agent environment
   1. 上海交通大学 自动化学院
   2. 老师是Ning Li
   3. 在仿真环境下完成的，算法用的是PPO，加了一个curiosity ratio c，就是他的改进，用多机环境的原因看起来是想说复杂任务，不过作者定义的这任务没感觉有多复杂。只有2个机器人，要去对面的一个target，中间还要经过一个中间点。
   4. 看起来RL部分做得不专业，我问了一下是取得最好的结果，而不是平均结果，因为我看作者画的图竟然只有一条线，没有阴影。
   
### mobile robot 2
1. object-aware hybrid map for indoor robot visual semantic navigation
哈工大的工作，我觉得全场最佳了吧，还有点用。
<div align=center>
<img  src="https://github.com/zoeyuchao/Conference_Minutes/blob/master/figure/ROBIO2019/6.jpg"  width="400" />
<img  src="https://github.com/zoeyuchao/Conference_Minutes/blob/master/figure/ROBIO2019/7.jpg"  width="400" />
</div>


### mobile robot 3
1. 3D LIDAR map compression using DNN

<div align=center>
<img  src="https://github.com/zoeyuchao/Conference_Minutes/blob/master/figure/ROBIO2019/1.jpg"  width="400" />
<img  src="https://github.com/zoeyuchao/Conference_Minutes/blob/master/figure/ROBIO2019/2.jpg"  width="400" />
<img  src="https://github.com/zoeyuchao/Conference_Minutes/blob/master/figure/ROBIO2019/3.jpg"  width="400" />
<img  src="https://github.com/zoeyuchao/Conference_Minutes/blob/master/figure/ROBIO2019/4.jpg"  width="400" />
<img  src="https://github.com/zoeyuchao/Conference_Minutes/blob/master/figure/ROBIO2019/5.jpg"  width="400" />
</div>

### FuChun Sun老师的speech
<div align=center>
<img  src="https://github.com/zoeyuchao/Conference_Minutes/blob/master/figure/ROBIO2019/8.jpg"  width="400" />
<img  src="https://github.com/zoeyuchao/Conference_Minutes/blob/master/figure/ROBIO2019/9.jpg"  width="400" />
<img  src="https://github.com/zoeyuchao/Conference_Minutes/blob/master/figure/ROBIO2019/10.jpg"  width="400" />
<img  src="https://github.com/zoeyuchao/Conference_Minutes/blob/master/figure/ROBIO2019/11.jpg"  width="400" />
</div>

不听了，没啥好工作，写作业去了。
