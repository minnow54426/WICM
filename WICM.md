# Introduction

BVPs can be written to a general form:
$$
T(x, y, \frac{dx}{dy}, \cdots, \frac{d^{n}y}{dx^{n}}) = 0, x \in [a, b]
$$
with corresponding boundary conditions, where T is a nonlinear operator and y is an unknown function of x.

# Wave approximation of multiple integrals

$$
{0} \cdots \subset V_0 \subset V_1 \subset \cdots \subset V_j \subset V_{j + 1} \subset  \cdots \subset L^2(R)
$$

orthogonal basis of the subspace $V_j$ :
$$
\phi_{j, k}(x) = 2^{\frac{j}{2}}\phi(2^jx - k)
$$
$\phi(x)$ is the so_called orthogonal scaling function.

$f(x) \in L^2(R)$ can be approximated by project this function from $L^2(R)$  to $V_j$ as :
$$
f(x) \approx P^jf(x) = \sum_{k} c_{j, k}\phi_{j, k}(x)
$$
where:
$$
c_{j, k} = \int_{-\infty}^{\infty}f(x)\phi_{j, k}(x)dx
$$

$$
\phi(x) = \sum_{k} p_k \phi(2x - k)  k = 0, 1, 2, \dots, 3N -1
$$

Such a scaling function has the unique property of shifted vanishing moments:
$$
\int_{-\infty}^{\infty}(t - M_1)^k\phi(t)dt = 0, 1 \leq k < N
$$
where 
$$
M_1 \triangleq \int_{-\infty}^{\infty}x\phi(x)dx = \sum _{k\in Z}p_kk/2
$$
is the first order moment of the scaling function.Then
$$
c_{j, k} \approx 2^{-j/2}f(\frac{k + M_1}{2^j})
$$
Then through $(3)$ we can obtain
$$
f(x) \approx P^jf(x) \approx \widetilde{P^j}f(x) = \sum_{k = -\infty}^{\infty}f_{M_1 + k}\phi(2^jx - k)
$$
where
$$
f_{M_1 + k} = f(x_{M_1 + k}),    x_{M_1 + k} = (M_1 + k)/2^j, f(x) = P^jf(x) = \widetilde{P^j}f(x)
$$
when $f(x)$ is any polynomial with an order up to $N -1$ , and 
$$
\Vert f(x) - \widetilde{P^j}f(x) \Vert_{L^2(R)} = O(2^{-jN})
$$
as long as 
$$
f(x) \in L^2(R) \cap C^N(R)
$$
If $f(x)$ is defined in $[0. 1]$, then  
$$
f(x) \approx \widetilde{P^j}f(x) = \sum_{k = 2- 3N}^{2^j -1}f_{k + M_1}\phi(2^jx - k)
$$
Define the n-tuple integral of the function f(x) as 
$$
f^{\int_{n}}(x) \triangleq \int_{0}^{x}\int_{0}^{\varepsilon_n}\cdots\int_{0}^{\epsilon_2}f(\varepsilon_1)d\varepsilon_1d\varepsilon_2\dots d\varepsilon_n
$$
Substituting $(14)$ to $(15)$, then 
$$
f^{\int_{n}}(x) \approx f^{\int_{n}}_{\widetilde{P^j}}(x) = \sum_{k = 2 - 3N}^{2^j - 1}f_{k + M_1}\phi^{\int_{n}}_{{j, k}}(x)
$$
where
$$
\phi^{\int_{n}}_{{j, k}}(x)  \triangleq\int_{0}^{x}\int_{0}^{\varepsilon_n}\cdots\int_{0}^{\epsilon_2}\phi(2^j\varepsilon_1 - k)d\varepsilon_1d\varepsilon_2\dots d\varepsilon_n
$$

$$
f^{\int_{n}}_{\widetilde{P^j}}(x) =\int_{0}^{x}\int_{0}^{\varepsilon_n}\cdots\int_{0}^{\epsilon_2}f^{\int_{n}}_{\widetilde{P^j}}(\varepsilon_1)d\varepsilon_1d\varepsilon_2\dots d\varepsilon_n
$$



# WICM

Assume that $x \in [0, 1]$ , and the boundary conditions located at the end points $ x = 0, 1.$Defining various derivatives of the unknown function $\frac{d^iy}{dx^i}$ as new functions $y_i$, converts $(1)$  into 
$$
\begin{cases}
T(x, y_0, y_1, \dots , y_n) = 0\\
y_0 = \int_{0}^{x}\int_{0}^{\varepsilon_n}\cdots\int_{0}^{\epsilon_2}y_n(\varepsilon_1)d\varepsilon_1d\varepsilon_2\dots d\varepsilon_n + \sum_{i = 0}^{n - 1}\frac{x^i}{i!}y_i(0)\\
y_1 = \int_{0}^{x}\int_{0}^{\varepsilon_{n - 1}}\cdots\int_{0}^{\epsilon_2}y_n(\varepsilon_1)d\varepsilon_1d\varepsilon_2\dots d\varepsilon_{n - 1} + \sum_{i = 1}^{n - 1}\frac{x^{i - 1}}{(i - 1)!}y_i(0)\\
\vdots\\
y_{n - 1} = \int_{0}^{x}y_nd\varepsilon + y_{n - 1}(0)
\end{cases}\\
x \in [0, 1]
$$
where $y_i(0)$ can be determined by the boundary conditions at the end points.

Approximate $y_n$ by
$$
y_n \approx \sum_{k = 0}^{2^j}y_n(\frac{k}{2^j})\phi_{j, k}(x)
$$
Substituting $(20)$ to $(19)$ leads to
$$
\begin{cases}
T(x, y_0, y_1, \dots , y_n) = 0\\
y_0(x) \approx \sum_{k = 0}^{2^j}y_{n, k}\phi_{j, k}^{\int_{n}}(x) + \sum_{i = 0}^{n - 1}\frac{x^i}{i!}y_i(0)\\
y_1(x) \approx \sum_{k = 0}^{2^j}y_{n, k}\phi_{j, k}^{\int_{n - 1}}(x) + \sum_{i = 1}^{n - 1}\frac{x^{i - 1}}{(i - 1)!}y_i(0)\\
\vdots \\
y_{n -1} \approx \sum_{k = 0}^{2^j}y_{n, k}\phi_{j, k}^{\int}(x) + y_{n - 1}(0)
\end{cases}
$$
Apply conventional collocation method to $(21)$ we obtain
$$
\begin{cases}
T(x_l, y_{0, l}, y_{1, l}, \dots , y_{n, l}) = 0\\
y_{0, l} \approx \sum_{k = 0}^{2^j}y_{n, k}\phi_{j, k}^{\int_{n}}(x_l) + \sum_{i = 0}^{n - 1}\frac{x_l^i}{i!}y_{i, 0}\\
y_{1, l} \approx \sum_{k = 0}^{2^j}y_{n, k}\phi_{j, k}^{\int_{n - 1}}(x_l) + \sum_{i = 1}^{n - 1}\frac{x_l^{i - 1}}{{i - 1}!}y_{i, 0}\\
\vdots \\
y_{n - 1, l}(x) \approx \sum_{k = 0}^{2^j}y_{n, k}\phi_{j, k}^{\int}(x_l) + y_{n - 1, 0}
\end{cases}
$$
where
$$
x_l = l/2^j and y_{i, l} = y_i(x_l), l = 0, 1, 2, \dots , 2^j.
$$


The boundary values of $y_i(0)$ can be determined from boundary conditions at other points.

The $(23)$ can be written into a matrix form as 
$$
T(x, A_ny_n + b_0, A_{n - 1}y_n + b_1, \dots , A_1y_n + b_{n - 1}) \approx 0
$$
where matrices and vectors are  
$$
A_i = \{a_{i, l, k} = \phi_{j, k}^{\int_{i}}(x_l)\}, b_i = \{b_{i, l} = \sum_{k = i}^{n - 1}x_l^k y_k(0)/i!\}, l, k = 0, 1, 2, \dots , 2^j
$$
Once $(24)$ is solved , then we can obtain $y_n(x_l)$ , the value of $y_i(x_l)$ can be achieved through the relation 
$$
y_i = A_{n - i}y_n + b_i
$$
The WICM can be easily extended to solve high dimensional nonlinear BVPs.

# Numerical examples

## Problem1(Bratu Equation)

$$
\frac{d^2u}{dx^2} + \lambda e^{u(x)} = 0, u(0) = u(1) = 0
$$

Define $u_2 = d^2u/dx^2$, then through $(19)$ we can obtain 
$$
u(x) = \int_{0}^{x}\int_{0}^{\varepsilon_2}u_2(\varepsilon_1)d\varepsilon_1d\varepsilon_2 + xu_1(0) + u(0)
$$
Because $u(0) = u(1) = 0$, we can obtain
$$
\begin{cases}
u(0) = \int_{0}^{0}\int_{0}^{\varepsilon_2}u_2(\varepsilon_1)d\varepsilon_1d\varepsilon_2 + 0u_1(0) + u(0) = 0\\
u(1) = u(x) = \int_{0}^{1}\int_{0}^{\varepsilon_2}u_2(\varepsilon_1)d\varepsilon_1d\varepsilon_2 + u_1(0) + u(0)
\end{cases}
$$
then we can get
$$
\begin{cases}
u(0) = 0\\
u_1(0) = -\int_{0}^{1}\int_{0}^{\varepsilon_2}u_2(\varepsilon_1)d\varepsilon_1d\varepsilon_2
\end{cases}
$$
Replace $\varepsilon_2$ with $\varepsilon$, we can get
$$
u(x) = \int_{0}^{x}\int_{0}^{\varepsilon}u_2(\varepsilon_1)d\varepsilon_1d\varepsilon - x\int_{0}^{1}\int_{0}^{\varepsilon}u_2(\varepsilon_1)d\varepsilon_1d\varepsilon
$$
Then $(27)$ is transformed into 
$$
\begin{cases}
u_2(x) + \lambda e^{u(x)} = 0\\
u_1(x) = \int_{0}^{x}u_2(\varepsilon)d\varepsilon + \int_{0}^{1}\int_{0}^{\varepsilon}u_2(\varepsilon_1)d\varepsilon_1d\varepsilon\\
u(x) = \int_{0}^{x}\int_{0}^{\varepsilon}u_2(\varepsilon_1)d\varepsilon_1d\varepsilon - x\int_{0}^{1}\int_{0}^{\varepsilon}u_2(\varepsilon_1)d\varepsilon_1d\varepsilon
\end{cases}
$$
For a function $f(\cdot)$ and a vector $x = \{x_k\}$, by defining $f \cdot(x) \triangleq \{f(x_k)\}$, then $(32)$ can be discretized into algebraic equations by the prospered WICM. 

From $(22)$ we can obtain that 
$$
\begin{align}
\begin{split}
u_{0, l} &= \sum_{k = 0}^{2^j}u_{2, k}\phi_{j, k}^{\int_2}(x_l) + \sum_{i = 0}^{n - 1}\frac{x_l^i}{i!}u_{i, 0}\\
& = \sum_{k = 0}^{2^j}u_{2, k}\phi_{j, k}^{\int_2}(x_l) + u_{0, 0} + x_lu_{1, 0}\\ 
& = \sum_{k = 0}^{2^j}u_{2, k}\phi_{j, k}^{\int_2}(x_l) - x_0\int_{0}^{1}\int_{0}^{\varepsilon}u_2(\varepsilon_1)d\varepsilon_1d\varepsilon + \int_{0}^{1}\int_{0}^{\varepsilon}u_2(\varepsilon_1)d\varepsilon_1d\varepsilon \\
& = \sum_{k = 0}^{2^j}u_{2, k}\phi_{j, k}^{\int_2}(x_l) - x_l\sum_{k = 0}^{2^j}u_{2, k}\phi_{j, k}^{\int_2}(1) \\
& = \sum_{k = 0}^{2^j}u_{2}(x_k)\phi_{j, k}^{\int_2}(x_l) - x_l\sum_{k = 0}^{2^j}u_{2}(x_k)\phi_{j, k}^{\int_2}(1) \\
\end{split}
\end{align}
$$


 Let 
$$
u_2  = \{u_2(x_k), x_k = \frac{k}{2^j}\}, A_2 = \{a_{2, k, l} = \phi_{j, k}^{\int_{2}}(x_l) - x_l\phi_{j, k}^{\int_{2}}(1)\}
$$
Then $(32)$ can be changed into 
$$
u_2 + \lambda e\cdot^{A_2u_2} \approx 0
$$
Once $u_2$ is obtained from $(35)$, then nodal values of the unknown function can be obtained by $u = A_2u_2$.

## Problem2(Nonlinear Fourth-order Differential Equation)

$$
\begin{cases}
u^{(4)}(x) - e^xu''(x) + u(x) + sin(u(x)) = f(x), 0 < x < 1\\
f(x ) = 1 + sin(1 + sinh(x)) - (e^x - 2)sinh(x)\\
u(0) =1, u'(0) = 1\\
u(1) = 1 + sinh(1), u'(1) = cosh(1).
\end{cases}
$$

where
$$
sinh(x) = \frac{e^x - e^{-x}}{2} , cosh(x) = \frac{e^x + e^{-x}}{2}
$$

Defining $u_4 = \frac{d^4u}{dx^4}$, then through $(19)$ we can obtain that
$$
\begin{align}
\begin{split}
u(x) & = \int_{0}^{x}\int_{0}^{\varepsilon_4}\int_{0}^{\varepsilon_3}\int_{0}^{\varepsilon_2}u_4(\varepsilon_1)d\varepsilon_1d\varepsilon_2d\varepsilon_3d\varepsilon_4 + \sum_{i = 0}^{3}\frac{x^i}{i!}u_i(0)\\
& = u_4^{\int_4}(x) + 1 + xu_1(0) + \frac{x^2}{2}u_2(0) + \frac{x^3}{6}u_3(0)
\end{split}
\end{align}
$$
And
$$
u'(x) = u_4^{\int_3}(x) + u_1(0) + xu_2(0) + \frac{x^2}{2}u_3(0)
$$

From the boundary conditions we can obtain
$$
\begin{cases}
u(0) = u_4^{\int_4}(0) + 1 = 0 + 1 = 1 \\
u'(0) = u_4^{\int_3}(0) + u_1(0) = 0 + 1 = 1 \\
u(1) = u_4^{\int_4}(1) + 1 + u_1(0) + \frac{1}{2}u_2(0) + \frac{1}{6}u_3(0) \\
u'(1) = u_4^{\int_3}(1) + u_1(0) + u_2(0) + \frac{1}{2}u_3(0)
\end{cases}
$$

Then we can obtain that
$$
\begin{cases}
u_2(0) = 6u(1) - 2u'(1) -6u_4^{\int_4}(1) + 2u_4^{\int_3}(1) - 6u(0) - 4u'(0) \\
u_3(0) = -12u(1) + 6u'(1) + 12u_4^{\int_4}(1) - 6u_4^{\int_3}(1) + 12u(0) + 6u'(0)
\end{cases}
$$
Then $(36)$ can be converted to 
$$
\begin{cases}
u_2 - e^x u_1 + u + sin(u) = f(x) \\
u = u_4^{\int_4}(x) + (2x^3 - 3x^2)u_4^{\int_4}(1) + (x^2 - x^3)u_4^{\int_3}(1) + a\frac{x^3}{6} + b\frac{x^2}{2} xu'(0) + u(0)
\end{cases}
$$


And 
$$
u_2 = \frac{d^2u}{dx^2} = u_4^{\int_2}(x) + (12x - 6)u_4^{\int_4}(1) + (2 - 6x)u_4^{\int_3}(1) + ax + b
$$
Where
$$
\begin{cases}
a = -12u(1) + 6u'(1) + 12u(0) + 6u'(0) \\
b = 6u(1) - 2u'(1) -6u(0) - 4u'(0)
\end{cases}
$$
From $(22)$ we can obtain that
$$
\begin{align}
\begin{split}

\end{split}
\end{align}
$$
