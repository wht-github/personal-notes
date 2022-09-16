# Signals and Systems

- $t$ denote continuous-time independent variable,use $()$
- $n$ denote the discrete-time independent variable, use $[]$

## Continuous-Time Complex Expoonential

$$x(t) = Ce^{at}$$

$C$ and $a$ are complex number

### Real Exponetial Signals

### Unit impluse & Unit Step Functinon

- unit impulse
$$\delta[n] =
\begin{cases}
    0,n \neq 0 \\
    1, n = 0
\end{cases}$$
- unit step
$$u[n] =
\begin{cases}
    0,n < 0 \\
    1, n \geq 0
\end{cases}$$

In particular, the discrete-time unit impulse is the first difference of the discrete-time step.
$$\delta[n] = u[n] + u[n-1]$$
$$u[n] = \Sigma^n_{m=-\inf}\delta[m]$$

unit impulse sample

continuous-time unit step

$$u(n) =
\begin{cases}
    0,n < 0 \\
    1, n > 0
\end{cases}$$

$$u(t) = \int_{-\infty}^{t}\delta(\tau)d\tau$$

$$\delta(t) = \lim_{\Delta \rarr 0}{\delta}_{\Delta}(t)$$

### System

*continuous-time system*, *discrete-time system*

#### Properties

#### Memoryless
a system is said to be *memoryless* if its output for each value of the independent variable at a given time is dependent only on the input at that same time

$$y(t) = x(t)$$

not *memoryless*
$$y[t] = x[t-1]$$

#### Invertibility and Inverse System
encoder & decoder

#### Causality
the value is not dependent on furture

#### Stability

not diverge

#### Time Inveriance
