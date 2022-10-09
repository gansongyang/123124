---
date created: 2022-10-09
date modified: 2022-10-09
title: Headphone Externalization
---

[[Lateralizaiton]] 和 [[Externalization]]

- 双声道的externalization相较于多声道，要复杂的多
- 双声道的externalization的很多实现算法会给音色带来较大损伤
- 在双声道中，人造混响中的干声很难被分离出来

1. 在左右声道中间构建一个虚拟SPK，可有拓宽声场，并使得前方的声源变宽
	- In the twospeak er setup, mono-aural sound produces afeed-forw ard comb-filter effect, as the signal propagates to an ear from twopaths, once from the closer speaker and second time from the cross-talk route.
2. [[Channel sepeartion]]
1. Modelling
	- Sound naturally attenuates with the distance in 1/r sense, ifaspherical radiator model is used.
	- air absorption isimportant when modeling large spaces with large distances between the sound sources and the listener.
2. Listener modelling
	- 除非使用个性化HRTF，否则自然的虚拟声源定位在耳机中很难实现。uncontrived localization of virtual sources with headphones is not possible unless individual HRTFs are used.

![[Screen Shot 2022-10-09 at 18.47.40.png]]

![[Screen1.png]]
