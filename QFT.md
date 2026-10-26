# QFT

## Contents

- [0. Mathematical Foundations](#qft-ch0)
  - [0.1 Fourier Transform](#fourier-transform)
  - [0.2 $`\gamma`$ Matrices: Weyl Representation](#gamma-matrices)
  - [0.3 IO(1,3) Group](#classical-poincare)
  - [0.4 Green's Functions](#greens-functions)
- [1. Classical Field Theory](#qft-ch1)
  - [1.1 Lagrangian Formalism](#lagrangian-formalism)
    - [Lagrangian](#mechanics-lagrangian)
    - [Symmetry Transformations and Noether's Theorem](#lagrangian-symmetry)
  - [1.2 Hamiltonian Formalism](#hamiltonian-formalism)
    - [Dynamical Systems](#dynamical-systems)
    - [Hamiltonian Formalism](#hamiltonian-mechanics)
    - [Symmetries and Noether's Theorem](#hamiltonian-symmetry)
  - [1.3 Definition of Classical Fields](#classical-field)
    - [Definition of Fields](#field-definition)
    - [Finite-Dimensional Representations of $`SO(1,3)^+`$ ](#lorentz-finite-representations)
  - [1.4 Dynamics of Classical Fields](#classical-dynamics)
    - [Lagrangian](#field-theory-lagrangian)
    - [Symmetry Transformations and Noether's Theorem](#classical-noether)
  - [1.5 Dirac Constraint](#dirac-constraint)
    - [Singular Lagrangians](#singular-lagrangian)
  - [1.6 The Scalar Field](#scalar-field)
    - [Lagrangian](#scalar-lagrangian)
    - [Solutions of the Klein–Gordon Equation](#scalar-field-solutions)
  - [1.7 The Dirac Field $`\psi`$ ](#dirac-field)
    - [Lagrangian](#dirac-lagrangian)
    - [Solutions of the Dirac Equation in the Weyl Representation](#weyl-spinor-solutions)
    - [Dirac Bilinears](#dirac-bilinears)
  - [1.8 The Proca Field](#proca-field)
    - [Lagrangian](#proca-lagrangian)
    - [Solutions of the Proca Equation](#proca-field-solutions)
  - [1.9 The Vector Field](#vector-field)
    - [Lagrangian](#maxwell-lagrangian)
    - [Solutions of the Maxwell Equations](#maxwell-field-solutions)
- [2. Operator Quantization](#qft-ch2)
  - [2.1 Canonical Quantization](#canonical-quantization)
  - [2.2 Quantization with Dirac Brackets](#quantization-with-dirac-brackets)
    - [Quantization of the Complex Scalar Field](#complex-scalar-field-quantization)
    - [Quantization of the Dirac Field](#dirac-field-quantization)
    - [Quantization of the Proca Field](#proca-field-quantization)
  - [2.3 Gupta–Bleuler Quantization](#gupta-bleuler-quantization)
  - [2.4 Symmetry](#symmetry)
    - [Schrödinger Picture](#schrodinger-picture)
    - [Heisenberg Picture](#heisenberg-picture)
- [3. The Standard Model](#qft-ch3)
  - [3.1 Yang–Mills Theory](#yang-mills)
  - [3.2 Quantum Electrodynamics](#qed)
  - [3.3 Quantum Chromodynamics](#qcd)
  - [3.4 Spontaneous Symmetry Breaking and the Higgs Mechanism](#higgs-mechanism)
    - [Higgs Lagrangian](#higgs-lagrangian)
    - [Spontaneous Symmetry Breaking](#spontaneous-symmetry-breaking)
    - [Higgs Mechanism](#higgs-mechanism-masses)
  - [3.5 Electroweak Theory](#electroweak-theory)
    - [Leptons in the Standard Model](#sm-leptons)
    - [Kinetic Terms](#electroweak-kinetic-terms)
    - [Yukawa Couplings and Charged-Lepton Masses](#charged-lepton-masses)
    - [Gauge-Boson Masses](#gauge-boson-masses)
    - [Quarks](#sm-quarks)
    - [Charged and Neutral Currents](#electroweak-currents)
- [4. Path Integrals](#qft-ch4)
  - [4.1 Path Integrals in Quantum Mechanics](#path-integrals-in-quantum-mechanics)
  - [4.2 Path Integrals in Quantum Field Theory](#path-integrals-in-field-theory)
  - [4.3 $`\phi^3`$ Theory](#phi-cubed-theory)
- [5. New Physics Beyond the Standard Model](#qft-ch5)
  - [5.1 Seesaw Mechanism](#seesaw-mechanism)
    - [Type-I Seesaw](#type-i-seesaw)
    - [Type-II Seesaw](#type-ii-seesaw)
    - [Type-III Seesaw](#type-iii-seesaw)
    - [Leptogenesis](#leptogenesis)
  - [5.2 Dark Matter](#dark-matter)
- [6. Scattering Theory](#qft-ch6)
  - [6.1 Interaction Picture](#interaction-picture)
  - [6.2 The S-Matrix and Wick's Theorem](#s-matrix-and-wick-theorem)
  - [6.3 Feynman Diagrams and Feynman Rules](#feynman-diagrams)
  - [6.4 Correlation Functions](#correlation-functions)
  - [6.5 LSZ Reduction Formula](#lsz-reduction)
  - [6.6 Cross Sections and Decay Rates](#cross-sections-and-decay-rates)
- [7. Renormalization](#qft-ch7)
  - [7.1 QED Renormalization](#qed-renormalization)
- [8. Multi-Loop Renormalization](#qft-ch8)
- [9. Cosmology](#qft-ch9)

---

<a id="qft-ch0"></a>
## 0. Mathematical Foundations

<a id="fourier-transform"></a>
### 0.1 Fourier Transform

We use the following convention for the four-dimensional Fourier transform, with the factor $`(2\pi)^{-4}`$ included in the inverse transform:

```math
\left.
\begin{aligned}
\widetilde f(p)&=\int d^4x\,e^{+ip\cdot x}f(x),\\
f(x)&=\int\frac{d^4p}{(2\pi)^4}\,e^{-ip\cdot x}\widetilde f(p).
\end{aligned}
\right.
\tag{0.1}
```

Here $`x^\mu=(t,\mathbf x)`$ and $`p^\mu=(p^0,\mathbf p)`$, and the phase is given by

```math
\left.
p\cdot x=p_\mu x^\mu=p^0t-\mathbf p\cdot\mathbf x.
\right.
\tag{0.2}
```

The Fourier representations of the Dirac $`\delta`$ function are

```math
\left.
\begin{aligned}
\int\frac{d^4p}{(2\pi)^4}\,e^{-ip\cdot(x-y)}&=\delta^{(4)}(x-y),\\[6pt]
\int d^4x\,e^{i(p-q)\cdot x}&=(2\pi)^4\delta^{(4)}(p-q).
\end{aligned}
\right.
\tag{0.3}
```


<br><br>

<a id="gamma-matrices"></a>
### 0.2 $`\gamma`$ Matrices: Weyl Representation

The Pauli matrices are

```math
\left.
\sigma^1=\begin{pmatrix}0&1\\1&0\end{pmatrix},\qquad
\sigma^2=\begin{pmatrix}0&-i\\i&0\end{pmatrix},\qquad
\sigma^3=\begin{pmatrix}1&0\\0&-1\end{pmatrix}.
\right.
\tag{0.4}
```

**Properties of the Pauli Matrices**

For each $`i=1,2,3`$,

```math
\left.
(\sigma^i)^\dagger=\sigma^i,\qquad
(\sigma^i)^2=I_2,\qquad
(\sigma^i)^{-1}=\sigma^i,\qquad
\mathop{\rm tr}\nolimits\,\sigma^i=0,\qquad
\det\sigma^i=-1.
\right.
\tag{0.5}
```

Thus, each Pauli matrix is both Hermitian and unitary, with eigenvalues $`+1`$ and $`-1`$.

The product identity is

```math
\left.
\sigma^i\sigma^j=\delta^{ij}I_2+i\epsilon^{ijk}\sigma^k.
\right.
\tag{0.6}
```

This gives the commutation and anticommutation relations, as well as the trace orthogonality relation:

```math
\left.
[\sigma^i,\sigma^j]=2i\epsilon^{ijk}\sigma^k,\qquad
\{\sigma^i,\sigma^j\}=2\delta^{ij}I_2,\qquad
\mathop{\rm tr}\nolimits (\sigma^i\sigma^j)=2\delta^{ij}.
\right.
\tag{0.7}
```

For any $`\mathbf a,\mathbf b\in\mathbb R^3`$, the product identity can also be written as

```math
\left.
(\mathbf a\cdot\boldsymbol\sigma)(\mathbf b\cdot\boldsymbol\sigma)
=(\mathbf a\cdot\mathbf b)I_2
+i(\mathbf a\times\mathbf b)\cdot\boldsymbol\sigma,
\qquad \boldsymbol\sigma=(\sigma^1,\sigma^2,\sigma^3).
\right.
\tag{0.8}
```

**$`\gamma`$ matrices**

Pauli four-vectors

```math
\left.
\sigma^\mu:=(I_2,\boldsymbol\sigma),\qquad
\bar\sigma^\mu:=(I_2,-\boldsymbol\sigma),\qquad \mu=0,1,2,3.
\right.
\tag{0.9}
```

Using them, the $`\gamma`$ matrices in the Weyl representation are defined as:

```math
\left.
\gamma^\mu:=
\begin{pmatrix}
0&\sigma^\mu\\
\bar\sigma^\mu&0
\end{pmatrix}_{4\times4}.
\right.
\tag{0.10}
```

These matrices satisfy 

```math
\left.
\{\gamma^\mu,\gamma^\nu\}=2\eta^{\mu\nu}I_4.
\right.
\tag{0.11}
```

```math
\left.
(\gamma^0)^2=I_4,\qquad
(\gamma^i)^2=-I_4,\\
(\gamma^0)^\dagger=\gamma^0,\qquad
(\gamma^i)^\dagger=-\gamma^i.
\right.
\tag{0.12}
```

Hence each $`\gamma^\mu`$ is unitary:

```math
\left.
(\gamma^\mu)^\dagger\gamma^\mu=I_4.
\right.
\tag{0.13}
```

Define

```math
\left.
\gamma^5:=i\gamma^0\gamma^1\gamma^2\gamma^3
=\begin{pmatrix}-I_2&0\\0&I_2\end{pmatrix}
.
\right.
\tag{0.14}
```

It satisfies

```math
\left.
(\gamma^5)^2=I_4,\qquad
\{\gamma^5,\gamma^\mu\}=0,\qquad
(\gamma^5)^\dagger = (\gamma^5).
\right.
\tag{0.15}
```

<br><br>

<a id="classical-poincare"></a>
### 0.3 IO(1,3) Group

**The Group O(1,3)** 

To distinguish a matrix $`\Lambda`$ from the corresponding tensor $`\Lambda`$ of coordinate transformation, we denote the matrix by $`[\Lambda]`$ and the tensor simply by $`\Lambda`$. We use the same notation for $`\eta`$.

The matrix $`[\Lambda]`$

```math
\left.
O(1,3):=\{[\Lambda]\in GL(4,\mathbb R)\mid [\Lambda]^T[\eta][\Lambda]=[\eta]\}.
\right.
\tag{0.16}
```

where $`[\eta]=\mathop{\rm diag}\nolimits (1,-1,-1,-1)`$. 

The tensor $`\Lambda`$ 

Given a specific diffeomorphism of Minkowskispacetime $`\phi:x\mapsto x'`$, we obtain a tensor

```math
\left.
\Lambda^\mu{}_\nu:=\frac{\partial x'^\mu}{\partial x^\nu}.
\right.
\tag{0.17}
```

By the way, we can prove that the isometries of Minkowski spacetime must be linear up to a translation.

The entry of $`[\Lambda]`$ in row $`\mu`$ and column $`\nu`$ is the corresponding component of the tensor $`\Lambda`$:

```math
\left.
[\Lambda]_{\mu\nu}=\Lambda^\mu{}_\nu.
\right.
\tag{0.18}
```

Similarly,

```math
\left.
[\eta]_{\mu\nu}=\eta_{\mu\nu}.
\right.
\tag{0.19}
```

Therefore, equivalently, we obtain the following relationship:

```math
\left.
\eta_{\mu\nu}\Lambda^\mu{}_\rho\Lambda^\nu{}_\sigma=\eta_{\rho\sigma}.
\right.
\tag{0.20}
```

where we have used the relation $`([\Lambda]^T)_{\mu\nu}=\Lambda^\nu{}_\mu`$. This is exactly the condition for $`\phi`$ to be an isometry of Minkowski spacetime.


The inverse and transpose of $`[\Lambda]`$ satisfy

```math
\left.
[\Lambda]^{-1}=[\eta][\Lambda]^T[\eta],\qquad
[\Lambda][\eta][\Lambda]^T=[\eta],
\right.
\tag{0.21}
```

so $`[\Lambda]^{-1}`$ and $`[\Lambda]^T`$ also belong to $`O(1,3)`$. 

In components, the first relation reads

```math
\left.
(\Lambda^{-1})^\mu{}_\nu=\Lambda_\nu{}^\mu.
\right.
\tag{0.22}
```

**Connectedness**

Taking the determinant of $`[\Lambda]^T[\eta][\Lambda]=[\eta]`$ gives

```math
\left.
(\det[\Lambda])^2=1\quad\Longrightarrow\quad\det[\Lambda]=\pm1.
\right.
\tag{0.23}
```

Setting $`\rho=\sigma=0`$ in $`\eta_{\mu\nu}\Lambda^\mu{}_\rho\Lambda^\nu{}_\sigma=\eta_{\rho\sigma}`$ gives

```math
\left.
(\Lambda^0{}_0)^2=1+\sum_i(\Lambda^i{}_0)^2\ge1\quad\Longrightarrow\quad\Lambda^0{}_0\ge1\ \text{or}\ \Lambda^0{}_0\le-1.
\right.
\tag{0.24}
```

We can prove that $`O(1,3)`$ has exactly these four connected components.

Define the time reversal $`T`$ and the space inversion $`P`$ by

```math
\left.
T:(t,\mathbf x)\mapsto(-t,\mathbf x),\qquad
P:(t,\mathbf x)\mapsto(t,-\mathbf x),
\right.
\tag{0.25}
```

whose matrices are

```math
\left.
[T]=\mathop{\rm diag}\nolimits (-1,1,1,1),\qquad
[P]=\mathop{\rm diag}\nolimits (1,-1,-1,-1).
\right.
\tag{0.26}
```

The corresponding tensors are

```math
\left.
T^\mu{}_\nu=\delta^\mu{}_\nu-2\delta^\mu{}_0\delta^0{}_\nu,\qquad
P^\mu{}_\nu=-\delta^\mu{}_\nu+2\delta^\mu{}_0\delta^0{}_\nu.
\right.
\tag{0.27}
```

<div style="display: flex; justify-content: center;">

| Connected component | $`\det[\Lambda]`$ | $`\Lambda^0{}_0`$ | Representative |
|:---:|:---:|:---:|:---:|
| $`\mathcal L^\uparrow_+`$ | $`+1`$ | $`\ge1`$ | $`I`$ |
| $`\mathcal L^\downarrow_+`$ | $`+1`$ | $`\le-1`$ | $`[PT]`$ |
| $`\mathcal L^\uparrow_-`$ | $`-1`$ | $`\ge1`$ | $`[P]`$ |
| $`\mathcal L^\downarrow_-`$ | $`-1`$ | $`\le-1`$ | $`[T]`$ |

</div>

$`SO(1,3)`$ consists of the two classes with $`\det[\Lambda]=+1`$:

```math
\left.
SO(1,3)=\mathcal L^\uparrow_+\cup\mathcal L^\downarrow_+.
\right.
\tag{0.28}
```

Furthermore, $`SO(1,3)^+=\mathcal L^\uparrow_+`$ is a subgroup of $`O(1,3)`$.

Physically, $`T`$ and $`P`$ correspond to time-reversal symmetry and parity symmetry, respectively. What is usually called Lorentz symmetry is invariance under $`SO(1,3)^+`$ only. The distinction matters: no violation of Lorentz symmetry has ever been observed, so it is regarded as a fundamental symmetry. Parity, in contrast, is violated in the weak interaction, as proposed by Lee and Yang and confirmed experimentally by Wu et al.; time-reversal symmetry is violated as well.

**Lie Algebra of O(1,3)**

Consider a one-parameter subgroup $`e^{tX}`$, $`t\in\mathbb R`$, of $`O(1,3)`$. It satisfies

```math
\left.
(e^{tX})^T[\eta]\,e^{tX}=[\eta].
\right.
\tag{0.29}
```

Expanding the left-hand side to first order in $`t`$ gives

```math
\left.
(I+tX^T)[\eta](I+tX)+O(t^2)=[\eta]+t\left(X^T[\eta]+[\eta]X\right)+O(t^2),
\right.
\tag{0.30}
```

so the first-order term must vanish:

```math
\left.
X^T[\eta]+[\eta]X=0.
\right.
\tag{0.31}
```

Therefore,

```math
\left.
\mathfrak o(1,3):=\{X\in M_4(\mathbb R)\mid X^T[\eta]+[\eta]X=0\}.
\right.
\tag{0.32}
```

Furthermore, this relation can be written more explicitly as

```math
\left.
[\eta]X=-X^T[\eta]=-([\eta]X)^T,
\right.
\tag{0.33}
```

which means that the matrix $`[\eta]X`$ is antisymmetric. 

An antisymmetric $`4\times4`$ matrix has $`4\times3/2=6`$ independent real parameters. Hence the general form of $`X`$ is

```math
\left.
X=\begin{pmatrix}
0&b^1&b^2&b^3\\
b^1&0&-\theta^3&\theta^2\\
b^2&\theta^3&0&-\theta^1\\
b^3&-\theta^2&\theta^1&0
\end{pmatrix}
=\sum_i\theta^iJ^i+\sum_ib^iK^i
\right.
\tag{0.34}
```

In physics, the following notation is commonly used:

```math
\left.
e^{-\frac i2\omega^{\mu\nu}J^{\mu\nu}}
\right.
\tag{0.35}
```

where $`\omega_{\mu\nu}`$ is antisymmetric in its indices, and

```math
\left.
-iJ^{ij}=\epsilon_{ijk}J^k,\qquad -iJ^{0i}=K^i.
\right.
\tag{0.36}
```

Each $`J^{\mu\nu}`$ is simply a $`4\times4`$ matrix, with $`\alpha,\beta`$ labelling its rows and columns. Its entries are

```math
\left.
(J^{\mu\nu})_{\alpha\beta}=i\left(\eta^{\mu\alpha}\delta^{\nu\beta}-\eta^{\nu\alpha}\delta^{\mu\beta}\right).
\right.
\tag{0.37}
```

Explicitly (row index $`\alpha`$, column index $`\beta`$; the remaining components follow from $`J^{\nu\mu}=-J^{\mu\nu}`$), the rotation generators $`J^{ij}=i\epsilon_{ijk}J^k`$ are Hermitian:

```math
\left.
J^{23}=\begin{pmatrix}0&0&0&0\\0&0&0&0\\0&0&0&-i\\0&0&i&0\end{pmatrix},\quad
J^{31}=\begin{pmatrix}0&0&0&0\\0&0&0&i\\0&0&0&0\\0&-i&0&0\end{pmatrix},\quad
J^{12}=\begin{pmatrix}0&0&0&0\\0&0&-i&0\\0&i&0&0\\0&0&0&0\end{pmatrix},
\right.
\tag{0.38}
```

and the boost generators $`J^{0i}=iK^i`$ are anti-Hermitian:

```math
\left.
J^{01}=\begin{pmatrix}0&i&0&0\\i&0&0&0\\0&0&0&0\\0&0&0&0\end{pmatrix},\quad
J^{02}=\begin{pmatrix}0&0&i&0\\0&0&0&0\\i&0&0&0\\0&0&0&0\end{pmatrix},\quad
J^{03}=\begin{pmatrix}0&0&0&i\\0&0&0&0\\0&0&0&0\\i&0&0&0\end{pmatrix}.
\right.
\tag{0.39}
```


<br><br>

<a id="greens-functions"></a>
### 0.4 Green's Functions

**Definition and Integral Solution**

In the general construction below, $`x,y`$ denote $`d`$ independent variables. Let $`\mathcal K_x`$ be a linear differential operator on $`\Omega\subseteq\mathbb R^d`$, and let $`\mathcal B`$ specify linear boundary or initial data:

```math
\left.
\mathcal K_xu(x)=f(x),\qquad \mathcal Bu=b.
\right.
\tag{0.40}
```

Assume the data are sufficiently regular and the integrals below exist. Equations involving $`\delta`$ functions are understood in the sense of distributions.

- **Green's function**: A kernel satisfying the differential equation and homogeneous boundary or initial conditions,

```math
\left.
\boxed{\mathcal K_xG(x,y)=\delta^{(d)}(x-y),\qquad \mathcal B_xG(x,y)=0.}
\right.
\tag{0.41}
```

The subscript $`x`$ specifies the variable on which the operator acts. The choice of boundary or initial conditions is part of the definition of $`G`$.

- **Integral solution**: If $`u_{\mathrm h}`$ solves the homogeneous equation with the prescribed data, then

```math
\left.
\begin{aligned}
\boxed{u(x)=u_{\mathrm h}(x)+\int_\Omega d^dy\,G(x,y)f(y),}\\
\mathcal K_xu_{\mathrm h}(x)=0,\qquad \mathcal Bu_{\mathrm h}=b.
\end{aligned}
\right.
\tag{0.42}
```

Indeed,

```math
\left.
\begin{aligned}
\mathcal K_xu(x)
&=\int_\Omega d^dy\,[\mathcal K_xG(x,y)]f(y)
=\int_\Omega d^dy\,\delta^{(d)}(x-y)f(y)=f(x),\\
\mathcal Bu&=\mathcal Bu_{\mathrm h}
+\int_\Omega d^dy\,[\mathcal B_xG(x,y)]f(y)=b.
\end{aligned}
\right.
\tag{0.43}
```

The solution is unique if $`\mathcal Ku=0`$, $`\mathcal Bu=0`$ has only the zero solution in the chosen function space. With nontrivial zero modes, uniqueness fails and solvability may impose compatibility conditions; an inverse on arbitrary sources cannot be assumed. Without boundary or initial conditions, two kernels satisfying the first equation in (0.41) can differ by a solution of the homogeneous equation in $`x`$.

**Construction by Fourier Transform**

For a constant-coefficient operator on Minkowski spacetime, return to $`x^\mu=(t,\mathbf x)`$ and the Fourier convention (0.1). If the chosen conditions are also translation invariant, $`G(x,y)=G(x-y)`$, and

```math
\left.
\begin{aligned}
\mathcal K(-ip)\widetilde G(p)&=1,\\
G(x-y)&=\int\frac{d^4p}{(2\pi)^4}\,
e^{-ip\cdot(x-y)}\widetilde G(p),\\
\widetilde G(p)&=\left[\frac{1}{\mathcal K(-ip)}\right]_{\mathrm{prescription}}.
\end{aligned}
\right.
\tag{0.44}
```

Here $`\mathcal K(-ip)`$ is obtained by replacing each $`\partial_\mu`$ with $`-ip_\mu`$. At zeros of $`\mathcal K(-ip)`$, the reciprocal requires a distributional prescription fixed by the chosen conditions; the algebraic equation alone does not select it.

**Poisson Equation and Boundary Data**

First consider a smooth source of compact support in $`\mathbb R^3`$:

```math
\left.
-\nabla^2u(\mathbf x)=f(\mathbf x),\qquad
u(\mathbf x)\to0\quad\text{as }|\mathbf x|\to\infty.
\right.
\tag{0.45}
```

For $`r:=|\mathbf x-\mathbf y|>0`$, a rotationally invariant kernel that vanishes at infinity obeys

```math
\left.
\nabla^2G_0(r)=\frac{1}{r^2}\frac{d}{dr}\left(r^2\frac{dG_0}{dr}\right)=0
\quad\Longrightarrow\quad G_0(r)=\frac{A}{r}.
\right.
\tag{0.46}
```

Integrating $`-\nabla^2G_0=\delta^{(3)}`$ over a ball $`B_\epsilon`$ centred at the source fixes $`A`$:

```math
\left.
\begin{aligned}
1&=-\int_{B_\epsilon}d^3x\,\nabla^2G_0
=-4\pi\epsilon^2\left.\frac{dG_0}{dr}\right|_{r=\epsilon}
=4\pi A,\\
G_0(\mathbf x,\mathbf y)&=\frac{1}{4\pi|\mathbf x-\mathbf y|}.
\end{aligned}
\right.
\tag{0.47}
```

Hence

```math
\left.
\boxed{u(\mathbf x)=\int_{\mathbb R^3}d^3y\,
\frac{f(\mathbf y)}{4\pi|\mathbf x-\mathbf y|}.}
\right.
\tag{0.48}
```

Now let $`\Omega\subset\mathbb R^3`$ be bounded with smooth boundary, and prescribe $`u=b`$ on $`\partial\Omega`$. The Dirichlet Green's function for $`-\nabla^2`$ is symmetric in its arguments and satisfies

```math
\left.
\begin{aligned}
-\nabla_{\mathbf y}^2G_D(\mathbf x,\mathbf y)
&=\delta^{(3)}(\mathbf y-\mathbf x),\qquad \mathbf y\in\Omega,\\
G_D(\mathbf x,\mathbf y)&=0,\qquad \mathbf y\in\partial\Omega.
\end{aligned}
\right.
\tag{0.49}
```

Let $`\mathbf n_y`$ be the outward unit normal and $`\partial_{n_y}:=\mathbf n_y\cdot\nabla_{\mathbf y}`$. Green's second identity is

```math
\left.
\int_\Omega d^3y\,(v\nabla^2w-w\nabla^2v)
=\int_{\partial\Omega}dS_y\,(v\partial_{n_y}w-w\partial_{n_y}v).
\right.
\tag{0.50}
```

Apply (0.50) to $`v=u`$, $`w=G_D(\mathbf x,\cdot)`$ on $`\Omega\setminus B_\epsilon(\mathbf x)`$ and take $`\epsilon\to0^+`$. For $`\mathbf x\in\Omega`$,

```math
\left.
\boxed{\begin{aligned}
u(\mathbf x)&=\int_\Omega d^3y\,G_D(\mathbf x,\mathbf y)f(\mathbf y)\\
&\quad-\int_{\partial\Omega}dS_y\,b(\mathbf y)\partial_{n_y}G_D(\mathbf x,\mathbf y).
\end{aligned}}
\right.
\tag{0.51}
```

The second term supplies the nonzero boundary data. The free-space kernel $`G_0`$ in (0.47) generally does not satisfy the boundary condition in (0.49).

**Klein–Gordon Equation and Initial Data**

With $`m\geq0`$ and the mostly-minus metric, consider

```math
\left.
(\Box+m^2)u(x)=f(x),\qquad
\Box:=\partial_\mu\partial^\mu=\partial_t^2-\nabla^2.
\right.
\tag{0.52}
```

- **Retarded Green's function**: The translation-invariant kernel with support only at nonnegative time differences,

```math
\left.
(\Box+m^2)G_{\mathrm{ret}}(t,\mathbf x)
=\delta(t)\delta^{(3)}(\mathbf x),\qquad
G_{\mathrm{ret}}(t,\mathbf x)=0\quad(t<0).
\right.
\tag{0.53}
```

Here the source point has been translated to the origin. Since $`\mathcal K(-ip)=m^2-p^2`$, the retarded prescription is

```math
\left.
\widetilde G_{\mathrm{ret}}(p)
=-\lim_{\epsilon\to0^+}\frac{1}{(p^0+i\epsilon)^2-E_{\mathbf p}^2},\qquad
E_{\mathbf p}:=\sqrt{\mathbf p^2+m^2}.
\right.
\tag{0.54}
```

Both poles lie below the real $`p^0`$ axis. Closing the contour in the lower half-plane for $`t>0`$ and the upper half-plane for $`t<0`$ gives

```math
\left.
\boxed{G_{\mathrm{ret}}(t,\mathbf x)
=\theta(t)\int\frac{d^3p}{(2\pi)^3}\,
e^{i\mathbf p\cdot\mathbf x}\frac{\sin(E_{\mathbf p}t)}{E_{\mathbf p}}.}
\right.
\tag{0.55}
```

Here $`\theta(t)`$ is the Heaviside function, and the value at $`E_{\mathbf p}=0`$ is understood by continuity. The equal-time limits are

```math
\left.
G_{\mathrm{ret}}(0^+,\mathbf x)=0,\qquad
\partial_tG_{\mathrm{ret}}(0^+,\mathbf x)=\delta^{(3)}(\mathbf x).
\right.
\tag{0.56}
```

For prescribed initial data $`u(t_0,\mathbf x)=u_0(\mathbf x)`$ and $`\partial_tu(t_0,\mathbf x)=u_1(\mathbf x)`$, (0.56) yields, for $`t>t_0`$,

```math
\left.
\boxed{\begin{aligned}
u(t,\mathbf x)
&=\int d^3y\,\bigl[
\partial_tG_{\mathrm{ret}}(t-t_0,\mathbf x-\mathbf y)u_0(\mathbf y)\\
&\hspace{4.5em}+G_{\mathrm{ret}}(t-t_0,\mathbf x-\mathbf y)u_1(\mathbf y)\bigr]\\
&\quad+\int_{t_0}^{t}dt'\int d^3y\,
G_{\mathrm{ret}}(t-t',\mathbf x-\mathbf y)f(t',\mathbf y).
\end{aligned}}
\right.
\tag{0.57}
```

For $`m=0`$, the spatial integral in (0.55) gives the wave-equation kernel. Writing $`r:=|\mathbf x|`$,

```math
\left.
\begin{aligned}
G_{\mathrm{ret}}(t,\mathbf x)\big|_{m=0}
&=\frac{\theta(t)}{2\pi^2r}\int_0^\infty dp\,\sin(pr)\sin(pt)\\
&=\boxed{\frac{\delta(t-r)}{4\pi r}}.
\end{aligned}
\right.
\tag{0.58}
```

With zero initial data, extend $`f(t',\mathbf y)`$ by zero for $`t'<t_0`$. Then (0.57) reduces to

```math
\left.
\boxed{u(t,\mathbf x)=\int d^3y\,
\frac{f(t-|\mathbf x-\mathbf y|,\mathbf y)}{4\pi|\mathbf x-\mathbf y|}.}
\right.
\tag{0.59}
```

For comparison with the scalar Feynman propagator defined in (6.12), the Feynman prescription for the same normalization $`\mathcal KG_F=\delta^{(4)}`$ gives

```math
\left.
\begin{aligned}
G_F(x-y)&=-\lim_{\varepsilon\to0^+}\int\frac{d^4p}{(2\pi)^4}\,
\frac{e^{-ip\cdot(x-y)}}{p^2-m^2+i\varepsilon}
=i\Delta_F(x-y),\\
(\Box_x+m^2)\Delta_F(x-y)&=-i\delta^{(4)}(x-y).
\end{aligned}
\right.
\tag{0.60}
```


---

<a id="qft-ch1"></a>
## 1. Classical Field Theory

<a id="lagrangian-formalism"></a>
### 1.1 Lagrangian Formalism

<a id="mechanics-lagrangian"></a>
#### Lagrangian

**Definition**

Consider a system with $`n`$ degrees of freedom.

- **Configuration space**: an open set $`\mathrm{Conf}\subset\mathbb R^n`$.
  - A configuration is a point $`q=(q_1,\ldots,q_n)\in\mathrm{Conf}`$.
  - The $`q_a`$ are the generalized coordinates.
- **Paths**: smooth curves, for any $`t_0<t_f`$,

```math
\left.
\begin{aligned}
C:[t_0,t_f]&\to\mathrm{Conf},\\
t&\mapsto C(t),
\end{aligned}
\right.
\tag{1.1}
```

with velocity $`\dot C(t):=dC/dt`$.

- **Dynamical structure**: the Lagrangian, a smooth function

```math
\left.
\begin{aligned}
L:\mathrm{Conf}\times\mathbb R^n\times\mathbb R&\to\mathbb R,\\
(q,\dot q,t)&\mapsto L(q,\dot q,t),
\end{aligned}
\right.
\tag{1.2}
```

in which $`\dot q\in\mathbb R^n`$ is an independent variable.

- **Action**: the functional on paths

```math
\left.
\boxed{
\begin{aligned}
S:\{\text{paths}\}&\to\mathbb R,\\
C&\mapsto S[C]:=\int_{t_0}^{t_f}dt\,L\bigl(C(t),\dot C(t),t\bigr).
\end{aligned}}
\right.
\tag{1.3}
```

- **Solutions**: paths $`C`$ at which $`S`$ is stationary under variations with fixed endpoints,

```math
\left.
\frac{d}{ds}S[C+s\eta]\Big|_{s=0}=0,
\right.
\tag{1.4}
```

for every smooth $`\eta:[t_0,t_f]\to\mathbb R^n`$ with $`\eta(t_0)=\eta(t_f)=0`$.

**Euler–Lagrange Equations**

For a path $`C`$ and $`\eta`$ as in (1.4), let $`\frac{\partial L}{\partial q_a}\big|_C`$ and $`\frac{\partial L}{\partial\dot q_a}\big|_C`$ denote the partial derivatives of $`L`$ evaluated at $`\bigl(C(t),\dot C(t),t\bigr)`$. Then

```math
\left.
\begin{aligned}
\frac{d}{ds}S[C+s\eta]\Big|_{s=0}
&=\int_{t_0}^{t_f}dt\sum_{a=1}^n\Bigl(\frac{\partial L}{\partial q_a}\Big|_C\,\eta_a+\frac{\partial L}{\partial\dot q_a}\Big|_C\,\dot\eta_a\Bigr)\\
&=\int_{t_0}^{t_f}dt\sum_{a=1}^n\biggl[\frac{\partial L}{\partial q_a}\Big|_C-\frac{d}{dt}\Bigl(\frac{\partial L}{\partial\dot q_a}\Big|_C\Bigr)\biggr]\eta_a\\
&\quad+\biggl[\sum_{a=1}^n\frac{\partial L}{\partial\dot q_a}\Big|_C\,\eta_a\biggr]_{t_0}^{t_f}.
\end{aligned}
\right.
\tag{1.5}
```

The boundary term vanishes because $`\eta(t_0)=\eta(t_f)=0`$. Since $`\eta`$ is arbitrary, $`C`$ is a solution if and only if

```math
\left.
\boxed{\frac{d}{dt}\Bigl(\frac{\partial L}{\partial\dot q_a}\Big|_C\Bigr)-\frac{\partial L}{\partial q_a}\Big|_C=0,\qquad a=1,\ldots,n.}
\right.
\tag{1.6}
```

<br><br>

<a id="lagrangian-symmetry"></a>
#### Symmetry Transformations and Noether's Theorem

**Transformations**

- **Transformation**: a pair $`(\phi,\tau)`$ of a diffeomorphism $`\phi:\mathrm{Conf}\to\mathrm{Conf}`$ and a constant $`\tau\in\mathbb R`$, acting as

```math
\left.
\begin{aligned}
(\phi,\tau):\mathrm{Conf}\times\mathbb R&\to\mathrm{Conf}\times\mathbb R,\\
(q,t)&\mapsto\bigl(\phi(q),\,t+\tau\bigr),
\end{aligned}
\right.
\tag{1.7}
```

where $`\phi_a(q)`$ denotes the $`a`$-th coordinate of $`\phi(q)`$.

- **Action on paths**: a path $`C:[t_0,t_f]\to\mathrm{Conf}`$ is mapped to the path

```math
\left.
\begin{aligned}
C':[t_0+\tau,t_f+\tau]&\to\mathrm{Conf},\\
t&\mapsto\phi\bigl(C(t-\tau)\bigr),
\end{aligned}
\right.
\tag{1.8}
```

with velocity $`\dot C'_a(t)=\sum_{b=1}^n\frac{\partial\phi_a}{\partial q_b}\bigl(C(t-\tau)\bigr)\,\dot C_b(t-\tau)`$.

**Symmetry Transformations**

- **Symmetry transformation**: a transformation $`(\phi,\tau)`$ under which the action of every path is invariant,

```math
\left.
\boxed{S[C']=S[C]\quad\text{for every path }C,}
\right.
\tag{1.9}
```

with $`C'`$ given by (1.8).

Write $`\frac{\partial\phi}{\partial q}(q)`$ for the Jacobian matrix with entries $`\frac{\partial\phi_a}{\partial q_b}(q)`$, so that the velocity in (1.8) is $`\dot C'(t)=\frac{\partial\phi}{\partial q}\bigl(C(t-\tau)\bigr)\,\dot C(t-\tau)`$. Substituting (1.8) into (1.3) and shifting $`t\to t+\tau`$,

```math
\left.
\begin{aligned}
S[C']
&=\int_{t_0+\tau}^{t_f+\tau}dt\,L\bigl(C'(t),\dot C'(t),t\bigr)\\
&=\int_{t_0}^{t_f}dt\,L\Bigl(\phi\bigl(C(t)\bigr),\ \frac{\partial\phi}{\partial q}\bigl(C(t)\bigr)\,\dot C(t),\ t+\tau\Bigr).
\end{aligned}
\right.
\tag{1.10}
```

Hence $`(\phi,\tau)`$ is a symmetry transformation if and only if

```math
\left.
\boxed{L\Bigl(\phi(q),\ \frac{\partial\phi}{\partial q}(q)\,\dot q,\ t+\tau\Bigr)=L(q,\dot q,t)\quad\text{for all }(q,\dot q,t)\in\mathrm{Conf}\times\mathbb R^n\times\mathbb R.}
\right.
\tag{1.11}
```

**Conserved Quantities**

- **Conserved quantity**: a smooth function

```math
\left.
\begin{aligned}
\mathcal Q:\mathrm{Conf}\times\mathbb R^n\times\mathbb R&\to\mathbb R,\\
(q,\dot q,t)&\mapsto\mathcal Q(q,\dot q,t),
\end{aligned}
\right.
\tag{1.12}
```

such that $`\mathcal Q\bigl(C(t),\dot C(t),t\bigr)`$ is independent of $`t`$ for every solution $`C`$.

**Noether's Theorem**

Let $`(\phi_\lambda,\tau_\lambda)`$, $`\lambda\in\mathbb R`$, be a one-parameter subgroup of symmetry transformations:

- $`\phi_\lambda\circ\phi_\mu=\phi_{\lambda+\mu}`$ and $`\tau_\lambda+\tau_\mu=\tau_{\lambda+\mu}`$ for all $`\lambda,\mu\in\mathbb R`$; in particular $`\phi_0=\mathrm{id}`$ and $`\tau_0=0`$;
- $`(\lambda,q)\mapsto\phi_\lambda(q)`$ and $`\lambda\mapsto\tau_\lambda`$ are smooth.

Define

```math
\left.
\begin{aligned}
X:\mathrm{Conf}&\to\mathbb R^n,\\
q&\mapsto\frac{\partial\phi_\lambda(q)}{\partial\lambda}\Big|_{\lambda=0},
\end{aligned}
\qquad
\tau':=\frac{d\tau_\lambda}{d\lambda}\Big|_{\lambda=0}.
\right.
\tag{1.13}
```

$`X`$ and $`\tau'`$ are the generators of the subgroup:

- $`\phi_\lambda`$ is the flow of $`X`$, i.e. $`\partial_\lambda\phi_\lambda(q)=X\bigl(\phi_\lambda(q)\bigr)`$;
- $`\tau_\lambda=\tau'\lambda`$.

Then

```math
\left.
\boxed{\mathcal Q(q,\dot q,t):=\sum_{a=1}^n\frac{\partial L}{\partial\dot q_a}(q,\dot q,t)\,X_a(q)
-\tau'\Bigl(\sum_{a=1}^n\frac{\partial L}{\partial\dot q_a}(q,\dot q,t)\,\dot q_a-L(q,\dot q,t)\Bigr)}
\right.
\tag{1.14}
```

is a conserved quantity.

**Proof**

Each $`(\phi_\lambda,\tau_\lambda)`$ satisfies (1.11). Differentiating (1.11) with respect to $`\lambda`$ at $`\lambda=0`$, using $`\phi_0=\mathrm{id}`$ and $`\frac{\partial}{\partial\lambda}\frac{\partial(\phi_\lambda)_a}{\partial q_b}\big|_{\lambda=0}=\frac{\partial X_a}{\partial q_b}`$, gives for all $`(q,\dot q,t)`$

```math
\left.
\sum_{a=1}^n\Bigl(\frac{\partial L}{\partial q_a}\,X_a(q)
+\frac{\partial L}{\partial\dot q_a}\sum_{b=1}^n\frac{\partial X_a}{\partial q_b}(q)\,\dot q_b\Bigr)
+\frac{\partial L}{\partial t}\,\tau'=0,
\right.
\tag{1.15}
```

with the partial derivatives of $`L`$ evaluated at $`(q,\dot q,t)`$. Let $`C`$ be a solution and write $`L|_C:=L\bigl(C(t),\dot C(t),t\bigr)`$. Evaluating (1.15) at $`\bigl(C(t),\dot C(t),t\bigr)`$, and applying the chain rule and (1.6) also to $`L|_C`$,

```math
\left.
\begin{aligned}
\frac{d}{dt}\Bigl(\sum_{a=1}^n\frac{\partial L}{\partial\dot q_a}\Big|_C\,X_a\bigl(C(t)\bigr)\Bigr)&=-\tau'\,\frac{\partial L}{\partial t}\Big|_C,\\
\frac{d}{dt}\Bigl(\sum_{a=1}^n\frac{\partial L}{\partial\dot q_a}\Big|_C\,\dot C_a(t)-L\big|_C\Bigr)&=-\frac{\partial L}{\partial t}\Big|_C.
\end{aligned}
\right.
\tag{1.16}
```

Subtracting $`\tau'`$ times the second line from the first gives $`\frac{d}{dt}\mathcal Q\bigl(C(t),\dot C(t),t\bigr)=0`$. $`\square`$

**(1) Time Translation and Energy**

Take $`(\phi_\lambda,\tau_\lambda)=(\mathrm{id},\lambda)`$, so that $`X=0`$ and $`\tau'=1`$. By (1.11), this is a subgroup of symmetry transformations if and only if $`L(q,\dot q,t+\lambda)=L(q,\dot q,t)`$ for all $`\lambda`$, i.e. $`\partial L/\partial t=0`$. Then (1.14) gives $`\mathcal Q=-E`$, with the energy

```math
\left.
\boxed{E(q,\dot q,t):=\sum_{a=1}^n\frac{\partial L}{\partial\dot q_a}(q,\dot q,t)\,\dot q_a-L(q,\dot q,t),}
\right.
\tag{1.17}
```

so $`E`$ is a conserved quantity. More generally, by the second line of (1.16), $`\frac{d}{dt}E\bigl(C(t),\dot C(t),t\bigr)=-\frac{\partial L}{\partial t}\big|_C`$ along every solution $`C`$.

**(2) Translations and Momentum**

Let $`\mathrm{Conf}=\mathbb R^n`$ and fix $`k\in\mathbb R^n`$. Take $`\phi_\lambda(q)=q+\lambda k`$ and $`\tau_\lambda=0`$, so that $`X=k`$ and $`\tau'=0`$. By (1.11), this is a subgroup of symmetry transformations if and only if $`L(q+\lambda k,\dot q,t)=L(q,\dot q,t)`$ for all $`\lambda`$, i.e. $`\sum_ak_a\,\partial L/\partial q_a=0`$. Then (1.14) gives the conserved quantity

```math
\left.
\boxed{\mathcal Q(q,\dot q,t)=\sum_{a=1}^nk_a\,\frac{\partial L}{\partial\dot q_a}(q,\dot q,t).}
\right.
\tag{1.18}
```

- For $`k`$ the $`b`$-th unit vector, the condition is $`\partial L/\partial q_b=0`$, and $`\partial L/\partial\dot q_b`$ is conserved.
- For $`N`$ particles in space, $`q=(\mathbf x_1,\ldots,\mathbf x_N)`$ with $`\mathbf x_A\in\mathbb R^3`$, take $`k=(\mathbf e,\ldots,\mathbf e)`$ for a fixed $`\mathbf e\in\mathbb R^3`$. Then $`\phi_\lambda`$ translates every particle by $`\lambda\mathbf e`$, and the conserved quantity is $`\sum_{A=1}^N\mathbf e\cdot\frac{\partial L}{\partial\dot{\mathbf x}_A}`$, the component of the total momentum along $`\mathbf e`$.

<br><br>

<a id="hamiltonian-formalism"></a>
### 1.2 Hamiltonian Formalism

<a id="dynamical-systems"></a>
#### Dynamical Systems

**Definition**

- **State space**: an open set $`M\subset\mathbb R^N`$.
  - A state is a point $`z=(z_1,\ldots,z_N)\in M`$.
  - The $`z_A`$ are the state variables.
- **State transition function**: a smooth function

```math
\left.
\begin{aligned}
F:M&\to\mathbb R^N,\\
z&\mapsto F(z).
\end{aligned}
\right.
\tag{1.19}
```

- **Solutions**: smooth curves $`C:I\to M`$, with $`I\subset\mathbb R`$ an open interval, such that

```math
\left.
\boxed{\dot C_A(t)=F_A\bigl(C(t)\bigr),\qquad A=1,\ldots,N.}
\right.
\tag{1.20}
```

**(1) Determinism**

Since $`F`$ is smooth, for every $`t_0\in\mathbb R`$ and $`z^{(0)}\in M`$ there is a unique maximal solution $`C`$ with $`C(t_0)=z^{(0)}`$. The state at one time therefore determines the state at every later and every earlier time on its interval, and through each point of $`M`$ passes exactly one solution curve.

Assume every maximal solution is defined on all of $`\mathbb R`$. The flow of $`F`$ is

```math
\left.
\begin{aligned}
\Phi_t:M&\to M,\\
z^{(0)}&\mapsto C(t),
\end{aligned}
\right.
\tag{1.21}
```

where $`C`$ is the solution with $`C(0)=z^{(0)}`$. It satisfies

- $`\partial_t\Phi_t(z)=F\bigl(\Phi_t(z)\bigr)`$ and $`\Phi_0=\mathrm{id}`$;
- $`\Phi_t\circ\Phi_s=\Phi_{t+s}`$, since $`F`$ does not depend on $`t`$, so each $`\Phi_t`$ is a diffeomorphism with inverse $`\Phi_{-t}`$.

**(2) Volume in State Space**

For a region $`D\subset M`$, write $`\mathrm{vol}(D):=\int_Dd^Nz`$ and $`J_t:=\frac{\partial\Phi_t}{\partial z}`$ for the Jacobian matrix of $`\Phi_t`$. Differentiating $`\partial_t\Phi_t=F\circ\Phi_t`$ with respect to $`z`$ and using Jacobi's formula $`d\det J=\det J\,\mathop{\rm tr}\nolimits (J^{-1}dJ)`$,

```math
\left.
\begin{aligned}
\partial_tJ_t&=\Bigl(\frac{\partial F}{\partial z}\circ\Phi_t\Bigr)J_t,
\qquad
\partial_t\det J_t=\Bigl(\sum_{A=1}^N\frac{\partial F_A}{\partial z_A}\circ\Phi_t\Bigr)\det J_t,\\
\frac{d}{dt}\mathrm{vol}\bigl(\Phi_t(D)\bigr)
&=\frac{d}{dt}\int_Dd^Nz\,\det J_t
=\int_{\Phi_t(D)}d^Nz\,\sum_{A=1}^N\frac{\partial F_A}{\partial z_A}.
\end{aligned}
\right.
\tag{1.22}
```

Hence $`\mathrm{vol}(\Phi_t(D))`$ is constant for every $`D`$ if and only if $`\sum_A\partial F_A/\partial z_A=0`$.

<br><br>

<a id="hamiltonian-mechanics"></a>
#### Hamiltonian Formalism

**Definition**

Consider a system with $`n`$ degrees of freedom.

- **Phase space**: an open set $`M\subset\mathbb R^{2n}`$.
  - A state is a point $`z=(q_1,\ldots,q_n,p_1,\ldots,p_n)\in M`$.
  - The $`q_a`$ are the generalized coordinates and the $`p_a`$ the momenta.
- **Observables**: smooth functions

```math
\left.
\begin{aligned}
f:M&\to\mathbb R,\\
z&\mapsto f(z).
\end{aligned}
\right.
\tag{1.23}
```

- **Dynamical structure**:
  - the Poisson bracket $`\{\ ,\ \}_{\mathrm{PB}}`$ of (1.81);
  - the Hamiltonian, a smooth function

```math
\left.
\begin{aligned}
H:M&\to\mathbb R,\\
z&\mapsto H(z),
\end{aligned}
\right.
\tag{1.24}
```

with no explicit time dependence.

- **Solutions**: smooth curves $`C:I\to M`$, with $`I\subset\mathbb R`$ an open interval, such that

```math
\left.
\frac{d}{dt}q_a\bigl(C(t)\bigr)=\frac{\partial H}{\partial p_a}\bigl(C(t)\bigr),\quad
\frac{d}{dt}p_a\bigl(C(t)\bigr)=-\frac{\partial H}{\partial q_a}\bigl(C(t)\bigr)
\qquad\Longleftrightarrow\qquad
\frac{d}{dt}f\bigl(C(t)\bigr)=\{f,H\}_{\mathrm{PB}}\bigl(C(t)\bigr)\quad\text{for all }f.
\right.
\tag{1.25}
```

<br><br>

<a id="hamiltonian-symmetry"></a>
#### Symmetries and Noether's Theorem

**Transformations**

- **Transformation**: a diffeomorphism with no explicit time dependence,

```math
\left.
\begin{aligned}
\phi:M&\to M,\\
z&\mapsto\phi(z),
\end{aligned}
\qquad
Q_a:=q_a\circ\phi,\quad P_a:=p_a\circ\phi,\quad \phi_*f:=f\circ\phi^{-1},
\right.
\tag{1.26}
```

where $`Q_a(z),P_a(z)`$ are the coordinates of $`\phi(z)`$, and $`\phi_*`$ is the pushforward of (1.58), with $`(\phi_*f)(\phi(z))=f(z)`$.

**Symmetry Transformations**

- **Symmetry transformation**: a transformation $`\phi`$ that preserves both the Poisson bracket and the Hamiltonian,

```math
\left.
\boxed{
\begin{aligned}
&\text{(i)}\quad\{f\circ\phi,\,g\circ\phi\}_{\mathrm{PB}}=\{f,g\}_{\mathrm{PB}}\circ\phi\quad\text{for all }f,g,\\
&\text{(ii)}\quad H\circ\phi=H.
\end{aligned}}
\right.
\tag{1.27}
```

A transformation satisfying (i) is a canonical transformation. Replacing $`f,g`$ by $`f\circ\phi^{-1},g\circ\phi^{-1}`$ shows that (i) is equivalent to $`\{\phi_*f,\phi_*g\}_{\mathrm{PB}}=\phi_*\{f,g\}_{\mathrm{PB}}`$; (ii) is equivalent to $`\phi_*H=H`$, i.e. $`H(\phi(z))=H(z)`$ for all $`z\in M`$.

Write $`z_A`$, $`A=1,\ldots,2n`$, for all phase-space coordinates and $`Z_A:=z_A\circ\phi`$. By the chain rule,

```math
\left.
\begin{aligned}
\{f\circ\phi,\,g\circ\phi\}_{\mathrm{PB}}
&=\sum_{A,B}\Bigl(\frac{\partial f}{\partial z_A}\circ\phi\Bigr)\Bigl(\frac{\partial g}{\partial z_B}\circ\phi\Bigr)\{Z_A,Z_B\}_{\mathrm{PB}},\\
\{f,g\}_{\mathrm{PB}}\circ\phi
&=\sum_{A,B}\Bigl(\frac{\partial f}{\partial z_A}\circ\phi\Bigr)\Bigl(\frac{\partial g}{\partial z_B}\circ\phi\Bigr)\{z_A,z_B\}_{\mathrm{PB}}.
\end{aligned}
\right.
\tag{1.28}
```

The brackets $`\{z_A,z_B\}_{\mathrm{PB}}`$ are constants, and $`f=z_A`$, $`g=z_B`$ pick out a single term, so (i) holds if and only if $`\{Z_A,Z_B\}_{\mathrm{PB}}=\{z_A,z_B\}_{\mathrm{PB}}`$. By (1.81), (i) is equivalent to

```math
\left.
\boxed{
\{Q_a,Q_b\}_{\mathrm{PB}}=\{P_a,P_b\}_{\mathrm{PB}}=0,\qquad
\{Q_a,P_b\}_{\mathrm{PB}}=\delta_{ab}.}
\right.
\tag{1.29}
```

A symmetry transformation maps solutions to solutions. Let $`C`$ be a solution and $`C':=\phi\circ C`$. Applying (1.25) to $`f\circ\phi`$, then (ii) and (i),

```math
\left.
\begin{aligned}
\frac{d}{dt}f\bigl(C'(t)\bigr)
&=\{f\circ\phi,\,H\}_{\mathrm{PB}}\bigl(C(t)\bigr)\\
&=\{f\circ\phi,\,H\circ\phi\}_{\mathrm{PB}}\bigl(C(t)\bigr)
=\{f,H\}_{\mathrm{PB}}\bigl(C'(t)\bigr)
\end{aligned}
\right.
\tag{1.30}
```

for every $`f`$, so $`C'`$ is a solution by (1.25).

**Conserved Quantities**

- **Conserved quantity**: an observable $`f`$ such that $`f\bigl(C(t)\bigr)`$ is independent of $`t`$ for every solution $`C`$.

(1.25) is (1.20) with $`N=2n`$ and $`F_A=\{z_A,H\}_{\mathrm{PB}}`$. Since a solution passes through each point of $`M`$, (1.25) shows that $`f`$ is a conserved quantity if and only if

```math
\left.
\boxed{\{f,H\}_{\mathrm{PB}}=0.}
\right.
\tag{1.31}
```

**Noether's Theorem**

Let $`\phi_\lambda`$, $`\lambda\in\mathbb R`$, be a one-parameter subgroup of symmetry transformations:

- $`\phi_\lambda\circ\phi_\mu=\phi_{\lambda+\mu}`$ for all $`\lambda,\mu\in\mathbb R`$; in particular $`\phi_0=\mathrm{id}`$;
- $`(\lambda,z)\mapsto\phi_\lambda(z)`$ is smooth.

Define the generator

```math
\left.
\begin{aligned}
X:M&\to\mathbb R^{2n},\\
z&\mapsto\frac{\partial\phi_\lambda(z)}{\partial\lambda}\Big|_{\lambda=0},
\end{aligned}
\right.
\tag{1.32}
```

so that $`\phi_\lambda`$ is the flow of $`X`$. If $`M`$ is simply connected, there is a smooth function $`G:M\to\mathbb R`$, unique up to an additive constant, with

```math
\left.
X_A=\{z_A,G\}_{\mathrm{PB}},\qquad A=1,\ldots,2n,
\right.
\tag{1.33}
```

and

```math
\left.
\boxed{\{G,H\}_{\mathrm{PB}}=0,}
\right.
\tag{1.34}
```

so $`G`$ is a conserved quantity.

**Proof**

Write $`\omega_{AB}:=\{z_A,z_B\}_{\mathrm{PB}}`$. By (1.81) it is constant and invertible, and $`\{f,g\}_{\mathrm{PB}}=\sum_{A,B}\omega_{AB}\frac{\partial f}{\partial z_A}\frac{\partial g}{\partial z_B}`$. Define $`Y`$ by $`X_A=\sum_B\omega_{AB}Y_B`$. Differentiate (i) with $`f=z_A`$, $`g=z_B`$, and (ii), with respect to $`\lambda`$ at $`\lambda=0`$:

```math
\left.
\begin{aligned}
0&=\{X_A,z_B\}_{\mathrm{PB}}+\{z_A,X_B\}_{\mathrm{PB}}
=\sum_{C,D}\omega_{AC}\,\omega_{BD}\Bigl(\frac{\partial Y_D}{\partial z_C}-\frac{\partial Y_C}{\partial z_D}\Bigr),\\
0&=\sum_A\frac{\partial H}{\partial z_A}\,X_A.
\end{aligned}
\right.
\tag{1.35}
```

Since $`\omega`$ is invertible, $`\partial Y_D/\partial z_C=\partial Y_C/\partial z_D`$. On a simply connected $`M`$ this gives $`Y_B=\partial G/\partial z_B`$ for a smooth $`G`$, unique up to a constant, i.e. (1.33). The second line of (1.35) is then $`\sum_A\frac{\partial H}{\partial z_A}\{z_A,G\}_{\mathrm{PB}}=\{H,G\}_{\mathrm{PB}}=0`$, which is (1.34). $`\square`$

**(1) Time Evolution and Energy**

Taking $`f=H`$ in (1.31), $`\{H,H\}_{\mathrm{PB}}=0`$, so $`H`$ is a conserved quantity. With $`G=H`$, (1.33) gives $`X_A=\{z_A,H\}_{\mathrm{PB}}=F_A`$, so the subgroup generated by $`H`$ is the time evolution $`\Phi_t`$ of (1.21).

**(2) Translations and Momentum**

Let $`M=\mathbb R^{2n}`$ and fix $`k\in\mathbb R^n`$. Take $`\phi_\lambda(q,p)=(q+\lambda k,\,p)`$. Then $`Q_a=q_a+\lambda k_a`$ and $`P_a=p_a`$ satisfy (1.29), and $`\phi_\lambda`$ is a symmetry transformation if and only if $`H(q+\lambda k,p)=H(q,p)`$ for all $`\lambda`$, i.e. $`\sum_ak_a\,\partial H/\partial q_a=0`$. Here $`X=(k,0)`$, and (1.33) holds with

```math
\left.
\boxed{G=\sum_{a=1}^nk_a\,p_a,}
\right.
\tag{1.36}
```

which is therefore conserved.

- For $`k`$ the $`b`$-th unit vector, the condition is $`\partial H/\partial q_b=0`$, and $`p_b`$ is conserved. For example, for $`H=\sum_ap_a^2/2m`$ every $`p_a`$ is conserved.
- For $`N`$ particles, $`q=(\mathbf x_1,\ldots,\mathbf x_N)`$ and $`p=(\mathbf p_1,\ldots,\mathbf p_N)`$, take $`k=(\mathbf e,\ldots,\mathbf e)`$. The conserved quantity is then $`\sum_{A=1}^N\mathbf e\cdot\mathbf p_A`$, the component of the total momentum along $`\mathbf e`$.

<br><br>

<a id="classical-field"></a>
### 1.3 Definition of Classical Fields

<a id="field-definition"></a>
#### Definition of Fields

**Definition**

```math
\left.
\text{Field}:\text{Spacetime}\longrightarrow\text{Vector Space},
\right.
\tag{1.37}
```

```math
\left.
\boxed{\Psi:\mathbb R^4\longrightarrow\mathbb R^n\ \text{or}\ \mathbb C^n
}
\right.
\tag{1.38}
```

Additional regularity conditions, such as $`C^\infty`$ smoothness, may be imposed.

The space of fields $`\{\Psi\}`$ carries a representation of $`ISO(1,3)^+`$. For $`(\Lambda,a)\in ISO(1,3)^+`$,

```math
\left.
\Psi\xrightarrow{\;(\Lambda,a)\;}U(\Lambda,a)\Psi,
\right.
\tag{1.39}
```

where $`U`$ is an infinite-dimensional representation that can be constructed from the finite-dimensional representation $`D(\Lambda)`$:

```math
\left.
\boxed{
\begin{aligned}
[U(\Lambda,a)\Psi]_\alpha(x)
&:=D_{\alpha\beta}(\Lambda)
[(\Lambda,a)_*\Psi]_\beta(x)\\
&=D_{\alpha\beta}(\Lambda)
\Psi_\beta(\Lambda^{-1}x-\Lambda^{-1}a).
\end{aligned}
}
\right.
\tag{1.40}
```

<br><br>

<a id="lorentz-finite-representations"></a>
#### Finite-Dimensional Representations of $`SO(1,3)^+`$

$`U`$ is constructed from $`D`$ by (1.40), and $`D`$ is recovered from $`U`$ through $`[U(\Lambda,0)\Psi](0)=D(\Lambda)\Psi(0)`$. Hence

```math
\left.
\begin{aligned}
\Psi_\alpha(x),\ \alpha=1,\ldots,n
&\quad\Longleftrightarrow\quad\text{infinite-dimensional representation }U(\Lambda,a)\\
&\quad\Longleftrightarrow\quad n\text{-dimensional representation }D(\Lambda)\text{ of }SO(1,3)^+.
\end{aligned}
\right.
\tag{1.41}
```

**Lie Algebra Representations**

For $`X,Y\in\mathfrak o(1,3)`$,

```math
\left.
\rho(X):=\frac{d}{dt}D(e^{tX})\Big|_{t=0},\qquad
D(e^{X})=e^{\rho(X)},\qquad
\rho([X,Y])=[\rho(X),\rho(Y)].
\right.
\tag{1.42}
```

$`SO(1,3)^+`$ is connected, so $`D`$ is determined by $`\rho`$. Extend $`\rho`$ complex-linearly, $`\rho(X+iY):=\rho(X)+i\rho(Y)`$, to the complexified Lie algebra $`\mathfrak o(1,3)_{\mathbb C}`$, defined by (0.32) with $`M_4(\mathbb R)`$ replaced by $`M_4(\mathbb C)`$. By (0.36), $`\mathfrak o(1,3)_{\mathbb C}`$ contains every $`J^{\mu\nu}`$, and $`D(e^{-\frac i2\omega_{\mu\nu}J^{\mu\nu}})=e^{-\frac i2\omega_{\mu\nu}\rho(J^{\mu\nu})}`$. For the Dirac field, $`\rho(J^{\mu\nu})=S^{\mu\nu}`$ (1.100).

**Decomposition of $`\mathfrak o(1,3)_{\mathbb C}`$**

From (0.34),

```math
\left.
[J^i,J^j]=\epsilon_{ijk}J^k,\qquad
[J^i,K^j]=\epsilon_{ijk}K^k,\qquad
[K^i,K^j]=-\epsilon_{ijk}J^k.
\right.
\tag{1.43}
```

Define

```math
\left.
\begin{aligned}
A^i&:=\frac12\Bigl(\frac12\epsilon_{ijk}J^{jk}+iJ^{0i}\Bigr)=\frac i2\bigl(J^i+iK^i\bigr),\\
B^i&:=\frac12\Bigl(\frac12\epsilon_{ijk}J^{jk}-iJ^{0i}\Bigr)=\frac i2\bigl(J^i-iK^i\bigr),
\end{aligned}
\right.
\tag{1.44}
```

i.e. $`A^1=\frac12(J^{23}+iJ^{01})`$, $`A^2=\frac12(J^{31}+iJ^{02})`$, $`A^3=\frac12(J^{12}+iJ^{03})`$, and $`B^i`$ is the same with $`iJ^{0i}\to-iJ^{0i}`$. $`A^i`$ and $`B^i`$ are not real, so they lie in $`\mathfrak o(1,3)_{\mathbb C}`$ but not in $`\mathfrak o(1,3)`$. By (1.43),

```math
\left.
\boxed{[A^i,A^j]=i\epsilon_{ijk}A^k,\qquad
[B^i,B^j]=i\epsilon_{ijk}B^k,\qquad
[A^i,B^j]=0.}
\right.
\tag{1.45}
```

Hence

```math
\left.
\mathfrak o(1,3)_{\mathbb C}=\mathfrak g_A\oplus\mathfrak g_B,\qquad
\mathfrak g_A:=\mathop{\rm span}\nolimits\,_{\mathbb C}\{A^1,A^2,A^3\},\quad
\mathfrak g_B:=\mathop{\rm span}\nolimits\,_{\mathbb C}\{B^1,B^2,B^3\}.
\right.
\tag{1.46}
```

The maps $`A^i\mapsto\sigma^i/2`$ and $`B^i\mapsto\sigma^i/2`$ identify each of $`\mathfrak g_A`$ and $`\mathfrak g_B`$ with the complexification of $`\mathfrak{su}(2)\cong\mathfrak o(3)`$.

**Irreducible Representations**

Take representations $`(\rho_A,V_A)`$ of $`\mathfrak g_A`$ and $`(\rho_B,V_B)`$ of $`\mathfrak g_B`$, with $`n_A:=\dim V_A`$ and $`n_B:=\dim V_B`$. Their tensor (Kronecker) product $`(\rho,V_A\otimes V_B)`$ is, for $`v_A\in\mathfrak g_A`$ and $`v_B\in\mathfrak g_B`$,

```math
\left.
\begin{aligned}
\rho(v_A+v_B)&:=\rho_A(v_A)\otimes I_{n_B}+I_{n_A}\otimes\rho_B(v_B),\\
\rho(v_A+v_B)\bigl(|a\rangle\otimes|b\rangle\bigr)&=\rho_A(v_A)|a\rangle\otimes|b\rangle+|a\rangle\otimes\rho_B(v_B)|b\rangle,\\
e^{\rho(v_A+v_B)}&=e^{\rho_A(v_A)}\otimes e^{\rho_B(v_B)}.
\end{aligned}
\right.
\tag{1.47}
```

The last line holds because the two terms in the first line commute.

The irreducible representations of $`\mathfrak{su}(2)`$ are $`V_j`$ with basis $`|j,m\rangle`$, $`m=-j,\ldots,j`$, on which $`\rho_A(A^3)`$ (or $`\rho_B(B^3)`$) acts as $`m`$. Here $`j=0,\frac12,1,\ldots`$ and $`\dim V_j=2j+1`$. Every finite-dimensional irreducible representation of $`\mathfrak g_A\oplus\mathfrak g_B`$ is $`V_{j_1}\otimes V_{j_2}`$, and every finite-dimensional representation is a direct sum of these:

```math
\left.
\boxed{(j_1,j_2),\qquad j_1,j_2\in\{0,\tfrac12,1,\tfrac32,\ldots\},\qquad\dim=(2j_1+1)(2j_2+1).}
\right.
\tag{1.48}
```

**Rotation by $`2\pi`$**

Since $`A^3+B^3=iJ^3`$ by (1.44), on $`(j_1,j_2)`$

```math
\left.
e^{2\pi J^3}=I_4,\qquad
e^{2\pi\rho(J^3)}=e^{-2\pi i\rho(A^3+B^3)}=(-1)^{2(j_1+j_2)}I_n.
\right.
\tag{1.49}
```

So $`D(e^X):=e^{\rho(X)}`$ is a representation of $`SO(1,3)^+`$ only for integer $`j_1+j_2`$. For half-integer $`j_1+j_2`$ it is defined only up to sign; for the Dirac field, $`\Lambda_{\frac12}=-I_4`$ at $`\theta^3=2\pi`$.

<br><br>

<a id="classical-dynamics"></a>
### 1.4 Dynamics of Classical Fields

<a id="field-theory-lagrangian"></a>
#### Lagrangian

Having defined classical fields, we now turn to their dynamics. In the Lagrangian formalism, this amounts to constructing a Lagrangian density for the fields.
In classical mechanics, the dynamical variables are the generalized coordinates $`q_a(t)`$, which depend only on time. In field theory, the dynamical variables are the field components $`\Psi_\alpha(x)`$, which depend on the spacetime point $`x=(t,\mathbf x)`$.

There are two ways to interpret $`x`$:

1. At fixed time $`t`$, the pair $`(\alpha,\mathbf x)`$ plays the role of the label $`a`$ in $`q_a(t)`$, so $`\Psi_\alpha(t,\mathbf x)`$ corresponds to $`q_a(t)`$.
2. More physically, the whole spacetime point $`x`$ plays the role of $`t`$ in classical mechanics, so $`\Psi_\alpha(x)`$ corresponds to $`q_a(t)`$.

**Definition**

- **Configuration space**: the fields $`\Psi`$, with $`\Psi(x)\in\mathbb R^n`$ or $`\mathbb C^n`$ at each $`x`$.
- **Dynamical structure**: the Lagrangian density, a smooth function

```math
\left.
\begin{aligned}
\mathcal L:(\mathbb R^n\ \text{or}\ \mathbb C^n)\times(\mathbb R^n\ \text{or}\ \mathbb C^n)^4&\to\mathbb R,\\
(\Psi_\alpha,\partial_\mu\Psi_\alpha)&\mapsto\mathcal L(\Psi_\alpha,\partial_\mu\Psi_\alpha),
\end{aligned}
\right.
\tag{1.50}
```

in which $`\partial_\mu\Psi_\alpha`$ are independent variables, with no explicit dependence on $`x`$.

- **Action**: the functional on fields, for any bounded region $`\Omega\subset\mathbb R^4`$,

```math
\left.
\boxed{S[\Psi]:=\int_\Omega d^4x\,\mathcal L\bigl(\Psi_\alpha(x),\partial_\mu\Psi_\alpha(x)\bigr).}
\right.
\tag{1.51}
```

- **Solutions**: fields $`\Psi`$ at which $`S`$ is stationary under variations vanishing on $`\partial\Omega`$,

```math
\left.
\frac{d}{ds}S[\Psi+s\eta]\Big|_{s=0}=0,
\right.
\tag{1.52}
```

for every smooth $`\eta`$ with $`\eta|_{\partial\Omega}=0`$ and every $`\Omega`$.

**Conditions on the Lagrangian Density**

For the local relativistic field theories considered here, we require:

- **Lorentz invariance:** the action constructed from $`\mathcal L`$ is a Lorentz scalar.
- **Reality:** the Lagrangian density $`\mathcal L`$ is real.
- **Locality:** $`\mathcal L`$ depends only on the fields and finitely many of their derivatives at the same spacetime point.

Further mathematical restrictions may be imposed as conventional choices rather than universal axioms; ultimately, the essential requirement is agreement with physical reality, so that the Lagrangian describes or explains at least part of the real world.




**Euler–Lagrange Equations**

As in (1.5), integrating by parts in (1.52) and using $`\eta|_{\partial\Omega}=0`$, $`\Psi`$ is a solution if and only if

```math
\left.
\boxed{\partial_\mu\frac{\partial\mathcal L}{\partial(\partial_\mu\Psi_\alpha)}
-\frac{\partial\mathcal L}{\partial\Psi_\alpha}=0.}
\right.
\tag{1.53}
```

**Hamiltonian Formulation**

For a regular Legendre transformation,

```math
\left.
\begin{aligned}
\pi_\alpha&:=\frac{\partial\mathcal L}{\partial\dot\Psi_\alpha},
&
\mathcal H&:=\pi_\alpha\dot\Psi_\alpha-\mathcal L,
&
H&=\int d^3x\,\mathcal H,\\
\dot\Psi_\alpha(t,\mathbf x)&=\frac{\delta H}{\delta\pi_\alpha(t,\mathbf x)},
&
\dot\pi_\alpha(t,\mathbf x)&=-\frac{\delta H}{\delta\Psi_\alpha(t,\mathbf x)}.
\end{aligned}
\right.
\tag{1.54}
```

<br><br>

<a id="classical-noether"></a>
#### Symmetry Transformations and Noether's Theorem

**Transformations**

- **Transformation**: a one-parameter family $`\phi_\lambda`$ with $`\phi_0=\mathrm{id}`$, acting on spacetime and on the field,

```math
\left.
\begin{aligned}
\phi_\lambda:\mathbb R^4&\to\mathbb R^4,\\
x&\mapsto x'=\phi_\lambda(x),
\end{aligned}
\qquad
x'^\mu=:x^\mu+\delta x^\mu,\qquad
\Psi\mapsto\Psi',
\right.
\tag{1.55}
```

where the form of $`\Psi'`$ is given in (1.58) and (1.66): for $`\phi_\lambda=(\Lambda,a)`$ a Poincaré transformation, $`\Psi'=U(\Lambda,a)\Psi`$ of (1.40); for an internal transformation, $`x'=x`$ and $`\Psi'=g(\lambda)\Psi`$.

**Symmetry Transformations**

- **Symmetry transformation**: a transformation under which the action of every field is invariant for every region,

```math
\left.
\boxed{S'=S\quad\text{for every }\Psi\text{ and every }\Omega,}
\right.
\tag{1.56}
```

with $`S'`$ the action of $`\Psi'`$ over $`\phi_\lambda(\Omega)`$, written out in (1.60).

**Conserved Quantities**

- **Conserved quantity**: a functional $`\mathcal Q[\Psi,t]`$ of the field and its derivatives on the time slice $`t`$, such that $`\mathcal Q[\Psi,t]`$ is independent of $`t`$ for every solution $`\Psi`$ that, together with its first derivatives, falls off fast enough at spatial infinity.

**Noether's Theorem**

If $`\phi_\lambda`$ is a symmetry transformation, then

```math
\left.
\boxed{
\mathcal Q[\Psi,t]:=\int d^3x\left(
\frac{\partial\mathcal L}{\partial\dot\Psi_\alpha}
\frac{\partial\,\delta x^\nu}{\partial\lambda}
\partial_\nu\Psi_\alpha
-\frac{\partial\mathcal L}{\partial\dot\Psi_\alpha}
\frac{\partial\,\delta_0\Psi_\alpha}{\partial\lambda}
-\mathcal L\frac{\partial\,\delta x^0}{\partial\lambda}
\right)
}
\right.
\tag{1.57}
```

is a conserved quantity, where $`\delta_0\Psi_\alpha`$ is defined in (1.58), the derivatives with respect to $`\lambda`$ are taken at $`\lambda=0`$, and the fall-off condition makes the integral converge and the surface term in (1.64) vanish.

**Proof**

**(A) Coordinate Transformation**

Let $`x'=\phi_\lambda(x)`$, with $`\lambda`$ infinitesimal. Define two field variations:

```math
\left.
\begin{aligned}
\delta_0\Psi_\alpha(x)
&:=\Psi'_\alpha(x')-\Psi_\alpha(x)
=D_{\alpha\beta}(\Lambda)\Psi_\beta(x)-\Psi_\alpha(x),\\
\delta\Psi_\alpha(x)
&:=\Psi'_\alpha(x)-\Psi_\alpha(x)
=[U(\Lambda,a)\Psi]_\alpha(x)-\Psi_\alpha(x).
\end{aligned}
\right.
\tag{1.58}
```

Here $`\Psi'`$ is the transformed field. Using the pushforward $`(\phi_\lambda)_*\Psi:=\Psi\circ\phi_\lambda^{-1}`$, we write $`\Psi'_\alpha=D_{\alpha\beta}(\Lambda)\,[(\phi_\lambda)_*\Psi]_\beta`$. Evaluating at $`x'`$ gives $`\Psi'_\alpha(x')=D_{\alpha\beta}(\Lambda)\Psi_\beta(x)`$, which is the last equality in the first line, so the first variation, $`\delta_0\Psi_\alpha`$, describes the transformation of the field itself. For $`\phi_\lambda=(\Lambda,a)`$, $`\Psi'=U(\Lambda,a)\Psi`$ by (1.40), which is the last equality in the second line. If $`\phi_\lambda`$ is not a Poincaré transformation, $`D(\Lambda)`$ is replaced by the identity and $`\delta_0\Psi_\alpha=0`$.

To first order in $`\lambda`$, the two variations are related by

```math
\left.
\begin{aligned}
\delta\Psi_\alpha(x)
&=\bigl[\Psi'_\alpha(x')-\Psi_\alpha(x)\bigr]
-\bigl[\Psi'_\alpha(x')-\Psi'_\alpha(x)\bigr]\\
&=\delta_0\Psi_\alpha(x)-\delta x^\mu\partial_\mu\Psi'_\alpha(x)\\
&=\delta_0\Psi_\alpha(x)-\delta x^\mu\partial_\mu\Psi_\alpha(x),
\end{aligned}
\right.
\tag{1.59}
```

where the last step uses $`\Psi'_\alpha=\Psi_\alpha+O(\lambda)`$.

Over a spacetime region $`\Omega`$, the actions before and after the transformation are

```math
\left.
\begin{aligned}
S&=\int_\Omega d^4x\,
\mathcal L\bigl(\Psi_\alpha(x),\partial_\mu\Psi_\alpha(x)\bigr),\\
S'&=\int_{\phi_\lambda(\Omega)}d^4x'\,
\mathcal L\bigl(\Psi'_\alpha(x'),\partial'_\mu\Psi'_\alpha(x')\bigr),
\end{aligned}
\right.
\tag{1.60}
```

where $`\partial'_\mu:=\partial/\partial x'^\mu`$. The same function $`\mathcal L`$ is used in $`S'`$: the transformation acts on the field configuration and on the region $`\Omega`$, not on the Lagrangian. No property of $`\mathcal L`$ is assumed here.

Change the integration variable in $`S'`$ from $`x'`$ back to $`x`$, so that $`\phi_\lambda(\Omega)`$ becomes $`\Omega`$. To first order in $`\lambda`$,

```math
\left.
\begin{aligned}
d^4x'
&=\det\!\left(\frac{\partial x'^\mu}{\partial x^\nu}\right)d^4x
=\bigl(1+\partial_\mu\delta x^\mu\bigr)d^4x,\\
\partial'_\mu
&=\frac{\partial x^\nu}{\partial x'^\mu}\partial_\nu
=\partial_\mu-(\partial_\mu\delta x^\nu)\partial_\nu,\\
\Psi'_\alpha(x')
&=\Psi_\alpha(x)+\delta_0\Psi_\alpha(x),\\
\partial'_\mu\Psi'_\alpha(x')
&=\partial_\mu\Psi_\alpha(x)
+\partial_\mu\delta_0\Psi_\alpha(x)
-(\partial_\mu\delta x^\nu)\partial_\nu\Psi_\alpha(x),
\end{aligned}
\right.
\tag{1.61}
```

where the third line is (1.58). Hence

```math
\left.
S'=\int_\Omega d^4x\,
\bigl(1+\partial_\mu\delta x^\mu\bigr)\,
\mathcal L\bigl(
\Psi_\alpha+\delta_0\Psi_\alpha,\ 
\partial_\mu\Psi_\alpha
+\partial_\mu\delta_0\Psi_\alpha
-(\partial_\mu\delta x^\nu)\partial_\nu\Psi_\alpha
\bigr).
\right.
\tag{1.62}
```

Expanding (1.62) to first order in $`\lambda`$ gives the off-shell identity

```math
\left.
\begin{aligned}
S'-S
&=\int_\Omega d^4x\,\biggl[
\mathcal L\,\partial_\mu\delta x^\mu
+\frac{\partial\mathcal L}{\partial\Psi_\alpha}\delta_0\Psi_\alpha\\
&\qquad
+\frac{\partial\mathcal L}{\partial(\partial_\mu\Psi_\alpha)}
\bigl(\partial_\mu\delta_0\Psi_\alpha-(\partial_\mu\delta x^\nu)\partial_\nu\Psi_\alpha\bigr)
\biggr]\\
&=\int_\Omega d^4x\,\biggl\{
\biggl[
\frac{\partial\mathcal L}{\partial\Psi_\alpha}
-\partial_\mu\frac{\partial\mathcal L}{\partial(\partial_\mu\Psi_\alpha)}
\biggr]\delta\Psi_\alpha\\
&\qquad
+\partial_\mu\biggl[
\mathcal L\,\delta x^\mu
+\frac{\partial\mathcal L}{\partial(\partial_\mu\Psi_\alpha)}\delta\Psi_\alpha
\biggr]
\biggr\}.
\end{aligned}
\right.
\tag{1.63}
```

The second equality substitutes $`\delta_0\Psi_\alpha=\delta\Psi_\alpha+\delta x^\nu\partial_\nu\Psi_\alpha`$ from (1.59) and uses the product rule together with $`\partial_\nu\mathcal L=\frac{\partial\mathcal L}{\partial\Psi_\alpha}\partial_\nu\Psi_\alpha+\frac{\partial\mathcal L}{\partial(\partial_\mu\Psi_\alpha)}\partial_\nu\partial_\mu\Psi_\alpha`$; the latter holds because $`\mathcal L`$ has no explicit $`x`$-dependence.

By hypothesis, the action is invariant: $`S'=S`$. Take $`\Omega=[t_1,t_2]\times V`$ and let $`\Psi_\alpha`$ satisfy the Euler–Lagrange equations, so that the Euler–Lagrange term in (1.63) vanishes. Gauss's theorem then gives

```math
\left.
\begin{aligned}
0
&=\int_\Omega d^4x\,\partial_\mu\biggl[
\mathcal L\,\delta x^\mu
+\frac{\partial\mathcal L}{\partial(\partial_\mu\Psi_\alpha)}\delta\Psi_\alpha
\biggr]\\
&=\biggl[\int_V d^3x\,\biggl(
\mathcal L\,\delta x^0
+\frac{\partial\mathcal L}{\partial\dot\Psi_\alpha}\delta\Psi_\alpha
\biggr)\biggr]_{t_1}^{t_2}\\
&\quad
+\int_{t_1}^{t_2}dt\oint_{\partial V}dS_i\,\biggl(
\mathcal L\,\delta x^i
+\frac{\partial\mathcal L}{\partial(\partial_i\Psi_\alpha)}\delta\Psi_\alpha
\biggr).
\end{aligned}
\right.
\tag{1.64}
```

By the fall-off condition, the surface term vanishes as $`V\to\mathbb R^3`$. Since $`t_1`$ and $`t_2`$ are arbitrary,

```math
\left.
\int d^3x\,\biggl(
\mathcal L\,\delta x^0
+\frac{\partial\mathcal L}{\partial\dot\Psi_\alpha}\delta\Psi_\alpha
\biggr)=\text{const}.
\right.
\tag{1.65}
```

Substituting $`\delta\Psi_\alpha=\delta_0\Psi_\alpha-\delta x^\nu\partial_\nu\Psi_\alpha`$ from (1.59), differentiating with respect to $`\lambda`$, and reversing the overall sign gives (1.57) for coordinate transformations.

**(B) Internal Transformation**

Now $`\phi_\lambda`$ acts trivially on spacetime, and on the field by a constant matrix $`g(\lambda)`$ with $`g(0)=I_n`$:

```math
\left.
x'^\mu=x^\mu,\qquad
\Psi'_\alpha(x)=g_{\alpha\beta}(\lambda)\,\Psi_\beta(x).
\right.
\tag{1.66}
```

Hence $`\delta x^\mu=0`$, and the two variations in (1.58) coincide: $`\delta\Psi_\alpha(x)=\delta_0\Psi_\alpha(x)=g_{\alpha\beta}(\lambda)\Psi_\beta(x)-\Psi_\alpha(x)`$. Repeating (1.60)–(1.65) with $`\delta x^\mu=0`$: in (1.61), $`d^4x'=d^4x`$ and $`\partial'_\mu=\partial_\mu`$; the terms containing $`\delta x^\mu`$ drop out of (1.62)–(1.64); and (1.65) becomes

```math
\left.
\int d^3x\,\frac{\partial\mathcal L}{\partial\dot\Psi_\alpha}\,\delta_0\Psi_\alpha=\text{const}.
\right.
\tag{1.67}
```

Differentiating with respect to $`\lambda`$ and reversing the overall sign gives (1.57) with $`\delta x^\mu=0`$. $`\square`$

<a id="spacetime-conserved-quantities"></a>
**(1) Spacetime Translations and Energy–Momentum**

Take $`\phi_\lambda(x)=x+\lambda\epsilon`$ for a fixed $`\epsilon\in\mathbb R^4`$, so that $`\delta x^\mu=\lambda\epsilon^\mu`$, $`\Lambda=I_4`$ and $`\delta_0\Psi_\alpha=0`$. By (1.60)–(1.62), $`S'=S`$ holds because $`\mathcal L`$ has no explicit $`x`$-dependence, and (1.57) gives

```math
\left.
\mathcal Q=\epsilon^\nu\int d^3x\Bigl(\frac{\partial\mathcal L}{\partial\dot\Psi_\alpha}\partial_\nu\Psi_\alpha-\delta^0{}_\nu\mathcal L\Bigr)=\epsilon^\nu P_\nu,
\right.
\tag{1.68}
```

with the canonical energy–momentum tensor and four-momentum

```math
\left.
\boxed{
\begin{aligned}
T^\mu{}_\nu&:=\frac{\partial\mathcal L}{\partial(\partial_\mu\Psi_\alpha)}
\,\partial_\nu\Psi_\alpha-\delta^\mu{}_\nu\mathcal L,
&
\partial_\mu T^\mu{}_\nu&=0,\\
P_\nu&:=\int d^3x\,T^0{}_\nu,
&
\frac{dP_\nu}{dt}&=0,
&
P_0&=H.
\end{aligned}}
\right.
\tag{1.69}
```

Here $`\partial_\mu T^\mu{}_\nu=0`$ holds on shell by (1.53), and $`P_0=H`$ by (1.54).

<br><br>

<a id="dirac-constraint"></a>
### 1.5 Dirac Constraint

<a id="singular-lagrangian"></a>
#### Singular Lagrangians

**Definition**

Let $`L:\mathrm{Conf}\times\mathbb R^n\to\mathbb R`$ be a smooth Lagrangian as in (1.2), without explicit time dependence.

- **Canonical momenta**:

```math
\left.
p_a:=\frac{\partial L}{\partial\dot q_a}(q,\dot q),\qquad a=1,\ldots,n.
\right.
\tag{1.70}
```

- **Hessian**: the symmetric matrix

```math
\left.
W_{ab}:=\frac{\partial^2L}{\partial\dot q_a\,\partial\dot q_b}(q,\dot q),\qquad a,b=1,\ldots,n.
\right.
\tag{1.71}
```

- **Regular and singular Lagrangians**: $`L`$ is regular if $`\det W\neq0`$ on $`\mathrm{Conf}\times\mathbb R^n`$, and singular otherwise. For a singular $`L`$ we assume that $`\mathop{\rm rank}\nolimits\,W=r<n`$ is constant.

If $`L`$ is regular, (1.70) can be solved for the velocities, $`\dot q=\dot q(q,p)`$, and

```math
\left.
H(q,p):=\sum_{a=1}^np_a\,\dot q_a(q,p)-L\bigl(q,\dot q(q,p)\bigr)
\right.
\tag{1.72}
```

is the Hamiltonian (1.24) of [Section 1.2](#hamiltonian-formalism). In the rest of this section $`L`$ is singular.

**Primary Constraints**

Since $`W`$ is symmetric, its rank equals the order of its largest invertible principal submatrix, so after reordering the coordinates

```math
\left.
\det\bigl(W_{ab}\bigr)_{a,b=1}^{r}\neq0.
\right.
\tag{1.73}
```

Indices $`\mu,\nu`$ run over the remaining values $`r+1,\ldots,n`$. By the implicit function theorem, the first $`r`$ equations of (1.70) can be solved locally for $`\dot q_1,\ldots,\dot q_r`$:

```math
\left.
\dot q_a=\varphi_a(q,p_b,\dot q_\mu),\qquad a=1,\ldots,r,
\right.
\tag{1.74}
```

where $`p_b`$ and $`\dot q_\mu`$ stand for $`(p_1,\ldots,p_r)`$ and $`(\dot q_{r+1},\ldots,\dot q_n)`$. Substituting (1.74) into the remaining equations of (1.70) gives

```math
\left.
p_\mu=\frac{\partial L}{\partial\dot q_\mu}\bigl(q,\varphi(q,p_b,\dot q_\nu),\dot q_\nu\bigr)=:g_\mu(q,p_b),
\right.
\tag{1.75}
```

and $`g_\mu`$ does not depend on $`\dot q_\nu`$: differentiating the identity $`p_b=\frac{\partial L}{\partial\dot q_b}(q,\varphi,\dot q_\nu)`$ with respect to $`\dot q_\nu`$ gives $`\sum_{a=1}^rW_{ba}\frac{\partial\varphi_a}{\partial\dot q_\nu}=-W_{b\nu}`$, hence

```math
\left.
\frac{\partial}{\partial\dot q_\nu}\frac{\partial L}{\partial\dot q_\mu}\bigl(q,\varphi,\dot q\bigr)
=W_{\mu\nu}+\sum_{a=1}^rW_{\mu a}\frac{\partial\varphi_a}{\partial\dot q_\nu}
=W_{\mu\nu}-\sum_{a,b=1}^rW_{\mu a}\bigl(W^{-1}\bigr)_{ab}W_{b\nu}=0,
\right.
\tag{1.76}
```

with $`(W^{-1})_{ab}`$ the inverse of the block (1.73). The last expression is the Schur complement of that block in $`W`$, which vanishes since $`\mathop{\rm rank}\nolimits\,W=r`$.

- **Primary constraints**:

```math
\left.
\boxed{\chi_\mu(q,p):=p_\mu-g_\mu(q,p_b)=0,\qquad\mu=r+1,\ldots,n.}
\right.
\tag{1.77}
```

The $`n`$ equations (1.70) are equivalent to (1.74) together with (1.77). The constraints (1.77) involve only $`(q,p)`$ and define the constraint surface in phase space, the image of the map $`(q,\dot q)\mapsto(q,p(q,\dot q))`$.

- **Weak equality**: $`F\approx G`$ means that the phase-space functions $`F`$ and $`G`$ agree on the constraint surface.

**Canonical Hamiltonian**

Define

```math
\left.
H_c:=\sum_{a=1}^np_a\dot q_a-L(q,\dot q),
\right.
\tag{1.78}
```

with (1.74) substituted for $`\dot q_1,\ldots,\dot q_r`$, so that $`H_c`$ is a function of $`(q,p,\dot q_\mu)`$. By (1.74), (1.75) and (1.77),

```math
\left.
\frac{\partial H_c}{\partial\dot q_\nu}
=\sum_{a=1}^r\Bigl(p_a-\frac{\partial L}{\partial\dot q_a}\Bigr)\frac{\partial\varphi_a}{\partial\dot q_\nu}
+p_\nu-\frac{\partial L}{\partial\dot q_\nu}
=\chi_\nu(q,p),
\right.
\tag{1.79}
```

which is independent of $`\dot q_\mu`$ and vanishes on the constraint surface. Hence $`H_c`$ is independent of $`\dot q_\mu`$ on the constraint surface, where by (1.77) it is a function of $`(q,p_1,\ldots,p_r)`$ alone.

**Total Hamiltonian and Consistency**

Let $`H_c`$ be the canonical Hamiltonian and $`u^A`$ the Lagrange multipliers enforcing the primary constraints.

```math
\left.
\boxed{
\begin{aligned}
H_T&=H_c+\sum_A u^A(t)\chi_A^{(1)},\\
\dot\chi_A&=\frac{\partial\chi_A}{\partial t}
+\{\chi_A,H_T\}_{\mathrm{PB}}\approx0.
\end{aligned}}
\right.
\tag{1.80}
```

Consistency may yield secondary and higher constraints, fix multipliers, or hold identically. Iterate until closure.

**First-Class and Second-Class Constraints**

```math
\left.
\{F,G\}_{\mathrm{PB}}
:=\sum_{a=1}^n\left(
\frac{\partial F}{\partial q_a}\frac{\partial G}{\partial p_a}
-\frac{\partial F}{\partial p_a}\frac{\partial G}{\partial q_a}
\right),
\qquad
\{q_a,p_b\}_{\mathrm{PB}}=\delta_{ab}.
\right.
\tag{1.81}
```

A constraint is first class if its Poisson bracket with every constraint vanishes weakly. After separating all first-class combinations, the remaining second-class constraints $`\chi_a^{\mathrm{sc}}`$ have an invertible bracket matrix:

```math
\left.
\{\chi^{\mathrm{fc}},\chi_A\}_{\mathrm{PB}}\approx0
\quad\text{for all }A,
\qquad
C_{ab}:=\{\chi_a^{\mathrm{sc}},\chi_b^{\mathrm{sc}}\}_{\mathrm{PB}},
\qquad
\det C\ne0.
\right.
\tag{1.82}
```

**Dirac Bracket**

```math
\left.
\boxed{
\begin{aligned}
\{F,G\}_{\mathrm D}
&:=\{F,G\}_{\mathrm{PB}}
-\sum_{a,b}\{F,\chi_a^{\mathrm{sc}}\}_{\mathrm{PB}}
(C^{-1})_{ab}\{\chi_b^{\mathrm{sc}},G\}_{\mathrm{PB}},\\
\{F,\chi_a^{\mathrm{sc}}\}_{\mathrm D}&=0.
\end{aligned}}
\right.
\tag{1.83}
```

Second-class constraints may then be imposed strongly. For fields, use functional derivatives, spatial integrals, and inverse integral kernels.

**Physical Degrees of Freedom**

For a regular system with independent constraints and gauge orbits of the expected dimension,

```math
\left.
\boxed{
N_{\mathrm{physical}}
=n-N_{\mathrm{first}}-\frac12N_{\mathrm{second}}.
}
\right.
\tag{1.84}
```

For fields, this counts local configuration degrees of freedom per spatial point, subject to boundary and zero-mode qualifications.


<br><br>
<a id="scalar-field"></a>
### 1.6 The Scalar Field

<a id="scalar-lagrangian"></a>
#### Lagrangian

**Real Scalar Field**

```math
\left.
\boxed{
\mathcal L=\frac12\partial_\mu\phi\,\partial^\mu\phi-V(\phi),
\qquad
\partial_\mu\partial^\mu\phi+V'(\phi)=0.
}
\qquad
V(\phi)=\frac12m^2\phi^2
\ \Longrightarrow\
(\partial_\mu\partial^\mu+m^2)\phi=0.
\right.
\tag{1.85}
```

```math
\left.
\pi=\dot\phi,
\qquad
\boxed{
\mathcal H=\frac12\pi^2+\frac12|\boldsymbol\nabla\phi|^2+V(\phi),
\qquad
H=\int d^3x\,\mathcal H.
}
\right.
\tag{1.86}
```

**Complex Scalar Field**

Treat $`\phi`$ and $`\phi^*`$ as independent variables:

```math
\left.
\boxed{
\begin{aligned}
\mathcal L&=\partial_\mu\phi^*\partial^\mu\phi-m^2\phi^*\phi,\\
(\partial_\mu\partial^\mu+m^2)\phi&=0,\qquad
(\partial_\mu\partial^\mu+m^2)\phi^*=0,\\
\pi_\phi&=\dot\phi^*,\qquad \pi_{\phi^*}=\dot\phi,\\
\mathcal H&=\pi_\phi\pi_{\phi^*}
+|\boldsymbol\nabla\phi|^2+m^2|\phi|^2.
\end{aligned}}
\right.
\tag{1.87}
```

**Conserved Quantities: Spacetime Symmetries**

Translations give the canonical energy–momentum tensor in (1.69):

```math
\left.
\boxed{\begin{aligned}
T^\mu{}_\nu&=\partial^\mu\phi\,\partial_\nu\phi-\delta^\mu{}_\nu\mathcal L
&&\text{(real field)},\\
T^\mu{}_\nu&=\partial^\mu\phi^*\,\partial_\nu\phi
+\partial^\mu\phi\,\partial_\nu\phi^*-\delta^\mu{}_\nu\mathcal L
&&\text{(complex field)},\\
\partial_\mu T^\mu{}_\nu&=0,\qquad
P_\nu=\int d^3x\,T^0{}_\nu,\qquad \frac{dP_\nu}{dt}=0.
\end{aligned}}
\right.
\tag{1.88}
```

For either field, $`T^{\mu\nu}:=T^\mu{}_\rho\eta^{\rho\nu}`$ is symmetric. Lorentz symmetry gives the rotation and boost charges

```math
\left.
\boxed{
J^{\mu\nu}=\int d^3x\,
\bigl(x^\mu T^{0\nu}-x^\nu T^{0\mu}\bigr),
\qquad
\frac{dJ^{\mu\nu}}{dt}=0.
}
\right.
\tag{1.89}
```

Here $`P_0`$ is the energy, $`P^i`$ are the spatial momenta, $`J^{ij}`$ generate rotations, and $`J^{0i}`$ generate boosts. These conservation laws hold on shell, with convergent integrals and vanishing boundary fluxes.

**Conserved Quantities: Internal and Gauge Symmetries**

The real scalar field has no $`U(1)`$ phase symmetry of the complex-field type. The complex Lagrangian (1.87) has a global $`U(1)`$ symmetry; it is not invariant under an arbitrary local phase $`\lambda(x)`$ without a gauge field. For constant $`\lambda`$, the conserved current and charge are

```math
\left.
\phi'=e^{i\lambda}\phi,
\qquad
\boxed{
j^\mu=i\bigl(\phi^*\partial^\mu\phi-\phi\,\partial^\mu\phi^*\bigr),
\qquad
\partial_\mu j^\mu=0,
\qquad
Q=\int d^3x\,j^0.
}
\right.
\tag{1.90}
```


<br><br>

<a id="scalar-field-solutions"></a>
#### Solutions of the Klein–Gordon Equation

For the real field take $`V(\phi)=\tfrac12m^2\phi^2`$; the complex field in (1.87) is already free. Define $`\Box:=\partial_\mu\partial^\mu`$. A plane wave obeys

```math
\left.
(\Box+m^2)e^{\mp ip\cdot x}=(m^2-p^2)e^{\mp ip\cdot x}=0,
\qquad
p^2=m^2,\qquad
p^0=E_{\mathbf p}:=\sqrt{\mathbf p^2+m^2}>0.
\right.
\tag{1.91}
```

Using the Lorentz-invariant measure written explicitly below, a real wave packet has the expansion

```math
\left.
\boxed{
\phi(x)=\int\frac{d^3p}{(2\pi)^3\,2E_{\mathbf p}}
\left[a(\mathbf p)e^{-ip\cdot x}+a^*(\mathbf p)e^{+ip\cdot x}\right].
}
\right.
\tag{1.92}
```

For a complex field the two frequency amplitudes are independent:

```math
\left.
\boxed{\begin{aligned}
\phi(x)&=\int\frac{d^3p}{(2\pi)^3\,2E_{\mathbf p}}
\left[a(\mathbf p)e^{-ip\cdot x}+b^*(\mathbf p)e^{+ip\cdot x}\right],\\
\phi^*(x)&=\int\frac{d^3p}{(2\pi)^3\,2E_{\mathbf p}}
\left[a^*(\mathbf p)e^{+ip\cdot x}+b(\mathbf p)e^{-ip\cdot x}\right].
\end{aligned}}
\right.
\tag{1.93}
```

The coefficients are classical complex amplitudes. The real-field condition is $`b=a`$. These free-field expansions do not apply to a general nonlinear potential $`V(\phi)`$.

<br><br>

<a id="dirac-field"></a>
### 1.7 The Dirac Field $`\psi`$

<a id="dirac-lagrangian"></a>
#### Lagrangian

The Lagrangian of the Dirac Field has the following form:

```math
\left.
\boxed{
\mathcal L=\bar\psi\bigl(i\gamma^\mu\partial_\mu-m\bigr)\psi,
}
\right.
\tag{1.94}
```

where $`\psi:\mathbb R^4\to\mathbb C^4`$ is the Dirac field, $`\bar\psi:=\psi^\dagger\gamma^0`$ is its Dirac adjoint, the $`\gamma^\mu`$ are given by (0.10), and $`m`$ is the mass. 

Treating $`\psi`$ and $`\bar\psi`$ as independent, the Euler–Lagrange equations give the Dirac equation and its adjoint:

```math
\left.
\boxed{\begin{aligned}
\bigl(i\gamma^\mu\partial_\mu-m\bigr)\psi&=0,\\
i(\partial_\mu\bar\psi)\gamma^\mu+m\bar\psi&=0.
\end{aligned}}
\right.
\tag{1.95}
```

**Hamiltonian**

Treating $`\psi`$ and $`\bar\psi`$ as independent, their conjugate momenta are

```math
\left.
\boxed{\begin{aligned}
\pi_\psi&:=\frac{\partial\mathcal L}{\partial\dot\psi}
=i\bar\psi\gamma^0=i\psi^\dagger,\\
\pi_{\bar\psi}&:=\frac{\partial\mathcal L}{\partial\dot{\bar\psi}}=0.
\end{aligned}}
\right.
\tag{1.96}
```

**Conserved Quantities: Spacetime Symmetries**

Translations give the canonical energy–momentum tensor and four-momentum

```math
\left.
\boxed{\begin{aligned}
T^\mu{}_\nu&=i\bar\psi\gamma^\mu\partial_\nu\psi-\delta^\mu{}_\nu\mathcal L,
&\partial_\mu T^\mu{}_\nu&=0,\\
P_\nu&=\int d^3x\,T^0{}_\nu,
&\frac{dP_\nu}{dt}&=0.
\end{aligned}}
\right.
\tag{1.97}
```

With $`T^{\mu\nu}:=T^\mu{}_\rho\eta^{\rho\nu}`$, Lorentz symmetry gives

```math
\left.
\boxed{\begin{aligned}
J^{\mu\nu}&=\int d^3x\left[
x^\mu T^{0\nu}-x^\nu T^{0\mu}
+\frac{i}{4}\psi^\dagger[\gamma^\mu,\gamma^\nu]\psi
\right],\\
\frac{dJ^{\mu\nu}}{dt}&=0.
\end{aligned}}
\right.
\tag{1.98}
```

The last term is the spin contribution. $`J^{ij}`$ and $`J^{0i}`$ are the rotation and boost charges. Conservation holds on shell, with convergent integrals and vanishing boundary fluxes.

**Conserved Quantities: Internal and Gauge Symmetries**

The free Dirac Lagrangian has a global $`U(1)`$ symmetry. For constant $`\lambda`$,

```math
\left.
\boxed{\begin{aligned}
\psi'&=e^{i\lambda}\psi,\qquad
\bar\psi'=e^{-i\lambda}\bar\psi,\\
j^\mu&=\bar\psi\gamma^\mu\psi,\qquad \partial_\mu j^\mu=0,\\
Q&=\int d^3x\,j^0=\int d^3x\,\psi^\dagger\psi,
\qquad \frac{dQ}{dt}=0.
\end{aligned}}
\right.
\tag{1.99}
```

For a local phase $`\lambda(x)`$, $`\mathcal L'=\mathcal L-j^\mu\partial_\mu\lambda`$; local gauge invariance requires coupling to a gauge field.

<br><br>

<a id="weyl-spinor-solutions"></a>
#### Solutions of the Dirac Equation in the Weyl Representation

**Spinor Representation of the Lorentz Group**

For the Dirac field, $`D(\Lambda)`$ in (1.40) is

```math
\left.
\Lambda_{\frac12}=\exp\Bigl(-\frac i2\omega_{\mu\nu}S^{\mu\nu}\Bigr),
\qquad
S^{\mu\nu}:=\frac i4[\gamma^\mu,\gamma^\nu],
\right.
\tag{1.100}
```

with the same $`\omega_{\mu\nu}`$ as in (0.35). In the Weyl representation every $`S^{\mu\nu}`$ is block diagonal:

```math
\left.
S^{0i}=-\frac i2\begin{pmatrix}\sigma^i&0\\0&-\sigma^i\end{pmatrix},
\qquad
S^{ij}=\frac12\epsilon^{ijk}\begin{pmatrix}\sigma^k&0\\0&\sigma^k\end{pmatrix}.
\right.
\tag{1.101}
```

The noncompact Lorentz group $`SO(1,3)^+`$ has no nontrivial finite-dimensional unitary representations; in the Weyl representation, $`(S^{0i})^\dagger=-S^{0i}`$, so the finite boost matrices for nonzero rapidity are not unitary.

Hence $`\Lambda_{\frac12}`$ is block diagonal: writing $`\psi=\begin{pmatrix}\psi_L\\\psi_R\end{pmatrix}`$, the left-handed and right-handed Weyl spinors $`\psi_L,\psi_R`$ transform independently. For an infinitesimal transformation, with $`\omega_{ij}=\epsilon_{ijk}\theta^k`$ and $`\omega_{0i}=b^i`$ as in (0.34),

```math
\left.
\begin{aligned}
\Lambda_{\frac12}
&\simeq I_4-\frac i2\omega_{\mu\nu}S^{\mu\nu}\\
&=I_4-\frac i2\begin{pmatrix}\boldsymbol\theta\cdot\boldsymbol\sigma&0\\0&\boldsymbol\theta\cdot\boldsymbol\sigma\end{pmatrix}
-i\Bigl(-\frac i2\Bigr)\begin{pmatrix}\mathbf b\cdot\boldsymbol\sigma&0\\0&-\mathbf b\cdot\boldsymbol\sigma\end{pmatrix}\\
&=\begin{pmatrix}I_2-i\boldsymbol\theta\cdot\frac{\boldsymbol\sigma}2-\mathbf b\cdot\frac{\boldsymbol\sigma}2&0\\0&I_2-i\boldsymbol\theta\cdot\frac{\boldsymbol\sigma}2+\mathbf b\cdot\frac{\boldsymbol\sigma}2\end{pmatrix},
\end{aligned}
\right.
\tag{1.102}
```

so that

```math
\left.
\begin{aligned}
\psi_L&\xrightarrow{\ \Lambda\ }\Bigl(I_2-i\boldsymbol\theta\cdot\frac{\boldsymbol\sigma}2-\mathbf b\cdot\frac{\boldsymbol\sigma}2\Bigr)\psi_L,\\
\psi_R&\xrightarrow{\ \Lambda\ }\Bigl(I_2-i\boldsymbol\theta\cdot\frac{\boldsymbol\sigma}2+\mathbf b\cdot\frac{\boldsymbol\sigma}2\Bigr)\psi_R.
\end{aligned}
\right.
\tag{1.103}
```

In terms of $`\psi_L,\psi_R`$, the Dirac equation (1.95) reads

```math
\left.
\begin{pmatrix}-m&i\sigma^\mu\partial_\mu\\i\bar\sigma^\mu\partial_\mu&-m\end{pmatrix}
\begin{pmatrix}\psi_L\\\psi_R\end{pmatrix}=0
\quad\Longleftrightarrow\quad
\begin{cases}
i\sigma^\mu\partial_\mu\psi_R-m\psi_L=0,\\
i\bar\sigma^\mu\partial_\mu\psi_L-m\psi_R=0.
\end{cases}
\right.
\tag{1.104}
```

For $`m=0`$ it reduces to the Weyl equations

```math
\left.
\begin{cases}
i\bigl(\partial_t-\boldsymbol\sigma\cdot\nabla\bigr)\psi_L=0,\\
i\bigl(\partial_t+\boldsymbol\sigma\cdot\nabla\bigr)\psi_R=0.
\end{cases}
\right.
\tag{1.105}
```

**Plane-Wave Solutions of the Dirac Equation**

Apply $`-i\gamma^\mu\partial_\mu-m`$ to the left-hand side of (1.95):

```math
\left.
\begin{aligned}
\bigl(-i\gamma^\mu\partial_\mu-m\bigr)\bigl(i\gamma^\nu\partial_\nu-m\bigr)\psi
&=\bigl(\gamma^\mu\gamma^\nu\partial_\mu\partial_\nu+m^2\bigr)\psi\\
&=\bigl(\eta^{\mu\nu}\partial_\mu\partial_\nu+m^2\bigr)\psi\\
&=\bigl(\Box+m^2\bigr)\psi,
\end{aligned}
\right.
\tag{1.106}
```

where $`\Box:=\eta^{\mu\nu}\partial_\mu\partial_\nu=\partial_t^2-\nabla^2`$. Since the left-hand side of (1.106) vanishes by (1.95), every component of $`\psi`$ satisfies the Klein–Gordon equation

```math
\left.
\bigl(\Box+m^2\bigr)\psi=0.
\right.
\tag{1.107}
```

A plane wave $`e^{-ip\cdot x}`$ satisfies (1.107) only if $`p^2=m^2`$. In the Weyl representation (0.10), the plane-wave solutions of (1.95) therefore take the form

```math
\left.
\psi(x)=\begin{pmatrix}u_L\\u_R\end{pmatrix}e^{-ip\cdot x},
\qquad
p^0=\pm E_{\mathbf p},\quad
E_{\mathbf p}:=\sqrt{\mathbf p^2+m^2},
\right.
\tag{1.108}
```

where $`u_L,u_R\in\mathbb C^2`$ are constant. Substituting (1.108) into (1.95) gives

```math
\left.
\bigl(\not p-m\bigr)\begin{pmatrix}u_L\\u_R\end{pmatrix}=0,
\qquad
\not p:=\gamma\cdot p=p^\mu\gamma_\mu.
\right.
\tag{1.109}
```

**(1) Rest Frame**

Take $`m>0`$ and work in the rest frame, $`\mathbf p=\mathbf 0`$; there we denote the constants in (1.108) by $`u_L(\mathbf 0)`$ and $`u_R(\mathbf 0)`$. First consider $`p^0>0`$. Then $`p^\mu=(m,\mathbf 0)`$, $`e^{-ip\cdot x}=e^{-imt}`$ and $`\not p=m\gamma^0`$, so (1.109) becomes

```math
\left.
\begin{aligned}
\bigl(m\gamma^0-m\bigr)\begin{pmatrix}u_L(\mathbf 0)\\u_R(\mathbf 0)\end{pmatrix}
&=\begin{pmatrix}-mI_2&mI_2\\mI_2&-mI_2\end{pmatrix}
\begin{pmatrix}u_L(\mathbf 0)\\u_R(\mathbf 0)\end{pmatrix}=0\\[6pt]
\Longrightarrow\quad u_L(\mathbf 0)&=u_R(\mathbf 0).
\end{aligned}
\right.
\tag{1.110}
```

Writing $`u:=\begin{pmatrix}u_L\\u_R\end{pmatrix}`$, there are two independent solutions

```math
\left.
u^s(\mathbf 0)=\sqrt m\begin{pmatrix}\xi^s\\\xi^s\end{pmatrix},\qquad s=1,2,
\right.
\tag{1.111}
```

where $`\{\xi^s\}`$ is a basis of $`\mathbb C^2`$ with $`\xi^{r\dagger}\xi^s=\delta^{rs}`$.

**(2) Boost**

Boost along $`z`$ with rapidity $`\eta`$, i.e. $`\omega_{03}=\eta`$ in (1.100), so that $`\mathbf p=(0,0,p^3)`$ and $`\tanh\eta=v=p^3/E_{\mathbf p}`$. Then

```math
\left.
\begin{aligned}
\Lambda_{\frac12}=e^{-i\eta S^{03}}
&=\exp\Bigl[-i\eta\Bigl(-\frac i2\Bigr)\begin{pmatrix}\sigma^3&0\\0&-\sigma^3\end{pmatrix}\Bigr]
=\begin{pmatrix}e^{-\frac12\eta\sigma^3}&0\\0&e^{\frac12\eta\sigma^3}\end{pmatrix}\\
&=\mathop{\rm diag}\nolimits \bigl(e^{-\eta/2},\,e^{\eta/2},\,e^{\eta/2},\,e^{-\eta/2}\bigr),
\end{aligned}
\right.
\tag{1.112}
```

```math
\left.
\tanh\eta=v
\ \Longrightarrow\
e^{\pm\eta}=\sqrt{\frac{1\pm v}{1\mp v}}=\frac{E_{\mathbf p}\pm p^3}{m},
\qquad
e^{\pm\eta/2}=\sqrt{\frac{E_{\mathbf p}\pm p^3}{m}}.
\right.
\tag{1.113}
```

Hence

```math
\left.
u^s(p)=\Lambda_{\frac12}u^s(\mathbf 0)
=\mathop{\rm diag}\nolimits \Bigl(\sqrt{E_{\mathbf p}-p^3},\,\sqrt{E_{\mathbf p}+p^3},\,\sqrt{E_{\mathbf p}+p^3},\,\sqrt{E_{\mathbf p}-p^3}\Bigr)
\begin{pmatrix}\xi^s\\\xi^s\end{pmatrix}.
\right.
\tag{1.114}
```

With $`\xi^1=\begin{pmatrix}1\\0\end{pmatrix}`$ and $`\xi^2=\begin{pmatrix}0\\1\end{pmatrix}`$,

```math
\left.
u^1(p)=\begin{pmatrix}\sqrt{E_{\mathbf p}-p^3}\\0\\\sqrt{E_{\mathbf p}+p^3}\\0\end{pmatrix}
\xrightarrow{\ \eta\to\infty\ }\sqrt{2E_{\mathbf p}}\begin{pmatrix}0\\0\\1\\0\end{pmatrix},
\qquad
u^2(p)=\begin{pmatrix}0\\\sqrt{E_{\mathbf p}+p^3}\\0\\\sqrt{E_{\mathbf p}-p^3}\end{pmatrix}
\xrightarrow{\ \eta\to\infty\ }\sqrt{2E_{\mathbf p}}\begin{pmatrix}0\\1\\0\\0\end{pmatrix}.
\right.
\tag{1.115}
```

**(3) Arbitrary Momentum**

Since $`\mathop{\rm diag}\nolimits \bigl(\sqrt{E_{\mathbf p}-p^3},\sqrt{E_{\mathbf p}+p^3}\bigr)=\sqrt{E_{\mathbf p}-p^3\sigma^3}`$ and $`\mathop{\rm diag}\nolimits \bigl(\sqrt{E_{\mathbf p}+p^3},\sqrt{E_{\mathbf p}-p^3}\bigr)=\sqrt{E_{\mathbf p}+p^3\sigma^3}`$, for arbitrary $`\mathbf p`$

```math
\left.
\sqrt m\,\Lambda_{\frac12}=\begin{pmatrix}\sqrt{p\cdot\sigma}&0\\0&\sqrt{p\cdot\bar\sigma}\end{pmatrix},
\qquad
p\cdot\sigma:=p_\mu\sigma^\mu=p^0I_2-\mathbf p\cdot\boldsymbol\sigma,
\quad
p\cdot\bar\sigma:=p_\mu\bar\sigma^\mu=p^0I_2+\mathbf p\cdot\boldsymbol\sigma,
\right.
\tag{1.116}
```

with positive square roots. The positive-energy solutions are

```math
\left.
\boxed{
\psi=u^s(p)\,e^{-ip\cdot x},\qquad
u^s(p)=\begin{pmatrix}\sqrt{p\cdot\sigma}\,\xi^s\\\sqrt{p\cdot\bar\sigma}\,\xi^s\end{pmatrix},\qquad
p^0=E_{\mathbf p}.
}
\right.
\tag{1.117}
```

**Verification**

```math
\left.
\begin{aligned}
(p\cdot\bar\sigma)(p\cdot\sigma)
&=\bigl(p^0I_2+p^i\sigma^i\bigr)\bigl(p^0I_2-p^j\sigma^j\bigr)
=(p^0)^2-\frac12\{\sigma^i,\sigma^j\}p^ip^j
=(p^0)^2-\mathbf p^2=m^2,\\[6pt]
\bigl(\not p-m\bigr)u^s(p)
&=\begin{pmatrix}-m&p\cdot\sigma\\p\cdot\bar\sigma&-m\end{pmatrix}
\begin{pmatrix}\sqrt{p\cdot\sigma}\,\xi^s\\\sqrt{p\cdot\bar\sigma}\,\xi^s\end{pmatrix}
=\begin{pmatrix}\sqrt{p\cdot\sigma}\,\bigl(\sqrt{(p\cdot\sigma)(p\cdot\bar\sigma)}-m\bigr)\xi^s\\\sqrt{p\cdot\bar\sigma}\,\bigl(\sqrt{(p\cdot\bar\sigma)(p\cdot\sigma)}-m\bigr)\xi^s\end{pmatrix}=0.
\end{aligned}
\right.
\tag{1.118}
```

**Negative-Energy Solutions**

For $`p^0=-E_{\mathbf p}`$, (1.109) becomes

```math
\left.
\bigl(-\gamma^0E_{\mathbf p}-\boldsymbol\gamma\cdot\mathbf p-m\bigr)u(p)=0
\quad\Longleftrightarrow\quad
\bigl(\gamma^0E_{\mathbf p}-\boldsymbol\gamma\cdot(-\mathbf p)+m\bigr)u(p)=0,
\right.
\tag{1.119}
```

which is the positive-energy equation $`\bigl(\gamma^0E_{\mathbf p}-\boldsymbol\gamma\cdot\mathbf p-m\bigr)u=0`$ with $`\mathbf p\to-\mathbf p`$ and $`m\to-m`$. Hence

```math
\left.
u^s(p)=\begin{pmatrix}\sqrt{E_{\mathbf p}I_2+\mathbf p\cdot\boldsymbol\sigma}\,\xi^s\\-\sqrt{E_{\mathbf p}I_2-\mathbf p\cdot\boldsymbol\sigma}\,\xi^s\end{pmatrix}
=\begin{pmatrix}\sqrt{-p\cdot\sigma}\,\xi^s\\-\sqrt{-p\cdot\bar\sigma}\,\xi^s\end{pmatrix},
\qquad p^0=-E_{\mathbf p}.
\right.
\tag{1.120}
```

**Antiparticle Solutions**

Define

```math
\left.
u^c(p):=\begin{pmatrix}i\sigma^2&0\\0&-i\sigma^2\end{pmatrix}\gamma^0\,u(p),
\qquad
i\sigma^2=\begin{pmatrix}0&1\\-1&0\end{pmatrix}.
\right.
\tag{1.121}
```

For $`\mathbf p=(0,0,p^3)`$,

```math
\left.
i\sigma^2\sqrt{p\cdot\bar\sigma}
=\begin{pmatrix}0&1\\-1&0\end{pmatrix}\begin{pmatrix}\sqrt{E_{\mathbf p}+p^3}&0\\0&\sqrt{E_{\mathbf p}-p^3}\end{pmatrix}
=\begin{pmatrix}0&\sqrt{E_{\mathbf p}-p^3}\\-\sqrt{E_{\mathbf p}+p^3}&0\end{pmatrix}
=\sqrt{p\cdot\sigma}\;i\sigma^2,
\right.
\tag{1.122}
```

and likewise $`i\sigma^2\sqrt{p\cdot\sigma}=\sqrt{p\cdot\bar\sigma}\;i\sigma^2`$. Applying (1.121) to (1.117) and writing $`\eta^s:=i\sigma^2\xi^s`$,

```math
\left.
u^c(p)=\begin{pmatrix}i\sigma^2\sqrt{p\cdot\bar\sigma}\,\xi^s\\-i\sigma^2\sqrt{p\cdot\sigma}\,\xi^s\end{pmatrix}
=\begin{pmatrix}\sqrt{p\cdot\sigma}\,\eta^s\\-\sqrt{p\cdot\bar\sigma}\,\eta^s\end{pmatrix},
\qquad p^0=E_{\mathbf p},
\right.
\tag{1.123}
```

which is (1.120) at $`-p`$ with $`\xi^s\to\eta^s`$. For arbitrary $`\mathbf p`$, the antiparticle solutions are

```math
\left.
\boxed{
\psi=v^s(p)\,e^{+ip\cdot x},\qquad
v^s(p):=\begin{pmatrix}\sqrt{p\cdot\sigma}\,\eta^s\\-\sqrt{p\cdot\bar\sigma}\,\eta^s\end{pmatrix},\qquad
\bigl(\not p+m\bigr)v^s(p)=0,\qquad
p^0=E_{\mathbf p}.
}
\right.
\tag{1.124}
```

**Properties of the Solutions**

**(1) Orthonormality**

From (1.117), $`u^\dagger u=2E_{\mathbf p}\,\xi^\dagger\xi`$ and $`\bar uu=2m\,\xi^\dagger\xi`$. With $`\xi^{r\dagger}\xi^s=\eta^{r\dagger}\eta^s=\delta^{rs}`$,

```math
\left.
\boxed{
\begin{aligned}
u^{r\dagger}(p)\,u^s(p)&=2E_{\mathbf p}\,\delta^{rs}, &\qquad \bar u^r(p)\,u^s(p)&=2m\,\delta^{rs},\\
v^{r\dagger}(p)\,v^s(p)&=2E_{\mathbf p}\,\delta^{rs}, &\qquad \bar v^r(p)\,v^s(p)&=-2m\,\delta^{rs},\\
u^{r\dagger}(p)\,v^s(p')&=v^{r\dagger}(p')\,u^s(p)=0, &\qquad p'&:=(p^0,-\mathbf p).
\end{aligned}
}
\right.
\tag{1.125}
```

**(2) Completeness (Spin Sums)**

With $`\sum_s\xi^s\xi^{s\dagger}=I_2`$,

```math
\left.
\boxed{
\sum_s u^s(p)\,\bar u^s(p)=\not p+m,\qquad
\sum_s v^s(p)\,\bar v^s(p)=\not p-m.
}
\right.
\tag{1.126}
```

<br><br>

<a id="dirac-bilinears"></a>
#### Dirac Bilinears

Bilinears have the form $`\bar\psi\Gamma\psi`$ with $`\Gamma`$ a $`4\times4`$ matrix. A basis of the $`4\times4`$ matrices consists of 16 matrices:

<div style="display: flex; justify-content: center;">

| $`\Gamma`$ | Number | Replaced by |
|:---:|:---:|:---:|
| $`I_4`$ | 1 | |
| $`\gamma^\mu`$ | 4 | |
| $`S^{\mu\nu}`$ | 6 | |
| $`\gamma^{[\mu}\gamma^\nu\gamma^{\rho]}`$ | 4 | $`\gamma^5\gamma^\mu`$ |
| $`\gamma^{[\mu}\gamma^\nu\gamma^\rho\gamma^{\sigma]}`$ | 1 | $`\gamma^5`$ |

</div>

where

```math
\left.
\gamma^5=\frac{i}{4!}\epsilon_{\mu\nu\rho\sigma}\gamma^\mu\gamma^\nu\gamma^\rho\gamma^\sigma,
\qquad \epsilon_{0123}=+1,
\right.
\tag{1.127}
```

which agrees with (0.14). Under $`\psi\to\Lambda_{\frac12}\psi`$, $`\bar\psi\to\bar\psi\Lambda_{\frac12}^{-1}`$,

```math
\left.
\begin{aligned}
\bar\psi\psi&\xrightarrow{\ \Lambda\ }\bar\psi\psi,\\
\bar\psi\gamma^\mu\psi&\xrightarrow{\ \Lambda\ }\bar\psi\Lambda_{\frac12}^{-1}\gamma^\mu\Lambda_{\frac12}\psi=\Lambda^\mu{}_\nu\,\bar\psi\gamma^\nu\psi,\\
\bar\psi S^{\mu\nu}\psi&\xrightarrow{\ \Lambda\ }\Lambda^\mu{}_\rho\Lambda^\nu{}_\sigma\,\bar\psi S^{\rho\sigma}\psi,\\
\bar\psi\gamma^5\gamma^\mu\psi&\xrightarrow{\ \Lambda\ }\det[\Lambda]\,\Lambda^\mu{}_\nu\,\bar\psi\gamma^5\gamma^\nu\psi\qquad\text{(pseudovector)},\\
\bar\psi\gamma^5\psi&\xrightarrow{\ \Lambda\ }\det[\Lambda]\,\bar\psi\gamma^5\psi\qquad\text{(pseudoscalar)}.
\end{aligned}
\right.
\tag{1.128}
```

**Proof** (for $`\gamma^5`$)

```math
\left.
\begin{aligned}
\Lambda_{\frac12}^{-1}\gamma^5\Lambda_{\frac12}
&=\frac{i}{4!}\epsilon_{\mu\nu\rho\sigma}\Lambda^\mu{}_\alpha\Lambda^\nu{}_\beta\Lambda^\rho{}_\kappa\Lambda^\sigma{}_\lambda\,\gamma^\alpha\gamma^\beta\gamma^\kappa\gamma^\lambda\\
&=\frac{i}{4!}\det[\Lambda]\,\epsilon_{\alpha\beta\kappa\lambda}\gamma^\alpha\gamma^\beta\gamma^\kappa\gamma^\lambda
=\det[\Lambda]\,\gamma^5.
\end{aligned}
\right.
\tag{1.129}
```

**Chirality**

```math
\left.
\gamma^5\begin{pmatrix}\psi_L\\0\end{pmatrix}=-\begin{pmatrix}\psi_L\\0\end{pmatrix},
\qquad
\gamma^5\begin{pmatrix}0\\\psi_R\end{pmatrix}=\begin{pmatrix}0\\\psi_R\end{pmatrix}.
\right.
\tag{1.130}
```

The left- and right-handed projection operators are

```math
\left.
P_L:=\frac{I_4-\gamma^5}2,\qquad P_R:=\frac{I_4+\gamma^5}2
\quad\Longrightarrow\quad
\begin{cases}
P_L+P_R=I_4,\\
P_LP_R=P_RP_L=0,\\
P_L^n=P_L,\quad P_R^n=P_R.
\end{cases}
\right.
\tag{1.131}
```

**Vector and Axial Currents**

```math
\left.
j^\mu:=\bar\psi\gamma^\mu\psi,\qquad
j^{\mu5}:=\bar\psi\gamma^\mu\gamma^5\psi.
\right.
\tag{1.132}
```

The Euler–Lagrange equation of (1.94) for $`\psi`$ is $`-i\partial_\mu\bar\psi\gamma^\mu-m\bar\psi=0`$. Together with (1.95),

```math
\left.
\partial_\mu j^\mu=(\partial_\mu\bar\psi)\gamma^\mu\psi+\bar\psi\gamma^\mu\partial_\mu\psi
=im\bar\psi\psi-im\bar\psi\psi=0
\quad\Longrightarrow\quad
\int d^3x\,\bar\psi\gamma^0\psi=\text{const}.
\right.
\tag{1.133}
```

**Helicity**

```math
\left.
h:=\frac{\mathbf p}{|\mathbf p|}\cdot\mathbf S,\qquad
\mathbf S:=\frac12\begin{pmatrix}\boldsymbol\sigma&0\\0&\boldsymbol\sigma\end{pmatrix}.
\right.
\tag{1.134}
```

For $`\mathbf p=(0,0,p^3)`$ with $`p^3>0`$, the spinors (1.115) satisfy $`h\,u^1=\frac12u^1`$ and $`h\,u^2=-\frac12u^2`$.


<br><br>

<a id="proca-field"></a>
### 1.8 The Proca Field

<a id="proca-lagrangian"></a>
#### Lagrangian

For a real vector field with $`m>0`$,

```math
\left.
F_{\mu\nu}:=\partial_\mu A_\nu-\partial_\nu A_\mu,
\qquad
\boxed{
\mathcal L=-\frac14F_{\mu\nu}F^{\mu\nu}
+\frac12m^2A_\mu A^\mu.
}
\right.
\tag{1.135}
```

```math
\left.
\boxed{
\partial_\mu F^{\mu\nu}+m^2A^\nu=0,
\qquad
\partial_\mu A^\mu=0,
\qquad
(\partial_\mu\partial^\mu+m^2)A^\nu=0.
}
\right.
\tag{1.136}
```

Here $`\partial_\mu A^\mu=0`$ follows from the equations of motion.

**Canonical Momenta and Hamiltonian**

Choose $`A_\mu`$ as canonical coordinates. All brackets below are at equal time:

```math
\left.
\Pi^\mu:=\frac{\partial\mathcal L}{\partial\dot A_\mu}=F^{\mu0},
\qquad
\Pi^0=0,
\qquad
\Pi^i=\dot A_i-\partial_iA_0,
\qquad
\{A_\mu(\mathbf x),\Pi^\nu(\mathbf y)\}_{\mathrm{PB}}
=\delta_\mu{}^\nu\delta^{(3)}(\mathbf x-\mathbf y).
\right.
\tag{1.137}
```

With vanishing spatial surface terms,

```math
\left.
\boxed{
\begin{aligned}
H_c&=\int d^3x\left[
\frac12\sum_i(\Pi^i)^2+\frac14\sum_{i,j}(F_{ij})^2
+\frac{m^2}{2}\sum_i(A_i)^2
-\frac{m^2}{2}A_0^2-A_0\partial_i\Pi^i\right],\\
H_T&=H_c+\int d^3x\,u\,\Pi^0.
\end{aligned}}
\right.
\tag{1.138}
```

**Second-Class Constraints**

```math
\left.
\boxed{
\begin{aligned}
\chi_1&:=\Pi^0\approx0,
&
\chi_2&:=\partial_i\Pi^i+m^2A_0\approx0,\\
\{\chi_1(\mathbf x),\chi_2(\mathbf y)\}_{\mathrm{PB}}
&=-m^2\delta^{(3)}(\mathbf x-\mathbf y),
&
N_{\mathrm{physical}}&=4-\frac22=3.
\end{aligned}}
\right.
\tag{1.139}
```

Preserving $`\chi_2`$ fixes $`u=\sum_i\partial_iA_i`$; there are no further constraints.

Here $`\chi_1`$ is primary and $`\chi_2`$ is secondary; both are second class.

**Reduced Hamiltonian**

Eliminating $`\Pi^0`$ and $`A_0`$ gives

```math
\left.
A_0=-\frac{\partial_i\Pi^i}{m^2},
\qquad
\boxed{
H_{\mathrm{red}}=\int d^3x\left[
\frac12\sum_i(\Pi^i)^2+\frac14\sum_{i,j}(F_{ij})^2
+\frac{m^2}{2}\sum_i(A_i)^2
+\frac{(\partial_i\Pi^i)^2}{2m^2}
\right]\ge0.
}
\right.
\tag{1.140}
```

**Conserved Quantities: Spacetime Symmetries**

For the canonical variables $`A_\mu`$, translations give

```math
\left.
\boxed{\begin{aligned}
T^\mu{}_\nu&=-F^{\mu\rho}\partial_\nu A_\rho-\delta^\mu{}_\nu\mathcal L,
&\partial_\mu T^\mu{}_\nu&=0,\\
P_\nu&=\int d^3x\,T^0{}_\nu,
&\frac{dP_\nu}{dt}&=0.
\end{aligned}}
\right.
\tag{1.141}
```

With $`T^{\mu\nu}:=T^\mu{}_\rho\eta^{\rho\nu}`$, the Lorentz charges include the vector spin contribution:

```math
\left.
\boxed{
J^{\mu\nu}=\int d^3x\left[
x^\mu T^{0\nu}-x^\nu T^{0\mu}
+\Pi^\mu A^\nu-\Pi^\nu A^\mu
\right],
\qquad
\frac{dJ^{\mu\nu}}{dt}=0.
}
\right.
\tag{1.142}
```

These are conserved on shell, with convergent integrals and vanishing boundary fluxes.

**Conserved Quantities: Internal and Gauge Symmetries**

For $`m>0`$, the mass term breaks the Maxwell gauge symmetry $`A_\mu\mapsto A_\mu+\partial_\mu\lambda(x)`$. The real Proca field has no complex $`U(1)`$ phase symmetry, so this model has no corresponding phase charge. Its constraint $`\partial_i\Pi^i+m^2A_0=0`$ is second class, as in (1.139).

<br><br>

<a id="proca-field-solutions"></a>
#### Solutions of the Proca Equation

For $`A^\mu(x)=\epsilon^\mu(p)e^{-ip\cdot x}`$, the field equation becomes

```math
\left.
\begin{aligned}
(m^2-p^2)\epsilon^\mu+p^\mu(p_\nu\epsilon^\nu)&=0,\\
m^2p_\mu\epsilon^\mu&=0.
\end{aligned}
\quad\Longrightarrow\quad
\boxed{p^2=m^2,\qquad p_\mu\epsilon^\mu=0}
\right.
\tag{1.143}
```

for a nonzero mode with $`m>0`$.

**Polarizations**

For $`p^2=m^2`$, $`p^0>0`$, there are three polarization vectors, $`r=1,2,3`$:

```math
\left.
\boxed{
p_\mu\epsilon_r^\mu(p)=0,
\qquad
\epsilon_{r\mu}^*(p)\epsilon_s^\mu(p)=-\delta_{rs},
\qquad
\sum_{r=1}^3\epsilon_r^\mu(p)\epsilon_r^{\nu*}(p)
=-\eta^{\mu\nu}+\frac{p^\mu p^\nu}{m^2}.
}
\right.
\tag{1.144}
```


At rest, one may take $`\epsilon_r^\mu=(0,\mathbf e_r)`$ for an orthonormal spatial basis $`\mathbf e_r`$. For $`\mathbf p\ne0`$, choose $`\mathbf e_1,\mathbf e_2`$ perpendicular to $`\mathbf p`$, with $`\mathbf e_a\cdot\mathbf e_b=\delta_{ab}`$. With $`E_{\mathbf p}=\sqrt{\mathbf p^2+m^2}`$, a basis with two transverse and one longitudinal polarization is

```math
\left.
\boxed{
\epsilon_a^\mu(p)=(0,\mathbf e_a)\quad(a=1,2),
\qquad
\epsilon_3^\mu(p)=\left(\frac{|\mathbf p|}{m},
\frac{E_{\mathbf p}}{m}\frac{\mathbf p}{|\mathbf p|}\right).
}
\right.
\tag{1.145}
```

The real field is a superposition of these three modes, with $`p^0=E_{\mathbf p}`$:

```math
\left.
\boxed{
A^\mu(x)=\sum_{r=1}^3\int\frac{d^3p}{(2\pi)^3\,2E_{\mathbf p}}
\left[
a_r(\mathbf p)\epsilon_r^\mu(p)e^{-ip\cdot x}
+a_r^*(\mathbf p)\epsilon_r^{\mu*}(p)e^{+ip\cdot x}
\right].
}
\right.
\tag{1.146}
```

Here $`a_r(\mathbf p)`$ are classical complex amplitudes; the transversality condition is imposed by the field equation, not by a gauge choice.

<br><br>

<a id="vector-field"></a>
### 1.9 The Vector Field

<a id="maxwell-lagrangian"></a>
#### Lagrangian

```math
\left.
\boxed{
\mathcal L=-\frac14F_{\mu\nu}F^{\mu\nu},
\qquad
\partial_\mu F^{\mu\nu}=0,
\qquad
A_\mu'=A_\mu+\partial_\mu\lambda(x).
}
\right.
\tag{1.147}
```

**Hamiltonian and First-Class Constraints**

```math
\left.
\begin{aligned}
\Pi^\mu&=F^{\mu0},\\
H_c&=\int d^3x\left[
\frac12\sum_i(\Pi^i)^2+\frac14\sum_{i,j}(F_{ij})^2
-A_0\partial_i\Pi^i\right],
&
H_T&=H_c+\int d^3x\,u\,\Pi^0,\\
\chi_1&:=\Pi^0\approx0,
&
\chi_2&:=\partial_i\Pi^i\approx0.
\end{aligned}
\right.
\tag{1.148}
```

Both constraints are first class:

```math
\left.
\{\chi_a(\mathbf x),\chi_b(\mathbf y)\}_{\mathrm{PB}}=0,
\qquad a,b=1,2,
\qquad
\boxed{N_{\mathrm{physical}}=4-2=2.}
\right.
\tag{1.149}
```

**Coulomb Gauge and Physical Hamiltonian**

In the absence of sources, with fields decaying at spatial infinity,

```math
\left.
\sum_i\partial_iA_i=0,
\qquad
A_0=0,
\qquad
\partial_i\Pi^i=0,
\qquad
\boxed{
H_{\mathrm{physical}}
=\int d^3x\left[
\frac12\sum_i(\Pi^i)^2+\frac14\sum_{i,j}(F_{ij})^2
\right]\ge0.
}
\right.
\tag{1.150}
```

The remaining canonical variables are transverse.

**Conserved Quantities: Spacetime Symmetries**

The canonical energy–momentum tensor and four-momentum are

```math
\left.
\boxed{\begin{aligned}
T^\mu{}_\nu&=-F^{\mu\rho}\partial_\nu A_\rho-\delta^\mu{}_\nu\mathcal L,
&\partial_\mu T^\mu{}_\nu&=0,\\
P_\nu&=\int d^3x\,T^0{}_\nu,
&\frac{dP_\nu}{dt}&=0.
\end{aligned}}
\right.
\tag{1.151}
```

With $`T^{\mu\nu}:=T^\mu{}_\rho\eta^{\rho\nu}`$, the rotation and boost charges are

```math
\left.
\boxed{
J^{\mu\nu}=\int d^3x\left[
x^\mu T^{0\nu}-x^\nu T^{0\mu}
+\Pi^\mu A^\nu-\Pi^\nu A^\mu
\right],
\qquad
\frac{dJ^{\mu\nu}}{dt}=0.
}
\right.
\tag{1.152}
```

These charges are conserved on shell when the integrals converge and boundary fluxes vanish. The canonical densities depend on the gauge; the integrated charges are invariant under gauge transformations whose boundary terms vanish.

**Conserved Quantities: Internal and Gauge Symmetries**

The local transformation in (1.147) gives a Noether identity and the Gauss constraint. For smooth source-free fields on all of $`\mathbb R^3`$,

```math
\left.
\boxed{\begin{aligned}
\partial_\nu\partial_\mu F^{\mu\nu}&\equiv0,
&\partial_i\Pi^i&=0,\\
Q_{\mathrm{el}}&:=\lim_{R\to\infty}\oint_{|\mathbf x|=R}\Pi^i\,dS_i=0.
\end{aligned}}
\right.
\tag{1.153}
```

There is no independent matter $`U(1)`$ number in this free-field model. Nonzero electric flux requires sources, singularities, or different boundary conditions.

<br><br>

<a id="maxwell-field-solutions"></a>
#### Solutions of the Maxwell Equations

**Lorenz Gauge**

```math
\left.
\partial_\mu A^\mu=0
\quad\Longrightarrow\quad
\partial_\mu\partial^\mu A^\nu=0,
\qquad
A_\mu\mapsto A_\mu+\partial_\mu\lambda,
\qquad
\partial_\mu\partial^\mu\lambda=0
\quad\text{(residual gauge freedom).}
\right.
\tag{1.154}
```


**Plane Waves and Physical Polarizations**

For a plane wave $`A^\mu(x)=\epsilon^\mu(p)e^{-ip\cdot x}`$ in Lorenz gauge,

```math
\left.
\boxed{
p^2=0,\qquad p^0=|\mathbf p|>0,\qquad
p_\mu\epsilon^\mu=0,\qquad
\epsilon^\mu\sim\epsilon^\mu+\lambda p^\mu.
}
\right.
\tag{1.155}
```

In the last expression, $`\lambda`$ is an arbitrary complex coefficient of a residual plane-wave gauge transformation. The constraint and this equivalence leave two physical polarizations. A Coulomb-gauge basis satisfies

```math
\left.
\boxed{\begin{aligned}
\epsilon_r^0(p)&=0,\qquad
\mathbf p\cdot\boldsymbol\epsilon_r(p)=0,\qquad
\boldsymbol\epsilon_r^*(p)\cdot\boldsymbol\epsilon_s(p)=\delta_{rs},
\qquad r,s=1,2,\\
\sum_{r=1}^2\epsilon_r^i(p)\epsilon_r^{j*}(p)
&=\delta^{ij}-\frac{p^ip^j}{|\mathbf p|^2}.
\end{aligned}}
\right.
\tag{1.156}
```

For source-free wave packets, the real field in this gauge is, with $`p^0=|\mathbf p|`$,

```math
\left.
\boxed{
A^\mu(x)=\sum_{r=1}^2\int\frac{d^3p}{(2\pi)^3\,2|\mathbf p|}
\left[
a_r(\mathbf p)\epsilon_r^\mu(p)e^{-ip\cdot x}
+a_r^*(\mathbf p)\epsilon_r^{\mu*}(p)e^{+ip\cdot x}
\right].
}
\right.
\tag{1.157}
```

The $`a_r(\mathbf p)`$ are classical complex amplitudes. Other gauge representatives follow by adding $`\partial^\mu\lambda(x)`$.

<br><br>

<a id="qft-ch2"></a>
## 2. Operator Quantization


The first viewpoint in [Section 1.4](#classical-dynamics) naturally leads to Operator quantization: spatial position labels the degrees of freedom, while time remains the evolution parameter. 


<br><br>
<a id="canonical-quantization"></a>
### 2.1 Canonical Quantization

Consider unconstrained  fields $`\phi_a(x)`$ with a Lagrangian density

```math
\left.
\mathcal L=\mathcal L(\phi_a,\partial_\mu\phi_a),
\qquad
L(t)=\int d^3x\,\mathcal L.
\right.
\tag{2.1}
```

At each fixed time, the field values form an infinite set of generalized coordinates:

```math
\left.
i\longleftrightarrow(a,\mathbf x),
\qquad
q_i(t)\longleftrightarrow\phi_a(t,\mathbf x).
\right.
\tag{2.2}
```

**Conjugate momentum**

The momentum density conjugate to $`\phi_a(t,\mathbf x)`$ is

```math
\left.
\pi_a(t,\mathbf x)
\equiv
\frac{\delta L(t)}{\delta\dot\phi_a(t,\mathbf x)}
=
\frac{\partial\mathcal L}{\partial\dot\phi_a(t,\mathbf x)}.
\right.
\tag{2.3}
```

**Poisson brackets and commutation relations**

The classical fields obey the equal-time canonical Poisson brackets

```math
\left.
\begin{aligned}
\{\phi_a(t,\mathbf x),\pi_b(t,\mathbf y)\}_{\mathrm{PB}}
&=\delta_{ab}\delta^{(3)}(\mathbf x-\mathbf y),\\
\{\phi_a(t,\mathbf x),\phi_b(t,\mathbf y)\}_{\mathrm{PB}}
&=\{\pi_a(t,\mathbf x),\pi_b(t,\mathbf y)\}_{\mathrm{PB}}=0.
\end{aligned}
\right.
\tag{2.4}
```

Canonical quantization promotes the fields and their conjugate momenta to operators and replaces these fundamental Poisson brackets according to

```math
\left.
\{\ ,\ \}_{\mathrm{PB}}
\longrightarrow
\frac{1}{i}[\ ,\ ].
\right.
\tag{2.5}
```

Thus,

```math
\left.
\boxed{
\begin{aligned}
[\hat\phi_a(t,\mathbf x),\hat\pi_b(t,\mathbf y)]
&=i\,\delta_{ab}\delta^{(3)}(\mathbf x-\mathbf y),\\
[\hat\phi_a(t,\mathbf x),\hat\phi_b(t,\mathbf y)]
&=[\hat\pi_a(t,\mathbf x),\hat\pi_b(t,\mathbf y)]=0.
\end{aligned}}
\right.
\tag{2.6}
```

Here $`\delta_{ab}\delta^{(3)}(\mathbf x-\mathbf y)`$ generalizes the Kronecker delta $`\delta_{ij}`$ to the field labels $`(a,\mathbf x)`$.

**Free Real Scalar Field**

For a free field of mass $`m`$, use the Lorentz-invariant measure $`d\Pi_{\mathbf p}`$ and positive-energy four-momentum $`p`$:

```math
\left.
\begin{aligned}
E_{\mathbf p}&=\sqrt{\mathbf p^2+m^2},\qquad p^0=E_{\mathbf p},\qquad d\Pi_{\mathbf p}:=\frac{d^3p}{(2\pi)^3\,2E_{\mathbf p}},\\
\hat\phi_I(x)&=\int d\Pi_{\mathbf p}\left(\hat a_{\mathbf p}e^{-ip\cdot x}+\hat a_{\mathbf p}^\dagger e^{+ip\cdot x}\right).
\end{aligned}
\right.
\tag{2.7}
```

The vacuum is normalized to one. The creation operators define covariantly normalized one-particle states:

```math
\left.
\boxed{\begin{aligned}
[\hat a_{\mathbf p},\hat a_{\mathbf q}^\dagger]&=2E_{\mathbf p}(2\pi)^3\delta^{(3)}(\mathbf p-\mathbf q),\qquad
[\hat a_{\mathbf p},\hat a_{\mathbf q}]=[\hat a_{\mathbf p}^\dagger,\hat a_{\mathbf q}^\dagger]=0,\\
\hat a_{\mathbf p}|0\rangle&=0,\qquad |\mathbf p\rangle:=\hat a_{\mathbf p}^\dagger|0\rangle,\\
\langle\mathbf p|\mathbf q\rangle&=2E_{\mathbf p}(2\pi)^3\delta^{(3)}(\mathbf p-\mathbf q).
\end{aligned}}
\right.
\tag{2.8}
```

Normal ordering, denoted by colons, places creation operators to the left of annihilation operators. With the vacuum energy subtracted,

```math
\left.
\begin{aligned}
:\hat H_0:&=\int d\Pi_{\mathbf p}\,E_{\mathbf p}\,\hat a_{\mathbf p}^\dagger\hat a_{\mathbf p},\qquad
:\hat{\mathbf P}:=\int d\Pi_{\mathbf p}\,\mathbf p\,\hat a_{\mathbf p}^\dagger\hat a_{\mathbf p},\\
\hat N&=\int d\Pi_{\mathbf p}\,\hat a_{\mathbf p}^\dagger\hat a_{\mathbf p}.
\end{aligned}
\right.
\tag{2.9}
```

**Free Dirac Field**

Using the spinors and their normalization in [Section 1.7](#dirac-field), the operators $`\hat b_{\mathbf p}^s`$ and $`\hat c_{\mathbf p}^s`$ annihilate particles and antiparticles, respectively:

```math
\left.
\hat\psi_I(x)=\sum_{s=1}^{2}\int d\Pi_{\mathbf p}\left(\hat b_{\mathbf p}^s u^s(p)e^{-ip\cdot x}+\hat c_{\mathbf p}^{s\dagger}v^s(p)e^{+ip\cdot x}\right).
\right.
\tag{2.10}
```

Fermionic quantization uses anticommutators; $`\alpha,\beta`$ below are Dirac component indices. All mode anticommutators not displayed vanish, and both annihilation operators annihilate $`|0\rangle`$.

```math
\left.
\boxed{\begin{aligned}
\{\hat b_{\mathbf p}^r,\hat b_{\mathbf q}^{s\dagger}\}&=\{\hat c_{\mathbf p}^r,\hat c_{\mathbf q}^{s\dagger}\}=2E_{\mathbf p}(2\pi)^3\delta^{rs}\delta^{(3)}(\mathbf p-\mathbf q),\\
\{\hat\psi_{I,\alpha}(t,\mathbf x),\hat\psi_{I,\beta}^\dagger(t,\mathbf y)\}&=\delta_{\alpha\beta}\delta^{(3)}(\mathbf x-\mathbf y),\\
\{\hat\psi_{I,\alpha}(t,\mathbf x),\hat\psi_{I,\beta}(t,\mathbf y)\}&=0.
\end{aligned}}
\right.
\tag{2.11}
```

Fermionic normal ordering includes a minus sign for every interchange of fermionic operators. The normal-ordered energy, momentum, and net fermion number are

```math
\left.
\begin{aligned}
:\hat H_0:&=\sum_s\int d\Pi_{\mathbf p}\,E_{\mathbf p}\left(\hat b_{\mathbf p}^{s\dagger}\hat b_{\mathbf p}^s+\hat c_{\mathbf p}^{s\dagger}\hat c_{\mathbf p}^s\right),\\
:\hat{\mathbf P}:&=\sum_s\int d\Pi_{\mathbf p}\,\mathbf p\left(\hat b_{\mathbf p}^{s\dagger}\hat b_{\mathbf p}^s+\hat c_{\mathbf p}^{s\dagger}\hat c_{\mathbf p}^s\right),\\
\hat Q&:=\int d^3x:\hat\psi_I^\dagger\hat\psi_I:
=\sum_s\int d\Pi_{\mathbf p}\left(\hat b_{\mathbf p}^{s\dagger}\hat b_{\mathbf p}^s-\hat c_{\mathbf p}^{s\dagger}\hat c_{\mathbf p}^s\right).
\end{aligned}
\right.
\tag{2.12}
```

<br><br>

<a id="quantization-with-dirac-brackets"></a>
### 2.2 Quantization with Dirac Brackets

<a id="complex-scalar-field-quantization"></a>
#### Quantization of the Complex Scalar Field

<br><br>

<a id="dirac-field-quantization"></a>
#### Quantization of the Dirac Field

<br><br>

<a id="proca-field-quantization"></a>
#### Quantization of the Proca Field

<br><br>

<a id="gupta-bleuler-quantization"></a>
### 2.3 Gupta–Bleuler Quantization

<br><br>

<a id="symmetry"></a>
### 2.4 Symmetry

<a id="schrodinger-picture"></a>
#### Schrödinger Picture

The dynamics is carried entirely by the states; operators do not evolve in time. Here an operator $`\hat O`$ is said to evolve in time if its dependence on $`t`$ changes when the Hamiltonian $`\hat H`$ is replaced.

This does not exclude an explicit time dependence $`\hat O_S(t)`$, which is fixed by the form of $`\hat O_S`$ and does not depend on $`\hat H`$. Hence

```math
\left.
\begin{gathered}
\frac{d\hat O_S}{dt}=\frac{\partial\hat O_S}{\partial t},\\[4pt]
i\frac{\partial}{\partial t}|\psi_S(t)\rangle=\hat H|\psi_S(t)\rangle.
\end{gathered}
\right.
\tag{2.13}
```

The solution of (2.13) with initial state $`|\psi_S(t_0)\rangle`$ depends on the time dependence of $`\hat H`$.

**(1) $`\hat H`$ without Explicit Time Dependence**

If $`\hat H`$ has no explicit time dependence, (2.13) is solved by

```math
\left.
|\psi_S(t)\rangle=e^{-i\hat H(t-t_0)}\,|\psi_S(t_0)\rangle .
\right.
\tag{2.14}
```

**(2) $`\hat H(t)`$ Commuting at Different Times**

Let $`\hat H=\hat H(t)`$ depend explicitly on $`t`$, with $`[\hat H(t_1),\hat H(t_2)]=0`$ for all $`t_1,t_2`$. Here $`\int_{t_0}^{t}dt'\,\hat H(t')`$ is the operator with matrix elements $`\int_{t_0}^{t}dt'\,\langle\phi|\hat H(t')|\chi\rangle`$. Then $`\hat H(t)`$ commutes with $`\int_{t_0}^{t}dt'\,\hat H(t')`$, and

```math
\left.
\begin{aligned}
\frac{\partial}{\partial t}\Bigl(\int_{t_0}^{t}dt'\,\hat H(t')\Bigr)^n
&=\sum_{k=0}^{n-1}\Bigl(\int_{t_0}^{t}dt'\,\hat H(t')\Bigr)^k\,\hat H(t)\,\Bigl(\int_{t_0}^{t}dt'\,\hat H(t')\Bigr)^{n-1-k}\\
&=n\,\hat H(t)\Bigl(\int_{t_0}^{t}dt'\,\hat H(t')\Bigr)^{n-1}.
\end{aligned}
\right.
\tag{2.15}
```

By (2.15), differentiating the exponential series of $`-i\int_{t_0}^{t}dt'\,\hat H(t')`$ term by term multiplies it by $`-i\hat H(t)`$ from the left, so

```math
\left.
|\psi_S(t)\rangle=\exp\Bigl(-i\int_{t_0}^{t}dt'\,\hat H(t')\Bigr)\,|\psi_S(t_0)\rangle ,
\right.
\tag{2.16}
```

which reduces to (2.14) for $`\hat H(t)=\hat H`$.

**(3) $`\hat H(t)`$ Not Commuting at Different Times**

In general $`[\hat H(t_1),\hat H(t_2)]\neq0`$; then the second equality of (2.15) fails and (2.16) no longer solves (2.13). Instead, integrate (2.13) and iterate:

```math
\left.
\begin{aligned}
|\psi_S(t)\rangle
&=|\psi_S(t_0)\rangle-i\int_{t_0}^{t}dt_1\,\hat H(t_1)\,|\psi_S(t_1)\rangle\\
&=\Bigl[1+(-i)\int_{t_0}^{t}dt_1\,\hat H(t_1)
+(-i)^2\int_{t_0}^{t}dt_1\int_{t_0}^{t_1}dt_2\,\hat H(t_1)\hat H(t_2)+\cdots\Bigr]|\psi_S(t_0)\rangle ,
\end{aligned}
\right.
\tag{2.17}
```

where the $`n`$-th term is integrated over $`t\ge t_1\ge\cdots\ge t_n\ge t_0`$, with later times to the left.

Define the time-ordered product

```math
\left.
\mathcal T[\hat H(t_1)\hat H(t_2)]
:=\theta(t_1-t_2)\,\hat H(t_1)\hat H(t_2)+\theta(t_2-t_1)\,\hat H(t_2)\hat H(t_1),
\right.
\tag{2.18}
```

and likewise for $`n`$ operators, ordered with time decreasing from left to right. $`\mathcal T[\hat H(t_1)\cdots\hat H(t_n)]`$ is symmetric under permutations of $`t_1,\ldots,t_n`$; the cube $`[t_0,t]^n`$ splits into $`n!`$ regions according to the ordering of the $`t_i`$, each contributing equally, and on $`t_1>\cdots>t_n`$ the time-ordered product is the ordered product in (2.17). Hence

```math
\left.
\int_{t_0}^{t}dt_1\int_{t_0}^{t_1}dt_2\cdots\int_{t_0}^{t_{n-1}}dt_n\,
\hat H(t_1)\cdots\hat H(t_n)
=\frac1{n!}\int_{t_0}^{t}dt_1\cdots\int_{t_0}^{t}dt_n\,
\mathcal T[\hat H(t_1)\cdots\hat H(t_n)],
\right.
\tag{2.19}
```

and (2.17) becomes the Dyson series

```math
\left.
\boxed{
\begin{gathered}
|\psi_S(t)\rangle=\mathcal T\exp\Bigl(-i\int_{t_0}^{t}dt'\,\hat H(t')\Bigr)|\psi_S(t_0)\rangle,\\[4pt]
\mathcal T\exp\Bigl(-i\int_{t_0}^{t}dt'\,\hat H(t')\Bigr)
:=\sum_{n=0}^{\infty}\frac{(-i)^n}{n!}\int_{t_0}^{t}dt_1\cdots dt_n\,
\mathcal T[\hat H(t_1)\cdots\hat H(t_n)].
\end{gathered}
}
\right.
\tag{2.20}
```

Alternatively, differentiate the $`n`$-th term of (2.20) with respect to $`t`$: each of the $`n`$ integration variables may take the upper limit $`t`$, which is then the latest time, so $`\mathcal T`$ places $`\hat H(t)`$ leftmost; the $`n`$ contributions are equal and give $`-i\hat H(t)`$ times the $`(n-1)`$-th term. Thus the series satisfies (2.13) and equals $`|\psi_S(t_0)\rangle`$ at $`t=t_0`$; the solution is unique. If $`[\hat H(t_1),\hat H(t_2)]=0`$, $`\mathcal T`$ can be dropped and (2.20) reduces to (2.16).

**Evolution Operator**

In each case the solution is linear in $`|\psi_S(t_0)\rangle`$:

```math
\left.
|\psi_S(t)\rangle=\hat U(t,t_0)\,|\psi_S(t_0)\rangle,
\qquad
i\frac{\partial}{\partial t}\hat U(t,t_0)=\hat H(t)\,\hat U(t,t_0),
\qquad
\hat U(t_0,t_0)=1,
\right.
\tag{2.21}
```

where the evolution operator $`\hat U(t,t_0)`$ is $`e^{-i\hat H(t-t_0)}`$, $`\exp\bigl(-i\int_{t_0}^{t}dt'\,\hat H(t')\bigr)`$ or $`\mathcal T\exp\bigl(-i\int_{t_0}^{t}dt'\,\hat H(t')\bigr)`$ in cases (1), (2) or (3). Since $`\hat H(t)`$ is Hermitian, $`\partial_t(\hat U^\dagger\hat U)=i\hat U^\dagger(\hat H^\dagger-\hat H)\hat U=0`$, so $`\hat U(t,t_0)`$ is unitary. Both sides of $`\hat U(t_2,t_1)\hat U(t_1,t_0)=\hat U(t_2,t_0)`$ satisfy (2.21) in $`t_2`$ and agree at $`t_2=t_1`$, so this composition law holds; at $`t_2=t_0`$ it gives $`\hat U(t,t_0)^\dagger=\hat U(t_0,t)`$.

<br><br>

<a id="heisenberg-picture"></a>
#### Heisenberg Picture

The Heisenberg picture is obtained from the Schrödinger picture by the transformation

```math
\left.
\boxed{
\begin{gathered}
|\psi_H(t)\rangle:=\hat U(t,0)^\dagger\,|\psi_S(t)\rangle=|\psi_S(0)\rangle,\\[4pt]
\hat O_H(t):=\hat U(t,0)^\dagger\,\hat O_S(t)\,\hat U(t,0).
\end{gathered}
}
\right.
\tag{2.22}
```

The two pictures coincide at $`t=0`$, and $`\langle\psi_H(t)|\hat O_H(t)|\psi_H(t)\rangle=\langle\psi_S(t)|\hat O_S(t)|\psi_S(t)\rangle`$. Hence $`i\partial_t|\psi_H(t)\rangle=0`$. 

Writing $`\hat U`$ for $`\hat U(t,0)`$ and differentiating the second of (2.22) with (2.13) and (2.21),

```math
\left.
\begin{aligned}
\frac{d\hat O_H}{dt}
&=\Bigl(\frac{\partial\hat U}{\partial t}\Bigr)^\dagger\hat O_S\,\hat U
+\hat U^\dagger\,\frac{d\hat O_S}{dt}\,\hat U
+\hat U^\dagger\hat O_S\,\frac{\partial\hat U}{\partial t}\\
&=i\,\hat U^\dagger\bigl[\hat H(t),\hat O_S\bigr]\hat U
+\hat U^\dagger\,\frac{\partial\hat O_S}{\partial t}\,\hat U\\
&=i\bigl[\hat H_H(t),\hat O_H\bigr]+\Bigl(\frac{\partial\hat O_S}{\partial t}\Bigr)_H,
\end{aligned}
\right.
\tag{2.23}
```

where $`\hat H_H(t):=\hat U^\dagger\hat H(t)\,\hat U`$ and $`(\partial\hat O_S/\partial t)_H:=\hat U^\dagger(\partial\hat O_S/\partial t)\,\hat U`$; the last step inserts $`\hat U\hat U^\dagger=1`$. In cases (1) and (2), $`\hat U(t,0)`$ commutes with $`\hat H(t)`$, so $`\hat H_H(t)=\hat H(t)`$. In case (1), (2.22) and (2.23) become

```math
\left.
\begin{gathered}
\hat O_H(t)=e^{i\hat Ht}\,\hat O_S(t)\,e^{-i\hat Ht},\\[4pt]
\frac{d\hat O_H}{dt}=i[\hat H,\hat O_H]+\Bigl(\frac{\partial\hat O_S}{\partial t}\Bigr)_H .
\end{gathered}
\right.
\tag{2.24}
```

<br><br>

<a id="qft-ch3"></a>
## 3. The Standard Model

<a id="yang-mills"></a>
### 3.1 Yang–Mills Theory

**Lie Group**

```math
\left.
\begin{aligned}
U(n)&=\{A\in M_n(\mathbb C)\mid A^\dagger A=I\},\\[6pt]
SU(n)&=\{A\in M_n(\mathbb C)\mid \det A=1,\ A^\dagger A=I\}.
\end{aligned}
\right.
\tag{3.1}
```


**$`U(n)`$**

Consider the one-parameter subgroup

```math
\left.
\begin{aligned}
g(\theta)&=e^{i\theta T},\qquad \theta\in\mathbb R,\quad T\in M_n(\mathbb C),\\[6pt]
\left.\frac{d}{d\theta}g(\theta)\right|_{\theta=0}&=iT,\\[6pt]
g^\dagger(\theta)g(\theta)=I\quad\text{for all }\theta\in\mathbb R
&\Longrightarrow i(T-T^\dagger)=0
\Longrightarrow T^\dagger=T.
\end{aligned}
\right.
\tag{3.2}
```

 The Lie algebra is

```math
\left.
\mathfrak{u}(n)=\{iT\in M_n(\mathbb C)\mid T^\dagger=T\}.
\right.
\tag{3.3}
```


**$`SU(n)`$**

The one-parameter subgroup and its generator are

```math
\left.
\begin{aligned}
g(\theta)&=e^{i\theta T},\qquad \theta\in\mathbb R,\quad T\in M_n(\mathbb C),\\[6pt]
\left.\frac{d}{d\theta}g(\theta)\right|_{\theta=0}&=iT.
\end{aligned}
\right.
\tag{3.4}
```


```math
\left.
0=\left.\frac{d}{d\theta}\bigl[g^\dagger(\theta)g(\theta)\bigr]\right|_{\theta=0}
=i(T-T^\dagger)
\quad\Longrightarrow\quad T^\dagger=T.
\right.
\tag{3.5}
```

We use the theorem $`\det(e^{i\theta T})=e^{i\theta\,\mathop{\rm tr}\nolimits\,T}`$, valid for any $`T\in M_n(\mathbb C)`$ and $`\theta\in\mathbb C`$.

```math
\left.
0=\left.\frac{d}{d\theta}\det g(\theta)\right|_{\theta=0}
=\left.\frac{d}{d\theta}e^{i\theta\,\mathop{\rm tr}\nolimits\,T}\right|_{\theta=0}
=i\,\mathop{\rm tr}\nolimits\,T
\quad\Longrightarrow\quad \mathop{\rm tr}\nolimits\,T=0.
\right.
\tag{3.6}
```

Thus $`T`$ is traceless and Hermitian, and the Lie algebra is

```math
\left.
\mathfrak{su}(n)=\{iT\in M_n(\mathbb C)\mid
\mathop{\rm tr}\nolimits\,T=0,\ T^\dagger=T\}.
\right.
\tag{3.7}
```

Scalar multiplication is taken over $`\mathbb R`$ to preserve anti-Hermiticity; hence $`\mathfrak{su}(n)`$ and  $`\mathfrak{u}(n)`$ are both real Lie algebras.

<a id="ym-4"></a>
**Structure Constants**

Let $`\{iT^a\}`$, with $`a=1,\ldots,n^2-1`$, be a basis of the real Lie algebra $`\mathfrak{su}(n)`$.
The structure constants $`f^{abc}`$ are defined by $`[T^a,T^b]=if^{abc}T^c`$.

**Reality: $`f^{abc}\in\mathbb R`$.**

Since the matrices $`T^a`$ are Hermitian,

```math
\left.
\begin{aligned}
([T^a,T^b])^\dagger&=-[T^a,T^b],\qquad
\mathop{\rm tr}\nolimits [T^a,T^b]=0,\\[6pt]
[T^a,T^b]&\in\mathfrak{su}(n),\\[6pt]
[T^a,T^b]&=f^{abc}(iT^c),\qquad f^{abc}\in\mathbb R.
\end{aligned}
\right.
\tag{3.8}
```

The expansion coefficients are real because $`\{iT^c\}`$ is a basis over $`\mathbb R`$.

<a id="ym-orthonormal"></a>
**Orthonormal Basis of $`\mathfrak{su}(n)`$**

For $`iT_1,iT_2\in\mathfrak{su}(n)`$, define

```math
\left.
\begin{aligned}
(\cdot,\cdot)&:\mathfrak{su}(n)\times\mathfrak{su}(n)\longrightarrow\mathbb R,\\[6pt]
(iT_1,iT_2)&:=-2\,\mathop{\rm tr}\nolimits \bigl[(iT_1)(iT_2)\bigr]\\
&=2\,\mathop{\rm tr}\nolimits (T_1T_2).
\end{aligned}
\right.
\tag{3.9}
```

**Proof** that (3.9) satisfies the axioms of an inner product



*(i) Real values.* 

Using $`T_1^\dagger=T_1`$, $`T_2^\dagger=T_2`$ and cyclicity of the trace,

```math
\left.
\begin{aligned}
\bigl[\mathop{\rm tr}\nolimits (T_1T_2)\bigr]^*
&=\mathop{\rm tr}\nolimits \bigl[(T_1T_2)^\dagger\bigr]
=\mathop{\rm tr}\nolimits (T_2^\dagger T_1^\dagger)\\
&=\mathop{\rm tr}\nolimits (T_2T_1)
=\mathop{\rm tr}\nolimits (T_1T_2),
\end{aligned}
\right.
\tag{3.10}
```

so $`(iT_1,iT_2)=2\,\mathop{\rm tr}\nolimits (T_1T_2)\in\mathbb R`$.

*(ii) Symmetry.* 

By cyclicity of the trace,

```math
\left.
\begin{aligned}
(iT_1,iT_2)&=2\,\mathop{\rm tr}\nolimits (T_1T_2)\\
&=2\,\mathop{\rm tr}\nolimits (T_2T_1)=(iT_2,iT_1).
\end{aligned}
\right.
\tag{3.11}
```

*(iii) Bilinearity.* 

For $`a,b\in\mathbb R`$, $`a\,iT_1+b\,iT_2=i(aT_1+bT_2)`$, 
and linearity of the trace gives $`(a\,iT_1+b\,iT_2,\,iT_3)=2\,\mathop{\rm tr}\nolimits \bigl[(aT_1+bT_2)T_3\bigr]=a\,(iT_1,iT_3)+b\,(iT_2,iT_3)`$. By (ii), the form is also linear in its second argument.

*(iv) Positive definiteness.* Using $`T=T^\dagger`$,

```math
\left.
\begin{aligned}
(iT,iT)&=2\,\mathop{\rm tr}\nolimits (T^2)=2\,\mathop{\rm tr}\nolimits (T^\dagger T)\\
&=2\sum_{j,k}|T_{jk}|^2\ge0.
\end{aligned}
\right.
\tag{3.12}
```

Equality holds if and only if $`T_{jk}=0`$ for all $`j,k`$, i.e. $`iT=0`$. $`\square`$

Having established that this form defines an inner product on $`\mathfrak{su}(n)`$, we may choose an orthonormal basis $`\{iT^a\}`$ satisfying $`(iT^a,iT^b)=\delta^{ab}`$. Equivalently,

```math
\left.
\boxed{\mathop{\rm tr}\nolimits (T^aT^b)=\frac12\delta^{ab}.}
\right.
\tag{3.13}
```

**Total antisymmetry.** With this normalization and cyclicity of the trace, we obtain

```math
\left.
\begin{aligned}
\mathop{\rm tr}\nolimits ([T^a,T^b]T^c)&=\frac{i}{2}f^{abc},\\
f^{abc}&=-2i\,\mathop{\rm tr}\nolimits ([T^a,T^b]T^c),\\
f^{bac}&=-f^{abc},\\
f^{acb}
&=-2i\,\mathop{\rm tr}\nolimits (T^aT^cT^b-T^cT^aT^b)\\
&=-2i\,\mathop{\rm tr}\nolimits (T^bT^aT^c-T^aT^bT^c)
=-f^{abc}.
\end{aligned}
\right.
\tag{3.14}
```

```math
\left.
\boxed{
f^{abc}=f^{[abc]}\in\mathbb R
}
\right.
\tag{3.15}
```

<a id="ym-5"></a>
**Local Symmetry and Covariant Derivative**

Fiber bundles provide a useful geometric picture of fields in Yang–Mills theory.
In this picture, an internal space is attached to each spacetime point, and the field takes its value in that space.
This makes an additional freedom explicit: we may choose a basis in each internal space,
and this choice can vary from point to point.
This local freedom of choice underlies gauge symmetry.

Building on this idea, we now develop the framework of gauge theory.

The field operator is defined as

```math
\left.
\Psi(x):=\begin{pmatrix}
\psi_1(x)\\
\vdots\\
\psi_n(x)
\end{pmatrix}.
\right.
\tag{3.16}
```

Define the Dirac adjoint by

```math
\left.
\begin{aligned}
\bar\Psi(x)&:=\bigl(\bar\psi_1(x),\ldots,\bar\psi_n(x)\bigr),\\[6pt]
\bar\psi_a(x)&:=\psi_a^\dagger(x)\gamma^0.
\end{aligned}
\right.
\tag{3.17}
```

The kinetic term of the Lagrangian density is

```math
\left.
\begin{aligned}
\mathcal L_{\mathrm{kin}}
&=\bar\Psi\,i\gamma^\mu I_n\partial_\mu\Psi\\[6pt]
&=\sum_{a=1}^{n}\bar\psi_a\,i\gamma^\mu\partial_\mu\psi_a.
\end{aligned}
\right.
\tag{3.18}
```



For $`SU(n)`$ in the defining representation $`U`$, let $`g_{\mathrm{YM}}`$ be the coupling and $`U(\theta)`$ the representation of the local group element. The connection and its transformation are

```math
\left.
\begin{aligned}
U(\theta)&:=e^{i\theta^a(x)T^a},\qquad \theta^a(x)\in\mathbb R,\\
A_\mu&:=A_\mu^aT^a,\qquad D_\mu:=\partial_\mu-ig_{\mathrm{YM}}A_\mu,
\qquad \Psi'=U(\theta)\Psi,\\
A_\mu'&=U(\theta)A_\mu U(\theta)^\dagger-\frac{i}{g_{\mathrm{YM}}}\bigl(\partial_\mu U(\theta)\bigr)U(\theta)^\dagger,\\
D_\mu'&=U(\theta)D_\mu U(\theta)^\dagger .
\end{aligned}
\right.
\tag{3.19}
```

The field strength is

```math
\left.
\begin{aligned}
[D_\mu,D_\nu]&=:-ig_{\mathrm{YM}}F_{\mu\nu},\\
F_{\mu\nu}&=\partial_\mu A_\nu-\partial_\nu A_\mu-ig_{\mathrm{YM}}[A_\mu,A_\nu],\\
F_{\mu\nu}^a&=\partial_\mu A_\nu^a-\partial_\nu A_\mu^a
+g_{\mathrm{YM}}f^{abc}A_\mu^bA_\nu^c,\\
F_{\mu\nu}'&=U(\theta)F_{\mu\nu}U(\theta)^\dagger .
\end{aligned}
\right.
\tag{3.20}
```

Including the gauge field, the kinetic term (3.18) becomes

```math
\left.
\boxed{
\begin{aligned}
\mathcal L_{\mathrm{kin}}
&=\bar\Psi\,i\gamma^\mu D_\mu\Psi
-\frac12\,\mathop{\rm tr}\nolimits (F_{\mu\nu}F^{\mu\nu})\\[6pt]
&=\bar\Psi\,i\gamma^\mu D_\mu\Psi-\frac14F_{\mu\nu}^aF^{a\mu\nu}.
\end{aligned}
}
\right.
\tag{3.21}
```

On a matrix-valued adjoint field $`X`$, define $`D_\mu X:=\partial_\mu X-ig_{\mathrm{YM}}[A_\mu,X]`$.

Using the definitions above, the field equations and the Bianchi identity simplify to

```math
\left.
\begin{aligned}
i\gamma^\mu D_\mu\Psi&=0,\qquad
D_\mu F^{\mu\nu}=-g_{\mathrm{YM}}j^\nu,\qquad
j^\nu:=(\bar\Psi\gamma^\nu T^a\Psi)T^a,\\
D_\mu F_{\nu\rho}+D_\nu F_{\rho\mu}+D_\rho F_{\mu\nu}&=0 .
\end{aligned}
\right.
\tag{3.22}
```

<br><br>

<a id="qed"></a>
### 3.2 Quantum Electrodynamics


**Gauge Group $`U(1)`$**

The gauge group of QED is $`U(1)`$, i.e. (3.1) with $`n=1`$; its Lie algebra $`\mathfrak u(1)=i\mathbb R`$ is Abelian. 

Let $`e>0`$ be the elementary charge and $`\theta:\mathbb R^4\to\mathbb R`$. The transformation is a flavor singlet: it acts identically on the three generations. It differs between representations of $`U(1)`$, which are labeled by the charge: a Dirac field $`\psi_f`$ as in (1.94) with charge $`Q_fe`$ transforms, with the same $`\theta`$ for every $`f`$, as

```math
\left.
\begin{aligned}
\psi_f'(x)&=e^{iQ_f\theta(x)}\psi_f(x),\qquad
\bar\psi_f'(x)=\bar\psi_f(x)\,e^{-iQ_f\theta(x)},\\[6pt]
Q_f&=\begin{cases}
\tfrac23, & f=u,c,t,\\
-\tfrac13, & f=d,s,b,\\
-1, & f=e,\mu,\tau,\\
0, & f=\nu_e,\nu_\mu,\nu_\tau.
\end{cases}
\end{aligned}
\right.
\tag{3.23}
```

**Covariant Derivative and Field Strength**

The photon field $`A_\mu`$ is real. Taking $`U(\theta)=e^{iQ\theta}`$ and replacing $`g_{\mathrm{YM}}A_\mu`$ by $`eQA_\mu`$ in (3.19)–(3.20) gives

```math
\left.
\begin{aligned}
D_\mu&:=\partial_\mu-ieQA_\mu,\qquad
D_\mu'\psi'=e^{iQ\theta}D_\mu\psi,\\
A_\mu'&=A_\mu+\frac1e\,\partial_\mu\theta,\\
[D_\mu,D_\nu]&=-ieQF_{\mu\nu},\qquad
F_{\mu\nu}=\partial_\mu A_\nu-\partial_\nu A_\mu=F_{\mu\nu}'.
\end{aligned}
\right.
\tag{3.24}
```



**The QED Lagrangian**

```math
\left.
\boxed{
\mathcal L_{\mathrm{QED}}
=\bar\psi\bigl(i\gamma^\mu D_\mu-m\bigr)\psi
-\frac14F_{\mu\nu}F^{\mu\nu},
}
\right.
\tag{3.25}
```

where $`m`$ is the mass of $`\psi`$ and $`D_\mu`$ acts on the $`\psi`$ to its right. By (3.23)–(3.24), $`\mathcal L_{\mathrm{QED}}`$ is gauge invariant. Substituting $`D_\mu`$,

```math
\left.
\mathcal L_{\mathrm{QED}}
=\bar\psi\bigl(i\gamma^\mu\partial_\mu-m\bigr)\psi
-\frac14F_{\mu\nu}F^{\mu\nu}
+eQA_\mu\bar\psi\gamma^\mu\psi,
\right.
\tag{3.26}
```

i.e. the Dirac Lagrangian (1.94), the Maxwell Lagrangian (1.147) and the interaction term.



**Equations of Motion**

With $`j^\nu=\bar\psi\gamma^\nu\psi`$ as in (1.132), $`\partial\mathcal L_{\mathrm{QED}}/\partial(\partial_\mu A_\nu)=-F^{\mu\nu}`$ and $`\partial\mathcal L_{\mathrm{QED}}/\partial A_\nu=eQ\,j^\nu`$. The Euler–Lagrange equations and the Bianchi identity are

```math
\left.
\begin{aligned}
\bigl(i\gamma^\mu D_\mu-m\bigr)\psi&=0,\qquad
\partial_\mu F^{\mu\nu}=-eQ\,j^\nu,\qquad
\partial_\nu j^\nu=0,\\
\partial_\mu F_{\nu\rho}+\partial_\nu F_{\rho\mu}+\partial_\rho F_{\mu\nu}&=0 .
\end{aligned}
\right.
\tag{3.27}
```

<br><br>

<a id="qcd"></a>
### 3.3 Quantum Chromodynamics

**Color Group $`SU(3)`$**

The gauge group of QCD is $`SU(3)`$. By (3.7) with $`n=3`$, $`\mathfrak{su}(3)`$ has a basis $`\{iT^a\}`$, $`a=1,\ldots,8`$, which we take orthonormal in the sense of (3.13). The standard choice is $`T^a:=\tfrac12\lambda^a`$, where the Gell-Mann matrices are

```math
\left.
\begin{aligned}
\lambda^1&=\begin{pmatrix}0&1&0\\1&0&0\\0&0&0\end{pmatrix},&
\lambda^2&=\begin{pmatrix}0&-i&0\\i&0&0\\0&0&0\end{pmatrix},&
\lambda^3&=\begin{pmatrix}1&0&0\\0&-1&0\\0&0&0\end{pmatrix},\\[6pt]
\lambda^4&=\begin{pmatrix}0&0&1\\0&0&0\\1&0&0\end{pmatrix},&
\lambda^5&=\begin{pmatrix}0&0&-i\\0&0&0\\i&0&0\end{pmatrix},&
\lambda^6&=\begin{pmatrix}0&0&0\\0&0&1\\0&1&0\end{pmatrix},\\[6pt]
\lambda^7&=\begin{pmatrix}0&0&0\\0&0&-i\\0&i&0\end{pmatrix},&
\lambda^8&=\frac1{\sqrt3}\begin{pmatrix}1&0&0\\0&1&0\\0&0&-2\end{pmatrix}.
\end{aligned}
\right.
\tag{3.28}
```

Each $`\lambda^a`$ is Hermitian and traceless, and $`\mathop{\rm tr}\nolimits (\lambda^a\lambda^b)=2\delta^{ab}`$, so $`\mathop{\rm tr}\nolimits (T^aT^b)=\tfrac12\delta^{ab}`$ as in (3.13). By (3.14), $`f^{abc}=-2i\,\mathop{\rm tr}\nolimits ([T^a,T^b]T^c)`$; up to the antisymmetry (3.15), the nonzero structure constants are

```math
\left.
\begin{aligned}
f^{123}&=1,\\[4pt]
f^{147}=f^{246}=f^{257}=f^{345}&=\tfrac12,\qquad
f^{156}=f^{367}=-\tfrac12,\\[4pt]
f^{458}=f^{678}&=\tfrac{\sqrt3}{2}.
\end{aligned}
\right.
\tag{3.29}
```

The quadratic Casimir $`T^aT^a`$ commutes with every $`T^b`$, since $`f^{bac}`$ is antisymmetric in $`a,c`$:

```math
\left.
[T^b,T^aT^a]=[T^b,T^a]T^a+T^a[T^b,T^a]=if^{bac}\bigl(T^cT^a+T^aT^c\bigr)=0.
\right.
\tag{3.30}
```

The defining representation of $`SU(3)`$ is irreducible, so by Schur's lemma $`T^aT^a=C_FI_3`$. Taking the trace with (3.13),

```math
\left.
3C_F=\mathop{\rm tr}\nolimits (T^aT^a)=\tfrac12\cdot8
\quad\Longrightarrow\quad
\boxed{T^aT^a=C_FI_3,\qquad C_F=\tfrac43.}
\right.
\tag{3.31}
```

**Quark Fields**

For each flavor $`f\in\{u,d,s,c,b,t\}`$ the quark field is a color triplet, i.e. the multiplet (3.16) with $`n=3`$, with Dirac adjoint as in (3.17):

```math
\left.
q_f(x):=\begin{pmatrix}\psi_{f,1}(x)\\\psi_{f,2}(x)\\\psi_{f,3}(x)\end{pmatrix},
\qquad
\bar q_f(x):=\bigl(\bar\psi_{f,1}(x),\bar\psi_{f,2}(x),\bar\psi_{f,3}(x)\bigr).
\right.
\tag{3.32}
```

Throughout this section $`\gamma^\mu`$ acts on the spinor index of each $`\psi_{f,a}`$ and the $`3\times3`$ matrices $`T^a`$ act on the color index, so $`\gamma^\mu`$ commutes with every matrix built from the $`T^a`$.

**Local $`SU(3)`$ Transformation**

Let $`\theta^a:\mathbb R^4\to\mathbb R`$, $`a=1,\ldots,8`$, and set

```math
\left.
g(x):=e^{i\theta^a(x)T^a}\in SU(3).
\right.
\tag{3.33}
```

This is the internal transformation (1.66) with $`g`$ now depending on $`x`$. The quark fields transform as

```math
\left.
q_f'(x)=g(x)\,q_f(x),\qquad
\bar q_f'(x)=\bar q_f(x)\,g^\dagger(x).
\right.
\tag{3.34}
```

Since $`\partial_\mu(gq_f)=g\,\partial_\mu q_f+(\partial_\mu g)\,q_f`$, the derivative term of (3.18) is not invariant under (3.34):

```math
\left.
\bar q_f'\,i\gamma^\mu\partial_\mu q_f'
=\bar q_f\,i\gamma^\mu\partial_\mu q_f
+\bar q_f\,i\gamma^\mu g^\dagger(\partial_\mu g)\,q_f.
\right.
\tag{3.35}
```

**Covariant Derivative and Gluon Fields**

Introduce eight real vector fields $`A^a_\mu`$, the gluon fields, and define

```math
\left.
A_\mu:=A^a_\mu T^a,\qquad
D_\mu:=\partial_\mu-ig_sA_\mu,
\right.
\tag{3.36}
```

where $`g_s\in\mathbb R`$ is the strong coupling constant and $`D_\mu`$ acts on color triplets. Let $`A_\mu'`$ denote the transformed gluon field and $`D_\mu':=\partial_\mu-ig_sA_\mu'`$. We require $`D_\mu'q_f'=g\,D_\mu q_f`$:

```math
\left.
\begin{aligned}
D_\mu'(gq_f)&=g\,\partial_\mu q_f+(\partial_\mu g)\,q_f-ig_sA_\mu'\,g\,q_f,\\[6pt]
g\,D_\mu q_f&=g\,\partial_\mu q_f-ig_s\,gA_\mu\,q_f.
\end{aligned}
\right.
\tag{3.37}
```

Equating the two for all $`q_f`$ gives $`A_\mu'g=gA_\mu-\frac{i}{g_s}\partial_\mu g`$, i.e.

```math
\left.
\boxed{
A_\mu'=gA_\mu g^\dagger-\frac{i}{g_s}(\partial_\mu g)\,g^\dagger
=gA_\mu g^\dagger+\frac{i}{g_s}\,g\,\partial_\mu g^\dagger.
}
\right.
\tag{3.38}
```

Differentiating $`gg^\dagger=I_3`$ gives $`\bigl((\partial_\mu g)g^\dagger\bigr)^\dagger=-(\partial_\mu g)g^\dagger`$, and Jacobi's formula $`\partial_\mu\det g=\det g\,\mathop{\rm tr}\nolimits (g^\dagger\partial_\mu g)`$ with $`\det g=1`$ gives $`\mathop{\rm tr}\nolimits \bigl((\partial_\mu g)g^\dagger\bigr)=0`$. Hence $`A_\mu'`$ is again Hermitian and traceless, $`A_\mu'=A_\mu'^aT^a`$ with real $`A_\mu'^a`$.

Since $`D_\mu'(gq_f)=g\,D_\mu q_f`$ holds for all $`q_f`$, as operators on color triplets

```math
\left.
D_\mu'=g\,D_\mu\,g^\dagger.
\right.
\tag{3.39}
```

For infinitesimal $`\theta^a`$, $`g=I_3+i\theta^aT^a+O(\theta^2)`$ and (3.38) gives

```math
\left.
\begin{aligned}
A_\mu'&=A_\mu+i\theta^b[T^b,A_\mu]+\frac1{g_s}(\partial_\mu\theta^a)T^a+O(\theta^2)\\
&=A_\mu-f^{bca}\theta^bA^c_\mu T^a+\frac1{g_s}(\partial_\mu\theta^a)T^a+O(\theta^2),\\[6pt]
\delta A^a_\mu:=A_\mu'^a-A_\mu^a
&=\frac1{g_s}\partial_\mu\theta^a+f^{abc}A^b_\mu\theta^c+O(\theta^2).
\end{aligned}
\right.
\tag{3.40}
```

**Field Strength**

Define $`F_{\mu\nu}`$ by $`[D_\mu,D_\nu]=:-ig_sF_{\mu\nu}`$. Since $`[\partial_\mu,A_\nu]q_f=(\partial_\mu A_\nu)q_f`$,

```math
\left.
\begin{aligned}
[D_\mu,D_\nu]
&=[\partial_\mu-ig_sA_\mu,\ \partial_\nu-ig_sA_\nu]\\
&=-ig_s\bigl(\partial_\mu A_\nu-\partial_\nu A_\mu\bigr)-g_s^2[A_\mu,A_\nu],\\[6pt]
F_{\mu\nu}&=\partial_\mu A_\nu-\partial_\nu A_\mu-ig_s[A_\mu,A_\nu].
\end{aligned}
\right.
\tag{3.41}
```

Expanding in the basis, $`F_{\mu\nu}=F^a_{\mu\nu}T^a`$ with

```math
\left.
\boxed{
F^a_{\mu\nu}=\partial_\mu A^a_\nu-\partial_\nu A^a_\mu+g_sf^{abc}A^b_\mu A^c_\nu.
}
\right.
\tag{3.42}
```

By (3.39), $`[D_\mu',D_\nu']=g[D_\mu,D_\nu]g^\dagger`$, so

```math
\left.
F_{\mu\nu}'=gF_{\mu\nu}g^\dagger,
\qquad
\delta F^a_{\mu\nu}=f^{abc}F^b_{\mu\nu}\theta^c+O(\theta^2).
\right.
\tag{3.43}
```

By cyclicity of the trace and (3.13),

```math
\left.
\mathop{\rm tr}\nolimits \bigl(F_{\mu\nu}'F'^{\mu\nu}\bigr)
=\mathop{\rm tr}\nolimits \bigl(F_{\mu\nu}F^{\mu\nu}\bigr)
=\tfrac12F^a_{\mu\nu}F^{a\mu\nu}.
\right.
\tag{3.44}
```

**The QCD Lagrangian**

```math
\left.
\boxed{
\mathcal L_{\mathrm{QCD}}
=\sum_{f}\bar q_f\bigl(i\gamma^\mu D_\mu-m_f\bigr)q_f
-\frac12\,\mathop{\rm tr}\nolimits \bigl(F_{\mu\nu}F^{\mu\nu}\bigr)
=\sum_{f}\bar q_f\bigl(i\gamma^\mu D_\mu-m_f\bigr)q_f
-\frac14F^a_{\mu\nu}F^{a\mu\nu},
}
\right.
\tag{3.45}
```

where the sum runs over the six flavors in (3.32), $`m_f`$ is the mass of flavor $`f`$, and $`D_\mu`$ acts on the $`q_f`$ to its right. Under (3.34) and (3.38), $`D_\mu'q_f'=g\,D_\mu q_f`$ by construction, so

```math
\left.
\bar q_f'\bigl(i\gamma^\mu D_\mu'-m_f\bigr)q_f'
=\bar q_f\,g^\dagger\bigl(i\gamma^\mu g\,D_\mu-m_f\,g\bigr)q_f
=\bar q_f\bigl(i\gamma^\mu D_\mu-m_f\bigr)q_f.
\right.
\tag{3.46}
```

Together with (3.44), $`\mathcal L_{\mathrm{QCD}}`$ is invariant under the local transformations (3.34), (3.38).

Substituting (3.36) and (3.42) into (3.45) separates the free and interaction terms:

```math
\left.
\begin{aligned}
\mathcal L_{\mathrm{QCD}}
={}&\sum_f\bar q_f\bigl(i\gamma^\mu\partial_\mu-m_f\bigr)q_f
-\frac14\bigl(\partial_\mu A^a_\nu-\partial_\nu A^a_\mu\bigr)\bigl(\partial^\mu A^{a\nu}-\partial^\nu A^{a\mu}\bigr)\\[6pt]
&+g_sA^a_\mu\sum_f\bar q_f\gamma^\mu T^aq_f
-\frac{g_s}{2}f^{abc}\bigl(\partial_\mu A^a_\nu-\partial_\nu A^a_\mu\bigr)A^{b\mu}A^{c\nu}
-\frac{g_s^2}{4}f^{abc}f^{ade}A^b_\mu A^c_\nu A^{d\mu}A^{e\nu}.
\end{aligned}
\right.
\tag{3.47}
```

**Equations of Motion**

Treating $`q_f`$, $`\bar q_f`$ and $`A^a_\mu`$ as independent, the Euler–Lagrange equation for $`\bar q_f`$ is

```math
\left.
\bigl(i\gamma^\mu D_\mu-m_f\bigr)q_f=0.
\right.
\tag{3.48}
```

For $`A^a_\nu`$, define the color current $`j^{a\nu}:=\sum_f\bar q_f\gamma^\nu T^aq_f`$. From (3.45) with (3.42) and (3.47),

```math
\left.
\begin{aligned}
\frac{\partial\mathcal L_{\mathrm{QCD}}}{\partial(\partial_\mu A^a_\nu)}
&=-\frac12F^{b\rho\sigma}\,\delta^{ab}\bigl(\delta^\mu_\rho\delta^\nu_\sigma-\delta^\mu_\sigma\delta^\nu_\rho\bigr)
=-F^{a\mu\nu},\\[6pt]
\frac{\partial\mathcal L_{\mathrm{QCD}}}{\partial A^a_\nu}
&=g_sj^{a\nu}-\frac12F^{b\rho\sigma}\,g_s\bigl(f^{bad}\delta^\nu_\rho A^d_\sigma+f^{bca}A^c_\rho\delta^\nu_\sigma\bigr)\\
&=g_sj^{a\nu}-g_sf^{abc}A^c_\mu F^{b\mu\nu}\\
&=g_sj^{a\nu}+g_sf^{abc}A^b_\mu F^{c\mu\nu}.
\end{aligned}
\right.
\tag{3.49}
```

The Euler–Lagrange equation $`\partial_\mu\bigl(\partial\mathcal L_{\mathrm{QCD}}/\partial(\partial_\mu A^a_\nu)\bigr)=\partial\mathcal L_{\mathrm{QCD}}/\partial A^a_\nu`$ then reads

```math
\left.
\boxed{
\partial_\mu F^{a\mu\nu}+g_sf^{abc}A^b_\mu F^{c\mu\nu}=-g_sj^{a\nu}.
}
\right.
\tag{3.50}
```

The left-hand side is the $`a`$-component of $`\partial_\mu F^{\mu\nu}-ig_s[A_\mu,F^{\mu\nu}]`$, the covariant derivative of $`F^{\mu\nu}`$ in the adjoint representation; with $`j^\nu:=j^{a\nu}T^a`$, (3.50) is

```math
\left.
D_\mu F^{\mu\nu}:=\partial_\mu F^{\mu\nu}-ig_s[A_\mu,F^{\mu\nu}]=-g_s\,j^\nu.
\right.
\tag{3.51}
```

<br><br>

<a id="higgs-mechanism"></a>
### 3.4 Spontaneous Symmetry Breaking and the Higgs Mechanism

<a id="higgs-lagrangian"></a>
#### Higgs Lagrangian

Let $`\Phi:=(\phi_1,\ldots,\phi_n)^T`$ be a multiplet of complex scalar fields. For $`\mu_H^2\in\mathbb R`$ and $`\lambda_H>0`$, the Higgs Lagrangian is

```math
\left.
\boxed{
\begin{aligned}
\mathcal L_{\mathrm{Higgs}}&=(\partial_\mu\Phi)^\dagger\partial^\mu\Phi-V(\Phi),\\
V(\Phi)&=-\mu_H^2\,\Phi^\dagger\Phi+\lambda_H(\Phi^\dagger\Phi)^2 .
\end{aligned}
}
\right.
\tag{3.52}
```

The Lagrangian (3.52) depends on $`\Phi`$ only through $`\Phi^\dagger\Phi`$ and $`(\partial_\mu\Phi)^\dagger\partial^\mu\Phi`$. For a constant $`g\in U(n)`$,

```math
\left.
\begin{aligned}
\Phi'&=g\,\Phi,\\
\Phi'^\dagger\Phi'&=\Phi^\dagger g^\dagger g\,\Phi=\Phi^\dagger\Phi,\\
(\partial_\mu\Phi')^\dagger\partial^\mu\Phi'&=(\partial_\mu\Phi)^\dagger g^\dagger g\,\partial^\mu\Phi=(\partial_\mu\Phi)^\dagger\partial^\mu\Phi,
\end{aligned}
\right.
\tag{3.53}
```

so $`\mathcal L_{\mathrm{Higgs}}`$ is invariant under global $`U(n)`$ transformations.

**Physical Vacuum**

The classical vacuum is the field configuration of minimum energy. The energy density of (3.52) is

```math
\left.
\mathcal H=(\partial_0\Phi)^\dagger\partial_0\Phi+\sum_{i=1}^3(\partial_i\Phi)^\dagger\partial_i\Phi+V(\Phi).
\right.
\tag{3.54}
```

The first two terms are nonnegative, so the classical vacuum is a constant $`\Phi=\Phi_0`$ minimizing $`V`$. Since $`\partial V/\partial(\Phi^\dagger\Phi)=-\mu_H^2+2\lambda_H\Phi^\dagger\Phi`$ and $`\Phi^\dagger\Phi\ge0`$,

```math
\left.
\boxed{
\begin{aligned}
\mu_H^2\le0:&\quad\Phi_0=0,\\
\mu_H^2>0:&\quad\Phi_0^\dagger\Phi_0=\frac{v^2}{2},\qquad
v:=\sqrt{\frac{\mu_H^2}{\lambda_H}},\qquad
V(\Phi_0)=-\frac{\lambda_Hv^4}{4}.
\end{aligned}
}
\right.
\tag{3.55}
```

For $`\mu_H^2\le0`$ the vacuum $`\Phi_0=0`$ is invariant under all of $`U(n)`$. From now on $`\mu_H^2>0`$: the vacua form the sphere $`\Phi_0^\dagger\Phi_0=v^2/2`$ in $`\mathbb C^n`$, and $`\Phi=0`$ is a local maximum of $`V`$. The physical vacuum is a single point of this sphere. We choose

```math
\left.
\boxed{
\Phi_0:=\frac1{\sqrt2}\begin{pmatrix}0\\\vdots\\0\\v\end{pmatrix}
}
\right.
\tag{3.56}
```

and from now on $`\Phi_0`$ denotes this vacuum.

 Any vacuum $`\Phi_0'`$ with $`\Phi_0'^\dagger\Phi_0'=v^2/2`$ equals $`g\,\Phi_0`$, where $`g\in U(n)`$ has last column $`\sqrt2\,\Phi_0'/v`$ and its other columns complete it to an orthonormal basis of $`\mathbb C^n`$; by (3.53), different choices are related by a symmetry transformation.

<br><br>

<a id="spontaneous-symmetry-breaking"></a>
#### Spontaneous Symmetry Breaking

A transformation $`g\in U(n)`$ is unbroken if it leaves the vacuum invariant. The unbroken subgroup is

```math
\left.
\boxed{
G_0:=\{g\in U(n)\mid g\,\Phi_0=\Phi_0\}\cong U(n-1).
}
\right.
\tag{3.57}
```

A unitary $`g`$ with $`g\Phi_0=\Phi_0`$ maps the orthogonal complement $`\Phi_0^\perp:=\{u\in\mathbb C^n\mid\Phi_0^\dagger u=0\}`$ to itself, and $`g\mapsto g|_{\Phi_0^\perp}`$ identifies $`G_0`$ with the unitary group of the $`(n-1)`$-dimensional space $`\Phi_0^\perp`$.

$`U(n)`$ is spontaneously broken to $`G_0`$ if $`G_0\neq U(n)`$, i.e. if the Lagrangian is invariant under $`U(n)`$ but the vacuum is not; by (3.57), $`U(n)`$ is spontaneously broken to $`G_0\cong U(n-1)`$.

Let $`T^a`$, $`a=1,\ldots,n^2`$, be Hermitian generators of $`U(n)`$ with $`\mathop{\rm tr}\nolimits (T^aT^b)=\frac12\delta^{ab}`$. A Hermitian $`n\times n`$ matrix $`T`$ is an unbroken generator if $`e^{i\theta T}\in G_0`$ for all $`\theta\in\mathbb R`$; differentiating $`e^{i\theta T}\Phi_0=\Phi_0`$ at $`\theta=0`$,

```math
\left.
e^{i\theta T}\in G_0\ \ \text{for all }\theta\in\mathbb R
\iff T\Phi_0=0 .
\right.
\tag{3.58}
```

The unbroken generators form the Lie algebra of $`G_0\cong U(n-1)`$, of dimension $`(n-1)^2`$, and the broken generators are the elements of its orthogonal complement under $`\mathop{\rm tr}\nolimits\,`$, of dimension $`n^2-(n-1)^2=2n-1`$. A broken $`T\neq0`$ satisfies $`T\Phi_0\neq0`$: otherwise $`T`$ would also be unbroken, and $`\mathop{\rm tr}\nolimits (T^2)=0`$.

Let $`G^a`$, $`a=1,\ldots,2n-1`$, be a basis of the broken generators. The matrix $`\Phi_0^\dagger\{G^a,G^b\}\Phi_0=2\,\mathop{\rm Re}\nolimits \bigl[(G^a\Phi_0)^\dagger G^b\Phi_0\bigr]`$ is real and symmetric. An orthogonal change of basis $`G^a\to O^{ab}G^b`$, $`O\in O(2n-1)`$, preserves $`\mathop{\rm tr}\nolimits (G^aG^b)=\frac12\delta^{ab}`$ and acts on this matrix by $`O(\,\cdot\,)O^T`$; choosing $`O`$ to diagonalize it,

```math
\left.
\begin{aligned}
\mathop{\rm tr}\nolimits (G^aG^b)&=\frac12\delta^{ab},\\
\Phi_0^\dagger\{G^a,G^b\}\Phi_0&=2\,\delta^{ab}\,\Phi_0^\dagger(G^a)^2\Phi_0,\qquad
\Phi_0^\dagger(G^a)^2\Phi_0=(G^a\Phi_0)^\dagger G^a\Phi_0>0 .
\end{aligned}
\right.
\tag{3.59}
```

From now on $`T^a:=G^a`$ for $`a=1,\ldots,2n-1`$, and $`T^a`$, $`a=2n,\ldots,n^2`$, span the unbroken generators.


**Parametrization of the Higgs Field**

Parametrize the $`2n`$ real fields of $`\Phi`$ by the Higgs field $`h`$ and $`\theta^a`$, $`a=1,\ldots,2n-1`$, along the broken generators:

```math
\left.
\boxed{
\begin{aligned}
\Phi&=\frac1{\sqrt2}\,e^{i\theta^a(x)G^a}\begin{pmatrix}0\\\vdots\\0\\v+h\end{pmatrix}\\
&=\Bigl(1+\frac hv\Bigr)U(\theta)\,\Phi_0,\\
U(\theta)&:=e^{iX},\qquad X:=\theta^a(x)G^a .
\end{aligned}
}
\right.
\tag{3.60}
```

<br><br>

<a id="higgs-mechanism-masses"></a>
#### Higgs Mechanism

Gauge the $`U(n)`$ symmetry (3.53) with the generators $`T^a`$, $`a=1,\ldots,n^2`$, chosen after (3.59), gauge fields $`A_\mu^a`$, and coupling $`g_{\mathrm{YM}}`$ as in (3.19). Replacing $`\partial_\mu`$ by $`D_\mu`$ in (3.52) and adding the gauge kinetic term of (3.21),

```math
\left.
\boxed{
\begin{aligned}
\mathcal L&=(D_\mu\Phi)^\dagger D^\mu\Phi-V(\Phi)-\frac14F_{\mu\nu}^aF^{a\mu\nu},\\
D_\mu\Phi&=\partial_\mu\Phi-ig_{\mathrm{YM}}A_\mu\Phi,\qquad A_\mu:=A_\mu^aT^a .
\end{aligned}
}
\right.
\tag{3.61}
```

By (3.19)–(3.20) with $`T^a`$ the generators of $`U(n)`$, $`\mathcal L`$ is invariant under $`\Phi'=U(\theta)\Phi`$, $`U(\theta)=e^{i\theta^a(x)T^a}`$; for $`\theta^a=0`$, $`a\ge2n`$, this is the $`U(\theta)`$ of (3.60).

Substitute the parametrization (3.60) into (3.61). With $`\mu_H^2=\lambda_Hv^2`$ from (3.55) and $`U^\dagger U=I_n`$, the potential depends only on $`h`$:

```math
\left.
\begin{aligned}
\Phi^\dagger\Phi&=\frac{(v+h)^2}2,\\
V&=\lambda_H\Bigl(\Phi^\dagger\Phi-\frac{v^2}2\Bigr)^2-\frac{\lambda_Hv^4}4\\
&=\lambda_Hv^2h^2+\lambda_Hv\,h^3+\frac{\lambda_H}4h^4-\frac{\lambda_Hv^4}4 .
\end{aligned}
\right.
\tag{3.62}
```

For the kinetic term, $`\Phi_0^\dagger\Phi_0=v^2/2`$, and since $`A^U_\mu`$ below is Hermitian, the terms linear in $`\partial_\mu h`$ cancel:

```math
\left.
\begin{aligned}
D_\mu\Phi&=\frac{\partial_\mu h}v\,U\Phi_0-ig_{\mathrm{YM}}\Bigl(1+\frac hv\Bigr)UA^U_\mu\Phi_0,\\
A^U_\mu&:=U^\dagger A_\mu U+\frac i{g_{\mathrm{YM}}}U^\dagger\partial_\mu U,\\
(D_\mu\Phi)^\dagger D^\mu\Phi&=\frac12\partial_\mu h\,\partial^\mu h\\
&\quad+\Bigl(1+\frac hv\Bigr)^2g_{\mathrm{YM}}^2\,\Phi_0^\dagger A^U_\mu A^{U\mu}\Phi_0 .
\end{aligned}
\right.
\tag{3.63}
```

Substituting (3.62) and (3.63) into (3.61),

```math
\left.
\boxed{
\begin{aligned}
\mathcal L={}&\frac12\partial_\mu h\,\partial^\mu h-\frac12m_h^2h^2\\
&-\lambda_Hv\,h^3-\frac{\lambda_H}4h^4+\frac{\lambda_Hv^4}4\\
&+\Bigl(1+\frac hv\Bigr)^2g_{\mathrm{YM}}^2\,\Phi_0^\dagger A^U_\mu A^{U\mu}\Phi_0\\
&-\frac14F_{\mu\nu}^aF^{a\mu\nu},\\
m_h^2={}&2\lambda_Hv^2=2\mu_H^2 .
\end{aligned}
}
\right.
\tag{3.64}
```

Since $`U^\dagger\partial_\mu U=i\partial_\mu X+O(\theta\,\partial\theta)`$, to first order $`A^U_\mu=A_\mu-\partial_\mu X/g_{\mathrm{YM}}`$. As $`T^a\Phi_0=0`$ for $`a\ge2n`$, by (3.59) the quadratic part of $`g_{\mathrm{YM}}^2\Phi_0^\dagger A^U_\mu A^{U\mu}\Phi_0`$ is

```math
\left.
\begin{aligned}
&\Phi_0^\dagger\bigl(g_{\mathrm{YM}}A_\mu-\partial_\mu X\bigr)\bigl(g_{\mathrm{YM}}A^\mu-\partial^\mu X\bigr)\Phi_0\\
&\qquad=\frac12\sum_{a=1}^{2n-1}m_a^2\Bigl(A_\mu^a-\frac{\partial_\mu\theta^a}{g_{\mathrm{YM}}}\Bigr)\Bigl(A^{a\mu}-\frac{\partial^\mu\theta^a}{g_{\mathrm{YM}}}\Bigr),\\
&m_a^2:=2g_{\mathrm{YM}}^2\,\Phi_0^\dagger(G^a)^2\Phi_0>0 .
\end{aligned}
\right.
\tag{3.65}
```

The $`A_\mu^a`$ with $`a\ge2n`$ do not appear in (3.65). Since $`U(\theta)\in U(n)`$, the gauge transformation (3.19)–(3.20) with $`U(\theta)^{-1}=U(\theta)^\dagger`$ gives

```math
\left.
\begin{aligned}
\Phi'&=U^\dagger\Phi=\Bigl(1+\frac hv\Bigr)\Phi_0,\\
A'_\mu&=U^\dagger A_\mu U-\frac i{g_{\mathrm{YM}}}\bigl(\partial_\mu U^\dagger\bigr)U=A^U_\mu,\\
F'_{\mu\nu}&=U^\dagger F_{\mu\nu}U .
\end{aligned}
\right.
\tag{3.66}
```

By gauge invariance, $`\mathcal L`$ equals (3.64) with $`\theta^a=0`$ and $`A_\mu`$ replaced by $`A'_\mu`$. With (3.59),

```math
\left.
\boxed{
\begin{aligned}
\mathcal L={}&\frac12\partial_\mu h\,\partial^\mu h-\frac12m_h^2h^2\\
&-\lambda_Hv\,h^3-\frac{\lambda_H}4h^4+\frac{\lambda_Hv^4}4\\
&-\frac14F'^a_{\mu\nu}F'^{a\mu\nu}\\
&+\frac12\Bigl(1+\frac hv\Bigr)^2\sum_{a=1}^{2n-1}m_a^2A'^a_\mu A'^{a\mu} .
\end{aligned}
}
\right.
\tag{3.67}
```

The $`\theta^a`$ no longer appear. To first order $`A'^a_\mu=A^a_\mu-\partial_\mu\theta^a/g_{\mathrm{YM}}`$ for $`a\le2n-1`$, so the quadratic part of the mass term in (3.67) is (3.65). Comparing with (1.85) and (1.135):

- the Higgs field $`h`$ has mass $`m_h`$ of (3.64);
- the $`2n-1`$ gauge fields $`A'^a_\mu`$, $`a\le2n-1`$, along the broken generators have masses $`m_a`$ of (3.65);
- the $`(n-1)^2`$ gauge fields $`A'^a_\mu`$, $`a\ge2n`$, along the unbroken generators are massless.

For $`n=2`$ and $`g_2=g_1=g_{\mathrm{YM}}`$, the $`m_a`$ are $`m_W`$, $`m_W`$ and $`m_Z`$ of (3.81).


<br><br>

<a id="electroweak-gauge-theory"></a>
<a id="electroweak-theory"></a>
### 3.5 Electroweak Theory

<a id="sm-leptons"></a>
#### Leptons in the Standard Model

The gauge group of the electroweak theory is $`SU(2)_L\times U(1)_Y`$. On an $`SU(2)_L`$ doublet $`T^a:=\sigma^a/2`$, $`a=1,2,3`$; on an $`SU(2)_L`$ singlet $`T^a:=0`$. A field $`\psi`$ of hypercharge $`Y`$ transforms as

```math
\left.
\begin{aligned}
\psi'(x)&=e^{i\theta^a(x)T^a+i\theta_Y(x)Y}\,\psi(x),\qquad \theta^a(x),\ \theta_Y(x)\in\mathbb R,\\
Q&:=T^3+Y,
\end{aligned}
\right.
\tag{3.68}
```

where $`Q`$ is the electric charge in units of $`e`$, as in (3.23).

The leptons come in three generations, labeled by the flavor index $`\alpha=e,\mu,\tau`$. With pairs denoting ($`SU(2)_L`$ representation, $`Y`$),

```math
\left.
\boxed{
\begin{aligned}
\ell_{\alpha L}&:=\begin{pmatrix}\nu_{\alpha L}\\ l_{\alpha L}\end{pmatrix}\sim\Bigl(\mathbf2,-\frac12\Bigr),\qquad
E_{\alpha R}\sim(\mathbf1,-1),\\
Q\,\nu_{\alpha L}&=0,\qquad Q\,l_{\alpha L}=-l_{\alpha L},\qquad Q\,E_{\alpha R}=-E_{\alpha R}.
\end{aligned}
}
\right.
\tag{3.69}
```

The fields are four-component spinors with $`P_L\nu_{\alpha L}=\nu_{\alpha L}`$, $`P_Ll_{\alpha L}=l_{\alpha L}`$ and $`P_RE_{\alpha R}=E_{\alpha R}`$, where $`P_{L,R}`$ are given in (1.131). The leptons are color singlets. The minimal renormalizable Standard Model contains no right-handed neutrino.

<br><br>

<a id="electroweak-kinetic-terms"></a>
#### Kinetic Terms

Let $`W_\mu^a`$, $`a=1,2,3`$, and $`B_\mu`$ be the real $`SU(2)_L`$ and $`U(1)_Y`$ gauge fields, and $`g_2,g_1>0`$ the couplings. With $`U(\theta):=e^{i\theta^a(x)\sigma^a/2}`$ and $`W_\mu:=W_\mu^a\sigma^a/2`$, (3.19) with $`g_{\mathrm{YM}}\to g_2`$ and (3.24) with $`eQ\to g_1Y`$ give

```math
\left.
\boxed{
\begin{aligned}
D_\mu&:=\partial_\mu-ig_2W_\mu^aT^a-ig_1YB_\mu,\\
W_\mu'&=U(\theta)W_\mu U(\theta)^\dagger-\frac i{g_2}\bigl(\partial_\mu U(\theta)\bigr)U(\theta)^\dagger,\qquad
B_\mu'=B_\mu+\frac1{g_1}\partial_\mu\theta_Y,
\end{aligned}
}
\right.
\tag{3.70}
```

so that $`D_\mu'\psi'=e^{i\theta^aT^a+i\theta_YY}D_\mu\psi`$ under (3.68). The field strengths are

```math
\left.
\begin{aligned}
W_{\mu\nu}^a&:=\partial_\mu W_\nu^a-\partial_\nu W_\mu^a+g_2\epsilon^{abc}W_\mu^bW_\nu^c,\qquad
B_{\mu\nu}:=\partial_\mu B_\nu-\partial_\nu B_\mu,\\
[D_\mu,D_\nu]&=-ig_2W_{\mu\nu}^aT^a-ig_1YB_{\mu\nu}.
\end{aligned}
\right.
\tag{3.71}
```

On the lepton fields (3.69), the covariant derivative (3.70) is

```math
\left.
D_\mu\ell_{\alpha L}=\Bigl(\partial_\mu-ig_2W_\mu^a\frac{\sigma^a}2+\frac i2g_1B_\mu\Bigr)\ell_{\alpha L},\qquad
D_\mu E_{\alpha R}=\bigl(\partial_\mu+ig_1B_\mu\bigr)E_{\alpha R}.
\right.
\tag{3.72}
```

The kinetic terms of the Lagrangian density are

```math
\left.
\boxed{
\begin{aligned}
\mathcal L_{\mathrm{kin}}
={}&-\frac14W_{\mu\nu}^aW^{a\mu\nu}-\frac14B_{\mu\nu}B^{\mu\nu}\\
&+\sum_{\alpha=e,\mu,\tau}\Bigl(\overline{\ell_{\alpha L}}\,i\gamma^\mu D_\mu\ell_{\alpha L}
+\overline{E_{\alpha R}}\,i\gamma^\mu D_\mu E_{\alpha R}\Bigr).
\end{aligned}
}
\right.
\tag{3.73}
```

By (3.20), (3.24) and (3.70), $`\mathcal L_{\mathrm{kin}}`$ is gauge invariant.

<br><br>

<a id="charged-lepton-masses"></a>
#### Yukawa Couplings and Charged-Lepton Masses

The Higgs doublet $`H=:(H^+,H^0)^T\sim(\mathbf2,\frac12)`$ is a color singlet. It is the $`\Phi`$ of (3.52) with $`n=2`$ and $`\mu_H^2>0`$, with $`\partial_\mu`$ replaced by (3.70). As $`\theta^a`$ and $`\theta_Y`$ vary, $`e^{i\theta^a\sigma^a/2+i\theta_Y/2}`$ covers $`U(2)`$, so by (3.56), (3.60) and (3.66)

```math
\left.
\begin{aligned}
\mathcal L_H&=(D_\mu H)^\dagger D^\mu H-V(H),\qquad
V(H)=-\mu_H^2H^\dagger H+\lambda_H(H^\dagger H)^2,\\
\langle H\rangle&=\frac1{\sqrt2}\begin{pmatrix}0\\v\end{pmatrix},\qquad Q\langle H\rangle=0,\qquad
H\big|_{\mathrm{unitary\ gauge}}=\frac1{\sqrt2}\begin{pmatrix}0\\v+h\end{pmatrix}.
\end{aligned}
\right.
\tag{3.74}
```

The Higgs field $`h`$ has the mass $`m_h`$ of (3.64).

Let $`y_l`$ be a complex $`3\times3`$ matrix; repeated flavor indices $`\alpha,\beta`$ are summed. The lepton Yukawa coupling is invariant under (3.68):

```math
\left.
\begin{aligned}
\mathcal L_Y^\ell&=-\overline{\ell_{\alpha L}}\,(y_l)_{\alpha\beta}\,H\,E_{\beta R}+\mathrm{h.c.},\qquad
\overline{\ell_{\alpha L}}H=\overline{\nu_{\alpha L}}H^++\overline{l_{\alpha L}}H^0,\\
\overline{\ell_{\alpha L}'}H'E_{\beta R}'
&=\overline{\ell_{\alpha L}}\,e^{\frac i2\theta_Y}U(\theta)^\dagger\;e^{\frac i2\theta_Y}U(\theta)H\;e^{-i\theta_Y}E_{\beta R}
=\overline{\ell_{\alpha L}}HE_{\beta R}.
\end{aligned}
\right.
\tag{3.75}
```

In the unitary gauge (3.74), $`H^+=0`$ and

```math
\left.
\mathcal L_Y^\ell=-\Bigl(1+\frac hv\Bigr)\overline{l_{\alpha L}}\,(M_l)_{\alpha\beta}\,E_{\beta R}+\mathrm{h.c.},\qquad
M_l:=\frac v{\sqrt2}\,y_l .
\right.
\tag{3.76}
```

The neutrinos $`\nu_{\alpha L}`$ do not appear in (3.76).

**Flavor Basis**

Write $`\ell_L:=(\ell_{eL},\ell_{\mu L},\ell_{\tau L})^T`$ and $`E_R:=(E_{eR},E_{\mu R},E_{\tau R})^T`$ in flavor space. For constant $`R_\ell,R_E\in U(3)`$, (3.73) is invariant under the change of basis in the first line below, and the singular value decomposition of $`M_l`$ fixes $`R_\ell`$ and $`R_E`$ by the second line:

```math
\left.
\begin{aligned}
\ell_L&\to R_\ell\,\ell_L,\qquad E_R\to R_E\,E_R,\qquad y_l\to R_\ell^\dagger\,y_l\,R_E,\\
R_\ell^\dagger M_lR_E&=\mathop{\rm diag}\nolimits (m_e,m_\mu,m_\tau),\qquad m_\alpha\ge0 .
\end{aligned}
\right.
\tag{3.77}
```

From now on we use this basis. With the Dirac fields $`l_\alpha:=l_{\alpha L}+E_{\alpha R}`$, (3.76) becomes

```math
\left.
\boxed{
\begin{aligned}
M_l&=\mathop{\rm diag}\nolimits (m_e,m_\mu,m_\tau),\\
\mathcal L_Y^\ell&=-\sum_{\alpha=e,\mu,\tau}m_\alpha\Bigl(1+\frac hv\Bigr)\bar l_\alpha l_\alpha .
\end{aligned}
}
\right.
\tag{3.78}
```

Since $`\overline{l_{\alpha L}}\,i\gamma^\mu\partial_\mu l_{\alpha L}+\overline{E_{\alpha R}}\,i\gamma^\mu\partial_\mu E_{\alpha R}=\bar l_\alpha\,i\gamma^\mu\partial_\mu l_\alpha`$, the free part of (3.73) and (3.78) contain the Dirac Lagrangian (1.94) of each $`l_\alpha`$ with mass $`m_\alpha`$. Thus the charged leptons $`l_e,l_\mu,l_\tau`$ are Dirac fields of masses $`m_e,m_\mu,m_\tau`$, coupled to $`h`$ with strength $`m_\alpha/v`$, while the neutrinos $`\nu_{\alpha L}`$ remain massless.

<br><br>

<a id="gauge-boson-masses"></a>
#### Gauge-Boson Masses

Substituting the unitary-gauge $`H`$ of (3.74) into (3.70), with $`T^a=\sigma^a/2`$ and $`Y=\frac12`$,

```math
\left.
\begin{aligned}
D_\mu H&=\frac1{\sqrt2}\begin{pmatrix}-\frac i2g_2\bigl(W_\mu^1-iW_\mu^2\bigr)(v+h)\\ \partial_\mu h+\frac i2\bigl(g_2W_\mu^3-g_1B_\mu\bigr)(v+h)\end{pmatrix},\\
(D_\mu H)^\dagger D^\mu H&=\frac12\partial_\mu h\,\partial^\mu h
+\frac{(v+h)^2}8\Bigl[g_2^2\bigl(W_\mu^1W^{1\mu}+W_\mu^2W^{2\mu}\bigr)\\
&\qquad+\bigl(g_2W_\mu^3-g_1B_\mu\bigr)\bigl(g_2W^{3\mu}-g_1B^\mu\bigr)\Bigr].
\end{aligned}
\right.
\tag{3.79}
```

Define

```math
\left.
\begin{aligned}
W_\mu^\pm&:=\frac{W_\mu^1\mp iW_\mu^2}{\sqrt2},\qquad
\tan\theta_W:=\frac{g_1}{g_2},\qquad
s_W:=\sin\theta_W,\qquad c_W:=\cos\theta_W,\\
Z_\mu&:=c_WW_\mu^3-s_WB_\mu,\qquad
A_\mu^{\mathrm{em}}:=s_WW_\mu^3+c_WB_\mu,\qquad
e:=g_2s_W=g_1c_W .
\end{aligned}
\right.
\tag{3.80}
```

Then $`W_\mu^1W^{1\mu}+W_\mu^2W^{2\mu}=2W_\mu^+W^{-\mu}`$ and $`g_2W_\mu^3-g_1B_\mu=\sqrt{g_2^2+g_1^2}\,Z_\mu`$, so

```math
\left.
\boxed{
\begin{aligned}
(D_\mu H)^\dagger D^\mu H&=\frac12\partial_\mu h\,\partial^\mu h
+\Bigl(1+\frac hv\Bigr)^2\Bigl(m_W^2W_\mu^+W^{-\mu}+\frac12m_Z^2Z_\mu Z^\mu\Bigr),\\
m_W&=\frac{g_2v}2,\qquad
m_Z=\frac v2\sqrt{g_2^2+g_1^2}=\frac{m_W}{c_W},\qquad
m_\gamma=0,\\
\frac{G_F}{\sqrt2}&=\frac{g_2^2}{8m_W^2}=\frac1{2v^2}.
\end{aligned}
}
\right.
\tag{3.81}
```

$`A_\mu^{\mathrm{em}}`$ does not appear in (3.81).

<br><br>

<a id="sm-quarks"></a>
#### Quarks

The quarks come in three generations, $`r=1,2,3`$, and are color triplets as in (3.32). With the pairs as in (3.69),

```math
\left.
\begin{aligned}
q_{rL}&:=\begin{pmatrix}u_{rL}\\ d_{rL}\end{pmatrix}\sim\Bigl(\mathbf2,\frac16\Bigr),\qquad
u_{rR}\sim\Bigl(\mathbf1,\frac23\Bigr),\qquad
d_{rR}\sim\Bigl(\mathbf1,-\frac13\Bigr),\\
Q\,u_{rL}&=\frac23u_{rL},\qquad Q\,d_{rL}=-\frac13d_{rL}.
\end{aligned}
\right.
\tag{3.82}
```

With $`D_\mu`$ of (3.70) plus the gluon term $`-ig_sA_\mu`$ of (3.36), the quark kinetic terms are

```math
\left.
\mathcal L_{\mathrm{kin}}^q=\sum_{r=1}^3\Bigl(\overline{q_{rL}}\,i\gamma^\mu D_\mu q_{rL}
+\overline{u_{rR}}\,i\gamma^\mu D_\mu u_{rR}
+\overline{d_{rR}}\,i\gamma^\mu D_\mu d_{rR}\Bigr).
\right.
\tag{3.83}
```

Let $`y_u,y_d`$ be complex $`3\times3`$ matrices, $`H^c:=i\sigma^2H^*\sim(\mathbf2,-\frac12)`$, and $`u_L:=(u_{1L},u_{2L},u_{3L})^T`$, and similarly $`u_R`$, $`d_L`$, $`d_R`$, in flavor space. Summing over $`r,s`$, the quark Yukawa couplings are gauge invariant, and in the unitary gauge (3.74)

```math
\left.
\begin{aligned}
\mathcal L_Y^q&=-\overline{q_{rL}}\,(y_d)_{rs}\,H\,d_{sR}-\overline{q_{rL}}\,(y_u)_{rs}\,H^c\,u_{sR}+\mathrm{h.c.},\qquad
H^c\big|_{\mathrm{unitary\ gauge}}=\frac1{\sqrt2}\begin{pmatrix}v+h\\0\end{pmatrix},\\
\mathcal L_Y^q&=-\Bigl(1+\frac hv\Bigr)\bigl(\overline{u_L}\,M_u\,u_R+\overline{d_L}\,M_d\,d_R\bigr)+\mathrm{h.c.},\qquad
M_{u,d}:=\frac v{\sqrt2}\,y_{u,d}.
\end{aligned}
\right.
\tag{3.84}
```

**Mass Basis and CKM Matrix**

With unitary $`R_{uL},R_{uR},R_{dL},R_{dR}`$ chosen by the singular value decompositions of $`M_u`$ and $`M_d`$, define the mass-basis fields $`u'`$, $`d'`$ by

```math
\left.
\boxed{
\begin{aligned}
u_{L,R}&=R_{uL,R}\,u_{L,R}',\qquad d_{L,R}=R_{dL,R}\,d_{L,R}',\\
R_{uL}^\dagger M_uR_{uR}&=\mathop{\rm diag}\nolimits (m_u,m_c,m_t),\qquad
R_{dL}^\dagger M_dR_{dR}=\mathop{\rm diag}\nolimits (m_d,m_s,m_b),\\
u_L'+u_R'&=(q_u,q_c,q_t)^T,\qquad d_L'+d_R'=(q_d,q_s,q_b)^T,\qquad
V_{\mathrm{CKM}}:=R_{uL}^\dagger R_{dL},\\
\mathcal L_Y^q&=-\sum_fm_f\Bigl(1+\frac hv\Bigr)\bar q_fq_f ,
\end{aligned}
}
\right.
\tag{3.85}
```

with $`m_f\ge0`$; the $`q_f`$ are the quark fields of (3.32), and the $`m_f`$ are the masses in (3.45).

<br><br>

<a id="electroweak-currents"></a>
#### Charged and Neutral Currents

The gauge-field terms of $`\bar\psi\,i\gamma^\mu D_\mu\psi`$ are $`\bar\psi\gamma^\mu(g_2W_\mu^aT^a+g_1YB_\mu)\psi`$. By (3.80), with $`T^\pm:=T^1\pm iT^2`$,

```math
\left.
g_2W_\mu^aT^a+g_1YB_\mu
=\frac{g_2}{\sqrt2}\bigl(W_\mu^+T^++W_\mu^-T^-\bigr)
+eQA_\mu^{\mathrm{em}}
+\frac{g_2}{c_W}\bigl(T^3-s_W^2Q\bigr)Z_\mu .
\right.
\tag{3.86}
```

Since $`\overline{\ell_{\alpha L}}\gamma^\mu T^+\ell_{\alpha L}=\overline{\nu_{\alpha L}}\gamma^\mu l_{\alpha L}`$ and, by (3.85), $`\overline{q_{rL}}\gamma^\mu T^+q_{rL}=\overline{u_L}\gamma^\mu d_L=\overline{u_L'}\gamma^\mu V_{\mathrm{CKM}}\,d_L'`$, the $`W_\mu^\pm`$ terms of (3.73) and (3.83) are, with $`q_{fL}:=P_Lq_f`$ and the rows and columns of $`V:=V_{\mathrm{CKM}}`$ labeled by $`f=u,c,t`$ and $`f'=d,s,b`$,

```math
\left.
\boxed{
\mathcal L_{\mathrm{CC}}
=\frac{g_2}{\sqrt2}\,W_\mu^+\Bigl(\sum_{\alpha=e,\mu,\tau}\overline{\nu_{\alpha L}}\gamma^\mu l_{\alpha L}
+\sum_{f=u,c,t}\ \sum_{f'=d,s,b}V_{ff'}\,\overline{q_{fL}}\gamma^\mu q_{f'L}\Bigr)+\mathrm{h.c.}
}
\right.
\tag{3.87}
```

Let $`\psi_f`$ be the field of the fermion $`f`$ of (3.23) in the bases (3.77) and (3.85): $`\psi_f=q_f`$ for the quarks, $`\psi_f=l_f`$ for $`f=e,\mu,\tau`$, and $`\psi_{\nu_\alpha}=\nu_{\alpha L}`$. Let $`T_f^3`$ be $`T^3`$ of its left-handed part: $`+\frac12`$ for $`q_u,q_c,q_t`$ and $`\nu_{\alpha L}`$, and $`-\frac12`$ for $`q_d,q_s,q_b`$ and $`l_\alpha`$. The $`A_\mu^{\mathrm{em}}`$ and $`Z_\mu`$ terms are

```math
\left.
\boxed{
\begin{aligned}
\mathcal L_{\mathrm{NC}}
={}&eA_\mu^{\mathrm{em}}\sum_fQ_f\,\bar\psi_f\gamma^\mu\psi_f\\
&+\frac{g_2}{c_W}Z_\mu\sum_f\bar\psi_f\gamma^\mu\bigl(T_f^3P_L-Q_fs_W^2\bigr)\psi_f .
\end{aligned}
}
\right.
\tag{3.88}
```

The first line is the interaction term of (3.26) with $`A_\mu=A_\mu^{\mathrm{em}}`$. The neutral currents are flavor diagonal at tree level.


<br><br>

<a id="qft-ch4"></a>
## 4. Path Integrals

<a id="path-integrals-in-quantum-mechanics"></a>
### 4.1 Path Integrals in Quantum Mechanics

**Principle**

Consider a system with $`n`$ degrees of freedom.

- **Configuration space**: $`\mathrm{Conf}=\mathbb R^n`$.
- **Dynamical structure**: the Lagrangian

```math
\left.
\begin{aligned}
L:\mathbb R^n\times\mathbb R^n&\to\mathbb R,\\
(x,y)&\mapsto\sum_{a=1}^n\frac12m_ay_a^2-V(x),
\end{aligned}
\right.
\tag{4.1}
```

in which $`m_a>0`$ and $`V:\mathbb R^n\to\mathbb R`$ is smooth.

- **Paths**: for $`t_i<t_f`$,

```math
\left.
\begin{aligned}
C:[t_i,t_f]&\to\mathrm{Conf},\\
t&\mapsto C(t).
\end{aligned}
\right.
\tag{4.2}
```

- **Action**: the functional on paths

```math
\left.
\begin{aligned}
S:\{\text{paths}\}&\to\mathbb R,\\
C&\mapsto S[C]:=\int_{t_i}^{t_f}dt\,L\bigl(C(t),\dot C(t)\bigr).
\end{aligned}
\right.
\tag{4.3}
```

**Quantization**

- **Initial configuration**:

```math
\left.
\begin{aligned}
Q_i:\{t_i\}&\to\mathrm{Conf},\\
t_i&\mapsto q_i.
\end{aligned}
\right.
\tag{4.4}
```

- **Final configuration**:

```math
\left.
\begin{aligned}
Q_f:\{t_f\}&\to\mathrm{Conf},\\
t_f&\mapsto q_f.
\end{aligned}
\right.
\tag{4.5}
```

- **Transition kernel**: the integral over the paths with these endpoints,

```math
\left.
\boxed{K(Q_f,Q_i):=\int_{C(t_i)=Q_i(t_i)}^{C(t_f)=Q_f(t_f)}\mathcal DC\,e^{iS[C]},}
\right.
\tag{4.6}
```

also written $`\int_{Q_i}^{Q_f}\mathcal DC\,e^{iS[C]}`$.

**Exact Definition of the Transition Kernel**

Divide $`[t_i,t_f]`$ into $`N+1`$ steps.

- **Measure**:

```math
\left.
\begin{gathered}
\Delta t:=\frac{t_f-t_i}{N+1},\qquad t_k:=t_i+k\,\Delta t\quad(k=0,\ldots,N+1),\\
\mathcal DC:=\lim_{N\to\infty}\mathcal N_N\prod_{k=1}^Nd^nC(t_k),\qquad
\mathcal N_N:=\prod_{a=1}^n\Bigl(\frac{m_a}{2\pi i\,\Delta t}\Bigr)^{\frac{N+1}{2}},
\end{gathered}
\right.
\tag{4.7}
```

so that $`t_0=t_i`$ and $`t_{N+1}=t_f`$, with $`d^nC(t_k):=\prod_{a=1}^ndC_a(t_k)`$.

- **Action**:

```math
\left.
S[C]=\lim_{N\to\infty}\Delta t\sum_{k=0}^NL\Bigl(C(t_k),\frac{C(t_{k+1})-C(t_k)}{\Delta t}\Bigr).
\right.
\tag{4.8}
```

Thus (4.6) means

```math
\left.
\boxed{
K(Q_f,Q_i)=\lim_{N\to\infty}\mathcal N_N\int\prod_{k=1}^Nd^nC(t_k)\,
\exp\biggl[i\,\Delta t\sum_{k=0}^NL\Bigl(C(t_k),\frac{C(t_{k+1})-C(t_k)}{\Delta t}\Bigr)\biggr],}
\right.
\tag{4.9}
```

with $`C(t_0):=q_i`$, $`C(t_{N+1}):=q_f`$, and each $`C(t_k)`$, $`1\le k\le N`$, integrated over $`\mathrm{Conf}`$.

**Functional Derivative**

For a source $`J:[t_i,t_f]\to\mathbb R^n`$, with $`J\cdot C:=\sum_{a=1}^nJ_aC_a`$,

```math
\left.
K^J(Q_f,Q_i):=\int_{Q_i}^{Q_f}\mathcal DC\,\exp\Bigl(i\int_{t_i}^{t_f}dt\,\bigl[L\bigl(C(t),\dot C(t)\bigr)+J(t)\cdot C(t)\bigr]\Bigr).
\right.
\tag{4.10}
```

In the sliced form (4.9) the source adds $`i\,\Delta t\sum_{k=0}^NJ(t_k)\cdot C(t_k)`$ to the exponent, so $`J`$ enters only through $`J(t_0),\ldots,J(t_N)`$. For $`t_i<t<t_f`$ define

```math
\left.
\frac{\delta}{\delta J_a(t)}:=\lim_{N\to\infty}\frac{1}{\Delta t}\frac{\partial}{\partial J_a(t_k)},\qquad t_k\to t.
\right.
\tag{4.11}
```

Writing $`L_j:=L\bigl(C(t_j),[C(t_{j+1})-C(t_j)]/\Delta t\bigr)`$,

```math
\left.
\begin{aligned}
\frac{\delta}{\delta J_a(t)}K^J(Q_f,Q_i)
&=\lim_{N\to\infty}\mathcal N_N\int\prod_{j=1}^Nd^nC(t_j)\,
\frac{1}{\Delta t}\frac{\partial}{\partial J_a(t_k)}\exp\biggl[i\,\Delta t\sum_{j=0}^N\bigl(L_j+J(t_j)\cdot C(t_j)\bigr)\biggr]\\
&=\lim_{N\to\infty}\mathcal N_N\int\prod_{j=1}^Nd^nC(t_j)\,
iC_a(t_k)\exp\biggl[i\,\Delta t\sum_{j=0}^N\bigl(L_j+J(t_j)\cdot C(t_j)\bigr)\biggr]\\
&=\int_{Q_i}^{Q_f}\mathcal DC\,iC_a(t)\exp\Bigl(i\int_{t_i}^{t_f}dt'\,\bigl[L\bigl(C(t'),\dot C(t')\bigr)+J(t')\cdot C(t')\bigr]\Bigr).
\end{aligned}
\right.
\tag{4.12}
```


**Example: Free Particle in One Dimension**

Take $`n=1`$, $`V=0`$ in (4.1):

```math
\left.
L(x,y)=\frac12my^2,\qquad Q_i(t_i)=q_i,\qquad Q_f(t_f)=q_f.
\right.
\tag{4.13}
```

By (4.7)–(4.9), with $`C(t_0)=q_i`$, $`C(t_{N+1})=q_f`$ and $`\mathcal N_N=\bigl(\frac{m}{2\pi i\,\Delta t}\bigr)^{\frac{N+1}{2}}`$,

```math
\left.
\begin{aligned}
K(Q_f,Q_i)&=\int_{Q_i}^{Q_f}\mathcal DC\,e^{i\int_{t_i}^{t_f}dt\,\frac12m\dot C^2}\\
&=\lim_{N\to\infty}\mathcal N_N\int\prod_{k=1}^{N}dC(t_k)\,e^{\frac{i}{\Delta t}\sum_{k=0}^{N}\frac12m\left(C(t_{k+1})-C(t_k)\right)^2}\\
&=\lim_{N\to\infty}\mathcal N_N\int\prod_{k=1}^{N}dC(t_k)\,
e^{\frac{i}{\Delta t}\left[\frac12mq_i^2+\frac12mq_f^2+mC^2(t_1)+\cdots+mC^2(t_N)\right]}\,
e^{\frac{i}{\Delta t}(-m)\left[q_iC(t_1)+C(t_1)C(t_2)+\cdots+C(t_N)q_f\right]}.
\end{aligned}
\right.
\tag{4.14}
```

Integrate $`C(t_1)`$, using $`\int_{-\infty}^{\infty}dx\,e^{iax^2}=\sqrt{\pi i/a}`$ for $`a>0`$ ($`a\to a+i\varepsilon`$, $`\varepsilon\to0^+`$):

```math
\left.
\begin{aligned}
\int dC(t_1)\,e^{\frac{i}{\Delta t}\left[mC^2(t_1)-mC(t_1)\left(q_i+C(t_2)\right)\right]}
&=\int dC(t_1)\,e^{\frac{im}{\Delta t}\left(C(t_1)-\frac{q_i+C(t_2)}{2}\right)^2}\,e^{-\frac{im}{4\Delta t}\left(q_i+C(t_2)\right)^2}\\
&=\sqrt{\frac{2\pi i\,\Delta t}{m}\cdot\frac12}\;e^{-\frac{im}{4\Delta t}\left(q_i+C(t_2)\right)^2}.
\end{aligned}
\right.
\tag{4.15}
```

After $`C(t_1),\ldots,C(t_{j-1})`$, $`1\le j\le N`$:

```math
\left.
K(Q_f,Q_i)=\lim_{N\to\infty}\mathcal N_N\Bigl(\frac{2\pi i\,\Delta t}{m}\Bigr)^{\frac{j-1}{2}}\frac{1}{\sqrt j}
\int\prod_{k=j}^{N}dC(t_k)\,
e^{\frac{im}{2\Delta t}\left[\frac{\left(C(t_j)-q_i\right)^2}{j}+C^2(t_j)+2C^2(t_{j+1})+\cdots+2C^2(t_N)+q_f^2\right]}\,
e^{\frac{im}{2\Delta t}(-2)\left[C(t_j)C(t_{j+1})+\cdots+C(t_N)q_f\right]}.
\right.
\tag{4.16}
```

Integrate $`C(t_j)`$:

```math
\left.
\begin{aligned}
\frac{\left(C(t_j)-q_i\right)^2}{j}+C^2(t_j)-2C(t_j)C(t_{j+1})
&=\frac{j+1}{j}\Bigl(C(t_j)-\frac{q_i+jC(t_{j+1})}{j+1}\Bigr)^2+\frac{\left(C(t_{j+1})-q_i\right)^2}{j+1}-C^2(t_{j+1}),\\
\int dC(t_j)\,e^{\frac{im}{2\Delta t}\frac{j+1}{j}\left(C(t_j)-\frac{q_i+jC(t_{j+1})}{j+1}\right)^2}
&=\sqrt{\frac{2\pi i\,\Delta t}{m}\cdot\frac{j}{j+1}},
\end{aligned}
\right.
\tag{4.17}
```

which gives (4.16) with $`j+1`$; for $`j=N`$, $`C(t_{N+1})=q_f`$ and the bracket becomes $`\frac{(q_f-q_i)^2}{N+1}`$. Hence, with $`(N+1)\Delta t=t_f-t_i`$,

```math
\left.
\begin{aligned}
K(Q_f,Q_i)&=\lim_{N\to\infty}\Bigl(\frac{m}{2\pi i\,\Delta t}\Bigr)^{\frac{N+1}{2}}\Bigl(\frac{2\pi i\,\Delta t}{m}\Bigr)^{\frac N2}\frac{1}{\sqrt{N+1}}\,
e^{\frac{im\left(q_f-q_i\right)^2}{2(N+1)\Delta t}}\\
&=\boxed{\sqrt{\frac{m}{2\pi i\,(t_f-t_i)}}\;e^{\frac{im\left(q_f-q_i\right)^2}{2(t_f-t_i)}}.}
\end{aligned}
\right.
\tag{4.18}
```

This example shows why the prefactor $`\mathcal N_N`$ is included in the definition (4.7) of the path integral. The result (4.18) is finite, while by its definition $`\mathcal N_N`$ diverges as $`N\to\infty`$; without the prefactor, the remaining factor $`\bigl(\frac{2\pi i\,\Delta t}{m}\bigr)^{\frac N2}\frac{1}{\sqrt{N+1}}`$ in (4.18) tends to zero, and so would $`K(Q_f,Q_i)`$.

**Relation to Operator Quantization**

Let $`\hat H:=\sum_{a=1}^n\hat p_a^2/(2m_a)+V(\hat q)`$ with $`[\hat q_a,\hat p_b]=i\delta_{ab}`$ and $`\hat q_a|q\rangle=q_a|q\rangle`$, and let $`\hat U(t_f,t_i)=e^{-i\hat H(t_f-t_i)}`$ be its evolution operator (2.21). Then, with $`q_i=Q_i(t_i)`$ and $`q_f=Q_f(t_f)`$,

```math
\left.
\boxed{K(Q_f,Q_i)=\langle q_f|\hat U(t_f,t_i)|q_i\rangle=\langle q_f,t_f|q_i,t_i\rangle}
\right.
\tag{4.19}
```

in the Schrödinger and Heisenberg pictures respectively, where $`|q,t\rangle:=\hat U(t,0)^\dagger|q\rangle`$ satisfies $`\hat q_H(t)|q,t\rangle=q\,|q,t\rangle`$ by (2.22).

<br><br>

<a id="path-integrals-in-field-theory"></a>
### 4.2 Path Integrals in Quantum Field Theory

Following the second viewpoint in [Section 1.4](#classical-dynamics), $`t`$ is replaced by $`x^\mu`$.

**Principle**

- **Configuration space**: $`\mathrm{Conf}=\mathbb R^n`$.
- **Dynamical structure**: the Lagrangian density

```math
\left.
\begin{aligned}
\mathcal L:\mathbb R^n\times(\mathbb R^n)^4&\to\mathbb R,\\
(x,y^\mu)&\mapsto\sum_{a=1}^n\frac12y_a^\mu y_{a\mu}-V(x),
\end{aligned}
\right.
\tag{4.20}
```

in which $`y^\mu\in\mathbb R^n`$, $`\mu=0,\ldots,3`$, and $`V:\mathbb R^n\to\mathbb R`$ is smooth.

- **Paths**: for $`t_i<t_f`$,

```math
\left.
\begin{aligned}
\phi:[t_i,t_f]\times\mathbb R^3&\to\mathrm{Conf},\\
x&\mapsto\phi(x),
\end{aligned}
\right.
\tag{4.21}
```

with $`\phi(t):=\phi(t,\cdot\,)`$ the configuration at time $`t`$.

- **Action**: the functional on paths

```math
\left.
\begin{aligned}
S:\{\text{paths}\}&\to\mathbb R,\\
\phi&\mapsto S[\phi]:=\int_{\mathbb R^3}d^3x\int_{t_i}^{t_f}dt\,\mathcal L\bigl(\phi(x),\partial_\mu\phi(x)\bigr).
\end{aligned}
\right.
\tag{4.22}
```

In the path integral the field takes the place of the path: a path (4.21) is a classical field (1.38) restricted to $`[t_i,t_f]\times\mathbb R^3`$. Paths are therefore denoted by $`\phi`$, and the integrals below are over field configurations.

Below, $`\int d^4x:=\int_{t_i}^{t_f}dt\int_{\mathbb R^3}d^3x`$.

**Quantization**

- **Initial configuration**:

```math
\left.
\begin{aligned}
\Phi_i:\{t_i\}\times\mathbb R^3&\to\mathrm{Conf},\\
(t_i,\mathbf x)&\mapsto\Phi_i(t_i,\mathbf x).
\end{aligned}
\right.
\tag{4.23}
```

- **Final configuration**:

```math
\left.
\begin{aligned}
\Phi_f:\{t_f\}\times\mathbb R^3&\to\mathrm{Conf},\\
(t_f,\mathbf x)&\mapsto\Phi_f(t_f,\mathbf x).
\end{aligned}
\right.
\tag{4.24}
```

- **Transition kernel**:

```math
\left.
\boxed{K(\Phi_f,\Phi_i):=\int_{\phi(t_i,\mathbf x)=\Phi_i(t_i,\mathbf x)}^{\phi(t_f,\mathbf x)=\Phi_f(t_f,\mathbf x)}\mathcal D\phi\,e^{iS[\phi]},}
\right.
\tag{4.25}
```

also written $`\int_{\Phi_i}^{\Phi_f}\mathcal D\phi\,e^{iS[\phi]}`$; the boundary conditions hold for every $`\mathbf x\in\mathbb R^3`$.

**Correlation Functions**

As in (4.19),

```math
\left.
K(\Phi_f,\Phi_i)=\langle\Phi_f|\hat U(t_f,t_i)|\Phi_i\rangle,
\right.
\tag{4.26}
```
 In operator quantization the vacuum expands in this basis, which defines the vacuum functional $`\Psi[\Phi]`$:

```math
\left.
|\mathrm{vac}\rangle=\int\mathcal D\Phi\,|\Phi\rangle\langle\Phi|\mathrm{vac}\rangle=\int\mathcal D\Phi\,|\Phi\rangle\,\Psi[\Phi],\qquad
\Psi[\Phi]:=\langle\Phi|\mathrm{vac}\rangle.
\right.
\tag{4.27}
```

Hence

```math
\left.
\begin{aligned}
K(\mathrm{vac}_f,\mathrm{vac}_i)&:=\langle\mathrm{vac}_f|\hat U(t_f,t_i)|\mathrm{vac}_i\rangle\\
&=\int\mathcal D\Phi_f\,\mathcal D\Phi_i\,\Psi^*[\Phi_f]\,\Psi[\Phi_i]\,K(\Phi_f,\Phi_i).
\end{aligned}
\right.
\tag{4.28}
```




- **Correlation function**: 

```math
\left.
\boxed{
\begin{aligned}
G_{a_1\cdots a_r}(x_1,\ldots,x_r)&:=\langle \phi_{a_1}(x_1)\cdots\phi_{a_r}(x_r)\rangle_{\mathrm{vac}}\\
&=\frac{\int_{\mathrm{vac}}^{\mathrm{vac}}\mathcal D\phi\,\phi_{a_1}(x_1)\cdots\phi_{a_r}(x_r)\,e^{iS[\phi]}}{\int_{\mathrm{vac}}^{\mathrm{vac}}\mathcal D\phi\,e^{iS[\phi]}},
\end{aligned}}
\right.
\tag{4.34}
```

with $`t_i<x_k^0<t_f`$. 

上述定义中的分母源自于对真空归一化的要求，在上述定义下，<1>=真空的模=1

- **Generating functional**: for a source $`J:[t_i,t_f]\times\mathbb R^3\to\mathbb R^n`$, with $`J\cdot\phi`$ as in (4.10),

```math
\left.
K^J(\Phi_f,\Phi_i):=\int_{\Phi_i}^{\Phi_f}\mathcal D\phi\,\exp\Bigl(iS[\phi]+i\int d^4x\,J(x)\cdot\phi(x)\Bigr),
\right.
\tag{4.29}
```

and, with the vacuum endpoints as in (4.28),

```math
\left.
\boxed{
Z[J]:=K^J(\mathrm{vac}_f,\mathrm{vac}_i)
=\int\mathcal D\Phi_f\,\mathcal D\Phi_i\,\Psi^*[\Phi_f]\,\Psi[\Phi_i]\,K^J(\Phi_f,\Phi_i),}
\right.
\tag{4.30}
```

so that $`Z[0]=K(\mathrm{vac}_f,\mathrm{vac}_i)`$.

As in (4.12), each $`\delta/\delta J_a(x)`$ acting on (4.29) brings down $`i\phi_a(x)`$, so by (4.30) and (4.33)

```math
\left.
\boxed{G_{a_1\cdots a_r}(x_1,\ldots,x_r)=\frac{1}{Z[0]}\left.\Bigl(-i\frac{\delta}{\delta J_{a_1}(x_1)}\Bigr)\cdots\Bigl(-i\frac{\delta}{\delta J_{a_r}(x_r)}\Bigr)Z[J]\right|_{J=0}.}
\right.
\tag{4.35}
```

**Connected Functions**

For a single real scalar field,

```math
\left.
\begin{aligned}
G_n(x_1,\ldots,x_n)&:=\langle\Omega|\mathcal T[\hat\phi_H(x_1)\cdots\hat\phi_H(x_n)]|\Omega\rangle
=\left.\frac{1}{Z[0]}\frac{1}{i^n}\frac{\delta^n Z[J]}{\delta J(x_1)\cdots\delta J(x_n)}\right|_{J=0},\\
W[J]&:=-i\ln Z[J],\qquad
G_{n,\mathrm c}=\left.\frac{1}{i^{n-1}}\frac{\delta^nW}{\delta J(x_1)\cdots\delta J(x_n)}\right|_{J=0}.
\end{aligned}
\right.
\tag{4.36}
```

Here $`|\Omega\rangle`$ is the normalized interacting vacuum and $`J(x)`$ is a commuting external source. Functional integrals require a regulator; the expressions below define their perturbative use.

**Effective Action and Schwinger--Dyson Equation**

The Legendre transform generates one-particle-irreducible (1PI) vertices, where a 1PI graph stays connected after cutting any single internal line:

```math
\left.
\phi_c(x):=\frac{\delta W}{\delta J(x)},\qquad
\Gamma[\phi_c]:=W[J]-\int d^4x\,J\phi_c,\qquad
\boxed{\frac{\delta\Gamma}{\delta\phi_c(x)}=-J(x).}
\right.
\tag{4.37}
```

For a translation-invariant scalar functional measure, with functional boundary terms absent,

```math
\left.
\left[
\left.\frac{\delta S}{\delta\phi(x)}\right|_{\phi\,\to\,(1/i)\delta/\delta J}
+J(x)\right]Z[J]=0.
\right.
\tag{4.38}
```

**Euclidean Continuation and Fermions**

When the time contour can be rotated without crossing singularities, $`t=-i\tau`$ gives, for $`\mathcal L=\tfrac12\partial_\mu\phi\partial^\mu\phi-V(\phi)`$,

```math
\left.
e^{iS}\longrightarrow e^{-S_E},\qquad
S_E=\int d\tau\,d^3x\left[\frac12(\partial_\tau\phi)^2
+\frac12(\boldsymbol\nabla\phi)^2+V(\phi)\right].
\right.
\tag{4.39}
```

Fermionic fields in the functional integral are independent Grassmann variables. With a fixed measure ordering, a quadratic Dirac action gives

```math
\left.
\int\mathcal D\bar\psi\,\mathcal D\psi\,
e^{i\int d^4x\,\bar\psi(i\gamma^\mu\partial_\mu-m)\psi}\ \propto\ \det(i\gamma^\mu\partial_\mu-m),
\right.
\tag{4.40}
```

where the field-independent normalization is absorbed into $`Z[0]`$ and the inverse of $`i\gamma^\mu\partial_\mu-m`$ uses the Feynman prescription.

**Gauge Fixing and Faddeev--Popov Ghosts**

For perturbative $`SU(3)`$ theory near the trivial gauge configuration, Lorenz gauge introduces the gauge parameter $`\xi`$ and anticommuting scalar ghost fields $`c^a,\bar c^a`$:

```math
\left.
\begin{aligned}
\mathcal L_{\mathrm{gf}}&=-\frac{1}{2\xi}(\partial^\mu A^a_\mu)^2,\\
\mathcal L_{\mathrm{gh}}&=-\bar c^a\partial^\mu(D_\mu^{ab}c^b),\qquad
D_\mu^{ab}:=\delta^{ab}\partial_\mu+g_s f^{acb}A^c_\mu,\\
\Delta_{\mathrm{FP}}[A]&=\det[-\partial^\mu D_\mu^{ab}].
\end{aligned}
\right.
\tag{4.41}
```

For an Abelian gauge field in this linear gauge, the determinant is field independent and the ghosts decouple. This local perturbative construction does not resolve global gauge-copy ambiguities.

<br><br>

<a id="phi-cubed-theory"></a>
### 4.3 $`\phi^3`$ Theory

**Action**

Take $`n=1`$, $`\mathrm{Conf}=\mathbb R`$ and $`V(\phi)=\frac12m^2\phi^2+\frac1{3!}\lambda\phi^3`$ in (4.20). With $`\Box:=\partial_\mu\partial^\mu`$ as in (1.91),

```math
\left.
\begin{aligned}
S[\phi]&=\int d^4x\,\mathcal L\bigl(\phi(x),\partial_\mu\phi(x)\bigr)\\
&=\int d^4x\,\Bigl[\frac12\partial_\mu\phi\,\partial^\mu\phi-\frac12m^2\phi^2-\frac1{3!}\lambda\phi^3\Bigr]\\
&=\int d^4x\,\Bigl[-\frac12\phi(\Box+m^2)\phi-\frac1{3!}\lambda\phi^3\Bigr]
+\frac12\int d^3x\,\bigl[\phi\,\partial_0\phi\bigr]_{x^0=t_i}^{x^0=t_f}.
\end{aligned}
\right.
\tag{4.42}
```

$`S_0[\phi]`$ denotes (4.42) at $`\lambda=0`$.

**Feynman Propagator**

```math
\left.
\begin{aligned}
(\Box+m^2)\Delta_F(x)&=-i\delta^{(4)}(x),\\
\Delta_F(x)&=\int\frac{d^4p}{(2\pi)^4}\,\frac{-i}{-p^2+m^2-i\varepsilon}\,e^{-ip\cdot x}
=\int\frac{d^4p}{(2\pi)^4}\,\frac{i}{p^2-m^2+i\varepsilon}\,e^{-ip\cdot x},
\end{aligned}
\right.
\tag{4.43}
```

with $`\varepsilon\to0^+`$; this is the function (6.12).

**Free Generating Functional**

From here on $`\mathrm{vac}`$ is the vacuum of $`S_0`$, and $`J`$ vanishes near $`x^0=t_i`$ and $`x^0=t_f`$. Let

```math
\left.
K_0^J(\Phi_f,\Phi_i):=\int_{\Phi_i}^{\Phi_f}\mathcal D\phi\,\exp\Bigl(iS_0[\phi]+i\int d^4x\,J(x)\phi(x)\Bigr),
\qquad K_0:=K_0^J\big|_{J=0}.
\right.
\tag{4.44}
```

In $`K_0^J(\mathrm{vac}_f,\mathrm{vac}_i)`$ shift the paths, together with $`\Phi_f`$ and $`\Phi_i`$, by

```math
\left.
\phi(x)\to\phi(x)+i\int d^4y\,\Delta_F(x-y)J(y),
\right.
\tag{4.45}
```

which leaves the measures in (4.28) unchanged. By (4.43), the integrand of $`\int d^4x`$ in the exponent becomes

```math
\left.
\begin{aligned}
&-\frac12\phi(\Box+m^2)\phi+J\phi\\
&\to-\frac12\phi(\Box+m^2)\phi+J\phi
\underbrace{-\frac i2\int d^4y\,\Delta_F(x-y)J(y)\,(\Box+m^2)\phi(x)}_{-\frac12J\phi}\\
&\qquad+J(x)\,i\int d^4y\,\Delta_F(x-y)J(y)
\underbrace{-\frac12\phi(x)\,i\int d^4y\,\bigl(-i\delta^{(4)}(x-y)\bigr)J(y)}_{-\frac12J\phi}\\
&\qquad\underbrace{+\frac12\int d^4y\,\Delta_F(x-y)J(y)\,(\Box+m^2)\int d^4\bar y\,\Delta_F(x-\bar y)J(\bar y)}_{-\frac i2J\Delta_FJ}\\
&\to-\frac12\phi(\Box+m^2)\phi+\frac i2\int d^4y\,J(y)\Delta_F(x-y)J(x),
\end{aligned}
\right.
\tag{4.46}
```

where the first underbrace holds after integrating by parts in $`x`$, up to terms at $`x^0=t_i,t_f`$. Write $`\chi(x):=i\int d^4y\,\Delta_F(x-y)J(y)`$ for the shift (4.45), so that $`(\Box+m^2)\chi=J`$ by (4.43). Including the terms at $`x^0=t_i,t_f`$ from (4.42) and from this integration by parts, the exponent of (4.44) after the shift is exactly

```math
\left.
\begin{aligned}
iS_0[\phi+\chi]+i\int d^4x\,J(\phi+\chi)
&=iS_0[\phi]-\frac12\int d^4x\,d^4y\,J(x)\Delta_F(x-y)J(y)\\
&\quad+i\int d^3x\,\Bigl[\bigl(\phi+\tfrac12\chi\bigr)\partial_0\chi\Bigr]_{x^0=t_i}^{x^0=t_f}.
\end{aligned}
\right.
\tag{4.47}
```

Closing the $`p^0`$ contour of (4.43) in the lower half-plane for $`x^0>0`$ and in the upper half-plane for $`x^0<0`$, around the poles $`p^0=\pm(E_{\mathbf p}-i\varepsilon')`$ with $`E_{\mathbf p}`$ as in (2.7) and $`\varepsilon'\to0^+`$,

```math
\left.
\Delta_F(x)=\int\frac{d^3p}{(2\pi)^3\,2E_{\mathbf p}}\,e^{i\mathbf p\cdot\mathbf x-iE_{\mathbf p}|x^0|}.
\right.
\tag{4.48}
```

Let $`\mathcal E:=(-\nabla^2+m^2)^{1/2}`$, i.e. $`\mathcal E\,e^{i\mathbf p\cdot\mathbf x}=E_{\mathbf p}\,e^{i\mathbf p\cdot\mathbf x}`$. Since $`J`$ vanishes near $`t_i`$ and $`t_f`$, (4.48) gives

```math
\left.
\partial_0\chi\big|_{x^0=t_f}=-i\mathcal E\chi\big|_{x^0=t_f},\qquad
\partial_0\chi\big|_{x^0=t_i}=+i\mathcal E\chi\big|_{x^0=t_i},
\right.
\tag{4.49}
```

so $`\chi`$ has only positive frequencies at $`t_f`$ and only negative frequencies at $`t_i`$.

For $`S_0`$ the vacuum is $`|0\rangle`$ of (2.8). At $`t=0`$ the Schrödinger-picture operators are $`\hat\phi(\mathbf x)=\hat\phi_I(0,\mathbf x)`$ and $`\hat\pi(\mathbf x)=\partial_0\hat\phi_I(0,\mathbf x)`$ by (6.2) and (1.86). Inverting (2.7), and acting with $`\hat\pi(\mathbf x)`$ as $`-i\,\delta/\delta\Phi(\mathbf x)`$ on $`\Psi[\Phi]=\langle\Phi|0\rangle`$,

```math
\left.
\begin{aligned}
\hat a_{\mathbf p}&=\int d^3x\,e^{-i\mathbf p\cdot\mathbf x}\bigl[E_{\mathbf p}\hat\phi(\mathbf x)+i\hat\pi(\mathbf x)\bigr],\\
0=\langle\Phi|\hat a_{\mathbf p}|0\rangle&=\int d^3x\,e^{-i\mathbf p\cdot\mathbf x}\Bigl[(\mathcal E\Phi)(\mathbf x)+\frac{\delta}{\delta\Phi(\mathbf x)}\Bigr]\Psi[\Phi]\quad\text{for all }\mathbf p,\\
\Psi[\Phi]&=\Psi[0]\exp\Bigl(-\frac12\int d^3x\,\Phi\,\mathcal E\,\Phi\Bigr),
\end{aligned}
\right.
\tag{4.50}
```

where the second line uses $`\int d^3x\,f\,\mathcal E\,g=\int d^3x\,(\mathcal Ef)\,g`$ and states $`\delta\Psi/\delta\Phi(\mathbf x)=-(\mathcal E\Phi)(\mathbf x)\Psi[\Phi]`$. With $`\chi_{f,i}:=\chi(t_{f,i},\cdot\,)`$, the shift turns $`\Psi^*[\Phi_f]\Psi[\Phi_i]`$ into $`\Psi^*[\Phi_f+\chi_f]\Psi[\Phi_i+\chi_i]`$, while $`\phi(t_{f,i},\cdot\,)=\Phi_{f,i}`$. By (4.49) and (4.50),

```math
\left.
\begin{aligned}
i\int d^3x\,\Bigl[\bigl(\phi+\tfrac12\chi\bigr)\partial_0\chi\Bigr]_{x^0=t_i}^{x^0=t_f}
&=\int d^3x\,\Bigl[\bigl(\Phi_f+\tfrac12\chi_f\bigr)\mathcal E\chi_f+\bigl(\Phi_i+\tfrac12\chi_i\bigr)\mathcal E\chi_i\Bigr],\\
\ln\frac{\Psi^*[\Phi_f+\chi_f]\,\Psi[\Phi_i+\chi_i]}{\Psi^*[\Phi_f]\,\Psi[\Phi_i]}
&=-\int d^3x\,\Bigl[\bigl(\Phi_f+\tfrac12\chi_f\bigr)\mathcal E\chi_f+\bigl(\Phi_i+\tfrac12\chi_i\bigr)\mathcal E\chi_i\Bigr],
\end{aligned}
\right.
\tag{4.51}
```

so the terms at $`x^0=t_i,t_f`$ in (4.47) cancel the change of $`\Psi^*[\Phi_f]\Psi[\Phi_i]`$. Hence

```math
\left.
K_0^J(\mathrm{vac}_f,\mathrm{vac}_i)=K_0(\mathrm{vac}_f,\mathrm{vac}_i)\,
\exp\Bigl[-\frac12\int d^4x\,d^4y\,J(x)\Delta_F(x-y)J(y)\Bigr],
\right.
\tag{4.52}
```

and

```math
\left.
\boxed{
\begin{aligned}
Z_0[J]&:=K_0^J(\mathrm{vac}_f,\mathrm{vac}_i)
=\int\mathcal D\Phi_f\,\mathcal D\Phi_i\,\Psi^*[\Phi_f]\,\Psi[\Phi_i]\,K_0^J(\Phi_f,\Phi_i)\\
&=Z_0[0]\,\exp\Bigl[-\frac12\int d^4x\,d^4y\,J(x)\Delta_F(x-y)J(y)\Bigr],
\end{aligned}}
\right.
\tag{4.53}
```

with $`Z_0[0]=K_0(\mathrm{vac}_f,\mathrm{vac}_i)`$ by (4.52).

**Two-Point Function**

For $`S_0`$ and $`t_i<z_1^0,z_2^0<t_f`$, by (4.35) and (4.53),

```math
\left.
\boxed{
\begin{aligned}
\langle\phi(z_1)\phi(z_2)\rangle_{\mathrm{vac}}
&=\frac{1}{Z_0[0]}\Bigl(-i\frac{\delta}{\delta J(z_1)}\Bigr)\Bigl(-i\frac{\delta}{\delta J(z_2)}\Bigr)Z_0[J]\Big|_{J=0}\\
&=\Bigl(-i\frac{\delta}{\delta J(z_1)}\Bigr)\Bigl(-i\frac{\delta}{\delta J(z_2)}\Bigr)
\exp\Bigl[-\frac12\int d^4x\,d^4y\,J(x)\Delta_F(x-y)J(y)\Bigr]\Big|_{J=0}\\
&=\frac12\Delta_F(z_1-z_2)+\frac12\Delta_F(z_2-z_1)\\
&=\Delta_F(z_1-z_2).
\end{aligned}}
\right.
\tag{4.54}
```

**Perturbation Expansion**

By (4.12), each $`-i\,\delta/\delta J(z)`$ acting on (4.44) inserts $`\phi(z)`$, so

```math
\left.
\begin{aligned}
K(\Phi_f,\Phi_i)
&=\int_{\Phi_i}^{\Phi_f}\mathcal D\phi\,\exp\Bigl(iS_0[\phi]+i\int d^4z\,\Bigl(-\frac{\lambda}{3!}\Bigr)\phi^3\Bigr)\\
&=\int_{\Phi_i}^{\Phi_f}\mathcal D\phi\,e^{iS_0[\phi]}\sum_{m=0}^\infty\frac1{m!}\Bigl(i\int d^4z\,\Bigl(-\frac{\lambda}{3!}\Bigr)\phi(z)^3\Bigr)^m\\
&=\sum_{m=0}^\infty\frac1{m!}\Bigl(-\frac{i\lambda}{3!}\Bigr)^m\prod_{k=1}^m\int d^4z_k\Bigl(-i\frac{\delta}{\delta J(z_k)}\Bigr)^3K_0^J(\Phi_f,\Phi_i)\Big|_{J=0}\\
&=\sum_{m=0}^\infty\frac1{m!}\Bigl(\frac{\lambda}{3!}\Bigr)^m\prod_{k=1}^m\int d^4z_k\Bigl(\frac{\delta}{\delta J(z_k)}\Bigr)^3K_0^J(\Phi_f,\Phi_i)\Big|_{J=0}.
\end{aligned}
\right.
\tag{4.55}
```

With the vacuum of $`S_0`$ at both ends, (4.52) gives

```math
\left.
\boxed{
\begin{aligned}
K(\mathrm{vac}_f,\mathrm{vac}_i)
&=\sum_{m=0}^\infty\frac1{m!}\Bigl(\frac{\lambda}{3!}\Bigr)^m\prod_{k=1}^m\int d^4z_k\Bigl(\frac{\delta}{\delta J(z_k)}\Bigr)^3\\
&\qquad\exp\Bigl[-\frac12\int d^4x\,d^4y\,J(x)\Delta_F(x-y)J(y)\Bigr]\Big|_{J=0}\cdot K_0(\mathrm{vac}_f,\mathrm{vac}_i).
\end{aligned}}
\right.
\tag{4.56}
```

<br><br>

<a id="qft-ch5"></a>
## 5. New Physics Beyond the Standard Model

**Effective Field Theory**

For energies $`E\ll M_*`$ and only Standard Model fields below the heavy scale $`M_*`$, the Standard Model effective field theory expands in local gauge-invariant operators:

```math
\left.
\begin{aligned}
\mathcal L_{\mathrm{EFT}}
&=\mathcal L_{\mathrm{SM}}
+\sum_{d>4}\sum_a\frac{C_a^{(d)}(\mu)}{M_*^{\,d-4}}\,
\mathcal O_a^{(d)}(\mu),\\
[\mathcal O_a^{(d)}]&=d,\qquad [C_a^{(d)}]=0 .
\end{aligned}
\right.
\tag{5.1}
```

Here brackets denote mass dimension, $`\mu`$ is the renormalization scale, and the coefficients are Wilson coefficients. Hermitian conjugates are included for non-Hermitian operators. This expansion assumes a linearly transforming Higgs doublet.

Using $`H^c`$ and $`L_{Lr}`$ above, define the gauge-singlet left-handed spinor $`n_{Lr}:=(H^c)^\dagger L_{Lr}`$. The antisymmetric matrix $`C:=i\gamma^2\gamma^0`$ contracts the spinor indices in the Lorentz scalar $`n_{Lr}^TCn_{Ls}`$. The dimension-five Weinberg term is

```math
\left.
\begin{aligned}
\mathcal L_5
&=-\frac{\kappa_{rs}}{2M_*}\,n_{Lr}^TCn_{Ls}
+\mathrm{h.c.},\qquad \kappa_{rs}=\kappa_{sr},\\
M_\nu&=\frac{v^2}{2M_*}\,\kappa .
\end{aligned}
\right.
\tag{5.2}
```

This term gives Majorana masses to the active neutrinos and violates total lepton number by two units.

<br><br>


<a id="seesaw-mechanism"></a>
### 5.1 Seesaw Mechanism

<a id="type-i-seesaw"></a>
#### Type-I Seesaw

<br><br>

<a id="type-ii-seesaw"></a>
#### Type-II Seesaw

<br><br>

<a id="type-iii-seesaw"></a>
#### Type-III Seesaw

<br><br>

<a id="leptogenesis"></a>
#### Leptogenesis

<br><br>

<a id="dark-matter"></a>
### 5.2 Dark Matter

<br><br>

<a id="qft-ch6"></a>
## 6. Scattering Theory

<a id="interaction-picture-dyson"></a>
<a id="perturbation-theory"></a>
<a id="interaction-picture"></a>
### 6.1 Interaction Picture

Let the Hamiltonian be

```math
\left.
\hat H=\hat H_0+\hat V
\right.
\tag{6.1}
```

The interaction picture evolves operators with $`\hat H_0`$ of (6.1) instead of $`\hat H`$:

```math
\left.
\boxed{
\begin{gathered}
\hat O_I(t):=e^{i\hat H_0t}\,\hat O_S\,e^{-i\hat H_0t},\\[4pt]
|\psi_I(t)\rangle:=e^{i\hat H_0t}\,|\psi_S(t)\rangle .
\end{gathered}
}
\right.
\tag{6.2}
```

The three pictures coincide at $`t=0`$, and $`\langle\psi_I(t)|\hat O_I(t)|\psi_I(t)\rangle=\langle\psi_S(t)|\hat O_S|\psi_S(t)\rangle`$.

Differentiating the first of (6.2),

```math
\left.
\frac{d\hat O_I}{dt}=i\,[\hat H_0,\hat O_I].
\right.
\tag{6.3}
```

In particular $`\hat H_{0,I}=\hat H_0`$, while the interaction term becomes time dependent. Differentiating the second of (6.2) and using $`i\partial_t|\psi_S\rangle=\hat H|\psi_S\rangle`$,

```math
\left.
i\partial_t|\psi_I(t)\rangle
=e^{i\hat H_0t}\bigl(\hat H-\hat H_0\bigr)|\psi_S(t)\rangle
=e^{i\hat H_0t}\hat Ve^{-i\hat H_0t}\,|\psi_I(t)\rangle,
\right.
\tag{6.4}
```

i.e.

```math
\left.
\boxed{
i\partial_t|\psi_I(t)\rangle=\hat V_I(t)\,|\psi_I(t)\rangle,
\qquad
\hat V_I(t):=e^{i\hat H_0t}\,\hat V\,e^{-i\hat H_0t}.
}
\right.
\tag{6.5}
```

Substituting $`\hat O_S=e^{-i\hat H_0t}\hat O_I(t)e^{i\hat H_0t}`$ into (2.22),

```math
\left.
\hat O_H(t)=\hat U_I(t,0)^\dagger\,\hat O_I(t)\,\hat U_I(t,0),
\qquad
\hat U_I(t,0):=e^{i\hat H_0t}\,\hat U(t,0).
\right.
\tag{6.6}
```

For a field operator, (6.6) reads $`\hat\phi_H(t,\mathbf x)=\hat U_I(t,0)^\dagger\,\hat\phi_I(t,\mathbf x)\,\hat U_I(t,0)`$, and by (6.3) $`\hat\phi_I(t,\mathbf x)`$ obeys the Heisenberg equation of $`\hat H_0`$ alone.

**Dyson Series**

The state equation (6.5) is the second line of (2.13) with $`\hat H`$ replaced by $`\hat V_I(t)`$. The interaction-picture evolution operator $`\hat U_I(t,t_0)`$, defined by $`|\psi_I(t)\rangle=\hat U_I(t,t_0)|\psi_I(t_0)\rangle`$, is therefore $`\hat U(t,t_0)`$ of (2.21) with $`\hat H\to\hat V_I(t)`$: it is unitary, $`\hat U_I(t_1,t_2)\hat U_I(t_2,t_3)=\hat U_I(t_1,t_3)`$, and $`\hat U_I(t,t_0)^\dagger=\hat U_I(t_0,t)`$. By (6.2) and (2.21),

```math
\left.
\hat U_I(t,t_0)=e^{i\hat H_0t}\,\hat U(t,t_0)\,e^{-i\hat H_0t_0},
\right.
\tag{6.7}
```

which reduces to the $`\hat U_I(t,0)`$ of (6.6) at $`t_0=0`$; when $`\hat H`$ has no explicit time dependence, $`\hat U(t,t_0)=e^{-i\hat H(t-t_0)}`$ by (2.14). Since $`[\hat V_I(t_1),\hat V_I(t_2)]\neq0`$ in general, case (3) of [Section 2.4](#symmetry) applies, and by (2.20)

```math
\left.
\boxed{
\hat U_I(t,t_0)=\mathcal T\exp\Bigl(-i\int_{t_0}^{t}dt'\,\hat V_I(t')\Bigr).
}
\right.
\tag{6.8}
```

In field theory, $`\hat V=\int d^3x\,\hat{\mathcal H}_{\mathrm{int}}\bigl(\hat\phi_S(\mathbf x)\bigr)`$. By (6.2), $`\hat V_I(t)=\int d^3x\,\hat{\mathcal H}_{\mathrm{int}}\bigl(\hat\phi_I(t,\mathbf x)\bigr)`$, and (6.8) becomes

```math
\left.
\hat U_I(t,t_0)=\mathcal T\exp\Bigl(-i\int_{t_0}^{t}dt'\int d^3x\,\hat{\mathcal H}_{\mathrm{int}}\bigl(\hat\phi_I(x)\bigr)\Bigr).
\right.
\tag{6.9}
```

For interactions without derivative couplings, $`\hat{\mathcal H}_{\mathrm{int}}=-\hat{\mathcal L}_{\mathrm{int}}`$.

<br><br>

<a id="s-matrix-and-wick-theorem"></a>
### 6.2 The S-Matrix and Wick's Theorem

**Asymptotic States and the S-Matrix**

Assume stable asymptotic particles and the existence of free-particle wave-packet limits. In-states approach the corresponding free states as $`t\to-\infty`$, and out-states as $`t\to+\infty`$. In perturbation theory, with adiabatic switching and the vacuum phase removed,

```math
\left.
\begin{aligned}
S_{fi}&:=\langle f,\mathrm{out}|i,\mathrm{in}\rangle=\langle f|\hat S|i\rangle,\\
\hat S&=\hat U_I(+\infty,-\infty)
=\mathcal T\exp\left(-i\int_{-\infty}^{+\infty}dt\,\hat V_I(t)\right).
\end{aligned}
\right.
\tag{6.10}
```

Let $`p_i`$ and $`p_f`$ denote the total initial and final four-momenta. The connected invariant amplitude $`\mathcal M_{fi}`$ and the transition operator $`\hat T`$ are defined by

```math
\left.
\boxed{\begin{aligned}
\hat S&=1+i\hat T,\qquad
\langle f|\hat T|i\rangle_{\mathrm c}=(2\pi)^4\delta^{(4)}(p_f-p_i)\,\mathcal M_{fi},\\
\hat S^\dagger\hat S&=1\quad\Longrightarrow\quad -i(\hat T-\hat T^\dagger)=\hat T^\dagger\hat T.
\end{aligned}}
\right.
\tag{6.11}
```

**Normal Ordering, Contractions, and Wick's Theorem**

Normal ordering refers to the free vacuum $`|0\rangle`$. For a free real scalar field, its contraction is the Feynman propagator; $`\varepsilon\to0^+`$ is understood:

```math
\left.
\begin{aligned}
\Delta_F(x-y)&:=\langle0|\mathcal T[\hat\phi_I(x)\hat\phi_I(y)]|0\rangle\\
&=\mathcal T[\hat\phi_I(x)\hat\phi_I(y)]-:\hat\phi_I(x)\hat\phi_I(y):\\
&=\int\frac{d^4p}{(2\pi)^4}\,\frac{i\,e^{-ip\cdot(x-y)}}{p^2-m^2+i\varepsilon}.
\end{aligned}
\right.
\tag{6.12}
```

Wick's theorem expresses a time-ordered product of free fields as the sum over all disjoint contractions, including no contractions. Writing $`\hat\phi_j:=\hat\phi_I(x_j)`$,

```math
\left.
\begin{aligned}
\mathcal T[\hat\phi_1\cdots\hat\phi_n]
&=\sum_{\text{disjoint pairings }P}
\left[\prod_{(i,j)\in P}\Delta_F(x_i-x_j)\right]
:\prod_{k\text{ unpaired in }P}\hat\phi_k:,\\
\langle0|\mathcal T[\hat\phi_1\hat\phi_2\hat\phi_3\hat\phi_4]|0\rangle
&=\Delta_F(x_1-x_2)\Delta_F(x_3-x_4)
+\Delta_F(x_1-x_3)\Delta_F(x_2-x_4)\\
&\quad+\Delta_F(x_1-x_4)\Delta_F(x_2-x_3).
\end{aligned}
\right.
\tag{6.13}
```

For fermions, time ordering and Wick contractions carry the sign of the required permutation of fermionic operators. Free-vacuum expectation values retain only fully contracted terms.


<br><br>

<a id="feynman-diagrams"></a>
### 6.3 Feynman Diagrams and Feynman Rules

**Scalar Example**

For a real scalar with quartic coupling $`\lambda`$, the momentum-space rules contribute to $`i\mathcal M`$. At tree level,

```math
\left.
\begin{aligned}
\mathcal L&=\frac12\partial_\mu\phi\,\partial^\mu\phi-\frac12m^2\phi^2-\frac{\lambda}{4!}\phi^4,\qquad
\hat{\mathcal H}_{\mathrm{int}}=\frac{\lambda}{4!}\hat\phi_I^4,\\
\text{internal scalar line}:&\quad\widetilde\Delta_F(p)=\frac{i}{p^2-m^2+i\varepsilon},\qquad
\text{four-scalar vertex}:\quad -i\lambda,\\
 i\mathcal M_{\phi\phi\to\phi\phi}^{\mathrm{tree}}&=-i\lambda.
\end{aligned}
\right.
\tag{6.14}
```

**Propagators and External States**

Define $`S_F(x-y):=\langle0|\mathcal T[\hat\psi_I(x)\overline{\hat\psi}_I(y)]|0\rangle`$ and $`D_{\mu\nu}(x-y):=\langle0|\mathcal T[\hat A_{I,\mu}(x)\hat A_{I,\nu}(y)]|0\rangle`$. Their Fourier transforms are

```math
\left.
\begin{aligned}
\widetilde S_F(p)&=\frac{i(\not p+m)}{p^2-m^2+i\varepsilon},\\
\widetilde D_{\mu\nu}^{(\xi)}(p)&=\frac{-i}{p^2+i\varepsilon}\left[\eta_{\mu\nu}-(1-\xi)\frac{p_\mu p_\nu}{p^2+i\varepsilon}\right],
\qquad \mathcal L_{\mathrm{gf}}=-\frac1{2\xi}(\partial_\mu A^\mu)^2,\\
\widetilde D_{\mu\nu}^{\mathrm{Proca}}(p)&=\frac{-i}{p^2-m_V^2+i\varepsilon}\left(\eta_{\mu\nu}-\frac{p_\mu p_\nu}{m_V^2}\right),\qquad m_V>0.
\end{aligned}
\right.
\tag{6.15}
```

Here $`\xi`$ is the covariant gauge parameter ($`\xi=1`$ is Feynman gauge), and $`m_V`$ is the Proca mass. For fields with unit one-particle pole residue, the external factors are

```math
\left.
\begin{array}{c|cc}
\text{external state}&\text{incoming}&\text{outgoing}\\ \hline
\text{scalar}&1&1\\
\text{fermion}&u^s(p)&\bar u^s(p)\\
\text{antifermion}&\bar v^s(p)&v^s(p)\\
\text{vector}&\epsilon_\mu^r(p)&\epsilon_\mu^{r*}(p)
\end{array}
\right.
\tag{6.16}
```

The $`\epsilon_\mu^r`$ are physical polarization vectors. External propagators are amputated; a general field normalization requires the pole-residue factors in [Section 6.5](#lsz-reduction).

**Diagram Rules**

Impose four-momentum conservation at every vertex, integrate each independent loop momentum with $`d^4\ell/(2\pi)^4`$, and sum connected amputated diagrams. Remove the overall $`(2\pi)^4\delta^{(4)}(p_f-p_i)`$ to obtain $`i\mathcal M`$. Divide each graph by its symmetry factor with the external legs held fixed. Each closed fermion loop contributes an additional minus sign; exchanging identical external fermions also changes the sign.

For example, the $`s`$-channel one-loop four-scalar graph has symmetry factor $`2`$:

```math
\left.
i\mathcal M_s^{\mathrm{1\,loop}}
=\frac{(-i\lambda)^2}{2}\int\frac{d^4\ell}{(2\pi)^4}
\frac{i}{\ell^2-m^2+i\varepsilon}
\frac{i}{(\ell+p_1+p_2)^2-m^2+i\varepsilon},
\qquad s:=(p_1+p_2)^2.
\right.
\tag{6.17}
```

Loop integrals require a regulator and, in a renormalized amplitude, the corresponding counterterms. The full one-loop four-point amplitude also contains the crossed channels.


<br><br>

<a id="correlation-functions"></a>
### 6.4 Correlation Functions

**Vacuum Correlation Functions**

Let $`|\Omega\rangle`$ be the interacting vacuum and $`|0\rangle`$ the free vacuum. With adiabatic vacuum projection understood, the Gell-Mann--Low formula gives

```math
\left.
\begin{aligned}
G_n(x_1,\ldots,x_n)&:=\frac{\langle\Omega|\mathcal T[\hat\phi_H(x_1)\cdots\hat\phi_H(x_n)]|\Omega\rangle}{\langle\Omega|\Omega\rangle}\\
&=\frac{\langle0|\mathcal T\left[\hat\phi_I(x_1)\cdots\hat\phi_I(x_n)\exp\left(-i\int dt\,\hat V_I(t)\right)\right]|0\rangle}
{\langle0|\mathcal T\exp\left(-i\int dt\,\hat V_I(t)\right)|0\rangle}.
\end{aligned}
\right.
\tag{6.18}
```

The denominator cancels disconnected vacuum bubbles. Graphs contributing to $`G_n`$ may still be disconnected if each component has external field insertions.

**Generating Functionals and Connected Functions**

For a real scalar source $`J(x)`$,

```math
\left.
\begin{aligned}
Z[J]&:=\frac{\langle\Omega|\mathcal T\exp\left(i\int d^4x\,J(x)\hat\phi_H(x)\right)|\Omega\rangle}{\langle\Omega|\Omega\rangle},\qquad Z[0]=1,\qquad W[J]:=-i\ln Z[J],\\
G_n(x_1,\ldots,x_n)&=\left.\frac1{i^n}\frac{\delta^nZ[J]}{\delta J(x_1)\cdots\delta J(x_n)}\right|_{J=0},\\
G_{n,\mathrm c}(x_1,\ldots,x_n)&=\left.i^{1-n}\frac{\delta^nW[J]}{\delta J(x_1)\cdots\delta J(x_n)}\right|_{J=0}.
\end{aligned}
\right.
\tag{6.19}
```

For $`G_1=0`$, the four-point function splits into connected and disconnected contributions as

```math
\left.
\begin{aligned}
G_4(x_1,x_2,x_3,x_4)
&=G_{4,\mathrm c}(x_1,x_2,x_3,x_4)
+G_2(x_1,x_2)G_2(x_3,x_4)\\
&\quad+G_2(x_1,x_3)G_2(x_2,x_4)
+G_2(x_1,x_4)G_2(x_2,x_3).
\end{aligned}
\right.
\tag{6.20}
```


<br><br>

<a id="lsz-reduction"></a>
### 6.5 LSZ Reduction Formula

**One-Particle Pole**

Consider a real scalar field with zero vacuum expectation value, an isolated stable one-particle pole of physical mass $`m_{\mathrm{phys}}>0`$, and nonzero overlap with that particle. Choose the particle-state phase so that

```math
\left.
\begin{aligned}
\langle\Omega|\hat\phi_H(0)|\mathbf p\rangle&=\sqrt{Z_{\mathrm{pole}}},\qquad Z_{\mathrm{pole}}>0,\qquad \langle\Omega|\Omega\rangle=1,\\
\widetilde G_2(p)&:=\int d^4x\,e^{ip\cdot x}G_2(x,0)
=\frac{iZ_{\mathrm{pole}}}{p^2-m_{\mathrm{phys}}^2+i\varepsilon}
+\text{terms regular at the pole}.
\end{aligned}
\right.
\tag{6.21}
```

Here $`Z_{\mathrm{pole}}`$ is the pole residue for the chosen field normalization. Assume the corresponding asymptotic scattering states exist.

**Reduction Formula**

For $`r`$ incoming momenta $`p_a`$ and $`s`$ outgoing momenta $`q_b`$, all with positive physical energies, define $`\widetilde G_{r+s,\mathrm c}`$ by Fourier transforming every position with $`e^{+ik\cdot x}`$. For a connected scattering process with $`r+s>2`$,

```math
\left.
\boxed{\begin{aligned}
&i(2\pi)^4\delta^{(4)}\left(\sum_{b=1}^{s}q_b-\sum_{a=1}^{r}p_a\right)\mathcal M_{fi}\\
&\quad=\lim_{\mathrm{on\ shell}}
\left[\prod_{b=1}^{s}\frac{q_b^2-m_{\mathrm{phys}}^2}{i\sqrt{Z_{\mathrm{pole}}}}\right]
\left[\prod_{a=1}^{r}\frac{p_a^2-m_{\mathrm{phys}}^2}{i\sqrt{Z_{\mathrm{pole}}}}\right]
\widetilde G_{r+s,\mathrm c}(q_1,\ldots,q_s,-p_1,\ldots,-p_r).
\end{aligned}}
\right.
\tag{6.22}
```

The limit means extracting the simultaneous external-pole residue with the Feynman prescription before taking all external momenta on shell. Each factor removes one external propagator and its field overlap. A field normalized to unit pole residue has $`Z_{\mathrm{pole}}=1`$.


<br><br>

<a id="cross-sections-and-decay-rates"></a>
### 6.6 Cross Sections and Decay Rates

**Phase Space and State Sums**

For total final momentum $`P`$ and $`n`$ on-shell outgoing momenta $`k_j`$,

```math
\left.
d\Phi_n(P;k_1,\ldots,k_n):=(2\pi)^4\delta^{(4)}\left(P-\sum_{j=1}^{n}k_j\right)
\prod_{j=1}^{n}\frac{d^3k_j}{(2\pi)^3\,2E_{\mathbf k_j}},\qquad
E_{\mathbf k_j}=\sqrt{\mathbf k_j^2+m_j^2}.
\right.
\tag{6.23}
```

Use $`\overline{|\mathcal M|^2}`$ for the sum over unobserved final spins and internal quantum numbers, averaged over the equally populated initial states. For two unpolarized initial particles with $`N_1,N_2`$ such states,

```math
\left.
\overline{|\mathcal M|^2}:=\frac1{N_1N_2}\sum_{\text{initial, final states}}|\mathcal M|^2,
\qquad C_{\mathrm{id}}:=\prod_a\nu_a!.
\right.
\tag{6.24}
```

Here $`\nu_a`$ is the number of identical final particles of species $`a`$. Divide by $`C_{\mathrm{id}}`$ when integrating the full phase space of labeled final momenta; omit this factor if the integration region already counts each physical final configuration once. Fixed initial polarizations are not averaged.

**Cross Sections and Decay Rates**

For $`1+2\to n`$ scattering and decay of a particle of mass $`M`$ at rest,

```math
\left.
\boxed{\begin{aligned}
d\sigma&=\frac{\overline{|\mathcal M|^2}}{4\sqrt{(p_1\cdot p_2)^2-m_1^2m_2^2}}\,\frac{d\Phi_n(p_1+p_2)}{C_{\mathrm{id}}},\\
d\Gamma&=\frac{\overline{|\mathcal M|^2}}{2M}\,\frac{d\Phi_n(P)}{C_{\mathrm{id}}},\qquad P=(M,\mathbf0).
\end{aligned}}
\right.
\tag{6.25}
```

In the decay formula, average only over the parent's initial states if an unpolarized rate is intended. For two-body final states, use the single-particle three-momentum magnitudes $`|\mathbf p_1|`$ and $`|\mathbf k_1|`$ for the initial and final states in the center-of-mass frame:

```math
\left.
\begin{aligned}
\frac{d\sigma_{2\to2}}{d\Omega}
&=\frac1{64\pi^2s\,C_{\mathrm{id}}}\frac{|\mathbf k_1|}{|\mathbf p_1|}\,\overline{|\mathcal M|^2},\qquad s=(p_1+p_2)^2,\\
\frac{d\Gamma_{1\to2}}{d\Omega}
&=\frac{|\mathbf k_1|}{32\pi^2M^2\,C_{\mathrm{id}}}\,\overline{|\mathcal M|^2},\\
\Gamma_{1\to2}&=\frac{|\mathbf k_1|}{8\pi M^2\,C_{\mathrm{id}}}\,\overline{|\mathcal M|^2}\qquad\text{if the squared amplitude is angle independent}.
\end{aligned}
\right.
\tag{6.26}
```

For the decay formulas, $`|\mathbf k_1|`$ is evaluated in the parent's rest frame. The solid-angle integrals use the same identical-particle counting convention as the full phase space.


<br><br>

<a id="qft-ch7"></a>
## 7. Renormalization

**Power Counting**

Square brackets here denote mass dimension. For canonical kinetic terms in $`d`$ spacetime dimensions,

```math
\left.
[\partial_\mu]=1,\qquad [\mathcal L]=d,\qquad
[\phi]=[A_\mu]=\frac{d-2}{2},\qquad [\psi]=\frac{d-1}{2},\qquad
[c_{\mathcal O}]=d-[\mathcal O].
\right.
\tag{7.1}
```

For an interaction $`c_{\mathcal O}\mathcal O`$, $`[\mathcal O]<d`$, $`=d`$, and $`>d`$ define relevant, marginal, and irrelevant operators at the Gaussian fixed point. Quantum anomalous dimensions modify this classification at other fixed points.

For a connected graph built from scalar, vector, and ghost propagators behaving as $`k^{-2}`$ and spinor propagators behaving as $`k^{-1}`$,

```math
\left.
L=I_B+I_F-V+1,\qquad
\omega=dL-2I_B-I_F+\sum_v n_{\partial,v}.
\right.
\tag{7.2}
```

Here $`L`$ counts loops, $`I_B,I_F`$ the respective internal lines, $`V`$ vertices, and $`n_{\partial,v}`$ derivatives at vertex $`v`$. The superficial degree $`\omega`$ counts simultaneous ultraviolet scaling; subdivergences and symmetry cancellations must be assessed separately.

**Dimensional Regularization and Counterterms**

Use $`d=4-\epsilon`$, with $`\epsilon`$ distinct from the Feynman $`\varepsilon`$. The renormalization scale is $`\mu`$:

```math
\left.
\int\frac{d^4k}{(2\pi)^4}\ \longrightarrow\
\int\frac{d^{4-\epsilon}k}{(2\pi)^{4-\epsilon}},\qquad
\frac{2}{\bar\epsilon}:=\frac{2}{\epsilon}-\gamma_E+\ln(4\pi).
\right.
\tag{7.3}
```

For real $`\phi^4`$ theory, the bare field is $`\phi_0=Z_\phi^{1/2}\phi_R`$. One convenient counterterm parametrization is

```math
\left.
\begin{aligned}
\mathcal L&=\mathcal L_R+\mathcal L_{\mathrm{ct}},\\
\mathcal L_R&=\frac12\partial_\mu\phi_R\partial^\mu\phi_R
-\frac12m^2\phi_R^2-\frac{\mu^{\epsilon}\lambda}{4!}\phi_R^4,\\
\mathcal L_{\mathrm{ct}}&=\frac12\delta Z_\phi\partial_\mu\phi_R\partial^\mu\phi_R
-\frac12\delta m^2\phi_R^2-\frac{\mu^{\epsilon}\delta\lambda}{4!}\phi_R^4,
\qquad\delta Z_\phi=Z_\phi-1.
\end{aligned}
\right.
\tag{7.4}
```

Here the factors of $`\mu`$ are carried by the couplings; no additional power of $`\mu`$ is included in each loop measure. Minimal subtraction (MS) removes pole terms; $`\overline{\mathrm{MS}}`$ also includes the displayed $`-\gamma_E+\ln4\pi`$ combination.

**Pole Mass and Field Normalization**

Defining the scalar self-energy by

```math
\left.
\widetilde G_{2,R}(p)=\frac{i}{p^2-m^2-\Sigma_R(p^2)+i\varepsilon},\qquad
\boxed{\Sigma_R(m^2)=0,\qquad \Sigma_R'(m^2)=0\quad\text{(on-shell scheme)},}
\right.
\tag{7.5}
```

the on-shell scheme makes $`m`$ the mass of an isolated stable particle and fixes the propagator residue to one. In other schemes the renormalized mass need not equal the pole mass. The ultraviolet factor $`Z_\phi`$ is not generally the finite pole residue $`Z_{\mathrm{pole}}`$ of the renormalized interpolating field used in LSZ.

**Renormalization Group**

Derivatives are taken at fixed bare parameters:

```math
\left.
\begin{aligned}
\beta_\lambda&:=\left.\mu\frac{d\lambda}{d\mu}\right|_{\mathrm{bare}},\qquad
\beta_{m^2}:=\left.\mu\frac{dm^2}{d\mu}\right|_{\mathrm{bare}},\\
\gamma_\phi&:=\left.\frac12\mu\frac{d\ln Z_\phi}{d\mu}\right|_{\mathrm{bare}},\\
0&=\left[\mu\frac{\partial}{\partial\mu}
+\beta_\lambda\frac{\partial}{\partial\lambda}
+\beta_{m^2}\frac{\partial}{\partial m^2}+n\gamma_\phi\right]G_{n,R}.
\end{aligned}
\right.
\tag{7.6}
```

This equation applies to renormalized elementary-field correlators at separated points; composite operators require their own renormalization. In four dimensions, the leading coefficients for real $`\phi^4`$ theory and for QCD with $`n_f`$ active Dirac quark flavors are

```math
\left.
\begin{aligned}
\beta_\lambda&=\frac{3\lambda^2}{16\pi^2}+O(\lambda^3),\\
\beta_{g_s}&=-\frac{g_s^3}{16\pi^2}\left(11-\frac23n_f\right)+O(g_s^5),
\qquad\alpha_s:=\frac{g_s^2}{4\pi},\\
\alpha_s(\mu)&=\frac{\alpha_s(\mu_0)}
{1+\dfrac{11-2n_f/3}{2\pi}\alpha_s(\mu_0)\ln(\mu/\mu_0)}
\quad\text{(one loop, fixed }n_f\text{)}.
\end{aligned}
\right.
\tag{7.7}
```

The QCD result is perturbative and uses a mass-independent scheme with threshold matching when the active flavor content changes.

**Ward Identities and Anomalies**

For a vector-like Abelian theory with a symmetry-preserving regulator, let $`\Gamma^\mu`$ be the proper current vertex with the coupling stripped off, and let $`S_R(p)=i\mathcal S_R(p)`$ be the full fermion propagator. Then

```math
\left.
q_\mu\Gamma^\mu(p+q,p)
=\mathcal S_R^{-1}(p+q)-\mathcal S_R^{-1}(p),\qquad Z_1=Z_2.
\right.
\tag{7.8}
```

Here $`Z_1`$ and $`Z_2`$ are the vertex and fermion-field renormalization constants. Non-Abelian gauge theories obey Slavnov--Taylor identities involving ghosts. A symmetry of the classical action may fail for the regulated quantum measure; gauge-anomaly cancellation is required for a consistent chiral gauge theory.

<br><br>

<a id="qed-renormalization"></a>
### 7.1 QED Renormalization

**Gauge-Fixed Lagrangian**

With the covariant gauge fixing of (6.15), the QED Lagrangian (3.26) for Dirac fields $`\psi_f`$ of charge $`Q_fe`$ and mass $`m_f`$ is

```math
\left.
\mathcal L
=\sum_f\bar\psi_f\bigl(i\gamma^\mu\partial_\mu-m_f\bigr)\psi_f
-\frac14F_{\mu\nu}F^{\mu\nu}
-\frac1{2\xi}(\partial_\mu A^\mu)^2
+eA_\mu\sum_fQ_f\,\bar\psi_f\gamma^\mu\psi_f .
\right.
\tag{7.9}
```

The Faddeev--Popov ghosts decouple, as noted after (4.41).


**Feynman Rules**

The momentum-space factors contributing to $`i\mathcal M`$ are

```math
\left.
\begin{array}{l|l}
\text{element}&\text{factor}\\ \hline
\text{fermion propagator, momentum }p\text{ along the arrow}&\dfrac{i(\not p+m_f)}{p^2-m_f^2+i\varepsilon}\\[12pt]
\text{photon propagator}&\dfrac{-i}{p^2+i\varepsilon}\left[\eta_{\mu\nu}-(1-\xi)\dfrac{p_\mu p_\nu}{p^2+i\varepsilon}\right]\\[12pt]
\text{fermion-photon vertex}&ieQ_f\gamma^\mu\\[4pt]
\text{incoming / outgoing fermion}&u^s(p)\ /\ \bar u^s(p)\\
\text{incoming / outgoing antifermion}&\bar v^s(p)\ /\ v^s(p)\\
\text{incoming / outgoing photon}&\epsilon^r_\mu(p)\ /\ \epsilon^{r*}_\mu(p)
\end{array}
\right.
\tag{7.10}
```

For the electron, $`Q_f=-1`$ and the vertex is $`-ie\gamma^\mu`$. Along each fermion line, write the factors in the order opposite to the arrow, so that the spinor indices form a matrix product. Impose four-momentum conservation at every vertex and integrate each loop momentum with $`\int d^4\ell/(2\pi)^4`$, continued to $`d`$ dimensions by (7.3). Each closed fermion loop gives a factor $`-1`$ and a Dirac trace; exchanging identical external fermions changes the sign, as in [Section 6.3](#feynman-diagrams).

**Tree Level: $`e^+e^-\to q\bar q`$**

<p align="center"><img src="figures/ee-to-qqbar.svg" alt="Tree-level s-channel diagram for e+ e- to q qbar" width="440"></p>

Time runs from left to right. Arrows on the fermion lines show the fermion-number flow; grey arrows show the four-momenta.

Label the spins of $`e^-,e^+,q,\bar q`$ by $`s,s',r,r'`$ and the colors of $`q,\bar q`$ by $`c,c'\in\{1,2,3\}`$; the photon vertex is diagonal in color, and $`p_1+p_2=k_1+k_2`$. Reading each fermion line against its arrow with (7.10),

```math
\left.
\begin{aligned}
i\mathcal M
={}&\bigl[\bar v^{s'}(p_2)\,(-ie\gamma^\mu)\,u^s(p_1)\bigr]\,
\frac{-i}{(p_1+p_2)^2+i\varepsilon}
\left[\eta_{\mu\nu}-(1-\xi)\frac{(p_1+p_2)_\mu(p_1+p_2)_\nu}{(p_1+p_2)^2+i\varepsilon}\right]\\[6pt]
&\times\bigl[\bar u^r(k_1)\,(ieQ_q\gamma^\nu)\,v^{r'}(k_2)\bigr]\,\delta_{cc'} .
\end{aligned}
\right.
\tag{7.11}
```


**Superficial Degree of Divergence**

For a connected QED graph, let $`V`$ be the number of vertices, $`I_\gamma,I_F`$ the numbers of internal photon and fermion lines, and $`E_\gamma,E_F`$ the numbers of external photon and fermion lines. Each vertex of (7.9) joins two fermion lines and one photon line and carries no derivative. Counting line ends and using (7.2) at $`d=4`$,

```math
\left.
\begin{aligned}
2V&=2I_F+E_F,\qquad V=2I_\gamma+E_\gamma,\qquad L=I_\gamma+I_F-V+1,\\[6pt]
\omega&=4L-2I_\gamma-I_F=2I_\gamma+3I_F-4V+4 .
\end{aligned}
\right.
\tag{7.12}
```

Eliminating $`I_\gamma=\tfrac12(V-E_\gamma)`$ and $`I_F=V-\tfrac12E_F`$,

```math
\left.
\boxed{\omega=4-E_\gamma-\frac32E_F .}
\right.
\tag{7.13}
```

The dependence on $`V`$ cancels because $`[e]=0`$ in four dimensions by (7.1).

**Two External Legs**

Every vertex conserves fermion number, so $`E_F`$ is even and two external legs means $`(E_F,E_\gamma)=(2,0)`$ or $`(0,2)`$. Let $`-i\Sigma(p)`$ and $`i\Pi^{\mu\nu}(p)`$ be the sums of amputated 1PI graphs with two external fermion lines and with two external photon lines, where $`p`$ is the external momentum.

**(1) Fermion Propagator**

```math
\left.
E_F=2,\qquad E_\gamma=0\qquad\Longrightarrow\qquad\omega=1 .
\right.
\tag{7.14}
```

<p align="center"><img src="figures/fermion-self-energy.svg" alt="One-loop fermion self-energy" width="322"></p>

The one-loop graph of $`-i\Sigma(p)`$ for a fermion $`f`$: the internal fermion carries $`\ell`$ along its arrow and the photon carries $`p-\ell`$.

Let $`-i\Sigma_2(p)`$ be the $`O(e^2)`$ part of $`-i\Sigma(p)`$. Starting at the vertex $`\nu`$ and reading the line against the arrow with (7.10),

```math
\left.
\begin{aligned}
-i\Sigma_2(p)
=\int\frac{d^4\ell}{(2\pi)^4}\,
&(ieQ_f\gamma^\nu)\,\frac{i(\not\ell+m_f)}{\ell^2-m_f^2+i\varepsilon}\,(ieQ_f\gamma^\mu)\\[6pt]
&\times\frac{-i}{(p-\ell)^2+i\varepsilon}\left[\eta_{\mu\nu}-(1-\xi)\frac{(p-\ell)_\mu(p-\ell)_\nu}{(p-\ell)^2+i\varepsilon}\right].
\end{aligned}
\right.
\tag{7.15}
```

For a quark, (7.15) multiplies the identity in color.

In $`d=4-\epsilon`$ dimensions, replace $`d^4\ell/(2\pi)^4`$ by $`d^d\ell/(2\pi)^d`$ as in (7.3), let the coupling carry the factor of $`\mu`$, $`e\to\mu^{\epsilon/2}e`$, as in (7.4), and continue the $`\gamma`$ matrices to $`d`$ dimensions with $`\{\gamma^\mu,\gamma^\nu\}=2\eta^{\mu\nu}I_4`$ and $`\eta^\mu{}_\mu=d`$. Collecting $`(ieQ_f)^2\,i\,(-i)=-e^2Q_f^2`$ and using $`\gamma^\nu\gamma_\nu=d\,I_4`$, $`\gamma^\nu\not a\gamma_\nu=-(d-2)\not a`$ and, for $`\ell=p-k`$, $`\not k(\not\ell+m_f)\not k=2(k\cdot p)\not k+k^2(m_f-\not p-\not k)`$, where $`k^2`$ cancels one factor $`\mathcal P_\gamma`$,

```math
\left.
\begin{aligned}
-i\Sigma_2(p)
={}&-\mu^{\epsilon}e^2Q_f^2\int\frac{d^d\ell}{(2\pi)^d}\left[
\frac{\gamma^\nu(\not\ell+m_f)\gamma_\nu}{\mathcal P_1\mathcal P_\gamma}
-(1-\xi)\,\frac{\not k(\not\ell+m_f)\not k}{\mathcal P_1\mathcal P_\gamma^2}\right]\\[6pt]
={}&-\mu^{\epsilon}e^2Q_f^2\int\frac{d^d\ell}{(2\pi)^d}\biggl\{
\frac{d\,m_f-(d-2)\not\ell}{\mathcal P_1\mathcal P_\gamma}
-(1-\xi)\biggl[\frac{m_f-\not p-\not k}{\mathcal P_1\mathcal P_\gamma}
+\frac{2(k\cdot p)\not k}{\mathcal P_1\mathcal P_\gamma^2}\biggr]\biggr\},\\[6pt]
\mathcal P_1:={}&\ell^2-m_f^2+i\varepsilon,\qquad
\mathcal P_\gamma:=k^2+i\varepsilon,\qquad
k:=p-\ell .
\end{aligned}
\right.
\tag{7.16}
```

Combine the denominators with a Feynman parameter $`x`$:

```math
\left.
\begin{aligned}
\frac{1}{\mathcal P_1\mathcal P_\gamma}
&=\int_0^1\frac{dx}{\bigl[x\mathcal P_\gamma+(1-x)\mathcal P_1\bigr]^2},\qquad
\frac{1}{\mathcal P_1\mathcal P_\gamma^2}
=\int_0^1\frac{2x\,dx}{\bigl[x\mathcal P_\gamma+(1-x)\mathcal P_1\bigr]^3},\\[6pt]
x\mathcal P_\gamma+(1-x)\mathcal P_1
&=(\ell-xp)^2-\Delta_{\Sigma,f}+i\varepsilon,\qquad
\Delta_{\Sigma,f}:=(1-x)\bigl(m_f^2-xp^2\bigr).
\end{aligned}
\right.
\tag{7.17}
```

Shift $`\ell\to\ell+xp`$, so that $`k\to(1-x)p-\ell`$, drop the terms odd in $`\ell`$, and replace $`\ell^\mu\ell^\nu`$ by $`\eta^{\mu\nu}\ell^2/d`$. The numerators of (7.16) become

```math
\left.
\begin{aligned}
d\,m_f-(d-2)\not\ell\ &\to\ d\,m_f-(d-2)x\not p,\\[4pt]
m_f-\not p-\not k\ &\to\ m_f-(2-x)\not p,\\[4pt]
2(k\cdot p)\not k\ &\to\ 2(1-x)^2p^2\not p+2(p\cdot\ell)\not\ell
\ \to\ 2(1-x)^2p^2\not p+\frac2d\,\ell^2\not p,
\end{aligned}
\right.
\tag{7.18}
```

so that

```math
\left.
\begin{aligned}
-i\Sigma_2(p)
={}&-\mu^{\epsilon}e^2Q_f^2\int_0^1dx\int\frac{d^d\ell}{(2\pi)^d}\,\biggl\{
\frac{d\,m_f-(d-2)x\not p-(1-\xi)\bigl[m_f-(2-x)\not p\bigr]}{\bigl(\ell^2-\Delta_{\Sigma,f}+i\varepsilon\bigr)^2}\\[6pt]
&-(1-\xi)\,\frac{2x\bigl[2(1-x)^2p^2+\frac2d\,\ell^2\bigr]\not p}{\bigl(\ell^2-\Delta_{\Sigma,f}+i\varepsilon\bigr)^3}\biggr\}.
\end{aligned}
\right.
\tag{7.19}
```

After Wick rotation, for $`\Delta>0`$ and continued to $`\Delta<0`$ through $`\Delta-i\varepsilon`$, with $`n=2,3`$,

```math
\left.
\begin{aligned}
\int\frac{d^d\ell}{(2\pi)^d}\,\frac{1}{(\ell^2-\Delta+i\varepsilon)^n}
&=\frac{(-1)^n\,i}{(4\pi)^{d/2}}\,\frac{\Gamma\bigl(n-\frac d2\bigr)}{\Gamma(n)}\,(\Delta-i\varepsilon)^{\frac d2-n},\\[6pt]
\int\frac{d^d\ell}{(2\pi)^d}\,\frac{\ell^2}{(\ell^2-\Delta+i\varepsilon)^n}
&=\frac{(-1)^{n-1}\,i}{(4\pi)^{d/2}}\,\frac d2\,\frac{\Gamma\bigl(n-1-\frac d2\bigr)}{\Gamma(n)}\,(\Delta-i\varepsilon)^{\frac d2-n+1}.
\end{aligned}
\right.
\tag{7.20}
```

Applying (7.20) to (7.19),

```math
\left.
\begin{aligned}
\Sigma_2(p)
={}&\frac{\mu^{\epsilon}e^2Q_f^2}{(4\pi)^{d/2}}\int_0^1dx\,\biggl\{
\Bigl[d\,m_f-(d-2)x\not p-(1-\xi)\bigl(m_f-2(1-x)\not p\bigr)\Bigr]\\[6pt]
&\times\Gamma\Bigl(2-\frac d2\Bigr)(\Delta_{\Sigma,f}-i\varepsilon)^{\frac d2-2}\\[6pt]
&+2(1-\xi)\,x(1-x)^2p^2\not p\;
\Gamma\Bigl(3-\frac d2\Bigr)(\Delta_{\Sigma,f}-i\varepsilon)^{\frac d2-3}\biggr\}.
\end{aligned}
\right.
\tag{7.21}
```

With $`d=4-\epsilon`$, $`\Gamma(\epsilon/2)=2/\epsilon-\gamma_E+O(\epsilon)`$ and $`2/\bar\epsilon`$ from (7.3),

```math
\left.
\boxed{
\begin{aligned}
\Sigma_2(p)={}&\frac{e^2Q_f^2}{16\pi^2}\int_0^1dx\,\biggl\{
\Bigl[4m_f-2x\not p-(1-\xi)\bigl(m_f-2(1-x)\not p\bigr)\Bigr]
\left[\frac2{\bar\epsilon}-\ln\frac{\Delta_{\Sigma,f}-i\varepsilon}{\mu^2}\right]\\[6pt]
&-2m_f+2x\not p+\frac{2(1-\xi)\,x(1-x)\,p^2\not p}{m_f^2-xp^2-i\varepsilon}\biggr\}+O(\epsilon)\\[6pt]
={}&\frac{e^2Q_f^2}{16\pi^2}\,\frac2\epsilon\,\bigl[(3+\xi)m_f-\xi\not p\bigr]+(\text{finite as }\epsilon\to0).
\end{aligned}
}
\right.
\tag{7.22}
```

**(2) Photon Propagator**

```math
\left.
E_\gamma=2,\qquad E_F=0\qquad\Longrightarrow\qquad\omega=2 .
\right.
\tag{7.23}
```

<p align="center"><img src="figures/photon-self-energy.svg" alt="One-loop photon self-energy" width="298"></p>

The one-loop graph of $`i\Pi^{\mu\nu}(p)`$, with a closed loop of a fermion $`f`$: the loop momenta $`\ell+p`$ and $`\ell`$ run along the arrows.

Let $`i\Pi_2^{\mu\nu}(p)`$ be the $`O(e^2)`$ part of $`i\Pi^{\mu\nu}(p)`$. Starting at the vertex $`\mu`$ and reading the loop against the arrows with (7.10),

```math
\left.
\begin{aligned}
i\Pi_2^{\mu\nu}(p)
=\sum_fN_{\mathrm c,f}\,(-1)\int\frac{d^4\ell}{(2\pi)^4}\,
\mathop{\rm tr}\nolimits \biggl[
&(ieQ_f\gamma^\mu)\,\frac{i(\not\ell+m_f)}{\ell^2-m_f^2+i\varepsilon}\\[6pt]
&\times(ieQ_f\gamma^\nu)\,\frac{i(\not\ell+\not p+m_f)}{(\ell+p)^2-m_f^2+i\varepsilon}\biggr],
\end{aligned}
\right.
\tag{7.24}
```

where the factor $`-1`$ and the Dirac trace come from the closed fermion loop, and $`N_{\mathrm c,f}`$ is the number of colors of $`f`$ ($`1`$ for a lepton, $`3`$ for a quark) from the color trace.

In $`d=4-\epsilon`$ dimensions, replace $`d^4\ell/(2\pi)^4`$ by $`d^d\ell/(2\pi)^d`$ as in (7.3) and let the coupling carry the factor of $`\mu`$, $`e\to\mu^{\epsilon/2}e`$, as in (7.4). Collecting $`(-1)(ieQ_f)^2i^2=-e^2Q_f^2`$ and using $`\mathop{\rm tr}\nolimits (\gamma^\mu\gamma^\nu)=4\eta^{\mu\nu}`$, $`\mathop{\rm tr}\nolimits (\gamma^\mu\gamma^\rho\gamma^\nu\gamma^\sigma)=4(\eta^{\mu\rho}\eta^{\nu\sigma}-\eta^{\mu\nu}\eta^{\rho\sigma}+\eta^{\mu\sigma}\eta^{\rho\nu})`$ and the vanishing of traces of an odd number of $`\gamma`$ matrices,

```math
\left.
\begin{aligned}
i\Pi_2^{\mu\nu}(p)
={}&-\mu^{\epsilon}e^2\sum_fN_{\mathrm c,f}Q_f^2\int\frac{d^d\ell}{(2\pi)^d}\,
\frac{\mathop{\rm tr}\nolimits \bigl[\gamma^\mu(\not\ell+m_f)\gamma^\nu(\not\ell+\not p+m_f)\bigr]}{\mathcal P_1\mathcal P_2}\\[6pt]
={}&-4\mu^{\epsilon}e^2\sum_fN_{\mathrm c,f}Q_f^2\int\frac{d^d\ell}{(2\pi)^d}\,\frac{1}{\mathcal P_1\mathcal P_2}\\
&\times\Bigl\{\ell^\mu(\ell+p)^\nu+\ell^\nu(\ell+p)^\mu-\eta^{\mu\nu}\bigl[\ell\cdot(\ell+p)-m_f^2\bigr]\Bigr\},\\[6pt]
\mathcal P_1:={}&\ell^2-m_f^2+i\varepsilon,\qquad
\mathcal P_2:=(\ell+p)^2-m_f^2+i\varepsilon .
\end{aligned}
\right.
\tag{7.25}
```

Combine the denominators with a Feynman parameter $`x`$:

```math
\left.
\begin{aligned}
\frac{1}{\mathcal P_1\mathcal P_2}
&=\int_0^1\frac{dx}{\bigl[x\mathcal P_2+(1-x)\mathcal P_1\bigr]^2}
=\int_0^1\frac{dx}{\bigl[(\ell+xp)^2-\Delta_f+i\varepsilon\bigr]^2},\\[6pt]
\Delta_f&:=m_f^2-x(1-x)p^2 .
\end{aligned}
\right.
\tag{7.26}
```

Shift $`\ell\to\ell-xp`$ and drop the terms odd in $`\ell`$, which integrate to zero; then replace $`\ell^\mu\ell^\nu`$ by $`\eta^{\mu\nu}\ell^2/d`$ under the integral. The numerator of (7.25) becomes

```math
\left.
\begin{aligned}
&\ell^\mu(\ell+p)^\nu+\ell^\nu(\ell+p)^\mu-\eta^{\mu\nu}\bigl[\ell\cdot(\ell+p)-m_f^2\bigr]\\[4pt]
&\quad\to\ 2\ell^\mu\ell^\nu-\eta^{\mu\nu}\ell^2-2x(1-x)p^\mu p^\nu+\eta^{\mu\nu}\bigl[x(1-x)p^2+m_f^2\bigr]\\[4pt]
&\quad\to\ 2x(1-x)\bigl(p^2\eta^{\mu\nu}-p^\mu p^\nu\bigr)+\eta^{\mu\nu}\Bigl[\frac{2-d}{d}\,\ell^2+\Delta_f\Bigr],
\end{aligned}
\right.
\tag{7.27}
```

so that

```math
\left.
\begin{aligned}
i\Pi_2^{\mu\nu}(p)
={}&-4\mu^{\epsilon}e^2\sum_fN_{\mathrm c,f}Q_f^2\int_0^1dx\int\frac{d^d\ell}{(2\pi)^d}\,
\frac{1}{\bigl(\ell^2-\Delta_f+i\varepsilon\bigr)^2}\\[6pt]
&\times\Bigl\{2x(1-x)\bigl(p^2\eta^{\mu\nu}-p^\mu p^\nu\bigr)+\eta^{\mu\nu}\Bigl[\frac{2-d}{d}\,\ell^2+\Delta_f\Bigr]\Bigr\}.
\end{aligned}
\right.
\tag{7.28}
```

After Wick rotation, for $`\Delta>0`$ and continued to $`\Delta<0`$ through $`\Delta-i\varepsilon`$,

```math
\left.
\begin{aligned}
\int\frac{d^d\ell}{(2\pi)^d}\,\frac{1}{(\ell^2-\Delta+i\varepsilon)^2}
&=\frac{i}{(4\pi)^{d/2}}\,\Gamma\Bigl(2-\frac d2\Bigr)(\Delta-i\varepsilon)^{\frac d2-2},\\[6pt]
\int\frac{d^d\ell}{(2\pi)^d}\,\frac{\ell^2}{(\ell^2-\Delta+i\varepsilon)^2}
&=-\frac{i}{(4\pi)^{d/2}}\,\frac d2\,\Gamma\Bigl(1-\frac d2\Bigr)(\Delta-i\varepsilon)^{\frac d2-1},\\[6pt]
\int\frac{d^d\ell}{(2\pi)^d}\,\frac{\frac{2-d}{d}\,\ell^2+\Delta}{(\ell^2-\Delta+i\varepsilon)^2}
&=\frac{i\,(\Delta-i\varepsilon)^{\frac d2-1}}{(4\pi)^{d/2}}\Bigl[\Bigl(\frac d2-1\Bigr)\Gamma\Bigl(1-\frac d2\Bigr)+\Gamma\Bigl(2-\frac d2\Bigr)\Bigr]=0,
\end{aligned}
\right.
\tag{7.29}
```

where the last line uses $`\Gamma(2-\tfrac d2)=(1-\tfrac d2)\Gamma(1-\tfrac d2)`$. Only the transverse term of (7.28) survives:

```math
\left.
\begin{aligned}
i\Pi_2^{\mu\nu}(p)
={}&-4\mu^{\epsilon}e^2\sum_fN_{\mathrm c,f}Q_f^2\int_0^1dx\,2x(1-x)\bigl(p^2\eta^{\mu\nu}-p^\mu p^\nu\bigr)\\[6pt]
&\times\frac{i}{(4\pi)^{d/2}}\,\Gamma\Bigl(2-\frac d2\Bigr)(\Delta_f-i\varepsilon)^{\frac d2-2} .
\end{aligned}
\right.
\tag{7.30}
```

With $`d=4-\epsilon`$, $`\Gamma(\epsilon/2)=2/\epsilon-\gamma_E+O(\epsilon)`$ and $`2/\bar\epsilon`$ from (7.3),

```math
\left.
\boxed{
\begin{aligned}
\Pi_2^{\mu\nu}(p)&=\bigl(p^2\eta^{\mu\nu}-p^\mu p^\nu\bigr)\,\Pi_2(p^2),\\[6pt]
\Pi_2(p^2)&=-\frac{e^2}{2\pi^2}\sum_fN_{\mathrm c,f}Q_f^2\int_0^1dx\,x(1-x)\left[\frac2{\bar\epsilon}-\ln\frac{\Delta_f-i\varepsilon}{\mu^2}\right]+O(\epsilon).
\end{aligned}
}
\right.
\tag{7.31}
```

**Three External Legs**

Three external legs means $`(E_F,E_\gamma)=(2,1)`$ or $`(0,3)`$. Let $`ieQ_f\Gamma^\mu(p',p)`$ be the sum of amputated 1PI graphs with an incoming fermion of momentum $`p`$, an outgoing fermion of momentum $`p':=p+q`$, and an incoming photon of momentum $`q`$ and index $`\mu`$, so that $`\Gamma^\mu`$ is the proper vertex of (7.8). Write $`\Gamma^\mu=\gamma^\mu+\Lambda^\mu`$.

**(1) Vertex**

```math
\left.
E_F=2,\qquad E_\gamma=1\qquad\Longrightarrow\qquad\omega=0 .
\right.
\tag{7.32}
```

<p align="center"><img src="figures/vertex.svg" alt="One-loop QED vertex" width="370"></p>

The one-loop graph of $`ieQ_f\Lambda^\mu(p',p)`$ for a fermion $`f`$: the internal fermions carry $`\ell`$ and $`\ell+q`$ along their arrows and the internal photon carries $`p-\ell`$.

Let $`\Lambda_2^\mu(p',p)`$ be the $`O(e^2)`$ part of $`\Lambda^\mu(p',p)`$. Starting at the vertex $`\nu`$ and reading the line against the arrow with (7.10),

```math
\left.
\begin{aligned}
ieQ_f\Lambda_2^\mu(p',p)
=\int\frac{d^4\ell}{(2\pi)^4}\,
&(ieQ_f\gamma^\nu)\,\frac{i(\not\ell+\not q+m_f)}{(\ell+q)^2-m_f^2+i\varepsilon}\,(ieQ_f\gamma^\mu)\\[6pt]
&\times\frac{i(\not\ell+m_f)}{\ell^2-m_f^2+i\varepsilon}\,(ieQ_f\gamma^\rho)\\[6pt]
&\times\frac{-i}{(p-\ell)^2+i\varepsilon}\left[\eta_{\nu\rho}-(1-\xi)\frac{(p-\ell)_\nu(p-\ell)_\rho}{(p-\ell)^2+i\varepsilon}\right].
\end{aligned}
\right.
\tag{7.33}
```

For a quark, (7.33) multiplies the identity in color.

In $`d=4-\epsilon`$ dimensions, continue as for (7.16), with the stripped coupling $`ieQ_f`$ also carrying $`\mu^{\epsilon/2}`$. Collecting $`(ieQ_f)^3\,i\cdot i\cdot(-i)=(ieQ_f)(-ie^2Q_f^2)`$,

```math
\left.
\begin{aligned}
\Lambda_2^\mu(p',p)
={}&-i\mu^{\epsilon}e^2Q_f^2\int\frac{d^d\ell}{(2\pi)^d}\biggl[
\frac{\gamma^\nu(\not\ell'+m_f)\gamma^\mu(\not\ell+m_f)\gamma_\nu}{\mathcal P_1\mathcal P_1'\mathcal P_\gamma}\\[6pt]
&-(1-\xi)\,\frac{\not k(\not\ell'+m_f)\gamma^\mu(\not\ell+m_f)\not k}{\mathcal P_1\mathcal P_1'\mathcal P_\gamma^2}\biggr],\\[6pt]
\ell':={}&\ell+q,\qquad k:=p-\ell,\\[6pt]
\mathcal P_1:={}&\ell^2-m_f^2+i\varepsilon,\qquad
\mathcal P_1':=\ell'^2-m_f^2+i\varepsilon,\qquad
\mathcal P_\gamma:=k^2+i\varepsilon .
\end{aligned}
\right.
\tag{7.34}
```

Combine the denominators with Feynman parameters $`x,y,z`$:

```math
\left.
\begin{aligned}
\frac{1}{\mathcal P_1\mathcal P_1'\mathcal P_\gamma}
&=2\int dF\,\frac{1}{\bigl[x\mathcal P_1+y\mathcal P_1'+z\mathcal P_\gamma\bigr]^3},\\[6pt]
\frac{1}{\mathcal P_1\mathcal P_1'\mathcal P_\gamma^2}
&=6\int dF\,\frac{z}{\bigl[x\mathcal P_1+y\mathcal P_1'+z\mathcal P_\gamma\bigr]^4},\\[6pt]
\int dF&:=\int_0^1dx\int_0^1dy\int_0^1dz\;\delta(x+y+z-1),\\[6pt]
x\mathcal P_1+y\mathcal P_1'+z\mathcal P_\gamma
&=(\ell+yq-zp)^2-\Delta_{V,f}+i\varepsilon,\\[6pt]
\Delta_{V,f}&:=(1-z)m_f^2-xz\,p^2-yz\,p'^2-xy\,q^2 .
\end{aligned}
\right.
\tag{7.35}
```

Shift $`\ell\to\ell+A`$, so that $`\ell'\to\ell+A'`$ and $`k\to K-\ell`$, with $`A:=(1-x)p-yp'`$, $`A':=(1-y)p'-xp`$ and $`K:=xp+yp'`$. Drop the terms odd in $`\ell`$ and replace $`\ell^\alpha\ell^\beta`$ by $`\eta^{\alpha\beta}\ell^2/d`$; with $`\not\ell\not\ell=\ell^2`$, the numerators of (7.34) become

```math
\left.
\begin{aligned}
\gamma^\nu(\not\ell'+m_f)\gamma^\mu(\not\ell+m_f)\gamma_\nu\ &\to\ \frac{(d-2)^2}{d}\,\ell^2\gamma^\mu+N^\mu,\\[4pt]
\not k(\not\ell'+m_f)\gamma^\mu(\not\ell+m_f)\not k\ &\to\ (\ell^2)^2\gamma^\mu+\ell^2N_2^\mu+N_0^\mu,\\[10pt]
N^\mu&:=\gamma^\nu(\not A'+m_f)\gamma^\mu(\not A+m_f)\gamma_\nu,\\[6pt]
N_0^\mu&:=\not K(\not A'+m_f)\gamma^\mu(\not A+m_f)\not K,\\[6pt]
N_2^\mu&:=-\gamma^\mu(\not A+m_f)\not K-\not K(\not A'+m_f)\gamma^\mu\\
&\quad\ +\frac1d\Bigl[N^\mu-(d-2)\not K\gamma^\mu\not K\\
&\qquad\quad-\gamma^\nu(\not A'+m_f)\gamma^\mu\gamma_\nu\not K-\not K\gamma^\nu\gamma^\mu(\not A+m_f)\gamma_\nu\Bigr],
\end{aligned}
\right.
\tag{7.36}
```

so that

```math
\left.
\begin{aligned}
\Lambda_2^\mu(p',p)
={}&-i\mu^{\epsilon}e^2Q_f^2\int dF\int\frac{d^d\ell}{(2\pi)^d}\,\biggl\{
\frac{2\bigl[\frac{(d-2)^2}{d}\,\ell^2\gamma^\mu+N^\mu\bigr]}{\bigl(\ell^2-\Delta_{V,f}+i\varepsilon\bigr)^3}\\[6pt]
&-6(1-\xi)\,z\,\frac{(\ell^2)^2\gamma^\mu+\ell^2N_2^\mu+N_0^\mu}{\bigl(\ell^2-\Delta_{V,f}+i\varepsilon\bigr)^4}\biggr\}.
\end{aligned}
\right.
\tag{7.37}
```

After Wick rotation, for $`\Delta>0`$ and continued to $`\Delta<0`$ through $`\Delta-i\varepsilon`$, the integrals (7.20) generalize to

```math
\left.
\int\frac{d^d\ell}{(2\pi)^d}\,\frac{(\ell^2)^a}{(\ell^2-\Delta+i\varepsilon)^n}
=\frac{(-1)^{n+a}\,i}{(4\pi)^{d/2}}\,
\frac{\Gamma\bigl(a+\frac d2\bigr)\,\Gamma\bigl(n-a-\frac d2\bigr)}{\Gamma\bigl(\frac d2\bigr)\,\Gamma(n)}\,
(\Delta-i\varepsilon)^{\frac d2+a-n}.
\right.
\tag{7.38}
```

Applying (7.38) to (7.37),

```math
\left.
\begin{aligned}
\Lambda_2^\mu(p',p)
={}&\frac{\mu^{\epsilon}e^2Q_f^2}{(4\pi)^{d/2}}\int dF\,\biggl\{
\Bigl[\frac{(d-2)^2}{2}-(1-\xi)\,z\,\frac{d(d+2)}{4}\Bigr]
\Gamma\Bigl(2-\frac d2\Bigr)(\Delta_{V,f}-i\varepsilon)^{\frac d2-2}\,\gamma^\mu\\[6pt]
&-\Gamma\Bigl(3-\frac d2\Bigr)(\Delta_{V,f}-i\varepsilon)^{\frac d2-3}
\Bigl[N^\mu-(1-\xi)\,z\,\frac d2\,N_2^\mu\Bigr]\\[6pt]
&-(1-\xi)\,z\,\Gamma\Bigl(4-\frac d2\Bigr)(\Delta_{V,f}-i\varepsilon)^{\frac d2-4}\,N_0^\mu\biggr\}.
\end{aligned}
\right.
\tag{7.39}
```

With $`d=4-\epsilon`$, $`\Gamma(\epsilon/2)=2/\epsilon-\gamma_E+O(\epsilon)`$, $`2/\bar\epsilon`$ from (7.3), and $`N^\mu`$, $`N_2^\mu`$ in the finite terms taken at $`d=4`$,

```math
\left.
\boxed{
\begin{aligned}
\Lambda_2^\mu(p',p)={}&\frac{e^2Q_f^2}{16\pi^2}\int dF\,\biggl\{
\bigl[2-6(1-\xi)z\bigr]\gamma^\mu\left[\frac2{\bar\epsilon}-\ln\frac{\Delta_{V,f}-i\varepsilon}{\mu^2}\right]
-\bigl[4-5(1-\xi)z\bigr]\gamma^\mu\\[6pt]
&-\frac{N^\mu-2(1-\xi)z\,N_2^\mu}{\Delta_{V,f}-i\varepsilon}
-\frac{(1-\xi)z\,N_0^\mu}{(\Delta_{V,f}-i\varepsilon)^2}\biggr\}+O(\epsilon)\\[6pt]
={}&\frac{e^2Q_f^2}{16\pi^2}\,\frac2\epsilon\,\xi\gamma^\mu+(\text{finite as }\epsilon\to0),\\[10pt]
N^\mu\big|_{d=4}={}&-2\not A\gamma^\mu\not A'+4m_f(A+A')^\mu-2m_f^2\gamma^\mu,\\[6pt]
N_2^\mu\big|_{d=4}={}&\frac14N^\mu\big|_{d=4}-\gamma^\mu\not A\not K-\not K\not A'\gamma^\mu-\frac12\not K\gamma^\mu\not K-(A+A')^\mu\not K-m_fK^\mu .
\end{aligned}
}
\right.
\tag{7.40}
```

The parameter integrals converge unless $`p^2=p'^2=m_f^2`$; in that on-shell case they diverge logarithmically at $`z\to1`$. With (7.22), the results satisfy $`q_\mu\Lambda_2^\mu(p+q,p)=\Sigma_2(p)-\Sigma_2(p+q)`$, as required by (7.8).

**(2) Three Photons**

```math
\left.
E_\gamma=3,\qquad E_F=0\qquad\Longrightarrow\qquad\omega=1 .
\right.
\tag{7.41}
```

The graphs with the two orientations of the fermion loop cancel (Furry's theorem), so the sum of 1PI graphs with three external photons vanishes.

<br><br>





































<a id="qft-ch8"></a>
## 8. Multi-Loop Renormalization

**Subdivergences and the Forest Formula**

Beyond one loop, divergent subgraphs may be nested, disjoint, or overlapping. In massive BPHZ renormalization, with subtraction points chosen to avoid infrared singularities, let $`\mathcal I_{\mathcal G}`$ denote the integrand of a 1PI graph $`\mathcal G`$ and $`t_\gamma`$ the Taylor subtraction in the external momenta of a divergent 1PI subgraph $`\gamma`$, through its superficial degree. Then

```math
\left.
\boxed{R\mathcal I_{\mathcal G}
=\sum_{F\in\mathfrak F(\mathcal G)}
\left[\prod_{\gamma\in F}(-t_\gamma)\right]\mathcal I_{\mathcal G}.}
\right.
\tag{8.1}
```

A forest $`F`$ contains only mutually nested or disjoint subtraction subgraphs. The sum includes the empty forest and, if divergent, the full graph. Nested subtractions act from the innermost subgraph outwards. Lower-order counterterm insertions are part of the higher-loop calculation.

**Pole Structure and Two-Loop Running**

For a multiplicative renormalization constant in a mass-independent minimal-subtraction scheme with a single coupling,

```math
\left.
Z=1+\sum_{L=1}^{\infty}
\left(\frac{g_s^2}{16\pi^2}\right)^L
\sum_{k=1}^{L}\frac{z_{Lk}}{\epsilon^k}.
\right.
\tag{8.2}
```

Renormalization-group consistency relates higher poles to lower-order data. For QCD,

```math
\left.
\begin{aligned}
\beta_{g_s}&=-\frac{\beta_0g_s^3}{16\pi^2}
-\frac{\beta_1g_s^5}{(16\pi^2)^2}+O(g_s^7),\\
\beta_0&=11-\frac23n_f,\qquad
\beta_1=102-\frac{38}{3}n_f.
\end{aligned}
\right.
\tag{8.3}
```

These first two coefficients are unchanged by analytic, scale-independent coupling redefinitions within the usual mass-independent schemes. Higher coefficients depend on the scheme.

**Integral Families and Integration by Parts**

For $`L`$ loop momenta $`k_\ell`$ and denominator factors $`D_j=q_j^2-m_j^2+i\varepsilon`$, where $`q_j`$ is a linear combination of loop and external momenta, define

```math
\left.
\begin{aligned}
I_{\nu_1\cdots\nu_N}
&:=\int\prod_{\ell=1}^{L}\frac{d^dk_\ell}{(2\pi)^d}
\prod_{j=1}^{N}D_j^{-\nu_j},\\
0&=\int\prod_{\ell=1}^{L}\frac{d^dk_\ell}{(2\pi)^d}
\frac{\partial}{\partial k_r^\mu}
\left(v^\mu\prod_{j=1}^{N}D_j^{-\nu_j}\right).
\end{aligned}
\right.
\tag{8.4}
```

Here $`v^\mu`$ is a loop or external momentum. Integration-by-parts identities hold by analytic continuation in dimensional regularization from a region where the surface terms vanish. Numerator scalar products can be included through zero or negative powers in a completed integral family.

**Master Integrals and Differential Equations**

After algebraic reduction, a chosen family can be expressed in a finite basis of master integrals $`M_r`$. For a kinematic invariant $`s`$,

```math
\left.
I_{\nu_1\cdots\nu_N}=\sum_r c_r(d,\{p\cdot p\},\{m^2\})M_r,
\qquad
\frac{\partial M_r}{\partial s}=\sum_t A_{rt}(d,\{p\cdot p\},\{m^2\})M_t.
\right.
\tag{8.5}
```

Boundary values and the Feynman analytic continuation are required to solve these equations. Ultraviolet and infrared poles must be distinguished before subtraction; a scaleless integral vanishes in dimensional regularization but may conceal a cancellation between ultraviolet and infrared poles. Higher-loop chiral calculations also require an explicit $`d`$-dimensional $`\gamma^5`$ prescription; the four-dimensional Weyl matrices alone do not supply one.

<br><br>

<a id="qft-ch9"></a>
## 9. Cosmology

