> 中文版第 1/4 部分 · [完整文件](QFT-zh.md) · [1](QFT-zh-part-01.md) · [2](QFT-zh-part-02.md) · [3](QFT-zh-part-03.md) · [4](QFT-zh-part-04.md)

# QFT（中文版）

## 目录

- [0. 数学基础](#qft-ch0)
  - [0.1 Fourier 变换](#fourier-transform)
  - [0.2 $`\gamma`$ 矩阵：Weyl 表示](#gamma-matrices)
  - [0.3 IO(1,3) 群](#classical-poincare)
  - [0.4 格林函数](#greens-functions)
- [1. 经典场论](#qft-ch1)
  - [1.1 拉格朗日形式](#lagrangian-formalism)
    - [拉氏量](#mechanics-lagrangian)
    - [对称变换与 Noether 定理](#lagrangian-symmetry)
  - [1.2 哈密顿形式](#hamiltonian-formalism)
    - [动力系统](#dynamical-systems)
    - [哈密顿形式](#hamiltonian-mechanics)
    - [对称性与 Noether 定理](#hamiltonian-symmetry)
  - [1.3 经典场的定义](#classical-field)
    - [场的定义](#field-definition)
    - [$`SO(1,3)^+`$ 的有限维表示](#lorentz-finite-representations)
  - [1.4 经典场的动力学](#classical-dynamics)
    - [拉氏量](#field-theory-lagrangian)
    - [对称变换与 Noether 定理](#classical-noether)
  - [1.5 Dirac 约束](#dirac-constraint)
    - [奇异拉氏量](#singular-lagrangian)
  - [1.6 标量场](QFT-zh-part-02.md#scalar-field)
    - [拉氏量](QFT-zh-part-02.md#scalar-lagrangian)
    - [Klein–Gordon 方程的解](QFT-zh-part-02.md#scalar-field-solutions)
  - [1.7 Dirac 场 $`\psi`$ ](QFT-zh-part-02.md#dirac-field)
    - [拉氏量](QFT-zh-part-02.md#dirac-lagrangian)
    - [Weyl 表示下 Dirac 方程的解](QFT-zh-part-02.md#weyl-spinor-solutions)
    - [Dirac 双线性型](QFT-zh-part-02.md#dirac-bilinears)
  - [1.8 Proca 场](QFT-zh-part-02.md#proca-field)
    - [拉氏量](QFT-zh-part-02.md#proca-lagrangian)
    - [Proca 方程的解](QFT-zh-part-02.md#proca-field-solutions)
  - [1.9 矢量场](QFT-zh-part-02.md#vector-field)
    - [拉氏量](QFT-zh-part-02.md#maxwell-lagrangian)
    - [Maxwell 方程的解](QFT-zh-part-02.md#maxwell-field-solutions)
- [2. 算符量子化](QFT-zh-part-02.md#qft-ch2)
  - [2.1 绘景](QFT-zh-part-02.md#pictures-of-time-evolution)
    - [Schrödinger 绘景](QFT-zh-part-02.md#schrodinger-picture)
    - [Heisenberg 绘景](QFT-zh-part-02.md#heisenberg-picture)
  - [2.2 正则量子化](QFT-zh-part-02.md#canonical-quantization)
    - [自由实标量场量子化](QFT-zh-part-02.md#free-real-scalar-field-quantization)
  - [2.3 用 Dirac 括号量子化](QFT-zh-part-02.md#quantization-with-dirac-brackets)
    - [复标量场的量子化](QFT-zh-part-02.md#complex-scalar-field-quantization)
    - [Dirac 场的量子化](QFT-zh-part-02.md#dirac-field-quantization)
    - [Proca 场的量子化](QFT-zh-part-02.md#proca-field-quantization)
  - [2.4 Gupta–Bleuler 量子化](QFT-zh-part-02.md#gupta-bleuler-quantization)
  - [2.5 对称性](QFT-zh-part-02.md#symmetry)
    - [Ward 恒等式](QFT-zh-part-02.md#ward-identity)
- [3. 路径积分](QFT-zh-part-02.md#qft-ch3)
  - [3.1 量子力学中的路径积分](QFT-zh-part-02.md#path-integrals-in-quantum-mechanics)
  - [3.2 量子场论中的路径积分](QFT-zh-part-02.md#path-integrals-in-field-theory)
  - [3.3 $`\phi^3`$ 理论](QFT-zh-part-03.md#phi-cubed-theory)
  - [3.4 费米子场的路径积分](QFT-zh-part-03.md#path-integrals-for-fermion-fields)
    - [Grassmann 代数](QFT-zh-part-03.md#grassmann-algebra)
    - [Grassmann 代数上的微积分](QFT-zh-part-03.md#grassmann-calculus)
  - [3.5 路径积分中的对称性](QFT-zh-part-03.md#symmetry-in-path-integrals)
  - [3.6 路径积分中的散射理论](QFT-zh-part-03.md#scattering-theory-in-path-integrals)
- [4. 散射理论](QFT-zh-part-03.md#qft-ch4)
  - [4.1 相互作用绘景](QFT-zh-part-03.md#interaction-picture)
  - [4.2 S 矩阵与 Wick 定理](QFT-zh-part-03.md#s-matrix-and-wick-theorem)
  - [4.3 费曼图与费曼规则](QFT-zh-part-03.md#feynman-diagrams)
  - [4.4 关联函数](QFT-zh-part-03.md#correlation-functions)
    - [微扰真空关联函数](QFT-zh-part-03.md#perturbative-correlation-functions)
    - [非微扰真空关联函数](QFT-zh-part-03.md#nonperturbative-correlation-functions)
  - [4.5 LSZ 约化公式](QFT-zh-part-03.md#lsz-reduction)
  - [4.6 截面与衰变率](QFT-zh-part-03.md#cross-sections-and-decay-rates)
- [5. 标准模型](QFT-zh-part-03.md#qft-ch5)
  - [5.1 Yang–Mills 理论](QFT-zh-part-03.md#yang-mills)
  - [5.2 量子电动力学](QFT-zh-part-03.md#qed)
  - [5.3 量子色动力学](QFT-zh-part-03.md#qcd)
  - [5.4 自发对称性破缺与 Higgs 机制](QFT-zh-part-03.md#higgs-mechanism)
    - [Higgs 拉氏量](QFT-zh-part-03.md#higgs-lagrangian)
    - [自发对称性破缺](QFT-zh-part-03.md#spontaneous-symmetry-breaking)
    - [Higgs 机制](QFT-zh-part-03.md#higgs-mechanism-masses)
  - [5.5 电弱理论](QFT-zh-part-04.md#electroweak-theory)
    - [标准模型中的轻子](QFT-zh-part-04.md#sm-leptons)
    - [动能项](QFT-zh-part-04.md#electroweak-kinetic-terms)
    - [Yukawa 耦合与带电轻子质量](QFT-zh-part-04.md#charged-lepton-masses)
    - [规范玻色子质量](QFT-zh-part-04.md#gauge-boson-masses)
    - [夸克](QFT-zh-part-04.md#sm-quarks)
    - [带电流与中性流](QFT-zh-part-04.md#electroweak-currents)
- [6. 超出标准模型的新物理](QFT-zh-part-04.md#qft-ch6)
  - [6.1 Seesaw 机制](QFT-zh-part-04.md#seesaw-mechanism)
    - [I 型 seesaw](QFT-zh-part-04.md#type-i-seesaw)
    - [II 型 seesaw](QFT-zh-part-04.md#type-ii-seesaw)
    - [III 型 seesaw](QFT-zh-part-04.md#type-iii-seesaw)
    - [轻子生成](QFT-zh-part-04.md#leptogenesis)
  - [6.2 $`U(1)_{L_\mu-L_\tau}`$ 规范对称性](QFT-zh-part-04.md#lmu-ltau-gauge-symmetry)
- [7. 重整化](QFT-zh-part-04.md#qft-ch7)
  - [7.1 QED 重整化](QFT-zh-part-04.md#qed-renormalization)
- [8. 多圈重整化](QFT-zh-part-04.md#qft-ch8)
- [9. 宇宙学](QFT-zh-part-04.md#qft-ch9)
  - [9.1 宇宙的几何](QFT-zh-part-04.md#geometry-of-the-universe)
    - [实验事实](QFT-zh-part-04.md#cosmology-experimental-facts)
    - [FLRW 度规](QFT-zh-part-04.md#flrw-metric)
  - [9.2 宇宙的演化](QFT-zh-part-04.md#evolution-of-the-universe)
    - [动力学](QFT-zh-part-04.md#cosmology-dynamics)
    - [暗物质](QFT-zh-part-04.md#dark-matter)
    - [暗能量](QFT-zh-part-04.md#dark-energy)
    - [宇宙演化](QFT-zh-part-04.md#cosmic-evolution)

---

<a id="qft-ch0"></a>
## 0. 数学基础

<a id="fourier-transform"></a>
### 0.1 Fourier 变换

四维 Fourier 变换采用如下约定，因子 $`(2\pi)^{-4}`$ 放在逆变换中：

```math
\left.
\begin{aligned}
\widetilde f(p)&=\int d^4x\,e^{+ip\cdot x}f(x),\\
f(x)&=\int\frac{d^4p}{(2\pi)^4}\,e^{-ip\cdot x}\widetilde f(p).
\end{aligned}
\right.
\tag{0.1}
```

其中 $`x^\mu=(t,\mathbf x)`$，$`p^\mu=(p^0,\mathbf p)`$，相位为

```math
\left.
p\cdot x=p_\mu x^\mu=p^0t-\mathbf p\cdot\mathbf x.
\right.
\tag{0.2}
```

Dirac $`\delta`$ 函数的 Fourier 表示为

```math
\left.
\begin{aligned}
\int\frac{d^4p}{(2\pi)^4}\,e^{-ip\cdot(x-y)}&=\delta^{(4)}(x-y),\\[6pt]
\int d^4x\,e^{i(p-q)\cdot x}&=(2\pi)^4\delta^{(4)}(p-q).
\end{aligned}
\right.
\tag{0.3}
```


<br><br>

<a id="gamma-matrices"></a>
### 0.2 $`\gamma`$ 矩阵：Weyl 表示

Pauli 矩阵为

```math
\left.
\sigma^1=\begin{pmatrix}0&1\\1&0\end{pmatrix},\qquad
\sigma^2=\begin{pmatrix}0&-i\\i&0\end{pmatrix},\qquad
\sigma^3=\begin{pmatrix}1&0\\0&-1\end{pmatrix}.
\right.
\tag{0.4}
```

**Pauli 矩阵的性质**

对每个 $`i=1,2,3`$，

```math
\left.
(\sigma^i)^\dagger=\sigma^i,\qquad
(\sigma^i)^2=I_2,\qquad
(\sigma^i)^{-1}=\sigma^i,\qquad
\mathop{\rm tr}\nolimits\,\sigma^i=0,\qquad
\det\sigma^i=-1.
\right.
\tag{0.5}
```

因此，每个 Pauli 矩阵既是厄米矩阵又是幺正矩阵，本征值为 $`+1`$ 和 $`-1`$。

乘积恒等式为

```math
\left.
\sigma^i\sigma^j=\delta^{ij}I_2+i\epsilon^{ijk}\sigma^k.
\right.
\tag{0.6}
```

由此得到对易关系与反对易关系，以及迹正交关系：

```math
\left.
[\sigma^i,\sigma^j]=2i\epsilon^{ijk}\sigma^k,\qquad
\{\sigma^i,\sigma^j\}=2\delta^{ij}I_2,\qquad
\mathop{\rm tr}\nolimits (\sigma^i\sigma^j)=2\delta^{ij}.
\right.
\tag{0.7}
```

对任意 $`\mathbf a,\mathbf b\in\mathbb R^3`$，乘积恒等式也可写成

```math
\left.
(\mathbf a\cdot\boldsymbol\sigma)(\mathbf b\cdot\boldsymbol\sigma)
=(\mathbf a\cdot\mathbf b)I_2
+i(\mathbf a\times\mathbf b)\cdot\boldsymbol\sigma,
\qquad \boldsymbol\sigma=(\sigma^1,\sigma^2,\sigma^3).
\right.
\tag{0.8}
```

**$`\gamma`$ 矩阵**

Pauli 四矢量

```math
\left.
\sigma^\mu:=(I_2,\boldsymbol\sigma),\qquad
\bar\sigma^\mu:=(I_2,-\boldsymbol\sigma),\qquad \mu=0,1,2,3.
\right.
\tag{0.9}
```

用它们定义 Weyl 表示下的 $`\gamma`$ 矩阵：

```math
\left.
\gamma^\mu:=
\begin{pmatrix}
0&\sigma^\mu\\
\bar\sigma^\mu&0
\end{pmatrix}_{4\times4}.
\right.
\tag{0.10}
```

这些矩阵满足

```math
\left.
\{\gamma^\mu,\gamma^\nu\}=2\eta^{\mu\nu}I_4.
\right.
\tag{0.11}
```

```math
\left.
(\gamma^0)^2=I_4,\qquad
(\gamma^i)^2=-I_4,\\
(\gamma^0)^\dagger=\gamma^0,\qquad
(\gamma^i)^\dagger=-\gamma^i.
\right.
\tag{0.12}
```

因此每个 $`\gamma^\mu`$ 都是幺正的：

```math
\left.
(\gamma^\mu)^\dagger\gamma^\mu=I_4.
\right.
\tag{0.13}
```

定义

```math
\left.
\gamma^5:=i\gamma^0\gamma^1\gamma^2\gamma^3
=\begin{pmatrix}-I_2&0\\0&I_2\end{pmatrix}
.
\right.
\tag{0.14}
```

它满足

```math
\left.
(\gamma^5)^2=I_4,\qquad
\{\gamma^5,\gamma^\mu\}=0,\qquad
(\gamma^5)^\dagger = (\gamma^5).
\right.
\tag{0.15}
```

<br><br>

<a id="classical-poincare"></a>
### 0.3 IO(1,3) 群

**O(1,3) 群**

为区分矩阵 $`\Lambda`$ 与相应的坐标变换张量 $`\Lambda`$，把矩阵记为 $`[\Lambda]`$，张量仍简记为 $`\Lambda`$。对 $`\eta`$ 采用同样的记号。

矩阵 $`[\Lambda]`$

```math
\left.
O(1,3):=\{[\Lambda]\in GL(4,\mathbb R)\mid [\Lambda]^T[\eta][\Lambda]=[\eta]\}.
\right.
\tag{0.16}
```

其中 $`[\eta]=\mathop{\rm diag}\nolimits (1,-1,-1,-1)`$。

张量 $`\Lambda`$

给定 Minkowski 时空的一个具体的微分同胚 $`\phi:x\mapsto x'`$，得到张量

```math
\left.
\Lambda^\mu{}_\nu:=\frac{\partial x'^\mu}{\partial x^\nu}.
\right.
\tag{0.17}
```

顺便指出，可以证明 Minkowski 时空的等距变换必为线性的，至多相差一个平移。

$`[\Lambda]`$ 第 $`\mu`$ 行、第 $`\nu`$ 列的矩阵元就是张量 $`\Lambda`$ 的相应分量：

```math
\left.
[\Lambda]_{\mu\nu}=\Lambda^\mu{}_\nu.
\right.
\tag{0.18}
```

同理，

```math
\left.
[\eta]_{\mu\nu}=\eta_{\mu\nu}.
\right.
\tag{0.19}
```

因此，等价地有如下关系：

```math
\left.
\eta_{\mu\nu}\Lambda^\mu{}_\rho\Lambda^\nu{}_\sigma=\eta_{\rho\sigma}.
\right.
\tag{0.20}
```

其中用到了关系 $`([\Lambda]^T)_{\mu\nu}=\Lambda^\nu{}_\mu`$。这正是 $`\phi`$ 为 Minkowski 时空等距变换的条件。


$`[\Lambda]`$ 的逆和转置满足

```math
\left.
[\Lambda]^{-1}=[\eta][\Lambda]^T[\eta],\qquad
[\Lambda][\eta][\Lambda]^T=[\eta],
\right.
\tag{0.21}
```

故 $`[\Lambda]^{-1}`$ 和 $`[\Lambda]^T`$ 也属于 $`O(1,3)`$。

写成分量形式，第一个关系为

```math
\left.
(\Lambda^{-1})^\mu{}_\nu=\Lambda_\nu{}^\mu.
\right.
\tag{0.22}
```

**连通性**

对 $`[\Lambda]^T[\eta][\Lambda]=[\eta]`$ 取行列式，得

```math
\left.
(\det[\Lambda])^2=1\quad\Longrightarrow\quad\det[\Lambda]=\pm1.
\right.
\tag{0.23}
```

在 $`\eta_{\mu\nu}\Lambda^\mu{}_\rho\Lambda^\nu{}_\sigma=\eta_{\rho\sigma}`$ 中令 $`\rho=\sigma=0`$，得

```math
\left.
(\Lambda^0{}_0)^2=1+\sum_i(\Lambda^i{}_0)^2\ge1\quad\Longrightarrow\quad\Lambda^0{}_0\ge1\ \text{或}\ \Lambda^0{}_0\le-1.
\right.
\tag{0.24}
```

可以证明，$`O(1,3)`$ 恰有这四个连通分支。

定义时间反演 $`T`$ 与空间反演 $`P`$ 为

```math
\left.
T:(t,\mathbf x)\mapsto(-t,\mathbf x),\qquad
P:(t,\mathbf x)\mapsto(t,-\mathbf x),
\right.
\tag{0.25}
```

其矩阵为

```math
\left.
[T]=\mathop{\rm diag}\nolimits (-1,1,1,1),\qquad
[P]=\mathop{\rm diag}\nolimits (1,-1,-1,-1).
\right.
\tag{0.26}
```

相应的张量为

```math
\left.
T^\mu{}_\nu=\delta^\mu{}_\nu-2\delta^\mu{}_0\delta^0{}_\nu,\qquad
P^\mu{}_\nu=-\delta^\mu{}_\nu+2\delta^\mu{}_0\delta^0{}_\nu.
\right.
\tag{0.27}
```

<div style="display: flex; justify-content: center;">

| 连通分支 | $`\det[\Lambda]`$ | $`\Lambda^0{}_0`$ | 代表元 |
|:---:|:---:|:---:|:---:|
| $`\mathcal L^\uparrow_+`$ | $`+1`$ | $`\ge1`$ | $`I`$ |
| $`\mathcal L^\downarrow_+`$ | $`+1`$ | $`\le-1`$ | $`[PT]`$ |
| $`\mathcal L^\uparrow_-`$ | $`-1`$ | $`\ge1`$ | $`[P]`$ |
| $`\mathcal L^\downarrow_-`$ | $`-1`$ | $`\le-1`$ | $`[T]`$ |

</div>

$`SO(1,3)`$ 由 $`\det[\Lambda]=+1`$ 的两类组成：

```math
\left.
SO(1,3)=\mathcal L^\uparrow_+\cup\mathcal L^\downarrow_+.
\right.
\tag{0.28}
```

此外，$`SO(1,3)^+=\mathcal L^\uparrow_+`$ 是 $`O(1,3)`$ 的子群。

从物理上看，$`T`$ 和 $`P`$ 分别对应时间反演对称性和宇称对称性。通常所说的 Lorentz 对称性仅指在 $`SO(1,3)^+`$ 下的不变性。这一区分很重要：Lorentz 对称性的破坏从未被观测到，因此它被视为基本对称性。相反，宇称在弱相互作用中不守恒，这由 Lee 和 Yang 提出，并由 Wu 等人在实验上证实；时间反演对称性同样被破坏。

**O(1,3) 的李代数**

考虑 $`O(1,3)`$ 的单参数子群 $`e^{tX}`$，$`t\in\mathbb R`$。它满足

```math
\left.
(e^{tX})^T[\eta]\,e^{tX}=[\eta].
\right.
\tag{0.29}
```

把左边展开到 $`t`$ 的一阶，得

```math
\left.
(I+tX^T)[\eta](I+tX)+O(t^2)=[\eta]+t\left(X^T[\eta]+[\eta]X\right)+O(t^2),
\right.
\tag{0.30}
```

故一阶项必须为零：

```math
\left.
X^T[\eta]+[\eta]X=0.
\right.
\tag{0.31}
```

因此，

```math
\left.
\mathfrak o(1,3):=\{X\in M_4(\mathbb R)\mid X^T[\eta]+[\eta]X=0\}.
\right.
\tag{0.32}
```

此外，这一关系可以更明确地写成

```math
\left.
[\eta]X=-X^T[\eta]=-([\eta]X)^T,
\right.
\tag{0.33}
```

这意味着矩阵 $`[\eta]X`$ 是反对称的。

$`4\times4`$ 反对称矩阵有 $`4\times3/2=6`$ 个独立的实参数。因此 $`X`$ 的一般形式为

```math
\left.
X=\begin{pmatrix}
0&b^1&b^2&b^3\\
b^1&0&-\theta^3&\theta^2\\
b^2&\theta^3&0&-\theta^1\\
b^3&-\theta^2&\theta^1&0
\end{pmatrix}
=\sum_i\theta^iJ^i+\sum_ib^iK^i
\right.
\tag{0.34}
```

物理中常用如下记号：

```math
\left.
e^{-\frac i2\omega^{\mu\nu}J^{\mu\nu}}
\right.
\tag{0.35}
```

其中 $`\omega_{\mu\nu}`$ 关于其指标反对称，且

```math
\left.
-iJ^{ij}=\epsilon_{ijk}J^k,\qquad -iJ^{0i}=K^i.
\right.
\tag{0.36}
```

每个 $`J^{\mu\nu}`$ 只是一个 $`4\times4`$ 矩阵，$`\alpha,\beta`$ 标记其行与列。其矩阵元为

```math
\left.
(J^{\mu\nu})_{\alpha\beta}=i\left(\eta^{\mu\alpha}\delta^{\nu\beta}-\eta^{\nu\alpha}\delta^{\mu\beta}\right).
\right.
\tag{0.37}
```

具体地（行指标为 $`\alpha`$，列指标为 $`\beta`$；其余分量由 $`J^{\nu\mu}=-J^{\mu\nu}`$ 给出），转动生成元 $`J^{ij}=i\epsilon_{ijk}J^k`$ 是厄米的：

```math
\left.
J^{23}=\begin{pmatrix}0&0&0&0\\0&0&0&0\\0&0&0&-i\\0&0&i&0\end{pmatrix},\quad
J^{31}=\begin{pmatrix}0&0&0&0\\0&0&0&i\\0&0&0&0\\0&-i&0&0\end{pmatrix},\quad
J^{12}=\begin{pmatrix}0&0&0&0\\0&0&-i&0\\0&i&0&0\\0&0&0&0\end{pmatrix},
\right.
\tag{0.38}
```

而 boost 生成元 $`J^{0i}=iK^i`$ 是反厄米的：

```math
\left.
J^{01}=\begin{pmatrix}0&i&0&0\\i&0&0&0\\0&0&0&0\\0&0&0&0\end{pmatrix},\quad
J^{02}=\begin{pmatrix}0&0&i&0\\0&0&0&0\\i&0&0&0\\0&0&0&0\end{pmatrix},\quad
J^{03}=\begin{pmatrix}0&0&0&i\\0&0&0&0\\0&0&0&0\\i&0&0&0\end{pmatrix}.
\right.
\tag{0.39}
```


<br><br>

<a id="greens-functions"></a>
### 0.4 格林函数

**定义与积分解**

在下面的一般构造中，$`x,y`$ 表示 $`d`$ 个独立变量。设 $`\mathcal K_x`$ 是 $`\Omega\subseteq\mathbb R^d`$ 上的线性微分算子，$`\mathcal B`$ 规定线性的边界数据或初始数据：

```math
\left.
\mathcal K_xu(x)=f(x),\qquad \mathcal Bu=b.
\right.
\tag{0.40}
```

假设数据足够正则，且下文的积分都存在。含 $`\delta`$ 函数的方程按分布意义理解。

- **格林函数**：满足该微分方程以及齐次边界条件或齐次初始条件的核，

```math
\left.
\boxed{\mathcal K_xG(x,y)=\delta^{(d)}(x-y),\qquad \mathcal B_xG(x,y)=0.}
\right.
\tag{0.41}
```

下标 $`x`$ 指明算子作用于哪个变量。边界条件或初始条件的选取是 $`G`$ 的定义的一部分。

- **积分解**：若 $`u_{\mathrm h}`$ 是满足给定数据的齐次方程的解，则

```math
\left.
\begin{aligned}
\boxed{u(x)=u_{\mathrm h}(x)+\int_\Omega d^dy\,G(x,y)f(y),}\\
\mathcal K_xu_{\mathrm h}(x)=0,\qquad \mathcal Bu_{\mathrm h}=b.
\end{aligned}
\right.
\tag{0.42}
```

事实上，

```math
\left.
\begin{aligned}
\mathcal K_xu(x)
&=\int_\Omega d^dy\,[\mathcal K_xG(x,y)]f(y)
=\int_\Omega d^dy\,\delta^{(d)}(x-y)f(y)=f(x),\\
\mathcal Bu&=\mathcal Bu_{\mathrm h}
+\int_\Omega d^dy\,[\mathcal B_xG(x,y)]f(y)=b.
\end{aligned}
\right.
\tag{0.43}
```

若 $`\mathcal Ku=0`$、$`\mathcal Bu=0`$ 在所选函数空间中只有零解，则解唯一。存在非平凡零模时，唯一性不成立，且可解性可能要求相容性条件；不能假定对任意源都存在逆。若不给定边界条件或初始条件，满足 (0.41) 第一式的两个核可以相差一个关于 $`x`$ 的齐次方程的解。

**用 Fourier 变换构造**

对 Minkowski 时空上的常系数算子，回到 $`x^\mu=(t,\mathbf x)`$ 和 Fourier 约定 (0.1)。若所选条件还具有平移不变性，则 $`G(x,y)=G(x-y)`$，且

```math
\left.
\begin{aligned}
\mathcal K(-ip)\widetilde G(p)&=1,\\
G(x-y)&=\int\frac{d^4p}{(2\pi)^4}\,
e^{-ip\cdot(x-y)}\widetilde G(p),\\
\widetilde G(p)&=\left[\frac{1}{\mathcal K(-ip)}\right]_{\mathrm{prescription}}.
\end{aligned}
\right.
\tag{0.44}
```

其中 $`\mathcal K(-ip)`$ 由把每个 $`\partial_\mu`$ 换成 $`-ip_\mu`$ 得到。在 $`\mathcal K(-ip)`$ 的零点处，求倒数需要一个由所选条件确定的分布意义下的处方；仅凭代数方程并不能选定它。

**Poisson 方程与边界数据**

先考虑 $`\mathbb R^3`$ 中光滑且紧支的源：

```math
\left.
-\nabla^2u(\mathbf x)=f(\mathbf x),\qquad
u(\mathbf x)\to0\quad\text{当 }|\mathbf x|\to\infty\text{ 时}.
\right.
\tag{0.45}
```

对 $`r:=|\mathbf x-\mathbf y|>0`$，在无穷远处为零的转动不变核满足

```math
\left.
\nabla^2G_0(r)=\frac{1}{r^2}\frac{d}{dr}\left(r^2\frac{dG_0}{dr}\right)=0
\quad\Longrightarrow\quad G_0(r)=\frac{A}{r}.
\right.
\tag{0.46}
```

在以源点为中心的球 $`B_\epsilon`$ 上积分 $`-\nabla^2G_0=\delta^{(3)}`$，可定出 $`A`$：

```math
\left.
\begin{aligned}
1&=-\int_{B_\epsilon}d^3x\,\nabla^2G_0
=-4\pi\epsilon^2\left.\frac{dG_0}{dr}\right|_{r=\epsilon}
=4\pi A,\\
G_0(\mathbf x,\mathbf y)&=\frac{1}{4\pi|\mathbf x-\mathbf y|}.
\end{aligned}
\right.
\tag{0.47}
```

因此

```math
\left.
\boxed{u(\mathbf x)=\int_{\mathbb R^3}d^3y\,
\frac{f(\mathbf y)}{4\pi|\mathbf x-\mathbf y|}.}
\right.
\tag{0.48}
```

现在设 $`\Omega\subset\mathbb R^3`$ 有界且边界光滑，并在 $`\partial\Omega`$ 上给定 $`u=b`$。$`-\nabla^2`$ 的 Dirichlet 格林函数关于其两个宗量对称，且满足

```math
\left.
\begin{aligned}
-\nabla_{\mathbf y}^2G_D(\mathbf x,\mathbf y)
&=\delta^{(3)}(\mathbf y-\mathbf x),\qquad \mathbf y\in\Omega,\\
G_D(\mathbf x,\mathbf y)&=0,\qquad \mathbf y\in\partial\Omega.
\end{aligned}
\right.
\tag{0.49}
```

设 $`\mathbf n_y`$ 为外法向单位矢量，$`\partial_{n_y}:=\mathbf n_y\cdot\nabla_{\mathbf y}`$。格林第二恒等式为

```math
\left.
\int_\Omega d^3y\,(v\nabla^2w-w\nabla^2v)
=\int_{\partial\Omega}dS_y\,(v\partial_{n_y}w-w\partial_{n_y}v).
\right.
\tag{0.50}
```

在 $`\Omega\setminus B_\epsilon(\mathbf x)`$ 上对 $`v=u`$，$`w=G_D(\mathbf x,\cdot)`$ 应用 (0.50)，再令 $`\epsilon\to0^+`$。对 $`\mathbf x\in\Omega`$，

```math
\left.
\boxed{\begin{aligned}
u(\mathbf x)&=\int_\Omega d^3y\,G_D(\mathbf x,\mathbf y)f(\mathbf y)\\
&\quad-\int_{\partial\Omega}dS_y\,b(\mathbf y)\partial_{n_y}G_D(\mathbf x,\mathbf y).
\end{aligned}}
\right.
\tag{0.51}
```

第二项给出非零边界数据的贡献。(0.47) 中的自由空间核 $`G_0`$ 一般不满足 (0.49) 中的边界条件。

**Klein–Gordon 方程与初始数据**

取 $`m\geq0`$ 及 mostly-minus 度规，考虑

```math
\left.
(\Box+m^2)u(x)=f(x),\qquad
\Box:=\partial_\mu\partial^\mu=\partial_t^2-\nabla^2.
\right.
\tag{0.52}
```

- **推迟格林函数**：只在非负时间差上有支集的平移不变核，

```math
\left.
(\Box+m^2)G_{\mathrm{ret}}(t,\mathbf x)
=\delta(t)\delta^{(3)}(\mathbf x),\qquad
G_{\mathrm{ret}}(t,\mathbf x)=0\quad(t<0).
\right.
\tag{0.53}
```

这里已把源点平移到原点。由于 $`\mathcal K(-ip)=m^2-p^2`$，推迟处方为

```math
\left.
\widetilde G_{\mathrm{ret}}(p)
=-\lim_{\epsilon\to0^+}\frac{1}{(p^0+i\epsilon)^2-E_{\mathbf p}^2},\qquad
E_{\mathbf p}:=\sqrt{\mathbf p^2+m^2}.
\right.
\tag{0.54}
```

两个极点都位于实 $`p^0`$ 轴下方。$`t>0`$ 时在下半平面闭合围道，$`t<0`$ 时在上半平面闭合围道，得

```math
\left.
\boxed{G_{\mathrm{ret}}(t,\mathbf x)
=\theta(t)\int\frac{d^3p}{(2\pi)^3}\,
e^{i\mathbf p\cdot\mathbf x}\frac{\sin(E_{\mathbf p}t)}{E_{\mathbf p}}.}
\right.
\tag{0.55}
```

其中 $`\theta(t)`$ 为 Heaviside 函数，$`E_{\mathbf p}=0`$ 处的值按连续性理解。等时极限为

```math
\left.
G_{\mathrm{ret}}(0^+,\mathbf x)=0,\qquad
\partial_tG_{\mathrm{ret}}(0^+,\mathbf x)=\delta^{(3)}(\mathbf x).
\right.
\tag{0.56}
```

对给定的初始数据 $`u(t_0,\mathbf x)=u_0(\mathbf x)`$ 和 $`\partial_tu(t_0,\mathbf x)=u_1(\mathbf x)`$，由 (0.56) 得，当 $`t>t_0`$ 时，

```math
\left.
\boxed{\begin{aligned}
u(t,\mathbf x)
&=\int d^3y\,\bigl[
\partial_tG_{\mathrm{ret}}(t-t_0,\mathbf x-\mathbf y)u_0(\mathbf y)\\
&\hspace{4.5em}+G_{\mathrm{ret}}(t-t_0,\mathbf x-\mathbf y)u_1(\mathbf y)\bigr]\\
&\quad+\int_{t_0}^{t}dt'\int d^3y\,
G_{\mathrm{ret}}(t-t',\mathbf x-\mathbf y)f(t',\mathbf y).
\end{aligned}}
\right.
\tag{0.57}
```

当 $`m=0`$ 时，(0.55) 中的空间积分给出波动方程的核。记 $`r:=|\mathbf x|`$，

```math
\left.
\begin{aligned}
G_{\mathrm{ret}}(t,\mathbf x)\big|_{m=0}
&=\frac{\theta(t)}{2\pi^2r}\int_0^\infty dp\,\sin(pr)\sin(pt)\\
&=\boxed{\frac{\delta(t-r)}{4\pi r}}.
\end{aligned}
\right.
\tag{0.58}
```

若初始数据为零，把 $`f(t',\mathbf y)`$ 在 $`t'<t_0`$ 处延拓为零。于是 (0.57) 化为

```math
\left.
\boxed{u(t,\mathbf x)=\int d^3y\,
\frac{f(t-|\mathbf x-\mathbf y|,\mathbf y)}{4\pi|\mathbf x-\mathbf y|}.}
\right.
\tag{0.59}
```

为与 (4.12) 中定义的标量费曼传播子比较，在同样的归一化 $`\mathcal KG_F=\delta^{(4)}`$ 下，费曼处方给出

```math
\left.
\begin{aligned}
G_F(x-y)&=-\lim_{\varepsilon\to0^+}\int\frac{d^4p}{(2\pi)^4}\,
\frac{e^{-ip\cdot(x-y)}}{p^2-m^2+i\varepsilon}
=i\Delta_F(x-y),\\
(\Box_x+m^2)\Delta_F(x-y)&=-i\delta^{(4)}(x-y).
\end{aligned}
\right.
\tag{0.60}
```


---

<a id="qft-ch1"></a>
## 1. 经典场论

<a id="lagrangian-formalism"></a>
### 1.1 拉格朗日形式

<a id="mechanics-lagrangian"></a>
#### 拉氏量

**定义**

考虑具有 $`n`$ 个自由度的系统。

- **位形空间**：开集 $`\mathrm{Conf}\subset\mathbb R^n`$。
  - 位形是一点 $`q=(q_1,\ldots,q_n)\in\mathrm{Conf}`$。
  - $`q_a`$ 称为广义坐标。
- **路径**：光滑曲线，对任意 $`t_0<t_f`$，

```math
\left.
\begin{aligned}
C:[t_0,t_f]&\to\mathrm{Conf},\\
t&\mapsto C(t),
\end{aligned}
\right.
\tag{1.1}
```

速度为 $`\dot C(t):=dC/dt`$。

- **动力学结构**：拉氏量，即光滑函数

```math
\left.
\begin{aligned}
L:\mathbb R^n\times\mathbb R^n\times\mathbb R&\to\mathbb R,\\
(x,y,t)&\mapsto L(x,y,t).
\end{aligned}
\right.
\tag{1.2}
```

- **作用量**：路径上的泛函

```math
\left.
\boxed{
\begin{aligned}
S:\{\text{路径}\}&\to\mathbb R,\\
C&\mapsto S[C]:=\int_{t_0}^{t_f}dt\,L\bigl(C(t),\dot C(t),t\bigr).
\end{aligned}}
\right.
\tag{1.3}
```

- **解**：在端点固定的变分下使 $`S`$ 取驻值的路径 $`\bar C`$，

```math
\left.
\frac{d}{ds}S[\bar C+s\eta]\Big|_{s=0}=0,
\right.
\tag{1.4}
```

对任意满足 $`\eta(t_0)=\eta(t_f)=0`$ 的光滑 $`\eta:[t_0,t_f]\to\mathbb R^n`$ 成立。

**Euler–Lagrange 方程**

将 $`L`$ 在 $`\bigl(C(t),\dot C(t),t\bigr)`$ 处取值的偏导数记为 $`\frac{\partial L}{\partial x_a}\big|_C`$ 和 $`\frac{\partial L}{\partial y_a}\big|_C`$。

与通常使用的 $`q_a,\dot q_a`$ 记号的对应关系为

```math
\left.
\begin{aligned}
\frac{\partial L}{\partial \dot q_a}&=\frac{\partial L}{\partial y_a}\Big|_C,\\
\frac{\partial L}{\partial q_a}&=\frac{\partial L}{\partial x_a}\Big|_C.
\end{aligned}
\right.
\tag{1.5}
```

则

```math
\left.
\begin{aligned}
\frac{d}{ds}S[C+s\eta]\Big|_{s=0}
&=\int_{t_0}^{t_f}dt\sum_{a=1}^n\Bigl(\frac{\partial L}{\partial x_a}\Big|_C\,\eta_a+\frac{\partial L}{\partial y_a}\Big|_C\,\dot\eta_a\Bigr)\\
&=\int_{t_0}^{t_f}dt\sum_{a=1}^n\biggl[\frac{\partial L}{\partial x_a}\Big|_C-\frac{d}{dt}\Bigl(\frac{\partial L}{\partial y_a}\Big|_C\Bigr)\biggr]\eta_a\\
&\quad+\biggl[\sum_{a=1}^n\frac{\partial L}{\partial y_a}\Big|_C\,\eta_a\biggr]_{t_0}^{t_f}.
\end{aligned}
\right.
\tag{1.6}
```

由于 $`\eta(t_0)=\eta(t_f)=0`$，边界项为零。

由于 $`\eta`$ 任意，解为满足下式的路径 $`\bar C`$：

```math
\left.
\boxed{\frac{d}{dt}\Bigl(\frac{\partial L}{\partial y_a}\Big|_{\bar C}\Bigr)-\frac{\partial L}{\partial x_a}\Big|_{\bar C}=0,\qquad a=1,\ldots,n.}
\right.
\tag{1.7}
```

<br><br>

<a id="lagrangian-symmetry"></a>
#### 对称变换与 Noether 定理

**变换**

- **内部变换**：
微分同胚的单参数族 $`\phi_\lambda:\mathrm{Conf}\to\mathrm{Conf}`$，$`\lambda\in\mathbb R`$，其中 $`(\lambda,q)\mapsto\phi_\lambda(q)`$ 光滑且 $`\phi_0=\mathrm{id}`$，它逐点作用于路径，

```math
\left.
\begin{aligned}
\Phi:\mathbb R\times\{\text{路径}\}&\to\{\text{路径}\},\\
(\lambda,C)&\mapsto\Phi_\lambda C:=\phi_\lambda\circ C,
\end{aligned}
\right.
\tag{1.8}
```

切矢或者说速度之间的关系为

```math
\left.
\frac{d}{dt}(\Phi_\lambda C)_a(t)=\sum_{b=1}^n\frac{\partial(\phi_\lambda)_a}{\partial q_b}\bigl(C(t)\bigr)\,\dot C_b(t),
\right.
\tag{1.9}
```

其中 $`(\phi_\lambda)_a(q)`$ 是 $`\phi_\lambda(q)`$ 的第 $`a`$ 个坐标。

把矩阵元为 $`\frac{\partial(\phi_\lambda)_a}{\partial q_b}(q)`$ 的 Jacobi 矩阵记为 $`\frac{\partial\phi_\lambda}{\partial q}(q)`$，于是 $`\Phi_\lambda C`$ 的速度为
```math
\frac{d}{dt}(\Phi_\lambda C)(t)=\frac{\partial\phi_\lambda}{\partial q}\bigl(C(t)\bigr)\,\dot C(t)
```

- **时间平移**：路径在时间上的平移，

```math
\left.
\begin{aligned}
\Theta:\mathbb R\times\{\text{路径}\}&\to\{\text{路径}\},\\
(\tau,C)&\mapsto\Theta_\tau C:=C(\cdot-\tau),
\end{aligned}
\right.
\tag{1.10}
```

于是 $`\Theta_\tau C:[t_0+\tau,t_f+\tau]\to\mathrm{Conf}`$，$`t\mapsto C(t-\tau)`$，其速度为

```math
\left.
\frac{d}{dt}(\Theta_\tau C)(t)=\dot C(t-\tau).
\right.
\tag{1.11}
```

**对称变换**

- **对称变换**：使每条路径的作用量都不变的内部变换 $`\Phi`$ 或时间平移 $`\Theta`$，即分别满足：

```math
\left.
\boxed{
\begin{aligned}
S[\Phi_\lambda C]&=S[C]\quad\text{对任意路径 }C\text{ 及任意 }\lambda\in\mathbb R,\\
S[\Theta_\tau C]&=S[C]\quad\text{对任意路径 }C\text{ 及任意 }\tau\in\mathbb R.
\end{aligned}}
\right.
\tag{1.12}
```


把变换后的路径代入作用量，并在第二种情形中作平移 $`t\to t+\tau`$，

```math
\left.
\begin{aligned}
S[\Phi_\lambda C]&=\int_{t_0}^{t_f}dt\,L\Bigl(\phi_\lambda\bigl(C(t)\bigr),\ \frac{\partial\phi_\lambda}{\partial q}\bigl(C(t)\bigr)\,\dot C(t),\ t\Bigr),\\
S[\Theta_\tau C]&=\int_{t_0+\tau}^{t_f+\tau}dt\,L\bigl(C(t-\tau),\dot C(t-\tau),t\bigr)=\int_{t_0}^{t_f}dt\,L\bigl(C(t),\dot C(t),t+\tau\bigr).
\end{aligned}
\right.
\tag{1.13}
```

因此，对称变换的等价定义如下：

$`\Phi`$ 或 $`\Theta`$ 是对称变换，当且仅当对所有 $`(x,y,t)\in\mathrm{Conf}\times\mathbb R^n\times\mathbb R`$ 以及所有 $`\lambda`$ 或所有 $`\tau`$，分别有：

```math
\left.
\boxed{
\begin{aligned}
L\Bigl(\phi_\lambda(x),\ \frac{\partial\phi_\lambda}{\partial q}(x)\,y,\ t\Bigr)&=L(x,y,t)
\end{aligned}}
\right.
\tag{1.14}
```

```math
\left.
\boxed{
L(x,y,t+\tau)=L(x,y,t)\quad(\forall\,\tau\in\mathbb R)
\quad\Longleftrightarrow\quad
\frac{\partial L}{\partial t}(x,y,t)=0.
}
\right.
\tag{1.15}
```


**守恒量**

- **守恒量**：光滑函数

```math
\left.
\begin{aligned}
\mathcal Q:\mathrm{Conf}\times\mathbb R^n\times\mathbb R&\to\mathbb R,\\
(x,y,t)&\mapsto\mathcal Q(x,y,t),
\end{aligned}
\right.
\tag{1.16}
```

使得对每个解 $`\bar C`$，$`\mathcal Q\bigl(\bar C(t),\dot{\bar C}(t),t\bigr)`$ 都与 $`t`$ 无关。

**Noether 定理**

**(A) 时间平移**

若 $`\Theta`$ 是对称变换，即在 $`\mathrm{Conf}\times\mathbb R^n\times\mathbb R`$ 上 $`\partial L/\partial t=0`$，则能量

```math
\left.
\boxed{E(x,y,t):=\sum_{a=1}^n\frac{\partial L}{\partial y_a}(x,y,t)\,y_a-L(x,y,t)}
\right.
\tag{1.17}
```

是守恒量。

**(B) 内部变换**

若 $`\Phi`$ 是对称变换，则对于生成元

```math
\left.
\begin{aligned}
X:\mathrm{Conf}&\to\mathbb R^n,\\
q&\mapsto\frac{\partial\phi_\lambda(q)}{\partial\lambda}\Big|_{\lambda=0},
\end{aligned}
\right.
\tag{1.18}
```

生成元给出 $`\lambda=0`$ 处无穷小变换的形式：$`\phi_\lambda(q)=q+\lambda\,X(q)+O(\lambda^2),`$ 即坐标按 $`q_a\mapsto q_a+\lambda X_a(q)`$ 变换。

相应地，速度的变换为 $`y\mapsto y+\lambda\,\frac{\partial X}{\partial q}(q)\,y+O(\lambda^2),`$ 即 $`y_a\mapsto y_a+\lambda\sum_b\frac{\partial X_a}{\partial q_b}(q)\,y_b`$。

函数

```math
\left.
\boxed{\mathcal Q(x,y,t):=\sum_{a=1}^n\frac{\partial L}{\partial y_a}(x,y,t)\,X_a(x)}
\right.
\tag{1.19}
```

是守恒量。

**证明**

(A) 设 $`\bar C`$ 是解。记 $`L|_{\bar C}:=L\bigl(\bar C(t),\dot{\bar C}(t),t\bigr)`$。

 由链式法则和 Euler–Lagrange 方程，

```math
\left.
\frac{d}{dt}E\bigl(\bar C(t),\dot{\bar C}(t),t\bigr)
=\frac{d}{dt}\Bigl(\sum_{a=1}^n\frac{\partial L}{\partial y_a}\Big|_{\bar C}\,\dot{\bar C}_a(t)-L\big|_{\bar C}\Bigr)
=-\frac{\partial L}{\partial t}\Big|_{\bar C}
\right.
\tag{1.20}
```

这对每个解都成立；若 $`\partial L/\partial t=0`$，则此式为零。

(B) 将第一个对称性条件在 $`\lambda=0`$ 处对 $`\lambda`$ 求导，得到：对所有 $`(x,y,t)\in\mathrm{Conf}\times\mathbb R^n\times\mathbb R`$，

```math
\left.
\sum_{a=1}^n\Bigl(\frac{\partial L}{\partial x_a}\,X_a(x)
+\frac{\partial L}{\partial y_a}\sum_{b=1}^n\frac{\partial X_a}{\partial q_b}(x)\,y_b\Bigr)=0,
\right.
\tag{1.21}
```

其中 $`L`$ 的偏导数在 $`(x,y,t)`$ 处取值。

对解 $`\bar C`$，由链式法则和 Euler–Lagrange 方程得

```math
\left.
\frac{d}{dt}\mathcal Q\bigl(\bar C(t),\dot{\bar C}(t),t\bigr)
=\sum_{a=1}^n\Bigl(\frac{\partial L}{\partial x_a}\Big|_{\bar C}\,X_a\bigl(\bar C(t)\bigr)
+\frac{\partial L}{\partial y_a}\Big|_{\bar C}\sum_{b=1}^n\frac{\partial X_a}{\partial q_b}\bigl(\bar C(t)\bigr)\,\dot{\bar C}_b(t)\Bigr),
\right.
\tag{1.22}
```

这正是上述恒等式在 $`\bigl(\bar C(t),\dot{\bar C}(t),t\bigr)`$ 处的取值，因此为零。$`\square`$


**动量**

固定 $`b\in\{1,\ldots,n\}`$，平移第 $`b`$ 个坐标，

```math
\left.
\bigl(\phi_\lambda(q)\bigr)_a=q_a+\lambda\,\delta_{ab}.
\right.
\tag{1.23}
```

Jacobi 矩阵 $`\partial\phi_\lambda/\partial q`$ 为单位矩阵，故速度不变，对称性条件化为：对所有 $`\lambda`$，$`L(\phi_\lambda(x),y,t)=L(x,y,t)`$，即 $`\partial L/\partial x_b=0`$。

生成元：$`X_a(q)=\delta_{ab}`$。

守恒量：

```math
\left.
\mathcal Q(x,y,t)=\sum_{a=1}^n\frac{\partial L}{\partial y_a}(x,y,t)\,\delta_{ab}=\frac{\partial L}{\partial y_b}(x,y,t),
\right.
\tag{1.24}
```

即与 $`q_b`$ 共轭的动量 $`p_b`$。



<br><br>

<a id="hamiltonian-formalism"></a>
### 1.2 哈密顿形式


<a id="dynamical-systems"></a>
#### 动力系统

**定义**

- **状态空间**：开集 $`M\subset\mathbb R^N`$。
  - 状态是一点 $`z=(z_1,\ldots,z_N)\in M`$。
  - $`z_A`$ 称为状态变量。
- **状态转移函数**：光滑函数

```math
\left.
\begin{aligned}
F:M&\to\mathbb R^N,\\
z&\mapsto F(z).
\end{aligned}
\right.
\tag{1.25}
```

- **解**：光滑曲线 $`C:I\to M`$，其中 $`I\subset\mathbb R`$ 是开区间，满足

```math
\left.
\boxed{\dot C_A(t)=F_A\bigl(C(t)\bigr),\qquad A=1,\ldots,N.}
\right.
\tag{1.26}
```

**(1) 确定性**

由于 $`F`$ 光滑，对每个 $`t_0\in\mathbb R`$ 和 $`z^{(0)}\in M`$，存在唯一的满足 $`C(t_0)=z^{(0)}`$ 的极大解 $`C`$。因此，某一时刻的状态决定了该解在其区间上所有更晚和更早时刻的状态，且 $`M`$ 的每一点恰有一条解曲线经过。

假设每个极大解都定义在整个 $`\mathbb R`$ 上。$`F`$ 的流为

```math
\left.
\begin{aligned}
\Phi_t:M&\to M,\\
z^{(0)}&\mapsto C(t),
\end{aligned}
\right.
\tag{1.27}
```

其中 $`C`$ 是满足 $`C(0)=z^{(0)}`$ 的解。它满足

- $`\partial_t\Phi_t(z)=F\bigl(\Phi_t(z)\bigr)`$ 且 $`\Phi_0=\mathrm{id}`$；
- $`\Phi_t\circ\Phi_s=\Phi_{t+s}`$（因为 $`F`$ 不依赖于 $`t`$），故每个 $`\Phi_t`$ 都是微分同胚，其逆为 $`\Phi_{-t}`$。

**(2) 状态空间中的体积**

对区域 $`D\subset M`$，记 $`\mathrm{vol}(D):=\int_Dd^Nz`$，并把 $`\Phi_t`$ 的 Jacobi 矩阵记为 $`J_t:=\frac{\partial\Phi_t}{\partial z}`$。把 $`\partial_t\Phi_t=F\circ\Phi_t`$ 对 $`z`$ 求导，并利用 Jacobi 公式 $`d\det J=\det J\,\mathop{\rm tr}\nolimits (J^{-1}dJ)`$，得：

```math
\left.
\begin{aligned}
\partial_tJ_t&=\Bigl(\frac{\partial F}{\partial z}\circ\Phi_t\Bigr)J_t,
\qquad
\partial_t\det J_t=\Bigl(\sum_{A=1}^N\frac{\partial F_A}{\partial z_A}\circ\Phi_t\Bigr)\det J_t,\\
\frac{d}{dt}\mathrm{vol}\bigl(\Phi_t(D)\bigr)
&=\frac{d}{dt}\int_Dd^Nz\,\det J_t
=\int_{\Phi_t(D)}d^Nz\,\sum_{A=1}^N\frac{\partial F_A}{\partial z_A}.
\end{aligned}
\right.
\tag{1.28}
```

因此，$`\mathrm{vol}(\Phi_t(D))`$ 对每个 $`D`$ 都是常数，当且仅当 $`\sum_A\partial F_A/\partial z_A=0`$。

<br><br>

<a id="hamiltonian-mechanics"></a>
#### 哈密顿形式

**定义**

考虑具有 $`n`$ 个自由度的系统。

- **相空间**：开集 $`M\subset\mathbb R^{2n}`$。
  - 状态是一点 $`z=(q_1,\ldots,q_n,p_1,\ldots,p_n)\in M`$。
  - $`q_a`$ 称为广义坐标，$`p_a`$ 称为动量。
- **可观测量**：光滑函数

```math
\left.
\begin{aligned}
f:M&\to\mathbb R,\\
z&\mapsto f(z).
\end{aligned}
\right.
\tag{1.29}
```

- **动力学结构**：
  - (1.87) 中的 Poisson 括号 $`\{\ ,\ \}_{\mathrm{PB}}`$；
  - 哈密顿量，即光滑函数

```math
\left.
\begin{aligned}
H:M&\to\mathbb R,\\
z&\mapsto H(z),
\end{aligned}
\right.
\tag{1.30}
```

且不显含时间。

- **解**：光滑曲线 $`C:I\to M`$，其中 $`I\subset\mathbb R`$ 是开区间，满足

```math
\left.
\frac{d}{dt}q_a\bigl(C(t)\bigr)=\frac{\partial H}{\partial p_a}\bigl(C(t)\bigr),\quad
\frac{d}{dt}p_a\bigl(C(t)\bigr)=-\frac{\partial H}{\partial q_a}\bigl(C(t)\bigr)
\qquad\Longleftrightarrow\qquad
\frac{d}{dt}f\bigl(C(t)\bigr)=\{f,H\}_{\mathrm{PB}}\bigl(C(t)\bigr)\quad\text{对所有 }f.
\right.
\tag{1.31}
```

<br><br>

<a id="hamiltonian-symmetry"></a>
#### 对称性与 Noether 定理

**变换**

- **变换**：不显含时间的微分同胚，

```math
\left.
\begin{aligned}
\phi:M&\to M,\\
z&\mapsto\phi(z),
\end{aligned}
\qquad
Q_a:=q_a\circ\phi,\quad P_a:=p_a\circ\phi,\quad \phi_*f:=f\circ\phi^{-1},
\right.
\tag{1.32}
```

其中 $`Q_a(z),P_a(z)`$ 是 $`\phi(z)`$ 的坐标，$`\phi_*`$ 是 (1.64) 中的推前，满足 $`(\phi_*f)(\phi(z))=f(z)`$。

**对称变换**

- **对称变换**：同时保持 Poisson 括号和哈密顿量不变的变换 $`\phi`$，

```math
\left.
\boxed{
\begin{aligned}
&\text{(i)}\quad\{f\circ\phi,\,g\circ\phi\}_{\mathrm{PB}}=\{f,g\}_{\mathrm{PB}}\circ\phi\quad\text{对所有 }f,g,\\
&\text{(ii)}\quad H\circ\phi=H.
\end{aligned}}
\right.
\tag{1.33}
```

满足 (i) 的变换称为正则变换。把 $`f,g`$ 换成 $`f\circ\phi^{-1},g\circ\phi^{-1}`$ 可知，(i) 等价于 $`\{\phi_*f,\phi_*g\}_{\mathrm{PB}}=\phi_*\{f,g\}_{\mathrm{PB}}`$；(ii) 等价于 $`\phi_*H=H`$，即对所有 $`z\in M`$ 有 $`H(\phi(z))=H(z)`$。

把全部相空间坐标记为 $`z_A`$，$`A=1,\ldots,2n`$，并记 $`Z_A:=z_A\circ\phi`$。由链式法则，

```math
\left.
\begin{aligned}
\{f\circ\phi,\,g\circ\phi\}_{\mathrm{PB}}
&=\sum_{A,B}\Bigl(\frac{\partial f}{\partial z_A}\circ\phi\Bigr)\Bigl(\frac{\partial g}{\partial z_B}\circ\phi\Bigr)\{Z_A,Z_B\}_{\mathrm{PB}},\\
\{f,g\}_{\mathrm{PB}}\circ\phi
&=\sum_{A,B}\Bigl(\frac{\partial f}{\partial z_A}\circ\phi\Bigr)\Bigl(\frac{\partial g}{\partial z_B}\circ\phi\Bigr)\{z_A,z_B\}_{\mathrm{PB}}.
\end{aligned}
\right.
\tag{1.34}
```

括号 $`\{z_A,z_B\}_{\mathrm{PB}}`$ 都是常数，而取 $`f=z_A`$，$`g=z_B`$ 只挑出一项，故 (i) 成立当且仅当 $`\{Z_A,Z_B\}_{\mathrm{PB}}=\{z_A,z_B\}_{\mathrm{PB}}`$。由 (1.87)，(i) 等价于

```math
\left.
\boxed{
\{Q_a,Q_b\}_{\mathrm{PB}}=\{P_a,P_b\}_{\mathrm{PB}}=0,\qquad
\{Q_a,P_b\}_{\mathrm{PB}}=\delta_{ab}.}
\right.
\tag{1.35}
```

对称变换把解映为解。设 $`C`$ 是解，$`C':=\phi\circ C`$。先对 $`f\circ\phi`$ 应用 (1.31)，再利用 (ii) 和 (i)，

```math
\left.
\begin{aligned}
\frac{d}{dt}f\bigl(C'(t)\bigr)
&=\{f\circ\phi,\,H\}_{\mathrm{PB}}\bigl(C(t)\bigr)\\
&=\{f\circ\phi,\,H\circ\phi\}_{\mathrm{PB}}\bigl(C(t)\bigr)
=\{f,H\}_{\mathrm{PB}}\bigl(C'(t)\bigr)
\end{aligned}
\right.
\tag{1.36}
```

对每个 $`f`$ 成立，故由 (1.31)，$`C'`$ 是解。

**守恒量**

- **守恒量**：可观测量 $`f`$，使得对每个解 $`C`$，$`f\bigl(C(t)\bigr)`$ 都与 $`t`$ 无关。

(1.31) 即 (1.26) 取 $`N=2n`$、$`F_A=\{z_A,H\}_{\mathrm{PB}}`$ 的情形。由于 $`M`$ 的每一点都有解经过，由 (1.31) 可知，$`f`$ 是守恒量当且仅当

```math
\left.
\boxed{\{f,H\}_{\mathrm{PB}}=0.}
\right.
\tag{1.37}
```

**Noether 定理**

设 $`\phi_\lambda`$，$`\lambda\in\mathbb R`$，为对称变换的单参数子群：

- 对所有 $`\lambda,\mu\in\mathbb R`$，$`\phi_\lambda\circ\phi_\mu=\phi_{\lambda+\mu}`$；特别地，$`\phi_0=\mathrm{id}`$；
- $`(\lambda,z)\mapsto\phi_\lambda(z)`$ 光滑。

定义生成元

```math
\left.
\begin{aligned}
X:M&\to\mathbb R^{2n},\\
z&\mapsto\frac{\partial\phi_\lambda(z)}{\partial\lambda}\Big|_{\lambda=0},
\end{aligned}
\right.
\tag{1.38}
```

于是 $`\phi_\lambda`$ 是 $`X`$ 的流。若 $`M`$ 单连通，则存在光滑函数 $`G:M\to\mathbb R`$（在相差一个可加常数的意义下唯一），满足

```math
\left.
X_A=\{z_A,G\}_{\mathrm{PB}},\qquad A=1,\ldots,2n,
\right.
\tag{1.39}
```

并且

```math
\left.
\boxed{\{G,H\}_{\mathrm{PB}}=0,}
\right.
\tag{1.40}
```

故 $`G`$ 是守恒量。

**证明**

记 $`\omega_{AB}:=\{z_A,z_B\}_{\mathrm{PB}}`$。由 (1.87)，它是常数且可逆，并且 $`\{f,g\}_{\mathrm{PB}}=\sum_{A,B}\omega_{AB}\frac{\partial f}{\partial z_A}\frac{\partial g}{\partial z_B}`$。用 $`X_A=\sum_B\omega_{AB}Y_B`$ 定义 $`Y`$。在 (i) 中取 $`f=z_A`$，$`g=z_B`$，再将它与 (ii) 一起在 $`\lambda=0`$ 处对 $`\lambda`$ 求导：

```math
\left.
\begin{aligned}
0&=\{X_A,z_B\}_{\mathrm{PB}}+\{z_A,X_B\}_{\mathrm{PB}}
=\sum_{C,D}\omega_{AC}\,\omega_{BD}\Bigl(\frac{\partial Y_D}{\partial z_C}-\frac{\partial Y_C}{\partial z_D}\Bigr),\\
0&=\sum_A\frac{\partial H}{\partial z_A}\,X_A.
\end{aligned}
\right.
\tag{1.41}
```

由于 $`\omega`$ 可逆，$`\partial Y_D/\partial z_C=\partial Y_C/\partial z_D`$。在单连通的 $`M`$ 上，由此得 $`Y_B=\partial G/\partial z_B`$，其中 $`G`$ 光滑，且在相差一个常数的意义下唯一，即 (1.39)。于是 (1.41) 的第二行为 $`\sum_A\frac{\partial H}{\partial z_A}\{z_A,G\}_{\mathrm{PB}}=\{H,G\}_{\mathrm{PB}}=0`$，即 (1.40)。$`\square`$

**(1) 时间演化与能量**

在 (1.37) 中取 $`f=H`$，有 $`\{H,H\}_{\mathrm{PB}}=0`$，故 $`H`$ 是守恒量。取 $`G=H`$，由 (1.39) 得 $`X_A=\{z_A,H\}_{\mathrm{PB}}=F_A`$，故 $`H`$ 生成的子群就是 (1.27) 的时间演化 $`\Phi_t`$。

**(2) 平移与动量**

设 $`M=\mathbb R^{2n}`$，固定 $`k\in\mathbb R^n`$。取 $`\phi_\lambda(q,p)=(q+\lambda k,\,p)`$。则 $`Q_a=q_a+\lambda k_a`$ 与 $`P_a=p_a`$ 满足 (1.35)，且 $`\phi_\lambda`$ 是对称变换当且仅当对所有 $`\lambda`$ 有 $`H(q+\lambda k,p)=H(q,p)`$，即 $`\sum_ak_a\,\partial H/\partial q_a=0`$。此时 $`X=(k,0)`$，(1.39) 在取下式时成立：

```math
\left.
\boxed{G=\sum_{a=1}^nk_a\,p_a,}
\right.
\tag{1.42}
```

因此它是守恒的。

- 当 $`k`$ 为第 $`b`$ 个单位矢量时，条件为 $`\partial H/\partial q_b=0`$，且 $`p_b`$ 守恒。例如，对 $`H=\sum_ap_a^2/2m`$，每个 $`p_a`$ 都守恒。
- 对 $`N`$ 个粒子，$`q=(\mathbf x_1,\ldots,\mathbf x_N)`$，$`p=(\mathbf p_1,\ldots,\mathbf p_N)`$，取 $`k=(\mathbf e,\ldots,\mathbf e)`$。此时守恒量为 $`\sum_{A=1}^N\mathbf e\cdot\mathbf p_A`$，即总动量沿 $`\mathbf e`$ 的分量。

<br><br>

<a id="classical-field"></a>
### 1.3 经典场的定义

<a id="field-definition"></a>
#### 场的定义

**定义**

```math
\left.
\text{场}:\text{时空}\longrightarrow\text{向量空间},
\right.
\tag{1.43}
```

```math
\left.
\boxed{\Psi:\mathbb R^4\longrightarrow\mathbb R^n\ \text{或}\ \mathbb C^n
}
\right.
\tag{1.44}
```

还可以附加正则性条件，例如 $`C^\infty`$ 光滑性。

场的空间 $`\{\Psi\}`$ 承载 $`ISO(1,3)^+`$ 的一个表示。对 $`(\Lambda,a)\in ISO(1,3)^+`$，

```math
\left.
\Psi\xrightarrow{\;(\Lambda,a)\;}U(\Lambda,a)\Psi,
\right.
\tag{1.45}
```

其中 $`U`$ 是无穷维表示，可由有限维表示 $`D(\Lambda)`$ 构造：

```math
\left.
\boxed{
\begin{aligned}
[U(\Lambda,a)\Psi]_\alpha(x)
&:=D_{\alpha\beta}(\Lambda)
[(\Lambda,a)_*\Psi]_\beta(x)\\
&=D_{\alpha\beta}(\Lambda)
\Psi_\beta(\Lambda^{-1}x-\Lambda^{-1}a).
\end{aligned}
}
\right.
\tag{1.46}
```

<br><br>

<a id="lorentz-finite-representations"></a>
#### $`SO(1,3)^+`$ 的有限维表示

$`U`$ 由 $`D`$ 按 (1.46) 构造，而 $`D`$ 可通过 $`[U(\Lambda,0)\Psi](0)=D(\Lambda)\Psi(0)`$ 从 $`U`$ 还原。因此

```math
\left.
\begin{aligned}
\Psi_\alpha(x),\ \alpha=1,\ldots,n
&\quad\Longleftrightarrow\quad\text{无穷维表示 }U(\Lambda,a)\\
&\quad\Longleftrightarrow\quad SO(1,3)^+\text{ 的 }n\text{ 维表示 }D(\Lambda).
\end{aligned}
\right.
\tag{1.47}
```

**李代数表示**

对 $`X,Y\in\mathfrak o(1,3)`$，

```math
\left.
\rho(X):=\frac{d}{dt}D(e^{tX})\Big|_{t=0},\qquad
D(e^{X})=e^{\rho(X)},\qquad
\rho([X,Y])=[\rho(X),\rho(Y)].
\right.
\tag{1.48}
```

$`SO(1,3)^+`$ 连通，故 $`D`$ 由 $`\rho`$ 决定。把 $`\rho`$ 按 $`\rho(X+iY):=\rho(X)+i\rho(Y)`$ 复线性地延拓到复化李代数 $`\mathfrak o(1,3)_{\mathbb C}`$，后者由把 (0.32) 中的 $`M_4(\mathbb R)`$ 换成 $`M_4(\mathbb C)`$ 来定义。由 (0.36)，$`\mathfrak o(1,3)_{\mathbb C}`$ 包含所有 $`J^{\mu\nu}`$，且 $`D(e^{-\frac i2\omega_{\mu\nu}J^{\mu\nu}})=e^{-\frac i2\omega_{\mu\nu}\rho(J^{\mu\nu})}`$。对 Dirac 场，$`\rho(J^{\mu\nu})=S^{\mu\nu}`$ (1.106)。

**$`\mathfrak o(1,3)_{\mathbb C}`$ 的分解**

由 (0.34)，

```math
\left.
[J^i,J^j]=\epsilon_{ijk}J^k,\qquad
[J^i,K^j]=\epsilon_{ijk}K^k,\qquad
[K^i,K^j]=-\epsilon_{ijk}J^k.
\right.
\tag{1.49}
```

定义

```math
\left.
\begin{aligned}
A^i&:=\frac12\Bigl(\frac12\epsilon_{ijk}J^{jk}+iJ^{0i}\Bigr)=\frac i2\bigl(J^i+iK^i\bigr),\\
B^i&:=\frac12\Bigl(\frac12\epsilon_{ijk}J^{jk}-iJ^{0i}\Bigr)=\frac i2\bigl(J^i-iK^i\bigr),
\end{aligned}
\right.
\tag{1.50}
```

即 $`A^1=\frac12(J^{23}+iJ^{01})`$，$`A^2=\frac12(J^{31}+iJ^{02})`$，$`A^3=\frac12(J^{12}+iJ^{03})`$，$`B^i`$ 的表达式与此相同，只需作替换 $`iJ^{0i}\to-iJ^{0i}`$。$`A^i`$ 和 $`B^i`$ 不是实的，因此属于 $`\mathfrak o(1,3)_{\mathbb C}`$ 而不属于 $`\mathfrak o(1,3)`$。由 (1.49)，

```math
\left.
\boxed{[A^i,A^j]=i\epsilon_{ijk}A^k,\qquad
[B^i,B^j]=i\epsilon_{ijk}B^k,\qquad
[A^i,B^j]=0.}
\right.
\tag{1.51}
```

因此

```math
\left.
\mathfrak o(1,3)_{\mathbb C}=\mathfrak g_A\oplus\mathfrak g_B,\qquad
\mathfrak g_A:=\mathop{\rm span}\nolimits\,_{\mathbb C}\{A^1,A^2,A^3\},\quad
\mathfrak g_B:=\mathop{\rm span}\nolimits\,_{\mathbb C}\{B^1,B^2,B^3\}.
\right.
\tag{1.52}
```

映射 $`A^i\mapsto\sigma^i/2`$ 和 $`B^i\mapsto\sigma^i/2`$ 分别把 $`\mathfrak g_A`$ 和 $`\mathfrak g_B`$ 等同于 $`\mathfrak{su}(2)\cong\mathfrak o(3)`$ 的复化。

**不可约表示**

取 $`\mathfrak g_A`$ 的表示 $`(\rho_A,V_A)`$ 和 $`\mathfrak g_B`$ 的表示 $`(\rho_B,V_B)`$，记 $`n_A:=\dim V_A`$，$`n_B:=\dim V_B`$。对 $`v_A\in\mathfrak g_A`$ 和 $`v_B\in\mathfrak g_B`$，二者的张量积（Kronecker 积）$`(\rho,V_A\otimes V_B)`$ 为：

```math
\left.
\begin{aligned}
\rho(v_A+v_B)&:=\rho_A(v_A)\otimes I_{n_B}+I_{n_A}\otimes\rho_B(v_B),\\
\rho(v_A+v_B)\bigl(|a\rangle\otimes|b\rangle\bigr)&=\rho_A(v_A)|a\rangle\otimes|b\rangle+|a\rangle\otimes\rho_B(v_B)|b\rangle,\\
e^{\rho(v_A+v_B)}&=e^{\rho_A(v_A)}\otimes e^{\rho_B(v_B)}.
\end{aligned}
\right.
\tag{1.53}
```

最后一行成立，是因为第一行中的两项对易。

$`\mathfrak{su}(2)`$ 的不可约表示为 $`V_j`$，其基为 $`|j,m\rangle`$，$`m=-j,\ldots,j`$，$`\rho_A(A^3)`$（或 $`\rho_B(B^3)`$）在其上的作用是乘以 $`m`$。这里 $`j=0,\frac12,1,\ldots`$，$`\dim V_j=2j+1`$。$`\mathfrak g_A\oplus\mathfrak g_B`$ 的每个有限维不可约表示都是 $`V_{j_1}\otimes V_{j_2}`$，而每个有限维表示都是它们的直和：

```math
\left.
\boxed{(j_1,j_2),\qquad j_1,j_2\in\{0,\tfrac12,1,\tfrac32,\ldots\},\qquad\dim=(2j_1+1)(2j_2+1).}
\right.
\tag{1.54}
```

**转动 $`2\pi`$**

由 (1.50)，$`A^3+B^3=iJ^3`$，故在 $`(j_1,j_2)`$ 上

```math
\left.
e^{2\pi J^3}=I_4,\qquad
e^{2\pi\rho(J^3)}=e^{-2\pi i\rho(A^3+B^3)}=(-1)^{2(j_1+j_2)}I_n.
\right.
\tag{1.55}
```

因此只有当 $`j_1+j_2`$ 为整数时，$`D(e^X):=e^{\rho(X)}`$ 才是 $`SO(1,3)^+`$ 的表示。当 $`j_1+j_2`$ 为半整数时，它只在相差一个符号的意义下有定义；对 Dirac 场，$`\theta^3=2\pi`$ 时 $`\Lambda_{\frac12}=-I_4`$。

<br><br>

<a id="classical-dynamics"></a>
### 1.4 经典场的动力学

<a id="field-theory-lagrangian"></a>
#### 拉氏量

定义了经典场之后，接下来讨论它们的动力学。在拉格朗日形式中，这相当于为场构造拉氏量密度。
在经典力学中，动力学变量是只依赖于时间的广义坐标 $`q_a(t)`$。在场论中，动力学变量是依赖于时空点 $`x=(t,\mathbf x)`$ 的场分量 $`\Psi_\alpha(x)`$。

对 $`x`$ 有两种理解方式：

1. 在固定时刻 $`t`$，指标对 $`(\alpha,\mathbf x)`$ 起 $`q_a(t)`$ 中标签 $`a`$ 的作用，故 $`\Psi_\alpha(t,\mathbf x)`$ 对应于 $`q_a(t)`$。
2. 更物理地看，整个时空点 $`x`$ 起经典力学中 $`t`$ 的作用，故 $`\Psi_\alpha(x)`$ 对应于 $`q_a(t)`$。

**定义**

- **位形空间**：场 $`\Psi`$，在每个 $`x`$ 处 $`\Psi(x)\in\mathbb R^n`$ 或 $`\mathbb C^n`$。
- **动力学结构**：拉氏量密度，即光滑函数

```math
\left.
\begin{aligned}
\mathcal L:(\mathbb R^n\ \text{或}\ \mathbb C^n)\times(\mathbb R^n\ \text{或}\ \mathbb C^n)^4&\to\mathbb R,\\
(\Psi_\alpha,\partial_\mu\Psi_\alpha)&\mapsto\mathcal L(\Psi_\alpha,\partial_\mu\Psi_\alpha),
\end{aligned}
\right.
\tag{1.56}
```

其中 $`\partial_\mu\Psi_\alpha`$ 视为独立变量，且不显含 $`x`$。

- **作用量**：场上的泛函，对任意有界区域 $`\Omega\subset\mathbb R^4`$，

```math
\left.
\boxed{S[\Psi]:=\int_\Omega d^4x\,\mathcal L\bigl(\Psi_\alpha(x),\partial_\mu\Psi_\alpha(x)\bigr).}
\right.
\tag{1.57}
```

- **解**：在 $`\partial\Omega`$ 上为零的变分下使 $`S`$ 取驻值的场 $`\Psi`$，

```math
\left.
\frac{d}{ds}S[\Psi+s\eta]\Big|_{s=0}=0,
\right.
\tag{1.58}
```

对每个满足 $`\eta|_{\partial\Omega}=0`$ 的光滑 $`\eta`$ 及每个 $`\Omega`$ 成立。

**对拉氏量密度的要求**

对这里考虑的局域相对论性场论，我们要求：

- **Lorentz 不变性**：由 $`\mathcal L`$ 构造的作用量是 Lorentz 标量。
- **实性**：拉氏量密度 $`\mathcal L`$ 是实的。
- **局域性**：$`\mathcal L`$ 只依赖于同一时空点处的场及其有限个导数。

还可以附加更多数学上的限制，但它们是约定性的选择，而非普适公理；归根结底，本质要求是与物理实在相符，使拉氏量至少能描述或解释现实世界的一部分。




**Euler–Lagrange 方程**

与 (1.6) 同理，对 (1.58) 分部积分并利用 $`\eta|_{\partial\Omega}=0`$，可知 $`\Psi`$ 是解当且仅当

```math
\left.
\boxed{\partial_\mu\frac{\partial\mathcal L}{\partial(\partial_\mu\Psi_\alpha)}
-\frac{\partial\mathcal L}{\partial\Psi_\alpha}=0.}
\right.
\tag{1.59}
```

**哈密顿表述**

对于正规的 Legendre 变换，

```math
\left.
\begin{aligned}
\pi_\alpha&:=\frac{\partial\mathcal L}{\partial\dot\Psi_\alpha},
&
\mathcal H&:=\pi_\alpha\dot\Psi_\alpha-\mathcal L,
&
H&=\int d^3x\,\mathcal H,\\
\dot\Psi_\alpha(t,\mathbf x)&=\frac{\delta H}{\delta\pi_\alpha(t,\mathbf x)},
&
\dot\pi_\alpha(t,\mathbf x)&=-\frac{\delta H}{\delta\Psi_\alpha(t,\mathbf x)}.
\end{aligned}
\right.
\tag{1.60}
```

<br><br>

<a id="classical-noether"></a>
#### 对称变换与 Noether 定理

**变换**

- **变换**：满足 $`\phi_0=\mathrm{id}`$ 的单参数族 $`\phi_\lambda`$，既作用于时空，也作用于场，

```math
\left.
\begin{aligned}
\phi_\lambda:\mathbb R^4&\to\mathbb R^4,\\
x&\mapsto x'=\phi_\lambda(x),
\end{aligned}
\qquad
x'^\mu=:x^\mu+\delta x^\mu,\qquad
\Psi\mapsto\Psi',
\right.
\tag{1.61}
```

其中 $`\Psi'`$ 的形式由 (1.64) 和 (1.72) 给出：若 $`\phi_\lambda=(\Lambda,a)`$ 是 Poincaré 变换，则有 (1.46) 的 $`\Psi'=U(\Lambda,a)\Psi`$；若为内部变换，则 $`x'=x`$，$`\Psi'=g(\lambda)\Psi`$。

**对称变换**

- **对称变换**：对每个区域都使每个场的作用量保持不变的变换，

```math
\left.
\boxed{S'=S\quad\text{对任意 }\Psi\text{ 及任意 }\Omega,}
\right.
\tag{1.62}
```

其中 $`S'`$ 是 $`\Psi'`$ 在 $`\phi_\lambda(\Omega)`$ 上的作用量，其显式表达式见 (1.66)。

**守恒量**

- **守恒量**：时间切片 $`t`$ 上场及其导数的泛函 $`\mathcal Q[\Psi,t]`$，使得对每个连同其一阶导数在空间无穷远处衰减得足够快的解 $`\Psi`$，$`\mathcal Q[\Psi,t]`$ 都与 $`t`$ 无关。

**Noether 定理**

若 $`\phi_\lambda`$ 是对称变换，则

```math
\left.
\boxed{
\mathcal Q[\Psi,t]:=\int d^3x\left(
\frac{\partial\mathcal L}{\partial\dot\Psi_\alpha}
\frac{\partial\,\delta x^\nu}{\partial\lambda}
\partial_\nu\Psi_\alpha
-\frac{\partial\mathcal L}{\partial\dot\Psi_\alpha}
\frac{\partial\,\delta_0\Psi_\alpha}{\partial\lambda}
-\mathcal L\frac{\partial\,\delta x^0}{\partial\lambda}
\right)
}
\right.
\tag{1.63}
```

是守恒量，其中 $`\delta_0\Psi_\alpha`$ 的定义见 (1.64)，对 $`\lambda`$ 的导数在 $`\lambda=0`$ 处取值，衰减条件保证积分收敛并使 (1.70) 中的表面项为零。

**证明**

**(A) 坐标变换**

设 $`x'=\phi_\lambda(x)`$，其中 $`\lambda`$ 为无穷小。定义两种场变分：

```math
\left.
\begin{aligned}
\delta_0\Psi_\alpha(x)
&:=\Psi'_\alpha(x')-\Psi_\alpha(x)
=D_{\alpha\beta}(\Lambda)\Psi_\beta(x)-\Psi_\alpha(x),\\
\delta\Psi_\alpha(x)
&:=\Psi'_\alpha(x)-\Psi_\alpha(x)
=[U(\Lambda,a)\Psi]_\alpha(x)-\Psi_\alpha(x).
\end{aligned}
\right.
\tag{1.64}
```

这里 $`\Psi'`$ 是变换后的场。利用推前 $`(\phi_\lambda)_*\Psi:=\Psi\circ\phi_\lambda^{-1}`$，可写出 $`\Psi'_\alpha=D_{\alpha\beta}(\Lambda)\,[(\phi_\lambda)_*\Psi]_\beta`$。在 $`x'`$ 处取值得 $`\Psi'_\alpha(x')=D_{\alpha\beta}(\Lambda)\Psi_\beta(x)`$，这就是第一行的最后一个等号，因此第一种变分 $`\delta_0\Psi_\alpha`$ 描述的是场本身的变换。对 $`\phi_\lambda=(\Lambda,a)`$，由 (1.46) 有 $`\Psi'=U(\Lambda,a)\Psi`$，这就是第二行的最后一个等号。若 $`\phi_\lambda`$ 不是 Poincaré 变换，则 $`D(\Lambda)`$ 换成单位矩阵，且 $`\delta_0\Psi_\alpha=0`$。

准确到 $`\lambda`$ 的一阶，两种变分的关系为

```math
\left.
\begin{aligned}
\delta\Psi_\alpha(x)
&=\bigl[\Psi'_\alpha(x')-\Psi_\alpha(x)\bigr]
-\bigl[\Psi'_\alpha(x')-\Psi'_\alpha(x)\bigr]\\
&=\delta_0\Psi_\alpha(x)-\delta x^\mu\partial_\mu\Psi'_\alpha(x)\\
&=\delta_0\Psi_\alpha(x)-\delta x^\mu\partial_\mu\Psi_\alpha(x),
\end{aligned}
\right.
\tag{1.65}
```

其中最后一步用到 $`\Psi'_\alpha=\Psi_\alpha+O(\lambda)`$。

在时空区域 $`\Omega`$ 上，变换前后的作用量分别为

```math
\left.
\begin{aligned}
S&=\int_\Omega d^4x\,
\mathcal L\bigl(\Psi_\alpha(x),\partial_\mu\Psi_\alpha(x)\bigr),\\
S'&=\int_{\phi_\lambda(\Omega)}d^4x'\,
\mathcal L\bigl(\Psi'_\alpha(x'),\partial'_\mu\Psi'_\alpha(x')\bigr),
\end{aligned}
\right.
\tag{1.66}
```

其中 $`\partial'_\mu:=\partial/\partial x'^\mu`$。$`S'`$ 中用的是同一个函数 $`\mathcal L`$：变换作用于场位形和区域 $`\Omega`$，而不作用于拉氏量。这里不假设 $`\mathcal L`$ 的任何性质。

把 $`S'`$ 中的积分变量从 $`x'`$ 换回 $`x`$，于是 $`\phi_\lambda(\Omega)`$ 变为 $`\Omega`$。准确到 $`\lambda`$ 的一阶，

```math
\left.
\begin{aligned}
d^4x'
&=\det\!\left(\frac{\partial x'^\mu}{\partial x^\nu}\right)d^4x
=\bigl(1+\partial_\mu\delta x^\mu\bigr)d^4x,\\
\partial'_\mu
&=\frac{\partial x^\nu}{\partial x'^\mu}\partial_\nu
=\partial_\mu-(\partial_\mu\delta x^\nu)\partial_\nu,\\
\Psi'_\alpha(x')
&=\Psi_\alpha(x)+\delta_0\Psi_\alpha(x),\\
\partial'_\mu\Psi'_\alpha(x')
&=\partial_\mu\Psi_\alpha(x)
+\partial_\mu\delta_0\Psi_\alpha(x)
-(\partial_\mu\delta x^\nu)\partial_\nu\Psi_\alpha(x),
\end{aligned}
\right.
\tag{1.67}
```

其中第三行即 (1.64)。因此

```math
\left.
S'=\int_\Omega d^4x\,
\bigl(1+\partial_\mu\delta x^\mu\bigr)\,
\mathcal L\bigl(
\Psi_\alpha+\delta_0\Psi_\alpha,\ 
\partial_\mu\Psi_\alpha
+\partial_\mu\delta_0\Psi_\alpha
-(\partial_\mu\delta x^\nu)\partial_\nu\Psi_\alpha
\bigr).
\right.
\tag{1.68}
```

把 (1.68) 展开到 $`\lambda`$ 的一阶，得到离壳恒等式

```math
\left.
\begin{aligned}
S'-S
&=\int_\Omega d^4x\,\biggl[
\mathcal L\,\partial_\mu\delta x^\mu
+\frac{\partial\mathcal L}{\partial\Psi_\alpha}\delta_0\Psi_\alpha\\
&\qquad
+\frac{\partial\mathcal L}{\partial(\partial_\mu\Psi_\alpha)}
\bigl(\partial_\mu\delta_0\Psi_\alpha-(\partial_\mu\delta x^\nu)\partial_\nu\Psi_\alpha\bigr)
\biggr]\\
&=\int_\Omega d^4x\,\biggl\{
\biggl[
\frac{\partial\mathcal L}{\partial\Psi_\alpha}
-\partial_\mu\frac{\partial\mathcal L}{\partial(\partial_\mu\Psi_\alpha)}
\biggr]\delta\Psi_\alpha\\
&\qquad
+\partial_\mu\biggl[
\mathcal L\,\delta x^\mu
+\frac{\partial\mathcal L}{\partial(\partial_\mu\Psi_\alpha)}\delta\Psi_\alpha
\biggr]
\biggr\}.
\end{aligned}
\right.
\tag{1.69}
```

第二个等号代入了 (1.65) 给出的 $`\delta_0\Psi_\alpha=\delta\Psi_\alpha+\delta x^\nu\partial_\nu\Psi_\alpha`$，并利用了乘积法则以及 $`\partial_\nu\mathcal L=\frac{\partial\mathcal L}{\partial\Psi_\alpha}\partial_\nu\Psi_\alpha+\frac{\partial\mathcal L}{\partial(\partial_\mu\Psi_\alpha)}\partial_\nu\partial_\mu\Psi_\alpha`$；后者成立是因为 $`\mathcal L`$ 不显含 $`x`$。

按假设，作用量不变：$`S'=S`$。取 $`\Omega=[t_1,t_2]\times V`$，并设 $`\Psi_\alpha`$ 满足 Euler–Lagrange 方程，于是 (1.69) 中的 Euler–Lagrange 项为零。再由 Gauss 定理得

```math
\left.
\begin{aligned}
0
&=\int_\Omega d^4x\,\partial_\mu\biggl[
\mathcal L\,\delta x^\mu
+\frac{\partial\mathcal L}{\partial(\partial_\mu\Psi_\alpha)}\delta\Psi_\alpha
\biggr]\\
&=\biggl[\int_V d^3x\,\biggl(
\mathcal L\,\delta x^0
+\frac{\partial\mathcal L}{\partial\dot\Psi_\alpha}\delta\Psi_\alpha
\biggr)\biggr]_{t_1}^{t_2}\\
&\quad
+\int_{t_1}^{t_2}dt\oint_{\partial V}dS_i\,\biggl(
\mathcal L\,\delta x^i
+\frac{\partial\mathcal L}{\partial(\partial_i\Psi_\alpha)}\delta\Psi_\alpha
\biggr).
\end{aligned}
\right.
\tag{1.70}
```

由衰减条件，当 $`V\to\mathbb R^3`$ 时表面项为零。由于 $`t_1`$ 和 $`t_2`$ 任意，

```math
\left.
\int d^3x\,\biggl(
\mathcal L\,\delta x^0
+\frac{\partial\mathcal L}{\partial\dot\Psi_\alpha}\delta\Psi_\alpha
\biggr)=\text{const}.
\right.
\tag{1.71}
```

代入 (1.65) 给出的 $`\delta\Psi_\alpha=\delta_0\Psi_\alpha-\delta x^\nu\partial_\nu\Psi_\alpha`$，对 $`\lambda`$ 求导，并改变整体符号，即得坐标变换情形的 (1.63)。

**(B) 内部变换**

现在 $`\phi_\lambda`$ 在时空上的作用是平凡的，在场上则通过满足 $`g(0)=I_n`$ 的常数矩阵 $`g(\lambda)`$ 作用：

```math
\left.
x'^\mu=x^\mu,\qquad
\Psi'_\alpha(x)=g_{\alpha\beta}(\lambda)\,\Psi_\beta(x).
\right.
\tag{1.72}
```

因此 $`\delta x^\mu=0`$，(1.64) 中的两种变分相同：$`\delta\Psi_\alpha(x)=\delta_0\Psi_\alpha(x)=g_{\alpha\beta}(\lambda)\Psi_\beta(x)-\Psi_\alpha(x)`$。取 $`\delta x^\mu=0`$ 重复 (1.66)–(1.71) 的推导：在 (1.67) 中 $`d^4x'=d^4x`$，$`\partial'_\mu=\partial_\mu`$；(1.68)–(1.70) 中含 $`\delta x^\mu`$ 的项消失；(1.71) 变为

```math
\left.
\int d^3x\,\frac{\partial\mathcal L}{\partial\dot\Psi_\alpha}\,\delta_0\Psi_\alpha=\text{const}.
\right.
\tag{1.73}
```

对 $`\lambda`$ 求导并改变整体符号，即得 $`\delta x^\mu=0`$ 时的 (1.63)。$`\square`$

<a id="spacetime-conserved-quantities"></a>
**(1) 时空平移与能量–动量**

对固定的 $`\epsilon\in\mathbb R^4`$，取 $`\phi_\lambda(x)=x+\lambda\epsilon`$，于是 $`\delta x^\mu=\lambda\epsilon^\mu`$，$`\Lambda=I_4`$，$`\delta_0\Psi_\alpha=0`$。根据 (1.66)–(1.68)，由于 $`\mathcal L`$ 不显含 $`x`$，有 $`S'=S`$，于是 (1.63) 给出

```math
\left.
\mathcal Q=\epsilon^\nu\int d^3x\Bigl(\frac{\partial\mathcal L}{\partial\dot\Psi_\alpha}\partial_\nu\Psi_\alpha-\delta^0{}_\nu\mathcal L\Bigr)=\epsilon^\nu P_\nu,
\right.
\tag{1.74}
```

其中正则能动张量和四动量为

```math
\left.
\boxed{
\begin{aligned}
T^\mu{}_\nu&:=\frac{\partial\mathcal L}{\partial(\partial_\mu\Psi_\alpha)}
\,\partial_\nu\Psi_\alpha-\delta^\mu{}_\nu\mathcal L,
&
\partial_\mu T^\mu{}_\nu&=0,\\
P_\nu&:=\int d^3x\,T^0{}_\nu,
&
\frac{dP_\nu}{dt}&=0,
&
P_0&=H.
\end{aligned}}
\right.
\tag{1.75}
```

这里 $`\partial_\mu T^\mu{}_\nu=0`$ 由 (1.59) 在壳成立，$`P_0=H`$ 则由 (1.60) 得到。

<br><br>

<a id="dirac-constraint"></a>
### 1.5 Dirac 约束

<a id="singular-lagrangian"></a>
#### 奇异拉氏量

**定义**

设 $`L:\mathbb R^n\times\mathbb R^n\to\mathbb R`$ 为 (1.2) 中那样的光滑拉氏量，且不显含时间。

- **正则动量**：

```math
\left.
p_a:=\frac{\partial L}{\partial\dot q_a}(q,\dot q),\qquad a=1,\ldots,n.
\right.
\tag{1.76}
```

- **Hesse 矩阵**：对称矩阵

```math
\left.
W_{ab}:=\frac{\partial^2L}{\partial\dot q_a\,\partial\dot q_b}(q,\dot q),\qquad a,b=1,\ldots,n.
\right.
\tag{1.77}
```

- **正规拉氏量与奇异拉氏量**：若在 $`\mathrm{Conf}\times\mathbb R^n`$ 上 $`\det W\neq0`$，则称 $`L`$ 是正规的，否则称为奇异的。对奇异的 $`L`$，假设 $`\mathop{\rm rank}\nolimits\,W=r<n`$ 为常数。

若 $`L`$ 正规，则可由 (1.76) 解出速度 $`\dot q=\dot q(q,p)`$，而

```math
\left.
H(q,p):=\sum_{a=1}^np_a\,\dot q_a(q,p)-L\bigl(q,\dot q(q,p)\bigr)
\right.
\tag{1.78}
```

就是 [1.2 节](#hamiltonian-formalism)的哈密顿量 (1.30)。本节其余部分中 $`L`$ 均为奇异的。

**奇异拉氏量的直观物理图像**

以 $`W`$ 为常数矩阵的情形 $`L=\frac12\sum_{a,b=1}^nW_{ab}\dot q_a\dot q_b-V(q)`$ 为例，$`W`$ 就是质量矩阵，$`W`$ 不满秩可以直观地理解为沿某些方向运动的「质量」为零。适当重新定义广义坐标，可把 $`W`$ 化成分块对角形：左上角的 $`r\times r`$ 块可逆（不妨取为对角），其余元素为零，于是动能项不含后 $`n-r`$ 个坐标的速度。按势能是否依赖这 $`n-r`$ 个坐标，分两种情况。

1. 新坐标下的势能只含前 $`r`$ 个坐标。后 $`n-r`$ 个坐标在 $`L`$ 中完全不出现，运动方程对它们没有任何限制，说明原先的数学描述有冗余。

2. 新坐标下的势能仍含后 $`n-r`$ 个坐标。这些坐标的 Euler–Lagrange 方程不含加速度，只是坐标之间的关系，说明系统存在约束。



**初级约束**

由于 $`W`$ 对称，它的秩等于其最大可逆主子矩阵的阶数，因此适当重排坐标后可使

```math
\left.
\det\bigl(W_{ab}\bigr)_{a,b=1}^{r}\neq0.
\right.
\tag{1.79}
```

指标 $`\mu,\nu`$ 取其余的值 $`r+1,\ldots,n`$。由隐函数定理，可从 (1.76) 的前 $`r`$ 个方程局部地解出 $`\dot q_1,\ldots,\dot q_r`$：

```math
\left.
\dot q_a=\varphi_a(q,p_b,\dot q_\mu),\qquad a=1,\ldots,r,
\right.
\tag{1.80}
```

其中 $`p_b`$ 与 $`\dot q_\mu`$ 分别代表 $`(p_1,\ldots,p_r)`$ 与 $`(\dot q_{r+1},\ldots,\dot q_n)`$。

把 (1.80) 代入 (1.76) 的其余方程，得到

```math
\left.
p_\mu=\frac{\partial L}{\partial\dot q_\mu}\bigl(q,\varphi(q,p_b,\dot q_\nu),\dot q_\nu\bigr)=:g_\mu(q,p_b,\dot q_\nu),
\right.
\tag{1.81}
```

并且,可以进一步证明 $`g_\mu`$ 不依赖于 $`\dot q_\nu`$, 证明如下：

将恒等式 $`p_b=\frac{\partial L}{\partial\dot q_b}(q,\varphi,\dot q_\nu)`$ 对 $`\dot q_\nu`$ 求导，得到 $`\sum_{a=1}^rW_{ba}\frac{\partial\varphi_a}{\partial\dot q_\nu}=-W_{b\nu}`$，因此

```math
\left.
\frac{\partial}{\partial\dot q_\nu}\frac{\partial L}{\partial\dot q_\mu}\bigl(q,\varphi,\dot q\bigr)
=W_{\mu\nu}+\sum_{a=1}^rW_{\mu a}\frac{\partial\varphi_a}{\partial\dot q_\nu}
=W_{\mu\nu}-\sum_{a,b=1}^rW_{\mu a}\bigl(W^{-1}\bigr)_{ab}W_{b\nu}=0,
\right.
\tag{1.82}
```

其中 $`(W^{-1})_{ab}`$ 是分块 (1.79) 的逆矩阵。最后一个表达式是该分块在 $`W`$ 中的 Schur 补，由于 $`\mathop{\rm rank}\nolimits\,W=r`$，它为零。

- **初级约束**：

```math
\left.
\boxed{\chi_\mu(q,p):=p_\mu-g_\mu(q,p_b)=0,\qquad\mu=r+1,\ldots,n.}
\right.
\tag{1.83}
```

$`n`$ 个方程 (1.76) 等价于 (1.80) 与 (1.83) 联立。约束 (1.83) 只含 $`(q,p)`$，它们在相空间中定义约束曲面，即映射 $`(q,\dot q)\mapsto(q,p(q,\dot q))`$ 的像。

- **弱等号**：$`F\approx G`$ 表示相空间函数 $`F`$ 与 $`G`$ 在约束曲面上相等。

**正则哈密顿量**

定义

```math
\left.
H_c:=\sum_{a=1}^np_a\dot q_a-L(q,\dot q),
\right.
\tag{1.84}
```

其中 $`\dot q_1,\ldots,\dot q_r`$ 按 (1.80) 代入，于是 $`H_c`$ 是 $`(q,p,\dot q_\mu)`$ 的函数。由 (1.80)、(1.81) 和 (1.83)，

```math
\left.
\frac{\partial H_c}{\partial\dot q_\nu}
=\sum_{a=1}^r\Bigl(p_a-\frac{\partial L}{\partial\dot q_a}\Bigr)\frac{\partial\varphi_a}{\partial\dot q_\nu}
+p_\nu-\frac{\partial L}{\partial\dot q_\nu}
=\chi_\nu(q,p),
\right.
\tag{1.85}
```

它与 $`\dot q_\mu`$ 无关，并且在约束曲面上为零。因此在约束曲面上 $`H_c`$ 与 $`\dot q_\mu`$ 无关；而由 (1.83)，它在约束曲面上只是 $`(q,p_1,\ldots,p_r)`$ 的函数。

**总哈密顿量与相容性**

设 $`H_c`$ 为正则哈密顿量，$`u^A`$ 为施加初级约束的拉格朗日乘子。

```math
\left.
\boxed{
\begin{aligned}
H_T&=H_c+\sum_A u^A(t)\chi_A^{(1)},\\
\dot\chi_A&=\frac{\partial\chi_A}{\partial t}
+\{\chi_A,H_T\}_{\mathrm{PB}}\approx0.
\end{aligned}}
\right.
\tag{1.86}
```

相容性条件可能给出次级及更高级的约束，可能确定乘子，也可能恒成立。反复迭代，直至封闭。

**第一类约束与第二类约束**

```math
\left.
\{F,G\}_{\mathrm{PB}}
:=\sum_{a=1}^n\left(
\frac{\partial F}{\partial q_a}\frac{\partial G}{\partial p_a}
-\frac{\partial F}{\partial p_a}\frac{\partial G}{\partial q_a}
\right),
\qquad
\{q_a,p_b\}_{\mathrm{PB}}=\delta_{ab}.
\right.
\tag{1.87}
```

若一个约束与每个约束的 Poisson 括号都弱等于零，则称它为第一类约束。分离出所有第一类组合后，剩下的第二类约束 $`\chi_a^{\mathrm{sc}}`$ 的括号矩阵可逆：

```math
\left.
\{\chi^{\mathrm{fc}},\chi_A\}_{\mathrm{PB}}\approx0
\quad\text{对所有 }A,
\qquad
C_{ab}:=\{\chi_a^{\mathrm{sc}},\chi_b^{\mathrm{sc}}\}_{\mathrm{PB}},
\qquad
\det C\ne0.
\right.
\tag{1.88}
```

**Dirac 括号**

```math
\left.
\boxed{
\begin{aligned}
\{F,G\}_{\mathrm D}
&:=\{F,G\}_{\mathrm{PB}}
-\sum_{a,b}\{F,\chi_a^{\mathrm{sc}}\}_{\mathrm{PB}}
(C^{-1})_{ab}\{\chi_b^{\mathrm{sc}},G\}_{\mathrm{PB}},\\
\{F,\chi_a^{\mathrm{sc}}\}_{\mathrm D}&=0.
\end{aligned}}
\right.
\tag{1.89}
```

于是第二类约束可以作为强等式施加。对于场，需使用泛函导数、空间积分和逆积分核。

**物理自由度**

对于约束相互独立、规范轨道具有预期维数的正规系统，

```math
\left.
\boxed{
N_{\mathrm{physical}}
=n-N_{\mathrm{first}}-\frac12N_{\mathrm{second}}.
}
\right.
\tag{1.90}
```

对于场，此式计数的是每个空间点上的局域位形自由度，并须附加边界与零模方面的限定。


<br><br>
