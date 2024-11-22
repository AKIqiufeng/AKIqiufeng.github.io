---
title: 汽车理论公式整理4
date: 2024-11-22 16:00:55
categories: 学习
tags:
  - 汽车理论
  - 公式
katex: true
single_column: true
---
## 第四章 汽车的制动性
整理中...
<!--more-->

###### 地面制动力：
<div>
$$
\begin{align}
&F_{Xb}=\begin{cases}
 F_{\mu }= \frac{T_{\mu}}{r} ,F_{\mu }\le F_{\varphi}\\
 F_{\varphi }=F_{Z}\varphi ,F_{\mu}>F_{\varphi}
\end{cases}\\
&F_{Xb}:地面制动力\\
&F_{\mu }:制动器制动力,T_{\mu}:制动器摩擦力矩\\
&\varphi:路面附着系数(由路面轮胎决定)
\end{align}
$$
</div>

###### 滑移率：
<div>
$$
\begin{align}
\begin{cases}
 u_{w}& = u_{\delta}+\omega_{w}r_{r0}\\
s&=\frac{u_{\delta}}{u_{w}}\times 100\% 
\end{cases}\Rightarrow s=\frac{u_{w}-\omega_{w}r_{r0}}{u_{w}}\times 100\% 
\end{align}
$$
</div>

###### 制动力系数,侧向力系数：
<div>
$$
\begin{align}
制动力系数：\varphi_{b}=\frac{F_{Xb}}{F_{Z}}\\
侧向力系数：\varphi_{l}=\frac{F_{Y}}{F_{Z}}
\end{align}
$$
</div>

###### 制动减速度：
<div>
$$
\begin{align}
&总地面制动力：F_{Xb}=(F_{Z1}+F_{Z2})\varphi_{b}=\varphi_{b}G=\frac{G}{g}\frac{du}{dt}\\
&制动减速度：a_{bmax}=\varphi_{b}g \\
&前后轮同时抱死：a_{bmax}=\varphi_{s}g \\
&装有ABS：a_{bmax}=\varphi_{p}g
\end{align}
$$
</div>

###### 充分发出的平均减速度：
<div>
$$
\begin{align}
&MFDD=\frac{(u_{b}^{2}-u_{e}^{2})}{25.92(s_{e}-s_{b})} \\
&u_{b}:0.8u_{0}\\
&u_{e}:0.1u_{0}\\
&u_{0}:起始制动车速\\
&s_{b}:u_{0}到u_{b}行驶的距离\\
&s_{e}:u_{0}到u_{e}行驶的距离
\end{align}
$$
</div>

###### 制动距离：
<div>
{% raw %}
$$
\begin{align}
&s=\frac{1}{3.6}({\tau _{2}}'+\frac{{\tau _2}''}{2} ) u_{a0}+\frac{u_{a0}^{2}}{25.92} \\
&u_{a0}:起始制动速度，单位：km/h
\end{align}
$$
{% endraw %}
</div>

###### 左右车轮制动力不相等度：
<div>
$$
\begin{align}
&\Delta F_{\mu r}=\frac{F_{\mu b}-F_{\mu 1}}{F_{\mu b}} \times 100\%\\
&F_{\mu b}：大的制动器制动力\\
&F_{\mu 1}：小的制动器制动力
\end{align}
$$
</div>
