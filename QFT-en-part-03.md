> English, part 3/4 · [Complete file](QFT.md) · [1](QFT-en-part-01.md) · [2](QFT-en-part-02.md) · [3](QFT-en-part-03.md) · [4](QFT-en-part-04.md)

<a id="electroweak-gauge-theory"></a>
<a id="electroweak-theory"></a>
### 3.5 Electroweak Theory

<a id="sm-leptons"></a>
#### Leptons in the Standard Model

The gauge group of the electroweak theory is $`SU(2)_L\times U(1)_Y`$. On an $`SU(2)_L`$ doublet $`T^a:=\sigma^a/2`$, $`a=1,2,3`$; on an $`SU(2)_L`$ singlet $`T^a:=0`$. A field $`\psi`$ of hypercharge $`Y`$ transforms as

```math
\begin{aligned}
\psi'(x)&=e^{i\theta^a(x)T^a+i\theta_Y(x)Y}\,\psi(x),\qquad \theta^a(x),\ \theta_Y(x)\in\mathbb R,\\
Q&:=T^3+Y,
\end{aligned}
```

where $`Q`$ is the electric charge in units of $`e`$, as in (3.23).

The leptons come in three generations, labeled by the flavor index $`\alpha=e,\mu,\tau`$. With pairs denoting ($`SU(2)_L`$ representation, $`Y`$),

```math
\boxed{
\begin{aligned}
\ell_{\alpha L}&:=\begin{pmatrix}\nu_{\alpha L}\\ l_{\alpha L}\end{pmatrix}\sim\Bigl(\mathbf2,-\frac12\Bigr),\qquad
E_{\alpha R}\sim(\mathbf1,-1),\\
Q\,\nu_{\alpha L}&=0,\qquad Q\,l_{\alpha L}=-l_{\alpha L},\qquad Q\,E_{\alpha R}=-E_{\alpha R}.
\end{aligned}
}
```

The fields are four-component spinors with $`P_L\nu_{\alpha L}=\nu_{\alpha L}`$, $`P_Ll_{\alpha L}=l_{\alpha L}`$ and $`P_RE_{\alpha R}=E_{\alpha R}`$, where $`P_{L,R}`$ are given in (1.131). The leptons are color singlets. The minimal renormalizable Standard Model contains no right-handed neutrino.

<br><br>

<a id="electroweak-kinetic-terms"></a>
#### Kinetic Terms

Let $`W_\mu^a`$, $`a=1,2,3`$, and $`B_\mu`$ be the real $`SU(2)_L`$ and $`U(1)_Y`$ gauge fields, and $`g_2,g_1>0`$ the couplings. With $`U(\theta):=e^{i\theta^a(x)\sigma^a/2}`$ and $`W_\mu:=W_\mu^a\sigma^a/2`$, (3.19) with $`g_{\mathrm{YM}}\to g_2`$ and (3.24) with $`eQ\to g_1Y`$ give

```math
\boxed{
\begin{aligned}
D_\mu&:=\partial_\mu-ig_2W_\mu^aT^a-ig_1YB_\mu,\\
W_\mu'&=U(\theta)W_\mu U(\theta)^\dagger-\frac i{g_2}\bigl(\partial_\mu U(\theta)\bigr)U(\theta)^\dagger,\qquad
B_\mu'=B_\mu+\frac1{g_1}\partial_\mu\theta_Y,
\end{aligned}
}
```

so that $`D_\mu'\psi'=e^{i\theta^aT^a+i\theta_YY}D_\mu\psi`$ under (3.68). The field strengths are

```math
\begin{aligned}
W_{\mu\nu}^a&:=\partial_\mu W_\nu^a-\partial_\nu W_\mu^a+g_2\epsilon^{abc}W_\mu^bW_\nu^c,\qquad
B_{\mu\nu}:=\partial_\mu B_\nu-\partial_\nu B_\mu,\\
[D_\mu,D_\nu]&=-ig_2W_{\mu\nu}^aT^a-ig_1YB_{\mu\nu}.
\end{aligned}
```

On the lepton fields (3.69), the covariant derivative (3.70) is

```math
D_\mu\ell_{\alpha L}=\Bigl(\partial_\mu-ig_2W_\mu^a\frac{\sigma^a}2+\frac i2g_1B_\mu\Bigr)\ell_{\alpha L},\qquad
D_\mu E_{\alpha R}=\bigl(\partial_\mu+ig_1B_\mu\bigr)E_{\alpha R}.
```

The kinetic terms of the Lagrangian density are

```math
\boxed{
\begin{aligned}
\mathcal L_{\mathrm{kin}}
={}&-\frac14W_{\mu\nu}^aW^{a\mu\nu}-\frac14B_{\mu\nu}B^{\mu\nu}\\
&+\sum_{\alpha=e,\mu,\tau}\Bigl(\overline{\ell_{\alpha L}}\,i\gamma^\mu D_\mu\ell_{\alpha L}
+\overline{E_{\alpha R}}\,i\gamma^\mu D_\mu E_{\alpha R}\Bigr).
\end{aligned}
}
```

By (3.20), (3.24) and (3.70), $`\mathcal L_{\mathrm{kin}}`$ is gauge invariant.

<br><br>

<a id="charged-lepton-masses"></a>
#### Yukawa Couplings and Charged-Lepton Masses

The Higgs doublet $`H=:(H^+,H^0)^T\sim(\mathbf2,\frac12)`$ is a color singlet. It is the $`\Phi`$ of (3.52) with $`n=2`$ and $`\mu_H^2>0`$, with $`\partial_\mu`$ replaced by (3.70). As $`\theta^a`$ and $`\theta_Y`$ vary, $`e^{i\theta^a\sigma^a/2+i\theta_Y/2}`$ covers $`U(2)`$, so by (3.56), (3.60) and (3.66)

```math
\begin{aligned}
\mathcal L_H&=(D_\mu H)^\dagger D^\mu H-V(H),\qquad
V(H)=-\mu_H^2H^\dagger H+\lambda_H(H^\dagger H)^2,\\
\langle H\rangle&=\frac1{\sqrt2}\begin{pmatrix}0\\v\end{pmatrix},\qquad Q\langle H\rangle=0,\qquad
H\big|_{\mathrm{unitary\ gauge}}=\frac1{\sqrt2}\begin{pmatrix}0\\v+h\end{pmatrix}.
\end{aligned}
```

The Higgs field $`h`$ has the mass $`m_h`$ of (3.64).

Let $`y_l`$ be a complex $`3\times3`$ matrix; repeated flavor indices $`\alpha,\beta`$ are summed. The lepton Yukawa coupling is invariant under (3.68):

```math
\begin{aligned}
\mathcal L_Y^\ell&=-\overline{\ell_{\alpha L}}\,(y_l)_{\alpha\beta}\,H\,E_{\beta R}+\mathrm{h.c.},\qquad
\overline{\ell_{\alpha L}}H=\overline{\nu_{\alpha L}}H^++\overline{l_{\alpha L}}H^0,\\
\overline{\ell_{\alpha L}'}H'E_{\beta R}'
&=\overline{\ell_{\alpha L}}\,e^{\frac i2\theta_Y}U(\theta)^\dagger\;e^{\frac i2\theta_Y}U(\theta)H\;e^{-i\theta_Y}E_{\beta R}
=\overline{\ell_{\alpha L}}HE_{\beta R}.
\end{aligned}
```

In the unitary gauge (3.74), $`H^+=0`$ and

```math
\mathcal L_Y^\ell=-\Bigl(1+\frac hv\Bigr)\overline{l_{\alpha L}}\,(M_l)_{\alpha\beta}\,E_{\beta R}+\mathrm{h.c.},\qquad
M_l:=\frac v{\sqrt2}\,y_l .
```

The neutrinos $`\nu_{\alpha L}`$ do not appear in (3.76).

**Flavor Basis**

Write $`\ell_L:=(\ell_{eL},\ell_{\mu L},\ell_{\tau L})^T`$ and $`E_R:=(E_{eR},E_{\mu R},E_{\tau R})^T`$ in flavor space. For constant $`R_\ell,R_E\in U(3)`$, (3.73) is invariant under the change of basis in the first line below, and the singular value decomposition of $`M_l`$ fixes $`R_\ell`$ and $`R_E`$ by the second line:

```math
\begin{aligned}
\ell_L&\to R_\ell\,\ell_L,\qquad E_R\to R_E\,E_R,\qquad y_l\to R_\ell^\dagger\,y_l\,R_E,\\
R_\ell^\dagger M_lR_E&=\mathop{\rm diag}\nolimits (m_e,m_\mu,m_\tau),\qquad m_\alpha\ge0 .
\end{aligned}
```

From now on we use this basis. With the Dirac fields $`l_\alpha:=l_{\alpha L}+E_{\alpha R}`$, (3.76) becomes

```math
\boxed{
\begin{aligned}
M_l&=\mathop{\rm diag}\nolimits (m_e,m_\mu,m_\tau),\\
\mathcal L_Y^\ell&=-\sum_{\alpha=e,\mu,\tau}m_\alpha\Bigl(1+\frac hv\Bigr)\bar l_\alpha l_\alpha .
\end{aligned}
}
```

Since $`\overline{l_{\alpha L}}\,i\gamma^\mu\partial_\mu l_{\alpha L}+\overline{E_{\alpha R}}\,i\gamma^\mu\partial_\mu E_{\alpha R}=\bar l_\alpha\,i\gamma^\mu\partial_\mu l_\alpha`$, the free part of (3.73) and (3.78) contain the Dirac Lagrangian (1.94) of each $`l_\alpha`$ with mass $`m_\alpha`$. Thus the charged leptons $`l_e,l_\mu,l_\tau`$ are Dirac fields of masses $`m_e,m_\mu,m_\tau`$, coupled to $`h`$ with strength $`m_\alpha/v`$, while the neutrinos $`\nu_{\alpha L}`$ remain massless.

<br><br>

<a id="gauge-boson-masses"></a>
#### Gauge-Boson Masses

Substituting the unitary-gauge $`H`$ of (3.74) into (3.70), with $`T^a=\sigma^a/2`$ and $`Y=\frac12`$,

```math
\begin{aligned}
D_\mu H&=\frac1{\sqrt2}\begin{pmatrix}-\frac i2g_2\bigl(W_\mu^1-iW_\mu^2\bigr)(v+h)\\ \partial_\mu h+\frac i2\bigl(g_2W_\mu^3-g_1B_\mu\bigr)(v+h)\end{pmatrix},\\
(D_\mu H)^\dagger D^\mu H&=\frac12\partial_\mu h\,\partial^\mu h
+\frac{(v+h)^2}8\Bigl[g_2^2\bigl(W_\mu^1W^{1\mu}+W_\mu^2W^{2\mu}\bigr)\\
&\qquad+\bigl(g_2W_\mu^3-g_1B_\mu\bigr)\bigl(g_2W^{3\mu}-g_1B^\mu\bigr)\Bigr].
\end{aligned}
```

Define

```math
\begin{aligned}
W_\mu^\pm&:=\frac{W_\mu^1\mp iW_\mu^2}{\sqrt2},\qquad
\tan\theta_W:=\frac{g_1}{g_2},\qquad
s_W:=\sin\theta_W,\qquad c_W:=\cos\theta_W,\\
Z_\mu&:=c_WW_\mu^3-s_WB_\mu,\qquad
A_\mu^{\mathrm{em}}:=s_WW_\mu^3+c_WB_\mu,\qquad
e:=g_2s_W=g_1c_W .
\end{aligned}
```

Then $`W_\mu^1W^{1\mu}+W_\mu^2W^{2\mu}=2W_\mu^+W^{-\mu}`$ and $`g_2W_\mu^3-g_1B_\mu=\sqrt{g_2^2+g_1^2}\,Z_\mu`$, so

```math
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
```

$`A_\mu^{\mathrm{em}}`$ does not appear in (3.81).

<br><br>

<a id="sm-quarks"></a>
#### Quarks

The quarks come in three generations, $`r=1,2,3`$, and are color triplets as in (3.32). With the pairs as in (3.69),

```math
\begin{aligned}
q_{rL}&:=\begin{pmatrix}u_{rL}\\ d_{rL}\end{pmatrix}\sim\Bigl(\mathbf2,\frac16\Bigr),\qquad
u_{rR}\sim\Bigl(\mathbf1,\frac23\Bigr),\qquad
d_{rR}\sim\Bigl(\mathbf1,-\frac13\Bigr),\\
Q\,u_{rL}&=\frac23u_{rL},\qquad Q\,d_{rL}=-\frac13d_{rL}.
\end{aligned}
```

With $`D_\mu`$ of (3.70) plus the gluon term $`-ig_sA_\mu`$ of (3.36), the quark kinetic terms are

```math
\mathcal L_{\mathrm{kin}}^q=\sum_{r=1}^3\Bigl(\overline{q_{rL}}\,i\gamma^\mu D_\mu q_{rL}
+\overline{u_{rR}}\,i\gamma^\mu D_\mu u_{rR}
+\overline{d_{rR}}\,i\gamma^\mu D_\mu d_{rR}\Bigr).
```

Let $`y_u,y_d`$ be complex $`3\times3`$ matrices, $`H^c:=i\sigma^2H^*\sim(\mathbf2,-\frac12)`$, and $`u_L:=(u_{1L},u_{2L},u_{3L})^T`$, and similarly $`u_R`$, $`d_L`$, $`d_R`$, in flavor space. Summing over $`r,s`$, the quark Yukawa couplings are gauge invariant, and in the unitary gauge (3.74)

```math
\begin{aligned}
\mathcal L_Y^q&=-\overline{q_{rL}}\,(y_d)_{rs}\,H\,d_{sR}-\overline{q_{rL}}\,(y_u)_{rs}\,H^c\,u_{sR}+\mathrm{h.c.},\qquad
H^c\big|_{\mathrm{unitary\ gauge}}=\frac1{\sqrt2}\begin{pmatrix}v+h\\0\end{pmatrix},\\
\mathcal L_Y^q&=-\Bigl(1+\frac hv\Bigr)\bigl(\overline{u_L}\,M_u\,u_R+\overline{d_L}\,M_d\,d_R\bigr)+\mathrm{h.c.},\qquad
M_{u,d}:=\frac v{\sqrt2}\,y_{u,d}.
\end{aligned}
```

**Mass Basis and CKM Matrix**

With unitary $`R_{uL},R_{uR},R_{dL},R_{dR}`$ chosen by the singular value decompositions of $`M_u`$ and $`M_d`$, define the mass-basis fields $`u'`$, $`d'`$ by

```math
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
```

with $`m_f\ge0`$; the $`q_f`$ are the quark fields of (3.32), and the $`m_f`$ are the masses in (3.45).

<br><br>

<a id="electroweak-currents"></a>
#### Charged and Neutral Currents

The gauge-field terms of $`\bar\psi\,i\gamma^\mu D_\mu\psi`$ are $`\bar\psi\gamma^\mu(g_2W_\mu^aT^a+g_1YB_\mu)\psi`$. By (3.80), with $`T^\pm:=T^1\pm iT^2`$,

```math
g_2W_\mu^aT^a+g_1YB_\mu
=\frac{g_2}{\sqrt2}\bigl(W_\mu^+T^++W_\mu^-T^-\bigr)
+eQA_\mu^{\mathrm{em}}
+\frac{g_2}{c_W}\bigl(T^3-s_W^2Q\bigr)Z_\mu .
```

Since $`\overline{\ell_{\alpha L}}\gamma^\mu T^+\ell_{\alpha L}=\overline{\nu_{\alpha L}}\gamma^\mu l_{\alpha L}`$ and, by (3.85), $`\overline{q_{rL}}\gamma^\mu T^+q_{rL}=\overline{u_L}\gamma^\mu d_L=\overline{u_L'}\gamma^\mu V_{\mathrm{CKM}}\,d_L'`$, the $`W_\mu^\pm`$ terms of (3.73) and (3.83) are, with $`q_{fL}:=P_Lq_f`$ and the rows and columns of $`V:=V_{\mathrm{CKM}}`$ labeled by $`f=u,c,t`$ and $`f'=d,s,b`$,

```math
\boxed{
\mathcal L_{\mathrm{CC}}
=\frac{g_2}{\sqrt2}\,W_\mu^+\Bigl(\sum_{\alpha=e,\mu,\tau}\overline{\nu_{\alpha L}}\gamma^\mu l_{\alpha L}
+\sum_{f=u,c,t}\ \sum_{f'=d,s,b}V_{ff'}\,\overline{q_{fL}}\gamma^\mu q_{f'L}\Bigr)+\mathrm{h.c.}
}
```

Let $`\psi_f`$ be the field of the fermion $`f`$ of (3.23) in the bases (3.77) and (3.85): $`\psi_f=q_f`$ for the quarks, $`\psi_f=l_f`$ for $`f=e,\mu,\tau`$, and $`\psi_{\nu_\alpha}=\nu_{\alpha L}`$. Let $`T_f^3`$ be $`T^3`$ of its left-handed part: $`+\frac12`$ for $`q_u,q_c,q_t`$ and $`\nu_{\alpha L}`$, and $`-\frac12`$ for $`q_d,q_s,q_b`$ and $`l_\alpha`$. The $`A_\mu^{\mathrm{em}}`$ and $`Z_\mu`$ terms are

```math
\boxed{
\begin{aligned}
\mathcal L_{\mathrm{NC}}
={}&eA_\mu^{\mathrm{em}}\sum_fQ_f\,\bar\psi_f\gamma^\mu\psi_f\\
&+\frac{g_2}{c_W}Z_\mu\sum_f\bar\psi_f\gamma^\mu\bigl(T_f^3P_L-Q_fs_W^2\bigr)\psi_f .
\end{aligned}
}
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
\begin{aligned}
L:\mathbb R^n\times\mathbb R^n&\to\mathbb R,\\
(x,y)&\mapsto\sum_{a=1}^n\frac12m_ay_a^2-V(x),
\end{aligned}
```

in which $`m_a>0`$ and $`V:\mathbb R^n\to\mathbb R`$ is smooth.

- **Paths**: for $`t_i<t_f`$,

```math
\begin{aligned}
C:[t_i,t_f]&\to\mathrm{Conf},\\
t&\mapsto C(t).
\end{aligned}
```

- **Action**: the functional on paths

```math
\begin{aligned}
S:\{\text{paths}\}&\to\mathbb R,\\
C&\mapsto S[C]:=\int_{t_i}^{t_f}dt\,L\bigl(C(t),\dot C(t)\bigr).
\end{aligned}
```

**Quantization**

- **Initial configuration**:

```math
\begin{aligned}
Q_i:\{t_i\}&\to\mathrm{Conf},\\
t_i&\mapsto q_i.
\end{aligned}
```

- **Final configuration**:

```math
\begin{aligned}
Q_f:\{t_f\}&\to\mathrm{Conf},\\
t_f&\mapsto q_f.
\end{aligned}
```

- **Transition kernel**: the integral over the paths with these endpoints,

```math
\boxed{K(Q_f,Q_i):=\int_{C(t_i)=Q_i(t_i)}^{C(t_f)=Q_f(t_f)}\mathcal DC\,e^{iS[C]},}
```

also written $`\int_{Q_i}^{Q_f}\mathcal DC\,e^{iS[C]}`$.

**Exact Definition of the Transition Kernel**

Divide $`[t_i,t_f]`$ into $`N+1`$ steps.

- **Measure**:

```math
\begin{gathered}
\Delta t:=\frac{t_f-t_i}{N+1},\qquad t_k:=t_i+k\,\Delta t\quad(k=0,\ldots,N+1),\\
\mathcal DC:=\lim_{N\to\infty}\mathcal N_N\prod_{k=1}^Nd^nC(t_k),\qquad
\mathcal N_N:=\prod_{a=1}^n\Bigl(\frac{m_a}{2\pi i\,\Delta t}\Bigr)^{\frac{N+1}{2}},
\end{gathered}
```

so that $`t_0=t_i`$ and $`t_{N+1}=t_f`$, with $`d^nC(t_k):=\prod_{a=1}^ndC_a(t_k)`$.

- **Action**:

```math
S[C]=\lim_{N\to\infty}\Delta t\sum_{k=0}^NL\Bigl(C(t_k),\frac{C(t_{k+1})-C(t_k)}{\Delta t}\Bigr).
```

Thus (4.6) means

```math
\boxed{
K(Q_f,Q_i)=\lim_{N\to\infty}\mathcal N_N\int\prod_{k=1}^Nd^nC(t_k)\,
\exp\biggl[i\,\Delta t\sum_{k=0}^NL\Bigl(C(t_k),\frac{C(t_{k+1})-C(t_k)}{\Delta t}\Bigr)\biggr],}
```

with $`C(t_0):=q_i`$, $`C(t_{N+1}):=q_f`$, and each $`C(t_k)`$, $`1\le k\le N`$, integrated over $`\mathrm{Conf}`$.

**Functional Derivative**

For a source $`J:[t_i,t_f]\to\mathbb R^n`$, with $`J\cdot C:=\sum_{a=1}^nJ_aC_a`$,

```math
K^J(Q_f,Q_i):=\int_{Q_i}^{Q_f}\mathcal DC\,\exp\Bigl(i\int_{t_i}^{t_f}dt\,\bigl[L\bigl(C(t),\dot C(t)\bigr)+J(t)\cdot C(t)\bigr]\Bigr).
```

In the sliced form (4.9) the source adds $`i\,\Delta t\sum_{k=0}^NJ(t_k)\cdot C(t_k)`$ to the exponent, so $`J`$ enters only through $`J(t_0),\ldots,J(t_N)`$. For $`t_i<t<t_f`$ define

```math
\frac{\delta}{\delta J_a(t)}:=\lim_{N\to\infty}\frac{1}{\Delta t}\frac{\partial}{\partial J_a(t_k)},\qquad t_k\to t.
```

Writing $`L_j:=L\bigl(C(t_j),[C(t_{j+1})-C(t_j)]/\Delta t\bigr)`$,

```math
\begin{aligned}
\frac{\delta}{\delta J_a(t)}K^J(Q_f,Q_i)
&=\lim_{N\to\infty}\mathcal N_N\int\prod_{j=1}^Nd^nC(t_j)\,
\frac{1}{\Delta t}\frac{\partial}{\partial J_a(t_k)}\exp\biggl[i\,\Delta t\sum_{j=0}^N\bigl(L_j+J(t_j)\cdot C(t_j)\bigr)\biggr]\\
&=\lim_{N\to\infty}\mathcal N_N\int\prod_{j=1}^Nd^nC(t_j)\,
iC_a(t_k)\exp\biggl[i\,\Delta t\sum_{j=0}^N\bigl(L_j+J(t_j)\cdot C(t_j)\bigr)\biggr]\\
&=\int_{Q_i}^{Q_f}\mathcal DC\,iC_a(t)\exp\Bigl(i\int_{t_i}^{t_f}dt'\,\bigl[L\bigl(C(t'),\dot C(t')\bigr)+J(t')\cdot C(t')\bigr]\Bigr).
\end{aligned}
```


**Example: Free Particle in One Dimension**

Take $`n=1`$, $`V=0`$ in (4.1):

```math
L(x,y)=\frac12my^2,\qquad Q_i(t_i)=q_i,\qquad Q_f(t_f)=q_f.
```

By (4.7)–(4.9), with $`C(t_0)=q_i`$, $`C(t_{N+1})=q_f`$ and $`\mathcal N_N=\bigl(\frac{m}{2\pi i\,\Delta t}\bigr)^{\frac{N+1}{2}}`$,

```math
\begin{aligned}
K(Q_f,Q_i)&=\int_{Q_i}^{Q_f}\mathcal DC\,e^{i\int_{t_i}^{t_f}dt\,\frac12m\dot C^2}\\
&=\lim_{N\to\infty}\mathcal N_N\int\prod_{k=1}^{N}dC(t_k)\,e^{\frac{i}{\Delta t}\sum_{k=0}^{N}\frac12m\left(C(t_{k+1})-C(t_k)\right)^2}\\
&=\lim_{N\to\infty}\mathcal N_N\int\prod_{k=1}^{N}dC(t_k)\,
e^{\frac{i}{\Delta t}\left[\frac12mq_i^2+\frac12mq_f^2+mC^2(t_1)+\cdots+mC^2(t_N)\right]}\,
e^{\frac{i}{\Delta t}(-m)\left[q_iC(t_1)+C(t_1)C(t_2)+\cdots+C(t_N)q_f\right]}.
\end{aligned}
```

Integrate $`C(t_1)`$, using $`\int_{-\infty}^{\infty}dx\,e^{iax^2}=\sqrt{\pi i/a}`$ for $`a>0`$ ($`a\to a+i\varepsilon`$, $`\varepsilon\to0^+`$):

```math
\begin{aligned}
\int dC(t_1)\,e^{\frac{i}{\Delta t}\left[mC^2(t_1)-mC(t_1)\left(q_i+C(t_2)\right)\right]}
&=\int dC(t_1)\,e^{\frac{im}{\Delta t}\left(C(t_1)-\frac{q_i+C(t_2)}{2}\right)^2}\,e^{-\frac{im}{4\Delta t}\left(q_i+C(t_2)\right)^2}\\
&=\sqrt{\frac{2\pi i\,\Delta t}{m}\cdot\frac12}\;e^{-\frac{im}{4\Delta t}\left(q_i+C(t_2)\right)^2}.
\end{aligned}
```

After $`C(t_1),\ldots,C(t_{j-1})`$, $`1\le j\le N`$:

```math
K(Q_f,Q_i)=\lim_{N\to\infty}\mathcal N_N\Bigl(\frac{2\pi i\,\Delta t}{m}\Bigr)^{\frac{j-1}{2}}\frac{1}{\sqrt j}
\int\prod_{k=j}^{N}dC(t_k)\,
e^{\frac{im}{2\Delta t}\left[\frac{\left(C(t_j)-q_i\right)^2}{j}+C^2(t_j)+2C^2(t_{j+1})+\cdots+2C^2(t_N)+q_f^2\right]}\,
e^{\frac{im}{2\Delta t}(-2)\left[C(t_j)C(t_{j+1})+\cdots+C(t_N)q_f\right]}.
```

Integrate $`C(t_j)`$:

```math
\begin{aligned}
\frac{\left(C(t_j)-q_i\right)^2}{j}+C^2(t_j)-2C(t_j)C(t_{j+1})
&=\frac{j+1}{j}\Bigl(C(t_j)-\frac{q_i+jC(t_{j+1})}{j+1}\Bigr)^2+\frac{\left(C(t_{j+1})-q_i\right)^2}{j+1}-C^2(t_{j+1}),\\
\int dC(t_j)\,e^{\frac{im}{2\Delta t}\frac{j+1}{j}\left(C(t_j)-\frac{q_i+jC(t_{j+1})}{j+1}\right)^2}
&=\sqrt{\frac{2\pi i\,\Delta t}{m}\cdot\frac{j}{j+1}},
\end{aligned}
```

which gives (4.16) with $`j+1`$; for $`j=N`$, $`C(t_{N+1})=q_f`$ and the bracket becomes $`\frac{(q_f-q_i)^2}{N+1}`$. Hence, with $`(N+1)\Delta t=t_f-t_i`$,

```math
\begin{aligned}
K(Q_f,Q_i)&=\lim_{N\to\infty}\Bigl(\frac{m}{2\pi i\,\Delta t}\Bigr)^{\frac{N+1}{2}}\Bigl(\frac{2\pi i\,\Delta t}{m}\Bigr)^{\frac N2}\frac{1}{\sqrt{N+1}}\,
e^{\frac{im\left(q_f-q_i\right)^2}{2(N+1)\Delta t}}\\
&=\boxed{\sqrt{\frac{m}{2\pi i\,(t_f-t_i)}}\;e^{\frac{im\left(q_f-q_i\right)^2}{2(t_f-t_i)}}.}
\end{aligned}
```

This example shows why the prefactor $`\mathcal N_N`$ is included in the definition (4.7) of the path integral. The result (4.18) is finite, while by its definition $`\mathcal N_N`$ diverges as $`N\to\infty`$; without the prefactor, the remaining factor $`\bigl(\frac{2\pi i\,\Delta t}{m}\bigr)^{\frac N2}\frac{1}{\sqrt{N+1}}`$ in (4.18) tends to zero, and so would $`K(Q_f,Q_i)`$.

**Relation to Operator Quantization**

Let $`\hat H:=\sum_{a=1}^n\hat p_a^2/(2m_a)+V(\hat q)`$ with $`[\hat q_a,\hat p_b]=i\delta_{ab}`$ and $`\hat q_a|q\rangle=q_a|q\rangle`$, and let $`\hat U(t_f,t_i)=e^{-i\hat H(t_f-t_i)}`$ be its evolution operator (2.21). Then, with $`q_i=Q_i(t_i)`$ and $`q_f=Q_f(t_f)`$,

```math
\boxed{K(Q_f,Q_i)=\langle q_f|\hat U(t_f,t_i)|q_i\rangle=\langle q_f,t_f|q_i,t_i\rangle}
```

in the Schrödinger and Heisenberg pictures respectively, where $`|q,t\rangle:=\hat U(t,0)^\dagger|q\rangle`$ satisfies $`\hat q_H(t)|q,t\rangle=q\,|q,t\rangle`$ by (2.22).

<br><br>

<a id="path-integrals-in-field-theory"></a>
### 4.2 Path Integrals in Quantum Field Theory

Following the second viewpoint in [Section 1.4](QFT-en-part-01.md#classical-dynamics), $`t`$ is replaced by $`x^\mu`$.

**Principle**

- **Configuration space**: $`\mathrm{Conf}=\mathbb R^n`$.
- **Dynamical structure**: the Lagrangian density

```math
\begin{aligned}
\mathcal L:\mathbb R^n\times(\mathbb R^n)^4&\to\mathbb R,\\
(x,y^\mu)&\mapsto\sum_{a=1}^n\frac12y_a^\mu y_{a\mu}-V(x),
\end{aligned}
```

in which $`y^\mu\in\mathbb R^n`$, $`\mu=0,\ldots,3`$, and $`V:\mathbb R^n\to\mathbb R`$ is smooth.

- **Paths**: for $`t_i<t_f`$,

```math
\begin{aligned}
\phi:[t_i,t_f]\times\mathbb R^3&\to\mathrm{Conf},\\
x&\mapsto\phi(x),
\end{aligned}
```

with $`\phi(t):=\phi(t,\cdot\,)`$ the configuration at time $`t`$.

- **Action**: the functional on paths

```math
\begin{aligned}
S:\{\text{paths}\}&\to\mathbb R,\\
\phi&\mapsto S[\phi]:=\int_{\mathbb R^3}d^3x\int_{t_i}^{t_f}dt\,\mathcal L\bigl(\phi(x),\partial_\mu\phi(x)\bigr).
\end{aligned}
```

In the path integral the field takes the place of the path: a path (4.21) is a classical field (1.38) restricted to $`[t_i,t_f]\times\mathbb R^3`$. Paths are therefore denoted by $`\phi`$, and the integrals below are over field configurations.

Below, $`\int d^4x:=\int_{t_i}^{t_f}dt\int_{\mathbb R^3}d^3x`$.

**Quantization**

- **Initial configuration**:

```math
\begin{aligned}
\Phi_i:\{t_i\}\times\mathbb R^3&\to\mathrm{Conf},\\
(t_i,\mathbf x)&\mapsto\Phi_i(t_i,\mathbf x).
\end{aligned}
```

- **Final configuration**:

```math
\begin{aligned}
\Phi_f:\{t_f\}\times\mathbb R^3&\to\mathrm{Conf},\\
(t_f,\mathbf x)&\mapsto\Phi_f(t_f,\mathbf x).
\end{aligned}
```

- **Transition kernel**:

```math
\boxed{K(\Phi_f,\Phi_i):=\int_{\phi(t_i,\mathbf x)=\Phi_i(t_i,\mathbf x)}^{\phi(t_f,\mathbf x)=\Phi_f(t_f,\mathbf x)}\mathcal D\phi\,e^{iS[\phi]},}
```

also written $`\int_{\Phi_i}^{\Phi_f}\mathcal D\phi\,e^{iS[\phi]}`$; the boundary conditions hold for every $`\mathbf x\in\mathbb R^3`$.

**Correlation Functions**

As in (4.19),

```math
K(\Phi_f,\Phi_i)=\langle\Phi_f|\hat U(t_f,t_i)|\Phi_i\rangle,
```
 In operator quantization the vacuum expands in this basis, which defines the vacuum functional $`\Psi[\Phi]`$:

```math
|\mathrm{vac}\rangle=\int\mathcal D\Phi\,|\Phi\rangle\langle\Phi|\mathrm{vac}\rangle=\int\mathcal D\Phi\,|\Phi\rangle\,\Psi[\Phi],\qquad
\Psi[\Phi]:=\langle\Phi|\mathrm{vac}\rangle.
```

Hence

```math
\begin{aligned}
K(\mathrm{vac}_f,\mathrm{vac}_i)&:=\langle\mathrm{vac}_f|\hat U(t_f,t_i)|\mathrm{vac}_i\rangle\\
&=\int\mathcal D\Phi_f\,\mathcal D\Phi_i\,\Psi^*[\Phi_f]\,\Psi[\Phi_i]\,K(\Phi_f,\Phi_i).
\end{aligned}
```




- **Correlation function**: 

```math
\boxed{
\begin{aligned}
G_{a_1\cdots a_r}(x_1,\ldots,x_r)&:=\langle \phi_{a_1}(x_1)\cdots\phi_{a_r}(x_r)\rangle_{\mathrm{vac}}\\
&=\frac{\int_{\mathrm{vac}}^{\mathrm{vac}}\mathcal D\phi\,\phi_{a_1}(x_1)\cdots\phi_{a_r}(x_r)\,e^{iS[\phi]}}{\int_{\mathrm{vac}}^{\mathrm{vac}}\mathcal D\phi\,e^{iS[\phi]}},
\end{aligned}}
```

with $`t_i<x_k^0<t_f`$. 

上述定义中的分母源自于对真空归一化的要求，在上述定义下，<1>=真空的模=1

- **Generating functional**: for a source $`J:[t_i,t_f]\times\mathbb R^3\to\mathbb R^n`$, with $`J\cdot\phi`$ as in (4.10),

```math
K^J(\Phi_f,\Phi_i):=\int_{\Phi_i}^{\Phi_f}\mathcal D\phi\,\exp\Bigl(iS[\phi]+i\int d^4x\,J(x)\cdot\phi(x)\Bigr),
```

and, with the vacuum endpoints as in (4.28),

```math
\boxed{
Z[J]:=K^J(\mathrm{vac}_f,\mathrm{vac}_i)
=\int\mathcal D\Phi_f\,\mathcal D\Phi_i\,\Psi^*[\Phi_f]\,\Psi[\Phi_i]\,K^J(\Phi_f,\Phi_i),}
```

so that $`Z[0]=K(\mathrm{vac}_f,\mathrm{vac}_i)`$.

As in (4.12), each $`\delta/\delta J_a(x)`$ acting on (4.29) brings down $`i\phi_a(x)`$, so by (4.30) and (4.33)

```math
\boxed{G_{a_1\cdots a_r}(x_1,\ldots,x_r)=\frac{1}{Z[0]}\left.\Bigl(-i\frac{\delta}{\delta J_{a_1}(x_1)}\Bigr)\cdots\Bigl(-i\frac{\delta}{\delta J_{a_r}(x_r)}\Bigr)Z[J]\right|_{J=0}.}
```

**Connected Functions**

For a single real scalar field,

```math
\begin{aligned}
G_n(x_1,\ldots,x_n)&:=\langle\Omega|\mathcal T[\hat\phi_H(x_1)\cdots\hat\phi_H(x_n)]|\Omega\rangle
=\left.\frac{1}{Z[0]}\frac{1}{i^n}\frac{\delta^n Z[J]}{\delta J(x_1)\cdots\delta J(x_n)}\right|_{J=0},\\
W[J]&:=-i\ln Z[J],\qquad
G_{n,\mathrm c}=\left.\frac{1}{i^{n-1}}\frac{\delta^nW}{\delta J(x_1)\cdots\delta J(x_n)}\right|_{J=0}.
\end{aligned}
```

Here $`|\Omega\rangle`$ is the normalized interacting vacuum and $`J(x)`$ is a commuting external source. Functional integrals require a regulator; the expressions below define their perturbative use.

**Effective Action and Schwinger--Dyson Equation**

The Legendre transform generates one-particle-irreducible (1PI) vertices, where a 1PI graph stays connected after cutting any single internal line:

```math
\phi_c(x):=\frac{\delta W}{\delta J(x)},\qquad
\Gamma[\phi_c]:=W[J]-\int d^4x\,J\phi_c,\qquad
\boxed{\frac{\delta\Gamma}{\delta\phi_c(x)}=-J(x).}
```

For a translation-invariant scalar functional measure, with functional boundary terms absent,

```math
\left[
\left.\frac{\delta S}{\delta\phi(x)}\right|_{\phi\,\to\,(1/i)\delta/\delta J}
+J(x)\right]Z[J]=0.
```

**Euclidean Continuation and Fermions**

When the time contour can be rotated without crossing singularities, $`t=-i\tau`$ gives, for $`\mathcal L=\tfrac12\partial_\mu\phi\partial^\mu\phi-V(\phi)`$,

```math
e^{iS}\longrightarrow e^{-S_E},\qquad
S_E=\int d\tau\,d^3x\left[\frac12(\partial_\tau\phi)^2
+\frac12(\boldsymbol\nabla\phi)^2+V(\phi)\right].
```

Fermionic fields in the functional integral are independent Grassmann variables. With a fixed measure ordering, a quadratic Dirac action gives

```math
\int\mathcal D\bar\psi\,\mathcal D\psi\,
e^{i\int d^4x\,\bar\psi(i\gamma^\mu\partial_\mu-m)\psi}\ \propto\ \det(i\gamma^\mu\partial_\mu-m),
```

where the field-independent normalization is absorbed into $`Z[0]`$ and the inverse of $`i\gamma^\mu\partial_\mu-m`$ uses the Feynman prescription.

**Gauge Fixing and Faddeev--Popov Ghosts**

For perturbative $`SU(3)`$ theory near the trivial gauge configuration, Lorenz gauge introduces the gauge parameter $`\xi`$ and anticommuting scalar ghost fields $`c^a,\bar c^a`$:

```math
\begin{aligned}
\mathcal L_{\mathrm{gf}}&=-\frac{1}{2\xi}(\partial^\mu A^a_\mu)^2,\\
\mathcal L_{\mathrm{gh}}&=-\bar c^a\partial^\mu(D_\mu^{ab}c^b),\qquad
D_\mu^{ab}:=\delta^{ab}\partial_\mu+g_s f^{acb}A^c_\mu,\\
\Delta_{\mathrm{FP}}[A]&=\det[-\partial^\mu D_\mu^{ab}].
\end{aligned}
```

For an Abelian gauge field in this linear gauge, the determinant is field independent and the ghosts decouple. This local perturbative construction does not resolve global gauge-copy ambiguities.

<br><br>

<a id="phi-cubed-theory"></a>
### 4.3 $`\phi^3`$ Theory

**Action**

Take $`n=1`$, $`\mathrm{Conf}=\mathbb R`$ and $`V(\phi)=\frac12m^2\phi^2+\frac1{3!}\lambda\phi^3`$ in (4.20). With $`\Box:=\partial_\mu\partial^\mu`$ as in (1.91),

```math
\begin{aligned}
S[\phi]&=\int d^4x\,\mathcal L\bigl(\phi(x),\partial_\mu\phi(x)\bigr)\\
&=\int d^4x\,\Bigl[\frac12\partial_\mu\phi\,\partial^\mu\phi-\frac12m^2\phi^2-\frac1{3!}\lambda\phi^3\Bigr]\\
&=\int d^4x\,\Bigl[-\frac12\phi(\Box+m^2)\phi-\frac1{3!}\lambda\phi^3\Bigr]
+\frac12\int d^3x\,\bigl[\phi\,\partial_0\phi\bigr]_{x^0=t_i}^{x^0=t_f}.
\end{aligned}
```

$`S_0[\phi]`$ denotes (4.42) at $`\lambda=0`$.

**Feynman Propagator**

```math
\begin{aligned}
(\Box+m^2)\Delta_F(x)&=-i\delta^{(4)}(x),\\
\Delta_F(x)&=\int\frac{d^4p}{(2\pi)^4}\,\frac{-i}{-p^2+m^2-i\varepsilon}\,e^{-ip\cdot x}
=\int\frac{d^4p}{(2\pi)^4}\,\frac{i}{p^2-m^2+i\varepsilon}\,e^{-ip\cdot x},
\end{aligned}
```

with $`\varepsilon\to0^+`$; this is the function (6.12).

**Free Generating Functional**

From here on $`\mathrm{vac}`$ is the vacuum of $`S_0`$, and $`J`$ vanishes near $`x^0=t_i`$ and $`x^0=t_f`$. Let

```math
K_0^J(\Phi_f,\Phi_i):=\int_{\Phi_i}^{\Phi_f}\mathcal D\phi\,\exp\Bigl(iS_0[\phi]+i\int d^4x\,J(x)\phi(x)\Bigr),
\qquad K_0:=K_0^J\big|_{J=0}.
```

In $`K_0^J(\mathrm{vac}_f,\mathrm{vac}_i)`$ shift the paths, together with $`\Phi_f`$ and $`\Phi_i`$, by

```math
\phi(x)\to\phi(x)+i\int d^4y\,\Delta_F(x-y)J(y),
```

which leaves the measures in (4.28) unchanged. By (4.43), the integrand of $`\int d^4x`$ in the exponent becomes

```math
\begin{aligned}
&-\frac12\phi(\Box+m^2)\phi+J\phi\\
&\to-\frac12\phi(\Box+m^2)\phi+J\phi
\underbrace{-\frac i2\int d^4y\,\Delta_F(x-y)J(y)\,(\Box+m^2)\phi(x)}_{-\frac12J\phi}\\
&\qquad+J(x)\,i\int d^4y\,\Delta_F(x-y)J(y)
\underbrace{-\frac12\phi(x)\,i\int d^4y\,\bigl(-i\delta^{(4)}(x-y)\bigr)J(y)}_{-\frac12J\phi}\\
&\qquad\underbrace{+\frac12\int d^4y\,\Delta_F(x-y)J(y)\,(\Box+m^2)\int d^4\bar y\,\Delta_F(x-\bar y)J(\bar y)}_{-\frac i2J\Delta_FJ}\\
&\to-\frac12\phi(\Box+m^2)\phi+\frac i2\int d^4y\,J(y)\Delta_F(x-y)J(x),
\end{aligned}
```

where the first underbrace holds after integrating by parts in $`x`$, up to terms at $`x^0=t_i,t_f`$. Write $`\chi(x):=i\int d^4y\,\Delta_F(x-y)J(y)`$ for the shift (4.45), so that $`(\Box+m^2)\chi=J`$ by (4.43). Including the terms at $`x^0=t_i,t_f`$ from (4.42) and from this integration by parts, the exponent of (4.44) after the shift is exactly

```math
\begin{aligned}
iS_0[\phi+\chi]+i\int d^4x\,J(\phi+\chi)
&=iS_0[\phi]-\frac12\int d^4x\,d^4y\,J(x)\Delta_F(x-y)J(y)\\
&\quad+i\int d^3x\,\Bigl[\bigl(\phi+\tfrac12\chi\bigr)\partial_0\chi\Bigr]_{x^0=t_i}^{x^0=t_f}.
\end{aligned}
```

Closing the $`p^0`$ contour of (4.43) in the lower half-plane for $`x^0>0`$ and in the upper half-plane for $`x^0<0`$, around the poles $`p^0=\pm(E_{\mathbf p}-i\varepsilon')`$ with $`E_{\mathbf p}`$ as in (2.7) and $`\varepsilon'\to0^+`$,

```math
\Delta_F(x)=\int\frac{d^3p}{(2\pi)^3\,2E_{\mathbf p}}\,e^{i\mathbf p\cdot\mathbf x-iE_{\mathbf p}|x^0|}.
```

Let $`\mathcal E:=(-\nabla^2+m^2)^{1/2}`$, i.e. $`\mathcal E\,e^{i\mathbf p\cdot\mathbf x}=E_{\mathbf p}\,e^{i\mathbf p\cdot\mathbf x}`$. Since $`J`$ vanishes near $`t_i`$ and $`t_f`$, (4.48) gives

```math
\partial_0\chi\big|_{x^0=t_f}=-i\mathcal E\chi\big|_{x^0=t_f},\qquad
\partial_0\chi\big|_{x^0=t_i}=+i\mathcal E\chi\big|_{x^0=t_i},
```

so $`\chi`$ has only positive frequencies at $`t_f`$ and only negative frequencies at $`t_i`$.

For $`S_0`$ the vacuum is $`|0\rangle`$ of (2.8). At $`t=0`$ the Schrödinger-picture operators are $`\hat\phi(\mathbf x)=\hat\phi_I(0,\mathbf x)`$ and $`\hat\pi(\mathbf x)=\partial_0\hat\phi_I(0,\mathbf x)`$ by (6.2) and (1.86). Inverting (2.7), and acting with $`\hat\pi(\mathbf x)`$ as $`-i\,\delta/\delta\Phi(\mathbf x)`$ on $`\Psi[\Phi]=\langle\Phi|0\rangle`$,

```math
\begin{aligned}
\hat a_{\mathbf p}&=\int d^3x\,e^{-i\mathbf p\cdot\mathbf x}\bigl[E_{\mathbf p}\hat\phi(\mathbf x)+i\hat\pi(\mathbf x)\bigr],\\
0=\langle\Phi|\hat a_{\mathbf p}|0\rangle&=\int d^3x\,e^{-i\mathbf p\cdot\mathbf x}\Bigl[(\mathcal E\Phi)(\mathbf x)+\frac{\delta}{\delta\Phi(\mathbf x)}\Bigr]\Psi[\Phi]\quad\text{for all }\mathbf p,\\
\Psi[\Phi]&=\Psi[0]\exp\Bigl(-\frac12\int d^3x\,\Phi\,\mathcal E\,\Phi\Bigr),
\end{aligned}
```

where the second line uses $`\int d^3x\,f\,\mathcal E\,g=\int d^3x\,(\mathcal Ef)\,g`$ and states $`\delta\Psi/\delta\Phi(\mathbf x)=-(\mathcal E\Phi)(\mathbf x)\Psi[\Phi]`$. With $`\chi_{f,i}:=\chi(t_{f,i},\cdot\,)`$, the shift turns $`\Psi^*[\Phi_f]\Psi[\Phi_i]`$ into $`\Psi^*[\Phi_f+\chi_f]\Psi[\Phi_i+\chi_i]`$, while $`\phi(t_{f,i},\cdot\,)=\Phi_{f,i}`$. By (4.49) and (4.50),

```math
\begin{aligned}
i\int d^3x\,\Bigl[\bigl(\phi+\tfrac12\chi\bigr)\partial_0\chi\Bigr]_{x^0=t_i}^{x^0=t_f}
&=\int d^3x\,\Bigl[\bigl(\Phi_f+\tfrac12\chi_f\bigr)\mathcal E\chi_f+\bigl(\Phi_i+\tfrac12\chi_i\bigr)\mathcal E\chi_i\Bigr],\\
\ln\frac{\Psi^*[\Phi_f+\chi_f]\,\Psi[\Phi_i+\chi_i]}{\Psi^*[\Phi_f]\,\Psi[\Phi_i]}
&=-\int d^3x\,\Bigl[\bigl(\Phi_f+\tfrac12\chi_f\bigr)\mathcal E\chi_f+\bigl(\Phi_i+\tfrac12\chi_i\bigr)\mathcal E\chi_i\Bigr],
\end{aligned}
```

so the terms at $`x^0=t_i,t_f`$ in (4.47) cancel the change of $`\Psi^*[\Phi_f]\Psi[\Phi_i]`$. Hence

```math
K_0^J(\mathrm{vac}_f,\mathrm{vac}_i)=K_0(\mathrm{vac}_f,\mathrm{vac}_i)\,
\exp\Bigl[-\frac12\int d^4x\,d^4y\,J(x)\Delta_F(x-y)J(y)\Bigr],
```

and

```math
\boxed{
\begin{aligned}
Z_0[J]&:=K_0^J(\mathrm{vac}_f,\mathrm{vac}_i)
=\int\mathcal D\Phi_f\,\mathcal D\Phi_i\,\Psi^*[\Phi_f]\,\Psi[\Phi_i]\,K_0^J(\Phi_f,\Phi_i)\\
&=Z_0[0]\,\exp\Bigl[-\frac12\int d^4x\,d^4y\,J(x)\Delta_F(x-y)J(y)\Bigr],
\end{aligned}}
```

with $`Z_0[0]=K_0(\mathrm{vac}_f,\mathrm{vac}_i)`$ by (4.52).

**Two-Point Function**

For $`S_0`$ and $`t_i<z_1^0,z_2^0<t_f`$, by (4.35) and (4.53),

```math
\boxed{
\begin{aligned}
\langle\phi(z_1)\phi(z_2)\rangle_{\mathrm{vac}}
&=\frac{1}{Z_0[0]}\Bigl(-i\frac{\delta}{\delta J(z_1)}\Bigr)\Bigl(-i\frac{\delta}{\delta J(z_2)}\Bigr)Z_0[J]\Big|_{J=0}\\
&=\Bigl(-i\frac{\delta}{\delta J(z_1)}\Bigr)\Bigl(-i\frac{\delta}{\delta J(z_2)}\Bigr)
\exp\Bigl[-\frac12\int d^4x\,d^4y\,J(x)\Delta_F(x-y)J(y)\Bigr]\Big|_{J=0}\\
&=\frac12\Delta_F(z_1-z_2)+\frac12\Delta_F(z_2-z_1)\\
&=\Delta_F(z_1-z_2).
\end{aligned}}
```

**Perturbation Expansion**

By (4.12), each $`-i\,\delta/\delta J(z)`$ acting on (4.44) inserts $`\phi(z)`$, so

```math
\begin{aligned}
K(\Phi_f,\Phi_i)
&=\int_{\Phi_i}^{\Phi_f}\mathcal D\phi\,\exp\Bigl(iS_0[\phi]+i\int d^4z\,\Bigl(-\frac{\lambda}{3!}\Bigr)\phi^3\Bigr)\\
&=\int_{\Phi_i}^{\Phi_f}\mathcal D\phi\,e^{iS_0[\phi]}\sum_{m=0}^\infty\frac1{m!}\Bigl(i\int d^4z\,\Bigl(-\frac{\lambda}{3!}\Bigr)\phi(z)^3\Bigr)^m\\
&=\sum_{m=0}^\infty\frac1{m!}\Bigl(-\frac{i\lambda}{3!}\Bigr)^m\prod_{k=1}^m\int d^4z_k\Bigl(-i\frac{\delta}{\delta J(z_k)}\Bigr)^3K_0^J(\Phi_f,\Phi_i)\Big|_{J=0}\\
&=\sum_{m=0}^\infty\frac1{m!}\Bigl(\frac{\lambda}{3!}\Bigr)^m\prod_{k=1}^m\int d^4z_k\Bigl(\frac{\delta}{\delta J(z_k)}\Bigr)^3K_0^J(\Phi_f,\Phi_i)\Big|_{J=0}.
\end{aligned}
```

With the vacuum of $`S_0`$ at both ends, (4.52) gives

```math
\boxed{
\begin{aligned}
K(\mathrm{vac}_f,\mathrm{vac}_i)
&=\sum_{m=0}^\infty\frac1{m!}\Bigl(\frac{\lambda}{3!}\Bigr)^m\prod_{k=1}^m\int d^4z_k\Bigl(\frac{\delta}{\delta J(z_k)}\Bigr)^3\\
&\qquad\exp\Bigl[-\frac12\int d^4x\,d^4y\,J(x)\Delta_F(x-y)J(y)\Bigr]\Big|_{J=0}\cdot K_0(\mathrm{vac}_f,\mathrm{vac}_i).
\end{aligned}}
```

<br><br>

<a id="path-integrals-for-fermion-fields"></a>
### 4.4 Path Integrals for Fermion Fields

<a id="grassmann-algebra"></a>
#### Grassmann Algebra

**Algebra**

Let $`\mathbb K=\mathbb R`$ or $`\mathbb C`$.

- **Algebra**: a vector space $`\mathcal A`$ over $`\mathbb K`$ with a product

```math
\begin{aligned}
\mathcal A\times\mathcal A&\to\mathcal A,\\
(u,v)&\mapsto uv,
\end{aligned}
```

that is bilinear: for all $`\alpha,\beta\in\mathbb K`$ and $`u,v,w\in\mathcal A`$,

```math
\begin{aligned}
u(\alpha v+\beta w)&=\alpha\,uv+\beta\,uw,\\
(\alpha v+\beta w)u&=\alpha\,vu+\beta\,wu.
\end{aligned}
```

- **Unital algebra**: an algebra with an element $`1\in\mathcal A`$ such that $`1u=u=u1`$ for all $`u\in\mathcal A`$.
  - For $`\alpha\in\mathbb K`$, $`\alpha1`$ is written $`\alpha`$.
- **Associative algebra**: an algebra in which $`(uv)w=u(vw)`$ for all $`u,v,w\in\mathcal A`$.

**Generator**

- **Generated subalgebra**: for an associative unital algebra $`\mathcal A`$ over $`\mathbb K`$ and a subset $`\Sigma\subset\mathcal A`$ with elements $`u_a`$, the subalgebra generated by $`\Sigma`$ is

```math
\mathcal A(\Sigma):=\Bigl\{f_0+\sum_{k\ge1}\sum_{a_1,\ldots,a_k}f_{a_1\cdots a_k}\,u_{a_1}\cdots u_{a_k}\;:\;f_0,\,f_{a_1\cdots a_k}\in\mathbb K\Bigr\},
```

where only finitely many coefficients are nonzero.

- **Generating set**: $`\Sigma`$ is a generating set of $`\mathcal A`$ if $`\mathcal A(\Sigma)=\mathcal A`$.

**Grassmann Algebra**

- **Grassmann (exterior) algebra**: an associative unital algebra over $`\mathbb K`$ with a generating set $`\{\zeta_1,\ldots,\zeta_n\}`$ such that

```math
\zeta_a\zeta_b+\zeta_b\zeta_a=0,\qquad a,b=1,\ldots,n,
```

in particular $`\zeta_a^2=0`$. No further relations are imposed: every relation among the $`\zeta_a`$ follows from (4.60). The algebra is denoted $`\mathcal G(\zeta_1,\ldots,\zeta_n)`$, or $`\mathcal G_n`$.

- **Basis**: the ordered monomials $`1`$ and $`\zeta_{a_1}\cdots\zeta_{a_k}`$ with $`a_1<\cdots<a_k`$ are linearly independent over $`\mathbb K`$, and

```math
\begin{aligned}
\mathcal G_n&=\mathop{\rm span}\nolimits\,_{\mathbb K}\{1,\ \zeta_{a_1}\cdots\zeta_{a_k}\mid 1\le a_1<\cdots<a_k\le n\},\\
\dim_{\mathbb K}\mathcal G_n&=2^n.
\end{aligned}
```

- **Expansion**: every $`f\in\mathcal G_n`$ has a unique expansion

```math
f=\sum_{k=0}^n\sum_{1\le a_1<\cdots<a_k\le n}f_{a_1\cdots a_k}\,\zeta_{a_1}\cdots\zeta_{a_k},\qquad f_{a_1\cdots a_k}\in\mathbb K,
```

in which the $`k=0`$ term is $`f_0`$.

<br><br>

<a id="grassmann-calculus"></a>
#### Calculus on the Grassmann Algebra

<br><br>

<a id="qft-ch5"></a>
## 5. New Physics Beyond the Standard Model



<a id="seesaw-mechanism"></a>
### 5.1 Seesaw Mechanism

<a id="type-i-seesaw"></a>
#### Type-I Seesaw

**Fields and Lagrangian**

Extend the Standard Model by $`n`$ right-handed neutrino fields. 

- **Right-handed neutrinos**: $`N_{IR}`$, $`I=1,\ldots,n`$, are four-component chiral spinors with $`P_RN_{IR}=N_{IR}`$ and are singlets of $`SU(3)_c\times SU(2)_L\times U(1)_Y`$.
- **Flavor multiplets**: $`N_R:=(N_{1R},\ldots,N_{nR})^T`$ and $`\nu_L:=(\nu_{eL},\nu_{\mu L},\nu_{\tau L})^T`$. The lepton doublets $`\ell_{\alpha L}`$, charged singlets $`E_{\alpha R}`$ and Higgs doublet $`H`$ are those of Section 3.5.




The conjugate Higgs doublet and the additional terms in the Lagrangian are

```math
H^c:=i\sigma^2H^*
=\begin{pmatrix}H^{0*}\\-H^-\end{pmatrix}
\sim\Bigl(\mathbf2,-\frac12\Bigr),\qquad H^-:=(H^+)^*,
```

```math
\boxed{
\begin{aligned}
\mathcal L_{\mathrm I}
={}&\mathcal L_{\mathrm{SM}}
+\overline{N_R}\,i\gamma^\mu\partial_\mu N_R\\
&-\left(\overline{\ell_{\alpha L}}\,(y_\nu)_{\alpha I}H^cN_{IR}
+\frac12\overline{N_R^c}\,M_RN_R+\mathrm{h.c.}\right),\\
y_\nu&\in\mathbb C^{3\times n},\qquad M_R\in\mathbb C^{n\times n},\qquad M_R^T=M_R.
\end{aligned}
}
```

Repeated flavor indices are summed. The Yukawa matrix $`y_\nu`$ is dimensionless and $`M_R`$ has mass dimension one. Under the electroweak transformation of Section 3.5,

```math
\begin{aligned}
\ell_L'&=e^{-i\theta_Y/2}U(\theta)\ell_L,
& (H^c)'&=e^{-i\theta_Y/2}U(\theta)H^c,
& N_R'&=N_R,\\
\overline{\ell_L'}\,y_\nu(H^c)'N_R'
&=\overline{\ell_L}\,y_\nu H^cN_R.
\end{aligned}
```

The Majorana term is gauge invariant. Its flavor matrix can be taken symmetric because $`\overline{N_{IR}^c}N_{JR}=\overline{N_{JR}^c}N_{IR}`$.

**Mass Terms after Symmetry Breaking**

In the unitary gauge,

```math
H=\frac1{\sqrt2}\begin{pmatrix}0\\v+h\end{pmatrix},\qquad
H^c=\frac1{\sqrt2}\begin{pmatrix}v+h\\0\end{pmatrix},\qquad
M_l=\frac v{\sqrt2}y_l,\qquad M_D:=\frac v{\sqrt2}y_\nu.
```

Here $`v\simeq246\,\mathrm{GeV}`$, as in Section 3.5. With $`l_L:=(l_{eL},l_{\mu L},l_{\tau L})^T`$,

```math
\begin{aligned}
-\mathcal L_{\mathrm{mass}+h}
={}&\overline{l_L}M_lE_R+\overline{\nu_L}M_DN_R
+\frac12\overline{N_R^c}M_RN_R\\
&+\frac hv\left(\overline{l_L}M_lE_R+\overline{\nu_L}M_DN_R\right)
+\mathrm{h.c.}
\end{aligned}
```

Using the charge-conjugation identity

```math
\overline{\nu_L}M_DN_R=\overline{N_R^c}M_D^T\nu_L^c,
```

define

```math
\Psi_L:=\begin{pmatrix}\nu_L\\N_R^c\end{pmatrix},\qquad
\Psi_L^c=\begin{pmatrix}\nu_L^c\\N_R\end{pmatrix},\qquad
\boxed{\mathcal M:=\begin{pmatrix}0_{3\times3}&M_D\\M_D^T&M_R\end{pmatrix}=\mathcal M^T}.
```

The mass terms become

```math
-\mathcal L_{\mathrm{mass}}
=\overline{l_L}M_lE_R+\frac12\overline{\Psi_L}\,\mathcal M\Psi_L^c+\mathrm{h.c.}
```

**Flavor Basis and Takagi Factorization**

For constant unitary matrices $`R_\ell,R_E\in U(3)`$ and $`R_N\in U(n)`$, write the old fields in terms of new fields as

```math
\begin{aligned}
\ell_L&=R_\ell\ell_L',\qquad E_R=R_EE_R',\qquad N_R=R_NN_R',\\
M_l'&=R_\ell^\dagger M_lR_E,\qquad
M_D'=R_\ell^\dagger M_DR_N,\qquad
M_R'=R_N^TM_RR_N.
\end{aligned}
```

These transformations preserve the kinetic and gauge terms. We use the charged-lepton mass basis of Section 3.5,

```math
M_l=D_l:=\mathop{\rm diag}\nolimits (m_e,m_\mu,m_\tau).
```

Since $`\mathcal M`$ is complex symmetric, there exists $`\mathcal U\in U(3+n)`$ such that

```math
\boxed{
\begin{aligned}
\mathcal M&=\mathcal U D\mathcal U^T,\qquad
\mathcal U^\dagger\mathcal M\mathcal U^*=D,\\
D&:=\mathop{\rm diag}\nolimits (D_\nu,D_N),\qquad
D_\nu:=\mathop{\rm diag}\nolimits (m_1,m_2,m_3),\qquad
D_N:=\mathop{\rm diag}\nolimits (M_1,\ldots,M_n),
\end{aligned}
}
```

where all masses are nonnegative. We label the three light states by $`i=1,2,3`$ and the $`n`$ heavy states by $`I=1,\ldots,n`$; the light labels allow either normal or inverted ordering. The field transformation and the diagonal mass terms are

```math
\begin{aligned}
\Psi_L&=\mathcal U\Psi_L^m,\qquad
\Psi_L^m:=\begin{pmatrix}\nu_L^m\\(N_R^m)^c\end{pmatrix},\qquad
\Psi_L^c=\mathcal U^*(\Psi_L^m)^c,\\
-\mathcal L_{\mathrm{mass}}
&=\overline{l_L}D_lE_R
+\frac12\overline{\nu_L^m}D_\nu(\nu_L^m)^c
+\frac12\overline{(N_R^m)^c}D_NN_R^m+\mathrm{h.c.}
\end{aligned}
```

Equivalently, one may first block diagonalize and then Takagi diagonalize each block:

```math
\begin{aligned}
\Psi_L&=W\begin{pmatrix}\nu_L^{\mathrm b}\\(N_R^{\mathrm b})^c\end{pmatrix},\qquad
W^\dagger\mathcal MW^*=\begin{pmatrix}M_\nu&0\\0&M_N\end{pmatrix},\\
M_\nu&=UD_\nu U^T,\qquad M_N=U_ND_NU_N^T,\\
\mathcal U&=W\begin{pmatrix}U&0\\0&U_N\end{pmatrix},\qquad
W\in U(3+n),\quad U\in U(3),\quad U_N\in U(n).
\end{aligned}
```

The matrices $`M_\nu`$ and $`M_N`$ refer to the block-diagonal basis; $`M_N`$ is generally different from the original block $`M_R`$.

**Rank and Parameter Counting**

The zero active-active block implies

```math
\mathcal M\begin{pmatrix}a\\0\end{pmatrix}=0
\quad\text{for }a\in\ker M_D^T,\qquad
\mathop{\rm rank}\nolimits\,\mathcal M\le\min(2n,3+n).
```

If $`M_R`$ is invertible, block elimination gives the exact rank identity

```math
\begin{aligned}
&\begin{pmatrix}I_3&-M_DM_R^{-1}\\0&I_n\end{pmatrix}
\mathcal M
\begin{pmatrix}I_3&0\\-M_R^{-1}M_D^T&I_n\end{pmatrix}
=\begin{pmatrix}-M_DM_R^{-1}M_D^T&0\\0&M_R\end{pmatrix},\\
&\mathop{\rm rank}\nolimits\,\mathcal M
=n+\mathop{\rm rank}\nolimits (-M_DM_R^{-1}M_D^T).
\end{aligned}
```

This congruence is not a unitary mass diagonalization. For generic matrices, the light rank is $`r=\min(n,3)`$ and there are $`3-r`$ massless light states. In particular, $`n=2`$ gives the minimal seesaw with one massless light neutrino at tree level:

```math
m_1=0\quad\text{(normal ordering)},\qquad
m_3=0\quad\text{(inverted ordering)}.
```

For the following counts, take $`n\ge1`$, generic rank and nondegenerate nonzero masses. Before quotienting by field redefinitions, the numbers of independent real parameters are

```math
\begin{aligned}
N(M_D)&=6n,\qquad N(M_R)=n(n+1),\qquad N(\mathcal M)=n^2+7n,\\
N(D)&=n+r=\min(2n,3+n),\\
N(\mathcal U)_{\mathrm{constrained}}
&=n^2+7n-(n+r).
\end{aligned}
```

The last line counts independent non-mass parameters of $`\mathcal M`$ at fixed $`D`$, with the zero-block constraint imposed and Takagi stabilizers removed. It is not the dimension of an unconstrained $`U(3+n)`$ matrix.

For nondegenerate charged-lepton masses, the remaining basis freedom is

```math
\begin{aligned}
\ell_L&=P\ell_L',\qquad E_R=PE_R',\qquad N_R=R_NN_R',\\
P&:=\mathop{\rm diag}\nolimits (e^{i\phi_e},e^{i\phi_\mu},e^{i\phi_\tau}),
\qquad R_N\in U(n),\\
M_D'&=P^\dagger M_DR_N,\qquad M_R'=R_N^TM_RR_N.
\end{aligned}
```

There are $`3+n^2`$ redundant real parameters. Excluding the three charged-lepton masses,

```math
\boxed{
\begin{aligned}
N_{\nu,\mathrm{phys}}&=(n^2+7n)-(3+n^2)=7n-3,\\
N_{\mathrm{masses}}&=n+r,\qquad
N_{\mathrm{mixing}}=6n-r-3.
\end{aligned}
}
```

Thus $`n=2`$ has four nonzero masses and seven mixing parameters, while $`n=3`$ has six masses and twelve mixing parameters.

**Charged Currents and the PMNS Matrix**

Write the upper blocks of $`\mathcal U`$ as

```math
K:=W_{11}U,\qquad R:=W_{12}U_N,\qquad
\nu_{\alpha L}=K_{\alpha i}\nu_{iL}^m+R_{\alpha I}(N_{IR}^m)^c.
```

In the charged-lepton mass basis, the leptonic charged current of Section 3.5 becomes

```math
\boxed{
\mathcal L_{\mathrm{CC}}^\ell
=\frac{g_2}{\sqrt2}W_\mu^-
\overline{l_{\alpha L}}\gamma^\mu
\left[K_{\alpha i}\nu_{iL}^m+R_{\alpha I}(N_{IR}^m)^c\right]
+\mathrm{h.c.}
}
```

Following the coefficient definition, set $`U_{\mathrm{PMNS}}:=K`$. Unitarity of $`\mathcal U`$ and its zero-block relation give

```math
\boxed{
\begin{aligned}
U_{\mathrm{PMNS}}U_{\mathrm{PMNS}}^\dagger
&=I_3-RR^\dagger,\\
KD_\nu K^T+RD_NR^T&=0_{3\times3}.
\end{aligned}
}
```

The light charged-current matrix $`U_{\mathrm{PMNS}}`$ is generally nonunitary; the Takagi matrix $`U`$ is unitary.

**Exact Parametrization of Light-Heavy Mixing**

Choose the singlet flavor basis so that the heavy block after block diagonalization is $`M_N=D_N`$, hence $`U_N=I_n`$. In the coordinate patch where $`W_{11}`$ is invertible, use the block-unitary freedom to write

```math
\begin{aligned}
X&\in\mathbb C^{3\times n},\qquad
A_X:=(I_3+XX^\dagger)^{-1/2},\qquad
B_X:=(I_n+X^\dagger X)^{-1/2},\\
A_XX&=XB_X,\qquad
\boxed{W(X):=\begin{pmatrix}A_X&A_XX\\-X^\dagger A_X&B_X\end{pmatrix}},
\qquad W^\dagger W=WW^\dagger=I_{3+n}.
\end{aligned}
```

The square roots are the positive Hermitian roots. The upper-left block of $`\mathcal M=W\,\mathop{\rm diag}\nolimits (M_\nu,D_N)W^T`$ is

```math
0=A_X(M_\nu+XD_NX^T)A_X^T
\quad\Longleftrightarrow\quad
\boxed{M_\nu=-XD_NX^T=UD_\nu U^T}.
```

The other blocks give

```math
\boxed{
\begin{aligned}
M_D&=A_XXD_N(B_X^T)^{-1},\\
M_R&=B_X\left[D_N-(X^\dagger X)D_N(X^\dagger X)^T\right]B_X^T.
\end{aligned}
}
```

For positive heavy masses, elimination of $`X`$ from the light block also yields

```math
\begin{aligned}
M_\nu
&=-A_X^{-1}M_DB_X^TD_N^{-1}B_XM_D^T(A_X^T)^{-1}\\
&=-A_X^{-1}M_D
\left(M_R+X^\dagger M_D+M_D^TX^*\right)^{-1}
M_D^T(A_X^T)^{-1}.
\end{aligned}
```

Here $`D_N`$ is the physical heavy spectrum. Neither $`M_R=D_N`$ nor $`X=M_DM_R^{-1}`$ is an exact identity in this basis.

**Construction from Masses and Mixing Parameters**

Take generic light rank $`r=\min(n,3)`$ and positive $`M_I`$. Let $`P_\nu`$ project onto the nonzero entries of $`D_\nu`$, and choose a complex $`3\times n`$ matrix $`O`$ with

```math
P_\nu:=\mathop{\rm diag}\nolimits (p_1,p_2,p_3),\qquad
p_i:=\begin{cases}1,&m_i>0,\\0,&m_i=0,\end{cases}
\qquad P_\nu O=O,\qquad OO^T=P_\nu.
```

Then

```math
\boxed{X=iU\sqrt{D_\nu}\,OD_N^{-1/2}},\qquad
-XD_NX^T=U\sqrt{D_\nu}\,OO^T\sqrt{D_\nu}\,U^T=UD_\nu U^T.
```

The orthogonality condition uses a transpose, not a Hermitian conjugate. For $`n>3`$ it does not require $`O^TO=I_n`$. The exact reconstruction is

```math
(D_\nu,D_N,U,O)\ \longrightarrow\ X\ \longrightarrow\ W(X)
\ \longrightarrow\
\mathcal M=W\begin{pmatrix}UD_\nu U^T&0\\0&D_N\end{pmatrix}W^T.
```

After removing the three charged-lepton phases and the $`U(3-r)`$ freedom in the massless subspace, the parameter counts are

```math
\begin{aligned}
N(U)&=9-(3-r)^2-3,\qquad
N(O)=2rn-r(r+1),\\
N(U)+N(O)&=6n-r-3,\qquad
(n+r)+N(U)+N(O)=7n-3.
\end{aligned}
```

For $`n=2`$ and normal ordering,

```math
\begin{aligned}
D_\nu&=\mathop{\rm diag}\nolimits (0,m_2,m_3),\qquad
D_N=\mathop{\rm diag}\nolimits (M_1,M_2),\\
O(z)&=\begin{pmatrix}0&0\\\cos z&-\sin z\\\sin z&\cos z\end{pmatrix},\qquad
z\in\mathbb C,\qquad O^TO=I_2,\qquad OO^T=\mathop{\rm diag}\nolimits (0,1,1).
\end{aligned}
```

For inverted ordering one may use

```math
D_\nu=\mathop{\rm diag}\nolimits (m_1,m_2,0),\qquad
O(z)=\begin{pmatrix}\cos z&-\sin z\\\sin z&\cos z\\0&0\end{pmatrix},\qquad
OO^T=\mathop{\rm diag}\nolimits (1,1,0).
```

Discrete column signs can be absorbed into the heavy Majorana fields. For three massive light states, a phase convention for the unitary matrix $`U`$ is

```math
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
```

Here $`c_{ij}:=\cos\theta_{ij}`$ and $`s_{ij}:=\sin\theta_{ij}`$.

For $`n=2`$, one Majorana phase is removable by rephasing the massless state. One can take $`\rho=0`$ in either ordering, after a common charged-lepton rephasing when needed. Thus $`U`$ contains three angles, one Dirac phase and one Majorana phase; together with the complex $`z`$ there are seven mixing parameters. The exact charged-current matrix is

```math
\boxed{
\begin{aligned}
U_{\mathrm{PMNS}}&=A_XU\\
&=U\left(I_3+\sqrt{D_\nu}\,OD_N^{-1}O^\dagger\sqrt{D_\nu}\right)^{-1/2}.
\end{aligned}
}
```

**Seesaw Limit and Casas–Ibarra Form**

The conventional seesaw regime has invertible $`M_R`$ and

```math
\frac{\sigma_{\max}(M_D)}{\sigma_{\min}(M_R)}\ll1,\qquad
\epsilon_X:=\sigma_{\max}(X)\ll1,
```

where $`\sigma_{\max}`$ and $`\sigma_{\min}`$ denote the largest and smallest singular values. Expanding the exact parametrization,

```math
\begin{aligned}
A_X&=I_3-\frac12XX^\dagger+\mathcal O(\epsilon_X^4),\qquad
B_X=I_n-\frac12X^\dagger X+\mathcal O(\epsilon_X^4),\\
W&=\begin{pmatrix}I_3-\frac12XX^\dagger&X\\-X^\dagger&I_n-\frac12X^\dagger X\end{pmatrix}
+\mathcal O(\epsilon_X^3).
\end{aligned}
```

To leading order in this basis,

```math
M_D\simeq XD_N,\qquad M_R\simeq D_N,\qquad
X\simeq M_DM_R^{-1}\simeq M_DD_N^{-1}.
```

The zero-block identity therefore gives

```math
\boxed{M_\nu=UD_\nu U^T\simeq-M_DM_R^{-1}M_D^T
\simeq-\frac{v^2}{2}\,y_\nu D_N^{-1}y_\nu^T}.
```

The charged-current matrix satisfies

```math
\begin{aligned}
U_{\mathrm{PMNS}}&=\left(I_3-\frac12XX^\dagger\right)U+\mathcal O(\epsilon_X^4),\\
U_{\mathrm{PMNS}}U_{\mathrm{PMNS}}^\dagger
&=I_3-XX^\dagger+\mathcal O(\epsilon_X^4).
\end{aligned}
```

Thus $`U_{\mathrm{PMNS}}\simeq U`$ only after neglecting second-order light-heavy mixing. Substituting the exact expression for $`X`$ into $`M_D\simeq XD_N`$ gives the Casas–Ibarra form,

```math
\boxed{
\begin{aligned}
M_D&\simeq iU\sqrt{D_\nu}\,O\sqrt{D_N},\qquad M_R\simeq D_N,\\
y_\nu&\simeq\frac{i\sqrt2}{v}\,U\sqrt{D_\nu}\,O\sqrt{D_N},\qquad
P_\nu O=O,\quad OO^T=P_\nu.
\end{aligned}
}
```

The construction of $`X`$ is exact; these expressions for $`M_D`$ and $`y_\nu`$ are leading-order approximations. In particular,

```math
\epsilon_X=\sigma_{\max}\!\left(\sqrt{D_\nu}\,OD_N^{-1/2}\right).
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
\hat H=\hat H_0+\hat V
```

The interaction picture evolves operators with $`\hat H_0`$ of (6.1) instead of $`\hat H`$:

```math
\boxed{
\begin{gathered}
\hat O_I(t):=e^{i\hat H_0t}\,\hat O_S\,e^{-i\hat H_0t},\\[4pt]
|\psi_I(t)\rangle:=e^{i\hat H_0t}\,|\psi_S(t)\rangle .
\end{gathered}
}
```

The three pictures coincide at $`t=0`$, and $`\langle\psi_I(t)|\hat O_I(t)|\psi_I(t)\rangle=\langle\psi_S(t)|\hat O_S|\psi_S(t)\rangle`$.

Differentiating the first of (6.2),

```math
\frac{d\hat O_I}{dt}=i\,[\hat H_0,\hat O_I].
```

In particular $`\hat H_{0,I}=\hat H_0`$, while the interaction term becomes time dependent. Differentiating the second of (6.2) and using $`i\partial_t|\psi_S\rangle=\hat H|\psi_S\rangle`$,

```math
i\partial_t|\psi_I(t)\rangle
=e^{i\hat H_0t}\bigl(\hat H-\hat H_0\bigr)|\psi_S(t)\rangle
=e^{i\hat H_0t}\hat Ve^{-i\hat H_0t}\,|\psi_I(t)\rangle,
```

i.e.

```math
\boxed{
i\partial_t|\psi_I(t)\rangle=\hat V_I(t)\,|\psi_I(t)\rangle,
\qquad
\hat V_I(t):=e^{i\hat H_0t}\,\hat V\,e^{-i\hat H_0t}.
}
```

Substituting $`\hat O_S=e^{-i\hat H_0t}\hat O_I(t)e^{i\hat H_0t}`$ into (2.22),

```math
\hat O_H(t)=\hat U_I(t,0)^\dagger\,\hat O_I(t)\,\hat U_I(t,0),
\qquad
\hat U_I(t,0):=e^{i\hat H_0t}\,\hat U(t,0).
```

For a field operator, (6.6) reads $`\hat\phi_H(t,\mathbf x)=\hat U_I(t,0)^\dagger\,\hat\phi_I(t,\mathbf x)\,\hat U_I(t,0)`$, and by (6.3) $`\hat\phi_I(t,\mathbf x)`$ obeys the Heisenberg equation of $`\hat H_0`$ alone.

**Dyson Series**

The state equation (6.5) is the second line of (2.13) with $`\hat H`$ replaced by $`\hat V_I(t)`$. The interaction-picture evolution operator $`\hat U_I(t,t_0)`$, defined by $`|\psi_I(t)\rangle=\hat U_I(t,t_0)|\psi_I(t_0)\rangle`$, is therefore $`\hat U(t,t_0)`$ of (2.21) with $`\hat H\to\hat V_I(t)`$: it is unitary, $`\hat U_I(t_1,t_2)\hat U_I(t_2,t_3)=\hat U_I(t_1,t_3)`$, and $`\hat U_I(t,t_0)^\dagger=\hat U_I(t_0,t)`$. By (6.2) and (2.21),

```math
\hat U_I(t,t_0)=e^{i\hat H_0t}\,\hat U(t,t_0)\,e^{-i\hat H_0t_0},
```

which reduces to the $`\hat U_I(t,0)`$ of (6.6) at $`t_0=0`$; when $`\hat H`$ has no explicit time dependence, $`\hat U(t,t_0)=e^{-i\hat H(t-t_0)}`$ by (2.14). Since $`[\hat V_I(t_1),\hat V_I(t_2)]\neq0`$ in general, case (3) of [Section 2.4](QFT-en-part-02.md#symmetry) applies, and by (2.20)

```math
\boxed{
\hat U_I(t,t_0)=\mathcal T\exp\Bigl(-i\int_{t_0}^{t}dt'\,\hat V_I(t')\Bigr).
}
```

In field theory, $`\hat V=\int d^3x\,\hat{\mathcal H}_{\mathrm{int}}\bigl(\hat\phi_S(\mathbf x)\bigr)`$. By (6.2), $`\hat V_I(t)=\int d^3x\,\hat{\mathcal H}_{\mathrm{int}}\bigl(\hat\phi_I(t,\mathbf x)\bigr)`$, and (6.8) becomes

```math
\hat U_I(t,t_0)=\mathcal T\exp\Bigl(-i\int_{t_0}^{t}dt'\int d^3x\,\hat{\mathcal H}_{\mathrm{int}}\bigl(\hat\phi_I(x)\bigr)\Bigr).
```

For interactions without derivative couplings, $`\hat{\mathcal H}_{\mathrm{int}}=-\hat{\mathcal L}_{\mathrm{int}}`$.

<br><br>

<a id="s-matrix-and-wick-theorem"></a>
### 6.2 The S-Matrix and Wick's Theorem

**Asymptotic States and the S-Matrix**

Assume stable asymptotic particles and the existence of free-particle wave-packet limits. In-states approach the corresponding free states as $`t\to-\infty`$, and out-states as $`t\to+\infty`$. In perturbation theory, with adiabatic switching and the vacuum phase removed,

```math
\begin{aligned}
S_{fi}&:=\langle f,\mathrm{out}|i,\mathrm{in}\rangle=\langle f|\hat S|i\rangle,\\
\hat S&=\hat U_I(+\infty,-\infty)
=\mathcal T\exp\left(-i\int_{-\infty}^{+\infty}dt\,\hat V_I(t)\right).
\end{aligned}
```

Let $`p_i`$ and $`p_f`$ denote the total initial and final four-momenta. The connected invariant amplitude $`\mathcal M_{fi}`$ and the transition operator $`\hat T`$ are defined by

```math
\boxed{\begin{aligned}
\hat S&=1+i\hat T,\qquad
\langle f|\hat T|i\rangle_{\mathrm c}=(2\pi)^4\delta^{(4)}(p_f-p_i)\,\mathcal M_{fi},\\
\hat S^\dagger\hat S&=1\quad\Longrightarrow\quad -i(\hat T-\hat T^\dagger)=\hat T^\dagger\hat T.
\end{aligned}}
```

**Normal Ordering, Contractions, and Wick's Theorem**

Normal ordering refers to the free vacuum $`|0\rangle`$. For a free real scalar field, its contraction is the Feynman propagator; $`\varepsilon\to0^+`$ is understood:

```math
\begin{aligned}
\Delta_F(x-y)&:=\langle0|\mathcal T[\hat\phi_I(x)\hat\phi_I(y)]|0\rangle\\
&=\mathcal T[\hat\phi_I(x)\hat\phi_I(y)]-:\hat\phi_I(x)\hat\phi_I(y):\\
&=\int\frac{d^4p}{(2\pi)^4}\,\frac{i\,e^{-ip\cdot(x-y)}}{p^2-m^2+i\varepsilon}.
\end{aligned}
```

Wick's theorem expresses a time-ordered product of free fields as the sum over all disjoint contractions, including no contractions. Writing $`\hat\phi_j:=\hat\phi_I(x_j)`$,

```math
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
```

For fermions, time ordering and Wick contractions carry the sign of the required permutation of fermionic operators. Free-vacuum expectation values retain only fully contracted terms.


<br><br>

<a id="feynman-diagrams"></a>
### 6.3 Feynman Diagrams and Feynman Rules

**Scalar Example**

For a real scalar with quartic coupling $`\lambda`$, the momentum-space rules contribute to $`i\mathcal M`$. At tree level,

```math
\begin{aligned}
\mathcal L&=\frac12\partial_\mu\phi\,\partial^\mu\phi-\frac12m^2\phi^2-\frac{\lambda}{4!}\phi^4,\qquad
\hat{\mathcal H}_{\mathrm{int}}=\frac{\lambda}{4!}\hat\phi_I^4,\\
\text{internal scalar line}:&\quad\widetilde\Delta_F(p)=\frac{i}{p^2-m^2+i\varepsilon},\qquad
\text{four-scalar vertex}:\quad -i\lambda,\\
 i\mathcal M_{\phi\phi\to\phi\phi}^{\mathrm{tree}}&=-i\lambda.
\end{aligned}
```

**Propagators and External States**

Define $`S_F(x-y):=\langle0|\mathcal T[\hat\psi_I(x)\overline{\hat\psi}_I(y)]|0\rangle`$ and $`D_{\mu\nu}(x-y):=\langle0|\mathcal T[\hat A_{I,\mu}(x)\hat A_{I,\nu}(y)]|0\rangle`$. Their Fourier transforms are

```math
\begin{aligned}
\widetilde S_F(p)&=\frac{i(\not p+m)}{p^2-m^2+i\varepsilon},\\
\widetilde D_{\mu\nu}^{(\xi)}(p)&=\frac{-i}{p^2+i\varepsilon}\left[\eta_{\mu\nu}-(1-\xi)\frac{p_\mu p_\nu}{p^2+i\varepsilon}\right],
\qquad \mathcal L_{\mathrm{gf}}=-\frac1{2\xi}(\partial_\mu A^\mu)^2,\\
\widetilde D_{\mu\nu}^{\mathrm{Proca}}(p)&=\frac{-i}{p^2-m_V^2+i\varepsilon}\left(\eta_{\mu\nu}-\frac{p_\mu p_\nu}{m_V^2}\right),\qquad m_V>0.
\end{aligned}
```

Here $`\xi`$ is the covariant gauge parameter ($`\xi=1`$ is Feynman gauge), and $`m_V`$ is the Proca mass. For fields with unit one-particle pole residue, the external factors are

```math
\begin{array}{c|cc}
\text{external state}&\text{incoming}&\text{outgoing}\\ \hline
\text{scalar}&1&1\\
\text{fermion}&u^s(p)&\bar u^s(p)\\
\text{antifermion}&\bar v^s(p)&v^s(p)\\
\text{vector}&\epsilon_\mu^r(p)&\epsilon_\mu^{r*}(p)
\end{array}
```

The $`\epsilon_\mu^r`$ are physical polarization vectors. External propagators are amputated; a general field normalization requires the pole-residue factors in [Section 6.5](QFT-en-part-04.md#lsz-reduction).

**Diagram Rules**

Impose four-momentum conservation at every vertex, integrate each independent loop momentum with $`d^4\ell/(2\pi)^4`$, and sum connected amputated diagrams. Remove the overall $`(2\pi)^4\delta^{(4)}(p_f-p_i)`$ to obtain $`i\mathcal M`$. Divide each graph by its symmetry factor with the external legs held fixed. Each closed fermion loop contributes an additional minus sign; exchanging identical external fermions also changes the sign.

For example, the $`s`$-channel one-loop four-scalar graph has symmetry factor $`2`$:

```math
i\mathcal M_s^{\mathrm{1\,loop}}
=\frac{(-i\lambda)^2}{2}\int\frac{d^4\ell}{(2\pi)^4}
\frac{i}{\ell^2-m^2+i\varepsilon}
\frac{i}{(\ell+p_1+p_2)^2-m^2+i\varepsilon},
\qquad s:=(p_1+p_2)^2.
```

Loop integrals require a regulator and, in a renormalized amplitude, the corresponding counterterms. The full one-loop four-point amplitude also contains the crossed channels.


<br><br>

<a id="correlation-functions"></a>
### 6.4 Correlation Functions

**Vacuum Correlation Functions**

Let $`|\Omega\rangle`$ be the interacting vacuum and $`|0\rangle`$ the free vacuum. With adiabatic vacuum projection understood, the Gell-Mann--Low formula gives

```math
\begin{aligned}
G_n(x_1,\ldots,x_n)&:=\frac{\langle\Omega|\mathcal T[\hat\phi_H(x_1)\cdots\hat\phi_H(x_n)]|\Omega\rangle}{\langle\Omega|\Omega\rangle}\\
&=\frac{\langle0|\mathcal T\left[\hat\phi_I(x_1)\cdots\hat\phi_I(x_n)\exp\left(-i\int dt\,\hat V_I(t)\right)\right]|0\rangle}
{\langle0|\mathcal T\exp\left(-i\int dt\,\hat V_I(t)\right)|0\rangle}.
\end{aligned}
```

The denominator cancels disconnected vacuum bubbles. Graphs contributing to $`G_n`$ may still be disconnected if each component has external field insertions.

**Generating Functionals and Connected Functions**

For a real scalar source $`J(x)`$,

```math
\begin{aligned}
Z[J]&:=\frac{\langle\Omega|\mathcal T\exp\left(i\int d^4x\,J(x)\hat\phi_H(x)\right)|\Omega\rangle}{\langle\Omega|\Omega\rangle},\qquad Z[0]=1,\qquad W[J]:=-i\ln Z[J],\\
G_n(x_1,\ldots,x_n)&=\left.\frac1{i^n}\frac{\delta^nZ[J]}{\delta J(x_1)\cdots\delta J(x_n)}\right|_{J=0},\\
G_{n,\mathrm c}(x_1,\ldots,x_n)&=\left.i^{1-n}\frac{\delta^nW[J]}{\delta J(x_1)\cdots\delta J(x_n)}\right|_{J=0}.
\end{aligned}
```

For $`G_1=0`$, the four-point function splits into connected and disconnected contributions as

```math
\begin{aligned}
G_4(x_1,x_2,x_3,x_4)
&=G_{4,\mathrm c}(x_1,x_2,x_3,x_4)
+G_2(x_1,x_2)G_2(x_3,x_4)\\
&\quad+G_2(x_1,x_3)G_2(x_2,x_4)
+G_2(x_1,x_4)G_2(x_2,x_3).
\end{aligned}
```


<br><br>

