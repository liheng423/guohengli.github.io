---
title: 'ODE Simple Recap'
date: 2025-03-09
permalink: /posts/2025/03/ode-recap-1/
tags:
  - ode
  - recap
---
### Disclaimer
> The content is a brief sum-up of *Elementray Differential Equations with Boundary Value Problems - C. Henry Edwards & David E. Penney*
> The book covers a toolkit for solving ODE.

## Fourier Series Methods
### Periodic Functions and Trigonometric Series (Look-back)

Orthogonal Functions
: Two functions are orthogonal on $[a, b]$ provided that
: $$
    \int_a^b u(t)v(t) \text{d}t=0
$$

:   Therefore,

:   $$
\int_{-\pi}^{\pi} \cos mt \cos nt \, dt = 
\begin{cases} 
0 & \text{if    } m \neq n, \\ 
\pi & \text{if  } m = n. 
\end{cases}
$$
:   $$
\int_{-\pi}^{\pi} \sin mt \sin nt \, dt = 
\begin{cases} 
0 & \text{if    } m \neq n, \\ 
\pi & \text{if  } m = n. 
\end{cases}
$$
:   $$
\int_{-\pi}^{\pi} \cos mt \sin nt \, dt = 0 \quad \text{for all } m \text{,} n.
$$

Based on this property, deriving the coefficients is easier:

$$
a_0=\frac{1}{\pi}=\int_{-\pi}^{\pi}f(t)dt\\
a_n=\frac{1}{\pi} \int_{-\pi}^{\pi} f(t) \cos(nt) \, dt\\
b_n = \frac{1}{\pi} \int_{-\pi}^{\pi} f(t) \sin(nt) \, dt
$$

Fourier Series and Fourier Coefficients
:   Let $ f(t) $ be a piecewise continuous function of period $ 2\pi $ that is defined for all $ t $. Then the Fourier series of $ f(t) $ is the series:

:   $$
f(t) = \frac{a_0}{2} + \sum_{n=1}^{\infty} (a_n \cos nt + b_n \sin nt)
$$

>*Why $a_0/2$*? 
> Because we follow the expression of $a_n$, whose derivation of $a_0/2$ includes $/2$

> Gibb's phenomenon
> the value of approximating curve tends to overshoot the limiting value of original function —either +1 or −1 in this case.

It can be verified that

$$
\int_{-\pi}^{\pi}f(t)dt=\int_{-a}^{a+2\pi}f(t)dt
$$

In case f (t) is given explicitly on the interval[0, 2$\pi$] rather than on [−$\pi$, $\pi$] (**This implies we could shift our bound anywhere we want.**)