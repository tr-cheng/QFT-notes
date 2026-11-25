> English, part 5/5 · [Complete file](QFT.md) · [1](QFT-en-part-01.md) · [2](QFT-en-part-02.md) · [3](QFT-en-part-03.md) · [4](QFT-en-part-04.md) · [5](QFT-en-part-05.md)

<a id="boltzmann-equation"></a>
### 8.3 Boltzmann Equation

<br><br>

## Appendix A. Summary of Feynman Rules

<a id="sm-feynman-rules"></a>
### A.1 Feynman Diagrams of the Standard Model

**Scope and Gauge**

- **Theory**: the minimal Standard Model of [Section 5.3](QFT-en-part-04.md#electroweak-theory) and [Section 5.4](QFT-en-part-04.md#qcd), with gauge group $`SU(3)_c\times SU(2)_L\times U(1)_Y`$, three generations of quarks and leptons in the mass bases of Section 5.3, and the Higgs doublet $`H`$. There are no right-handed neutrinos, so the neutrinos are massless; the seesaw fields of [Chapter 6](QFT-en-part-04.md#qft-ch6) are not included.
- **Electroweak gauge**: the unitary gauge $`H=(0,v_{\mathrm{SM}}+h)^T/\sqrt2`$ of Section 5.3, with $`v_{\mathrm{SM}}\simeq246\,\mathrm{GeV}`$. The electroweak bosons are $`W^\pm_\mu`$, $`Z_\mu`$, $`A^{\mathrm{em}}_\mu`$ and $`h`$; there are no Goldstone fields.
- **Photon and gluons**: the covariant gauge fixing of [Section 4.3](QFT-en-part-03.md#feynman-diagrams), with one parameter $`\xi`$ for $`A^{\mathrm{em}}_\mu`$ and for the gluons $`A^a_\mu`$ of Section 5.4 (separate parameters may be used),

```math
\left.
\mathcal L_{\mathrm{gf}}=-\frac1{2\xi}\bigl(\partial^\mu A^{\mathrm{em}}_\mu\bigr)^2-\frac1{2\xi}\bigl(\partial^\mu A^a_\mu\bigr)^2 .
\right.
\tag{A.1}
```

- **Order**: tree level, with the tree-level masses of [Section 5.2](QFT-en-part-03.md#sm-fermions) and Section 5.3.
  - Tree graphs contain no closed loops, so the Faddeev--Popov ghosts of [Section 3.2](QFT-en-part-02.md#path-integrals-in-field-theory) and the counterterms of [Chapter 7](QFT-en-part-04.md#qft-ch7) do not enter.
  - These rules are not a loop-ready set: loop calculations in a renormalizable gauge need additional Goldstone, ghost and counterterm rules, which are not given here.
  - Widths are not included. The propagators below are the fixed-order tree-level ones; predictions near the $`W^\pm`$, $`Z`$, $`h`$ or $`t`$ resonance require an appropriate treatment of the width, such as a resummation of the self-energy.

These choices hold only in this subsection.

**Fields and Free Lagrangian**

- **Fermions**: $`\psi_f`$ as in the neutral currents of Section 5.3: $`\psi_f=q_f`$ for $`f=u,d,s,c,b,t`$ (color triplets), $`\psi_f=l_f`$ for $`f=e,\mu,\tau`$, and $`\psi_{\nu_\alpha}=\nu_{\alpha L}`$. Here $`m_f`$ is the mass of $`\psi_f`$, with $`m_{\nu_\alpha}=0`$; $`Q_f`$ is the charge of [Section 5.3](QFT-en-part-04.md#qed), and $`T_f^3`$ is that of Section 5.3.
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

By [Section 4.1](QFT-en-part-03.md#interaction-picture) and [Section 4.2](QFT-en-part-03.md#s-matrix-and-wick-theorem), for interactions without derivatives $`\hat{\mathcal H}_{\mathrm{int}}=-\hat{\mathcal L}_{\mathrm{int}}`$, and the order-$`n`$ term of $`\hat S`$ is

```math
\left.
\frac{i^n}{n!}\int d^4x_1\cdots d^4x_n\,\mathcal T\bigl[\hat{\mathcal L}_{\mathrm{int}}(x_1)\cdots\hat{\mathcal L}_{\mathrm{int}}(x_n)\bigr].
\right.
\tag{A.6}
```

Wick's theorem pairs the fields: a contraction between two factors gives a propagator of $`\mathcal L_0`$, a contraction with an external state gives an external factor, and each factor $`i\int d^4x\,\hat{\mathcal L}_{\mathrm{int}}`$ gives a vertex, its $`x`$-integral imposing four-momentum conservation. The $`1/n!`$ cancels against the permutations of the $`n`$ vertices. 

$`\mathcal L_{3g}`$ and $`\mathcal L_{3W}`$ contain derivatives, and the massive vector fields are constrained (Section 1.8), so $`\hat{\mathcal H}_{\mathrm{int}}\neq-\hat{\mathcal L}_{\mathrm{int}}`$ and the time-ordered products of $`\partial_\mu\hat A_\nu`$ and of massive vector fields contain noncovariant contact terms. At tree level these two effects cancel (not derived here). The rules below are the covariant ones, which also follow from the functional integral of [Chapter 3](QFT-en-part-02.md#qft-ch3) with weight $`e^{iS}`$.

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
- **Fermion lines**: arrows show the flow of fermion number, and the momentum of a fermion propagator points along the arrow. Along each line, write the factors in the order opposite to the arrow, as in [Section 7.2](QFT-en-part-04.md#qed-renormalization). For an external antifermion the arrow points opposite to its motion.
- **Color**: quark colors are $`c,c'\in\{1,2,3\}`$, as in Section 7.2. In $`(T^a)_{c'c}`$, $`c`$ is the color of the quark line entering the vertex and $`c'`$ that of the line leaving it; all other vertices on quark lines carry $`\delta_{c'c}`$.

**Propagators**

The contractions of the fields of $`\mathcal L_0`$, Fourier transformed as in [Section 0.1](QFT-en-part-01.md#fourier-transform), are those of Section 4.3, with $`\delta^{ab}`$ for gluons. In $`\mathcal L_0`$, $`W^1_\mu`$ and $`W^2_\mu`$ are real Proca fields of mass $`m_W`$, so

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

External quarks and gluons also carry their color and adjoint indices. $`W^\pm`$ and $`Z`$ have the three polarizations of [Section 1.8](QFT-en-part-02.md#proca-field), and $`\gamma`$ and $`g`$ the two physical ones. Neutrinos use the $`m=0`$ spinors of [Section 1.7](QFT-en-part-02.md#dirac-field); through the $`P_L`$ in their vertices, only $`P_Lu^s`$ and $`P_Lv^s`$ contribute.

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
5. The sum is $`i\mathcal M_{fi}`$ of Section 4.2. Cross sections and decay rates follow from [Section 4.6](QFT-en-part-03.md#cross-sections-and-decay-rates), with $`C_{\mathrm{id}}`$ for identical final particles.

**Example: $`t\to bW^+`$**

Let the $`t`$ have momentum $`p`$, spin $`s`$, color $`c`$, the $`b`$ momentum $`p'`$, spin $`s'`$, color $`c'`$, and the $`W^+`$ momentum $`k`$, polarization $`r`$, with $`p=p'+k`$. The outgoing $`W^+`$ sits on a $`W^-_\mu`$ leg, and the line enters as $`q_t`$ and leaves as $`q_b`$, so

```math
\left.
i\mathcal M=\bar u^{s'}(p')\Bigl(i\frac{g_2}{\sqrt2}V^*_{tb}\gamma^\mu P_L\Bigr)u^s(p)\,\epsilon^{r*}_\mu(k)\,\delta_{c'c} .
\right.
\tag{A.22}
```
