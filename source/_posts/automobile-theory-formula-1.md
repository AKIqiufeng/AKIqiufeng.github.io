---
title: 汽车理论公式整理1
date: 2024-11-22 16:00:55
categories: 学习
tags:
  - 汽车理论
  - 公式
katex: true
single_column: true
---
## 第一章 汽车的动力性

<!--more-->
##### 驱动力：
$$
\begin{aligned}
&F_t=\frac{T_t}{r}=\frac{T_{tq}i_gi_o\eta_T}{r}\\
&T_{tq}:发动机转矩\\
&i_g:变速器传动比\\
&i_0:主减速器传动比
\end{aligned}
$$


##### 发动机的功率(kW)：
$$
\begin{aligned}
&P_e=\frac{T_{tq}n}{9550}\\
&T_{tq}:发动机转矩 n\cdot m \\
&n:发动机转速 r/min
\end{aligned}
$$ ##### 传动系机械效率
$$
\eta _T=\frac{P_{in}-P_T}{P_{in}}
$$
输入传动系统的功率$P_{in}$  ,损失的功率$P_T$  
等速时：$P_{in}=P_e$
$$
\eta _T=\frac{P_e-P_T}{P_e}=\boxed{1-\frac{P_T}{P_e}}=\eta _离\cdot \eta _变\cdot \eta _传\cdot \eta_{主减}
$$

##### 行驶速度与转速：
$$
u_a=0.377\frac{rn}{i_gi_0}
$$

##### 滚动阻力：
$$
F_f=Wf=\frac{T_f}{r}
$$

##### 地面切向反作用力$F_{X2}$
真正作用在驱动轮上驱动汽车行驶的力
$$
F_{X2}=F_t-F_f
$$

##### 空气阻力：
$$
F_W=C_DA\cdot \frac{1}{2}\rho u_r^2=\boxed{\frac{C_DAu_a^2}{21.15}}
$$

##### 坡道阻力：
$$
F_i=G\sin\alpha \approx G\tan\alpha = Gi
$$

##### 道路阻力：
$$
\begin{aligned}
&F_\Psi=Gf+Gi=G(f+i)=G\Psi\\
&\Psi ：道路阻力系数
\end{aligned}
$$

##### 加速阻力：
$$
\begin{aligned}
&F_j= \delta m\frac{\mathrm{d} u}{\mathrm{d}t}\\
&\delta : 旋转质量换算系数\\
&\delta =1+\frac{1}{m}\frac{\sum I_W}{r^2}  +\frac{1}{m}\frac{I_fi_g^2i_0^2\eta_T}{r^2}
\end{aligned}
$$

##### ⭐汽车行驶方程式：
$$
\begin{aligned}
F_t &=F_f+F_W+F_i+F_j\\
\frac{T_{tq}i_gi_0\eta_T}{r^2} &=Gf\cos\alpha +\frac{C_DAu_a^2}{21.15}+G\sin \alpha +\delta m\frac{\mathrm{d}x }{\mathrm{d}t }  
\end{aligned}
$$

##### 动力因数：
$$
D=\frac{F_t-F_W}{G}=\boxed{\Psi+\frac{\delta}{g}\frac{\mathrm{d}x}{\mathrm{d}t}}
$$

##### 粗略计算爬坡度：
$$
i =D-f
$$


##### 最大爬坡度：
$$
\begin{aligned}
&I档时：\\
&\alpha _{max} = \arcsin \frac{D_{Imax}-f\sqrt{1-D_{Imax}^2+f^2} }{1+f^2} \\
&i_{max}=\tan \alpha _{max}
\end{aligned}
$$

##### 附着力：
$$
\begin{aligned}
&F_\varphi =F_{Xmax}=F_Z \varphi \\
&\varphi:附着系数\\
&汽车行驶附着条件（对后驱）：\\
&F_{X2}\le F_{Z2}\varphi \\
&\boxed{\frac{F_{X2}}{F_{Z2}}\le \varphi}
\end{aligned}
$$

##### 等效坡度q：
$$
q=i+\frac{1}{\cos \alpha}\frac{1}{g}\frac{\mathrm{d}u}{\mathrm{d}t}
$$
##### 附着率（以及最大等效坡度）：
###### 后轮驱动：
后驱动轮附着率：
$$
C_{\varphi 2}=\frac{q}{\frac{a}{L}+\frac{h_g}{L}q}
$$
在一定附着系数$\varphi$的路面上：
汽车能通过的最大等效坡度：
$$
q=\frac{\frac{a}{L}}{\frac{1}{\varphi}-\frac{h_g}{L}}
$$
 
###### 前轮驱动
前驱动轮附着率：
$$
C_{\varphi 1}=\frac{q}{\frac{b}{L}-\frac{h_g}{L}q}
$$
汽车能通过的最大等效坡度：
$$
q=\frac{\frac{b}{L}}{\frac{1}{\varphi}+\frac{h_g}{L}}
$$

###### 四轮驱动：
后轮转矩分配系数：
$$
\begin{aligned}
&\psi =\frac{T_{t2}}{T_{t1}+T_{t2}}\\
&T_{t1}:前驱动轴驱动转矩\\
&T_{t2}:后驱动轴驱动转矩
\end{aligned}
$$
前轴附着率：
$$
C_{\varphi 1}=\frac{(1-\psi)q}{\frac{b}{L}-\frac{h_g}{L}q}
$$
后轴附着率：
$$
C_{\varphi 2}=\frac{\psi q}{\frac{a}{L}+\frac{h_g}{L}q}
$$
最大等效坡度：
$$
\begin{aligned}
&C_{\varphi 1}>C_{\varphi 2}:前轮要求高，取前轮\\
&q=\frac{\frac{b}{L}}{\frac{1-\psi}{\varphi}+\frac{h_g}{L}}\\
&C_{\varphi 1}<C_{\varphi 2}:后轮要求高，后前轮\\
&q=\frac{\frac{a}{L}}{\frac{\psi}{\varphi}-\frac{h_g}{L}}
\end{aligned}
$$

##### 汽车功率平衡方程式：
$$
P_e=\frac{1}{\eta _T}(\frac{Gfu_a}{3600}+\frac{Giu_a}{3600}+\frac{C_DAu_a^3}{76140}+\frac{\delta mu_a}{3600}\frac{\mathrm{d}u}{\mathrm{d}t})
$$

$$
后备功率：P_e-\frac{1}{\eta _T}(P_f+P_W)
$$