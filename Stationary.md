## 平稳性是什么&为什么重要

从最直观的意义上说，平稳性意味着生成时间序列的过程的***统计属性不会随时间而变化***。

这并不意味着该系列不会随时间而变化，只是它的变化*方式*本身不会随时间而变化。

因此，代数等价物也许是一个线性函数，而不是一个常数函数;线性函数的值随着x的增长而变化，但它的变化*方式*保持不变 - 它具有恒定的斜率;一个捕获该变化率的值。



Due to these properties, stationarity has become a common assumption for many practices and tools in time series analysis. These include trend estimation, forecasting and causal inference, among others.



## 关于Stationary

**stationarity — of any kind — is a property of a stochastic process**, and **not** of any finite or infinite realization of it (i.e. a time series of values).

平稳性是一个随机过程的性质，而非随机过程的某一个实现的性质。是内蕴在某个观测序列背后的，非观测的。



## Strong Stationary

[*Strong stationarity*](https://en.wikipedia.org/wiki/Stationary_process) requires the shift-invariance (in time) of the finite-dimensional distributions of a stochastic process. This means that the distribution of a finite sub-sequence of random variables of the stochastic process remains the same as we shift it along the time index axis. For example, all [i.i.d.](https://en.wikipedia.org/wiki/Independent_and_identically_distributed_random_variables) stochastic processes are stationary.[³](https://towardsdatascience.com/stationarity-in-time-series-analysis-90c94f27322#f21b)

任意有限维分布是shift-invariance in time的。分布的平稳性包含了各阶矩的平稳性。

> **Note:** This definition does not assume the [existence/finiteness](https://www.statlect.com/fundamentals-of-probability/moments) of any moment of the random variables composing the stochastic process!

各阶矩不一定存在/有限（存在性和有限性是等价的吗？）



## Weak Stationary

[*Weak stationarity*](https://en.wikipedia.org/wiki/Stationary_process#Weak_or_wide-sense_stationarity) only requires the shift-invariance (in time) of the first moment and the cross moment (the auto-covariance).

Formally, the process *{x*ᵢ *; i∈ℤ}* is *weakly stationary* if:
\1. The first moment of *x*ᵢ is constant; i.e. *∀t, E[x*ᵢ*]=𝜇*
\2. The second moment of *x*ᵢ is finite for all t; i.e. *∀t, E[x*ᵢ*²]<∞* (which also implies of course *E[(x*ᵢ*-𝜇)²]<∞*; i.e. that variance is finite for all *t*)
\3. The cross moment — i.e. the auto-covariance — depends only on the difference *u-v*; i.e. *∀u,v,a, cov(xᵤ, xᵥ)=cov(xᵤ₊ₐ, xᵥ₊ₐ)*

——一阶矩不变，二阶矩有限，一定阶数的cross moment不变



关于stationary，一个直观的图：

![img](https://miro.medium.com/max/700/1*tkx0_wwQ2JT7pSlTeg4yzg.png)



## 白噪声序列（and 高斯白噪声）

[**White Noise Process**](https://en.wikipedia.org/wiki/White_noise)**:** **A white noise process is a serially uncorrelated stochastic process with a mean of zero and a constant and finite variance.**

Formally, the process *{x*ᵢ *; i∈ℤ}* is a *white noise process* if:

- 1. The first moment of *x*ᵢ is always zero; i.e. *∀t, E[x*ᵢ*]=0*

  - 2. The second moment of *x*ᵢ is finite for all t; i.e. *∀t, E[(x*ᵢ*-𝜇)²]<∞*

    - 3. The cross moment *E[xᵤ xᵥ]* is zero when u≠v; i.e. *∀u,v w. u*≠v, *cov(xᵤ, xᵥ)=0*

白噪声——一阶矩为0，二阶矩有限，协方差为零。

Note that this implies that **every white noise process is a weak stationary process**. If, additionally, every variable xᵢ follows a normal distribution with zero mean and the same variance *σ²*, then the process is said to be a ***Gaussian white noise process***.



## 关系

- 白噪声序列是一种特殊的weak stationary process
- 高斯白噪声序列是一种特殊的白噪声序列
- 有限二阶矩的强平稳序列一定是弱平稳序列
- 高斯过程的弱平稳性可以推出强平稳性





