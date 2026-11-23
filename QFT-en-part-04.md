> English, part 4/5 · [Complete file](QFT.md) · [1](QFT-en-part-01.md) · [2](QFT-en-part-02.md) · [3](QFT-en-part-03.md) · [4](QFT-en-part-04.md) · [5](QFT-en-part-05.md)

<a id="qcd"></a>
### 5.4 Gluon $`g`$: Quantum Chromodynamics

<a id="qcd-gauge-symmetry"></a>
#### Gauge Symmetry $`SU(3)_c`$

- **Generators and covariant derivative**: the generators $`T^a`$ ($`a=1,\ldots,8`$) of $`SU(3)_c`$ on the fields of [Section 5.2](QFT-en-part-03.md#sm-fermions), and the covariant derivative, are

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
\tag{5.61}
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
\tag{5.62}
```

The defining representation of $`SU(3)`$ is irreducible, so by Schur's lemma $`T^aT^a=C_FI_3`$. Taking the trace with (5.13),

```math
\left.
3C_F=\mathop{\rm tr}\nolimits (T^aT^a)=\tfrac12\cdot8
\quad\Longrightarrow\quad
\boxed{T^aT^a=C_FI_3,\qquad C_F=\tfrac43.}
\right.
\tag{5.63}
```

**Quark Fields**

For each flavor $`f\in\{u,d,s,c,b,t\}`$ the quark field is a color triplet, i.e. the multiplet (5.16) with $`n=3`$, with Dirac adjoint as in (5.17):

```math
\left.
q_f(x):=\begin{pmatrix}\psi_{f,1}(x)\\\psi_{f,2}(x)\\\psi_{f,3}(x)\end{pmatrix},
\qquad
\bar q_f(x):=\bigl(\bar\psi_{f,1}(x),\bar\psi_{f,2}(x),\bar\psi_{f,3}(x)\bigr).
\right.
\tag{5.64}
```

Throughout this section $`\gamma^\mu`$ acts on the spinor index of each $`\psi_{f,a}`$ and the $`3\times3`$ matrices $`T^a`$ act on the color index, so $`\gamma^\mu`$ commutes with every matrix built from the $`T^a`$.

**Local $`SU(3)`$ Transformation**

Let $`\theta^a:\mathbb R^4\to\mathbb R`$, $`a=1,\ldots,8`$, and set

```math
\left.
g(x):=e^{i\theta^a(x)T^a}\in SU(3).
\right.
\tag{5.65}
```

This is the internal transformation (1.72) with $`g`$ now depending on $`x`$. The quark fields transform as

```math
\left.
q_f'(x)=g(x)\,q_f(x),\qquad
\bar q_f'(x)=\bar q_f(x)\,g^\dagger(x).
\right.
\tag{5.66}
```

Since $`\partial_\mu(gq_f)=g\,\partial_\mu q_f+(\partial_\mu g)\,q_f`$, the derivative term of (5.18) is not invariant under (5.66):

```math
\left.
\bar q_f'\,i\gamma^\mu\partial_\mu q_f'
=\bar q_f\,i\gamma^\mu\partial_\mu q_f
+\bar q_f\,i\gamma^\mu g^\dagger(\partial_\mu g)\,q_f.
\right.
\tag{5.67}
```

**Covariant Derivative and Gluon Fields**

Introduce eight real vector fields $`A^a_\mu`$, the gluon fields, and define

```math
\left.
A_\mu:=A^a_\mu T^a,\qquad
D_\mu:=\partial_\mu-ig_sA_\mu,
\right.
\tag{5.68}
```

where $`g_s\in\mathbb R`$ is the strong coupling constant and $`D_\mu`$ acts on color triplets. Let $`A_\mu'`$ denote the transformed gluon field and $`D_\mu':=\partial_\mu-ig_sA_\mu'`$. We require $`D_\mu'q_f'=g\,D_\mu q_f`$:

```math
\left.
\begin{aligned}
D_\mu'(gq_f)&=g\,\partial_\mu q_f+(\partial_\mu g)\,q_f-ig_sA_\mu'\,g\,q_f,\\[6pt]
g\,D_\mu q_f&=g\,\partial_\mu q_f-ig_s\,gA_\mu\,q_f.
\end{aligned}
\right.
\tag{5.69}
```

Equating the two for all $`q_f`$ gives $`A_\mu'g=gA_\mu-\frac{i}{g_s}\partial_\mu g`$, i.e.

```math
\left.
\boxed{
A_\mu'=gA_\mu g^\dagger-\frac{i}{g_s}(\partial_\mu g)\,g^\dagger
=gA_\mu g^\dagger+\frac{i}{g_s}\,g\,\partial_\mu g^\dagger.
}
\right.
\tag{5.70}
```

Differentiating $`gg^\dagger=I_3`$ gives $`\bigl((\partial_\mu g)g^\dagger\bigr)^\dagger=-(\partial_\mu g)g^\dagger`$, and Jacobi's formula $`\partial_\mu\det g=\det g\,\mathop{\rm tr}\nolimits (g^\dagger\partial_\mu g)`$ with $`\det g=1`$ gives $`\mathop{\rm tr}\nolimits \bigl((\partial_\mu g)g^\dagger\bigr)=0`$. Hence $`A_\mu'`$ is again Hermitian and traceless, $`A_\mu'=A_\mu'^aT^a`$ with real $`A_\mu'^a`$.

Since $`D_\mu'(gq_f)=g\,D_\mu q_f`$ holds for all $`q_f`$, as operators on color triplets

```math
\left.
D_\mu'=g\,D_\mu\,g^\dagger.
\right.
\tag{5.71}
```

For infinitesimal $`\theta^a`$, $`g=I_3+i\theta^aT^a+O(\theta^2)`$ and (5.70) gives

```math
\left.
\begin{aligned}
A_\mu'&=A_\mu+i\theta^b[T^b,A_\mu]+\frac1{g_s}(\partial_\mu\theta^a)T^a+O(\theta^2)\\
&=A_\mu-f^{bca}\theta^bA^c_\mu T^a+\frac1{g_s}(\partial_\mu\theta^a)T^a+O(\theta^2),\\[6pt]
\delta A^a_\mu:=A_\mu'^a-A_\mu^a
&=\frac1{g_s}\partial_\mu\theta^a+f^{abc}A^b_\mu\theta^c+O(\theta^2).
\end{aligned}
\right.
\tag{5.72}
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
\tag{5.73}
```

Expanding in the basis, $`F_{\mu\nu}=F^a_{\mu\nu}T^a`$ with

```math
\left.
\boxed{
F^a_{\mu\nu}=\partial_\mu A^a_\nu-\partial_\nu A^a_\mu+g_sf^{abc}A^b_\mu A^c_\nu.
}
\right.
\tag{5.74}
```

By (5.71), $`[D_\mu',D_\nu']=g[D_\mu,D_\nu]g^\dagger`$, so

```math
\left.
F_{\mu\nu}'=gF_{\mu\nu}g^\dagger,
\qquad
\delta F^a_{\mu\nu}=f^{abc}F^b_{\mu\nu}\theta^c+O(\theta^2).
\right.
\tag{5.75}
```

By cyclicity of the trace and (5.13),

```math
\left.
\mathop{\rm tr}\nolimits \bigl(F_{\mu\nu}'F'^{\mu\nu}\bigr)
=\mathop{\rm tr}\nolimits \bigl(F_{\mu\nu}F^{\mu\nu}\bigr)
=\tfrac12F^a_{\mu\nu}F^{a\mu\nu}.
\right.
\tag{5.76}
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
\tag{5.77}
```

where the sum runs over the six flavors in (5.64), $`m_f`$ is the mass of flavor $`f`$, and $`D_\mu`$ acts on the $`q_f`$ to its right. Under (5.66) and (5.70), $`D_\mu'q_f'=g\,D_\mu q_f`$ by construction, so

```math
\left.
\bar q_f'\bigl(i\gamma^\mu D_\mu'-m_f\bigr)q_f'
=\bar q_f\,g^\dagger\bigl(i\gamma^\mu g\,D_\mu-m_f\,g\bigr)q_f
=\bar q_f\bigl(i\gamma^\mu D_\mu-m_f\bigr)q_f.
\right.
\tag{5.78}
```

Together with (5.76), $`\mathcal L_{\mathrm{QCD}}`$ is invariant under the local transformations (5.66), (5.70).

Substituting (5.68) and (5.74) into (5.77) separates the free and interaction terms:

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
\tag{5.79}
```

**Equations of Motion**

Treating $`q_f`$, $`\bar q_f`$ and $`A^a_\mu`$ as independent, the Euler–Lagrange equation for $`\bar q_f`$ is

```math
\left.
\bigl(i\gamma^\mu D_\mu-m_f\bigr)q_f=0.
\right.
\tag{5.80}
```

For $`A^a_\nu`$, define the color current $`j^{a\nu}:=\sum_f\bar q_f\gamma^\nu T^aq_f`$. From (5.77) with (5.74) and (5.79),

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
\tag{5.81}
```

The Euler–Lagrange equation $`\partial_\mu\bigl(\partial\mathcal L_{\mathrm{QCD}}/\partial(\partial_\mu A^a_\nu)\bigr)=\partial\mathcal L_{\mathrm{QCD}}/\partial A^a_\nu`$ then reads

```math
\left.
\boxed{
\partial_\mu F^{a\mu\nu}+g_sf^{abc}A^b_\mu F^{c\mu\nu}=-g_sj^{a\nu}.
}
\right.
\tag{5.82}
```

The left-hand side is the $`a`$-component of $`\partial_\mu F^{\mu\nu}-ig_s[A_\mu,F^{\mu\nu}]`$, the covariant derivative of $`F^{\mu\nu}`$ in the adjoint representation; with $`j^\nu:=j^{a\nu}T^a`$, (5.82) is

```math
\left.
D_\mu F^{\mu\nu}:=\partial_\mu F^{\mu\nu}-ig_s[A_\mu,F^{\mu\nu}]=-g_s\,j^\nu.
\right.
\tag{5.83}
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

With the covariant gauge fixing of (4.15), the QED Lagrangian (5.58) for Dirac fields $`\psi_f`$ of charge $`Q_fe`$ and mass $`m_f`$ is

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

For the electron, $`Q_f=-1`$ and the vertex is $`-ie\gamma^\mu`$. Along each fermion line, write the factors in the order opposite to the arrow, so that the spinor indices form a matrix product. Impose four-momentum conservation at every vertex and integrate each loop momentum with $`\int d^4\ell/(2\pi)^4`$, continued to $`\int d^d\ell/(2\pi)^d`$ in $`d=4-\epsilon`$ dimensions. Each closed fermion loop gives a factor $`-1`$ and a Dirac trace; exchanging identical external fermions changes the sign, as in [Section 4.3](QFT-en-part-03.md#feynman-diagrams).

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

