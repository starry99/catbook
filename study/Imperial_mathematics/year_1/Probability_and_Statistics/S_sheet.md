---
layout: simple
title: Statistics Part Memory Sheet
---

#### Based on the lectures and notes of [Dr. Dean Bodenham](https://www.ma.imperial.ac.uk/~dab10/).
## 1. Central tendency and dispersion

### Theorem (The minimum expected square deviation is the mean)

Given a random variable $$X$$, over all values $$a \in \mathbb{R}$$,

$$
\min _{a} \mathrm{E}\left[(X-a)^{2}\right]=\mathrm{E}\left[(X-\mathrm{E}[X])^{2}\right] .
$$

$$
\begin{aligned}
\mathrm{E}\left[(X-a)^{2}\right] & =\mathrm{E}\left[(X-\mathrm{E}[X]+\mathrm{E}[X]-a)^{2}\right] \\
& =\mathrm{E}\left[([X-\mathrm{E}[X]]+[\mathrm{E}[X]-a])^{2}\right] \\
& =\mathrm{E}\left[(X-\mathrm{E}[X])^{2}\right]+0+\mathrm{E}\left[(\mathrm{E}[X]-a)^{2}\right] \\
& =\mathrm{E}\left[(X-\mathrm{E}[X])^{2}\right]+(\mathrm{E}[X]-a)^{2},
\end{aligned}
$$

$$
\mathrm{E}[X-\mathrm{E}[X]]=\mathrm{E}[X]-\mathrm{E}[\mathrm{E}[X]]=\mathrm{E}[X]-\mathrm{E}[X]=0,
$$

$$
\begin{aligned}
2 \mathrm{E}[(X-\mathrm{E}[X])(\mathrm{E}[X]-a)] & =2(\mathrm{E}[X]-a) \mathrm{E}[X-\mathrm{E}[X]] \\
& =2(\mathrm{E}[X]-a) \cdot 0 \\
& =0 .
\end{aligned}
$$

$$
\begin{aligned}
\mathrm{E}\left[(X-a)^{2}\right] & =\mathrm{E}\left[(X-\mathrm{E}[X])^{2}\right]+(\mathrm{E}[X]-a)^{2} \\
\Rightarrow & \mathrm{E}\left[(X-a)^{2}\right] \geq \mathrm{E}\left[(X-\mathrm{E}[X])^{2}\right] .
\end{aligned}
$$

### Definition (Variance and standard deviation)

The variance of a random variable $$X$$ is defined as

$$
\operatorname{Var}(X)=\mathrm{E}\left[(X-\mathrm{E}[X])^{2}\right] .
$$

The positive square root of $$\operatorname{Var}(X)$$ is the standard deviation of $$X$$.

### Remark

The variance is the minimum expected square deviation.
For any random variable $$X$$, the variance of $$X$$ is denoted $$\operatorname{Var}(X)$$ and

- is defined as $$\operatorname{Var}(X)=\mathrm{E}\left[(X-\mathrm{E}[X])^{2}\right]$$

- can be rewritten as $$\operatorname{Var}(X)=\mathrm{E}\left[X^{2}\right]-(\mathrm{E}[X])^{2}$$,

- can be interpreted as $$\operatorname{Var}(X)=\min _{a \in \mathbb{R}} \mathrm{E}\left[(X-a)^{2}\right]$$.

### Proposition

Suppose that the random variable $$X$$ is known to only take values in the bounded range $$[a, b]$$. Then

$$
\operatorname{Var}(X) \leq \frac{(b-a)^{2}}{4}
$$

### Exercise

$$
\begin{aligned}
\sigma^{2} & =\operatorname{Var}(X)=\mathrm{E}\left[X^{2}\right]-(\mathrm{E}[X])^{2} \\
\Rightarrow \mathrm{E}\left[X^{2}\right] & =\sigma^{2}+(\mathrm{E}[X])^{2}=\sigma^{2}+(\mu)^{2}=\mu^{2}+\sigma^{2}
\end{aligned}
$$

### Definition (Sample Mean)

Given the random variables $$X_{1}, X_{2}, \ldots, X_{n}$$, the sample mean $$\bar{X}$$ is the statistic defined as the arithmetic mean of these variables,

$$
\bar{X}=\frac{X_{1}+X_{2}+\cdots+X_{n}}{n}=\frac{1}{n} \sum_{i=1}^{n} X_{i} .
$$

### Definition (Sample Variance)

Given the random variables $$X_{1}, X_{2}, \ldots, X_{n}$$, the sample variance $$S^{2}$$ is defined by

$$
S^{2}=\frac{1}{n-1} \sum_{i=1}^{n}\left(X_{i}-\bar{X}\right)^{2}
$$

The sample standard deviation is the statistic defined by $$S=\sqrt{S^{2}}$$.

### Proposition

Suppose that the random variables $$X_{1}, X_{2}, \ldots, X_{n}$$ are independently sampled from a distribution $$F_{X}$$ that has mean $$\mu$$ and finite variance $$\sigma^{2}$$. Then

 $$\mathrm{E}(\bar{X})=\mu$$

 $$\operatorname{Var}(\bar{X})=\frac{\sigma^{2}}{n}$$

 $$\mathrm{E}\left(S^{2}\right)=\sigma^{2}$$

### Definition (The Sample mean for a set of observations)

For real values $$x_{1}, x_{2}, \ldots, x_{n}$$, the sample variance $$s^{2}$$ is defined as

$$
s^{2}=\frac{1}{n-1} \sum_{i=1}^{n}\left(x_{i}-\bar{x}\right)^{2}, \quad \text { where } \quad \bar{x}=\frac{1}{n} \sum_{j=1}^{n} x_{j} .
$$

Proof:

$$
\begin{aligned}
\sum_{i=1}^{n}\left(x_{i}-a\right)^{2} & =\sum_{i=1}^{n}\left[\left(x_{i}-\bar{x}\right)+(\bar{x}-a)\right]^{2}\\
&=\sum_{i=1}^{n}\left[\left(x_{i}-\bar{x}\right)^{2}+2\left(x_{i}-\bar{x}\right)(\bar{x}-a)+(\bar{x}-a)^{2}\right] \\
& =\sum_{i=1}^{n}\left(x_{i}-\bar{x}\right)^{2}+2(\bar{x}-a) \cdot 0+n(\bar{x}-a)^{2} \\
& =\sum_{i=1}^{n}\left(x_{i}-\bar{x}\right)^{2}+n(\bar{x}-a)^{2}
\end{aligned}
$$

$$
\sum_{i=1}^{n}\left(x_{i}-a\right)^{2} \geq \sum_{i=1}^{n}\left(x_{i}-\bar{x}\right)^{2}
$$

### Theorem (Markov's inequality)

If a random variable $$X$$ can only take nonnegative values, then

$$
\mathrm{P}(X \geq a) \leq \frac{\mathrm{E}(X)}{a}, \quad \text { for all } a>0
$$

Proof: Fix a positive number $$a>0$$, and define the random variable

$$
Y_{a}= \begin{cases}0, & \text { if } X<a \\ a, & \text { if } X \geq a\end{cases}
$$

This definition of $$Y_{a}$$ ensures that $$Y_{a} \leq X$$ for all values of $$a$$ and $$X$$, and therefore:

$$
\mathrm{E}\left(Y_{a}\right) \leq \mathrm{E}(X)
$$

On the other hand, since $$Y_{a}$$ is a discrete random variable, one can computes its expectation as

$$
\begin{aligned}
\mathrm{E}\left(Y_{a}\right) & =0 \cdot \mathrm{P}\left(Y_{a}=0\right)+a \cdot \mathrm{P}\left(Y_{a}=a\right) \\
& =0 \cdot \mathrm{P}(X<a)+a \cdot \mathrm{P}(X \geq a) . \\
\Rightarrow \mathrm{E}\left(Y_{a}\right) & =a \cdot \mathrm{P}(X \geq a) .
\end{aligned}
$$

Combining Equations (1.13) and (1.14), one obtains

$$
a \cdot \mathrm{P}(X \geq a) \leq \mathrm{E}(X)
$$

from which the inequality in Equation (1.12) follows.

### Theorem (Chebyshev's inequality)

If $$X$$ is a random variable with mean $$\mu$$ and variance $$\sigma^{2}$$, then for all $$c>0$$,

$$
\mathrm{P}(|X-\mu| \geq c) \leq \frac{\sigma^{2}}{c^{2}}
$$

### Corollary

If $$X$$ is a random variable with mean $$\mu$$ and variance $$\sigma^{2}$$, then for all $$k>0$$,

$$
\mathrm{P}(|X-\mu| \geq k \sigma) \leq \frac{1}{k^{2}}
$$

### Definition (Parameter)

In a problem of statisical inference, a characteristic or combination of characteristics that determine the (joint) distribution for the random variable(s) of interest is called a parameter of the distribution. i.e. (mean, variance, etc.)

### Definition (Statistic)

Suppose that the observable random variables of interest are $$X_{1}, X_{2}, \ldots, X_{n}$$. Let $$r$$ be an arbitrary real-valued function of $$n$$ random variables. Then the random variable $$T=r\left(X_{1}, X_{2}, \ldots, X_{n}\right)=r(\mathbf{X}) (T: X^n \to F)$$ is called a statistic.

### Definition (Point Estimator)

 Given a sample of random variables $$X_{1}, X_{2}, \ldots, X_{n}$$, a point estimator is any function $$\widehat{\Theta}\left(X_{1}, X_{2}, \ldots, X_{n}\right)$$.

### Definition (The stndard error of an estimator)

The standard error of the estimator $$\widehat{\Theta}$$ is defined as the square root of its variance, i.e. $$\mathrm{SE}_{\widehat{\Theta}}=\sqrt{\operatorname{Var}(\widehat{\Theta})}$$.

### Definition (Interval Estimator)

An interval estimate of a real-valued parameter $$\theta$$ is any pair of functions $$L(\mathbf{x})$$ and $$U(\mathbf{x})$$ of a sample that satisfy $$L(\mathbf{x}) \leq U(\mathbf{x})$$, for all possible $$\mathbf{x}=\left(x_{1}, \ldots, x_{n}\right)$$. The random interval $$[L(\mathbf{X}), U(\mathbf{X})]$$ is called an interval estimator, and if $$\mathbf{X}=\mathbf{x}$$ is observed then the inference $$L(\mathbf{x}) \leq \theta \leq U(\mathbf{x})$$ is made.

### Definitiion (Confidence Probability)

For an interval estimator $$[L(\mathbf{X}), U(\mathbf{X})]$$ of a parameter $$\theta$$, the coverage probability of $$[L(\mathbf{X}), U(\mathbf{X})]$$ is the probability that the random interval $$[L(\mathbf{X}), U(\mathbf{X})]$$ covers the true parameter, $$\theta$$. In symbols, it is denoted by either $$\mathrm{P}(\theta \in[L(\mathbf{X}), U(\mathbf{X})] \mid \theta)$$ or $$\mathrm{P}_{\theta}(\theta \in[L(\mathbf{X}), U(\mathbf{X})])$$.

### Definition (Confidence Interval)

If the interval estimator $$[L(\mathbf{X}), U(\mathbf{X})]$$ is designed so that $$L(\mathbf{X}) \leq U(\mathbf{X})$$ and

$$
\mathrm{P}_{\theta}(L(\mathbf{X}) \leq \theta \leq U(\mathbf{X})) \geq 1-\alpha,
$$

for every possible value of $$\theta$$, and some $$\alpha \in(0,1)$$, then we call $$[L(\mathbf{X}), U(\mathbf{X})]$$ a $$1-\alpha$$ confidence interval.

### Definition (Estimation Error)

The estimation error of the estimator $$\widehat{\Theta}$$ of a parameter $$\theta$$ is defined to be $$\widehat{\Theta}-\theta$$.

### Definition (Bias)

The bias of the estimator $$\widehat{\Theta}$$ of a parameter $$\theta$$, denoted by $$b_{\theta}(\widehat{\Theta})$$, is the expected value of the estimation error:

$$
b_{\theta}(\widehat{\Theta})=\mathrm{E}[\hat{\Theta}]-\theta
$$

### Definition (Unbiased Estimator)

The estimator $$\widehat{\Theta}$$ of a parameter $$\theta$$ is called unbiased if $$E[\widehat{\Theta}]=\theta$$, for every possible value of $$\theta$$.

### Definition (Mean Squared Error)

The mean squared error of the estimator $$\widehat{\Theta}$$ of a parameter $$\theta$$ is defined as the quantity $$\mathrm{E}\left[(\widehat{\Theta}-\theta)^{2}\right]$$.

### Theorem

The mean squared error of an estimator $$\widehat{\Theta}$$ of a parameter $$\theta$$ can be expressed in terms of its bias and variance:

$$
\mathrm{E}\left[(\widehat{\Theta}-\theta)^{2}\right]=\left[b_{\theta}(\widehat{\Theta})\right]^{2}+\operatorname{Var}(\widehat{\Theta}) .
$$

### Definition (The Support of a function)

The support of a function is the set of values in the domain that are not mapped to zero, i.e. the support of the function $$f: \mathbb{R} \rightarrow \mathbb{R}$$ is the set $$\{x \in \mathbb{R} \mid f(x) \neq 0\}$$.

### Definition (Mode)

For a random variable $$X$$ with probability density (or mass) function $$f_{X}$$, the mode of the distribution of $$X$$ is defined as

$$
\operatorname{mode}(X)=\arg \underset{x}{\max } f_{X}(x)
$$

### Definition (Median)

For a random variable $$X$$, a median of the distribution of $$X$$ is defined as a value $$m$$ such that

$$
\mathrm{P}(X \geq m) \geq \frac{1}{2} \quad \text { and } \quad \mathrm{P}(X \leq m) \geq \frac{1}{2}
$$

While there is no standard notation for this, it is possible to write $$m=\operatorname{median}(X)$$.

### Theorem

Suppose that $$m$$ is a median of the distribution for the random variable $$X$$. Then, for any real value $$a$$,

$$
\min _{a} \mathrm{E}(|X-a|)=\mathrm{E}(|X-m|)
$$

### Definition (The Sample median)

Given a sample of observations $$x_{1}, x_{2}, \ldots, x_{n}$$, the sample median $$m$$ is defined as

$$
m= \begin{cases}x_{([n+1] / 2)}, & \text { if } n \text { is odd } \\ \frac{1}{2}\left(x_{(n / 2)}+x_{(n / 2+1)}\right), & \text { if } n \text { is even }\end{cases}
$$

where $$\left\{x_{(1)}, x_{(2)}, \ldots, x_{(n)}\right\}=\left\{x_{1}, x_{2}, \ldots, x_{n}\right\}$$ and $$x_{(1)} \leq x_{(2)} \leq \cdots \leq x_{(n)}$$. Note that $$x_{(1)}, x_{(2)}, \ldots, x_{(n)}$$ are known as the order statistics. Note that when $$n$$ is even, any value in the interval $$\left[x_{(n / 2)}, x_{(n / 2+1)}\right]$$ is a sample median.

### Proposition

Given a sample of observations $$x_{1}, x_{2}, \ldots, x_{n}$$, with sample median $$m$$. Then, for any real value $$a$$,

$$
\min _{a}\left(\sum_{i=1}^{n}\left|x_{i}-a\right|\right)=\sum_{i=1}^{n}\left|x_{i}-m\right|
$$

### Definition (Quantile function)

Let the cumulative distribution function for the random variable $$X$$ be denoted by $$F_{X}$$. Then the function $$F_{X}^{-1}:(0,1) \rightarrow \mathbb{R}$$ is called the quantile function for the distribution $$X$$, for all $$p \in(0,1) F_{X}^{-1}(p)$$ is defined to be the smallest value $$x$$ such that $$F_{X}(x) \geq p$$.

### Definition (Lower and Upper Quantiles)

Given a quantile function $$F_{X}^{-1}$$ for a random variable $$X$$, the lower quartile is defined as $$q_{0.25}=F_{X}^{-1}(0.25)$$ while the upper quartile is defined as $$q_{0.75}=$$ $$F_{X}^{-1}(0.75)$$

### Definition (Interquartile Range)

 Given a quantile function $$F_{X}^{-1}$$ for a random variable $$X$$, the interquartile range is defined as IQR $$=F_{X}^{-1}(0.75)-F_{X}^{-1}(0.25)$$.

## Exploratory Data Analysis

### The bar chart

This provides a nice visual representation of the counts of the nominal data.
![](https://cdn.mathpix.com/cropped/2023_05_04_ad277764122c4c61e9f3g-044.jpg?height=388&width=464&top_left_y=1904&top_left_x=472)

### The pie chart

A variant of the bar chart for visualising discrete data is the pie chart which represents the data as proportions of a disc.

![](https://cdn.mathpix.com/cropped/2023_05_04_ad277764122c4c61e9f3g-045.jpg?height=750&width=1156&top_left_y=1341&top_left_x=234)

### The histogram

For continuous data, where data is measured to arbitrary precision and therefore almost every value is different, a bar chart is not suitable (the bar plot of $$n$$ values would be $$n$$ bars of height 1 , one for each different value).

However, a natural idea is to count values that are 'close together' as belonging to one category, and then let the $$x$$-axis indicate the value of the categories/bars. This is essentially the definition of a histogram.

![](https://cdn.mathpix.com/cropped/2023_05_04_ad277764122c4c61e9f3g-046.jpg?height=675&width=1391&top_left_y=1663&top_left_x=367)

### The line plot

There are situations when a set of observations is recorded in a particular order; such sequences of data are called time series, because the data are often a set of measurements which are recorded at certain times. In these situations, it is important to visualise these measurements in the relevant order and we plot the data so that the $$x$$-axis is time, and the $$y$$-axis is the value of the measurement. Although the measurements are recorded at discrete times, in order to indicate that the underlying process does still exist between the discrete measurements, we often choose to join up the individual points with line segments, creating a line plot.

![](https://cdn.mathpix.com/cropped/2023_05_04_ad277764122c4c61e9f3g-048.jpg?height=1188&width=1614&top_left_y=1132&top_left_x=232)

### The scatterplot

There are times when each data point consists of a collection of measurements.

![](https://cdn.mathpix.com/cropped/2023_05_04_ad277764122c4c61e9f3g-052.jpg?height=1496&width=1352&top_left_y=858&top_left_x=385)

### The Q-Q plot

The quantile-quantile plot or $$\mathbf{Q}-\mathbf{Q}$$ plot is a very useful plot that can be used to compare two probability distributions by plotting their quantiles against each other.
![](https://cdn.mathpix.com/cropped/2023_05_04_ad277764122c4c61e9f3g-054.jpg?height=586&width=1405&top_left_y=951&top_left_x=360)

### The Box plot

A box plot is graphical technique for visualising the distribution of a data set. It is particularly useful for visualising the spread of data and identifying values which can be considered outliers, where outliers are extreme values that are significantly different to the other data.
![](https://cdn.mathpix.com/cropped/2023_05_04_ad277764122c4c61e9f3g-059.jpg?height=853&width=1328&top_left_y=533&top_left_x=388)

## 3. Samples of Normal Random Variables

### Proposition

Suppose that $$X_{1}, X_{2}, \ldots, X_{n}$$ are independent random variables, and that for $$i \in\{1,2, \ldots, n\}, X_{i} \sim \mathrm{N}\left(\mu_{i}, \sigma_{i}^{2}\right)$$, where each $$\mu_{i}$$ and each $$\sigma_{i}$$ is finite. Then, defining $$Y=\sum_{i=1}^{n} X_{i}$$

$$
Y \sim \mathrm{N}\left(\mu, \sigma^{2}\right)
$$

where

$$
\mu=\sum_{i=1}^{n} \mu_{i}
$$

and

$$
\sigma^{2}=\sum_{i=1}^{n} \sigma_{i}^{2}
$$

### Corollary

Suppose $$X_{1}, X_{2}, \ldots, X_{n}$$ are i.i.d. random variables distributed according to $$\mathrm{N}\left(\mu, \sigma^{2}\right)$$. Then $$\bar{X}=\frac{1}{n} \sum_{i=1}^{n} X_{i} \sim \mathrm{N}\left(\mu, \frac{\sigma^{2}}{n}\right)$$.

### Proposition

Suppose that $$X_{1}, X_{2}, \ldots, X_{n}$$ are i.i.d. random variables distributed according to $$\mathrm{N}\left(\mu, \sigma^{2}\right)$$, with $$\bar{X}=\frac{1}{n} \sum_{i=1}^{n} X_{i}$$ and $$S^{2}=\frac{1}{n-1} \sum_{i=1}^{n}\left(X_{i}-\bar{X}\right)^{2}$$. Then $$\bar{X}$$ and $$S^{2}$$ are independent random variables and

$$
\frac{(n-1) S^{2}}{\sigma^{2}} \sim \chi_{n-1}^{2}
$$

### Confidence Intervals for normal random variables

#### Case 1: normal distribution with variance known

Suppose that the random variables $$X_{1}, X_{2}, \ldots, X_{n}$$ follow a normal distribution with unknown mean $$\theta$$ and known variance $$\sigma^{2}$$. Our goal is to obtain confidence interval for the unknown mean $$\theta$$. Suppose we wish to obtain a $$(1-\alpha)$$ confidence interval for some value $$\alpha$$. If we consider the sample mean

$$
\bar{X}=\frac{1}{n} \sum_{i=1}^{n} X_{i}
$$

we know from Corollary 3.1 .3 that

$$
\bar{X} \sim \mathrm{N}\left(\theta, \frac{\sigma^{2}}{n}\right)
$$

If one knew the value of $$\theta$$, then one could define $$Z$$ as

$$
Z=\frac{\theta-\bar{X}}{\sigma / \sqrt{n}} \sim \mathrm{N}(0,1)
$$

Using the cumulative distribution function $$F$$, we can find the value $$z_{\alpha / 2}$$ where

$$
\mathrm{P}\left(Z<z_{\alpha / 2}\right)=\mathrm{P}\left(Z \leq z_{\alpha / 2}\right)=\frac{\alpha}{2}
$$

(Recall that $$\mathrm{P}\left(Z<z_{\alpha / 2}\right)=\mathrm{P}\left(Z \leq z_{\alpha / 2}\right)$$ because the normal distribution is continuous and therefore $$\mathrm{P}\left(Z=z_{\alpha / 2}\right)=0$$.)

We can similarly find $$z_{1-\alpha / 2}$$, where

$$
\mathrm{P}\left(Z<z_{1-\alpha / 2}\right)=1-\frac{\alpha}{2} .
$$

(In fact, using the symmetry of the normal distribution, $$z_{1-\alpha / 2}=-z_{\alpha / 2}$$.) Then,

$$
\mathrm{P}\left(z_{\alpha / 2}<Z<z_{1-\alpha / 2}\right)=1-\alpha .
$$
Therefore, we can obtain a confidence interval for $$\theta$$ by manipulating this equation as follows:

$$
\begin{aligned}
& \mathrm{P}\left(z_{\alpha / 2}<Z<z_{1-\alpha / 2}\right)=1-\alpha . \\
\Rightarrow & \mathrm{P}\left(z_{\alpha / 2}<\frac{\theta-\bar{X}}{\sigma / \sqrt{n}}<z_{1-\alpha / 2}\right)=1-\alpha \\
\Rightarrow & \mathrm{P}\left(z_{\alpha / 2} \frac{\sigma}{\sqrt{n}}<\theta-\bar{X}<z_{1-\alpha / 2} \frac{\sigma}{\sqrt{n}}\right)=1-\alpha \\
\Rightarrow & \mathrm{P}\left(\bar{X}+z_{\alpha / 2} \frac{\sigma}{\sqrt{n}}<\theta<\bar{X}+z_{1-\alpha / 2} \frac{\sigma}{\sqrt{n}}\right)=1-\alpha \\
\Rightarrow & \mathrm{P}\left(\bar{X}-z_{1-\alpha / 2} \frac{\sigma}{\sqrt{n}}<\theta<\bar{X}+z_{1-\alpha / 2} \frac{\sigma}{\sqrt{n}}\right)=1-\alpha .
\end{aligned}
$$

#### Case 2: normal distribution with unknow variance known

Now suppose that the sample of random variables $$X_{1}, X_{2}, \ldots, X_{n}$$ can be assumed to follow a normal distribution with unknown mean $$\theta$$, but suppose further that the variance $$\sigma^{2}$$ is also unknown. While we would again be able to deduce that $$\bar{X} \sim \mathrm{N}\left(\theta, \frac{\sigma^{2}}{n}\right)$$, even if one knew the value of $$\theta$$, defining $$Z$$ as

$$
Z=\frac{\theta-\bar{X}}{\sigma / \sqrt{n}}
$$

would not be possible as before because $$\sigma^{2}$$ is unknown. One may consider replacing $$\sigma^{2}$$ with $$S^{2}$$, where

$$
S^{2}=\frac{1}{n-1} \sum_{i=1}^{n}\left(X_{i}-\bar{X}\right)^{2}
$$

and then defining

$$
T=\frac{\theta-\bar{X}}{S / \sqrt{n}}
$$

Proposition 3.4.1. Suppose that $$X_{1}, X_{2}, \ldots, X_{n}$$ are independent random variables that follow a $$\mathrm{N}\left(\mu, \sigma^{2}\right)$$ distribution, and $$\bar{X}=\frac{1}{n} \sum_{i=1} X_{i}$$ and $$S^{2}=\frac{1}{n-1}\left(\bar{X}-X_{i}\right)^{2}$$, as usual. Show that the random variable $$T$$, where

$$
T=\frac{\mu-\bar{X}}{S / \sqrt{n}}
$$

can be written in the form

$$
T=\frac{U}{\sqrt{V / p}}
$$

where

- $$U \sim \mathrm{N}(0,1)$$

- $$p=n-1$$

- $$V \sim \chi_{p}^{2}$$, the chi-squared distribution with $$p$$ degrees of freedom,

- $$U$$ and $$V$$ are independent random variables.

## 4. Hypothesis Testing

### Definition (Hypothesis)

A hypothesis is a statement about a parameter (or parameters) of interest.

### Definition (Null Hypothesis and Alternative Hypothesis)

In a given experiment, there will always be at least two competing hypotheses. The null hypothesis, denoted $$H_{0}$$, is the so-called default position, which specifies the conditions under which the experiment is assumed to have taken place. The alternative hypothesis, denoted $$H_{1}$$, is the hypothesis that is complementary to the null hypothesis. A hypothesis test uses data from the experiment to decide which of these two competing hypotheses is supported given the data.

### Definition (P-value)

Suppose the data $$\mathbf{x}$$ is observed, and the test statistic $$t(\mathbf{x})$$ is computed. Then the $$\boldsymbol{p}$$-value is the probability of obtaining a test statistic at least as extreme as $$t(\mathbf{x})$$ under the assumption that the null hypothesis $$H_{0}$$ is true.

### How to decide if the null hypothesis should be rejected? or How to decide if the $$p$$ value is small enough?

1. Whatever the value of $$p$$-value $$p$$, we declare after the experiment that the data provides evidence to reject the null hypothesis at significance level $$p$$.

2. Before conducting the experiment, one decides in advance which significance level one would require in order to reject the null hypothesis. Suppose it is decided that the null hypothesis would only be rejected if the $$p$$-value were less than a value $$\alpha$$. This value $$\alpha \in(0,1)$$ is sometimes called the significance threshold. Then in order to decide whether or not to reject the null hypothesis, we compare the $$p$$-value to $$\alpha$$. If the value of $$p$$ is computed and $$p<\alpha$$, then the null hypothesis is rejected at significance threshold $$\alpha$$. One may then be inclined to believe that the alternative hypothesis 'is true'. On the other hand, if $$p \nless \alpha$$, then the $$p$$-value is not extreme enough for the null hypothesis to be rejected. In this case, we fail to reject the null hypothesis.
 Suppose that $$\alpha$$ is the significance threshold, and $$p$$ is the computed $$p$$-value.

- If $$p<\alpha$$, then the null hypothesis is rejected, data supports the alternative hypothesis.$$H_{1}$$

- If $$p \nless \alpha$$. Then the null hypothesis fails to be rejected.


### Summary making decisions and statements about hypotheses

- We specify our null and alternative hypotheses in advance of the experiment.

- Our decision about the null hypothesis is based on data from an experiment.

- We never 'accept' a hypothesis as being true after analysing the data.

- We either reject or fail to reject the null hypothesis $$H_{0}$$.

- Failing to reject $$H_{0}$$ does not mean it is 'accepted'; the result of the experiment is inconclusive.

- If $$H_{0}$$ is rejected, we may say that the data supports the alternative hypothesis $$H_{1}$$.

### How to set up a hypothesis test?

1. Make the conclusion you wish the data to support the alternative hypothesis $$H_{1}$$.

2. Then make the opposite conclusion the null hypothesis $$H_{0}$$.

3. The null hypothesis then provides our assumptions for our random variables and the distribution of the test statistic.

### Test two-sided hypothesis

Suppose that, as described above, $$X_{1}, X_{2}, \ldots, X_{n} \stackrel{\text { i.i.d. }}{\sim} \mathrm{N}\left(\theta, \sigma^{2}\right)$$, where $$\theta$$ is unknown and $$\sigma^{2}$$ is known. Suppose we specify our null hypothesis $$H_{0}$$ and alternative hypothesis $$H_{1}$$ as

$$
\begin{aligned}
& H_{0}: \theta=\theta_{0}, \\
& H_{1}: \theta \neq \theta_{0} .
\end{aligned}
$$

If we assume the null hypothesis $$H_{0}$$ is true, then

$$
\begin{aligned}
& \mathrm{E}\left[X_{i}\right]=\theta=\theta_{0}, \quad \text { for } i=1,2, \ldots, n . \\
\Rightarrow & \mathrm{E}[\bar{X}]=\theta_{0} \\
\Rightarrow & \bar{X} \sim \mathrm{N}\left(\theta_{0}, \frac{\sigma^{2}}{n}\right) \\
\Rightarrow & Z=\frac{\theta_{0}-\bar{X}}{\sigma / \sqrt{n}} \sim \mathrm{N}(0,1) .
\end{aligned}
$$

Suppose the signifance level is specified as $$\alpha$$. Then, just as we derived the confidence interval in Section 3.3.1,

$$
\begin{aligned}
& \mathrm{P}\left(z_{\alpha / 2}<Z<z_{1-\alpha / 2}\right)=1-\alpha \\
\Rightarrow & \mathrm{P}\left(z_{\alpha / 2}<\frac{\theta_{0}-\bar{X}}{\sigma / \sqrt{n}}<z_{1-\alpha / 2}\right)=1-\alpha \\
\Rightarrow & \mathrm{P}\left(\bar{X}+z_{\alpha / 2} \frac{\sigma}{\sqrt{n}}<\theta_{0}<\bar{X}+z_{1-\alpha / 2} \frac{\sigma}{\sqrt{n}}\right)=1-\alpha .
\end{aligned}
$$

Then,

$$
\begin{aligned}
& \mathrm{P}\left(\theta_{0} \in\left(\bar{X}+z_{\alpha / 2} \frac{\sigma}{\sqrt{n}}, \bar{X}+z_{1-\alpha / 2} \frac{\sigma}{\sqrt{n}}\right)\right)=1-\alpha \\
\Rightarrow & \mathrm{P}\left(\theta_{0} \notin\left(\bar{X}+z_{\alpha / 2} \frac{\sigma}{\sqrt{n}}, \bar{X}+z_{1-\alpha / 2} \frac{\sigma}{\sqrt{n}}\right)\right)=\alpha
\end{aligned}
$$

Then, suppose that the random variables $$\mathbf{X}=\left(X_{1}, X_{2}, \ldots, X_{n}\right)$$ are observed as the data $$\mathbf{x}=\left(x_{1}, x_{2}, \ldots, x_{n}\right)$$, we can compute the sample mean $$\bar{x}$$ and then the realization of the interval as

$$
\left(\bar{x}+z_{\alpha / 2} \frac{\sigma}{\sqrt{n}}, \bar{x}+z_{1-\alpha / 2} \frac{\sigma}{\sqrt{n}}\right)
$$

If $$\theta_{0} \notin\left(\bar{x}+z_{\alpha / 2} \frac{\sigma}{\sqrt{n}}, \bar{x}+z_{1-\alpha / 2} \frac{\sigma}{\sqrt{n}},\right)$$, then the null hypothesis $$H_{0}$$ is rejected, because the probability of this occurring was considered, in some sense, to be less than $$\alpha$$.

Therefore, computing the $$(1-\alpha)$$-confidence interval allows us to decide whether or not to reject the null hypothesis.

### Computing the $$p$$-value

Our test statistic $$Z=\frac{\theta_{0}-\bar{X}}{\sigma / \sqrt{n}}$$ is assumed to follow a $$N(0,1)$$ distribution, and we would compute a 'p-value' as $$\widetilde{p}=1-F_{Z}(z)$$, where $$z=\frac{\theta_{0}-\bar{x}}{\sigma / \sqrt{n}}$$ is the realization of $$Z$$ after observing the data $$\mathbf{x}$$. Above we showed that $$\theta_{0} \notin\left(\bar{x}+z_{\alpha / 2} \frac{\sigma}{\sqrt{n}}, \bar{x}+z_{1-\alpha / 2} \frac{\sigma}{\sqrt{n}},\right)$$ will result in $$H_{0}$$ being rejected. We see that

$$
\theta_{0}<\bar{x}+z_{\alpha / 2} \frac{\sigma}{\sqrt{n}} \Rightarrow \frac{\theta_{0}-\bar{x}}{\sigma / \sqrt{n}}<z_{\alpha / 2} \Rightarrow z<z_{\alpha / 2}, \Rightarrow F_{Z}(z)<\frac{\alpha}{2} \Rightarrow 
$$

$$
\widetilde{p}=1-F_{Z}(z)>1-\frac{\alpha}{2}
$$

or

$$
\begin{aligned}
\theta_{0}>\bar{x}+z_{1-\alpha / 2} \frac{\sigma}{\sqrt{n}} \Rightarrow \frac{\theta_{0}-\bar{x}}{\sigma / \sqrt{n}}>z_{1-\alpha / 2} \Rightarrow z>z_{1-\alpha / 2} & \Rightarrow F_{Z}(z)>1-\frac{\alpha}{2} \\
& \Rightarrow \widetilde{p}=1-F_{Z}(z)<\frac{\alpha}{2}
\end{aligned}
$$

### Theorem (The random variabel as a Cumulative Distribution Function is uniformly distributed)

Let $$X$$ be a random variable with continous cumulative distribution function $$F_{X}$$, and let $$Y=F_{X}(X)$$. Then $$Y$$ is uniformly distributed on the interval $$[0,1]$$.

### Corollary ($$p$$-value is uniformly distributed)

Assuming the null hypothesis is true, a $$p$$-value based on a continuous test statistic follows a $$\operatorname{Unif}(0,1)$$ distribution.

### Definition (Type I error and Type II error)

- $$\text{Type I error}$$ : If the null hypothesis has been rejected, when in fact the null hypothesis is true, then we say a Type I error has occurred.
- $$\text{Type II error}$$ :If the null hypothesis fails to be rejected, when in fact the null hypothesis is false, then we say a Type II error has occurred.

### Definition (Power of a test)

The probability of correctly rejecting the null hypothesis, when in fact the null hypothesis is false, is defined as the power of the test, and is computed as $$\mathrm{P}$$ (Reject $$H_{0} \mid H_{0}$$ is false) $$=1-\beta$$, where $$\beta$$ is the probability of a Type II error occurring.

[![Screenshot-2023-05-04-at-21-57-57.png](https://i.postimg.cc/J4Gp3JdP/Screenshot-2023-05-04-at-21-57-57.png)](https://postimg.cc/9rHPC427)

### Definition (Student's two sample test)

#### Assumptions

- The two samples of random variables $$\mathbf{X}$$ and $$\mathbf{Y}$$ are independent and each follow a normal distribution.

- The means $$\theta_{1}$$ and $$\theta_{2}$$ of the two samples are unknown.

- The variances of the two samples are unknown but are assumed to be equal, i.e. $$\sigma_{1}^{2}=\sigma_{2}^{2}$$.
Define the null hypothesis $$H_{0}$$ and alternative hypothesis $$H_{1}$$ to be

$$
\begin{aligned}
& H_{0}: \theta_{1}=\theta_{2}, \\
& H_{1}: \theta_{1} \neq \theta_{2} .
\end{aligned}
$$

Then, since under the null hypothesis $$\theta_{1}-\theta_{2}=0$$, the $$t$$-statistic becomes

$$
T=\frac{\bar{X}-\bar{Y}}{S_{p} \sqrt{\frac{1}{n}+\frac{1}{m}}}
$$

where

$$
S_{X}^{2}=\frac{1}{n-1} \sum_{i=1}^{n}\left(X_{i}-\bar{X}\right)^{2}, \quad S_{Y}^{2}=\frac{1}{m-1} \sum_{j=1}^{m}\left(Y_{j}-\bar{Y}\right)^{2}
$$

$$
S_{p}^{2}=\frac{1}{n+m-2}\left((n-1) S_{X}^{2}+(m-1) S_{Y}^{2}\right),
$$

Compute the statistic

$$
t=\frac{\bar{x}-\bar{y}}{s_{p} \sqrt{\frac{1}{n}+\frac{1}{m}}}
$$

and from this statistic, which under the null hypothesis follows a $$\boldsymbol{t}$$-distribution with $$\boldsymbol{n}+\boldsymbol{m}-\mathbf{2}$$ degrees of freedom, we can compute a $$p$$-value.

- $$p$$-value $$<$$ $$\alpha$$, we would reject the null hypothesis at level $$\alpha$$. If $$T \sim t_{n+m-2}$$, then
$$
\mathrm{P}\left(|T| \leq t_{n+m-2,1-\alpha / 2}\right)=1-\alpha,
$$
so we would reject the null hypotheses if the realized statistic $$|t|>t_{n+m-2,1-\alpha / 2}$$.

- If the $$p$$-value is not significant and we fail to reject the null hypothesis it does not mean that $$\theta_{1}=\theta_{2}$$ ! In such a case, where we fail to reject the null hypothesis, we cannot make any conclusion.

## 5. Pitfalls in Statistics

### Correction for multiple hypothesis testing

#### Definition (Bonferroni correction)

If there are $$n$$ tests, and the nominal signficance threshold is $$\alpha$$, then one should use the adjusted significance threshold $$\alpha^{\prime}=\alpha / n$$. Then, if we let $$\widetilde{A}_{i}$$ be the event that $$p_{i}<\alpha / n$$, and $$\tilde{A}$$ be the event that at least one $$p_{i}$$ is less than $$\alpha / n$$, then

$$
\mathrm{P}(\tilde{A})=\mathrm{P}\left(\bigcup_{i=1}^{n} \widetilde{A}_{i}\right) \leq \sum_{i=1}^{n} \mathrm{P}\left(\tilde{A}_{i}\right)=\sum_{i=1}^{n} \frac{\alpha}{n}=n \cdot \frac{\alpha}{n}=\alpha .
$$

#### Theorem (Boole's inequality)

For a set of events $$A_{i}, i=1,2, \ldots n$$,

$$
\mathrm{P}\left(\bigcup_{i=1}^{n} A_{i}\right) \leq \sum_{i=1}^{n} \mathrm{P}\left(A_{i}\right)
$$

### Spurious correlations and causality

Correlation does not imply causation.

### Simpson's paradox

#### Definition (Simpson's paradox)

Simpson's paradox is a phenomenon that allows a statistical trend in groups of data to disappear or even reverse when these groups are combined.

### Anscombe's quartet

#### Definition (Anscombe's quartet)

Even if several data sets in graph look very different, they can have the same summary statistics, such as mean, variance, correlation, and linear regression line.

## 6. Covariance and Correlation

### Definition (Covariance)

The covariance of two random variables $$X$$ and $$Y$$, with means $$\mu_{X}$$ and $$\mu_{Y}$$, respectively, is the number defined by

$$
\operatorname{Cov}(X, Y)=\mathrm{E}\left[\left(X-\mu_{X}\right)\left(Y-\mu_{Y}\right)\right]
$$

### Remark

$$
\operatorname{Cov}(X, X)=\mathrm{E}\left[\left(X-\mu_{X}\right)^{2}\right]=\operatorname{Var}(X)
$$

$$
\operatorname{Cov}(Y, X)=\operatorname{Cov}(X, Y)
$$

$$
\operatorname{Var}(X+Y)=\operatorname{Var}(X)+\operatorname{Var}(Y)+2 \operatorname{Cov}(X, Y) .
$$

$$
\operatorname{Var}(a X+b Y)=a^{2} \operatorname{Var}(X)+b^{2} \operatorname{Var}(Y)+2 a b \operatorname{Cov}(X, Y) \text {. }
$$

$$
\mathrm{E}(a X+b Y)=a \mathrm{E}(X)+b \mathrm{E}(Y)=a \mu_{X}+b \mu_{Y}=\mu_{a X+b Y} .
$$

### Theorem

For any two random variables $$X$$ and $$Y$$, with variances $$\sigma_{X}^{2}$$ and $$\sigma_{Y}^{2}$$, respectively,

$$
|\operatorname{Cov}(X, Y)| \leq \sigma_{X} \sigma_{Y}
$$

### Definition (Simple covariance and observed simple covariance)

Suppose the random variables $$X_{1}, X_{2}, \ldots, X_{n}$$ follow distribution $$F_{X}$$, and the random variables $$Y_{1}, Y_{2}, \ldots, Y_{n}$$ follow distribution $$F_{Y}$$. Then the sample covariance is defined as

$$
\frac{1}{n-1} \sum_{i=1}^{n}\left(X_{i}-\bar{X}\right)\left(Y_{i}-\bar{Y}\right) .
$$

Suppose the random variables $$X_{1}, X_{2}, \ldots, X_{n}$$ are observed as $$x_{1}, x_{2}, \ldots, x_{n}$$, respectively, and the random variables $$Y_{1}, Y_{2}, \ldots, Y_{n}$$ are observed as $$y_{1}, y_{2}, \ldots, y_{n}$$, respectively. Then the observed sample covariance is defined as

$$
\frac{1}{n-1} \sum_{i=1}^{n}\left(x_{i}-\bar{x}\right)\left(y_{i}-\bar{y}\right) .
$$

### Definition (Correlation)

Definition 6.2. The correlation of the two random variables $$X$$ and $$Y$$, with variances $$\sigma_{X}^{2}$$ and $$\sigma_{Y}^{2}$$, respectively, is the number defined as

$$
\rho_{X Y}=\frac{\operatorname{Cov}(X, Y)}{\sigma_{X} \sigma_{Y}}
$$

### Corollary

For any random variables $$X$$ and $$Y$$,

$$
-1 \leq \rho_{X Y} \leq 1 .
$$

### Corollary

For any two random variables $$X$$ and $$Y$$

$$
|\rho_{X Y}\right|=1
$$

if and only if there exist numbers $$a \neq 0$$ and $$b$$ such that

$$
\mathrm{P}(Y=a X+b)=1
$$

If $$\rho_{X Y}=1$$, then $$a>0$$, and if $$\rho_{X Y}=-1$$, then $$a<0$$.

### Definition (Simple correlation and observed simple correlation)

Suppose the random variables $$X_{1}, X_{2}, \ldots, X_{n}$$ are observed as $$x_{1}, x_{2}, \ldots, x_{n}$$, respectively, and the random variables $$Y_{1}, Y_{2}, \ldots, Y_{n}$$ are observed as $$y_{1}, y_{2}, \ldots, y_{n}$$, respectively. Then the observed sample correlation is defined as

$$
r_{X Y}=\frac{\sum_{i=1}^{n}\left(x_{i}-\bar{x}\right)\left(y_{i}-\bar{y}\right)}{\sqrt{\sum_{i=1}^{n}\left(x_{i}-\bar{x}\right)^{2}} \sqrt{\sum_{i=1}^{n}\left(y_{i}-\bar{y}\right)^{2}}} .
$$

### Proposition

Suppose that the pairs of measurements $$\left(x_{1}, y_{1}\right),\left(x_{2}, y_{2}\right), \ldots,\left(x_{n}, y_{n}\right)$$ are observed. Define the pairs $$\left(u_{1}, v_{1}\right),\left(u_{2}, v_{2}\right), \ldots\left(u_{n}, v_{n}\right)$$ by

$$
u_{i}=a x_{i}+b, \quad v_{i}=c y_{i}+d, \quad i \in\{1,2, \ldots, n\}
$$

for some $$a, b, c, d \in \mathbb{R}$$ with $$a>0$$ and $$c>0$$. Then

$$
\begin{align*}
r_{X Y}&=\frac{\sum_{i=1}^{n}\left(x_{i}-\bar{x}\right)\left(y_{i}-\bar{y}\right)}{\sqrt{\sum_{i=1}^{n}\left(x_{i}-\bar{x}\right)^{2}} \sqrt{\sum_{i=1}^{n}\left(y_{i}-\bar{y}\right)^{2}}}\\
&=\frac{\sum_{i=1}^{n}\left(u_{i}-\bar{u}\right)\left(v_{i}-\bar{v}\right)}{\sqrt{\sum_{i=1}^{n}\left(u_{i}-\bar{u}\right)^{2}} \sqrt{\sum_{i=1}^{n}\left(v_{i}-\bar{v}\right)^{2}}}\\
&=r_{U V} .
\end{align*}
$$

## 7. Statistical models

### Definition (Realization)

Let $$\Omega$$ be the sample space for an experiment and let $$X$$ be a random variable defined on that sample space. Then for a particular elementary event $$\omega \in \Omega$$, the value $$x=X(\omega) \in \mathbb{R}$$ is called a realisation of the random variable $$X$$.
A realisation of $$x$$ of $$X$$ is also called an observation of $$X$$.

### Definition (Parameter space)

The space containing all possible values of the parameter $$\theta$$ is called the parameter space and is denoted by $$\Theta$$, i.e. $$\theta \in \Theta$$.

### Definition (Statistical model)

A statistical model consists of

1. an identification of random variables of interest (both observable and hypothetically observable),

2. a specification of a joint distribution or family of possible distributions for the observable random variables,

3. the identification of any parameter(s) $$\theta$$ of those distributions that are assumed unknown and possibly hypothetically observable,

4. (Bayesian model) a specification of a (joint) distribution for the unknown parameters.

## 8. Likelihood

### Definition (Likelihood function)

 Suppose we have a statistical model for the random variables $$\mathbf{X}$$ described by $$\left\{\mathrm{P}_{\theta} \mid \theta \in \Theta\right\}$$, and where each $$\mathrm{P}_{\theta}$$ is specified by the probability density function (or probability mass function) $$f_{\theta}$$. Having observed the data $$\mathbf{x}$$, the likelihood function $$L(\cdot \mid \mathbf{x}): \Theta \rightarrow \mathbb{R}$$ is defined by $$L(\theta \mid \mathbf{x})=f_{\theta}(\mathbf{x})$$ for any $$\theta \in \Theta$$.

### Definition (Likelihood)

For any $$\theta \in \Theta, L(\theta \mid \mathbf{x})$$ is called the likelihood of $$\theta$$ given the observed data $$\mathrm{x}$$.

#### Remark

$$
L(\theta \mid \mathbf{x})=f(\mathbf{x} \mid \theta)=\prod_{i=1}^{n} f\left(x_{i} \mid \theta\right)
$$

#### Definition (Likelihood ratios)

$$
\frac{L\left(\theta_{1} \mid \mathbf{x}\right)}{L\left(\theta_{2} \mid \mathbf{x}\right)}=\frac{\mathrm{P}_{\theta_{1}}(\mathbf{X}=\mathbf{x})}{\mathrm{P}_{\theta_{2}}(\mathbf{X}=\mathbf{x})}, \quad \theta_{1}, \theta_{2} \in \Theta, \quad \mathbf{X} \text { is discrete. }
$$

$$
\frac{L\left(\theta_{1} \mid x\right)}{L\left(\theta_{2} \mid x\right)} \approx \frac{\mathrm{P}_{\theta_{1}}(x-\delta<X<x+\delta)}{\mathrm{P}_{\theta_{2}}(x-\delta<X<x+\delta)}, \quad \theta_{1}, \theta_{2} \in \Theta, \quad X \text { is continuous. }
$$

### Definition (Equivalent likelihood functions)

Given the likelihood function $$L(\cdot \mid \mathbf{x})$$, any function $$L^{\prime}(\cdot \mid \mathbf{x})=c L(\cdot \mid \mathbf{x})$$ for $$c>0$$ is an equivalent likelihood function for the parameter $$\theta$$.

### Exercise

Show that
$$
\sum_{i=1}^{n}\left(x_{i}-\theta\right)^{2}=(n-1) s^{2}+n(\bar{x}-\theta)^{2}
$$

where $$\bar{x}$$ and $$s^{2}$$ are defined in terms of $$x_{1}, x_{2}, \ldots, x_{n}$$ as usual.

$$
\begin{aligned}
\sum_{i=1}^{n}\left(x_{i}-\theta\right)^{2} & =\sum_{i=1}^{n}\left(x_{i}-\bar{x}+\bar{x}-\theta\right)^{2} \\
& =\sum_{i=1}^{n}\left(x_{i}-\bar{x}\right)^{2}+2(\bar{x}-\theta) \sum_{i=1}^{n}\left(x_{i}-\bar{x}\right)+\sum_{i=1}^{n}(\bar{x}-\theta)^{2} \\
& =(n-1) s^{2}+2(\bar{x}-\theta) \cdot 0+n(\bar{x}-\theta)^{2}=(n-1) s^{2}+n(\bar{x}-\theta)^{2},
\end{aligned}
$$

since $$\sum_{i=1}^{n}\left(x_{i}-\bar{x}\right)=\sum_{i=1}^{n} x_{i}-\sum_{i=1}^{n} \bar{x}=n \bar{x}-n \bar{x}=0$$.

### Definition (Maximum likelihood estimate)

Suppose $$L(\theta \mid \mathbf{x})$$ is the likelihood of the parameter $$\theta$$ given the observed data $$\mathbf{x}$$. Then the parameter value $$\widehat{\theta}(\mathbf{x})$$ at which $$L(\theta \mid \mathbf{x})$$ attains its maximum as a function of $$\theta$$, with $$\mathbf{x}$$ held fixed, is called the maximum likelihood estimate of $$\theta$$.

### Definition (Maximum likelihood estimator)

If $$L(\theta \mid \mathbf{x})$$ is the likelihood of the parameter $$\theta$$, given the observed data $$\mathbf{x}$$, with maximum likelihood estimate $$\hat{\theta}(\mathbf{x})$$, then a maximum likelihood estimator of the parameter $$\theta$$ based on the random sample $$\mathbf{X}$$ is $$\widehat{\theta}(\mathbf{X})$$.

### The Log-Likelihood Function

$$
\theta_{1} \leq \theta_{2} \Rightarrow \log \left(\theta_{1}\right) \leq \log \left(\theta_{2}\right)
$$
Therefore, finding the value $$\widehat{\theta}$$ that maximises $$\log L(\theta \mid \mathbf{x})$$ is equivalent to finding the value that maximises $$L(\theta \mid \mathbf{x})$$. We call the transformation $$\log L(\theta \mid \mathbf{x})$$ the log-likelihood.

## 9. Simple Linear Regression

### Definition (Predictor and response variables)

If $$X$$ and $$Y$$ are quantities and r.v.s, then if $$Y=f(X)$$ then $$X$$ is the predictor and $$Y$$ is the response

### Definition (Residual)

If we have $$\hat{\beta}_{0}$$ and $$\hat{\beta}_{1}$$ which are the best estimates of $$\beta_{0}$$ and $$\beta_{1}$$, then the residuals $$\hat{e}_{i}$$ are $$\hat{e}_{i}=y_{i}-\left(\hat{\beta}_{0}+\hat{\beta}_{i} x_{i}\right)$$

### Definition (Residual sum of squares)

The residual sum of squares $$\mathbf{R S S}$$ is $$\sum_{i=1}^{n}\left(\hat{e}_{i}\right)^{2}$$. If we minimise the $$\mathbf{R S S}$$ then we have optimal estimates

### Solving the least squares problem

Given pairs of observations $$\left(x_{1}, y_{1}\right), \ldots,\left(x_{n}, y_{n}\right)$$ with $$\bar{x}=\frac{1}{n} \sum_{i=1}^{n} x_{i}$$ and $$\bar{y}=\frac{1}{n} \sum_{i=1}^{n} y_{i}$$ then:

- The sum of squares $$S_{x x}, S_{y y}$$ are $$S_{x x}=\sum_{i=1}^{n}\left(x_{i}-\bar{x}\right)^{2}$$ and $$S_{y y}=\sum_{i=1}^{n}\left(y_{i}-\bar{y}\right)^{2}$$

- The sum of cross products $$S_{x y}$$ is $$S_{x y}=\sum_{i=1}^{n}\left(x_{i}-\bar{x}\right)\left(y_{i}-\bar{y}\right)$$

- The residual sum of squares FUNCTION $$\operatorname{RSS}\left(\beta_{0}, \beta_{1}\right)$$ is $$\operatorname{RSS}\left(\beta_{0}, \beta_{1}\right)=\sum_{i=1}^{n}\left[y_{i}-\left(\beta_{0}+\beta_{1} x_{i}\right)\right]^{2}$$

The $$\beta_{0}$$ that minimises the sum of squares is $$\hat{\beta}_{0}=\bar{y}-\hat{\beta_{1}} \bar{x}=\bar{y}-\frac{S_{x y}}{S_{x x}} \bar{x}$$

The $$\beta_{1}$$ that minimises the sum of squares is $$\hat{\beta}_{1}=\frac{S_{x y}}{S_{x x}}$$

These apply if $$Y=F(X)$$

### Definition (Simple linear regression model)

For $$i \in$$ $$\{1,2, \ldots, n\}$$

$$
Y_{i}=\beta_{0}+\beta_{1} x_{i}+\epsilon_{i}
$$

where

- the $$x_{i}$$ are assumed to be fixed, known values (we have measured them),

- the parameters $$\beta_{0}, \beta_{1}$$ are fixed, unknown parameters,

- the $$\epsilon_{i}$$ are independent random variables,

-Assume $$\epsilon_{i} \sim \mathrm{N}\left(0, \sigma^{2}\right)$$, for some unknown $$\sigma^{2}$$.

The $$Y_{i}$$ are random variables, depending on the observed $$x_{i}$$ and the unobserved random errors $$\epsilon_{i}$$. In the experiment, the $$Y_{i}$$ are observed as $$y_{i}$$ for $$i \in\{1,2, \ldots, n\}$$.
$$
\begin{aligned}
\mathrm{E}\left(Y_{i}\right) & =\mathrm{E}\left(\beta_{0}+\beta_{1} x_{i}+\epsilon_{i}\right)=\beta_{0}+\beta_{1} x_{i}+\mathrm{E}\left(\epsilon_{i}\right)=\beta_{0}+\beta_{1} x_{i}+(0) \\
\Rightarrow \mathrm{E}\left(Y_{i}\right) & =\beta_{0}+\beta_{1} x_{i} \\
\operatorname{Var}\left(Y_{i}\right) & =\operatorname{Var}\left(\beta_{0}+\beta_{1} x_{i}+\epsilon_{i}\right)=\operatorname{Var}\left(\epsilon_{i}\right)=\sigma^{2} \\
\Rightarrow \operatorname{Var}\left(Y_{i}\right) & =\sigma^{2}
\end{aligned}
$$

$$
Y_{i} \sim \mathrm{N}\left(\beta_{0}+\beta_{1} x_{i}, \sigma^{2}\right)
$$
with the parameters $$\beta_{0}, \beta_{1}$$ and $$\sigma^{2}$$ unknown.

### Summary

Given the simple linear regression (conditional normal) model,

$$
Y_{i}=\beta_{0}+\beta_{1} x_{i}+\epsilon_{i}
$$

where the $$\epsilon_{i} \sim \mathrm{N}\left(0, \sigma^{2}\right)$$ and are independent, the maximum likelihood estimators for the parameters $$\beta_{0}, \beta_{1}$$ and $$\sigma^{2}$$ are

$$
\begin{aligned}
\widehat{\beta}_{0} & =\bar{y}-\left(\frac{S_{x y}}{S_{x x}}\right) \bar{x} \\
\widehat{\beta}_{1} & =\frac{S_{x y}}{S_{x x}} \\
\widehat{\sigma}^{2} & =\frac{1}{n}\left(\widehat{\mathrm{RSS}_{x y}}\right)=\frac{1}{n} \sum_{i=1}^{n}\left[y_{i}-\left(\widehat{\beta}_{0}+\widehat{\beta}_{1} x_{i}\right)\right]^{2} .
\end{aligned}
$$

### Remark

If our model is correct the residuals $$\widehat{\epsilon}_{i}$$, when plotted, should appear to be independently distributed according to some $$\mathrm{N}\left(0, \sigma^{2}\right)$$.

### Definition (The $$R^2$$ statistic)

 The statistic $$R^{2}$$ (pronounced 'R-squared') is defined as

$$
R^{2}=\frac{S_{yy}-\widehat{\mathrm{RSS}}_{x y} }{S_{y y}}
$$

### Remark

Interpreting the definition of $$R^{2}$$, it measures the difference between the sum of squares and the estimated residual sum of squares, normalised by the sum of squares.

As $$\widehat{\mathrm{RSS}}_{x y}=S_{y y}-\frac{\left(S_{x y}\right)^{2}}{S_{x x}}$$, then $$R^{2}=\frac{\left(S_{x y}^{2}\right)}{S_{x x} S_{y y}}=r_{X Y}^{2}$$, so $$R^{2} \in[0,1]$$

Sometimes the $$R^{2}$$ statistic is quoted as evidence that a model fits the data well. This usually happens when the $$R^{2}$$ statistic is close to 1 . While an $$R^{2}$$ value close to 1 does indicate that the fitted line is 'close' to the data, we must remember that it $$R^{2}$$ is only the square of the correlation. The next section explores this further. 

### Exercise

Show that

$$
\begin{aligned}
& \widehat{\mathrm{RSS}}_{x y}=S_{y y}-\frac{\left(S_{x y}\right)^{2}}{S_{x x}} \\
& \widehat{\mathrm{RSS}}_{x y}=\sum_{i=1}^{n}\left[y_{i}-\left(\widehat{\beta}_{0}+\widehat{\beta}_{1} x_{i}\right)\right]^{2} \\
& =\sum_{i=1}^{n}\left[y_{i}-\left(\bar{y}-\frac{S_{x y}}{S_{x x}} \bar{x}+\frac{S_{x y}}{S_{x x}} x_{i}\right)\right]^{2} \\
& =\sum_{i=1}^{n}\left[\left(y_{i}-\bar{y}\right)-\frac{S_{x y}}{S_{x x}}\left(x_{i}-\bar{x}\right)\right]^{2} \\
& =\sum_{i=1}^{n}\left[\left(y_{i}-\bar{y}\right)-2 \frac{S_{x y}}{S_{x x}}\left(x_{i}-\bar{x}\right)\left(y_{i}-\bar{y}\right)+\left(\frac{S_{x y}}{S_{x x}}\right)^{2}\left(x_{i}-\bar{x}\right)^{2}\right] \\
& =\sum_{i=1}^{n}\left(y_{i}-\bar{y}\right)^{2}-2 \frac{S_{x y}}{S_{x x}} \sum_{i=1}^{n}\left(x_{i}-\bar{x}\right)\left(y_{i}-\bar{y}\right)+\left(\frac{S_{x y}}{S_{x x}}\right)^{2} \sum_{i=1}^{n}\left(x_{i}-\bar{x}\right)^{2} \\
& =S_{y y}-2 \frac{S_{x y}}{S_{x x}} S_{x y}+\left(\frac{S_{x y}}{S_{x x}}\right)^{2} S_{x x} \\
& =S_{y y}-2 \frac{\left(S_{x y}\right)^{2}}{S_{x x}}+\left(\frac{\left(S_{x y}\right)^{2}}{S_{x x}}\right) \\
& =S_{y y}-\frac{\left(S_{x y}\right)^{2}}{S_{x x}}
\end{aligned}
$$

as required.

### Evaluating the fit of a model

Model 1 is more suitable as fitting the data well because its $$R^{2}$$ value is close to 1 . However, the residual plot for Model 1 has a ' $$\mathrm{U}$$ 'shape, and clearly shows that Model 1 does not fit the data well.

