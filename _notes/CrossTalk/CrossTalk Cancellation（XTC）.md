#### 实现多扬声器还原成双耳的效果，主要是为了拓展声场和更加自然的听音感, 但是目前比较适用于两个扬声器的应用场景
transaural reproduction通过一部分扬声器实现不用耳机设备依然可以体验binarual rendering, <font colorfont  color="red"  size="3"  > 涉及HRTF处理就要注意音色的问题，未必能获得更自然的听感，但是可以考虑利用HRTF抬高水平高度 </font>
1. 传统的算法需要固定的场景，保持听者和设备的位置固定。
2. 新的动态算法，可以实现动态交互，但是需要头部追踪设备和实时反向滤波器的支持
#### 实现XTC动态稳定性有两种方法
- optimal loudspeaker configuration, 把SPKs放在听者面前可以提升针对头转动场景的算法稳定性，此外，把SPKs放在高于听者脑袋水平面的位置，可以有效降低头转动带来的负面影响
- dynamic transaural system,  采用如微软Kinect等外部设备追踪头部运动，但是延迟是一个关键点
#### 对于频率的敏感度
针对低频300Hz，头部的转动对XTC算法的影响较小, 但是在高频，耳朵与扬声器同侧的情况下，很难做到干净的reproduction. 如下图在脑袋右转30度时，耳朵与SPK同侧，在高频部分多了unwanted signal [[@Hiroaki Kurabayashi,  2014]]
![[Screen Shot 2022-11-18 at 14.46.44.png|600]]

![[Screen Shot 2022-11-18 at 14.31.47.png|600]]
#### 实验设定：
rotation精度5度, SPK 1m的距离
<font  color="red"  size="3" >左耳impulse, 右耳无信号的stimuli, 为了去掉相关性的干扰</font> 
#### 动态系统的关键：延迟问题
实验中对比了穿戴式头部追踪和外部追踪设备的延迟问题，穿戴式头部追踪Colibri大约有10ms的延迟，而微软的Kinect延迟大约在100ms,  [[@Satoshi Yairi, Yukio Iwaya, 2007]] 通过实验判断人对virtual auditory display (VAD)设备使用过程中，对延迟的threshold大约在60ms.  [[@Hiroaki Kurabayashi,  2014]] 论文使用Kinect实现的动态算法验证表明，即使延迟在100ms, 动态XTC算法依然可以实现binarual空间效果, <font  color="red"  size="3" > 但是延迟问题依然是影响目前动态XTC算法的关键。</font> 

微软的外部追踪仪，400刀左右
![[MS kinect2.png| 400]]
![[MS kinect.png| 400]]

