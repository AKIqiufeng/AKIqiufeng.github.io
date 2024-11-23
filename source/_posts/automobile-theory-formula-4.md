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

<!--more-->

##### 地面制动力：
<div>
$$
\begin{aligned}
&F_{Xb}=\begin{cases}
 F_{\mu }= \frac{T_{\mu}}{r} ,F_{\mu }\le F_{\varphi}\\
 F_{\varphi }=F_{Z}\varphi ,F_{\mu}>F_{\varphi}
\end{cases}\\
&F_{Xb}:地面制动力\\
&F_{\mu }:制动器制动力,T_{\mu}:制动器摩擦力矩\\
&\varphi:路面附着系数(由路面轮胎决定)
\end{aligned}
$$
</div>

##### 滑移率：
<div>
$$
\begin{aligned}
\begin{cases}
 u_{w}& = u_{\delta}+\omega_{w}r_{r0}\\
s&=\frac{u_{\delta}}{u_{w}}\times 100\% 
\end{cases}\Rightarrow s=\frac{u_{w}-\omega_{w}r_{r0}}{u_{w}}\times 100\% 
\end{aligned}
$$
</div>

##### 制动力系数,侧向力系数：
<div>
$$
\begin{aligned}
制动力系数：\varphi_{b}=\frac{F_{Xb}}{F_{Z}}\\
侧向力系数：\varphi_{l}=\frac{F_{Y}}{F_{Z}}
\end{aligned}
$$
</div>

##### 制动减速度：
<div>
$$
\begin{aligned}
&总地面制动力：F_{Xb}=(F_{Z1}+F_{Z2})\varphi_{b}=\varphi_{b}G=\frac{G}{g}\frac{du}{dt}\\
&制动减速度：a_{bmax}=\varphi_{b}g \\
&前后轮同时抱死：a_{bmax}=\varphi_{s}g \\
&装有ABS：a_{bmax}=\varphi_{p}g
\end{aligned}
$$
</div>

##### 充分发出的平均减速度：
<div>
$$
\begin{aligned}
&MFDD=\frac{(u_{b}^{2}-u_{e}^{2})}{25.92(s_{e}-s_{b})} \\
&u_{b}:0.8u_{0}\\
&u_{e}:0.1u_{0}\\
&u_{0}:起始制动车速\\
&s_{b}:u_{0}到u_{b}行驶的距离\\
&s_{e}:u_{0}到u_{e}行驶的距离
\end{aligned}
$$
</div>

##### 制动距离：
<div>
{% raw %}
$$
\begin{aligned}
&s=\frac{1}{3.6}({\tau _{2}}'+\frac{{\tau _2}''}{2} ) u_{a0}+\frac{u_{a0}^{2}}{25.92} \\
&u_{a0}:起始制动速度，单位：km/h
\end{aligned}
$$
{% endraw %}
</div>

##### 左右车轮制动力不相等度：
<div>
$$
\begin{aligned}
&\Delta F_{\mu r}=\frac{F_{\mu b}-F_{\mu 1}}{F_{\mu b}} \times 100\%\\
&F_{\mu b}：大的制动器制动力\\
&F_{\mu 1}：小的制动器制动力
\end{aligned}
$$
</div>

##### 制动强度定义：
<div>
$$
\begin{aligned}
&\frac{du}{dt}：制动减速度\\
&制动强度定义：a_b=\frac{du}{dt}=zg\\
&z：制动强度 
\end{aligned}
$$
</div>

##### 前后轮法向作用力：
<div>
$$
\begin{aligned}
&\begin{cases}
F_{Z1}=\frac{G}{L} (b+zh_g)\\
F_{Z2}=\frac{G}{L}(a-zh_g)
\end{cases}\\
&a:前轴到质心距离，b:后轴到质心距离\\
&前后轮都抱死时：F_{Xb}=F_\varphi =G\varphi\\
&即：\frac{du}{dt}=\varphi g\\
& 替换公式中的zh_g为\varphi h_g 
\end{aligned}
$$
</div>

##### 制动器制动力分配系数：
<div>
$$
\begin{aligned}
&\beta=\frac{F_{\mu 1}}{F_\mu}=\frac{F_{\mu 1}}{F_{\mu 1}+F_{\mu 2}}\\
&F_{\mu 1}:前制动器制动力，F_{\mu 2}:后制动器制动力\\
&\beta线（制动力分配线）斜率:\\
&k=\tan \theta =\frac{1-\beta}{\beta} 
\end{aligned}
$$
</div>

##### ⭐同步附着系数：
<div>
$$
\varphi _0=\frac{L\beta -b}{h_g}
$$
</div>

##### 利用附着系数
<div>
$$
\begin{aligned}
&定义式：\varphi _i=\frac{F_{Xbi}}{F_{Zi}}\\
&前轴：\varphi_f=\frac{F_{Xb1}}{F_{Z1}}=\frac{\beta z}{\frac{1}{L}(b+zh_g)} \\
&后轴：\varphi_r=\frac{F_{Xb2}}{F_{Z2}}=\frac{(1-\beta )z}{\frac{1}{L}(a-zh_g)} \\
\end{aligned}
$$
</div>

##### 制动效率：
<div>
$$
\begin{aligned}
&定义式：E=\frac{z}{\varphi }\\
&前轴：E_f=\frac{z}{\varphi _f}=\frac{b/L}{\beta -\varphi _f h_g/L} \\
&后轴：E_r=\frac{z}{\varphi _r}=\frac{a/L}{(1-\beta )+\varphi _r h_g/L} \\
\end{aligned}
$$
</div>