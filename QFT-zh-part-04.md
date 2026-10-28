> 中文版第 4/4 部分 · [完整文件](QFT-zh.md) · [1](QFT-zh-part-01.md) · [2](QFT-zh-part-02.md) · [3](QFT-zh-part-03.md) · [4](QFT-zh-part-04.md)

<a id="lsz-reduction"></a>
### 6.5 LSZ 约化公式



**单粒子极点**

考虑一个实标量场，其真空期望值为零，有一个物理质量为 $`m_{\mathrm{phys}}>0`$ 的孤立稳定单粒子极点，且与该粒子有非零交叠。选取粒子态的相位，使得

```math
\begin{aligned}
\langle\Omega|\hat\phi_H(0)|\mathbf p\rangle&=\sqrt{Z_{\mathrm{pole}}},\qquad Z_{\mathrm{pole}}>0,\qquad \langle\Omega|\Omega\rangle=1,\\
\widetilde G_2(p)&:=\int d^4x\,e^{ip\cdot x}G_2(x,0)
=\frac{iZ_{\mathrm{pole}}}{p^2-m_{\mathrm{phys}}^2+i\varepsilon}
+\text{在极点处正则的项}.
\end{aligned}
```

其中 $`Z_{\mathrm{pole}}`$ 为所选场归一化下的极点留数。假设相应的渐近散射态存在。

**约化公式**

对 $`r`$ 个入射动量 $`p_a`$ 与 $`s`$ 个出射动量 $`q_b`$（物理能量均为正），把每个位置都用 $`e^{+ik\cdot x}`$ 作 Fourier 变换，由此定义 $`\widetilde G_{r+s,\mathrm c}`$。对 $`r+s>2`$ 的连通散射过程，

```math
\boxed{\begin{aligned}
&i(2\pi)^4\delta^{(4)}\left(\sum_{b=1}^{s}q_b-\sum_{a=1}^{r}p_a\right)\mathcal M_{fi}\\
&\quad=\lim_{\mathrm{on\ shell}}
\left[\prod_{b=1}^{s}\frac{q_b^2-m_{\mathrm{phys}}^2}{i\sqrt{Z_{\mathrm{pole}}}}\right]
\left[\prod_{a=1}^{r}\frac{p_a^2-m_{\mathrm{phys}}^2}{i\sqrt{Z_{\mathrm{pole}}}}\right]
\widetilde G_{r+s,\mathrm c}(q_1,\ldots,q_s,-p_1,\ldots,-p_r).
\end{aligned}}
```

这里的极限是指：先按费曼处方同时提取所有外腿极点的留数，再令所有外动量在壳。每个因子去掉一条外传播子及其场交叠。归一化为单位极点留数的场有 $`Z_{\mathrm{pole}}=1`$。


<br><br>

<a id="cross-sections-and-decay-rates"></a>
### 6.6 截面与衰变率

**相空间与态求和**

对末态总动量 $`P`$ 与 $`n`$ 个在壳出射动量 $`k_j`$，

```math
d\Phi_n(P;k_1,\ldots,k_n):=(2\pi)^4\delta^{(4)}\left(P-\sum_{j=1}^{n}k_j\right)
\prod_{j=1}^{n}\frac{d^3k_j}{(2\pi)^3\,2E_{\mathbf k_j}},\qquad
E_{\mathbf k_j}=\sqrt{\mathbf k_j^2+m_j^2}.
```

用 $`\overline{|\mathcal M|^2}`$ 表示对未观测的末态自旋与内部量子数求和、并对等概率分布的初态求平均的结果。对两个非极化的初态粒子，若它们分别有 $`N_1,N_2`$ 个这样的态，

```math
\overline{|\mathcal M|^2}:=\frac1{N_1N_2}\sum_{\text{初态、末态}}|\mathcal M|^2,
\qquad C_{\mathrm{id}}:=\prod_a\nu_a!.
```

其中 $`\nu_a`$ 为末态中第 $`a`$ 种全同粒子的个数。对带标记的末态动量在完整相空间上积分时，要除以 $`C_{\mathrm{id}}`$；若积分区域已使每个物理末态位形只计一次，则省去这一因子。固定的初态偏振不作平均。

**截面与衰变率**

对 $`1+2\to n`$ 散射，以及质量为 $`M`$ 的静止粒子的衰变，

```math
\boxed{\begin{aligned}
d\sigma&=\frac{\overline{|\mathcal M|^2}}{4\sqrt{(p_1\cdot p_2)^2-m_1^2m_2^2}}\,\frac{d\Phi_n(p_1+p_2)}{C_{\mathrm{id}}},\\
d\Gamma&=\frac{\overline{|\mathcal M|^2}}{2M}\,\frac{d\Phi_n(P)}{C_{\mathrm{id}}},\qquad P=(M,\mathbf0).
\end{aligned}}
```

在衰变公式中，若要得到非极化的衰变率，只对母粒子的初态求平均。对两体末态，用质心系中初态与末态的单粒子三动量大小 $`|\mathbf p_1|`$ 与 $`|\mathbf k_1|`$：

```math
\begin{aligned}
\frac{d\sigma_{2\to2}}{d\Omega}
&=\frac1{64\pi^2s\,C_{\mathrm{id}}}\frac{|\mathbf k_1|}{|\mathbf p_1|}\,\overline{|\mathcal M|^2},\qquad s=(p_1+p_2)^2,\\
\frac{d\Gamma_{1\to2}}{d\Omega}
&=\frac{|\mathbf k_1|}{32\pi^2M^2\,C_{\mathrm{id}}}\,\overline{|\mathcal M|^2},\\
\Gamma_{1\to2}&=\frac{|\mathbf k_1|}{8\pi M^2\,C_{\mathrm{id}}}\,\overline{|\mathcal M|^2}\qquad\text{若振幅平方与角度无关}.
\end{aligned}
```

在衰变公式中，$`|\mathbf k_1|`$ 在母粒子静止系中取值。立体角积分采用与完整相空间相同的全同粒子计数约定。


<br><br>

<a id="qft-ch7"></a>
## 7. 重整化

**幂次计数**

这里方括号表示质量量纲。对 $`d`$ 维时空中的正则动能项，

```math
[\partial_\mu]=1,\qquad [\mathcal L]=d,\qquad
[\phi]=[A_\mu]=\frac{d-2}{2},\qquad [\psi]=\frac{d-1}{2},\qquad
[c_{\mathcal O}]=d-[\mathcal O].
```

对相互作用 $`c_{\mathcal O}\mathcal O`$，在 Gauss 不动点处，$`[\mathcal O]<d`$、$`=d`$ 与 $`>d`$ 分别定义相关、边缘与无关算符。在其他不动点处，量子反常量纲会改变这一分类。

对由标量、矢量和鬼场传播子（行为如 $`k^{-2}`$）以及旋量传播子（行为如 $`k^{-1}`$）构成的连通图，

```math
L=I_B+I_F-V+1,\qquad
\omega=dL-2I_B-I_F+\sum_v n_{\partial,v}.
```

其中 $`L`$ 为圈数，$`I_B,I_F`$ 分别为这两类内线的条数，$`V`$ 为顶点数，$`n_{\partial,v}`$ 为顶点 $`v`$ 上的导数个数。表观发散度 $`\omega`$ 刻画所有圈动量同时作紫外标度时的行为；子发散与对称性导致的相消须另行判断。

**维数正规化与反项**

取 $`d=4-\epsilon`$，其中 $`\epsilon`$ 有别于费曼处方中的 $`\varepsilon`$。重整化标度为 $`\mu`$：

```math
\int\frac{d^4k}{(2\pi)^4}\ \longrightarrow\
\int\frac{d^{4-\epsilon}k}{(2\pi)^{4-\epsilon}},\qquad
\frac{2}{\bar\epsilon}:=\frac{2}{\epsilon}-\gamma_E+\ln(4\pi).
```

对实 $`\phi^4`$ 理论，裸场为 $`\phi_0=Z_\phi^{1/2}\phi_R`$。一种方便的反项参数化为

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

这里 $`\mu`$ 因子由耦合常数携带，每个圈积分测度中不再额外包含 $`\mu`$ 的幂。最小减除 (MS) 去掉极点项；$`\overline{\mathrm{MS}}`$ 的减除还包括上式中的 $`-\gamma_E+\ln4\pi`$ 组合。

**极点质量与场归一化**

按下式定义标量自能

```math
\widetilde G_{2,R}(p)=\frac{i}{p^2-m^2-\Sigma_R(p^2)+i\varepsilon},\qquad
\boxed{\Sigma_R(m^2)=0,\qquad \Sigma_R'(m^2)=0\quad\text{（在壳方案）},}
```

则在壳方案使 $`m`$ 为孤立稳定粒子的质量，并把传播子的留数定为 1。在其他方案中，重整化质量不必等于极点质量。紫外因子 $`Z_\phi`$ 一般并不是 LSZ 中所用重整化内插场的有限极点留数 $`Z_{\mathrm{pole}}`$。

**重整化群**

求导时保持裸参数固定：

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

此方程适用于互不重合的点上重整化基本场的关联函数；复合算符需要各自的重整化。在四维中，实 $`\phi^4`$ 理论以及含 $`n_f`$ 个活跃 Dirac 夸克味的 QCD 的领头系数为

```math
\begin{aligned}
\beta_\lambda&=\frac{3\lambda^2}{16\pi^2}+O(\lambda^3),\\
\beta_{g_s}&=-\frac{g_s^3}{16\pi^2}\left(11-\frac23n_f\right)+O(g_s^5),
\qquad\alpha_s:=\frac{g_s^2}{4\pi},\\
\alpha_s(\mu)&=\frac{\alpha_s(\mu_0)}
{1+\dfrac{11-2n_f/3}{2\pi}\alpha_s(\mu_0)\ln(\mu/\mu_0)}
\quad\text{（单圈，固定 }n_f\text{）}.
\end{aligned}
```

QCD 的结果是微扰的，采用与质量无关的方案，并在活跃味的组成改变时作阈值匹配。

**Ward 恒等式与反常**

对采用保持对称性的正规子的矢量型阿贝尔理论，设 $`\Gamma^\mu`$ 为去掉耦合常数后的正规流顶点，$`S_R(p)=i\mathcal S_R(p)`$ 为完整的费米子传播子。于是

```math
q_\mu\Gamma^\mu(p+q,p)
=\mathcal S_R^{-1}(p+q)-\mathcal S_R^{-1}(p),\qquad Z_1=Z_2.
```

其中 $`Z_1`$ 与 $`Z_2`$ 分别为顶点与费米子场的重整化常数。非阿贝尔规范理论满足含鬼场的 Slavnov--Taylor 恒等式。经典作用量的对称性在正规化后的量子测度下可能不再成立；自洽的手征规范理论要求规范反常相消。

<br><br>

<a id="qed-renormalization"></a>
### 7.1 QED 重整化

**规范固定后的拉氏量**

采用 (6.15) 的协变规范固定，电荷为 $`Q_fe`$、质量为 $`m_f`$ 的 Dirac 场 $`\psi_f`$ 的 QED 拉氏量 (3.26) 为

```math
\mathcal L
=\sum_f\bar\psi_f\bigl(i\gamma^\mu\partial_\mu-m_f\bigr)\psi_f
-\frac14F_{\mu\nu}F^{\mu\nu}
-\frac1{2\xi}(\partial_\mu A^\mu)^2
+eA_\mu\sum_fQ_f\,\bar\psi_f\gamma^\mu\psi_f .
```

如 (4.41) 之后所述，Faddeev--Popov 鬼场退耦。


**费曼规则**

对 $`i\mathcal M`$ 有贡献的动量空间因子为

```math
\begin{array}{l|l}
\text{图元}&\text{因子}\\ \hline
\text{费米子传播子，动量 }p\text{ 沿箭头方向}&\dfrac{i(\not p+m_f)}{p^2-m_f^2+i\varepsilon}\\[12pt]
\text{光子传播子}&\dfrac{-i}{p^2+i\varepsilon}\left[\eta_{\mu\nu}-(1-\xi)\dfrac{p_\mu p_\nu}{p^2+i\varepsilon}\right]\\[12pt]
\text{费米子–光子顶点}&ieQ_f\gamma^\mu\\[4pt]
\text{入射 / 出射费米子}&u^s(p)\ /\ \bar u^s(p)\\
\text{入射 / 出射反费米子}&\bar v^s(p)\ /\ v^s(p)\\
\text{入射 / 出射光子}&\epsilon^r_\mu(p)\ /\ \epsilon^{r*}_\mu(p)
\end{array}
```

对电子，$`Q_f=-1`$，顶点为 $`-ie\gamma^\mu`$。沿每条费米子线，按与箭头相反的顺序写出各因子，使旋量指标构成矩阵乘积。在每个顶点施加四动量守恒，每个圈动量用 $`\int d^4\ell/(2\pi)^4`$ 积分，并按 (7.3) 延拓到 $`d`$ 维。每个闭合费米子圈给出因子 $`-1`$ 和一个 Dirac 迹；与 [6.3 节](QFT-zh-part-03.md#feynman-diagrams) 相同，交换全同的外费米子改变符号。

**树级：$`e^+e^-\to q\bar q`$**

<p align="center"><img src="figures/ee-to-qqbar.svg" alt="e+ e- → q qbar 的树级 s 道图" width="440"></p>

时间从左向右。费米子线上的箭头表示费米子数的流向；灰色箭头表示四动量。

把 $`e^-,e^+,q,\bar q`$ 的自旋分别记为 $`s,s',r,r'`$，把 $`q,\bar q`$ 的色记为 $`c,c'\in\{1,2,3\}`$；光子顶点在色空间中是对角的，且 $`p_1+p_2=k_1+k_2`$。用 (7.10) 逆着箭头读出每条费米子线，

```math
\begin{aligned}
i\mathcal M
={}&\bigl[\bar v^{s'}(p_2)\,(-ie\gamma^\mu)\,u^s(p_1)\bigr]\,
\frac{-i}{(p_1+p_2)^2+i\varepsilon}
\left[\eta_{\mu\nu}-(1-\xi)\frac{(p_1+p_2)_\mu(p_1+p_2)_\nu}{(p_1+p_2)^2+i\varepsilon}\right]\\[6pt]
&\times\bigl[\bar u^r(k_1)\,(ieQ_q\gamma^\nu)\,v^{r'}(k_2)\bigr]\,\delta_{cc'} .
\end{aligned}
```


**表观发散度**

对 QED 的连通图，设 $`V`$ 为顶点数，$`I_\gamma,I_F`$ 分别为光子内线与费米子内线的条数，$`E_\gamma,E_F`$ 分别为光子外线与费米子外线的条数。(7.9) 的每个顶点连接两条费米子线和一条光子线，且不含导数。统计线的端点数，并在 $`d=4`$ 时利用 (7.2)，

```math
\begin{aligned}
2V&=2I_F+E_F,\qquad V=2I_\gamma+E_\gamma,\qquad L=I_\gamma+I_F-V+1,\\[6pt]
\omega&=4L-2I_\gamma-I_F=2I_\gamma+3I_F-4V+4 .
\end{aligned}
```

利用 $`I_\gamma=\tfrac12(V-E_\gamma)`$ 与 $`I_F=V-\tfrac12E_F`$ 消元，

```math
\boxed{\omega=4-E_\gamma-\frac32E_F .}
```

由 (7.1)，四维中 $`[e]=0`$，因此对 $`V`$ 的依赖相消。

**两条外腿**

每个顶点都守恒费米子数，因此 $`E_F`$ 为偶数，两条外腿即 $`(E_F,E_\gamma)=(2,0)`$ 或 $`(0,2)`$。设 $`-i\Sigma(p)`$ 与 $`i\Pi^{\mu\nu}(p)`$ 分别为含两条费米子外线、含两条光子外线的截肢 1PI 图之和，其中 $`p`$ 为外动量。

**(1) 费米子传播子**

```math
E_F=2,\qquad E_\gamma=0\qquad\Longrightarrow\qquad\omega=1 .
```

<p align="center"><img src="figures/fermion-self-energy.svg" alt="单圈费米子自能" width="322"></p>

费米子 $`f`$ 的 $`-i\Sigma(p)`$ 的单圈图：内费米子沿其箭头携带 $`\ell`$，光子携带 $`p-\ell`$。

设 $`-i\Sigma_2(p)`$ 为 $`-i\Sigma(p)`$ 的 $`O(e^2)`$ 部分。从顶点 $`\nu`$ 出发，用 (7.10) 逆着箭头读这条线，

```math
\begin{aligned}
-i\Sigma_2(p)
=\int\frac{d^4\ell}{(2\pi)^4}\,
&(ieQ_f\gamma^\nu)\,\frac{i(\not\ell+m_f)}{\ell^2-m_f^2+i\varepsilon}\,(ieQ_f\gamma^\mu)\\[6pt]
&\times\frac{-i}{(p-\ell)^2+i\varepsilon}\left[\eta_{\mu\nu}-(1-\xi)\frac{(p-\ell)_\mu(p-\ell)_\nu}{(p-\ell)^2+i\varepsilon}\right].
\end{aligned}
```

对夸克，(7.15) 乘以色空间中的单位矩阵。

在 $`d=4-\epsilon`$ 维中，如 (7.3) 把 $`d^4\ell/(2\pi)^4`$ 换成 $`d^d\ell/(2\pi)^d`$，如 (7.4) 令耦合常数携带 $`\mu`$ 因子，即 $`e\to\mu^{\epsilon/2}e`$，并按 $`\{\gamma^\mu,\gamma^\nu\}=2\eta^{\mu\nu}I_4`$ 与 $`\eta^\mu{}_\mu=d`$ 把 $`\gamma`$ 矩阵延拓到 $`d`$ 维。合并因子 $`(ieQ_f)^2\,i\,(-i)=-e^2Q_f^2`$，并利用 $`\gamma^\nu\gamma_\nu=d\,I_4`$、$`\gamma^\nu\not a\gamma_\nu=-(d-2)\not a`$，以及对 $`\ell=p-k`$ 成立的 $`\not k(\not\ell+m_f)\not k=2(k\cdot p)\not k+k^2(m_f-\not p-\not k)`$，其中 $`k^2`$ 消去一个因子 $`\mathcal P_\gamma`$，

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

用费曼参数 $`x`$ 合并分母：

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

作平移 $`\ell\to\ell+xp`$，于是 $`k\to(1-x)p-\ell`$；去掉 $`\ell`$ 的奇次项，并把 $`\ell^\mu\ell^\nu`$ 换成 $`\eta^{\mu\nu}\ell^2/d`$。(7.16) 的分子变为

```math
\begin{aligned}
d\,m_f-(d-2)\not\ell\ &\to\ d\,m_f-(d-2)x\not p,\\[4pt]
m_f-\not p-\not k\ &\to\ m_f-(2-x)\not p,\\[4pt]
2(k\cdot p)\not k\ &\to\ 2(1-x)^2p^2\not p+2(p\cdot\ell)\not\ell
\ \to\ 2(1-x)^2p^2\not p+\frac2d\,\ell^2\not p,
\end{aligned}
```

于是

```math
\begin{aligned}
-i\Sigma_2(p)
={}&-\mu^{\epsilon}e^2Q_f^2\int_0^1dx\int\frac{d^d\ell}{(2\pi)^d}\,\biggl\{
\frac{d\,m_f-(d-2)x\not p-(1-\xi)\bigl[m_f-(2-x)\not p\bigr]}{\bigl(\ell^2-\Delta_{\Sigma,f}+i\varepsilon\bigr)^2}\\[6pt]
&-(1-\xi)\,\frac{2x\bigl[2(1-x)^2p^2+\frac2d\,\ell^2\bigr]\not p}{\bigl(\ell^2-\Delta_{\Sigma,f}+i\varepsilon\bigr)^3}\biggr\}.
\end{aligned}
```

Wick 转动后，对 $`\Delta>0`$ 求积分，再经 $`\Delta-i\varepsilon`$ 延拓到 $`\Delta<0`$；对 $`n=2,3`$，

```math
\begin{aligned}
\int\frac{d^d\ell}{(2\pi)^d}\,\frac{1}{(\ell^2-\Delta+i\varepsilon)^n}
&=\frac{(-1)^n\,i}{(4\pi)^{d/2}}\,\frac{\Gamma\bigl(n-\frac d2\bigr)}{\Gamma(n)}\,(\Delta-i\varepsilon)^{\frac d2-n},\\[6pt]
\int\frac{d^d\ell}{(2\pi)^d}\,\frac{\ell^2}{(\ell^2-\Delta+i\varepsilon)^n}
&=\frac{(-1)^{n-1}\,i}{(4\pi)^{d/2}}\,\frac d2\,\frac{\Gamma\bigl(n-1-\frac d2\bigr)}{\Gamma(n)}\,(\Delta-i\varepsilon)^{\frac d2-n+1}.
\end{aligned}
```

把 (7.20) 用于 (7.19)，

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

取 $`d=4-\epsilon`$，利用 $`\Gamma(\epsilon/2)=2/\epsilon-\gamma_E+O(\epsilon)`$ 和 (7.3) 中的 $`2/\bar\epsilon`$，

```math
\boxed{
\begin{aligned}
\Sigma_2(p)={}&\frac{e^2Q_f^2}{16\pi^2}\int_0^1dx\,\biggl\{
\Bigl[4m_f-2x\not p-(1-\xi)\bigl(m_f-2(1-x)\not p\bigr)\Bigr]
\left[\frac2{\bar\epsilon}-\ln\frac{\Delta_{\Sigma,f}-i\varepsilon}{\mu^2}\right]\\[6pt]
&-2m_f+2x\not p+\frac{2(1-\xi)\,x(1-x)\,p^2\not p}{m_f^2-xp^2-i\varepsilon}\biggr\}+O(\epsilon)\\[6pt]
={}&\frac{e^2Q_f^2}{16\pi^2}\,\frac2\epsilon\,\bigl[(3+\xi)m_f-\xi\not p\bigr]+(\epsilon\to0\text{ 时有限}).
\end{aligned}
}
```

**(2) 光子传播子**

```math
E_\gamma=2,\qquad E_F=0\qquad\Longrightarrow\qquad\omega=2 .
```

<p align="center"><img src="figures/photon-self-energy.svg" alt="单圈光子自能" width="298"></p>

$`i\Pi^{\mu\nu}(p)`$ 的单圈图，含费米子 $`f`$ 的一个闭合圈：圈上的动量 $`\ell+p`$ 与 $`\ell`$ 沿箭头方向流动。

设 $`i\Pi_2^{\mu\nu}(p)`$ 为 $`i\Pi^{\mu\nu}(p)`$ 的 $`O(e^2)`$ 部分。从顶点 $`\mu`$ 出发，用 (7.10) 逆着箭头读这个圈，

```math
\begin{aligned}
i\Pi_2^{\mu\nu}(p)
=\sum_fN_{\mathrm c,f}\,(-1)\int\frac{d^4\ell}{(2\pi)^4}\,
\mathop{\rm tr}\nolimits \biggl[
&(ieQ_f\gamma^\mu)\,\frac{i(\not\ell+m_f)}{\ell^2-m_f^2+i\varepsilon}\\[6pt]
&\times(ieQ_f\gamma^\nu)\,\frac{i(\not\ell+\not p+m_f)}{(\ell+p)^2-m_f^2+i\varepsilon}\biggr],
\end{aligned}
```

其中因子 $`-1`$ 与 Dirac 迹来自闭合费米子圈，$`N_{\mathrm c,f}`$ 为 $`f`$ 的色数（轻子为 $`1`$，夸克为 $`3`$），来自色迹。

在 $`d=4-\epsilon`$ 维中，如 (7.3) 把 $`d^4\ell/(2\pi)^4`$ 换成 $`d^d\ell/(2\pi)^d`$，并如 (7.4) 令耦合常数携带 $`\mu`$ 因子，即 $`e\to\mu^{\epsilon/2}e`$。合并因子 $`(-1)(ieQ_f)^2i^2=-e^2Q_f^2`$，并利用 $`\mathop{\rm tr}\nolimits (\gamma^\mu\gamma^\nu)=4\eta^{\mu\nu}`$、$`\mathop{\rm tr}\nolimits (\gamma^\mu\gamma^\rho\gamma^\nu\gamma^\sigma)=4(\eta^{\mu\rho}\eta^{\nu\sigma}-\eta^{\mu\nu}\eta^{\rho\sigma}+\eta^{\mu\sigma}\eta^{\rho\nu})`$，以及奇数个 $`\gamma`$ 矩阵之积的迹为零，

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

用费曼参数 $`x`$ 合并分母：

```math
\begin{aligned}
\frac{1}{\mathcal P_1\mathcal P_2}
&=\int_0^1\frac{dx}{\bigl[x\mathcal P_2+(1-x)\mathcal P_1\bigr]^2}
=\int_0^1\frac{dx}{\bigl[(\ell+xp)^2-\Delta_f+i\varepsilon\bigr]^2},\\[6pt]
\Delta_f&:=m_f^2-x(1-x)p^2 .
\end{aligned}
```

作平移 $`\ell\to\ell-xp`$，并去掉积分为零的 $`\ell`$ 奇次项；再在积分号下把 $`\ell^\mu\ell^\nu`$ 换成 $`\eta^{\mu\nu}\ell^2/d`$。(7.25) 的分子变为

```math
\begin{aligned}
&\ell^\mu(\ell+p)^\nu+\ell^\nu(\ell+p)^\mu-\eta^{\mu\nu}\bigl[\ell\cdot(\ell+p)-m_f^2\bigr]\\[4pt]
&\quad\to\ 2\ell^\mu\ell^\nu-\eta^{\mu\nu}\ell^2-2x(1-x)p^\mu p^\nu+\eta^{\mu\nu}\bigl[x(1-x)p^2+m_f^2\bigr]\\[4pt]
&\quad\to\ 2x(1-x)\bigl(p^2\eta^{\mu\nu}-p^\mu p^\nu\bigr)+\eta^{\mu\nu}\Bigl[\frac{2-d}{d}\,\ell^2+\Delta_f\Bigr],
\end{aligned}
```

于是

```math
\begin{aligned}
i\Pi_2^{\mu\nu}(p)
={}&-4\mu^{\epsilon}e^2\sum_fN_{\mathrm c,f}Q_f^2\int_0^1dx\int\frac{d^d\ell}{(2\pi)^d}\,
\frac{1}{\bigl(\ell^2-\Delta_f+i\varepsilon\bigr)^2}\\[6pt]
&\times\Bigl\{2x(1-x)\bigl(p^2\eta^{\mu\nu}-p^\mu p^\nu\bigr)+\eta^{\mu\nu}\Bigl[\frac{2-d}{d}\,\ell^2+\Delta_f\Bigr]\Bigr\}.
\end{aligned}
```

Wick 转动后，对 $`\Delta>0`$ 求积分，再经 $`\Delta-i\varepsilon`$ 延拓到 $`\Delta<0`$，

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

其中最后一行用到 $`\Gamma(2-\tfrac d2)=(1-\tfrac d2)\Gamma(1-\tfrac d2)`$。(7.28) 中只有横向项保留下来：

```math
\begin{aligned}
i\Pi_2^{\mu\nu}(p)
={}&-4\mu^{\epsilon}e^2\sum_fN_{\mathrm c,f}Q_f^2\int_0^1dx\,2x(1-x)\bigl(p^2\eta^{\mu\nu}-p^\mu p^\nu\bigr)\\[6pt]
&\times\frac{i}{(4\pi)^{d/2}}\,\Gamma\Bigl(2-\frac d2\Bigr)(\Delta_f-i\varepsilon)^{\frac d2-2} .
\end{aligned}
```

取 $`d=4-\epsilon`$，利用 $`\Gamma(\epsilon/2)=2/\epsilon-\gamma_E+O(\epsilon)`$ 和 (7.3) 中的 $`2/\bar\epsilon`$，

```math
\boxed{
\begin{aligned}
\Pi_2^{\mu\nu}(p)&=\bigl(p^2\eta^{\mu\nu}-p^\mu p^\nu\bigr)\,\Pi_2(p^2),\\[6pt]
\Pi_2(p^2)&=-\frac{e^2}{2\pi^2}\sum_fN_{\mathrm c,f}Q_f^2\int_0^1dx\,x(1-x)\left[\frac2{\bar\epsilon}-\ln\frac{\Delta_f-i\varepsilon}{\mu^2}\right]+O(\epsilon).
\end{aligned}
}
```

**三条外腿**

三条外腿即 $`(E_F,E_\gamma)=(2,1)`$ 或 $`(0,3)`$。设 $`ieQ_f\Gamma^\mu(p',p)`$ 为截肢 1PI 图之和，图中有动量为 $`p`$ 的入射费米子、动量为 $`p':=p+q`$ 的出射费米子，以及动量为 $`q`$、指标为 $`\mu`$ 的入射光子，这样 $`\Gamma^\mu`$ 就是 (7.8) 中的正规顶点。记 $`\Gamma^\mu=\gamma^\mu+\Lambda^\mu`$。

**(1) 顶点**

```math
E_F=2,\qquad E_\gamma=1\qquad\Longrightarrow\qquad\omega=0 .
```

<p align="center"><img src="figures/vertex.svg" alt="单圈 QED 顶点" width="370"></p>

费米子 $`f`$ 的 $`ieQ_f\Lambda^\mu(p',p)`$ 的单圈图：两条内费米子线沿各自的箭头分别携带 $`\ell`$ 与 $`\ell+q`$，内光子携带 $`p-\ell`$。

设 $`\Lambda_2^\mu(p',p)`$ 为 $`\Lambda^\mu(p',p)`$ 的 $`O(e^2)`$ 部分。从顶点 $`\nu`$ 出发，用 (7.10) 逆着箭头读这条线，

```math
\begin{aligned}
ieQ_f\Lambda_2^\mu(p',p)
=\int\frac{d^4\ell}{(2\pi)^4}\,
&(ieQ_f\gamma^\nu)\,\frac{i(\not\ell+\not q+m_f)}{(\ell+q)^2-m_f^2+i\varepsilon}\,(ieQ_f\gamma^\mu)\\[6pt]
&\times\frac{i(\not\ell+m_f)}{\ell^2-m_f^2+i\varepsilon}\,(ieQ_f\gamma^\rho)\\[6pt]
&\times\frac{-i}{(p-\ell)^2+i\varepsilon}\left[\eta_{\nu\rho}-(1-\xi)\frac{(p-\ell)_\nu(p-\ell)_\rho}{(p-\ell)^2+i\varepsilon}\right].
\end{aligned}
```

对夸克，(7.33) 乘以色空间中的单位矩阵。

在 $`d=4-\epsilon`$ 维中，按 (7.16) 的做法延拓，其中剥离出的耦合 $`ieQ_f`$ 也携带 $`\mu^{\epsilon/2}`$。合并因子 $`(ieQ_f)^3\,i\cdot i\cdot(-i)=(ieQ_f)(-ie^2Q_f^2)`$，

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

用费曼参数 $`x,y,z`$ 合并分母：

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

作平移 $`\ell\to\ell+A`$，于是 $`\ell'\to\ell+A'`$，$`k\to K-\ell`$，其中 $`A:=(1-x)p-yp'`$，$`A':=(1-y)p'-xp`$，$`K:=xp+yp'`$。去掉 $`\ell`$ 的奇次项，并把 $`\ell^\alpha\ell^\beta`$ 换成 $`\eta^{\alpha\beta}\ell^2/d`$；再利用 $`\not\ell\not\ell=\ell^2`$，(7.34) 的分子变为

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

于是

```math
\begin{aligned}
\Lambda_2^\mu(p',p)
={}&-i\mu^{\epsilon}e^2Q_f^2\int dF\int\frac{d^d\ell}{(2\pi)^d}\,\biggl\{
\frac{2\bigl[\frac{(d-2)^2}{d}\,\ell^2\gamma^\mu+N^\mu\bigr]}{\bigl(\ell^2-\Delta_{V,f}+i\varepsilon\bigr)^3}\\[6pt]
&-6(1-\xi)\,z\,\frac{(\ell^2)^2\gamma^\mu+\ell^2N_2^\mu+N_0^\mu}{\bigl(\ell^2-\Delta_{V,f}+i\varepsilon\bigr)^4}\biggr\}.
\end{aligned}
```

Wick 转动后，对 $`\Delta>0`$ 求积分，再经 $`\Delta-i\varepsilon`$ 延拓到 $`\Delta<0`$，积分 (7.20) 推广为

```math
\int\frac{d^d\ell}{(2\pi)^d}\,\frac{(\ell^2)^a}{(\ell^2-\Delta+i\varepsilon)^n}
=\frac{(-1)^{n+a}\,i}{(4\pi)^{d/2}}\,
\frac{\Gamma\bigl(a+\frac d2\bigr)\,\Gamma\bigl(n-a-\frac d2\bigr)}{\Gamma\bigl(\frac d2\bigr)\,\Gamma(n)}\,
(\Delta-i\varepsilon)^{\frac d2+a-n}.
```

把 (7.38) 用于 (7.37)，

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

取 $`d=4-\epsilon`$，利用 $`\Gamma(\epsilon/2)=2/\epsilon-\gamma_E+O(\epsilon)`$ 与 (7.3) 中的 $`2/\bar\epsilon`$，并在有限项中取 $`N^\mu`$、$`N_2^\mu`$ 在 $`d=4`$ 时的值，

```math
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
```

除非 $`p^2=p'^2=m_f^2`$，参数积分都收敛；在这一在壳情形下，积分在 $`z\to1`$ 处对数发散。结合 (7.22)，上述结果满足 $`q_\mu\Lambda_2^\mu(p+q,p)=\Sigma_2(p)-\Sigma_2(p+q)`$，这正是 (7.8) 所要求的。

**(2) 三光子**

```math
E_\gamma=3,\qquad E_F=0\qquad\Longrightarrow\qquad\omega=1 .
```

费米子圈两种取向的图相互抵消（Furry 定理），因此含三条光子外线的 1PI 图之和为零。

<br><br>





































<a id="qft-ch8"></a>
## 8. 多圈重整化

**子发散与森林公式**

在单圈以上，发散子图可以是嵌套的、不相交的或重叠的。在有质量的 BPHZ 重整化中，取减除点以避开红外奇点；设 $`\mathcal I_{\mathcal G}`$ 为 1PI 图 $`\mathcal G`$ 的被积函数，$`t_\gamma`$ 为按发散 1PI 子图 $`\gamma`$ 的外动量作 Taylor 展开、展开到其表观发散度阶的减除。则

```math
\boxed{R\mathcal I_{\mathcal G}
=\sum_{F\in\mathfrak F(\mathcal G)}
\left[\prod_{\gamma\in F}(-t_\gamma)\right]\mathcal I_{\mathcal G}.}
```

森林 $`F`$ 只包含两两嵌套或不相交的减除子图。求和包括空森林；若整个图发散，也包括整个图。嵌套的减除从最内层子图开始向外依次作用。低阶反项的插入是高圈计算的一部分。

**极点结构与两圈跑动**

对单一耦合的、与质量无关的最小减除方案中的乘性重整化常数，

```math
Z=1+\sum_{L=1}^{\infty}
\left(\frac{g_s^2}{16\pi^2}\right)^L
\sum_{k=1}^{L}\frac{z_{Lk}}{\epsilon^k}.
```

重整化群的自洽性把高次极点与低阶数据联系起来。对 QCD，

```math
\begin{aligned}
\beta_{g_s}&=-\frac{\beta_0g_s^3}{16\pi^2}
-\frac{\beta_1g_s^5}{(16\pi^2)^2}+O(g_s^7),\\
\beta_0&=11-\frac23n_f,\qquad
\beta_1=102-\frac{38}{3}n_f.
\end{aligned}
```

在通常的与质量无关的方案范围内，这前两个系数在解析的、与标度无关的耦合重定义下保持不变。更高阶的系数依赖于方案。

**积分族与分部积分**

对 $`L`$ 个圈动量 $`k_\ell`$ 与分母因子 $`D_j=q_j^2-m_j^2+i\varepsilon`$（其中 $`q_j`$ 为圈动量与外动量的线性组合），定义

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

其中 $`v^\mu`$ 为圈动量或外动量。在维数正规化中，分部积分恒等式通过从表面项为零的区域作解析延拓而成立。分子中的标量积可在补全的积分族中以零次或负次幂计入。

**主积分与微分方程**

经代数约化后，选定的积分族可以用由主积分 $`M_r`$ 构成的有限基表示。对运动学不变量 $`s`$，

```math
I_{\nu_1\cdots\nu_N}=\sum_r c_r(d,\{p\cdot p\},\{m^2\})M_r,
\qquad
\frac{\partial M_r}{\partial s}=\sum_t A_{rt}(d,\{p\cdot p\},\{m^2\})M_t.
```

求解这些方程需要边界值和费曼解析延拓。减除前必须区分紫外极点与红外极点；无标度积分在维数正规化中为零，但可能掩盖紫外极点与红外极点之间的相消。高圈手征计算还需要明确的 $`d`$ 维 $`\gamma^5`$ 处方；仅靠四维 Weyl 矩阵给不出这样的处方。

<br><br>

<a id="qft-ch9"></a>
## 9. 宇宙学

