> 中文版第 4/4 部分 · [完整文件](QFT-zh.md) · [1](QFT-zh-part-01.md) · [2](QFT-zh-part-02.md) · [3](QFT-zh-part-03.md) · [4](QFT-zh-part-04.md)

<a id="electroweak-gauge-theory"></a>
<a id="electroweak-theory"></a>
### 5.5 电弱理论

<a id="sm-leptons"></a>
#### 标准模型中的轻子

电弱理论的规范群为 $`SU(2)_L\times U(1)_Y`$。在 $`SU(2)_L`$ 双重态上 $`T^a:=\sigma^a/2`$，$`a=1,2,3`$；在 $`SU(2)_L`$ 单态上 $`T^a:=0`$。超荷为 $`Y`$ 的场 $`\psi`$ 的变换为

```math
\left.
\begin{aligned}
\psi'(x)&=e^{i\theta^a(x)T^a+i\theta_Y(x)Y}\,\psi(x),\qquad \theta^a(x),\ \theta_Y(x)\in\mathbb R,\\
Q&:=T^3+Y,
\end{aligned}
\right.
\tag{5.68}
```

其中 $`Q`$ 是以 $`e`$ 为单位的电荷，与 (5.23) 相同。

轻子分为三代，用味指标 $`\alpha=e,\mu,\tau`$ 标记。以下有序对的含义为（$`SU(2)_L`$ 表示，$`Y`$），

```math
\left.
\boxed{
\begin{aligned}
\ell_{\alpha L}&:=\begin{pmatrix}\nu_{\alpha L}\\ l_{\alpha L}\end{pmatrix}\sim\Bigl(\mathbf2,-\frac12\Bigr),\qquad
E_{\alpha R}\sim(\mathbf1,-1),\\
Q\,\nu_{\alpha L}&=0,\qquad Q\,l_{\alpha L}=-l_{\alpha L},\qquad Q\,E_{\alpha R}=-E_{\alpha R}.
\end{aligned}
}
\right.
\tag{5.69}
```

这些场都是四分量旋量，满足 $`P_L\nu_{\alpha L}=\nu_{\alpha L}`$、$`P_Ll_{\alpha L}=l_{\alpha L}`$ 与 $`P_RE_{\alpha R}=E_{\alpha R}`$，其中 $`P_{L,R}`$ 由 (1.137) 给出。轻子是色单态。最小可重整化标准模型不含右手中微子。

<br><br>

<a id="electroweak-kinetic-terms"></a>
#### 动能项

设 $`W_\mu^a`$，$`a=1,2,3`$，与 $`B_\mu`$ 分别为 $`SU(2)_L`$ 与 $`U(1)_Y`$ 的实规范场，$`g_2,g_1>0`$ 为相应的耦合。令 $`U(\theta):=e^{i\theta^a(x)\sigma^a/2}`$，$`W_\mu:=W_\mu^a\sigma^a/2`$，由 (5.19) 取 $`g_{\mathrm{YM}}\to g_2`$、(5.24) 取 $`eQ\to g_1Y`$，得

```math
\left.
\boxed{
\begin{aligned}
D_\mu&:=\partial_\mu-ig_2W_\mu^aT^a-ig_1YB_\mu,\\
W_\mu'&=U(\theta)W_\mu U(\theta)^\dagger-\frac i{g_2}\bigl(\partial_\mu U(\theta)\bigr)U(\theta)^\dagger,\qquad
B_\mu'=B_\mu+\frac1{g_1}\partial_\mu\theta_Y,
\end{aligned}
}
\right.
\tag{5.70}
```

使得在 (5.68) 下 $`D_\mu'\psi'=e^{i\theta^aT^a+i\theta_YY}D_\mu\psi`$。场强为

```math
\left.
\begin{aligned}
W_{\mu\nu}^a&:=\partial_\mu W_\nu^a-\partial_\nu W_\mu^a+g_2\epsilon^{abc}W_\mu^bW_\nu^c,\qquad
B_{\mu\nu}:=\partial_\mu B_\nu-\partial_\nu B_\mu,\\
[D_\mu,D_\nu]&=-ig_2W_{\mu\nu}^aT^a-ig_1YB_{\mu\nu}.
\end{aligned}
\right.
\tag{5.71}
```

作用在轻子场 (5.69) 上，协变导数 (5.70) 为

```math
\left.
D_\mu\ell_{\alpha L}=\Bigl(\partial_\mu-ig_2W_\mu^a\frac{\sigma^a}2+\frac i2g_1B_\mu\Bigr)\ell_{\alpha L},\qquad
D_\mu E_{\alpha R}=\bigl(\partial_\mu+ig_1B_\mu\bigr)E_{\alpha R}.
\right.
\tag{5.72}
```

拉氏量密度的动能项为

```math
\left.
\boxed{
\begin{aligned}
\mathcal L_{\mathrm{kin}}
={}&-\frac14W_{\mu\nu}^aW^{a\mu\nu}-\frac14B_{\mu\nu}B^{\mu\nu}\\
&+\sum_{\alpha=e,\mu,\tau}\Bigl(\overline{\ell_{\alpha L}}\,i\gamma^\mu D_\mu\ell_{\alpha L}
+\overline{E_{\alpha R}}\,i\gamma^\mu D_\mu E_{\alpha R}\Bigr).
\end{aligned}
}
\right.
\tag{5.73}
```

由 (5.20)、(5.24) 与 (5.70)，$`\mathcal L_{\mathrm{kin}}`$ 是规范不变的。

<br><br>

<a id="charged-lepton-masses"></a>
#### Yukawa 耦合与带电轻子质量

Higgs 双重态 $`H=:(H^+,H^0)^T\sim(\mathbf2,\frac12)`$ 是色单态。它就是 (5.52) 中取 $`n=2`$ 且 $`\mu_H^2>0`$、并把 $`\partial_\mu`$ 换成 (5.70) 后的 $`\Phi`$。当 $`\theta^a`$ 与 $`\theta_Y`$ 变化时，$`e^{i\theta^a\sigma^a/2+i\theta_Y/2}`$ 取遍 $`U(2)`$，因此由 (5.56)、(5.60) 与 (5.66) 得

```math
\left.
\begin{aligned}
\mathcal L_H&=(D_\mu H)^\dagger D^\mu H-V(H),\qquad
V(H)=-\mu_H^2H^\dagger H+\lambda_H(H^\dagger H)^2,\\
\langle H\rangle&=\frac1{\sqrt2}\begin{pmatrix}0\\v_{\mathrm{SM}}\end{pmatrix},\qquad Q\langle H\rangle=0,\qquad
H\big|_{\mathrm{unitary\ gauge}}=\frac1{\sqrt2}\begin{pmatrix}0\\v_{\mathrm{SM}}+h\end{pmatrix}.
\end{aligned}
\right.
\tag{5.74}
```

Higgs 场 $`h`$ 的质量为 (5.64) 的 $`m_h`$。

设 $`Y_l`$ 为复 $`3\times3`$ 矩阵；重复的味指标 $`\alpha,\beta`$ 求和。轻子 Yukawa 耦合在 (5.68) 下不变：

```math
\left.
\begin{aligned}
\mathcal L_Y^\ell&=-\overline{\ell_{\alpha L}}\,(Y_l)_{\alpha\beta}\,H\,E_{\beta R}+\mathrm{h.c.},\qquad
\overline{\ell_{\alpha L}}H=\overline{\nu_{\alpha L}}H^++\overline{l_{\alpha L}}H^0,\\
\overline{\ell_{\alpha L}'}H'E_{\beta R}'
&=\overline{\ell_{\alpha L}}\,e^{\frac i2\theta_Y}U(\theta)^\dagger\;e^{\frac i2\theta_Y}U(\theta)H\;e^{-i\theta_Y}E_{\beta R}
=\overline{\ell_{\alpha L}}HE_{\beta R}.
\end{aligned}
\right.
\tag{5.75}
```

在幺正规范 (5.74) 下，$`H^+=0`$，且

```math
\left.
\mathcal L_Y^\ell=-\Bigl(1+\frac h{v_{\mathrm{SM}}}\Bigr)\overline{l_{\alpha L}}\,(M_l)_{\alpha\beta}\,E_{\beta R}+\mathrm{h.c.},\qquad
M_l:=\frac{v_{\mathrm{SM}}}{\sqrt2}\,Y_l .
\right.
\tag{5.76}
```

中微子 $`\nu_{\alpha L}`$ 不出现在 (5.76) 中。

**味基**

在味空间中记 $`\ell_L:=(\ell_{eL},\ell_{\mu L},\ell_{\tau L})^T`$，$`E_R:=(E_{eR},E_{\mu R},E_{\tau R})^T`$。对常数 $`R_\ell,R_E\in U(3)`$，(5.73) 在下面第一行的基变换下不变；$`M_l`$ 的奇异值分解按第二行确定 $`R_\ell`$ 与 $`R_E`$：

```math
\left.
\begin{aligned}
\ell_L&\to R_\ell\,\ell_L,\qquad E_R\to R_E\,E_R,\qquad Y_l\to R_\ell^\dagger\,Y_l\,R_E,\\
R_\ell^\dagger M_lR_E&=\mathop{\rm diag}\nolimits (m_e,m_\mu,m_\tau),\qquad m_\alpha\ge0 .
\end{aligned}
\right.
\tag{5.77}
```

此后采用这组基。用 Dirac 场 $`l_\alpha:=l_{\alpha L}+E_{\alpha R}`$，(5.76) 化为

```math
\left.
\boxed{
\begin{aligned}
M_l&=\mathop{\rm diag}\nolimits (m_e,m_\mu,m_\tau),\\
\mathcal L_Y^\ell&=-\sum_{\alpha=e,\mu,\tau}m_\alpha\Bigl(1+\frac h{v_{\mathrm{SM}}}\Bigr)\bar l_\alpha l_\alpha .
\end{aligned}
}
\right.
\tag{5.78}
```

由于 $`\overline{l_{\alpha L}}\,i\gamma^\mu\partial_\mu l_{\alpha L}+\overline{E_{\alpha R}}\,i\gamma^\mu\partial_\mu E_{\alpha R}=\bar l_\alpha\,i\gamma^\mu\partial_\mu l_\alpha`$，(5.73) 的自由部分与 (5.78) 合起来包含每个 $`l_\alpha`$ 的 Dirac 拉氏量 (1.100)，质量为 $`m_\alpha`$。因此带电轻子 $`l_e,l_\mu,l_\tau`$ 是质量为 $`m_e,m_\mu,m_\tau`$ 的 Dirac 场，以强度 $`m_\alpha/v_{\mathrm{SM}}`$ 与 $`h`$ 耦合，而中微子 $`\nu_{\alpha L}`$ 仍无质量。

<br><br>

<a id="gauge-boson-masses"></a>
#### 规范玻色子质量

把 (5.74) 中幺正规范下的 $`H`$ 代入 (5.70)，取 $`T^a=\sigma^a/2`$，$`Y=\frac12`$，

```math
\left.
\begin{aligned}
D_\mu H&=\frac1{\sqrt2}\begin{pmatrix}-\frac i2g_2\bigl(W_\mu^1-iW_\mu^2\bigr)(v_{\mathrm{SM}}+h)\\ \partial_\mu h+\frac i2\bigl(g_2W_\mu^3-g_1B_\mu\bigr)(v_{\mathrm{SM}}+h)\end{pmatrix},\\
(D_\mu H)^\dagger D^\mu H&=\frac12\partial_\mu h\,\partial^\mu h
+\frac{(v_{\mathrm{SM}}+h)^2}8\Bigl[g_2^2\bigl(W_\mu^1W^{1\mu}+W_\mu^2W^{2\mu}\bigr)\\
&\qquad+\bigl(g_2W_\mu^3-g_1B_\mu\bigr)\bigl(g_2W^{3\mu}-g_1B^\mu\bigr)\Bigr].
\end{aligned}
\right.
\tag{5.79}
```

定义

```math
\left.
\begin{aligned}
W_\mu^\pm&:=\frac{W_\mu^1\mp iW_\mu^2}{\sqrt2},\qquad
\tan\theta_W:=\frac{g_1}{g_2},\qquad
s_W:=\sin\theta_W,\qquad c_W:=\cos\theta_W,\\
Z_\mu&:=c_WW_\mu^3-s_WB_\mu,\qquad
A_\mu^{\mathrm{em}}:=s_WW_\mu^3+c_WB_\mu,\qquad
e:=g_2s_W=g_1c_W .
\end{aligned}
\right.
\tag{5.80}
```

于是 $`W_\mu^1W^{1\mu}+W_\mu^2W^{2\mu}=2W_\mu^+W^{-\mu}`$，$`g_2W_\mu^3-g_1B_\mu=\sqrt{g_2^2+g_1^2}\,Z_\mu`$，因此

```math
\left.
\boxed{
\begin{aligned}
(D_\mu H)^\dagger D^\mu H&=\frac12\partial_\mu h\,\partial^\mu h
+\Bigl(1+\frac h{v_{\mathrm{SM}}}\Bigr)^2\Bigl(m_W^2W_\mu^+W^{-\mu}+\frac12m_Z^2Z_\mu Z^\mu\Bigr),\\
m_W&=\frac{g_2v_{\mathrm{SM}}}2,\qquad
m_Z=\frac{v_{\mathrm{SM}}}2\sqrt{g_2^2+g_1^2}=\frac{m_W}{c_W},\qquad
m_\gamma=0,\\
\frac{G_F}{\sqrt2}&=\frac{g_2^2}{8m_W^2}=\frac1{2v_{\mathrm{SM}}^2}.
\end{aligned}
}
\right.
\tag{5.81}
```

$`A_\mu^{\mathrm{em}}`$ 不出现在 (5.81) 中。

<br><br>

<a id="sm-quarks"></a>
#### 夸克

夸克分为三代，$`r=1,2,3`$，并且与 (5.32) 一样是色三重态。有序对的含义同 (5.69)，

```math
\left.
\begin{aligned}
q_{rL}&:=\begin{pmatrix}u_{rL}\\ d_{rL}\end{pmatrix}\sim\Bigl(\mathbf2,\frac16\Bigr),\qquad
u_{rR}\sim\Bigl(\mathbf1,\frac23\Bigr),\qquad
d_{rR}\sim\Bigl(\mathbf1,-\frac13\Bigr),\\
Q\,u_{rL}&=\frac23u_{rL},\qquad Q\,d_{rL}=-\frac13d_{rL}.
\end{aligned}
\right.
\tag{5.82}
```

取 (5.70) 的 $`D_\mu`$ 再加上 (5.36) 的胶子项 $`-ig_sA_\mu`$，夸克动能项为

```math
\left.
\mathcal L_{\mathrm{kin}}^q=\sum_{r=1}^3\Bigl(\overline{q_{rL}}\,i\gamma^\mu D_\mu q_{rL}
+\overline{u_{rR}}\,i\gamma^\mu D_\mu u_{rR}
+\overline{d_{rR}}\,i\gamma^\mu D_\mu d_{rR}\Bigr).
\right.
\tag{5.83}
```

设 $`y_u,y_d`$ 为复 $`3\times3`$ 矩阵，$`H^c:=i\sigma^2H^*\sim(\mathbf2,-\frac12)`$，并在味空间中记 $`u_L:=(u_{1L},u_{2L},u_{3L})^T`$，$`u_R`$、$`d_L`$、$`d_R`$ 类似。对 $`r,s`$ 求和，夸克 Yukawa 耦合是规范不变的；在幺正规范 (5.74) 下，

```math
\left.
\begin{aligned}
\mathcal L_Y^q&=-\overline{q_{rL}}\,(y_d)_{rs}\,H\,d_{sR}-\overline{q_{rL}}\,(y_u)_{rs}\,H^c\,u_{sR}+\mathrm{h.c.},\qquad
H^c\big|_{\mathrm{unitary\ gauge}}=\frac1{\sqrt2}\begin{pmatrix}v_{\mathrm{SM}}+h\\0\end{pmatrix},\\
\mathcal L_Y^q&=-\Bigl(1+\frac h{v_{\mathrm{SM}}}\Bigr)\bigl(\overline{u_L}\,M_u\,u_R+\overline{d_L}\,M_d\,d_R\bigr)+\mathrm{h.c.},\qquad
M_{u,d}:=\frac{v_{\mathrm{SM}}}{\sqrt2}\,y_{u,d}.
\end{aligned}
\right.
\tag{5.84}
```

**质量基与 CKM 矩阵**

由 $`M_u`$ 与 $`M_d`$ 的奇异值分解选定幺正矩阵 $`R_{uL},R_{uR},R_{dL},R_{dR}`$，按下式定义质量基中的场 $`u'`$、$`d'`$

```math
\left.
\boxed{
\begin{aligned}
u_{L,R}&=R_{uL,R}\,u_{L,R}',\qquad d_{L,R}=R_{dL,R}\,d_{L,R}',\\
R_{uL}^\dagger M_uR_{uR}&=\mathop{\rm diag}\nolimits (m_u,m_c,m_t),\qquad
R_{dL}^\dagger M_dR_{dR}=\mathop{\rm diag}\nolimits (m_d,m_s,m_b),\\
u_L'+u_R'&=(q_u,q_c,q_t)^T,\qquad d_L'+d_R'=(q_d,q_s,q_b)^T,\qquad
V_{\mathrm{CKM}}:=R_{uL}^\dagger R_{dL},\\
\mathcal L_Y^q&=-\sum_fm_f\Bigl(1+\frac h{v_{\mathrm{SM}}}\Bigr)\bar q_fq_f ,
\end{aligned}
}
\right.
\tag{5.85}
```

其中 $`m_f\ge0`$；$`q_f`$ 是 (5.32) 的夸克场，$`m_f`$ 是 (5.45) 中的质量。

<br><br>

<a id="electroweak-currents"></a>
#### 带电流与中性流

$`\bar\psi\,i\gamma^\mu D_\mu\psi`$ 中含规范场的项为 $`\bar\psi\gamma^\mu(g_2W_\mu^aT^a+g_1YB_\mu)\psi`$。由 (5.80)，记 $`T^\pm:=T^1\pm iT^2`$，

```math
\left.
g_2W_\mu^aT^a+g_1YB_\mu
=\frac{g_2}{\sqrt2}\bigl(W_\mu^+T^++W_\mu^-T^-\bigr)
+eQA_\mu^{\mathrm{em}}
+\frac{g_2}{c_W}\bigl(T^3-s_W^2Q\bigr)Z_\mu .
\right.
\tag{5.86}
```

由于 $`\overline{\ell_{\alpha L}}\gamma^\mu T^+\ell_{\alpha L}=\overline{\nu_{\alpha L}}\gamma^\mu l_{\alpha L}`$，且由 (5.85)，$`\overline{q_{rL}}\gamma^\mu T^+q_{rL}=\overline{u_L}\gamma^\mu d_L=\overline{u_L'}\gamma^\mu V_{\mathrm{CKM}}\,d_L'`$，记 $`q_{fL}:=P_Lq_f`$，并分别用 $`f=u,c,t`$ 与 $`f'=d,s,b`$ 标记 $`V:=V_{\mathrm{CKM}}`$ 的行与列，则 (5.73) 与 (5.83) 中的 $`W_\mu^\pm`$ 项为：

```math
\left.
\boxed{
\mathcal L_{\mathrm{CC}}
=\frac{g_2}{\sqrt2}\,W_\mu^+\Bigl(\sum_{\alpha=e,\mu,\tau}\overline{\nu_{\alpha L}}\gamma^\mu l_{\alpha L}
+\sum_{f=u,c,t}\ \sum_{f'=d,s,b}V_{ff'}\,\overline{q_{fL}}\gamma^\mu q_{f'L}\Bigr)+\mathrm{h.c.}
}
\right.
\tag{5.87}
```

设 $`\psi_f`$ 为 (5.23) 中费米子 $`f`$ 在基 (5.77) 与 (5.85) 下的场：对夸克 $`\psi_f=q_f`$，对 $`f=e,\mu,\tau`$ 有 $`\psi_f=l_f`$，并且 $`\psi_{\nu_\alpha}=\nu_{\alpha L}`$。设 $`T_f^3`$ 为其左手部分的 $`T^3`$：对 $`q_u,q_c,q_t`$ 与 $`\nu_{\alpha L}`$ 为 $`+\frac12`$，对 $`q_d,q_s,q_b`$ 与 $`l_\alpha`$ 为 $`-\frac12`$。$`A_\mu^{\mathrm{em}}`$ 项与 $`Z_\mu`$ 项为

```math
\left.
\boxed{
\begin{aligned}
\mathcal L_{\mathrm{NC}}
={}&eA_\mu^{\mathrm{em}}\sum_fQ_f\,\bar\psi_f\gamma^\mu\psi_f\\
&+\frac{g_2}{c_W}Z_\mu\sum_f\bar\psi_f\gamma^\mu\bigl(T_f^3P_L-Q_fs_W^2\bigr)\psi_f .
\end{aligned}
}
\right.
\tag{5.88}
```

第一行就是 (5.26) 中取 $`A_\mu=A_\mu^{\mathrm{em}}`$ 的相互作用项。中性流在树级是味对角的。


<br><br>

<a id="qft-ch6"></a>
## 6. 超出标准模型的新物理



<a id="seesaw-mechanism"></a>
### 6.1 Seesaw 机制

<a id="type-i-seesaw"></a>
#### I 型 seesaw

**场与拉氏量**

在标准模型中加入 $`n`$ 个右手中微子场。

- **右手中微子**：$`N_{IR}`$，$`I=1,\ldots,n`$，是满足 $`P_RN_{IR}=N_{IR}`$ 的四分量手征旋量，并且是 $`SU(3)_c\times SU(2)_L\times U(1)_Y`$ 的单态。
- **味多重态**：$`N_R:=(N_{1R},\ldots,N_{nR})^T`$，$`\nu_L:=(\nu_{eL},\nu_{\mu L},\nu_{\tau L})^T`$。轻子双重态 $`\ell_{\alpha L}`$、带电单态 $`E_{\alpha R}`$ 与 Higgs 双重态 $`H`$ 同 5.5 节。




共轭 Higgs 双重态以及拉氏量中新增的项为

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

重复的味指标求和。Yukawa 矩阵 $`Y_\nu`$ 无量纲，$`M_R`$ 的质量量纲为 1。在 5.5 节的电弱变换下，

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

Majorana 项是规范不变的。由于 $`\overline{N_{IR}^c}N_{JR}=\overline{N_{JR}^c}N_{IR}`$，其味矩阵可以取为对称矩阵。

**对称性破缺后的质量项**

在幺正规范下，

```math
\left.
H=\frac1{\sqrt2}\begin{pmatrix}0\\v_{\mathrm{SM}}+h\end{pmatrix},\qquad
H^c=\frac1{\sqrt2}\begin{pmatrix}v_{\mathrm{SM}}+h\\0\end{pmatrix},\qquad
M_l=\frac{v_{\mathrm{SM}}}{\sqrt2}Y_l,\qquad M_D:=\frac{v_{\mathrm{SM}}}{\sqrt2}Y_\nu.
\right.
\tag{6.4}
```

这里 $`v_{\mathrm{SM}}\simeq246\,\mathrm{GeV}`$，同 5.5 节。记 $`l_L:=(l_{eL},l_{\mu L},l_{\tau L})^T`$，

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

利用电荷共轭恒等式

```math
\left.
\overline{\nu_L}M_DN_R=\overline{N_R^c}M_D^T\nu_L^c,
\right.
\tag{6.6}
```

定义

```math
\left.
\Psi_L:=\begin{pmatrix}\nu_L\\N_R^c\end{pmatrix},\qquad
\Psi_L^c=\begin{pmatrix}\nu_L^c\\N_R\end{pmatrix},\qquad
\boxed{\mathcal M:=\begin{pmatrix}0_{3\times3}&M_D\\M_D^T&M_R\end{pmatrix}=\mathcal M^T}.
\right.
\tag{6.7}
```

质量项化为

```math
\left.
-\mathcal L_{\mathrm{mass}}
=\overline{l_L}M_lE_R+\frac12\overline{\Psi_L}\,\mathcal M\Psi_L^c+\mathrm{h.c.}
\right.
\tag{6.8}
```

**味基与 Takagi 分解**

对常数幺正矩阵 $`R_\ell,R_E\in U(3)`$ 与 $`R_N\in U(n)`$，把旧场用新场表示为

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

这些变换保持动能项与规范项不变。采用 5.5 节的带电轻子质量基，

```math
\left.
M_l=D_l:=\mathop{\rm diag}\nolimits (m_e,m_\mu,m_\tau).
\right.
\tag{6.10}
```

由于 $`\mathcal M`$ 是复对称矩阵，存在 $`\mathcal U\in U(3+n)`$ 使得

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

其中所有质量均非负。三个轻态用 $`i=1,2,3`$ 标记，$`n`$ 个重态用 $`I=1,\ldots,n`$ 标记；轻态的标记既可按正序也可按倒序排列。场变换与对角的质量项为

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

等价地，也可以先分块对角化，再对每个块作 Takagi 对角化：

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

矩阵 $`M_\nu`$ 与 $`M_N`$ 是相对于分块对角基而言的；$`M_N`$ 一般不同于原来的块 $`M_R`$。

**秩与参数计数**

活跃–活跃块为零意味着

```math
\left.
\mathcal M\begin{pmatrix}a\\0\end{pmatrix}=0
\quad\text{对 }a\in\ker M_D^T,\qquad
\mathop{\rm rank}\nolimits\,\mathcal M\le\min(2n,3+n).
\right.
\tag{6.14}
```

若 $`M_R`$ 可逆，分块消元给出精确的秩恒等式

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

这一合同变换并不是幺正的质量对角化。对一般的矩阵，轻部分的秩为 $`r=\min(n,3)`$，有 $`3-r`$ 个无质量轻态。特别地，$`n=2`$ 给出最小 seesaw，在树级有一个无质量的轻中微子：

```math
\left.
m_1=0\quad\text{（正序）},\qquad
m_3=0\quad\text{（倒序）}.
\right.
\tag{6.16}
```

以下计数中取 $`n\ge1`$、一般的秩以及非简并的非零质量。在商去场重定义之前，独立实参数的个数为

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

最后一行计数的是固定 $`D`$ 时 $`\mathcal M`$ 的独立非质量参数，其中已施加零块约束并去掉了 Takagi 稳定子。它不是无约束的 $`U(3+n)`$ 矩阵的维数。

对非简并的带电轻子质量，剩余的基自由度为

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

共有 $`3+n^2`$ 个冗余实参数。不计三个带电轻子质量，

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

因此 $`n=2`$ 时有四个非零质量和七个混合参数，而 $`n=3`$ 时有六个质量和十二个混合参数。

**带电流与 PMNS 矩阵**

把 $`\mathcal U`$ 的上方分块记为

```math
\left.
K:=W_{11}U,\qquad R:=W_{12}U_N,\qquad
\nu_{\alpha L}=K_{\alpha i}\nu_{iL}^m+R_{\alpha I}(N_{IR}^m)^c.
\right.
\tag{6.20}
```

在带电轻子质量基中，5.5 节的轻子带电流化为

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

按系数定义，令 $`U_{\mathrm{PMNS}}:=K`$。由 $`\mathcal U`$ 的幺正性及其零块关系得

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

轻态的带电流矩阵 $`U_{\mathrm{PMNS}}`$ 一般不是幺正的；Takagi 矩阵 $`U`$ 是幺正的。

**轻–重混合的精确参数化**

选取单态的味基，使分块对角化后的重块为 $`M_N=D_N`$，从而 $`U_N=I_n`$。在 $`W_{11}`$ 可逆的坐标域内，利用分块幺正自由度写出

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

平方根取正定的厄米平方根。$`\mathcal M=W\,\mathop{\rm diag}\nolimits (M_\nu,D_N)W^T`$ 的左上块为

```math
\left.
0=A_X(M_\nu+XD_NX^T)A_X^T
\quad\Longleftrightarrow\quad
\boxed{M_\nu=-XD_NX^T=UD_\nu U^T}.
\right.
\tag{6.24}
```

其余各块给出

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

对正的重质量，从轻块中消去 $`X`$ 还可得到

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

这里 $`D_N`$ 是物理的重质量谱。在这组基中，$`M_R=D_N`$ 与 $`X=M_DM_R^{-1}`$ 都不是严格成立的恒等式。

**由质量与混合参数构造**

取一般的轻部分秩 $`r=\min(n,3)`$ 以及正的 $`M_I`$。设 $`P_\nu`$ 投影到 $`D_\nu`$ 的非零元上，并选取复 $`3\times n`$ 矩阵 $`O`$，满足

```math
\left.
P_\nu:=\mathop{\rm diag}\nolimits (p_1,p_2,p_3),\qquad
p_i:=\begin{cases}1,&m_i>0,\\0,&m_i=0,\end{cases}
\qquad P_\nu O=O,\qquad OO^T=P_\nu.
\right.
\tag{6.27}
```

则

```math
\left.
\boxed{X=iU\sqrt{D_\nu}\,OD_N^{-1/2}},\qquad
-XD_NX^T=U\sqrt{D_\nu}\,OO^T\sqrt{D_\nu}\,U^T=UD_\nu U^T.
\right.
\tag{6.28}
```

正交条件用的是转置，而不是厄米共轭。当 $`n>3`$ 时，它并不要求 $`O^TO=I_n`$。精确的重构为

```math
\left.
(D_\nu,D_N,U,O)\ \longrightarrow\ X\ \longrightarrow\ W(X)
\ \longrightarrow\
\mathcal M=W\begin{pmatrix}UD_\nu U^T&0\\0&D_N\end{pmatrix}W^T.
\right.
\tag{6.29}
```

去掉三个带电轻子相位以及无质量子空间中的 $`U(3-r)`$ 自由度之后，参数计数为

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

对 $`n=2`$ 与正序，

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

对倒序可取

```math
\left.
D_\nu=\mathop{\rm diag}\nolimits (m_1,m_2,0),\qquad
O(z)=\begin{pmatrix}\cos z&-\sin z\\\sin z&\cos z\\0&0\end{pmatrix},\qquad
OO^T=\mathop{\rm diag}\nolimits (1,1,0).
\right.
\tag{6.32}
```

离散的列符号可以吸收进重 Majorana 场。对三个有质量的轻态，幺正矩阵 $`U`$ 的一种相位约定为

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

这里 $`c_{ij}:=\cos\theta_{ij}`$，$`s_{ij}:=\sin\theta_{ij}`$。

对 $`n=2`$，可以通过对无质量态重新定相去掉一个 Majorana 相位。在两种排序下都可以取 $`\rho=0`$，必要时先对带电轻子作一次共同的重新定相。因此 $`U`$ 包含三个角、一个 Dirac 相位和一个 Majorana 相位；连同复参数 $`z`$，共有七个混合参数。精确的带电流矩阵为

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

**Seesaw 极限与 Casas–Ibarra 形式**

常规的 seesaw 区域中 $`M_R`$ 可逆，且

```math
\left.
\frac{\sigma_{\max}(M_D)}{\sigma_{\min}(M_R)}\ll1,\qquad
\epsilon_X:=\sigma_{\max}(X)\ll1,
\right.
\tag{6.35}
```

其中 $`\sigma_{\max}`$ 与 $`\sigma_{\min}`$ 分别表示最大与最小奇异值。展开精确参数化，

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

在这组基中，到领头阶，

```math
\left.
M_D\simeq XD_N,\qquad M_R\simeq D_N,\qquad
X\simeq M_DM_R^{-1}\simeq M_DD_N^{-1}.
\right.
\tag{6.37}
```

因此零块恒等式给出

```math
\left.
\boxed{M_\nu=UD_\nu U^T\simeq-M_DM_R^{-1}M_D^T
\simeq-\frac{v_{\mathrm{SM}}^2}{2}\,Y_\nu D_N^{-1}Y_\nu^T}.
\right.
\tag{6.38}
```

带电流矩阵满足

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

因此只有在忽略二阶的轻–重混合之后才有 $`U_{\mathrm{PMNS}}\simeq U`$。把 $`X`$ 的精确表达式代入 $`M_D\simeq XD_N`$，得到 Casas–Ibarra 形式，

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

$`X`$ 的构造是精确的；上面 $`M_D`$ 与 $`Y_\nu`$ 的表达式是领头阶近似。特别地，

```math
\left.
\epsilon_X=\sigma_{\max}\!\left(\sqrt{D_\nu}\,OD_N^{-1/2}\right).
\right.
\tag{6.41}
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

<a id="lmu-ltau-gauge-symmetry"></a>
### 6.2 $`U(1)_{L_\mu-L_\tau}`$ 规范对称性

轻子双重态 $`\ell_{\alpha L}`$、带电单态 $`E_{\alpha R}`$、Higgs 双重态 $`H`$、规范场 $`W_\mu^a,B_\mu`$ 及其耦合 $`g_2,g_1`$ 与 Yukawa 矩阵 $`Y_l`$ 同 5.5 节。

标准模型拉氏量密度中含轻子场的项为

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

在 5.5 节的味基中，

```math
\left.
Y_l=\frac{\sqrt2}{v_{\mathrm{SM}}}\,\mathop{\rm diag}\nolimits (m_e,m_\mu,m_\tau).
\right.
\tag{6.43}
```

#### $`U(1)_{L_\mu-L_\tau}`$ 规范对称变换

设 $`\theta:\mathbb R^4\to\mathbb R`$，引入实规范场 $`Z'_\mu`$ 与耦合 $`g_{Z'}>0`$，轻子场与 $`Z'_\mu`$ 的变换为


```math
\left.
\begin{gathered}
\begin{aligned}
\ell_{\alpha L}'(x)&=e^{iQ_\alpha\theta(x)}\ell_{\alpha L}(x),\\
E_{\alpha R}'(x)&=e^{iQ_\alpha\theta(x)}E_{\alpha R}(x),\\
(Z'_\mu)'(x)&=Z'_\mu(x)+\frac1{g_{Z'}}\partial_\mu\theta(x),
\end{aligned}\\[6pt]
\text{其中的 }U(1)_{L_\mu-L_\tau}\text{ 荷为}\quad
Q_\alpha=\begin{cases}
0, & \alpha=e,\\
1, & \alpha=\mu,\\
-1, & \alpha=\tau.
\end{cases}
\end{gathered}
\right.
\tag{6.44}
```

标准模型的其余场不变。

(6.42) 中的协变导数变为

```math
\left.
\begin{aligned}
D_\mu\ell_{\alpha L}&=\Bigl(\partial_\mu-ig_2W_\mu^a\frac{\sigma^a}2+\frac i2g_1B_\mu-ig_{Z'}Q_\alpha Z'_\mu\Bigr)\ell_{\alpha L},\\
D_\mu E_{\alpha R}&=\bigl(\partial_\mu+ig_1B_\mu-ig_{Z'}Q_\alpha Z'_\mu\bigr)E_{\alpha R}.
\end{aligned}
\right.
\tag{6.45}
```


#### 拉氏量



















<br><br>

<a id="qft-ch7"></a>
## 7. 重整化

**幂次计数**

这里方括号表示质量量纲。对 $`d`$ 维时空中的正则动能项，

```math
\left.
[\partial_\mu]=1,\qquad [\mathcal L]=d,\qquad
[\phi]=[A_\mu]=\frac{d-2}{2},\qquad [\psi]=\frac{d-1}{2},\qquad
[c_{\mathcal O}]=d-[\mathcal O].
\right.
\tag{7.1}
```

对相互作用 $`c_{\mathcal O}\mathcal O`$，在 Gauss 不动点处，$`[\mathcal O]<d`$、$`=d`$ 与 $`>d`$ 分别定义相关、边缘与无关算符。在其他不动点处，量子反常量纲会改变这一分类。

对由标量、矢量和鬼场传播子（行为如 $`k^{-2}`$）以及旋量传播子（行为如 $`k^{-1}`$）构成的连通图，

```math
\left.
L=I_B+I_F-V+1,\qquad
\omega=dL-2I_B-I_F+\sum_v n_{\partial,v}.
\right.
\tag{7.2}
```

其中 $`L`$ 为圈数，$`I_B,I_F`$ 分别为这两类内线的条数，$`V`$ 为顶点数，$`n_{\partial,v}`$ 为顶点 $`v`$ 上的导数个数。表观发散度 $`\omega`$ 刻画所有圈动量同时作紫外标度时的行为；子发散与对称性导致的相消须另行判断。

**维数正规化与反项**

取 $`d=4-\epsilon`$，其中 $`\epsilon`$ 有别于费曼处方中的 $`\varepsilon`$。重整化标度为 $`\mu`$：

```math
\left.
\int\frac{d^4k}{(2\pi)^4}\ \longrightarrow\
\int\frac{d^{4-\epsilon}k}{(2\pi)^{4-\epsilon}},\qquad
\frac{2}{\bar\epsilon}:=\frac{2}{\epsilon}-\gamma_E+\ln(4\pi).
\right.
\tag{7.3}
```

对实 $`\phi^4`$ 理论，裸场为 $`\phi_0=Z_\phi^{1/2}\phi_R`$。一种方便的反项参数化为

```math
\left.
\begin{aligned}
\mathcal L&=\mathcal L_R+\mathcal L_{\mathrm{ct}},\\
\mathcal L_R&=\frac12\partial_\mu\phi_R\partial^\mu\phi_R
-\frac12m^2\phi_R^2-\frac{\mu^{\epsilon}\lambda}{4!}\phi_R^4,\\
\mathcal L_{\mathrm{ct}}&=\frac12\delta Z_\phi\partial_\mu\phi_R\partial^\mu\phi_R
-\frac12\delta m^2\phi_R^2-\frac{\mu^{\epsilon}\delta\lambda}{4!}\phi_R^4,
\qquad\delta Z_\phi=Z_\phi-1.
\end{aligned}
\right.
\tag{7.4}
```

这里 $`\mu`$ 因子由耦合常数携带，每个圈积分测度中不再额外包含 $`\mu`$ 的幂。最小减除 (MS) 去掉极点项；$`\overline{\mathrm{MS}}`$ 的减除还包括上式中的 $`-\gamma_E+\ln4\pi`$ 组合。

**极点质量与场归一化**

按下式定义标量自能

```math
\left.
\widetilde G_{2,R}(p)=\frac{i}{p^2-m^2-\Sigma_R(p^2)+i\varepsilon},\qquad
\boxed{\Sigma_R(m^2)=0,\qquad \Sigma_R'(m^2)=0\quad\text{（在壳方案）},}
\right.
\tag{7.5}
```

则在壳方案使 $`m`$ 为孤立稳定粒子的质量，并把传播子的留数定为 1。在其他方案中，重整化质量不必等于极点质量。紫外因子 $`Z_\phi`$ 一般并不是 LSZ 中所用重整化内插场的有限极点留数 $`Z_{\mathrm{pole}}`$。

**重整化群**

求导时保持裸参数固定：

```math
\left.
\begin{aligned}
\beta_\lambda&:=\left.\mu\frac{d\lambda}{d\mu}\right|_{\mathrm{bare}},\qquad
\beta_{m^2}:=\left.\mu\frac{dm^2}{d\mu}\right|_{\mathrm{bare}},\\
\gamma_\phi&:=\left.\frac12\mu\frac{d\ln Z_\phi}{d\mu}\right|_{\mathrm{bare}},\\
0&=\left[\mu\frac{\partial}{\partial\mu}
+\beta_\lambda\frac{\partial}{\partial\lambda}
+\beta_{m^2}\frac{\partial}{\partial m^2}+n\gamma_\phi\right]G_{n,R}.
\end{aligned}
\right.
\tag{7.6}
```

此方程适用于互不重合的点上重整化基本场的关联函数；复合算符需要各自的重整化。在四维中，实 $`\phi^4`$ 理论以及含 $`n_f`$ 个活跃 Dirac 夸克味的 QCD 的领头系数为

```math
\left.
\begin{aligned}
\beta_\lambda&=\frac{3\lambda^2}{16\pi^2}+O(\lambda^3),\\
\beta_{g_s}&=-\frac{g_s^3}{16\pi^2}\left(11-\frac23n_f\right)+O(g_s^5),
\qquad\alpha_s:=\frac{g_s^2}{4\pi},\\
\alpha_s(\mu)&=\frac{\alpha_s(\mu_0)}
{1+\dfrac{11-2n_f/3}{2\pi}\alpha_s(\mu_0)\ln(\mu/\mu_0)}
\quad\text{（单圈，固定 }n_f\text{）}.
\end{aligned}
\right.
\tag{7.7}
```

QCD 的结果是微扰的，采用与质量无关的方案，并在活跃味的组成改变时作阈值匹配。

**Ward 恒等式与反常**

对采用保持对称性的正规子的矢量型阿贝尔理论，设 $`\Gamma^\mu`$ 为去掉耦合常数后的正规流顶点，$`S_R(p)=i\mathcal S_R(p)`$ 为完整的费米子传播子。于是

```math
\left.
q_\mu\Gamma^\mu(p+q,p)
=\mathcal S_R^{-1}(p+q)-\mathcal S_R^{-1}(p),\qquad Z_1=Z_2.
\right.
\tag{7.8}
```

其中 $`Z_1`$ 与 $`Z_2`$ 分别为顶点与费米子场的重整化常数。非阿贝尔规范理论满足含鬼场的 Slavnov--Taylor 恒等式。经典作用量的对称性在正规化后的量子测度下可能不再成立；自洽的手征规范理论要求规范反常相消。

<br><br>

<a id="qed-renormalization"></a>
### 7.1 QED 重整化

**规范固定后的拉氏量**

采用 (4.15) 的协变规范固定，电荷为 $`Q_fe`$、质量为 $`m_f`$ 的 Dirac 场 $`\psi_f`$ 的 QED 拉氏量 (5.26) 为

```math
\left.
\mathcal L
=\sum_f\bar\psi_f\bigl(i\gamma^\mu\partial_\mu-m_f\bigr)\psi_f
-\frac14F_{\mu\nu}F^{\mu\nu}
-\frac1{2\xi}(\partial_\mu A^\mu)^2
+eA_\mu\sum_fQ_f\,\bar\psi_f\gamma^\mu\psi_f .
\right.
\tag{7.9}
```

如 (3.38) 之后所述，Faddeev--Popov 鬼场退耦。


**费曼规则**

对 $`i\mathcal M`$ 有贡献的动量空间因子为

```math
\left.
\begin{array}{l|l}
\text{图元}&\text{因子}\\ \hline
\text{费米子传播子，动量 }p\text{ 沿箭头方向}&\dfrac{i(\not p+m_f)}{p^2-m_f^2+i\varepsilon}\\[12pt]
\text{光子传播子}&\dfrac{-i}{p^2+i\varepsilon}\left[\eta_{\mu\nu}-(1-\xi)\dfrac{p_\mu p_\nu}{p^2+i\varepsilon}\right]\\[12pt]
\text{费米子–光子顶点}&ieQ_f\gamma^\mu\\[4pt]
\text{入射 / 出射费米子}&u^s(p)\ /\ \bar u^s(p)\\
\text{入射 / 出射反费米子}&\bar v^s(p)\ /\ v^s(p)\\
\text{入射 / 出射光子}&\epsilon^r_\mu(p)\ /\ \epsilon^{r*}_\mu(p)
\end{array}
\right.
\tag{7.10}
```

对电子，$`Q_f=-1`$，顶点为 $`-ie\gamma^\mu`$。沿每条费米子线，按与箭头相反的顺序写出各因子，使旋量指标构成矩阵乘积。在每个顶点施加四动量守恒，每个圈动量用 $`\int d^4\ell/(2\pi)^4`$ 积分，并按 (7.3) 延拓到 $`d`$ 维。每个闭合费米子圈给出因子 $`-1`$ 和一个 Dirac 迹；与 [4.3 节](QFT-zh-part-03.md#feynman-diagrams) 相同，交换全同的外费米子改变符号。

**树级：$`e^+e^-\to q\bar q`$**

<p align="center"><img src="figures/ee-to-qqbar.svg" alt="e+ e- → q qbar 的树级 s 道图" width="440"></p>

时间从左向右。费米子线上的箭头表示费米子数的流向；灰色箭头表示四动量。

把 $`e^-,e^+,q,\bar q`$ 的自旋分别记为 $`s,s',r,r'`$，把 $`q,\bar q`$ 的色记为 $`c,c'\in\{1,2,3\}`$；光子顶点在色空间中是对角的，且 $`p_1+p_2=k_1+k_2`$。用 (7.10) 逆着箭头读出每条费米子线，

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
\tag{7.11}
```


**表观发散度**

对 QED 的连通图，设 $`V`$ 为顶点数，$`I_\gamma,I_F`$ 分别为光子内线与费米子内线的条数，$`E_\gamma,E_F`$ 分别为光子外线与费米子外线的条数。(7.9) 的每个顶点连接两条费米子线和一条光子线，且不含导数。统计线的端点数，并在 $`d=4`$ 时利用 (7.2)，

```math
\left.
\begin{aligned}
2V&=2I_F+E_F,\qquad V=2I_\gamma+E_\gamma,\qquad L=I_\gamma+I_F-V+1,\\[6pt]
\omega&=4L-2I_\gamma-I_F=2I_\gamma+3I_F-4V+4 .
\end{aligned}
\right.
\tag{7.12}
```

利用 $`I_\gamma=\tfrac12(V-E_\gamma)`$ 与 $`I_F=V-\tfrac12E_F`$ 消元，

```math
\left.
\boxed{\omega=4-E_\gamma-\frac32E_F .}
\right.
\tag{7.13}
```

由 (7.1)，四维中 $`[e]=0`$，因此对 $`V`$ 的依赖相消。

**两条外腿**

每个顶点都守恒费米子数，因此 $`E_F`$ 为偶数，两条外腿即 $`(E_F,E_\gamma)=(2,0)`$ 或 $`(0,2)`$。设 $`-i\Sigma(p)`$ 与 $`i\Pi^{\mu\nu}(p)`$ 分别为含两条费米子外线、含两条光子外线的截肢 1PI 图之和，其中 $`p`$ 为外动量。

**(1) 费米子传播子**

```math
\left.
E_F=2,\qquad E_\gamma=0\qquad\Longrightarrow\qquad\omega=1 .
\right.
\tag{7.14}
```

<p align="center"><img src="figures/fermion-self-energy.svg" alt="单圈费米子自能" width="322"></p>

费米子 $`f`$ 的 $`-i\Sigma(p)`$ 的单圈图：内费米子沿其箭头携带 $`\ell`$，光子携带 $`p-\ell`$。

设 $`-i\Sigma_2(p)`$ 为 $`-i\Sigma(p)`$ 的 $`O(e^2)`$ 部分。从顶点 $`\nu`$ 出发，用 (7.10) 逆着箭头读这条线，

```math
\left.
\begin{aligned}
-i\Sigma_2(p)
=\int\frac{d^4\ell}{(2\pi)^4}\,
&(ieQ_f\gamma^\nu)\,\frac{i(\not\ell+m_f)}{\ell^2-m_f^2+i\varepsilon}\,(ieQ_f\gamma^\mu)\\[6pt]
&\times\frac{-i}{(p-\ell)^2+i\varepsilon}\left[\eta_{\mu\nu}-(1-\xi)\frac{(p-\ell)_\mu(p-\ell)_\nu}{(p-\ell)^2+i\varepsilon}\right].
\end{aligned}
\right.
\tag{7.15}
```

对夸克，(7.15) 乘以色空间中的单位矩阵。

在 $`d=4-\epsilon`$ 维中，如 (7.3) 把 $`d^4\ell/(2\pi)^4`$ 换成 $`d^d\ell/(2\pi)^d`$，如 (7.4) 令耦合常数携带 $`\mu`$ 因子，即 $`e\to\mu^{\epsilon/2}e`$，并按 $`\{\gamma^\mu,\gamma^\nu\}=2\eta^{\mu\nu}I_4`$ 与 $`\eta^\mu{}_\mu=d`$ 把 $`\gamma`$ 矩阵延拓到 $`d`$ 维。合并因子 $`(ieQ_f)^2\,i\,(-i)=-e^2Q_f^2`$，并利用 $`\gamma^\nu\gamma_\nu=d\,I_4`$、$`\gamma^\nu\not a\gamma_\nu=-(d-2)\not a`$，以及对 $`\ell=p-k`$ 成立的 $`\not k(\not\ell+m_f)\not k=2(k\cdot p)\not k+k^2(m_f-\not p-\not k)`$，其中 $`k^2`$ 消去一个因子 $`\mathcal P_\gamma`$，

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
\tag{7.16}
```

用费曼参数 $`x`$ 合并分母：

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
\tag{7.17}
```

作平移 $`\ell\to\ell+xp`$，于是 $`k\to(1-x)p-\ell`$；去掉 $`\ell`$ 的奇次项，并把 $`\ell^\mu\ell^\nu`$ 换成 $`\eta^{\mu\nu}\ell^2/d`$。(7.16) 的分子变为

```math
\left.
\begin{aligned}
d\,m_f-(d-2)\not\ell\ &\to\ d\,m_f-(d-2)x\not p,\\[4pt]
m_f-\not p-\not k\ &\to\ m_f-(2-x)\not p,\\[4pt]
2(k\cdot p)\not k\ &\to\ 2(1-x)^2p^2\not p+2(p\cdot\ell)\not\ell
\ \to\ 2(1-x)^2p^2\not p+\frac2d\,\ell^2\not p,
\end{aligned}
\right.
\tag{7.18}
```

于是

```math
\left.
\begin{aligned}
-i\Sigma_2(p)
={}&-\mu^{\epsilon}e^2Q_f^2\int_0^1dx\int\frac{d^d\ell}{(2\pi)^d}\,\biggl\{
\frac{d\,m_f-(d-2)x\not p-(1-\xi)\bigl[m_f-(2-x)\not p\bigr]}{\bigl(\ell^2-\Delta_{\Sigma,f}+i\varepsilon\bigr)^2}\\[6pt]
&-(1-\xi)\,\frac{2x\bigl[2(1-x)^2p^2+\frac2d\,\ell^2\bigr]\not p}{\bigl(\ell^2-\Delta_{\Sigma,f}+i\varepsilon\bigr)^3}\biggr\}.
\end{aligned}
\right.
\tag{7.19}
```

Wick 转动后，对 $`\Delta>0`$ 求积分，再经 $`\Delta-i\varepsilon`$ 延拓到 $`\Delta<0`$；对 $`n=2,3`$，

```math
\left.
\begin{aligned}
\int\frac{d^d\ell}{(2\pi)^d}\,\frac{1}{(\ell^2-\Delta+i\varepsilon)^n}
&=\frac{(-1)^n\,i}{(4\pi)^{d/2}}\,\frac{\Gamma\bigl(n-\frac d2\bigr)}{\Gamma(n)}\,(\Delta-i\varepsilon)^{\frac d2-n},\\[6pt]
\int\frac{d^d\ell}{(2\pi)^d}\,\frac{\ell^2}{(\ell^2-\Delta+i\varepsilon)^n}
&=\frac{(-1)^{n-1}\,i}{(4\pi)^{d/2}}\,\frac d2\,\frac{\Gamma\bigl(n-1-\frac d2\bigr)}{\Gamma(n)}\,(\Delta-i\varepsilon)^{\frac d2-n+1}.
\end{aligned}
\right.
\tag{7.20}
```

把 (7.20) 用于 (7.19)，

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
\tag{7.21}
```

取 $`d=4-\epsilon`$，利用 $`\Gamma(\epsilon/2)=2/\epsilon-\gamma_E+O(\epsilon)`$ 和 (7.3) 中的 $`2/\bar\epsilon`$，

```math
\left.
\boxed{
\begin{aligned}
\Sigma_2(p)={}&\frac{e^2Q_f^2}{16\pi^2}\int_0^1dx\,\biggl\{
\Bigl[4m_f-2x\not p-(1-\xi)\bigl(m_f-2(1-x)\not p\bigr)\Bigr]
\left[\frac2{\bar\epsilon}-\ln\frac{\Delta_{\Sigma,f}-i\varepsilon}{\mu^2}\right]\\[6pt]
&-2m_f+2x\not p+\frac{2(1-\xi)\,x(1-x)\,p^2\not p}{m_f^2-xp^2-i\varepsilon}\biggr\}+O(\epsilon)\\[6pt]
={}&\frac{e^2Q_f^2}{16\pi^2}\,\frac2\epsilon\,\bigl[(3+\xi)m_f-\xi\not p\bigr]+(\epsilon\to0\text{ 时有限}).
\end{aligned}
}
\right.
\tag{7.22}
```

**(2) 光子传播子**

```math
\left.
E_\gamma=2,\qquad E_F=0\qquad\Longrightarrow\qquad\omega=2 .
\right.
\tag{7.23}
```

<p align="center"><img src="figures/photon-self-energy.svg" alt="单圈光子自能" width="298"></p>

$`i\Pi^{\mu\nu}(p)`$ 的单圈图，含费米子 $`f`$ 的一个闭合圈：圈上的动量 $`\ell+p`$ 与 $`\ell`$ 沿箭头方向流动。

设 $`i\Pi_2^{\mu\nu}(p)`$ 为 $`i\Pi^{\mu\nu}(p)`$ 的 $`O(e^2)`$ 部分。从顶点 $`\mu`$ 出发，用 (7.10) 逆着箭头读这个圈，

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
\tag{7.24}
```

其中因子 $`-1`$ 与 Dirac 迹来自闭合费米子圈，$`N_{\mathrm c,f}`$ 为 $`f`$ 的色数（轻子为 $`1`$，夸克为 $`3`$），来自色迹。

在 $`d=4-\epsilon`$ 维中，如 (7.3) 把 $`d^4\ell/(2\pi)^4`$ 换成 $`d^d\ell/(2\pi)^d`$，并如 (7.4) 令耦合常数携带 $`\mu`$ 因子，即 $`e\to\mu^{\epsilon/2}e`$。合并因子 $`(-1)(ieQ_f)^2i^2=-e^2Q_f^2`$，并利用 $`\mathop{\rm tr}\nolimits (\gamma^\mu\gamma^\nu)=4\eta^{\mu\nu}`$、$`\mathop{\rm tr}\nolimits (\gamma^\mu\gamma^\rho\gamma^\nu\gamma^\sigma)=4(\eta^{\mu\rho}\eta^{\nu\sigma}-\eta^{\mu\nu}\eta^{\rho\sigma}+\eta^{\mu\sigma}\eta^{\rho\nu})`$，以及奇数个 $`\gamma`$ 矩阵之积的迹为零，

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
\tag{7.25}
```

用费曼参数 $`x`$ 合并分母：

```math
\left.
\begin{aligned}
\frac{1}{\mathcal P_1\mathcal P_2}
&=\int_0^1\frac{dx}{\bigl[x\mathcal P_2+(1-x)\mathcal P_1\bigr]^2}
=\int_0^1\frac{dx}{\bigl[(\ell+xp)^2-\Delta_f+i\varepsilon\bigr]^2},\\[6pt]
\Delta_f&:=m_f^2-x(1-x)p^2 .
\end{aligned}
\right.
\tag{7.26}
```

作平移 $`\ell\to\ell-xp`$，并去掉积分为零的 $`\ell`$ 奇次项；再在积分号下把 $`\ell^\mu\ell^\nu`$ 换成 $`\eta^{\mu\nu}\ell^2/d`$。(7.25) 的分子变为

```math
\left.
\begin{aligned}
&\ell^\mu(\ell+p)^\nu+\ell^\nu(\ell+p)^\mu-\eta^{\mu\nu}\bigl[\ell\cdot(\ell+p)-m_f^2\bigr]\\[4pt]
&\quad\to\ 2\ell^\mu\ell^\nu-\eta^{\mu\nu}\ell^2-2x(1-x)p^\mu p^\nu+\eta^{\mu\nu}\bigl[x(1-x)p^2+m_f^2\bigr]\\[4pt]
&\quad\to\ 2x(1-x)\bigl(p^2\eta^{\mu\nu}-p^\mu p^\nu\bigr)+\eta^{\mu\nu}\Bigl[\frac{2-d}{d}\,\ell^2+\Delta_f\Bigr],
\end{aligned}
\right.
\tag{7.27}
```

于是

```math
\left.
\begin{aligned}
i\Pi_2^{\mu\nu}(p)
={}&-4\mu^{\epsilon}e^2\sum_fN_{\mathrm c,f}Q_f^2\int_0^1dx\int\frac{d^d\ell}{(2\pi)^d}\,
\frac{1}{\bigl(\ell^2-\Delta_f+i\varepsilon\bigr)^2}\\[6pt]
&\times\Bigl\{2x(1-x)\bigl(p^2\eta^{\mu\nu}-p^\mu p^\nu\bigr)+\eta^{\mu\nu}\Bigl[\frac{2-d}{d}\,\ell^2+\Delta_f\Bigr]\Bigr\}.
\end{aligned}
\right.
\tag{7.28}
```

Wick 转动后，对 $`\Delta>0`$ 求积分，再经 $`\Delta-i\varepsilon`$ 延拓到 $`\Delta<0`$，

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
\tag{7.29}
```

其中最后一行用到 $`\Gamma(2-\tfrac d2)=(1-\tfrac d2)\Gamma(1-\tfrac d2)`$。(7.28) 中只有横向项保留下来：

```math
\left.
\begin{aligned}
i\Pi_2^{\mu\nu}(p)
={}&-4\mu^{\epsilon}e^2\sum_fN_{\mathrm c,f}Q_f^2\int_0^1dx\,2x(1-x)\bigl(p^2\eta^{\mu\nu}-p^\mu p^\nu\bigr)\\[6pt]
&\times\frac{i}{(4\pi)^{d/2}}\,\Gamma\Bigl(2-\frac d2\Bigr)(\Delta_f-i\varepsilon)^{\frac d2-2} .
\end{aligned}
\right.
\tag{7.30}
```

取 $`d=4-\epsilon`$，利用 $`\Gamma(\epsilon/2)=2/\epsilon-\gamma_E+O(\epsilon)`$ 和 (7.3) 中的 $`2/\bar\epsilon`$，

```math
\left.
\boxed{
\begin{aligned}
\Pi_2^{\mu\nu}(p)&=\bigl(p^2\eta^{\mu\nu}-p^\mu p^\nu\bigr)\,\Pi_2(p^2),\\[6pt]
\Pi_2(p^2)&=-\frac{e^2}{2\pi^2}\sum_fN_{\mathrm c,f}Q_f^2\int_0^1dx\,x(1-x)\left[\frac2{\bar\epsilon}-\ln\frac{\Delta_f-i\varepsilon}{\mu^2}\right]+O(\epsilon).
\end{aligned}
}
\right.
\tag{7.31}
```

**三条外腿**

三条外腿即 $`(E_F,E_\gamma)=(2,1)`$ 或 $`(0,3)`$。设 $`ieQ_f\Gamma^\mu(p',p)`$ 为截肢 1PI 图之和，图中有动量为 $`p`$ 的入射费米子、动量为 $`p':=p+q`$ 的出射费米子，以及动量为 $`q`$、指标为 $`\mu`$ 的入射光子，这样 $`\Gamma^\mu`$ 就是 (7.8) 中的正规顶点。记 $`\Gamma^\mu=\gamma^\mu+\Lambda^\mu`$。

**(1) 顶点**

```math
\left.
E_F=2,\qquad E_\gamma=1\qquad\Longrightarrow\qquad\omega=0 .
\right.
\tag{7.32}
```

<p align="center"><img src="figures/vertex.svg" alt="单圈 QED 顶点" width="370"></p>

费米子 $`f`$ 的 $`ieQ_f\Lambda^\mu(p',p)`$ 的单圈图：两条内费米子线沿各自的箭头分别携带 $`\ell`$ 与 $`\ell+q`$，内光子携带 $`p-\ell`$。

设 $`\Lambda_2^\mu(p',p)`$ 为 $`\Lambda^\mu(p',p)`$ 的 $`O(e^2)`$ 部分。从顶点 $`\nu`$ 出发，用 (7.10) 逆着箭头读这条线，

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
\tag{7.33}
```

对夸克，(7.33) 乘以色空间中的单位矩阵。

在 $`d=4-\epsilon`$ 维中，按 (7.16) 的做法延拓，其中剥离出的耦合 $`ieQ_f`$ 也携带 $`\mu^{\epsilon/2}`$。合并因子 $`(ieQ_f)^3\,i\cdot i\cdot(-i)=(ieQ_f)(-ie^2Q_f^2)`$，

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
\tag{7.34}
```

用费曼参数 $`x,y,z`$ 合并分母：

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
\tag{7.35}
```

作平移 $`\ell\to\ell+A`$，于是 $`\ell'\to\ell+A'`$，$`k\to K-\ell`$，其中 $`A:=(1-x)p-yp'`$，$`A':=(1-y)p'-xp`$，$`K:=xp+yp'`$。去掉 $`\ell`$ 的奇次项，并把 $`\ell^\alpha\ell^\beta`$ 换成 $`\eta^{\alpha\beta}\ell^2/d`$；再利用 $`\not\ell\not\ell=\ell^2`$，(7.34) 的分子变为

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
\tag{7.36}
```

于是

```math
\left.
\begin{aligned}
\Lambda_2^\mu(p',p)
={}&-i\mu^{\epsilon}e^2Q_f^2\int dF\int\frac{d^d\ell}{(2\pi)^d}\,\biggl\{
\frac{2\bigl[\frac{(d-2)^2}{d}\,\ell^2\gamma^\mu+N^\mu\bigr]}{\bigl(\ell^2-\Delta_{V,f}+i\varepsilon\bigr)^3}\\[6pt]
&-6(1-\xi)\,z\,\frac{(\ell^2)^2\gamma^\mu+\ell^2N_2^\mu+N_0^\mu}{\bigl(\ell^2-\Delta_{V,f}+i\varepsilon\bigr)^4}\biggr\}.
\end{aligned}
\right.
\tag{7.37}
```

Wick 转动后，对 $`\Delta>0`$ 求积分，再经 $`\Delta-i\varepsilon`$ 延拓到 $`\Delta<0`$，积分 (7.20) 推广为

```math
\left.
\int\frac{d^d\ell}{(2\pi)^d}\,\frac{(\ell^2)^a}{(\ell^2-\Delta+i\varepsilon)^n}
=\frac{(-1)^{n+a}\,i}{(4\pi)^{d/2}}\,
\frac{\Gamma\bigl(a+\frac d2\bigr)\,\Gamma\bigl(n-a-\frac d2\bigr)}{\Gamma\bigl(\frac d2\bigr)\,\Gamma(n)}\,
(\Delta-i\varepsilon)^{\frac d2+a-n}.
\right.
\tag{7.38}
```

把 (7.38) 用于 (7.37)，

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
\tag{7.39}
```

取 $`d=4-\epsilon`$，利用 $`\Gamma(\epsilon/2)=2/\epsilon-\gamma_E+O(\epsilon)`$ 与 (7.3) 中的 $`2/\bar\epsilon`$，并在有限项中取 $`N^\mu`$、$`N_2^\mu`$ 在 $`d=4`$ 时的值，

```math
\left.
\boxed{
\begin{aligned}
\Lambda_2^\mu(p',p)={}&\frac{e^2Q_f^2}{16\pi^2}\int dF\,\biggl\{
\bigl[2-6(1-\xi)z\bigr]\gamma^\mu\left[\frac2{\bar\epsilon}-\ln\frac{\Delta_{V,f}-i\varepsilon}{\mu^2}\right]
-\bigl[4-5(1-\xi)z\bigr]\gamma^\mu\\[6pt]
&-\frac{N^\mu-2(1-\xi)z\,N_2^\mu}{\Delta_{V,f}-i\varepsilon}
-\frac{(1-\xi)z\,N_0^\mu}{(\Delta_{V,f}-i\varepsilon)^2}\biggr\}+O(\epsilon)\\[6pt]
={}&\frac{e^2Q_f^2}{16\pi^2}\,\frac2\epsilon\,\xi\gamma^\mu+(\epsilon\to0\text{ 时有限}),\\[10pt]
N^\mu\big|_{d=4}={}&-2\not A\gamma^\mu\not A'+4m_f(A+A')^\mu-2m_f^2\gamma^\mu,\\[6pt]
N_2^\mu\big|_{d=4}={}&\frac14N^\mu\big|_{d=4}-\gamma^\mu\not A\not K-\not K\not A'\gamma^\mu-\frac12\not K\gamma^\mu\not K-(A+A')^\mu\not K-m_fK^\mu .
\end{aligned}
}
\right.
\tag{7.40}
```

除非 $`p^2=p'^2=m_f^2`$，参数积分都收敛；在这一在壳情形下，积分在 $`z\to1`$ 处对数发散。结合 (7.22)，上述结果满足 $`q_\mu\Lambda_2^\mu(p+q,p)=\Sigma_2(p)-\Sigma_2(p+q)`$，这正是 (7.8) 所要求的。

**(2) 三光子**

```math
\left.
E_\gamma=3,\qquad E_F=0\qquad\Longrightarrow\qquad\omega=1 .
\right.
\tag{7.41}
```

费米子圈两种取向的图相互抵消（Furry 定理），因此含三条光子外线的 1PI 图之和为零。

<br><br>





































<a id="qft-ch8"></a>
## 8. 多圈重整化

**子发散与森林公式**

在单圈以上，发散子图可以是嵌套的、不相交的或重叠的。在有质量的 BPHZ 重整化中，取减除点以避开红外奇点；设 $`\mathcal I_{\mathcal G}`$ 为 1PI 图 $`\mathcal G`$ 的被积函数，$`t_\gamma`$ 为按发散 1PI 子图 $`\gamma`$ 的外动量作 Taylor 展开、展开到其表观发散度阶的减除。则

```math
\left.
\boxed{R\mathcal I_{\mathcal G}
=\sum_{F\in\mathfrak F(\mathcal G)}
\left[\prod_{\gamma\in F}(-t_\gamma)\right]\mathcal I_{\mathcal G}.}
\right.
\tag{8.1}
```

森林 $`F`$ 只包含两两嵌套或不相交的减除子图。求和包括空森林；若整个图发散，也包括整个图。嵌套的减除从最内层子图开始向外依次作用。低阶反项的插入是高圈计算的一部分。

**极点结构与两圈跑动**

对单一耦合的、与质量无关的最小减除方案中的乘性重整化常数，

```math
\left.
Z=1+\sum_{L=1}^{\infty}
\left(\frac{g_s^2}{16\pi^2}\right)^L
\sum_{k=1}^{L}\frac{z_{Lk}}{\epsilon^k}.
\right.
\tag{8.2}
```

重整化群的自洽性把高次极点与低阶数据联系起来。对 QCD，

```math
\left.
\begin{aligned}
\beta_{g_s}&=-\frac{\beta_0g_s^3}{16\pi^2}
-\frac{\beta_1g_s^5}{(16\pi^2)^2}+O(g_s^7),\\
\beta_0&=11-\frac23n_f,\qquad
\beta_1=102-\frac{38}{3}n_f.
\end{aligned}
\right.
\tag{8.3}
```

在通常的与质量无关的方案范围内，这前两个系数在解析的、与标度无关的耦合重定义下保持不变。更高阶的系数依赖于方案。

**积分族与分部积分**

对 $`L`$ 个圈动量 $`k_\ell`$ 与分母因子 $`D_j=q_j^2-m_j^2+i\varepsilon`$（其中 $`q_j`$ 为圈动量与外动量的线性组合），定义

```math
\left.
\begin{aligned}
I_{\nu_1\cdots\nu_N}
&:=\int\prod_{\ell=1}^{L}\frac{d^dk_\ell}{(2\pi)^d}
\prod_{j=1}^{N}D_j^{-\nu_j},\\
0&=\int\prod_{\ell=1}^{L}\frac{d^dk_\ell}{(2\pi)^d}
\frac{\partial}{\partial k_r^\mu}
\left(v^\mu\prod_{j=1}^{N}D_j^{-\nu_j}\right).
\end{aligned}
\right.
\tag{8.4}
```

其中 $`v^\mu`$ 为圈动量或外动量。在维数正规化中，分部积分恒等式通过从表面项为零的区域作解析延拓而成立。分子中的标量积可在补全的积分族中以零次或负次幂计入。

**主积分与微分方程**

经代数约化后，选定的积分族可以用由主积分 $`M_r`$ 构成的有限基表示。对运动学不变量 $`s`$，

```math
\left.
I_{\nu_1\cdots\nu_N}=\sum_r c_r(d,\{p\cdot p\},\{m^2\})M_r,
\qquad
\frac{\partial M_r}{\partial s}=\sum_t A_{rt}(d,\{p\cdot p\},\{m^2\})M_t.
\right.
\tag{8.5}
```

求解这些方程需要边界值和费曼解析延拓。减除前必须区分紫外极点与红外极点；无标度积分在维数正规化中为零，但可能掩盖紫外极点与红外极点之间的相消。高圈手征计算还需要明确的 $`d`$ 维 $`\gamma^5`$ 处方；仅靠四维 Weyl 矩阵给不出这样的处方。

<br><br>

<a id="qft-ch9"></a>
## 9. 宇宙学

<a id="geometry-of-the-universe"></a>
### 9.1 宇宙的几何

<a id="cosmology-experimental-facts"></a>
#### 实验事实

1. Hubble 定律：宇宙在膨胀。
2. 宇宙微波背景（CMB）是各向同性的。
3. 星系的大尺度分布是均匀的。

<br><br>

<a id="flrw-metric"></a>
#### FLRW 度规

```math
\left.
ds^2=dt^2-a(t)^2\left[\frac{dr^2}{1-kr^2}+r^2\bigl(d\theta^2+\sin^2\theta\,d\phi^2\bigr)\right]
\right.
\tag{9.1}
```

<br><br>

<a id="evolution-of-the-universe"></a>
### 9.2 宇宙的演化

<a id="cosmology-dynamics"></a>
#### 动力学

```math
\left.
\left(\frac{\dot a}{a}\right)^2=\frac{8\pi G}{3}\rho-\frac{k}{a^2}
\right.
\tag{9.2}
```

<br><br>

<a id="dark-matter"></a>
#### 暗物质

**实验结果**

<br><br>

<a id="dark-energy"></a>
#### 暗能量

<br><br>

<a id="cosmic-evolution"></a>
#### 宇宙演化

1. 辐射主导时期（早期宇宙）
2. 物质主导时期
3. 暗能量主导时期

