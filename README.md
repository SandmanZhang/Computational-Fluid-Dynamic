# Numerical Method for Solving Conservative PDE System
## Project 1: Upwind Scheme for Solving 2D-Euler Equations System
### 1.1.Problem Statement
$$
\frac{\partial{\tilde{\rho}}}{\partial{t}} + \frac{\partial{\tilde{u}}}{\partial{x}} + \frac{\partial{\tilde{v}}}{\partial{y}} = 0
$$

$$
\frac{\partial{\tilde{u}}}{\partial{t}} + \frac{\partial{\tilde{\rho}}}{\partial{x}} = 0
$$

$$
\frac{\partial{\tilde{v}}}{\partial{t}} + \frac{\partial{\tilde{p}}}{\partial{y}} = 0
$$

$$
\frac{\partial{\tilde{p}}}{\partial{t}} + \gamma\frac{\partial{\tilde{u}}}{\partial{x}} + \gamma\frac{\partial{\tilde{v}}}{\partial{y}} = 0
$$

With Initial Condition:

$$
\tilde{u}(x,y,0)=\tilde{v}(x,y,0)=0, \forall (x,y)\in\Omega
$$

$$
\tilde{\rho}(x,y,0) = \tilde{p}(x,y,0)=\begin{cases}
    -1 & \text{if } (x,y) \in B \\
    0 & \text{if } (x,y) \in \Omega \\B
\end{cases} 
$$

Where $B=\\{(x,y)|(x-x_0)^2+(y-y_0)^2<=r^2\\},\rho_0>0$. The boundary conditions are:

$$
\tilde{u}(0,y,t)=\tilde{u}(1,y,t)=\tilde{v}(x,0,t)=\tilde{v}(x,1,t)=0
$$
### 1.2.Numerical Scheme and Result:
Please refer to PDF report in the file:Project 1

## Project 2: HLLC Solver for 1D-Euler Equations System with Riemann Problem & Woodward-Collela Blast Wave Problem

### 2.Problem Statement
  
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

### 2.1.Numerical Scheme and Result:
Please refer to PDF report in the file:Project 2







