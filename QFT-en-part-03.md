> English, part 3/5 · [Complete file](QFT.md) · [1](QFT-en-part-01.md) · [2](QFT-en-part-02.md) · [3](QFT-en-part-03.md) · [4](QFT-en-part-04.md) · [5](QFT-en-part-05.md)

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

which reduces to the $`\hat U_I(t,0)`$ of (4.6) at $`t_0=0`$; when $`\hat H`$ has no explicit time dependence, $`\hat U_S(t,t_0)=e^{-i\hat H(t-t_0)}`$ by (2.4). Since $`[\hat V_I(t_1),\hat V_I(t_2)]\neq0`$ in general, case (3) of [Section 2.1](QFT-en-part-02.md#schrodinger-picture) applies, and by (2.11)

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

