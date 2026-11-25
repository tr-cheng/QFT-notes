# QFT

> Read in parts: [1](QFT-en-part-01.md) · [2](QFT-en-part-02.md) · [3](QFT-en-part-03.md) · [4](QFT-en-part-04.md) · [5](QFT-en-part-05.md)


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
  - [2.1 Pictures of Time Evolution](#pictures-of-time-evolution)
    - [Schrödinger Picture](#schrodinger-picture)
    - [Heisenberg Picture](#heisenberg-picture)
  - [2.2 Canonical Quantization](#canonical-quantization)
    - [Quantization of the Free Real Scalar Field](#free-real-scalar-field-quantization)
  - [2.3 Quantization with Dirac Brackets](#quantization-with-dirac-brackets)
    - [Quantization of the Complex Scalar Field](#complex-scalar-field-quantization)
    - [Quantization of the Dirac Field](#dirac-field-quantization)
    - [Quantization of the Proca Field](#proca-field-quantization)
  - [2.4 Gupta–Bleuler Quantization](#gupta-bleuler-quantization)
  - [2.5 Symmetry](#symmetry)
    - [Ward Identity](#ward-identity)
- [3. Path Integrals](#qft-ch3)
  - [3.1 Path Integrals in Quantum Mechanics](#path-integrals-in-quantum-mechanics)
  - [3.2 Path Integrals in Quantum Field Theory](#path-integrals-in-field-theory)
  - [3.3 $`\phi^3`$ Theory](#phi-cubed-theory)
  - [3.4 Path Integrals for Fermion Fields](#path-integrals-for-fermion-fields)
    - [Grassmann Algebra](#grassmann-algebra)
    - [Calculus on the Grassmann Algebra](#grassmann-calculus)
  - [3.5 Symmetry in Path Integrals](#symmetry-in-path-integrals)
  - [3.6 Scattering Theory in Path Integrals](#scattering-theory-in-path-integrals)
- [4. Scattering Theory](#qft-ch4)
  - [4.1 Interaction Picture](#interaction-picture)
  - [4.2 The S-Matrix and Wick's Theorem](#s-matrix-and-wick-theorem)
  - [4.3 Feynman Diagrams and Feynman Rules](#feynman-diagrams)
  - [4.4 Correlation Functions](#correlation-functions)
    - [Perturbative Vacuum Correlation Functions](#perturbative-correlation-functions)
    - [Nonperturbative Vacuum Correlation Functions](#nonperturbative-correlation-functions)
  - [4.5 LSZ Reduction Formula](#lsz-reduction)
  - [4.6 Cross Sections and Decay Rates](#cross-sections-and-decay-rates)
- [5. The Standard Model](#qft-ch5)
  - [5.1 Yang–Mills Theory](#yang-mills)
    - [Lie Group](#lie-group)
    - [Local Gauge Symmetry](#local-gauge-symmetry)
  - [5.2 Fermions and Bosons in the Standard Model](#sm-fermions)
    - [General Higgs Lagrangian](#higgs-lagrangian)
    - [Fermions and the Higgs Boson in the Standard Model](#sm-fermions-and-higgs)
    - [Field Redefinitions and Flavor](#field-redefinitions-and-flavor)
  - [5.3 $`W^\pm`$, $`Z^0`$, $`\gamma`$: Electroweak Theory](#electroweak-theory)
    - [Gauge Symmetry $`SU(2)_L\times U(1)_Y`$ ](#electroweak-gauge-symmetry)
    - [Interaction](#electroweak-interaction)
  - [5.4 Gluon $`g`$: Quantum Chromodynamics](#qcd)
    - [Gauge Symmetry $`SU(3)_c`$ ](#qcd-gauge-symmetry)
- [6. New Physics Beyond the Standard Model](#qft-ch6)
  - [6.1 Seesaw Mechanism](#seesaw-mechanism)
    - [Type-I Seesaw](#type-i-seesaw)
    - [Type-II Seesaw](#type-ii-seesaw)
    - [Type-III Seesaw](#type-iii-seesaw)
    - [Leptogenesis](#leptogenesis)
  - [6.2 $`U(1)_{L_\mu-L_\tau}`$ Gauge Symmetry](#lmu-ltau-gauge-symmetry)
- [7. Renormalization](#qft-ch7)
  - [7.1 Forest Formula](#forest-formula)
    - [Basic Definitions of Graphs](#graph-definitions)
    - [$`\mathcal{L}_{CT}`$ and R-Operation Recursion Formula](#r-operation-recursion)
  - [7.2 QED Renormalization](#qed-renormalization)
- [8. Cosmology](#qft-ch8)
  - [8.1 Geometry of the Universe](#geometry-of-the-universe)
    - [Experimental Facts](#cosmology-experimental-facts)
    - [FLRW Metric](#flrw-metric)
  - [8.2 Evolution of the Universe](#evolution-of-the-universe)
    - [Dynamics](#cosmology-dynamics)
    - [Dark Matter](#dark-matter)
    - [Dark Energy](#dark-energy)
    - [Cosmic Evolution](#cosmic-evolution)
  - [8.3 Boltzmann Equation](#boltzmann-equation)

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

For comparison with the scalar Feynman propagator defined in (4.12), the Feynman prescription for the same normalization $`\mathcal KG_F=\delta^{(4)}`$ gives

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
L:\mathbb R^n\times\mathbb R^n\times\mathbb R&\to\mathbb R,\\
(x,y,t)&\mapsto L(x,y,t).
\end{aligned}
\right.
\tag{1.2}
```

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

- **Solutions**: paths $`\bar C`$ at which $`S`$ is stationary under variations with fixed endpoints,

```math
\left.
\frac{d}{ds}S[\bar C+s\eta]\Big|_{s=0}=0,
\right.
\tag{1.4}
```

for every smooth $`\eta:[t_0,t_f]\to\mathbb R^n`$ with $`\eta(t_0)=\eta(t_f)=0`$.

**Euler–Lagrange Equations**

Write $`\frac{\partial L}{\partial x_a}\big|_C`$ and $`\frac{\partial L}{\partial y_a}\big|_C`$ for the partial derivatives of $`L`$ evaluated at $`\bigl(C(t),\dot C(t),t\bigr)`$.

The correspondence with the usual notation $`q_a,\dot q_a`$ is

```math
\left.
\begin{aligned}
\frac{\partial L}{\partial \dot q_a}&=\frac{\partial L}{\partial y_a}\Big|_C,\\
\frac{\partial L}{\partial q_a}&=\frac{\partial L}{\partial x_a}\Big|_C.
\end{aligned}
\right.
\tag{1.5}
```

Then

```math
\left.
\begin{aligned}
\frac{d}{ds}S[C+s\eta]\Big|_{s=0}
&=\int_{t_0}^{t_f}dt\sum_{a=1}^n\Bigl(\frac{\partial L}{\partial x_a}\Big|_C\,\eta_a+\frac{\partial L}{\partial y_a}\Big|_C\,\dot\eta_a\Bigr)\\
&=\int_{t_0}^{t_f}dt\sum_{a=1}^n\biggl[\frac{\partial L}{\partial x_a}\Big|_C-\frac{d}{dt}\Bigl(\frac{\partial L}{\partial y_a}\Big|_C\Bigr)\biggr]\eta_a\\
&\quad+\biggl[\sum_{a=1}^n\frac{\partial L}{\partial y_a}\Big|_C\,\eta_a\biggr]_{t_0}^{t_f}.
\end{aligned}
\right.
\tag{1.6}
```

The boundary term vanishes because $`\eta(t_0)=\eta(t_f)=0`$. 

Since $`\eta`$ is arbitrary, the solutions are the paths $`\bar C`$ with

```math
\left.
\boxed{\frac{d}{dt}\Bigl(\frac{\partial L}{\partial y_a}\Big|_{\bar C}\Bigr)-\frac{\partial L}{\partial x_a}\Big|_{\bar C}=0,\qquad a=1,\ldots,n.}
\right.
\tag{1.7}
```







<br><br>

<a id="lagrangian-symmetry"></a>
#### Symmetry Transformations and Noether's Theorem

**Transformations**

- **Internal transformation**: 
a one-parameter family of diffeomorphisms $`\phi_\lambda:\mathrm{Conf}\to\mathrm{Conf}`$, $`\lambda\in\mathbb R`$, with $`(\lambda,q)\mapsto\phi_\lambda(q)`$ smooth and $`\phi_0=\mathrm{id}`$, acting on paths pointwise,

```math
\left.
\begin{aligned}
\Phi:\mathbb R\times\{\text{paths}\}&\to\{\text{paths}\},\\
(\lambda,C)&\mapsto\Phi_\lambda C:=\phi_\lambda\circ C,
\end{aligned}
\right.
\tag{1.8}
```

The tangent vectors, or velocities, are related by

```math
\left.
\frac{d}{dt}(\Phi_\lambda C)_a(t)=\sum_{b=1}^n\frac{\partial(\phi_\lambda)_a}{\partial q_b}\bigl(C(t)\bigr)\,\dot C_b(t),
\right.
\tag{1.9}
```

where $`(\phi_\lambda)_a(q)`$ is the $`a`$-th coordinate of $`\phi_\lambda(q)`$.

**Proof.** The main ingredient is the theorem that, under a smooth map, the image of the tangent vector of a curve is the tangent vector of the image curve.

Write $`\frac{\partial\phi_\lambda}{\partial q}(q)`$ for the Jacobian matrix with entries $`\frac{\partial(\phi_\lambda)_a}{\partial q_b}(q)`$, so that the velocity of $`\Phi_\lambda C`$ is
```math
\frac{d}{dt}(\Phi_\lambda C)(t)=\frac{\partial\phi_\lambda}{\partial q}\bigl(C(t)\bigr)\,\dot C(t)
```

- **Time translation**: the shift of paths in time,

```math
\left.
\begin{aligned}
\Theta:\mathbb R\times\{\text{paths}\}&\to\{\text{paths}\},\\
(\tau,C)&\mapsto\Theta_\tau C:=C(\cdot-\tau),
\end{aligned}
\right.
\tag{1.10}
```

so that $`\Theta_\tau C:[t_0+\tau,t_f+\tau]\to\mathrm{Conf}`$, $`t\mapsto C(t-\tau)`$, with velocity

```math
\left.
\frac{d}{dt}(\Theta_\tau C)(t)=\dot C(t-\tau).
\right.
\tag{1.11}
```

**Symmetry Transformations**

- **Symmetry transformation**: an internal transformation $`\Phi`$, respectively a time translation $`\Theta`$, under which the action of every path is invariant,

```math
\left.
\boxed{
\begin{aligned}
S[\Phi_\lambda C]&=S[C]\quad\text{for every path }C\text{ and every }\lambda\in\mathbb R,\\
S[\Theta_\tau C]&=S[C]\quad\text{for every path }C\text{ and every }\tau\in\mathbb R.
\end{aligned}}
\right.
\tag{1.12}
```


Substituting the transformed paths into the action, and shifting $`t\to t+\tau`$ in the second case,

```math
\left.
\begin{aligned}
S[\Phi_\lambda C]&=\int_{t_0}^{t_f}dt\,L\Bigl(\phi_\lambda\bigl(C(t)\bigr),\ \frac{\partial\phi_\lambda}{\partial q}\bigl(C(t)\bigr)\,\dot C(t),\ t\Bigr),\\
S[\Theta_\tau C]&=\int_{t_0+\tau}^{t_f+\tau}dt\,L\bigl(C(t-\tau),\dot C(t-\tau),t\bigr)=\int_{t_0}^{t_f}dt\,L\bigl(C(t),\dot C(t),t+\tau\bigr).
\end{aligned}
\right.
\tag{1.13}
```

Hence symmetry transformations have the following equivalent definition:

$`\Phi`$, respectively $`\Theta`$, is a symmetry transformation if and only if, for all $`(x,y,t)\in\mathrm{Conf}\times\mathbb R^n\times\mathbb R`$ and all $`\lambda`$, respectively all $`\tau`$,

```math
\left.
\boxed{
\begin{aligned}
L\Bigl(\phi_\lambda(x),\ \frac{\partial\phi_\lambda}{\partial q}(x)\,y,\ t\Bigr)&=L(x,y,t)
\end{aligned}}
\right.
\tag{1.14}
```

```math
\left.
\boxed{
L(x,y,t+\tau)=L(x,y,t)\quad(\forall\,\tau\in\mathbb R)
\quad\Longleftrightarrow\quad
\frac{\partial L}{\partial t}(x,y,t)=0.
}
\right.
\tag{1.15}
```


**Conserved Quantities**

- **Conserved quantity**: a smooth function

```math
\left.
\begin{aligned}
\mathcal Q:\mathrm{Conf}\times\mathbb R^n\times\mathbb R&\to\mathbb R,\\
(x,y,t)&\mapsto\mathcal Q(x,y,t),
\end{aligned}
\right.
\tag{1.16}
```

such that $`\mathcal Q\bigl(\bar C(t),\dot{\bar C}(t),t\bigr)`$ is independent of $`t`$ for every solution $`\bar C`$.

**Noether's Theorem**

**(A) Time Translation**

If $`\Theta`$ is a symmetry transformation, i.e. $`\partial L/\partial t=0`$ on $`\mathrm{Conf}\times\mathbb R^n\times\mathbb R`$, then the energy

```math
\left.
\boxed{E(x,y,t):=\sum_{a=1}^n\frac{\partial L}{\partial y_a}(x,y,t)\,y_a-L(x,y,t)}
\right.
\tag{1.17}
```

is a conserved quantity.

**(B) Internal Transformation**

If $`\Phi`$ is a symmetry transformation, then, with the generator

```math
\left.
\begin{aligned}
X:\mathrm{Conf}&\to\mathbb R^n,\\
q&\mapsto\frac{\partial\phi_\lambda(q)}{\partial\lambda}\Big|_{\lambda=0},
\end{aligned}
\right.
\tag{1.18}
```

The generator gives the form of the infinitesimal transformation at $`\lambda=0`$: $`\phi_\lambda(q)=q+\lambda\,X(q)+O(\lambda^2),`$ i.e. the coordinates transform as $`q_a\mapsto q_a+\lambda X_a(q)`$.

Correspondingly, the velocity transforms as $`y\mapsto y+\lambda\,\frac{\partial X}{\partial q}(q)\,y+O(\lambda^2),`$ i.e. $`y_a\mapsto y_a+\lambda\sum_b\frac{\partial X_a}{\partial q_b}(q)\,y_b`$.

the function

```math
\left.
\boxed{\mathcal Q(x,y,t):=\sum_{a=1}^n\frac{\partial L}{\partial y_a}(x,y,t)\,X_a(x)}
\right.
\tag{1.19}
```

is a conserved quantity.

**Proof**

(A) Let $`\bar C`$ be a solution. Write $`L|_{\bar C}:=L\bigl(\bar C(t),\dot{\bar C}(t),t\bigr)`$.

 By the chain rule and the Euler–Lagrange equations,

```math
\left.
\frac{d}{dt}E\bigl(\bar C(t),\dot{\bar C}(t),t\bigr)
=\frac{d}{dt}\Bigl(\sum_{a=1}^n\frac{\partial L}{\partial y_a}\Big|_{\bar C}\,\dot{\bar C}_a(t)-L\big|_{\bar C}\Bigr)
=-\frac{\partial L}{\partial t}\Big|_{\bar C}
\right.
\tag{1.20}
```

along every solution, which vanishes if $`\partial L/\partial t=0`$.

(B) Differentiating the first symmetry condition with respect to $`\lambda`$ at $`\lambda=0`$,  gives for all $`(x,y,t)\in\mathrm{Conf}\times\mathbb R^n\times\mathbb R`$

```math
\left.
\sum_{a=1}^n\Bigl(\frac{\partial L}{\partial x_a}\,X_a(x)
+\frac{\partial L}{\partial y_a}\sum_{b=1}^n\frac{\partial X_a}{\partial q_b}(x)\,y_b\Bigr)=0,
\right.
\tag{1.21}
```

with the partial derivatives of $`L`$ evaluated at $`(x,y,t)`$. 

For a solution $`\bar C`$, the chain rule and the Euler–Lagrange equations give

```math
\left.
\frac{d}{dt}\mathcal Q\bigl(\bar C(t),\dot{\bar C}(t),t\bigr)
=\sum_{a=1}^n\Bigl(\frac{\partial L}{\partial x_a}\Big|_{\bar C}\,X_a\bigl(\bar C(t)\bigr)
+\frac{\partial L}{\partial y_a}\Big|_{\bar C}\sum_{b=1}^n\frac{\partial X_a}{\partial q_b}\bigl(\bar C(t)\bigr)\,\dot{\bar C}_b(t)\Bigr),
\right.
\tag{1.22}
```

which is the identity above evaluated at $`\bigl(\bar C(t),\dot{\bar C}(t),t\bigr)`$, hence zero. $`\square`$


**Momentum**

Fix $`b\in\{1,\ldots,n\}`$ and translate the $`b`$-th coordinate,

```math
\left.
\bigl(\phi_\lambda(q)\bigr)_a=q_a+\lambda\,\delta_{ab}.
\right.
\tag{1.23}
```

The Jacobian $`\partial\phi_\lambda/\partial q`$ is the identity, so the velocity is unchanged, and the symmetry condition reads $`L(\phi_\lambda(x),y,t)=L(x,y,t)`$ for all $`\lambda`$, i.e. $`\partial L/\partial x_b=0`$.

Generator: $`X_a(q)=\delta_{ab}`$.

Conserved quantity:

```math
\left.
\mathcal Q(x,y,t)=\sum_{a=1}^n\frac{\partial L}{\partial y_a}(x,y,t)\,\delta_{ab}=\frac{\partial L}{\partial y_b}(x,y,t),
\right.
\tag{1.24}
```

the momentum $`p_b`$ conjugate to $`q_b`$.



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
\tag{1.25}
```

- **Solutions**: smooth curves $`C:I\to M`$, with $`I\subset\mathbb R`$ an open interval, such that

```math
\left.
\boxed{\dot C_A(t)=F_A\bigl(C(t)\bigr),\qquad A=1,\ldots,N.}
\right.
\tag{1.26}
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
\tag{1.27}
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
\tag{1.28}
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
\tag{1.29}
```

- **Dynamical structure**:
  - the Poisson bracket $`\{\ ,\ \}_{\mathrm{PB}}`$ of (1.87);
  - the Hamiltonian, a smooth function

```math
\left.
\begin{aligned}
H:M&\to\mathbb R,\\
z&\mapsto H(z),
\end{aligned}
\right.
\tag{1.30}
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
\tag{1.31}
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
\tag{1.32}
```

where $`Q_a(z),P_a(z)`$ are the coordinates of $`\phi(z)`$, and $`\phi_*`$ is the pushforward of (1.64), with $`(\phi_*f)(\phi(z))=f(z)`$.

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
\tag{1.33}
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
\tag{1.34}
```

The brackets $`\{z_A,z_B\}_{\mathrm{PB}}`$ are constants, and $`f=z_A`$, $`g=z_B`$ pick out a single term, so (i) holds if and only if $`\{Z_A,Z_B\}_{\mathrm{PB}}=\{z_A,z_B\}_{\mathrm{PB}}`$. By (1.87), (i) is equivalent to

```math
\left.
\boxed{
\{Q_a,Q_b\}_{\mathrm{PB}}=\{P_a,P_b\}_{\mathrm{PB}}=0,\qquad
\{Q_a,P_b\}_{\mathrm{PB}}=\delta_{ab}.}
\right.
\tag{1.35}
```

A symmetry transformation maps solutions to solutions. Let $`C`$ be a solution and $`C':=\phi\circ C`$. Applying (1.31) to $`f\circ\phi`$, then (ii) and (i),

```math
\left.
\begin{aligned}
\frac{d}{dt}f\bigl(C'(t)\bigr)
&=\{f\circ\phi,\,H\}_{\mathrm{PB}}\bigl(C(t)\bigr)\\
&=\{f\circ\phi,\,H\circ\phi\}_{\mathrm{PB}}\bigl(C(t)\bigr)
=\{f,H\}_{\mathrm{PB}}\bigl(C'(t)\bigr)
\end{aligned}
\right.
\tag{1.36}
```

for every $`f`$, so $`C'`$ is a solution by (1.31).

**Conserved Quantities**

- **Conserved quantity**: an observable $`f`$ such that $`f\bigl(C(t)\bigr)`$ is independent of $`t`$ for every solution $`C`$.

(1.31) is (1.26) with $`N=2n`$ and $`F_A=\{z_A,H\}_{\mathrm{PB}}`$. Since a solution passes through each point of $`M`$, (1.31) shows that $`f`$ is a conserved quantity if and only if

```math
\left.
\boxed{\{f,H\}_{\mathrm{PB}}=0.}
\right.
\tag{1.37}
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
\tag{1.38}
```

so that $`\phi_\lambda`$ is the flow of $`X`$. If $`M`$ is simply connected, there is a smooth function $`G:M\to\mathbb R`$, unique up to an additive constant, with

```math
\left.
X_A=\{z_A,G\}_{\mathrm{PB}},\qquad A=1,\ldots,2n,
\right.
\tag{1.39}
```

and

```math
\left.
\boxed{\{G,H\}_{\mathrm{PB}}=0,}
\right.
\tag{1.40}
```

so $`G`$ is a conserved quantity.

**Proof**

Write $`\omega_{AB}:=\{z_A,z_B\}_{\mathrm{PB}}`$. By (1.87) it is constant and invertible, and $`\{f,g\}_{\mathrm{PB}}=\sum_{A,B}\omega_{AB}\frac{\partial f}{\partial z_A}\frac{\partial g}{\partial z_B}`$. Define $`Y`$ by $`X_A=\sum_B\omega_{AB}Y_B`$. Differentiate (i) with $`f=z_A`$, $`g=z_B`$, and (ii), with respect to $`\lambda`$ at $`\lambda=0`$:

```math
\left.
\begin{aligned}
0&=\{X_A,z_B\}_{\mathrm{PB}}+\{z_A,X_B\}_{\mathrm{PB}}
=\sum_{C,D}\omega_{AC}\,\omega_{BD}\Bigl(\frac{\partial Y_D}{\partial z_C}-\frac{\partial Y_C}{\partial z_D}\Bigr),\\
0&=\sum_A\frac{\partial H}{\partial z_A}\,X_A.
\end{aligned}
\right.
\tag{1.41}
```

Since $`\omega`$ is invertible, $`\partial Y_D/\partial z_C=\partial Y_C/\partial z_D`$. On a simply connected $`M`$ this gives $`Y_B=\partial G/\partial z_B`$ for a smooth $`G`$, unique up to a constant, i.e. (1.39). The second line of (1.41) is then $`\sum_A\frac{\partial H}{\partial z_A}\{z_A,G\}_{\mathrm{PB}}=\{H,G\}_{\mathrm{PB}}=0`$, which is (1.40). $`\square`$

**(1) Time Evolution and Energy**

Taking $`f=H`$ in (1.37), $`\{H,H\}_{\mathrm{PB}}=0`$, so $`H`$ is a conserved quantity. With $`G=H`$, (1.39) gives $`X_A=\{z_A,H\}_{\mathrm{PB}}=F_A`$, so the subgroup generated by $`H`$ is the time evolution $`\Phi_t`$ of (1.27).

**(2) Translations and Momentum**

Let $`M=\mathbb R^{2n}`$ and fix $`k\in\mathbb R^n`$. Take $`\phi_\lambda(q,p)=(q+\lambda k,\,p)`$. Then $`Q_a=q_a+\lambda k_a`$ and $`P_a=p_a`$ satisfy (1.35), and $`\phi_\lambda`$ is a symmetry transformation if and only if $`H(q+\lambda k,p)=H(q,p)`$ for all $`\lambda`$, i.e. $`\sum_ak_a\,\partial H/\partial q_a=0`$. Here $`X=(k,0)`$, and (1.39) holds with

```math
\left.
\boxed{G=\sum_{a=1}^nk_a\,p_a,}
\right.
\tag{1.42}
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
\tag{1.43}
```

```math
\left.
\boxed{\Psi:\mathbb R^4\longrightarrow\mathbb R^n\ \text{or}\ \mathbb C^n
}
\right.
\tag{1.44}
```

Additional regularity conditions, such as $`C^\infty`$ smoothness, may be imposed.

The space of fields $`\{\Psi\}`$ carries a representation of $`ISO(1,3)^+`$. For $`(\Lambda,a)\in ISO(1,3)^+`$,

```math
\left.
\Psi\xrightarrow{\;(\Lambda,a)\;}U(\Lambda,a)\Psi,
\right.
\tag{1.45}
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
\tag{1.46}
```

<br><br>

<a id="lorentz-finite-representations"></a>
#### Finite-Dimensional Representations of $`SO(1,3)^+`$

$`U`$ is constructed from $`D`$ by (1.46), and $`D`$ is recovered from $`U`$ through $`[U(\Lambda,0)\Psi](0)=D(\Lambda)\Psi(0)`$. Hence

```math
\left.
\begin{aligned}
\Psi_\alpha(x),\ \alpha=1,\ldots,n
&\quad\Longleftrightarrow\quad\text{infinite-dimensional representation }U(\Lambda,a)\\
&\quad\Longleftrightarrow\quad n\text{-dimensional representation }D(\Lambda)\text{ of }SO(1,3)^+.
\end{aligned}
\right.
\tag{1.47}
```

**Lie Algebra Representations**

For $`X,Y\in\mathfrak o(1,3)`$,

```math
\left.
\rho(X):=\frac{d}{dt}D(e^{tX})\Big|_{t=0},\qquad
D(e^{X})=e^{\rho(X)},\qquad
\rho([X,Y])=[\rho(X),\rho(Y)].
\right.
\tag{1.48}
```

$`SO(1,3)^+`$ is connected, so $`D`$ is determined by $`\rho`$. Extend $`\rho`$ complex-linearly, $`\rho(X+iY):=\rho(X)+i\rho(Y)`$, to the complexified Lie algebra $`\mathfrak o(1,3)_{\mathbb C}`$, defined by (0.32) with $`M_4(\mathbb R)`$ replaced by $`M_4(\mathbb C)`$. By (0.36), $`\mathfrak o(1,3)_{\mathbb C}`$ contains every $`J^{\mu\nu}`$, and $`D(e^{-\frac i2\omega_{\mu\nu}J^{\mu\nu}})=e^{-\frac i2\omega_{\mu\nu}\rho(J^{\mu\nu})}`$. For the Dirac field, $`\rho(J^{\mu\nu})=S^{\mu\nu}`$ (1.106).

**Decomposition of $`\mathfrak o(1,3)_{\mathbb C}`$**

From (0.34),

```math
\left.
[J^i,J^j]=\epsilon_{ijk}J^k,\qquad
[J^i,K^j]=\epsilon_{ijk}K^k,\qquad
[K^i,K^j]=-\epsilon_{ijk}J^k.
\right.
\tag{1.49}
```

Define

```math
\left.
\begin{aligned}
A^i&:=\frac12\Bigl(\frac12\epsilon_{ijk}J^{jk}+iJ^{0i}\Bigr)=\frac i2\bigl(J^i+iK^i\bigr),\\
B^i&:=\frac12\Bigl(\frac12\epsilon_{ijk}J^{jk}-iJ^{0i}\Bigr)=\frac i2\bigl(J^i-iK^i\bigr),
\end{aligned}
\right.
\tag{1.50}
```

i.e. $`A^1=\frac12(J^{23}+iJ^{01})`$, $`A^2=\frac12(J^{31}+iJ^{02})`$, $`A^3=\frac12(J^{12}+iJ^{03})`$, and $`B^i`$ is the same with $`iJ^{0i}\to-iJ^{0i}`$. $`A^i`$ and $`B^i`$ are not real, so they lie in $`\mathfrak o(1,3)_{\mathbb C}`$ but not in $`\mathfrak o(1,3)`$. By (1.49),

```math
\left.
\boxed{[A^i,A^j]=i\epsilon_{ijk}A^k,\qquad
[B^i,B^j]=i\epsilon_{ijk}B^k,\qquad
[A^i,B^j]=0.}
\right.
\tag{1.51}
```

Hence

```math
\left.
\mathfrak o(1,3)_{\mathbb C}=\mathfrak g_A\oplus\mathfrak g_B,\qquad
\mathfrak g_A:=\mathop{\rm span}\nolimits\,_{\mathbb C}\{A^1,A^2,A^3\},\quad
\mathfrak g_B:=\mathop{\rm span}\nolimits\,_{\mathbb C}\{B^1,B^2,B^3\}.
\right.
\tag{1.52}
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
\tag{1.53}
```

The last line holds because the two terms in the first line commute.

The irreducible representations of $`\mathfrak{su}(2)`$ are $`V_j`$ with basis $`|j,m\rangle`$, $`m=-j,\ldots,j`$, on which $`\rho_A(A^3)`$ (or $`\rho_B(B^3)`$) acts as $`m`$. Here $`j=0,\frac12,1,\ldots`$ and $`\dim V_j=2j+1`$. Every finite-dimensional irreducible representation of $`\mathfrak g_A\oplus\mathfrak g_B`$ is $`V_{j_1}\otimes V_{j_2}`$, and every finite-dimensional representation is a direct sum of these:

```math
\left.
\boxed{(j_1,j_2),\qquad j_1,j_2\in\{0,\tfrac12,1,\tfrac32,\ldots\},\qquad\dim=(2j_1+1)(2j_2+1).}
\right.
\tag{1.54}
```

**Rotation by $`2\pi`$**

Since $`A^3+B^3=iJ^3`$ by (1.50), on $`(j_1,j_2)`$

```math
\left.
e^{2\pi J^3}=I_4,\qquad
e^{2\pi\rho(J^3)}=e^{-2\pi i\rho(A^3+B^3)}=(-1)^{2(j_1+j_2)}I_n.
\right.
\tag{1.55}
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
\tag{1.56}
```

in which $`\partial_\mu\Psi_\alpha`$ are independent variables, with no explicit dependence on $`x`$.

- **Action**: the functional on fields, for any bounded region $`\Omega\subset\mathbb R^4`$,

```math
\left.
\boxed{S[\Psi]:=\int_\Omega d^4x\,\mathcal L\bigl(\Psi_\alpha(x),\partial_\mu\Psi_\alpha(x)\bigr).}
\right.
\tag{1.57}
```

- **Solutions**: fields $`\Psi`$ at which $`S`$ is stationary under variations vanishing on $`\partial\Omega`$,

```math
\left.
\frac{d}{ds}S[\Psi+s\eta]\Big|_{s=0}=0,
\right.
\tag{1.58}
```

for every smooth $`\eta`$ with $`\eta|_{\partial\Omega}=0`$ and every $`\Omega`$.

**Conditions on the Lagrangian Density**

For the local relativistic field theories considered here, we require:

- **Lorentz invariance:** the action constructed from $`\mathcal L`$ is a Lorentz scalar.
- **Reality:** the Lagrangian density $`\mathcal L`$ is real.
- **Locality:** $`\mathcal L`$ depends only on the fields and finitely many of their derivatives at the same spacetime point.

Further mathematical restrictions may be imposed as conventional choices rather than universal axioms; ultimately, the essential requirement is agreement with physical reality, so that the Lagrangian describes or explains at least part of the real world.




**Euler–Lagrange Equations**

As in (1.6), integrating by parts in (1.58) and using $`\eta|_{\partial\Omega}=0`$, $`\Psi`$ is a solution if and only if

```math
\left.
\boxed{\partial_\mu\frac{\partial\mathcal L}{\partial(\partial_\mu\Psi_\alpha)}
-\frac{\partial\mathcal L}{\partial\Psi_\alpha}=0.}
\right.
\tag{1.59}
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
\tag{1.60}
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
\tag{1.61}
```

where the form of $`\Psi'`$ is given in (1.64) and (1.72): for $`\phi_\lambda=(\Lambda,a)`$ a Poincaré transformation, $`\Psi'=U(\Lambda,a)\Psi`$ of (1.46); for an internal transformation, $`x'=x`$ and $`\Psi'=g(\lambda)\Psi`$.

**Symmetry Transformations**

- **Symmetry transformation**: a transformation under which the action of every field is invariant for every region,

```math
\left.
\boxed{S'=S\quad\text{for every }\Psi\text{ and every }\Omega,}
\right.
\tag{1.62}
```

with $`S'`$ the action of $`\Psi'`$ over $`\phi_\lambda(\Omega)`$, written out in (1.66).

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
\tag{1.63}
```

is a conserved quantity, where $`\delta_0\Psi_\alpha`$ is defined in (1.64), the derivatives with respect to $`\lambda`$ are taken at $`\lambda=0`$, and the fall-off condition makes the integral converge and the surface term in (1.70) vanish.

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
\tag{1.64}
```

Here $`\Psi'`$ is the transformed field. Using the pushforward $`(\phi_\lambda)_*\Psi:=\Psi\circ\phi_\lambda^{-1}`$, we write $`\Psi'_\alpha=D_{\alpha\beta}(\Lambda)\,[(\phi_\lambda)_*\Psi]_\beta`$. Evaluating at $`x'`$ gives $`\Psi'_\alpha(x')=D_{\alpha\beta}(\Lambda)\Psi_\beta(x)`$, which is the last equality in the first line, so the first variation, $`\delta_0\Psi_\alpha`$, describes the transformation of the field itself. For $`\phi_\lambda=(\Lambda,a)`$, $`\Psi'=U(\Lambda,a)\Psi`$ by (1.46), which is the last equality in the second line. If $`\phi_\lambda`$ is not a Poincaré transformation, $`D(\Lambda)`$ is replaced by the identity and $`\delta_0\Psi_\alpha=0`$.

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
\tag{1.65}
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
\tag{1.66}
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
\tag{1.67}
```

where the third line is (1.64). Hence

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
\tag{1.68}
```

Expanding (1.68) to first order in $`\lambda`$ gives the off-shell identity

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
\tag{1.69}
```

The second equality substitutes $`\delta_0\Psi_\alpha=\delta\Psi_\alpha+\delta x^\nu\partial_\nu\Psi_\alpha`$ from (1.65) and uses the product rule together with $`\partial_\nu\mathcal L=\frac{\partial\mathcal L}{\partial\Psi_\alpha}\partial_\nu\Psi_\alpha+\frac{\partial\mathcal L}{\partial(\partial_\mu\Psi_\alpha)}\partial_\nu\partial_\mu\Psi_\alpha`$; the latter holds because $`\mathcal L`$ has no explicit $`x`$-dependence.

By hypothesis, the action is invariant: $`S'=S`$. Take $`\Omega=[t_1,t_2]\times V`$ and let $`\Psi_\alpha`$ satisfy the Euler–Lagrange equations, so that the Euler–Lagrange term in (1.69) vanishes. Gauss's theorem then gives

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
\tag{1.70}
```

By the fall-off condition, the surface term vanishes as $`V\to\mathbb R^3`$. Since $`t_1`$ and $`t_2`$ are arbitrary,

```math
\left.
\int d^3x\,\biggl(
\mathcal L\,\delta x^0
+\frac{\partial\mathcal L}{\partial\dot\Psi_\alpha}\delta\Psi_\alpha
\biggr)=\text{const}.
\right.
\tag{1.71}
```

Substituting $`\delta\Psi_\alpha=\delta_0\Psi_\alpha-\delta x^\nu\partial_\nu\Psi_\alpha`$ from (1.65), differentiating with respect to $`\lambda`$, and reversing the overall sign gives (1.63) for coordinate transformations.

**(B) Internal Transformation**

Now $`\phi_\lambda`$ acts trivially on spacetime, and on the field by a constant matrix $`g(\lambda)`$ with $`g(0)=I_n`$:

```math
\left.
x'^\mu=x^\mu,\qquad
\Psi'_\alpha(x)=g_{\alpha\beta}(\lambda)\,\Psi_\beta(x).
\right.
\tag{1.72}
```

Hence $`\delta x^\mu=0`$, and the two variations in (1.64) coincide: $`\delta\Psi_\alpha(x)=\delta_0\Psi_\alpha(x)=g_{\alpha\beta}(\lambda)\Psi_\beta(x)-\Psi_\alpha(x)`$. Repeating (1.66)–(1.71) with $`\delta x^\mu=0`$: in (1.67), $`d^4x'=d^4x`$ and $`\partial'_\mu=\partial_\mu`$; the terms containing $`\delta x^\mu`$ drop out of (1.68)–(1.70); and (1.71) becomes

```math
\left.
\int d^3x\,\frac{\partial\mathcal L}{\partial\dot\Psi_\alpha}\,\delta_0\Psi_\alpha=\text{const}.
\right.
\tag{1.73}
```

Differentiating with respect to $`\lambda`$ and reversing the overall sign gives (1.63) with $`\delta x^\mu=0`$. $`\square`$

<a id="spacetime-conserved-quantities"></a>
**(1) Spacetime Translations and Energy–Momentum**

Take $`\phi_\lambda(x)=x+\lambda\epsilon`$ for a fixed $`\epsilon\in\mathbb R^4`$, so that $`\delta x^\mu=\lambda\epsilon^\mu`$, $`\Lambda=I_4`$ and $`\delta_0\Psi_\alpha=0`$. By (1.66)–(1.68), $`S'=S`$ holds because $`\mathcal L`$ has no explicit $`x`$-dependence, and (1.63) gives

```math
\left.
\mathcal Q=\epsilon^\nu\int d^3x\Bigl(\frac{\partial\mathcal L}{\partial\dot\Psi_\alpha}\partial_\nu\Psi_\alpha-\delta^0{}_\nu\mathcal L\Bigr)=\epsilon^\nu P_\nu,
\right.
\tag{1.74}
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
\tag{1.75}
```

Here $`\partial_\mu T^\mu{}_\nu=0`$ holds on shell by (1.59), and $`P_0=H`$ by (1.60).

<br><br>

<a id="dirac-constraint"></a>
### 1.5 Dirac Constraint

<a id="singular-lagrangian"></a>
#### Singular Lagrangians

**Definition**

Let $`L:\mathbb R^n\times\mathbb R^n\to\mathbb R`$ be a smooth Lagrangian as in (1.2), without explicit time dependence.

- **Canonical momenta**:

```math
\left.
p_a:=\frac{\partial L}{\partial\dot q_a}(q,\dot q),\qquad a=1,\ldots,n.
\right.
\tag{1.76}
```

- **Hessian**: the symmetric matrix

```math
\left.
W_{ab}:=\frac{\partial^2L}{\partial\dot q_a\,\partial\dot q_b}(q,\dot q),\qquad a,b=1,\ldots,n.
\right.
\tag{1.77}
```

- **Regular and singular Lagrangians**: $`L`$ is regular if $`\det W\neq0`$ on $`\mathrm{Conf}\times\mathbb R^n`$, and singular otherwise. For a singular $`L`$ we assume that $`\mathop{\rm rank}\nolimits\,W=r<n`$ is constant.

If $`L`$ is regular, (1.76) can be solved for the velocities, $`\dot q=\dot q(q,p)`$, and

```math
\left.
H(q,p):=\sum_{a=1}^np_a\,\dot q_a(q,p)-L\bigl(q,\dot q(q,p)\bigr)
\right.
\tag{1.78}
```

is the Hamiltonian (1.30) of [Section 1.2](#hamiltonian-formalism). In the rest of this section $`L`$ is singular.

**Intuitive Physical Picture of Singular Lagrangians**

Take as an example the case of a constant matrix $`W`$, $`L=\frac12\sum_{a,b=1}^nW_{ab}\dot q_a\dot q_b-V(q)`$. Then $`W`$ is the mass matrix, and a $`W`$ that is not of full rank can be understood intuitively as a vanishing "mass" for motion along some directions. A suitable redefinition of the generalized coordinates brings $`W`$ to block-diagonal form: the upper-left $`r\times r`$ block is invertible (and may be taken diagonal), and all other entries vanish, so the kinetic term contains no velocities of the last $`n-r`$ coordinates. There are two cases, according to whether the potential depends on these $`n-r`$ coordinates.

1. In the new coordinates the potential contains only the first $`r`$ coordinates. The last $`n-r`$ coordinates do not appear in $`L`$ at all, and the equations of motion place no restriction on them: the original mathematical description is redundant.

2. In the new coordinates the potential still contains the last $`n-r`$ coordinates. Their Euler–Lagrange equations contain no accelerations and are only relations among the coordinates: the system is subject to constraints.



**Primary Constraints**

Since $`W`$ is symmetric, its rank equals the order of its largest invertible principal submatrix, so after reordering the coordinates

```math
\left.
\det\bigl(W_{ab}\bigr)_{a,b=1}^{r}\neq0.
\right.
\tag{1.79}
```

Indices $`\mu,\nu`$ run over the remaining values $`r+1,\ldots,n`$. By the implicit function theorem, the first $`r`$ equations of (1.76) can be solved locally for $`\dot q_1,\ldots,\dot q_r`$:

```math
\left.
\dot q_a=\varphi_a(q,p_b,\dot q_\mu),\qquad a=1,\ldots,r,
\right.
\tag{1.80}
```

where $`p_b`$ and $`\dot q_\mu`$ stand for $`(p_1,\ldots,p_r)`$ and $`(\dot q_{r+1},\ldots,\dot q_n)`$.

Substituting (1.80) into the remaining equations of (1.76) gives

```math
\left.
p_\mu=\frac{\partial L}{\partial\dot q_\mu}\bigl(q,\varphi(q,p_b,\dot q_\nu),\dot q_\nu\bigr)=:g_\mu(q,p_b,\dot q_\nu),
\right.
\tag{1.81}
```

and one can further show that $`g_\mu`$ does not depend on $`\dot q_\nu`$, as follows.

Differentiating the identity $`p_b=\frac{\partial L}{\partial\dot q_b}(q,\varphi,\dot q_\nu)`$ with respect to $`\dot q_\nu`$ gives $`\sum_{a=1}^rW_{ba}\frac{\partial\varphi_a}{\partial\dot q_\nu}=-W_{b\nu}`$, hence

```math
\left.
\frac{\partial}{\partial\dot q_\nu}\frac{\partial L}{\partial\dot q_\mu}\bigl(q,\varphi,\dot q\bigr)
=W_{\mu\nu}+\sum_{a=1}^rW_{\mu a}\frac{\partial\varphi_a}{\partial\dot q_\nu}
=W_{\mu\nu}-\sum_{a,b=1}^rW_{\mu a}\bigl(W^{-1}\bigr)_{ab}W_{b\nu}=0,
\right.
\tag{1.82}
```

with $`(W^{-1})_{ab}`$ the inverse of the block (1.79). The last expression is the Schur complement of that block in $`W`$, which vanishes since $`\mathop{\rm rank}\nolimits\,W=r`$.

- **Primary constraints**:

```math
\left.
\boxed{\chi_\mu(q,p):=p_\mu-g_\mu(q,p_b)=0,\qquad\mu=r+1,\ldots,n.}
\right.
\tag{1.83}
```

The $`n`$ equations (1.76) are equivalent to (1.80) together with (1.83). The constraints (1.83) involve only $`(q,p)`$ and define the constraint surface in phase space, the image of the map $`(q,\dot q)\mapsto(q,p(q,\dot q))`$.

- **Weak equality**: $`F\approx G`$ means that the phase-space functions $`F`$ and $`G`$ agree on the constraint surface.

**Canonical Hamiltonian**

Define

```math
\left.
H_c:=\sum_{a=1}^np_a\dot q_a-L(q,\dot q),
\right.
\tag{1.84}
```

with (1.80) substituted for $`\dot q_1,\ldots,\dot q_r`$, so that $`H_c`$ is a function of $`(q,p,\dot q_\mu)`$. By (1.80), (1.81) and (1.83),

```math
\left.
\frac{\partial H_c}{\partial\dot q_\nu}
=\sum_{a=1}^r\Bigl(p_a-\frac{\partial L}{\partial\dot q_a}\Bigr)\frac{\partial\varphi_a}{\partial\dot q_\nu}
+p_\nu-\frac{\partial L}{\partial\dot q_\nu}
=\chi_\nu(q,p),
\right.
\tag{1.85}
```

which is independent of $`\dot q_\mu`$ and vanishes on the constraint surface. Hence $`H_c`$ is independent of $`\dot q_\mu`$ on the constraint surface, where by (1.83) it is a function of $`(q,p_1,\ldots,p_r)`$ alone.

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
\tag{1.86}
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
\tag{1.87}
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
\tag{1.88}
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
\tag{1.89}
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
\tag{1.90}
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
\tag{1.91}
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
\tag{1.92}
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
\tag{1.93}
```

**Conserved Quantities: Spacetime Symmetries**

Translations give the canonical energy–momentum tensor in (1.75):

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
\tag{1.94}
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
\tag{1.95}
```

Here $`P_0`$ is the energy, $`P^i`$ are the spatial momenta, $`J^{ij}`$ generate rotations, and $`J^{0i}`$ generate boosts. These conservation laws hold on shell, with convergent integrals and vanishing boundary fluxes.

**Conserved Quantities: Internal and Gauge Symmetries**

The real scalar field has no $`U(1)`$ phase symmetry of the complex-field type. The complex Lagrangian (1.93) has a global $`U(1)`$ symmetry; it is not invariant under an arbitrary local phase $`\lambda(x)`$ without a gauge field. For constant $`\lambda`$, the conserved current and charge are

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
\tag{1.96}
```


<br><br>

<a id="scalar-field-solutions"></a>
#### Solutions of the Klein–Gordon Equation

For the real field take $`V(\phi)=\tfrac12m^2\phi^2`$; the complex field in (1.93) is already free. Define $`\Box:=\partial_\mu\partial^\mu`$. A plane wave obeys

```math
\left.
(\Box+m^2)e^{\mp ip\cdot x}=(m^2-p^2)e^{\mp ip\cdot x}=0,
\qquad
p^2=m^2,\qquad
p^0=E_{\mathbf p}:=\sqrt{\mathbf p^2+m^2}>0.
\right.
\tag{1.97}
```

Using the Lorentz-invariant measure written explicitly below, a real wave packet has the expansion

```math
\left.
\boxed{
\phi(x)=\int\frac{d^3p}{(2\pi)^3\,2E_{\mathbf p}}
\left[a(\mathbf p)e^{-ip\cdot x}+a^*(\mathbf p)e^{+ip\cdot x}\right].
}
\right.
\tag{1.98}
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
\tag{1.99}
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
\tag{1.100}
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
\tag{1.101}
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
\tag{1.102}
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
\tag{1.103}
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
\tag{1.104}
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
\tag{1.105}
```

For a local phase $`\lambda(x)`$, $`\mathcal L'=\mathcal L-j^\mu\partial_\mu\lambda`$; local gauge invariance requires coupling to a gauge field.

<br><br>

<a id="weyl-spinor-solutions"></a>
#### Solutions of the Dirac Equation in the Weyl Representation

**Spinor Representation of the Lorentz Group**

For the Dirac field, $`D(\Lambda)`$ in (1.46) is

```math
\left.
\Lambda_{\frac12}=\exp\Bigl(-\frac i2\omega_{\mu\nu}S^{\mu\nu}\Bigr),
\qquad
S^{\mu\nu}:=\frac i4[\gamma^\mu,\gamma^\nu],
\right.
\tag{1.106}
```

with the same $`\omega_{\mu\nu}`$ as in (0.35). In the Weyl representation every $`S^{\mu\nu}`$ is block diagonal:

```math
\left.
S^{0i}=-\frac i2\begin{pmatrix}\sigma^i&0\\0&-\sigma^i\end{pmatrix},
\qquad
S^{ij}=\frac12\epsilon^{ijk}\begin{pmatrix}\sigma^k&0\\0&\sigma^k\end{pmatrix}.
\right.
\tag{1.107}
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
\tag{1.108}
```

so that

```math
\left.
\begin{aligned}
\psi_L&\xrightarrow{\ \Lambda\ }\Bigl(I_2-i\boldsymbol\theta\cdot\frac{\boldsymbol\sigma}2-\mathbf b\cdot\frac{\boldsymbol\sigma}2\Bigr)\psi_L,\\
\psi_R&\xrightarrow{\ \Lambda\ }\Bigl(I_2-i\boldsymbol\theta\cdot\frac{\boldsymbol\sigma}2+\mathbf b\cdot\frac{\boldsymbol\sigma}2\Bigr)\psi_R.
\end{aligned}
\right.
\tag{1.109}
```

In terms of $`\psi_L,\psi_R`$, the Dirac equation (1.101) reads

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
\tag{1.110}
```

For $`m=0`$ it reduces to the Weyl equations

```math
\left.
\begin{cases}
i\bigl(\partial_t-\boldsymbol\sigma\cdot\nabla\bigr)\psi_L=0,\\
i\bigl(\partial_t+\boldsymbol\sigma\cdot\nabla\bigr)\psi_R=0.
\end{cases}
\right.
\tag{1.111}
```

**Plane-Wave Solutions of the Dirac Equation**

Apply $`-i\gamma^\mu\partial_\mu-m`$ to the left-hand side of (1.101):

```math
\left.
\begin{aligned}
\bigl(-i\gamma^\mu\partial_\mu-m\bigr)\bigl(i\gamma^\nu\partial_\nu-m\bigr)\psi
&=\bigl(\gamma^\mu\gamma^\nu\partial_\mu\partial_\nu+m^2\bigr)\psi\\
&=\bigl(\eta^{\mu\nu}\partial_\mu\partial_\nu+m^2\bigr)\psi\\
&=\bigl(\Box+m^2\bigr)\psi,
\end{aligned}
\right.
\tag{1.112}
```

where $`\Box:=\eta^{\mu\nu}\partial_\mu\partial_\nu=\partial_t^2-\nabla^2`$. Since the left-hand side of (1.112) vanishes by (1.101), every component of $`\psi`$ satisfies the Klein–Gordon equation

```math
\left.
\bigl(\Box+m^2\bigr)\psi=0.
\right.
\tag{1.113}
```

A plane wave $`e^{-ip\cdot x}`$ satisfies (1.113) only if $`p^2=m^2`$. In the Weyl representation (0.10), the plane-wave solutions of (1.101) therefore take the form

```math
\left.
\psi(x)=\begin{pmatrix}u_L\\u_R\end{pmatrix}e^{-ip\cdot x},
\qquad
p^0=\pm E_{\mathbf p},\quad
E_{\mathbf p}:=\sqrt{\mathbf p^2+m^2},
\right.
\tag{1.114}
```

where $`u_L,u_R\in\mathbb C^2`$ are constant. Substituting (1.114) into (1.101) gives

```math
\left.
\bigl(\not p-m\bigr)\begin{pmatrix}u_L\\u_R\end{pmatrix}=0,
\qquad
\not p:=\gamma\cdot p=p^\mu\gamma_\mu.
\right.
\tag{1.115}
```

**(1) Rest Frame**

Take $`m>0`$ and work in the rest frame, $`\mathbf p=\mathbf 0`$; there we denote the constants in (1.114) by $`u_L(\mathbf 0)`$ and $`u_R(\mathbf 0)`$. First consider $`p^0>0`$. Then $`p^\mu=(m,\mathbf 0)`$, $`e^{-ip\cdot x}=e^{-imt}`$ and $`\not p=m\gamma^0`$, so (1.115) becomes

```math
\left.
\begin{aligned}
\bigl(m\gamma^0-m\bigr)\begin{pmatrix}u_L(\mathbf 0)\\u_R(\mathbf 0)\end{pmatrix}
&=\begin{pmatrix}-mI_2&mI_2\\mI_2&-mI_2\end{pmatrix}
\begin{pmatrix}u_L(\mathbf 0)\\u_R(\mathbf 0)\end{pmatrix}=0\\[6pt]
\Longrightarrow\quad u_L(\mathbf 0)&=u_R(\mathbf 0).
\end{aligned}
\right.
\tag{1.116}
```

Writing $`u:=\begin{pmatrix}u_L\\u_R\end{pmatrix}`$, there are two independent solutions

```math
\left.
u^s(\mathbf 0)=\sqrt m\begin{pmatrix}\xi^s\\\xi^s\end{pmatrix},\qquad s=1,2,
\right.
\tag{1.117}
```

where $`\{\xi^s\}`$ is a basis of $`\mathbb C^2`$ with $`\xi^{r\dagger}\xi^s=\delta^{rs}`$.

**(2) Boost**

Boost along $`z`$ with rapidity $`\eta`$, i.e. $`\omega_{03}=\eta`$ in (1.106), so that $`\mathbf p=(0,0,p^3)`$ and $`\tanh\eta=v=p^3/E_{\mathbf p}`$. Then

```math
\left.
\begin{aligned}
\Lambda_{\frac12}=e^{-i\eta S^{03}}
&=\exp\Bigl[-i\eta\Bigl(-\frac i2\Bigr)\begin{pmatrix}\sigma^3&0\\0&-\sigma^3\end{pmatrix}\Bigr]
=\begin{pmatrix}e^{-\frac12\eta\sigma^3}&0\\0&e^{\frac12\eta\sigma^3}\end{pmatrix}\\
&=\mathop{\rm diag}\nolimits \bigl(e^{-\eta/2},\,e^{\eta/2},\,e^{\eta/2},\,e^{-\eta/2}\bigr),
\end{aligned}
\right.
\tag{1.118}
```

```math
\left.
\tanh\eta=v
\ \Longrightarrow\
e^{\pm\eta}=\sqrt{\frac{1\pm v}{1\mp v}}=\frac{E_{\mathbf p}\pm p^3}{m},
\qquad
e^{\pm\eta/2}=\sqrt{\frac{E_{\mathbf p}\pm p^3}{m}}.
\right.
\tag{1.119}
```

Hence

```math
\left.
u^s(p)=\Lambda_{\frac12}u^s(\mathbf 0)
=\mathop{\rm diag}\nolimits \Bigl(\sqrt{E_{\mathbf p}-p^3},\,\sqrt{E_{\mathbf p}+p^3},\,\sqrt{E_{\mathbf p}+p^3},\,\sqrt{E_{\mathbf p}-p^3}\Bigr)
\begin{pmatrix}\xi^s\\\xi^s\end{pmatrix}.
\right.
\tag{1.120}
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
\tag{1.121}
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
\tag{1.122}
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
\tag{1.123}
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
\tag{1.124}
```

**Negative-Energy Solutions**

For $`p^0=-E_{\mathbf p}`$, (1.115) becomes

```math
\left.
\bigl(-\gamma^0E_{\mathbf p}-\boldsymbol\gamma\cdot\mathbf p-m\bigr)u(p)=0
\quad\Longleftrightarrow\quad
\bigl(\gamma^0E_{\mathbf p}-\boldsymbol\gamma\cdot(-\mathbf p)+m\bigr)u(p)=0,
\right.
\tag{1.125}
```

which is the positive-energy equation $`\bigl(\gamma^0E_{\mathbf p}-\boldsymbol\gamma\cdot\mathbf p-m\bigr)u=0`$ with $`\mathbf p\to-\mathbf p`$ and $`m\to-m`$. Hence

```math
\left.
u^s(p)=\begin{pmatrix}\sqrt{E_{\mathbf p}I_2+\mathbf p\cdot\boldsymbol\sigma}\,\xi^s\\-\sqrt{E_{\mathbf p}I_2-\mathbf p\cdot\boldsymbol\sigma}\,\xi^s\end{pmatrix}
=\begin{pmatrix}\sqrt{-p\cdot\sigma}\,\xi^s\\-\sqrt{-p\cdot\bar\sigma}\,\xi^s\end{pmatrix},
\qquad p^0=-E_{\mathbf p}.
\right.
\tag{1.126}
```

**Antiparticle Solutions**

Define

```math
\left.
u^c(p):=\begin{pmatrix}i\sigma^2&0\\0&-i\sigma^2\end{pmatrix}\gamma^0\,u(p),
\qquad
i\sigma^2=\begin{pmatrix}0&1\\-1&0\end{pmatrix}.
\right.
\tag{1.127}
```

For $`\mathbf p=(0,0,p^3)`$,

```math
\left.
i\sigma^2\sqrt{p\cdot\bar\sigma}
=\begin{pmatrix}0&1\\-1&0\end{pmatrix}\begin{pmatrix}\sqrt{E_{\mathbf p}+p^3}&0\\0&\sqrt{E_{\mathbf p}-p^3}\end{pmatrix}
=\begin{pmatrix}0&\sqrt{E_{\mathbf p}-p^3}\\-\sqrt{E_{\mathbf p}+p^3}&0\end{pmatrix}
=\sqrt{p\cdot\sigma}\;i\sigma^2,
\right.
\tag{1.128}
```

and likewise $`i\sigma^2\sqrt{p\cdot\sigma}=\sqrt{p\cdot\bar\sigma}\;i\sigma^2`$. Applying (1.127) to (1.123) and writing $`\eta^s:=i\sigma^2\xi^s`$,

```math
\left.
u^c(p)=\begin{pmatrix}i\sigma^2\sqrt{p\cdot\bar\sigma}\,\xi^s\\-i\sigma^2\sqrt{p\cdot\sigma}\,\xi^s\end{pmatrix}
=\begin{pmatrix}\sqrt{p\cdot\sigma}\,\eta^s\\-\sqrt{p\cdot\bar\sigma}\,\eta^s\end{pmatrix},
\qquad p^0=E_{\mathbf p},
\right.
\tag{1.129}
```

which is (1.126) at $`-p`$ with $`\xi^s\to\eta^s`$. For arbitrary $`\mathbf p`$, the antiparticle solutions are

```math
\left.
\boxed{
\psi=v^s(p)\,e^{+ip\cdot x},\qquad
v^s(p):=\begin{pmatrix}\sqrt{p\cdot\sigma}\,\eta^s\\-\sqrt{p\cdot\bar\sigma}\,\eta^s\end{pmatrix},\qquad
\bigl(\not p+m\bigr)v^s(p)=0,\qquad
p^0=E_{\mathbf p}.
}
\right.
\tag{1.130}
```

**Properties of the Solutions**

**(1) Orthonormality**

From (1.123), $`u^\dagger u=2E_{\mathbf p}\,\xi^\dagger\xi`$ and $`\bar uu=2m\,\xi^\dagger\xi`$. With $`\xi^{r\dagger}\xi^s=\eta^{r\dagger}\eta^s=\delta^{rs}`$,

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
\tag{1.131}
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
\tag{1.132}
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
\tag{1.133}
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
\tag{1.134}
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
\tag{1.135}
```

**Chirality**

```math
\left.
\gamma^5\begin{pmatrix}\psi_L\\0\end{pmatrix}=-\begin{pmatrix}\psi_L\\0\end{pmatrix},
\qquad
\gamma^5\begin{pmatrix}0\\\psi_R\end{pmatrix}=\begin{pmatrix}0\\\psi_R\end{pmatrix}.
\right.
\tag{1.136}
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
\tag{1.137}
```

**Vector and Axial Currents**

```math
\left.
j^\mu:=\bar\psi\gamma^\mu\psi,\qquad
j^{\mu5}:=\bar\psi\gamma^\mu\gamma^5\psi.
\right.
\tag{1.138}
```

The Euler–Lagrange equation of (1.100) for $`\psi`$ is $`-i\partial_\mu\bar\psi\gamma^\mu-m\bar\psi=0`$. Together with (1.101),

```math
\left.
\partial_\mu j^\mu=(\partial_\mu\bar\psi)\gamma^\mu\psi+\bar\psi\gamma^\mu\partial_\mu\psi
=im\bar\psi\psi-im\bar\psi\psi=0
\quad\Longrightarrow\quad
\int d^3x\,\bar\psi\gamma^0\psi=\text{const}.
\right.
\tag{1.139}
```

**Helicity**

```math
\left.
h:=\frac{\mathbf p}{|\mathbf p|}\cdot\mathbf S,\qquad
\mathbf S:=\frac12\begin{pmatrix}\boldsymbol\sigma&0\\0&\boldsymbol\sigma\end{pmatrix}.
\right.
\tag{1.140}
```

For $`\mathbf p=(0,0,p^3)`$ with $`p^3>0`$, the spinors (1.121) satisfy $`h\,u^1=\frac12u^1`$ and $`h\,u^2=-\frac12u^2`$.


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
\tag{1.141}
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
\tag{1.142}
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
\tag{1.143}
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
\tag{1.144}
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
\tag{1.145}
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
\tag{1.146}
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
\tag{1.147}
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
\tag{1.148}
```

These are conserved on shell, with convergent integrals and vanishing boundary fluxes.

**Conserved Quantities: Internal and Gauge Symmetries**

For $`m>0`$, the mass term breaks the Maxwell gauge symmetry $`A_\mu\mapsto A_\mu+\partial_\mu\lambda(x)`$. The real Proca field has no complex $`U(1)`$ phase symmetry, so this model has no corresponding phase charge. Its constraint $`\partial_i\Pi^i+m^2A_0=0`$ is second class, as in (1.145).

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
\tag{1.149}
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
\tag{1.150}
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
\tag{1.151}
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
\tag{1.152}
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
\tag{1.153}
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
\tag{1.154}
```

Both constraints are first class:

```math
\left.
\{\chi_a(\mathbf x),\chi_b(\mathbf y)\}_{\mathrm{PB}}=0,
\qquad a,b=1,2,
\qquad
\boxed{N_{\mathrm{physical}}=4-2=2.}
\right.
\tag{1.155}
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
\tag{1.156}
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
\tag{1.157}
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
\tag{1.158}
```

These charges are conserved on shell when the integrals converge and boundary fluxes vanish. The canonical densities depend on the gauge; the integrated charges are invariant under gauge transformations whose boundary terms vanish.

**Conserved Quantities: Internal and Gauge Symmetries**

The local transformation in (1.153) gives a Noether identity and the Gauss constraint. For smooth source-free fields on all of $`\mathbb R^3`$,

```math
\left.
\boxed{\begin{aligned}
\partial_\nu\partial_\mu F^{\mu\nu}&\equiv0,
&\partial_i\Pi^i&=0,\\
Q_{\mathrm{el}}&:=\lim_{R\to\infty}\oint_{|\mathbf x|=R}\Pi^i\,dS_i=0.
\end{aligned}}
\right.
\tag{1.159}
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
\tag{1.160}
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
\tag{1.161}
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
\tag{1.162}
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
\tag{1.163}
```

The $`a_r(\mathbf p)`$ are classical complex amplitudes. Other gauge representatives follow by adding $`\partial^\mu\lambda(x)`$.

<br><br>

<a id="qft-ch2"></a>
## 2. Operator Quantization


The first viewpoint in [Section 1.4](#classical-dynamics) naturally leads to Operator quantization: spatial position labels the degrees of freedom, while time remains the evolution parameter. 


<br><br>
<a id="pictures-of-time-evolution"></a>
### 2.1 Pictures of Time Evolution

Throughout, the pictures are taken to coincide at $`t=0`$.

In the Hamiltonian formalism the dynamics is given by the Hamiltonian $`\hat H`$. The time dependence of an observable therefore has two sources:

1. The first is the dynamics of the system, i.e. the time evolution generated by $`\hat H`$, which differs from system to system: a different Hamiltonian gives the observable a different time dependence. 

2. The second is a change in the form of the observable itself, which appears as an explicit time dependence and is described mathematically by the partial derivative with respect to $`t`$.

For example, the position and momentum operators are the most basic observables. Their form is fixed by their own definition, so they carry no explicit time dependence, but they can still evolve in time. The form of an interaction, by contrast, can change with time: for a charged system, varying the strength of an external magnetic field by hand changes the form of the interaction.

<br>

<a id="schrodinger-picture"></a>
#### Schrödinger Picture

**The dynamics is carried entirely by the states; operators do not evolve in time.**

```math
\left.
\frac{d \hat O}{dt} - \frac{\partial \hat O}{\partial t} = 0
\right.
\tag{2.1}
```

Hence

```math
\left.
\frac{d\hat q_i}{dt}=\frac{\partial\hat q_i}{\partial t}=0,
\qquad
\frac{d\hat p_i}{dt}=\frac{\partial\hat p_i}{\partial t}=0.
\right.
\tag{2.2}
```

The time dependence of the states comes from the dynamics; as one of the axioms of quantum mechanics, it is given by the celebrated Schrödinger equation

```math
\left.
i\frac{\partial}{\partial t}|\psi_S(t)\rangle=\hat H_S|\psi_S(t)\rangle.

\right.
\tag{2.3}
```

Note that the form of $`\hat H_S`$ in the equation may change with time; accordingly, the solution of the Schrödinger equation takes three forms.

(1) $`\frac{\partial \hat H_S}{\partial t} = 0`$ 



```math
\left.
|\psi_S(t)\rangle=e^{-i\hat H_S(t-t_0)}\,|\psi_S(t_0)\rangle .
\right.
\tag{2.4}
```

where the exponential of an operator is defined by the power series:

```math
\left.
e^{\hat O}:=\sum_{n=0}^{\infty}\frac{1}{n!}\,\hat O^n.
\right.
\tag{2.5}
```

(2) $`\frac{\partial\hat H_S}{\partial t}\neq0`$, but $`[\hat H_S(t),\hat H_S(t')]=0`$ for all $`t,t'`$

```math
\left.
|\psi_S(t)\rangle=\exp\Bigl(-i\int_{t_0}^{t}d\tau\,\hat H_S(\tau)\Bigr)\,|\psi_S(t_0)\rangle ,
\right.
\tag{2.6}
```

where

```math
\left.
\langle \psi_1 | \int_{t_0}^{t}d\tau\,\hat H_S(\tau) |  \psi_2  \rangle  := \int_{t_0}^{t}d\tau\,\langle\psi_1 |\hat H_S(\tau)|\psi_2\rangle
\right.
\tag{2.7}
```

One can show that

```math
\left.
\langle \psi_1 | [\int_{t_0}^{t}d\tau\,\hat H_S(\tau)]^n |  \psi_2  \rangle  = \int_{t_0}^{t}...\int_{t_0}^{t}d\tau_1 ... d\tau_n\,\langle\psi_1 |\hat H_S(\tau_1)...\hat H_S(\tau_n)|\psi_2\rangle
\right.
\tag{2.8}
```



```math
\left.
\begin{aligned}
\frac{\partial}{\partial t}\Bigl(\int_{t_0}^{t}d\tau\,\hat H_S(\tau)\Bigr)^n
&=\sum_{k=0}^{n-1}\Bigl(\int_{t_0}^{t}d\tau\,\hat H_S(\tau)\Bigr)^k\,\hat H_S(t)\,\Bigl(\int_{t_0}^{t}d\tau\,\hat H_S(\tau)\Bigr)^{n-1-k}\\
&=n\,\hat H_S(t)\Bigl(\int_{t_0}^{t}d\tau\,\hat H_S(\tau)\Bigr)^{n-1}.
\end{aligned}
\right.
\tag{2.9}
```

Hence

```math
\left.
\begin{aligned}
\frac{\partial}{\partial t}\exp\Bigl(-i\int_{t_0}^{t}d\tau\,\hat H_S(\tau)\Bigr)
&=\sum_{n=1}^{\infty}\frac{(-i)^n}{n!}\,n\,\hat H_S(t)\Bigl(\int_{t_0}^{t}d\tau\,\hat H_S(\tau)\Bigr)^{n-1}\\
&=-i\hat H_S(t)\exp\Bigl(-i\int_{t_0}^{t}d\tau\,\hat H_S(\tau)\Bigr).
\end{aligned}
\right.
\tag{2.10}
```

With these formulas one verifies that the solution indeed has the form given above.



(3) $`[\hat H_S(t),\hat H_S(t')]\neq0`$ for some $`t,t'`$

```math
\left.
|\psi_S(t)\rangle=\mathcal T\exp\Bigl(-i\int_{t_0}^{t}d\tau\,\hat H_S(\tau)\Bigr)\,|\psi_S(t_0)\rangle ,
\right.
\tag{2.11}
```

where the time-ordered exponential is defined by the series (the Dyson series):

```math
\left.
\mathcal T\exp\Bigl(-i\int_{t_0}^{t}d\tau\,\hat H_S(\tau)\Bigr)
:=\sum_{n=0}^{\infty}\frac{(-i)^n}{n!}\int_{t_0}^{t}d\tau_1\cdots\int_{t_0}^{t}d\tau_n\,
\mathcal T[\hat H_S(\tau_1)\cdots\hat H_S(\tau_n)],
\right.
\tag{2.12}
```

The time-ordered product $`\mathcal T`$ orders the operators with time decreasing from left to right:

```math
\left.
\mathcal T[\hat H_S(\tau_1)\hat H_S(\tau_2)]
:=\theta(\tau_1-\tau_2)\,\hat H_S(\tau_1)\hat H_S(\tau_2)+\theta(\tau_2-\tau_1)\,\hat H_S(\tau_2)\hat H_S(\tau_1),
\right.
\tag{2.13}
```

The case of $`n`$ operators is analogous.

One can show that

```math
\left.
\frac{\partial}{\partial t}\int_{t_0}^{t}d\tau_1\cdots\int_{t_0}^{t}d\tau_n\,
\mathcal T[\hat H_S(\tau_1)\cdots\hat H_S(\tau_n)]
=n\,\hat H_S(t)\int_{t_0}^{t}d\tau_1\cdots\int_{t_0}^{t}d\tau_{n-1}\,
\mathcal T[\hat H_S(\tau_1)\cdots\hat H_S(\tau_{n-1})],
\right.
\tag{2.14}
```

Hence

```math
\left.
\begin{aligned}
\frac{\partial}{\partial t}\mathcal T\exp\Bigl(-i\int_{t_0}^{t}d\tau\,\hat H_S(\tau)\Bigr)
&=\sum_{n=1}^{\infty}\frac{(-i)^n}{n!}\,n\,\hat H_S(t)\int_{t_0}^{t}d\tau_1\cdots\int_{t_0}^{t}d\tau_{n-1}\,
\mathcal T[\hat H_S(\tau_1)\cdots\hat H_S(\tau_{n-1})]\\
&=-i\hat H_S(t)\,\mathcal T\exp\Bigl(-i\int_{t_0}^{t}d\tau\,\hat H_S(\tau)\Bigr).
\end{aligned}
\right.
\tag{2.15}
```

If $`[\hat H_S(t),\hat H_S(t')]=0`$ for all $`t,t'`$, then $`\mathcal T`$ can be dropped and the above reduces to case (2); if they do not commute, the second equality of the power identity in case (2) fails and $`\mathcal T`$ must be kept.

This series can be obtained by integrating the Schrödinger equation and iterating:

```math
\left.
\begin{aligned}
|\psi_S(t)\rangle
&=|\psi_S(t_0)\rangle-i\int_{t_0}^{t}d\tau_1\,\hat H_S(\tau_1)\,|\psi_S(\tau_1)\rangle\\
&=\Bigl[1+(-i)\int_{t_0}^{t}d\tau_1\,\hat H_S(\tau_1)
+(-i)^2\int_{t_0}^{t}d\tau_1\int_{t_0}^{\tau_1}d\tau_2\,\hat H_S(\tau_1)\hat H_S(\tau_2)+\cdots\Bigr]|\psi_S(t_0)\rangle ,
\end{aligned}
\right.
\tag{2.16}
```

where the $`n`$-th term is integrated over $`t\ge\tau_1\ge\cdots\ge\tau_n\ge t_0`$, with operators at later times to the left.

$`\mathcal T[\hat H_S(\tau_1)\cdots\hat H_S(\tau_n)]`$ is symmetric under permutations of $`\tau_1,\ldots,\tau_n`$; the cube $`[t_0,t]^n`$ splits into $`n!`$ regions according to the ordering of the $`\tau_i`$, each contributing equally, and on $`\tau_1>\cdots>\tau_n`$ the time-ordered product is the ordered product.

Hence

```math
\left.
\int_{t_0}^{t}d\tau_1\int_{t_0}^{\tau_1}d\tau_2\cdots\int_{t_0}^{\tau_{n-1}}d\tau_n\,
\hat H_S(\tau_1)\cdots\hat H_S(\tau_n)
=\frac1{n!}\int_{t_0}^{t}d\tau_1\cdots\int_{t_0}^{t}d\tau_n\,
\mathcal T[\hat H_S(\tau_1)\cdots\hat H_S(\tau_n)],
\right.
\tag{2.17}
```

Substituting this gives the defining series of the time-ordered exponential.

**Evolution Operator**

In each case the solution is linear in $`|\psi_S(t_0)\rangle`$:

```math
\left.
|\psi_S(t)\rangle=\hat U_S(t,t_0)\,|\psi_S(t_0)\rangle,
\right.
\tag{2.18}
```

where
```math
\left.
i\frac{\partial}{\partial t}\hat U_S(t,t_0)=\hat H_S(t)\,\hat U_S(t,t_0),
\qquad
\hat U_S(t_0,t_0)=1.
\right.
\tag{2.19}
```

The evolution operator $`\hat U_S(t,t_0)`$ is the operator exponential acting on $`|\psi_S(t_0)\rangle`$ in the three cases above.

It is easy to show that
```math
\left.
\hat U_S(t_2,t_0) = \hat U_S(t_2,t_1) \hat U_S(t_1,t_0)
\right.
\tag{2.20}
```

```math
\left.
\hat U_S(t,t_0)^\dagger  \hat U_S(t,t_0) = \hat 1
\right.
\tag{2.21}
```


```math
\left.
\hat U_S(t,t_0)^\dagger = \hat U_S(t_0,t)
\right.
\tag{2.22}
```

<br><br>

<a id="heisenberg-picture"></a>
#### Heisenberg Picture

**The dynamics is carried entirely by the operators; states do not evolve in time.**

The Heisenberg picture is obtained from the Schrödinger picture by the transformation

```math
\left.
\boxed{
\begin{gathered}
|\psi_H(t)\rangle:=\hat U_S(t,0)^\dagger\,|\psi_S(t)\rangle=|\psi_S(0)\rangle,\\[4pt]
\hat O_H(t):=\hat U_S(t,0)^\dagger\,\hat O_S(t)\,\hat U_S(t,0).
\end{gathered}
}
\right.
\tag{2.23}
```

Since the pictures are taken to coincide at $`t=0`$, we abbreviate $`\hat U_S(t,0)`$ as $`\hat U_S`$ below.

The two pictures give the same expectation values

```math
\left.
\langle\psi_H(t)| \hat O_H(t) |\psi_H(t)\rangle =
\langle\psi_H(t)|\hat U_S^\dagger \hat U_S \hat O_H(t) \hat U_S^\dagger \hat U_S|\psi_H(t)\rangle=\langle\psi_S(t)|\hat O_S(t)|\psi_S(t)\rangle
\right.
\tag{2.24}
```

We now compute the time dependence of states and operators in the Heisenberg picture

```math
\left.
\begin{aligned}
\frac{d\hat O_H}{dt}
&=\Bigl(\frac{\partial\hat U_S}{\partial t}\Bigr)^\dagger\hat O_S\,\hat U_S
+\hat U_S^\dagger\,\frac{d\hat O_S}{dt}\,\hat U_S
+\hat U_S^\dagger\hat O_S\,\frac{\partial\hat U_S}{\partial t}\\
&=i\,\hat U_S^\dagger\bigl[\hat H_S(t),\hat O_S\bigr]\hat U_S
+\hat U_S^\dagger\,\frac{\partial\hat O_S}{\partial t}\,\hat U_S\\
&=i\bigl[\hat H_H(t),\hat O_H\bigr]+\Bigl(\frac{\partial\hat O_S}{\partial t}\Bigr)_H,
\end{aligned}
\right.
\tag{2.25}
```

where $`\hat H_H(t):=\hat U_S^\dagger\hat H_S(t)\,\hat U_S`$ and $`(\partial\hat O_S/\partial t)_H:=\hat U_S^\dagger(\partial\hat O_S/\partial t)\,\hat U_S`$.

In cases (1) and (2), $`\hat U_S(t,0)`$ commutes with $`\hat H_S(t)`$, so $`\hat H_H(t)=\hat H_S(t)`$.



<br><br>

<a id="canonical-quantization"></a>
<a id="canonical-commutation-relations"></a>
### 2.2 Canonical Quantization

Consider a field $`\phi:\mathbb R^4\to\mathbb R^n`$ without Dirac constraints, with components $`\phi_a`$.

The Lagrangian density is a smooth function

```math
\left.
\begin{aligned}
\mathcal L:\mathbb R^n\times(\mathbb R^n)^4&\to\mathbb R,\\
(x,y^\mu)&\mapsto\mathcal L(x,y^\mu),
\end{aligned}
\right.
\tag{2.26}
```

where $`y^\mu\in\mathbb R^n`$, $`\mu=0,\ldots,3`$.

Write $`\mathcal L|_\phi`$ and $`\frac{\partial\mathcal L}{\partial y^\mu_a}\big|_\phi`$ for $`\mathcal L`$ and its partial derivatives evaluated at $`\bigl(\phi(x),\partial_\mu\phi(x)\bigr)`$; they are functions of $`x`$.

The Lagrangian is

```math
\left.
L(t):=\int d^3x\,\mathcal L|_\phi(t,\mathbf x).
\right.
\tag{2.27}
```

At each fixed time, the field values form an infinite set of generalized coordinates:

```math
\left.
i\longleftrightarrow(a,\mathbf x),
\qquad
q_i(t)\longleftrightarrow\phi_a(t,\mathbf x).
\right.
\tag{2.28}
```

**Conjugate momentum**

The momentum density conjugate to $`\phi_a(t,\mathbf x)`$ is

```math
\left.
\pi_a(t,\mathbf x)
:=
\frac{\partial\mathcal L}{\partial y^0_a}\Big|_\phi(t,\mathbf x).
\right.
\tag{2.29}
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
\tag{2.30}
```

Canonical quantization promotes the fields and their conjugate momenta to operators and replaces these fundamental Poisson brackets according to

```math
\left.
\{\ ,\ \}_{\mathrm{PB}}
\longrightarrow
\frac{1}{i}[\ ,\ ].
\right.
\tag{2.31}
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
\tag{2.32}
```

Here $`\delta_{ab}\delta^{(3)}(\mathbf x-\mathbf y)`$ generalizes the Kronecker delta $`\delta_{ij}`$ to the field labels $`(a,\mathbf x)`$.

<br><br>

<a id="free-real-scalar-field-quantization"></a>
#### Quantization of the Free Real Scalar Field

For a free field of mass $`m`$, use the Lorentz-invariant measure $`d\Pi_{\mathbf p}`$ and positive-energy four-momentum $`p`$:

```math
\left.
\begin{aligned}
E_{\mathbf p}&=\sqrt{\mathbf p^2+m^2},\qquad p^0=E_{\mathbf p},\qquad d\Pi_{\mathbf p}:=\frac{d^3p}{(2\pi)^3\,2E_{\mathbf p}},\\
\hat\phi_I(x)&=\int d\Pi_{\mathbf p}\left(\hat a_{\mathbf p}e^{-ip\cdot x}+\hat a_{\mathbf p}^\dagger e^{+ip\cdot x}\right).
\end{aligned}
\right.
\tag{2.33}
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
\tag{2.34}
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
\tag{2.35}
```

<br><br>

<a id="quantization-with-dirac-brackets"></a>
### 2.3 Quantization with Dirac Brackets

<a id="complex-scalar-field-quantization"></a>
#### Quantization of the Complex Scalar Field

<br><br>

<a id="dirac-field-quantization"></a>
#### Quantization of the Dirac Field

**Free Dirac Field**

Using the spinors and their normalization in [Section 1.7](#dirac-field), the operators $`\hat b_{\mathbf p}^s`$ and $`\hat c_{\mathbf p}^s`$ annihilate particles and antiparticles, respectively:

```math
\left.
\hat\psi_I(x)=\sum_{s=1}^{2}\int d\Pi_{\mathbf p}\left(\hat b_{\mathbf p}^s u^s(p)e^{-ip\cdot x}+\hat c_{\mathbf p}^{s\dagger}v^s(p)e^{+ip\cdot x}\right).
\right.
\tag{2.36}
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
\tag{2.37}
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
\tag{2.38}
```

<br><br>

<a id="proca-field-quantization"></a>
#### Quantization of the Proca Field

<br><br>

<a id="gupta-bleuler-quantization"></a>
### 2.4 Gupta–Bleuler Quantization

<br><br>

<a id="symmetry"></a>
### 2.5 Symmetry

<a id="ward-identity"></a>
#### Ward Identity

<br><br>

<a id="qft-ch3"></a>
## 3. Path Integrals

<a id="path-integrals-in-quantum-mechanics"></a>
### 3.1 Path Integrals in Quantum Mechanics

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
\tag{3.1}
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
\tag{3.2}
```

- **Action**: the functional on paths

```math
\left.
\begin{aligned}
S:\{\text{paths}\}&\to\mathbb R,\\
C&\mapsto S[C]:=\int_{t_i}^{t_f}dt\,L\bigl(C(t),\dot C(t)\bigr).
\end{aligned}
\right.
\tag{3.3}
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
\tag{3.4}
```

- **Final configuration**:

```math
\left.
\begin{aligned}
Q_f:\{t_f\}&\to\mathrm{Conf},\\
t_f&\mapsto q_f.
\end{aligned}
\right.
\tag{3.5}
```

- **Transition kernel**: the integral over the paths with these endpoints,

```math
\left.
\boxed{K(Q_f,Q_i):=\int_{C(t_i)=Q_i(t_i)}^{C(t_f)=Q_f(t_f)}\mathcal DC\,e^{iS[C]},}
\right.
\tag{3.6}
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
\tag{3.7}
```

so that $`t_0=t_i`$ and $`t_{N+1}=t_f`$, with $`d^nC(t_k):=\prod_{a=1}^ndC_a(t_k)`$.

- **Action**:

```math
\left.
S[C]=\lim_{N\to\infty}\Delta t\sum_{k=0}^NL\Bigl(C(t_k),\frac{C(t_{k+1})-C(t_k)}{\Delta t}\Bigr).
\right.
\tag{3.8}
```

Thus (3.6) means

```math
\left.
\boxed{
K(Q_f,Q_i)=\lim_{N\to\infty}\mathcal N_N\int\prod_{k=1}^Nd^nC(t_k)\,
\exp\biggl[i\,\Delta t\sum_{k=0}^NL\Bigl(C(t_k),\frac{C(t_{k+1})-C(t_k)}{\Delta t}\Bigr)\biggr],}
\right.
\tag{3.9}
```

with $`C(t_0):=q_i`$, $`C(t_{N+1}):=q_f`$, and each $`C(t_k)`$, $`1\le k\le N`$, integrated over $`\mathrm{Conf}`$.

**Functional Derivative**

For a source $`J:[t_i,t_f]\to\mathbb R^n`$, with $`J\cdot C:=\sum_{a=1}^nJ_aC_a`$,

```math
\left.
K^J(Q_f,Q_i):=\int_{Q_i}^{Q_f}\mathcal DC\,\exp\Bigl(i\int_{t_i}^{t_f}dt\,\bigl[L\bigl(C(t),\dot C(t)\bigr)+J(t)\cdot C(t)\bigr]\Bigr).
\right.
\tag{3.10}
```

In the sliced form (3.9) the source adds $`i\,\Delta t\sum_{k=0}^NJ(t_k)\cdot C(t_k)`$ to the exponent, so $`J`$ enters only through $`J(t_0),\ldots,J(t_N)`$. For $`t_i<t<t_f`$ define

```math
\left.
\frac{\delta}{\delta J_a(t)}:=\lim_{N\to\infty}\frac{1}{\Delta t}\frac{\partial}{\partial J_a(t_k)},\qquad t_k\to t.
\right.
\tag{3.11}
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
\tag{3.12}
```


**Example: Free Particle in One Dimension**

Take $`n=1`$, $`V=0`$ in (3.1):

```math
\left.
L(x,y)=\frac12my^2,\qquad Q_i(t_i)=q_i,\qquad Q_f(t_f)=q_f.
\right.
\tag{3.13}
```

By (3.7)–(3.9), with $`C(t_0)=q_i`$, $`C(t_{N+1})=q_f`$ and $`\mathcal N_N=\bigl(\frac{m}{2\pi i\,\Delta t}\bigr)^{\frac{N+1}{2}}`$,

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
\tag{3.14}
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
\tag{3.15}
```

After $`C(t_1),\ldots,C(t_{j-1})`$, $`1\le j\le N`$:

```math
\left.
K(Q_f,Q_i)=\lim_{N\to\infty}\mathcal N_N\Bigl(\frac{2\pi i\,\Delta t}{m}\Bigr)^{\frac{j-1}{2}}\frac{1}{\sqrt j}
\int\prod_{k=j}^{N}dC(t_k)\,
e^{\frac{im}{2\Delta t}\left[\frac{\left(C(t_j)-q_i\right)^2}{j}+C^2(t_j)+2C^2(t_{j+1})+\cdots+2C^2(t_N)+q_f^2\right]}\,
e^{\frac{im}{2\Delta t}(-2)\left[C(t_j)C(t_{j+1})+\cdots+C(t_N)q_f\right]}.
\right.
\tag{3.16}
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
\tag{3.17}
```

which gives (3.16) with $`j+1`$; for $`j=N`$, $`C(t_{N+1})=q_f`$ and the bracket becomes $`\frac{(q_f-q_i)^2}{N+1}`$. Hence, with $`(N+1)\Delta t=t_f-t_i`$,

```math
\left.
\begin{aligned}
K(Q_f,Q_i)&=\lim_{N\to\infty}\Bigl(\frac{m}{2\pi i\,\Delta t}\Bigr)^{\frac{N+1}{2}}\Bigl(\frac{2\pi i\,\Delta t}{m}\Bigr)^{\frac N2}\frac{1}{\sqrt{N+1}}\,
e^{\frac{im\left(q_f-q_i\right)^2}{2(N+1)\Delta t}}\\
&=\boxed{\sqrt{\frac{m}{2\pi i\,(t_f-t_i)}}\;e^{\frac{im\left(q_f-q_i\right)^2}{2(t_f-t_i)}}.}
\end{aligned}
\right.
\tag{3.18}
```

This example shows why the prefactor $`\mathcal N_N`$ is included in the definition (3.7) of the path integral. The result (3.18) is finite, while by its definition $`\mathcal N_N`$ diverges as $`N\to\infty`$; without the prefactor, the remaining factor $`\bigl(\frac{2\pi i\,\Delta t}{m}\bigr)^{\frac N2}\frac{1}{\sqrt{N+1}}`$ in (3.18) tends to zero, and so would $`K(Q_f,Q_i)`$.

**Relation to Operator Quantization**

Let $`\hat H:=\sum_{a=1}^n\hat p_a^2/(2m_a)+V(\hat q)`$ with $`[\hat q_a,\hat p_b]=i\delta_{ab}`$ and $`\hat q_a|q\rangle=q_a|q\rangle`$, and let $`\hat U_S(t_f,t_i)=e^{-i\hat H(t_f-t_i)}`$ be its evolution operator (2.18). Then, with $`q_i=Q_i(t_i)`$ and $`q_f=Q_f(t_f)`$,

```math
\left.
\boxed{K(Q_f,Q_i)=\langle q_f|\hat U_S(t_f,t_i)|q_i\rangle=\langle q_f,t_f|q_i,t_i\rangle}
\right.
\tag{3.19}
```

in the Schrödinger and Heisenberg pictures respectively, where $`|q,t\rangle:=\hat U_S(t,0)^\dagger|q\rangle`$ satisfies $`\hat q_H(t)|q,t\rangle=q\,|q,t\rangle`$ by (2.23).

<br><br>

<a id="path-integrals-in-field-theory"></a>
### 3.2 Path Integrals in Quantum Field Theory

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
\tag{3.20}
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
\tag{3.21}
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
\tag{3.22}
```

In the path integral the field takes the place of the path: a path (3.21) is a classical field (1.44) restricted to $`[t_i,t_f]\times\mathbb R^3`$. Paths are therefore denoted by $`\phi`$, and the integrals below are over field configurations.

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
\tag{3.23}
```

- **Final configuration**:

```math
\left.
\begin{aligned}
\Phi_f:\{t_f\}\times\mathbb R^3&\to\mathrm{Conf},\\
(t_f,\mathbf x)&\mapsto\Phi_f(t_f,\mathbf x).
\end{aligned}
\right.
\tag{3.24}
```

- **Transition kernel**:

```math
\left.
\boxed{K(\Phi_f,\Phi_i):=\int_{\phi(t_i,\mathbf x)=\Phi_i(t_i,\mathbf x)}^{\phi(t_f,\mathbf x)=\Phi_f(t_f,\mathbf x)}\mathcal D\phi\,e^{iS[\phi]},}
\right.
\tag{3.25}
```

also written $`\int_{\Phi_i}^{\Phi_f}\mathcal D\phi\,e^{iS[\phi]}`$; the boundary conditions hold for every $`\mathbf x\in\mathbb R^3`$.

**Correlation Functions**

As in (3.19),

```math
\left.
K(\Phi_f,\Phi_i)=\langle\Phi_f|\hat U_S(t_f,t_i)|\Phi_i\rangle,
\right.
\tag{3.26}
```
 In operator quantization the vacuum expands in this basis, which defines the vacuum functional $`\Psi[\Phi]`$:

```math
\left.
|\mathrm{vac}\rangle=\int\mathcal D\Phi\,|\Phi\rangle\langle\Phi|\mathrm{vac}\rangle=\int\mathcal D\Phi\,|\Phi\rangle\,\Psi[\Phi],\qquad
\Psi[\Phi]:=\langle\Phi|\mathrm{vac}\rangle.
\right.
\tag{3.27}
```

Hence

```math
\left.
\begin{aligned}
K(\mathrm{vac}_f,\mathrm{vac}_i)&:=\langle\mathrm{vac}_f|\hat U_S(t_f,t_i)|\mathrm{vac}_i\rangle\\
&=\int\mathcal D\Phi_f\,\mathcal D\Phi_i\,\Psi^*[\Phi_f]\,\Psi[\Phi_i]\,K(\Phi_f,\Phi_i).
\end{aligned}
\right.
\tag{3.28}
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
\tag{3.29}
```

with $`t_i<x_k^0<t_f`$. 

上述定义中的分母源自于对真空归一化的要求，在上述定义下，<1>=真空的模=1

- **Generating functional**: for a source $`J:[t_i,t_f]\times\mathbb R^3\to\mathbb R^n`$, with $`J\cdot\phi`$ as in (3.10),

```math
\left.
K^J(\Phi_f,\Phi_i):=\int_{\Phi_i}^{\Phi_f}\mathcal D\phi\,\exp\Bigl(iS[\phi]+i\int d^4x\,J(x)\cdot\phi(x)\Bigr),
\right.
\tag{3.30}
```

and, with the vacuum endpoints as in (3.28),

```math
\left.
\boxed{
Z[J]:=K^J(\mathrm{vac}_f,\mathrm{vac}_i)
=\int\mathcal D\Phi_f\,\mathcal D\Phi_i\,\Psi^*[\Phi_f]\,\Psi[\Phi_i]\,K^J(\Phi_f,\Phi_i),}
\right.
\tag{3.31}
```

so that $`Z[0]=K(\mathrm{vac}_f,\mathrm{vac}_i)`$.

As in (3.12), each $`\delta/\delta J_a(x)`$ acting on (3.30) brings down $`i\phi_a(x)`$, so by (3.31) and (3.29)

```math
\left.
\boxed{G_{a_1\cdots a_r}(x_1,\ldots,x_r)=\frac{1}{Z[0]}\left.\Bigl(-i\frac{\delta}{\delta J_{a_1}(x_1)}\Bigr)\cdots\Bigl(-i\frac{\delta}{\delta J_{a_r}(x_r)}\Bigr)Z[J]\right|_{J=0}.}
\right.
\tag{3.32}
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
\tag{3.33}
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
\tag{3.34}
```

For a translation-invariant scalar functional measure, with functional boundary terms absent,

```math
\left.
\left[
\left.\frac{\delta S}{\delta\phi(x)}\right|_{\phi\,\to\,(1/i)\delta/\delta J}
+J(x)\right]Z[J]=0.
\right.
\tag{3.35}
```

**Euclidean Continuation and Fermions**

When the time contour can be rotated without crossing singularities, $`t=-i\tau`$ gives, for $`\mathcal L=\tfrac12\partial_\mu\phi\partial^\mu\phi-V(\phi)`$,

```math
\left.
e^{iS}\longrightarrow e^{-S_E},\qquad
S_E=\int d\tau\,d^3x\left[\frac12(\partial_\tau\phi)^2
+\frac12(\boldsymbol\nabla\phi)^2+V(\phi)\right].
\right.
\tag{3.36}
```

Fermionic fields in the functional integral are independent Grassmann variables. With a fixed measure ordering, a quadratic Dirac action gives

```math
\left.
\int\mathcal D\bar\psi\,\mathcal D\psi\,
e^{i\int d^4x\,\bar\psi(i\gamma^\mu\partial_\mu-m)\psi}\ \propto\ \det(i\gamma^\mu\partial_\mu-m),
\right.
\tag{3.37}
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
\tag{3.38}
```

For an Abelian gauge field in this linear gauge, the determinant is field independent and the ghosts decouple. This local perturbative construction does not resolve global gauge-copy ambiguities.

<br><br>

<a id="phi-cubed-theory"></a>
### 3.3 $`\phi^3`$ Theory

**Action**

Take $`n=1`$, $`\mathrm{Conf}=\mathbb R`$ and $`V(\phi)=\frac12m^2\phi^2+\frac1{3!}\lambda\phi^3`$ in (3.20). With $`\Box:=\partial_\mu\partial^\mu`$ as in (1.97),

```math
\left.
\begin{aligned}
S[\phi]&=\int d^4x\,\mathcal L\bigl(\phi(x),\partial_\mu\phi(x)\bigr)\\
&=\int d^4x\,\Bigl[\frac12\partial_\mu\phi\,\partial^\mu\phi-\frac12m^2\phi^2-\frac1{3!}\lambda\phi^3\Bigr]\\
&=\int d^4x\,\Bigl[-\frac12\phi(\Box+m^2)\phi-\frac1{3!}\lambda\phi^3\Bigr]
+\frac12\int d^3x\,\bigl[\phi\,\partial_0\phi\bigr]_{x^0=t_i}^{x^0=t_f}.
\end{aligned}
\right.
\tag{3.39}
```

$`S_0[\phi]`$ denotes (3.39) at $`\lambda=0`$.

**Feynman Propagator**

```math
\left.
\begin{aligned}
(\Box+m^2)\Delta_F(x)&=-i\delta^{(4)}(x),\\
\Delta_F(x)&=\int\frac{d^4p}{(2\pi)^4}\,\frac{-i}{-p^2+m^2-i\varepsilon}\,e^{-ip\cdot x}
=\int\frac{d^4p}{(2\pi)^4}\,\frac{i}{p^2-m^2+i\varepsilon}\,e^{-ip\cdot x},
\end{aligned}
\right.
\tag{3.40}
```

with $`\varepsilon\to0^+`$; this is the function (4.12).

**Free Generating Functional**

From here on $`\mathrm{vac}`$ is the vacuum of $`S_0`$, and $`J`$ vanishes near $`x^0=t_i`$ and $`x^0=t_f`$. Let

```math
\left.
K_0^J(\Phi_f,\Phi_i):=\int_{\Phi_i}^{\Phi_f}\mathcal D\phi\,\exp\Bigl(iS_0[\phi]+i\int d^4x\,J(x)\phi(x)\Bigr),
\qquad K_0:=K_0^J\big|_{J=0}.
\right.
\tag{3.41}
```

In $`K_0^J(\mathrm{vac}_f,\mathrm{vac}_i)`$ shift the paths, together with $`\Phi_f`$ and $`\Phi_i`$, by

```math
\left.
\phi(x)\to\phi(x)+i\int d^4y\,\Delta_F(x-y)J(y),
\right.
\tag{3.42}
```

which leaves the measures in (3.28) unchanged. By (3.40), the integrand of $`\int d^4x`$ in the exponent becomes

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
\tag{3.43}
```

where the first underbrace holds after integrating by parts in $`x`$, up to terms at $`x^0=t_i,t_f`$. Write $`\chi(x):=i\int d^4y\,\Delta_F(x-y)J(y)`$ for the shift (3.42), so that $`(\Box+m^2)\chi=J`$ by (3.40). Including the terms at $`x^0=t_i,t_f`$ from (3.39) and from this integration by parts, the exponent of (3.41) after the shift is exactly

```math
\left.
\begin{aligned}
iS_0[\phi+\chi]+i\int d^4x\,J(\phi+\chi)
&=iS_0[\phi]-\frac12\int d^4x\,d^4y\,J(x)\Delta_F(x-y)J(y)\\
&\quad+i\int d^3x\,\Bigl[\bigl(\phi+\tfrac12\chi\bigr)\partial_0\chi\Bigr]_{x^0=t_i}^{x^0=t_f}.
\end{aligned}
\right.
\tag{3.44}
```

Closing the $`p^0`$ contour of (3.40) in the lower half-plane for $`x^0>0`$ and in the upper half-plane for $`x^0<0`$, around the poles $`p^0=\pm(E_{\mathbf p}-i\varepsilon')`$ with $`E_{\mathbf p}`$ as in (2.33) and $`\varepsilon'\to0^+`$,

```math
\left.
\Delta_F(x)=\int\frac{d^3p}{(2\pi)^3\,2E_{\mathbf p}}\,e^{i\mathbf p\cdot\mathbf x-iE_{\mathbf p}|x^0|}.
\right.
\tag{3.45}
```

Let $`\mathcal E:=(-\nabla^2+m^2)^{1/2}`$, i.e. $`\mathcal E\,e^{i\mathbf p\cdot\mathbf x}=E_{\mathbf p}\,e^{i\mathbf p\cdot\mathbf x}`$. Since $`J`$ vanishes near $`t_i`$ and $`t_f`$, (3.45) gives

```math
\left.
\partial_0\chi\big|_{x^0=t_f}=-i\mathcal E\chi\big|_{x^0=t_f},\qquad
\partial_0\chi\big|_{x^0=t_i}=+i\mathcal E\chi\big|_{x^0=t_i},
\right.
\tag{3.46}
```

so $`\chi`$ has only positive frequencies at $`t_f`$ and only negative frequencies at $`t_i`$.

For $`S_0`$ the vacuum is $`|0\rangle`$ of (2.34). At $`t=0`$ the Schrödinger-picture operators are $`\hat\phi(\mathbf x)=\hat\phi_I(0,\mathbf x)`$ and $`\hat\pi(\mathbf x)=\partial_0\hat\phi_I(0,\mathbf x)`$ by (4.2) and (1.92). Inverting (2.33), and acting with $`\hat\pi(\mathbf x)`$ as $`-i\,\delta/\delta\Phi(\mathbf x)`$ on $`\Psi[\Phi]=\langle\Phi|0\rangle`$,

```math
\left.
\begin{aligned}
\hat a_{\mathbf p}&=\int d^3x\,e^{-i\mathbf p\cdot\mathbf x}\bigl[E_{\mathbf p}\hat\phi(\mathbf x)+i\hat\pi(\mathbf x)\bigr],\\
0=\langle\Phi|\hat a_{\mathbf p}|0\rangle&=\int d^3x\,e^{-i\mathbf p\cdot\mathbf x}\Bigl[(\mathcal E\Phi)(\mathbf x)+\frac{\delta}{\delta\Phi(\mathbf x)}\Bigr]\Psi[\Phi]\quad\text{for all }\mathbf p,\\
\Psi[\Phi]&=\Psi[0]\exp\Bigl(-\frac12\int d^3x\,\Phi\,\mathcal E\,\Phi\Bigr),
\end{aligned}
\right.
\tag{3.47}
```

where the second line uses $`\int d^3x\,f\,\mathcal E\,g=\int d^3x\,(\mathcal Ef)\,g`$ and states $`\delta\Psi/\delta\Phi(\mathbf x)=-(\mathcal E\Phi)(\mathbf x)\Psi[\Phi]`$. With $`\chi_{f,i}:=\chi(t_{f,i},\cdot\,)`$, the shift turns $`\Psi^*[\Phi_f]\Psi[\Phi_i]`$ into $`\Psi^*[\Phi_f+\chi_f]\Psi[\Phi_i+\chi_i]`$, while $`\phi(t_{f,i},\cdot\,)=\Phi_{f,i}`$. By (3.46) and (3.47),

```math
\left.
\begin{aligned}
i\int d^3x\,\Bigl[\bigl(\phi+\tfrac12\chi\bigr)\partial_0\chi\Bigr]_{x^0=t_i}^{x^0=t_f}
&=\int d^3x\,\Bigl[\bigl(\Phi_f+\tfrac12\chi_f\bigr)\mathcal E\chi_f+\bigl(\Phi_i+\tfrac12\chi_i\bigr)\mathcal E\chi_i\Bigr],\\
\ln\frac{\Psi^*[\Phi_f+\chi_f]\,\Psi[\Phi_i+\chi_i]}{\Psi^*[\Phi_f]\,\Psi[\Phi_i]}
&=-\int d^3x\,\Bigl[\bigl(\Phi_f+\tfrac12\chi_f\bigr)\mathcal E\chi_f+\bigl(\Phi_i+\tfrac12\chi_i\bigr)\mathcal E\chi_i\Bigr],
\end{aligned}
\right.
\tag{3.48}
```

so the terms at $`x^0=t_i,t_f`$ in (3.44) cancel the change of $`\Psi^*[\Phi_f]\Psi[\Phi_i]`$. Hence

```math
\left.
K_0^J(\mathrm{vac}_f,\mathrm{vac}_i)=K_0(\mathrm{vac}_f,\mathrm{vac}_i)\,
\exp\Bigl[-\frac12\int d^4x\,d^4y\,J(x)\Delta_F(x-y)J(y)\Bigr],
\right.
\tag{3.49}
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
\tag{3.50}
```

with $`Z_0[0]=K_0(\mathrm{vac}_f,\mathrm{vac}_i)`$ by (3.49).

**Two-Point Function**

For $`S_0`$ and $`t_i<z_1^0,z_2^0<t_f`$, by (3.32) and (3.50),

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
\tag{3.51}
```

**Perturbation Expansion**

By (3.12), each $`-i\,\delta/\delta J(z)`$ acting on (3.41) inserts $`\phi(z)`$, so

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
\tag{3.52}
```

With the vacuum of $`S_0`$ at both ends, (3.49) gives

```math
\left.
\boxed{
\begin{aligned}
K(\mathrm{vac}_f,\mathrm{vac}_i)
&=\sum_{m=0}^\infty\frac1{m!}\Bigl(\frac{\lambda}{3!}\Bigr)^m\prod_{k=1}^m\int d^4z_k\Bigl(\frac{\delta}{\delta J(z_k)}\Bigr)^3\\
&\qquad\exp\Bigl[-\frac12\int d^4x\,d^4y\,J(x)\Delta_F(x-y)J(y)\Bigr]\Big|_{J=0}\cdot K_0(\mathrm{vac}_f,\mathrm{vac}_i).
\end{aligned}}
\right.
\tag{3.53}
```

<br><br>

<a id="path-integrals-for-fermion-fields"></a>
### 3.4 Path Integrals for Fermion Fields

<a id="grassmann-algebra"></a>
#### Grassmann Algebra

**Algebra**

Let $`\mathbb K=\mathbb R`$ or $`\mathbb C`$.

- **Algebra**: a vector space $`\mathcal A`$ over $`\mathbb K`$ with a product

```math
\left.
\begin{aligned}
\mathcal A\times\mathcal A&\to\mathcal A,\\
(u,v)&\mapsto uv,
\end{aligned}
\right.
\tag{3.54}
```

that is bilinear: for all $`\alpha,\beta\in\mathbb K`$ and $`u,v,w\in\mathcal A`$,

```math
\left.
\begin{aligned}
u(\alpha v+\beta w)&=\alpha\,uv+\beta\,uw,\\
(\alpha v+\beta w)u&=\alpha\,vu+\beta\,wu.
\end{aligned}
\right.
\tag{3.55}
```

- **Unital algebra**: an algebra with an element $`1\in\mathcal A`$ such that $`1u=u=u1`$ for all $`u\in\mathcal A`$.
  - For $`\alpha\in\mathbb K`$, $`\alpha1`$ is written $`\alpha`$.
- **Associative algebra**: an algebra in which $`(uv)w=u(vw)`$ for all $`u,v,w\in\mathcal A`$.

**Generator**

- **Generated subalgebra**: for an associative unital algebra $`\mathcal A`$ over $`\mathbb K`$ and a subset $`\Sigma\subset\mathcal A`$ with elements $`u_a`$, the subalgebra generated by $`\Sigma`$ is

```math
\left.
\mathcal A(\Sigma):=\Bigl\{f_0+\sum_{k\ge1}\sum_{a_1,\ldots,a_k}f_{a_1\cdots a_k}\,u_{a_1}\cdots u_{a_k}\;:\;f_0,\,f_{a_1\cdots a_k}\in\mathbb K\Bigr\},
\right.
\tag{3.56}
```

where only finitely many coefficients are nonzero.

- **Generating set**: $`\Sigma`$ is a generating set of $`\mathcal A`$ if $`\mathcal A(\Sigma)=\mathcal A`$.

**Grassmann Algebra**

- **Grassmann (exterior) algebra**: an associative unital algebra over $`\mathbb K`$ with a generating set $`\{\zeta_1,\ldots,\zeta_n\}`$ such that

```math
\left.
\zeta_a\zeta_b+\zeta_b\zeta_a=0,\qquad a,b=1,\ldots,n,
\right.
\tag{3.57}
```

in particular $`\zeta_a^2=0`$. No further relations are imposed: every relation among the $`\zeta_a`$ follows from (3.57). The algebra is denoted $`\mathcal G(\zeta_1,\ldots,\zeta_n)`$, or $`\mathcal G_n`$.

- **Basis**: the ordered monomials $`1`$ and $`\zeta_{a_1}\cdots\zeta_{a_k}`$ with $`a_1<\cdots<a_k`$ are linearly independent over $`\mathbb K`$, and

```math
\left.
\begin{aligned}
\mathcal G_n&=\mathop{\rm span}\nolimits\,_{\mathbb K}\{1,\ \zeta_{a_1}\cdots\zeta_{a_k}\mid 1\le a_1<\cdots<a_k\le n\},\\
\dim_{\mathbb K}\mathcal G_n&=2^n.
\end{aligned}
\right.
\tag{3.58}
```

- **Expansion**: every $`f\in\mathcal G_n`$ has a unique expansion

```math
\left.
f=\sum_{k=0}^n\sum_{1\le a_1<\cdots<a_k\le n}f_{a_1\cdots a_k}\,\zeta_{a_1}\cdots\zeta_{a_k},\qquad f_{a_1\cdots a_k}\in\mathbb K,
\right.
\tag{3.59}
```

in which the $`k=0`$ term is $`f_0`$.

<br><br>

<a id="grassmann-calculus"></a>
#### Calculus on the Grassmann Algebra

<br><br>

<a id="symmetry-in-path-integrals"></a>
### 3.5 Symmetry in Path Integrals

<br><br>

<a id="scattering-theory-in-path-integrals"></a>
### 3.6 Scattering Theory in Path Integrals

<br><br>

<a id="qft-ch4"></a>
## 4. Scattering Theory

<a id="interaction-picture-dyson"></a>
<a id="perturbation-theory"></a>
<a id="interaction-picture"></a>
### 4.1 Interaction Picture

Let the Hamiltonian be

```math
\left.
\hat H=\hat H_0+\hat V
\right.
\tag{4.1}
```

The interaction picture evolves operators with $`\hat H_0`$ of (4.1) instead of $`\hat H`$:

```math
\left.
\boxed{
\begin{gathered}
\hat O_I(t):=e^{i\hat H_0t}\,\hat O_S\,e^{-i\hat H_0t},\\[4pt]
|\psi_I(t)\rangle:=e^{i\hat H_0t}\,|\psi_S(t)\rangle .
\end{gathered}
}
\right.
\tag{4.2}
```

The three pictures coincide at $`t=0`$, and $`\langle\psi_I(t)|\hat O_I(t)|\psi_I(t)\rangle=\langle\psi_S(t)|\hat O_S|\psi_S(t)\rangle`$.

Differentiating the first of (4.2),

```math
\left.
\frac{d\hat O_I}{dt}=i\,[\hat H_0,\hat O_I].
\right.
\tag{4.3}
```

In particular $`\hat H_{0,I}=\hat H_0`$, while the interaction term becomes time dependent. Differentiating the second of (4.2) and using $`i\partial_t|\psi_S\rangle=\hat H|\psi_S\rangle`$,

```math
\left.
i\partial_t|\psi_I(t)\rangle
=e^{i\hat H_0t}\bigl(\hat H-\hat H_0\bigr)|\psi_S(t)\rangle
=e^{i\hat H_0t}\hat Ve^{-i\hat H_0t}\,|\psi_I(t)\rangle,
\right.
\tag{4.4}
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
\tag{4.5}
```

Substituting $`\hat O_S=e^{-i\hat H_0t}\hat O_I(t)e^{i\hat H_0t}`$ into (2.23),

```math
\left.
\hat O_H(t)=\hat U_I(t,0)^\dagger\,\hat O_I(t)\,\hat U_I(t,0),
\qquad
\hat U_I(t,0):=e^{i\hat H_0t}\,\hat U_S(t,0).
\right.
\tag{4.6}
```

For a field operator, (4.6) reads $`\hat\phi_H(t,\mathbf x)=\hat U_I(t,0)^\dagger\,\hat\phi_I(t,\mathbf x)\,\hat U_I(t,0)`$, and by (4.3) $`\hat\phi_I(t,\mathbf x)`$ obeys the Heisenberg equation of $`\hat H_0`$ alone.

**Dyson Series**

The state equation (4.5) is (2.3) with $`\hat H_S`$ replaced by $`\hat V_I(t)`$. The interaction-picture evolution operator $`\hat U_I(t,t_0)`$, defined by $`|\psi_I(t)\rangle=\hat U_I(t,t_0)|\psi_I(t_0)\rangle`$, is therefore $`\hat U_S(t,t_0)`$ of (2.18) with $`\hat H_S\to\hat V_I(t)`$: it is unitary, $`\hat U_I(t_1,t_2)\hat U_I(t_2,t_3)=\hat U_I(t_1,t_3)`$, and $`\hat U_I(t,t_0)^\dagger=\hat U_I(t_0,t)`$. By (4.2) and (2.18),

```math
\left.
\hat U_I(t,t_0)=e^{i\hat H_0t}\,\hat U_S(t,t_0)\,e^{-i\hat H_0t_0},
\right.
\tag{4.7}
```

which reduces to the $`\hat U_I(t,0)`$ of (4.6) at $`t_0=0`$; when $`\hat H`$ has no explicit time dependence, $`\hat U_S(t,t_0)=e^{-i\hat H(t-t_0)}`$ by (2.4). Since $`[\hat V_I(t_1),\hat V_I(t_2)]\neq0`$ in general, case (3) of [Section 2.1](#schrodinger-picture) applies, and by (2.11)

```math
\left.
\boxed{
\hat U_I(t,t_0)=\mathcal T\exp\Bigl(-i\int_{t_0}^{t}dt'\,\hat V_I(t')\Bigr).
}
\right.
\tag{4.8}
```

In field theory, $`\hat V=\int d^3x\,\hat{\mathcal H}_{\mathrm{int}}\bigl(\hat\phi_S(\mathbf x)\bigr)`$. By (4.2), $`\hat V_I(t)=\int d^3x\,\hat{\mathcal H}_{\mathrm{int}}\bigl(\hat\phi_I(t,\mathbf x)\bigr)`$, and (4.8) becomes

```math
\left.
\hat U_I(t,t_0)=\mathcal T\exp\Bigl(-i\int_{t_0}^{t}dt'\int d^3x\,\hat{\mathcal H}_{\mathrm{int}}\bigl(\hat\phi_I(x)\bigr)\Bigr).
\right.
\tag{4.9}
```

For interactions without derivative couplings, $`\hat{\mathcal H}_{\mathrm{int}}=-\hat{\mathcal L}_{\mathrm{int}}`$.

<br><br>

<a id="s-matrix-and-wick-theorem"></a>
### 4.2 The S-Matrix and Wick's Theorem

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
\tag{4.10}
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
\tag{4.11}
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
\tag{4.12}
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
\tag{4.13}
```

For fermions, time ordering and Wick contractions carry the sign of the required permutation of fermionic operators. Free-vacuum expectation values retain only fully contracted terms.


<br><br>

<a id="feynman-diagrams"></a>
### 4.3 Feynman Diagrams and Feynman Rules

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
\tag{4.14}
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
\tag{4.15}
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
\tag{4.16}
```

The $`\epsilon_\mu^r`$ are physical polarization vectors. External propagators are amputated; a general field normalization requires the pole-residue factors in [Section 4.5](#lsz-reduction).

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
\tag{4.17}
```

Loop integrals require a regulator and, in a renormalized amplitude, the corresponding counterterms. The full one-loop four-point amplitude also contains the crossed channels.


<br><br>

<a id="correlation-functions"></a>
### 4.4 Correlation Functions

<a id="perturbative-correlation-functions"></a>
#### Perturbative Vacuum Correlation Functions

**Vacuum Correlation Functions**

Let $`|\Omega\rangle`$ be the interacting vacuum and $`|0\rangle`$ the free vacuum.

```math
\left.
\begin{aligned}
G_n(x_1,\ldots,x_n)&:=\frac{\langle\Omega|\mathcal T[\hat\phi_H(x_1)\cdots\hat\phi_H(x_n)]|\Omega\rangle}{\langle\Omega|\Omega\rangle}\\
&=\frac{\langle0|\mathcal T\left[\hat\phi_I(x_1)\cdots\hat\phi_I(x_n)\exp\left(-i\int dt\,\hat V_I(t)\right)\right]|0\rangle}
{\langle0|\mathcal T\exp\left(-i\int dt\,\hat V_I(t)\right)|0\rangle}.
\end{aligned}
\right.
\tag{4.18}
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
\tag{4.19}
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
\tag{4.20}
```




<br><br>

<a id="nonperturbative-correlation-functions"></a>
#### Nonperturbative Vacuum Correlation Functions





<br><br>

<a id="lsz-reduction"></a>
### 4.5 LSZ Reduction Formula

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
\tag{4.21}
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
\tag{4.22}
```

The limit means extracting the simultaneous external-pole residue with the Feynman prescription before taking all external momenta on shell. Each factor removes one external propagator and its field overlap. A field normalized to unit pole residue has $`Z_{\mathrm{pole}}=1`$.


<br><br>

<a id="cross-sections-and-decay-rates"></a>
### 4.6 Cross Sections and Decay Rates

**Phase Space and State Sums**

For total final momentum $`P`$ and $`n`$ on-shell outgoing momenta $`k_j`$,

```math
\left.
d\Phi_n(P;k_1,\ldots,k_n):=(2\pi)^4\delta^{(4)}\left(P-\sum_{j=1}^{n}k_j\right)
\prod_{j=1}^{n}\frac{d^3k_j}{(2\pi)^3\,2E_{\mathbf k_j}},\qquad
E_{\mathbf k_j}=\sqrt{\mathbf k_j^2+m_j^2}.
\right.
\tag{4.23}
```

Use $`\overline{|\mathcal M|^2}`$ for the sum over unobserved final spins and internal quantum numbers, averaged over the equally populated initial states. For two unpolarized initial particles with $`N_1,N_2`$ such states,

```math
\left.
\overline{|\mathcal M|^2}:=\frac1{N_1N_2}\sum_{\text{initial, final states}}|\mathcal M|^2,
\qquad C_{\mathrm{id}}:=\prod_a\nu_a!.
\right.
\tag{4.24}
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
\tag{4.25}
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
\tag{4.26}
```

For the decay formulas, $`|\mathbf k_1|`$ is evaluated in the parent's rest frame. The solid-angle integrals use the same identical-particle counting convention as the full phase space.


<br><br>

<a id="qft-ch5"></a>
## 5. The Standard Model

<a id="yang-mills"></a>
### 5.1 Yang–Mills Theory


<a id="lie-group"></a>
#### Lie Group

```math
\left.
\begin{aligned}
U(n)&=\{A\in M_n(\mathbb C)\mid A^\dagger A=I\},\\[6pt]
SU(n)&=\{A\in M_n(\mathbb C)\mid \det A=1,\ A^\dagger A=I\}.
\end{aligned}
\right.
\tag{5.1}
```


**$`\mathfrak{u}(n)`$**

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
\tag{5.2}
```

 The Lie algebra is

```math
\left.
\mathfrak{u}(n)=\{iT\in M_n(\mathbb C)\mid T^\dagger=T\}.
\right.
\tag{5.3}
```

Hermiticity $`T^\dagger=T`$ means $`T_{jj}\in\mathbb R`$ and $`T_{kj}=T_{jk}^*`$ for $`j<k`$, i.e. $`n+2\cdot\frac{n(n-1)}{2}=n^2`$ real conditions on the $`2n^2`$ real parameters of $`M_n(\mathbb C)`$. Hence $`\dim\mathfrak{u}(n)=2n^2-n^2=n^2`$.


**$`\mathfrak{su}(n)`$**

The one-parameter subgroup and its generator are

```math
\left.
\begin{aligned}
g(\theta)&=e^{i\theta T},\qquad \theta\in\mathbb R,\quad T\in M_n(\mathbb C),\\[6pt]
\left.\frac{d}{d\theta}g(\theta)\right|_{\theta=0}&=iT.
\end{aligned}
\right.
\tag{5.4}
```


```math
\left.
0=\left.\frac{d}{d\theta}\bigl[g^\dagger(\theta)g(\theta)\bigr]\right|_{\theta=0}
=i(T-T^\dagger)
\quad\Longrightarrow\quad T^\dagger=T.
\right.
\tag{5.5}
```

We use the theorem $`\det(e^{i\theta T})=e^{i\theta\,\mathop{\rm tr}\nolimits\,T}`$, valid for any $`T\in M_n(\mathbb C)`$ and $`\theta\in\mathbb C`$.

```math
\left.
0=\left.\frac{d}{d\theta}\det g(\theta)\right|_{\theta=0}
=\left.\frac{d}{d\theta}e^{i\theta\,\mathop{\rm tr}\nolimits\,T}\right|_{\theta=0}
=i\,\mathop{\rm tr}\nolimits\,T
\quad\Longrightarrow\quad \mathop{\rm tr}\nolimits\,T=0.
\right.
\tag{5.6}
```

Thus $`T`$ is traceless and Hermitian, and the Lie algebra is

```math
\left.
\mathfrak{su}(n)=\{iT\in M_n(\mathbb C)\mid
\mathop{\rm tr}\nolimits\,T=0,\ T^\dagger=T\}.
\right.
\tag{5.7}
```

Since $`\mathop{\rm tr}\nolimits\,T=\sum_jT_{jj}\in\mathbb R`$ for Hermitian $`T`$, tracelessness $`\mathop{\rm tr}\nolimits\,T=0`$ is one further real condition. Hence $`\dim\mathfrak{su}(n)=2n^2-n^2-1=n^2-1`$.

Scalar multiplication is taken over $`\mathbb R`$ to preserve anti-Hermiticity; hence $`\mathfrak{su}(n)`$ and  $`\mathfrak{u}(n)`$ are both real Lie algebras.




<a id="ym-4"></a>
<div style="margin-left: 2em;">

$`\circ`$ Structure Constants $`f^{abc}`$

Let $`\{iT^a\}`$, with $`a=1,\ldots,n^2-1`$, be a basis of the real Lie algebra $`\mathfrak{su}(n)`$.
The structure constants $`f^{abc}`$ are defined by $`[T^a,T^b]=if^{abc}T^c`$.

**Claim.** $`f^{abc}\in\mathbb R`$.

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
\tag{5.8}
```

The expansion coefficients are real because $`\{iT^c\}`$ is a basis over $`\mathbb R`$.

</div>

<div style="margin-left: 2em;">

$`\circ`$ Inner Product on $`\mathfrak{su}(n)`$

For $`iT_1,iT_2\in\mathfrak{su}(n)`$, define

```math
\left.
\begin{aligned}
(\cdot,\cdot)&:\mathfrak{su}(n)\times\mathfrak{su}(n)\longrightarrow\mathbb R,\\[6pt]
(iT_1,iT_2)&:=-2\,\mathop{\rm tr}\nolimits \bigl[(iT_1)(iT_2)\bigr]\\
&=2\,\mathop{\rm tr}\nolimits (T_1T_2).
\end{aligned}
\right.
\tag{5.9}
```

**Proof** that (5.9) satisfies the axioms of an inner product



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
\tag{5.10}
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
\tag{5.11}
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
\tag{5.12}
```

Equality holds if and only if $`T_{jk}=0`$ for all $`j,k`$, i.e. $`iT=0`$. $`\square`$

</div>

<a id="ym-orthonormal"></a>
<div style="margin-left: 2em;">

$`\circ`$ Orthonormal Basis of $`\mathfrak{su}(n)`$ and Total Antisymmetry of $`f^{abc}`$

Since (5.9) is an inner product on $`\mathfrak{su}(n)`$, we may choose an orthonormal basis $`\{iT^a\}`$ satisfying $`(iT^a,iT^b)=\delta^{ab}`$. Equivalently,

```math
\left.
\boxed{\mathop{\rm tr}\nolimits (T^aT^b)=\frac12\delta^{ab}.}
\right.
\tag{5.13}
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
\tag{5.14}
```

```math
\left.
\boxed{
f^{abc}=f^{[abc]}\in\mathbb R
}
\right.
\tag{5.15}
```

</div>

<br><br>

<a id="ym-5"></a>
<a id="local-gauge-symmetry"></a>
#### Local Gauge Symmetry

Fiber bundles provide a useful geometric picture of fields in Yang–Mills theory.
In this picture, an internal space is a fiber which is attached to each spacetime point, and the field takes its value in that fiber.
This makes an additional freedom explicit: we may choose a basis in each fiber,
and this choice can vary from point to point.
It is this local freedom of choice that leads to the  gauge symmetry.

Building on this idea, we now develop the framework of gauge theory below.

The field operator is defined as

```math
\left.
\Psi(x):=\begin{pmatrix}
\psi_1(x)\\
\vdots\\
\psi_n(x)
\end{pmatrix},
\right.
\tag{5.16}
```

where each $`\psi_J`$ is a Dirac spinor and $`J=1,\ldots,n`$ is the index of the internal space, e.g. color, generation.

Define the Dirac adjoint by

```math
\left.
\begin{aligned}
\bar\Psi(x)&:=\bigl(\bar\psi_1(x),\ldots,\bar\psi_n(x)\bigr),\\[6pt]
\bar\psi_J(x)&:=\psi_J^\dagger(x)\gamma^0.
\end{aligned}
\right.
\tag{5.17}
```

The Lagrangian density contains the kinetic term

```math
\left.
\mathcal L\supset\bar\Psi\,i\gamma^\mu I_n\partial_\mu\Psi=\sum_{J=1}^{n}\bar\psi_J\,i\gamma^\mu\partial_\mu\psi_J.
\right.
\tag{5.18}
```



Let $`R`$ be the representation of $`SU(n)`$ on the internal space. Let $`g_{\mathrm{YM}}`$ be the coupling and $`R(\theta)`$ the representation of the local group element.

To compare fields in different internal spaces, we need to establish a relation between these internal spaces.

- **Wilson line**: for a path $`C:[0,1]\to\mathbb R^4`$ from $`C(0)=x`$ to $`C(1)=y`$, the Wilson line along $`C`$ maps the internal space at $`x`$ to that at $`y`$:

```math
\left.
W_C(y,x):=\mathcal P\exp\Bigl(ig_{\mathrm{YM}}\int_0^1ds\,\dot C^\mu(s)A_\mu\bigl(C(s)\bigr)\Bigr),
\right.
\tag{5.19}
```

where $`A_\mu:=A_\mu^aT^a`$, with $`A_\mu^a`$ real and $`T^a`$ the generators in the representation $`R`$, is the connection and $`\dot C^\mu:=dC^\mu/ds`$. In general, $`W_C(y,x)`$ depends on the path $`C`$, not only on its endpoints $`x`$ and $`y`$.

The path-ordered exponential is defined as $`\mathcal T\exp`$ in (2.12)–(2.13) with $`\tau\to s`$ and $`-i\hat H_S(\tau)\to ig_{\mathrm{YM}}\dot C^\mu(s)A_\mu(C(s))`$, so $`\mathcal P`$ puts factors with larger $`s`$ to the left.

Thus $`W_C(y,x)\Psi(x)`$ lies in the internal space at $`y`$, so under a gauge transformation we require it to transform like $`\Psi(y)`$:

```math
\left.
W_C(y,x)\Psi(x)\to R\bigl(\theta(y)\bigr)\,W_C(y,x)\Psi(x).
\right.
\tag{5.20}
```

Since $`\Psi(x)\to R\bigl(\theta(x)\bigr)\Psi(x)`$, the Wilson line must transform as

```math
\left.
W_C(y,x)\to R\bigl(\theta(y)\bigr)\,W_C(y,x)\,R\bigl(\theta(x)\bigr)^{-1}.
\right.
\tag{5.21}
```

- **Covariant derivative on fields in the representation $`R`$**: $`D_\mu:=\partial_\mu-ig_{\mathrm{YM}}A_\mu`$.

Under a gauge transformation, the covariant derivative transforms as

```math
\left.
D_\mu\Psi\to R(\theta)\,D_\mu\Psi,\qquad\text{i.e.}\qquad D_\mu\to R(\theta)\,D_\mu\,R(\theta)^{-1}.
\right.
\tag{5.22}
```

**Proof.** For an infinitesimal displacement $`\delta x^\mu`$ and the straight path $`C(s):=x+s\,\delta x`$, to first order in $`\delta x`$, (5.19) gives

```math
\left.
\begin{aligned}
W_C(x+\delta x,x)&=I_n+ig_{\mathrm{YM}}\,\delta x^\mu A_\mu(x),\\
\delta x^\mu D_\mu\Psi(x)&=\Psi(x+\delta x)-W_C(x+\delta x,x)\Psi(x).
\end{aligned}
\right.
\tag{5.23}
```

By (5.20), both terms on the right of the second line are multiplied by $`R(\theta(x+\delta x))=R(\theta(x))+O(\delta x)`$ under a gauge transformation, so $`\delta x^\mu D_\mu\Psi(x)\to R(\theta(x))\,\delta x^\mu D_\mu\Psi(x)`$ to first order. 
Since $`\delta x^\mu`$ is arbitrary, (5.22) follows. $`\square`$

Then, by (5.22), $`A_\mu`$ must transform as

```math
\left.
A_\mu\to R(\theta)\,A_\mu\,R(\theta)^{-1}-\frac{i}{g_{\mathrm{YM}}}\bigl(\partial_\mu R(\theta)\bigr)R(\theta)^{-1}.
\right.
\tag{5.24}
```

- **Field strength**: $`[D_\mu,D_\nu]=:-ig_{\mathrm{YM}}F_{\mu\nu}`$.

With $`F_{\mu\nu}=:F_{\mu\nu}^aT^a`$, this gives

```math
\left.
\begin{aligned}
F_{\mu\nu}&=\partial_\mu A_\nu-\partial_\nu A_\mu-ig_{\mathrm{YM}}[A_\mu,A_\nu],\\
F_{\mu\nu}^a&=\partial_\mu A_\nu^a-\partial_\nu A_\mu^a+g_{\mathrm{YM}}f^{abc}A_\mu^bA_\nu^c.
\end{aligned}
\right.
\tag{5.25}
```

Under a gauge transformation, the field strength transforms as

```math
\left.
F_{\mu\nu}\to R(\theta)\,F_{\mu\nu}\,R(\theta)^{-1}.
\right.
\tag{5.26}
```

**Proof.** By (5.22), $`[D_\mu,D_\nu]\to R(\theta)\,[D_\mu,D_\nu]\,R(\theta)^{-1}`$, and $`[D_\mu,D_\nu]=-ig_{\mathrm{YM}}F_{\mu\nu}`$. $`\square`$

 



Including the gauge field, a gauge-invariant extension of the kinetic term (5.18) is

```math
\left.
\boxed{
\mathcal L\supset\bar\Psi\,i\gamma^\mu D_\mu\Psi-\frac14F_{\mu\nu}^aF^{a\mu\nu}.
}
\right.
\tag{5.27}
```


- **Covariant derivative on adjoint fields**: for a matrix-valued field $`X`$ with $`X\to R(\theta)\,X\,R(\theta)^{-1}`$, such as $`F_{\mu\nu}`$, $`D_\mu X:=\partial_\mu X-ig_{\mathrm{YM}}[A_\mu,X]`$.

- **Equations of motion**: using the definitions above and $`j^\nu:=(\bar\Psi\gamma^\nu T^a\Psi)T^a`$, the field equations of (5.27) are

```math
\left.
\boxed{
\begin{aligned}
i\gamma^\mu D_\mu\Psi&=0,\\
D_\mu F^{\mu\nu}&=-g_{\mathrm{YM}}j^\nu.
\end{aligned}
}
\right.
\tag{5.28}
```

In addition, $`F_{\mu\nu}`$ satisfies the Bianchi identity $`D_\mu F_{\nu\rho}+D_\nu F_{\rho\mu}+D_\rho F_{\mu\nu}=0`$.

<br><br>

<a id="sm-fermions"></a>
### 5.2 Fermions and Bosons in the Standard Model

<a id="higgs-mechanism"></a>
<a id="higgs-lagrangian"></a>
#### General Higgs Lagrangian

Let $`\Phi:=(\phi_1,\ldots,\phi_n)^T`$ be a multiplet of complex scalar fields. 

For $`\mu_H^2\in\mathbb R`$ and $`\lambda_H>0`$, the Higgs Lagrangian is

```math
\left.
\boxed{
\begin{aligned}
\mathcal L_{\mathrm{Higgs}}&=(\partial_\mu\Phi)^\dagger\partial^\mu\Phi-V(\Phi),\\
V(\Phi)&=-\mu_H^2\,\Phi^\dagger\Phi+\lambda_H(\Phi^\dagger\Phi)^2 .
\end{aligned}
}
\right.
\tag{5.29}
```

The Lagrangian (5.29) depends on $`\Phi`$ only through $`\Phi^\dagger\Phi`$ and $`(\partial_\mu\Phi)^\dagger\partial^\mu\Phi`$. 

For a global gauge transformation $`U\in U(n)`$,

```math
\left.
\begin{aligned}
\Phi'&=U\,\Phi,\\
\Phi'^\dagger\Phi'&=\Phi^\dagger U^\dagger U\,\Phi=\Phi^\dagger\Phi,\\
(\partial_\mu\Phi')^\dagger\partial^\mu\Phi'&=(\partial_\mu\Phi)^\dagger U^\dagger U\,\partial^\mu\Phi=(\partial_\mu\Phi)^\dagger\partial^\mu\Phi,
\end{aligned}
\right.
\tag{5.30}
```

so $`\mathcal L_{\mathrm{Higgs}}`$ is invariant under global $`U(n)`$ transformations.










 - **Spontaneous Symmetry Breaking: Nonzero Vacuum Expectation Value**

The classical vacuum is the field configuration of minimum energy.

 The energy density of (5.29) is

```math
\left.
\mathcal H=(\partial_0\Phi)^\dagger\partial_0\Phi+\sum_{i=1}^3(\partial_i\Phi)^\dagger\partial_i\Phi+V(\Phi).
\right.
\tag{5.31}
```

The first two terms are nonnegative, so the classical vacuum is a constant $`\Phi=\Phi_0`$ minimizing $`V`$. 



Since $`\partial V/\partial(\Phi^\dagger\Phi)=-\mu_H^2+2\lambda_H\Phi^\dagger\Phi`$ and $`\Phi^\dagger\Phi\ge0`$,

```math
\left.
\boxed{
\begin{aligned}
\mu_H^2\le0:&\quad\Phi_0=0,\\
\mu_H^2>0:&\quad\Phi_0^\dagger\Phi_0=\frac{v_{\mathrm{SM}}^2}{2},\qquad
v_{\mathrm{SM}}:=\sqrt{\frac{\mu_H^2}{\lambda_H}},\qquad
V(\Phi_0)=-\frac{\lambda_Hv_{\mathrm{SM}}^4}{4}.
\end{aligned}
}
\right.
\tag{5.32}
```


For $`\mu_H^2\le0`$ the vacuum $`\Phi_0=0`$ is invariant under all of $`U(n)`$. 

From now on $`\mu_H^2>0`$: the vacua form the sphere $`\Phi_0^\dagger\Phi_0=v_{\mathrm{SM}}^2/2`$ in $`\mathbb C^n`$, and $`\Phi=0`$ is a local maximum of $`V`$.  
These vacua are degenerate. This degeneracy is called a symmetry-enforced vacuum degeneracy, as opposed to an accidental degeneracy, in which two vacua have the same energy but no symmetry protects this equality.

Physically, however, the vacuum must be unique, so in the mathematical description a physical vacuum has to be chosen by hand. We choose

```math
\left.
\boxed{
\Phi_0:=\frac1{\sqrt2}\begin{pmatrix}0\\\vdots\\0\\v_{\mathrm{SM}}\end{pmatrix}
}
\right.
\tag{5.33}
```

and from now on $`\Phi_0`$ denotes this vacuum.

This choice is arbitrary: any point of the sphere could serve as the physical vacuum.

If the degeneracy is symmetry-enforced, choosing the physical vacuum by hand breaks that symmetry: not all symmetries of the Lagrangian are symmetries of the physical vacuum. Here $`\mathcal L_{\mathrm{Higgs}}`$ is invariant under all of $`U(n)`$, but $`\Phi_0`$ is not. This is spontaneous symmetry breaking. 
 
 A symmetry transformation of the Lagrangian is unbroken if it leaves the physical vacuum invariant, and broken otherwise.


Broken generators are denoted $`G`$, and unbroken ones are still denoted $`T`$:

```math
\left.
\boxed{
\begin{aligned}
T\Phi_0&=0\qquad(\text{unbroken}),\\
G\Phi_0&\neq0\qquad(\text{broken}).
\end{aligned}
}
\right.
\tag{5.34}
```

The $`iT`$ with $`T`$ unbroken form a representation of $`\mathfrak u(n-1)`$, so in $`\mathop{\rm tr}\nolimits\,`$-orthonormal bases,

```math
\left.
\begin{aligned}
G^a\Phi_0&\neq0,\qquad a=1,\ldots,2n-1,\\
T^a\Phi_0&=0,\qquad a=2n,\ldots,n^2,\\
\mathop{\rm tr}\nolimits (G^aG^b)&=\mathop{\rm tr}\nolimits (T^aT^b)=\frac12\delta^{ab},\qquad\mathop{\rm tr}\nolimits (G^aT^b)=0 .
\end{aligned}
\right.
\tag{5.35}
```





Parametrize the $`2n`$ real fields of $`\Phi`$ by the Higgs field $`h`$ and $`\phi'^a`$, $`a=1,\ldots,2n-1`$, along the broken generators:

```math
\left.
\boxed{
\begin{aligned}
\Phi&=\frac1{\sqrt2}\,e^{i\phi'^a(x)G^a}\begin{pmatrix}0\\\vdots\\0\\v_{\mathrm{SM}}+h\end{pmatrix} .
\end{aligned}
}
\right.
\tag{5.36}
```

<a id="higgs-mechanism-masses"></a>
**Higgs Mechanism**

Gauge the $`U(n)`$ symmetry (5.30) with the generators $`T^a`$, $`a=1,\ldots,n^2`$, of (5.35) (with $`T^a:=G^a`$ for $`a\le2n-1`$), gauge fields $`A_\mu^a`$, and coupling $`g_{\mathrm{YM}}`$ as in (5.22)–(5.24). Replacing $`\partial_\mu`$ by $`D_\mu`$ in (5.29) and adding the gauge kinetic term of (5.27),

```math
\left.
\boxed{
\begin{aligned}
\mathcal L&=(D_\mu\Phi)^\dagger D^\mu\Phi-V(\Phi)-\frac14F_{\mu\nu}^aF^{a\mu\nu},\\
D_\mu\Phi&=\partial_\mu\Phi-ig_{\mathrm{YM}}A_\mu\Phi,\qquad A_\mu:=A_\mu^aT^a .
\end{aligned}
}
\right.
\tag{5.37}
```


Substitute the parametrization (5.36) into (5.37), written as $`\Phi=(1+h/v_{\mathrm{SM}})\,U(\phi')\Phi_0`$ with $`U(\phi'):=e^{i\phi'^aG^a}`$. With $`\mu_H^2=\lambda_Hv_{\mathrm{SM}}^2`$ from (5.32) and $`U(\phi')^\dagger U(\phi')=I_n`$, the potential depends only on $`h`$:

```math
\left.
\begin{aligned}
\Phi^\dagger\Phi&=\frac{(v_{\mathrm{SM}}+h)^2}2,\\
V&=\lambda_H\Bigl(\Phi^\dagger\Phi-\frac{v_{\mathrm{SM}}^2}2\Bigr)^2-\frac{\lambda_Hv_{\mathrm{SM}}^4}4\\
&=\lambda_Hv_{\mathrm{SM}}^2h^2+\lambda_Hv_{\mathrm{SM}}\,h^3+\frac{\lambda_H}4h^4-\frac{\lambda_Hv_{\mathrm{SM}}^4}4 .
\end{aligned}
\right.
\tag{5.38}
```

For the kinetic term, use $`\partial_\mu U(\phi')=U(\phi')\,U(\phi')^\dagger\partial_\mu U(\phi')`$. Since $`(\partial_\mu U(\phi')^\dagger)U(\phi')=-U(\phi')^\dagger\partial_\mu U(\phi')`$, $`A^{U(\phi')}_\mu`$ is Hermitian, so $`\Phi_0^\dagger A^{U(\phi')}_\mu\Phi_0`$ is real and the cross terms in $`(D_\mu\Phi)^\dagger D^\mu\Phi`$ cancel. With $`\Phi_0^\dagger\Phi_0=v_{\mathrm{SM}}^2/2`$,

```math
\left.
\begin{aligned}
D_\mu\Phi&=\frac{\partial_\mu h}{v_{\mathrm{SM}}}\,U(\phi')\Phi_0+\Bigl(1+\frac h{v_{\mathrm{SM}}}\Bigr)\bigl(\partial_\mu U(\phi')-ig_{\mathrm{YM}}A_\mu U(\phi')\bigr)\Phi_0\\
&=\frac{\partial_\mu h}{v_{\mathrm{SM}}}\,U(\phi')\Phi_0-ig_{\mathrm{YM}}\Bigl(1+\frac h{v_{\mathrm{SM}}}\Bigr)U(\phi')A^{U(\phi')}_\mu\Phi_0,\\
A^{U(\phi')}_\mu&:=U(\phi')^\dagger A_\mu U(\phi')+\frac i{g_{\mathrm{YM}}}U(\phi')^\dagger\partial_\mu U(\phi'),\\
(D_\mu\Phi)^\dagger D^\mu\Phi&=\frac12\partial_\mu h\,\partial^\mu h\\
&\quad+\Bigl(1+\frac h{v_{\mathrm{SM}}}\Bigr)^2g_{\mathrm{YM}}^2\,\Phi_0^\dagger A^{U(\phi')}_\mu A^{U(\phi')\mu}\Phi_0 .
\end{aligned}
\right.
\tag{5.39}
```

Substituting (5.38) and (5.39) into (5.37),

```math
\left.
\boxed{
\begin{aligned}
\mathcal L={}&\frac12\partial_\mu h\,\partial^\mu h-\frac12m_h^2h^2\\
&-\lambda_Hv_{\mathrm{SM}}\,h^3-\frac{\lambda_H}4h^4+\frac{\lambda_Hv_{\mathrm{SM}}^4}4\\
&+\Bigl(1+\frac h{v_{\mathrm{SM}}}\Bigr)^2g_{\mathrm{YM}}^2\,\Phi_0^\dagger A^{U(\phi')}_\mu A^{U(\phi')\mu}\Phi_0\\
&-\frac14F_{\mu\nu}^aF^{a\mu\nu},\\
m_h^2={}&2\lambda_Hv_{\mathrm{SM}}^2=2\mu_H^2 .
\end{aligned}
}
\right.
\tag{5.40}
```

Define the field $`A'_\mu`$ and its field strength by

```math
\left.
\begin{aligned}
A'_\mu&:=A^{U(\phi')}_\mu=U(\phi')^\dagger A_\mu U(\phi')+\frac i{g_{\mathrm{YM}}}U(\phi')^\dagger\partial_\mu U(\phi'),\\
F'_{\mu\nu}&:=\partial_\mu A'_\nu-\partial_\nu A'_\mu-ig_{\mathrm{YM}}[A'_\mu,A'_\nu]=U(\phi')^\dagger F_{\mu\nu}U(\phi') .
\end{aligned}
\right.
\tag{5.41}
```

Changing the field variables $`(\Phi,A_\mu)\to(h,\phi'^a,A'_\mu)`$ by (5.36) and (5.41), (5.40) becomes

```math
\left.
\boxed{
\begin{aligned}
\mathcal L={}&\frac12\partial_\mu h\,\partial^\mu h-\frac12m_h^2h^2\\
&-\lambda_Hv_{\mathrm{SM}}\,h^3-\frac{\lambda_H}4h^4+\frac{\lambda_Hv_{\mathrm{SM}}^4}4\\
&+\Bigl(1+\frac h{v_{\mathrm{SM}}}\Bigr)^2g_{\mathrm{YM}}^2\,\Phi_0^\dagger A'_\mu A'^\mu\Phi_0\\
&-\frac14F'^a_{\mu\nu}F'^{a\mu\nu} .
\end{aligned}
}
\right.
\tag{5.42}
```

With $`A'_\mu=A'^a_\mu T^a`$,  and $`T^a\Phi_0=0`$ for $`a\ge2n`$,

```math
\left.
\begin{aligned}
\mathcal L={}&\frac12\partial_\mu h\,\partial^\mu h-\frac12m_h^2h^2\\
&-\lambda_Hv_{\mathrm{SM}}\,h^3-\frac{\lambda_H}4h^4+\frac{\lambda_Hv_{\mathrm{SM}}^4}4\\
&+\frac12\Bigl(1+\frac h{v_{\mathrm{SM}}}\Bigr)^2\sum_{a,b=1}^{2n-1}(M^2)^{ab}A'^a_\mu A'^{b\mu}\\
&-\frac14F'^a_{\mu\nu}F'^{a\mu\nu},\\
(M^2)^{ab}:={}&g_{\mathrm{YM}}^2\,\Phi_0^\dagger\{G^a,G^b\}\Phi_0.
\end{aligned}
\right.
\tag{5.43}
```



<br><br>

<a id="sm-fermions-and-higgs"></a>
#### Fermions and the Higgs Boson in the Standard Model

| | Generation $`\alpha`$ | $`SU(2)_L`$ $`i`$ | Color $`c`$ |
|:---:|:---:|:---:|:---:|
| $`(\ell_L)_{\alpha i}`$ | $`1,2,3`$ | $`1,2`$ | $`1`$ |
| $`(E_R)_\alpha`$ | $`1,2,3`$ | $`1`$ | $`1`$ |
| $`(Q_L)_{\alpha ic}`$ | $`1,2,3`$ | $`1,2`$ | $`r,b,g`$ |
| $`(u_R)_{\alpha c}`$ | $`1,2,3`$ | $`1`$ | $`r,b,g`$ |
| $`(d_R)_{\alpha c}`$ | $`1,2,3`$ | $`1`$ | $`r,b,g`$ |
| $`H_i`$ | $`1`$ | $`1,2`$ | $`1`$ |

The index of a singlet (entry $`1`$) is not written explicitly.

The arbitrary choices in the Standard Model are fixed as follows.

- **Generators of $`SU(3)_c`$**: $`T_c^a=\frac{\lambda^a}2`$ on the color index $`c`$, where the Gell-Mann matrices $`\lambda^a`$ ($`a=1,\ldots,8`$) are

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
\lambda^8&=\frac1{\sqrt3}\begin{pmatrix}1&0&0\\0&1&0\\0&0&-2\end{pmatrix},
\end{aligned}
\right.
\tag{5.44}
```

with $`c=r,b,g`$ corresponding to their rows and columns $`1,2,3`$.

 Up to the antisymmetry (5.15), the nonzero structure constants in $`[T_c^a,T_c^b]=if^{abc}T_c^c`$ are

```math
\left.
\begin{aligned}
f^{123}&=1,\\[4pt]
f^{147}=f^{246}=f^{257}=f^{345}&=\tfrac12,\qquad
f^{156}=f^{367}=-\tfrac12,\\[4pt]
f^{458}=f^{678}&=\tfrac{\sqrt3}{2}.
\end{aligned}
\right.
\tag{5.45}
```

- **Generators of $`SU(2)_L`$**: $`T_L^a=\frac{\sigma^a}2`$ on the index $`i`$, where the Pauli matrices $`\sigma^a`$ ($`a=1,2,3`$) are

```math
\left.
\sigma^1=\begin{pmatrix}0&1\\1&0\end{pmatrix},\qquad
\sigma^2=\begin{pmatrix}0&-i\\i&0\end{pmatrix},\qquad
\sigma^3=\begin{pmatrix}1&0\\0&-1\end{pmatrix},
\right.
\tag{5.46}
```

so that $`[T_L^a,T_L^b]=i\epsilon^{abc}T_L^c`$.

- **Generator of $`U(1)_Y`$**: the hypercharge $`Y`$ are

| | $`\ell_L`$ | $`E_R`$ | $`Q_L`$ | $`u_R`$ | $`d_R`$ | $`H`$ |
|:---:|:---:|:---:|:---:|:---:|:---:|:---:|
| $`Y`$ | $`-\frac12`$ | $`-1`$ | $`\frac16`$ | $`\frac23`$ | $`-\frac13`$ | $`\frac12`$ |

- **Generators on the fields**: on the fields of the table, the generators of $`SU(3)_c`$, $`SU(2)_L`$ and $`U(1)_Y`$ are

```math
\left.
\begin{aligned}
\ell_L&:\quad T_c^a=I_i\otimes0\otimes I_\alpha, &
T_L^a&=\frac{\sigma^a}{2}\otimes I_c\otimes I_\alpha, &
Y&=-\frac12\,I_i\otimes I_c\otimes I_\alpha,\\
E_R&:\quad T_c^a=I_i\otimes0\otimes I_\alpha, &
T_L^a&=0\otimes I_c\otimes I_\alpha, &
Y&=-I_i\otimes I_c\otimes I_\alpha,\\
Q_L&:\quad T_c^a=I_i\otimes\frac{\lambda^a}{2}\otimes I_\alpha, &
T_L^a&=\frac{\sigma^a}{2}\otimes I_c\otimes I_\alpha, &
Y&=\frac16\,I_i\otimes I_c\otimes I_\alpha,\\
u_R&:\quad T_c^a=I_i\otimes\frac{\lambda^a}{2}\otimes I_\alpha, &
T_L^a&=0\otimes I_c\otimes I_\alpha, &
Y&=\frac23\,I_i\otimes I_c\otimes I_\alpha,\\
d_R&:\quad T_c^a=I_i\otimes\frac{\lambda^a}{2}\otimes I_\alpha, &
T_L^a&=0\otimes I_c\otimes I_\alpha, &
Y&=-\frac13\,I_i\otimes I_c\otimes I_\alpha,\\
H&:\quad T_c^a=I_i\otimes0\otimes I_\alpha, &
T_L^a&=\frac{\sigma^a}{2}\otimes I_c\otimes I_\alpha, &
Y&=\frac12\,I_i\otimes I_c\otimes I_\alpha,
\end{aligned}
\right.
\tag{5.47}
```

where $`I_i`$, $`I_c`$, $`I_\alpha`$ are the identities on the indices $`i`$, $`c`$, $`\alpha`$ (the number $`1`$ on a singlet), and $`0`$ is the generator on a singlet.

- **Signs of the couplings**: $`g_s,g_2,g_1>0`$ in the covariant derivative

```math
\left.
D_\mu=\partial_\mu-ig_sA_\mu^aT_c^a-ig_2W_\mu^aT_L^a-ig_1YB_\mu .
\right.
\tag{5.48}
```

- **Vacuum expectation value of $`H`$**:

```math
\left.
\langle H\rangle=\frac1{\sqrt2}\begin{pmatrix}0\\v_{\mathrm{SM}}\end{pmatrix},\qquad v_{\mathrm{SM}}>0,
\right.
\tag{5.49}
```

which is $`\Phi_0`$ of (5.33) with $`n=2`$.

the mass matrix of (5.43) in the basis $`(W'^1_\mu,W'^2_\mu,W'^3_\mu,B'_\mu)`$ is

```math
\left.
M^2=\frac{v_{\mathrm{SM}}^2}4\begin{pmatrix}g_2^2&0&0&0\\0&g_2^2&0&0\\0&0&g_2^2&-g_1g_2\\0&0&-g_1g_2&g_1^2\end{pmatrix}.
\right.
\tag{5.50}
```

<br><br>

<a id="field-redefinitions-and-flavor"></a>
#### Yukawa Coupling and Flavor

Besides the gauge interactions in the covariant derivative (5.48), the Lagrangian density contains the Yukawa terms, whose couplings $`Y_l,Y_d,Y_u`$ are complex $`3\times3`$ matrices carrying only the generation indices:

```math
\left.
\begin{aligned}
\mathcal L\supset{}&-\overline{(\ell_L)_\alpha}(Y_l)_{\alpha\beta}H(E_R)_\beta-\overline{(E_R)_\beta}(Y_l)^*_{\alpha\beta}H^\dagger(\ell_L)_\alpha\\
&-\overline{(Q_L)_\alpha}(Y_d)_{\alpha\beta}H(d_R)_\beta-\overline{(d_R)_\beta}(Y_d)^*_{\alpha\beta}H^\dagger(Q_L)_\alpha\\
&-\overline{(Q_L)_\alpha}(Y_u)_{\alpha\beta}H^c(u_R)_\beta-\overline{(u_R)_\beta}(Y_u)^*_{\alpha\beta}(H^c)^\dagger(Q_L)_\alpha,\\[6pt]
H^c:={}&i\sigma^2H^*=\begin{pmatrix}0&1\\-1&0\end{pmatrix}\begin{pmatrix}H_1^*\\H_2^*\end{pmatrix}=\begin{pmatrix}H_2^*\\-H_1^*\end{pmatrix},
\end{aligned}
\right.
\tag{5.51}
```

where $`H=(H_1,H_2)^T`$ in the index $`i`$ and the repeated $`\alpha,\beta`$ are summed.

Each Yukawa term in (5.51) is invariant under the $`SU(3)_c\times SU(2)_L\times U(1)_Y`$ gauge transformations.

For example, consider the term $`-\overline{(Q_L)_\alpha}(Y_u)_{\alpha\beta}H^c(u_R)_\beta`$. A gauge transformation acts on each field $`\psi`$ of (5.47) as $`\psi\to e^{i\theta_c^aT_c^a+i\theta_L^aT_L^a+i\theta_YY}\psi`$ with real $`\theta_c^a(x)`$, $`\theta_L^a(x)`$, $`\theta_Y(x)`$. 

With $`U_c:=e^{i\theta_c^a\lambda^a/2}`$ and $`U_L:=e^{i\theta_L^a\sigma^a/2}`$,

```math
\left.
\begin{aligned}
(Q_L)_\alpha&\to e^{\frac i6\theta_Y}(U_L\otimes U_c)(Q_L)_\alpha,\\
(u_R)_\beta&\to e^{\frac{2i}3\theta_Y}U_c(u_R)_\beta,\\
H&\to e^{\frac i2\theta_Y}U_LH,\\
H^c&\to i\sigma^2\bigl(e^{\frac i2\theta_Y}U_LH\bigr)^*=e^{-\frac i2\theta_Y}\bigl[i\sigma^2U_L^*(i\sigma^2)^\dagger\bigr]i\sigma^2H^*=e^{-\frac i2\theta_Y}U_LH^c,\\
\overline{(Q_L)_\alpha}H^c(u_R)_\beta&\to e^{i(-\frac16-\frac12+\frac23)\theta_Y}\,\overline{(Q_L)_\alpha}(U_L\otimes U_c)^\dagger(U_L\otimes U_c)H^c(u_R)_\beta=\overline{(Q_L)_\alpha}H^c(u_R)_\beta,
\end{aligned}
\right.
\tag{5.52}
```

where $`i\sigma^2U_L^*(i\sigma^2)^\dagger=U_L`$ because $`i\sigma^2(\sigma^a)^*(i\sigma^2)^\dagger=-\sigma^a`$ by (5.46).

With the generation indices written explicitly, the Lagrangian density of the Standard Model contains the fermion kinetic terms, with the covariant derivative (5.48) and the generators (5.47), and the Yukawa terms (5.51):

```math
\left.
\begin{aligned}
\mathcal L\supset{}&\overline{(\ell_L)_\alpha}\,i\gamma^\mu\Bigl(\partial_\mu-ig_2W_\mu^a\frac{\sigma^a}2+\frac i2g_1B_\mu\Bigr)(\ell_L)_\alpha\\
&+\overline{(E_R)_\alpha}\,i\gamma^\mu\bigl(\partial_\mu+ig_1B_\mu\bigr)(E_R)_\alpha\\
&+\overline{(Q_L)_\alpha}\,i\gamma^\mu\Bigl(\partial_\mu-ig_sA_\mu^a\frac{\lambda^a}2-ig_2W_\mu^a\frac{\sigma^a}2-\frac i6g_1B_\mu\Bigr)(Q_L)_\alpha\\
&+\overline{(u_R)_\alpha}\,i\gamma^\mu\Bigl(\partial_\mu-ig_sA_\mu^a\frac{\lambda^a}2-\frac{2i}3g_1B_\mu\Bigr)(u_R)_\alpha\\
&+\overline{(d_R)_\alpha}\,i\gamma^\mu\Bigl(\partial_\mu-ig_sA_\mu^a\frac{\lambda^a}2+\frac i3g_1B_\mu\Bigr)(d_R)_\alpha\\[6pt]
&-\overline{(\ell_L)_\alpha}(Y_l)_{\alpha\beta}H(E_R)_\beta-\overline{(E_R)_\beta}(Y_l)^*_{\alpha\beta}H^\dagger(\ell_L)_\alpha\\
&-\overline{(Q_L)_\alpha}(Y_d)_{\alpha\beta}H(d_R)_\beta-\overline{(d_R)_\beta}(Y_d)^*_{\alpha\beta}H^\dagger(Q_L)_\alpha\\
&-\overline{(Q_L)_\alpha}(Y_u)_{\alpha\beta}H^c(u_R)_\beta-\overline{(u_R)_\beta}(Y_u)^*_{\alpha\beta}(H^c)^\dagger(Q_L)_\alpha,
\end{aligned}
\right.
\tag{5.53}
```

where $`\sigma^a/2`$ acts on the index $`i`$, $`\lambda^a/2`$ on the index $`c`$, and the repeated $`\alpha,\beta`$ are summed.











- **Generation transformation**: with a constant $`S_\psi\in U(3)`$ for each field, acting only on the generation index,

```math
\left.
(\psi)_\alpha\to(S_\psi)_{\alpha\beta}(\psi)_\beta,\qquad\psi=\ell_L,E_R,Q_L,u_R,d_R .
\right.
\tag{5.54}
```

Inserting $`S_\psi S_\psi^\dagger=I_\alpha`$ into the kinetic and Yukawa terms of (5.53),

```math
\left.
\begin{aligned}
\overline{(\psi)_\alpha}\,i\gamma^\mu D_\mu(\psi)_\alpha
&=\overline{(\psi)_\alpha}(S_\psi S_\psi^\dagger)_{\alpha\beta}\,i\gamma^\mu D_\mu(\psi)_\beta
=\overline{(S_\psi^\dagger\psi)_\alpha}\,i\gamma^\mu D_\mu(S_\psi^\dagger\psi)_\alpha,\\
\overline{(\ell_L)_\alpha}(Y_l)_{\alpha\beta}H(E_R)_\beta
&=\overline{(\ell_L)_\alpha}(S_{\ell_L}S_{\ell_L}^\dagger Y_lS_{E_R}S_{E_R}^\dagger)_{\alpha\beta}H(E_R)_\beta\\
&=\overline{(S_{\ell_L}^\dagger\ell_L)_\alpha}(S_{\ell_L}^\dagger Y_lS_{E_R})_{\alpha\beta}H(S_{E_R}^\dagger E_R)_\beta,
\end{aligned}
\right.
\tag{5.55}
```

and likewise for the other terms of (5.51), where $`S_\psi^\dagger`$ commutes with $`i\gamma^\mu D_\mu`$ because $`S_\psi`$ is constant and acts only on the generation index. Replacing the fields by $`S_\psi\psi`$ as in (5.54) turns each $`S_\psi^\dagger\psi`$ into $`\psi`$, so the kinetic terms are unchanged and (5.51) keeps its form with the Yukawa matrices replaced by

```math
\left.
Y_l\to S_{\ell_L}^\dagger Y_lS_{E_R},\qquad Y_d\to S_{Q_L}^\dagger Y_dS_{d_R},\qquad Y_u\to S_{Q_L}^\dagger Y_uS_{u_R} .
\right.
\tag{5.56}
```

Since (5.54) only changes the field variables, Yukawa matrices related by (5.56) describe the same physics. The parametrization of the Yukawa interactions by $`Y_l,Y_d,Y_u`$ is therefore redundant: the number of physical parameters is smaller than the number of real parameters in $`Y_l,Y_d,Y_u`$.

**Parametrization of the Yukawa Couplings: Singular Value Decomposition**

<div style="margin-left: 2em;">

$`\circ`$ Leptons

By the singular value decomposition, the complex $`3\times3`$ matrix $`Y_l`$ can be written as

```math
\left.
Y_l=S_1\begin{pmatrix}y_1&0&0\\0&y_2&0\\0&0&y_3\end{pmatrix}S_2^\dagger,\qquad S_1,S_2\in U(3),\qquad 0\le y_1\le y_2\le y_3,
\right.
\tag{5.57}
```

where $`y_1^2,y_2^2,y_3^2`$ are the eigenvalues of $`Y_l^\dagger Y_l`$.

- **Orbit**: For fixed $`Y_{l,\mathrm{diag}}:=\mathop{\rm diag}\nolimits (y_1,y_2,y_3)`$, the orbit of $`Y_{l,\mathrm{diag}}`$ is the image of the map

```math
\left.
\begin{aligned}
\mathcal F_l: U(3)\times U(3)&\to M_3(\mathbb C),\\
(S_1,S_2)&\mapsto S_1Y_{l,\mathrm{diag}}S_2^\dagger,
\end{aligned}
\right.
\tag{5.58}
```

where $`M_3(\mathbb C)`$ is the space of complex $`3\times3`$ matrices, of real dimension $`18`$. The question is the real dimension of the orbit.

- **Stabilizer**: The subgroup of pairs $`(S_1,S_2)`$ with $`S_1Y_{l,\mathrm{diag}}S_2^\dagger=Y_{l,\mathrm{diag}}`$.

For $`0<y_1<y_2<y_3`$, the stabilizer condition and its Hermitian conjugate give $`S_1Y_{l,\mathrm{diag}}^2S_1^\dagger=Y_{l,\mathrm{diag}}^2=S_2Y_{l,\mathrm{diag}}^2S_2^\dagger`$. The diagonal entries of $`Y_{l,\mathrm{diag}}^2`$ are distinct, so $`S_1`$ and $`S_2`$ are diagonal, and since $`Y_{l,\mathrm{diag}}`$ is invertible, the stabilizer is

```math
\left.
S_1=S_2=\mathop{\rm diag}\nolimits (e^{i\varphi_1},e^{i\varphi_2},e^{i\varphi_3}),\qquad \varphi_k\in\mathbb R .
\right.
\tag{5.59}
```

The orbit is $`U(3)\times U(3)`$ modulo the stabilizer, so its real dimension is $`2\dim U(3)-3=18-3=15`$. The spectrum of $`Y_l^\dagger Y_l`$ fixes the ordered singular values, so by (5.57) every $`Y_l`$ belongs to exactly one orbit, and for $`0<y_1<y_2<y_3`$ the real parameters of $`Y_l`$ split as $`18=15+3`$: $`15`$ along the orbit and the $`3`$ singular values. When singular values coincide or vanish, the stabilizer is larger and the orbit has dimension less than $`15`$.

Under (5.56), $`S_{\ell_L}`$ and $`S_{E_R}`$ move $`Y_l`$ along its orbit. In particular, the generation transformation (5.54) with $`S_{\ell_L}=S_1`$ and $`S_{E_R}=S_2`$ gives

```math
\left.
\boxed{Y_l\to S_{\ell_L}^\dagger Y_lS_{E_R}=\begin{pmatrix}y_1&0&0\\0&y_2&0\\0&0&y_3\end{pmatrix}}\,.
\right.
\tag{5.60}
```

The $`15`$ real parameters along the orbit are therefore unphysical generation degrees of freedom, and $`Y_l`$ has $`3`$ physical parameters, $`y_1,y_2,y_3`$.

Excluding the unphysical generation degrees of freedom, what remains is flavor: for $`y_1<y_2<y_3`$ the three generations are physically distinct, and in the basis of (5.60), called the flavor basis, the generation index $`\alpha=1,2,3`$ of $`\ell_L`$ and $`E_R`$ labels the flavors $`e,\mu,\tau`$.

</div>

<div style="margin-left: 2em;">

$`\circ`$ Quarks

The matrices $`Y_d`$ and $`Y_u`$ have the singular value decompositions

```math
\left.
\begin{aligned}
Y_d&=S_3\begin{pmatrix}y_d&0&0\\0&y_s&0\\0&0&y_b\end{pmatrix}S_4^\dagger,&&0\le y_d\le y_s\le y_b,\\
Y_u&=S_5\begin{pmatrix}y_u&0&0\\0&y_c&0\\0&0&y_t\end{pmatrix}S_6^\dagger,&&0\le y_u\le y_c\le y_t,
\end{aligned}
\right.
\tag{5.61}
```

with $`S_3,S_4,S_5,S_6\in U(3)`$. Unlike $`Y_l`$, they share $`S_{Q_L}`$ in (5.56), which can remove only one of the left matrices $`S_3`$ and $`S_5`$. The generation transformation (5.54) with $`S_{Q_L}=S_3`$, $`S_{d_R}=S_4`$ and $`S_{u_R}=S_6`$ gives

```math
\left.
\boxed{Y_d\to\begin{pmatrix}y_d&0&0\\0&y_s&0\\0&0&y_b\end{pmatrix},\qquad Y_u\to V_{\mathrm{CKM}}^\dagger\begin{pmatrix}y_u&0&0\\0&y_c&0\\0&0&y_t\end{pmatrix}},\qquad V_{\mathrm{CKM}}:=S_5^\dagger S_3\in U(3).
\right.
\tag{5.62}
```

The generation transformations that keep the form (5.62) keep the diagonal matrices $`Y_dY_d^\dagger`$, $`Y_d^\dagger Y_d`$ and $`Y_u^\dagger Y_u`$, whose entries are distinct for $`0<y_d<y_s<y_b`$ and $`0<y_u<y_c<y_t`$, so $`S_{Q_L},S_{d_R},S_{u_R}`$ are diagonal; keeping $`Y_d`$ also requires $`S_{d_R}=S_{Q_L}`$. These transformations, and their action on $`V_{\mathrm{CKM}}`$ by (5.56), are

```math
\left.
\begin{aligned}
&S_{Q_L}=S_{d_R}=\mathop{\rm diag}\nolimits (e^{i\varphi_1},e^{i\varphi_2},e^{i\varphi_3}),\qquad S_{u_R}=\mathop{\rm diag}\nolimits (e^{i\varphi'_1},e^{i\varphi'_2},e^{i\varphi'_3}),\\
&(V_{\mathrm{CKM}})_{\alpha\beta}\to e^{i(\varphi_\beta-\varphi'_\alpha)}(V_{\mathrm{CKM}})_{\alpha\beta}.
\end{aligned}
\right.
\tag{5.63}
```

Of the $`9`$ real parameters of $`V_{\mathrm{CKM}}`$, $`3`$ angles and $`6`$ phases, (5.63) removes $`5`$ phases, since $`V_{\mathrm{CKM}}`$ is unchanged when all six $`\varphi_\alpha,\varphi'_\alpha`$ are equal. $`V_{\mathrm{CKM}}`$ therefore has $`3`$ angles and $`1`$ phase, and $`Y_d,Y_u`$ have $`6+4=10`$ physical parameters out of their $`36`$ real parameters; with the $`3`$ of $`Y_l`$, the Yukawa interactions (5.51) have $`13`$ physical parameters out of $`54`$.

In the basis of (5.62), the generation indices of $`d_R`$ and $`u_R`$ label the flavors $`d,s,b`$ and $`u,c,t`$, and that of $`Q_L`$ labels $`d,s,b`$ in $`Y_d`$; in $`Y_u`$, the flavors $`u,c,t`$ are labeled by the index of $`V_{\mathrm{CKM}}Q_L`$. Unless $`V_{\mathrm{CKM}}`$ is diagonal, the generation index of $`Q_L`$ cannot label the flavors of $`Y_d`$ and $`Y_u`$ at the same time.

</div>


















<br><br>

<a id="electroweak-gauge-theory"></a>
<a id="electroweak-theory"></a>
### 5.3 $`W^\pm`$, $`Z^0`$, $`\gamma`$: Electroweak Theory




<a id="qed"></a>
<a id="electroweak-gauge-symmetry"></a>
#### Gauge Symmetry $`SU(2)_L\times U(1)_Y`$



- **Generators and covariant derivative**: the generators $`T^a`$ ($`a=1,2,3`$) of $`SU(2)_L`$ and $`Y`$ of $`U(1)_Y`$ on the fields of [Section 5.2](#sm-fermions), and the covariant derivative, are

```math
\left.
\begin{aligned}
\ell_L&:\quad T^a=\frac{\sigma^a}{2}\otimes I_\alpha\otimes I_s, &
Y&=-\frac12\,I_i\otimes I_\alpha\otimes I_s,\\
E_R&:\quad T^a=0, &
Y&=-I_\alpha\otimes I_s,\\
Q_L&:\quad T^a=\frac{\sigma^a}{2}\otimes I_c\otimes I_\alpha\otimes I_s, &
Y&=\frac16\,I_i\otimes I_c\otimes I_\alpha\otimes I_s,\\
u_R&:\quad T^a=0, &
Y&=\frac23\,I_c\otimes I_\alpha\otimes I_s,\\
d_R&:\quad T^a=0, &
Y&=-\frac13\,I_c\otimes I_\alpha\otimes I_s,\\[6pt]
D_\mu&:=\partial_\mu-ig_2W_\mu^aT^a-ig_1YB_\mu,
\end{aligned}
\right.
\tag{5.64}
```

where $`\sigma^a/2`$ acts on the $`SU(2)_L`$ index $`i`$, and $`I_i`$, $`I_c`$, $`I_\alpha`$, $`I_s`$ are the identities on the indices $`i`$, $`c`$, $`\alpha`$, $`s`$. 

In $`D_\mu`$, $`W_\mu^a`$ and $`B_\mu`$ are the real $`SU(2)_L`$ and $`U(1)_Y`$ gauge fields, $`g_2,g_1>0`$ are the couplings, and $`T^a`$, $`Y`$ are those of the field on which $`D_\mu`$ acts.



<a id="electroweak-interaction"></a>
#### Interaction 

- **Electric charge, Weinberg angle and the fields $`W_\mu^\pm`$, $`Z_\mu`$, $`A_\mu^{\mathrm{em}}`$**: with $`T^a`$, $`Y`$ those of a field of (5.64),

```math
\left.
\begin{aligned}
Q&:=T^3+Y,\qquad T^\pm:=T^1\pm iT^2,\\
\tan\theta_W&:=\frac{g_1}{g_2},\qquad s_W:=\sin\theta_W=\frac{g_1}{\sqrt{g_1^2+g_2^2}},\qquad c_W:=\cos\theta_W=\frac{g_2}{\sqrt{g_1^2+g_2^2}},\\
e&:=g_2s_W=g_1c_W=\frac{g_1g_2}{\sqrt{g_1^2+g_2^2}},\\
W_\mu^\pm&:=\frac{W_\mu^1\mp iW_\mu^2}{\sqrt2},\qquad
\begin{pmatrix}Z_\mu\\A_\mu^{\mathrm{em}}\end{pmatrix}:=\begin{pmatrix}c_W&-s_W\\s_W&c_W\end{pmatrix}\begin{pmatrix}W_\mu^3\\B_\mu\end{pmatrix}.
\end{aligned}
\right.
\tag{5.65}
```

Thus $`Q=\mathop{\rm diag}\nolimits (0,-1)`$ on $`\ell_L`$, $`-1`$ on $`E_R`$, $`\mathop{\rm diag}\nolimits (\frac23,-\frac13)`$ on $`Q_L`$, $`\frac23`$ on $`u_R`$ and $`-\frac13`$ on $`d_R`$, where $`\mathop{\rm diag}\nolimits\,`$ acts on the index $`i`$ and each entry multiplies the identities on the other indices. 



The Lagrangian density contains the lepton and quark interaction terms

```math
\left.
\begin{aligned}
\mathcal L&\supset\overline{\ell_L}\gamma^\mu\Bigl(g_2W_\mu^a\frac{\sigma^a}2-\frac{g_1}2B_\mu\Bigr)\ell_L-g_1B_\mu\,\overline{E_R}\gamma^\mu E_R,\\
\mathcal L&\supset\overline{Q_L}\gamma^\mu\Bigl(g_2W_\mu^a\frac{\sigma^a}2+\frac{g_1}6B_\mu\Bigr)Q_L+\frac23g_1B_\mu\,\overline{u_R}\gamma^\mu u_R-\frac13g_1B_\mu\,\overline{d_R}\gamma^\mu d_R.
\end{aligned}
\right.
\tag{5.66}
```

Inverting (5.65), 

```math
\left.
\begin{aligned}
g_2W_\mu^aT^a+g_1YB_\mu
&=\frac{g_2}{\sqrt2}\bigl(W_\mu^+T^++W_\mu^-T^-\bigr)+A_\mu^{\mathrm{em}}\bigl(g_2s_WT^3+g_1c_WY\bigr)+Z_\mu\bigl(g_2c_WT^3-g_1s_WY\bigr)\\
&=\frac{g_2}{\sqrt2}\bigl(W_\mu^+T^++W_\mu^-T^-\bigr)+eQA_\mu^{\mathrm{em}}+\frac{g_2}{c_W}\bigl(T^3-s_W^2Q\bigr)Z_\mu .
\end{aligned}
\right.
\tag{5.67}
```

Write $`\ell_L=(\nu_L,l_L)^T`$ and $`Q_L=(u_L,d_L)^T`$ in the index $`i`$. Then $`\overline{\ell_L}\gamma^\mu T^+\ell_L=\overline{\nu_L}\gamma^\mu l_L`$ and $`\overline{Q_L}\gamma^\mu T^+Q_L=\overline{u_L}\gamma^\mu d_L`$, while $`T^\pm=T^3=0`$ on $`E_R`$, $`u_R`$, $`d_R`$. 

Since $`\bar\psi_1\gamma^\mu\psi_2=\overline{P_L\psi_1}\gamma^\mu P_L\psi_2+\overline{P_R\psi_1}\gamma^\mu P_R\psi_2`$ by (1.137), the $`A_\mu^{\mathrm{em}}`$ terms combine into the Dirac fields $`l:=l_L+E_R`$, $`u:=u_L+u_R`$ and $`d:=d_L+d_R`$. 

Substituting (5.67) into (5.66), the lepton terms are

```math
\left.
\boxed{
\begin{aligned}
\mathcal L\supset{}&\frac{g_2}{\sqrt2}\bigl(W_\mu^+\,\overline{\nu_L}\gamma^\mu l_L+W_\mu^-\,\overline{l_L}\gamma^\mu\nu_L\bigr)-eA_\mu^{\mathrm{em}}\,\bar l\gamma^\mu l\\
&+\frac{g_2}{c_W}Z_\mu\Bigl[\frac12\,\overline{\nu_L}\gamma^\mu\nu_L+\Bigl(-\frac12+s_W^2\Bigr)\overline{l_L}\gamma^\mu l_L+s_W^2\,\overline{E_R}\gamma^\mu E_R\Bigr],
\end{aligned}
}
\right.
\tag{5.68}
```

and the quark terms are

```math
\left.
\boxed{
\begin{aligned}
\mathcal L\supset{}&\frac{g_2}{\sqrt2}\bigl(W_\mu^+\,\overline{u_L}\gamma^\mu d_L+W_\mu^-\,\overline{d_L}\gamma^\mu u_L\bigr)+eA_\mu^{\mathrm{em}}\Bigl(\frac23\,\bar u\gamma^\mu u-\frac13\,\bar d\gamma^\mu d\Bigr)\\
&+\frac{g_2}{c_W}Z_\mu\Bigl[\Bigl(\frac12-\frac23s_W^2\Bigr)\overline{u_L}\gamma^\mu u_L-\frac23s_W^2\,\overline{u_R}\gamma^\mu u_R\\
&\qquad\qquad+\Bigl(-\frac12+\frac13s_W^2\Bigr)\overline{d_L}\gamma^\mu d_L+\frac13s_W^2\,\overline{d_R}\gamma^\mu d_R\Bigr].
\end{aligned}
}
\right.
\tag{5.69}
```








<a id="qcd"></a>
### 5.4 Gluon $`g`$: Quantum Chromodynamics

<a id="qcd-gauge-symmetry"></a>
#### Gauge Symmetry $`SU(3)_c`$

- **Generators and covariant derivative**: the generators $`T^a`$ ($`a=1,\ldots,8`$) of $`SU(3)_c`$ on the fields of [Section 5.2](#sm-fermions), and the covariant derivative, are

```math
\left.
\begin{aligned}
\ell_L&:\quad T^a=0,\\
E_R&:\quad T^a=0,\\
Q_L&:\quad T^a=I_i\otimes\frac{\lambda^a}{2}\otimes I_\alpha\otimes I_s,\\
u_R&:\quad T^a=\frac{\lambda^a}{2}\otimes I_\alpha\otimes I_s,\\
d_R&:\quad T^a=\frac{\lambda^a}{2}\otimes I_\alpha\otimes I_s,\\[6pt]
D_\mu&:=\partial_\mu-ig_sA_\mu^aT^a,
\end{aligned}
\right.
\tag{5.70}
```

where $`\lambda^a/2`$ acts on the color index $`c`$, and $`I_i`$, $`I_\alpha`$, $`I_s`$ are the identities on the indices $`i`$, $`\alpha`$, $`s`$.

In $`D_\mu`$, $`A_\mu^a`$ are the real $`SU(3)_c`$ gauge fields, $`g_s>0`$ is the coupling, and $`T^a`$ are those of the field on which $`D_\mu`$ acts.




The gauge group of QCD is $`SU(3)`$. By (5.7) with $`n=3`$, $`\mathfrak{su}(3)`$ has a basis $`\{iT^a\}`$, $`a=1,\ldots,8`$, which we take orthonormal in the sense of (5.13). The standard choice is $`T^a:=\tfrac12\lambda^a`$, where the Gell-Mann matrices are


Each $`\lambda^a`$ is Hermitian and traceless, and $`\mathop{\rm tr}\nolimits (\lambda^a\lambda^b)=2\delta^{ab}`$, so $`\mathop{\rm tr}\nolimits (T^aT^b)=\tfrac12\delta^{ab}`$ as in (5.13). By (5.14), $`f^{abc}=-2i\,\mathop{\rm tr}\nolimits ([T^a,T^b]T^c)`$; up to the antisymmetry (5.15), the nonzero structure constants are

The quadratic Casimir $`T^aT^a`$ commutes with every $`T^b`$, since $`f^{bac}`$ is antisymmetric in $`a,c`$:

```math
\left.
[T^b,T^aT^a]=[T^b,T^a]T^a+T^a[T^b,T^a]=if^{bac}\bigl(T^cT^a+T^aT^c\bigr)=0.
\right.
\tag{5.71}
```

The defining representation of $`SU(3)`$ is irreducible, so by Schur's lemma $`T^aT^a=C_FI_3`$. Taking the trace with (5.13),

```math
\left.
3C_F=\mathop{\rm tr}\nolimits (T^aT^a)=\tfrac12\cdot8
\quad\Longrightarrow\quad
\boxed{T^aT^a=C_FI_3,\qquad C_F=\tfrac43.}
\right.
\tag{5.72}
```

**Quark Fields**

For each flavor $`f\in\{u,d,s,c,b,t\}`$ the quark field is a color triplet, i.e. the multiplet (5.16) with $`n=3`$, with Dirac adjoint as in (5.17):

```math
\left.
q_f(x):=\begin{pmatrix}\psi_{f,1}(x)\\\psi_{f,2}(x)\\\psi_{f,3}(x)\end{pmatrix},
\qquad
\bar q_f(x):=\bigl(\bar\psi_{f,1}(x),\bar\psi_{f,2}(x),\bar\psi_{f,3}(x)\bigr).
\right.
\tag{5.73}
```

Throughout this section $`\gamma^\mu`$ acts on the spinor index of each $`\psi_{f,a}`$ and the $`3\times3`$ matrices $`T^a`$ act on the color index, so $`\gamma^\mu`$ commutes with every matrix built from the $`T^a`$.

**Local $`SU(3)`$ Transformation**

Let $`\theta^a:\mathbb R^4\to\mathbb R`$, $`a=1,\ldots,8`$, and set

```math
\left.
g(x):=e^{i\theta^a(x)T^a}\in SU(3).
\right.
\tag{5.74}
```

This is the internal transformation (1.72) with $`g`$ now depending on $`x`$. The quark fields transform as

```math
\left.
q_f'(x)=g(x)\,q_f(x),\qquad
\bar q_f'(x)=\bar q_f(x)\,g^\dagger(x).
\right.
\tag{5.75}
```

Since $`\partial_\mu(gq_f)=g\,\partial_\mu q_f+(\partial_\mu g)\,q_f`$, the derivative term of (5.18) is not invariant under (5.75):

```math
\left.
\bar q_f'\,i\gamma^\mu\partial_\mu q_f'
=\bar q_f\,i\gamma^\mu\partial_\mu q_f
+\bar q_f\,i\gamma^\mu g^\dagger(\partial_\mu g)\,q_f.
\right.
\tag{5.76}
```

**Covariant Derivative and Gluon Fields**

Introduce eight real vector fields $`A^a_\mu`$, the gluon fields, and define

```math
\left.
A_\mu:=A^a_\mu T^a,\qquad
D_\mu:=\partial_\mu-ig_sA_\mu,
\right.
\tag{5.77}
```

where $`g_s\in\mathbb R`$ is the strong coupling constant and $`D_\mu`$ acts on color triplets. Let $`A_\mu'`$ denote the transformed gluon field and $`D_\mu':=\partial_\mu-ig_sA_\mu'`$. We require $`D_\mu'q_f'=g\,D_\mu q_f`$:

```math
\left.
\begin{aligned}
D_\mu'(gq_f)&=g\,\partial_\mu q_f+(\partial_\mu g)\,q_f-ig_sA_\mu'\,g\,q_f,\\[6pt]
g\,D_\mu q_f&=g\,\partial_\mu q_f-ig_s\,gA_\mu\,q_f.
\end{aligned}
\right.
\tag{5.78}
```

Equating the two for all $`q_f`$ gives $`A_\mu'g=gA_\mu-\frac{i}{g_s}\partial_\mu g`$, i.e.

```math
\left.
\boxed{
A_\mu'=gA_\mu g^\dagger-\frac{i}{g_s}(\partial_\mu g)\,g^\dagger
=gA_\mu g^\dagger+\frac{i}{g_s}\,g\,\partial_\mu g^\dagger.
}
\right.
\tag{5.79}
```

Differentiating $`gg^\dagger=I_3`$ gives $`\bigl((\partial_\mu g)g^\dagger\bigr)^\dagger=-(\partial_\mu g)g^\dagger`$, and Jacobi's formula $`\partial_\mu\det g=\det g\,\mathop{\rm tr}\nolimits (g^\dagger\partial_\mu g)`$ with $`\det g=1`$ gives $`\mathop{\rm tr}\nolimits \bigl((\partial_\mu g)g^\dagger\bigr)=0`$. Hence $`A_\mu'`$ is again Hermitian and traceless, $`A_\mu'=A_\mu'^aT^a`$ with real $`A_\mu'^a`$.

Since $`D_\mu'(gq_f)=g\,D_\mu q_f`$ holds for all $`q_f`$, as operators on color triplets

```math
\left.
D_\mu'=g\,D_\mu\,g^\dagger.
\right.
\tag{5.80}
```

For infinitesimal $`\theta^a`$, $`g=I_3+i\theta^aT^a+O(\theta^2)`$ and (5.79) gives

```math
\left.
\begin{aligned}
A_\mu'&=A_\mu+i\theta^b[T^b,A_\mu]+\frac1{g_s}(\partial_\mu\theta^a)T^a+O(\theta^2)\\
&=A_\mu-f^{bca}\theta^bA^c_\mu T^a+\frac1{g_s}(\partial_\mu\theta^a)T^a+O(\theta^2),\\[6pt]
\delta A^a_\mu:=A_\mu'^a-A_\mu^a
&=\frac1{g_s}\partial_\mu\theta^a+f^{abc}A^b_\mu\theta^c+O(\theta^2).
\end{aligned}
\right.
\tag{5.81}
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
\tag{5.82}
```

Expanding in the basis, $`F_{\mu\nu}=F^a_{\mu\nu}T^a`$ with

```math
\left.
\boxed{
F^a_{\mu\nu}=\partial_\mu A^a_\nu-\partial_\nu A^a_\mu+g_sf^{abc}A^b_\mu A^c_\nu.
}
\right.
\tag{5.83}
```

By (5.80), $`[D_\mu',D_\nu']=g[D_\mu,D_\nu]g^\dagger`$, so

```math
\left.
F_{\mu\nu}'=gF_{\mu\nu}g^\dagger,
\qquad
\delta F^a_{\mu\nu}=f^{abc}F^b_{\mu\nu}\theta^c+O(\theta^2).
\right.
\tag{5.84}
```

By cyclicity of the trace and (5.13),

```math
\left.
\mathop{\rm tr}\nolimits \bigl(F_{\mu\nu}'F'^{\mu\nu}\bigr)
=\mathop{\rm tr}\nolimits \bigl(F_{\mu\nu}F^{\mu\nu}\bigr)
=\tfrac12F^a_{\mu\nu}F^{a\mu\nu}.
\right.
\tag{5.85}
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
\tag{5.86}
```

where the sum runs over the six flavors in (5.73), $`m_f`$ is the mass of flavor $`f`$, and $`D_\mu`$ acts on the $`q_f`$ to its right. Under (5.75) and (5.79), $`D_\mu'q_f'=g\,D_\mu q_f`$ by construction, so

```math
\left.
\bar q_f'\bigl(i\gamma^\mu D_\mu'-m_f\bigr)q_f'
=\bar q_f\,g^\dagger\bigl(i\gamma^\mu g\,D_\mu-m_f\,g\bigr)q_f
=\bar q_f\bigl(i\gamma^\mu D_\mu-m_f\bigr)q_f.
\right.
\tag{5.87}
```

Together with (5.85), $`\mathcal L_{\mathrm{QCD}}`$ is invariant under the local transformations (5.75), (5.79).

Substituting (5.77) and (5.83) into (5.86) separates the free and interaction terms:

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
\tag{5.88}
```

**Equations of Motion**

Treating $`q_f`$, $`\bar q_f`$ and $`A^a_\mu`$ as independent, the Euler–Lagrange equation for $`\bar q_f`$ is

```math
\left.
\bigl(i\gamma^\mu D_\mu-m_f\bigr)q_f=0.
\right.
\tag{5.89}
```

For $`A^a_\nu`$, define the color current $`j^{a\nu}:=\sum_f\bar q_f\gamma^\nu T^aq_f`$. From (5.86) with (5.83) and (5.88),

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
\tag{5.90}
```

The Euler–Lagrange equation $`\partial_\mu\bigl(\partial\mathcal L_{\mathrm{QCD}}/\partial(\partial_\mu A^a_\nu)\bigr)=\partial\mathcal L_{\mathrm{QCD}}/\partial A^a_\nu`$ then reads

```math
\left.
\boxed{
\partial_\mu F^{a\mu\nu}+g_sf^{abc}A^b_\mu F^{c\mu\nu}=-g_sj^{a\nu}.
}
\right.
\tag{5.91}
```

The left-hand side is the $`a`$-component of $`\partial_\mu F^{\mu\nu}-ig_s[A_\mu,F^{\mu\nu}]`$, the covariant derivative of $`F^{\mu\nu}`$ in the adjoint representation; with $`j^\nu:=j^{a\nu}T^a`$, (5.91) is

```math
\left.
D_\mu F^{\mu\nu}:=\partial_\mu F^{\mu\nu}-ig_s[A_\mu,F^{\mu\nu}]=-g_s\,j^\nu.
\right.
\tag{5.92}
```

<br><br>

<a id="qft-ch6"></a>
## 6. New Physics Beyond the Standard Model



<a id="seesaw-mechanism"></a>
### 6.1 Seesaw Mechanism

<a id="type-i-seesaw"></a>
#### Type-I Seesaw

**Fields and Lagrangian**

Extend the Standard Model by $`n`$ right-handed neutrino fields. 

- **Right-handed neutrinos**: $`N_{IR}`$, $`I=1,\ldots,n`$, are four-component chiral spinors with $`P_RN_{IR}=N_{IR}`$ and are singlets of $`SU(3)_c\times SU(2)_L\times U(1)_Y`$.
- **Flavor multiplets**: $`N_R:=(N_{1R},\ldots,N_{nR})^T`$ and $`\nu_L:=(\nu_{eL},\nu_{\mu L},\nu_{\tau L})^T`$. The lepton doublets $`\ell_{\alpha L}`$, charged singlets $`E_{\alpha R}`$ and Higgs doublet $`H`$ are those of Section 5.3.




The conjugate Higgs doublet and the additional terms in the Lagrangian are

```math
\left.
H^c:=i\sigma^2H^*
=\begin{pmatrix}H^{0*}\\-H^-\end{pmatrix}
\sim\Bigl(\mathbf2,-\frac12\Bigr),\qquad H^-:=(H^+)^*,
\right.
\tag{6.1}
```

```math
\left.
\boxed{
\begin{aligned}
\mathcal L_{\mathrm I}
={}&\mathcal L_{\mathrm{SM}}
+\overline{N_R}\,i\gamma^\mu\partial_\mu N_R\\
&-\left(\overline{\ell_{\alpha L}}\,(Y_\nu)_{\alpha I}H^cN_{IR}
+\frac12\overline{N_R^c}\,M_RN_R+\mathrm{h.c.}\right),\\
Y_\nu&\in\mathbb C^{3\times n},\qquad M_R\in\mathbb C^{n\times n},\qquad M_R^T=M_R.
\end{aligned}
}
\right.
\tag{6.2}
```

Repeated flavor indices are summed. The Yukawa matrix $`Y_\nu`$ is dimensionless and $`M_R`$ has mass dimension one. Under the electroweak transformation of Section 5.3,

```math
\left.
\begin{aligned}
\ell_L'&=e^{-i\theta_Y/2}U(\theta)\ell_L,
& (H^c)'&=e^{-i\theta_Y/2}U(\theta)H^c,
& N_R'&=N_R,\\
\overline{\ell_L'}\,Y_\nu(H^c)'N_R'
&=\overline{\ell_L}\,Y_\nu H^cN_R.
\end{aligned}
\right.
\tag{6.3}
```

The Majorana term is gauge invariant. Its flavor matrix can be taken symmetric because $`\overline{N_{IR}^c}N_{JR}=\overline{N_{JR}^c}N_{IR}`$.

**Mass Terms after Symmetry Breaking**

In the unitary gauge,

```math
\left.
H=\frac1{\sqrt2}\begin{pmatrix}0\\v_{\mathrm{SM}}+h\end{pmatrix},\qquad
H^c=\frac1{\sqrt2}\begin{pmatrix}v_{\mathrm{SM}}+h\\0\end{pmatrix},\qquad
M_l=\frac{v_{\mathrm{SM}}}{\sqrt2}Y_l,\qquad M_D:=\frac{v_{\mathrm{SM}}}{\sqrt2}Y_\nu.
\right.
\tag{6.4}
```

Here $`v_{\mathrm{SM}}\simeq246\,\mathrm{GeV}`$, as in Section 5.3. With $`l_L:=(l_{eL},l_{\mu L},l_{\tau L})^T`$,

```math
\left.
\begin{aligned}
-\mathcal L_{\mathrm{mass}+h}
={}&\overline{l_L}M_lE_R+\overline{\nu_L}M_DN_R
+\frac12\overline{N_R^c}M_RN_R\\
&+\frac h{v_{\mathrm{SM}}}\left(\overline{l_L}M_lE_R+\overline{\nu_L}M_DN_R\right)
+\mathrm{h.c.}
\end{aligned}
\right.
\tag{6.5}
```

Using the charge-conjugation identity

```math
\left.
\overline{\nu_L}M_DN_R=\overline{N_R^c}M_D^T\nu_L^c,
\right.
\tag{6.6}
```

define

```math
\left.
\Psi_L:=\begin{pmatrix}\nu_L\\N_R^c\end{pmatrix},\qquad
\Psi_L^c=\begin{pmatrix}\nu_L^c\\N_R\end{pmatrix},\qquad
\boxed{\mathcal M:=\begin{pmatrix}0_{3\times3}&M_D\\M_D^T&M_R\end{pmatrix}=\mathcal M^T}.
\right.
\tag{6.7}
```

The mass terms become

```math
\left.
-\mathcal L_{\mathrm{mass}}
=\overline{l_L}M_lE_R+\frac12\overline{\Psi_L}\,\mathcal M\Psi_L^c+\mathrm{h.c.}
\right.
\tag{6.8}
```

**Flavor Basis and Takagi Factorization**

For constant unitary matrices $`R_\ell,R_E\in U(3)`$ and $`R_N\in U(n)`$, write the old fields in terms of new fields as

```math
\left.
\begin{aligned}
\ell_L&=R_\ell\ell_L',\qquad E_R=R_EE_R',\qquad N_R=R_NN_R',\\
M_l'&=R_\ell^\dagger M_lR_E,\qquad
M_D'=R_\ell^\dagger M_DR_N,\qquad
M_R'=R_N^TM_RR_N.
\end{aligned}
\right.
\tag{6.9}
```

These transformations preserve the kinetic and gauge terms. We use the charged-lepton mass basis of Section 5.3,

```math
\left.
M_l=D_l:=\mathop{\rm diag}\nolimits (m_e,m_\mu,m_\tau).
\right.
\tag{6.10}
```

Since $`\mathcal M`$ is complex symmetric, there exists $`\mathcal U\in U(3+n)`$ such that

```math
\left.
\boxed{
\begin{aligned}
\mathcal M&=\mathcal U D\mathcal U^T,\qquad
\mathcal U^\dagger\mathcal M\mathcal U^*=D,\\
D&:=\mathop{\rm diag}\nolimits (D_\nu,D_N),\qquad
D_\nu:=\mathop{\rm diag}\nolimits (m_1,m_2,m_3),\qquad
D_N:=\mathop{\rm diag}\nolimits (M_1,\ldots,M_n),
\end{aligned}
}
\right.
\tag{6.11}
```

where all masses are nonnegative. We label the three light states by $`i=1,2,3`$ and the $`n`$ heavy states by $`I=1,\ldots,n`$; the light labels allow either normal or inverted ordering. The field transformation and the diagonal mass terms are

```math
\left.
\begin{aligned}
\Psi_L&=\mathcal U\Psi_L^m,\qquad
\Psi_L^m:=\begin{pmatrix}\nu_L^m\\(N_R^m)^c\end{pmatrix},\qquad
\Psi_L^c=\mathcal U^*(\Psi_L^m)^c,\\
-\mathcal L_{\mathrm{mass}}
&=\overline{l_L}D_lE_R
+\frac12\overline{\nu_L^m}D_\nu(\nu_L^m)^c
+\frac12\overline{(N_R^m)^c}D_NN_R^m+\mathrm{h.c.}
\end{aligned}
\right.
\tag{6.12}
```

Equivalently, one may first block diagonalize and then Takagi diagonalize each block:

```math
\left.
\begin{aligned}
\Psi_L&=W\begin{pmatrix}\nu_L^{\mathrm b}\\(N_R^{\mathrm b})^c\end{pmatrix},\qquad
W^\dagger\mathcal MW^*=\begin{pmatrix}M_\nu&0\\0&M_N\end{pmatrix},\\
M_\nu&=UD_\nu U^T,\qquad M_N=U_ND_NU_N^T,\\
\mathcal U&=W\begin{pmatrix}U&0\\0&U_N\end{pmatrix},\qquad
W\in U(3+n),\quad U\in U(3),\quad U_N\in U(n).
\end{aligned}
\right.
\tag{6.13}
```

The matrices $`M_\nu`$ and $`M_N`$ refer to the block-diagonal basis; $`M_N`$ is generally different from the original block $`M_R`$.

**Rank and Parameter Counting**

The zero active-active block implies

```math
\left.
\mathcal M\begin{pmatrix}a\\0\end{pmatrix}=0
\quad\text{for }a\in\ker M_D^T,\qquad
\mathop{\rm rank}\nolimits\,\mathcal M\le\min(2n,3+n).
\right.
\tag{6.14}
```

If $`M_R`$ is invertible, block elimination gives the exact rank identity

```math
\left.
\begin{aligned}
&\begin{pmatrix}I_3&-M_DM_R^{-1}\\0&I_n\end{pmatrix}
\mathcal M
\begin{pmatrix}I_3&0\\-M_R^{-1}M_D^T&I_n\end{pmatrix}
=\begin{pmatrix}-M_DM_R^{-1}M_D^T&0\\0&M_R\end{pmatrix},\\
&\mathop{\rm rank}\nolimits\,\mathcal M
=n+\mathop{\rm rank}\nolimits (-M_DM_R^{-1}M_D^T).
\end{aligned}
\right.
\tag{6.15}
```

This congruence is not a unitary mass diagonalization. For generic matrices, the light rank is $`r=\min(n,3)`$ and there are $`3-r`$ massless light states. In particular, $`n=2`$ gives the minimal seesaw with one massless light neutrino at tree level:

```math
\left.
m_1=0\quad\text{(normal ordering)},\qquad
m_3=0\quad\text{(inverted ordering)}.
\right.
\tag{6.16}
```

For the following counts, take $`n\ge1`$, generic rank and nondegenerate nonzero masses. Before quotienting by field redefinitions, the numbers of independent real parameters are

```math
\left.
\begin{aligned}
N(M_D)&=6n,\qquad N(M_R)=n(n+1),\qquad N(\mathcal M)=n^2+7n,\\
N(D)&=n+r=\min(2n,3+n),\\
N(\mathcal U)_{\mathrm{constrained}}
&=n^2+7n-(n+r).
\end{aligned}
\right.
\tag{6.17}
```

The last line counts independent non-mass parameters of $`\mathcal M`$ at fixed $`D`$, with the zero-block constraint imposed and Takagi stabilizers removed. It is not the dimension of an unconstrained $`U(3+n)`$ matrix.

For nondegenerate charged-lepton masses, the remaining basis freedom is

```math
\left.
\begin{aligned}
\ell_L&=P\ell_L',\qquad E_R=PE_R',\qquad N_R=R_NN_R',\\
P&:=\mathop{\rm diag}\nolimits (e^{i\phi_e},e^{i\phi_\mu},e^{i\phi_\tau}),
\qquad R_N\in U(n),\\
M_D'&=P^\dagger M_DR_N,\qquad M_R'=R_N^TM_RR_N.
\end{aligned}
\right.
\tag{6.18}
```

There are $`3+n^2`$ redundant real parameters. Excluding the three charged-lepton masses,

```math
\left.
\boxed{
\begin{aligned}
N_{\nu,\mathrm{phys}}&=(n^2+7n)-(3+n^2)=7n-3,\\
N_{\mathrm{masses}}&=n+r,\qquad
N_{\mathrm{mixing}}=6n-r-3.
\end{aligned}
}
\right.
\tag{6.19}
```

Thus $`n=2`$ has four nonzero masses and seven mixing parameters, while $`n=3`$ has six masses and twelve mixing parameters.

**Charged Currents and the PMNS Matrix**

Write the upper blocks of $`\mathcal U`$ as

```math
\left.
K:=W_{11}U,\qquad R:=W_{12}U_N,\qquad
\nu_{\alpha L}=K_{\alpha i}\nu_{iL}^m+R_{\alpha I}(N_{IR}^m)^c.
\right.
\tag{6.20}
```

In the charged-lepton mass basis, the leptonic charged current of Section 5.3 becomes

```math
\left.
\boxed{
\mathcal L_{\mathrm{CC}}^\ell
=\frac{g_2}{\sqrt2}W_\mu^-
\overline{l_{\alpha L}}\gamma^\mu
\left[K_{\alpha i}\nu_{iL}^m+R_{\alpha I}(N_{IR}^m)^c\right]
+\mathrm{h.c.}
}
\right.
\tag{6.21}
```

Following the coefficient definition, set $`U_{\mathrm{PMNS}}:=K`$. Unitarity of $`\mathcal U`$ and its zero-block relation give

```math
\left.
\boxed{
\begin{aligned}
U_{\mathrm{PMNS}}U_{\mathrm{PMNS}}^\dagger
&=I_3-RR^\dagger,\\
KD_\nu K^T+RD_NR^T&=0_{3\times3}.
\end{aligned}
}
\right.
\tag{6.22}
```

The light charged-current matrix $`U_{\mathrm{PMNS}}`$ is generally nonunitary; the Takagi matrix $`U`$ is unitary.

**Exact Parametrization of Light-Heavy Mixing**

Choose the singlet flavor basis so that the heavy block after block diagonalization is $`M_N=D_N`$, hence $`U_N=I_n`$. In the coordinate patch where $`W_{11}`$ is invertible, use the block-unitary freedom to write

```math
\left.
\begin{aligned}
X&\in\mathbb C^{3\times n},\qquad
A_X:=(I_3+XX^\dagger)^{-1/2},\qquad
B_X:=(I_n+X^\dagger X)^{-1/2},\\
A_XX&=XB_X,\qquad
\boxed{W(X):=\begin{pmatrix}A_X&A_XX\\-X^\dagger A_X&B_X\end{pmatrix}},
\qquad W^\dagger W=WW^\dagger=I_{3+n}.
\end{aligned}
\right.
\tag{6.23}
```

The square roots are the positive Hermitian roots. The upper-left block of $`\mathcal M=W\,\mathop{\rm diag}\nolimits (M_\nu,D_N)W^T`$ is

```math
\left.
0=A_X(M_\nu+XD_NX^T)A_X^T
\quad\Longleftrightarrow\quad
\boxed{M_\nu=-XD_NX^T=UD_\nu U^T}.
\right.
\tag{6.24}
```

The other blocks give

```math
\left.
\boxed{
\begin{aligned}
M_D&=A_XXD_N(B_X^T)^{-1},\\
M_R&=B_X\left[D_N-(X^\dagger X)D_N(X^\dagger X)^T\right]B_X^T.
\end{aligned}
}
\right.
\tag{6.25}
```

For positive heavy masses, elimination of $`X`$ from the light block also yields

```math
\left.
\begin{aligned}
M_\nu
&=-A_X^{-1}M_DB_X^TD_N^{-1}B_XM_D^T(A_X^T)^{-1}\\
&=-A_X^{-1}M_D
\left(M_R+X^\dagger M_D+M_D^TX^*\right)^{-1}
M_D^T(A_X^T)^{-1}.
\end{aligned}
\right.
\tag{6.26}
```

Here $`D_N`$ is the physical heavy spectrum. Neither $`M_R=D_N`$ nor $`X=M_DM_R^{-1}`$ is an exact identity in this basis.

**Construction from Masses and Mixing Parameters**

Take generic light rank $`r=\min(n,3)`$ and positive $`M_I`$. Let $`P_\nu`$ project onto the nonzero entries of $`D_\nu`$, and choose a complex $`3\times n`$ matrix $`O`$ with

```math
\left.
P_\nu:=\mathop{\rm diag}\nolimits (p_1,p_2,p_3),\qquad
p_i:=\begin{cases}1,&m_i>0,\\0,&m_i=0,\end{cases}
\qquad P_\nu O=O,\qquad OO^T=P_\nu.
\right.
\tag{6.27}
```

Then

```math
\left.
\boxed{X=iU\sqrt{D_\nu}\,OD_N^{-1/2}},\qquad
-XD_NX^T=U\sqrt{D_\nu}\,OO^T\sqrt{D_\nu}\,U^T=UD_\nu U^T.
\right.
\tag{6.28}
```

The orthogonality condition uses a transpose, not a Hermitian conjugate. For $`n>3`$ it does not require $`O^TO=I_n`$. The exact reconstruction is

```math
\left.
(D_\nu,D_N,U,O)\ \longrightarrow\ X\ \longrightarrow\ W(X)
\ \longrightarrow\
\mathcal M=W\begin{pmatrix}UD_\nu U^T&0\\0&D_N\end{pmatrix}W^T.
\right.
\tag{6.29}
```

After removing the three charged-lepton phases and the $`U(3-r)`$ freedom in the massless subspace, the parameter counts are

```math
\left.
\begin{aligned}
N(U)&=9-(3-r)^2-3,\qquad
N(O)=2rn-r(r+1),\\
N(U)+N(O)&=6n-r-3,\qquad
(n+r)+N(U)+N(O)=7n-3.
\end{aligned}
\right.
\tag{6.30}
```

For $`n=2`$ and normal ordering,

```math
\left.
\begin{aligned}
D_\nu&=\mathop{\rm diag}\nolimits (0,m_2,m_3),\qquad
D_N=\mathop{\rm diag}\nolimits (M_1,M_2),\\
O(z)&=\begin{pmatrix}0&0\\\cos z&-\sin z\\\sin z&\cos z\end{pmatrix},\qquad
z\in\mathbb C,\qquad O^TO=I_2,\qquad OO^T=\mathop{\rm diag}\nolimits (0,1,1).
\end{aligned}
\right.
\tag{6.31}
```

For inverted ordering one may use

```math
\left.
D_\nu=\mathop{\rm diag}\nolimits (m_1,m_2,0),\qquad
O(z)=\begin{pmatrix}\cos z&-\sin z\\\sin z&\cos z\\0&0\end{pmatrix},\qquad
OO^T=\mathop{\rm diag}\nolimits (1,1,0).
\right.
\tag{6.32}
```

Discrete column signs can be absorbed into the heavy Majorana fields. For three massive light states, a phase convention for the unitary matrix $`U`$ is

```math
\left.
\boxed{
U=\begin{pmatrix}
c_{12}c_{13}&s_{12}c_{13}&s_{13}e^{-i\delta}\\
-s_{12}c_{23}-c_{12}s_{23}s_{13}e^{i\delta}
&c_{12}c_{23}-s_{12}s_{23}s_{13}e^{i\delta}&s_{23}c_{13}\\
s_{12}s_{23}-c_{12}c_{23}s_{13}e^{i\delta}
&-c_{12}s_{23}-s_{12}c_{23}s_{13}e^{i\delta}&c_{23}c_{13}
\end{pmatrix}
\mathop{\rm diag}\nolimits (e^{i\rho},e^{i\sigma},1)
}.
\right.
\tag{6.33}
```

Here $`c_{ij}:=\cos\theta_{ij}`$ and $`s_{ij}:=\sin\theta_{ij}`$.

For $`n=2`$, one Majorana phase is removable by rephasing the massless state. One can take $`\rho=0`$ in either ordering, after a common charged-lepton rephasing when needed. Thus $`U`$ contains three angles, one Dirac phase and one Majorana phase; together with the complex $`z`$ there are seven mixing parameters. The exact charged-current matrix is

```math
\left.
\boxed{
\begin{aligned}
U_{\mathrm{PMNS}}&=A_XU\\
&=U\left(I_3+\sqrt{D_\nu}\,OD_N^{-1}O^\dagger\sqrt{D_\nu}\right)^{-1/2}.
\end{aligned}
}
\right.
\tag{6.34}
```

**Seesaw Limit and Casas–Ibarra Form**

The conventional seesaw regime has invertible $`M_R`$ and

```math
\left.
\frac{\sigma_{\max}(M_D)}{\sigma_{\min}(M_R)}\ll1,\qquad
\epsilon_X:=\sigma_{\max}(X)\ll1,
\right.
\tag{6.35}
```

where $`\sigma_{\max}`$ and $`\sigma_{\min}`$ denote the largest and smallest singular values. Expanding the exact parametrization,

```math
\left.
\begin{aligned}
A_X&=I_3-\frac12XX^\dagger+\mathcal O(\epsilon_X^4),\qquad
B_X=I_n-\frac12X^\dagger X+\mathcal O(\epsilon_X^4),\\
W&=\begin{pmatrix}I_3-\frac12XX^\dagger&X\\-X^\dagger&I_n-\frac12X^\dagger X\end{pmatrix}
+\mathcal O(\epsilon_X^3).
\end{aligned}
\right.
\tag{6.36}
```

To leading order in this basis,

```math
\left.
M_D\simeq XD_N,\qquad M_R\simeq D_N,\qquad
X\simeq M_DM_R^{-1}\simeq M_DD_N^{-1}.
\right.
\tag{6.37}
```

The zero-block identity therefore gives

```math
\left.
\boxed{M_\nu=UD_\nu U^T\simeq-M_DM_R^{-1}M_D^T
\simeq-\frac{v_{\mathrm{SM}}^2}{2}\,Y_\nu D_N^{-1}Y_\nu^T}.
\right.
\tag{6.38}
```

The charged-current matrix satisfies

```math
\left.
\begin{aligned}
U_{\mathrm{PMNS}}&=\left(I_3-\frac12XX^\dagger\right)U+\mathcal O(\epsilon_X^4),\\
U_{\mathrm{PMNS}}U_{\mathrm{PMNS}}^\dagger
&=I_3-XX^\dagger+\mathcal O(\epsilon_X^4).
\end{aligned}
\right.
\tag{6.39}
```

Thus $`U_{\mathrm{PMNS}}\simeq U`$ only after neglecting second-order light-heavy mixing. Substituting the exact expression for $`X`$ into $`M_D\simeq XD_N`$ gives the Casas–Ibarra form,

```math
\left.
\boxed{
\begin{aligned}
M_D&\simeq iU\sqrt{D_\nu}\,O\sqrt{D_N},\qquad M_R\simeq D_N,\\
Y_\nu&\simeq\frac{i\sqrt2}{v_{\mathrm{SM}}}\,U\sqrt{D_\nu}\,O\sqrt{D_N},\qquad
P_\nu O=O,\quad OO^T=P_\nu.
\end{aligned}
}
\right.
\tag{6.40}
```

The construction of $`X`$ is exact; these expressions for $`M_D`$ and $`Y_\nu`$ are leading-order approximations. In particular,

```math
\left.
\epsilon_X=\sigma_{\max}\!\left(\sqrt{D_\nu}\,OD_N^{-1/2}\right).
\right.
\tag{6.41}
```

Since $`O`$ is complex orthogonal rather than unitary, $`m_i\ll M_I`$ alone does not ensure small light-heavy mixing.

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

<a id="lmu-ltau-gauge-symmetry"></a>
### 6.2 $`U(1)_{L_\mu-L_\tau}`$ Gauge Symmetry

The lepton doublets $`\ell_{\alpha L}`$, charged singlets $`E_{\alpha R}`$, Higgs doublet $`H`$, gauge fields $`W_\mu^a,B_\mu`$ with couplings $`g_2,g_1`$, and Yukawa matrix $`Y_l`$ are those of Section 5.3.

The terms of the Standard Model Lagrangian density that contain lepton fields are

```math
\left.
\boxed{
\begin{aligned}
\mathcal L_{\mathrm{SM}}^\ell
&=\sum_{\alpha=e,\mu,\tau}\Bigl(\overline{\ell_{\alpha L}}\,i\gamma^\mu D_\mu\ell_{\alpha L}
+\overline{E_{\alpha R}}\,i\gamma^\mu D_\mu E_{\alpha R}\Bigr)\\
&\quad-\sum_{\alpha,\beta=e,\mu,\tau}\Bigl(\overline{\ell_{\alpha L}}\,(Y_l)_{\alpha\beta}\,H\,E_{\beta R}+\mathrm{h.c.}\Bigr),\\
D_\mu\ell_{\alpha L}&=\Bigl(\partial_\mu-ig_2W_\mu^a\frac{\sigma^a}2+\frac i2g_1B_\mu\Bigr)\ell_{\alpha L},\\
D_\mu E_{\alpha R}&=\bigl(\partial_\mu+ig_1B_\mu\bigr)E_{\alpha R}.
\end{aligned}
}
\right.
\tag{6.42}
```

In the flavor basis of Section 5.3,

```math
\left.
Y_l=\frac{\sqrt2}{v_{\mathrm{SM}}}\,\mathop{\rm diag}\nolimits (m_e,m_\mu,m_\tau).
\right.
\tag{6.43}
```

#### $`U(1)_{L_\mu-L_\tau}`$ Gauge Symmetry Transformations

Let $`\theta:\mathbb R^4\to\mathbb R`$ and introduce a real gauge field $`Z'_\mu`$ with coupling $`g_{Z'}>0`$. The lepton fields and $`Z'_\mu`$ transform as


```math
\left.
\begin{gathered}
\begin{aligned}
\ell_{\alpha L}'(x)&=e^{iQ_\alpha\theta(x)}\ell_{\alpha L}(x),\\
E_{\alpha R}'(x)&=e^{iQ_\alpha\theta(x)}E_{\alpha R}(x),\\
(Z'_\mu)'(x)&=Z'_\mu(x)+\frac1{g_{Z'}}\partial_\mu\theta(x),
\end{aligned}\\[6pt]
\text{where the }U(1)_{L_\mu-L_\tau}\text{ charges are}\quad
Q_\alpha=\begin{cases}
0, & \alpha=e,\\
1, & \alpha=\mu,\\
-1, & \alpha=\tau.
\end{cases}
\end{gathered}
\right.
\tag{6.44}
```

The remaining Standard Model fields are unchanged.

The covariant derivatives in (6.42) become

```math
\left.
\begin{aligned}
D_\mu\ell_{\alpha L}&=\Bigl(\partial_\mu-ig_2W_\mu^a\frac{\sigma^a}2+\frac i2g_1B_\mu-ig_{Z'}Q_\alpha Z'_\mu\Bigr)\ell_{\alpha L},\\
D_\mu E_{\alpha R}&=\bigl(\partial_\mu+ig_1B_\mu-ig_{Z'}Q_\alpha Z'_\mu\bigr)E_{\alpha R}.
\end{aligned}
\right.
\tag{6.45}
```


#### Lagrangian



















<br><br>

<a id="qft-ch7"></a>
## 7. Renormalization

<a id="forest-formula"></a>
### 7.1 Forest Formula

<a id="graph-definitions"></a>
#### Basic Definitions of Graphs

- **Graph**: a Feynman graph $`\mathcal G`$ consists of a finite set $`V(\mathcal G)`$ of vertices, a finite set $`I(\mathcal G)`$ of internal lines, each joining two vertices (possibly the same vertex), and a finite set $`E(\mathcal G)`$ of external lines, each attached to one vertex.
  - Several internal lines may join the same pair of vertices.
  - $`\mathcal G`$ is connected if any two vertices are joined by a chain of internal lines. A loop is a closed chain of internal lines.
  - For connected $`\mathcal G`$, the number of loops is $`L(\mathcal G)=|I(\mathcal G)|-|V(\mathcal G)|+1`$, where $`|\cdot|`$ is the number of elements; for a disconnected graph, $`L`$ is the sum over its connected components.
- **1PI**: $`\mathcal G`$ is one-particle irreducible (1PI) if it is connected and stays connected when any one internal line is cut.
  - Equivalently, $`\mathcal G`$ is connected and every internal line lies on a loop.
- **Subgraph**: a nonempty set $`I(\gamma)\subseteq I(\mathcal G)`$ of internal lines, together with the set $`V(\gamma)`$ of their endpoints, defines a subgraph $`\gamma`$ of $`\mathcal G`$, written $`\gamma\subseteq\mathcal G`$.
  - The external lines of $`\gamma`$ are the external lines of $`\mathcal G`$ attached to $`V(\gamma)`$ and the internal lines of $`\mathcal G`$ outside $`I(\gamma)`$ with an endpoint in $`V(\gamma)`$; such an internal line with both endpoints in $`V(\gamma)`$ counts as two external lines of $`\gamma`$.
- **Spanning tree**: for connected $`\mathcal G`$, a maximal set of internal lines containing no loop.
  - Its lines connect all vertices of $`\mathcal G`$, and there are $`|V(\mathcal G)|-1`$ of them.
  - Each of the remaining $`L(\mathcal G)`$ internal lines closes exactly one loop with lines of the tree. With independent loop momenta assigned to these lines, momentum conservation at the vertices fixes the momenta of the tree lines.
- **Reduced graph**: for $`\gamma\subseteq\mathcal G`$, the reduced graph $`\mathcal G/\gamma`$ is obtained by contracting each connected component of $`\gamma`$ to a point: the lines $`I(\gamma)`$ are removed, the vertices of each connected component of $`\gamma`$ are merged into a single vertex, and all other internal and external lines of $`\mathcal G`$ are kept.
  - $`I(\mathcal G/\gamma)=I(\mathcal G)\setminus I(\gamma)`$ and $`L(\mathcal G/\gamma)=L(\mathcal G)-L(\gamma)`$.
  - If $`\mathcal G`$ is 1PI, so is $`\mathcal G/\gamma`$.
- **Renormalization part**: a 1PI subgraph $`\gamma\subseteq\mathcal G`$ whose superficial degree of divergence $`\omega(\gamma)`$, namely $`d\,L(\gamma)`$ plus the degree of the integrand of $`\gamma`$ in its loop momenta, satisfies $`\omega(\gamma)\ge0`$; $`\gamma=\mathcal G`$ is allowed.
- **Nested, disjoint, overlapping**: two subgraphs $`\gamma_1,\gamma_2\subseteq\mathcal G`$ are nested if $`\gamma_1\subseteq\gamma_2`$ or $`\gamma_2\subseteq\gamma_1`$, disjoint if $`V(\gamma_1)\cap V(\gamma_2)=\emptyset`$, and overlapping otherwise.
- **Forest**: a set of renormalization parts of $`\mathcal G`$, any two of which are nested or disjoint; the empty set is a forest.

<br><br>

<a id="r-operation-recursion"></a>
#### $`\mathcal{L}_{CT}`$ and R-Operation Recursion Formula

Original Lagrangian : $`\mathcal L`$

**1-Loop Level**

- **Divergent part**: for a 1PI graph $`\mathcal G`$, $`T\circ\mathcal G`$ is the divergent part of $`\mathcal G`$, a polynomial in the external momenta of $`\mathcal G`$.
- **Counterterm Feynman rule**: the counterterm vertex associated with $`\mathcal G`$ has the Feynman rule $`C(\mathcal G):=-T\circ\mathcal G`$.
- **Counterterm Lagrangian**: $`\mathcal L_{CT}^{(\mathcal G)}`$ is the term of the counterterm Lagrangian whose Feynman rule is $`C(\mathcal G)`$.













<br><br>

<a id="qed-renormalization"></a>
### 7.2 QED Renormalization

**Gauge-Fixed Lagrangian**

With the covariant gauge fixing of (4.15), the QED Lagrangian (5.67) for Dirac fields $`\psi_f`$ of charge $`Q_fe`$ and mass $`m_f`$ is

```math
\left.
\mathcal L
=\sum_f\bar\psi_f\bigl(i\gamma^\mu\partial_\mu-m_f\bigr)\psi_f
-\frac14F_{\mu\nu}F^{\mu\nu}
-\frac1{2\xi}(\partial_\mu A^\mu)^2
+eA_\mu\sum_fQ_f\,\bar\psi_f\gamma^\mu\psi_f .
\right.
\tag{7.1}
```

The Faddeev--Popov ghosts decouple, as noted after (3.38).


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
\tag{7.2}
```

For the electron, $`Q_f=-1`$ and the vertex is $`-ie\gamma^\mu`$. Along each fermion line, write the factors in the order opposite to the arrow, so that the spinor indices form a matrix product. Impose four-momentum conservation at every vertex and integrate each loop momentum with $`\int d^4\ell/(2\pi)^4`$, continued to $`\int d^d\ell/(2\pi)^d`$ in $`d=4-\epsilon`$ dimensions. Each closed fermion loop gives a factor $`-1`$ and a Dirac trace; exchanging identical external fermions changes the sign, as in [Section 4.3](#feynman-diagrams).

**Tree Level: $`e^+e^-\to q\bar q`$**

<p align="center"><img src="figures/ee-to-qqbar.svg" alt="Tree-level s-channel diagram for e+ e- to q qbar" width="440"></p>

Time runs from left to right. Arrows on the fermion lines show the fermion-number flow; grey arrows show the four-momenta.

Label the spins of $`e^-,e^+,q,\bar q`$ by $`s,s',r,r'`$ and the colors of $`q,\bar q`$ by $`c,c'\in\{1,2,3\}`$; the photon vertex is diagonal in color, and $`p_1+p_2=k_1+k_2`$. Reading each fermion line against its arrow with (7.2),

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
\tag{7.3}
```


**Superficial Degree of Divergence**

For a connected QED graph, let $`V`$ be the number of vertices, $`I_\gamma,I_F`$ the numbers of internal photon and fermion lines, and $`E_\gamma,E_F`$ the numbers of external photon and fermion lines. Each vertex of (7.1) joins two fermion lines and one photon line and carries no derivative. Counting line ends, and counting powers of loop momenta at $`d=4`$ with photon propagators $`\sim\ell^{-2}`$ and fermion propagators $`\sim\ell^{-1}`$,

```math
\left.
\begin{aligned}
2V&=2I_F+E_F,\qquad V=2I_\gamma+E_\gamma,\qquad L=I_\gamma+I_F-V+1,\\[6pt]
\omega&=4L-2I_\gamma-I_F=2I_\gamma+3I_F-4V+4 .
\end{aligned}
\right.
\tag{7.4}
```

Eliminating $`I_\gamma=\tfrac12(V-E_\gamma)`$ and $`I_F=V-\tfrac12E_F`$,

```math
\left.
\boxed{\omega=4-E_\gamma-\frac32E_F .}
\right.
\tag{7.5}
```

The dependence on $`V`$ cancels because $`[e]=0`$ in four dimensions.

**Two External Legs**

Every vertex conserves fermion number, so $`E_F`$ is even and two external legs means $`(E_F,E_\gamma)=(2,0)`$ or $`(0,2)`$. Let $`-i\Sigma(p)`$ and $`i\Pi^{\mu\nu}(p)`$ be the sums of amputated 1PI graphs with two external fermion lines and with two external photon lines, where $`p`$ is the external momentum.

**(1) Fermion Propagator**

```math
\left.
E_F=2,\qquad E_\gamma=0\qquad\Longrightarrow\qquad\omega=1 .
\right.
\tag{7.6}
```

<p align="center"><img src="figures/fermion-self-energy.svg" alt="One-loop fermion self-energy" width="322"></p>

The one-loop graph of $`-i\Sigma(p)`$ for a fermion $`f`$: the internal fermion carries $`\ell`$ along its arrow and the photon carries $`p-\ell`$.

Let $`-i\Sigma_2(p)`$ be the $`O(e^2)`$ part of $`-i\Sigma(p)`$. Starting at the vertex $`\nu`$ and reading the line against the arrow with (7.2),

```math
\left.
\begin{aligned}
-i\Sigma_2(p)
=\int\frac{d^4\ell}{(2\pi)^4}\,
&(ieQ_f\gamma^\nu)\,\frac{i(\not\ell+m_f)}{\ell^2-m_f^2+i\varepsilon}\,(ieQ_f\gamma^\mu)\\[6pt]
&\times\frac{-i}{(p-\ell)^2+i\varepsilon}\left[\eta_{\mu\nu}-(1-\xi)\frac{(p-\ell)_\mu(p-\ell)_\nu}{(p-\ell)^2+i\varepsilon}\right].
\end{aligned}
\right.
\tag{7.7}
```

For a quark, (7.7) multiplies the identity in color.

In $`d=4-\epsilon`$ dimensions, replace $`d^4\ell/(2\pi)^4`$ by $`d^d\ell/(2\pi)^d`$, let the coupling carry the factor of $`\mu`$, $`e\to\mu^{\epsilon/2}e`$, and continue the $`\gamma`$ matrices to $`d`$ dimensions with $`\{\gamma^\mu,\gamma^\nu\}=2\eta^{\mu\nu}I_4`$ and $`\eta^\mu{}_\mu=d`$. Collecting $`(ieQ_f)^2\,i\,(-i)=-e^2Q_f^2`$ and using $`\gamma^\nu\gamma_\nu=d\,I_4`$, $`\gamma^\nu\not a\gamma_\nu=-(d-2)\not a`$ and, for $`\ell=p-k`$, $`\not k(\not\ell+m_f)\not k=2(k\cdot p)\not k+k^2(m_f-\not p-\not k)`$, where $`k^2`$ cancels one factor $`\mathcal P_\gamma`$,

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
\tag{7.8}
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
\tag{7.9}
```

Shift $`\ell\to\ell+xp`$, so that $`k\to(1-x)p-\ell`$, drop the terms odd in $`\ell`$, and replace $`\ell^\mu\ell^\nu`$ by $`\eta^{\mu\nu}\ell^2/d`$. The numerators of (7.8) become

```math
\left.
\begin{aligned}
d\,m_f-(d-2)\not\ell\ &\to\ d\,m_f-(d-2)x\not p,\\[4pt]
m_f-\not p-\not k\ &\to\ m_f-(2-x)\not p,\\[4pt]
2(k\cdot p)\not k\ &\to\ 2(1-x)^2p^2\not p+2(p\cdot\ell)\not\ell
\ \to\ 2(1-x)^2p^2\not p+\frac2d\,\ell^2\not p,
\end{aligned}
\right.
\tag{7.10}
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
\tag{7.11}
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
\tag{7.12}
```

Applying (7.12) to (7.11),

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
\tag{7.13}
```

With $`d=4-\epsilon`$, $`\Gamma(\epsilon/2)=2/\epsilon-\gamma_E+O(\epsilon)`$ and $`2/\bar\epsilon:=2/\epsilon-\gamma_E+\ln4\pi`$,

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
\tag{7.14}
```

**(2) Photon Propagator**

```math
\left.
E_\gamma=2,\qquad E_F=0\qquad\Longrightarrow\qquad\omega=2 .
\right.
\tag{7.15}
```

<p align="center"><img src="figures/photon-self-energy.svg" alt="One-loop photon self-energy" width="298"></p>

The one-loop graph of $`i\Pi^{\mu\nu}(p)`$, with a closed loop of a fermion $`f`$: the loop momenta $`\ell+p`$ and $`\ell`$ run along the arrows.

Let $`i\Pi_2^{\mu\nu}(p)`$ be the $`O(e^2)`$ part of $`i\Pi^{\mu\nu}(p)`$. Starting at the vertex $`\mu`$ and reading the loop against the arrows with (7.2),

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
\tag{7.16}
```

where the factor $`-1`$ and the Dirac trace come from the closed fermion loop, and $`N_{\mathrm c,f}`$ is the number of colors of $`f`$ ($`1`$ for a lepton, $`3`$ for a quark) from the color trace.

In $`d=4-\epsilon`$ dimensions, replace $`d^4\ell/(2\pi)^4`$ by $`d^d\ell/(2\pi)^d`$ and let the coupling carry the factor of $`\mu`$, $`e\to\mu^{\epsilon/2}e`$. Collecting $`(-1)(ieQ_f)^2i^2=-e^2Q_f^2`$ and using $`\mathop{\rm tr}\nolimits (\gamma^\mu\gamma^\nu)=4\eta^{\mu\nu}`$, $`\mathop{\rm tr}\nolimits (\gamma^\mu\gamma^\rho\gamma^\nu\gamma^\sigma)=4(\eta^{\mu\rho}\eta^{\nu\sigma}-\eta^{\mu\nu}\eta^{\rho\sigma}+\eta^{\mu\sigma}\eta^{\rho\nu})`$ and the vanishing of traces of an odd number of $`\gamma`$ matrices,

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
\tag{7.17}
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
\tag{7.18}
```

Shift $`\ell\to\ell-xp`$ and drop the terms odd in $`\ell`$, which integrate to zero; then replace $`\ell^\mu\ell^\nu`$ by $`\eta^{\mu\nu}\ell^2/d`$ under the integral. The numerator of (7.17) becomes

```math
\left.
\begin{aligned}
&\ell^\mu(\ell+p)^\nu+\ell^\nu(\ell+p)^\mu-\eta^{\mu\nu}\bigl[\ell\cdot(\ell+p)-m_f^2\bigr]\\[4pt]
&\quad\to\ 2\ell^\mu\ell^\nu-\eta^{\mu\nu}\ell^2-2x(1-x)p^\mu p^\nu+\eta^{\mu\nu}\bigl[x(1-x)p^2+m_f^2\bigr]\\[4pt]
&\quad\to\ 2x(1-x)\bigl(p^2\eta^{\mu\nu}-p^\mu p^\nu\bigr)+\eta^{\mu\nu}\Bigl[\frac{2-d}{d}\,\ell^2+\Delta_f\Bigr],
\end{aligned}
\right.
\tag{7.19}
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
\tag{7.20}
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
\tag{7.21}
```

where the last line uses $`\Gamma(2-\tfrac d2)=(1-\tfrac d2)\Gamma(1-\tfrac d2)`$. Only the transverse term of (7.20) survives:

```math
\left.
\begin{aligned}
i\Pi_2^{\mu\nu}(p)
={}&-4\mu^{\epsilon}e^2\sum_fN_{\mathrm c,f}Q_f^2\int_0^1dx\,2x(1-x)\bigl(p^2\eta^{\mu\nu}-p^\mu p^\nu\bigr)\\[6pt]
&\times\frac{i}{(4\pi)^{d/2}}\,\Gamma\Bigl(2-\frac d2\Bigr)(\Delta_f-i\varepsilon)^{\frac d2-2} .
\end{aligned}
\right.
\tag{7.22}
```

With $`d=4-\epsilon`$, $`\Gamma(\epsilon/2)=2/\epsilon-\gamma_E+O(\epsilon)`$ and $`2/\bar\epsilon`$ as in (7.14),

```math
\left.
\boxed{
\begin{aligned}
\Pi_2^{\mu\nu}(p)&=\bigl(p^2\eta^{\mu\nu}-p^\mu p^\nu\bigr)\,\Pi_2(p^2),\\[6pt]
\Pi_2(p^2)&=-\frac{e^2}{2\pi^2}\sum_fN_{\mathrm c,f}Q_f^2\int_0^1dx\,x(1-x)\left[\frac2{\bar\epsilon}-\ln\frac{\Delta_f-i\varepsilon}{\mu^2}\right]+O(\epsilon).
\end{aligned}
}
\right.
\tag{7.23}
```

**Three External Legs**

Three external legs means $`(E_F,E_\gamma)=(2,1)`$ or $`(0,3)`$. Let $`ieQ_f\Gamma^\mu(p',p)`$ be the sum of amputated 1PI graphs with an incoming fermion of momentum $`p`$, an outgoing fermion of momentum $`p':=p+q`$, and an incoming photon of momentum $`q`$ and index $`\mu`$. Write $`\Gamma^\mu=\gamma^\mu+\Lambda^\mu`$.

**(1) Vertex**

```math
\left.
E_F=2,\qquad E_\gamma=1\qquad\Longrightarrow\qquad\omega=0 .
\right.
\tag{7.24}
```

<p align="center"><img src="figures/vertex.svg" alt="One-loop QED vertex" width="370"></p>

The one-loop graph of $`ieQ_f\Lambda^\mu(p',p)`$ for a fermion $`f`$: the internal fermions carry $`\ell`$ and $`\ell+q`$ along their arrows and the internal photon carries $`p-\ell`$.

Let $`\Lambda_2^\mu(p',p)`$ be the $`O(e^2)`$ part of $`\Lambda^\mu(p',p)`$. Starting at the vertex $`\nu`$ and reading the line against the arrow with (7.2),

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
\tag{7.25}
```

For a quark, (7.25) multiplies the identity in color.

In $`d=4-\epsilon`$ dimensions, continue as for (7.8), with the stripped coupling $`ieQ_f`$ also carrying $`\mu^{\epsilon/2}`$. Collecting $`(ieQ_f)^3\,i\cdot i\cdot(-i)=(ieQ_f)(-ie^2Q_f^2)`$,

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
\tag{7.26}
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
\tag{7.27}
```

Shift $`\ell\to\ell+A`$, so that $`\ell'\to\ell+A'`$ and $`k\to K-\ell`$, with $`A:=(1-x)p-yp'`$, $`A':=(1-y)p'-xp`$ and $`K:=xp+yp'`$. Drop the terms odd in $`\ell`$ and replace $`\ell^\alpha\ell^\beta`$ by $`\eta^{\alpha\beta}\ell^2/d`$; with $`\not\ell\not\ell=\ell^2`$, the numerators of (7.26) become

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
\tag{7.28}
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
\tag{7.29}
```

After Wick rotation, for $`\Delta>0`$ and continued to $`\Delta<0`$ through $`\Delta-i\varepsilon`$, the integrals (7.12) generalize to

```math
\left.
\int\frac{d^d\ell}{(2\pi)^d}\,\frac{(\ell^2)^a}{(\ell^2-\Delta+i\varepsilon)^n}
=\frac{(-1)^{n+a}\,i}{(4\pi)^{d/2}}\,
\frac{\Gamma\bigl(a+\frac d2\bigr)\,\Gamma\bigl(n-a-\frac d2\bigr)}{\Gamma\bigl(\frac d2\bigr)\,\Gamma(n)}\,
(\Delta-i\varepsilon)^{\frac d2+a-n}.
\right.
\tag{7.30}
```

Applying (7.30) to (7.29),

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
\tag{7.31}
```

With $`d=4-\epsilon`$, $`\Gamma(\epsilon/2)=2/\epsilon-\gamma_E+O(\epsilon)`$, $`2/\bar\epsilon`$ as in (7.14), and $`N^\mu`$, $`N_2^\mu`$ in the finite terms taken at $`d=4`$,

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
\tag{7.32}
```

The parameter integrals converge unless $`p^2=p'^2=m_f^2`$; in that on-shell case they diverge logarithmically at $`z\to1`$. With (7.14), the results satisfy $`q_\mu\Lambda_2^\mu(p+q,p)=\Sigma_2(p)-\Sigma_2(p+q)`$, as required by the Ward identity.

**(2) Three Photons**

```math
\left.
E_\gamma=3,\qquad E_F=0\qquad\Longrightarrow\qquad\omega=1 .
\right.
\tag{7.33}
```

The graphs with the two orientations of the fermion loop cancel (Furry's theorem), so the sum of 1PI graphs with three external photons vanishes.

<br><br>





































<a id="qft-ch8"></a>
## 8. Cosmology

<a id="geometry-of-the-universe"></a>
### 8.1 Geometry of the Universe

<a id="cosmology-experimental-facts"></a>
#### Experimental Facts

1. Hubble's law: the universe is expanding.
2. The cosmic microwave background (CMB) is isotropic.
3. The large-scale distribution of galaxies is homogeneous.

<br><br>

<a id="flrw-metric"></a>
#### FLRW Metric

```math
\left.
ds^2=dt^2-a(t)^2\left[\frac{dr^2}{1-kr^2}+r^2\bigl(d\theta^2+\sin^2\theta\,d\phi^2\bigr)\right]
\right.
\tag{8.1}
```

<br><br>

<a id="evolution-of-the-universe"></a>
### 8.2 Evolution of the Universe

<a id="cosmology-dynamics"></a>
#### Dynamics

```math
\left.
\left(\frac{\dot a}{a}\right)^2=\frac{8\pi G}{3}\rho-\frac{k}{a^2}
\right.
\tag{8.2}
```

<br><br>

<a id="dark-matter"></a>
#### Dark Matter

**Experimental Results**

<br><br>

<a id="dark-energy"></a>
#### Dark Energy

<br><br>

<a id="cosmic-evolution"></a>
#### Cosmic Evolution

1. Radiation-dominated era (the early universe)
2. Matter-dominated era
3. Dark-energy-dominated era

<br><br>

<a id="boltzmann-equation"></a>
### 8.3 Boltzmann Equation

<br><br>

## Appendix A. Summary of Feynman Rules

<a id="sm-feynman-rules"></a>
### A.1 Feynman Diagrams of the Standard Model

**Scope and Gauge**

- **Theory**: the minimal Standard Model of [Section 5.3](#electroweak-theory) and [Section 5.4](#qcd), with gauge group $`SU(3)_c\times SU(2)_L\times U(1)_Y`$, three generations of quarks and leptons in the mass bases of Section 5.3, and the Higgs doublet $`H`$. There are no right-handed neutrinos, so the neutrinos are massless; the seesaw fields of [Chapter 6](#qft-ch6) are not included.
- **Electroweak gauge**: the unitary gauge $`H=(0,v_{\mathrm{SM}}+h)^T/\sqrt2`$ of Section 5.3, with $`v_{\mathrm{SM}}\simeq246\,\mathrm{GeV}`$. The electroweak bosons are $`W^\pm_\mu`$, $`Z_\mu`$, $`A^{\mathrm{em}}_\mu`$ and $`h`$; there are no Goldstone fields.
- **Photon and gluons**: the covariant gauge fixing of [Section 4.3](#feynman-diagrams), with one parameter $`\xi`$ for $`A^{\mathrm{em}}_\mu`$ and for the gluons $`A^a_\mu`$ of Section 5.4 (separate parameters may be used),

```math
\left.
\mathcal L_{\mathrm{gf}}=-\frac1{2\xi}\bigl(\partial^\mu A^{\mathrm{em}}_\mu\bigr)^2-\frac1{2\xi}\bigl(\partial^\mu A^a_\mu\bigr)^2 .
\right.
\tag{A.1}
```

- **Order**: tree level, with the tree-level masses of [Section 5.2](#sm-fermions) and Section 5.3.
  - Tree graphs contain no closed loops, so the Faddeev--Popov ghosts of [Section 3.2](#path-integrals-in-field-theory) and the counterterms of [Chapter 7](#qft-ch7) do not enter.
  - These rules are not a loop-ready set: loop calculations in a renormalizable gauge need additional Goldstone, ghost and counterterm rules, which are not given here.
  - Widths are not included. The propagators below are the fixed-order tree-level ones; predictions near the $`W^\pm`$, $`Z`$, $`h`$ or $`t`$ resonance require an appropriate treatment of the width, such as a resummation of the self-energy.

These choices hold only in this subsection.

**Fields and Free Lagrangian**

- **Fermions**: $`\psi_f`$ as in the neutral currents of Section 5.3: $`\psi_f=q_f`$ for $`f=u,d,s,c,b,t`$ (color triplets), $`\psi_f=l_f`$ for $`f=e,\mu,\tau`$, and $`\psi_{\nu_\alpha}=\nu_{\alpha L}`$. Here $`m_f`$ is the mass of $`\psi_f`$, with $`m_{\nu_\alpha}=0`$; $`Q_f`$ is the charge of [Section 5.3](#qed), and $`T_f^3`$ is that of Section 5.3.
- **Vector fields**: $`A^{\mathrm{em}}_\mu`$, $`Z_\mu`$, $`W^\pm_\mu`$ of Section 5.3 and the gluons $`A^a_\mu`$, $`a=1,\ldots,8`$. For each of them write $`X_{\mu\nu}:=\partial_\mu X_\nu-\partial_\nu X_\mu`$.
- **Scalar**: the Higgs field $`h`$.

Inverting the definitions of $`W^\pm_\mu`$, $`Z_\mu`$ and $`A^{\mathrm{em}}_\mu`$ in Section 5.3,

```math
\left.
W^1_\mu=\frac{W^+_\mu+W^-_\mu}{\sqrt2},\qquad
W^2_\mu=\frac{i\bigl(W^+_\mu-W^-_\mu\bigr)}{\sqrt2},\qquad
W^3_\mu=c_WZ_\mu+s_WA^{\mathrm{em}}_\mu,\qquad
B_\mu=-s_WZ_\mu+c_WA^{\mathrm{em}}_\mu .
\right.
\tag{A.2}
```

Since $`W^1_\mu W^{1\nu}+W^2_\mu W^{2\nu}=W^+_\mu W^{-\nu}+W^-_\mu W^{+\nu}`$ and $`(W^3_\mu,B_\mu)\mapsto(Z_\mu,A^{\mathrm{em}}_\mu)`$ is a rotation, the quadratic parts of the gauge kinetic terms, the mass terms of the Gauge-Boson Masses part of Section 5.3, the Higgs mass of Section 5.2 and $`\mathcal L_{\mathrm{gf}}`$ give

```math
\left.
\begin{aligned}
\mathcal L_0={}&\sum_f\bar\psi_f\bigl(i\gamma^\mu\partial_\mu-m_f\bigr)\psi_f
-\frac14A^{\mathrm{em}}_{\mu\nu}A^{\mathrm{em}\,\mu\nu}-\frac1{2\xi}\bigl(\partial^\mu A^{\mathrm{em}}_\mu\bigr)^2
-\frac14A^a_{\mu\nu}A^{a\mu\nu}-\frac1{2\xi}\bigl(\partial^\mu A^a_\mu\bigr)^2\\
&-\frac12W^+_{\mu\nu}W^{-\mu\nu}+m_W^2W^+_\mu W^{-\mu}
-\frac14Z_{\mu\nu}Z^{\mu\nu}+\frac12m_Z^2Z_\mu Z^\mu
+\frac12\partial_\mu h\,\partial^\mu h-\frac12m_h^2h^2 .
\end{aligned}
\right.
\tag{A.3}
```

**Interaction Lagrangian**

Write $`\mathcal L_{\mathrm{SM}}+\mathcal L_{\mathrm{gf}}=\mathcal L_0+\mathcal L_{\mathrm{int}}`$. From Sections 5.2--5.4, with $`\lambda_H=m_h^2/(2v_{\mathrm{SM}}^2)`$ and the constant $`\lambda_Hv_{\mathrm{SM}}^4/4`$ dropped,

```math
\left.
\begin{aligned}
\mathcal L_{\mathrm{int}}={}&\mathcal L_{\mathrm{NC}}+\mathcal L_{\mathrm{CC}}
+g_sA^a_\mu\sum_{f}\bar q_f\gamma^\mu T^aq_f
-\sum_f\frac{m_f}{v_{\mathrm{SM}}}\,h\,\bar\psi_f\psi_f\\
&+\Bigl(\frac{2h}{v_{\mathrm{SM}}}+\frac{h^2}{v_{\mathrm{SM}}^2}\Bigr)\Bigl(m_W^2W^+_\mu W^{-\mu}+\frac12m_Z^2Z_\mu Z^\mu\Bigr)
-\frac{m_h^2}{2v_{\mathrm{SM}}}h^3-\frac{m_h^2}{8v_{\mathrm{SM}}^2}h^4\\
&+\mathcal L_{3g}+\mathcal L_{4g}+\mathcal L_{3W}+\mathcal L_{4W},
\end{aligned}
\right.
\tag{A.4}
```

where $`\mathcal L_{\mathrm{NC}}`$ and $`\mathcal L_{\mathrm{CC}}`$ are the currents of Section 5.3, and the cubic and quartic parts of $`-\frac14F^a_{\mu\nu}F^{a\mu\nu}`$ in Section 5.4 are

```math
\left.
\mathcal L_{3g}=-g_sf^{abc}\bigl(\partial_\mu A^a_\nu\bigr)A^{b\mu}A^{c\nu},\qquad
\mathcal L_{4g}=-\frac{g_s^2}4f^{abc}f^{ade}A^b_\mu A^c_\nu A^{d\mu}A^{e\nu},
\right.
\tag{A.5}
```

using the antisymmetry of $`f^{abc}A^{b\mu}A^{c\nu}`$ in $`\mu,\nu`$. Since $`W^a_{\mu\nu}`$ of Section 5.3 has the form of $`F^a_{\mu\nu}`$ with $`g_s\to g_2`$ and $`f^{abc}\to\epsilon^{abc}`$, $`\mathcal L_{3W}`$ and $`\mathcal L_{4W}`$ are $`\mathcal L_{3g}`$ and $`\mathcal L_{4g}`$ with these replacements, $`A^a_\mu\to W^a_\mu`$ and $`a=1,2,3`$; $`B_\mu`$ has no self-interactions.

**From the Lagrangian to the Rules**

By [Section 4.1](#interaction-picture) and [Section 4.2](#s-matrix-and-wick-theorem), for interactions without derivatives $`\hat{\mathcal H}_{\mathrm{int}}=-\hat{\mathcal L}_{\mathrm{int}}`$, and the order-$`n`$ term of $`\hat S`$ is

```math
\left.
\frac{i^n}{n!}\int d^4x_1\cdots d^4x_n\,\mathcal T\bigl[\hat{\mathcal L}_{\mathrm{int}}(x_1)\cdots\hat{\mathcal L}_{\mathrm{int}}(x_n)\bigr].
\right.
\tag{A.6}
```

Wick's theorem pairs the fields: a contraction between two factors gives a propagator of $`\mathcal L_0`$, a contraction with an external state gives an external factor, and each factor $`i\int d^4x\,\hat{\mathcal L}_{\mathrm{int}}`$ gives a vertex, its $`x`$-integral imposing four-momentum conservation. The $`1/n!`$ cancels against the permutations of the $`n`$ vertices. 

$`\mathcal L_{3g}`$ and $`\mathcal L_{3W}`$ contain derivatives, and the massive vector fields are constrained (Section 1.8), so $`\hat{\mathcal H}_{\mathrm{int}}\neq-\hat{\mathcal L}_{\mathrm{int}}`$ and the time-ordered products of $`\partial_\mu\hat A_\nu`$ and of massive vector fields contain noncovariant contact terms. At tree level these two effects cancel (not derived here). The rules below are the covariant ones, which also follow from the functional integral of [Chapter 3](#qft-ch3) with weight $`e^{iS}`$.

**Vertex Rule**

- **Legs**: leg $`j=1,\ldots,n`$ of a vertex sits on a boson field of $`\mathcal L_{\mathrm{int}}`$ ($`h`$, $`A^{\mathrm{em}}_\mu`$, $`Z_\mu`$, $`W^+_\mu`$, $`W^-_\mu`$ or $`A^a_\mu`$), with four-momentum $`k_j`$ flowing into the vertex and wave function $`\varepsilon_j`$: a vector $`\varepsilon_j^\mu`$, and $`1`$ for $`h`$. A gluon leg also carries an adjoint index $`a_j`$.
- **Vertex factor**: replace each boson field by the plane waves of its legs,

```math
\left.
\phi(x)\to\sum_{j\text{ on }\phi}c_j\,\varepsilon_j\,e^{-ik_j\cdot x},\qquad
A^a_\mu(x)\to\sum_{j\text{ on }A}c_j\,\delta^{aa_j}\varepsilon_{j\mu}\,e^{-ik_j\cdot x},
\right.
\tag{A.7}
```

so that $`\partial_\mu\to-ik_{j\mu}`$ on leg $`j`$, and keep the term proportional to $`c_1\cdots c_n`$:

```math
\left.
\boxed{i\int d^4x\,\mathcal L_{\mathrm{int}}\Big|_{c_1c_2\cdots c_n}=(2\pi)^4\delta^{(4)}\Bigl(\sum_{j=1}^nk_j\Bigr)\,i\mathcal V(\varepsilon_1,\ldots,\varepsilon_n).}
\right.
\tag{A.8}
```

The vertex factor is the tensor $`i\mathcal V`$, obtained by removing the $`\varepsilon_j`$; purely bosonic vertices below are written with lower Lorentz indices. The term linear in every $`c_j`$ sums over all ways of attaching the legs to identical fields, which gives the combinatorial factors of identical fields.

- **Fermion bilinears**: a term $`\bar\psi_{f'}\Gamma\psi_f`$, with $`\Gamma`$ a matrix in spinor and color space multiplying boson fields, gives the matrix $`i\Gamma`$, with its boson legs as above; the fermion line enters the vertex as $`\psi_f`$ and leaves it as $`\psi_{f'}`$.

**Charged and Colored Lines**

- **Charge of $`W^\pm`$**: for $`\theta^3=\theta_Y=\theta`$ constant and $`\theta^1=\theta^2=0`$, the transformation of Section 5.3 is $`e^{i\theta Q}`$. The infinitesimal transformation of the gauge field in Section 5.4, with $`f^{abc}\to\epsilon^{abc}`$, gives $`\delta W^1_\mu=\theta W^2_\mu`$ and $`\delta W^2_\mu=-\theta W^1_\mu`$, so

```math
\left.
\delta W^\pm_\mu=\pm i\theta\,W^\pm_\mu .
\right.
\tag{A.9}
```

Thus $`W^+_\mu`$ has charge $`+e`$ in the sense of Section 5.3, and, like a field $`\psi_f`$ of charge $`Q_fe`$, it annihilates the particle of that charge: a leg on $`W^+_\mu`$ is an incoming $`W^+`$ or an outgoing $`W^-`$, and a leg on $`W^-_\mu`$ is an incoming $`W^-`$ or an outgoing $`W^+`$.
- **Internal $`W`$ lines**: an internal $`W`$ line joins a $`W^+_\mu`$ leg of one vertex to a $`W^-_\nu`$ leg of another. If $`k`$ flows into the first vertex through its $`W^+_\mu`$ leg, then $`-k`$ flows into the second through its $`W^-_\nu`$ leg.
- **Fermion lines**: arrows show the flow of fermion number, and the momentum of a fermion propagator points along the arrow. Along each line, write the factors in the order opposite to the arrow, as in [Section 7.2](#qed-renormalization). For an external antifermion the arrow points opposite to its motion.
- **Color**: quark colors are $`c,c'\in\{1,2,3\}`$, as in Section 7.2. In $`(T^a)_{c'c}`$, $`c`$ is the color of the quark line entering the vertex and $`c'`$ that of the line leaving it; all other vertices on quark lines carry $`\delta_{c'c}`$.

**Propagators**

The contractions of the fields of $`\mathcal L_0`$, Fourier transformed as in [Section 0.1](#fourier-transform), are those of Section 4.3, with $`\delta^{ab}`$ for gluons. In $`\mathcal L_0`$, $`W^1_\mu`$ and $`W^2_\mu`$ are real Proca fields of mass $`m_W`$, so

```math
\left.
\langle0|\mathcal T[\hat W^+_\mu\hat W^-_\nu]|0\rangle=\frac12\Bigl(\langle0|\mathcal T[\hat W^1_\mu\hat W^1_\nu]|0\rangle+\langle0|\mathcal T[\hat W^2_\mu\hat W^2_\nu]|0\rangle\Bigr),\qquad
\langle0|\mathcal T[\hat W^\pm_\mu\hat W^\pm_\nu]|0\rangle=0 .
\right.
\tag{A.10}
```

Since $`\nu_{\alpha L}=P_L\nu_{\alpha L}`$ and $`\overline{\nu_{\alpha L}}=\overline{\nu_{\alpha L}}P_R`$, the neutrino contraction is $`P_L\widetilde S_F(p)P_R`$ at $`m=0`$, and $`P_L\not pP_R=P_L\not p`$. With $`p`$ the momentum of the line,

```math
\left.
\begin{array}{l|l}
\text{line}&\text{factor}\\ \hline
\psi_f,\ f\neq\nu_\alpha,\ p\text{ along the arrow}&\dfrac{i(\not p+m_f)}{p^2-m_f^2+i\varepsilon}\quad(\times\,\delta_{c'c}\text{ for quarks})\\[12pt]
\nu_{\alpha L},\ p\text{ along the arrow}&\dfrac{iP_L\not p}{p^2+i\varepsilon}\\[12pt]
A^{\mathrm{em}}_\mu\text{ to }A^{\mathrm{em}}_\nu&\dfrac{-i}{p^2+i\varepsilon}\left[\eta_{\mu\nu}-(1-\xi)\dfrac{p_\mu p_\nu}{p^2+i\varepsilon}\right]\\[12pt]
A^a_\mu\text{ to }A^b_\nu&\delta^{ab}\,\dfrac{-i}{p^2+i\varepsilon}\left[\eta_{\mu\nu}-(1-\xi)\dfrac{p_\mu p_\nu}{p^2+i\varepsilon}\right]\\[12pt]
W^+_\mu\text{ to }W^-_\nu&\dfrac{-i}{p^2-m_W^2+i\varepsilon}\left(\eta_{\mu\nu}-\dfrac{p_\mu p_\nu}{m_W^2}\right)\\[12pt]
Z_\mu\text{ to }Z_\nu&\dfrac{-i}{p^2-m_Z^2+i\varepsilon}\left(\eta_{\mu\nu}-\dfrac{p_\mu p_\nu}{m_Z^2}\right)\\[12pt]
h&\dfrac{i}{p^2-m_h^2+i\varepsilon}
\end{array}
\right.
\tag{A.11}
```

**External Lines**

The fields have unit pole residue at tree level, so by Section 4.3 and the charge assignment above,

```math
\left.
\begin{array}{l|ll}
\text{external state}&\text{incoming}&\text{outgoing}\\ \hline
\text{fermion}&u^s(p)&\bar u^s(p)\\
\text{antifermion}&\bar v^s(p)&v^s(p)\\
\gamma,\ g,\ Z&\epsilon^r_\mu(p)&\epsilon^{r*}_\mu(p)\\
W^+&\epsilon^r_\mu(p)\text{ on a }W^+_\mu\text{ leg}&\epsilon^{r*}_\mu(p)\text{ on a }W^-_\mu\text{ leg}\\
W^-&\epsilon^r_\mu(p)\text{ on a }W^-_\mu\text{ leg}&\epsilon^{r*}_\mu(p)\text{ on a }W^+_\mu\text{ leg}\\
h&1&1
\end{array}
\right.
\tag{A.12}
```

External quarks and gluons also carry their color and adjoint indices. $`W^\pm`$ and $`Z`$ have the three polarizations of [Section 1.8](#proca-field), and $`\gamma`$ and $`g`$ the two physical ones. Neutrinos use the $`m=0`$ spinors of [Section 1.7](#dirac-field); through the $`P_L`$ in their vertices, only $`P_Lu^s`$ and $`P_Lv^s`$ contribute.

**Vertices: Fermions**

The rows follow from $`\mathcal L_{\mathrm{NC}}`$, $`\mathcal L_{\mathrm{CC}}`$, the quark--gluon term and the $`h\bar\psi_f\psi_f`$ term. Since $`P_R\gamma^\mu=\gamma^\mu P_L`$, $`\overline{q_{fL}}\gamma^\mu q_{f'L}=\bar q_f\gamma^\mu P_Lq_{f'}`$, and with $`(W^+_\mu)^*=W^-_\mu`$ the Hermitian conjugate in $`\mathcal L_{\mathrm{CC}}`$ is

```math
\left.
\frac{g_2}{\sqrt2}\,W^-_\mu\Bigl(\sum_{\alpha=e,\mu,\tau}\bar l_\alpha\gamma^\mu P_L\nu_{\alpha L}
+\sum_{f=u,c,t}\ \sum_{f'=d,s,b}V^*_{ff'}\,\bar q_{f'}\gamma^\mu P_Lq_f\Bigr).
\right.
\tag{A.13}
```

With "in" the fermion line entering the vertex along its arrow, "out" the line leaving it, and the boson leg carrying the index $`\mu`$,

```math
\left.
\begin{array}{lll|l}
\text{in}&\text{out}&\text{boson}&i\mathcal V\\ \hline
\psi_f&\psi_f&A^{\mathrm{em}}_\mu&ieQ_f\gamma^\mu\\[4pt]
\psi_f&\psi_f&Z_\mu&i\dfrac{g_2}{c_W}\gamma^\mu\bigl(T_f^3P_L-Q_fs_W^2\bigr)\\[10pt]
q_f,\ \text{color }c&q_f,\ \text{color }c'&A^a_\mu&ig_s\gamma^\mu(T^a)_{c'c}\\[4pt]
q_{f'},\ f'=d,s,b&q_f,\ f=u,c,t&W^+_\mu&i\dfrac{g_2}{\sqrt2}V_{ff'}\gamma^\mu P_L\\[10pt]
q_f,\ f=u,c,t&q_{f'},\ f'=d,s,b&W^-_\mu&i\dfrac{g_2}{\sqrt2}V^*_{ff'}\gamma^\mu P_L\\[10pt]
l_\alpha&\nu_{\alpha L}&W^+_\mu&i\dfrac{g_2}{\sqrt2}\gamma^\mu P_L\\[10pt]
\nu_{\alpha L}&l_\alpha&W^-_\mu&i\dfrac{g_2}{\sqrt2}\gamma^\mu P_L\\[10pt]
\psi_f&\psi_f&h&-i\dfrac{m_f}{v_{\mathrm{SM}}}
\end{array}
\right.
\tag{A.14}
```

The $`Z`$ vertex equals $`i\frac{g_2}{c_W}\gamma^\mu\bigl[(T_f^3-Q_fs_W^2)P_L-Q_fs_W^2P_R\bigr]`$; for $`\nu_{\alpha L}`$ it is $`i\frac{g_2}{2c_W}\gamma^\mu P_L`$. The photon vertex of the electron is $`-ie\gamma^\mu`$, as in Section 7.2. The neutral and $`h`$ vertices are flavor diagonal, and the neutrinos have no $`\gamma`$ or $`h`$ vertex.

**Vertices: Higgs and Gauge Bosons**

The $`h`$ terms of $`\mathcal L_{\mathrm{int}}`$ contain no derivatives. Attaching the legs to identical fields gives a factor $`2`$ for $`ZZ`$ and for $`hh`$, $`2\cdot2`$ for $`hhZZ`$, $`3!`$ for $`h^3`$ and $`4!`$ for $`h^4`$. With $`m_W=g_2v_{\mathrm{SM}}/2`$ and $`m_Z=m_W/c_W`$,

```math
\left.
\begin{array}{l|l}
\text{legs}&i\mathcal V\\ \hline
h\,W^+_\mu W^-_\nu&i\dfrac{2m_W^2}{v_{\mathrm{SM}}}\eta_{\mu\nu}=ig_2m_W\eta_{\mu\nu}\\[10pt]
h\,Z_\mu Z_\nu&i\dfrac{2m_Z^2}{v_{\mathrm{SM}}}\eta_{\mu\nu}=i\dfrac{g_2m_Z}{c_W}\eta_{\mu\nu}\\[10pt]
h\,h\,W^+_\mu W^-_\nu&i\dfrac{2m_W^2}{v_{\mathrm{SM}}^2}\eta_{\mu\nu}=i\dfrac{g_2^2}{2}\eta_{\mu\nu}\\[10pt]
h\,h\,Z_\mu Z_\nu&i\dfrac{2m_Z^2}{v_{\mathrm{SM}}^2}\eta_{\mu\nu}=i\dfrac{g_2^2}{2c_W^2}\eta_{\mu\nu}\\[10pt]
h\,h\,h&-i\dfrac{3m_h^2}{v_{\mathrm{SM}}}\\[10pt]
h\,h\,h\,h&-i\dfrac{3m_h^2}{v_{\mathrm{SM}}^2}
\end{array}
\right.
\tag{A.15}
```

**Vertices: Gauge-Boson Self-Interactions**

Define

```math
\left.
\begin{aligned}
\mathcal Y^{(3)}_{\mu\nu\rho}(k_1,k_2,k_3)&:=\eta_{\mu\nu}(k_1-k_2)_\rho+\eta_{\nu\rho}(k_2-k_3)_\mu+\eta_{\rho\mu}(k_3-k_1)_\nu,\\
\mathcal Y^{(4)}_{\mu\nu,\rho\sigma}&:=2\eta_{\mu\nu}\eta_{\rho\sigma}-\eta_{\mu\rho}\eta_{\nu\sigma}-\eta_{\mu\sigma}\eta_{\nu\rho}.
\end{aligned}
\right.
\tag{A.16}
```

**(1) Gluons**

Label the legs $`j=1,2,3,4`$ by $`(a_1,\mu),(a_2,\nu),(a_3,\rho),(a_4,\sigma)`$ with momenta $`k_j`$ into the vertex. In $`\mathcal L_{3g}`$ the rule sums over the assignments $`\pi\in S_3`$ of the legs to the three fields, the first being the differentiated one. By $`f^{a_{\pi(1)}a_{\pi(2)}a_{\pi(3)}}=\mathop{\rm sgn}\nolimits (\pi)f^{a_1a_2a_3}`$,

```math
\left.
\begin{aligned}
i\mathcal V(\varepsilon_1,\varepsilon_2,\varepsilon_3)
&=i\,(-g_s)\,(-i)\,f^{a_1a_2a_3}\sum_{\pi\in S_3}\,\mathop{\rm sgn}\nolimits (\pi)\,\bigl(k_{\pi(1)}\cdot\varepsilon_{\pi(2)}\bigr)\bigl(\varepsilon_{\pi(1)}\cdot\varepsilon_{\pi(3)}\bigr)\\
&=g_sf^{a_1a_2a_3}\,\mathcal Y^{(3)}_{\mu\nu\rho}(k_1,k_2,k_3)\,\varepsilon_1^\mu\varepsilon_2^\nu\varepsilon_3^\rho .
\end{aligned}
\right.
\tag{A.17}
```

In $`\mathcal L_{4g}`$ the $`4!`$ assignments fall into six classes of four equal terms, since $`f^{abc}f^{ade}A^b_\mu A^c_\nu A^{d\mu}A^{e\nu}`$ is invariant under $`(b,c)\leftrightarrow(d,e)`$ and under the simultaneous exchanges $`b\leftrightarrow c`$, $`d\leftrightarrow e`$. Writing the summed adjoint index of the result as $`b`$,

```math
\left.
\boxed{
\begin{aligned}
A^{a_1}_\mu A^{a_2}_\nu A^{a_3}_\rho:\quad i\mathcal V&=g_sf^{a_1a_2a_3}\,\mathcal Y^{(3)}_{\mu\nu\rho}(k_1,k_2,k_3),\\
A^{a_1}_\mu A^{a_2}_\nu A^{a_3}_\rho A^{a_4}_\sigma:\quad i\mathcal V&=-ig_s^2\Bigl[f^{a_1a_2b}f^{a_3a_4b}\bigl(\eta_{\mu\rho}\eta_{\nu\sigma}-\eta_{\mu\sigma}\eta_{\nu\rho}\bigr)
+f^{a_1a_3b}f^{a_2a_4b}\bigl(\eta_{\mu\nu}\eta_{\rho\sigma}-\eta_{\mu\sigma}\eta_{\nu\rho}\bigr)\\
&\qquad+f^{a_1a_4b}f^{a_2a_3b}\bigl(\eta_{\mu\nu}\eta_{\rho\sigma}-\eta_{\mu\rho}\eta_{\nu\sigma}\bigr)\Bigr].
\end{aligned}}
\right.
\tag{A.18}
```

**(2) Electroweak Gauge Bosons**

$`\mathcal L_{3W}`$ and $`\mathcal L_{4W}`$ give the vertices of (1) with $`g_s\to g_2`$, $`f^{abc}\to\epsilon^{abc}`$, for legs on $`W^a_\mu`$, $`a=1,2,3`$. By the inverted definitions above, a leg on $`W^+_\mu`$, $`W^-_\mu`$, $`Z_\mu`$ or $`A^{\mathrm{em}}_\mu`$ is a leg on $`W^a_\mu`$ with the isospin vector $`n_+^a`$, $`n_-^a`$, $`c_Wn_3^a`$ or $`s_Wn_3^a`$ in place of $`\delta^{aa_j}`$, where

```math
\left.
n_\pm:=\frac1{\sqrt2}(1,\pm i,0),\qquad n_3:=(0,0,1),\qquad (x\times y)^a:=\epsilon^{abc}x^by^c .
\right.
\tag{A.19}
```

These satisfy, with no complex conjugation in $`x^ay^a`$,

```math
\left.
n_+\times n_-=-i\,n_3,\qquad n_\pm\times n_3=\pm i\,n_\pm,\qquad
n_+^an_-^a=n_3^an_3^a=1,\qquad n_\pm^an_\pm^a=n_\pm^an_3^a=0 .
\right.
\tag{A.20}
```

Hence $`\epsilon^{abc}n_+^an_-^bn_3^c=n_+^a(n_-\times n_3)^a=-i`$, so the three-boson vertex is $`-ig_2`$ times $`c_W`$ or $`s_W`$, with $`g_2s_W=e`$. Let $`x_j`$ be the isospin vector of leg $`j`$. In the four-boson vertex the three terms carry $`(x_1\times x_2)^b(x_3\times x_4)^b`$, $`(x_1\times x_3)^b(x_2\times x_4)^b`$ and $`(x_1\times x_4)^b(x_2\times x_3)^b`$. For legs $`W^+W^+W^-W^-`$, in this order, the first vanishes and the other two equal $`(n_+\times n_-)^b(n_+\times n_-)^b=-1`$. For legs $`W^+W^-`$ followed by two neutral legs, the first vanishes and the other two equal $`(n_+\times n_3)^b(n_-\times n_3)^b=1`$, times $`c_W^2`$, $`s_W^2`$ or $`c_Ws_W`$. With all momenta into the vertex,

```math
\left.
\begin{array}{l|l}
\text{legs}&i\mathcal V\\ \hline
W^+_\mu(k_1)\,W^-_\nu(k_2)\,A^{\mathrm{em}}_\rho(k_3)&-ie\,\mathcal Y^{(3)}_{\mu\nu\rho}(k_1,k_2,k_3)\\[4pt]
W^+_\mu(k_1)\,W^-_\nu(k_2)\,Z_\rho(k_3)&-ig_2c_W\,\mathcal Y^{(3)}_{\mu\nu\rho}(k_1,k_2,k_3)\\[4pt]
W^+_\mu\,W^+_\nu\,W^-_\rho\,W^-_\sigma&ig_2^2\,\mathcal Y^{(4)}_{\mu\nu,\rho\sigma}\\[4pt]
W^+_\mu\,W^-_\nu\,Z_\rho\,Z_\sigma&-ig_2^2c_W^2\,\mathcal Y^{(4)}_{\mu\nu,\rho\sigma}\\[4pt]
W^+_\mu\,W^-_\nu\,A^{\mathrm{em}}_\rho\,A^{\mathrm{em}}_\sigma&-ie^2\,\mathcal Y^{(4)}_{\mu\nu,\rho\sigma}\\[4pt]
W^+_\mu\,W^-_\nu\,Z_\rho\,A^{\mathrm{em}}_\sigma&-ieg_2c_W\,\mathcal Y^{(4)}_{\mu\nu,\rho\sigma}
\end{array}
\right.
\tag{A.21}
```

For example, for an incoming $`W^+`$ of momentum $`p`$ and an outgoing $`W^+`$ of momentum $`p'`$ at a $`W^+W^-A^{\mathrm{em}}`$ vertex, the $`W^+_\mu`$ leg has $`k_1=p`$ and $`\varepsilon_1=\epsilon(p)`$, and the $`W^-_\nu`$ leg has $`k_2=-p'`$ and $`\varepsilon_2=\epsilon^*(p')`$.

These tables exhaust $`\mathcal L_{\mathrm{int}}`$. In particular, at tree level no vertex contains only neutral gauge bosons, and $`h`$ couples neither to $`\gamma`$ nor to gluons.

**Assembling Diagrams**

1. Draw every connected tree graph with the given external lines and the vertices above; each internal $`W`$ line joins a $`W^+`$ leg to a $`W^-`$ leg.
2. Fix the internal momenta by four-momentum conservation at each vertex.
3. Multiply the vertex factors, propagators and external factors. Lorentz indices are raised and lowered with $`\eta`$, so that each repeated Lorentz index occurs once up and once down; e.g. an external vector on the leg $`\mu`$ of a vertex gives $`i\mathcal V_{\mu\cdots}\,\epsilon^{r\mu}(p)`$ with $`\epsilon^{r\mu}=\eta^{\mu\nu}\epsilon^r_\nu`$, and a vector propagator $`D_{\alpha\beta}`$ of the table joins the vertex factors $`i\mathcal V_{\cdots\mu}`$ and $`i\mathcal V'_{\nu\cdots}`$ of its two ends through $`\eta^{\mu\alpha}D_{\alpha\beta}\eta^{\beta\nu}`$. Contract the spinor indices along each fermion line against the arrow, the colors along each quark line, and the adjoint indices of internal gluons with $`\delta^{ab}`$.
4. Exchanging identical external fermions changes the sign, as in Section 4.3. Tree graphs have symmetry factor $`1`$, because the factors from identical fields are already in the vertices.
5. The sum is $`i\mathcal M_{fi}`$ of Section 4.2. Cross sections and decay rates follow from [Section 4.6](#cross-sections-and-decay-rates), with $`C_{\mathrm{id}}`$ for identical final particles.

**Example: $`t\to bW^+`$**

Let the $`t`$ have momentum $`p`$, spin $`s`$, color $`c`$, the $`b`$ momentum $`p'`$, spin $`s'`$, color $`c'`$, and the $`W^+`$ momentum $`k`$, polarization $`r`$, with $`p=p'+k`$. The outgoing $`W^+`$ sits on a $`W^-_\mu`$ leg, and the line enters as $`q_t`$ and leaves as $`q_b`$, so

```math
\left.
i\mathcal M=\bar u^{s'}(p')\Bigl(i\frac{g_2}{\sqrt2}V^*_{tb}\gamma^\mu P_L\Bigr)u^s(p)\,\epsilon^{r*}_\mu(k)\,\delta_{c'c} .
\right.
\tag{A.22}
```
