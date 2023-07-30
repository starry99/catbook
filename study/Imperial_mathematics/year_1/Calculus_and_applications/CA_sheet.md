---
layout: simple
title: Calculus and Application Memory Sheet
---

#### Based on the lectures and notes of [Prof. Demetrios Papageorgiou](https://www.imperial.ac.uk/people/d.papageorgiou) and [Dr. Vahid Shahrezaei](https://www.imperial.ac.uk/people/v.shahrezaei).
## 1. Differentiation

### Mean Value and Intermediate Theorem


-  Let $$f$$ be a function which is defined and differentiable on the open interval $$(a, b)$$. Let $$c$$ be a number in the interval which is a maximum for the function.Then $$f^{\prime}(c)=0$$. $$f^{\prime}(c)=0$$ also, if $$c$$ is a minimum of $$f$$.
- Let $$f(x)$$ be continuous over the closed interval $$a \leq x \leq b$$ and differentiable on the open interval $$a<x<b$$. Assume also that $$f(a)=f(b)$$.
 Then there exists a point $$c, a<c<b$$, such that $$f^{\prime}(c)=0$$
- (The Mean Value Theorem)
Suppose $$f$$ is continuous on $$[a, b]$$ and differentiable on $$(a, b)$$. Then there exists $$a<c<b$$ such that

$$
f^{\prime}(c)=\frac{f(b)-f(a)}{b-a}
$$

- (Intermediate Value Theorem)
  Let $$f$$ be continuous on the closed interval $$a \leq x \leq b$$. Given any number $$y^{*}$$ between $$f(a)$$ and $$f(b)$$, there exists a point $$x^{*}$$ between $$a$$ and $$b$$ such that $$f\left(x^{*}\right)=$$ $$y^{*}$$.

### Some special derivatives

$$
\frac{d}{d x} \log_a(x) =\frac{1}{x \log(a)}\\
\frac{d}{d x} \tan(x) =\sec^2(x)\\
\frac{d}{d x} \cot(x) =-\csc^2(x)\\
\frac{d}{d x} \sec(x) =\sec(x) \tan(x)\\
\frac{d}{d x} \csc(x) =-\csc(x) \cot(x)\\
\frac{d}{d x} \sin^{-1}(x) =\frac{1}{\sqrt{1-x^2}}\\
\frac{d}{d x} \cos^{-1}(x) =-\frac{1}{\sqrt{1-x^2}}\\
\frac{d}{d x} \tan^{-1}(x) =\frac{1}{1+x^2}\\
\frac{d}{dx} \cot^{-1}{-1}(x) = -\frac{1}{1+x^2}\\
\frac{d}{d x} \csc^{-1}(x) =-\frac{1}{|x| \sqrt{x^2-1}}\\
\frac{d}{d x} sec^{-1}(x) =\frac{1}{|x| \sqrt{x^2-1}}\\
\frac{d}{d x} \sinh(x) =\cosh(x)\\
\frac{d}{d x} \cosh(x) =\sinh(x)\\
\frac{d}{d x} \tanh(x) =\operatorname{sech}^2(x)\\
\frac{d}{d x} \operatorname{sech}(x) =-\operatorname{sech}(x) \tanh(x)\\
\frac{d}{dx} \operatorname{csch}(x) =-\operatorname{csch}(x) \coth(x)\\
\frac{d}{d x} \coth(x) =-\operatorname{csch}^2(x)\\
\frac{d}{d x} \operatorname{sinh^{-1}}(x) =\frac{1}{\sqrt{x^2+1}}\\
\frac{d}{d x} \operatorname{cosh^{-1}}(x) =\frac{1}{\sqrt{x^2-1}}\\
\frac{d}{d x} \operatorname{tanh^{-1}}(x) =\frac{1}{1-x^2}\\
\frac{d}{d x} \operatorname{coth^{-1}}(x) =\frac{1}{1-x^2}\\
\frac{d}{d x} \operatorname{sech^{-1}}(x) =-\frac{1}{x \sqrt{1-x^2}}\\
\frac{d}{d x} \operatorname{csch^{-1}}(x) =-\frac{1}{|x| \sqrt{x^2+1}}\\
$$

## 2. Integration

### Techniques of Integration

#### Some trigonometric formulas

$$
\begin{aligned}
&\cos (2 x)  =2 \cos ^{2}(x)-1=1-2 \sin ^{2}(x) \\
&\sin (2 x)  =2 \sin (x) \cos (x) \\
&\sin (x \pm y)  =\sin (x) \cos (y) \pm \cos (x) \sin (y) \\
&\cos (x \pm y)  =\cos (x) \cos (y) \mp \sin (x) \sin (y) \\
&\sin (x) \cos (y)  =\frac{1}{2}[\sin (x+y)+\sin (x-y)] \\
&\sin (x) \sin (y)  =\frac{1}{2}[\cos (x-y)-\cos (x+y)] \\
&\cos (x) \cos (y)  =\frac{1}{2}[\cos (x+y)+\cos (x-y)]\\
&\tan(x)^2+1=\sec(x)^2\\
&\cot(x)^2+1=\csc(x)^2\\
&\cosh (x)  =\frac{e^{x}+e^{-x}}{2} \\
&\sinh (x)  =\frac{e^{x}-e^{-x}}{2} \\
&\cosh ^{2}(x)-\sinh ^{2}(x)  =1 \\
&\cosh (x+y)  =\cosh (x) \cosh (y)+\sinh (x) \sinh (y) \\
&\sinh (x+y) =\sinh (x) \cosh (y)+\cosh (x) \sinh (y) \\
&\sinh (2 x)  =2 \sinh (x) \cosh (x) \\
&\cosh (2 x)  =2 \cosh ^{2}(x)-1=1+2 \sinh ^{2}(x) \\
\end{aligned}
$$

#### Trigonometric substitution

(1) If $$\sqrt{a^{2}-x^{2}}$$ appears in an integral, $$\operatorname{try} x=a \sin (\theta), \mathrm{d} x=a \cos (\theta) \mathrm{d} \theta, \sqrt{a^{2}-x^{2}}=$$ $$a \cos (\theta)(a>0, \theta$$ acute $$)$$.

(2) If $$\sqrt{x^{2}-a^{2}}$$ occurs, $$\operatorname{try} x=a \sec (\theta), \mathrm{d} x=a \tan (\theta) \sec (\theta) \mathrm{d} \theta$$ and $$\sqrt{x^{2}-a^{2}}=$$ $$a \tan (\theta)$$.

(3) If $$\sqrt{a^{2}+x^{2}}$$ or $$a^{2}+x^{2}$$ occur, $$\operatorname{try} x=a \tan (\theta), \mathrm{d} x=a \sec ^{2}(\theta) \mathrm{d} \theta, \sqrt{a^{2}+x^{2}}=$$ $$a \sec (\theta)$$. Also $$x=a \sinh (\theta), \mathrm{d} x=a \cosh (\theta) \mathrm{d} \theta, \sqrt{a^{2}+x^{2}}=a \cosh (\theta)$$.

#### Trigonometric integrals

$$
\int \sin ^{m}(x) \cos ^{n}(x) \mathrm{d} x \quad m, n \text { integers }
$$

For:

- $$n=1 \quad$$ substitute $$u=\sin (x) \Rightarrow \int \sin ^{m}(x) \cos (x) \mathrm{d} x=\int u^{m} \mathrm{~d} u$$
- $$n=1, m=-1 \quad \int \frac{\cos (x)}{\sin (x)} \mathrm{d} x=\log |\sin (x)|+c$$
- $$m, n \neq 1 \quad$$ Write in terms of $$\sin ^{p}(x) \cos (x)$$ or similar, or use double angle formulae Important - use trig formulas! - a reminder of double angle formulas.

#### Recursion formulas

$$
\begin{aligned}
\text { Let } I_{n} & =\int \sin ^{n}(x) \mathrm{d} x \\
\text { Then } I_{n} & =-\frac{1}{n} \sin ^{n-1}(x) \cos (x)+\frac{n-1}{n} I_{n-2}
\end{aligned}
$$

### Improper Integrals

#### Comparison Test

Suppose $$f$$ and $$g$$ satisfy:

(i) 
$$
 |f(x)| \leq g(x) 
$$

for all $$ x \geq a $$

(ii) $$\int_{a}^{b} f(x) \mathrm{d} x$$ and $$\int_{a}^{b} g(x) \mathrm{d} x$$ exist for every $$b>a$$.

Then

(a) If $$\int_{a}^{\infty} g(x) \mathrm{d} x$$ is convergent, so is $$\int_{a}^{\infty} f(x) \mathrm{d} x$$

(b) If $$\int_{a}^{\infty} f(x) \mathrm{d} x$$ is divergent, so is $$\int_{a}^{\infty} g(x) \mathrm{d} x$$

Similarly for $$\int_{-\infty}^{b} f(x) \mathrm{d} x$$ and $$\int_{-\infty}^{\infty} f(x) \mathrm{d} x$$.

#### Special improper integrals

$$
\int_{0}^{1} \frac{1}{x^{p}} \mathrm{~d} x\left\{\begin{array}{lll}
\text { converges } & \text { if } & p<1 \\
\text { diverges } & \text { if } & p \geq 1
\end{array}\right.
$$

### Mean Value Theorem and Intermediate Value Theorem for Integrals

- (Mean Value Theorem for Integrals)
 Let $$f$$ be continuous on $$[a, b]$$. Then there exists a point $$x_{0} \in(a, b)$$ such that

$$
f\left(x_{0}\right)=\frac{1}{b-a} \int_{a}^{b} f(x) \mathrm{d} x .
$$

- (Integral mean value theorem)
  Let $$f$$ and $$g$$ be continuous on $$[a, b]$$ with $$g(x) \geq 0$$ for $$x \in[a, b]$$. Then there exists a $$c$$ between $$a$$ and $$b$$ with

$$
\int_{a}^{b} f(x) g(x) d x=f(c) \int_{a}^{b} g(x) d x
$$

### Applications of Integrals

#### Length of a curve

$$
\begin{aligned}
\text { Total length } & =\lim _{n \rightarrow \infty,(h \rightarrow 0, \Delta x \rightarrow 0)} \sum \Delta x \sqrt{1+\left(\frac{f\left(x_{i}\right)-f\left(x_{i-1}\right)}{x_{i}-x_{i-1}}\right)^{2}} \\
L & =\int_{a}^{b}\sqrt{1+\left(f^{\prime}(x)\right)^{2}} \mathrm{~d} x
\end{aligned}
$$
$$
L=\int_{t_{0}}^{t_{1}}\sqrt{\left(\frac{\mathrm{d} x}{\mathrm{~d} t}\right)^{2}+\left(\frac{\mathrm{d} y}{\mathrm{~d} t}\right)^{2}} \mathrm{~d} t
$$

#### Volume of Revolution

- Rotation about the x-axis
- 
$$
V=\int_{a}^{b} \pi(f(x))^{2} \mathrm{~d} x .
$$

- Rotation about the y-axis
  
$$
\begin{gathered}
\underbrace{2 \pi x}_{\text {(a) }} \overbrace{f(x)}^{(\mathrm{b})} \underbrace{\mathrm{d} x}_{\text {(c) }} \\
\Rightarrow V=\int_{a}^{b} 2 \pi x f(x) \mathrm{d} x .
\end{gathered}
$$

$$
V=\int_{c}^{d} \pi(f^{-1}(y))^{2} \mathrm{~d} y .
$$

#### Surface Area of Revolution

- Rotation about the x-axis
  
$$
S=\int_{a}^{b} 2 \pi f(x) \sqrt{1+\left(f^{\prime}(x)\right)^{2}} \mathrm{~d} x
$$

- Rotation about the y-axis
  
$$
S=\int_{c}^{d} 2 \pi y \sqrt{1+\left(f^{\prime}(y)\right)^{2}} \mathrm{~d} y
$$

#### Centre of Mass

$$
\bar{x}=\frac{\int_{a}^{b} x(f(x)-g(x)) \mathrm{d} x}{\int_{a}^{b}(f(x)-g(x)) \mathrm{d} x} \quad \bar{y}=\frac{\frac{1}{2} \int_{a}^{b}\left(f(x)^{2}-g(x)^{2}\right) \mathrm{d} x}{\int_{a}^{b}(f(x)-g(x)) \mathrm{d} x}
$$

#### Theorem of Pappus

Let $$R$$ be a region that lies on one side of a line $$l$$. $$A=$$ area of $$R$$
$$V=$$ Volume obtained by rotating about $$l$$
$$d=$$ distance travelled by the centre of mass when $$R$$ is rotated about $$l$$
Then $$V=A d$$

#### Length of curves and areas using polar coordinates

- Length of a curve
  
$$
\begin{aligned}
L & =\int_{\theta=\alpha}^{\beta}\left[\left(f^{\prime} \cos (\theta)-f \sin (\theta)\right)^{2}+\left(f^{\prime} \sin (\theta)+f \cos (\theta)\right)^{2}\right]^{1 / 2} \mathrm{~d} \theta \\
& =\int_{\alpha}^{\beta} \sqrt{\left(f^{\prime}(\theta)\right)^{2}+(f(\theta))^{2}} \mathrm{~d} \theta \\
& =\int_{\alpha}^{\beta}\left[\left(\frac{\mathrm{d} r}{\mathrm{~d} \theta}\right)^{2}+r^{2}\right]^{1 / 2} \mathrm{~d} \theta
\end{aligned}
$$

- Area
  
$$
\begin{aligned}
\Delta A & =\frac{1}{2}\left(f\left(\theta_{i}\right)\right)^{2} \Delta \theta_{i} \\
\Rightarrow A & =\frac{1}{2} \int_{\alpha}^{\beta} f(\theta)^{2} \mathrm{~d} \theta=\frac{1}{2} \int_{\alpha}^{\beta} r^{2} \mathrm{~d} \theta
\end{aligned}
$$

## Series

#### Convergence and Divergence

##### The integral test

Let $$f(x)$$ be a function which is defined for all $$x \geq 1$$, and is positive and decreasing. Then the series

$$
\sum_{n=1}^{\infty} f(n)
$$

converges if and only if the improper integral

$$
\int_{1}^{\infty} f(x) \mathrm{d} x
$$ converges.

### Taylor Series

- $$a_{n}  =\frac{f^{(n)}\left(x_{0}\right)}{n !}$$
- $$f(x)  =\sum_{n=0}^{\infty} \frac{f^{(n)}\left(x_{0}\right)}{n !}\left(x-x_{0}\right)^{n}$$
- Maclaurin series
  
$$
f(x)=\sum_{n=0}^{\infty} \frac{f^{(n)}(0)}{n !} x^{n}
$$

#### Taylor's Theorem

 Let $$f$$ be a function defined on a closed interval between two numbers $$x_{0}$$ and $$x$$. Assume that the function has $$n+1$$ derivatives on the interval and that they are all continuous. Then
 $$
\begin{aligned}
f(x)=f\left(x_{0}\right)+ & f^{\prime}\left(x_{0}\right)\left(x-x_{0}\right)+\frac{f^{(2)}\left(x_{0}\right)}{2 !}\left(x-x_{0}\right)+\ldots \\
& +\frac{f^{(n)}\left(x_{0}\right)}{n !}\left(x-x_{0}\right)^{n}+R_{n}
\end{aligned}
$$

- Remainder
  $$
R_{n}(x)=f(x)-\sum_{k=0}^{n} \frac{f^{(k)}\left(x_{0}\right)}{k !}\left(x-x_{0}\right)^{k}
$$
- Integral form of the remainder
$$
R_{n}=\int_{x_{0}}^{x} \frac{(x-t)^{n}}{n !} f^{(n+1)}(t) \mathrm{d} t
$$
- Lagrange form of the remainder
$$
R_{n}=\frac{f^{(n+1)}(c)}{(n+1) !} (x-x_0)^{n+1}
$$

where $$c$$ is between $$x_0$$ and $$x$$

#### Some important Taylor series

$$
\begin{aligned}
& \frac{1}{1-x}=\sum_{n=0}^{\infty} x^{n} \quad (-1,1)\\
& \frac{1}{1+x}=\sum_{n=0}^{\infty}(-1)^{n} x^{n} \quad (-1,1)\\
& e^{x}=\sum_{n=0}^{\infty} \frac{x^{n}}{n !} \quad (-\infty,+\infty) \\
& \sin x=\sum_{n=0}^{\infty} \frac{(-1)^{n} x^{2 n+1}}{(2 n+1) !}\quad (-\infty,+\infty)\\
& \cos x=\sum_{n=0}^{\infty} \frac{(-1)^{n} x^{2 n}}{(2 n) !}\quad (-\infty,+\infty)\\
& \log (1+x)=\sum_{n=1}^{\infty}(-1)^{n-1} \frac{x^{n}}{n}\quad (-\infty,+\infty)\\
& (1+x)^\alpha = \sum_{n=0}^\infty\tbinom{\alpha}{n}x^n = \sum_{n=0}^{\infty} \frac{\alpha(\alpha-1)\cdots(\alpha-n+1)}{n!}x^n \quad (-1,1)
\end{aligned}
$$

### Fourier Series

#### The Fourier series of a function $$f(x)$$ with period $$2 \pi$$

The Fourier series of a function $$f(x)$$ with period $$2 \pi$$ is
$$
f(x)=\frac{1}{2} a_{0}+\sum_{n=1}^{\infty}\left(a_{n} \cos (n x)+b_{n} \sin (n x)\right)
$$ where:

- $$a_{n}=\frac{1}{\pi} \int_{-\pi}^{\pi} f(x) \cos (n x) d x=0$$ if $$f(x)$$ is odd.
- $$b_{n}=\frac{1}{\pi} \int_{-\pi}^{\pi} f(x) \sin (n x) d x=0$$ if $$f(x)$$ is even.
Discontinuities are defined as $$f(x)=\frac{1}{2}\left[f\left(x^{+}\right)+f\left(x^{-}\right)\right]$$. If $$f(x)$$ is continuous at $$x$$, then $$f(x^{+})=f(x^{-})=f(x)$$.

#### Fourier series on 2-$$L$$ period

If $$f(x)$$ has period $$2 L$$, then
$$
f(x)=\frac{1}{2} a_{0}+\sum_{n=1}^{\infty}\left[a_{n} \cos \left(\frac{n \pi x}{L}\right)+b_{n} \sin \left(\frac{n \pi x}{L}\right)\right]
$$ where:

- $$a_{n}=\frac{1}{L} \int_{-L}^{L} f(x) \cos \left(\frac{n \pi x}{L}\right) d x=0$$ if $$f(x)$$ is odd.

- $$b_{n}=\frac{1}{L} \int_{-L}^{L} f(x) \sin \left(\frac{n \pi x}{L}\right) d x=0$$ if $$f(x)$$ is even.

#### Parseval's theorem

If $$f(x)$$ is represented by its Fourier series

$$
f(x)=\frac{1}{2} a_{0}+\sum_{n=1}^{\infty}+\sum_{n=1}^{\infty} a_{n} \cos (n x)+b_{n} \sin (n x), \quad-\pi \leq x \leq \pi
$$

then we have

$$
\frac{1}{\pi} \int_{-\pi}^{\pi} f^{2} \mathrm{~d} x=\frac{1}{2} a_{0}^{2}+\sum_{n=1}^{\infty}\left(a_{n}^{2}+b_{n}^{2}\right) .
$$

## 4. Fourier Transform

### Fourier Transform

If $$f(x)$$ is a function and $$\hat{f}(\omega)$$ is its Fourier transform, and they both decay at $$\pm \infty$$, then:

$$
f(x)=\frac{1}{2 \pi} \int_{-\infty}^{\infty} \hat{f}(\omega) e^{i \omega x} d \omega
$$
The inverse transform is
$$\hat{f}(\omega)=\int_{-\infty}^{\infty} f(x) e^{-i \omega x} d x
$$

- Cosine transform
  $$
\hat{f}_{c}(\omega)=\int_{0}^{\infty} f(x) \cos (\omega x) d x
$$
  If $$f(x)$$ is odd then $$\hat{f}(\omega)=-2 i \hat{f}_{s}(\omega)$$
- Sine transform
$$
\hat{f}_{s}(\omega)=\int_{0}^{\infty} f(x) \sin (\omega x) d x
$$
If $$f(x)$$ is even then $$\hat{f}(\omega)=2 \hat{f}_{c}(\omega)$$

### Properties of Fourier Transform

- $$\mathcal{F}\{a f(x)+b g(x)\}=a \hat{f}(\omega)+b \hat{g}(\omega)$$

- $$\mathcal{F}^{-1}\{a \hat{f}(\omega)+b \hat{g}(\omega)\}=a f(x)+b g(x)$$

- If $$a>0 ; \mathcal{F}\{f(a x)\}=\frac{1}{a} \hat{f}\left(\frac{\omega}{a}\right)$$

- $$\mathcal{F}\{f(-x)\}=\hat{f}(-\omega)$$

- (Shifted)
  $$\mathcal{F}\left\{f\left(x-x_{0}\right)\right\}=e^{-i \omega x_{0}}   \hat{f}(\omega)$$
 $$\mathcal{F}\left\{e^{i \omega_{0} x} f(x)\right\}=\hat{f}\left(\omega-\omega_{0}\right)$$

- (Symmetry Formula)
  $$\mathcal{F}\{\hat{f}(x)\}=2 \pi f(-\omega)$$

- $$\mathcal{F}\left\{\frac{d^{n} f}{d x^{n}}(x)\right\}=(i \omega)^{n} \hat{f}(\omega)$$

- $$\mathcal{F}\{x f(x)\}=i \frac{d \hat{f}}{d \omega}(\omega)$$
- If $$f(x)$$ is complex-valued and $$[f(x)]^{*}$$ is it complex conjugate, then:

$$
\mathcal{F}\left\{[f(x)]^{*}\right\}=[\hat{f}(-\omega)]^{*}
$$

There is also the Fourier sine $$\mathcal{F}_{s}\{f(x)\}$$ and Fourier cosine $$\mathcal{F}_{c}\{f(x)\}$$ transforms:

$$
\mathcal{F}_{s}\{f(x)\}=\int_{0}^{\infty} f(x) \cos (\omega x) d x ; \quad \mathcal{F}_{c}\{f(x)\}=\int_{0}^{\infty} f(x) \sin (\omega x) d x
$$

with properties:

- $$\mathcal{F}_{c}\left\{f^{\prime}(x)\right\}=-f(0)+\omega \hat{f}_{s}(\omega)$$

- $$\mathcal{F}_{s}\left\{f^{\prime}(x)\right\}=-\omega \hat{f}_{c}(\omega)$$

- $$\mathcal{F}_{c}\left\{f^{\prime \prime}(x)\right\}=-f^{\prime}(0)-\omega^{2} \hat{f}_{c}(\omega)$$

- $$\mathcal{F}_{s}\left\{f^{\prime \prime}(x)\right\}=\omega f(0)-\omega^{2} \hat{f}_{s}(\omega)$$

### Convolution

#### Definition (Convolution)

The convolution of two functions $$f(x)$$ and $$g(x)$$ is defined as

$$
f(x) *g(x)=\int_{-\infty}^{\infty} f(x-y) g(y) d y
$$

#### Theorem (Convolution Theorem)

$$
\text { If } f(x) * g(x)=\int_{-\infty}^{\infty} f(x-u) g(u) d u, \text { then } \mathcal{F}\{f * g\}=\hat{f}(\omega) \hat{g}(\omega)
$$
Besides,
$$
\mathcal{F}\{f g\}=\frac{1}{2 \pi} \hat{f}(\omega)* \hat{g}(\omega)
$$

### The Energy Theorem

If $$f(x)$$ is real-valued, then:

$$
\frac{1}{2 \pi} \int_{-\infty}^{\infty}|\hat{f}(\omega)| d \omega=\int_{-\infty}^{\infty}[f(x)]^{2} d x
$$

### The Dirac Delta Function

$$
\delta(x)=\left\{\begin{array}{ll}
0 & x \neq 0 \\
\infty & x=0
\end{array}  \quad \text { such that the area under it is } 1\right.
$$
$$
\delta(x)=\frac{1}{2\pi} \int_{-\infty}^{\infty} e^{\pm i \omega x} d \omega \rightarrow \delta(\omega-\omega_0)=\frac{1}{2 \pi} \int_{-\infty}^{\infty} e^{\pm i (\omega-\omega_0) x} d x
$$
The Dirac delta function has the following properties:

- $$
  \int_{-\infty}^{\infty} g(x) \delta(x) d x=g(0), \quad \int_{-\infty}^{\infty} g(x) \delta(x-a) d x=g(a)
$$
- $$f(x) \delta(x-x_0)=f(x_0) \delta(x-x_0)$$
- $$f(x) \delta(x)=f(0) \delta(x)$$
- $$\delta(a x)=\frac{1}{|a|} \delta(x)$$
- $$\delta^{\prime}(x)=-\delta^{\prime}(-x)$$
- $$\delta^{\prime}(a x)=-\frac{1}{|a|} \delta^{\prime}(x)$$
- x $$\delta'(x) = -\delta(x)$$
- $$\delta(-x)=\delta(x)$$

### Fourier Transform of some special functions

- $$\mathcal{F}\{e^{-a |x|}\} = \frac{2a}{a^2+\omega^2}$$
- $$ h(x) =\begin{cases} 1 & |x|<a \\ 0 & |x|>a \end{cases} \rightarrow \hat{h}(\omega) = \frac{2 \sin (a \omega)}{\omega}$$  

## 5. Ordinary Differential Equations

### First-Order ODEs

A first order ODE is linear if $$\frac{d y}{d x}+p(x) y=q(x)$$
we have solution:
$$y_{G S}\left(x ; C_{1}\right)=e^{-\int p(x) d x}\left[\int e^{\int p(x) d x} q(x) d x+\frac{C_{1}}{A}\right]$$

A first order ODE is Dimensionally Homogeneous if $$\frac{d y}{d x}=F\left(\frac{y}{x}\right)$$

We solve by letting $$\mathbf{u}=\frac{\mathbf{y}}{\mathbf{x}}$$. The ODE becomes $$u+x \frac{d u}{d x}=F(u)$$, and by solving this then $$y_{G S}=u_{G S}(x ; C) x$$

#### Bernoulli Equation

A first order ODE IS Bernoulli if $$\frac{d y}{d x}+p(x) y=q(x) y^{n}$$
We solve by changing the variables $$\mathbf{u}=\mathbf{y}^{\mathbf{1 - n}}$$, and the ODE becomes $$\frac{d u}{d x}+(1-n) u p(x)=(1-n) q(x)$$ and solving to get $$y_{G S}(x ; C)=u_{G S}^{\frac{1}{1-n}}$$

### Second-Order ODEs

$$u = \frac{dy}{dx}$$, transform the second order ODE into a first order ODE.

### Linear ODEs

#### Definition (Wronskian)

The Wronskian $$\mathbf{W}_{k \times k}\left[\left\{y_{i}(x)\right\}_{i=1}^{k}\right]$$ is the determinant of the Wronskian matrix $$W$$, which is

$$
W=\left(\begin{array}{cccc}
y_{1}(x) & y_{2}(x) & \ldots & y_{k}(x) \\
\frac{d y_{1}}{d x}(x) & \frac{d y_{2}}{d x}(x) & \cdots & \frac{d y_{k}}{d x}(x) \\
\vdots & \vdots & \ddots & \vdots \\
\frac{d^{k-1} y_{1}}{d x^{k-1}}(x) & \frac{d^{k-1} y_{2}}{d x^{k-1}}(x) & \frac{d^{k-1} y_{k}}{d x^{k-1}}(x) &
\end{array}\right)
$$

If $$\mathbf{W}_{k \times k}\left[\left\{y_{i}(x)\right\}_{i=1}^{k}\right] \neq 0$$, the set $$\left\{y_{i}(x)\right\}_{i=1}^{k}$$ is linearly independent

#### Eurler - Cauchy Equation

##### Definition (Euler - Cauchy Equation)

$$
\mathcal{L}[y]=\beta_k x^k \frac{d^k y}{d x^k}+\beta_{k-1} x^{k-1} \frac{d^{k-1} y}{d x^{k-1}}+\cdots+\beta_1 x \frac{d y}{d x}+\beta_0 y=f(x)
$$
Let $$ x = e^t $$, then
$$
x^k y^k = D(D-1)(D-2)...(D-k+1)y
$$

#### Use Fourier Transform to solve ODE

We use the property $$\mathcal{F}\left\{\frac{d^{n} f}{d x^{n}}\right\}=(i \omega)^{n} \hat{f}(\omega)$$ to solve linear ODEs.

### Qualitative Analysis of ODEs

#### Fixed Points and Stability

The asymptotic behaviour of $$\mathrm{y}(\mathrm{t})$$ is what happens as $$t \rightarrow \infty$$

$$\vec{y}^{*}$$ is a fixed point or equilibrium point of a system of 1st order ODEs if once $$\vec{y}\left(t_{0}\right)=\vec{y}^{*}$$ at some time $$t_{0}$$ then $$\forall t>t_{0}, \vec{y}(t)=\vec{y}^{*}$$. As the fixed point remains unchanged w.r.t time, at a fixed point we have that $$\left[\frac{d \vec{y}}{d t}\right]_{\vec{y}=\vec{y}^{*}}=0$$

A fixed point $$\vec{y}^{*}$$ s stability can be described in 3 ways:

- Lyapunov stable if $$\forall \epsilon>0, \exists \delta>0$$ such that if $$\left\|\vec{y}(0)-\vec{y}^{*}\right\|<\delta \Longrightarrow \forall t \geq 0,\left\|\vec{y}(t)-\vec{y}^{*}\right\|<\epsilon$$. In words it means that that points close to the fixed point don't blow up but also they don't approach the fixed point

- Asymptotically stable if it is Lyapunov stable and $$\exists \delta>0$$ such that if $$\left\|\vec{y}(0)-\vec{y}^{*}\right\|<\delta$$ then $$\lim _{t \rightarrow \infty}\left\|\vec{y}(t)-\vec{y}^{*}\right\|=0$$

- Asymptotically unstable otherwise

We can draw the solutions and their trajectory over time on a phase plane, where the arrows indicate which way the solution moves in as time grows

Solutions of ODEs are uniquely defined by initial conditions, except at singularities or fixed points. The phase plane cannot cross itself except at those points.

#### Drawing Phase Portraits of systems of 1st order ODEs

[![2real.jpg](https://i.postimg.cc/Fsyrtcnp/2real.jpg)](https://postimg.cc/MvG2Vcwf)
[![2repeated.jpg](https://i.postimg.cc/BbW0kQTR/2repeated.jpg)](https://postimg.cc/34ZVDhbZ)
[![noreal.jpg](https://i.postimg.cc/qq8TTVQq/noreal.jpg)](https://postimg.cc/XB7hfPR6)

#### Behaviour catalogue

[![IMG-0649.jpg](https://i.postimg.cc/sgVddW5Y/IMG-0649.jpg)](https://postimg.cc/mt667tXk)

### Bifurcations

#### Linear Systems

In linear systems, the bifurcations are related to changes in the stability of the system:

$$\forall i, \operatorname{Re}\left\{\lambda_{i}\right\} \leq 0 \leftrightarrow \exists i$$ s.t. $$\operatorname{Re}\left\{\lambda_{i}\right\}>0$$

#### Nonlinear Systems

We consider 1D non-linear systems, where $$y(t)$$ are trajectories on the real line, and there are 2 kinds of special points: Fixed points: $$\frac{d y^{*}}{d t}=f\left(y^{*}\right)=0$$ and Singularities: $$f\left(y_{\text {sing }}\right)$$ undefined.

We can group the bifurcation points into 3 main types:

- Points where the number and stability of the fixed points change are saddle-node bifurcations

- Points where the stability of the fixed points exchanges are transcritical bifurcations

- Points where the number of fixed points increases are supercritical pitchfork bifurcations, and points where the number of fixed points decreases are called subcritical pitchfork bifurcations

In 1D, oscillations cannot occur as we are flowing on the real line and thus cannot turn back (there are no dimensions to do so)

#### Linear Stability Analysis

If

$$
y=y^{*}+\epsilon
$$

where $$\epsilon$$ is a small perturbation from $$y^{*}$$
then

$$\frac{d y}{d t}=f(y)=\frac{d \epsilon}{d t}=f\left(y^{*}+\epsilon\right)=f\left(y^{*}\right)+\left.\epsilon_{d f}^{d y}\right|_{y=y^{*}}+
$$

HOT's, so we can approximate

$$
\frac{d y}{d t}=\frac{d \epsilon}{d t}=\left.\frac{d f}{d y}\right|_{y=y^{*}}
$$

so if
$$\left.\frac{d f}{d y}\right|_{y=y^{*}}>0
$$

then $$y^{*}$$ is unstable, and if

$$
\left.\frac{d f}{d y}\right|_{y=y^{*}}<0
$$

then $$y^{*}$$ is stable

## 6. Multivariable Calculus

### Total Derivative

The total derivative $$d f$$ of a function
$$
 f\left(x_{1}, \ldots, x_{n}\right) \textbf{ is } d f=\sum_{i=1}^{n} \frac{\partial f}{\partial x_{i}} d x_{i}=\frac{\partial f}{\partial x_{1}} d x_{1}+\frac{\partial f}{\partial x_{2}} d x_{2}+\cdots+\frac{\partial f}{\partial x_{n}} d x_{n}
$$

If $$u=u(x, y)$$ and $$x=x(t), y=y(t), t \in \mathbb{R}$$ then by the total derivative

$$
\frac{d u}{d t}=\left(\frac{\partial u}{\partial x}\right)_{y}\left(\frac{d x}{d t}\right)+\left(\frac{\partial u}{\partial y}\right)_{x}\left(\frac{d y}{d t}\right)
$$

If $$u=u(x, y)$$ and $$x=x(t), y=y(t), t \in \mathbb{R}$$ then by the total derivative

$$
\frac{d u}{d t}=\left(\frac{\partial u}{\partial x}\right)_{y}\left(\frac{d x}{d t}\right)+\left(\frac{\partial u}{\partial y}\right)_{x}\left(\frac{d y}{d t}\right)
$$

If $$u=\left(x_{1}, \ldots, x_{n}\right)$$ and $$x_{i}=x_{i}(t), t \in \mathbb{R} \forall i$$ then 

$$
\frac{d u}{d t}=\sum_{i=1}^{n}\left(\frac{\partial u}{\partial x_{i}}\right) \frac{d x_{i}}{d t}
$$

If $$h=h(x, y)$$ with $$x=x(u, v)$$ and $$y=y(u, v)$$ then using the total derivative,

$$
\left(\frac{\partial h}{\partial u}\right)_{v}=\left(\frac{\partial h}{\partial y}\right)_{x}\left(\frac{\partial y}{\partial u}\right)_{v}+\left(\frac{\partial h}{\partial x}\right)_{y}\left(\frac{\partial x}{\partial u}\right)_{v}
$$

and

$$\left(\frac{\partial h}{\partial v}\right)_{u}=\left(\frac{\partial h}{\partial y}\right)_{x}\left(\frac{\partial y}{\partial v}\right)_{u}+\left(\frac{\partial h}{\partial x}\right)_{y}\left(\frac{\partial x}{\partial v}\right)_{u}
$$

### Implicit Function

Functions of 2 variables $$f(x, y)$$ are in explicit form if they are of the form $$z=f(x, y)$$ and they are in implicit form if they are of the form $$F(x, y, z)=0$$

For functions of 2 variables in implicit form, $$F(x, y, z)=0$$, the following holds:

$$
\left(\frac{\partial z}{\partial x}\right)_{y}=-\frac{\left(\frac{\partial F}{\partial x}\right)_{y, z}}{\left(\frac{\partial F}{\partial z}\right)_{x, y}} \quad\left(\frac{\partial z}{\partial y}\right)_{x}=-\frac{\left(\frac{\partial F}{\partial y}\right)_{x, z}}{\left(\frac{\partial F}{\partial z}\right)_{x, y}}
$$

### Gradient

The gradient of a function $$f(x, y)$$ is

$$
 \nabla f=\left(\frac{\partial f}{\partial x}, \frac{\partial f}{\partial y}\right)
$$

### Taylor Series

If $$\vec{x}_{0}=\left(\begin{array}{l}x_{0} \\ y_{0}\end{array}\right), \overrightarrow{\Delta x}=\left(\begin{array}{c}\Delta x \\ \Delta y\end{array}\right)$$ and $$\vec{\nabla} f\left(\overrightarrow{x_{0}}\right)=\left(\begin{array}{c}\frac{\partial f}{\partial x} \\ \frac{\partial f}{\partial y}\end{array}\right)_{\overrightarrow{x_{0}}}$$, then the 2D Taylor expansion up to 2nd order is

$$
f\left(\vec{x}_{0}+\overrightarrow{\Delta x}\right)=f\left(\vec{x}_{0}\right)+\vec{\nabla} f\left(\vec{x}_{0}\right)^{T} \overrightarrow{\Delta x}+\frac{1}{2} \overrightarrow{\Delta x}^{T} H\left(\vec{x}_{0}\right) \overrightarrow{\Delta x}
$$

where 

$$
H\left(\vec{x}_{0}\right)
$$ 

is the Hessian matrix, defined as

#### Haessian Matrix

$$
H_{i j}\left(\vec{x}_{0}\right)=\left(\frac{\partial^{2} f}{\partial x_{i} \partial y_{j}}\right)_{\vec{x}_{0}}, \text { so } H\left(\vec{x}_{0}\right)=\left[\begin{array}{cc}
\left.\frac{\partial^{2} f}{\partial^{2} x}\right|_{\vec{x}_{0}} & \left.\frac{\partial^{2} f}{\partial x \partial y}\right|_{\vec{x}_{0}} \\
\left.\frac{\partial^{2} f}{\partial x \partial y}\right|_{\vec{x}_{0}} & \left.\frac{\partial^{2} f}{\partial^{2} y}\right|_{\vec{x}_{0}}
\end{array}\right]
$$

This generalises to $$n$$ dimensions.

### Change of Coordinates

If $$r=r(x, y)$$ and $$\theta=\theta(x, y)$$, then

$$
\left(\begin{array}{l}
d x \\
d y
\end{array}\right)=\left[\begin{array}{ll}
\left(\frac{\partial x}{\partial r}\right)_{\theta} & \left(\frac{\partial x}{\partial \theta}\right)_{r} \\
\left(\frac{\partial y}{\partial r}\right)_{\theta} & \left(\frac{\partial y}{\partial \theta}\right)_{r}
\end{array}\right]\left(\begin{array}{l}
d r \\
d \theta
\end{array}\right)
$$

### Exact ODEs

If the first order ODE $$\frac{d y}{d x}=-\frac{F(x, y)}{G(x, y)}=f(x, y)$$ satisfies $$\frac{\partial F}{\partial y}=\frac{\partial G}{\partial x}$$ (condition of integrability) then $$\exists u(x, y)$$ s.t. $$F=\left(\frac{\partial u}{\partial x}\right)_{y}, G=\left(\frac{\partial u}{\partial y}\right)_{x}$$ and $$u(x, y)=0$$ is a solution.

If the ODE is not exact, we can find an integrating factor $$\lambda(x)$$ or $$\lambda(y)$$ such that it becomes exact. If we have $$F(x, y) d x+G(x, y) d y=0$$ then we look for an integrating factor $$\lambda=\lambda(x)$$ or $$\lambda(y)$$ s.t. $$\lambda F(x, y) d x+\lambda G(x, y) d y=0$$ is exact.

### Sketching functions of 2 variables

To sketch functions in 2 variables, we do the following:

1. Check continuity and find singularities

2. Find asymptotic behaviour: $$\lim _{x, y \rightarrow \pm \infty} f(x, y)$$ and $$\lim_{\vec{x} \rightarrow \vec{x}_{\text {sing }}} f(x, y)$$

3. Obtain some level curves, e.g. $$f(\vec{x})=0$$ and find where $$f(\vec{x})>0$$ and $$f(\vec{x})<0$$

4. Find stationary points: minima, maxima and saddle points

If $$\vec{x}^{*}$$ is a stationary point, we can find out what type of stationary point it is using the eigenvalues of the Hessian matrix $$H\left(\vec{x}^{*}\right)$$ :

- If $$\lambda_{1}, \lambda_{2} \in \mathbb{R}^{+}$$, then $$\vec{x}^{*}$$ is a minimum

- If $$\lambda_{1}, \lambda_{2} \in \mathbb{R}^{-}$$, then $$\vec{x}^{*}$$ is a maximum

- If $$\lambda_{1} \in \mathbb{R}^{+}$$and $$\lambda_{2} \in \mathbb{R}^{-}$$or vice versa then $$\vec{x}^{*}$$ is a saddle point
