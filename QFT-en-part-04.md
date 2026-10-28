> English, part 4/4 · [Complete file](QFT.md) · [1](QFT-en-part-01.md) · [2](QFT-en-part-02.md) · [3](QFT-en-part-03.md) · [4](QFT-en-part-04.md)

<a id="lsz-reduction"></a>
### 6.5 LSZ Reduction Formula

**One-Particle Pole**

Consider a real scalar field with zero vacuum expectation value, an isolated stable one-particle pole of physical mass $`m_{\mathrm{phys}}>0`$, and nonzero overlap with that particle. Choose the particle-state phase so that

```math
\begin{aligned}
\langle\Omega|\hat\phi_H(0)|\mathbf p\rangle&=\sqrt{Z_{\mathrm{pole}}},\qquad Z_{\mathrm{pole}}>0,\qquad \langle\Omega|\Omega\rangle=1,\\
\widetilde G_2(p)&:=\int d^4x\,e^{ip\cdot x}G_2(x,0)
=\frac{iZ_{\mathrm{pole}}}{p^2-m_{\mathrm{phys}}^2+i\varepsilon}
+\text{terms regular at the pole}.
\end{aligned}
```

Here $`Z_{\mathrm{pole}}`$ is the pole residue for the chosen field normalization. Assume the corresponding asymptotic scattering states exist.

**Reduction Formula**

For $`r`$ incoming momenta $`p_a`$ and $`s`$ outgoing momenta $`q_b`$, all with positive physical energies, define $`\widetilde G_{r+s,\mathrm c}`$ by Fourier transforming every position with $`e^{+ik\cdot x}`$. For a connected scattering process with $`r+s>2`$,

```math
\boxed{\begin{aligned}
&i(2\pi)^4\delta^{(4)}\left(\sum_{b=1}^{s}q_b-\sum_{a=1}^{r}p_a\right)\mathcal M_{fi}\\
&\quad=\lim_{\mathrm{on\ shell}}
\left[\prod_{b=1}^{s}\frac{q_b^2-m_{\mathrm{phys}}^2}{i\sqrt{Z_{\mathrm{pole}}}}\right]
\left[\prod_{a=1}^{r}\frac{p_a^2-m_{\mathrm{phys}}^2}{i\sqrt{Z_{\mathrm{pole}}}}\right]
\widetilde G_{r+s,\mathrm c}(q_1,\ldots,q_s,-p_1,\ldots,-p_r).
\end{aligned}}
```

The limit means extracting the simultaneous external-pole residue with the Feynman prescription before taking all external momenta on shell. Each factor removes one external propagator and its field overlap. A field normalized to unit pole residue has $`Z_{\mathrm{pole}}=1`$.


<br><br>

<a id="cross-sections-and-decay-rates"></a>
### 6.6 Cross Sections and Decay Rates

**Phase Space and State Sums**

For total final momentum $`P`$ and $`n`$ on-shell outgoing momenta $`k_j`$,

```math
d\Phi_n(P;k_1,\ldots,k_n):=(2\pi)^4\delta^{(4)}\left(P-\sum_{j=1}^{n}k_j\right)
\prod_{j=1}^{n}\frac{d^3k_j}{(2\pi)^3\,2E_{\mathbf k_j}},\qquad
E_{\mathbf k_j}=\sqrt{\mathbf k_j^2+m_j^2}.
```

Use $`\overline{|\mathcal M|^2}`$ for the sum over unobserved final spins and internal quantum numbers, averaged over the equally populated initial states. For two unpolarized initial particles with $`N_1,N_2`$ such states,

```math
\overline{|\mathcal M|^2}:=\frac1{N_1N_2}\sum_{\text{initial, final states}}|\mathcal M|^2,
\qquad C_{\mathrm{id}}:=\prod_a\nu_a!.
```

Here $`\nu_a`$ is the number of identical final particles of species $`a`$. Divide by $`C_{\mathrm{id}}`$ when integrating the full phase space of labeled final momenta; omit this factor if the integration region already counts each physical final configuration once. Fixed initial polarizations are not averaged.

**Cross Sections and Decay Rates**

For $`1+2\to n`$ scattering and decay of a particle of mass $`M`$ at rest,

```math
\boxed{\begin{aligned}
d\sigma&=\frac{\overline{|\mathcal M|^2}}{4\sqrt{(p_1\cdot p_2)^2-m_1^2m_2^2}}\,\frac{d\Phi_n(p_1+p_2)}{C_{\mathrm{id}}},\\
d\Gamma&=\frac{\overline{|\mathcal M|^2}}{2M}\,\frac{d\Phi_n(P)}{C_{\mathrm{id}}},\qquad P=(M,\mathbf0).
\end{aligned}}
```

In the decay formula, average only over the parent's initial states if an unpolarized rate is intended. For two-body final states, use the single-particle three-momentum magnitudes $`|\mathbf p_1|`$ and $`|\mathbf k_1|`$ for the initial and final states in the center-of-mass frame:

```math
\begin{aligned}
\frac{d\sigma_{2\to2}}{d\Omega}
&=\frac1{64\pi^2s\,C_{\mathrm{id}}}\frac{|\mathbf k_1|}{|\mathbf p_1|}\,\overline{|\mathcal M|^2},\qquad s=(p_1+p_2)^2,\\
\frac{d\Gamma_{1\to2}}{d\Omega}
&=\frac{|\mathbf k_1|}{32\pi^2M^2\,C_{\mathrm{id}}}\,\overline{|\mathcal M|^2},\\
\Gamma_{1\to2}&=\frac{|\mathbf k_1|}{8\pi M^2\,C_{\mathrm{id}}}\,\overline{|\mathcal M|^2}\qquad\text{if the squared amplitude is angle independent}.
\end{aligned}
```

For the decay formulas, $`|\mathbf k_1|`$ is evaluated in the parent's rest frame. The solid-angle integrals use the same identical-particle counting convention as the full phase space.


<br><br>

<a id="qft-ch7"></a>
## 7. Renormalization

**Power Counting**

Square brackets here denote mass dimension. For canonical kinetic terms in $`d`$ spacetime dimensions,

```math
[\partial_\mu]=1,\qquad [\mathcal L]=d,\qquad
[\phi]=[A_\mu]=\frac{d-2}{2},\qquad [\psi]=\frac{d-1}{2},\qquad
[c_{\mathcal O}]=d-[\mathcal O].
```

For an interaction $`c_{\mathcal O}\mathcal O`$, $`[\mathcal O]<d`$, $`=d`$, and $`>d`$ define relevant, marginal, and irrelevant operators at the Gaussian fixed point. Quantum anomalous dimensions modify this classification at other fixed points.

For a connected graph built from scalar, vector, and ghost propagators behaving as $`k^{-2}`$ and spinor propagators behaving as $`k^{-1}`$,

```math
L=I_B+I_F-V+1,\qquad
\omega=dL-2I_B-I_F+\sum_v n_{\partial,v}.
```

Here $`L`$ counts loops, $`I_B,I_F`$ the respective internal lines, $`V`$ vertices, and $`n_{\partial,v}`$ derivatives at vertex $`v`$. The superficial degree $`\omega`$ counts simultaneous ultraviolet scaling; subdivergences and symmetry cancellations must be assessed separately.

**Dimensional Regularization and Counterterms**

Use $`d=4-\epsilon`$, with $`\epsilon`$ distinct from the Feynman $`\varepsilon`$. The renormalization scale is $`\mu`$:

```math
\int\frac{d^4k}{(2\pi)^4}\ \longrightarrow\
\int\frac{d^{4-\epsilon}k}{(2\pi)^{4-\epsilon}},\qquad
\frac{2}{\bar\epsilon}:=\frac{2}{\epsilon}-\gamma_E+\ln(4\pi).
```

For real $`\phi^4`$ theory, the bare field is $`\phi_0=Z_\phi^{1/2}\phi_R`$. One convenient counterterm parametrization is

```math
\begin{aligned}
\mathcal L&=\mathcal L_R+\mathcal L_{\mathrm{ct}},\\
\mathcal L_R&=\frac12\partial_\mu\phi_R\partial^\mu\phi_R
-\frac12m^2\phi_R^2-\frac{\mu^{\epsilon}\lambda}{4!}\phi_R^4,\\
\mathcal L_{\mathrm{ct}}&=\frac12\delta Z_\phi\partial_\mu\phi_R\partial^\mu\phi_R
-\frac12\delta m^2\phi_R^2-\frac{\mu^{\epsilon}\delta\lambda}{4!}\phi_R^4,
\qquad\delta Z_\phi=Z_\phi-1.
\end{aligned}
```

Here the factors of $`\mu`$ are carried by the couplings; no additional power of $`\mu`$ is included in each loop measure. Minimal subtraction (MS) removes pole terms; $`\overline{\mathrm{MS}}`$ also includes the displayed $`-\gamma_E+\ln4\pi`$ combination.

**Pole Mass and Field Normalization**

Defining the scalar self-energy by

```math
\widetilde G_{2,R}(p)=\frac{i}{p^2-m^2-\Sigma_R(p^2)+i\varepsilon},\qquad
\boxed{\Sigma_R(m^2)=0,\qquad \Sigma_R'(m^2)=0\quad\text{(on-shell scheme)},}
```

the on-shell scheme makes $`m`$ the mass of an isolated stable particle and fixes the propagator residue to one. In other schemes the renormalized mass need not equal the pole mass. The ultraviolet factor $`Z_\phi`$ is not generally the finite pole residue $`Z_{\mathrm{pole}}`$ of the renormalized interpolating field used in LSZ.

**Renormalization Group**

Derivatives are taken at fixed bare parameters:

```math
\begin{aligned}
\beta_\lambda&:=\left.\mu\frac{d\lambda}{d\mu}\right|_{\mathrm{bare}},\qquad
\beta_{m^2}:=\left.\mu\frac{dm^2}{d\mu}\right|_{\mathrm{bare}},\\
\gamma_\phi&:=\left.\frac12\mu\frac{d\ln Z_\phi}{d\mu}\right|_{\mathrm{bare}},\\
0&=\left[\mu\frac{\partial}{\partial\mu}
+\beta_\lambda\frac{\partial}{\partial\lambda}
+\beta_{m^2}\frac{\partial}{\partial m^2}+n\gamma_\phi\right]G_{n,R}.
\end{aligned}
```

This equation applies to renormalized elementary-field correlators at separated points; composite operators require their own renormalization. In four dimensions, the leading coefficients for real $`\phi^4`$ theory and for QCD with $`n_f`$ active Dirac quark flavors are

```math
\begin{aligned}
\beta_\lambda&=\frac{3\lambda^2}{16\pi^2}+O(\lambda^3),\\
\beta_{g_s}&=-\frac{g_s^3}{16\pi^2}\left(11-\frac23n_f\right)+O(g_s^5),
\qquad\alpha_s:=\frac{g_s^2}{4\pi},\\
\alpha_s(\mu)&=\frac{\alpha_s(\mu_0)}
{1+\dfrac{11-2n_f/3}{2\pi}\alpha_s(\mu_0)\ln(\mu/\mu_0)}
\quad\text{(one loop, fixed }n_f\text{)}.
\end{aligned}
```

The QCD result is perturbative and uses a mass-independent scheme with threshold matching when the active flavor content changes.

**Ward Identities and Anomalies**

For a vector-like Abelian theory with a symmetry-preserving regulator, let $`\Gamma^\mu`$ be the proper current vertex with the coupling stripped off, and let $`S_R(p)=i\mathcal S_R(p)`$ be the full fermion propagator. Then

```math
q_\mu\Gamma^\mu(p+q,p)
=\mathcal S_R^{-1}(p+q)-\mathcal S_R^{-1}(p),\qquad Z_1=Z_2.
```

Here $`Z_1`$ and $`Z_2`$ are the vertex and fermion-field renormalization constants. Non-Abelian gauge theories obey Slavnov--Taylor identities involving ghosts. A symmetry of the classical action may fail for the regulated quantum measure; gauge-anomaly cancellation is required for a consistent chiral gauge theory.

<br><br>

<a id="qed-renormalization"></a>
### 7.1 QED Renormalization

**Gauge-Fixed Lagrangian**

With the covariant gauge fixing of (6.15), the QED Lagrangian (3.26) for Dirac fields $`\psi_f`$ of charge $`Q_fe`$ and mass $`m_f`$ is

```math
\mathcal L
=\sum_f\bar\psi_f\bigl(i\gamma^\mu\partial_\mu-m_f\bigr)\psi_f
-\frac14F_{\mu\nu}F^{\mu\nu}
-\frac1{2\xi}(\partial_\mu A^\mu)^2
+eA_\mu\sum_fQ_f\,\bar\psi_f\gamma^\mu\psi_f .
```

The Faddeev--Popov ghosts decouple, as noted after (4.41).


**Feynman Rules**

The momentum-space factors contributing to $`i\mathcal M`$ are

```math
\begin{array}{l|l}
\text{element}&\text{factor}\\ \hline
\text{fermion propagator, momentum }p\text{ along the arrow}&\dfrac{i(\not p+m_f)}{p^2-m_f^2+i\varepsilon}\\[12pt]
\text{photon propagator}&\dfrac{-i}{p^2+i\varepsilon}\left[\eta_{\mu\nu}-(1-\xi)\dfrac{p_\mu p_\nu}{p^2+i\varepsilon}\right]\\[12pt]
\text{fermion-photon vertex}&ieQ_f\gamma^\mu\\[4pt]
\text{incoming / outgoing fermion}&u^s(p)\ /\ \bar u^s(p)\\
\text{incoming / outgoing antifermion}&\bar v^s(p)\ /\ v^s(p)\\
\text{incoming / outgoing photon}&\epsilon^r_\mu(p)\ /\ \epsilon^{r*}_\mu(p)
\end{array}
```

For the electron, $`Q_f=-1`$ and the vertex is $`-ie\gamma^\mu`$. Along each fermion line, write the factors in the order opposite to the arrow, so that the spinor indices form a matrix product. Impose four-momentum conservation at every vertex and integrate each loop momentum with $`\int d^4\ell/(2\pi)^4`$, continued to $`d`$ dimensions by (7.3). Each closed fermion loop gives a factor $`-1`$ and a Dirac trace; exchanging identical external fermions changes the sign, as in [Section 6.3](QFT-en-part-03.md#feynman-diagrams).

**Tree Level: $`e^+e^-\to q\bar q`$**

<p align="center"><img src="figures/ee-to-qqbar.svg" alt="Tree-level s-channel diagram for e+ e- to q qbar" width="440"></p>

Time runs from left to right. Arrows on the fermion lines show the fermion-number flow; grey arrows show the four-momenta.

Label the spins of $`e^-,e^+,q,\bar q`$ by $`s,s',r,r'`$ and the colors of $`q,\bar q`$ by $`c,c'\in\{1,2,3\}`$; the photon vertex is diagonal in color, and $`p_1+p_2=k_1+k_2`$. Reading each fermion line against its arrow with (7.10),

```math
\begin{aligned}
i\mathcal M
={}&\bigl[\bar v^{s'}(p_2)\,(-ie\gamma^\mu)\,u^s(p_1)\bigr]\,
\frac{-i}{(p_1+p_2)^2+i\varepsilon}
\left[\eta_{\mu\nu}-(1-\xi)\frac{(p_1+p_2)_\mu(p_1+p_2)_\nu}{(p_1+p_2)^2+i\varepsilon}\right]\\[6pt]
&\times\bigl[\bar u^r(k_1)\,(ieQ_q\gamma^\nu)\,v^{r'}(k_2)\bigr]\,\delta_{cc'} .
\end{aligned}
```


**Superficial Degree of Divergence**

For a connected QED graph, let $`V`$ be the number of vertices, $`I_\gamma,I_F`$ the numbers of internal photon and fermion lines, and $`E_\gamma,E_F`$ the numbers of external photon and fermion lines. Each vertex of (7.9) joins two fermion lines and one photon line and carries no derivative. Counting line ends and using (7.2) at $`d=4`$,

```math
\begin{aligned}
2V&=2I_F+E_F,\qquad V=2I_\gamma+E_\gamma,\qquad L=I_\gamma+I_F-V+1,\\[6pt]
\omega&=4L-2I_\gamma-I_F=2I_\gamma+3I_F-4V+4 .
\end{aligned}
```

Eliminating $`I_\gamma=\tfrac12(V-E_\gamma)`$ and $`I_F=V-\tfrac12E_F`$,

```math
\boxed{\omega=4-E_\gamma-\frac32E_F .}
```

The dependence on $`V`$ cancels because $`[e]=0`$ in four dimensions by (7.1).

**Two External Legs**

Every vertex conserves fermion number, so $`E_F`$ is even and two external legs means $`(E_F,E_\gamma)=(2,0)`$ or $`(0,2)`$. Let $`-i\Sigma(p)`$ and $`i\Pi^{\mu\nu}(p)`$ be the sums of amputated 1PI graphs with two external fermion lines and with two external photon lines, where $`p`$ is the external momentum.

**(1) Fermion Propagator**

```math
E_F=2,\qquad E_\gamma=0\qquad\Longrightarrow\qquad\omega=1 .
```

<p align="center"><img src="figures/fermion-self-energy.svg" alt="One-loop fermion self-energy" width="322"></p>

The one-loop graph of $`-i\Sigma(p)`$ for a fermion $`f`$: the internal fermion carries $`\ell`$ along its arrow and the photon carries $`p-\ell`$.

Let $`-i\Sigma_2(p)`$ be the $`O(e^2)`$ part of $`-i\Sigma(p)`$. Starting at the vertex $`\nu`$ and reading the line against the arrow with (7.10),

```math
\begin{aligned}
-i\Sigma_2(p)
=\int\frac{d^4\ell}{(2\pi)^4}\,
&(ieQ_f\gamma^\nu)\,\frac{i(\not\ell+m_f)}{\ell^2-m_f^2+i\varepsilon}\,(ieQ_f\gamma^\mu)\\[6pt]
&\times\frac{-i}{(p-\ell)^2+i\varepsilon}\left[\eta_{\mu\nu}-(1-\xi)\frac{(p-\ell)_\mu(p-\ell)_\nu}{(p-\ell)^2+i\varepsilon}\right].
\end{aligned}
```

For a quark, (7.15) multiplies the identity in color.

In $`d=4-\epsilon`$ dimensions, replace $`d^4\ell/(2\pi)^4`$ by $`d^d\ell/(2\pi)^d`$ as in (7.3), let the coupling carry the factor of $`\mu`$, $`e\to\mu^{\epsilon/2}e`$, as in (7.4), and continue the $`\gamma`$ matrices to $`d`$ dimensions with $`\{\gamma^\mu,\gamma^\nu\}=2\eta^{\mu\nu}I_4`$ and $`\eta^\mu{}_\mu=d`$. Collecting $`(ieQ_f)^2\,i\,(-i)=-e^2Q_f^2`$ and using $`\gamma^\nu\gamma_\nu=d\,I_4`$, $`\gamma^\nu\not a\gamma_\nu=-(d-2)\not a`$ and, for $`\ell=p-k`$, $`\not k(\not\ell+m_f)\not k=2(k\cdot p)\not k+k^2(m_f-\not p-\not k)`$, where $`k^2`$ cancels one factor $`\mathcal P_\gamma`$,

```math
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
```

Combine the denominators with a Feynman parameter $`x`$:

```math
\begin{aligned}
\frac{1}{\mathcal P_1\mathcal P_\gamma}
&=\int_0^1\frac{dx}{\bigl[x\mathcal P_\gamma+(1-x)\mathcal P_1\bigr]^2},\qquad
\frac{1}{\mathcal P_1\mathcal P_\gamma^2}
=\int_0^1\frac{2x\,dx}{\bigl[x\mathcal P_\gamma+(1-x)\mathcal P_1\bigr]^3},\\[6pt]
x\mathcal P_\gamma+(1-x)\mathcal P_1
&=(\ell-xp)^2-\Delta_{\Sigma,f}+i\varepsilon,\qquad
\Delta_{\Sigma,f}:=(1-x)\bigl(m_f^2-xp^2\bigr).
\end{aligned}
```

Shift $`\ell\to\ell+xp`$, so that $`k\to(1-x)p-\ell`$, drop the terms odd in $`\ell`$, and replace $`\ell^\mu\ell^\nu`$ by $`\eta^{\mu\nu}\ell^2/d`$. The numerators of (7.16) become

```math
\begin{aligned}
d\,m_f-(d-2)\not\ell\ &\to\ d\,m_f-(d-2)x\not p,\\[4pt]
m_f-\not p-\not k\ &\to\ m_f-(2-x)\not p,\\[4pt]
2(k\cdot p)\not k\ &\to\ 2(1-x)^2p^2\not p+2(p\cdot\ell)\not\ell
\ \to\ 2(1-x)^2p^2\not p+\frac2d\,\ell^2\not p,
\end{aligned}
```

so that

```math
\begin{aligned}
-i\Sigma_2(p)
={}&-\mu^{\epsilon}e^2Q_f^2\int_0^1dx\int\frac{d^d\ell}{(2\pi)^d}\,\biggl\{
\frac{d\,m_f-(d-2)x\not p-(1-\xi)\bigl[m_f-(2-x)\not p\bigr]}{\bigl(\ell^2-\Delta_{\Sigma,f}+i\varepsilon\bigr)^2}\\[6pt]
&-(1-\xi)\,\frac{2x\bigl[2(1-x)^2p^2+\frac2d\,\ell^2\bigr]\not p}{\bigl(\ell^2-\Delta_{\Sigma,f}+i\varepsilon\bigr)^3}\biggr\}.
\end{aligned}
```

After Wick rotation, for $`\Delta>0`$ and continued to $`\Delta<0`$ through $`\Delta-i\varepsilon`$, with $`n=2,3`$,

```math
\begin{aligned}
\int\frac{d^d\ell}{(2\pi)^d}\,\frac{1}{(\ell^2-\Delta+i\varepsilon)^n}
&=\frac{(-1)^n\,i}{(4\pi)^{d/2}}\,\frac{\Gamma\bigl(n-\frac d2\bigr)}{\Gamma(n)}\,(\Delta-i\varepsilon)^{\frac d2-n},\\[6pt]
\int\frac{d^d\ell}{(2\pi)^d}\,\frac{\ell^2}{(\ell^2-\Delta+i\varepsilon)^n}
&=\frac{(-1)^{n-1}\,i}{(4\pi)^{d/2}}\,\frac d2\,\frac{\Gamma\bigl(n-1-\frac d2\bigr)}{\Gamma(n)}\,(\Delta-i\varepsilon)^{\frac d2-n+1}.
\end{aligned}
```

Applying (7.20) to (7.19),

```math
\begin{aligned}
\Sigma_2(p)
={}&\frac{\mu^{\epsilon}e^2Q_f^2}{(4\pi)^{d/2}}\int_0^1dx\,\biggl\{
\Bigl[d\,m_f-(d-2)x\not p-(1-\xi)\bigl(m_f-2(1-x)\not p\bigr)\Bigr]\\[6pt]
&\times\Gamma\Bigl(2-\frac d2\Bigr)(\Delta_{\Sigma,f}-i\varepsilon)^{\frac d2-2}\\[6pt]
&+2(1-\xi)\,x(1-x)^2p^2\not p\;
\Gamma\Bigl(3-\frac d2\Bigr)(\Delta_{\Sigma,f}-i\varepsilon)^{\frac d2-3}\biggr\}.
\end{aligned}
```

With $`d=4-\epsilon`$, $`\Gamma(\epsilon/2)=2/\epsilon-\gamma_E+O(\epsilon)`$ and $`2/\bar\epsilon`$ from (7.3),

```math
\boxed{
\begin{aligned}
\Sigma_2(p)={}&\frac{e^2Q_f^2}{16\pi^2}\int_0^1dx\,\biggl\{
\Bigl[4m_f-2x\not p-(1-\xi)\bigl(m_f-2(1-x)\not p\bigr)\Bigr]
\left[\frac2{\bar\epsilon}-\ln\frac{\Delta_{\Sigma,f}-i\varepsilon}{\mu^2}\right]\\[6pt]
&-2m_f+2x\not p+\frac{2(1-\xi)\,x(1-x)\,p^2\not p}{m_f^2-xp^2-i\varepsilon}\biggr\}+O(\epsilon)\\[6pt]
={}&\frac{e^2Q_f^2}{16\pi^2}\,\frac2\epsilon\,\bigl[(3+\xi)m_f-\xi\not p\bigr]+(\text{finite as }\epsilon\to0).
\end{aligned}
}
```

**(2) Photon Propagator**

```math
E_\gamma=2,\qquad E_F=0\qquad\Longrightarrow\qquad\omega=2 .
```

<p align="center"><img src="figures/photon-self-energy.svg" alt="One-loop photon self-energy" width="298"></p>

The one-loop graph of $`i\Pi^{\mu\nu}(p)`$, with a closed loop of a fermion $`f`$: the loop momenta $`\ell+p`$ and $`\ell`$ run along the arrows.

Let $`i\Pi_2^{\mu\nu}(p)`$ be the $`O(e^2)`$ part of $`i\Pi^{\mu\nu}(p)`$. Starting at the vertex $`\mu`$ and reading the loop against the arrows with (7.10),

```math
\begin{aligned}
i\Pi_2^{\mu\nu}(p)
=\sum_fN_{\mathrm c,f}\,(-1)\int\frac{d^4\ell}{(2\pi)^4}\,
\mathop{\rm tr}\nolimits \biggl[
&(ieQ_f\gamma^\mu)\,\frac{i(\not\ell+m_f)}{\ell^2-m_f^2+i\varepsilon}\\[6pt]
&\times(ieQ_f\gamma^\nu)\,\frac{i(\not\ell+\not p+m_f)}{(\ell+p)^2-m_f^2+i\varepsilon}\biggr],
\end{aligned}
```

where the factor $`-1`$ and the Dirac trace come from the closed fermion loop, and $`N_{\mathrm c,f}`$ is the number of colors of $`f`$ ($`1`$ for a lepton, $`3`$ for a quark) from the color trace.

In $`d=4-\epsilon`$ dimensions, replace $`d^4\ell/(2\pi)^4`$ by $`d^d\ell/(2\pi)^d`$ as in (7.3) and let the coupling carry the factor of $`\mu`$, $`e\to\mu^{\epsilon/2}e`$, as in (7.4). Collecting $`(-1)(ieQ_f)^2i^2=-e^2Q_f^2`$ and using $`\mathop{\rm tr}\nolimits (\gamma^\mu\gamma^\nu)=4\eta^{\mu\nu}`$, $`\mathop{\rm tr}\nolimits (\gamma^\mu\gamma^\rho\gamma^\nu\gamma^\sigma)=4(\eta^{\mu\rho}\eta^{\nu\sigma}-\eta^{\mu\nu}\eta^{\rho\sigma}+\eta^{\mu\sigma}\eta^{\rho\nu})`$ and the vanishing of traces of an odd number of $`\gamma`$ matrices,

```math
\begin{aligned}
i\Pi_2^{\mu\nu}(p)
={}&-\mu^{\epsilon}e^2\sum_fN_{\mathrm c,f}Q_f^2\int\frac{d^d\ell}{(2\pi)^d}\,
\frac{\mathop{\rm tr}\nolimits \bigl[\gamma^\mu(\not\ell+m_f)\gamma^\nu(\not\ell+\not p+m_f)\bigr]}{\mathcal P_1\mathcal P_2}\\[6pt]
={}&-4\mu^{\epsilon}e^2\sum_fN_{\mathrm c,f}Q_f^2\int\frac{d^d\ell}{(2\pi)^d}\,\frac{1}{\mathcal P_1\mathcal P_2}\\
&\times\Bigl\{\ell^\mu(\ell+p)^\nu+\ell^\nu(\ell+p)^\mu-\eta^{\mu\nu}\bigl[\ell\cdot(\ell+p)-m_f^2\bigr]\Bigr\},\\[6pt]
\mathcal P_1:={}&\ell^2-m_f^2+i\varepsilon,\qquad
\mathcal P_2:=(\ell+p)^2-m_f^2+i\varepsilon .
\end{aligned}
```

Combine the denominators with a Feynman parameter $`x`$:

```math
\begin{aligned}
\frac{1}{\mathcal P_1\mathcal P_2}
&=\int_0^1\frac{dx}{\bigl[x\mathcal P_2+(1-x)\mathcal P_1\bigr]^2}
=\int_0^1\frac{dx}{\bigl[(\ell+xp)^2-\Delta_f+i\varepsilon\bigr]^2},\\[6pt]
\Delta_f&:=m_f^2-x(1-x)p^2 .
\end{aligned}
```

Shift $`\ell\to\ell-xp`$ and drop the terms odd in $`\ell`$, which integrate to zero; then replace $`\ell^\mu\ell^\nu`$ by $`\eta^{\mu\nu}\ell^2/d`$ under the integral. The numerator of (7.25) becomes

```math
\begin{aligned}
&\ell^\mu(\ell+p)^\nu+\ell^\nu(\ell+p)^\mu-\eta^{\mu\nu}\bigl[\ell\cdot(\ell+p)-m_f^2\bigr]\\[4pt]
&\quad\to\ 2\ell^\mu\ell^\nu-\eta^{\mu\nu}\ell^2-2x(1-x)p^\mu p^\nu+\eta^{\mu\nu}\bigl[x(1-x)p^2+m_f^2\bigr]\\[4pt]
&\quad\to\ 2x(1-x)\bigl(p^2\eta^{\mu\nu}-p^\mu p^\nu\bigr)+\eta^{\mu\nu}\Bigl[\frac{2-d}{d}\,\ell^2+\Delta_f\Bigr],
\end{aligned}
```

so that

```math
\begin{aligned}
i\Pi_2^{\mu\nu}(p)
={}&-4\mu^{\epsilon}e^2\sum_fN_{\mathrm c,f}Q_f^2\int_0^1dx\int\frac{d^d\ell}{(2\pi)^d}\,
\frac{1}{\bigl(\ell^2-\Delta_f+i\varepsilon\bigr)^2}\\[6pt]
&\times\Bigl\{2x(1-x)\bigl(p^2\eta^{\mu\nu}-p^\mu p^\nu\bigr)+\eta^{\mu\nu}\Bigl[\frac{2-d}{d}\,\ell^2+\Delta_f\Bigr]\Bigr\}.
\end{aligned}
```

After Wick rotation, for $`\Delta>0`$ and continued to $`\Delta<0`$ through $`\Delta-i\varepsilon`$,

```math
\begin{aligned}
\int\frac{d^d\ell}{(2\pi)^d}\,\frac{1}{(\ell^2-\Delta+i\varepsilon)^2}
&=\frac{i}{(4\pi)^{d/2}}\,\Gamma\Bigl(2-\frac d2\Bigr)(\Delta-i\varepsilon)^{\frac d2-2},\\[6pt]
\int\frac{d^d\ell}{(2\pi)^d}\,\frac{\ell^2}{(\ell^2-\Delta+i\varepsilon)^2}
&=-\frac{i}{(4\pi)^{d/2}}\,\frac d2\,\Gamma\Bigl(1-\frac d2\Bigr)(\Delta-i\varepsilon)^{\frac d2-1},\\[6pt]
\int\frac{d^d\ell}{(2\pi)^d}\,\frac{\frac{2-d}{d}\,\ell^2+\Delta}{(\ell^2-\Delta+i\varepsilon)^2}
&=\frac{i\,(\Delta-i\varepsilon)^{\frac d2-1}}{(4\pi)^{d/2}}\Bigl[\Bigl(\frac d2-1\Bigr)\Gamma\Bigl(1-\frac d2\Bigr)+\Gamma\Bigl(2-\frac d2\Bigr)\Bigr]=0,
\end{aligned}
```

where the last line uses $`\Gamma(2-\tfrac d2)=(1-\tfrac d2)\Gamma(1-\tfrac d2)`$. Only the transverse term of (7.28) survives:

```math
\begin{aligned}
i\Pi_2^{\mu\nu}(p)
={}&-4\mu^{\epsilon}e^2\sum_fN_{\mathrm c,f}Q_f^2\int_0^1dx\,2x(1-x)\bigl(p^2\eta^{\mu\nu}-p^\mu p^\nu\bigr)\\[6pt]
&\times\frac{i}{(4\pi)^{d/2}}\,\Gamma\Bigl(2-\frac d2\Bigr)(\Delta_f-i\varepsilon)^{\frac d2-2} .
\end{aligned}
```

With $`d=4-\epsilon`$, $`\Gamma(\epsilon/2)=2/\epsilon-\gamma_E+O(\epsilon)`$ and $`2/\bar\epsilon`$ from (7.3),

```math
\boxed{
\begin{aligned}
\Pi_2^{\mu\nu}(p)&=\bigl(p^2\eta^{\mu\nu}-p^\mu p^\nu\bigr)\,\Pi_2(p^2),\\[6pt]
\Pi_2(p^2)&=-\frac{e^2}{2\pi^2}\sum_fN_{\mathrm c,f}Q_f^2\int_0^1dx\,x(1-x)\left[\frac2{\bar\epsilon}-\ln\frac{\Delta_f-i\varepsilon}{\mu^2}\right]+O(\epsilon).
\end{aligned}
}
```

**Three External Legs**

Three external legs means $`(E_F,E_\gamma)=(2,1)`$ or $`(0,3)`$. Let $`ieQ_f\Gamma^\mu(p',p)`$ be the sum of amputated 1PI graphs with an incoming fermion of momentum $`p`$, an outgoing fermion of momentum $`p':=p+q`$, and an incoming photon of momentum $`q`$ and index $`\mu`$, so that $`\Gamma^\mu`$ is the proper vertex of (7.8). Write $`\Gamma^\mu=\gamma^\mu+\Lambda^\mu`$.

**(1) Vertex**

```math
E_F=2,\qquad E_\gamma=1\qquad\Longrightarrow\qquad\omega=0 .
```

<p align="center"><img src="figures/vertex.svg" alt="One-loop QED vertex" width="370"></p>

The one-loop graph of $`ieQ_f\Lambda^\mu(p',p)`$ for a fermion $`f`$: the internal fermions carry $`\ell`$ and $`\ell+q`$ along their arrows and the internal photon carries $`p-\ell`$.

Let $`\Lambda_2^\mu(p',p)`$ be the $`O(e^2)`$ part of $`\Lambda^\mu(p',p)`$. Starting at the vertex $`\nu`$ and reading the line against the arrow with (7.10),

```math
\begin{aligned}
ieQ_f\Lambda_2^\mu(p',p)
=\int\frac{d^4\ell}{(2\pi)^4}\,
&(ieQ_f\gamma^\nu)\,\frac{i(\not\ell+\not q+m_f)}{(\ell+q)^2-m_f^2+i\varepsilon}\,(ieQ_f\gamma^\mu)\\[6pt]
&\times\frac{i(\not\ell+m_f)}{\ell^2-m_f^2+i\varepsilon}\,(ieQ_f\gamma^\rho)\\[6pt]
&\times\frac{-i}{(p-\ell)^2+i\varepsilon}\left[\eta_{\nu\rho}-(1-\xi)\frac{(p-\ell)_\nu(p-\ell)_\rho}{(p-\ell)^2+i\varepsilon}\right].
\end{aligned}
```

For a quark, (7.33) multiplies the identity in color.

In $`d=4-\epsilon`$ dimensions, continue as for (7.16), with the stripped coupling $`ieQ_f`$ also carrying $`\mu^{\epsilon/2}`$. Collecting $`(ieQ_f)^3\,i\cdot i\cdot(-i)=(ieQ_f)(-ie^2Q_f^2)`$,

```math
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
```

Combine the denominators with Feynman parameters $`x,y,z`$:

```math
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
```

Shift $`\ell\to\ell+A`$, so that $`\ell'\to\ell+A'`$ and $`k\to K-\ell`$, with $`A:=(1-x)p-yp'`$, $`A':=(1-y)p'-xp`$ and $`K:=xp+yp'`$. Drop the terms odd in $`\ell`$ and replace $`\ell^\alpha\ell^\beta`$ by $`\eta^{\alpha\beta}\ell^2/d`$; with $`\not\ell\not\ell=\ell^2`$, the numerators of (7.34) become

```math
\begin{aligned}
\gamma^\nu(\not\ell'+m_f)\gamma^\mu(\not\ell+m_f)\gamma_\nu\ &\to\ \frac{(d-2)^2}{d}\,\ell^2\gamma^\mu+N^\mu,\\[4pt]
\not k(\not\ell'+m_f)\gamma^\mu(\not\ell+m_f)\not k\ &\to\ (\ell^2)^2\gamma^\mu+\ell^2N_2^\mu+N_0^\mu,\\[10pt]
N^\mu&:=\gamma^\nu(\not A'+m_f)\gamma^\mu(\not A+m_f)\gamma_\nu,\\[6pt]
N_0^\mu&:=\not K(\not A'+m_f)\gamma^\mu(\not A+m_f)\not K,\\[6pt]
N_2^\mu&:=-\gamma^\mu(\not A+m_f)\not K-\not K(\not A'+m_f)\gamma^\mu\\
&\quad\ +\frac1d\Bigl[N^\mu-(d-2)\not K\gamma^\mu\not K\\
&\qquad\quad-\gamma^\nu(\not A'+m_f)\gamma^\mu\gamma_\nu\not K-\not K\gamma^\nu\gamma^\mu(\not A+m_f)\gamma_\nu\Bigr],
\end{aligned}
```

so that

```math
\begin{aligned}
\Lambda_2^\mu(p',p)
={}&-i\mu^{\epsilon}e^2Q_f^2\int dF\int\frac{d^d\ell}{(2\pi)^d}\,\biggl\{
\frac{2\bigl[\frac{(d-2)^2}{d}\,\ell^2\gamma^\mu+N^\mu\bigr]}{\bigl(\ell^2-\Delta_{V,f}+i\varepsilon\bigr)^3}\\[6pt]
&-6(1-\xi)\,z\,\frac{(\ell^2)^2\gamma^\mu+\ell^2N_2^\mu+N_0^\mu}{\bigl(\ell^2-\Delta_{V,f}+i\varepsilon\bigr)^4}\biggr\}.
\end{aligned}
```

After Wick rotation, for $`\Delta>0`$ and continued to $`\Delta<0`$ through $`\Delta-i\varepsilon`$, the integrals (7.20) generalize to

```math
\int\frac{d^d\ell}{(2\pi)^d}\,\frac{(\ell^2)^a}{(\ell^2-\Delta+i\varepsilon)^n}
=\frac{(-1)^{n+a}\,i}{(4\pi)^{d/2}}\,
\frac{\Gamma\bigl(a+\frac d2\bigr)\,\Gamma\bigl(n-a-\frac d2\bigr)}{\Gamma\bigl(\frac d2\bigr)\,\Gamma(n)}\,
(\Delta-i\varepsilon)^{\frac d2+a-n}.
```

Applying (7.38) to (7.37),

```math
\begin{aligned}
\Lambda_2^\mu(p',p)
={}&\frac{\mu^{\epsilon}e^2Q_f^2}{(4\pi)^{d/2}}\int dF\,\biggl\{
\Bigl[\frac{(d-2)^2}{2}-(1-\xi)\,z\,\frac{d(d+2)}{4}\Bigr]
\Gamma\Bigl(2-\frac d2\Bigr)(\Delta_{V,f}-i\varepsilon)^{\frac d2-2}\,\gamma^\mu\\[6pt]
&-\Gamma\Bigl(3-\frac d2\Bigr)(\Delta_{V,f}-i\varepsilon)^{\frac d2-3}
\Bigl[N^\mu-(1-\xi)\,z\,\frac d2\,N_2^\mu\Bigr]\\[6pt]
&-(1-\xi)\,z\,\Gamma\Bigl(4-\frac d2\Bigr)(\Delta_{V,f}-i\varepsilon)^{\frac d2-4}\,N_0^\mu\biggr\}.
\end{aligned}
```

With $`d=4-\epsilon`$, $`\Gamma(\epsilon/2)=2/\epsilon-\gamma_E+O(\epsilon)`$, $`2/\bar\epsilon`$ from (7.3), and $`N^\mu`$, $`N_2^\mu`$ in the finite terms taken at $`d=4`$,

```math
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
```

The parameter integrals converge unless $`p^2=p'^2=m_f^2`$; in that on-shell case they diverge logarithmically at $`z\to1`$. With (7.22), the results satisfy $`q_\mu\Lambda_2^\mu(p+q,p)=\Sigma_2(p)-\Sigma_2(p+q)`$, as required by (7.8).

**(2) Three Photons**

```math
E_\gamma=3,\qquad E_F=0\qquad\Longrightarrow\qquad\omega=1 .
```

The graphs with the two orientations of the fermion loop cancel (Furry's theorem), so the sum of 1PI graphs with three external photons vanishes.

<br><br>





































<a id="qft-ch8"></a>
## 8. Multi-Loop Renormalization

**Subdivergences and the Forest Formula**

Beyond one loop, divergent subgraphs may be nested, disjoint, or overlapping. In massive BPHZ renormalization, with subtraction points chosen to avoid infrared singularities, let $`\mathcal I_{\mathcal G}`$ denote the integrand of a 1PI graph $`\mathcal G`$ and $`t_\gamma`$ the Taylor subtraction in the external momenta of a divergent 1PI subgraph $`\gamma`$, through its superficial degree. Then

```math
\boxed{R\mathcal I_{\mathcal G}
=\sum_{F\in\mathfrak F(\mathcal G)}
\left[\prod_{\gamma\in F}(-t_\gamma)\right]\mathcal I_{\mathcal G}.}
```

A forest $`F`$ contains only mutually nested or disjoint subtraction subgraphs. The sum includes the empty forest and, if divergent, the full graph. Nested subtractions act from the innermost subgraph outwards. Lower-order counterterm insertions are part of the higher-loop calculation.

**Pole Structure and Two-Loop Running**

For a multiplicative renormalization constant in a mass-independent minimal-subtraction scheme with a single coupling,

```math
Z=1+\sum_{L=1}^{\infty}
\left(\frac{g_s^2}{16\pi^2}\right)^L
\sum_{k=1}^{L}\frac{z_{Lk}}{\epsilon^k}.
```

Renormalization-group consistency relates higher poles to lower-order data. For QCD,

```math
\begin{aligned}
\beta_{g_s}&=-\frac{\beta_0g_s^3}{16\pi^2}
-\frac{\beta_1g_s^5}{(16\pi^2)^2}+O(g_s^7),\\
\beta_0&=11-\frac23n_f,\qquad
\beta_1=102-\frac{38}{3}n_f.
\end{aligned}
```

These first two coefficients are unchanged by analytic, scale-independent coupling redefinitions within the usual mass-independent schemes. Higher coefficients depend on the scheme.

**Integral Families and Integration by Parts**

For $`L`$ loop momenta $`k_\ell`$ and denominator factors $`D_j=q_j^2-m_j^2+i\varepsilon`$, where $`q_j`$ is a linear combination of loop and external momenta, define

```math
\begin{aligned}
I_{\nu_1\cdots\nu_N}
&:=\int\prod_{\ell=1}^{L}\frac{d^dk_\ell}{(2\pi)^d}
\prod_{j=1}^{N}D_j^{-\nu_j},\\
0&=\int\prod_{\ell=1}^{L}\frac{d^dk_\ell}{(2\pi)^d}
\frac{\partial}{\partial k_r^\mu}
\left(v^\mu\prod_{j=1}^{N}D_j^{-\nu_j}\right).
\end{aligned}
```

Here $`v^\mu`$ is a loop or external momentum. Integration-by-parts identities hold by analytic continuation in dimensional regularization from a region where the surface terms vanish. Numerator scalar products can be included through zero or negative powers in a completed integral family.

**Master Integrals and Differential Equations**

After algebraic reduction, a chosen family can be expressed in a finite basis of master integrals $`M_r`$. For a kinematic invariant $`s`$,

```math
I_{\nu_1\cdots\nu_N}=\sum_r c_r(d,\{p\cdot p\},\{m^2\})M_r,
\qquad
\frac{\partial M_r}{\partial s}=\sum_t A_{rt}(d,\{p\cdot p\},\{m^2\})M_t.
```

Boundary values and the Feynman analytic continuation are required to solve these equations. Ultraviolet and infrared poles must be distinguished before subtraction; a scaleless integral vanishes in dimensional regularization but may conceal a cancellation between ultraviolet and infrared poles. Higher-loop chiral calculations also require an explicit $`d`$-dimensional $`\gamma^5`$ prescription; the four-dimensional Weyl matrices alone do not supply one.

<br><br>

<a id="qft-ch9"></a>
## 9. Cosmology

