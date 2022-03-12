> 在许多年后，面对行刑队，奥蕾莉亚诺又会hi想起



ACF关注的是整体的相关性

PACF关注特定的某一期



一般来说，一个模型如果合适，那模型的残差应该满足均值为0的正态分布，并且对于任意的滞后阶数，残差自相关系数都应该为零。换句话说，模型的残差应该满足独立正态分布（即残差间没有关联） 。

```text
qqnorm(fit$residuals) 
qqline(fit$residuals)
Box.test(fit$residuals, type="Ljung-Box") 
```



•原始序列的差分序列图

```stylus
plot(diff.appl,type='l')
```



**赤池信息量准则**（英语：Akaike information criterion，简称**AIC**）是评估统计模型的复杂度和衡量[统计](https://zh.wikipedia.org/wiki/统计)模型“拟合”资料之优良性（英语：Goodness of Fit，白话：合身的程度）的一种标准，是由[日本](https://zh.wikipedia.org/wiki/日本)统计学家[赤池弘次](https://zh.wikipedia.org/w/index.php?title=赤池弘次&action=edit&redlink=1)创立和发展的。赤池信息量准则建立在[信息熵](https://zh.wikipedia.org/wiki/熵_(信息论))的概念基础上。



## AIC

在一般的情况下，AIC可以表示为：

其中：*K*是[参数](https://zh.wikipedia.org/wiki/参数)的数量，L是[似然函数](https://zh.wikipedia.org/wiki/似然函数)。

假设条件是模型的误差服从独立正态分布。

让*n*为观察数，*RSS*为[残差](https://zh.wikipedia.org/w/index.php?title=残差&action=edit&redlink=1)[平方和](https://zh.wikipedia.org/wiki/平方和)，那么AIC变为：

增加自由参数的数目提高了拟合的优良性，AIC鼓励数据拟合的优良性但是尽量避免出现[过度拟合](https://zh.wikipedia.org/wiki/過適)（Overfitting）的情况。

所以优先考虑的模型应是AIC值最小的那一个。赤池信息量准则的方法是寻找可以最好地解释数据但包含最少自由参数的模型。



***B***

## BIC

In [statistics](https://en.wikipedia.org/wiki/Statistics), the **Bayesian information criterion** (**BIC**) or **Schwarz information criterion** (also **SIC**, **SBC**, **SBIC**) is a criterion for [model selection](https://en.wikipedia.org/wiki/Model_selection) among a finite set of models; models with lower BIC are generally preferred. It is based, in part, on the [likelihood function](https://en.wikipedia.org/wiki/Likelihood_function) and it is closely related to the [Akaike information criterion](https://en.wikipedia.org/wiki/Akaike_information_criterion) (AIC).

希望越小越好

When fitting models, it is possible to increase the likelihood by adding parameters, but doing so may result in [overfitting](https://en.wikipedia.org/wiki/Overfitting). Both BIC and AIC attempt to resolve this problem by introducing a penalty term for the number of parameters in the model; the penalty term is larger in BIC than in AIC.



![{\displaystyle \mathrm {BIC} =k\ln(n)-2\ln({\widehat {L}}).\ }](https://wikimedia.org/api/rest_v1/media/math/render/svg/9fb26ce833300f98a6df6039624fc7ffaf4ce7fb)

其中k总共估计的参数数量，n是总共的观察点，L是一个似然函数，描述模型拟合的优度。





## Ljung-Box检验



**Ljung-Box 检验**（以 Greta M. Ljung 和 George E. P. Box 命名）是一种统计检验，用于***检验时间序列的一组自相关项中是否有任何一个与零不同***。它不是在每个不同的滞后处测试随机性，而是基于许多滞后来测试"整体"随机性，因此是一个portmanteau测试。

这个测试有时被称为Ljung-Box Q测试，它与Box-Pierce测试密切相关（以George E. P. Box和David A. Pierce的名字命名）。事实上，Ljung-Box检验统计量在导致使用Box-Pierce统计量的论文中被明确描述，[1][2]并且该统计量得名。Box-Pierce 检验统计量是 Ljung-Box 统计量的简化版本，随后的仿真研究显示其性能较差。





# A













