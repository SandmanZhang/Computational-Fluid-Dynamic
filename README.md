


## Project 2: HLLC Solver for 1D-Euler Equations System with Riemann Problem & Woodward-Collela Blast Wave Problem

### Problem Statement
<div style="text-align: left;">
  
$$
\frac{\partial{\rho}}{\partial{t}} + \frac{\partial{(\rho u)}}{\partial{x}}=0
$$

$$
\frac{\partial{(\rho u)}}{\partial{t}} + \frac{\partial{(\rho u^2 + p)}}{\partial{x}}=0
$$

$$
\frac{\partial{(\rho v)}}{\partial{t}} + \frac{\partial{(\rho uv)}}{\partial{x}}=0
$$

$$
\frac{\partial{e}}{\partial{t}} + \frac{\partial{u(e + p)}}{\partial{x}}=0
$$

#### (1) Riemann Problem Boundary
$$
p(x,0) = 1
\quad
u(x,0) = 0
\quad
v(x,0) = \begin{cases}
    -1 & \text{if } x > 0 \\
    1 & \text{if } x < 0
\end{cases} 
\quad
\rho(x,0) = \begin{cases}
    -1 & \text{if } x > 0 \\
    1 & \text{if } x < 0
\end{cases}
$$

#### (2) Woodward-Collela Blast Wave Problem
$$
\rho(x,0) = 1
\quad
u(x,0) = 0
\quad
p(x,0) = \begin{cases}
    1000 & \text{if } x \in (0,0.1) \\
    0.01 & \text{if } x \in (0.1,0.9)\\
    100 & \text{if } x \in (0.9,1.0)
\end{cases} 
\quad
v(x,0) = \begin{cases}
    -10 & \text{if } x \in (0,0.5) \\
    20 & \text{if } x \in (0.5,1.0)
\end{cases}
$$

With reflective boundary condition:

$$
u(0,t)=u(1,t)=0
$$







