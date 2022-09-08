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

