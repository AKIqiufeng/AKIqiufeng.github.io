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
<div>
$$
\begin{aligned}
&F_t=\frac{T_t}{r}=\frac{T_{tq}i_gi_o\eta_T}{r}\\
&T_{tq}:发动机转矩\\
&i_g:变速器传动比\\
&i_0:主减速器传动比
\end{aligned}
$$
<div>

##### 发动机的功率(kW)：
<div>$$
\begin{aligned}
&P_e=\frac{T_{tq}n}{9550}\\
&T_{tq}:发动机转矩 n\cdot m \\
&n:发动机转速 r/min
\end{aligned}
$$</div>

##### 传动系机械效率
<div>$$
\eta _T=\frac{P_{in}-P_T}{P_{in}}
$$</div>
<div>
输入传动系统的功率$P_{in}$  ,损失的功率$P_T$  
等速时：$P_{in}=P_e$
<div>$$
\eta _T=\frac{P_e-P_T}{P_e}=\boxed{1-\frac{P_T}{P_e}}=\eta _离\cdot \eta _变\cdot \eta _传\cdot \eta_{主减}
$$</div>

##### 行驶速度与转速：
<div>$$
u_a=0.377\frac{rn}{i_gi_0}
$$</div>

##### 滚动阻力：
<div>$$
F_f=Wf=\frac{T_f}{r}
$$</div>

##### 地面切向反作用力$F_{X2}$
真正作用在驱动轮上驱动汽车行驶的力
<div>$$
F_{X2}=F_t-F_f
$$</div>

##### 空气阻力：
<div>$$
F_W=C_DA\cdot \frac{1}{2}\rho u_r^2=\boxed{\frac{C_DAu_a^2}{21.15}}
$$</div>

##### 坡道阻力：
<div>$$
F_i=G\sin\alpha \approx G\tan\alpha = Gi
$$</div>

##### 道路阻力：
<div>$$
\begin{aligned}
&F_\Psi=Gf+Gi=G(f+i)=G\Psi\\
&\Psi ：道路阻力系数
\end{aligned}
$$</div>

##### 加速阻力：
<div>$$
\begin{aligned}
&F_j= \delta m\frac{\mathrm{d} u}{\mathrm{d}t}\\
&\delta : 旋转质量换算系数\\
&\delta =1+\frac{1}{m}\frac{\sum I_W}{r^2}  +\frac{1}{m}\frac{I_fi_g^2i_0^2\eta_T}{r^2}
\end{aligned}
$$</div>

##### ⭐汽车行驶方程式：
<div>$$
\begin{aligned}
F_t &=F_f+F_W+F_i+F_j\\
\frac{T_{tq}i_gi_0\eta_T}{r^2} &=Gf\cos\alpha +\frac{C_DAu_a^2}{21.15}+G\sin \alpha +\delta m\frac{\mathrm{d}x }{\mathrm{d}t }  
\end{aligned}
$$</div>

##### 动力因数：
<div>$$
D=\frac{F_t-F_W}{G}=\boxed{\Psi+\frac{\delta}{g}\frac{\mathrm{d}x}{\mathrm{d}t}}
$$</div>

##### 粗略计算爬坡度：
<div>$$
i =D-f
$$</div>


##### 最大爬坡度：
<div>$$
\begin{aligned}
&I档时：\\
&\alpha _{max} = \arcsin \frac{D_{Imax}-f\sqrt{1-D_{Imax}^2+f^2} }{1+f^2} \\
&i_{max}=\tan \alpha _{max}
\end{aligned}
$$</div>

##### 附着力：
<div>$$
\begin{aligned}
&F_\varphi =F_{Xmax}=F_Z \varphi \\
&\varphi:附着系数\\
&汽车行驶附着条件（对后驱）：\\
&F_{X2}\le F_{Z2}\varphi \\
&\boxed{\frac{F_{X2}}{F_{Z2}}\le \varphi}
\end{aligned}
$$</div>

##### 等效坡度q：
<div>$$
q=i+\frac{1}{\cos \alpha}\frac{1}{g}\frac{\mathrm{d}u}{\mathrm{d}t}
$$</div>

##### 附着率（以及最大等效坡度）：
###### 后轮驱动：
后驱动轮附着率：
<div>$$
C_{\varphi 2}=\frac{q}{\frac{a}{L}+\frac{h_g}{L}q}
$$</div>
在一定附着系数$\varphi$的路面上：
汽车能通过的最大等效坡度：
<div>$$
q=\frac{\frac{a}{L}}{\frac{1}{\varphi}-\frac{h_g}{L}}
$$</div>
 
###### 前轮驱动
前驱动轮附着率：
<div>$$
C_{\varphi 1}=\frac{q}{\frac{b}{L}-\frac{h_g}{L}q}
$$</div>
汽车能通过的最大等效坡度：
<div>$$
q=\frac{\frac{b}{L}}{\frac{1}{\varphi}+\frac{h_g}{L}}
$$</div>

###### 四轮驱动：
后轮转矩分配系数：
<div>$$
\begin{aligned}
&\psi =\frac{T_{t2}}{T_{t1}+T_{t2}}\\
&T_{t1}:前驱动轴驱动转矩\\
&T_{t2}:后驱动轴驱动转矩
\end{aligned}
$$</div>
前轴附着率：
<div>$$
C_{\varphi 1}=\frac{(1-\psi)q}{\frac{b}{L}-\frac{h_g}{L}q}
$$</div>
后轴附着率：
<div>$$
C_{\varphi 2}=\frac{\psi q}{\frac{a}{L}+\frac{h_g}{L}q}
$$</div>
最大等效坡度：
<div>$$
\begin{aligned}
&C_{\varphi 1} > C_{\varphi 2}:前轮要求高，取前轮\\
&q=\frac{\frac{b}{L}}{\frac{1-\psi}{\varphi}+\frac{h_g}{L}}\\
&C_{\varphi 1} < C_{\varphi 2}:后轮要求高，后前轮\\
&q=\frac{\frac{a}{L}}{\frac{\psi}{\varphi}-\frac{h_g}{L}}
\end{aligned}
$$</div>

##### 汽车功率平衡方程式：
<div>$$
P_e=\frac{1}{\eta _T}(\frac{Gfu_a}{3600}+\frac{Giu_a}{3600}+\frac{C_DAu_a^3}{76140}+\frac{\delta mu_a}{3600}\frac{\mathrm{d}u}{\mathrm{d}t})
$$</div>
<div>$$
后备功率：P_e-\frac{1}{\eta _T}(P_f+P_W)
$$</div>