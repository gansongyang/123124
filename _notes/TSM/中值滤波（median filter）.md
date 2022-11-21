the median is defined as the mean of the two middle values(even), or the middle value (odd)
对于一组数据$A = (a_{1},a_{2},...,a_{L})$ , 按从小到大的顺便排列后得到 $A= (\tilde{a}_{1},\tilde{a}_{2},\tilde{a}_{3},...,\tilde{a}_{L})$ ，对应的中值定义为：
$$\mu_{\frac{1}{2}}(A)= 
\begin{cases}
\tilde{a}_{\frac{L+1}{2}}, & \quad \text{L is odd}  \\[10pt]
(\tilde{a}_{\frac{L}{2}} + \tilde{a}_{\frac{L+1}{2}})/2, &\quad \text{L is even}
\end{cases}$$

**Median Filter**：
$$\mu_{1/2}^{L}(A)[n]= \mu_{1/2}(a_{n-(L-1)/2},...,a_{n+(L-1)/2})$$
A = (..., 0, 5, 3, 2, 8, 2, 0,...) , 对于L=3, $\mu_{1/2}^{L}(A)= (..., 0,3,3,3,2,2,0,...)$ , ***注意** median filter需要先排序***


#### Two matlab function
- **movmedian.m** 没有pad zero，所以第一位和最后一位的结果，是原数据组的前二/后二数据的平均值
- **medfilt1.m** 执行了zero pad 操作，再调用movmedian.m



for $L_{freq}$ and $L_{time}$  , it

从构建声音场景的底层逻辑来说，传统的多声道和双耳系统，主要是依赖心理声学得以实现。
但是WFS和HOA基于声全息的理念，精准还原现实的物理声音场景。

通过WFS技术，
1. 在视听室内的任何一个位置都是听音的黄金位
2. 和双耳系统不同的是，虚拟声源不会随着听者的移动而移动，
3. 在视听室内的任何一个位置都可以准确感知虚拟声源的定位
4. 虚拟声源的位置和单一扬声器的位置不再捆绑在一起，虚拟声源可以布置在视听室内的任何一点，
5. 听者将不再会注意到单一扬声器，从而使得试听体验更加的自然通透

应用场景
1. 回放：在不同场景（汽车、酒吧、小聚会厅）回放大剧场录制的全景声
2. 现场：把声相定位在舞台中，实现观众的注意力集中在舞台，声画同步
3. 如果不局限WFS，在虚拟现实中回放，可以实现观众自由在演绎者身边穿梭，获得更沉浸的听音体验







