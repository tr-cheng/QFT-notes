> English, part 2/5 · [Complete file](QFT.md) · [1](QFT-en-part-01.md) · [2](QFT-en-part-02.md) · [3](QFT-en-part-03.md) · [4](QFT-en-part-04.md) · [5](QFT-en-part-05.md)

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


The first viewpoint in [Section 1.4](QFT-en-part-01.md#classical-dynamics) naturally leads to Operator quantization: spatial position labels the degrees of freedom, while time remains the evolution parameter. 


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

Following the second viewpoint in [Section 1.4](QFT-en-part-01.md#classical-dynamics), $`t`$ is replaced by $`x^\mu`$.

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

