> English, part 1/4 · [Complete file](QFT.md) · [1](QFT-en-part-01.md) · [2](QFT-en-part-02.md) · [3](QFT-en-part-03.md) · [4](QFT-en-part-04.md)

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
  - [1.7 The Dirac Field $`\psi`$ ](QFT-en-part-02.md#dirac-field)
    - [Lagrangian](QFT-en-part-02.md#dirac-lagrangian)
    - [Solutions of the Dirac Equation in the Weyl Representation](QFT-en-part-02.md#weyl-spinor-solutions)
    - [Dirac Bilinears](QFT-en-part-02.md#dirac-bilinears)
  - [1.8 The Proca Field](QFT-en-part-02.md#proca-field)
    - [Lagrangian](QFT-en-part-02.md#proca-lagrangian)
    - [Solutions of the Proca Equation](QFT-en-part-02.md#proca-field-solutions)
  - [1.9 The Vector Field](QFT-en-part-02.md#vector-field)
    - [Lagrangian](QFT-en-part-02.md#maxwell-lagrangian)
    - [Solutions of the Maxwell Equations](QFT-en-part-02.md#maxwell-field-solutions)
- [2. Operator Quantization](QFT-en-part-02.md#qft-ch2)
  - [2.1 Canonical Quantization](QFT-en-part-02.md#canonical-quantization)
  - [2.2 Quantization with Dirac Brackets](QFT-en-part-02.md#quantization-with-dirac-brackets)
    - [Quantization of the Complex Scalar Field](QFT-en-part-02.md#complex-scalar-field-quantization)
    - [Quantization of the Dirac Field](QFT-en-part-02.md#dirac-field-quantization)
    - [Quantization of the Proca Field](QFT-en-part-02.md#proca-field-quantization)
  - [2.3 Gupta–Bleuler Quantization](QFT-en-part-02.md#gupta-bleuler-quantization)
  - [2.4 Symmetry](QFT-en-part-02.md#symmetry)
    - [Schrödinger Picture](QFT-en-part-02.md#schrodinger-picture)
    - [Heisenberg Picture](QFT-en-part-02.md#heisenberg-picture)
- [3. The Standard Model](QFT-en-part-02.md#qft-ch3)
  - [3.1 Yang–Mills Theory](QFT-en-part-02.md#yang-mills)
  - [3.2 Quantum Electrodynamics](QFT-en-part-02.md#qed)
  - [3.3 Quantum Chromodynamics](QFT-en-part-02.md#qcd)
  - [3.4 Spontaneous Symmetry Breaking and the Higgs Mechanism](QFT-en-part-02.md#higgs-mechanism)
    - [Higgs Lagrangian](QFT-en-part-02.md#higgs-lagrangian)
    - [Spontaneous Symmetry Breaking](QFT-en-part-02.md#spontaneous-symmetry-breaking)
    - [Higgs Mechanism](QFT-en-part-02.md#higgs-mechanism-masses)
  - [3.5 Electroweak Theory](QFT-en-part-03.md#electroweak-theory)
    - [Leptons in the Standard Model](QFT-en-part-03.md#sm-leptons)
    - [Kinetic Terms](QFT-en-part-03.md#electroweak-kinetic-terms)
    - [Yukawa Couplings and Charged-Lepton Masses](QFT-en-part-03.md#charged-lepton-masses)
    - [Gauge-Boson Masses](QFT-en-part-03.md#gauge-boson-masses)
    - [Quarks](QFT-en-part-03.md#sm-quarks)
    - [Charged and Neutral Currents](QFT-en-part-03.md#electroweak-currents)
- [4. Path Integrals](QFT-en-part-03.md#qft-ch4)
  - [4.1 Path Integrals in Quantum Mechanics](QFT-en-part-03.md#path-integrals-in-quantum-mechanics)
  - [4.2 Path Integrals in Quantum Field Theory](QFT-en-part-03.md#path-integrals-in-field-theory)
  - [4.3 $`\phi^3`$ Theory](QFT-en-part-03.md#phi-cubed-theory)
  - [4.4 Path Integrals for Fermion Fields](QFT-en-part-03.md#path-integrals-for-fermion-fields)
    - [Grassmann Algebra](QFT-en-part-03.md#grassmann-algebra)
    - [Calculus on the Grassmann Algebra](QFT-en-part-03.md#grassmann-calculus)
- [5. New Physics Beyond the Standard Model](QFT-en-part-03.md#qft-ch5)
  - [5.1 Seesaw Mechanism](QFT-en-part-03.md#seesaw-mechanism)
    - [Type-I Seesaw](QFT-en-part-03.md#type-i-seesaw)
    - [Type-II Seesaw](QFT-en-part-03.md#type-ii-seesaw)
    - [Type-III Seesaw](QFT-en-part-03.md#type-iii-seesaw)
    - [Leptogenesis](QFT-en-part-03.md#leptogenesis)
  - [5.2 Dark Matter](QFT-en-part-03.md#dark-matter)
- [6. Scattering Theory](QFT-en-part-03.md#qft-ch6)
  - [6.1 Interaction Picture](QFT-en-part-03.md#interaction-picture)
  - [6.2 The S-Matrix and Wick's Theorem](QFT-en-part-03.md#s-matrix-and-wick-theorem)
  - [6.3 Feynman Diagrams and Feynman Rules](QFT-en-part-03.md#feynman-diagrams)
  - [6.4 Correlation Functions](QFT-en-part-03.md#correlation-functions)
  - [6.5 LSZ Reduction Formula](QFT-en-part-04.md#lsz-reduction)
  - [6.6 Cross Sections and Decay Rates](QFT-en-part-04.md#cross-sections-and-decay-rates)
- [7. Renormalization](QFT-en-part-04.md#qft-ch7)
  - [7.1 QED Renormalization](QFT-en-part-04.md#qed-renormalization)
- [8. Multi-Loop Renormalization](QFT-en-part-04.md#qft-ch8)
- [9. Cosmology](QFT-en-part-04.md#qft-ch9)

---

<a id="qft-ch0"></a>
## 0. Mathematical Foundations

<a id="fourier-transform"></a>
### 0.1 Fourier Transform

We use the following convention for the four-dimensional Fourier transform, with the factor $`(2\pi)^{-4}`$ included in the inverse transform:

```math
\begin{aligned}
\widetilde f(p)&=\int d^4x\,e^{+ip\cdot x}f(x),\\
f(x)&=\int\frac{d^4p}{(2\pi)^4}\,e^{-ip\cdot x}\widetilde f(p).
\end{aligned}
```

Here $`x^\mu=(t,\mathbf x)`$ and $`p^\mu=(p^0,\mathbf p)`$, and the phase is given by

```math
p\cdot x=p_\mu x^\mu=p^0t-\mathbf p\cdot\mathbf x.
```

The Fourier representations of the Dirac $`\delta`$ function are

```math
\begin{aligned}
\int\frac{d^4p}{(2\pi)^4}\,e^{-ip\cdot(x-y)}&=\delta^{(4)}(x-y),\\[6pt]
\int d^4x\,e^{i(p-q)\cdot x}&=(2\pi)^4\delta^{(4)}(p-q).
\end{aligned}
```


<br><br>

<a id="gamma-matrices"></a>
### 0.2 $`\gamma`$ Matrices: Weyl Representation

The Pauli matrices are

```math
\sigma^1=\begin{pmatrix}0&1\\1&0\end{pmatrix},\qquad
\sigma^2=\begin{pmatrix}0&-i\\i&0\end{pmatrix},\qquad
\sigma^3=\begin{pmatrix}1&0\\0&-1\end{pmatrix}.
```

**Properties of the Pauli Matrices**

For each $`i=1,2,3`$,

```math
(\sigma^i)^\dagger=\sigma^i,\qquad
(\sigma^i)^2=I_2,\qquad
(\sigma^i)^{-1}=\sigma^i,\qquad
\mathop{\rm tr}\nolimits\,\sigma^i=0,\qquad
\det\sigma^i=-1.
```

Thus, each Pauli matrix is both Hermitian and unitary, with eigenvalues $`+1`$ and $`-1`$.

The product identity is

```math
\sigma^i\sigma^j=\delta^{ij}I_2+i\epsilon^{ijk}\sigma^k.
```

This gives the commutation and anticommutation relations, as well as the trace orthogonality relation:

```math
[\sigma^i,\sigma^j]=2i\epsilon^{ijk}\sigma^k,\qquad
\{\sigma^i,\sigma^j\}=2\delta^{ij}I_2,\qquad
\mathop{\rm tr}\nolimits (\sigma^i\sigma^j)=2\delta^{ij}.
```

For any $`\mathbf a,\mathbf b\in\mathbb R^3`$, the product identity can also be written as

```math
(\mathbf a\cdot\boldsymbol\sigma)(\mathbf b\cdot\boldsymbol\sigma)
=(\mathbf a\cdot\mathbf b)I_2
+i(\mathbf a\times\mathbf b)\cdot\boldsymbol\sigma,
\qquad \boldsymbol\sigma=(\sigma^1,\sigma^2,\sigma^3).
```

**$`\gamma`$ matrices**

Pauli four-vectors

```math
\sigma^\mu:=(I_2,\boldsymbol\sigma),\qquad
\bar\sigma^\mu:=(I_2,-\boldsymbol\sigma),\qquad \mu=0,1,2,3.
```

Using them, the $`\gamma`$ matrices in the Weyl representation are defined as:

```math
\gamma^\mu:=
\begin{pmatrix}
0&\sigma^\mu\\
\bar\sigma^\mu&0
\end{pmatrix}_{4\times4}.
```

These matrices satisfy 

```math
\{\gamma^\mu,\gamma^\nu\}=2\eta^{\mu\nu}I_4.
```

```math
(\gamma^0)^2=I_4,\qquad
(\gamma^i)^2=-I_4,\\
(\gamma^0)^\dagger=\gamma^0,\qquad
(\gamma^i)^\dagger=-\gamma^i.
```

Hence each $`\gamma^\mu`$ is unitary:

```math
(\gamma^\mu)^\dagger\gamma^\mu=I_4.
```

Define

```math
\gamma^5:=i\gamma^0\gamma^1\gamma^2\gamma^3
=\begin{pmatrix}-I_2&0\\0&I_2\end{pmatrix}
.
```

It satisfies

```math
(\gamma^5)^2=I_4,\qquad
\{\gamma^5,\gamma^\mu\}=0,\qquad
(\gamma^5)^\dagger = (\gamma^5).
```

<br><br>

<a id="classical-poincare"></a>
### 0.3 IO(1,3) Group

**The Group O(1,3)** 

To distinguish a matrix $`\Lambda`$ from the corresponding tensor $`\Lambda`$ of coordinate transformation, we denote the matrix by $`[\Lambda]`$ and the tensor simply by $`\Lambda`$. We use the same notation for $`\eta`$.

The matrix $`[\Lambda]`$

```math
O(1,3):=\{[\Lambda]\in GL(4,\mathbb R)\mid [\Lambda]^T[\eta][\Lambda]=[\eta]\}.
```

where $`[\eta]=\mathop{\rm diag}\nolimits (1,-1,-1,-1)`$. 

The tensor $`\Lambda`$ 

Given a specific diffeomorphism of Minkowskispacetime $`\phi:x\mapsto x'`$, we obtain a tensor

```math
\Lambda^\mu{}_\nu:=\frac{\partial x'^\mu}{\partial x^\nu}.
```

By the way, we can prove that the isometries of Minkowski spacetime must be linear up to a translation.

The entry of $`[\Lambda]`$ in row $`\mu`$ and column $`\nu`$ is the corresponding component of the tensor $`\Lambda`$:

```math
[\Lambda]_{\mu\nu}=\Lambda^\mu{}_\nu.
```

Similarly,

```math
[\eta]_{\mu\nu}=\eta_{\mu\nu}.
```

Therefore, equivalently, we obtain the following relationship:

```math
\eta_{\mu\nu}\Lambda^\mu{}_\rho\Lambda^\nu{}_\sigma=\eta_{\rho\sigma}.
```

where we have used the relation $`([\Lambda]^T)_{\mu\nu}=\Lambda^\nu{}_\mu`$. This is exactly the condition for $`\phi`$ to be an isometry of Minkowski spacetime.


The inverse and transpose of $`[\Lambda]`$ satisfy

```math
[\Lambda]^{-1}=[\eta][\Lambda]^T[\eta],\qquad
[\Lambda][\eta][\Lambda]^T=[\eta],
```

so $`[\Lambda]^{-1}`$ and $`[\Lambda]^T`$ also belong to $`O(1,3)`$. 

In components, the first relation reads

```math
(\Lambda^{-1})^\mu{}_\nu=\Lambda_\nu{}^\mu.
```

**Connectedness**

Taking the determinant of $`[\Lambda]^T[\eta][\Lambda]=[\eta]`$ gives

```math
(\det[\Lambda])^2=1\quad\Longrightarrow\quad\det[\Lambda]=\pm1.
```

Setting $`\rho=\sigma=0`$ in $`\eta_{\mu\nu}\Lambda^\mu{}_\rho\Lambda^\nu{}_\sigma=\eta_{\rho\sigma}`$ gives

```math
(\Lambda^0{}_0)^2=1+\sum_i(\Lambda^i{}_0)^2\ge1\quad\Longrightarrow\quad\Lambda^0{}_0\ge1\ \text{or}\ \Lambda^0{}_0\le-1.
```

We can prove that $`O(1,3)`$ has exactly these four connected components.

Define the time reversal $`T`$ and the space inversion $`P`$ by

```math
T:(t,\mathbf x)\mapsto(-t,\mathbf x),\qquad
P:(t,\mathbf x)\mapsto(t,-\mathbf x),
```

whose matrices are

```math
[T]=\mathop{\rm diag}\nolimits (-1,1,1,1),\qquad
[P]=\mathop{\rm diag}\nolimits (1,-1,-1,-1).
```

The corresponding tensors are

```math
T^\mu{}_\nu=\delta^\mu{}_\nu-2\delta^\mu{}_0\delta^0{}_\nu,\qquad
P^\mu{}_\nu=-\delta^\mu{}_\nu+2\delta^\mu{}_0\delta^0{}_\nu.
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
SO(1,3)=\mathcal L^\uparrow_+\cup\mathcal L^\downarrow_+.
```

Furthermore, $`SO(1,3)^+=\mathcal L^\uparrow_+`$ is a subgroup of $`O(1,3)`$.

Physically, $`T`$ and $`P`$ correspond to time-reversal symmetry and parity symmetry, respectively. What is usually called Lorentz symmetry is invariance under $`SO(1,3)^+`$ only. The distinction matters: no violation of Lorentz symmetry has ever been observed, so it is regarded as a fundamental symmetry. Parity, in contrast, is violated in the weak interaction, as proposed by Lee and Yang and confirmed experimentally by Wu et al.; time-reversal symmetry is violated as well.

**Lie Algebra of O(1,3)**

Consider a one-parameter subgroup $`e^{tX}`$, $`t\in\mathbb R`$, of $`O(1,3)`$. It satisfies

```math
(e^{tX})^T[\eta]\,e^{tX}=[\eta].
```

Expanding the left-hand side to first order in $`t`$ gives

```math
(I+tX^T)[\eta](I+tX)+O(t^2)=[\eta]+t\left(X^T[\eta]+[\eta]X\right)+O(t^2),
```

so the first-order term must vanish:

```math
X^T[\eta]+[\eta]X=0.
```

Therefore,

```math
\mathfrak o(1,3):=\{X\in M_4(\mathbb R)\mid X^T[\eta]+[\eta]X=0\}.
```

Furthermore, this relation can be written more explicitly as

```math
[\eta]X=-X^T[\eta]=-([\eta]X)^T,
```

which means that the matrix $`[\eta]X`$ is antisymmetric. 

An antisymmetric $`4\times4`$ matrix has $`4\times3/2=6`$ independent real parameters. Hence the general form of $`X`$ is

```math
X=\begin{pmatrix}
0&b^1&b^2&b^3\\
b^1&0&-\theta^3&\theta^2\\
b^2&\theta^3&0&-\theta^1\\
b^3&-\theta^2&\theta^1&0
\end{pmatrix}
=\sum_i\theta^iJ^i+\sum_ib^iK^i
```

In physics, the following notation is commonly used:

```math
e^{-\frac i2\omega^{\mu\nu}J^{\mu\nu}}
```

where $`\omega_{\mu\nu}`$ is antisymmetric in its indices, and

```math
-iJ^{ij}=\epsilon_{ijk}J^k,\qquad -iJ^{0i}=K^i.
```

Each $`J^{\mu\nu}`$ is simply a $`4\times4`$ matrix, with $`\alpha,\beta`$ labelling its rows and columns. Its entries are

```math
(J^{\mu\nu})_{\alpha\beta}=i\left(\eta^{\mu\alpha}\delta^{\nu\beta}-\eta^{\nu\alpha}\delta^{\mu\beta}\right).
```

Explicitly (row index $`\alpha`$, column index $`\beta`$; the remaining components follow from $`J^{\nu\mu}=-J^{\mu\nu}`$), the rotation generators $`J^{ij}=i\epsilon_{ijk}J^k`$ are Hermitian:

```math
J^{23}=\begin{pmatrix}0&0&0&0\\0&0&0&0\\0&0&0&-i\\0&0&i&0\end{pmatrix},\quad
J^{31}=\begin{pmatrix}0&0&0&0\\0&0&0&i\\0&0&0&0\\0&-i&0&0\end{pmatrix},\quad
J^{12}=\begin{pmatrix}0&0&0&0\\0&0&-i&0\\0&i&0&0\\0&0&0&0\end{pmatrix},
```

and the boost generators $`J^{0i}=iK^i`$ are anti-Hermitian:

```math
J^{01}=\begin{pmatrix}0&i&0&0\\i&0&0&0\\0&0&0&0\\0&0&0&0\end{pmatrix},\quad
J^{02}=\begin{pmatrix}0&0&i&0\\0&0&0&0\\i&0&0&0\\0&0&0&0\end{pmatrix},\quad
J^{03}=\begin{pmatrix}0&0&0&i\\0&0&0&0\\0&0&0&0\\i&0&0&0\end{pmatrix}.
```


<br><br>

<a id="greens-functions"></a>
### 0.4 Green's Functions

**Definition and Integral Solution**

In the general construction below, $`x,y`$ denote $`d`$ independent variables. Let $`\mathcal K_x`$ be a linear differential operator on $`\Omega\subseteq\mathbb R^d`$, and let $`\mathcal B`$ specify linear boundary or initial data:

```math
\mathcal K_xu(x)=f(x),\qquad \mathcal Bu=b.
```

Assume the data are sufficiently regular and the integrals below exist. Equations involving $`\delta`$ functions are understood in the sense of distributions.

- **Green's function**: A kernel satisfying the differential equation and homogeneous boundary or initial conditions,

```math
\boxed{\mathcal K_xG(x,y)=\delta^{(d)}(x-y),\qquad \mathcal B_xG(x,y)=0.}
```

The subscript $`x`$ specifies the variable on which the operator acts. The choice of boundary or initial conditions is part of the definition of $`G`$.

- **Integral solution**: If $`u_{\mathrm h}`$ solves the homogeneous equation with the prescribed data, then

```math
\begin{aligned}
\boxed{u(x)=u_{\mathrm h}(x)+\int_\Omega d^dy\,G(x,y)f(y),}\\
\mathcal K_xu_{\mathrm h}(x)=0,\qquad \mathcal Bu_{\mathrm h}=b.
\end{aligned}
```

Indeed,

```math
\begin{aligned}
\mathcal K_xu(x)
&=\int_\Omega d^dy\,[\mathcal K_xG(x,y)]f(y)
=\int_\Omega d^dy\,\delta^{(d)}(x-y)f(y)=f(x),\\
\mathcal Bu&=\mathcal Bu_{\mathrm h}
+\int_\Omega d^dy\,[\mathcal B_xG(x,y)]f(y)=b.
\end{aligned}
```

The solution is unique if $`\mathcal Ku=0`$, $`\mathcal Bu=0`$ has only the zero solution in the chosen function space. With nontrivial zero modes, uniqueness fails and solvability may impose compatibility conditions; an inverse on arbitrary sources cannot be assumed. Without boundary or initial conditions, two kernels satisfying the first equation in (0.41) can differ by a solution of the homogeneous equation in $`x`$.

**Construction by Fourier Transform**

For a constant-coefficient operator on Minkowski spacetime, return to $`x^\mu=(t,\mathbf x)`$ and the Fourier convention (0.1). If the chosen conditions are also translation invariant, $`G(x,y)=G(x-y)`$, and

```math
\begin{aligned}
\mathcal K(-ip)\widetilde G(p)&=1,\\
G(x-y)&=\int\frac{d^4p}{(2\pi)^4}\,
e^{-ip\cdot(x-y)}\widetilde G(p),\\
\widetilde G(p)&=\left[\frac{1}{\mathcal K(-ip)}\right]_{\mathrm{prescription}}.
\end{aligned}
```

Here $`\mathcal K(-ip)`$ is obtained by replacing each $`\partial_\mu`$ with $`-ip_\mu`$. At zeros of $`\mathcal K(-ip)`$, the reciprocal requires a distributional prescription fixed by the chosen conditions; the algebraic equation alone does not select it.

**Poisson Equation and Boundary Data**

First consider a smooth source of compact support in $`\mathbb R^3`$:

```math
-\nabla^2u(\mathbf x)=f(\mathbf x),\qquad
u(\mathbf x)\to0\quad\text{as }|\mathbf x|\to\infty.
```

For $`r:=|\mathbf x-\mathbf y|>0`$, a rotationally invariant kernel that vanishes at infinity obeys

```math
\nabla^2G_0(r)=\frac{1}{r^2}\frac{d}{dr}\left(r^2\frac{dG_0}{dr}\right)=0
\quad\Longrightarrow\quad G_0(r)=\frac{A}{r}.
```

Integrating $`-\nabla^2G_0=\delta^{(3)}`$ over a ball $`B_\epsilon`$ centred at the source fixes $`A`$:

```math
\begin{aligned}
1&=-\int_{B_\epsilon}d^3x\,\nabla^2G_0
=-4\pi\epsilon^2\left.\frac{dG_0}{dr}\right|_{r=\epsilon}
=4\pi A,\\
G_0(\mathbf x,\mathbf y)&=\frac{1}{4\pi|\mathbf x-\mathbf y|}.
\end{aligned}
```

Hence

```math
\boxed{u(\mathbf x)=\int_{\mathbb R^3}d^3y\,
\frac{f(\mathbf y)}{4\pi|\mathbf x-\mathbf y|}.}
```

Now let $`\Omega\subset\mathbb R^3`$ be bounded with smooth boundary, and prescribe $`u=b`$ on $`\partial\Omega`$. The Dirichlet Green's function for $`-\nabla^2`$ is symmetric in its arguments and satisfies

```math
\begin{aligned}
-\nabla_{\mathbf y}^2G_D(\mathbf x,\mathbf y)
&=\delta^{(3)}(\mathbf y-\mathbf x),\qquad \mathbf y\in\Omega,\\
G_D(\mathbf x,\mathbf y)&=0,\qquad \mathbf y\in\partial\Omega.
\end{aligned}
```

Let $`\mathbf n_y`$ be the outward unit normal and $`\partial_{n_y}:=\mathbf n_y\cdot\nabla_{\mathbf y}`$. Green's second identity is

```math
\int_\Omega d^3y\,(v\nabla^2w-w\nabla^2v)
=\int_{\partial\Omega}dS_y\,(v\partial_{n_y}w-w\partial_{n_y}v).
```

Apply (0.50) to $`v=u`$, $`w=G_D(\mathbf x,\cdot)`$ on $`\Omega\setminus B_\epsilon(\mathbf x)`$ and take $`\epsilon\to0^+`$. For $`\mathbf x\in\Omega`$,

```math
\boxed{\begin{aligned}
u(\mathbf x)&=\int_\Omega d^3y\,G_D(\mathbf x,\mathbf y)f(\mathbf y)\\
&\quad-\int_{\partial\Omega}dS_y\,b(\mathbf y)\partial_{n_y}G_D(\mathbf x,\mathbf y).
\end{aligned}}
```

The second term supplies the nonzero boundary data. The free-space kernel $`G_0`$ in (0.47) generally does not satisfy the boundary condition in (0.49).

**Klein–Gordon Equation and Initial Data**

With $`m\geq0`$ and the mostly-minus metric, consider

```math
(\Box+m^2)u(x)=f(x),\qquad
\Box:=\partial_\mu\partial^\mu=\partial_t^2-\nabla^2.
```

- **Retarded Green's function**: The translation-invariant kernel with support only at nonnegative time differences,

```math
(\Box+m^2)G_{\mathrm{ret}}(t,\mathbf x)
=\delta(t)\delta^{(3)}(\mathbf x),\qquad
G_{\mathrm{ret}}(t,\mathbf x)=0\quad(t<0).
```

Here the source point has been translated to the origin. Since $`\mathcal K(-ip)=m^2-p^2`$, the retarded prescription is

```math
\widetilde G_{\mathrm{ret}}(p)
=-\lim_{\epsilon\to0^+}\frac{1}{(p^0+i\epsilon)^2-E_{\mathbf p}^2},\qquad
E_{\mathbf p}:=\sqrt{\mathbf p^2+m^2}.
```

Both poles lie below the real $`p^0`$ axis. Closing the contour in the lower half-plane for $`t>0`$ and the upper half-plane for $`t<0`$ gives

```math
\boxed{G_{\mathrm{ret}}(t,\mathbf x)
=\theta(t)\int\frac{d^3p}{(2\pi)^3}\,
e^{i\mathbf p\cdot\mathbf x}\frac{\sin(E_{\mathbf p}t)}{E_{\mathbf p}}.}
```

Here $`\theta(t)`$ is the Heaviside function, and the value at $`E_{\mathbf p}=0`$ is understood by continuity. The equal-time limits are

```math
G_{\mathrm{ret}}(0^+,\mathbf x)=0,\qquad
\partial_tG_{\mathrm{ret}}(0^+,\mathbf x)=\delta^{(3)}(\mathbf x).
```

For prescribed initial data $`u(t_0,\mathbf x)=u_0(\mathbf x)`$ and $`\partial_tu(t_0,\mathbf x)=u_1(\mathbf x)`$, (0.56) yields, for $`t>t_0`$,

```math
\boxed{\begin{aligned}
u(t,\mathbf x)
&=\int d^3y\,\bigl[
\partial_tG_{\mathrm{ret}}(t-t_0,\mathbf x-\mathbf y)u_0(\mathbf y)\\
&\hspace{4.5em}+G_{\mathrm{ret}}(t-t_0,\mathbf x-\mathbf y)u_1(\mathbf y)\bigr]\\
&\quad+\int_{t_0}^{t}dt'\int d^3y\,
G_{\mathrm{ret}}(t-t',\mathbf x-\mathbf y)f(t',\mathbf y).
\end{aligned}}
```

For $`m=0`$, the spatial integral in (0.55) gives the wave-equation kernel. Writing $`r:=|\mathbf x|`$,

```math
\begin{aligned}
G_{\mathrm{ret}}(t,\mathbf x)\big|_{m=0}
&=\frac{\theta(t)}{2\pi^2r}\int_0^\infty dp\,\sin(pr)\sin(pt)\\
&=\boxed{\frac{\delta(t-r)}{4\pi r}}.
\end{aligned}
```

With zero initial data, extend $`f(t',\mathbf y)`$ by zero for $`t'<t_0`$. Then (0.57) reduces to

```math
\boxed{u(t,\mathbf x)=\int d^3y\,
\frac{f(t-|\mathbf x-\mathbf y|,\mathbf y)}{4\pi|\mathbf x-\mathbf y|}.}
```

For comparison with the scalar Feynman propagator defined in (6.12), the Feynman prescription for the same normalization $`\mathcal KG_F=\delta^{(4)}`$ gives

```math
\begin{aligned}
G_F(x-y)&=-\lim_{\varepsilon\to0^+}\int\frac{d^4p}{(2\pi)^4}\,
\frac{e^{-ip\cdot(x-y)}}{p^2-m^2+i\varepsilon}
=i\Delta_F(x-y),\\
(\Box_x+m^2)\Delta_F(x-y)&=-i\delta^{(4)}(x-y).
\end{aligned}
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
\begin{aligned}
C:[t_0,t_f]&\to\mathrm{Conf},\\
t&\mapsto C(t),
\end{aligned}
```

with velocity $`\dot C(t):=dC/dt`$.

- **Dynamical structure**: the Lagrangian, a smooth function

```math
\begin{aligned}
L:\mathbb R^n\times\mathbb R^n\times\mathbb R&\to\mathbb R,\\
(x,y,t)&\mapsto L(x,y,t).
\end{aligned}
```

- **Action**: the functional on paths

```math
\boxed{
\begin{aligned}
S:\{\text{paths}\}&\to\mathbb R,\\
C&\mapsto S[C]:=\int_{t_0}^{t_f}dt\,L\bigl(C(t),\dot C(t),t\bigr).
\end{aligned}}
```

- **Solutions**: paths $`\bar C`$ at which $`S`$ is stationary under variations with fixed endpoints,

```math
\frac{d}{ds}S[\bar C+s\eta]\Big|_{s=0}=0,
```

for every smooth $`\eta:[t_0,t_f]\to\mathbb R^n`$ with $`\eta(t_0)=\eta(t_f)=0`$.

**Euler–Lagrange Equations**

For a path $`C`$ and $`\eta`$ as in the definition of solutions, write $`\frac{\partial L}{\partial x_a}\big|_C`$ and $`\frac{\partial L}{\partial y_a}\big|_C`$ for the partial derivatives of $`L`$ evaluated at $`\bigl(C(t),\dot C(t),t\bigr)`$. Then

```math
\begin{aligned}
\frac{d}{ds}S[C+s\eta]\Big|_{s=0}
&=\int_{t_0}^{t_f}dt\sum_{a=1}^n\Bigl(\frac{\partial L}{\partial x_a}\Big|_C\,\eta_a+\frac{\partial L}{\partial y_a}\Big|_C\,\dot\eta_a\Bigr)\\
&=\int_{t_0}^{t_f}dt\sum_{a=1}^n\biggl[\frac{\partial L}{\partial x_a}\Big|_C-\frac{d}{dt}\Bigl(\frac{\partial L}{\partial y_a}\Big|_C\Bigr)\biggr]\eta_a\\
&\quad+\biggl[\sum_{a=1}^n\frac{\partial L}{\partial y_a}\Big|_C\,\eta_a\biggr]_{t_0}^{t_f}.
\end{aligned}
```

The boundary term vanishes because $`\eta(t_0)=\eta(t_f)=0`$. 

Since $`\eta`$ is arbitrary, the solutions are exactly the paths $`\bar C`$ with

```math
\boxed{\frac{d}{dt}\Bigl(\frac{\partial L}{\partial y_a}\Big|_{\bar C}\Bigr)-\frac{\partial L}{\partial x_a}\Big|_{\bar C}=0,\qquad a=1,\ldots,n.}
```

<br><br>

<a id="lagrangian-symmetry"></a>
#### Symmetry Transformations and Noether's Theorem

**Transformations**

- **Internal transformation**: 
a one-parameter family of diffeomorphisms $`\phi_\lambda:\mathrm{Conf}\to\mathrm{Conf}`$, $`\lambda\in\mathbb R`$, with $`(\lambda,q)\mapsto\phi_\lambda(q)`$ smooth and $`\phi_0=\mathrm{id}`$, acting on paths pointwise,

```math
\begin{aligned}
\Phi:\mathbb R\times\{\text{paths}\}&\to\{\text{paths}\},\\
(\lambda,C)&\mapsto\Phi_\lambda C:=\phi_\lambda\circ C,
\end{aligned}
```

so that $`\Phi_\lambda C:[t_0,t_f]\to\mathrm{Conf}`$, $`t\mapsto\phi_\lambda\bigl(C(t)\bigr)`$, with velocity

```math
\frac{d}{dt}(\Phi_\lambda C)_a(t)=\sum_{b=1}^n\frac{\partial(\phi_\lambda)_a}{\partial q_b}\bigl(C(t)\bigr)\,\dot C_b(t),
```

where $`(\phi_\lambda)_a(q)`$ is the $`a`$-th coordinate of $`\phi_\lambda(q)`$.

- **Time translation**: the shift of paths in time,

```math
\begin{aligned}
\Theta:\mathbb R\times\{\text{paths}\}&\to\{\text{paths}\},\\
(\tau,C)&\mapsto\Theta_\tau C:=C(\cdot-\tau),
\end{aligned}
```

so that $`\Theta_\tau C:[t_0+\tau,t_f+\tau]\to\mathrm{Conf}`$, $`t\mapsto C(t-\tau)`$, with velocity

```math
\frac{d}{dt}(\Theta_\tau C)(t)=\dot C(t-\tau).
```

**Symmetry Transformations**

- **Symmetry transformation**: an internal transformation $`\Phi`$, respectively a time translation $`\Theta`$, under which the action of every path is invariant,

```math
\boxed{
\begin{aligned}
S[\Phi_\lambda C]&=S[C]\quad\text{for every path }C\text{ and every }\lambda\in\mathbb R,\\
S[\Theta_\tau C]&=S[C]\quad\text{for every path }C\text{ and every }\tau\in\mathbb R.
\end{aligned}}
```

Write $`\frac{\partial\phi_\lambda}{\partial q}(q)`$ for the Jacobian matrix with entries $`\frac{\partial(\phi_\lambda)_a}{\partial q_b}(q)`$, so that the velocity of $`\Phi_\lambda C`$ is $`\frac{\partial\phi_\lambda}{\partial q}\bigl(C(t)\bigr)\,\dot C(t)`$. 

Substituting the transformed paths into the action, and shifting $`t\to t+\tau`$ in the second case,

```math
\begin{aligned}
S[\Phi_\lambda C]&=\int_{t_0}^{t_f}dt\,L\Bigl(\phi_\lambda\bigl(C(t)\bigr),\ \frac{\partial\phi_\lambda}{\partial q}\bigl(C(t)\bigr)\,\dot C(t),\ t\Bigr),\\
S[\Theta_\tau C]&=\int_{t_0+\tau}^{t_f+\tau}dt\,L\bigl(C(t-\tau),\dot C(t-\tau),t\bigr)=\int_{t_0}^{t_f}dt\,L\bigl(C(t),\dot C(t),t+\tau\bigr).
\end{aligned}
```

Hence $`\Phi`$, respectively $`\Theta`$, is a symmetry transformation if and only if, for all $`(x,y,t)\in\mathrm{Conf}\times\mathbb R^n\times\mathbb R`$ and all $`\lambda`$, respectively all $`\tau`$,

```math
\boxed{
\begin{aligned}
L\Bigl(\phi_\lambda(x),\ \frac{\partial\phi_\lambda}{\partial q}(x)\,y,\ t\Bigr)&=L(x,y,t),\\
L(x,y,t+\tau)&=L(x,y,t).
\end{aligned}}
```

The second condition holds for all $`\tau`$ if and only if $`\partial L/\partial t=0`$ on $`\mathrm{Conf}\times\mathbb R^n\times\mathbb R`$.

**Conserved Quantities**

- **Conserved quantity**: a smooth function

```math
\begin{aligned}
\mathcal Q:\mathrm{Conf}\times\mathbb R^n\times\mathbb R&\to\mathbb R,\\
(x,y,t)&\mapsto\mathcal Q(x,y,t),
\end{aligned}
```

such that $`\mathcal Q\bigl(\bar C(t),\dot{\bar C}(t),t\bigr)`$ is independent of $`t`$ for every solution $`\bar C`$.

**Noether's Theorem**

**(A) Time Translation**

If $`\Theta`$ is a symmetry transformation, i.e. $`\partial L/\partial t=0`$ on $`\mathrm{Conf}\times\mathbb R^n\times\mathbb R`$, then the energy

```math
\boxed{E(x,y,t):=\sum_{a=1}^n\frac{\partial L}{\partial y_a}(x,y,t)\,y_a-L(x,y,t)}
```

is a conserved quantity.

**(B) Internal Transformation**

If $`\Phi`$ is a symmetry transformation, then, with the generator

```math
\begin{aligned}
X:\mathrm{Conf}&\to\mathbb R^n,\\
q&\mapsto\frac{\partial\phi_\lambda(q)}{\partial\lambda}\Big|_{\lambda=0},
\end{aligned}
```

The generator gives the form of the infinitesimal transformation at $`\lambda=0`$: $`\phi_\lambda(q)=q+\lambda\,X(q)+O(\lambda^2),`$ i.e. the coordinates transform as $`q_a\mapsto q_a+\lambda X_a(q)`$.

Correspondingly, the velocity transforms as $`y\mapsto y+\lambda\,\frac{\partial X}{\partial q}(q)\,y+O(\lambda^2),`$ i.e. $`y_a\mapsto y_a+\lambda\sum_b\frac{\partial X_a}{\partial q_b}(q)\,y_b`$.

the function

```math
\boxed{\mathcal Q(x,y,t):=\sum_{a=1}^n\frac{\partial L}{\partial y_a}(x,y,t)\,X_a(x)}
```

is a conserved quantity.

**Proof**

(A) Let $`\bar C`$ be a solution. Write $`L|_{\bar C}:=L\bigl(\bar C(t),\dot{\bar C}(t),t\bigr)`$.

 By the chain rule and the Euler–Lagrange equations,

```math
\frac{d}{dt}E\bigl(\bar C(t),\dot{\bar C}(t),t\bigr)
=\frac{d}{dt}\Bigl(\sum_{a=1}^n\frac{\partial L}{\partial y_a}\Big|_{\bar C}\,\dot{\bar C}_a(t)-L\big|_{\bar C}\Bigr)
=-\frac{\partial L}{\partial t}\Big|_{\bar C}
```

along every solution, which vanishes if $`\partial L/\partial t=0`$.

(B) Differentiating the first symmetry condition with respect to $`\lambda`$ at $`\lambda=0`$,  gives for all $`(x,y,t)\in\mathrm{Conf}\times\mathbb R^n\times\mathbb R`$

```math
\sum_{a=1}^n\Bigl(\frac{\partial L}{\partial x_a}\,X_a(x)
+\frac{\partial L}{\partial y_a}\sum_{b=1}^n\frac{\partial X_a}{\partial q_b}(x)\,y_b\Bigr)=0,
```

with the partial derivatives of $`L`$ evaluated at $`(x,y,t)`$. 

For a solution $`\bar C`$, the chain rule and the Euler–Lagrange equations give

```math
\frac{d}{dt}\mathcal Q\bigl(\bar C(t),\dot{\bar C}(t),t\bigr)
=\sum_{a=1}^n\Bigl(\frac{\partial L}{\partial x_a}\Big|_{\bar C}\,X_a\bigl(\bar C(t)\bigr)
+\frac{\partial L}{\partial y_a}\Big|_{\bar C}\sum_{b=1}^n\frac{\partial X_a}{\partial q_b}\bigl(\bar C(t)\bigr)\,\dot{\bar C}_b(t)\Bigr),
```

which is the identity above evaluated at $`\bigl(\bar C(t),\dot{\bar C}(t),t\bigr)`$, hence zero. $`\square`$


**Momentum**

Fix $`b\in\{1,\ldots,n\}`$ and translate the $`b`$-th coordinate,

```math
\bigl(\phi_\lambda(q)\bigr)_a=q_a+\lambda\,\delta_{ab}.
```

The Jacobian $`\partial\phi_\lambda/\partial q`$ is the identity, so the velocity is unchanged, and the symmetry condition reads $`L(\phi_\lambda(x),y,t)=L(x,y,t)`$ for all $`\lambda`$, i.e. $`\partial L/\partial x_b=0`$.

Generator: $`X_a(q)=\delta_{ab}`$.

Conserved quantity:

```math
\mathcal Q(x,y,t)=\sum_{a=1}^n\frac{\partial L}{\partial y_a}(x,y,t)\,\delta_{ab}=\frac{\partial L}{\partial y_b}(x,y,t),
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
\begin{aligned}
F:M&\to\mathbb R^N,\\
z&\mapsto F(z).
\end{aligned}
```

- **Solutions**: smooth curves $`C:I\to M`$, with $`I\subset\mathbb R`$ an open interval, such that

```math
\boxed{\dot C_A(t)=F_A\bigl(C(t)\bigr),\qquad A=1,\ldots,N.}
```

**(1) Determinism**

Since $`F`$ is smooth, for every $`t_0\in\mathbb R`$ and $`z^{(0)}\in M`$ there is a unique maximal solution $`C`$ with $`C(t_0)=z^{(0)}`$. The state at one time therefore determines the state at every later and every earlier time on its interval, and through each point of $`M`$ passes exactly one solution curve.

Assume every maximal solution is defined on all of $`\mathbb R`$. The flow of $`F`$ is

```math
\begin{aligned}
\Phi_t:M&\to M,\\
z^{(0)}&\mapsto C(t),
\end{aligned}
```

where $`C`$ is the solution with $`C(0)=z^{(0)}`$. It satisfies

- $`\partial_t\Phi_t(z)=F\bigl(\Phi_t(z)\bigr)`$ and $`\Phi_0=\mathrm{id}`$;
- $`\Phi_t\circ\Phi_s=\Phi_{t+s}`$, since $`F`$ does not depend on $`t`$, so each $`\Phi_t`$ is a diffeomorphism with inverse $`\Phi_{-t}`$.

**(2) Volume in State Space**

For a region $`D\subset M`$, write $`\mathrm{vol}(D):=\int_Dd^Nz`$ and $`J_t:=\frac{\partial\Phi_t}{\partial z}`$ for the Jacobian matrix of $`\Phi_t`$. Differentiating $`\partial_t\Phi_t=F\circ\Phi_t`$ with respect to $`z`$ and using Jacobi's formula $`d\det J=\det J\,\mathop{\rm tr}\nolimits (J^{-1}dJ)`$,

```math
\begin{aligned}
\partial_tJ_t&=\Bigl(\frac{\partial F}{\partial z}\circ\Phi_t\Bigr)J_t,
\qquad
\partial_t\det J_t=\Bigl(\sum_{A=1}^N\frac{\partial F_A}{\partial z_A}\circ\Phi_t\Bigr)\det J_t,\\
\frac{d}{dt}\mathrm{vol}\bigl(\Phi_t(D)\bigr)
&=\frac{d}{dt}\int_Dd^Nz\,\det J_t
=\int_{\Phi_t(D)}d^Nz\,\sum_{A=1}^N\frac{\partial F_A}{\partial z_A}.
\end{aligned}
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
\begin{aligned}
f:M&\to\mathbb R,\\
z&\mapsto f(z).
\end{aligned}
```

- **Dynamical structure**:
  - the Poisson bracket $`\{\ ,\ \}_{\mathrm{PB}}`$ of (1.81);
  - the Hamiltonian, a smooth function

```math
\begin{aligned}
H:M&\to\mathbb R,\\
z&\mapsto H(z),
\end{aligned}
```

with no explicit time dependence.

- **Solutions**: smooth curves $`C:I\to M`$, with $`I\subset\mathbb R`$ an open interval, such that

```math
\frac{d}{dt}q_a\bigl(C(t)\bigr)=\frac{\partial H}{\partial p_a}\bigl(C(t)\bigr),\quad
\frac{d}{dt}p_a\bigl(C(t)\bigr)=-\frac{\partial H}{\partial q_a}\bigl(C(t)\bigr)
\qquad\Longleftrightarrow\qquad
\frac{d}{dt}f\bigl(C(t)\bigr)=\{f,H\}_{\mathrm{PB}}\bigl(C(t)\bigr)\quad\text{for all }f.
```

<br><br>

<a id="hamiltonian-symmetry"></a>
#### Symmetries and Noether's Theorem

**Transformations**

- **Transformation**: a diffeomorphism with no explicit time dependence,

```math
\begin{aligned}
\phi:M&\to M,\\
z&\mapsto\phi(z),
\end{aligned}
\qquad
Q_a:=q_a\circ\phi,\quad P_a:=p_a\circ\phi,\quad \phi_*f:=f\circ\phi^{-1},
```

where $`Q_a(z),P_a(z)`$ are the coordinates of $`\phi(z)`$, and $`\phi_*`$ is the pushforward of (1.58), with $`(\phi_*f)(\phi(z))=f(z)`$.

**Symmetry Transformations**

- **Symmetry transformation**: a transformation $`\phi`$ that preserves both the Poisson bracket and the Hamiltonian,

```math
\boxed{
\begin{aligned}
&\text{(i)}\quad\{f\circ\phi,\,g\circ\phi\}_{\mathrm{PB}}=\{f,g\}_{\mathrm{PB}}\circ\phi\quad\text{for all }f,g,\\
&\text{(ii)}\quad H\circ\phi=H.
\end{aligned}}
```

A transformation satisfying (i) is a canonical transformation. Replacing $`f,g`$ by $`f\circ\phi^{-1},g\circ\phi^{-1}`$ shows that (i) is equivalent to $`\{\phi_*f,\phi_*g\}_{\mathrm{PB}}=\phi_*\{f,g\}_{\mathrm{PB}}`$; (ii) is equivalent to $`\phi_*H=H`$, i.e. $`H(\phi(z))=H(z)`$ for all $`z\in M`$.

Write $`z_A`$, $`A=1,\ldots,2n`$, for all phase-space coordinates and $`Z_A:=z_A\circ\phi`$. By the chain rule,

```math
\begin{aligned}
\{f\circ\phi,\,g\circ\phi\}_{\mathrm{PB}}
&=\sum_{A,B}\Bigl(\frac{\partial f}{\partial z_A}\circ\phi\Bigr)\Bigl(\frac{\partial g}{\partial z_B}\circ\phi\Bigr)\{Z_A,Z_B\}_{\mathrm{PB}},\\
\{f,g\}_{\mathrm{PB}}\circ\phi
&=\sum_{A,B}\Bigl(\frac{\partial f}{\partial z_A}\circ\phi\Bigr)\Bigl(\frac{\partial g}{\partial z_B}\circ\phi\Bigr)\{z_A,z_B\}_{\mathrm{PB}}.
\end{aligned}
```

The brackets $`\{z_A,z_B\}_{\mathrm{PB}}`$ are constants, and $`f=z_A`$, $`g=z_B`$ pick out a single term, so (i) holds if and only if $`\{Z_A,Z_B\}_{\mathrm{PB}}=\{z_A,z_B\}_{\mathrm{PB}}`$. By (1.81), (i) is equivalent to

```math
\boxed{
\{Q_a,Q_b\}_{\mathrm{PB}}=\{P_a,P_b\}_{\mathrm{PB}}=0,\qquad
\{Q_a,P_b\}_{\mathrm{PB}}=\delta_{ab}.}
```

A symmetry transformation maps solutions to solutions. Let $`C`$ be a solution and $`C':=\phi\circ C`$. Applying (1.25) to $`f\circ\phi`$, then (ii) and (i),

```math
\begin{aligned}
\frac{d}{dt}f\bigl(C'(t)\bigr)
&=\{f\circ\phi,\,H\}_{\mathrm{PB}}\bigl(C(t)\bigr)\\
&=\{f\circ\phi,\,H\circ\phi\}_{\mathrm{PB}}\bigl(C(t)\bigr)
=\{f,H\}_{\mathrm{PB}}\bigl(C'(t)\bigr)
\end{aligned}
```

for every $`f`$, so $`C'`$ is a solution by (1.25).

**Conserved Quantities**

- **Conserved quantity**: an observable $`f`$ such that $`f\bigl(C(t)\bigr)`$ is independent of $`t`$ for every solution $`C`$.

(1.25) is (1.20) with $`N=2n`$ and $`F_A=\{z_A,H\}_{\mathrm{PB}}`$. Since a solution passes through each point of $`M`$, (1.25) shows that $`f`$ is a conserved quantity if and only if

```math
\boxed{\{f,H\}_{\mathrm{PB}}=0.}
```

**Noether's Theorem**

Let $`\phi_\lambda`$, $`\lambda\in\mathbb R`$, be a one-parameter subgroup of symmetry transformations:

- $`\phi_\lambda\circ\phi_\mu=\phi_{\lambda+\mu}`$ for all $`\lambda,\mu\in\mathbb R`$; in particular $`\phi_0=\mathrm{id}`$;
- $`(\lambda,z)\mapsto\phi_\lambda(z)`$ is smooth.

Define the generator

```math
\begin{aligned}
X:M&\to\mathbb R^{2n},\\
z&\mapsto\frac{\partial\phi_\lambda(z)}{\partial\lambda}\Big|_{\lambda=0},
\end{aligned}
```

so that $`\phi_\lambda`$ is the flow of $`X`$. If $`M`$ is simply connected, there is a smooth function $`G:M\to\mathbb R`$, unique up to an additive constant, with

```math
X_A=\{z_A,G\}_{\mathrm{PB}},\qquad A=1,\ldots,2n,
```

and

```math
\boxed{\{G,H\}_{\mathrm{PB}}=0,}
```

so $`G`$ is a conserved quantity.

**Proof**

Write $`\omega_{AB}:=\{z_A,z_B\}_{\mathrm{PB}}`$. By (1.81) it is constant and invertible, and $`\{f,g\}_{\mathrm{PB}}=\sum_{A,B}\omega_{AB}\frac{\partial f}{\partial z_A}\frac{\partial g}{\partial z_B}`$. Define $`Y`$ by $`X_A=\sum_B\omega_{AB}Y_B`$. Differentiate (i) with $`f=z_A`$, $`g=z_B`$, and (ii), with respect to $`\lambda`$ at $`\lambda=0`$:

```math
\begin{aligned}
0&=\{X_A,z_B\}_{\mathrm{PB}}+\{z_A,X_B\}_{\mathrm{PB}}
=\sum_{C,D}\omega_{AC}\,\omega_{BD}\Bigl(\frac{\partial Y_D}{\partial z_C}-\frac{\partial Y_C}{\partial z_D}\Bigr),\\
0&=\sum_A\frac{\partial H}{\partial z_A}\,X_A.
\end{aligned}
```

Since $`\omega`$ is invertible, $`\partial Y_D/\partial z_C=\partial Y_C/\partial z_D`$. On a simply connected $`M`$ this gives $`Y_B=\partial G/\partial z_B`$ for a smooth $`G`$, unique up to a constant, i.e. (1.33). The second line of (1.35) is then $`\sum_A\frac{\partial H}{\partial z_A}\{z_A,G\}_{\mathrm{PB}}=\{H,G\}_{\mathrm{PB}}=0`$, which is (1.34). $`\square`$

**(1) Time Evolution and Energy**

Taking $`f=H`$ in (1.31), $`\{H,H\}_{\mathrm{PB}}=0`$, so $`H`$ is a conserved quantity. With $`G=H`$, (1.33) gives $`X_A=\{z_A,H\}_{\mathrm{PB}}=F_A`$, so the subgroup generated by $`H`$ is the time evolution $`\Phi_t`$ of (1.21).

**(2) Translations and Momentum**

Let $`M=\mathbb R^{2n}`$ and fix $`k\in\mathbb R^n`$. Take $`\phi_\lambda(q,p)=(q+\lambda k,\,p)`$. Then $`Q_a=q_a+\lambda k_a`$ and $`P_a=p_a`$ satisfy (1.29), and $`\phi_\lambda`$ is a symmetry transformation if and only if $`H(q+\lambda k,p)=H(q,p)`$ for all $`\lambda`$, i.e. $`\sum_ak_a\,\partial H/\partial q_a=0`$. Here $`X=(k,0)`$, and (1.33) holds with

```math
\boxed{G=\sum_{a=1}^nk_a\,p_a,}
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
\text{Field}:\text{Spacetime}\longrightarrow\text{Vector Space},
```

```math
\boxed{\Psi:\mathbb R^4\longrightarrow\mathbb R^n\ \text{or}\ \mathbb C^n
}
```

Additional regularity conditions, such as $`C^\infty`$ smoothness, may be imposed.

The space of fields $`\{\Psi\}`$ carries a representation of $`ISO(1,3)^+`$. For $`(\Lambda,a)\in ISO(1,3)^+`$,

```math
\Psi\xrightarrow{\;(\Lambda,a)\;}U(\Lambda,a)\Psi,
```

where $`U`$ is an infinite-dimensional representation that can be constructed from the finite-dimensional representation $`D(\Lambda)`$:

```math
\boxed{
\begin{aligned}
[U(\Lambda,a)\Psi]_\alpha(x)
&:=D_{\alpha\beta}(\Lambda)
[(\Lambda,a)_*\Psi]_\beta(x)\\
&=D_{\alpha\beta}(\Lambda)
\Psi_\beta(\Lambda^{-1}x-\Lambda^{-1}a).
\end{aligned}
}
```

<br><br>

<a id="lorentz-finite-representations"></a>
#### Finite-Dimensional Representations of $`SO(1,3)^+`$

$`U`$ is constructed from $`D`$ by (1.40), and $`D`$ is recovered from $`U`$ through $`[U(\Lambda,0)\Psi](0)=D(\Lambda)\Psi(0)`$. Hence

```math
\begin{aligned}
\Psi_\alpha(x),\ \alpha=1,\ldots,n
&\quad\Longleftrightarrow\quad\text{infinite-dimensional representation }U(\Lambda,a)\\
&\quad\Longleftrightarrow\quad n\text{-dimensional representation }D(\Lambda)\text{ of }SO(1,3)^+.
\end{aligned}
```

**Lie Algebra Representations**

For $`X,Y\in\mathfrak o(1,3)`$,

```math
\rho(X):=\frac{d}{dt}D(e^{tX})\Big|_{t=0},\qquad
D(e^{X})=e^{\rho(X)},\qquad
\rho([X,Y])=[\rho(X),\rho(Y)].
```

$`SO(1,3)^+`$ is connected, so $`D`$ is determined by $`\rho`$. Extend $`\rho`$ complex-linearly, $`\rho(X+iY):=\rho(X)+i\rho(Y)`$, to the complexified Lie algebra $`\mathfrak o(1,3)_{\mathbb C}`$, defined by (0.32) with $`M_4(\mathbb R)`$ replaced by $`M_4(\mathbb C)`$. By (0.36), $`\mathfrak o(1,3)_{\mathbb C}`$ contains every $`J^{\mu\nu}`$, and $`D(e^{-\frac i2\omega_{\mu\nu}J^{\mu\nu}})=e^{-\frac i2\omega_{\mu\nu}\rho(J^{\mu\nu})}`$. For the Dirac field, $`\rho(J^{\mu\nu})=S^{\mu\nu}`$ (1.100).

**Decomposition of $`\mathfrak o(1,3)_{\mathbb C}`$**

From (0.34),

```math
[J^i,J^j]=\epsilon_{ijk}J^k,\qquad
[J^i,K^j]=\epsilon_{ijk}K^k,\qquad
[K^i,K^j]=-\epsilon_{ijk}J^k.
```

Define

```math
\begin{aligned}
A^i&:=\frac12\Bigl(\frac12\epsilon_{ijk}J^{jk}+iJ^{0i}\Bigr)=\frac i2\bigl(J^i+iK^i\bigr),\\
B^i&:=\frac12\Bigl(\frac12\epsilon_{ijk}J^{jk}-iJ^{0i}\Bigr)=\frac i2\bigl(J^i-iK^i\bigr),
\end{aligned}
```

i.e. $`A^1=\frac12(J^{23}+iJ^{01})`$, $`A^2=\frac12(J^{31}+iJ^{02})`$, $`A^3=\frac12(J^{12}+iJ^{03})`$, and $`B^i`$ is the same with $`iJ^{0i}\to-iJ^{0i}`$. $`A^i`$ and $`B^i`$ are not real, so they lie in $`\mathfrak o(1,3)_{\mathbb C}`$ but not in $`\mathfrak o(1,3)`$. By (1.43),

```math
\boxed{[A^i,A^j]=i\epsilon_{ijk}A^k,\qquad
[B^i,B^j]=i\epsilon_{ijk}B^k,\qquad
[A^i,B^j]=0.}
```

Hence

```math
\mathfrak o(1,3)_{\mathbb C}=\mathfrak g_A\oplus\mathfrak g_B,\qquad
\mathfrak g_A:=\mathop{\rm span}\nolimits\,_{\mathbb C}\{A^1,A^2,A^3\},\quad
\mathfrak g_B:=\mathop{\rm span}\nolimits\,_{\mathbb C}\{B^1,B^2,B^3\}.
```

The maps $`A^i\mapsto\sigma^i/2`$ and $`B^i\mapsto\sigma^i/2`$ identify each of $`\mathfrak g_A`$ and $`\mathfrak g_B`$ with the complexification of $`\mathfrak{su}(2)\cong\mathfrak o(3)`$.

**Irreducible Representations**

Take representations $`(\rho_A,V_A)`$ of $`\mathfrak g_A`$ and $`(\rho_B,V_B)`$ of $`\mathfrak g_B`$, with $`n_A:=\dim V_A`$ and $`n_B:=\dim V_B`$. Their tensor (Kronecker) product $`(\rho,V_A\otimes V_B)`$ is, for $`v_A\in\mathfrak g_A`$ and $`v_B\in\mathfrak g_B`$,

```math
\begin{aligned}
\rho(v_A+v_B)&:=\rho_A(v_A)\otimes I_{n_B}+I_{n_A}\otimes\rho_B(v_B),\\
\rho(v_A+v_B)\bigl(|a\rangle\otimes|b\rangle\bigr)&=\rho_A(v_A)|a\rangle\otimes|b\rangle+|a\rangle\otimes\rho_B(v_B)|b\rangle,\\
e^{\rho(v_A+v_B)}&=e^{\rho_A(v_A)}\otimes e^{\rho_B(v_B)}.
\end{aligned}
```

The last line holds because the two terms in the first line commute.

The irreducible representations of $`\mathfrak{su}(2)`$ are $`V_j`$ with basis $`|j,m\rangle`$, $`m=-j,\ldots,j`$, on which $`\rho_A(A^3)`$ (or $`\rho_B(B^3)`$) acts as $`m`$. Here $`j=0,\frac12,1,\ldots`$ and $`\dim V_j=2j+1`$. Every finite-dimensional irreducible representation of $`\mathfrak g_A\oplus\mathfrak g_B`$ is $`V_{j_1}\otimes V_{j_2}`$, and every finite-dimensional representation is a direct sum of these:

```math
\boxed{(j_1,j_2),\qquad j_1,j_2\in\{0,\tfrac12,1,\tfrac32,\ldots\},\qquad\dim=(2j_1+1)(2j_2+1).}
```

**Rotation by $`2\pi`$**

Since $`A^3+B^3=iJ^3`$ by (1.44), on $`(j_1,j_2)`$

```math
e^{2\pi J^3}=I_4,\qquad
e^{2\pi\rho(J^3)}=e^{-2\pi i\rho(A^3+B^3)}=(-1)^{2(j_1+j_2)}I_n.
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
\begin{aligned}
\mathcal L:(\mathbb R^n\ \text{or}\ \mathbb C^n)\times(\mathbb R^n\ \text{or}\ \mathbb C^n)^4&\to\mathbb R,\\
(\Psi_\alpha,\partial_\mu\Psi_\alpha)&\mapsto\mathcal L(\Psi_\alpha,\partial_\mu\Psi_\alpha),
\end{aligned}
```

in which $`\partial_\mu\Psi_\alpha`$ are independent variables, with no explicit dependence on $`x`$.

- **Action**: the functional on fields, for any bounded region $`\Omega\subset\mathbb R^4`$,

```math
\boxed{S[\Psi]:=\int_\Omega d^4x\,\mathcal L\bigl(\Psi_\alpha(x),\partial_\mu\Psi_\alpha(x)\bigr).}
```

- **Solutions**: fields $`\Psi`$ at which $`S`$ is stationary under variations vanishing on $`\partial\Omega`$,

```math
\frac{d}{ds}S[\Psi+s\eta]\Big|_{s=0}=0,
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
\boxed{\partial_\mu\frac{\partial\mathcal L}{\partial(\partial_\mu\Psi_\alpha)}
-\frac{\partial\mathcal L}{\partial\Psi_\alpha}=0.}
```

**Hamiltonian Formulation**

For a regular Legendre transformation,

```math
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
```

<br><br>

<a id="classical-noether"></a>
#### Symmetry Transformations and Noether's Theorem

**Transformations**

- **Transformation**: a one-parameter family $`\phi_\lambda`$ with $`\phi_0=\mathrm{id}`$, acting on spacetime and on the field,

```math
\begin{aligned}
\phi_\lambda:\mathbb R^4&\to\mathbb R^4,\\
x&\mapsto x'=\phi_\lambda(x),
\end{aligned}
\qquad
x'^\mu=:x^\mu+\delta x^\mu,\qquad
\Psi\mapsto\Psi',
```

where the form of $`\Psi'`$ is given in (1.58) and (1.66): for $`\phi_\lambda=(\Lambda,a)`$ a Poincaré transformation, $`\Psi'=U(\Lambda,a)\Psi`$ of (1.40); for an internal transformation, $`x'=x`$ and $`\Psi'=g(\lambda)\Psi`$.

**Symmetry Transformations**

- **Symmetry transformation**: a transformation under which the action of every field is invariant for every region,

```math
\boxed{S'=S\quad\text{for every }\Psi\text{ and every }\Omega,}
```

with $`S'`$ the action of $`\Psi'`$ over $`\phi_\lambda(\Omega)`$, written out in (1.60).

**Conserved Quantities**

- **Conserved quantity**: a functional $`\mathcal Q[\Psi,t]`$ of the field and its derivatives on the time slice $`t`$, such that $`\mathcal Q[\Psi,t]`$ is independent of $`t`$ for every solution $`\Psi`$ that, together with its first derivatives, falls off fast enough at spatial infinity.

**Noether's Theorem**

If $`\phi_\lambda`$ is a symmetry transformation, then

```math
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
```

is a conserved quantity, where $`\delta_0\Psi_\alpha`$ is defined in (1.58), the derivatives with respect to $`\lambda`$ are taken at $`\lambda=0`$, and the fall-off condition makes the integral converge and the surface term in (1.64) vanish.

**Proof**

**(A) Coordinate Transformation**

Let $`x'=\phi_\lambda(x)`$, with $`\lambda`$ infinitesimal. Define two field variations:

```math
\begin{aligned}
\delta_0\Psi_\alpha(x)
&:=\Psi'_\alpha(x')-\Psi_\alpha(x)
=D_{\alpha\beta}(\Lambda)\Psi_\beta(x)-\Psi_\alpha(x),\\
\delta\Psi_\alpha(x)
&:=\Psi'_\alpha(x)-\Psi_\alpha(x)
=[U(\Lambda,a)\Psi]_\alpha(x)-\Psi_\alpha(x).
\end{aligned}
```

Here $`\Psi'`$ is the transformed field. Using the pushforward $`(\phi_\lambda)_*\Psi:=\Psi\circ\phi_\lambda^{-1}`$, we write $`\Psi'_\alpha=D_{\alpha\beta}(\Lambda)\,[(\phi_\lambda)_*\Psi]_\beta`$. Evaluating at $`x'`$ gives $`\Psi'_\alpha(x')=D_{\alpha\beta}(\Lambda)\Psi_\beta(x)`$, which is the last equality in the first line, so the first variation, $`\delta_0\Psi_\alpha`$, describes the transformation of the field itself. For $`\phi_\lambda=(\Lambda,a)`$, $`\Psi'=U(\Lambda,a)\Psi`$ by (1.40), which is the last equality in the second line. If $`\phi_\lambda`$ is not a Poincaré transformation, $`D(\Lambda)`$ is replaced by the identity and $`\delta_0\Psi_\alpha=0`$.

To first order in $`\lambda`$, the two variations are related by

```math
\begin{aligned}
\delta\Psi_\alpha(x)
&=\bigl[\Psi'_\alpha(x')-\Psi_\alpha(x)\bigr]
-\bigl[\Psi'_\alpha(x')-\Psi'_\alpha(x)\bigr]\\
&=\delta_0\Psi_\alpha(x)-\delta x^\mu\partial_\mu\Psi'_\alpha(x)\\
&=\delta_0\Psi_\alpha(x)-\delta x^\mu\partial_\mu\Psi_\alpha(x),
\end{aligned}
```

where the last step uses $`\Psi'_\alpha=\Psi_\alpha+O(\lambda)`$.

Over a spacetime region $`\Omega`$, the actions before and after the transformation are

```math
\begin{aligned}
S&=\int_\Omega d^4x\,
\mathcal L\bigl(\Psi_\alpha(x),\partial_\mu\Psi_\alpha(x)\bigr),\\
S'&=\int_{\phi_\lambda(\Omega)}d^4x'\,
\mathcal L\bigl(\Psi'_\alpha(x'),\partial'_\mu\Psi'_\alpha(x')\bigr),
\end{aligned}
```

where $`\partial'_\mu:=\partial/\partial x'^\mu`$. The same function $`\mathcal L`$ is used in $`S'`$: the transformation acts on the field configuration and on the region $`\Omega`$, not on the Lagrangian. No property of $`\mathcal L`$ is assumed here.

Change the integration variable in $`S'`$ from $`x'`$ back to $`x`$, so that $`\phi_\lambda(\Omega)`$ becomes $`\Omega`$. To first order in $`\lambda`$,

```math
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
```

where the third line is (1.58). Hence

```math
S'=\int_\Omega d^4x\,
\bigl(1+\partial_\mu\delta x^\mu\bigr)\,
\mathcal L\bigl(
\Psi_\alpha+\delta_0\Psi_\alpha,\ 
\partial_\mu\Psi_\alpha
+\partial_\mu\delta_0\Psi_\alpha
-(\partial_\mu\delta x^\nu)\partial_\nu\Psi_\alpha
\bigr).
```

Expanding (1.62) to first order in $`\lambda`$ gives the off-shell identity

```math
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
```

The second equality substitutes $`\delta_0\Psi_\alpha=\delta\Psi_\alpha+\delta x^\nu\partial_\nu\Psi_\alpha`$ from (1.59) and uses the product rule together with $`\partial_\nu\mathcal L=\frac{\partial\mathcal L}{\partial\Psi_\alpha}\partial_\nu\Psi_\alpha+\frac{\partial\mathcal L}{\partial(\partial_\mu\Psi_\alpha)}\partial_\nu\partial_\mu\Psi_\alpha`$; the latter holds because $`\mathcal L`$ has no explicit $`x`$-dependence.

By hypothesis, the action is invariant: $`S'=S`$. Take $`\Omega=[t_1,t_2]\times V`$ and let $`\Psi_\alpha`$ satisfy the Euler–Lagrange equations, so that the Euler–Lagrange term in (1.63) vanishes. Gauss's theorem then gives

```math
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
```

By the fall-off condition, the surface term vanishes as $`V\to\mathbb R^3`$. Since $`t_1`$ and $`t_2`$ are arbitrary,

```math
\int d^3x\,\biggl(
\mathcal L\,\delta x^0
+\frac{\partial\mathcal L}{\partial\dot\Psi_\alpha}\delta\Psi_\alpha
\biggr)=\text{const}.
```

Substituting $`\delta\Psi_\alpha=\delta_0\Psi_\alpha-\delta x^\nu\partial_\nu\Psi_\alpha`$ from (1.59), differentiating with respect to $`\lambda`$, and reversing the overall sign gives (1.57) for coordinate transformations.

**(B) Internal Transformation**

Now $`\phi_\lambda`$ acts trivially on spacetime, and on the field by a constant matrix $`g(\lambda)`$ with $`g(0)=I_n`$:

```math
x'^\mu=x^\mu,\qquad
\Psi'_\alpha(x)=g_{\alpha\beta}(\lambda)\,\Psi_\beta(x).
```

Hence $`\delta x^\mu=0`$, and the two variations in (1.58) coincide: $`\delta\Psi_\alpha(x)=\delta_0\Psi_\alpha(x)=g_{\alpha\beta}(\lambda)\Psi_\beta(x)-\Psi_\alpha(x)`$. Repeating (1.60)–(1.65) with $`\delta x^\mu=0`$: in (1.61), $`d^4x'=d^4x`$ and $`\partial'_\mu=\partial_\mu`$; the terms containing $`\delta x^\mu`$ drop out of (1.62)–(1.64); and (1.65) becomes

```math
\int d^3x\,\frac{\partial\mathcal L}{\partial\dot\Psi_\alpha}\,\delta_0\Psi_\alpha=\text{const}.
```

Differentiating with respect to $`\lambda`$ and reversing the overall sign gives (1.57) with $`\delta x^\mu=0`$. $`\square`$

<a id="spacetime-conserved-quantities"></a>
**(1) Spacetime Translations and Energy–Momentum**

Take $`\phi_\lambda(x)=x+\lambda\epsilon`$ for a fixed $`\epsilon\in\mathbb R^4`$, so that $`\delta x^\mu=\lambda\epsilon^\mu`$, $`\Lambda=I_4`$ and $`\delta_0\Psi_\alpha=0`$. By (1.60)–(1.62), $`S'=S`$ holds because $`\mathcal L`$ has no explicit $`x`$-dependence, and (1.57) gives

```math
\mathcal Q=\epsilon^\nu\int d^3x\Bigl(\frac{\partial\mathcal L}{\partial\dot\Psi_\alpha}\partial_\nu\Psi_\alpha-\delta^0{}_\nu\mathcal L\Bigr)=\epsilon^\nu P_\nu,
```

with the canonical energy–momentum tensor and four-momentum

```math
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
p_a:=\frac{\partial L}{\partial\dot q_a}(q,\dot q),\qquad a=1,\ldots,n.
```

- **Hessian**: the symmetric matrix

```math
W_{ab}:=\frac{\partial^2L}{\partial\dot q_a\,\partial\dot q_b}(q,\dot q),\qquad a,b=1,\ldots,n.
```

- **Regular and singular Lagrangians**: $`L`$ is regular if $`\det W\neq0`$ on $`\mathrm{Conf}\times\mathbb R^n`$, and singular otherwise. For a singular $`L`$ we assume that $`\mathop{\rm rank}\nolimits\,W=r<n`$ is constant.

If $`L`$ is regular, (1.70) can be solved for the velocities, $`\dot q=\dot q(q,p)`$, and

```math
H(q,p):=\sum_{a=1}^np_a\,\dot q_a(q,p)-L\bigl(q,\dot q(q,p)\bigr)
```

is the Hamiltonian (1.24) of [Section 1.2](#hamiltonian-formalism). In the rest of this section $`L`$ is singular.

**Primary Constraints**

Since $`W`$ is symmetric, its rank equals the order of its largest invertible principal submatrix, so after reordering the coordinates

```math
\det\bigl(W_{ab}\bigr)_{a,b=1}^{r}\neq0.
```

Indices $`\mu,\nu`$ run over the remaining values $`r+1,\ldots,n`$. By the implicit function theorem, the first $`r`$ equations of (1.70) can be solved locally for $`\dot q_1,\ldots,\dot q_r`$:

```math
\dot q_a=\varphi_a(q,p_b,\dot q_\mu),\qquad a=1,\ldots,r,
```

where $`p_b`$ and $`\dot q_\mu`$ stand for $`(p_1,\ldots,p_r)`$ and $`(\dot q_{r+1},\ldots,\dot q_n)`$. Substituting (1.74) into the remaining equations of (1.70) gives

```math
p_\mu=\frac{\partial L}{\partial\dot q_\mu}\bigl(q,\varphi(q,p_b,\dot q_\nu),\dot q_\nu\bigr)=:g_\mu(q,p_b),
```

and $`g_\mu`$ does not depend on $`\dot q_\nu`$: differentiating the identity $`p_b=\frac{\partial L}{\partial\dot q_b}(q,\varphi,\dot q_\nu)`$ with respect to $`\dot q_\nu`$ gives $`\sum_{a=1}^rW_{ba}\frac{\partial\varphi_a}{\partial\dot q_\nu}=-W_{b\nu}`$, hence

```math
\frac{\partial}{\partial\dot q_\nu}\frac{\partial L}{\partial\dot q_\mu}\bigl(q,\varphi,\dot q\bigr)
=W_{\mu\nu}+\sum_{a=1}^rW_{\mu a}\frac{\partial\varphi_a}{\partial\dot q_\nu}
=W_{\mu\nu}-\sum_{a,b=1}^rW_{\mu a}\bigl(W^{-1}\bigr)_{ab}W_{b\nu}=0,
```

with $`(W^{-1})_{ab}`$ the inverse of the block (1.73). The last expression is the Schur complement of that block in $`W`$, which vanishes since $`\mathop{\rm rank}\nolimits\,W=r`$.

- **Primary constraints**:

```math
\boxed{\chi_\mu(q,p):=p_\mu-g_\mu(q,p_b)=0,\qquad\mu=r+1,\ldots,n.}
```

The $`n`$ equations (1.70) are equivalent to (1.74) together with (1.77). The constraints (1.77) involve only $`(q,p)`$ and define the constraint surface in phase space, the image of the map $`(q,\dot q)\mapsto(q,p(q,\dot q))`$.

- **Weak equality**: $`F\approx G`$ means that the phase-space functions $`F`$ and $`G`$ agree on the constraint surface.

**Canonical Hamiltonian**

Define

```math
H_c:=\sum_{a=1}^np_a\dot q_a-L(q,\dot q),
```

with (1.74) substituted for $`\dot q_1,\ldots,\dot q_r`$, so that $`H_c`$ is a function of $`(q,p,\dot q_\mu)`$. By (1.74), (1.75) and (1.77),

```math
\frac{\partial H_c}{\partial\dot q_\nu}
=\sum_{a=1}^r\Bigl(p_a-\frac{\partial L}{\partial\dot q_a}\Bigr)\frac{\partial\varphi_a}{\partial\dot q_\nu}
+p_\nu-\frac{\partial L}{\partial\dot q_\nu}
=\chi_\nu(q,p),
```

which is independent of $`\dot q_\mu`$ and vanishes on the constraint surface. Hence $`H_c`$ is independent of $`\dot q_\mu`$ on the constraint surface, where by (1.77) it is a function of $`(q,p_1,\ldots,p_r)`$ alone.

**Total Hamiltonian and Consistency**

Let $`H_c`$ be the canonical Hamiltonian and $`u^A`$ the Lagrange multipliers enforcing the primary constraints.

```math
\boxed{
\begin{aligned}
H_T&=H_c+\sum_A u^A(t)\chi_A^{(1)},\\
\dot\chi_A&=\frac{\partial\chi_A}{\partial t}
+\{\chi_A,H_T\}_{\mathrm{PB}}\approx0.
\end{aligned}}
```

Consistency may yield secondary and higher constraints, fix multipliers, or hold identically. Iterate until closure.

**First-Class and Second-Class Constraints**

```math
\{F,G\}_{\mathrm{PB}}
:=\sum_{a=1}^n\left(
\frac{\partial F}{\partial q_a}\frac{\partial G}{\partial p_a}
-\frac{\partial F}{\partial p_a}\frac{\partial G}{\partial q_a}
\right),
\qquad
\{q_a,p_b\}_{\mathrm{PB}}=\delta_{ab}.
```

A constraint is first class if its Poisson bracket with every constraint vanishes weakly. After separating all first-class combinations, the remaining second-class constraints $`\chi_a^{\mathrm{sc}}`$ have an invertible bracket matrix:

```math
\{\chi^{\mathrm{fc}},\chi_A\}_{\mathrm{PB}}\approx0
\quad\text{for all }A,
\qquad
C_{ab}:=\{\chi_a^{\mathrm{sc}},\chi_b^{\mathrm{sc}}\}_{\mathrm{PB}},
\qquad
\det C\ne0.
```

**Dirac Bracket**

```math
\boxed{
\begin{aligned}
\{F,G\}_{\mathrm D}
&:=\{F,G\}_{\mathrm{PB}}
-\sum_{a,b}\{F,\chi_a^{\mathrm{sc}}\}_{\mathrm{PB}}
(C^{-1})_{ab}\{\chi_b^{\mathrm{sc}},G\}_{\mathrm{PB}},\\
\{F,\chi_a^{\mathrm{sc}}\}_{\mathrm D}&=0.
\end{aligned}}
```

Second-class constraints may then be imposed strongly. For fields, use functional derivatives, spatial integrals, and inverse integral kernels.

**Physical Degrees of Freedom**

For a regular system with independent constraints and gauge orbits of the expected dimension,

```math
\boxed{
N_{\mathrm{physical}}
=n-N_{\mathrm{first}}-\frac12N_{\mathrm{second}}.
}
```

For fields, this counts local configuration degrees of freedom per spatial point, subject to boundary and zero-mode qualifications.


<br><br>
<a id="scalar-field"></a>
### 1.6 The Scalar Field

<a id="scalar-lagrangian"></a>
#### Lagrangian

**Real Scalar Field**

```math
\boxed{
\mathcal L=\frac12\partial_\mu\phi\,\partial^\mu\phi-V(\phi),
\qquad
\partial_\mu\partial^\mu\phi+V'(\phi)=0.
}
\qquad
V(\phi)=\frac12m^2\phi^2
\ \Longrightarrow\
(\partial_\mu\partial^\mu+m^2)\phi=0.
```

```math
\pi=\dot\phi,
\qquad
\boxed{
\mathcal H=\frac12\pi^2+\frac12|\boldsymbol\nabla\phi|^2+V(\phi),
\qquad
H=\int d^3x\,\mathcal H.
}
```

**Complex Scalar Field**

Treat $`\phi`$ and $`\phi^*`$ as independent variables:

```math
\boxed{
\begin{aligned}
\mathcal L&=\partial_\mu\phi^*\partial^\mu\phi-m^2\phi^*\phi,\\
(\partial_\mu\partial^\mu+m^2)\phi&=0,\qquad
(\partial_\mu\partial^\mu+m^2)\phi^*=0,\\
\pi_\phi&=\dot\phi^*,\qquad \pi_{\phi^*}=\dot\phi,\\
\mathcal H&=\pi_\phi\pi_{\phi^*}
+|\boldsymbol\nabla\phi|^2+m^2|\phi|^2.
\end{aligned}}
```

**Conserved Quantities: Spacetime Symmetries**

Translations give the canonical energy–momentum tensor in (1.69):

```math
\boxed{\begin{aligned}
T^\mu{}_\nu&=\partial^\mu\phi\,\partial_\nu\phi-\delta^\mu{}_\nu\mathcal L
&&\text{(real field)},\\
T^\mu{}_\nu&=\partial^\mu\phi^*\,\partial_\nu\phi
+\partial^\mu\phi\,\partial_\nu\phi^*-\delta^\mu{}_\nu\mathcal L
&&\text{(complex field)},\\
\partial_\mu T^\mu{}_\nu&=0,\qquad
P_\nu=\int d^3x\,T^0{}_\nu,\qquad \frac{dP_\nu}{dt}=0.
\end{aligned}}
```

For either field, $`T^{\mu\nu}:=T^\mu{}_\rho\eta^{\rho\nu}`$ is symmetric. Lorentz symmetry gives the rotation and boost charges

```math
\boxed{
J^{\mu\nu}=\int d^3x\,
\bigl(x^\mu T^{0\nu}-x^\nu T^{0\mu}\bigr),
\qquad
\frac{dJ^{\mu\nu}}{dt}=0.
}
```

Here $`P_0`$ is the energy, $`P^i`$ are the spatial momenta, $`J^{ij}`$ generate rotations, and $`J^{0i}`$ generate boosts. These conservation laws hold on shell, with convergent integrals and vanishing boundary fluxes.

**Conserved Quantities: Internal and Gauge Symmetries**

The real scalar field has no $`U(1)`$ phase symmetry of the complex-field type. The complex Lagrangian (1.87) has a global $`U(1)`$ symmetry; it is not invariant under an arbitrary local phase $`\lambda(x)`$ without a gauge field. For constant $`\lambda`$, the conserved current and charge are

```math
\phi'=e^{i\lambda}\phi,
\qquad
\boxed{
j^\mu=i\bigl(\phi^*\partial^\mu\phi-\phi\,\partial^\mu\phi^*\bigr),
\qquad
\partial_\mu j^\mu=0,
\qquad
Q=\int d^3x\,j^0.
}
```


<br><br>

<a id="scalar-field-solutions"></a>
#### Solutions of the Klein–Gordon Equation

For the real field take $`V(\phi)=\tfrac12m^2\phi^2`$; the complex field in (1.87) is already free. Define $`\Box:=\partial_\mu\partial^\mu`$. A plane wave obeys

```math
(\Box+m^2)e^{\mp ip\cdot x}=(m^2-p^2)e^{\mp ip\cdot x}=0,
\qquad
p^2=m^2,\qquad
p^0=E_{\mathbf p}:=\sqrt{\mathbf p^2+m^2}>0.
```

Using the Lorentz-invariant measure written explicitly below, a real wave packet has the expansion

```math
\boxed{
\phi(x)=\int\frac{d^3p}{(2\pi)^3\,2E_{\mathbf p}}
\left[a(\mathbf p)e^{-ip\cdot x}+a^*(\mathbf p)e^{+ip\cdot x}\right].
}
```

For a complex field the two frequency amplitudes are independent:

```math
\boxed{\begin{aligned}
\phi(x)&=\int\frac{d^3p}{(2\pi)^3\,2E_{\mathbf p}}
\left[a(\mathbf p)e^{-ip\cdot x}+b^*(\mathbf p)e^{+ip\cdot x}\right],\\
\phi^*(x)&=\int\frac{d^3p}{(2\pi)^3\,2E_{\mathbf p}}
\left[a^*(\mathbf p)e^{+ip\cdot x}+b(\mathbf p)e^{-ip\cdot x}\right].
\end{aligned}}
```

The coefficients are classical complex amplitudes. The real-field condition is $`b=a`$. These free-field expansions do not apply to a general nonlinear potential $`V(\phi)`$.

<br><br>

