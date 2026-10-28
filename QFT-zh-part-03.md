> 中文版第 3/4 部分 · [完整文件](QFT-zh.md) · [1](QFT-zh-part-01.md) · [2](QFT-zh-part-02.md) · [3](QFT-zh-part-03.md) · [4](QFT-zh-part-04.md)

<a id="electroweak-gauge-theory"></a>
<a id="electroweak-theory"></a>
### 3.5 电弱理论

<a id="sm-leptons"></a>
#### 标准模型中的轻子

电弱理论的规范群为 $`SU(2)_L\times U(1)_Y`$。在 $`SU(2)_L`$ 双重态上 $`T^a:=\sigma^a/2`$，$`a=1,2,3`$；在 $`SU(2)_L`$ 单态上 $`T^a:=0`$。超荷为 $`Y`$ 的场 $`\psi`$ 的变换为

```math
\begin{aligned}
\psi'(x)&=e^{i\theta^a(x)T^a+i\theta_Y(x)Y}\,\psi(x),\qquad \theta^a(x),\ \theta_Y(x)\in\mathbb R,\\
Q&:=T^3+Y,
\end{aligned}
```

其中 $`Q`$ 是以 $`e`$ 为单位的电荷，与 (3.23) 相同。

轻子分为三代，用味指标 $`\alpha=e,\mu,\tau`$ 标记。以下有序对的含义为（$`SU(2)_L`$ 表示，$`Y`$），

```math
\boxed{
\begin{aligned}
\ell_{\alpha L}&:=\begin{pmatrix}\nu_{\alpha L}\\ l_{\alpha L}\end{pmatrix}\sim\Bigl(\mathbf2,-\frac12\Bigr),\qquad
E_{\alpha R}\sim(\mathbf1,-1),\\
Q\,\nu_{\alpha L}&=0,\qquad Q\,l_{\alpha L}=-l_{\alpha L},\qquad Q\,E_{\alpha R}=-E_{\alpha R}.
\end{aligned}
}
```

这些场都是四分量旋量，满足 $`P_L\nu_{\alpha L}=\nu_{\alpha L}`$、$`P_Ll_{\alpha L}=l_{\alpha L}`$ 与 $`P_RE_{\alpha R}=E_{\alpha R}`$，其中 $`P_{L,R}`$ 由 (1.131) 给出。轻子是色单态。最小可重整化标准模型不含右手中微子。

<br><br>

<a id="electroweak-kinetic-terms"></a>
#### 动能项

设 $`W_\mu^a`$，$`a=1,2,3`$，与 $`B_\mu`$ 分别为 $`SU(2)_L`$ 与 $`U(1)_Y`$ 的实规范场，$`g_2,g_1>0`$ 为相应的耦合。令 $`U(\theta):=e^{i\theta^a(x)\sigma^a/2}`$，$`W_\mu:=W_\mu^a\sigma^a/2`$，由 (3.19) 取 $`g_{\mathrm{YM}}\to g_2`$、(3.24) 取 $`eQ\to g_1Y`$，得

```math
\boxed{
\begin{aligned}
D_\mu&:=\partial_\mu-ig_2W_\mu^aT^a-ig_1YB_\mu,\\
W_\mu'&=U(\theta)W_\mu U(\theta)^\dagger-\frac i{g_2}\bigl(\partial_\mu U(\theta)\bigr)U(\theta)^\dagger,\qquad
B_\mu'=B_\mu+\frac1{g_1}\partial_\mu\theta_Y,
\end{aligned}
}
```

使得在 (3.68) 下 $`D_\mu'\psi'=e^{i\theta^aT^a+i\theta_YY}D_\mu\psi`$。场强为

```math
\begin{aligned}
W_{\mu\nu}^a&:=\partial_\mu W_\nu^a-\partial_\nu W_\mu^a+g_2\epsilon^{abc}W_\mu^bW_\nu^c,\qquad
B_{\mu\nu}:=\partial_\mu B_\nu-\partial_\nu B_\mu,\\
[D_\mu,D_\nu]&=-ig_2W_{\mu\nu}^aT^a-ig_1YB_{\mu\nu}.
\end{aligned}
```

作用在轻子场 (3.69) 上，协变导数 (3.70) 为

```math
D_\mu\ell_{\alpha L}=\Bigl(\partial_\mu-ig_2W_\mu^a\frac{\sigma^a}2+\frac i2g_1B_\mu\Bigr)\ell_{\alpha L},\qquad
D_\mu E_{\alpha R}=\bigl(\partial_\mu+ig_1B_\mu\bigr)E_{\alpha R}.
```

拉氏量密度的动能项为

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

由 (3.20)、(3.24) 与 (3.70)，$`\mathcal L_{\mathrm{kin}}`$ 是规范不变的。

<br><br>

<a id="charged-lepton-masses"></a>
#### Yukawa 耦合与带电轻子质量

Higgs 双重态 $`H=:(H^+,H^0)^T\sim(\mathbf2,\frac12)`$ 是色单态。它就是 (3.52) 中取 $`n=2`$ 且 $`\mu_H^2>0`$、并把 $`\partial_\mu`$ 换成 (3.70) 后的 $`\Phi`$。当 $`\theta^a`$ 与 $`\theta_Y`$ 变化时，$`e^{i\theta^a\sigma^a/2+i\theta_Y/2}`$ 取遍 $`U(2)`$，因此由 (3.56)、(3.60) 与 (3.66) 得

```math
\begin{aligned}
\mathcal L_H&=(D_\mu H)^\dagger D^\mu H-V(H),\qquad
V(H)=-\mu_H^2H^\dagger H+\lambda_H(H^\dagger H)^2,\\
\langle H\rangle&=\frac1{\sqrt2}\begin{pmatrix}0\\v\end{pmatrix},\qquad Q\langle H\rangle=0,\qquad
H\big|_{\mathrm{unitary\ gauge}}=\frac1{\sqrt2}\begin{pmatrix}0\\v+h\end{pmatrix}.
\end{aligned}
```

Higgs 场 $`h`$ 的质量为 (3.64) 的 $`m_h`$。

设 $`y_l`$ 为复 $`3\times3`$ 矩阵；重复的味指标 $`\alpha,\beta`$ 求和。轻子 Yukawa 耦合在 (3.68) 下不变：

```math
\begin{aligned}
\mathcal L_Y^\ell&=-\overline{\ell_{\alpha L}}\,(y_l)_{\alpha\beta}\,H\,E_{\beta R}+\mathrm{h.c.},\qquad
\overline{\ell_{\alpha L}}H=\overline{\nu_{\alpha L}}H^++\overline{l_{\alpha L}}H^0,\\
\overline{\ell_{\alpha L}'}H'E_{\beta R}'
&=\overline{\ell_{\alpha L}}\,e^{\frac i2\theta_Y}U(\theta)^\dagger\;e^{\frac i2\theta_Y}U(\theta)H\;e^{-i\theta_Y}E_{\beta R}
=\overline{\ell_{\alpha L}}HE_{\beta R}.
\end{aligned}
```

在幺正规范 (3.74) 下，$`H^+=0`$，且

```math
\mathcal L_Y^\ell=-\Bigl(1+\frac hv\Bigr)\overline{l_{\alpha L}}\,(M_l)_{\alpha\beta}\,E_{\beta R}+\mathrm{h.c.},\qquad
M_l:=\frac v{\sqrt2}\,y_l .
```

中微子 $`\nu_{\alpha L}`$ 不出现在 (3.76) 中。

**味基**

在味空间中记 $`\ell_L:=(\ell_{eL},\ell_{\mu L},\ell_{\tau L})^T`$，$`E_R:=(E_{eR},E_{\mu R},E_{\tau R})^T`$。对常数 $`R_\ell,R_E\in U(3)`$，(3.73) 在下面第一行的基变换下不变；$`M_l`$ 的奇异值分解按第二行确定 $`R_\ell`$ 与 $`R_E`$：

```math
\begin{aligned}
\ell_L&\to R_\ell\,\ell_L,\qquad E_R\to R_E\,E_R,\qquad y_l\to R_\ell^\dagger\,y_l\,R_E,\\
R_\ell^\dagger M_lR_E&=\mathop{\rm diag}\nolimits (m_e,m_\mu,m_\tau),\qquad m_\alpha\ge0 .
\end{aligned}
```

此后采用这组基。用 Dirac 场 $`l_\alpha:=l_{\alpha L}+E_{\alpha R}`$，(3.76) 化为

```math
\boxed{
\begin{aligned}
M_l&=\mathop{\rm diag}\nolimits (m_e,m_\mu,m_\tau),\\
\mathcal L_Y^\ell&=-\sum_{\alpha=e,\mu,\tau}m_\alpha\Bigl(1+\frac hv\Bigr)\bar l_\alpha l_\alpha .
\end{aligned}
}
```

由于 $`\overline{l_{\alpha L}}\,i\gamma^\mu\partial_\mu l_{\alpha L}+\overline{E_{\alpha R}}\,i\gamma^\mu\partial_\mu E_{\alpha R}=\bar l_\alpha\,i\gamma^\mu\partial_\mu l_\alpha`$，(3.73) 的自由部分与 (3.78) 合起来包含每个 $`l_\alpha`$ 的 Dirac 拉氏量 (1.94)，质量为 $`m_\alpha`$。因此带电轻子 $`l_e,l_\mu,l_\tau`$ 是质量为 $`m_e,m_\mu,m_\tau`$ 的 Dirac 场，以强度 $`m_\alpha/v`$ 与 $`h`$ 耦合，而中微子 $`\nu_{\alpha L}`$ 仍无质量。

<br><br>

<a id="gauge-boson-masses"></a>
#### 规范玻色子质量

把 (3.74) 中幺正规范下的 $`H`$ 代入 (3.70)，取 $`T^a=\sigma^a/2`$，$`Y=\frac12`$，

```math
\begin{aligned}
D_\mu H&=\frac1{\sqrt2}\begin{pmatrix}-\frac i2g_2\bigl(W_\mu^1-iW_\mu^2\bigr)(v+h)\\ \partial_\mu h+\frac i2\bigl(g_2W_\mu^3-g_1B_\mu\bigr)(v+h)\end{pmatrix},\\
(D_\mu H)^\dagger D^\mu H&=\frac12\partial_\mu h\,\partial^\mu h
+\frac{(v+h)^2}8\Bigl[g_2^2\bigl(W_\mu^1W^{1\mu}+W_\mu^2W^{2\mu}\bigr)\\
&\qquad+\bigl(g_2W_\mu^3-g_1B_\mu\bigr)\bigl(g_2W^{3\mu}-g_1B^\mu\bigr)\Bigr].
\end{aligned}
```

定义

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

于是 $`W_\mu^1W^{1\mu}+W_\mu^2W^{2\mu}=2W_\mu^+W^{-\mu}`$，$`g_2W_\mu^3-g_1B_\mu=\sqrt{g_2^2+g_1^2}\,Z_\mu`$，因此

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

$`A_\mu^{\mathrm{em}}`$ 不出现在 (3.81) 中。

<br><br>

<a id="sm-quarks"></a>
#### 夸克

夸克分为三代，$`r=1,2,3`$，并且与 (3.32) 一样是色三重态。有序对的含义同 (3.69)，

```math
\begin{aligned}
q_{rL}&:=\begin{pmatrix}u_{rL}\\ d_{rL}\end{pmatrix}\sim\Bigl(\mathbf2,\frac16\Bigr),\qquad
u_{rR}\sim\Bigl(\mathbf1,\frac23\Bigr),\qquad
d_{rR}\sim\Bigl(\mathbf1,-\frac13\Bigr),\\
Q\,u_{rL}&=\frac23u_{rL},\qquad Q\,d_{rL}=-\frac13d_{rL}.
\end{aligned}
```

取 (3.70) 的 $`D_\mu`$ 再加上 (3.36) 的胶子项 $`-ig_sA_\mu`$，夸克动能项为

```math
\mathcal L_{\mathrm{kin}}^q=\sum_{r=1}^3\Bigl(\overline{q_{rL}}\,i\gamma^\mu D_\mu q_{rL}
+\overline{u_{rR}}\,i\gamma^\mu D_\mu u_{rR}
+\overline{d_{rR}}\,i\gamma^\mu D_\mu d_{rR}\Bigr).
```

设 $`y_u,y_d`$ 为复 $`3\times3`$ 矩阵，$`H^c:=i\sigma^2H^*\sim(\mathbf2,-\frac12)`$，并在味空间中记 $`u_L:=(u_{1L},u_{2L},u_{3L})^T`$，$`u_R`$、$`d_L`$、$`d_R`$ 类似。对 $`r,s`$ 求和，夸克 Yukawa 耦合是规范不变的；在幺正规范 (3.74) 下，

```math
\begin{aligned}
\mathcal L_Y^q&=-\overline{q_{rL}}\,(y_d)_{rs}\,H\,d_{sR}-\overline{q_{rL}}\,(y_u)_{rs}\,H^c\,u_{sR}+\mathrm{h.c.},\qquad
H^c\big|_{\mathrm{unitary\ gauge}}=\frac1{\sqrt2}\begin{pmatrix}v+h\\0\end{pmatrix},\\
\mathcal L_Y^q&=-\Bigl(1+\frac hv\Bigr)\bigl(\overline{u_L}\,M_u\,u_R+\overline{d_L}\,M_d\,d_R\bigr)+\mathrm{h.c.},\qquad
M_{u,d}:=\frac v{\sqrt2}\,y_{u,d}.
\end{aligned}
```

**质量基与 CKM 矩阵**

由 $`M_u`$ 与 $`M_d`$ 的奇异值分解选定幺正矩阵 $`R_{uL},R_{uR},R_{dL},R_{dR}`$，按下式定义质量基中的场 $`u'`$、$`d'`$

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

其中 $`m_f\ge0`$；$`q_f`$ 是 (3.32) 的夸克场，$`m_f`$ 是 (3.45) 中的质量。

<br><br>

<a id="electroweak-currents"></a>
#### 带电流与中性流

$`\bar\psi\,i\gamma^\mu D_\mu\psi`$ 中含规范场的项为 $`\bar\psi\gamma^\mu(g_2W_\mu^aT^a+g_1YB_\mu)\psi`$。由 (3.80)，记 $`T^\pm:=T^1\pm iT^2`$，

```math
g_2W_\mu^aT^a+g_1YB_\mu
=\frac{g_2}{\sqrt2}\bigl(W_\mu^+T^++W_\mu^-T^-\bigr)
+eQA_\mu^{\mathrm{em}}
+\frac{g_2}{c_W}\bigl(T^3-s_W^2Q\bigr)Z_\mu .
```

由于 $`\overline{\ell_{\alpha L}}\gamma^\mu T^+\ell_{\alpha L}=\overline{\nu_{\alpha L}}\gamma^\mu l_{\alpha L}`$，且由 (3.85)，$`\overline{q_{rL}}\gamma^\mu T^+q_{rL}=\overline{u_L}\gamma^\mu d_L=\overline{u_L'}\gamma^\mu V_{\mathrm{CKM}}\,d_L'`$，记 $`q_{fL}:=P_Lq_f`$，并分别用 $`f=u,c,t`$ 与 $`f'=d,s,b`$ 标记 $`V:=V_{\mathrm{CKM}}`$ 的行与列，则 (3.73) 与 (3.83) 中的 $`W_\mu^\pm`$ 项为：

```math
\boxed{
\mathcal L_{\mathrm{CC}}
=\frac{g_2}{\sqrt2}\,W_\mu^+\Bigl(\sum_{\alpha=e,\mu,\tau}\overline{\nu_{\alpha L}}\gamma^\mu l_{\alpha L}
+\sum_{f=u,c,t}\ \sum_{f'=d,s,b}V_{ff'}\,\overline{q_{fL}}\gamma^\mu q_{f'L}\Bigr)+\mathrm{h.c.}
}
```

设 $`\psi_f`$ 为 (3.23) 中费米子 $`f`$ 在基 (3.77) 与 (3.85) 下的场：对夸克 $`\psi_f=q_f`$，对 $`f=e,\mu,\tau`$ 有 $`\psi_f=l_f`$，并且 $`\psi_{\nu_\alpha}=\nu_{\alpha L}`$。设 $`T_f^3`$ 为其左手部分的 $`T^3`$：对 $`q_u,q_c,q_t`$ 与 $`\nu_{\alpha L}`$ 为 $`+\frac12`$，对 $`q_d,q_s,q_b`$ 与 $`l_\alpha`$ 为 $`-\frac12`$。$`A_\mu^{\mathrm{em}}`$ 项与 $`Z_\mu`$ 项为

```math
\boxed{
\begin{aligned}
\mathcal L_{\mathrm{NC}}
={}&eA_\mu^{\mathrm{em}}\sum_fQ_f\,\bar\psi_f\gamma^\mu\psi_f\\
&+\frac{g_2}{c_W}Z_\mu\sum_f\bar\psi_f\gamma^\mu\bigl(T_f^3P_L-Q_fs_W^2\bigr)\psi_f .
\end{aligned}
}
```

第一行就是 (3.26) 中取 $`A_\mu=A_\mu^{\mathrm{em}}`$ 的相互作用项。中性流在树级是味对角的。


<br><br>

<a id="qft-ch4"></a>
## 4. 路径积分

<a id="path-integrals-in-quantum-mechanics"></a>
### 4.1 量子力学中的路径积分

**原理**

考虑具有 $`n`$ 个自由度的系统。

- **位形空间**：$`\mathrm{Conf}=\mathbb R^n`$。
- **动力学结构**：拉氏量

```math
\begin{aligned}
L:\mathbb R^n\times\mathbb R^n&\to\mathbb R,\\
(x,y)&\mapsto\sum_{a=1}^n\frac12m_ay_a^2-V(x),
\end{aligned}
```

其中 $`m_a>0`$，$`V:\mathbb R^n\to\mathbb R`$ 光滑。

- **路径**：对 $`t_i<t_f`$，

```math
\begin{aligned}
C:[t_i,t_f]&\to\mathrm{Conf},\\
t&\mapsto C(t).
\end{aligned}
```

- **作用量**：路径上的泛函

```math
\begin{aligned}
S:\{\text{路径}\}&\to\mathbb R,\\
C&\mapsto S[C]:=\int_{t_i}^{t_f}dt\,L\bigl(C(t),\dot C(t)\bigr).
\end{aligned}
```

**量子化**

- **初位形**：

```math
\begin{aligned}
Q_i:\{t_i\}&\to\mathrm{Conf},\\
t_i&\mapsto q_i.
\end{aligned}
```

- **末位形**：

```math
\begin{aligned}
Q_f:\{t_f\}&\to\mathrm{Conf},\\
t_f&\mapsto q_f.
\end{aligned}
```

- **跃迁核**：对具有上述端点的路径的积分，

```math
\boxed{K(Q_f,Q_i):=\int_{C(t_i)=Q_i(t_i)}^{C(t_f)=Q_f(t_f)}\mathcal DC\,e^{iS[C]},}
```

也记作 $`\int_{Q_i}^{Q_f}\mathcal DC\,e^{iS[C]}`$。

**跃迁核的精确定义**

把 $`[t_i,t_f]`$ 分成 $`N+1`$ 步。

- **测度**：

```math
\begin{gathered}
\Delta t:=\frac{t_f-t_i}{N+1},\qquad t_k:=t_i+k\,\Delta t\quad(k=0,\ldots,N+1),\\
\mathcal DC:=\lim_{N\to\infty}\mathcal N_N\prod_{k=1}^Nd^nC(t_k),\qquad
\mathcal N_N:=\prod_{a=1}^n\Bigl(\frac{m_a}{2\pi i\,\Delta t}\Bigr)^{\frac{N+1}{2}},
\end{gathered}
```

于是 $`t_0=t_i`$，$`t_{N+1}=t_f`$，其中 $`d^nC(t_k):=\prod_{a=1}^ndC_a(t_k)`$。

- **作用量**：

```math
S[C]=\lim_{N\to\infty}\Delta t\sum_{k=0}^NL\Bigl(C(t_k),\frac{C(t_{k+1})-C(t_k)}{\Delta t}\Bigr).
```

因此 (4.6) 的含义是

```math
\boxed{
K(Q_f,Q_i)=\lim_{N\to\infty}\mathcal N_N\int\prod_{k=1}^Nd^nC(t_k)\,
\exp\biggl[i\,\Delta t\sum_{k=0}^NL\Bigl(C(t_k),\frac{C(t_{k+1})-C(t_k)}{\Delta t}\Bigr)\biggr],}
```

其中 $`C(t_0):=q_i`$，$`C(t_{N+1}):=q_f`$，每个 $`C(t_k)`$，$`1\le k\le N`$，都在 $`\mathrm{Conf}`$ 上积分。

**泛函导数**

对源 $`J:[t_i,t_f]\to\mathbb R^n`$，记 $`J\cdot C:=\sum_{a=1}^nJ_aC_a`$，

```math
K^J(Q_f,Q_i):=\int_{Q_i}^{Q_f}\mathcal DC\,\exp\Bigl(i\int_{t_i}^{t_f}dt\,\bigl[L\bigl(C(t),\dot C(t)\bigr)+J(t)\cdot C(t)\bigr]\Bigr).
```

在切片形式 (4.9) 中，源在指数中加入 $`i\,\Delta t\sum_{k=0}^NJ(t_k)\cdot C(t_k)`$，因此 $`J`$ 只通过 $`J(t_0),\ldots,J(t_N)`$ 进入。对 $`t_i<t<t_f`$ 定义

```math
\frac{\delta}{\delta J_a(t)}:=\lim_{N\to\infty}\frac{1}{\Delta t}\frac{\partial}{\partial J_a(t_k)},\qquad t_k\to t.
```

记 $`L_j:=L\bigl(C(t_j),[C(t_{j+1})-C(t_j)]/\Delta t\bigr)`$，

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


**例：一维自由粒子**

在 (4.1) 中取 $`n=1`$，$`V=0`$：

```math
L(x,y)=\frac12my^2,\qquad Q_i(t_i)=q_i,\qquad Q_f(t_f)=q_f.
```

由 (4.7)–(4.9)，其中 $`C(t_0)=q_i`$，$`C(t_{N+1})=q_f`$，$`\mathcal N_N=\bigl(\frac{m}{2\pi i\,\Delta t}\bigr)^{\frac{N+1}{2}}`$，

```math
\begin{aligned}
K(Q_f,Q_i)&=\int_{Q_i}^{Q_f}\mathcal DC\,e^{i\int_{t_i}^{t_f}dt\,\frac12m\dot C^2}\\
&=\lim_{N\to\infty}\mathcal N_N\int\prod_{k=1}^{N}dC(t_k)\,e^{\frac{i}{\Delta t}\sum_{k=0}^{N}\frac12m\left(C(t_{k+1})-C(t_k)\right)^2}\\
&=\lim_{N\to\infty}\mathcal N_N\int\prod_{k=1}^{N}dC(t_k)\,
e^{\frac{i}{\Delta t}\left[\frac12mq_i^2+\frac12mq_f^2+mC^2(t_1)+\cdots+mC^2(t_N)\right]}\,
e^{\frac{i}{\Delta t}(-m)\left[q_iC(t_1)+C(t_1)C(t_2)+\cdots+C(t_N)q_f\right]}.
\end{aligned}
```

对 $`C(t_1)`$ 积分，并利用对 $`a>0`$ 成立的 $`\int_{-\infty}^{\infty}dx\,e^{iax^2}=\sqrt{\pi i/a}`$ ($`a\to a+i\varepsilon`$, $`\varepsilon\to0^+`$)：

```math
\begin{aligned}
\int dC(t_1)\,e^{\frac{i}{\Delta t}\left[mC^2(t_1)-mC(t_1)\left(q_i+C(t_2)\right)\right]}
&=\int dC(t_1)\,e^{\frac{im}{\Delta t}\left(C(t_1)-\frac{q_i+C(t_2)}{2}\right)^2}\,e^{-\frac{im}{4\Delta t}\left(q_i+C(t_2)\right)^2}\\
&=\sqrt{\frac{2\pi i\,\Delta t}{m}\cdot\frac12}\;e^{-\frac{im}{4\Delta t}\left(q_i+C(t_2)\right)^2}.
\end{aligned}
```

积分掉 $`C(t_1),\ldots,C(t_{j-1})`$ 之后，$`1\le j\le N`$：

```math
K(Q_f,Q_i)=\lim_{N\to\infty}\mathcal N_N\Bigl(\frac{2\pi i\,\Delta t}{m}\Bigr)^{\frac{j-1}{2}}\frac{1}{\sqrt j}
\int\prod_{k=j}^{N}dC(t_k)\,
e^{\frac{im}{2\Delta t}\left[\frac{\left(C(t_j)-q_i\right)^2}{j}+C^2(t_j)+2C^2(t_{j+1})+\cdots+2C^2(t_N)+q_f^2\right]}\,
e^{\frac{im}{2\Delta t}(-2)\left[C(t_j)C(t_{j+1})+\cdots+C(t_N)q_f\right]}.
```

对 $`C(t_j)`$ 积分：

```math
\begin{aligned}
\frac{\left(C(t_j)-q_i\right)^2}{j}+C^2(t_j)-2C(t_j)C(t_{j+1})
&=\frac{j+1}{j}\Bigl(C(t_j)-\frac{q_i+jC(t_{j+1})}{j+1}\Bigr)^2+\frac{\left(C(t_{j+1})-q_i\right)^2}{j+1}-C^2(t_{j+1}),\\
\int dC(t_j)\,e^{\frac{im}{2\Delta t}\frac{j+1}{j}\left(C(t_j)-\frac{q_i+jC(t_{j+1})}{j+1}\right)^2}
&=\sqrt{\frac{2\pi i\,\Delta t}{m}\cdot\frac{j}{j+1}},
\end{aligned}
```

这就给出 $`j+1`$ 时的 (4.16)；当 $`j=N`$ 时，$`C(t_{N+1})=q_f`$，方括号化为 $`\frac{(q_f-q_i)^2}{N+1}`$。因此，利用 $`(N+1)\Delta t=t_f-t_i`$，

```math
\begin{aligned}
K(Q_f,Q_i)&=\lim_{N\to\infty}\Bigl(\frac{m}{2\pi i\,\Delta t}\Bigr)^{\frac{N+1}{2}}\Bigl(\frac{2\pi i\,\Delta t}{m}\Bigr)^{\frac N2}\frac{1}{\sqrt{N+1}}\,
e^{\frac{im\left(q_f-q_i\right)^2}{2(N+1)\Delta t}}\\
&=\boxed{\sqrt{\frac{m}{2\pi i\,(t_f-t_i)}}\;e^{\frac{im\left(q_f-q_i\right)^2}{2(t_f-t_i)}}.}
\end{aligned}
```

这个例子说明了为什么路径积分的定义 (4.7) 中要包含预因子 $`\mathcal N_N`$。结果 (4.18) 有限，而按定义 $`\mathcal N_N`$ 在 $`N\to\infty`$ 时发散；若没有这个预因子，(4.18) 中剩下的因子 $`\bigl(\frac{2\pi i\,\Delta t}{m}\bigr)^{\frac N2}\frac{1}{\sqrt{N+1}}`$ 趋于零，$`K(Q_f,Q_i)`$ 也将趋于零。

**与算符量子化的关系**

设 $`\hat H:=\sum_{a=1}^n\hat p_a^2/(2m_a)+V(\hat q)`$，其中 $`[\hat q_a,\hat p_b]=i\delta_{ab}`$，$`\hat q_a|q\rangle=q_a|q\rangle`$，并设 $`\hat U(t_f,t_i)=e^{-i\hat H(t_f-t_i)}`$ 为其演化算符 (2.21)。于是，记 $`q_i=Q_i(t_i)`$，$`q_f=Q_f(t_f)`$，

```math
\boxed{K(Q_f,Q_i)=\langle q_f|\hat U(t_f,t_i)|q_i\rangle=\langle q_f,t_f|q_i,t_i\rangle}
```

两种写法分别对应 Schrödinger 绘景与 Heisenberg 绘景，其中由 (2.22)，$`|q,t\rangle:=\hat U(t,0)^\dagger|q\rangle`$ 满足 $`\hat q_H(t)|q,t\rangle=q\,|q,t\rangle`$。

<br><br>

<a id="path-integrals-in-field-theory"></a>
### 4.2 量子场论中的路径积分

按照 [1.4 节](QFT-zh-part-01.md#classical-dynamics)中的第二种观点，把 $`t`$ 换成 $`x^\mu`$。

**原理**

- **位形空间**：$`\mathrm{Conf}=\mathbb R^n`$。
- **动力学结构**：拉氏量密度

```math
\begin{aligned}
\mathcal L:\mathbb R^n\times(\mathbb R^n)^4&\to\mathbb R,\\
(x,y^\mu)&\mapsto\sum_{a=1}^n\frac12y_a^\mu y_{a\mu}-V(x),
\end{aligned}
```

其中 $`y^\mu\in\mathbb R^n`$，$`\mu=0,\ldots,3`$，$`V:\mathbb R^n\to\mathbb R`$ 光滑。

- **路径**：对 $`t_i<t_f`$，

```math
\begin{aligned}
\phi:[t_i,t_f]\times\mathbb R^3&\to\mathrm{Conf},\\
x&\mapsto\phi(x),
\end{aligned}
```

其中 $`\phi(t):=\phi(t,\cdot\,)`$ 为时刻 $`t`$ 的位形。

- **作用量**：路径上的泛函

```math
\begin{aligned}
S:\{\text{路径}\}&\to\mathbb R,\\
\phi&\mapsto S[\phi]:=\int_{\mathbb R^3}d^3x\int_{t_i}^{t_f}dt\,\mathcal L\bigl(\phi(x),\partial_\mu\phi(x)\bigr).
\end{aligned}
```

在路径积分中，场取代了路径的地位：路径 (4.21) 就是限制在 $`[t_i,t_f]\times\mathbb R^3`$ 上的经典场 (1.38)。因此路径记为 $`\phi`$，下面的积分都是对场位形的积分。

以下 $`\int d^4x:=\int_{t_i}^{t_f}dt\int_{\mathbb R^3}d^3x`$。

**量子化**

- **初位形**：

```math
\begin{aligned}
\Phi_i:\{t_i\}\times\mathbb R^3&\to\mathrm{Conf},\\
(t_i,\mathbf x)&\mapsto\Phi_i(t_i,\mathbf x).
\end{aligned}
```

- **末位形**：

```math
\begin{aligned}
\Phi_f:\{t_f\}\times\mathbb R^3&\to\mathrm{Conf},\\
(t_f,\mathbf x)&\mapsto\Phi_f(t_f,\mathbf x).
\end{aligned}
```

- **跃迁核**：

```math
\boxed{K(\Phi_f,\Phi_i):=\int_{\phi(t_i,\mathbf x)=\Phi_i(t_i,\mathbf x)}^{\phi(t_f,\mathbf x)=\Phi_f(t_f,\mathbf x)}\mathcal D\phi\,e^{iS[\phi]},}
```

也记作 $`\int_{\Phi_i}^{\Phi_f}\mathcal D\phi\,e^{iS[\phi]}`$；边界条件对每个 $`\mathbf x\in\mathbb R^3`$ 成立。

**关联函数**

与 (4.19) 同理，

```math
K(\Phi_f,\Phi_i)=\langle\Phi_f|\hat U(t_f,t_i)|\Phi_i\rangle,
```
 在算符量子化中，真空可按这组基展开，由此定义真空泛函 $`\Psi[\Phi]`$：

```math
|\mathrm{vac}\rangle=\int\mathcal D\Phi\,|\Phi\rangle\langle\Phi|\mathrm{vac}\rangle=\int\mathcal D\Phi\,|\Phi\rangle\,\Psi[\Phi],\qquad
\Psi[\Phi]:=\langle\Phi|\mathrm{vac}\rangle.
```

因此

```math
\begin{aligned}
K(\mathrm{vac}_f,\mathrm{vac}_i)&:=\langle\mathrm{vac}_f|\hat U(t_f,t_i)|\mathrm{vac}_i\rangle\\
&=\int\mathcal D\Phi_f\,\mathcal D\Phi_i\,\Psi^*[\Phi_f]\,\Psi[\Phi_i]\,K(\Phi_f,\Phi_i).
\end{aligned}
```




- **关联函数**：

```math
\boxed{
\begin{aligned}
G_{a_1\cdots a_r}(x_1,\ldots,x_r)&:=\langle \phi_{a_1}(x_1)\cdots\phi_{a_r}(x_r)\rangle_{\mathrm{vac}}\\
&=\frac{\int_{\mathrm{vac}}^{\mathrm{vac}}\mathcal D\phi\,\phi_{a_1}(x_1)\cdots\phi_{a_r}(x_r)\,e^{iS[\phi]}}{\int_{\mathrm{vac}}^{\mathrm{vac}}\mathcal D\phi\,e^{iS[\phi]}},
\end{aligned}}
```

其中 $`t_i<x_k^0<t_f`$。

上述定义中的分母源自于对真空归一化的要求，在上述定义下，<1>=真空的模=1

- **生成泛函**：对源 $`J:[t_i,t_f]\times\mathbb R^3\to\mathbb R^n`$，$`J\cdot\phi`$ 的含义同 (4.10)，

```math
K^J(\Phi_f,\Phi_i):=\int_{\Phi_i}^{\Phi_f}\mathcal D\phi\,\exp\Bigl(iS[\phi]+i\int d^4x\,J(x)\cdot\phi(x)\Bigr),
```

并且，取 (4.28) 中的真空端点，

```math
\boxed{
Z[J]:=K^J(\mathrm{vac}_f,\mathrm{vac}_i)
=\int\mathcal D\Phi_f\,\mathcal D\Phi_i\,\Psi^*[\Phi_f]\,\Psi[\Phi_i]\,K^J(\Phi_f,\Phi_i),}
```

于是 $`Z[0]=K(\mathrm{vac}_f,\mathrm{vac}_i)`$。

与 (4.12) 同理，每个 $`\delta/\delta J_a(x)`$ 作用于 (4.29) 都拉下一个 $`i\phi_a(x)`$，因此由 (4.30) 与 (4.33)，

```math
\boxed{G_{a_1\cdots a_r}(x_1,\ldots,x_r)=\frac{1}{Z[0]}\left.\Bigl(-i\frac{\delta}{\delta J_{a_1}(x_1)}\Bigr)\cdots\Bigl(-i\frac{\delta}{\delta J_{a_r}(x_r)}\Bigr)Z[J]\right|_{J=0}.}
```

**连通函数**

对单个实标量场，

```math
\begin{aligned}
G_n(x_1,\ldots,x_n)&:=\langle\Omega|\mathcal T[\hat\phi_H(x_1)\cdots\hat\phi_H(x_n)]|\Omega\rangle
=\left.\frac{1}{Z[0]}\frac{1}{i^n}\frac{\delta^n Z[J]}{\delta J(x_1)\cdots\delta J(x_n)}\right|_{J=0},\\
W[J]&:=-i\ln Z[J],\qquad
G_{n,\mathrm c}=\left.\frac{1}{i^{n-1}}\frac{\delta^nW}{\delta J(x_1)\cdots\delta J(x_n)}\right|_{J=0}.
\end{aligned}
```

这里 $`|\Omega\rangle`$ 是归一化的相互作用真空，$`J(x)`$ 是对易的外源。泛函积分需要正规子；下面的表达式定义了它们在微扰论中的用法。

**有效作用量与 Schwinger--Dyson 方程**

Legendre 变换生成单粒子不可约 (1PI) 顶点；1PI 图是指切断任意一条内线后仍保持连通的图：

```math
\phi_c(x):=\frac{\delta W}{\delta J(x)},\qquad
\Gamma[\phi_c]:=W[J]-\int d^4x\,J\phi_c,\qquad
\boxed{\frac{\delta\Gamma}{\delta\phi_c(x)}=-J(x).}
```

当标量泛函测度平移不变且不存在泛函边界项时，

```math
\left[
\left.\frac{\delta S}{\delta\phi(x)}\right|_{\phi\,\to\,(1/i)\delta/\delta J}
+J(x)\right]Z[J]=0.
```

**欧氏延拓与费米子**

当时间围道可以转动而不越过奇点时，对 $`\mathcal L=\tfrac12\partial_\mu\phi\partial^\mu\phi-V(\phi)`$，$`t=-i\tau`$ 给出：

```math
e^{iS}\longrightarrow e^{-S_E},\qquad
S_E=\int d\tau\,d^3x\left[\frac12(\partial_\tau\phi)^2
+\frac12(\boldsymbol\nabla\phi)^2+V(\phi)\right].
```

泛函积分中的费米子场是独立的 Grassmann 变量。在测度次序固定时，二次 Dirac 作用量给出

```math
\int\mathcal D\bar\psi\,\mathcal D\psi\,
e^{i\int d^4x\,\bar\psi(i\gamma^\mu\partial_\mu-m)\psi}\ \propto\ \det(i\gamma^\mu\partial_\mu-m),
```

其中与场无关的归一化因子被吸收进 $`Z[0]`$，$`i\gamma^\mu\partial_\mu-m`$ 的逆采用费曼处方。

**规范固定与 Faddeev--Popov 鬼场**

对平凡规范位形附近的微扰 $`SU(3)`$ 理论，Lorenz 规范引入规范参数 $`\xi`$ 以及反对易的标量鬼场 $`c^a,\bar c^a`$：

```math
\begin{aligned}
\mathcal L_{\mathrm{gf}}&=-\frac{1}{2\xi}(\partial^\mu A^a_\mu)^2,\\
\mathcal L_{\mathrm{gh}}&=-\bar c^a\partial^\mu(D_\mu^{ab}c^b),\qquad
D_\mu^{ab}:=\delta^{ab}\partial_\mu+g_s f^{acb}A^c_\mu,\\
\Delta_{\mathrm{FP}}[A]&=\det[-\partial^\mu D_\mu^{ab}].
\end{aligned}
```

对这种线性规范下的阿贝尔规范场，该行列式与场无关，鬼场退耦。这种局域的微扰构造不能消除全局的规范复本歧义。

<br><br>

<a id="phi-cubed-theory"></a>
### 4.3 $`\phi^3`$ 理论

**作用量**

在 (4.20) 中取 $`n=1`$，$`\mathrm{Conf}=\mathbb R`$，$`V(\phi)=\frac12m^2\phi^2+\frac1{3!}\lambda\phi^3`$。利用 (1.91) 中的 $`\Box:=\partial_\mu\partial^\mu`$，

```math
\begin{aligned}
S[\phi]&=\int d^4x\,\mathcal L\bigl(\phi(x),\partial_\mu\phi(x)\bigr)\\
&=\int d^4x\,\Bigl[\frac12\partial_\mu\phi\,\partial^\mu\phi-\frac12m^2\phi^2-\frac1{3!}\lambda\phi^3\Bigr]\\
&=\int d^4x\,\Bigl[-\frac12\phi(\Box+m^2)\phi-\frac1{3!}\lambda\phi^3\Bigr]
+\frac12\int d^3x\,\bigl[\phi\,\partial_0\phi\bigr]_{x^0=t_i}^{x^0=t_f}.
\end{aligned}
```

$`S_0[\phi]`$ 表示 (4.42) 取 $`\lambda=0`$ 的情形。

**费曼传播子**

```math
\begin{aligned}
(\Box+m^2)\Delta_F(x)&=-i\delta^{(4)}(x),\\
\Delta_F(x)&=\int\frac{d^4p}{(2\pi)^4}\,\frac{-i}{-p^2+m^2-i\varepsilon}\,e^{-ip\cdot x}
=\int\frac{d^4p}{(2\pi)^4}\,\frac{i}{p^2-m^2+i\varepsilon}\,e^{-ip\cdot x},
\end{aligned}
```

其中 $`\varepsilon\to0^+`$；这就是 (6.12) 中的函数。

**自由生成泛函**

此后 $`\mathrm{vac}`$ 指 $`S_0`$ 的真空，且 $`J`$ 在 $`x^0=t_i`$ 与 $`x^0=t_f`$ 附近为零。令

```math
K_0^J(\Phi_f,\Phi_i):=\int_{\Phi_i}^{\Phi_f}\mathcal D\phi\,\exp\Bigl(iS_0[\phi]+i\int d^4x\,J(x)\phi(x)\Bigr),
\qquad K_0:=K_0^J\big|_{J=0}.
```

在 $`K_0^J(\mathrm{vac}_f,\mathrm{vac}_i)`$ 中把路径连同 $`\Phi_f`$ 与 $`\Phi_i`$ 一起作平移

```math
\phi(x)\to\phi(x)+i\int d^4y\,\Delta_F(x-y)J(y),
```

这不改变 (4.28) 中的测度。由 (4.43)，指数中 $`\int d^4x`$ 的被积函数变为

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

其中第一个下花括号在对 $`x`$ 分部积分后成立，至多相差 $`x^0=t_i,t_f`$ 处的项。把平移 (4.45) 记为 $`\chi(x):=i\int d^4y\,\Delta_F(x-y)J(y)`$，则由 (4.43) 有 $`(\Box+m^2)\chi=J`$。计入来自 (4.42) 以及这次分部积分的 $`x^0=t_i,t_f`$ 处的项，平移后 (4.44) 的指数恰为

```math
\begin{aligned}
iS_0[\phi+\chi]+i\int d^4x\,J(\phi+\chi)
&=iS_0[\phi]-\frac12\int d^4x\,d^4y\,J(x)\Delta_F(x-y)J(y)\\
&\quad+i\int d^3x\,\Bigl[\bigl(\phi+\tfrac12\chi\bigr)\partial_0\chi\Bigr]_{x^0=t_i}^{x^0=t_f}.
\end{aligned}
```

把 (4.43) 的 $`p^0`$ 围道在 $`x^0>0`$ 时闭合于下半平面、在 $`x^0<0`$ 时闭合于上半平面，围绕极点 $`p^0=\pm(E_{\mathbf p}-i\varepsilon')`$，其中 $`E_{\mathbf p}`$ 同 (2.7)，$`\varepsilon'\to0^+`$，

```math
\Delta_F(x)=\int\frac{d^3p}{(2\pi)^3\,2E_{\mathbf p}}\,e^{i\mathbf p\cdot\mathbf x-iE_{\mathbf p}|x^0|}.
```

令 $`\mathcal E:=(-\nabla^2+m^2)^{1/2}`$，即 $`\mathcal E\,e^{i\mathbf p\cdot\mathbf x}=E_{\mathbf p}\,e^{i\mathbf p\cdot\mathbf x}`$。由于 $`J`$ 在 $`t_i`$ 与 $`t_f`$ 附近为零，由 (4.48) 得

```math
\partial_0\chi\big|_{x^0=t_f}=-i\mathcal E\chi\big|_{x^0=t_f},\qquad
\partial_0\chi\big|_{x^0=t_i}=+i\mathcal E\chi\big|_{x^0=t_i},
```

因此 $`\chi`$ 在 $`t_f`$ 处只含正频，在 $`t_i`$ 处只含负频。

对 $`S_0`$，真空为 (2.8) 的 $`|0\rangle`$。由 (6.2) 与 (1.86)，在 $`t=0`$ 时 Schrödinger 绘景的算符为 $`\hat\phi(\mathbf x)=\hat\phi_I(0,\mathbf x)`$ 与 $`\hat\pi(\mathbf x)=\partial_0\hat\phi_I(0,\mathbf x)`$。反解 (2.7)，并令 $`\hat\pi(\mathbf x)`$ 以 $`-i\,\delta/\delta\Phi(\mathbf x)`$ 的形式作用于 $`\Psi[\Phi]=\langle\Phi|0\rangle`$，

```math
\begin{aligned}
\hat a_{\mathbf p}&=\int d^3x\,e^{-i\mathbf p\cdot\mathbf x}\bigl[E_{\mathbf p}\hat\phi(\mathbf x)+i\hat\pi(\mathbf x)\bigr],\\
0=\langle\Phi|\hat a_{\mathbf p}|0\rangle&=\int d^3x\,e^{-i\mathbf p\cdot\mathbf x}\Bigl[(\mathcal E\Phi)(\mathbf x)+\frac{\delta}{\delta\Phi(\mathbf x)}\Bigr]\Psi[\Phi]\quad\text{对所有 }\mathbf p,\\
\Psi[\Phi]&=\Psi[0]\exp\Bigl(-\frac12\int d^3x\,\Phi\,\mathcal E\,\Phi\Bigr),
\end{aligned}
```

其中第二行用到 $`\int d^3x\,f\,\mathcal E\,g=\int d^3x\,(\mathcal Ef)\,g`$，该行即 $`\delta\Psi/\delta\Phi(\mathbf x)=-(\mathcal E\Phi)(\mathbf x)\Psi[\Phi]`$。记 $`\chi_{f,i}:=\chi(t_{f,i},\cdot\,)`$，平移把 $`\Psi^*[\Phi_f]\Psi[\Phi_i]`$ 变为 $`\Psi^*[\Phi_f+\chi_f]\Psi[\Phi_i+\chi_i]`$，而 $`\phi(t_{f,i},\cdot\,)=\Phi_{f,i}`$。由 (4.49) 与 (4.50)，

```math
\begin{aligned}
i\int d^3x\,\Bigl[\bigl(\phi+\tfrac12\chi\bigr)\partial_0\chi\Bigr]_{x^0=t_i}^{x^0=t_f}
&=\int d^3x\,\Bigl[\bigl(\Phi_f+\tfrac12\chi_f\bigr)\mathcal E\chi_f+\bigl(\Phi_i+\tfrac12\chi_i\bigr)\mathcal E\chi_i\Bigr],\\
\ln\frac{\Psi^*[\Phi_f+\chi_f]\,\Psi[\Phi_i+\chi_i]}{\Psi^*[\Phi_f]\,\Psi[\Phi_i]}
&=-\int d^3x\,\Bigl[\bigl(\Phi_f+\tfrac12\chi_f\bigr)\mathcal E\chi_f+\bigl(\Phi_i+\tfrac12\chi_i\bigr)\mathcal E\chi_i\Bigr],
\end{aligned}
```

因此 (4.47) 中 $`x^0=t_i,t_f`$ 处的项与 $`\Psi^*[\Phi_f]\Psi[\Phi_i]`$ 的变化相消。于是

```math
K_0^J(\mathrm{vac}_f,\mathrm{vac}_i)=K_0(\mathrm{vac}_f,\mathrm{vac}_i)\,
\exp\Bigl[-\frac12\int d^4x\,d^4y\,J(x)\Delta_F(x-y)J(y)\Bigr],
```

以及

```math
\boxed{
\begin{aligned}
Z_0[J]&:=K_0^J(\mathrm{vac}_f,\mathrm{vac}_i)
=\int\mathcal D\Phi_f\,\mathcal D\Phi_i\,\Psi^*[\Phi_f]\,\Psi[\Phi_i]\,K_0^J(\Phi_f,\Phi_i)\\
&=Z_0[0]\,\exp\Bigl[-\frac12\int d^4x\,d^4y\,J(x)\Delta_F(x-y)J(y)\Bigr],
\end{aligned}}
```

其中由 (4.52)，$`Z_0[0]=K_0(\mathrm{vac}_f,\mathrm{vac}_i)`$。

**两点函数**

对 $`S_0`$ 及 $`t_i<z_1^0,z_2^0<t_f`$，由 (4.35) 与 (4.53)，

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

**微扰展开**

由 (4.12)，每个 $`-i\,\delta/\delta J(z)`$ 作用于 (4.44) 都插入一个 $`\phi(z)`$，因此

```math
\begin{aligned}
K(\Phi_f,\Phi_i)
&=\int_{\Phi_i}^{\Phi_f}\mathcal D\phi\,\exp\Bigl(iS_0[\phi]+i\int d^4z\,\Bigl(-\frac{\lambda}{3!}\Bigr)\phi^3\Bigr)\\
&=\int_{\Phi_i}^{\Phi_f}\mathcal D\phi\,e^{iS_0[\phi]}\sum_{m=0}^\infty\frac1{m!}\Bigl(i\int d^4z\,\Bigl(-\frac{\lambda}{3!}\Bigr)\phi(z)^3\Bigr)^m\\
&=\sum_{m=0}^\infty\frac1{m!}\Bigl(-\frac{i\lambda}{3!}\Bigr)^m\prod_{k=1}^m\int d^4z_k\Bigl(-i\frac{\delta}{\delta J(z_k)}\Bigr)^3K_0^J(\Phi_f,\Phi_i)\Big|_{J=0}\\
&=\sum_{m=0}^\infty\frac1{m!}\Bigl(\frac{\lambda}{3!}\Bigr)^m\prod_{k=1}^m\int d^4z_k\Bigl(\frac{\delta}{\delta J(z_k)}\Bigr)^3K_0^J(\Phi_f,\Phi_i)\Big|_{J=0}.
\end{aligned}
```

两端都取 $`S_0`$ 的真空，由 (4.52) 得

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
### 4.4 费米子场的路径积分

<a id="grassmann-algebra"></a>
#### Grassmann 代数

**代数**

设 $`\mathbb K=\mathbb R`$ 或 $`\mathbb C`$。

- **代数**：$`\mathbb K`$ 上的向量空间 $`\mathcal A`$，带有乘积

```math
\begin{aligned}
\mathcal A\times\mathcal A&\to\mathcal A,\\
(u,v)&\mapsto uv,
\end{aligned}
```

且乘积是双线性的：对所有 $`\alpha,\beta\in\mathbb K`$ 与 $`u,v,w\in\mathcal A`$，

```math
\begin{aligned}
u(\alpha v+\beta w)&=\alpha\,uv+\beta\,uw,\\
(\alpha v+\beta w)u&=\alpha\,vu+\beta\,wu.
\end{aligned}
```

- **含幺代数**：含有元素 $`1\in\mathcal A`$ 的代数，使得对所有 $`u\in\mathcal A`$ 都有 $`1u=u=u1`$。
  - 对 $`\alpha\in\mathbb K`$，把 $`\alpha1`$ 记为 $`\alpha`$。
- **结合代数**：对所有 $`u,v,w\in\mathcal A`$ 都有 $`(uv)w=u(vw)`$ 的代数。

**生成元**

- **生成子代数**：对 $`\mathbb K`$ 上的含幺结合代数 $`\mathcal A`$ 以及元素为 $`u_a`$ 的子集 $`\Sigma\subset\mathcal A`$，由 $`\Sigma`$ 生成的子代数为

```math
\mathcal A(\Sigma):=\Bigl\{f_0+\sum_{k\ge1}\sum_{a_1,\ldots,a_k}f_{a_1\cdots a_k}\,u_{a_1}\cdots u_{a_k}\;:\;f_0,\,f_{a_1\cdots a_k}\in\mathbb K\Bigr\},
```

其中只有有限个系数非零。

- **生成集**：若 $`\mathcal A(\Sigma)=\mathcal A`$，则称 $`\Sigma`$ 为 $`\mathcal A`$ 的生成集。

**Grassmann 代数**

- **Grassmann（外）代数**：$`\mathbb K`$ 上具有生成集 $`\{\zeta_1,\ldots,\zeta_n\}`$ 的含幺结合代数，满足

```math
\zeta_a\zeta_b+\zeta_b\zeta_a=0,\qquad a,b=1,\ldots,n,
```

特别地，$`\zeta_a^2=0`$。不再附加其他关系：$`\zeta_a`$ 之间的任何关系都由 (4.60) 推出。该代数记为 $`\mathcal G(\zeta_1,\ldots,\zeta_n)`$，或 $`\mathcal G_n`$。

- **基**：有序单项式 $`1`$ 与满足 $`a_1<\cdots<a_k`$ 的 $`\zeta_{a_1}\cdots\zeta_{a_k}`$ 在 $`\mathbb K`$ 上线性无关，且

```math
\begin{aligned}
\mathcal G_n&=\mathop{\rm span}\nolimits\,_{\mathbb K}\{1,\ \zeta_{a_1}\cdots\zeta_{a_k}\mid 1\le a_1<\cdots<a_k\le n\},\\
\dim_{\mathbb K}\mathcal G_n&=2^n.
\end{aligned}
```

- **展开**：每个 $`f\in\mathcal G_n`$ 都有唯一的展开

```math
f=\sum_{k=0}^n\sum_{1\le a_1<\cdots<a_k\le n}f_{a_1\cdots a_k}\,\zeta_{a_1}\cdots\zeta_{a_k},\qquad f_{a_1\cdots a_k}\in\mathbb K,
```

其中 $`k=0`$ 的项为 $`f_0`$。

<br><br>

<a id="grassmann-calculus"></a>
#### Grassmann 代数上的微积分

<br><br>

<a id="qft-ch5"></a>
## 5. 超出标准模型的新物理



<a id="seesaw-mechanism"></a>
### 5.1 Seesaw 机制

<a id="type-i-seesaw"></a>
#### I 型 seesaw

**场与拉氏量**

在标准模型中加入 $`n`$ 个右手中微子场。

- **右手中微子**：$`N_{IR}`$，$`I=1,\ldots,n`$，是满足 $`P_RN_{IR}=N_{IR}`$ 的四分量手征旋量，并且是 $`SU(3)_c\times SU(2)_L\times U(1)_Y`$ 的单态。
- **味多重态**：$`N_R:=(N_{1R},\ldots,N_{nR})^T`$，$`\nu_L:=(\nu_{eL},\nu_{\mu L},\nu_{\tau L})^T`$。轻子双重态 $`\ell_{\alpha L}`$、带电单态 $`E_{\alpha R}`$ 与 Higgs 双重态 $`H`$ 同 3.5 节。




共轭 Higgs 双重态以及拉氏量中新增的项为

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

重复的味指标求和。Yukawa 矩阵 $`y_\nu`$ 无量纲，$`M_R`$ 的质量量纲为 1。在 3.5 节的电弱变换下，

```math
\begin{aligned}
\ell_L'&=e^{-i\theta_Y/2}U(\theta)\ell_L,
& (H^c)'&=e^{-i\theta_Y/2}U(\theta)H^c,
& N_R'&=N_R,\\
\overline{\ell_L'}\,y_\nu(H^c)'N_R'
&=\overline{\ell_L}\,y_\nu H^cN_R.
\end{aligned}
```

Majorana 项是规范不变的。由于 $`\overline{N_{IR}^c}N_{JR}=\overline{N_{JR}^c}N_{IR}`$，其味矩阵可以取为对称矩阵。

**对称性破缺后的质量项**

在幺正规范下，

```math
H=\frac1{\sqrt2}\begin{pmatrix}0\\v+h\end{pmatrix},\qquad
H^c=\frac1{\sqrt2}\begin{pmatrix}v+h\\0\end{pmatrix},\qquad
M_l=\frac v{\sqrt2}y_l,\qquad M_D:=\frac v{\sqrt2}y_\nu.
```

这里 $`v\simeq246\,\mathrm{GeV}`$，同 3.5 节。记 $`l_L:=(l_{eL},l_{\mu L},l_{\tau L})^T`$，

```math
\begin{aligned}
-\mathcal L_{\mathrm{mass}+h}
={}&\overline{l_L}M_lE_R+\overline{\nu_L}M_DN_R
+\frac12\overline{N_R^c}M_RN_R\\
&+\frac hv\left(\overline{l_L}M_lE_R+\overline{\nu_L}M_DN_R\right)
+\mathrm{h.c.}
\end{aligned}
```

利用电荷共轭恒等式

```math
\overline{\nu_L}M_DN_R=\overline{N_R^c}M_D^T\nu_L^c,
```

定义

```math
\Psi_L:=\begin{pmatrix}\nu_L\\N_R^c\end{pmatrix},\qquad
\Psi_L^c=\begin{pmatrix}\nu_L^c\\N_R\end{pmatrix},\qquad
\boxed{\mathcal M:=\begin{pmatrix}0_{3\times3}&M_D\\M_D^T&M_R\end{pmatrix}=\mathcal M^T}.
```

质量项化为

```math
-\mathcal L_{\mathrm{mass}}
=\overline{l_L}M_lE_R+\frac12\overline{\Psi_L}\,\mathcal M\Psi_L^c+\mathrm{h.c.}
```

**味基与 Takagi 分解**

对常数幺正矩阵 $`R_\ell,R_E\in U(3)`$ 与 $`R_N\in U(n)`$，把旧场用新场表示为

```math
\begin{aligned}
\ell_L&=R_\ell\ell_L',\qquad E_R=R_EE_R',\qquad N_R=R_NN_R',\\
M_l'&=R_\ell^\dagger M_lR_E,\qquad
M_D'=R_\ell^\dagger M_DR_N,\qquad
M_R'=R_N^TM_RR_N.
\end{aligned}
```

这些变换保持动能项与规范项不变。采用 3.5 节的带电轻子质量基，

```math
M_l=D_l:=\mathop{\rm diag}\nolimits (m_e,m_\mu,m_\tau).
```

由于 $`\mathcal M`$ 是复对称矩阵，存在 $`\mathcal U\in U(3+n)`$ 使得

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

其中所有质量均非负。三个轻态用 $`i=1,2,3`$ 标记，$`n`$ 个重态用 $`I=1,\ldots,n`$ 标记；轻态的标记既可按正序也可按倒序排列。场变换与对角的质量项为

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

等价地，也可以先分块对角化，再对每个块作 Takagi 对角化：

```math
\begin{aligned}
\Psi_L&=W\begin{pmatrix}\nu_L^{\mathrm b}\\(N_R^{\mathrm b})^c\end{pmatrix},\qquad
W^\dagger\mathcal MW^*=\begin{pmatrix}M_\nu&0\\0&M_N\end{pmatrix},\\
M_\nu&=UD_\nu U^T,\qquad M_N=U_ND_NU_N^T,\\
\mathcal U&=W\begin{pmatrix}U&0\\0&U_N\end{pmatrix},\qquad
W\in U(3+n),\quad U\in U(3),\quad U_N\in U(n).
\end{aligned}
```

矩阵 $`M_\nu`$ 与 $`M_N`$ 是相对于分块对角基而言的；$`M_N`$ 一般不同于原来的块 $`M_R`$。

**秩与参数计数**

活跃–活跃块为零意味着

```math
\mathcal M\begin{pmatrix}a\\0\end{pmatrix}=0
\quad\text{对 }a\in\ker M_D^T,\qquad
\mathop{\rm rank}\nolimits\,\mathcal M\le\min(2n,3+n).
```

若 $`M_R`$ 可逆，分块消元给出精确的秩恒等式

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

这一合同变换并不是幺正的质量对角化。对一般的矩阵，轻部分的秩为 $`r=\min(n,3)`$，有 $`3-r`$ 个无质量轻态。特别地，$`n=2`$ 给出最小 seesaw，在树级有一个无质量的轻中微子：

```math
m_1=0\quad\text{（正序）},\qquad
m_3=0\quad\text{（倒序）}.
```

以下计数中取 $`n\ge1`$、一般的秩以及非简并的非零质量。在商去场重定义之前，独立实参数的个数为

```math
\begin{aligned}
N(M_D)&=6n,\qquad N(M_R)=n(n+1),\qquad N(\mathcal M)=n^2+7n,\\
N(D)&=n+r=\min(2n,3+n),\\
N(\mathcal U)_{\mathrm{constrained}}
&=n^2+7n-(n+r).
\end{aligned}
```

最后一行计数的是固定 $`D`$ 时 $`\mathcal M`$ 的独立非质量参数，其中已施加零块约束并去掉了 Takagi 稳定子。它不是无约束的 $`U(3+n)`$ 矩阵的维数。

对非简并的带电轻子质量，剩余的基自由度为

```math
\begin{aligned}
\ell_L&=P\ell_L',\qquad E_R=PE_R',\qquad N_R=R_NN_R',\\
P&:=\mathop{\rm diag}\nolimits (e^{i\phi_e},e^{i\phi_\mu},e^{i\phi_\tau}),
\qquad R_N\in U(n),\\
M_D'&=P^\dagger M_DR_N,\qquad M_R'=R_N^TM_RR_N.
\end{aligned}
```

共有 $`3+n^2`$ 个冗余实参数。不计三个带电轻子质量，

```math
\boxed{
\begin{aligned}
N_{\nu,\mathrm{phys}}&=(n^2+7n)-(3+n^2)=7n-3,\\
N_{\mathrm{masses}}&=n+r,\qquad
N_{\mathrm{mixing}}=6n-r-3.
\end{aligned}
}
```

因此 $`n=2`$ 时有四个非零质量和七个混合参数，而 $`n=3`$ 时有六个质量和十二个混合参数。

**带电流与 PMNS 矩阵**

把 $`\mathcal U`$ 的上方分块记为

```math
K:=W_{11}U,\qquad R:=W_{12}U_N,\qquad
\nu_{\alpha L}=K_{\alpha i}\nu_{iL}^m+R_{\alpha I}(N_{IR}^m)^c.
```

在带电轻子质量基中，3.5 节的轻子带电流化为

```math
\boxed{
\mathcal L_{\mathrm{CC}}^\ell
=\frac{g_2}{\sqrt2}W_\mu^-
\overline{l_{\alpha L}}\gamma^\mu
\left[K_{\alpha i}\nu_{iL}^m+R_{\alpha I}(N_{IR}^m)^c\right]
+\mathrm{h.c.}
}
```

按系数定义，令 $`U_{\mathrm{PMNS}}:=K`$。由 $`\mathcal U`$ 的幺正性及其零块关系得

```math
\boxed{
\begin{aligned}
U_{\mathrm{PMNS}}U_{\mathrm{PMNS}}^\dagger
&=I_3-RR^\dagger,\\
KD_\nu K^T+RD_NR^T&=0_{3\times3}.
\end{aligned}
}
```

轻态的带电流矩阵 $`U_{\mathrm{PMNS}}`$ 一般不是幺正的；Takagi 矩阵 $`U`$ 是幺正的。

**轻–重混合的精确参数化**

选取单态的味基，使分块对角化后的重块为 $`M_N=D_N`$，从而 $`U_N=I_n`$。在 $`W_{11}`$ 可逆的坐标域内，利用分块幺正自由度写出

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

平方根取正定的厄米平方根。$`\mathcal M=W\,\mathop{\rm diag}\nolimits (M_\nu,D_N)W^T`$ 的左上块为

```math
0=A_X(M_\nu+XD_NX^T)A_X^T
\quad\Longleftrightarrow\quad
\boxed{M_\nu=-XD_NX^T=UD_\nu U^T}.
```

其余各块给出

```math
\boxed{
\begin{aligned}
M_D&=A_XXD_N(B_X^T)^{-1},\\
M_R&=B_X\left[D_N-(X^\dagger X)D_N(X^\dagger X)^T\right]B_X^T.
\end{aligned}
}
```

对正的重质量，从轻块中消去 $`X`$ 还可得到

```math
\begin{aligned}
M_\nu
&=-A_X^{-1}M_DB_X^TD_N^{-1}B_XM_D^T(A_X^T)^{-1}\\
&=-A_X^{-1}M_D
\left(M_R+X^\dagger M_D+M_D^TX^*\right)^{-1}
M_D^T(A_X^T)^{-1}.
\end{aligned}
```

这里 $`D_N`$ 是物理的重质量谱。在这组基中，$`M_R=D_N`$ 与 $`X=M_DM_R^{-1}`$ 都不是严格成立的恒等式。

**由质量与混合参数构造**

取一般的轻部分秩 $`r=\min(n,3)`$ 以及正的 $`M_I`$。设 $`P_\nu`$ 投影到 $`D_\nu`$ 的非零元上，并选取复 $`3\times n`$ 矩阵 $`O`$，满足

```math
P_\nu:=\mathop{\rm diag}\nolimits (p_1,p_2,p_3),\qquad
p_i:=\begin{cases}1,&m_i>0,\\0,&m_i=0,\end{cases}
\qquad P_\nu O=O,\qquad OO^T=P_\nu.
```

则

```math
\boxed{X=iU\sqrt{D_\nu}\,OD_N^{-1/2}},\qquad
-XD_NX^T=U\sqrt{D_\nu}\,OO^T\sqrt{D_\nu}\,U^T=UD_\nu U^T.
```

正交条件用的是转置，而不是厄米共轭。当 $`n>3`$ 时，它并不要求 $`O^TO=I_n`$。精确的重构为

```math
(D_\nu,D_N,U,O)\ \longrightarrow\ X\ \longrightarrow\ W(X)
\ \longrightarrow\
\mathcal M=W\begin{pmatrix}UD_\nu U^T&0\\0&D_N\end{pmatrix}W^T.
```

去掉三个带电轻子相位以及无质量子空间中的 $`U(3-r)`$ 自由度之后，参数计数为

```math
\begin{aligned}
N(U)&=9-(3-r)^2-3,\qquad
N(O)=2rn-r(r+1),\\
N(U)+N(O)&=6n-r-3,\qquad
(n+r)+N(U)+N(O)=7n-3.
\end{aligned}
```

对 $`n=2`$ 与正序，

```math
\begin{aligned}
D_\nu&=\mathop{\rm diag}\nolimits (0,m_2,m_3),\qquad
D_N=\mathop{\rm diag}\nolimits (M_1,M_2),\\
O(z)&=\begin{pmatrix}0&0\\\cos z&-\sin z\\\sin z&\cos z\end{pmatrix},\qquad
z\in\mathbb C,\qquad O^TO=I_2,\qquad OO^T=\mathop{\rm diag}\nolimits (0,1,1).
\end{aligned}
```

对倒序可取

```math
D_\nu=\mathop{\rm diag}\nolimits (m_1,m_2,0),\qquad
O(z)=\begin{pmatrix}\cos z&-\sin z\\\sin z&\cos z\\0&0\end{pmatrix},\qquad
OO^T=\mathop{\rm diag}\nolimits (1,1,0).
```

离散的列符号可以吸收进重 Majorana 场。对三个有质量的轻态，幺正矩阵 $`U`$ 的一种相位约定为

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

这里 $`c_{ij}:=\cos\theta_{ij}`$，$`s_{ij}:=\sin\theta_{ij}`$。

对 $`n=2`$，可以通过对无质量态重新定相去掉一个 Majorana 相位。在两种排序下都可以取 $`\rho=0`$，必要时先对带电轻子作一次共同的重新定相。因此 $`U`$ 包含三个角、一个 Dirac 相位和一个 Majorana 相位；连同复参数 $`z`$，共有七个混合参数。精确的带电流矩阵为

```math
\boxed{
\begin{aligned}
U_{\mathrm{PMNS}}&=A_XU\\
&=U\left(I_3+\sqrt{D_\nu}\,OD_N^{-1}O^\dagger\sqrt{D_\nu}\right)^{-1/2}.
\end{aligned}
}
```

**Seesaw 极限与 Casas–Ibarra 形式**

常规的 seesaw 区域中 $`M_R`$ 可逆，且

```math
\frac{\sigma_{\max}(M_D)}{\sigma_{\min}(M_R)}\ll1,\qquad
\epsilon_X:=\sigma_{\max}(X)\ll1,
```

其中 $`\sigma_{\max}`$ 与 $`\sigma_{\min}`$ 分别表示最大与最小奇异值。展开精确参数化，

```math
\begin{aligned}
A_X&=I_3-\frac12XX^\dagger+\mathcal O(\epsilon_X^4),\qquad
B_X=I_n-\frac12X^\dagger X+\mathcal O(\epsilon_X^4),\\
W&=\begin{pmatrix}I_3-\frac12XX^\dagger&X\\-X^\dagger&I_n-\frac12X^\dagger X\end{pmatrix}
+\mathcal O(\epsilon_X^3).
\end{aligned}
```

在这组基中，到领头阶，

```math
M_D\simeq XD_N,\qquad M_R\simeq D_N,\qquad
X\simeq M_DM_R^{-1}\simeq M_DD_N^{-1}.
```

因此零块恒等式给出

```math
\boxed{M_\nu=UD_\nu U^T\simeq-M_DM_R^{-1}M_D^T
\simeq-\frac{v^2}{2}\,y_\nu D_N^{-1}y_\nu^T}.
```

带电流矩阵满足

```math
\begin{aligned}
U_{\mathrm{PMNS}}&=\left(I_3-\frac12XX^\dagger\right)U+\mathcal O(\epsilon_X^4),\\
U_{\mathrm{PMNS}}U_{\mathrm{PMNS}}^\dagger
&=I_3-XX^\dagger+\mathcal O(\epsilon_X^4).
\end{aligned}
```

因此只有在忽略二阶的轻–重混合之后才有 $`U_{\mathrm{PMNS}}\simeq U`$。把 $`X`$ 的精确表达式代入 $`M_D\simeq XD_N`$，得到 Casas–Ibarra 形式，

```math
\boxed{
\begin{aligned}
M_D&\simeq iU\sqrt{D_\nu}\,O\sqrt{D_N},\qquad M_R\simeq D_N,\\
y_\nu&\simeq\frac{i\sqrt2}{v}\,U\sqrt{D_\nu}\,O\sqrt{D_N},\qquad
P_\nu O=O,\quad OO^T=P_\nu.
\end{aligned}
}
```

$`X`$ 的构造是精确的；上面 $`M_D`$ 与 $`y_\nu`$ 的表达式是领头阶近似。特别地，

```math
\epsilon_X=\sigma_{\max}\!\left(\sqrt{D_\nu}\,OD_N^{-1/2}\right).
```

由于 $`O`$ 是复正交矩阵而非幺正矩阵，仅凭 $`m_i\ll M_I`$ 并不能保证轻–重混合很小。

<br><br>

<a id="type-ii-seesaw"></a>
#### II 型 seesaw

<br><br>

<a id="type-iii-seesaw"></a>
#### III 型 seesaw

<br><br>

<a id="leptogenesis"></a>
#### 轻子生成

<br><br>

<a id="dark-matter"></a>
### 5.2 暗物质

<br><br>

<a id="qft-ch6"></a>
## 6. 散射理论

<a id="interaction-picture-dyson"></a>
<a id="perturbation-theory"></a>
<a id="interaction-picture"></a>
### 6.1 相互作用绘景

设哈密顿量为

```math
\hat H=\hat H_0+\hat V
```

相互作用绘景用 (6.1) 中的 $`\hat H_0`$ 而不是 $`\hat H`$ 来演化算符：

```math
\boxed{
\begin{gathered}
\hat O_I(t):=e^{i\hat H_0t}\,\hat O_S\,e^{-i\hat H_0t},\\[4pt]
|\psi_I(t)\rangle:=e^{i\hat H_0t}\,|\psi_S(t)\rangle .
\end{gathered}
}
```

三个绘景在 $`t=0`$ 时重合，且 $`\langle\psi_I(t)|\hat O_I(t)|\psi_I(t)\rangle=\langle\psi_S(t)|\hat O_S|\psi_S(t)\rangle`$。

对 (6.2) 的第一式求导，

```math
\frac{d\hat O_I}{dt}=i\,[\hat H_0,\hat O_I].
```

特别地，$`\hat H_{0,I}=\hat H_0`$，而相互作用项变为含时的。对 (6.2) 的第二式求导，并利用 $`i\partial_t|\psi_S\rangle=\hat H|\psi_S\rangle`$，

```math
i\partial_t|\psi_I(t)\rangle
=e^{i\hat H_0t}\bigl(\hat H-\hat H_0\bigr)|\psi_S(t)\rangle
=e^{i\hat H_0t}\hat Ve^{-i\hat H_0t}\,|\psi_I(t)\rangle,
```

即

```math
\boxed{
i\partial_t|\psi_I(t)\rangle=\hat V_I(t)\,|\psi_I(t)\rangle,
\qquad
\hat V_I(t):=e^{i\hat H_0t}\,\hat V\,e^{-i\hat H_0t}.
}
```

把 $`\hat O_S=e^{-i\hat H_0t}\hat O_I(t)e^{i\hat H_0t}`$ 代入 (2.22)，

```math
\hat O_H(t)=\hat U_I(t,0)^\dagger\,\hat O_I(t)\,\hat U_I(t,0),
\qquad
\hat U_I(t,0):=e^{i\hat H_0t}\,\hat U(t,0).
```

对场算符，(6.6) 写作 $`\hat\phi_H(t,\mathbf x)=\hat U_I(t,0)^\dagger\,\hat\phi_I(t,\mathbf x)\,\hat U_I(t,0)`$，且由 (6.3)，$`\hat\phi_I(t,\mathbf x)`$ 满足仅由 $`\hat H_0`$ 给出的 Heisenberg 方程。

**Dyson 级数**

态方程 (6.5) 就是把 (2.13) 第二行中的 $`\hat H`$ 换成 $`\hat V_I(t)`$ 所得的方程。因此，由 $`|\psi_I(t)\rangle=\hat U_I(t,t_0)|\psi_I(t_0)\rangle`$ 定义的相互作用绘景演化算符 $`\hat U_I(t,t_0)`$，就是在 (2.21) 的 $`\hat U(t,t_0)`$ 中作替换 $`\hat H\to\hat V_I(t)`$ 所得的算符：它是幺正的，满足 $`\hat U_I(t_1,t_2)\hat U_I(t_2,t_3)=\hat U_I(t_1,t_3)`$，且 $`\hat U_I(t,t_0)^\dagger=\hat U_I(t_0,t)`$。由 (6.2) 与 (2.21)，

```math
\hat U_I(t,t_0)=e^{i\hat H_0t}\,\hat U(t,t_0)\,e^{-i\hat H_0t_0},
```

上式在 $`t_0=0`$ 时化为 (6.6) 中的 $`\hat U_I(t,0)`$；当 $`\hat H`$ 不显含时间时，由 (2.14)，$`\hat U(t,t_0)=e^{-i\hat H(t-t_0)}`$。由于一般有 $`[\hat V_I(t_1),\hat V_I(t_2)]\neq0`$，适用 [2.4 节](QFT-zh-part-02.md#symmetry) 的情况 (3)，由 (2.20) 得

```math
\boxed{
\hat U_I(t,t_0)=\mathcal T\exp\Bigl(-i\int_{t_0}^{t}dt'\,\hat V_I(t')\Bigr).
}
```

在场论中，$`\hat V=\int d^3x\,\hat{\mathcal H}_{\mathrm{int}}\bigl(\hat\phi_S(\mathbf x)\bigr)`$。由 (6.2)，$`\hat V_I(t)=\int d^3x\,\hat{\mathcal H}_{\mathrm{int}}\bigl(\hat\phi_I(t,\mathbf x)\bigr)`$，于是 (6.8) 化为

```math
\hat U_I(t,t_0)=\mathcal T\exp\Bigl(-i\int_{t_0}^{t}dt'\int d^3x\,\hat{\mathcal H}_{\mathrm{int}}\bigl(\hat\phi_I(x)\bigr)\Bigr).
```

对不含导数耦合的相互作用，$`\hat{\mathcal H}_{\mathrm{int}}=-\hat{\mathcal L}_{\mathrm{int}}`$。

<br><br>

<a id="s-matrix-and-wick-theorem"></a>
### 6.2 S 矩阵与 Wick 定理

**渐近态与 S 矩阵**

假设渐近粒子是稳定的，且自由粒子波包极限存在。入态在 $`t\to-\infty`$ 时趋于相应的自由态，出态在 $`t\to+\infty`$ 时趋于相应的自由态。在微扰论中，采用绝热开关并去掉真空相位，

```math
\begin{aligned}
S_{fi}&:=\langle f,\mathrm{out}|i,\mathrm{in}\rangle=\langle f|\hat S|i\rangle,\\
\hat S&=\hat U_I(+\infty,-\infty)
=\mathcal T\exp\left(-i\int_{-\infty}^{+\infty}dt\,\hat V_I(t)\right).
\end{aligned}
```

设 $`p_i`$ 与 $`p_f`$ 分别为初态与末态的总四动量。连通不变振幅 $`\mathcal M_{fi}`$ 与跃迁算符 $`\hat T`$ 由下式定义

```math
\boxed{\begin{aligned}
\hat S&=1+i\hat T,\qquad
\langle f|\hat T|i\rangle_{\mathrm c}=(2\pi)^4\delta^{(4)}(p_f-p_i)\,\mathcal M_{fi},\\
\hat S^\dagger\hat S&=1\quad\Longrightarrow\quad -i(\hat T-\hat T^\dagger)=\hat T^\dagger\hat T.
\end{aligned}}
```

**正规序、收缩与 Wick 定理**

正规序相对于自由真空 $`|0\rangle`$ 定义。对自由实标量场，其收缩即费曼传播子；默认 $`\varepsilon\to0^+`$：

```math
\begin{aligned}
\Delta_F(x-y)&:=\langle0|\mathcal T[\hat\phi_I(x)\hat\phi_I(y)]|0\rangle\\
&=\mathcal T[\hat\phi_I(x)\hat\phi_I(y)]-:\hat\phi_I(x)\hat\phi_I(y):\\
&=\int\frac{d^4p}{(2\pi)^4}\,\frac{i\,e^{-ip\cdot(x-y)}}{p^2-m^2+i\varepsilon}.
\end{aligned}
```

Wick 定理把自由场的编时乘积表示为对所有不相交收缩的求和，其中包括不作任何收缩的项。记 $`\hat\phi_j:=\hat\phi_I(x_j)`$，

```math
\begin{aligned}
\mathcal T[\hat\phi_1\cdots\hat\phi_n]
&=\sum_{\text{不相交配对 }P}
\left[\prod_{(i,j)\in P}\Delta_F(x_i-x_j)\right]
:\prod_{k\text{ 在 }P\text{ 中未配对}}\hat\phi_k:,\\
\langle0|\mathcal T[\hat\phi_1\hat\phi_2\hat\phi_3\hat\phi_4]|0\rangle
&=\Delta_F(x_1-x_2)\Delta_F(x_3-x_4)
+\Delta_F(x_1-x_3)\Delta_F(x_2-x_4)\\
&\quad+\Delta_F(x_1-x_4)\Delta_F(x_2-x_3).
\end{aligned}
```

对费米子，编时与 Wick 收缩都要带上重排费米子算符所需置换的符号。自由真空期望值只保留完全收缩的项。


<br><br>

<a id="feynman-diagrams"></a>
### 6.3 费曼图与费曼规则

**标量的例子**

对四次耦合为 $`\lambda`$ 的实标量场，动量空间中的规则给出对 $`i\mathcal M`$ 的贡献。树级下，

```math
\begin{aligned}
\mathcal L&=\frac12\partial_\mu\phi\,\partial^\mu\phi-\frac12m^2\phi^2-\frac{\lambda}{4!}\phi^4,\qquad
\hat{\mathcal H}_{\mathrm{int}}=\frac{\lambda}{4!}\hat\phi_I^4,\\
\text{标量内线}:&\quad\widetilde\Delta_F(p)=\frac{i}{p^2-m^2+i\varepsilon},\qquad
\text{四标量顶点}:\quad -i\lambda,\\
 i\mathcal M_{\phi\phi\to\phi\phi}^{\mathrm{tree}}&=-i\lambda.
\end{aligned}
```

**传播子与外态**

定义 $`S_F(x-y):=\langle0|\mathcal T[\hat\psi_I(x)\overline{\hat\psi}_I(y)]|0\rangle`$ 与 $`D_{\mu\nu}(x-y):=\langle0|\mathcal T[\hat A_{I,\mu}(x)\hat A_{I,\nu}(y)]|0\rangle`$，其 Fourier 变换为

```math
\begin{aligned}
\widetilde S_F(p)&=\frac{i(\not p+m)}{p^2-m^2+i\varepsilon},\\
\widetilde D_{\mu\nu}^{(\xi)}(p)&=\frac{-i}{p^2+i\varepsilon}\left[\eta_{\mu\nu}-(1-\xi)\frac{p_\mu p_\nu}{p^2+i\varepsilon}\right],
\qquad \mathcal L_{\mathrm{gf}}=-\frac1{2\xi}(\partial_\mu A^\mu)^2,\\
\widetilde D_{\mu\nu}^{\mathrm{Proca}}(p)&=\frac{-i}{p^2-m_V^2+i\varepsilon}\left(\eta_{\mu\nu}-\frac{p_\mu p_\nu}{m_V^2}\right),\qquad m_V>0.
\end{aligned}
```

其中 $`\xi`$ 为协变规范参数（$`\xi=1`$ 为费曼规范），$`m_V`$ 为 Proca 质量。对单粒子极点留数为 1 的场，外态因子为

```math
\begin{array}{c|cc}
\text{外态}&\text{入射}&\text{出射}\\ \hline
\text{标量}&1&1\\
\text{费米子}&u^s(p)&\bar u^s(p)\\
\text{反费米子}&\bar v^s(p)&v^s(p)\\
\text{矢量}&\epsilon_\mu^r(p)&\epsilon_\mu^{r*}(p)
\end{array}
```

$`\epsilon_\mu^r`$ 为物理偏振矢量。外传播子被截去；对一般的场归一化，需要用到 [6.5 节](QFT-zh-part-04.md#lsz-reduction) 中的极点留数因子。

**图的规则**

在每个顶点施加四动量守恒，每个独立圈动量用 $`d^4\ell/(2\pi)^4`$ 积分，并对连通截肢图求和。去掉整体因子 $`(2\pi)^4\delta^{(4)}(p_f-p_i)`$，即得 $`i\mathcal M`$。每个图都要除以外腿固定时的对称因子。每个闭合费米子圈额外贡献一个负号；交换全同的外费米子也改变符号。

例如，$`s`$ 道单圈四标量图的对称因子为 $`2`$：

```math
i\mathcal M_s^{\mathrm{1\,loop}}
=\frac{(-i\lambda)^2}{2}\int\frac{d^4\ell}{(2\pi)^4}
\frac{i}{\ell^2-m^2+i\varepsilon}
\frac{i}{(\ell+p_1+p_2)^2-m^2+i\varepsilon},
\qquad s:=(p_1+p_2)^2.
```

圈积分需要正规子，在重整化的振幅中还需要相应的反项。完整的单圈四点振幅也包含交叉道。


<br><br>

<a id="correlation-functions"></a>
### 6.4 关联函数

<a id="perturbative-correlation-functions"></a>
#### 微扰真空关联函数

**真空关联函数**

设 $`|\Omega\rangle`$ 为相互作用真空，$`|0\rangle`$ 为自由真空。

```math
\begin{aligned}
G_n(x_1,\ldots,x_n)&:=\frac{\langle\Omega|\mathcal T[\hat\phi_H(x_1)\cdots\hat\phi_H(x_n)]|\Omega\rangle}{\langle\Omega|\Omega\rangle}\\
&=\frac{\langle0|\mathcal T\left[\hat\phi_I(x_1)\cdots\hat\phi_I(x_n)\exp\left(-i\int dt\,\hat V_I(t)\right)\right]|0\rangle}
{\langle0|\mathcal T\exp\left(-i\int dt\,\hat V_I(t)\right)|0\rangle}.
\end{aligned}
```

分母消去不连通的真空泡。若每个连通分支都带有外部场插入，对 $`G_n`$ 有贡献的图仍可以是不连通的。

**生成泛函与连通函数**

对实标量源 $`J(x)`$，

```math
\begin{aligned}
Z[J]&:=\frac{\langle\Omega|\mathcal T\exp\left(i\int d^4x\,J(x)\hat\phi_H(x)\right)|\Omega\rangle}{\langle\Omega|\Omega\rangle},\qquad Z[0]=1,\qquad W[J]:=-i\ln Z[J],\\
G_n(x_1,\ldots,x_n)&=\left.\frac1{i^n}\frac{\delta^nZ[J]}{\delta J(x_1)\cdots\delta J(x_n)}\right|_{J=0},\\
G_{n,\mathrm c}(x_1,\ldots,x_n)&=\left.i^{1-n}\frac{\delta^nW[J]}{\delta J(x_1)\cdots\delta J(x_n)}\right|_{J=0}.
\end{aligned}
```

当 $`G_1=0`$ 时，四点函数按下式分解为连通贡献与不连通贡献

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

<a id="nonperturbative-correlation-functions"></a>
#### 非微扰真空关联函数





<br><br>

