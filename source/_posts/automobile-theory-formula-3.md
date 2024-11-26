---
title: 汽车理论公式整理3
date: 2024-11-22 20:00:55
categories: 学习
tags:
  - 汽车理论
  - 公式
katex: true
single_column: true
sticky: 5
---
## 第三章 汽车动力装置参数的选择

<!--more-->
#### 发动机功率选择
##### 由$u_{amax}$确定发动机功率
<div>$$
p_e=\frac{1}{\eta _T}\left(\frac{Gf}{3600}u_{amax}+\frac{C_DA}{76140}u_{amax}^3\right)
$$</div>

##### 由比功率确定发动机功率
###### 比功率($kW/t$)：
<div>$$
\begin{aligned}
汽车比功率&=\frac{1000P_e}{m} \\
&=\frac{fg}{3.6\eta _T}u_{amax}+\frac{C_DA}{76.14m\eta _T}u_{amax}^3 
\end{aligned}
$$</div>
货车主要取决于第二项（空气阻力），随质量增大减小
轿车主要与$u_{amax}$有关，还与$C_DA/m$、$\eta _T$有关

#### 最小传动比选择
选择因素：最高车速（动力性）、后背功率（燃油经济性）、驾驶性能
##### 传动系总传动比：
<div>$$
\begin{aligned}
&i_t=i_gi_0i_c\\
&i_c:副变速器传动比
\end{aligned}
$$</div>

##### 不同i0时汽车功率平衡图

<img src="https://r2.haier-mail.com/imghost/2024/11/屏幕截图%202024-11-24%20205503.png" width="50%" height="50%" alt="不同i0时汽车功率平衡图"/>

###### 最高车速：
主减速器传动比为$i_{02}$时，最高车速最大，$i_0$适中
###### 后备功率：
主减速器传动比为$i_{01}$时，后备功率小，动力性差，燃油经济性好
主减速器传动比为$i_{03}$时，后备功率大，动力性好，燃油经济性差
###### 驾驶性能：
加速性、动力装置的转矩响应、噪声与振动

#### 最大传动比的选择
选择因素：最大爬坡度、附着率、最低稳定车速
##### 最大爬坡度：
(忽略空气阻力)
<div>$$
\begin{aligned}
F_{tmax}&=F_f+F_{imax}\\
\frac{T_{tqmax}i_{g1}i_0\eta_T}{r^2} &=Gf\cos\alpha _{max}++G\sin \alpha _{max}\\
i_{g1}&\ge \frac{G(f\cos \alpha _{max}+\sin \alpha _{max})r}{T_{tqmax}i_0\eta_T}
\end{aligned}
$$</div>

##### 附着条件：
<div>$$
\begin{aligned}
&F_{Xmax}\le F_\varphi\\
&F_{tmax}=\frac{T_{tq}i_{gmax}i_0\eta_T}{r^2}\le F_\varphi
\end{aligned}
$$</div>

##### 最低稳定车速：
<div>$$
i_{tmax}=0.377\frac{n_{min}r}{u_{amin}}
$$</div>

#### 传动系挡数与各档传动比的选择
档位越多，对动力性和燃油经济性都有利
汽车各档传动比分配基本原则：**按等比级数分配**
充分利用发动机提供的功率，提高动力性。
无冲击接合、便于起步和操纵、便于与副变速器结合
