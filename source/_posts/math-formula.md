---
title: 高数部分公式整理
date: 2024-11-22 16:02:07
categories: 学习
tags:
  - 高数
  - 公式
katex: true
single_column: true
sticky: 10
---
*记录高数中一些常用的公式*
更新中。。。
<!--more-->
#### 常用等价无穷小
当$x\to 0$时：
<div>$$
\begin{aligned}
&\sin x \sim \tan x \sim \arcsin x \sim \arctan x \sim x\\
& e^x-1 \sim \ln{(1+x)} \sim x\\
&a^x-1\sim x\ln {a}\\
&1-\cos x\sim \frac{1}{2}x^2\\
&(1+x)^a\sim ax\\
&x-\ln{(1+x)}\sim \frac{1}{2}x^2\\
&x-\sin x\sim \arcsin x-x\sim \frac{1}{6}x^3\\
&\tan x-x\sim x-\arctan x\sim \frac{1}{3}x^3\\
&\tan x-\sin x\sim \arcsin x-\arctan x\sim \frac{1}{2}x^3   
\end{aligned}
$$</div>

#### 基本求导公式
<div>$$
\begin{aligned}
&C'=0(C为常数)&(x^\alpha )'=\alpha x^{\alpha -1}\\
&(\sin x)'=\cos x&(\cos x)'=-\sin x\\
&(\tan x)'=\sec ^2x&(\cot x)'=-\csc ^2x\\
&(\sec x)'=\sec x\tan x&(\csc x)'=-\csc x\cot x\\
&(a^x)'=a^x\ln a&(e^x)'=e^x\\
&(\arcsin x)'=\frac{1}{\sqrt{1-x^2} } &(\arccos x)'=-\frac{1}{\sqrt{1-x^2} }\\
&(\arctan x)'=\frac{1}{1+x^2} &(\operatorname{arccot} x)'=-\frac{1}{1+x^2} 
\end{aligned}
$$</div>

##### 点火公式
<div>$$
\begin{aligned}
\int_{0}^{\frac{\pi }{2} } \sin^{n} x =\int_{0}^{\frac{\pi }{2} } \cos^{n} x=\begin{cases}
\frac{n-1}{n}\times \frac{n-3}{n-2}\times \dotsb\times \frac{1}{2}\times\frac{\pi}{2},n为正偶数  \\ 
\frac{n-1}{n}\times \frac{n-3}{n-2}\times \dotsb\times \frac{2}{3}\times 1 ,n为大于1的正奇数 
\end{cases}
\end{aligned}
$$</div>