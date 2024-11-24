---
title: 汽车理论公式整理2
date: 2024-11-22 13:00:55
categories: 学习
tags:
  - 汽车理论
  - 公式
katex: true
single_column: true
sticky: 2
---
## 第二章 汽车的燃油经济性

<!--more-->
循环工况分为四个部分：
#### 等速工况
等速时，发动机功率：
<div>$$
P_e=\frac{1}{\eta _T}(P_f+P_W)
$$</div>

##### 单位时间，燃油消耗量$Q_t$：
<div>$$
Q_t =\frac{P_eb}{367.1\rho g}
$$</div>

##### 等速行驶s行程，燃油消耗量$Q$：
<div>$$
Q=Q_tt=Q_t\frac{3.6 s}{u_a}=\frac{P_ebs}{102u_a\rho g}
$$</div>

##### 等速百公里燃油消耗量$Q_s$：
<div>$$
Q_s=\frac{P_eb\cdot100}{102u_a\rho g}=\boxed{\frac{P_eb}{1.02u_a\rho g}}
$$</div>

#### 等加速工况
单位时间，燃油消耗量$Q_t$(小区间看作等速)：
<div>$$
Q_t =\frac{P_eb}{367.1\rho g}
$$</div>

##### 速度每增加1km/h，时间：
<div>$$
\Delta t=\frac{1}{3.6\frac{\mathrm{d}u}{\mathrm{d}t}}
$$</div>

##### 每个区间燃油消耗量：
(平均的燃油消耗量\*时间)
<div>$$
Q_1=\frac{1}{2}(Q_{t0}+Q_{t1})\Delta t
$$</div>

##### 整个过程行驶的距离：
<div>$$
S_a=\frac{u_{a2}^2-u_{a1}^2}{25.92\frac{\mathrm{d}u}{\mathrm{d}t}}
$$</div>

#### 等减速工况
##### 减速时间：
（等减速运动计算时间）
<div>$$
t=\frac{v_{a2}-v_{a3}}{a}=\boxed{\frac{u_{a2}-u_{a3}}{3.6\frac{\mathrm{d}u}{\mathrm{d}t_d}}}
$$</div>

##### 整个减速过程燃油消耗量：
<div>$$
\begin{aligned}
&Q_d=Q_it=\frac{u_{a2}-u_{a3}}{3.6\frac{\mathrm{d}u}{\mathrm{d}t_d}}Q_i\\
&Q_i:怠速燃油消耗率
\end{aligned}
$$</div>

##### 这个过程行驶的距离：
（与加速过程计算公式相同）
<div>$$
S_a=\frac{u_{a2}^2-u_{a1}^2}{25.92\frac{\mathrm{d}u}{\mathrm{d}t}}
$$</div>

#### 怠速停车
##### 燃油消耗量：
<div>$$
\begin{aligned}
&Q_{id}=Q_it_s\\
&t_s:怠速时间
\end{aligned}
$$</div>

#### 整个循环工况
##### 评价指标$Q_s$：
百公里燃油消耗量：
<div>$$
Q_s=\frac{\sum Q}{s}\times 100
$$</div>

#### 影响燃油经济性的因素
##### 等速百公里燃油消耗量：
（与上面相同）
<div>$$
\begin{aligned}
&Q_s=\frac{P_eb}{1.02u_a\rho g}=\frac{CFb}{\eta_T}\\
&C:常数\\
&F:行驶阻力，F=F_f+F_W
\end{aligned}
$$</div>

##### 负荷率：
<div>$$
负荷率=\frac{使用复合}{最大负荷}
$$</div>
负荷率低，燃油消耗率b增大，经济性差

#### 调速特性
##### 无级变速器调节特性：
传动比$i'$与转速$n$及行驶速度$u_a$的关系：
<div>$$
\begin{aligned}
&i'=0.377\frac{nr}{i_0u_a}=A\frac{n}{u_a}  \\
&A:对某一汽车为常数，A=0.377\frac{r}{i_0} 
\end{aligned}
$$</div>

