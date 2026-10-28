> English, part 2/4 · [Complete file](QFT.md) · [1](QFT-en-part-01.md) · [2](QFT-en-part-02.md) · [3](QFT-en-part-03.md) · [4](QFT-en-part-04.md)

<a id="dirac-field"></a>
### 1.7 The Dirac Field $`\psi`$

<a id="dirac-lagrangian"></a>
#### Lagrangian

The Lagrangian of the Dirac Field has the following form:

```math
\boxed{
\mathcal L=\bar\psi\bigl(i\gamma^\mu\partial_\mu-m\bigr)\psi,
}
```

where $`\psi:\mathbb R^4\to\mathbb C^4`$ is the Dirac field, $`\bar\psi:=\psi^\dagger\gamma^0`$ is its Dirac adjoint, the $`\gamma^\mu`$ are given by (0.10), and $`m`$ is the mass. 

Treating $`\psi`$ and $`\bar\psi`$ as independent, the Euler–Lagrange equations give the Dirac equation and its adjoint:

```math
\boxed{\begin{aligned}
\bigl(i\gamma^\mu\partial_\mu-m\bigr)\psi&=0,\\
i(\partial_\mu\bar\psi)\gamma^\mu+m\bar\psi&=0.
\end{aligned}}
```

**Hamiltonian**

Treating $`\psi`$ and $`\bar\psi`$ as independent, their conjugate momenta are

```math
\boxed{\begin{aligned}
\pi_\psi&:=\frac{\partial\mathcal L}{\partial\dot\psi}
=i\bar\psi\gamma^0=i\psi^\dagger,\\
\pi_{\bar\psi}&:=\frac{\partial\mathcal L}{\partial\dot{\bar\psi}}=0.
\end{aligned}}
```

**Conserved Quantities: Spacetime Symmetries**

Translations give the canonical energy–momentum tensor and four-momentum

```math
\boxed{\begin{aligned}
T^\mu{}_\nu&=i\bar\psi\gamma^\mu\partial_\nu\psi-\delta^\mu{}_\nu\mathcal L,
&\partial_\mu T^\mu{}_\nu&=0,\\
P_\nu&=\int d^3x\,T^0{}_\nu,
&\frac{dP_\nu}{dt}&=0.
\end{aligned}}
```

With $`T^{\mu\nu}:=T^\mu{}_\rho\eta^{\rho\nu}`$, Lorentz symmetry gives

```math
\boxed{\begin{aligned}
J^{\mu\nu}&=\int d^3x\left[
x^\mu T^{0\nu}-x^\nu T^{0\mu}
+\frac{i}{4}\psi^\dagger[\gamma^\mu,\gamma^\nu]\psi
\right],\\
\frac{dJ^{\mu\nu}}{dt}&=0.
\end{aligned}}
```

The last term is the spin contribution. $`J^{ij}`$ and $`J^{0i}`$ are the rotation and boost charges. Conservation holds on shell, with convergent integrals and vanishing boundary fluxes.

**Conserved Quantities: Internal and Gauge Symmetries**

The free Dirac Lagrangian has a global $`U(1)`$ symmetry. For constant $`\lambda`$,

```math
\boxed{\begin{aligned}
\psi'&=e^{i\lambda}\psi,\qquad
\bar\psi'=e^{-i\lambda}\bar\psi,\\
j^\mu&=\bar\psi\gamma^\mu\psi,\qquad \partial_\mu j^\mu=0,\\
Q&=\int d^3x\,j^0=\int d^3x\,\psi^\dagger\psi,
\qquad \frac{dQ}{dt}=0.
\end{aligned}}
```

For a local phase $`\lambda(x)`$, $`\mathcal L'=\mathcal L-j^\mu\partial_\mu\lambda`$; local gauge invariance requires coupling to a gauge field.

<br><br>

<a id="weyl-spinor-solutions"></a>
#### Solutions of the Dirac Equation in the Weyl Representation

**Spinor Representation of the Lorentz Group**

For the Dirac field, $`D(\Lambda)`$ in (1.40) is

```math
\Lambda_{\frac12}=\exp\Bigl(-\frac i2\omega_{\mu\nu}S^{\mu\nu}\Bigr),
\qquad
S^{\mu\nu}:=\frac i4[\gamma^\mu,\gamma^\nu],
```

with the same $`\omega_{\mu\nu}`$ as in (0.35). In the Weyl representation every $`S^{\mu\nu}`$ is block diagonal:

```math
S^{0i}=-\frac i2\begin{pmatrix}\sigma^i&0\\0&-\sigma^i\end{pmatrix},
\qquad
S^{ij}=\frac12\epsilon^{ijk}\begin{pmatrix}\sigma^k&0\\0&\sigma^k\end{pmatrix}.
```

The noncompact Lorentz group $`SO(1,3)^+`$ has no nontrivial finite-dimensional unitary representations; in the Weyl representation, $`(S^{0i})^\dagger=-S^{0i}`$, so the finite boost matrices for nonzero rapidity are not unitary.

Hence $`\Lambda_{\frac12}`$ is block diagonal: writing $`\psi=\begin{pmatrix}\psi_L\\\psi_R\end{pmatrix}`$, the left-handed and right-handed Weyl spinors $`\psi_L,\psi_R`$ transform independently. For an infinitesimal transformation, with $`\omega_{ij}=\epsilon_{ijk}\theta^k`$ and $`\omega_{0i}=b^i`$ as in (0.34),

```math
\begin{aligned}
\Lambda_{\frac12}
&\simeq I_4-\frac i2\omega_{\mu\nu}S^{\mu\nu}\\
&=I_4-\frac i2\begin{pmatrix}\boldsymbol\theta\cdot\boldsymbol\sigma&0\\0&\boldsymbol\theta\cdot\boldsymbol\sigma\end{pmatrix}
-i\Bigl(-\frac i2\Bigr)\begin{pmatrix}\mathbf b\cdot\boldsymbol\sigma&0\\0&-\mathbf b\cdot\boldsymbol\sigma\end{pmatrix}\\
&=\begin{pmatrix}I_2-i\boldsymbol\theta\cdot\frac{\boldsymbol\sigma}2-\mathbf b\cdot\frac{\boldsymbol\sigma}2&0\\0&I_2-i\boldsymbol\theta\cdot\frac{\boldsymbol\sigma}2+\mathbf b\cdot\frac{\boldsymbol\sigma}2\end{pmatrix},
\end{aligned}
```

so that

```math
\begin{aligned}
\psi_L&\xrightarrow{\ \Lambda\ }\Bigl(I_2-i\boldsymbol\theta\cdot\frac{\boldsymbol\sigma}2-\mathbf b\cdot\frac{\boldsymbol\sigma}2\Bigr)\psi_L,\\
\psi_R&\xrightarrow{\ \Lambda\ }\Bigl(I_2-i\boldsymbol\theta\cdot\frac{\boldsymbol\sigma}2+\mathbf b\cdot\frac{\boldsymbol\sigma}2\Bigr)\psi_R.
\end{aligned}
```

In terms of $`\psi_L,\psi_R`$, the Dirac equation (1.95) reads

```math
\begin{pmatrix}-m&i\sigma^\mu\partial_\mu\\i\bar\sigma^\mu\partial_\mu&-m\end{pmatrix}
\begin{pmatrix}\psi_L\\\psi_R\end{pmatrix}=0
\quad\Longleftrightarrow\quad
\begin{cases}
i\sigma^\mu\partial_\mu\psi_R-m\psi_L=0,\\
i\bar\sigma^\mu\partial_\mu\psi_L-m\psi_R=0.
\end{cases}
```

For $`m=0`$ it reduces to the Weyl equations

```math
\begin{cases}
i\bigl(\partial_t-\boldsymbol\sigma\cdot\nabla\bigr)\psi_L=0,\\
i\bigl(\partial_t+\boldsymbol\sigma\cdot\nabla\bigr)\psi_R=0.
\end{cases}
```

**Plane-Wave Solutions of the Dirac Equation**

Apply $`-i\gamma^\mu\partial_\mu-m`$ to the left-hand side of (1.95):

```math
\begin{aligned}
\bigl(-i\gamma^\mu\partial_\mu-m\bigr)\bigl(i\gamma^\nu\partial_\nu-m\bigr)\psi
&=\bigl(\gamma^\mu\gamma^\nu\partial_\mu\partial_\nu+m^2\bigr)\psi\\
&=\bigl(\eta^{\mu\nu}\partial_\mu\partial_\nu+m^2\bigr)\psi\\
&=\bigl(\Box+m^2\bigr)\psi,
\end{aligned}
```

where $`\Box:=\eta^{\mu\nu}\partial_\mu\partial_\nu=\partial_t^2-\nabla^2`$. Since the left-hand side of (1.106) vanishes by (1.95), every component of $`\psi`$ satisfies the Klein–Gordon equation

```math
\bigl(\Box+m^2\bigr)\psi=0.
```

A plane wave $`e^{-ip\cdot x}`$ satisfies (1.107) only if $`p^2=m^2`$. In the Weyl representation (0.10), the plane-wave solutions of (1.95) therefore take the form

```math
\psi(x)=\begin{pmatrix}u_L\\u_R\end{pmatrix}e^{-ip\cdot x},
\qquad
p^0=\pm E_{\mathbf p},\quad
E_{\mathbf p}:=\sqrt{\mathbf p^2+m^2},
```

where $`u_L,u_R\in\mathbb C^2`$ are constant. Substituting (1.108) into (1.95) gives

```math
\bigl(\not p-m\bigr)\begin{pmatrix}u_L\\u_R\end{pmatrix}=0,
\qquad
\not p:=\gamma\cdot p=p^\mu\gamma_\mu.
```

**(1) Rest Frame**

Take $`m>0`$ and work in the rest frame, $`\mathbf p=\mathbf 0`$; there we denote the constants in (1.108) by $`u_L(\mathbf 0)`$ and $`u_R(\mathbf 0)`$. First consider $`p^0>0`$. Then $`p^\mu=(m,\mathbf 0)`$, $`e^{-ip\cdot x}=e^{-imt}`$ and $`\not p=m\gamma^0`$, so (1.109) becomes

```math
\begin{aligned}
\bigl(m\gamma^0-m\bigr)\begin{pmatrix}u_L(\mathbf 0)\\u_R(\mathbf 0)\end{pmatrix}
&=\begin{pmatrix}-mI_2&mI_2\\mI_2&-mI_2\end{pmatrix}
\begin{pmatrix}u_L(\mathbf 0)\\u_R(\mathbf 0)\end{pmatrix}=0\\[6pt]
\Longrightarrow\quad u_L(\mathbf 0)&=u_R(\mathbf 0).
\end{aligned}
```

Writing $`u:=\begin{pmatrix}u_L\\u_R\end{pmatrix}`$, there are two independent solutions

```math
u^s(\mathbf 0)=\sqrt m\begin{pmatrix}\xi^s\\\xi^s\end{pmatrix},\qquad s=1,2,
```

where $`\{\xi^s\}`$ is a basis of $`\mathbb C^2`$ with $`\xi^{r\dagger}\xi^s=\delta^{rs}`$.

**(2) Boost**

Boost along $`z`$ with rapidity $`\eta`$, i.e. $`\omega_{03}=\eta`$ in (1.100), so that $`\mathbf p=(0,0,p^3)`$ and $`\tanh\eta=v=p^3/E_{\mathbf p}`$. Then

```math
\begin{aligned}
\Lambda_{\frac12}=e^{-i\eta S^{03}}
&=\exp\Bigl[-i\eta\Bigl(-\frac i2\Bigr)\begin{pmatrix}\sigma^3&0\\0&-\sigma^3\end{pmatrix}\Bigr]
=\begin{pmatrix}e^{-\frac12\eta\sigma^3}&0\\0&e^{\frac12\eta\sigma^3}\end{pmatrix}\\
&=\mathop{\rm diag}\nolimits \bigl(e^{-\eta/2},\,e^{\eta/2},\,e^{\eta/2},\,e^{-\eta/2}\bigr),
\end{aligned}
```

```math
\tanh\eta=v
\ \Longrightarrow\
e^{\pm\eta}=\sqrt{\frac{1\pm v}{1\mp v}}=\frac{E_{\mathbf p}\pm p^3}{m},
\qquad
e^{\pm\eta/2}=\sqrt{\frac{E_{\mathbf p}\pm p^3}{m}}.
```

Hence

```math
u^s(p)=\Lambda_{\frac12}u^s(\mathbf 0)
=\mathop{\rm diag}\nolimits \Bigl(\sqrt{E_{\mathbf p}-p^3},\,\sqrt{E_{\mathbf p}+p^3},\,\sqrt{E_{\mathbf p}+p^3},\,\sqrt{E_{\mathbf p}-p^3}\Bigr)
\begin{pmatrix}\xi^s\\\xi^s\end{pmatrix}.
```

With $`\xi^1=\begin{pmatrix}1\\0\end{pmatrix}`$ and $`\xi^2=\begin{pmatrix}0\\1\end{pmatrix}`$,

```math
u^1(p)=\begin{pmatrix}\sqrt{E_{\mathbf p}-p^3}\\0\\\sqrt{E_{\mathbf p}+p^3}\\0\end{pmatrix}
\xrightarrow{\ \eta\to\infty\ }\sqrt{2E_{\mathbf p}}\begin{pmatrix}0\\0\\1\\0\end{pmatrix},
\qquad
u^2(p)=\begin{pmatrix}0\\\sqrt{E_{\mathbf p}+p^3}\\0\\\sqrt{E_{\mathbf p}-p^3}\end{pmatrix}
\xrightarrow{\ \eta\to\infty\ }\sqrt{2E_{\mathbf p}}\begin{pmatrix}0\\1\\0\\0\end{pmatrix}.
```

**(3) Arbitrary Momentum**

Since $`\mathop{\rm diag}\nolimits \bigl(\sqrt{E_{\mathbf p}-p^3},\sqrt{E_{\mathbf p}+p^3}\bigr)=\sqrt{E_{\mathbf p}-p^3\sigma^3}`$ and $`\mathop{\rm diag}\nolimits \bigl(\sqrt{E_{\mathbf p}+p^3},\sqrt{E_{\mathbf p}-p^3}\bigr)=\sqrt{E_{\mathbf p}+p^3\sigma^3}`$, for arbitrary $`\mathbf p`$

```math
\sqrt m\,\Lambda_{\frac12}=\begin{pmatrix}\sqrt{p\cdot\sigma}&0\\0&\sqrt{p\cdot\bar\sigma}\end{pmatrix},
\qquad
p\cdot\sigma:=p_\mu\sigma^\mu=p^0I_2-\mathbf p\cdot\boldsymbol\sigma,
\quad
p\cdot\bar\sigma:=p_\mu\bar\sigma^\mu=p^0I_2+\mathbf p\cdot\boldsymbol\sigma,
```

with positive square roots. The positive-energy solutions are

```math
\boxed{
\psi=u^s(p)\,e^{-ip\cdot x},\qquad
u^s(p)=\begin{pmatrix}\sqrt{p\cdot\sigma}\,\xi^s\\\sqrt{p\cdot\bar\sigma}\,\xi^s\end{pmatrix},\qquad
p^0=E_{\mathbf p}.
}
```

**Verification**

```math
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
```

**Negative-Energy Solutions**

For $`p^0=-E_{\mathbf p}`$, (1.109) becomes

```math
\bigl(-\gamma^0E_{\mathbf p}-\boldsymbol\gamma\cdot\mathbf p-m\bigr)u(p)=0
\quad\Longleftrightarrow\quad
\bigl(\gamma^0E_{\mathbf p}-\boldsymbol\gamma\cdot(-\mathbf p)+m\bigr)u(p)=0,
```

which is the positive-energy equation $`\bigl(\gamma^0E_{\mathbf p}-\boldsymbol\gamma\cdot\mathbf p-m\bigr)u=0`$ with $`\mathbf p\to-\mathbf p`$ and $`m\to-m`$. Hence

```math
u^s(p)=\begin{pmatrix}\sqrt{E_{\mathbf p}I_2+\mathbf p\cdot\boldsymbol\sigma}\,\xi^s\\-\sqrt{E_{\mathbf p}I_2-\mathbf p\cdot\boldsymbol\sigma}\,\xi^s\end{pmatrix}
=\begin{pmatrix}\sqrt{-p\cdot\sigma}\,\xi^s\\-\sqrt{-p\cdot\bar\sigma}\,\xi^s\end{pmatrix},
\qquad p^0=-E_{\mathbf p}.
```

**Antiparticle Solutions**

Define

```math
u^c(p):=\begin{pmatrix}i\sigma^2&0\\0&-i\sigma^2\end{pmatrix}\gamma^0\,u(p),
\qquad
i\sigma^2=\begin{pmatrix}0&1\\-1&0\end{pmatrix}.
```

For $`\mathbf p=(0,0,p^3)`$,

```math
i\sigma^2\sqrt{p\cdot\bar\sigma}
=\begin{pmatrix}0&1\\-1&0\end{pmatrix}\begin{pmatrix}\sqrt{E_{\mathbf p}+p^3}&0\\0&\sqrt{E_{\mathbf p}-p^3}\end{pmatrix}
=\begin{pmatrix}0&\sqrt{E_{\mathbf p}-p^3}\\-\sqrt{E_{\mathbf p}+p^3}&0\end{pmatrix}
=\sqrt{p\cdot\sigma}\;i\sigma^2,
```

and likewise $`i\sigma^2\sqrt{p\cdot\sigma}=\sqrt{p\cdot\bar\sigma}\;i\sigma^2`$. Applying (1.121) to (1.117) and writing $`\eta^s:=i\sigma^2\xi^s`$,

```math
u^c(p)=\begin{pmatrix}i\sigma^2\sqrt{p\cdot\bar\sigma}\,\xi^s\\-i\sigma^2\sqrt{p\cdot\sigma}\,\xi^s\end{pmatrix}
=\begin{pmatrix}\sqrt{p\cdot\sigma}\,\eta^s\\-\sqrt{p\cdot\bar\sigma}\,\eta^s\end{pmatrix},
\qquad p^0=E_{\mathbf p},
```

which is (1.120) at $`-p`$ with $`\xi^s\to\eta^s`$. For arbitrary $`\mathbf p`$, the antiparticle solutions are

```math
\boxed{
\psi=v^s(p)\,e^{+ip\cdot x},\qquad
v^s(p):=\begin{pmatrix}\sqrt{p\cdot\sigma}\,\eta^s\\-\sqrt{p\cdot\bar\sigma}\,\eta^s\end{pmatrix},\qquad
\bigl(\not p+m\bigr)v^s(p)=0,\qquad
p^0=E_{\mathbf p}.
}
```

**Properties of the Solutions**

**(1) Orthonormality**

From (1.117), $`u^\dagger u=2E_{\mathbf p}\,\xi^\dagger\xi`$ and $`\bar uu=2m\,\xi^\dagger\xi`$. With $`\xi^{r\dagger}\xi^s=\eta^{r\dagger}\eta^s=\delta^{rs}`$,

```math
\boxed{
\begin{aligned}
u^{r\dagger}(p)\,u^s(p)&=2E_{\mathbf p}\,\delta^{rs}, &\qquad \bar u^r(p)\,u^s(p)&=2m\,\delta^{rs},\\
v^{r\dagger}(p)\,v^s(p)&=2E_{\mathbf p}\,\delta^{rs}, &\qquad \bar v^r(p)\,v^s(p)&=-2m\,\delta^{rs},\\
u^{r\dagger}(p)\,v^s(p')&=v^{r\dagger}(p')\,u^s(p)=0, &\qquad p'&:=(p^0,-\mathbf p).
\end{aligned}
}
```

**(2) Completeness (Spin Sums)**

With $`\sum_s\xi^s\xi^{s\dagger}=I_2`$,

```math
\boxed{
\sum_s u^s(p)\,\bar u^s(p)=\not p+m,\qquad
\sum_s v^s(p)\,\bar v^s(p)=\not p-m.
}
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
\gamma^5=\frac{i}{4!}\epsilon_{\mu\nu\rho\sigma}\gamma^\mu\gamma^\nu\gamma^\rho\gamma^\sigma,
\qquad \epsilon_{0123}=+1,
```

which agrees with (0.14). Under $`\psi\to\Lambda_{\frac12}\psi`$, $`\bar\psi\to\bar\psi\Lambda_{\frac12}^{-1}`$,

```math
\begin{aligned}
\bar\psi\psi&\xrightarrow{\ \Lambda\ }\bar\psi\psi,\\
\bar\psi\gamma^\mu\psi&\xrightarrow{\ \Lambda\ }\bar\psi\Lambda_{\frac12}^{-1}\gamma^\mu\Lambda_{\frac12}\psi=\Lambda^\mu{}_\nu\,\bar\psi\gamma^\nu\psi,\\
\bar\psi S^{\mu\nu}\psi&\xrightarrow{\ \Lambda\ }\Lambda^\mu{}_\rho\Lambda^\nu{}_\sigma\,\bar\psi S^{\rho\sigma}\psi,\\
\bar\psi\gamma^5\gamma^\mu\psi&\xrightarrow{\ \Lambda\ }\det[\Lambda]\,\Lambda^\mu{}_\nu\,\bar\psi\gamma^5\gamma^\nu\psi\qquad\text{(pseudovector)},\\
\bar\psi\gamma^5\psi&\xrightarrow{\ \Lambda\ }\det[\Lambda]\,\bar\psi\gamma^5\psi\qquad\text{(pseudoscalar)}.
\end{aligned}
```

**Proof** (for $`\gamma^5`$)

```math
\begin{aligned}
\Lambda_{\frac12}^{-1}\gamma^5\Lambda_{\frac12}
&=\frac{i}{4!}\epsilon_{\mu\nu\rho\sigma}\Lambda^\mu{}_\alpha\Lambda^\nu{}_\beta\Lambda^\rho{}_\kappa\Lambda^\sigma{}_\lambda\,\gamma^\alpha\gamma^\beta\gamma^\kappa\gamma^\lambda\\
&=\frac{i}{4!}\det[\Lambda]\,\epsilon_{\alpha\beta\kappa\lambda}\gamma^\alpha\gamma^\beta\gamma^\kappa\gamma^\lambda
=\det[\Lambda]\,\gamma^5.
\end{aligned}
```

**Chirality**

```math
\gamma^5\begin{pmatrix}\psi_L\\0\end{pmatrix}=-\begin{pmatrix}\psi_L\\0\end{pmatrix},
\qquad
\gamma^5\begin{pmatrix}0\\\psi_R\end{pmatrix}=\begin{pmatrix}0\\\psi_R\end{pmatrix}.
```

The left- and right-handed projection operators are

```math
P_L:=\frac{I_4-\gamma^5}2,\qquad P_R:=\frac{I_4+\gamma^5}2
\quad\Longrightarrow\quad
\begin{cases}
P_L+P_R=I_4,\\
P_LP_R=P_RP_L=0,\\
P_L^n=P_L,\quad P_R^n=P_R.
\end{cases}
```

**Vector and Axial Currents**

```math
j^\mu:=\bar\psi\gamma^\mu\psi,\qquad
j^{\mu5}:=\bar\psi\gamma^\mu\gamma^5\psi.
```

The Euler–Lagrange equation of (1.94) for $`\psi`$ is $`-i\partial_\mu\bar\psi\gamma^\mu-m\bar\psi=0`$. Together with (1.95),

```math
\partial_\mu j^\mu=(\partial_\mu\bar\psi)\gamma^\mu\psi+\bar\psi\gamma^\mu\partial_\mu\psi
=im\bar\psi\psi-im\bar\psi\psi=0
\quad\Longrightarrow\quad
\int d^3x\,\bar\psi\gamma^0\psi=\text{const}.
```

**Helicity**

```math
h:=\frac{\mathbf p}{|\mathbf p|}\cdot\mathbf S,\qquad
\mathbf S:=\frac12\begin{pmatrix}\boldsymbol\sigma&0\\0&\boldsymbol\sigma\end{pmatrix}.
```

For $`\mathbf p=(0,0,p^3)`$ with $`p^3>0`$, the spinors (1.115) satisfy $`h\,u^1=\frac12u^1`$ and $`h\,u^2=-\frac12u^2`$.


<br><br>

<a id="proca-field"></a>
### 1.8 The Proca Field

<a id="proca-lagrangian"></a>
#### Lagrangian

For a real vector field with $`m>0`$,

```math
F_{\mu\nu}:=\partial_\mu A_\nu-\partial_\nu A_\mu,
\qquad
\boxed{
\mathcal L=-\frac14F_{\mu\nu}F^{\mu\nu}
+\frac12m^2A_\mu A^\mu.
}
```

```math
\boxed{
\partial_\mu F^{\mu\nu}+m^2A^\nu=0,
\qquad
\partial_\mu A^\mu=0,
\qquad
(\partial_\mu\partial^\mu+m^2)A^\nu=0.
}
```

Here $`\partial_\mu A^\mu=0`$ follows from the equations of motion.

**Canonical Momenta and Hamiltonian**

Choose $`A_\mu`$ as canonical coordinates. All brackets below are at equal time:

```math
\Pi^\mu:=\frac{\partial\mathcal L}{\partial\dot A_\mu}=F^{\mu0},
\qquad
\Pi^0=0,
\qquad
\Pi^i=\dot A_i-\partial_iA_0,
\qquad
\{A_\mu(\mathbf x),\Pi^\nu(\mathbf y)\}_{\mathrm{PB}}
=\delta_\mu{}^\nu\delta^{(3)}(\mathbf x-\mathbf y).
```

With vanishing spatial surface terms,

```math
\boxed{
\begin{aligned}
H_c&=\int d^3x\left[
\frac12\sum_i(\Pi^i)^2+\frac14\sum_{i,j}(F_{ij})^2
+\frac{m^2}{2}\sum_i(A_i)^2
-\frac{m^2}{2}A_0^2-A_0\partial_i\Pi^i\right],\\
H_T&=H_c+\int d^3x\,u\,\Pi^0.
\end{aligned}}
```

**Second-Class Constraints**

```math
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
```

Preserving $`\chi_2`$ fixes $`u=\sum_i\partial_iA_i`$; there are no further constraints.

Here $`\chi_1`$ is primary and $`\chi_2`$ is secondary; both are second class.

**Reduced Hamiltonian**

Eliminating $`\Pi^0`$ and $`A_0`$ gives

```math
A_0=-\frac{\partial_i\Pi^i}{m^2},
\qquad
\boxed{
H_{\mathrm{red}}=\int d^3x\left[
\frac12\sum_i(\Pi^i)^2+\frac14\sum_{i,j}(F_{ij})^2
+\frac{m^2}{2}\sum_i(A_i)^2
+\frac{(\partial_i\Pi^i)^2}{2m^2}
\right]\ge0.
}
```

**Conserved Quantities: Spacetime Symmetries**

For the canonical variables $`A_\mu`$, translations give

```math
\boxed{\begin{aligned}
T^\mu{}_\nu&=-F^{\mu\rho}\partial_\nu A_\rho-\delta^\mu{}_\nu\mathcal L,
&\partial_\mu T^\mu{}_\nu&=0,\\
P_\nu&=\int d^3x\,T^0{}_\nu,
&\frac{dP_\nu}{dt}&=0.
\end{aligned}}
```

With $`T^{\mu\nu}:=T^\mu{}_\rho\eta^{\rho\nu}`$, the Lorentz charges include the vector spin contribution:

```math
\boxed{
J^{\mu\nu}=\int d^3x\left[
x^\mu T^{0\nu}-x^\nu T^{0\mu}
+\Pi^\mu A^\nu-\Pi^\nu A^\mu
\right],
\qquad
\frac{dJ^{\mu\nu}}{dt}=0.
}
```

These are conserved on shell, with convergent integrals and vanishing boundary fluxes.

**Conserved Quantities: Internal and Gauge Symmetries**

For $`m>0`$, the mass term breaks the Maxwell gauge symmetry $`A_\mu\mapsto A_\mu+\partial_\mu\lambda(x)`$. The real Proca field has no complex $`U(1)`$ phase symmetry, so this model has no corresponding phase charge. Its constraint $`\partial_i\Pi^i+m^2A_0=0`$ is second class, as in (1.139).

<br><br>

<a id="proca-field-solutions"></a>
#### Solutions of the Proca Equation

For $`A^\mu(x)=\epsilon^\mu(p)e^{-ip\cdot x}`$, the field equation becomes

```math
\begin{aligned}
(m^2-p^2)\epsilon^\mu+p^\mu(p_\nu\epsilon^\nu)&=0,\\
m^2p_\mu\epsilon^\mu&=0.
\end{aligned}
\quad\Longrightarrow\quad
\boxed{p^2=m^2,\qquad p_\mu\epsilon^\mu=0}
```

for a nonzero mode with $`m>0`$.

**Polarizations**

For $`p^2=m^2`$, $`p^0>0`$, there are three polarization vectors, $`r=1,2,3`$:

```math
\boxed{
p_\mu\epsilon_r^\mu(p)=0,
\qquad
\epsilon_{r\mu}^*(p)\epsilon_s^\mu(p)=-\delta_{rs},
\qquad
\sum_{r=1}^3\epsilon_r^\mu(p)\epsilon_r^{\nu*}(p)
=-\eta^{\mu\nu}+\frac{p^\mu p^\nu}{m^2}.
}
```


At rest, one may take $`\epsilon_r^\mu=(0,\mathbf e_r)`$ for an orthonormal spatial basis $`\mathbf e_r`$. For $`\mathbf p\ne0`$, choose $`\mathbf e_1,\mathbf e_2`$ perpendicular to $`\mathbf p`$, with $`\mathbf e_a\cdot\mathbf e_b=\delta_{ab}`$. With $`E_{\mathbf p}=\sqrt{\mathbf p^2+m^2}`$, a basis with two transverse and one longitudinal polarization is

```math
\boxed{
\epsilon_a^\mu(p)=(0,\mathbf e_a)\quad(a=1,2),
\qquad
\epsilon_3^\mu(p)=\left(\frac{|\mathbf p|}{m},
\frac{E_{\mathbf p}}{m}\frac{\mathbf p}{|\mathbf p|}\right).
}
```

The real field is a superposition of these three modes, with $`p^0=E_{\mathbf p}`$:

```math
\boxed{
A^\mu(x)=\sum_{r=1}^3\int\frac{d^3p}{(2\pi)^3\,2E_{\mathbf p}}
\left[
a_r(\mathbf p)\epsilon_r^\mu(p)e^{-ip\cdot x}
+a_r^*(\mathbf p)\epsilon_r^{\mu*}(p)e^{+ip\cdot x}
\right].
}
```

Here $`a_r(\mathbf p)`$ are classical complex amplitudes; the transversality condition is imposed by the field equation, not by a gauge choice.

<br><br>

<a id="vector-field"></a>
### 1.9 The Vector Field

<a id="maxwell-lagrangian"></a>
#### Lagrangian

```math
\boxed{
\mathcal L=-\frac14F_{\mu\nu}F^{\mu\nu},
\qquad
\partial_\mu F^{\mu\nu}=0,
\qquad
A_\mu'=A_\mu+\partial_\mu\lambda(x).
}
```

**Hamiltonian and First-Class Constraints**

```math
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
```

Both constraints are first class:

```math
\{\chi_a(\mathbf x),\chi_b(\mathbf y)\}_{\mathrm{PB}}=0,
\qquad a,b=1,2,
\qquad
\boxed{N_{\mathrm{physical}}=4-2=2.}
```

**Coulomb Gauge and Physical Hamiltonian**

In the absence of sources, with fields decaying at spatial infinity,

```math
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
```

The remaining canonical variables are transverse.

**Conserved Quantities: Spacetime Symmetries**

The canonical energy–momentum tensor and four-momentum are

```math
\boxed{\begin{aligned}
T^\mu{}_\nu&=-F^{\mu\rho}\partial_\nu A_\rho-\delta^\mu{}_\nu\mathcal L,
&\partial_\mu T^\mu{}_\nu&=0,\\
P_\nu&=\int d^3x\,T^0{}_\nu,
&\frac{dP_\nu}{dt}&=0.
\end{aligned}}
```

With $`T^{\mu\nu}:=T^\mu{}_\rho\eta^{\rho\nu}`$, the rotation and boost charges are

```math
\boxed{
J^{\mu\nu}=\int d^3x\left[
x^\mu T^{0\nu}-x^\nu T^{0\mu}
+\Pi^\mu A^\nu-\Pi^\nu A^\mu
\right],
\qquad
\frac{dJ^{\mu\nu}}{dt}=0.
}
```

These charges are conserved on shell when the integrals converge and boundary fluxes vanish. The canonical densities depend on the gauge; the integrated charges are invariant under gauge transformations whose boundary terms vanish.

**Conserved Quantities: Internal and Gauge Symmetries**

The local transformation in (1.147) gives a Noether identity and the Gauss constraint. For smooth source-free fields on all of $`\mathbb R^3`$,

```math
\boxed{\begin{aligned}
\partial_\nu\partial_\mu F^{\mu\nu}&\equiv0,
&\partial_i\Pi^i&=0,\\
Q_{\mathrm{el}}&:=\lim_{R\to\infty}\oint_{|\mathbf x|=R}\Pi^i\,dS_i=0.
\end{aligned}}
```

There is no independent matter $`U(1)`$ number in this free-field model. Nonzero electric flux requires sources, singularities, or different boundary conditions.

<br><br>

<a id="maxwell-field-solutions"></a>
#### Solutions of the Maxwell Equations

**Lorenz Gauge**

```math
\partial_\mu A^\mu=0
\quad\Longrightarrow\quad
\partial_\mu\partial^\mu A^\nu=0,
\qquad
A_\mu\mapsto A_\mu+\partial_\mu\lambda,
\qquad
\partial_\mu\partial^\mu\lambda=0
\quad\text{(residual gauge freedom).}
```


**Plane Waves and Physical Polarizations**

For a plane wave $`A^\mu(x)=\epsilon^\mu(p)e^{-ip\cdot x}`$ in Lorenz gauge,

```math
\boxed{
p^2=0,\qquad p^0=|\mathbf p|>0,\qquad
p_\mu\epsilon^\mu=0,\qquad
\epsilon^\mu\sim\epsilon^\mu+\lambda p^\mu.
}
```

In the last expression, $`\lambda`$ is an arbitrary complex coefficient of a residual plane-wave gauge transformation. The constraint and this equivalence leave two physical polarizations. A Coulomb-gauge basis satisfies

```math
\boxed{\begin{aligned}
\epsilon_r^0(p)&=0,\qquad
\mathbf p\cdot\boldsymbol\epsilon_r(p)=0,\qquad
\boldsymbol\epsilon_r^*(p)\cdot\boldsymbol\epsilon_s(p)=\delta_{rs},
\qquad r,s=1,2,\\
\sum_{r=1}^2\epsilon_r^i(p)\epsilon_r^{j*}(p)
&=\delta^{ij}-\frac{p^ip^j}{|\mathbf p|^2}.
\end{aligned}}
```

For source-free wave packets, the real field in this gauge is, with $`p^0=|\mathbf p|`$,

```math
\boxed{
A^\mu(x)=\sum_{r=1}^2\int\frac{d^3p}{(2\pi)^3\,2|\mathbf p|}
\left[
a_r(\mathbf p)\epsilon_r^\mu(p)e^{-ip\cdot x}
+a_r^*(\mathbf p)\epsilon_r^{\mu*}(p)e^{+ip\cdot x}
\right].
}
```

The $`a_r(\mathbf p)`$ are classical complex amplitudes. Other gauge representatives follow by adding $`\partial^\mu\lambda(x)`$.

<br><br>

<a id="qft-ch2"></a>
## 2. Operator Quantization


The first viewpoint in [Section 1.4](QFT-en-part-01.md#classical-dynamics) naturally leads to Operator quantization: spatial position labels the degrees of freedom, while time remains the evolution parameter. 


<br><br>
<a id="canonical-quantization"></a>
### 2.1 Canonical Quantization

Consider unconstrained  fields $`\phi_a(x)`$ with a Lagrangian density

```math
\mathcal L=\mathcal L(\phi_a,\partial_\mu\phi_a),
\qquad
L(t)=\int d^3x\,\mathcal L.
```

At each fixed time, the field values form an infinite set of generalized coordinates:

```math
i\longleftrightarrow(a,\mathbf x),
\qquad
q_i(t)\longleftrightarrow\phi_a(t,\mathbf x).
```

**Conjugate momentum**

The momentum density conjugate to $`\phi_a(t,\mathbf x)`$ is

```math
\pi_a(t,\mathbf x)
\equiv
\frac{\delta L(t)}{\delta\dot\phi_a(t,\mathbf x)}
=
\frac{\partial\mathcal L}{\partial\dot\phi_a(t,\mathbf x)}.
```

**Poisson brackets and commutation relations**

The classical fields obey the equal-time canonical Poisson brackets

```math
\begin{aligned}
\{\phi_a(t,\mathbf x),\pi_b(t,\mathbf y)\}_{\mathrm{PB}}
&=\delta_{ab}\delta^{(3)}(\mathbf x-\mathbf y),\\
\{\phi_a(t,\mathbf x),\phi_b(t,\mathbf y)\}_{\mathrm{PB}}
&=\{\pi_a(t,\mathbf x),\pi_b(t,\mathbf y)\}_{\mathrm{PB}}=0.
\end{aligned}
```

Canonical quantization promotes the fields and their conjugate momenta to operators and replaces these fundamental Poisson brackets according to

```math
\{\ ,\ \}_{\mathrm{PB}}
\longrightarrow
\frac{1}{i}[\ ,\ ].
```

Thus,

```math
\boxed{
\begin{aligned}
[\hat\phi_a(t,\mathbf x),\hat\pi_b(t,\mathbf y)]
&=i\,\delta_{ab}\delta^{(3)}(\mathbf x-\mathbf y),\\
[\hat\phi_a(t,\mathbf x),\hat\phi_b(t,\mathbf y)]
&=[\hat\pi_a(t,\mathbf x),\hat\pi_b(t,\mathbf y)]=0.
\end{aligned}}
```

Here $`\delta_{ab}\delta^{(3)}(\mathbf x-\mathbf y)`$ generalizes the Kronecker delta $`\delta_{ij}`$ to the field labels $`(a,\mathbf x)`$.

**Free Real Scalar Field**

For a free field of mass $`m`$, use the Lorentz-invariant measure $`d\Pi_{\mathbf p}`$ and positive-energy four-momentum $`p`$:

```math
\begin{aligned}
E_{\mathbf p}&=\sqrt{\mathbf p^2+m^2},\qquad p^0=E_{\mathbf p},\qquad d\Pi_{\mathbf p}:=\frac{d^3p}{(2\pi)^3\,2E_{\mathbf p}},\\
\hat\phi_I(x)&=\int d\Pi_{\mathbf p}\left(\hat a_{\mathbf p}e^{-ip\cdot x}+\hat a_{\mathbf p}^\dagger e^{+ip\cdot x}\right).
\end{aligned}
```

The vacuum is normalized to one. The creation operators define covariantly normalized one-particle states:

```math
\boxed{\begin{aligned}
[\hat a_{\mathbf p},\hat a_{\mathbf q}^\dagger]&=2E_{\mathbf p}(2\pi)^3\delta^{(3)}(\mathbf p-\mathbf q),\qquad
[\hat a_{\mathbf p},\hat a_{\mathbf q}]=[\hat a_{\mathbf p}^\dagger,\hat a_{\mathbf q}^\dagger]=0,\\
\hat a_{\mathbf p}|0\rangle&=0,\qquad |\mathbf p\rangle:=\hat a_{\mathbf p}^\dagger|0\rangle,\\
\langle\mathbf p|\mathbf q\rangle&=2E_{\mathbf p}(2\pi)^3\delta^{(3)}(\mathbf p-\mathbf q).
\end{aligned}}
```

Normal ordering, denoted by colons, places creation operators to the left of annihilation operators. With the vacuum energy subtracted,

```math
\begin{aligned}
:\hat H_0:&=\int d\Pi_{\mathbf p}\,E_{\mathbf p}\,\hat a_{\mathbf p}^\dagger\hat a_{\mathbf p},\qquad
:\hat{\mathbf P}:=\int d\Pi_{\mathbf p}\,\mathbf p\,\hat a_{\mathbf p}^\dagger\hat a_{\mathbf p},\\
\hat N&=\int d\Pi_{\mathbf p}\,\hat a_{\mathbf p}^\dagger\hat a_{\mathbf p}.
\end{aligned}
```

**Free Dirac Field**

Using the spinors and their normalization in [Section 1.7](#dirac-field), the operators $`\hat b_{\mathbf p}^s`$ and $`\hat c_{\mathbf p}^s`$ annihilate particles and antiparticles, respectively:

```math
\hat\psi_I(x)=\sum_{s=1}^{2}\int d\Pi_{\mathbf p}\left(\hat b_{\mathbf p}^s u^s(p)e^{-ip\cdot x}+\hat c_{\mathbf p}^{s\dagger}v^s(p)e^{+ip\cdot x}\right).
```

Fermionic quantization uses anticommutators; $`\alpha,\beta`$ below are Dirac component indices. All mode anticommutators not displayed vanish, and both annihilation operators annihilate $`|0\rangle`$.

```math
\boxed{\begin{aligned}
\{\hat b_{\mathbf p}^r,\hat b_{\mathbf q}^{s\dagger}\}&=\{\hat c_{\mathbf p}^r,\hat c_{\mathbf q}^{s\dagger}\}=2E_{\mathbf p}(2\pi)^3\delta^{rs}\delta^{(3)}(\mathbf p-\mathbf q),\\
\{\hat\psi_{I,\alpha}(t,\mathbf x),\hat\psi_{I,\beta}^\dagger(t,\mathbf y)\}&=\delta_{\alpha\beta}\delta^{(3)}(\mathbf x-\mathbf y),\\
\{\hat\psi_{I,\alpha}(t,\mathbf x),\hat\psi_{I,\beta}(t,\mathbf y)\}&=0.
\end{aligned}}
```

Fermionic normal ordering includes a minus sign for every interchange of fermionic operators. The normal-ordered energy, momentum, and net fermion number are

```math
\begin{aligned}
:\hat H_0:&=\sum_s\int d\Pi_{\mathbf p}\,E_{\mathbf p}\left(\hat b_{\mathbf p}^{s\dagger}\hat b_{\mathbf p}^s+\hat c_{\mathbf p}^{s\dagger}\hat c_{\mathbf p}^s\right),\\
:\hat{\mathbf P}:&=\sum_s\int d\Pi_{\mathbf p}\,\mathbf p\left(\hat b_{\mathbf p}^{s\dagger}\hat b_{\mathbf p}^s+\hat c_{\mathbf p}^{s\dagger}\hat c_{\mathbf p}^s\right),\\
\hat Q&:=\int d^3x:\hat\psi_I^\dagger\hat\psi_I:
=\sum_s\int d\Pi_{\mathbf p}\left(\hat b_{\mathbf p}^{s\dagger}\hat b_{\mathbf p}^s-\hat c_{\mathbf p}^{s\dagger}\hat c_{\mathbf p}^s\right).
\end{aligned}
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
\begin{gathered}
\frac{d\hat O_S}{dt}=\frac{\partial\hat O_S}{\partial t},\\[4pt]
i\frac{\partial}{\partial t}|\psi_S(t)\rangle=\hat H|\psi_S(t)\rangle.
\end{gathered}
```

The solution of (2.13) with initial state $`|\psi_S(t_0)\rangle`$ depends on the time dependence of $`\hat H`$.

**(1) $`\hat H`$ without Explicit Time Dependence**

If $`\hat H`$ has no explicit time dependence, (2.13) is solved by

```math
|\psi_S(t)\rangle=e^{-i\hat H(t-t_0)}\,|\psi_S(t_0)\rangle .
```

**(2) $`\hat H(t)`$ Commuting at Different Times**

Let $`\hat H=\hat H(t)`$ depend explicitly on $`t`$, with $`[\hat H(t_1),\hat H(t_2)]=0`$ for all $`t_1,t_2`$. Here $`\int_{t_0}^{t}dt'\,\hat H(t')`$ is the operator with matrix elements $`\int_{t_0}^{t}dt'\,\langle\phi|\hat H(t')|\chi\rangle`$. Then $`\hat H(t)`$ commutes with $`\int_{t_0}^{t}dt'\,\hat H(t')`$, and

```math
\begin{aligned}
\frac{\partial}{\partial t}\Bigl(\int_{t_0}^{t}dt'\,\hat H(t')\Bigr)^n
&=\sum_{k=0}^{n-1}\Bigl(\int_{t_0}^{t}dt'\,\hat H(t')\Bigr)^k\,\hat H(t)\,\Bigl(\int_{t_0}^{t}dt'\,\hat H(t')\Bigr)^{n-1-k}\\
&=n\,\hat H(t)\Bigl(\int_{t_0}^{t}dt'\,\hat H(t')\Bigr)^{n-1}.
\end{aligned}
```

By (2.15), differentiating the exponential series of $`-i\int_{t_0}^{t}dt'\,\hat H(t')`$ term by term multiplies it by $`-i\hat H(t)`$ from the left, so

```math
|\psi_S(t)\rangle=\exp\Bigl(-i\int_{t_0}^{t}dt'\,\hat H(t')\Bigr)\,|\psi_S(t_0)\rangle ,
```

which reduces to (2.14) for $`\hat H(t)=\hat H`$.

**(3) $`\hat H(t)`$ Not Commuting at Different Times**

In general $`[\hat H(t_1),\hat H(t_2)]\neq0`$; then the second equality of (2.15) fails and (2.16) no longer solves (2.13). Instead, integrate (2.13) and iterate:

```math
\begin{aligned}
|\psi_S(t)\rangle
&=|\psi_S(t_0)\rangle-i\int_{t_0}^{t}dt_1\,\hat H(t_1)\,|\psi_S(t_1)\rangle\\
&=\Bigl[1+(-i)\int_{t_0}^{t}dt_1\,\hat H(t_1)
+(-i)^2\int_{t_0}^{t}dt_1\int_{t_0}^{t_1}dt_2\,\hat H(t_1)\hat H(t_2)+\cdots\Bigr]|\psi_S(t_0)\rangle ,
\end{aligned}
```

where the $`n`$-th term is integrated over $`t\ge t_1\ge\cdots\ge t_n\ge t_0`$, with later times to the left.

Define the time-ordered product

```math
\mathcal T[\hat H(t_1)\hat H(t_2)]
:=\theta(t_1-t_2)\,\hat H(t_1)\hat H(t_2)+\theta(t_2-t_1)\,\hat H(t_2)\hat H(t_1),
```

and likewise for $`n`$ operators, ordered with time decreasing from left to right. $`\mathcal T[\hat H(t_1)\cdots\hat H(t_n)]`$ is symmetric under permutations of $`t_1,\ldots,t_n`$; the cube $`[t_0,t]^n`$ splits into $`n!`$ regions according to the ordering of the $`t_i`$, each contributing equally, and on $`t_1>\cdots>t_n`$ the time-ordered product is the ordered product in (2.17). Hence

```math
\int_{t_0}^{t}dt_1\int_{t_0}^{t_1}dt_2\cdots\int_{t_0}^{t_{n-1}}dt_n\,
\hat H(t_1)\cdots\hat H(t_n)
=\frac1{n!}\int_{t_0}^{t}dt_1\cdots\int_{t_0}^{t}dt_n\,
\mathcal T[\hat H(t_1)\cdots\hat H(t_n)],
```

and (2.17) becomes the Dyson series

```math
\boxed{
\begin{gathered}
|\psi_S(t)\rangle=\mathcal T\exp\Bigl(-i\int_{t_0}^{t}dt'\,\hat H(t')\Bigr)|\psi_S(t_0)\rangle,\\[4pt]
\mathcal T\exp\Bigl(-i\int_{t_0}^{t}dt'\,\hat H(t')\Bigr)
:=\sum_{n=0}^{\infty}\frac{(-i)^n}{n!}\int_{t_0}^{t}dt_1\cdots dt_n\,
\mathcal T[\hat H(t_1)\cdots\hat H(t_n)].
\end{gathered}
}
```

Alternatively, differentiate the $`n`$-th term of (2.20) with respect to $`t`$: each of the $`n`$ integration variables may take the upper limit $`t`$, which is then the latest time, so $`\mathcal T`$ places $`\hat H(t)`$ leftmost; the $`n`$ contributions are equal and give $`-i\hat H(t)`$ times the $`(n-1)`$-th term. Thus the series satisfies (2.13) and equals $`|\psi_S(t_0)\rangle`$ at $`t=t_0`$; the solution is unique. If $`[\hat H(t_1),\hat H(t_2)]=0`$, $`\mathcal T`$ can be dropped and (2.20) reduces to (2.16).

**Evolution Operator**

In each case the solution is linear in $`|\psi_S(t_0)\rangle`$:

```math
|\psi_S(t)\rangle=\hat U(t,t_0)\,|\psi_S(t_0)\rangle,
\qquad
i\frac{\partial}{\partial t}\hat U(t,t_0)=\hat H(t)\,\hat U(t,t_0),
\qquad
\hat U(t_0,t_0)=1,
```

where the evolution operator $`\hat U(t,t_0)`$ is $`e^{-i\hat H(t-t_0)}`$, $`\exp\bigl(-i\int_{t_0}^{t}dt'\,\hat H(t')\bigr)`$ or $`\mathcal T\exp\bigl(-i\int_{t_0}^{t}dt'\,\hat H(t')\bigr)`$ in cases (1), (2) or (3). Since $`\hat H(t)`$ is Hermitian, $`\partial_t(\hat U^\dagger\hat U)=i\hat U^\dagger(\hat H^\dagger-\hat H)\hat U=0`$, so $`\hat U(t,t_0)`$ is unitary. Both sides of $`\hat U(t_2,t_1)\hat U(t_1,t_0)=\hat U(t_2,t_0)`$ satisfy (2.21) in $`t_2`$ and agree at $`t_2=t_1`$, so this composition law holds; at $`t_2=t_0`$ it gives $`\hat U(t,t_0)^\dagger=\hat U(t_0,t)`$.

<br><br>

<a id="heisenberg-picture"></a>
#### Heisenberg Picture

The Heisenberg picture is obtained from the Schrödinger picture by the transformation

```math
\boxed{
\begin{gathered}
|\psi_H(t)\rangle:=\hat U(t,0)^\dagger\,|\psi_S(t)\rangle=|\psi_S(0)\rangle,\\[4pt]
\hat O_H(t):=\hat U(t,0)^\dagger\,\hat O_S(t)\,\hat U(t,0).
\end{gathered}
}
```

The two pictures coincide at $`t=0`$, and $`\langle\psi_H(t)|\hat O_H(t)|\psi_H(t)\rangle=\langle\psi_S(t)|\hat O_S(t)|\psi_S(t)\rangle`$. Hence $`i\partial_t|\psi_H(t)\rangle=0`$. 

Writing $`\hat U`$ for $`\hat U(t,0)`$ and differentiating the second of (2.22) with (2.13) and (2.21),

```math
\begin{aligned}
\frac{d\hat O_H}{dt}
&=\Bigl(\frac{\partial\hat U}{\partial t}\Bigr)^\dagger\hat O_S\,\hat U
+\hat U^\dagger\,\frac{d\hat O_S}{dt}\,\hat U
+\hat U^\dagger\hat O_S\,\frac{\partial\hat U}{\partial t}\\
&=i\,\hat U^\dagger\bigl[\hat H(t),\hat O_S\bigr]\hat U
+\hat U^\dagger\,\frac{\partial\hat O_S}{\partial t}\,\hat U\\
&=i\bigl[\hat H_H(t),\hat O_H\bigr]+\Bigl(\frac{\partial\hat O_S}{\partial t}\Bigr)_H,
\end{aligned}
```

where $`\hat H_H(t):=\hat U^\dagger\hat H(t)\,\hat U`$ and $`(\partial\hat O_S/\partial t)_H:=\hat U^\dagger(\partial\hat O_S/\partial t)\,\hat U`$; the last step inserts $`\hat U\hat U^\dagger=1`$. In cases (1) and (2), $`\hat U(t,0)`$ commutes with $`\hat H(t)`$, so $`\hat H_H(t)=\hat H(t)`$. In case (1), (2.22) and (2.23) become

```math
\begin{gathered}
\hat O_H(t)=e^{i\hat Ht}\,\hat O_S(t)\,e^{-i\hat Ht},\\[4pt]
\frac{d\hat O_H}{dt}=i[\hat H,\hat O_H]+\Bigl(\frac{\partial\hat O_S}{\partial t}\Bigr)_H .
\end{gathered}
```

<br><br>

<a id="qft-ch3"></a>
## 3. The Standard Model

<a id="yang-mills"></a>
### 3.1 Yang–Mills Theory

**Lie Group**

```math
\begin{aligned}
U(n)&=\{A\in M_n(\mathbb C)\mid A^\dagger A=I\},\\[6pt]
SU(n)&=\{A\in M_n(\mathbb C)\mid \det A=1,\ A^\dagger A=I\}.
\end{aligned}
```


**$`U(n)`$**

Consider the one-parameter subgroup

```math
\begin{aligned}
g(\theta)&=e^{i\theta T},\qquad \theta\in\mathbb R,\quad T\in M_n(\mathbb C),\\[6pt]
\left.\frac{d}{d\theta}g(\theta)\right|_{\theta=0}&=iT,\\[6pt]
g^\dagger(\theta)g(\theta)=I\quad\text{for all }\theta\in\mathbb R
&\Longrightarrow i(T-T^\dagger)=0
\Longrightarrow T^\dagger=T.
\end{aligned}
```

 The Lie algebra is

```math
\mathfrak{u}(n)=\{iT\in M_n(\mathbb C)\mid T^\dagger=T\}.
```


**$`SU(n)`$**

The one-parameter subgroup and its generator are

```math
\begin{aligned}
g(\theta)&=e^{i\theta T},\qquad \theta\in\mathbb R,\quad T\in M_n(\mathbb C),\\[6pt]
\left.\frac{d}{d\theta}g(\theta)\right|_{\theta=0}&=iT.
\end{aligned}
```


```math
0=\left.\frac{d}{d\theta}\bigl[g^\dagger(\theta)g(\theta)\bigr]\right|_{\theta=0}
=i(T-T^\dagger)
\quad\Longrightarrow\quad T^\dagger=T.
```

We use the theorem $`\det(e^{i\theta T})=e^{i\theta\,\mathop{\rm tr}\nolimits\,T}`$, valid for any $`T\in M_n(\mathbb C)`$ and $`\theta\in\mathbb C`$.

```math
0=\left.\frac{d}{d\theta}\det g(\theta)\right|_{\theta=0}
=\left.\frac{d}{d\theta}e^{i\theta\,\mathop{\rm tr}\nolimits\,T}\right|_{\theta=0}
=i\,\mathop{\rm tr}\nolimits\,T
\quad\Longrightarrow\quad \mathop{\rm tr}\nolimits\,T=0.
```

Thus $`T`$ is traceless and Hermitian, and the Lie algebra is

```math
\mathfrak{su}(n)=\{iT\in M_n(\mathbb C)\mid
\mathop{\rm tr}\nolimits\,T=0,\ T^\dagger=T\}.
```

Scalar multiplication is taken over $`\mathbb R`$ to preserve anti-Hermiticity; hence $`\mathfrak{su}(n)`$ and  $`\mathfrak{u}(n)`$ are both real Lie algebras.

<a id="ym-4"></a>
**Structure Constants**

Let $`\{iT^a\}`$, with $`a=1,\ldots,n^2-1`$, be a basis of the real Lie algebra $`\mathfrak{su}(n)`$.
The structure constants $`f^{abc}`$ are defined by $`[T^a,T^b]=if^{abc}T^c`$.

**Reality: $`f^{abc}\in\mathbb R`$.**

Since the matrices $`T^a`$ are Hermitian,

```math
\begin{aligned}
([T^a,T^b])^\dagger&=-[T^a,T^b],\qquad
\mathop{\rm tr}\nolimits [T^a,T^b]=0,\\[6pt]
[T^a,T^b]&\in\mathfrak{su}(n),\\[6pt]
[T^a,T^b]&=f^{abc}(iT^c),\qquad f^{abc}\in\mathbb R.
\end{aligned}
```

The expansion coefficients are real because $`\{iT^c\}`$ is a basis over $`\mathbb R`$.

<a id="ym-orthonormal"></a>
**Orthonormal Basis of $`\mathfrak{su}(n)`$**

For $`iT_1,iT_2\in\mathfrak{su}(n)`$, define

```math
\begin{aligned}
(\cdot,\cdot)&:\mathfrak{su}(n)\times\mathfrak{su}(n)\longrightarrow\mathbb R,\\[6pt]
(iT_1,iT_2)&:=-2\,\mathop{\rm tr}\nolimits \bigl[(iT_1)(iT_2)\bigr]\\
&=2\,\mathop{\rm tr}\nolimits (T_1T_2).
\end{aligned}
```

**Proof** that (3.9) satisfies the axioms of an inner product



*(i) Real values.* 

Using $`T_1^\dagger=T_1`$, $`T_2^\dagger=T_2`$ and cyclicity of the trace,

```math
\begin{aligned}
\bigl[\mathop{\rm tr}\nolimits (T_1T_2)\bigr]^*
&=\mathop{\rm tr}\nolimits \bigl[(T_1T_2)^\dagger\bigr]
=\mathop{\rm tr}\nolimits (T_2^\dagger T_1^\dagger)\\
&=\mathop{\rm tr}\nolimits (T_2T_1)
=\mathop{\rm tr}\nolimits (T_1T_2),
\end{aligned}
```

so $`(iT_1,iT_2)=2\,\mathop{\rm tr}\nolimits (T_1T_2)\in\mathbb R`$.

*(ii) Symmetry.* 

By cyclicity of the trace,

```math
\begin{aligned}
(iT_1,iT_2)&=2\,\mathop{\rm tr}\nolimits (T_1T_2)\\
&=2\,\mathop{\rm tr}\nolimits (T_2T_1)=(iT_2,iT_1).
\end{aligned}
```

*(iii) Bilinearity.* 

For $`a,b\in\mathbb R`$, $`a\,iT_1+b\,iT_2=i(aT_1+bT_2)`$, 
and linearity of the trace gives $`(a\,iT_1+b\,iT_2,\,iT_3)=2\,\mathop{\rm tr}\nolimits \bigl[(aT_1+bT_2)T_3\bigr]=a\,(iT_1,iT_3)+b\,(iT_2,iT_3)`$. By (ii), the form is also linear in its second argument.

*(iv) Positive definiteness.* Using $`T=T^\dagger`$,

```math
\begin{aligned}
(iT,iT)&=2\,\mathop{\rm tr}\nolimits (T^2)=2\,\mathop{\rm tr}\nolimits (T^\dagger T)\\
&=2\sum_{j,k}|T_{jk}|^2\ge0.
\end{aligned}
```

Equality holds if and only if $`T_{jk}=0`$ for all $`j,k`$, i.e. $`iT=0`$. $`\square`$

Having established that this form defines an inner product on $`\mathfrak{su}(n)`$, we may choose an orthonormal basis $`\{iT^a\}`$ satisfying $`(iT^a,iT^b)=\delta^{ab}`$. Equivalently,

```math
\boxed{\mathop{\rm tr}\nolimits (T^aT^b)=\frac12\delta^{ab}.}
```

**Total antisymmetry.** With this normalization and cyclicity of the trace, we obtain

```math
\begin{aligned}
\mathop{\rm tr}\nolimits ([T^a,T^b]T^c)&=\frac{i}{2}f^{abc},\\
f^{abc}&=-2i\,\mathop{\rm tr}\nolimits ([T^a,T^b]T^c),\\
f^{bac}&=-f^{abc},\\
f^{acb}
&=-2i\,\mathop{\rm tr}\nolimits (T^aT^cT^b-T^cT^aT^b)\\
&=-2i\,\mathop{\rm tr}\nolimits (T^bT^aT^c-T^aT^bT^c)
=-f^{abc}.
\end{aligned}
```

```math
\boxed{
f^{abc}=f^{[abc]}\in\mathbb R
}
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
\Psi(x):=\begin{pmatrix}
\psi_1(x)\\
\vdots\\
\psi_n(x)
\end{pmatrix}.
```

Define the Dirac adjoint by

```math
\begin{aligned}
\bar\Psi(x)&:=\bigl(\bar\psi_1(x),\ldots,\bar\psi_n(x)\bigr),\\[6pt]
\bar\psi_a(x)&:=\psi_a^\dagger(x)\gamma^0.
\end{aligned}
```

The kinetic term of the Lagrangian density is

```math
\begin{aligned}
\mathcal L_{\mathrm{kin}}
&=\bar\Psi\,i\gamma^\mu I_n\partial_\mu\Psi\\[6pt]
&=\sum_{a=1}^{n}\bar\psi_a\,i\gamma^\mu\partial_\mu\psi_a.
\end{aligned}
```



For $`SU(n)`$ in the defining representation $`U`$, let $`g_{\mathrm{YM}}`$ be the coupling and $`U(\theta)`$ the representation of the local group element. The connection and its transformation are

```math
\begin{aligned}
U(\theta)&:=e^{i\theta^a(x)T^a},\qquad \theta^a(x)\in\mathbb R,\\
A_\mu&:=A_\mu^aT^a,\qquad D_\mu:=\partial_\mu-ig_{\mathrm{YM}}A_\mu,
\qquad \Psi'=U(\theta)\Psi,\\
A_\mu'&=U(\theta)A_\mu U(\theta)^\dagger-\frac{i}{g_{\mathrm{YM}}}\bigl(\partial_\mu U(\theta)\bigr)U(\theta)^\dagger,\\
D_\mu'&=U(\theta)D_\mu U(\theta)^\dagger .
\end{aligned}
```

The field strength is

```math
\begin{aligned}
[D_\mu,D_\nu]&=:-ig_{\mathrm{YM}}F_{\mu\nu},\\
F_{\mu\nu}&=\partial_\mu A_\nu-\partial_\nu A_\mu-ig_{\mathrm{YM}}[A_\mu,A_\nu],\\
F_{\mu\nu}^a&=\partial_\mu A_\nu^a-\partial_\nu A_\mu^a
+g_{\mathrm{YM}}f^{abc}A_\mu^bA_\nu^c,\\
F_{\mu\nu}'&=U(\theta)F_{\mu\nu}U(\theta)^\dagger .
\end{aligned}
```

Including the gauge field, the kinetic term (3.18) becomes

```math
\boxed{
\begin{aligned}
\mathcal L_{\mathrm{kin}}
&=\bar\Psi\,i\gamma^\mu D_\mu\Psi
-\frac12\,\mathop{\rm tr}\nolimits (F_{\mu\nu}F^{\mu\nu})\\[6pt]
&=\bar\Psi\,i\gamma^\mu D_\mu\Psi-\frac14F_{\mu\nu}^aF^{a\mu\nu}.
\end{aligned}
}
```

On a matrix-valued adjoint field $`X`$, define $`D_\mu X:=\partial_\mu X-ig_{\mathrm{YM}}[A_\mu,X]`$.

Using the definitions above, the field equations and the Bianchi identity simplify to

```math
\begin{aligned}
i\gamma^\mu D_\mu\Psi&=0,\qquad
D_\mu F^{\mu\nu}=-g_{\mathrm{YM}}j^\nu,\qquad
j^\nu:=(\bar\Psi\gamma^\nu T^a\Psi)T^a,\\
D_\mu F_{\nu\rho}+D_\nu F_{\rho\mu}+D_\rho F_{\mu\nu}&=0 .
\end{aligned}
```

<br><br>

<a id="qed"></a>
### 3.2 Quantum Electrodynamics


**Gauge Group $`U(1)`$**

The gauge group of QED is $`U(1)`$, i.e. (3.1) with $`n=1`$; its Lie algebra $`\mathfrak u(1)=i\mathbb R`$ is Abelian. 

Let $`e>0`$ be the elementary charge and $`\theta:\mathbb R^4\to\mathbb R`$. The transformation is a flavor singlet: it acts identically on the three generations. It differs between representations of $`U(1)`$, which are labeled by the charge: a Dirac field $`\psi_f`$ as in (1.94) with charge $`Q_fe`$ transforms, with the same $`\theta`$ for every $`f`$, as

```math
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
```

**Covariant Derivative and Field Strength**

The photon field $`A_\mu`$ is real. Taking $`U(\theta)=e^{iQ\theta}`$ and replacing $`g_{\mathrm{YM}}A_\mu`$ by $`eQA_\mu`$ in (3.19)–(3.20) gives

```math
\begin{aligned}
D_\mu&:=\partial_\mu-ieQA_\mu,\qquad
D_\mu'\psi'=e^{iQ\theta}D_\mu\psi,\\
A_\mu'&=A_\mu+\frac1e\,\partial_\mu\theta,\\
[D_\mu,D_\nu]&=-ieQF_{\mu\nu},\qquad
F_{\mu\nu}=\partial_\mu A_\nu-\partial_\nu A_\mu=F_{\mu\nu}'.
\end{aligned}
```



**The QED Lagrangian**

```math
\boxed{
\mathcal L_{\mathrm{QED}}
=\bar\psi\bigl(i\gamma^\mu D_\mu-m\bigr)\psi
-\frac14F_{\mu\nu}F^{\mu\nu},
}
```

where $`m`$ is the mass of $`\psi`$ and $`D_\mu`$ acts on the $`\psi`$ to its right. By (3.23)–(3.24), $`\mathcal L_{\mathrm{QED}}`$ is gauge invariant. Substituting $`D_\mu`$,

```math
\mathcal L_{\mathrm{QED}}
=\bar\psi\bigl(i\gamma^\mu\partial_\mu-m\bigr)\psi
-\frac14F_{\mu\nu}F^{\mu\nu}
+eQA_\mu\bar\psi\gamma^\mu\psi,
```

i.e. the Dirac Lagrangian (1.94), the Maxwell Lagrangian (1.147) and the interaction term.



**Equations of Motion**

With $`j^\nu=\bar\psi\gamma^\nu\psi`$ as in (1.132), $`\partial\mathcal L_{\mathrm{QED}}/\partial(\partial_\mu A_\nu)=-F^{\mu\nu}`$ and $`\partial\mathcal L_{\mathrm{QED}}/\partial A_\nu=eQ\,j^\nu`$. The Euler–Lagrange equations and the Bianchi identity are

```math
\begin{aligned}
\bigl(i\gamma^\mu D_\mu-m\bigr)\psi&=0,\qquad
\partial_\mu F^{\mu\nu}=-eQ\,j^\nu,\qquad
\partial_\nu j^\nu=0,\\
\partial_\mu F_{\nu\rho}+\partial_\nu F_{\rho\mu}+\partial_\rho F_{\mu\nu}&=0 .
\end{aligned}
```

<br><br>

<a id="qcd"></a>
### 3.3 Quantum Chromodynamics

**Color Group $`SU(3)`$**

The gauge group of QCD is $`SU(3)`$. By (3.7) with $`n=3`$, $`\mathfrak{su}(3)`$ has a basis $`\{iT^a\}`$, $`a=1,\ldots,8`$, which we take orthonormal in the sense of (3.13). The standard choice is $`T^a:=\tfrac12\lambda^a`$, where the Gell-Mann matrices are

```math
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
```

Each $`\lambda^a`$ is Hermitian and traceless, and $`\mathop{\rm tr}\nolimits (\lambda^a\lambda^b)=2\delta^{ab}`$, so $`\mathop{\rm tr}\nolimits (T^aT^b)=\tfrac12\delta^{ab}`$ as in (3.13). By (3.14), $`f^{abc}=-2i\,\mathop{\rm tr}\nolimits ([T^a,T^b]T^c)`$; up to the antisymmetry (3.15), the nonzero structure constants are

```math
\begin{aligned}
f^{123}&=1,\\[4pt]
f^{147}=f^{246}=f^{257}=f^{345}&=\tfrac12,\qquad
f^{156}=f^{367}=-\tfrac12,\\[4pt]
f^{458}=f^{678}&=\tfrac{\sqrt3}{2}.
\end{aligned}
```

The quadratic Casimir $`T^aT^a`$ commutes with every $`T^b`$, since $`f^{bac}`$ is antisymmetric in $`a,c`$:

```math
[T^b,T^aT^a]=[T^b,T^a]T^a+T^a[T^b,T^a]=if^{bac}\bigl(T^cT^a+T^aT^c\bigr)=0.
```

The defining representation of $`SU(3)`$ is irreducible, so by Schur's lemma $`T^aT^a=C_FI_3`$. Taking the trace with (3.13),

```math
3C_F=\mathop{\rm tr}\nolimits (T^aT^a)=\tfrac12\cdot8
\quad\Longrightarrow\quad
\boxed{T^aT^a=C_FI_3,\qquad C_F=\tfrac43.}
```

**Quark Fields**

For each flavor $`f\in\{u,d,s,c,b,t\}`$ the quark field is a color triplet, i.e. the multiplet (3.16) with $`n=3`$, with Dirac adjoint as in (3.17):

```math
q_f(x):=\begin{pmatrix}\psi_{f,1}(x)\\\psi_{f,2}(x)\\\psi_{f,3}(x)\end{pmatrix},
\qquad
\bar q_f(x):=\bigl(\bar\psi_{f,1}(x),\bar\psi_{f,2}(x),\bar\psi_{f,3}(x)\bigr).
```

Throughout this section $`\gamma^\mu`$ acts on the spinor index of each $`\psi_{f,a}`$ and the $`3\times3`$ matrices $`T^a`$ act on the color index, so $`\gamma^\mu`$ commutes with every matrix built from the $`T^a`$.

**Local $`SU(3)`$ Transformation**

Let $`\theta^a:\mathbb R^4\to\mathbb R`$, $`a=1,\ldots,8`$, and set

```math
g(x):=e^{i\theta^a(x)T^a}\in SU(3).
```

This is the internal transformation (1.66) with $`g`$ now depending on $`x`$. The quark fields transform as

```math
q_f'(x)=g(x)\,q_f(x),\qquad
\bar q_f'(x)=\bar q_f(x)\,g^\dagger(x).
```

Since $`\partial_\mu(gq_f)=g\,\partial_\mu q_f+(\partial_\mu g)\,q_f`$, the derivative term of (3.18) is not invariant under (3.34):

```math
\bar q_f'\,i\gamma^\mu\partial_\mu q_f'
=\bar q_f\,i\gamma^\mu\partial_\mu q_f
+\bar q_f\,i\gamma^\mu g^\dagger(\partial_\mu g)\,q_f.
```

**Covariant Derivative and Gluon Fields**

Introduce eight real vector fields $`A^a_\mu`$, the gluon fields, and define

```math
A_\mu:=A^a_\mu T^a,\qquad
D_\mu:=\partial_\mu-ig_sA_\mu,
```

where $`g_s\in\mathbb R`$ is the strong coupling constant and $`D_\mu`$ acts on color triplets. Let $`A_\mu'`$ denote the transformed gluon field and $`D_\mu':=\partial_\mu-ig_sA_\mu'`$. We require $`D_\mu'q_f'=g\,D_\mu q_f`$:

```math
\begin{aligned}
D_\mu'(gq_f)&=g\,\partial_\mu q_f+(\partial_\mu g)\,q_f-ig_sA_\mu'\,g\,q_f,\\[6pt]
g\,D_\mu q_f&=g\,\partial_\mu q_f-ig_s\,gA_\mu\,q_f.
\end{aligned}
```

Equating the two for all $`q_f`$ gives $`A_\mu'g=gA_\mu-\frac{i}{g_s}\partial_\mu g`$, i.e.

```math
\boxed{
A_\mu'=gA_\mu g^\dagger-\frac{i}{g_s}(\partial_\mu g)\,g^\dagger
=gA_\mu g^\dagger+\frac{i}{g_s}\,g\,\partial_\mu g^\dagger.
}
```

Differentiating $`gg^\dagger=I_3`$ gives $`\bigl((\partial_\mu g)g^\dagger\bigr)^\dagger=-(\partial_\mu g)g^\dagger`$, and Jacobi's formula $`\partial_\mu\det g=\det g\,\mathop{\rm tr}\nolimits (g^\dagger\partial_\mu g)`$ with $`\det g=1`$ gives $`\mathop{\rm tr}\nolimits \bigl((\partial_\mu g)g^\dagger\bigr)=0`$. Hence $`A_\mu'`$ is again Hermitian and traceless, $`A_\mu'=A_\mu'^aT^a`$ with real $`A_\mu'^a`$.

Since $`D_\mu'(gq_f)=g\,D_\mu q_f`$ holds for all $`q_f`$, as operators on color triplets

```math
D_\mu'=g\,D_\mu\,g^\dagger.
```

For infinitesimal $`\theta^a`$, $`g=I_3+i\theta^aT^a+O(\theta^2)`$ and (3.38) gives

```math
\begin{aligned}
A_\mu'&=A_\mu+i\theta^b[T^b,A_\mu]+\frac1{g_s}(\partial_\mu\theta^a)T^a+O(\theta^2)\\
&=A_\mu-f^{bca}\theta^bA^c_\mu T^a+\frac1{g_s}(\partial_\mu\theta^a)T^a+O(\theta^2),\\[6pt]
\delta A^a_\mu:=A_\mu'^a-A_\mu^a
&=\frac1{g_s}\partial_\mu\theta^a+f^{abc}A^b_\mu\theta^c+O(\theta^2).
\end{aligned}
```

**Field Strength**

Define $`F_{\mu\nu}`$ by $`[D_\mu,D_\nu]=:-ig_sF_{\mu\nu}`$. Since $`[\partial_\mu,A_\nu]q_f=(\partial_\mu A_\nu)q_f`$,

```math
\begin{aligned}
[D_\mu,D_\nu]
&=[\partial_\mu-ig_sA_\mu,\ \partial_\nu-ig_sA_\nu]\\
&=-ig_s\bigl(\partial_\mu A_\nu-\partial_\nu A_\mu\bigr)-g_s^2[A_\mu,A_\nu],\\[6pt]
F_{\mu\nu}&=\partial_\mu A_\nu-\partial_\nu A_\mu-ig_s[A_\mu,A_\nu].
\end{aligned}
```

Expanding in the basis, $`F_{\mu\nu}=F^a_{\mu\nu}T^a`$ with

```math
\boxed{
F^a_{\mu\nu}=\partial_\mu A^a_\nu-\partial_\nu A^a_\mu+g_sf^{abc}A^b_\mu A^c_\nu.
}
```

By (3.39), $`[D_\mu',D_\nu']=g[D_\mu,D_\nu]g^\dagger`$, so

```math
F_{\mu\nu}'=gF_{\mu\nu}g^\dagger,
\qquad
\delta F^a_{\mu\nu}=f^{abc}F^b_{\mu\nu}\theta^c+O(\theta^2).
```

By cyclicity of the trace and (3.13),

```math
\mathop{\rm tr}\nolimits \bigl(F_{\mu\nu}'F'^{\mu\nu}\bigr)
=\mathop{\rm tr}\nolimits \bigl(F_{\mu\nu}F^{\mu\nu}\bigr)
=\tfrac12F^a_{\mu\nu}F^{a\mu\nu}.
```

**The QCD Lagrangian**

```math
\boxed{
\mathcal L_{\mathrm{QCD}}
=\sum_{f}\bar q_f\bigl(i\gamma^\mu D_\mu-m_f\bigr)q_f
-\frac12\,\mathop{\rm tr}\nolimits \bigl(F_{\mu\nu}F^{\mu\nu}\bigr)
=\sum_{f}\bar q_f\bigl(i\gamma^\mu D_\mu-m_f\bigr)q_f
-\frac14F^a_{\mu\nu}F^{a\mu\nu},
}
```

where the sum runs over the six flavors in (3.32), $`m_f`$ is the mass of flavor $`f`$, and $`D_\mu`$ acts on the $`q_f`$ to its right. Under (3.34) and (3.38), $`D_\mu'q_f'=g\,D_\mu q_f`$ by construction, so

```math
\bar q_f'\bigl(i\gamma^\mu D_\mu'-m_f\bigr)q_f'
=\bar q_f\,g^\dagger\bigl(i\gamma^\mu g\,D_\mu-m_f\,g\bigr)q_f
=\bar q_f\bigl(i\gamma^\mu D_\mu-m_f\bigr)q_f.
```

Together with (3.44), $`\mathcal L_{\mathrm{QCD}}`$ is invariant under the local transformations (3.34), (3.38).

Substituting (3.36) and (3.42) into (3.45) separates the free and interaction terms:

```math
\begin{aligned}
\mathcal L_{\mathrm{QCD}}
={}&\sum_f\bar q_f\bigl(i\gamma^\mu\partial_\mu-m_f\bigr)q_f
-\frac14\bigl(\partial_\mu A^a_\nu-\partial_\nu A^a_\mu\bigr)\bigl(\partial^\mu A^{a\nu}-\partial^\nu A^{a\mu}\bigr)\\[6pt]
&+g_sA^a_\mu\sum_f\bar q_f\gamma^\mu T^aq_f
-\frac{g_s}{2}f^{abc}\bigl(\partial_\mu A^a_\nu-\partial_\nu A^a_\mu\bigr)A^{b\mu}A^{c\nu}
-\frac{g_s^2}{4}f^{abc}f^{ade}A^b_\mu A^c_\nu A^{d\mu}A^{e\nu}.
\end{aligned}
```

**Equations of Motion**

Treating $`q_f`$, $`\bar q_f`$ and $`A^a_\mu`$ as independent, the Euler–Lagrange equation for $`\bar q_f`$ is

```math
\bigl(i\gamma^\mu D_\mu-m_f\bigr)q_f=0.
```

For $`A^a_\nu`$, define the color current $`j^{a\nu}:=\sum_f\bar q_f\gamma^\nu T^aq_f`$. From (3.45) with (3.42) and (3.47),

```math
\begin{aligned}
\frac{\partial\mathcal L_{\mathrm{QCD}}}{\partial(\partial_\mu A^a_\nu)}
&=-\frac12F^{b\rho\sigma}\,\delta^{ab}\bigl(\delta^\mu_\rho\delta^\nu_\sigma-\delta^\mu_\sigma\delta^\nu_\rho\bigr)
=-F^{a\mu\nu},\\[6pt]
\frac{\partial\mathcal L_{\mathrm{QCD}}}{\partial A^a_\nu}
&=g_sj^{a\nu}-\frac12F^{b\rho\sigma}\,g_s\bigl(f^{bad}\delta^\nu_\rho A^d_\sigma+f^{bca}A^c_\rho\delta^\nu_\sigma\bigr)\\
&=g_sj^{a\nu}-g_sf^{abc}A^c_\mu F^{b\mu\nu}\\
&=g_sj^{a\nu}+g_sf^{abc}A^b_\mu F^{c\mu\nu}.
\end{aligned}
```

The Euler–Lagrange equation $`\partial_\mu\bigl(\partial\mathcal L_{\mathrm{QCD}}/\partial(\partial_\mu A^a_\nu)\bigr)=\partial\mathcal L_{\mathrm{QCD}}/\partial A^a_\nu`$ then reads

```math
\boxed{
\partial_\mu F^{a\mu\nu}+g_sf^{abc}A^b_\mu F^{c\mu\nu}=-g_sj^{a\nu}.
}
```

The left-hand side is the $`a`$-component of $`\partial_\mu F^{\mu\nu}-ig_s[A_\mu,F^{\mu\nu}]`$, the covariant derivative of $`F^{\mu\nu}`$ in the adjoint representation; with $`j^\nu:=j^{a\nu}T^a`$, (3.50) is

```math
D_\mu F^{\mu\nu}:=\partial_\mu F^{\mu\nu}-ig_s[A_\mu,F^{\mu\nu}]=-g_s\,j^\nu.
```

<br><br>

<a id="higgs-mechanism"></a>
### 3.4 Spontaneous Symmetry Breaking and the Higgs Mechanism

<a id="higgs-lagrangian"></a>
#### Higgs Lagrangian

Let $`\Phi:=(\phi_1,\ldots,\phi_n)^T`$ be a multiplet of complex scalar fields. For $`\mu_H^2\in\mathbb R`$ and $`\lambda_H>0`$, the Higgs Lagrangian is

```math
\boxed{
\begin{aligned}
\mathcal L_{\mathrm{Higgs}}&=(\partial_\mu\Phi)^\dagger\partial^\mu\Phi-V(\Phi),\\
V(\Phi)&=-\mu_H^2\,\Phi^\dagger\Phi+\lambda_H(\Phi^\dagger\Phi)^2 .
\end{aligned}
}
```

The Lagrangian (3.52) depends on $`\Phi`$ only through $`\Phi^\dagger\Phi`$ and $`(\partial_\mu\Phi)^\dagger\partial^\mu\Phi`$. For a constant $`g\in U(n)`$,

```math
\begin{aligned}
\Phi'&=g\,\Phi,\\
\Phi'^\dagger\Phi'&=\Phi^\dagger g^\dagger g\,\Phi=\Phi^\dagger\Phi,\\
(\partial_\mu\Phi')^\dagger\partial^\mu\Phi'&=(\partial_\mu\Phi)^\dagger g^\dagger g\,\partial^\mu\Phi=(\partial_\mu\Phi)^\dagger\partial^\mu\Phi,
\end{aligned}
```

so $`\mathcal L_{\mathrm{Higgs}}`$ is invariant under global $`U(n)`$ transformations.

**Physical Vacuum**

The classical vacuum is the field configuration of minimum energy. The energy density of (3.52) is

```math
\mathcal H=(\partial_0\Phi)^\dagger\partial_0\Phi+\sum_{i=1}^3(\partial_i\Phi)^\dagger\partial_i\Phi+V(\Phi).
```

The first two terms are nonnegative, so the classical vacuum is a constant $`\Phi=\Phi_0`$ minimizing $`V`$. Since $`\partial V/\partial(\Phi^\dagger\Phi)=-\mu_H^2+2\lambda_H\Phi^\dagger\Phi`$ and $`\Phi^\dagger\Phi\ge0`$,

```math
\boxed{
\begin{aligned}
\mu_H^2\le0:&\quad\Phi_0=0,\\
\mu_H^2>0:&\quad\Phi_0^\dagger\Phi_0=\frac{v^2}{2},\qquad
v:=\sqrt{\frac{\mu_H^2}{\lambda_H}},\qquad
V(\Phi_0)=-\frac{\lambda_Hv^4}{4}.
\end{aligned}
}
```

For $`\mu_H^2\le0`$ the vacuum $`\Phi_0=0`$ is invariant under all of $`U(n)`$. From now on $`\mu_H^2>0`$: the vacua form the sphere $`\Phi_0^\dagger\Phi_0=v^2/2`$ in $`\mathbb C^n`$, and $`\Phi=0`$ is a local maximum of $`V`$. The physical vacuum is a single point of this sphere. We choose

```math
\boxed{
\Phi_0:=\frac1{\sqrt2}\begin{pmatrix}0\\\vdots\\0\\v\end{pmatrix}
}
```

and from now on $`\Phi_0`$ denotes this vacuum.

 Any vacuum $`\Phi_0'`$ with $`\Phi_0'^\dagger\Phi_0'=v^2/2`$ equals $`g\,\Phi_0`$, where $`g\in U(n)`$ has last column $`\sqrt2\,\Phi_0'/v`$ and its other columns complete it to an orthonormal basis of $`\mathbb C^n`$; by (3.53), different choices are related by a symmetry transformation.

<br><br>

<a id="spontaneous-symmetry-breaking"></a>
#### Spontaneous Symmetry Breaking

A transformation $`g\in U(n)`$ is unbroken if it leaves the vacuum invariant. The unbroken subgroup is

```math
\boxed{
G_0:=\{g\in U(n)\mid g\,\Phi_0=\Phi_0\}\cong U(n-1).
}
```

A unitary $`g`$ with $`g\Phi_0=\Phi_0`$ maps the orthogonal complement $`\Phi_0^\perp:=\{u\in\mathbb C^n\mid\Phi_0^\dagger u=0\}`$ to itself, and $`g\mapsto g|_{\Phi_0^\perp}`$ identifies $`G_0`$ with the unitary group of the $`(n-1)`$-dimensional space $`\Phi_0^\perp`$.

$`U(n)`$ is spontaneously broken to $`G_0`$ if $`G_0\neq U(n)`$, i.e. if the Lagrangian is invariant under $`U(n)`$ but the vacuum is not; by (3.57), $`U(n)`$ is spontaneously broken to $`G_0\cong U(n-1)`$.

Let $`T^a`$, $`a=1,\ldots,n^2`$, be Hermitian generators of $`U(n)`$ with $`\mathop{\rm tr}\nolimits (T^aT^b)=\frac12\delta^{ab}`$. A Hermitian $`n\times n`$ matrix $`T`$ is an unbroken generator if $`e^{i\theta T}\in G_0`$ for all $`\theta\in\mathbb R`$; differentiating $`e^{i\theta T}\Phi_0=\Phi_0`$ at $`\theta=0`$,

```math
e^{i\theta T}\in G_0\ \ \text{for all }\theta\in\mathbb R
\iff T\Phi_0=0 .
```

The unbroken generators form the Lie algebra of $`G_0\cong U(n-1)`$, of dimension $`(n-1)^2`$, and the broken generators are the elements of its orthogonal complement under $`\mathop{\rm tr}\nolimits\,`$, of dimension $`n^2-(n-1)^2=2n-1`$. A broken $`T\neq0`$ satisfies $`T\Phi_0\neq0`$: otherwise $`T`$ would also be unbroken, and $`\mathop{\rm tr}\nolimits (T^2)=0`$.

Let $`G^a`$, $`a=1,\ldots,2n-1`$, be a basis of the broken generators. The matrix $`\Phi_0^\dagger\{G^a,G^b\}\Phi_0=2\,\mathop{\rm Re}\nolimits \bigl[(G^a\Phi_0)^\dagger G^b\Phi_0\bigr]`$ is real and symmetric. An orthogonal change of basis $`G^a\to O^{ab}G^b`$, $`O\in O(2n-1)`$, preserves $`\mathop{\rm tr}\nolimits (G^aG^b)=\frac12\delta^{ab}`$ and acts on this matrix by $`O(\,\cdot\,)O^T`$; choosing $`O`$ to diagonalize it,

```math
\begin{aligned}
\mathop{\rm tr}\nolimits (G^aG^b)&=\frac12\delta^{ab},\\
\Phi_0^\dagger\{G^a,G^b\}\Phi_0&=2\,\delta^{ab}\,\Phi_0^\dagger(G^a)^2\Phi_0,\qquad
\Phi_0^\dagger(G^a)^2\Phi_0=(G^a\Phi_0)^\dagger G^a\Phi_0>0 .
\end{aligned}
```

From now on $`T^a:=G^a`$ for $`a=1,\ldots,2n-1`$, and $`T^a`$, $`a=2n,\ldots,n^2`$, span the unbroken generators.


**Parametrization of the Higgs Field**

Parametrize the $`2n`$ real fields of $`\Phi`$ by the Higgs field $`h`$ and $`\theta^a`$, $`a=1,\ldots,2n-1`$, along the broken generators:

```math
\boxed{
\begin{aligned}
\Phi&=\frac1{\sqrt2}\,e^{i\theta^a(x)G^a}\begin{pmatrix}0\\\vdots\\0\\v+h\end{pmatrix}\\
&=\Bigl(1+\frac hv\Bigr)U(\theta)\,\Phi_0,\\
U(\theta)&:=e^{iX},\qquad X:=\theta^a(x)G^a .
\end{aligned}
}
```

<br><br>

<a id="higgs-mechanism-masses"></a>
#### Higgs Mechanism

Gauge the $`U(n)`$ symmetry (3.53) with the generators $`T^a`$, $`a=1,\ldots,n^2`$, chosen after (3.59), gauge fields $`A_\mu^a`$, and coupling $`g_{\mathrm{YM}}`$ as in (3.19). Replacing $`\partial_\mu`$ by $`D_\mu`$ in (3.52) and adding the gauge kinetic term of (3.21),

```math
\boxed{
\begin{aligned}
\mathcal L&=(D_\mu\Phi)^\dagger D^\mu\Phi-V(\Phi)-\frac14F_{\mu\nu}^aF^{a\mu\nu},\\
D_\mu\Phi&=\partial_\mu\Phi-ig_{\mathrm{YM}}A_\mu\Phi,\qquad A_\mu:=A_\mu^aT^a .
\end{aligned}
}
```

By (3.19)–(3.20) with $`T^a`$ the generators of $`U(n)`$, $`\mathcal L`$ is invariant under $`\Phi'=U(\theta)\Phi`$, $`U(\theta)=e^{i\theta^a(x)T^a}`$; for $`\theta^a=0`$, $`a\ge2n`$, this is the $`U(\theta)`$ of (3.60).

Substitute the parametrization (3.60) into (3.61). With $`\mu_H^2=\lambda_Hv^2`$ from (3.55) and $`U^\dagger U=I_n`$, the potential depends only on $`h`$:

```math
\begin{aligned}
\Phi^\dagger\Phi&=\frac{(v+h)^2}2,\\
V&=\lambda_H\Bigl(\Phi^\dagger\Phi-\frac{v^2}2\Bigr)^2-\frac{\lambda_Hv^4}4\\
&=\lambda_Hv^2h^2+\lambda_Hv\,h^3+\frac{\lambda_H}4h^4-\frac{\lambda_Hv^4}4 .
\end{aligned}
```

For the kinetic term, $`\Phi_0^\dagger\Phi_0=v^2/2`$, and since $`A^U_\mu`$ below is Hermitian, the terms linear in $`\partial_\mu h`$ cancel:

```math
\begin{aligned}
D_\mu\Phi&=\frac{\partial_\mu h}v\,U\Phi_0-ig_{\mathrm{YM}}\Bigl(1+\frac hv\Bigr)UA^U_\mu\Phi_0,\\
A^U_\mu&:=U^\dagger A_\mu U+\frac i{g_{\mathrm{YM}}}U^\dagger\partial_\mu U,\\
(D_\mu\Phi)^\dagger D^\mu\Phi&=\frac12\partial_\mu h\,\partial^\mu h\\
&\quad+\Bigl(1+\frac hv\Bigr)^2g_{\mathrm{YM}}^2\,\Phi_0^\dagger A^U_\mu A^{U\mu}\Phi_0 .
\end{aligned}
```

Substituting (3.62) and (3.63) into (3.61),

```math
\boxed{
\begin{aligned}
\mathcal L={}&\frac12\partial_\mu h\,\partial^\mu h-\frac12m_h^2h^2\\
&-\lambda_Hv\,h^3-\frac{\lambda_H}4h^4+\frac{\lambda_Hv^4}4\\
&+\Bigl(1+\frac hv\Bigr)^2g_{\mathrm{YM}}^2\,\Phi_0^\dagger A^U_\mu A^{U\mu}\Phi_0\\
&-\frac14F_{\mu\nu}^aF^{a\mu\nu},\\
m_h^2={}&2\lambda_Hv^2=2\mu_H^2 .
\end{aligned}
}
```

Since $`U^\dagger\partial_\mu U=i\partial_\mu X+O(\theta\,\partial\theta)`$, to first order $`A^U_\mu=A_\mu-\partial_\mu X/g_{\mathrm{YM}}`$. As $`T^a\Phi_0=0`$ for $`a\ge2n`$, by (3.59) the quadratic part of $`g_{\mathrm{YM}}^2\Phi_0^\dagger A^U_\mu A^{U\mu}\Phi_0`$ is

```math
\begin{aligned}
&\Phi_0^\dagger\bigl(g_{\mathrm{YM}}A_\mu-\partial_\mu X\bigr)\bigl(g_{\mathrm{YM}}A^\mu-\partial^\mu X\bigr)\Phi_0\\
&\qquad=\frac12\sum_{a=1}^{2n-1}m_a^2\Bigl(A_\mu^a-\frac{\partial_\mu\theta^a}{g_{\mathrm{YM}}}\Bigr)\Bigl(A^{a\mu}-\frac{\partial^\mu\theta^a}{g_{\mathrm{YM}}}\Bigr),\\
&m_a^2:=2g_{\mathrm{YM}}^2\,\Phi_0^\dagger(G^a)^2\Phi_0>0 .
\end{aligned}
```

The $`A_\mu^a`$ with $`a\ge2n`$ do not appear in (3.65). Since $`U(\theta)\in U(n)`$, the gauge transformation (3.19)–(3.20) with $`U(\theta)^{-1}=U(\theta)^\dagger`$ gives

```math
\begin{aligned}
\Phi'&=U^\dagger\Phi=\Bigl(1+\frac hv\Bigr)\Phi_0,\\
A'_\mu&=U^\dagger A_\mu U-\frac i{g_{\mathrm{YM}}}\bigl(\partial_\mu U^\dagger\bigr)U=A^U_\mu,\\
F'_{\mu\nu}&=U^\dagger F_{\mu\nu}U .
\end{aligned}
```

By gauge invariance, $`\mathcal L`$ equals (3.64) with $`\theta^a=0`$ and $`A_\mu`$ replaced by $`A'_\mu`$. With (3.59),

```math
\boxed{
\begin{aligned}
\mathcal L={}&\frac12\partial_\mu h\,\partial^\mu h-\frac12m_h^2h^2\\
&-\lambda_Hv\,h^3-\frac{\lambda_H}4h^4+\frac{\lambda_Hv^4}4\\
&-\frac14F'^a_{\mu\nu}F'^{a\mu\nu}\\
&+\frac12\Bigl(1+\frac hv\Bigr)^2\sum_{a=1}^{2n-1}m_a^2A'^a_\mu A'^{a\mu} .
\end{aligned}
}
```

The $`\theta^a`$ no longer appear. To first order $`A'^a_\mu=A^a_\mu-\partial_\mu\theta^a/g_{\mathrm{YM}}`$ for $`a\le2n-1`$, so the quadratic part of the mass term in (3.67) is (3.65). Comparing with (1.85) and (1.135):

- the Higgs field $`h`$ has mass $`m_h`$ of (3.64);
- the $`2n-1`$ gauge fields $`A'^a_\mu`$, $`a\le2n-1`$, along the broken generators have masses $`m_a`$ of (3.65);
- the $`(n-1)^2`$ gauge fields $`A'^a_\mu`$, $`a\ge2n`$, along the unbroken generators are massless.

For $`n=2`$ and $`g_2=g_1=g_{\mathrm{YM}}`$, the $`m_a`$ are $`m_W`$, $`m_W`$ and $`m_Z`$ of (3.81).


<br><br>

