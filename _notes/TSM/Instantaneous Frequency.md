$$\omega = lim_{t_{2}\rightarrow t_{1}} \frac{\varphi_{2}-\varphi_1}{t_{2}-t_{1}}$$



measuring frequency, 
对于FFT后的一个信号，say, 第三个bin， k=3，对应的频率为 $\omega[k]=\omega_{3}$

第一帧对应的phase相位 $\varphi_{1}[k]$为 $7\omega_{3}$ , 200的samples (hopzize)后的第二帧对应的相位 $\varphi_{2}[k]$应该是 $207\omega_{3}$  
measuring frequency should be 
$$\hat{\omega}_{2}[k] = \frac{\varphi_{2}[k]-\varphi_{1}[k]}{HA}=\frac{ 207\omega_{3} - 7\omega_{3}}{200} =  \omega_{3}   $$
这个时候 测量的频率 $\hat{\omega}_2[k]$ 与理论的表达式频率$\omega[k]=\omega_{3}$ 相同

但是实际上，非稳态信号并不能满足这个条件，存在额外的误差 $\Delta\omega_{2}[k]$
$$\hat{\omega}_{2}[k] = \omega_{3}+ \Delta\omega_{2}[k] $$
所以要进行误差校正
$$\varphi_{m+1}[k] = \{ \varphi_{m}[k] + HA(\hat{\omega}_{m+1}) \}_{ppa} = 
\{ \varphi_{m}[k] + HA(\omega_{k}+ \Delta \omega_{m+1}[k] ) \}_{ppa}$$
the Instantaneous freuqency should be

