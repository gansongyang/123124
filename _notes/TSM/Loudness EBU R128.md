### K- weighting filtering 
prefilter 1: high shelf filtering 
![[k_pre1.svg]] 

prefilter 2: high pass filtering 
![[k_pre2.svg]]

| ** Pre filter stage 1, normolized by $a_{0}$** | ***high shelf filter***     |
| --------------------------------------------- | --------------------------- |
| $b_{0} = 1.53518288636375$                    | $a_{0} = 1.0$               |
| $b_{1} = –2.69180403019920$                   | $a_{1} = –1.69069958659869$ |
| $b_{02} = 1.19842626333314$                   | $a_{2} = 0.73250470609639$  |
| **Pre filter stage 2, normolized by $a_{0}$** | ***high pass filter***      |
| $b_{0} = 0.99504429701789$                    | $a_{0} = 1.0$               |
| $b_{1} = –1.99008859403578$                   | $a_{1} = –1.99007628401842$ |
| $b_{02} = 0.99504429701789$                   | $a_{2} = 0.99010090405314$  |



### 单通道intergrated loudness 计算流程
![[响度Loudness.drawio.svg]]
