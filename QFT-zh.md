# QFT（中文版）

> 分段阅读: [1](QFT-zh-part-01.md) · [2](QFT-zh-part-02.md) · [3](QFT-zh-part-03.md) · [4](QFT-zh-part-04.md)


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
  - [1.6 标量场](#scalar-field)
    - [拉氏量](#scalar-lagrangian)
    - [Klein–Gordon 方程的解](#scalar-field-solutions)
  - [1.7 Dirac 场 $`\psi`$ ](#dirac-field)
    - [拉氏量](#dirac-lagrangian)
    - [Weyl 表示下 Dirac 方程的解](#weyl-spinor-solutions)
    - [Dirac 双线性型](#dirac-bilinears)
  - [1.8 Proca 场](#proca-field)
    - [拉氏量](#proca-lagrangian)
    - [Proca 方程的解](#proca-field-solutions)
  - [1.9 矢量场](#vector-field)
    - [拉氏量](#maxwell-lagrangian)
    - [Maxwell 方程的解](#maxwell-field-solutions)
- [2. 算符量子化](#qft-ch2)
  - [2.1 正则量子化](#canonical-quantization)
  - [2.2 用 Dirac 括号量子化](#quantization-with-dirac-brackets)
    - [复标量场的量子化](#complex-scalar-field-quantization)
    - [Dirac 场的量子化](#dirac-field-quantization)
    - [Proca 场的量子化](#proca-field-quantization)
  - [2.3 Gupta–Bleuler 量子化](#gupta-bleuler-quantization)
  - [2.4 对称性](#symmetry)
    - [Schrödinger 绘景](#schrodinger-picture)
    - [Heisenberg 绘景](#heisenberg-picture)
- [3. 标准模型](#qft-ch3)
  - [3.1 Yang–Mills 理论](#yang-mills)
  - [3.2 量子电动力学](#qed)
  - [3.3 量子色动力学](#qcd)
  - [3.4 自发对称性破缺与 Higgs 机制](#higgs-mechanism)
    - [Higgs 拉氏量](#higgs-lagrangian)
    - [自发对称性破缺](#spontaneous-symmetry-breaking)
    - [Higgs 机制](#higgs-mechanism-masses)
  - [3.5 电弱理论](#electroweak-theory)
    - [标准模型中的轻子](#sm-leptons)
    - [动能项](#electroweak-kinetic-terms)
    - [Yukawa 耦合与带电轻子质量](#charged-lepton-masses)
    - [规范玻色子质量](#gauge-boson-masses)
    - [夸克](#sm-quarks)
    - [带电流与中性流](#electroweak-currents)
- [4. 路径积分](#qft-ch4)
  - [4.1 量子力学中的路径积分](#path-integrals-in-quantum-mechanics)
  - [4.2 量子场论中的路径积分](#path-integrals-in-field-theory)
  - [4.3 $`\phi^3`$ 理论](#phi-cubed-theory)
  - [4.4 费米子场的路径积分](#path-integrals-for-fermion-fields)
    - [Grassmann 代数](#grassmann-algebra)
    - [Grassmann 代数上的微积分](#grassmann-calculus)
- [5. 超出标准模型的新物理](#qft-ch5)
  - [5.1 Seesaw 机制](#seesaw-mechanism)
    - [I 型 seesaw](#type-i-seesaw)
    - [II 型 seesaw](#type-ii-seesaw)
    - [III 型 seesaw](#type-iii-seesaw)
    - [轻子生成](#leptogenesis)
  - [5.2 暗物质](#dark-matter)
- [6. 散射理论](#qft-ch6)
  - [6.1 相互作用绘景](#interaction-picture)
  - [6.2 S 矩阵与 Wick 定理](#s-matrix-and-wick-theorem)
  - [6.3 费曼图与费曼规则](#feynman-diagrams)
  - [6.4 关联函数](#correlation-functions)
    - [微扰真空关联函数](#perturbative-correlation-functions)
    - [非微扰真空关联函数](#nonperturbative-correlation-functions)
  - [6.5 LSZ 约化公式](#lsz-reduction)
  - [6.6 截面与衰变率](#cross-sections-and-decay-rates)
- [7. 重整化](#qft-ch7)
  - [7.1 QED 重整化](#qed-renormalization)
- [8. 多圈重整化](#qft-ch8)
- [9. 宇宙学](#qft-ch9)

---

<a id="qft-ch0"></a>
## 0. 数学基础

<a id="fourier-transform"></a>
### 0.1 Fourier 变换

四维 Fourier 变换采用如下约定，因子 $`(2\pi)^{-4}`$ 放在逆变换中：

```math
\begin{aligned}
\widetilde f(p)&=\int d^4x\,e^{+ip\cdot x}f(x),\\
f(x)&=\int\frac{d^4p}{(2\pi)^4}\,e^{-ip\cdot x}\widetilde f(p).
\end{aligned}
```

其中 $`x^\mu=(t,\mathbf x)`$，$`p^\mu=(p^0,\mathbf p)`$，相位为

```math
p\cdot x=p_\mu x^\mu=p^0t-\mathbf p\cdot\mathbf x.
```

Dirac $`\delta`$ 函数的 Fourier 表示为

```math
\begin{aligned}
\int\frac{d^4p}{(2\pi)^4}\,e^{-ip\cdot(x-y)}&=\delta^{(4)}(x-y),\\[6pt]
\int d^4x\,e^{i(p-q)\cdot x}&=(2\pi)^4\delta^{(4)}(p-q).
\end{aligned}
```


<br><br>

<a id="gamma-matrices"></a>
### 0.2 $`\gamma`$ 矩阵：Weyl 表示

Pauli 矩阵为

```math
\sigma^1=\begin{pmatrix}0&1\\1&0\end{pmatrix},\qquad
\sigma^2=\begin{pmatrix}0&-i\\i&0\end{pmatrix},\qquad
\sigma^3=\begin{pmatrix}1&0\\0&-1\end{pmatrix}.
```

**Pauli 矩阵的性质**

对每个 $`i=1,2,3`$，

```math
(\sigma^i)^\dagger=\sigma^i,\qquad
(\sigma^i)^2=I_2,\qquad
(\sigma^i)^{-1}=\sigma^i,\qquad
\mathop{\rm tr}\nolimits\,\sigma^i=0,\qquad
\det\sigma^i=-1.
```

因此，每个 Pauli 矩阵既是厄米矩阵又是幺正矩阵，本征值为 $`+1`$ 和 $`-1`$。

乘积恒等式为

```math
\sigma^i\sigma^j=\delta^{ij}I_2+i\epsilon^{ijk}\sigma^k.
```

由此得到对易关系与反对易关系，以及迹正交关系：

```math
[\sigma^i,\sigma^j]=2i\epsilon^{ijk}\sigma^k,\qquad
\{\sigma^i,\sigma^j\}=2\delta^{ij}I_2,\qquad
\mathop{\rm tr}\nolimits (\sigma^i\sigma^j)=2\delta^{ij}.
```

对任意 $`\mathbf a,\mathbf b\in\mathbb R^3`$，乘积恒等式也可写成

```math
(\mathbf a\cdot\boldsymbol\sigma)(\mathbf b\cdot\boldsymbol\sigma)
=(\mathbf a\cdot\mathbf b)I_2
+i(\mathbf a\times\mathbf b)\cdot\boldsymbol\sigma,
\qquad \boldsymbol\sigma=(\sigma^1,\sigma^2,\sigma^3).
```

**$`\gamma`$ 矩阵**

Pauli 四矢量

```math
\sigma^\mu:=(I_2,\boldsymbol\sigma),\qquad
\bar\sigma^\mu:=(I_2,-\boldsymbol\sigma),\qquad \mu=0,1,2,3.
```

用它们定义 Weyl 表示下的 $`\gamma`$ 矩阵：

```math
\gamma^\mu:=
\begin{pmatrix}
0&\sigma^\mu\\
\bar\sigma^\mu&0
\end{pmatrix}_{4\times4}.
```

这些矩阵满足

```math
\{\gamma^\mu,\gamma^\nu\}=2\eta^{\mu\nu}I_4.
```

```math
(\gamma^0)^2=I_4,\qquad
(\gamma^i)^2=-I_4,\\
(\gamma^0)^\dagger=\gamma^0,\qquad
(\gamma^i)^\dagger=-\gamma^i.
```

因此每个 $`\gamma^\mu`$ 都是幺正的：

```math
(\gamma^\mu)^\dagger\gamma^\mu=I_4.
```

定义

```math
\gamma^5:=i\gamma^0\gamma^1\gamma^2\gamma^3
=\begin{pmatrix}-I_2&0\\0&I_2\end{pmatrix}
.
```

它满足

```math
(\gamma^5)^2=I_4,\qquad
\{\gamma^5,\gamma^\mu\}=0,\qquad
(\gamma^5)^\dagger = (\gamma^5).
```

<br><br>

<a id="classical-poincare"></a>
### 0.3 IO(1,3) 群

**O(1,3) 群**

为区分矩阵 $`\Lambda`$ 与相应的坐标变换张量 $`\Lambda`$，把矩阵记为 $`[\Lambda]`$，张量仍简记为 $`\Lambda`$。对 $`\eta`$ 采用同样的记号。

矩阵 $`[\Lambda]`$

```math
O(1,3):=\{[\Lambda]\in GL(4,\mathbb R)\mid [\Lambda]^T[\eta][\Lambda]=[\eta]\}.
```

其中 $`[\eta]=\mathop{\rm diag}\nolimits (1,-1,-1,-1)`$。

张量 $`\Lambda`$

给定 Minkowski 时空的一个具体的微分同胚 $`\phi:x\mapsto x'`$，得到张量

```math
\Lambda^\mu{}_\nu:=\frac{\partial x'^\mu}{\partial x^\nu}.
```

顺便指出，可以证明 Minkowski 时空的等距变换必为线性的，至多相差一个平移。

$`[\Lambda]`$ 第 $`\mu`$ 行、第 $`\nu`$ 列的矩阵元就是张量 $`\Lambda`$ 的相应分量：

```math
[\Lambda]_{\mu\nu}=\Lambda^\mu{}_\nu.
```

同理，

```math
[\eta]_{\mu\nu}=\eta_{\mu\nu}.
```

因此，等价地有如下关系：

```math
\eta_{\mu\nu}\Lambda^\mu{}_\rho\Lambda^\nu{}_\sigma=\eta_{\rho\sigma}.
```

其中用到了关系 $`([\Lambda]^T)_{\mu\nu}=\Lambda^\nu{}_\mu`$。这正是 $`\phi`$ 为 Minkowski 时空等距变换的条件。


$`[\Lambda]`$ 的逆和转置满足

```math
[\Lambda]^{-1}=[\eta][\Lambda]^T[\eta],\qquad
[\Lambda][\eta][\Lambda]^T=[\eta],
```

故 $`[\Lambda]^{-1}`$ 和 $`[\Lambda]^T`$ 也属于 $`O(1,3)`$。

写成分量形式，第一个关系为

```math
(\Lambda^{-1})^\mu{}_\nu=\Lambda_\nu{}^\mu.
```

**连通性**

对 $`[\Lambda]^T[\eta][\Lambda]=[\eta]`$ 取行列式，得

```math
(\det[\Lambda])^2=1\quad\Longrightarrow\quad\det[\Lambda]=\pm1.
```

在 $`\eta_{\mu\nu}\Lambda^\mu{}_\rho\Lambda^\nu{}_\sigma=\eta_{\rho\sigma}`$ 中令 $`\rho=\sigma=0`$，得

```math
(\Lambda^0{}_0)^2=1+\sum_i(\Lambda^i{}_0)^2\ge1\quad\Longrightarrow\quad\Lambda^0{}_0\ge1\ \text{或}\ \Lambda^0{}_0\le-1.
```

可以证明，$`O(1,3)`$ 恰有这四个连通分支。

定义时间反演 $`T`$ 与空间反演 $`P`$ 为

```math
T:(t,\mathbf x)\mapsto(-t,\mathbf x),\qquad
P:(t,\mathbf x)\mapsto(t,-\mathbf x),
```

其矩阵为

```math
[T]=\mathop{\rm diag}\nolimits (-1,1,1,1),\qquad
[P]=\mathop{\rm diag}\nolimits (1,-1,-1,-1).
```

相应的张量为

```math
T^\mu{}_\nu=\delta^\mu{}_\nu-2\delta^\mu{}_0\delta^0{}_\nu,\qquad
P^\mu{}_\nu=-\delta^\mu{}_\nu+2\delta^\mu{}_0\delta^0{}_\nu.
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
SO(1,3)=\mathcal L^\uparrow_+\cup\mathcal L^\downarrow_+.
```

此外，$`SO(1,3)^+=\mathcal L^\uparrow_+`$ 是 $`O(1,3)`$ 的子群。

从物理上看，$`T`$ 和 $`P`$ 分别对应时间反演对称性和宇称对称性。通常所说的 Lorentz 对称性仅指在 $`SO(1,3)^+`$ 下的不变性。这一区分很重要：Lorentz 对称性的破坏从未被观测到，因此它被视为基本对称性。相反，宇称在弱相互作用中不守恒，这由 Lee 和 Yang 提出，并由 Wu 等人在实验上证实；时间反演对称性同样被破坏。

**O(1,3) 的李代数**

考虑 $`O(1,3)`$ 的单参数子群 $`e^{tX}`$，$`t\in\mathbb R`$。它满足

```math
(e^{tX})^T[\eta]\,e^{tX}=[\eta].
```

把左边展开到 $`t`$ 的一阶，得

```math
(I+tX^T)[\eta](I+tX)+O(t^2)=[\eta]+t\left(X^T[\eta]+[\eta]X\right)+O(t^2),
```

故一阶项必须为零：

```math
X^T[\eta]+[\eta]X=0.
```

因此，

```math
\mathfrak o(1,3):=\{X\in M_4(\mathbb R)\mid X^T[\eta]+[\eta]X=0\}.
```

此外，这一关系可以更明确地写成

```math
[\eta]X=-X^T[\eta]=-([\eta]X)^T,
```

这意味着矩阵 $`[\eta]X`$ 是反对称的。

$`4\times4`$ 反对称矩阵有 $`4\times3/2=6`$ 个独立的实参数。因此 $`X`$ 的一般形式为

```math
X=\begin{pmatrix}
0&b^1&b^2&b^3\\
b^1&0&-\theta^3&\theta^2\\
b^2&\theta^3&0&-\theta^1\\
b^3&-\theta^2&\theta^1&0
\end{pmatrix}
=\sum_i\theta^iJ^i+\sum_ib^iK^i
```

物理中常用如下记号：

```math
e^{-\frac i2\omega^{\mu\nu}J^{\mu\nu}}
```

其中 $`\omega_{\mu\nu}`$ 关于其指标反对称，且

```math
-iJ^{ij}=\epsilon_{ijk}J^k,\qquad -iJ^{0i}=K^i.
```

每个 $`J^{\mu\nu}`$ 只是一个 $`4\times4`$ 矩阵，$`\alpha,\beta`$ 标记其行与列。其矩阵元为

```math
(J^{\mu\nu})_{\alpha\beta}=i\left(\eta^{\mu\alpha}\delta^{\nu\beta}-\eta^{\nu\alpha}\delta^{\mu\beta}\right).
```

具体地（行指标为 $`\alpha`$，列指标为 $`\beta`$；其余分量由 $`J^{\nu\mu}=-J^{\mu\nu}`$ 给出），转动生成元 $`J^{ij}=i\epsilon_{ijk}J^k`$ 是厄米的：

```math
J^{23}=\begin{pmatrix}0&0&0&0\\0&0&0&0\\0&0&0&-i\\0&0&i&0\end{pmatrix},\quad
J^{31}=\begin{pmatrix}0&0&0&0\\0&0&0&i\\0&0&0&0\\0&-i&0&0\end{pmatrix},\quad
J^{12}=\begin{pmatrix}0&0&0&0\\0&0&-i&0\\0&i&0&0\\0&0&0&0\end{pmatrix},
```

而 boost 生成元 $`J^{0i}=iK^i`$ 是反厄米的：

```math
J^{01}=\begin{pmatrix}0&i&0&0\\i&0&0&0\\0&0&0&0\\0&0&0&0\end{pmatrix},\quad
J^{02}=\begin{pmatrix}0&0&i&0\\0&0&0&0\\i&0&0&0\\0&0&0&0\end{pmatrix},\quad
J^{03}=\begin{pmatrix}0&0&0&i\\0&0&0&0\\0&0&0&0\\i&0&0&0\end{pmatrix}.
```


<br><br>

<a id="greens-functions"></a>
### 0.4 格林函数

**定义与积分解**

在下面的一般构造中，$`x,y`$ 表示 $`d`$ 个独立变量。设 $`\mathcal K_x`$ 是 $`\Omega\subseteq\mathbb R^d`$ 上的线性微分算子，$`\mathcal B`$ 规定线性的边界数据或初始数据：

```math
\mathcal K_xu(x)=f(x),\qquad \mathcal Bu=b.
```

假设数据足够正则，且下文的积分都存在。含 $`\delta`$ 函数的方程按分布意义理解。

- **格林函数**：满足该微分方程以及齐次边界条件或齐次初始条件的核，

```math
\boxed{\mathcal K_xG(x,y)=\delta^{(d)}(x-y),\qquad \mathcal B_xG(x,y)=0.}
```

下标 $`x`$ 指明算子作用于哪个变量。边界条件或初始条件的选取是 $`G`$ 的定义的一部分。

- **积分解**：若 $`u_{\mathrm h}`$ 是满足给定数据的齐次方程的解，则

```math
\begin{aligned}
\boxed{u(x)=u_{\mathrm h}(x)+\int_\Omega d^dy\,G(x,y)f(y),}\\
\mathcal K_xu_{\mathrm h}(x)=0,\qquad \mathcal Bu_{\mathrm h}=b.
\end{aligned}
```

事实上，

```math
\begin{aligned}
\mathcal K_xu(x)
&=\int_\Omega d^dy\,[\mathcal K_xG(x,y)]f(y)
=\int_\Omega d^dy\,\delta^{(d)}(x-y)f(y)=f(x),\\
\mathcal Bu&=\mathcal Bu_{\mathrm h}
+\int_\Omega d^dy\,[\mathcal B_xG(x,y)]f(y)=b.
\end{aligned}
```

若 $`\mathcal Ku=0`$、$`\mathcal Bu=0`$ 在所选函数空间中只有零解，则解唯一。存在非平凡零模时，唯一性不成立，且可解性可能要求相容性条件；不能假定对任意源都存在逆。若不给定边界条件或初始条件，满足 (0.41) 第一式的两个核可以相差一个关于 $`x`$ 的齐次方程的解。

**用 Fourier 变换构造**

对 Minkowski 时空上的常系数算子，回到 $`x^\mu=(t,\mathbf x)`$ 和 Fourier 约定 (0.1)。若所选条件还具有平移不变性，则 $`G(x,y)=G(x-y)`$，且

```math
\begin{aligned}
\mathcal K(-ip)\widetilde G(p)&=1,\\
G(x-y)&=\int\frac{d^4p}{(2\pi)^4}\,
e^{-ip\cdot(x-y)}\widetilde G(p),\\
\widetilde G(p)&=\left[\frac{1}{\mathcal K(-ip)}\right]_{\mathrm{prescription}}.
\end{aligned}
```

其中 $`\mathcal K(-ip)`$ 由把每个 $`\partial_\mu`$ 换成 $`-ip_\mu`$ 得到。在 $`\mathcal K(-ip)`$ 的零点处，求倒数需要一个由所选条件确定的分布意义下的处方；仅凭代数方程并不能选定它。

**Poisson 方程与边界数据**

先考虑 $`\mathbb R^3`$ 中光滑且紧支的源：

```math
-\nabla^2u(\mathbf x)=f(\mathbf x),\qquad
u(\mathbf x)\to0\quad\text{当 }|\mathbf x|\to\infty\text{ 时}.
```

对 $`r:=|\mathbf x-\mathbf y|>0`$，在无穷远处为零的转动不变核满足

```math
\nabla^2G_0(r)=\frac{1}{r^2}\frac{d}{dr}\left(r^2\frac{dG_0}{dr}\right)=0
\quad\Longrightarrow\quad G_0(r)=\frac{A}{r}.
```

在以源点为中心的球 $`B_\epsilon`$ 上积分 $`-\nabla^2G_0=\delta^{(3)}`$，可定出 $`A`$：

```math
\begin{aligned}
1&=-\int_{B_\epsilon}d^3x\,\nabla^2G_0
=-4\pi\epsilon^2\left.\frac{dG_0}{dr}\right|_{r=\epsilon}
=4\pi A,\\
G_0(\mathbf x,\mathbf y)&=\frac{1}{4\pi|\mathbf x-\mathbf y|}.
\end{aligned}
```

因此

```math
\boxed{u(\mathbf x)=\int_{\mathbb R^3}d^3y\,
\frac{f(\mathbf y)}{4\pi|\mathbf x-\mathbf y|}.}
```

现在设 $`\Omega\subset\mathbb R^3`$ 有界且边界光滑，并在 $`\partial\Omega`$ 上给定 $`u=b`$。$`-\nabla^2`$ 的 Dirichlet 格林函数关于其两个宗量对称，且满足

```math
\begin{aligned}
-\nabla_{\mathbf y}^2G_D(\mathbf x,\mathbf y)
&=\delta^{(3)}(\mathbf y-\mathbf x),\qquad \mathbf y\in\Omega,\\
G_D(\mathbf x,\mathbf y)&=0,\qquad \mathbf y\in\partial\Omega.
\end{aligned}
```

设 $`\mathbf n_y`$ 为外法向单位矢量，$`\partial_{n_y}:=\mathbf n_y\cdot\nabla_{\mathbf y}`$。格林第二恒等式为

```math
\int_\Omega d^3y\,(v\nabla^2w-w\nabla^2v)
=\int_{\partial\Omega}dS_y\,(v\partial_{n_y}w-w\partial_{n_y}v).
```

在 $`\Omega\setminus B_\epsilon(\mathbf x)`$ 上对 $`v=u`$，$`w=G_D(\mathbf x,\cdot)`$ 应用 (0.50)，再令 $`\epsilon\to0^+`$。对 $`\mathbf x\in\Omega`$，

```math
\boxed{\begin{aligned}
u(\mathbf x)&=\int_\Omega d^3y\,G_D(\mathbf x,\mathbf y)f(\mathbf y)\\
&\quad-\int_{\partial\Omega}dS_y\,b(\mathbf y)\partial_{n_y}G_D(\mathbf x,\mathbf y).
\end{aligned}}
```

第二项给出非零边界数据的贡献。(0.47) 中的自由空间核 $`G_0`$ 一般不满足 (0.49) 中的边界条件。

**Klein–Gordon 方程与初始数据**

取 $`m\geq0`$ 及 mostly-minus 度规，考虑

```math
(\Box+m^2)u(x)=f(x),\qquad
\Box:=\partial_\mu\partial^\mu=\partial_t^2-\nabla^2.
```

- **推迟格林函数**：只在非负时间差上有支集的平移不变核，

```math
(\Box+m^2)G_{\mathrm{ret}}(t,\mathbf x)
=\delta(t)\delta^{(3)}(\mathbf x),\qquad
G_{\mathrm{ret}}(t,\mathbf x)=0\quad(t<0).
```

这里已把源点平移到原点。由于 $`\mathcal K(-ip)=m^2-p^2`$，推迟处方为

```math
\widetilde G_{\mathrm{ret}}(p)
=-\lim_{\epsilon\to0^+}\frac{1}{(p^0+i\epsilon)^2-E_{\mathbf p}^2},\qquad
E_{\mathbf p}:=\sqrt{\mathbf p^2+m^2}.
```

两个极点都位于实 $`p^0`$ 轴下方。$`t>0`$ 时在下半平面闭合围道，$`t<0`$ 时在上半平面闭合围道，得

```math
\boxed{G_{\mathrm{ret}}(t,\mathbf x)
=\theta(t)\int\frac{d^3p}{(2\pi)^3}\,
e^{i\mathbf p\cdot\mathbf x}\frac{\sin(E_{\mathbf p}t)}{E_{\mathbf p}}.}
```

其中 $`\theta(t)`$ 为 Heaviside 函数，$`E_{\mathbf p}=0`$ 处的值按连续性理解。等时极限为

```math
G_{\mathrm{ret}}(0^+,\mathbf x)=0,\qquad
\partial_tG_{\mathrm{ret}}(0^+,\mathbf x)=\delta^{(3)}(\mathbf x).
```

对给定的初始数据 $`u(t_0,\mathbf x)=u_0(\mathbf x)`$ 和 $`\partial_tu(t_0,\mathbf x)=u_1(\mathbf x)`$，由 (0.56) 得，当 $`t>t_0`$ 时，

```math
\boxed{\begin{aligned}
u(t,\mathbf x)
&=\int d^3y\,\bigl[
\partial_tG_{\mathrm{ret}}(t-t_0,\mathbf x-\mathbf y)u_0(\mathbf y)\\
&\hspace{4.5em}+G_{\mathrm{ret}}(t-t_0,\mathbf x-\mathbf y)u_1(\mathbf y)\bigr]\\
&\quad+\int_{t_0}^{t}dt'\int d^3y\,
G_{\mathrm{ret}}(t-t',\mathbf x-\mathbf y)f(t',\mathbf y).
\end{aligned}}
```

当 $`m=0`$ 时，(0.55) 中的空间积分给出波动方程的核。记 $`r:=|\mathbf x|`$，

```math
\begin{aligned}
G_{\mathrm{ret}}(t,\mathbf x)\big|_{m=0}
&=\frac{\theta(t)}{2\pi^2r}\int_0^\infty dp\,\sin(pr)\sin(pt)\\
&=\boxed{\frac{\delta(t-r)}{4\pi r}}.
\end{aligned}
```

若初始数据为零，把 $`f(t',\mathbf y)`$ 在 $`t'<t_0`$ 处延拓为零。于是 (0.57) 化为

```math
\boxed{u(t,\mathbf x)=\int d^3y\,
\frac{f(t-|\mathbf x-\mathbf y|,\mathbf y)}{4\pi|\mathbf x-\mathbf y|}.}
```

为与 (6.12) 中定义的标量费曼传播子比较，在同样的归一化 $`\mathcal KG_F=\delta^{(4)}`$ 下，费曼处方给出

```math
\begin{aligned}
G_F(x-y)&=-\lim_{\varepsilon\to0^+}\int\frac{d^4p}{(2\pi)^4}\,
\frac{e^{-ip\cdot(x-y)}}{p^2-m^2+i\varepsilon}
=i\Delta_F(x-y),\\
(\Box_x+m^2)\Delta_F(x-y)&=-i\delta^{(4)}(x-y).
\end{aligned}
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
\begin{aligned}
C:[t_0,t_f]&\to\mathrm{Conf},\\
t&\mapsto C(t),
\end{aligned}
```

速度为 $`\dot C(t):=dC/dt`$。

- **动力学结构**：拉氏量，即光滑函数

```math
\begin{aligned}
L:\mathbb R^n\times\mathbb R^n\times\mathbb R&\to\mathbb R,\\
(x,y,t)&\mapsto L(x,y,t).
\end{aligned}
```

- **作用量**：路径上的泛函

```math
\boxed{
\begin{aligned}
S:\{\text{路径}\}&\to\mathbb R,\\
C&\mapsto S[C]:=\int_{t_0}^{t_f}dt\,L\bigl(C(t),\dot C(t),t\bigr).
\end{aligned}}
```

- **解**：在端点固定的变分下使 $`S`$ 取驻值的路径 $`\bar C`$，

```math
\frac{d}{ds}S[\bar C+s\eta]\Big|_{s=0}=0,
```

对任意满足 $`\eta(t_0)=\eta(t_f)=0`$ 的光滑 $`\eta:[t_0,t_f]\to\mathbb R^n`$ 成立。

**Euler–Lagrange 方程**

将 $`L`$ 在 $`\bigl(C(t),\dot C(t),t\bigr)`$ 处取值的偏导数记为 $`\frac{\partial L}{\partial x_a}\big|_C`$ 和 $`\frac{\partial L}{\partial y_a}\big|_C`$。

与通常使用的 $`q_a,\dot q_a`$ 记号的对应关系为

```math
\begin{aligned}
\frac{\partial L}{\partial \dot q_a}&=\frac{\partial L}{\partial y_a}\Big|_C,\\
\frac{\partial L}{\partial q_a}&=\frac{\partial L}{\partial x_a}\Big|_C.
\end{aligned}
```

则

```math
\begin{aligned}
\frac{d}{ds}S[C+s\eta]\Big|_{s=0}
&=\int_{t_0}^{t_f}dt\sum_{a=1}^n\Bigl(\frac{\partial L}{\partial x_a}\Big|_C\,\eta_a+\frac{\partial L}{\partial y_a}\Big|_C\,\dot\eta_a\Bigr)\\
&=\int_{t_0}^{t_f}dt\sum_{a=1}^n\biggl[\frac{\partial L}{\partial x_a}\Big|_C-\frac{d}{dt}\Bigl(\frac{\partial L}{\partial y_a}\Big|_C\Bigr)\biggr]\eta_a\\
&\quad+\biggl[\sum_{a=1}^n\frac{\partial L}{\partial y_a}\Big|_C\,\eta_a\biggr]_{t_0}^{t_f}.
\end{aligned}
```

由于 $`\eta(t_0)=\eta(t_f)=0`$，边界项为零。

由于 $`\eta`$ 任意，解为满足下式的路径 $`\bar C`$：

```math
\boxed{\frac{d}{dt}\Bigl(\frac{\partial L}{\partial y_a}\Big|_{\bar C}\Bigr)-\frac{\partial L}{\partial x_a}\Big|_{\bar C}=0,\qquad a=1,\ldots,n.}
```

<br><br>

<a id="lagrangian-symmetry"></a>
#### 对称变换与 Noether 定理

**变换**

- **内部变换**：
微分同胚的单参数族 $`\phi_\lambda:\mathrm{Conf}\to\mathrm{Conf}`$，$`\lambda\in\mathbb R`$，其中 $`(\lambda,q)\mapsto\phi_\lambda(q)`$ 光滑且 $`\phi_0=\mathrm{id}`$，它逐点作用于路径，

```math
\begin{aligned}
\Phi:\mathbb R\times\{\text{路径}\}&\to\{\text{路径}\},\\
(\lambda,C)&\mapsto\Phi_\lambda C:=\phi_\lambda\circ C,
\end{aligned}
```

切矢或者说速度之间的关系为

```math
\frac{d}{dt}(\Phi_\lambda C)_a(t)=\sum_{b=1}^n\frac{\partial(\phi_\lambda)_a}{\partial q_b}\bigl(C(t)\bigr)\,\dot C_b(t),
```

其中 $`(\phi_\lambda)_a(q)`$ 是 $`\phi_\lambda(q)`$ 的第 $`a`$ 个坐标。

把矩阵元为 $`\frac{\partial(\phi_\lambda)_a}{\partial q_b}(q)`$ 的 Jacobi 矩阵记为 $`\frac{\partial\phi_\lambda}{\partial q}(q)`$，于是 $`\Phi_\lambda C`$ 的速度为
```math
\frac{d}{dt}(\Phi_\lambda C)(t)=\frac{\partial\phi_\lambda}{\partial q}\bigl(C(t)\bigr)\,\dot C(t)
```

- **时间平移**：路径在时间上的平移，

```math
\begin{aligned}
\Theta:\mathbb R\times\{\text{路径}\}&\to\{\text{路径}\},\\
(\tau,C)&\mapsto\Theta_\tau C:=C(\cdot-\tau),
\end{aligned}
```

于是 $`\Theta_\tau C:[t_0+\tau,t_f+\tau]\to\mathrm{Conf}`$，$`t\mapsto C(t-\tau)`$，其速度为

```math
\frac{d}{dt}(\Theta_\tau C)(t)=\dot C(t-\tau).
```

**对称变换**

- **对称变换**：使每条路径的作用量都不变的内部变换 $`\Phi`$ 或时间平移 $`\Theta`$，即分别满足：

```math
\boxed{
\begin{aligned}
S[\Phi_\lambda C]&=S[C]\quad\text{对任意路径 }C\text{ 及任意 }\lambda\in\mathbb R,\\
S[\Theta_\tau C]&=S[C]\quad\text{对任意路径 }C\text{ 及任意 }\tau\in\mathbb R.
\end{aligned}}
```


把变换后的路径代入作用量，并在第二种情形中作平移 $`t\to t+\tau`$，

```math
\begin{aligned}
S[\Phi_\lambda C]&=\int_{t_0}^{t_f}dt\,L\Bigl(\phi_\lambda\bigl(C(t)\bigr),\ \frac{\partial\phi_\lambda}{\partial q}\bigl(C(t)\bigr)\,\dot C(t),\ t\Bigr),\\
S[\Theta_\tau C]&=\int_{t_0+\tau}^{t_f+\tau}dt\,L\bigl(C(t-\tau),\dot C(t-\tau),t\bigr)=\int_{t_0}^{t_f}dt\,L\bigl(C(t),\dot C(t),t+\tau\bigr).
\end{aligned}
```

因此，对称变换的等价定义如下：

$`\Phi`$ 或 $`\Theta`$ 是对称变换，当且仅当对所有 $`(x,y,t)\in\mathrm{Conf}\times\mathbb R^n\times\mathbb R`$ 以及所有 $`\lambda`$ 或所有 $`\tau`$，分别有：

```math
\boxed{
\begin{aligned}
L\Bigl(\phi_\lambda(x),\ \frac{\partial\phi_\lambda}{\partial q}(x)\,y,\ t\Bigr)&=L(x,y,t)
\end{aligned}}
```

```math
\boxed{
L(x,y,t+\tau)=L(x,y,t)\quad(\forall\,\tau\in\mathbb R)
\quad\Longleftrightarrow\quad
\frac{\partial L}{\partial t}(x,y,t)=0.
}
```


**守恒量**

- **守恒量**：光滑函数

```math
\begin{aligned}
\mathcal Q:\mathrm{Conf}\times\mathbb R^n\times\mathbb R&\to\mathbb R,\\
(x,y,t)&\mapsto\mathcal Q(x,y,t),
\end{aligned}
```

使得对每个解 $`\bar C`$，$`\mathcal Q\bigl(\bar C(t),\dot{\bar C}(t),t\bigr)`$ 都与 $`t`$ 无关。

**Noether 定理**

**(A) 时间平移**

若 $`\Theta`$ 是对称变换，即在 $`\mathrm{Conf}\times\mathbb R^n\times\mathbb R`$ 上 $`\partial L/\partial t=0`$，则能量

```math
\boxed{E(x,y,t):=\sum_{a=1}^n\frac{\partial L}{\partial y_a}(x,y,t)\,y_a-L(x,y,t)}
```

是守恒量。

**(B) 内部变换**

若 $`\Phi`$ 是对称变换，则对于生成元

```math
\begin{aligned}
X:\mathrm{Conf}&\to\mathbb R^n,\\
q&\mapsto\frac{\partial\phi_\lambda(q)}{\partial\lambda}\Big|_{\lambda=0},
\end{aligned}
```

生成元给出 $`\lambda=0`$ 处无穷小变换的形式：$`\phi_\lambda(q)=q+\lambda\,X(q)+O(\lambda^2),`$ 即坐标按 $`q_a\mapsto q_a+\lambda X_a(q)`$ 变换。

相应地，速度的变换为 $`y\mapsto y+\lambda\,\frac{\partial X}{\partial q}(q)\,y+O(\lambda^2),`$ 即 $`y_a\mapsto y_a+\lambda\sum_b\frac{\partial X_a}{\partial q_b}(q)\,y_b`$。

函数

```math
\boxed{\mathcal Q(x,y,t):=\sum_{a=1}^n\frac{\partial L}{\partial y_a}(x,y,t)\,X_a(x)}
```

是守恒量。

**证明**

(A) 设 $`\bar C`$ 是解。记 $`L|_{\bar C}:=L\bigl(\bar C(t),\dot{\bar C}(t),t\bigr)`$。

 由链式法则和 Euler–Lagrange 方程，

```math
\frac{d}{dt}E\bigl(\bar C(t),\dot{\bar C}(t),t\bigr)
=\frac{d}{dt}\Bigl(\sum_{a=1}^n\frac{\partial L}{\partial y_a}\Big|_{\bar C}\,\dot{\bar C}_a(t)-L\big|_{\bar C}\Bigr)
=-\frac{\partial L}{\partial t}\Big|_{\bar C}
```

这对每个解都成立；若 $`\partial L/\partial t=0`$，则此式为零。

(B) 将第一个对称性条件在 $`\lambda=0`$ 处对 $`\lambda`$ 求导，得到：对所有 $`(x,y,t)\in\mathrm{Conf}\times\mathbb R^n\times\mathbb R`$，

```math
\sum_{a=1}^n\Bigl(\frac{\partial L}{\partial x_a}\,X_a(x)
+\frac{\partial L}{\partial y_a}\sum_{b=1}^n\frac{\partial X_a}{\partial q_b}(x)\,y_b\Bigr)=0,
```

其中 $`L`$ 的偏导数在 $`(x,y,t)`$ 处取值。

对解 $`\bar C`$，由链式法则和 Euler–Lagrange 方程得

```math
\frac{d}{dt}\mathcal Q\bigl(\bar C(t),\dot{\bar C}(t),t\bigr)
=\sum_{a=1}^n\Bigl(\frac{\partial L}{\partial x_a}\Big|_{\bar C}\,X_a\bigl(\bar C(t)\bigr)
+\frac{\partial L}{\partial y_a}\Big|_{\bar C}\sum_{b=1}^n\frac{\partial X_a}{\partial q_b}\bigl(\bar C(t)\bigr)\,\dot{\bar C}_b(t)\Bigr),
```

这正是上述恒等式在 $`\bigl(\bar C(t),\dot{\bar C}(t),t\bigr)`$ 处的取值，因此为零。$`\square`$


**动量**

固定 $`b\in\{1,\ldots,n\}`$，平移第 $`b`$ 个坐标，

```math
\bigl(\phi_\lambda(q)\bigr)_a=q_a+\lambda\,\delta_{ab}.
```

Jacobi 矩阵 $`\partial\phi_\lambda/\partial q`$ 为单位矩阵，故速度不变，对称性条件化为：对所有 $`\lambda`$，$`L(\phi_\lambda(x),y,t)=L(x,y,t)`$，即 $`\partial L/\partial x_b=0`$。

生成元：$`X_a(q)=\delta_{ab}`$。

守恒量：

```math
\mathcal Q(x,y,t)=\sum_{a=1}^n\frac{\partial L}{\partial y_a}(x,y,t)\,\delta_{ab}=\frac{\partial L}{\partial y_b}(x,y,t),
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
\begin{aligned}
F:M&\to\mathbb R^N,\\
z&\mapsto F(z).
\end{aligned}
```

- **解**：光滑曲线 $`C:I\to M`$，其中 $`I\subset\mathbb R`$ 是开区间，满足

```math
\boxed{\dot C_A(t)=F_A\bigl(C(t)\bigr),\qquad A=1,\ldots,N.}
```

**(1) 确定性**

由于 $`F`$ 光滑，对每个 $`t_0\in\mathbb R`$ 和 $`z^{(0)}\in M`$，存在唯一的满足 $`C(t_0)=z^{(0)}`$ 的极大解 $`C`$。因此，某一时刻的状态决定了该解在其区间上所有更晚和更早时刻的状态，且 $`M`$ 的每一点恰有一条解曲线经过。

假设每个极大解都定义在整个 $`\mathbb R`$ 上。$`F`$ 的流为

```math
\begin{aligned}
\Phi_t:M&\to M,\\
z^{(0)}&\mapsto C(t),
\end{aligned}
```

其中 $`C`$ 是满足 $`C(0)=z^{(0)}`$ 的解。它满足

- $`\partial_t\Phi_t(z)=F\bigl(\Phi_t(z)\bigr)`$ 且 $`\Phi_0=\mathrm{id}`$；
- $`\Phi_t\circ\Phi_s=\Phi_{t+s}`$（因为 $`F`$ 不依赖于 $`t`$），故每个 $`\Phi_t`$ 都是微分同胚，其逆为 $`\Phi_{-t}`$。

**(2) 状态空间中的体积**

对区域 $`D\subset M`$，记 $`\mathrm{vol}(D):=\int_Dd^Nz`$，并把 $`\Phi_t`$ 的 Jacobi 矩阵记为 $`J_t:=\frac{\partial\Phi_t}{\partial z}`$。把 $`\partial_t\Phi_t=F\circ\Phi_t`$ 对 $`z`$ 求导，并利用 Jacobi 公式 $`d\det J=\det J\,\mathop{\rm tr}\nolimits (J^{-1}dJ)`$，得：

```math
\begin{aligned}
\partial_tJ_t&=\Bigl(\frac{\partial F}{\partial z}\circ\Phi_t\Bigr)J_t,
\qquad
\partial_t\det J_t=\Bigl(\sum_{A=1}^N\frac{\partial F_A}{\partial z_A}\circ\Phi_t\Bigr)\det J_t,\\
\frac{d}{dt}\mathrm{vol}\bigl(\Phi_t(D)\bigr)
&=\frac{d}{dt}\int_Dd^Nz\,\det J_t
=\int_{\Phi_t(D)}d^Nz\,\sum_{A=1}^N\frac{\partial F_A}{\partial z_A}.
\end{aligned}
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
\begin{aligned}
f:M&\to\mathbb R,\\
z&\mapsto f(z).
\end{aligned}
```

- **动力学结构**：
  - (1.81) 中的 Poisson 括号 $`\{\ ,\ \}_{\mathrm{PB}}`$；
  - 哈密顿量，即光滑函数

```math
\begin{aligned}
H:M&\to\mathbb R,\\
z&\mapsto H(z),
\end{aligned}
```

且不显含时间。

- **解**：光滑曲线 $`C:I\to M`$，其中 $`I\subset\mathbb R`$ 是开区间，满足

```math
\frac{d}{dt}q_a\bigl(C(t)\bigr)=\frac{\partial H}{\partial p_a}\bigl(C(t)\bigr),\quad
\frac{d}{dt}p_a\bigl(C(t)\bigr)=-\frac{\partial H}{\partial q_a}\bigl(C(t)\bigr)
\qquad\Longleftrightarrow\qquad
\frac{d}{dt}f\bigl(C(t)\bigr)=\{f,H\}_{\mathrm{PB}}\bigl(C(t)\bigr)\quad\text{对所有 }f.
```

<br><br>

<a id="hamiltonian-symmetry"></a>
#### 对称性与 Noether 定理

**变换**

- **变换**：不显含时间的微分同胚，

```math
\begin{aligned}
\phi:M&\to M,\\
z&\mapsto\phi(z),
\end{aligned}
\qquad
Q_a:=q_a\circ\phi,\quad P_a:=p_a\circ\phi,\quad \phi_*f:=f\circ\phi^{-1},
```

其中 $`Q_a(z),P_a(z)`$ 是 $`\phi(z)`$ 的坐标，$`\phi_*`$ 是 (1.58) 中的推前，满足 $`(\phi_*f)(\phi(z))=f(z)`$。

**对称变换**

- **对称变换**：同时保持 Poisson 括号和哈密顿量不变的变换 $`\phi`$，

```math
\boxed{
\begin{aligned}
&\text{(i)}\quad\{f\circ\phi,\,g\circ\phi\}_{\mathrm{PB}}=\{f,g\}_{\mathrm{PB}}\circ\phi\quad\text{对所有 }f,g,\\
&\text{(ii)}\quad H\circ\phi=H.
\end{aligned}}
```

满足 (i) 的变换称为正则变换。把 $`f,g`$ 换成 $`f\circ\phi^{-1},g\circ\phi^{-1}`$ 可知，(i) 等价于 $`\{\phi_*f,\phi_*g\}_{\mathrm{PB}}=\phi_*\{f,g\}_{\mathrm{PB}}`$；(ii) 等价于 $`\phi_*H=H`$，即对所有 $`z\in M`$ 有 $`H(\phi(z))=H(z)`$。

把全部相空间坐标记为 $`z_A`$，$`A=1,\ldots,2n`$，并记 $`Z_A:=z_A\circ\phi`$。由链式法则，

```math
\begin{aligned}
\{f\circ\phi,\,g\circ\phi\}_{\mathrm{PB}}
&=\sum_{A,B}\Bigl(\frac{\partial f}{\partial z_A}\circ\phi\Bigr)\Bigl(\frac{\partial g}{\partial z_B}\circ\phi\Bigr)\{Z_A,Z_B\}_{\mathrm{PB}},\\
\{f,g\}_{\mathrm{PB}}\circ\phi
&=\sum_{A,B}\Bigl(\frac{\partial f}{\partial z_A}\circ\phi\Bigr)\Bigl(\frac{\partial g}{\partial z_B}\circ\phi\Bigr)\{z_A,z_B\}_{\mathrm{PB}}.
\end{aligned}
```

括号 $`\{z_A,z_B\}_{\mathrm{PB}}`$ 都是常数，而取 $`f=z_A`$，$`g=z_B`$ 只挑出一项，故 (i) 成立当且仅当 $`\{Z_A,Z_B\}_{\mathrm{PB}}=\{z_A,z_B\}_{\mathrm{PB}}`$。由 (1.81)，(i) 等价于

```math
\boxed{
\{Q_a,Q_b\}_{\mathrm{PB}}=\{P_a,P_b\}_{\mathrm{PB}}=0,\qquad
\{Q_a,P_b\}_{\mathrm{PB}}=\delta_{ab}.}
```

对称变换把解映为解。设 $`C`$ 是解，$`C':=\phi\circ C`$。先对 $`f\circ\phi`$ 应用 (1.25)，再利用 (ii) 和 (i)，

```math
\begin{aligned}
\frac{d}{dt}f\bigl(C'(t)\bigr)
&=\{f\circ\phi,\,H\}_{\mathrm{PB}}\bigl(C(t)\bigr)\\
&=\{f\circ\phi,\,H\circ\phi\}_{\mathrm{PB}}\bigl(C(t)\bigr)
=\{f,H\}_{\mathrm{PB}}\bigl(C'(t)\bigr)
\end{aligned}
```

对每个 $`f`$ 成立，故由 (1.25)，$`C'`$ 是解。

**守恒量**

- **守恒量**：可观测量 $`f`$，使得对每个解 $`C`$，$`f\bigl(C(t)\bigr)`$ 都与 $`t`$ 无关。

(1.25) 即 (1.20) 取 $`N=2n`$、$`F_A=\{z_A,H\}_{\mathrm{PB}}`$ 的情形。由于 $`M`$ 的每一点都有解经过，由 (1.25) 可知，$`f`$ 是守恒量当且仅当

```math
\boxed{\{f,H\}_{\mathrm{PB}}=0.}
```

**Noether 定理**

设 $`\phi_\lambda`$，$`\lambda\in\mathbb R`$，为对称变换的单参数子群：

- 对所有 $`\lambda,\mu\in\mathbb R`$，$`\phi_\lambda\circ\phi_\mu=\phi_{\lambda+\mu}`$；特别地，$`\phi_0=\mathrm{id}`$；
- $`(\lambda,z)\mapsto\phi_\lambda(z)`$ 光滑。

定义生成元

```math
\begin{aligned}
X:M&\to\mathbb R^{2n},\\
z&\mapsto\frac{\partial\phi_\lambda(z)}{\partial\lambda}\Big|_{\lambda=0},
\end{aligned}
```

于是 $`\phi_\lambda`$ 是 $`X`$ 的流。若 $`M`$ 单连通，则存在光滑函数 $`G:M\to\mathbb R`$（在相差一个可加常数的意义下唯一），满足

```math
X_A=\{z_A,G\}_{\mathrm{PB}},\qquad A=1,\ldots,2n,
```

并且

```math
\boxed{\{G,H\}_{\mathrm{PB}}=0,}
```

故 $`G`$ 是守恒量。

**证明**

记 $`\omega_{AB}:=\{z_A,z_B\}_{\mathrm{PB}}`$。由 (1.81)，它是常数且可逆，并且 $`\{f,g\}_{\mathrm{PB}}=\sum_{A,B}\omega_{AB}\frac{\partial f}{\partial z_A}\frac{\partial g}{\partial z_B}`$。用 $`X_A=\sum_B\omega_{AB}Y_B`$ 定义 $`Y`$。在 (i) 中取 $`f=z_A`$，$`g=z_B`$，再将它与 (ii) 一起在 $`\lambda=0`$ 处对 $`\lambda`$ 求导：

```math
\begin{aligned}
0&=\{X_A,z_B\}_{\mathrm{PB}}+\{z_A,X_B\}_{\mathrm{PB}}
=\sum_{C,D}\omega_{AC}\,\omega_{BD}\Bigl(\frac{\partial Y_D}{\partial z_C}-\frac{\partial Y_C}{\partial z_D}\Bigr),\\
0&=\sum_A\frac{\partial H}{\partial z_A}\,X_A.
\end{aligned}
```

由于 $`\omega`$ 可逆，$`\partial Y_D/\partial z_C=\partial Y_C/\partial z_D`$。在单连通的 $`M`$ 上，由此得 $`Y_B=\partial G/\partial z_B`$，其中 $`G`$ 光滑，且在相差一个常数的意义下唯一，即 (1.33)。于是 (1.35) 的第二行为 $`\sum_A\frac{\partial H}{\partial z_A}\{z_A,G\}_{\mathrm{PB}}=\{H,G\}_{\mathrm{PB}}=0`$，即 (1.34)。$`\square`$

**(1) 时间演化与能量**

在 (1.31) 中取 $`f=H`$，有 $`\{H,H\}_{\mathrm{PB}}=0`$，故 $`H`$ 是守恒量。取 $`G=H`$，由 (1.33) 得 $`X_A=\{z_A,H\}_{\mathrm{PB}}=F_A`$，故 $`H`$ 生成的子群就是 (1.21) 的时间演化 $`\Phi_t`$。

**(2) 平移与动量**

设 $`M=\mathbb R^{2n}`$，固定 $`k\in\mathbb R^n`$。取 $`\phi_\lambda(q,p)=(q+\lambda k,\,p)`$。则 $`Q_a=q_a+\lambda k_a`$ 与 $`P_a=p_a`$ 满足 (1.29)，且 $`\phi_\lambda`$ 是对称变换当且仅当对所有 $`\lambda`$ 有 $`H(q+\lambda k,p)=H(q,p)`$，即 $`\sum_ak_a\,\partial H/\partial q_a=0`$。此时 $`X=(k,0)`$，(1.33) 在取下式时成立：

```math
\boxed{G=\sum_{a=1}^nk_a\,p_a,}
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
\text{场}:\text{时空}\longrightarrow\text{向量空间},
```

```math
\boxed{\Psi:\mathbb R^4\longrightarrow\mathbb R^n\ \text{或}\ \mathbb C^n
}
```

还可以附加正则性条件，例如 $`C^\infty`$ 光滑性。

场的空间 $`\{\Psi\}`$ 承载 $`ISO(1,3)^+`$ 的一个表示。对 $`(\Lambda,a)\in ISO(1,3)^+`$，

```math
\Psi\xrightarrow{\;(\Lambda,a)\;}U(\Lambda,a)\Psi,
```

其中 $`U`$ 是无穷维表示，可由有限维表示 $`D(\Lambda)`$ 构造：

```math
\boxed{
\begin{aligned}
[U(\Lambda,a)\Psi]_\alpha(x)
&:=D_{\alpha\beta}(\Lambda)
[(\Lambda,a)_*\Psi]_\beta(x)\\
&=D_{\alpha\beta}(\Lambda)
\Psi_\beta(\Lambda^{-1}x-\Lambda^{-1}a).
\end{aligned}
}
```

<br><br>

<a id="lorentz-finite-representations"></a>
#### $`SO(1,3)^+`$ 的有限维表示

$`U`$ 由 $`D`$ 按 (1.40) 构造，而 $`D`$ 可通过 $`[U(\Lambda,0)\Psi](0)=D(\Lambda)\Psi(0)`$ 从 $`U`$ 还原。因此

```math
\begin{aligned}
\Psi_\alpha(x),\ \alpha=1,\ldots,n
&\quad\Longleftrightarrow\quad\text{无穷维表示 }U(\Lambda,a)\\
&\quad\Longleftrightarrow\quad SO(1,3)^+\text{ 的 }n\text{ 维表示 }D(\Lambda).
\end{aligned}
```

**李代数表示**

对 $`X,Y\in\mathfrak o(1,3)`$，

```math
\rho(X):=\frac{d}{dt}D(e^{tX})\Big|_{t=0},\qquad
D(e^{X})=e^{\rho(X)},\qquad
\rho([X,Y])=[\rho(X),\rho(Y)].
```

$`SO(1,3)^+`$ 连通，故 $`D`$ 由 $`\rho`$ 决定。把 $`\rho`$ 按 $`\rho(X+iY):=\rho(X)+i\rho(Y)`$ 复线性地延拓到复化李代数 $`\mathfrak o(1,3)_{\mathbb C}`$，后者由把 (0.32) 中的 $`M_4(\mathbb R)`$ 换成 $`M_4(\mathbb C)`$ 来定义。由 (0.36)，$`\mathfrak o(1,3)_{\mathbb C}`$ 包含所有 $`J^{\mu\nu}`$，且 $`D(e^{-\frac i2\omega_{\mu\nu}J^{\mu\nu}})=e^{-\frac i2\omega_{\mu\nu}\rho(J^{\mu\nu})}`$。对 Dirac 场，$`\rho(J^{\mu\nu})=S^{\mu\nu}`$ (1.100)。

**$`\mathfrak o(1,3)_{\mathbb C}`$ 的分解**

由 (0.34)，

```math
[J^i,J^j]=\epsilon_{ijk}J^k,\qquad
[J^i,K^j]=\epsilon_{ijk}K^k,\qquad
[K^i,K^j]=-\epsilon_{ijk}J^k.
```

定义

```math
\begin{aligned}
A^i&:=\frac12\Bigl(\frac12\epsilon_{ijk}J^{jk}+iJ^{0i}\Bigr)=\frac i2\bigl(J^i+iK^i\bigr),\\
B^i&:=\frac12\Bigl(\frac12\epsilon_{ijk}J^{jk}-iJ^{0i}\Bigr)=\frac i2\bigl(J^i-iK^i\bigr),
\end{aligned}
```

即 $`A^1=\frac12(J^{23}+iJ^{01})`$，$`A^2=\frac12(J^{31}+iJ^{02})`$，$`A^3=\frac12(J^{12}+iJ^{03})`$，$`B^i`$ 的表达式与此相同，只需作替换 $`iJ^{0i}\to-iJ^{0i}`$。$`A^i`$ 和 $`B^i`$ 不是实的，因此属于 $`\mathfrak o(1,3)_{\mathbb C}`$ 而不属于 $`\mathfrak o(1,3)`$。由 (1.43)，

```math
\boxed{[A^i,A^j]=i\epsilon_{ijk}A^k,\qquad
[B^i,B^j]=i\epsilon_{ijk}B^k,\qquad
[A^i,B^j]=0.}
```

因此

```math
\mathfrak o(1,3)_{\mathbb C}=\mathfrak g_A\oplus\mathfrak g_B,\qquad
\mathfrak g_A:=\mathop{\rm span}\nolimits\,_{\mathbb C}\{A^1,A^2,A^3\},\quad
\mathfrak g_B:=\mathop{\rm span}\nolimits\,_{\mathbb C}\{B^1,B^2,B^3\}.
```

映射 $`A^i\mapsto\sigma^i/2`$ 和 $`B^i\mapsto\sigma^i/2`$ 分别把 $`\mathfrak g_A`$ 和 $`\mathfrak g_B`$ 等同于 $`\mathfrak{su}(2)\cong\mathfrak o(3)`$ 的复化。

**不可约表示**

取 $`\mathfrak g_A`$ 的表示 $`(\rho_A,V_A)`$ 和 $`\mathfrak g_B`$ 的表示 $`(\rho_B,V_B)`$，记 $`n_A:=\dim V_A`$，$`n_B:=\dim V_B`$。对 $`v_A\in\mathfrak g_A`$ 和 $`v_B\in\mathfrak g_B`$，二者的张量积（Kronecker 积）$`(\rho,V_A\otimes V_B)`$ 为：

```math
\begin{aligned}
\rho(v_A+v_B)&:=\rho_A(v_A)\otimes I_{n_B}+I_{n_A}\otimes\rho_B(v_B),\\
\rho(v_A+v_B)\bigl(|a\rangle\otimes|b\rangle\bigr)&=\rho_A(v_A)|a\rangle\otimes|b\rangle+|a\rangle\otimes\rho_B(v_B)|b\rangle,\\
e^{\rho(v_A+v_B)}&=e^{\rho_A(v_A)}\otimes e^{\rho_B(v_B)}.
\end{aligned}
```

最后一行成立，是因为第一行中的两项对易。

$`\mathfrak{su}(2)`$ 的不可约表示为 $`V_j`$，其基为 $`|j,m\rangle`$，$`m=-j,\ldots,j`$，$`\rho_A(A^3)`$（或 $`\rho_B(B^3)`$）在其上的作用是乘以 $`m`$。这里 $`j=0,\frac12,1,\ldots`$，$`\dim V_j=2j+1`$。$`\mathfrak g_A\oplus\mathfrak g_B`$ 的每个有限维不可约表示都是 $`V_{j_1}\otimes V_{j_2}`$，而每个有限维表示都是它们的直和：

```math
\boxed{(j_1,j_2),\qquad j_1,j_2\in\{0,\tfrac12,1,\tfrac32,\ldots\},\qquad\dim=(2j_1+1)(2j_2+1).}
```

**转动 $`2\pi`$**

由 (1.44)，$`A^3+B^3=iJ^3`$，故在 $`(j_1,j_2)`$ 上

```math
e^{2\pi J^3}=I_4,\qquad
e^{2\pi\rho(J^3)}=e^{-2\pi i\rho(A^3+B^3)}=(-1)^{2(j_1+j_2)}I_n.
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
\begin{aligned}
\mathcal L:(\mathbb R^n\ \text{或}\ \mathbb C^n)\times(\mathbb R^n\ \text{或}\ \mathbb C^n)^4&\to\mathbb R,\\
(\Psi_\alpha,\partial_\mu\Psi_\alpha)&\mapsto\mathcal L(\Psi_\alpha,\partial_\mu\Psi_\alpha),
\end{aligned}
```

其中 $`\partial_\mu\Psi_\alpha`$ 视为独立变量，且不显含 $`x`$。

- **作用量**：场上的泛函，对任意有界区域 $`\Omega\subset\mathbb R^4`$，

```math
\boxed{S[\Psi]:=\int_\Omega d^4x\,\mathcal L\bigl(\Psi_\alpha(x),\partial_\mu\Psi_\alpha(x)\bigr).}
```

- **解**：在 $`\partial\Omega`$ 上为零的变分下使 $`S`$ 取驻值的场 $`\Psi`$，

```math
\frac{d}{ds}S[\Psi+s\eta]\Big|_{s=0}=0,
```

对每个满足 $`\eta|_{\partial\Omega}=0`$ 的光滑 $`\eta`$ 及每个 $`\Omega`$ 成立。

**对拉氏量密度的要求**

对这里考虑的局域相对论性场论，我们要求：

- **Lorentz 不变性**：由 $`\mathcal L`$ 构造的作用量是 Lorentz 标量。
- **实性**：拉氏量密度 $`\mathcal L`$ 是实的。
- **局域性**：$`\mathcal L`$ 只依赖于同一时空点处的场及其有限个导数。

还可以附加更多数学上的限制，但它们是约定性的选择，而非普适公理；归根结底，本质要求是与物理实在相符，使拉氏量至少能描述或解释现实世界的一部分。




**Euler–Lagrange 方程**

与 (1.5) 同理，对 (1.52) 分部积分并利用 $`\eta|_{\partial\Omega}=0`$，可知 $`\Psi`$ 是解当且仅当

```math
\boxed{\partial_\mu\frac{\partial\mathcal L}{\partial(\partial_\mu\Psi_\alpha)}
-\frac{\partial\mathcal L}{\partial\Psi_\alpha}=0.}
```

**哈密顿表述**

对于正规的 Legendre 变换，

```math
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
```

<br><br>

<a id="classical-noether"></a>
#### 对称变换与 Noether 定理

**变换**

- **变换**：满足 $`\phi_0=\mathrm{id}`$ 的单参数族 $`\phi_\lambda`$，既作用于时空，也作用于场，

```math
\begin{aligned}
\phi_\lambda:\mathbb R^4&\to\mathbb R^4,\\
x&\mapsto x'=\phi_\lambda(x),
\end{aligned}
\qquad
x'^\mu=:x^\mu+\delta x^\mu,\qquad
\Psi\mapsto\Psi',
```

其中 $`\Psi'`$ 的形式由 (1.58) 和 (1.66) 给出：若 $`\phi_\lambda=(\Lambda,a)`$ 是 Poincaré 变换，则有 (1.40) 的 $`\Psi'=U(\Lambda,a)\Psi`$；若为内部变换，则 $`x'=x`$，$`\Psi'=g(\lambda)\Psi`$。

**对称变换**

- **对称变换**：对每个区域都使每个场的作用量保持不变的变换，

```math
\boxed{S'=S\quad\text{对任意 }\Psi\text{ 及任意 }\Omega,}
```

其中 $`S'`$ 是 $`\Psi'`$ 在 $`\phi_\lambda(\Omega)`$ 上的作用量，其显式表达式见 (1.60)。

**守恒量**

- **守恒量**：时间切片 $`t`$ 上场及其导数的泛函 $`\mathcal Q[\Psi,t]`$，使得对每个连同其一阶导数在空间无穷远处衰减得足够快的解 $`\Psi`$，$`\mathcal Q[\Psi,t]`$ 都与 $`t`$ 无关。

**Noether 定理**

若 $`\phi_\lambda`$ 是对称变换，则

```math
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
```

是守恒量，其中 $`\delta_0\Psi_\alpha`$ 的定义见 (1.58)，对 $`\lambda`$ 的导数在 $`\lambda=0`$ 处取值，衰减条件保证积分收敛并使 (1.64) 中的表面项为零。

**证明**

**(A) 坐标变换**

设 $`x'=\phi_\lambda(x)`$，其中 $`\lambda`$ 为无穷小。定义两种场变分：

```math
\begin{aligned}
\delta_0\Psi_\alpha(x)
&:=\Psi'_\alpha(x')-\Psi_\alpha(x)
=D_{\alpha\beta}(\Lambda)\Psi_\beta(x)-\Psi_\alpha(x),\\
\delta\Psi_\alpha(x)
&:=\Psi'_\alpha(x)-\Psi_\alpha(x)
=[U(\Lambda,a)\Psi]_\alpha(x)-\Psi_\alpha(x).
\end{aligned}
```

这里 $`\Psi'`$ 是变换后的场。利用推前 $`(\phi_\lambda)_*\Psi:=\Psi\circ\phi_\lambda^{-1}`$，可写出 $`\Psi'_\alpha=D_{\alpha\beta}(\Lambda)\,[(\phi_\lambda)_*\Psi]_\beta`$。在 $`x'`$ 处取值得 $`\Psi'_\alpha(x')=D_{\alpha\beta}(\Lambda)\Psi_\beta(x)`$，这就是第一行的最后一个等号，因此第一种变分 $`\delta_0\Psi_\alpha`$ 描述的是场本身的变换。对 $`\phi_\lambda=(\Lambda,a)`$，由 (1.40) 有 $`\Psi'=U(\Lambda,a)\Psi`$，这就是第二行的最后一个等号。若 $`\phi_\lambda`$ 不是 Poincaré 变换，则 $`D(\Lambda)`$ 换成单位矩阵，且 $`\delta_0\Psi_\alpha=0`$。

准确到 $`\lambda`$ 的一阶，两种变分的关系为

```math
\begin{aligned}
\delta\Psi_\alpha(x)
&=\bigl[\Psi'_\alpha(x')-\Psi_\alpha(x)\bigr]
-\bigl[\Psi'_\alpha(x')-\Psi'_\alpha(x)\bigr]\\
&=\delta_0\Psi_\alpha(x)-\delta x^\mu\partial_\mu\Psi'_\alpha(x)\\
&=\delta_0\Psi_\alpha(x)-\delta x^\mu\partial_\mu\Psi_\alpha(x),
\end{aligned}
```

其中最后一步用到 $`\Psi'_\alpha=\Psi_\alpha+O(\lambda)`$。

在时空区域 $`\Omega`$ 上，变换前后的作用量分别为

```math
\begin{aligned}
S&=\int_\Omega d^4x\,
\mathcal L\bigl(\Psi_\alpha(x),\partial_\mu\Psi_\alpha(x)\bigr),\\
S'&=\int_{\phi_\lambda(\Omega)}d^4x'\,
\mathcal L\bigl(\Psi'_\alpha(x'),\partial'_\mu\Psi'_\alpha(x')\bigr),
\end{aligned}
```

其中 $`\partial'_\mu:=\partial/\partial x'^\mu`$。$`S'`$ 中用的是同一个函数 $`\mathcal L`$：变换作用于场位形和区域 $`\Omega`$，而不作用于拉氏量。这里不假设 $`\mathcal L`$ 的任何性质。

把 $`S'`$ 中的积分变量从 $`x'`$ 换回 $`x`$，于是 $`\phi_\lambda(\Omega)`$ 变为 $`\Omega`$。准确到 $`\lambda`$ 的一阶，

```math
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
```

其中第三行即 (1.58)。因此

```math
S'=\int_\Omega d^4x\,
\bigl(1+\partial_\mu\delta x^\mu\bigr)\,
\mathcal L\bigl(
\Psi_\alpha+\delta_0\Psi_\alpha,\ 
\partial_\mu\Psi_\alpha
+\partial_\mu\delta_0\Psi_\alpha
-(\partial_\mu\delta x^\nu)\partial_\nu\Psi_\alpha
\bigr).
```

把 (1.62) 展开到 $`\lambda`$ 的一阶，得到离壳恒等式

```math
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
```

第二个等号代入了 (1.59) 给出的 $`\delta_0\Psi_\alpha=\delta\Psi_\alpha+\delta x^\nu\partial_\nu\Psi_\alpha`$，并利用了乘积法则以及 $`\partial_\nu\mathcal L=\frac{\partial\mathcal L}{\partial\Psi_\alpha}\partial_\nu\Psi_\alpha+\frac{\partial\mathcal L}{\partial(\partial_\mu\Psi_\alpha)}\partial_\nu\partial_\mu\Psi_\alpha`$；后者成立是因为 $`\mathcal L`$ 不显含 $`x`$。

按假设，作用量不变：$`S'=S`$。取 $`\Omega=[t_1,t_2]\times V`$，并设 $`\Psi_\alpha`$ 满足 Euler–Lagrange 方程，于是 (1.63) 中的 Euler–Lagrange 项为零。再由 Gauss 定理得

```math
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
```

由衰减条件，当 $`V\to\mathbb R^3`$ 时表面项为零。由于 $`t_1`$ 和 $`t_2`$ 任意，

```math
\int d^3x\,\biggl(
\mathcal L\,\delta x^0
+\frac{\partial\mathcal L}{\partial\dot\Psi_\alpha}\delta\Psi_\alpha
\biggr)=\text{const}.
```

代入 (1.59) 给出的 $`\delta\Psi_\alpha=\delta_0\Psi_\alpha-\delta x^\nu\partial_\nu\Psi_\alpha`$，对 $`\lambda`$ 求导，并改变整体符号，即得坐标变换情形的 (1.57)。

**(B) 内部变换**

现在 $`\phi_\lambda`$ 在时空上的作用是平凡的，在场上则通过满足 $`g(0)=I_n`$ 的常数矩阵 $`g(\lambda)`$ 作用：

```math
x'^\mu=x^\mu,\qquad
\Psi'_\alpha(x)=g_{\alpha\beta}(\lambda)\,\Psi_\beta(x).
```

因此 $`\delta x^\mu=0`$，(1.58) 中的两种变分相同：$`\delta\Psi_\alpha(x)=\delta_0\Psi_\alpha(x)=g_{\alpha\beta}(\lambda)\Psi_\beta(x)-\Psi_\alpha(x)`$。取 $`\delta x^\mu=0`$ 重复 (1.60)–(1.65) 的推导：在 (1.61) 中 $`d^4x'=d^4x`$，$`\partial'_\mu=\partial_\mu`$；(1.62)–(1.64) 中含 $`\delta x^\mu`$ 的项消失；(1.65) 变为

```math
\int d^3x\,\frac{\partial\mathcal L}{\partial\dot\Psi_\alpha}\,\delta_0\Psi_\alpha=\text{const}.
```

对 $`\lambda`$ 求导并改变整体符号，即得 $`\delta x^\mu=0`$ 时的 (1.57)。$`\square`$

<a id="spacetime-conserved-quantities"></a>
**(1) 时空平移与能量–动量**

对固定的 $`\epsilon\in\mathbb R^4`$，取 $`\phi_\lambda(x)=x+\lambda\epsilon`$，于是 $`\delta x^\mu=\lambda\epsilon^\mu`$，$`\Lambda=I_4`$，$`\delta_0\Psi_\alpha=0`$。根据 (1.60)–(1.62)，由于 $`\mathcal L`$ 不显含 $`x`$，有 $`S'=S`$，于是 (1.57) 给出

```math
\mathcal Q=\epsilon^\nu\int d^3x\Bigl(\frac{\partial\mathcal L}{\partial\dot\Psi_\alpha}\partial_\nu\Psi_\alpha-\delta^0{}_\nu\mathcal L\Bigr)=\epsilon^\nu P_\nu,
```

其中正则能动张量和四动量为

```math
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
```

这里 $`\partial_\mu T^\mu{}_\nu=0`$ 由 (1.53) 在壳成立，$`P_0=H`$ 则由 (1.54) 得到。

<br><br>

<a id="dirac-constraint"></a>
### 1.5 Dirac 约束

<a id="singular-lagrangian"></a>
#### 奇异拉氏量

**定义**

设 $`L:\mathrm{Conf}\times\mathbb R^n\to\mathbb R`$ 为 (1.2) 中那样的光滑拉氏量，且不显含时间。

- **正则动量**：

```math
p_a:=\frac{\partial L}{\partial\dot q_a}(q,\dot q),\qquad a=1,\ldots,n.
```

- **Hesse 矩阵**：对称矩阵

```math
W_{ab}:=\frac{\partial^2L}{\partial\dot q_a\,\partial\dot q_b}(q,\dot q),\qquad a,b=1,\ldots,n.
```

- **正规拉氏量与奇异拉氏量**：若在 $`\mathrm{Conf}\times\mathbb R^n`$ 上 $`\det W\neq0`$，则称 $`L`$ 是正规的，否则称为奇异的。对奇异的 $`L`$，假设 $`\mathop{\rm rank}\nolimits\,W=r<n`$ 为常数。

若 $`L`$ 正规，则可由 (1.70) 解出速度 $`\dot q=\dot q(q,p)`$，而

```math
H(q,p):=\sum_{a=1}^np_a\,\dot q_a(q,p)-L\bigl(q,\dot q(q,p)\bigr)
```

就是 [1.2 节](#hamiltonian-formalism)的哈密顿量 (1.24)。本节其余部分中 $`L`$ 均为奇异的。

**初级约束**

由于 $`W`$ 对称，它的秩等于其最大可逆主子矩阵的阶数，因此适当重排坐标后可使

```math
\det\bigl(W_{ab}\bigr)_{a,b=1}^{r}\neq0.
```

指标 $`\mu,\nu`$ 取其余的值 $`r+1,\ldots,n`$。由隐函数定理，可从 (1.70) 的前 $`r`$ 个方程局部地解出 $`\dot q_1,\ldots,\dot q_r`$：

```math
\dot q_a=\varphi_a(q,p_b,\dot q_\mu),\qquad a=1,\ldots,r,
```

其中 $`p_b`$ 与 $`\dot q_\mu`$ 分别代表 $`(p_1,\ldots,p_r)`$ 与 $`(\dot q_{r+1},\ldots,\dot q_n)`$。把 (1.74) 代入 (1.70) 的其余方程，得到

```math
p_\mu=\frac{\partial L}{\partial\dot q_\mu}\bigl(q,\varphi(q,p_b,\dot q_\nu),\dot q_\nu\bigr)=:g_\mu(q,p_b),
```

并且 $`g_\mu`$ 不依赖于 $`\dot q_\nu`$：将恒等式 $`p_b=\frac{\partial L}{\partial\dot q_b}(q,\varphi,\dot q_\nu)`$ 对 $`\dot q_\nu`$ 求导，得到 $`\sum_{a=1}^rW_{ba}\frac{\partial\varphi_a}{\partial\dot q_\nu}=-W_{b\nu}`$，因此

```math
\frac{\partial}{\partial\dot q_\nu}\frac{\partial L}{\partial\dot q_\mu}\bigl(q,\varphi,\dot q\bigr)
=W_{\mu\nu}+\sum_{a=1}^rW_{\mu a}\frac{\partial\varphi_a}{\partial\dot q_\nu}
=W_{\mu\nu}-\sum_{a,b=1}^rW_{\mu a}\bigl(W^{-1}\bigr)_{ab}W_{b\nu}=0,
```

其中 $`(W^{-1})_{ab}`$ 是分块 (1.73) 的逆矩阵。最后一个表达式是该分块在 $`W`$ 中的 Schur 补，由于 $`\mathop{\rm rank}\nolimits\,W=r`$，它为零。

- **初级约束**：

```math
\boxed{\chi_\mu(q,p):=p_\mu-g_\mu(q,p_b)=0,\qquad\mu=r+1,\ldots,n.}
```

$`n`$ 个方程 (1.70) 等价于 (1.74) 与 (1.77) 联立。约束 (1.77) 只含 $`(q,p)`$，它们在相空间中定义约束曲面，即映射 $`(q,\dot q)\mapsto(q,p(q,\dot q))`$ 的像。

- **弱等号**：$`F\approx G`$ 表示相空间函数 $`F`$ 与 $`G`$ 在约束曲面上相等。

**正则哈密顿量**

定义

```math
H_c:=\sum_{a=1}^np_a\dot q_a-L(q,\dot q),
```

其中 $`\dot q_1,\ldots,\dot q_r`$ 按 (1.74) 代入，于是 $`H_c`$ 是 $`(q,p,\dot q_\mu)`$ 的函数。由 (1.74)、(1.75) 和 (1.77)，

```math
\frac{\partial H_c}{\partial\dot q_\nu}
=\sum_{a=1}^r\Bigl(p_a-\frac{\partial L}{\partial\dot q_a}\Bigr)\frac{\partial\varphi_a}{\partial\dot q_\nu}
+p_\nu-\frac{\partial L}{\partial\dot q_\nu}
=\chi_\nu(q,p),
```

它与 $`\dot q_\mu`$ 无关，并且在约束曲面上为零。因此在约束曲面上 $`H_c`$ 与 $`\dot q_\mu`$ 无关；而由 (1.77)，它在约束曲面上只是 $`(q,p_1,\ldots,p_r)`$ 的函数。

**总哈密顿量与相容性**

设 $`H_c`$ 为正则哈密顿量，$`u^A`$ 为施加初级约束的拉格朗日乘子。

```math
\boxed{
\begin{aligned}
H_T&=H_c+\sum_A u^A(t)\chi_A^{(1)},\\
\dot\chi_A&=\frac{\partial\chi_A}{\partial t}
+\{\chi_A,H_T\}_{\mathrm{PB}}\approx0.
\end{aligned}}
```

相容性条件可能给出次级及更高级的约束，可能确定乘子，也可能恒成立。反复迭代，直至封闭。

**第一类约束与第二类约束**

```math
\{F,G\}_{\mathrm{PB}}
:=\sum_{a=1}^n\left(
\frac{\partial F}{\partial q_a}\frac{\partial G}{\partial p_a}
-\frac{\partial F}{\partial p_a}\frac{\partial G}{\partial q_a}
\right),
\qquad
\{q_a,p_b\}_{\mathrm{PB}}=\delta_{ab}.
```

若一个约束与每个约束的 Poisson 括号都弱等于零，则称它为第一类约束。分离出所有第一类组合后，剩下的第二类约束 $`\chi_a^{\mathrm{sc}}`$ 的括号矩阵可逆：

```math
\{\chi^{\mathrm{fc}},\chi_A\}_{\mathrm{PB}}\approx0
\quad\text{对所有 }A,
\qquad
C_{ab}:=\{\chi_a^{\mathrm{sc}},\chi_b^{\mathrm{sc}}\}_{\mathrm{PB}},
\qquad
\det C\ne0.
```

**Dirac 括号**

```math
\boxed{
\begin{aligned}
\{F,G\}_{\mathrm D}
&:=\{F,G\}_{\mathrm{PB}}
-\sum_{a,b}\{F,\chi_a^{\mathrm{sc}}\}_{\mathrm{PB}}
(C^{-1})_{ab}\{\chi_b^{\mathrm{sc}},G\}_{\mathrm{PB}},\\
\{F,\chi_a^{\mathrm{sc}}\}_{\mathrm D}&=0.
\end{aligned}}
```

于是第二类约束可以作为强等式施加。对于场，需使用泛函导数、空间积分和逆积分核。

**物理自由度**

对于约束相互独立、规范轨道具有预期维数的正规系统，

```math
\boxed{
N_{\mathrm{physical}}
=n-N_{\mathrm{first}}-\frac12N_{\mathrm{second}}.
}
```

对于场，此式计数的是每个空间点上的局域位形自由度，并须附加边界与零模方面的限定。


<br><br>
<a id="scalar-field"></a>
### 1.6 标量场

<a id="scalar-lagrangian"></a>
#### 拉氏量

**实标量场**

```math
\boxed{
\mathcal L=\frac12\partial_\mu\phi\,\partial^\mu\phi-V(\phi),
\qquad
\partial_\mu\partial^\mu\phi+V'(\phi)=0.
}
\qquad
V(\phi)=\frac12m^2\phi^2
\ \Longrightarrow\
(\partial_\mu\partial^\mu+m^2)\phi=0.
```

```math
\pi=\dot\phi,
\qquad
\boxed{
\mathcal H=\frac12\pi^2+\frac12|\boldsymbol\nabla\phi|^2+V(\phi),
\qquad
H=\int d^3x\,\mathcal H.
}
```

**复标量场**

把 $`\phi`$ 与 $`\phi^*`$ 看作独立变量：

```math
\boxed{
\begin{aligned}
\mathcal L&=\partial_\mu\phi^*\partial^\mu\phi-m^2\phi^*\phi,\\
(\partial_\mu\partial^\mu+m^2)\phi&=0,\qquad
(\partial_\mu\partial^\mu+m^2)\phi^*=0,\\
\pi_\phi&=\dot\phi^*,\qquad \pi_{\phi^*}=\dot\phi,\\
\mathcal H&=\pi_\phi\pi_{\phi^*}
+|\boldsymbol\nabla\phi|^2+m^2|\phi|^2.
\end{aligned}}
```

**守恒量：时空对称性**

平移给出 (1.69) 中的正则能动张量：

```math
\boxed{\begin{aligned}
T^\mu{}_\nu&=\partial^\mu\phi\,\partial_\nu\phi-\delta^\mu{}_\nu\mathcal L
&&\text{（实场）},\\
T^\mu{}_\nu&=\partial^\mu\phi^*\,\partial_\nu\phi
+\partial^\mu\phi\,\partial_\nu\phi^*-\delta^\mu{}_\nu\mathcal L
&&\text{（复场）},\\
\partial_\mu T^\mu{}_\nu&=0,\qquad
P_\nu=\int d^3x\,T^0{}_\nu,\qquad \frac{dP_\nu}{dt}=0.
\end{aligned}}
```

对两种场，$`T^{\mu\nu}:=T^\mu{}_\rho\eta^{\rho\nu}`$ 都是对称的。Lorentz 对称性给出转动荷与 boost 荷

```math
\boxed{
J^{\mu\nu}=\int d^3x\,
\bigl(x^\mu T^{0\nu}-x^\nu T^{0\mu}\bigr),
\qquad
\frac{dJ^{\mu\nu}}{dt}=0.
}
```

其中 $`P_0`$ 是能量，$`P^i`$ 是空间动量，$`J^{ij}`$ 生成转动，$`J^{0i}`$ 生成 boost。这些守恒律在壳成立，并要求积分收敛、边界通量为零。

**守恒量：内部对称性与规范对称性**

实标量场没有复场那样的 $`U(1)`$ 相位对称性。复场拉氏量 (1.87) 具有全局 $`U(1)`$ 对称性；没有规范场时，它在任意局域相位 $`\lambda(x)`$ 下并非不变。对常数 $`\lambda`$，守恒流与荷为

```math
\phi'=e^{i\lambda}\phi,
\qquad
\boxed{
j^\mu=i\bigl(\phi^*\partial^\mu\phi-\phi\,\partial^\mu\phi^*\bigr),
\qquad
\partial_\mu j^\mu=0,
\qquad
Q=\int d^3x\,j^0.
}
```


<br><br>

<a id="scalar-field-solutions"></a>
#### Klein–Gordon 方程的解

对实场取 $`V(\phi)=\tfrac12m^2\phi^2`$；(1.87) 中的复场本身已是自由场。定义 $`\Box:=\partial_\mu\partial^\mu`$。平面波满足

```math
(\Box+m^2)e^{\mp ip\cdot x}=(m^2-p^2)e^{\mp ip\cdot x}=0,
\qquad
p^2=m^2,\qquad
p^0=E_{\mathbf p}:=\sqrt{\mathbf p^2+m^2}>0.
```

采用下式中显式写出的 Lorentz 不变测度，实波包的展开为

```math
\boxed{
\phi(x)=\int\frac{d^3p}{(2\pi)^3\,2E_{\mathbf p}}
\left[a(\mathbf p)e^{-ip\cdot x}+a^*(\mathbf p)e^{+ip\cdot x}\right].
}
```

对复场，两种频率的振幅相互独立：

```math
\boxed{\begin{aligned}
\phi(x)&=\int\frac{d^3p}{(2\pi)^3\,2E_{\mathbf p}}
\left[a(\mathbf p)e^{-ip\cdot x}+b^*(\mathbf p)e^{+ip\cdot x}\right],\\
\phi^*(x)&=\int\frac{d^3p}{(2\pi)^3\,2E_{\mathbf p}}
\left[a^*(\mathbf p)e^{+ip\cdot x}+b(\mathbf p)e^{-ip\cdot x}\right].
\end{aligned}}
```

这些系数是经典复振幅。实场条件为 $`b=a`$。这些自由场展开不适用于一般的非线性势 $`V(\phi)`$。

<br><br>

<a id="dirac-field"></a>
### 1.7 Dirac 场 $`\psi`$

<a id="dirac-lagrangian"></a>
#### 拉氏量

Dirac 场的拉氏量具有如下形式：

```math
\boxed{
\mathcal L=\bar\psi\bigl(i\gamma^\mu\partial_\mu-m\bigr)\psi,
}
```

其中 $`\psi:\mathbb R^4\to\mathbb C^4`$ 是 Dirac 场，$`\bar\psi:=\psi^\dagger\gamma^0`$ 是它的 Dirac 共轭，$`\gamma^\mu`$ 由 (0.10) 给出，$`m`$ 是质量。

把 $`\psi`$ 与 $`\bar\psi`$ 看作相互独立，Euler–Lagrange 方程给出 Dirac 方程及其共轭方程：

```math
\boxed{\begin{aligned}
\bigl(i\gamma^\mu\partial_\mu-m\bigr)\psi&=0,\\
i(\partial_\mu\bar\psi)\gamma^\mu+m\bar\psi&=0.
\end{aligned}}
```

**哈密顿量**

把 $`\psi`$ 与 $`\bar\psi`$ 看作相互独立，它们的共轭动量为

```math
\boxed{\begin{aligned}
\pi_\psi&:=\frac{\partial\mathcal L}{\partial\dot\psi}
=i\bar\psi\gamma^0=i\psi^\dagger,\\
\pi_{\bar\psi}&:=\frac{\partial\mathcal L}{\partial\dot{\bar\psi}}=0.
\end{aligned}}
```

**守恒量：时空对称性**

平移给出正则能动张量与四动量

```math
\boxed{\begin{aligned}
T^\mu{}_\nu&=i\bar\psi\gamma^\mu\partial_\nu\psi-\delta^\mu{}_\nu\mathcal L,
&\partial_\mu T^\mu{}_\nu&=0,\\
P_\nu&=\int d^3x\,T^0{}_\nu,
&\frac{dP_\nu}{dt}&=0.
\end{aligned}}
```

记 $`T^{\mu\nu}:=T^\mu{}_\rho\eta^{\rho\nu}`$，Lorentz 对称性给出

```math
\boxed{\begin{aligned}
J^{\mu\nu}&=\int d^3x\left[
x^\mu T^{0\nu}-x^\nu T^{0\mu}
+\frac{i}{4}\psi^\dagger[\gamma^\mu,\gamma^\nu]\psi
\right],\\
\frac{dJ^{\mu\nu}}{dt}&=0.
\end{aligned}}
```

最后一项是自旋贡献。$`J^{ij}`$ 与 $`J^{0i}`$ 分别是转动荷与 boost 荷。守恒性在壳成立，并要求积分收敛、边界通量为零。

**守恒量：内部对称性与规范对称性**

自由 Dirac 拉氏量具有全局 $`U(1)`$ 对称性。对常数 $`\lambda`$，

```math
\boxed{\begin{aligned}
\psi'&=e^{i\lambda}\psi,\qquad
\bar\psi'=e^{-i\lambda}\bar\psi,\\
j^\mu&=\bar\psi\gamma^\mu\psi,\qquad \partial_\mu j^\mu=0,\\
Q&=\int d^3x\,j^0=\int d^3x\,\psi^\dagger\psi,
\qquad \frac{dQ}{dt}=0.
\end{aligned}}
```

对局域相位 $`\lambda(x)`$，$`\mathcal L'=\mathcal L-j^\mu\partial_\mu\lambda`$；局域规范不变性要求与规范场耦合。

<br><br>

<a id="weyl-spinor-solutions"></a>
#### Weyl 表示下 Dirac 方程的解

**Lorentz 群的旋量表示**

对 Dirac 场，(1.40) 中的 $`D(\Lambda)`$ 为

```math
\Lambda_{\frac12}=\exp\Bigl(-\frac i2\omega_{\mu\nu}S^{\mu\nu}\Bigr),
\qquad
S^{\mu\nu}:=\frac i4[\gamma^\mu,\gamma^\nu],
```

其中 $`\omega_{\mu\nu}`$ 与 (0.35) 中相同。在 Weyl 表示下，每个 $`S^{\mu\nu}`$ 都是分块对角的：

```math
S^{0i}=-\frac i2\begin{pmatrix}\sigma^i&0\\0&-\sigma^i\end{pmatrix},
\qquad
S^{ij}=\frac12\epsilon^{ijk}\begin{pmatrix}\sigma^k&0\\0&\sigma^k\end{pmatrix}.
```

非紧的 Lorentz 群 $`SO(1,3)^+`$ 没有非平凡的有限维幺正表示；在 Weyl 表示下 $`(S^{0i})^\dagger=-S^{0i}`$，因此快度非零时，有限 boost 矩阵不是幺正的。

因此 $`\Lambda_{\frac12}`$ 是分块对角的：记 $`\psi=\begin{pmatrix}\psi_L\\\psi_R\end{pmatrix}`$，左手与右手 Weyl 旋量 $`\psi_L,\psi_R`$ 各自独立地变换。对无穷小变换，与 (0.34) 一样取 $`\omega_{ij}=\epsilon_{ijk}\theta^k`$、$`\omega_{0i}=b^i`$，

```math
\begin{aligned}
\Lambda_{\frac12}
&\simeq I_4-\frac i2\omega_{\mu\nu}S^{\mu\nu}\\
&=I_4-\frac i2\begin{pmatrix}\boldsymbol\theta\cdot\boldsymbol\sigma&0\\0&\boldsymbol\theta\cdot\boldsymbol\sigma\end{pmatrix}
-i\Bigl(-\frac i2\Bigr)\begin{pmatrix}\mathbf b\cdot\boldsymbol\sigma&0\\0&-\mathbf b\cdot\boldsymbol\sigma\end{pmatrix}\\
&=\begin{pmatrix}I_2-i\boldsymbol\theta\cdot\frac{\boldsymbol\sigma}2-\mathbf b\cdot\frac{\boldsymbol\sigma}2&0\\0&I_2-i\boldsymbol\theta\cdot\frac{\boldsymbol\sigma}2+\mathbf b\cdot\frac{\boldsymbol\sigma}2\end{pmatrix},
\end{aligned}
```

于是

```math
\begin{aligned}
\psi_L&\xrightarrow{\ \Lambda\ }\Bigl(I_2-i\boldsymbol\theta\cdot\frac{\boldsymbol\sigma}2-\mathbf b\cdot\frac{\boldsymbol\sigma}2\Bigr)\psi_L,\\
\psi_R&\xrightarrow{\ \Lambda\ }\Bigl(I_2-i\boldsymbol\theta\cdot\frac{\boldsymbol\sigma}2+\mathbf b\cdot\frac{\boldsymbol\sigma}2\Bigr)\psi_R.
\end{aligned}
```

用 $`\psi_L,\psi_R`$ 表示，Dirac 方程 (1.95) 为

```math
\begin{pmatrix}-m&i\sigma^\mu\partial_\mu\\i\bar\sigma^\mu\partial_\mu&-m\end{pmatrix}
\begin{pmatrix}\psi_L\\\psi_R\end{pmatrix}=0
\quad\Longleftrightarrow\quad
\begin{cases}
i\sigma^\mu\partial_\mu\psi_R-m\psi_L=0,\\
i\bar\sigma^\mu\partial_\mu\psi_L-m\psi_R=0.
\end{cases}
```

$`m=0`$ 时，它化为 Weyl 方程

```math
\begin{cases}
i\bigl(\partial_t-\boldsymbol\sigma\cdot\nabla\bigr)\psi_L=0,\\
i\bigl(\partial_t+\boldsymbol\sigma\cdot\nabla\bigr)\psi_R=0.
\end{cases}
```

**Dirac 方程的平面波解**

将 $`-i\gamma^\mu\partial_\mu-m`$ 作用于 (1.95) 的左边：

```math
\begin{aligned}
\bigl(-i\gamma^\mu\partial_\mu-m\bigr)\bigl(i\gamma^\nu\partial_\nu-m\bigr)\psi
&=\bigl(\gamma^\mu\gamma^\nu\partial_\mu\partial_\nu+m^2\bigr)\psi\\
&=\bigl(\eta^{\mu\nu}\partial_\mu\partial_\nu+m^2\bigr)\psi\\
&=\bigl(\Box+m^2\bigr)\psi,
\end{aligned}
```

其中 $`\Box:=\eta^{\mu\nu}\partial_\mu\partial_\nu=\partial_t^2-\nabla^2`$。由 (1.95)，(1.106) 的左边为零，因此 $`\psi`$ 的每个分量都满足 Klein–Gordon 方程

```math
\bigl(\Box+m^2\bigr)\psi=0.
```

平面波 $`e^{-ip\cdot x}`$ 只有在 $`p^2=m^2`$ 时才满足 (1.107)。因此在 Weyl 表示 (0.10) 下，(1.95) 的平面波解具有如下形式

```math
\psi(x)=\begin{pmatrix}u_L\\u_R\end{pmatrix}e^{-ip\cdot x},
\qquad
p^0=\pm E_{\mathbf p},\quad
E_{\mathbf p}:=\sqrt{\mathbf p^2+m^2},
```

其中 $`u_L,u_R\in\mathbb C^2`$ 为常量。把 (1.108) 代入 (1.95)，得到

```math
\bigl(\not p-m\bigr)\begin{pmatrix}u_L\\u_R\end{pmatrix}=0,
\qquad
\not p:=\gamma\cdot p=p^\mu\gamma_\mu.
```

**(1) 静止系**

取 $`m>0`$，在静止系 $`\mathbf p=\mathbf 0`$ 中讨论；此时把 (1.108) 中的常量记为 $`u_L(\mathbf 0)`$ 和 $`u_R(\mathbf 0)`$。先考虑 $`p^0>0`$。这时 $`p^\mu=(m,\mathbf 0)`$，$`e^{-ip\cdot x}=e^{-imt}`$，$`\not p=m\gamma^0`$，于是 (1.109) 化为

```math
\begin{aligned}
\bigl(m\gamma^0-m\bigr)\begin{pmatrix}u_L(\mathbf 0)\\u_R(\mathbf 0)\end{pmatrix}
&=\begin{pmatrix}-mI_2&mI_2\\mI_2&-mI_2\end{pmatrix}
\begin{pmatrix}u_L(\mathbf 0)\\u_R(\mathbf 0)\end{pmatrix}=0\\[6pt]
\Longrightarrow\quad u_L(\mathbf 0)&=u_R(\mathbf 0).
\end{aligned}
```

记 $`u:=\begin{pmatrix}u_L\\u_R\end{pmatrix}`$，共有两个独立解

```math
u^s(\mathbf 0)=\sqrt m\begin{pmatrix}\xi^s\\\xi^s\end{pmatrix},\qquad s=1,2,
```

其中 $`\{\xi^s\}`$ 是 $`\mathbb C^2`$ 的一组基，满足 $`\xi^{r\dagger}\xi^s=\delta^{rs}`$。

**(2) Boost**

沿 $`z`$ 方向做快度为 $`\eta`$ 的 boost，即在 (1.100) 中取 $`\omega_{03}=\eta`$，从而 $`\mathbf p=(0,0,p^3)`$，$`\tanh\eta=v=p^3/E_{\mathbf p}`$。于是

```math
\begin{aligned}
\Lambda_{\frac12}=e^{-i\eta S^{03}}
&=\exp\Bigl[-i\eta\Bigl(-\frac i2\Bigr)\begin{pmatrix}\sigma^3&0\\0&-\sigma^3\end{pmatrix}\Bigr]
=\begin{pmatrix}e^{-\frac12\eta\sigma^3}&0\\0&e^{\frac12\eta\sigma^3}\end{pmatrix}\\
&=\mathop{\rm diag}\nolimits \bigl(e^{-\eta/2},\,e^{\eta/2},\,e^{\eta/2},\,e^{-\eta/2}\bigr),
\end{aligned}
```

```math
\tanh\eta=v
\ \Longrightarrow\
e^{\pm\eta}=\sqrt{\frac{1\pm v}{1\mp v}}=\frac{E_{\mathbf p}\pm p^3}{m},
\qquad
e^{\pm\eta/2}=\sqrt{\frac{E_{\mathbf p}\pm p^3}{m}}.
```

因此

```math
u^s(p)=\Lambda_{\frac12}u^s(\mathbf 0)
=\mathop{\rm diag}\nolimits \Bigl(\sqrt{E_{\mathbf p}-p^3},\,\sqrt{E_{\mathbf p}+p^3},\,\sqrt{E_{\mathbf p}+p^3},\,\sqrt{E_{\mathbf p}-p^3}\Bigr)
\begin{pmatrix}\xi^s\\\xi^s\end{pmatrix}.
```

取 $`\xi^1=\begin{pmatrix}1\\0\end{pmatrix}`$，$`\xi^2=\begin{pmatrix}0\\1\end{pmatrix}`$，

```math
u^1(p)=\begin{pmatrix}\sqrt{E_{\mathbf p}-p^3}\\0\\\sqrt{E_{\mathbf p}+p^3}\\0\end{pmatrix}
\xrightarrow{\ \eta\to\infty\ }\sqrt{2E_{\mathbf p}}\begin{pmatrix}0\\0\\1\\0\end{pmatrix},
\qquad
u^2(p)=\begin{pmatrix}0\\\sqrt{E_{\mathbf p}+p^3}\\0\\\sqrt{E_{\mathbf p}-p^3}\end{pmatrix}
\xrightarrow{\ \eta\to\infty\ }\sqrt{2E_{\mathbf p}}\begin{pmatrix}0\\1\\0\\0\end{pmatrix}.
```

**(3) 任意动量**

由于 $`\mathop{\rm diag}\nolimits \bigl(\sqrt{E_{\mathbf p}-p^3},\sqrt{E_{\mathbf p}+p^3}\bigr)=\sqrt{E_{\mathbf p}-p^3\sigma^3}`$，$`\mathop{\rm diag}\nolimits \bigl(\sqrt{E_{\mathbf p}+p^3},\sqrt{E_{\mathbf p}-p^3}\bigr)=\sqrt{E_{\mathbf p}+p^3\sigma^3}`$，对任意 $`\mathbf p`$ 有

```math
\sqrt m\,\Lambda_{\frac12}=\begin{pmatrix}\sqrt{p\cdot\sigma}&0\\0&\sqrt{p\cdot\bar\sigma}\end{pmatrix},
\qquad
p\cdot\sigma:=p_\mu\sigma^\mu=p^0I_2-\mathbf p\cdot\boldsymbol\sigma,
\quad
p\cdot\bar\sigma:=p_\mu\bar\sigma^\mu=p^0I_2+\mathbf p\cdot\boldsymbol\sigma,
```

其中取正平方根。正能解为

```math
\boxed{
\psi=u^s(p)\,e^{-ip\cdot x},\qquad
u^s(p)=\begin{pmatrix}\sqrt{p\cdot\sigma}\,\xi^s\\\sqrt{p\cdot\bar\sigma}\,\xi^s\end{pmatrix},\qquad
p^0=E_{\mathbf p}.
}
```

**验证**

```math
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
```

**负能解**

对 $`p^0=-E_{\mathbf p}`$，(1.109) 化为

```math
\bigl(-\gamma^0E_{\mathbf p}-\boldsymbol\gamma\cdot\mathbf p-m\bigr)u(p)=0
\quad\Longleftrightarrow\quad
\bigl(\gamma^0E_{\mathbf p}-\boldsymbol\gamma\cdot(-\mathbf p)+m\bigr)u(p)=0,
```

这正是正能方程 $`\bigl(\gamma^0E_{\mathbf p}-\boldsymbol\gamma\cdot\mathbf p-m\bigr)u=0`$ 作代换 $`\mathbf p\to-\mathbf p`$、$`m\to-m`$ 的结果。因此

```math
u^s(p)=\begin{pmatrix}\sqrt{E_{\mathbf p}I_2+\mathbf p\cdot\boldsymbol\sigma}\,\xi^s\\-\sqrt{E_{\mathbf p}I_2-\mathbf p\cdot\boldsymbol\sigma}\,\xi^s\end{pmatrix}
=\begin{pmatrix}\sqrt{-p\cdot\sigma}\,\xi^s\\-\sqrt{-p\cdot\bar\sigma}\,\xi^s\end{pmatrix},
\qquad p^0=-E_{\mathbf p}.
```

**反粒子解**

定义

```math
u^c(p):=\begin{pmatrix}i\sigma^2&0\\0&-i\sigma^2\end{pmatrix}\gamma^0\,u(p),
\qquad
i\sigma^2=\begin{pmatrix}0&1\\-1&0\end{pmatrix}.
```

对 $`\mathbf p=(0,0,p^3)`$，

```math
i\sigma^2\sqrt{p\cdot\bar\sigma}
=\begin{pmatrix}0&1\\-1&0\end{pmatrix}\begin{pmatrix}\sqrt{E_{\mathbf p}+p^3}&0\\0&\sqrt{E_{\mathbf p}-p^3}\end{pmatrix}
=\begin{pmatrix}0&\sqrt{E_{\mathbf p}-p^3}\\-\sqrt{E_{\mathbf p}+p^3}&0\end{pmatrix}
=\sqrt{p\cdot\sigma}\;i\sigma^2,
```

同理 $`i\sigma^2\sqrt{p\cdot\sigma}=\sqrt{p\cdot\bar\sigma}\;i\sigma^2`$。将 (1.121) 用于 (1.117)，并记 $`\eta^s:=i\sigma^2\xi^s`$，

```math
u^c(p)=\begin{pmatrix}i\sigma^2\sqrt{p\cdot\bar\sigma}\,\xi^s\\-i\sigma^2\sqrt{p\cdot\sigma}\,\xi^s\end{pmatrix}
=\begin{pmatrix}\sqrt{p\cdot\sigma}\,\eta^s\\-\sqrt{p\cdot\bar\sigma}\,\eta^s\end{pmatrix},
\qquad p^0=E_{\mathbf p},
```

这正是 (1.120) 取在 $`-p`$ 处、并作代换 $`\xi^s\to\eta^s`$ 的结果。对任意 $`\mathbf p`$，反粒子解为

```math
\boxed{
\psi=v^s(p)\,e^{+ip\cdot x},\qquad
v^s(p):=\begin{pmatrix}\sqrt{p\cdot\sigma}\,\eta^s\\-\sqrt{p\cdot\bar\sigma}\,\eta^s\end{pmatrix},\qquad
\bigl(\not p+m\bigr)v^s(p)=0,\qquad
p^0=E_{\mathbf p}.
}
```

**解的性质**

**(1) 正交归一性**

由 (1.117)，$`u^\dagger u=2E_{\mathbf p}\,\xi^\dagger\xi`$，$`\bar uu=2m\,\xi^\dagger\xi`$。利用 $`\xi^{r\dagger}\xi^s=\eta^{r\dagger}\eta^s=\delta^{rs}`$，

```math
\boxed{
\begin{aligned}
u^{r\dagger}(p)\,u^s(p)&=2E_{\mathbf p}\,\delta^{rs}, &\qquad \bar u^r(p)\,u^s(p)&=2m\,\delta^{rs},\\
v^{r\dagger}(p)\,v^s(p)&=2E_{\mathbf p}\,\delta^{rs}, &\qquad \bar v^r(p)\,v^s(p)&=-2m\,\delta^{rs},\\
u^{r\dagger}(p)\,v^s(p')&=v^{r\dagger}(p')\,u^s(p)=0, &\qquad p'&:=(p^0,-\mathbf p).
\end{aligned}
}
```

**(2) 完备性（自旋求和）**

利用 $`\sum_s\xi^s\xi^{s\dagger}=I_2`$，

```math
\boxed{
\sum_s u^s(p)\,\bar u^s(p)=\not p+m,\qquad
\sum_s v^s(p)\,\bar v^s(p)=\not p-m.
}
```

<br><br>

<a id="dirac-bilinears"></a>
#### Dirac 双线性型

双线性型的形式为 $`\bar\psi\Gamma\psi`$，其中 $`\Gamma`$ 为 $`4\times4`$ 矩阵。$`4\times4`$ 矩阵的一组基由 16 个矩阵组成：

<div style="display: flex; justify-content: center;">

| $`\Gamma`$ | 个数 | 替换为 |
|:---:|:---:|:---:|
| $`I_4`$ | 1 | |
| $`\gamma^\mu`$ | 4 | |
| $`S^{\mu\nu}`$ | 6 | |
| $`\gamma^{[\mu}\gamma^\nu\gamma^{\rho]}`$ | 4 | $`\gamma^5\gamma^\mu`$ |
| $`\gamma^{[\mu}\gamma^\nu\gamma^\rho\gamma^{\sigma]}`$ | 1 | $`\gamma^5`$ |

</div>

其中

```math
\gamma^5=\frac{i}{4!}\epsilon_{\mu\nu\rho\sigma}\gamma^\mu\gamma^\nu\gamma^\rho\gamma^\sigma,
\qquad \epsilon_{0123}=+1,
```

这与 (0.14) 一致。在 $`\psi\to\Lambda_{\frac12}\psi`$、$`\bar\psi\to\bar\psi\Lambda_{\frac12}^{-1}`$ 下，

```math
\begin{aligned}
\bar\psi\psi&\xrightarrow{\ \Lambda\ }\bar\psi\psi,\\
\bar\psi\gamma^\mu\psi&\xrightarrow{\ \Lambda\ }\bar\psi\Lambda_{\frac12}^{-1}\gamma^\mu\Lambda_{\frac12}\psi=\Lambda^\mu{}_\nu\,\bar\psi\gamma^\nu\psi,\\
\bar\psi S^{\mu\nu}\psi&\xrightarrow{\ \Lambda\ }\Lambda^\mu{}_\rho\Lambda^\nu{}_\sigma\,\bar\psi S^{\rho\sigma}\psi,\\
\bar\psi\gamma^5\gamma^\mu\psi&\xrightarrow{\ \Lambda\ }\det[\Lambda]\,\Lambda^\mu{}_\nu\,\bar\psi\gamma^5\gamma^\nu\psi\qquad\text{（赝矢量）},\\
\bar\psi\gamma^5\psi&\xrightarrow{\ \Lambda\ }\det[\Lambda]\,\bar\psi\gamma^5\psi\qquad\text{（赝标量）}.
\end{aligned}
```

**证明**（$`\gamma^5`$ 的情形）

```math
\begin{aligned}
\Lambda_{\frac12}^{-1}\gamma^5\Lambda_{\frac12}
&=\frac{i}{4!}\epsilon_{\mu\nu\rho\sigma}\Lambda^\mu{}_\alpha\Lambda^\nu{}_\beta\Lambda^\rho{}_\kappa\Lambda^\sigma{}_\lambda\,\gamma^\alpha\gamma^\beta\gamma^\kappa\gamma^\lambda\\
&=\frac{i}{4!}\det[\Lambda]\,\epsilon_{\alpha\beta\kappa\lambda}\gamma^\alpha\gamma^\beta\gamma^\kappa\gamma^\lambda
=\det[\Lambda]\,\gamma^5.
\end{aligned}
```

**手征**

```math
\gamma^5\begin{pmatrix}\psi_L\\0\end{pmatrix}=-\begin{pmatrix}\psi_L\\0\end{pmatrix},
\qquad
\gamma^5\begin{pmatrix}0\\\psi_R\end{pmatrix}=\begin{pmatrix}0\\\psi_R\end{pmatrix}.
```

左手与右手投影算符为

```math
P_L:=\frac{I_4-\gamma^5}2,\qquad P_R:=\frac{I_4+\gamma^5}2
\quad\Longrightarrow\quad
\begin{cases}
P_L+P_R=I_4,\\
P_LP_R=P_RP_L=0,\\
P_L^n=P_L,\quad P_R^n=P_R.
\end{cases}
```

**矢量流与轴矢流**

```math
j^\mu:=\bar\psi\gamma^\mu\psi,\qquad
j^{\mu5}:=\bar\psi\gamma^\mu\gamma^5\psi.
```

(1.94) 关于 $`\psi`$ 的 Euler–Lagrange 方程为 $`-i\partial_\mu\bar\psi\gamma^\mu-m\bar\psi=0`$。结合 (1.95)，

```math
\partial_\mu j^\mu=(\partial_\mu\bar\psi)\gamma^\mu\psi+\bar\psi\gamma^\mu\partial_\mu\psi
=im\bar\psi\psi-im\bar\psi\psi=0
\quad\Longrightarrow\quad
\int d^3x\,\bar\psi\gamma^0\psi=\text{const}.
```

**螺旋度**

```math
h:=\frac{\mathbf p}{|\mathbf p|}\cdot\mathbf S,\qquad
\mathbf S:=\frac12\begin{pmatrix}\boldsymbol\sigma&0\\0&\boldsymbol\sigma\end{pmatrix}.
```

对 $`\mathbf p=(0,0,p^3)`$ 且 $`p^3>0`$，旋量 (1.115) 满足 $`h\,u^1=\frac12u^1`$，$`h\,u^2=-\frac12u^2`$。


<br><br>

<a id="proca-field"></a>
### 1.8 Proca 场

<a id="proca-lagrangian"></a>
#### 拉氏量

对 $`m>0`$ 的实矢量场，

```math
F_{\mu\nu}:=\partial_\mu A_\nu-\partial_\nu A_\mu,
\qquad
\boxed{
\mathcal L=-\frac14F_{\mu\nu}F^{\mu\nu}
+\frac12m^2A_\mu A^\mu.
}
```

```math
\boxed{
\partial_\mu F^{\mu\nu}+m^2A^\nu=0,
\qquad
\partial_\mu A^\mu=0,
\qquad
(\partial_\mu\partial^\mu+m^2)A^\nu=0.
}
```

其中 $`\partial_\mu A^\mu=0`$ 由运动方程推出。

**正则动量与哈密顿量**

取 $`A_\mu`$ 为正则坐标。下面的括号都是等时括号：

```math
\Pi^\mu:=\frac{\partial\mathcal L}{\partial\dot A_\mu}=F^{\mu0},
\qquad
\Pi^0=0,
\qquad
\Pi^i=\dot A_i-\partial_iA_0,
\qquad
\{A_\mu(\mathbf x),\Pi^\nu(\mathbf y)\}_{\mathrm{PB}}
=\delta_\mu{}^\nu\delta^{(3)}(\mathbf x-\mathbf y).
```

在空间表面项为零的条件下，

```math
\boxed{
\begin{aligned}
H_c&=\int d^3x\left[
\frac12\sum_i(\Pi^i)^2+\frac14\sum_{i,j}(F_{ij})^2
+\frac{m^2}{2}\sum_i(A_i)^2
-\frac{m^2}{2}A_0^2-A_0\partial_i\Pi^i\right],\\
H_T&=H_c+\int d^3x\,u\,\Pi^0.
\end{aligned}}
```

**第二类约束**

```math
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
```

保持 $`\chi_2`$ 成立的条件定出 $`u=\sum_i\partial_iA_i`$；此后不再有新的约束。

其中 $`\chi_1`$ 是初级约束，$`\chi_2`$ 是次级约束；两者都是第二类的。

**约化哈密顿量**

消去 $`\Pi^0`$ 和 $`A_0`$，得到

```math
A_0=-\frac{\partial_i\Pi^i}{m^2},
\qquad
\boxed{
H_{\mathrm{red}}=\int d^3x\left[
\frac12\sum_i(\Pi^i)^2+\frac14\sum_{i,j}(F_{ij})^2
+\frac{m^2}{2}\sum_i(A_i)^2
+\frac{(\partial_i\Pi^i)^2}{2m^2}
\right]\ge0.
}
```

**守恒量：时空对称性**

以 $`A_\mu`$ 为正则变量，平移给出

```math
\boxed{\begin{aligned}
T^\mu{}_\nu&=-F^{\mu\rho}\partial_\nu A_\rho-\delta^\mu{}_\nu\mathcal L,
&\partial_\mu T^\mu{}_\nu&=0,\\
P_\nu&=\int d^3x\,T^0{}_\nu,
&\frac{dP_\nu}{dt}&=0.
\end{aligned}}
```

记 $`T^{\mu\nu}:=T^\mu{}_\rho\eta^{\rho\nu}`$，Lorentz 荷包含矢量场的自旋贡献：

```math
\boxed{
J^{\mu\nu}=\int d^3x\left[
x^\mu T^{0\nu}-x^\nu T^{0\mu}
+\Pi^\mu A^\nu-\Pi^\nu A^\mu
\right],
\qquad
\frac{dJ^{\mu\nu}}{dt}=0.
}
```

它们在壳守恒，并要求积分收敛、边界通量为零。

**守恒量：内部对称性与规范对称性**

$`m>0`$ 时，质量项破坏 Maxwell 规范对称性 $`A_\mu\mapsto A_\mu+\partial_\mu\lambda(x)`$。实 Proca 场没有复 $`U(1)`$ 相位对称性，因此该模型没有相应的相位荷。其约束 $`\partial_i\Pi^i+m^2A_0=0`$ 是第二类的，如 (1.139)。

<br><br>

<a id="proca-field-solutions"></a>
#### Proca 方程的解

对 $`A^\mu(x)=\epsilon^\mu(p)e^{-ip\cdot x}`$，场方程化为

```math
\begin{aligned}
(m^2-p^2)\epsilon^\mu+p^\mu(p_\nu\epsilon^\nu)&=0,\\
m^2p_\mu\epsilon^\mu&=0.
\end{aligned}
\quad\Longrightarrow\quad
\boxed{p^2=m^2,\qquad p_\mu\epsilon^\mu=0}
```

这对 $`m>0`$ 的非零模式成立。

**偏振**

对 $`p^2=m^2`$、$`p^0>0`$，共有三个偏振矢量，$`r=1,2,3`$：

```math
\boxed{
p_\mu\epsilon_r^\mu(p)=0,
\qquad
\epsilon_{r\mu}^*(p)\epsilon_s^\mu(p)=-\delta_{rs},
\qquad
\sum_{r=1}^3\epsilon_r^\mu(p)\epsilon_r^{\nu*}(p)
=-\eta^{\mu\nu}+\frac{p^\mu p^\nu}{m^2}.
}
```


静止时，可取 $`\epsilon_r^\mu=(0,\mathbf e_r)`$，其中 $`\mathbf e_r`$ 是空间的一组正交归一基。对 $`\mathbf p\ne0`$，取 $`\mathbf e_1,\mathbf e_2`$ 垂直于 $`\mathbf p`$，且 $`\mathbf e_a\cdot\mathbf e_b=\delta_{ab}`$。记 $`E_{\mathbf p}=\sqrt{\mathbf p^2+m^2}`$，由两个横偏振和一个纵偏振构成的基为

```math
\boxed{
\epsilon_a^\mu(p)=(0,\mathbf e_a)\quad(a=1,2),
\qquad
\epsilon_3^\mu(p)=\left(\frac{|\mathbf p|}{m},
\frac{E_{\mathbf p}}{m}\frac{\mathbf p}{|\mathbf p|}\right).
}
```

实场是这三个模式的叠加，其中 $`p^0=E_{\mathbf p}`$：

```math
\boxed{
A^\mu(x)=\sum_{r=1}^3\int\frac{d^3p}{(2\pi)^3\,2E_{\mathbf p}}
\left[
a_r(\mathbf p)\epsilon_r^\mu(p)e^{-ip\cdot x}
+a_r^*(\mathbf p)\epsilon_r^{\mu*}(p)e^{+ip\cdot x}
\right].
}
```

其中 $`a_r(\mathbf p)`$ 是经典复振幅；横向条件来自场方程，而非规范选择。

<br><br>

<a id="vector-field"></a>
### 1.9 矢量场

<a id="maxwell-lagrangian"></a>
#### 拉氏量

```math
\boxed{
\mathcal L=-\frac14F_{\mu\nu}F^{\mu\nu},
\qquad
\partial_\mu F^{\mu\nu}=0,
\qquad
A_\mu'=A_\mu+\partial_\mu\lambda(x).
}
```

**哈密顿量与第一类约束**

```math
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
```

两个约束都是第一类的：

```math
\{\chi_a(\mathbf x),\chi_b(\mathbf y)\}_{\mathrm{PB}}=0,
\qquad a,b=1,2,
\qquad
\boxed{N_{\mathrm{physical}}=4-2=2.}
```

**Coulomb 规范与物理哈密顿量**

在无源且场在空间无穷远衰减的情况下，

```math
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
```

剩下的正则变量是横向的。

**守恒量：时空对称性**

正则能动张量与四动量为

```math
\boxed{\begin{aligned}
T^\mu{}_\nu&=-F^{\mu\rho}\partial_\nu A_\rho-\delta^\mu{}_\nu\mathcal L,
&\partial_\mu T^\mu{}_\nu&=0,\\
P_\nu&=\int d^3x\,T^0{}_\nu,
&\frac{dP_\nu}{dt}&=0.
\end{aligned}}
```

记 $`T^{\mu\nu}:=T^\mu{}_\rho\eta^{\rho\nu}`$，转动荷与 boost 荷为

```math
\boxed{
J^{\mu\nu}=\int d^3x\left[
x^\mu T^{0\nu}-x^\nu T^{0\mu}
+\Pi^\mu A^\nu-\Pi^\nu A^\mu
\right],
\qquad
\frac{dJ^{\mu\nu}}{dt}=0.
}
```

当积分收敛且边界通量为零时，这些荷在壳守恒。正则密度依赖于规范；积分后的荷在边界项为零的规范变换下不变。

**守恒量：内部对称性与规范对称性**

(1.147) 中的局域变换给出一个 Noether 恒等式以及 Gauss 约束。对于在整个 $`\mathbb R^3`$ 上光滑且无源的场，

```math
\boxed{\begin{aligned}
\partial_\nu\partial_\mu F^{\mu\nu}&\equiv0,
&\partial_i\Pi^i&=0,\\
Q_{\mathrm{el}}&:=\lim_{R\to\infty}\oint_{|\mathbf x|=R}\Pi^i\,dS_i=0.
\end{aligned}}
```

这一自由场模型中没有独立的物质 $`U(1)`$ 粒子数。非零电通量需要源、奇点或不同的边界条件。

<br><br>

<a id="maxwell-field-solutions"></a>
#### Maxwell 方程的解

**Lorenz 规范**

```math
\partial_\mu A^\mu=0
\quad\Longrightarrow\quad
\partial_\mu\partial^\mu A^\nu=0,
\qquad
A_\mu\mapsto A_\mu+\partial_\mu\lambda,
\qquad
\partial_\mu\partial^\mu\lambda=0
\quad\text{（剩余规范自由度）。}
```


**平面波与物理偏振**

对 Lorenz 规范下的平面波 $`A^\mu(x)=\epsilon^\mu(p)e^{-ip\cdot x}`$，

```math
\boxed{
p^2=0,\qquad p^0=|\mathbf p|>0,\qquad
p_\mu\epsilon^\mu=0,\qquad
\epsilon^\mu\sim\epsilon^\mu+\lambda p^\mu.
}
```

最后一式中，$`\lambda`$ 是剩余平面波规范变换的任意复系数。该约束与这一等价关系留下两个物理偏振。Coulomb 规范下的一组基满足

```math
\boxed{\begin{aligned}
\epsilon_r^0(p)&=0,\qquad
\mathbf p\cdot\boldsymbol\epsilon_r(p)=0,\qquad
\boldsymbol\epsilon_r^*(p)\cdot\boldsymbol\epsilon_s(p)=\delta_{rs},
\qquad r,s=1,2,\\
\sum_{r=1}^2\epsilon_r^i(p)\epsilon_r^{j*}(p)
&=\delta^{ij}-\frac{p^ip^j}{|\mathbf p|^2}.
\end{aligned}}
```

对无源波包，取 $`p^0=|\mathbf p|`$，该规范下的实场为：

```math
\boxed{
A^\mu(x)=\sum_{r=1}^2\int\frac{d^3p}{(2\pi)^3\,2|\mathbf p|}
\left[
a_r(\mathbf p)\epsilon_r^\mu(p)e^{-ip\cdot x}
+a_r^*(\mathbf p)\epsilon_r^{\mu*}(p)e^{+ip\cdot x}
\right].
}
```

$`a_r(\mathbf p)`$ 是经典复振幅。加上 $`\partial^\mu\lambda(x)`$ 即得其他规范代表元。

<br><br>

<a id="qft-ch2"></a>
## 2. 算符量子化


[1.4 节](#classical-dynamics)中的第一种观点自然导向算符量子化：空间位置标记自由度，而时间仍是演化参数。


<br><br>
<a id="canonical-quantization"></a>
### 2.1 正则量子化

考虑无约束的场 $`\phi_a(x)`$，其拉氏量密度为

```math
\mathcal L=\mathcal L(\phi_a,\partial_\mu\phi_a),
\qquad
L(t)=\int d^3x\,\mathcal L.
```

在每个固定时刻，场值构成无穷多个广义坐标：

```math
i\longleftrightarrow(a,\mathbf x),
\qquad
q_i(t)\longleftrightarrow\phi_a(t,\mathbf x).
```

**共轭动量**

与 $`\phi_a(t,\mathbf x)`$ 共轭的动量密度为

```math
\pi_a(t,\mathbf x)
\equiv
\frac{\delta L(t)}{\delta\dot\phi_a(t,\mathbf x)}
=
\frac{\partial\mathcal L}{\partial\dot\phi_a(t,\mathbf x)}.
```

**Poisson 括号与对易关系**

经典场满足等时正则 Poisson 括号

```math
\begin{aligned}
\{\phi_a(t,\mathbf x),\pi_b(t,\mathbf y)\}_{\mathrm{PB}}
&=\delta_{ab}\delta^{(3)}(\mathbf x-\mathbf y),\\
\{\phi_a(t,\mathbf x),\phi_b(t,\mathbf y)\}_{\mathrm{PB}}
&=\{\pi_a(t,\mathbf x),\pi_b(t,\mathbf y)\}_{\mathrm{PB}}=0.
\end{aligned}
```

正则量子化把场及其共轭动量提升为算符，并把这些基本 Poisson 括号按下式替换

```math
\{\ ,\ \}_{\mathrm{PB}}
\longrightarrow
\frac{1}{i}[\ ,\ ].
```

于是，

```math
\boxed{
\begin{aligned}
[\hat\phi_a(t,\mathbf x),\hat\pi_b(t,\mathbf y)]
&=i\,\delta_{ab}\delta^{(3)}(\mathbf x-\mathbf y),\\
[\hat\phi_a(t,\mathbf x),\hat\phi_b(t,\mathbf y)]
&=[\hat\pi_a(t,\mathbf x),\hat\pi_b(t,\mathbf y)]=0.
\end{aligned}}
```

这里 $`\delta_{ab}\delta^{(3)}(\mathbf x-\mathbf y)`$ 把 Kronecker δ 符号 $`\delta_{ij}`$ 推广到场标签 $`(a,\mathbf x)`$。

**自由实标量场**

对质量为 $`m`$ 的自由场，采用 Lorentz 不变测度 $`d\Pi_{\mathbf p}`$ 与正能四动量 $`p`$：

```math
\begin{aligned}
E_{\mathbf p}&=\sqrt{\mathbf p^2+m^2},\qquad p^0=E_{\mathbf p},\qquad d\Pi_{\mathbf p}:=\frac{d^3p}{(2\pi)^3\,2E_{\mathbf p}},\\
\hat\phi_I(x)&=\int d\Pi_{\mathbf p}\left(\hat a_{\mathbf p}e^{-ip\cdot x}+\hat a_{\mathbf p}^\dagger e^{+ip\cdot x}\right).
\end{aligned}
```

真空归一化为 1。产生算符定义协变归一化的单粒子态：

```math
\boxed{\begin{aligned}
[\hat a_{\mathbf p},\hat a_{\mathbf q}^\dagger]&=2E_{\mathbf p}(2\pi)^3\delta^{(3)}(\mathbf p-\mathbf q),\qquad
[\hat a_{\mathbf p},\hat a_{\mathbf q}]=[\hat a_{\mathbf p}^\dagger,\hat a_{\mathbf q}^\dagger]=0,\\
\hat a_{\mathbf p}|0\rangle&=0,\qquad |\mathbf p\rangle:=\hat a_{\mathbf p}^\dagger|0\rangle,\\
\langle\mathbf p|\mathbf q\rangle&=2E_{\mathbf p}(2\pi)^3\delta^{(3)}(\mathbf p-\mathbf q).
\end{aligned}}
```

正规序用冒号表示，它把产生算符放在湮灭算符的左边。减去真空能后，

```math
\begin{aligned}
:\hat H_0:&=\int d\Pi_{\mathbf p}\,E_{\mathbf p}\,\hat a_{\mathbf p}^\dagger\hat a_{\mathbf p},\qquad
:\hat{\mathbf P}:=\int d\Pi_{\mathbf p}\,\mathbf p\,\hat a_{\mathbf p}^\dagger\hat a_{\mathbf p},\\
\hat N&=\int d\Pi_{\mathbf p}\,\hat a_{\mathbf p}^\dagger\hat a_{\mathbf p}.
\end{aligned}
```

**自由 Dirac 场**

采用 [1.7 节](#dirac-field)的旋量及其归一化，算符 $`\hat b_{\mathbf p}^s`$ 与 $`\hat c_{\mathbf p}^s`$ 分别湮灭粒子与反粒子：

```math
\hat\psi_I(x)=\sum_{s=1}^{2}\int d\Pi_{\mathbf p}\left(\hat b_{\mathbf p}^s u^s(p)e^{-ip\cdot x}+\hat c_{\mathbf p}^{s\dagger}v^s(p)e^{+ip\cdot x}\right).
```

费米子的量子化使用反对易子；下面的 $`\alpha,\beta`$ 是 Dirac 分量指标。未列出的模式反对易子都为零，并且两种湮灭算符都湮灭 $`|0\rangle`$。

```math
\boxed{\begin{aligned}
\{\hat b_{\mathbf p}^r,\hat b_{\mathbf q}^{s\dagger}\}&=\{\hat c_{\mathbf p}^r,\hat c_{\mathbf q}^{s\dagger}\}=2E_{\mathbf p}(2\pi)^3\delta^{rs}\delta^{(3)}(\mathbf p-\mathbf q),\\
\{\hat\psi_{I,\alpha}(t,\mathbf x),\hat\psi_{I,\beta}^\dagger(t,\mathbf y)\}&=\delta_{\alpha\beta}\delta^{(3)}(\mathbf x-\mathbf y),\\
\{\hat\psi_{I,\alpha}(t,\mathbf x),\hat\psi_{I,\beta}(t,\mathbf y)\}&=0.
\end{aligned}}
```

费米子的正规序每交换一次费米子算符就引入一个负号。正规序后的能量、动量与净费米子数为

```math
\begin{aligned}
:\hat H_0:&=\sum_s\int d\Pi_{\mathbf p}\,E_{\mathbf p}\left(\hat b_{\mathbf p}^{s\dagger}\hat b_{\mathbf p}^s+\hat c_{\mathbf p}^{s\dagger}\hat c_{\mathbf p}^s\right),\\
:\hat{\mathbf P}:&=\sum_s\int d\Pi_{\mathbf p}\,\mathbf p\left(\hat b_{\mathbf p}^{s\dagger}\hat b_{\mathbf p}^s+\hat c_{\mathbf p}^{s\dagger}\hat c_{\mathbf p}^s\right),\\
\hat Q&:=\int d^3x:\hat\psi_I^\dagger\hat\psi_I:
=\sum_s\int d\Pi_{\mathbf p}\left(\hat b_{\mathbf p}^{s\dagger}\hat b_{\mathbf p}^s-\hat c_{\mathbf p}^{s\dagger}\hat c_{\mathbf p}^s\right).
\end{aligned}
```

<br><br>

<a id="quantization-with-dirac-brackets"></a>
### 2.2 用 Dirac 括号量子化

<a id="complex-scalar-field-quantization"></a>
#### 复标量场的量子化

<br><br>

<a id="dirac-field-quantization"></a>
#### Dirac 场的量子化

<br><br>

<a id="proca-field-quantization"></a>
#### Proca 场的量子化

<br><br>

<a id="gupta-bleuler-quantization"></a>
### 2.3 Gupta–Bleuler 量子化

<br><br>

<a id="symmetry"></a>
### 2.4 对称性

<a id="schrodinger-picture"></a>
#### Schrödinger 绘景

动力学完全由态承担；算符不随时间演化。这里称算符 $`\hat O`$ 随时间演化，是指更换哈密顿量 $`\hat H`$ 时，它对 $`t`$ 的依赖随之改变。

这并不排除 $`\hat O_S(t)`$ 显含时间；这种时间依赖由 $`\hat O_S`$ 的形式确定，与 $`\hat H`$ 无关。因此

```math
\begin{gathered}
\frac{d\hat O_S}{dt}=\frac{\partial\hat O_S}{\partial t},\\[4pt]
i\frac{\partial}{\partial t}|\psi_S(t)\rangle=\hat H|\psi_S(t)\rangle.
\end{gathered}
```

以 $`|\psi_S(t_0)\rangle`$ 为初态时，(2.13) 的解取决于 $`\hat H`$ 的时间依赖。

**(1) $`\hat H`$ 不显含时间**

若 $`\hat H`$ 不显含时间，(2.13) 的解为

```math
|\psi_S(t)\rangle=e^{-i\hat H(t-t_0)}\,|\psi_S(t_0)\rangle .
```

**(2) 不同时刻的 $`\hat H(t)`$ 对易**

设 $`\hat H=\hat H(t)`$ 显含 $`t`$，且对所有 $`t_1,t_2`$ 都有 $`[\hat H(t_1),\hat H(t_2)]=0`$。这里 $`\int_{t_0}^{t}dt'\,\hat H(t')`$ 指矩阵元为 $`\int_{t_0}^{t}dt'\,\langle\phi|\hat H(t')|\chi\rangle`$ 的算符。于是 $`\hat H(t)`$ 与 $`\int_{t_0}^{t}dt'\,\hat H(t')`$ 对易，并且

```math
\begin{aligned}
\frac{\partial}{\partial t}\Bigl(\int_{t_0}^{t}dt'\,\hat H(t')\Bigr)^n
&=\sum_{k=0}^{n-1}\Bigl(\int_{t_0}^{t}dt'\,\hat H(t')\Bigr)^k\,\hat H(t)\,\Bigl(\int_{t_0}^{t}dt'\,\hat H(t')\Bigr)^{n-1-k}\\
&=n\,\hat H(t)\Bigl(\int_{t_0}^{t}dt'\,\hat H(t')\Bigr)^{n-1}.
\end{aligned}
```

由 (2.15)，对 $`-i\int_{t_0}^{t}dt'\,\hat H(t')`$ 的指数级数逐项求导，相当于从左边乘以 $`-i\hat H(t)`$，因此

```math
|\psi_S(t)\rangle=\exp\Bigl(-i\int_{t_0}^{t}dt'\,\hat H(t')\Bigr)\,|\psi_S(t_0)\rangle ,
```

当 $`\hat H(t)=\hat H`$ 时，它化为 (2.14)。

**(3) 不同时刻的 $`\hat H(t)`$ 不对易**

一般情况下 $`[\hat H(t_1),\hat H(t_2)]\neq0`$；这时 (2.15) 的第二个等号不成立，(2.16) 也不再是 (2.13) 的解。此时改为对 (2.13) 积分并迭代：

```math
\begin{aligned}
|\psi_S(t)\rangle
&=|\psi_S(t_0)\rangle-i\int_{t_0}^{t}dt_1\,\hat H(t_1)\,|\psi_S(t_1)\rangle\\
&=\Bigl[1+(-i)\int_{t_0}^{t}dt_1\,\hat H(t_1)
+(-i)^2\int_{t_0}^{t}dt_1\int_{t_0}^{t_1}dt_2\,\hat H(t_1)\hat H(t_2)+\cdots\Bigr]|\psi_S(t_0)\rangle ,
\end{aligned}
```

其中第 $`n`$ 项的积分区域为 $`t\ge t_1\ge\cdots\ge t_n\ge t_0`$，较晚时刻的算符在左边。

定义编时乘积

```math
\mathcal T[\hat H(t_1)\hat H(t_2)]
:=\theta(t_1-t_2)\,\hat H(t_1)\hat H(t_2)+\theta(t_2-t_1)\,\hat H(t_2)\hat H(t_1),
```

$`n`$ 个算符的情形同理，按时间从左到右递减排列。$`\mathcal T[\hat H(t_1)\cdots\hat H(t_n)]`$ 在 $`t_1,\ldots,t_n`$ 的置换下对称；按 $`t_i`$ 的大小次序，立方体 $`[t_0,t]^n`$ 分成 $`n!`$ 个区域，各区域的贡献相等，而在 $`t_1>\cdots>t_n`$ 上，编时乘积就是 (2.17) 中的有序乘积。因此

```math
\int_{t_0}^{t}dt_1\int_{t_0}^{t_1}dt_2\cdots\int_{t_0}^{t_{n-1}}dt_n\,
\hat H(t_1)\cdots\hat H(t_n)
=\frac1{n!}\int_{t_0}^{t}dt_1\cdots\int_{t_0}^{t}dt_n\,
\mathcal T[\hat H(t_1)\cdots\hat H(t_n)],
```

于是 (2.17) 成为 Dyson 级数

```math
\boxed{
\begin{gathered}
|\psi_S(t)\rangle=\mathcal T\exp\Bigl(-i\int_{t_0}^{t}dt'\,\hat H(t')\Bigr)|\psi_S(t_0)\rangle,\\[4pt]
\mathcal T\exp\Bigl(-i\int_{t_0}^{t}dt'\,\hat H(t')\Bigr)
:=\sum_{n=0}^{\infty}\frac{(-i)^n}{n!}\int_{t_0}^{t}dt_1\cdots dt_n\,
\mathcal T[\hat H(t_1)\cdots\hat H(t_n)].
\end{gathered}
}
```

或者，把 (2.20) 的第 $`n`$ 项对 $`t`$ 求导：$`n`$ 个积分变量中的每一个都可以取上限 $`t`$，这时它是最晚的时刻，因此 $`\mathcal T`$ 把 $`\hat H(t)`$ 放在最左边；这 $`n`$ 个贡献相等，合起来给出 $`-i\hat H(t)`$ 乘以第 $`(n-1)`$ 项。所以该级数满足 (2.13)，并且在 $`t=t_0`$ 时等于 $`|\psi_S(t_0)\rangle`$；解是唯一的。若 $`[\hat H(t_1),\hat H(t_2)]=0`$，则可去掉 $`\mathcal T`$，(2.20) 化为 (2.16)。

**演化算符**

每种情形下，解都线性依赖于 $`|\psi_S(t_0)\rangle`$：

```math
|\psi_S(t)\rangle=\hat U(t,t_0)\,|\psi_S(t_0)\rangle,
\qquad
i\frac{\partial}{\partial t}\hat U(t,t_0)=\hat H(t)\,\hat U(t,t_0),
\qquad
\hat U(t_0,t_0)=1,
```

其中演化算符 $`\hat U(t,t_0)`$ 在情形 (1)、(2)、(3) 中分别为 $`e^{-i\hat H(t-t_0)}`$、$`\exp\bigl(-i\int_{t_0}^{t}dt'\,\hat H(t')\bigr)`$ 和 $`\mathcal T\exp\bigl(-i\int_{t_0}^{t}dt'\,\hat H(t')\bigr)`$。由于 $`\hat H(t)`$ 厄米，$`\partial_t(\hat U^\dagger\hat U)=i\hat U^\dagger(\hat H^\dagger-\hat H)\hat U=0`$，因此 $`\hat U(t,t_0)`$ 是幺正的。$`\hat U(t_2,t_1)\hat U(t_1,t_0)=\hat U(t_2,t_0)`$ 的两边作为 $`t_2`$ 的函数都满足 (2.21)，且在 $`t_2=t_1`$ 时相等，所以这一复合律成立；取 $`t_2=t_0`$ 即得 $`\hat U(t,t_0)^\dagger=\hat U(t_0,t)`$。

<br><br>

<a id="heisenberg-picture"></a>
#### Heisenberg 绘景

Heisenberg 绘景由 Schrödinger 绘景经如下变换得到

```math
\boxed{
\begin{gathered}
|\psi_H(t)\rangle:=\hat U(t,0)^\dagger\,|\psi_S(t)\rangle=|\psi_S(0)\rangle,\\[4pt]
\hat O_H(t):=\hat U(t,0)^\dagger\,\hat O_S(t)\,\hat U(t,0).
\end{gathered}
}
```

两个绘景在 $`t=0`$ 时重合，且 $`\langle\psi_H(t)|\hat O_H(t)|\psi_H(t)\rangle=\langle\psi_S(t)|\hat O_S(t)|\psi_S(t)\rangle`$。因此 $`i\partial_t|\psi_H(t)\rangle=0`$。

把 $`\hat U(t,0)`$ 简记为 $`\hat U`$，利用 (2.13) 与 (2.21) 对 (2.22) 的第二式求导，

```math
\begin{aligned}
\frac{d\hat O_H}{dt}
&=\Bigl(\frac{\partial\hat U}{\partial t}\Bigr)^\dagger\hat O_S\,\hat U
+\hat U^\dagger\,\frac{d\hat O_S}{dt}\,\hat U
+\hat U^\dagger\hat O_S\,\frac{\partial\hat U}{\partial t}\\
&=i\,\hat U^\dagger\bigl[\hat H(t),\hat O_S\bigr]\hat U
+\hat U^\dagger\,\frac{\partial\hat O_S}{\partial t}\,\hat U\\
&=i\bigl[\hat H_H(t),\hat O_H\bigr]+\Bigl(\frac{\partial\hat O_S}{\partial t}\Bigr)_H,
\end{aligned}
```

其中 $`\hat H_H(t):=\hat U^\dagger\hat H(t)\,\hat U`$，$`(\partial\hat O_S/\partial t)_H:=\hat U^\dagger(\partial\hat O_S/\partial t)\,\hat U`$；最后一步插入了 $`\hat U\hat U^\dagger=1`$。在情形 (1) 和 (2) 中，$`\hat U(t,0)`$ 与 $`\hat H(t)`$ 对易，因此 $`\hat H_H(t)=\hat H(t)`$。在情形 (1) 中，(2.22) 与 (2.23) 化为

```math
\begin{gathered}
\hat O_H(t)=e^{i\hat Ht}\,\hat O_S(t)\,e^{-i\hat Ht},\\[4pt]
\frac{d\hat O_H}{dt}=i[\hat H,\hat O_H]+\Bigl(\frac{\partial\hat O_S}{\partial t}\Bigr)_H .
\end{gathered}
```

<br><br>

<a id="qft-ch3"></a>
## 3. 标准模型

<a id="yang-mills"></a>
### 3.1 Yang–Mills 理论

**李群**

```math
\begin{aligned}
U(n)&=\{A\in M_n(\mathbb C)\mid A^\dagger A=I\},\\[6pt]
SU(n)&=\{A\in M_n(\mathbb C)\mid \det A=1,\ A^\dagger A=I\}.
\end{aligned}
```


**$`U(n)`$**

考虑单参数子群

```math
\begin{aligned}
g(\theta)&=e^{i\theta T},\qquad \theta\in\mathbb R,\quad T\in M_n(\mathbb C),\\[6pt]
\left.\frac{d}{d\theta}g(\theta)\right|_{\theta=0}&=iT,\\[6pt]
g^\dagger(\theta)g(\theta)=I\quad\text{对所有 }\theta\in\mathbb R
&\Longrightarrow i(T-T^\dagger)=0
\Longrightarrow T^\dagger=T.
\end{aligned}
```

 李代数为

```math
\mathfrak{u}(n)=\{iT\in M_n(\mathbb C)\mid T^\dagger=T\}.
```


**$`SU(n)`$**

单参数子群及其生成元为

```math
\begin{aligned}
g(\theta)&=e^{i\theta T},\qquad \theta\in\mathbb R,\quad T\in M_n(\mathbb C),\\[6pt]
\left.\frac{d}{d\theta}g(\theta)\right|_{\theta=0}&=iT.
\end{aligned}
```


```math
0=\left.\frac{d}{d\theta}\bigl[g^\dagger(\theta)g(\theta)\bigr]\right|_{\theta=0}
=i(T-T^\dagger)
\quad\Longrightarrow\quad T^\dagger=T.
```

我们用到定理 $`\det(e^{i\theta T})=e^{i\theta\,\mathop{\rm tr}\nolimits\,T}`$，它对任意 $`T\in M_n(\mathbb C)`$ 和 $`\theta\in\mathbb C`$ 成立。

```math
0=\left.\frac{d}{d\theta}\det g(\theta)\right|_{\theta=0}
=\left.\frac{d}{d\theta}e^{i\theta\,\mathop{\rm tr}\nolimits\,T}\right|_{\theta=0}
=i\,\mathop{\rm tr}\nolimits\,T
\quad\Longrightarrow\quad \mathop{\rm tr}\nolimits\,T=0.
```

因此 $`T`$ 是无迹的厄米矩阵，李代数为

```math
\mathfrak{su}(n)=\{iT\in M_n(\mathbb C)\mid
\mathop{\rm tr}\nolimits\,T=0,\ T^\dagger=T\}.
```

为保持反厄米性，数乘取在 $`\mathbb R`$ 上；因此 $`\mathfrak{su}(n)`$ 和 $`\mathfrak{u}(n)`$ 都是实李代数。

<a id="ym-4"></a>
**结构常数**

设 $`\{iT^a\}`$ 是实李代数 $`\mathfrak{su}(n)`$ 的一组基，其中 $`a=1,\ldots,n^2-1`$。
结构常数 $`f^{abc}`$ 由 $`[T^a,T^b]=if^{abc}T^c`$ 定义。

**实性：$`f^{abc}\in\mathbb R`$。**

由于矩阵 $`T^a`$ 厄米，

```math
\begin{aligned}
([T^a,T^b])^\dagger&=-[T^a,T^b],\qquad
\mathop{\rm tr}\nolimits [T^a,T^b]=0,\\[6pt]
[T^a,T^b]&\in\mathfrak{su}(n),\\[6pt]
[T^a,T^b]&=f^{abc}(iT^c),\qquad f^{abc}\in\mathbb R.
\end{aligned}
```

由于 $`\{iT^c\}`$ 是 $`\mathbb R`$ 上的基，展开系数为实数。

<a id="ym-orthonormal"></a>
**$`\mathfrak{su}(n)`$ 的正交归一基**

对 $`iT_1,iT_2\in\mathfrak{su}(n)`$，定义

```math
\begin{aligned}
(\cdot,\cdot)&:\mathfrak{su}(n)\times\mathfrak{su}(n)\longrightarrow\mathbb R,\\[6pt]
(iT_1,iT_2)&:=-2\,\mathop{\rm tr}\nolimits \bigl[(iT_1)(iT_2)\bigr]\\
&=2\,\mathop{\rm tr}\nolimits (T_1T_2).
\end{aligned}
```

**证明** (3.9) 满足内积公理



*(i) 实值性。*

利用 $`T_1^\dagger=T_1`$、$`T_2^\dagger=T_2`$ 以及迹的循环性，

```math
\begin{aligned}
\bigl[\mathop{\rm tr}\nolimits (T_1T_2)\bigr]^*
&=\mathop{\rm tr}\nolimits \bigl[(T_1T_2)^\dagger\bigr]
=\mathop{\rm tr}\nolimits (T_2^\dagger T_1^\dagger)\\
&=\mathop{\rm tr}\nolimits (T_2T_1)
=\mathop{\rm tr}\nolimits (T_1T_2),
\end{aligned}
```

因此 $`(iT_1,iT_2)=2\,\mathop{\rm tr}\nolimits (T_1T_2)\in\mathbb R`$。

*(ii) 对称性。*

由迹的循环性，

```math
\begin{aligned}
(iT_1,iT_2)&=2\,\mathop{\rm tr}\nolimits (T_1T_2)\\
&=2\,\mathop{\rm tr}\nolimits (T_2T_1)=(iT_2,iT_1).
\end{aligned}
```

*(iii) 双线性。*

对 $`a,b\in\mathbb R`$，有 $`a\,iT_1+b\,iT_2=i(aT_1+bT_2)`$，
再由迹的线性得 $`(a\,iT_1+b\,iT_2,\,iT_3)=2\,\mathop{\rm tr}\nolimits \bigl[(aT_1+bT_2)T_3\bigr]=a\,(iT_1,iT_3)+b\,(iT_2,iT_3)`$。由 (ii)，该形式对第二个宗量也是线性的。

*(iv) 正定性。* 利用 $`T=T^\dagger`$，

```math
\begin{aligned}
(iT,iT)&=2\,\mathop{\rm tr}\nolimits (T^2)=2\,\mathop{\rm tr}\nolimits (T^\dagger T)\\
&=2\sum_{j,k}|T_{jk}|^2\ge0.
\end{aligned}
```

等号成立当且仅当对所有 $`j,k`$ 都有 $`T_{jk}=0`$，即 $`iT=0`$。$`\square`$

既然已证明该形式是 $`\mathfrak{su}(n)`$ 上的内积，就可以选取满足 $`(iT^a,iT^b)=\delta^{ab}`$ 的正交归一基 $`\{iT^a\}`$。等价地，

```math
\boxed{\mathop{\rm tr}\nolimits (T^aT^b)=\frac12\delta^{ab}.}
```

**全反对称性**。利用这一归一化与迹的循环性，得到

```math
\begin{aligned}
\mathop{\rm tr}\nolimits ([T^a,T^b]T^c)&=\frac{i}{2}f^{abc},\\
f^{abc}&=-2i\,\mathop{\rm tr}\nolimits ([T^a,T^b]T^c),\\
f^{bac}&=-f^{abc},\\
f^{acb}
&=-2i\,\mathop{\rm tr}\nolimits (T^aT^cT^b-T^cT^aT^b)\\
&=-2i\,\mathop{\rm tr}\nolimits (T^bT^aT^c-T^aT^bT^c)
=-f^{abc}.
\end{aligned}
```

```math
\boxed{
f^{abc}=f^{[abc]}\in\mathbb R
}
```

<a id="ym-5"></a>
**局域对称性与协变导数**

纤维丛为 Yang–Mills 理论中的场提供了一幅有用的几何图像。
在这幅图像中，每个时空点上附着一个内部空间，场在该点取值于这个空间。
这使一种额外的自由变得明显：我们可以在每个内部空间中选取一组基，
并且这种选取可以逐点变化。
这种局域的选取自由是规范对称性的基础。

基于这一想法，下面建立规范理论的框架。

场算符定义为

```math
\Psi(x):=\begin{pmatrix}
\psi_1(x)\\
\vdots\\
\psi_n(x)
\end{pmatrix}.
```

Dirac 共轭定义为

```math
\begin{aligned}
\bar\Psi(x)&:=\bigl(\bar\psi_1(x),\ldots,\bar\psi_n(x)\bigr),\\[6pt]
\bar\psi_a(x)&:=\psi_a^\dagger(x)\gamma^0.
\end{aligned}
```

拉氏量密度的动能项为

```math
\begin{aligned}
\mathcal L_{\mathrm{kin}}
&=\bar\Psi\,i\gamma^\mu I_n\partial_\mu\Psi\\[6pt]
&=\sum_{a=1}^{n}\bar\psi_a\,i\gamma^\mu\partial_\mu\psi_a.
\end{aligned}
```



对定义表示 $`U`$ 下的 $`SU(n)`$，设 $`g_{\mathrm{YM}}`$ 为耦合常数，$`U(\theta)`$ 为局域群元的表示。联络及其变换为

```math
\begin{aligned}
U(\theta)&:=e^{i\theta^a(x)T^a},\qquad \theta^a(x)\in\mathbb R,\\
A_\mu&:=A_\mu^aT^a,\qquad D_\mu:=\partial_\mu-ig_{\mathrm{YM}}A_\mu,
\qquad \Psi'=U(\theta)\Psi,\\
A_\mu'&=U(\theta)A_\mu U(\theta)^\dagger-\frac{i}{g_{\mathrm{YM}}}\bigl(\partial_\mu U(\theta)\bigr)U(\theta)^\dagger,\\
D_\mu'&=U(\theta)D_\mu U(\theta)^\dagger .
\end{aligned}
```

场强为

```math
\begin{aligned}
[D_\mu,D_\nu]&=:-ig_{\mathrm{YM}}F_{\mu\nu},\\
F_{\mu\nu}&=\partial_\mu A_\nu-\partial_\nu A_\mu-ig_{\mathrm{YM}}[A_\mu,A_\nu],\\
F_{\mu\nu}^a&=\partial_\mu A_\nu^a-\partial_\nu A_\mu^a
+g_{\mathrm{YM}}f^{abc}A_\mu^bA_\nu^c,\\
F_{\mu\nu}'&=U(\theta)F_{\mu\nu}U(\theta)^\dagger .
\end{aligned}
```

计入规范场后，动能项 (3.18) 变为

```math
\boxed{
\begin{aligned}
\mathcal L_{\mathrm{kin}}
&=\bar\Psi\,i\gamma^\mu D_\mu\Psi
-\frac12\,\mathop{\rm tr}\nolimits (F_{\mu\nu}F^{\mu\nu})\\[6pt]
&=\bar\Psi\,i\gamma^\mu D_\mu\Psi-\frac14F_{\mu\nu}^aF^{a\mu\nu}.
\end{aligned}
}
```

对取矩阵值的伴随场 $`X`$，定义 $`D_\mu X:=\partial_\mu X-ig_{\mathrm{YM}}[A_\mu,X]`$。

利用以上定义，场方程与 Bianchi 恒等式简化为

```math
\begin{aligned}
i\gamma^\mu D_\mu\Psi&=0,\qquad
D_\mu F^{\mu\nu}=-g_{\mathrm{YM}}j^\nu,\qquad
j^\nu:=(\bar\Psi\gamma^\nu T^a\Psi)T^a,\\
D_\mu F_{\nu\rho}+D_\nu F_{\rho\mu}+D_\rho F_{\mu\nu}&=0 .
\end{aligned}
```

<br><br>

<a id="qed"></a>
### 3.2 量子电动力学


**规范群 $`U(1)`$**

QED 的规范群是 $`U(1)`$，即 (3.1) 取 $`n=1`$；其李代数 $`\mathfrak u(1)=i\mathbb R`$ 是阿贝尔的。

设 $`e>0`$ 为元电荷，$`\theta:\mathbb R^4\to\mathbb R`$。该变换是味单态：它对三代的作用相同。它在 $`U(1)`$ 的不同表示上取不同的形式，这些表示以荷标记：如 (1.94) 的 Dirac 场 $`\psi_f`$ 带荷 $`Q_fe`$，对每个 $`f`$ 取同一个 $`\theta`$，其变换为

```math
\begin{aligned}
\psi_f'(x)&=e^{iQ_f\theta(x)}\psi_f(x),\qquad
\bar\psi_f'(x)=\bar\psi_f(x)\,e^{-iQ_f\theta(x)},\\[6pt]
Q_f&=\begin{cases}
\tfrac23, & f=u,c,t,\\
-\tfrac13, & f=d,s,b,\\
-1, & f=e,\mu,\tau,\\
0, & f=\nu_e,\nu_\mu,\nu_\tau.
\end{cases}
\end{aligned}
```

**协变导数与场强**

光子场 $`A_\mu`$ 是实场。在 (3.19)–(3.20) 中取 $`U(\theta)=e^{iQ\theta}`$，并把 $`g_{\mathrm{YM}}A_\mu`$ 换成 $`eQA_\mu`$，得到

```math
\begin{aligned}
D_\mu&:=\partial_\mu-ieQA_\mu,\qquad
D_\mu'\psi'=e^{iQ\theta}D_\mu\psi,\\
A_\mu'&=A_\mu+\frac1e\,\partial_\mu\theta,\\
[D_\mu,D_\nu]&=-ieQF_{\mu\nu},\qquad
F_{\mu\nu}=\partial_\mu A_\nu-\partial_\nu A_\mu=F_{\mu\nu}'.
\end{aligned}
```



**QED 拉氏量**

```math
\boxed{
\mathcal L_{\mathrm{QED}}
=\bar\psi\bigl(i\gamma^\mu D_\mu-m\bigr)\psi
-\frac14F_{\mu\nu}F^{\mu\nu},
}
```

其中 $`m`$ 是 $`\psi`$ 的质量，$`D_\mu`$ 作用于其右侧的 $`\psi`$。由 (3.23)–(3.24)，$`\mathcal L_{\mathrm{QED}}`$ 是规范不变的。代入 $`D_\mu`$，

```math
\mathcal L_{\mathrm{QED}}
=\bar\psi\bigl(i\gamma^\mu\partial_\mu-m\bigr)\psi
-\frac14F_{\mu\nu}F^{\mu\nu}
+eQA_\mu\bar\psi\gamma^\mu\psi,
```

即 Dirac 拉氏量 (1.94)、Maxwell 拉氏量 (1.147) 与相互作用项之和。



**运动方程**

取 (1.132) 中的 $`j^\nu=\bar\psi\gamma^\nu\psi`$，则 $`\partial\mathcal L_{\mathrm{QED}}/\partial(\partial_\mu A_\nu)=-F^{\mu\nu}`$，$`\partial\mathcal L_{\mathrm{QED}}/\partial A_\nu=eQ\,j^\nu`$。Euler–Lagrange 方程与 Bianchi 恒等式为

```math
\begin{aligned}
\bigl(i\gamma^\mu D_\mu-m\bigr)\psi&=0,\qquad
\partial_\mu F^{\mu\nu}=-eQ\,j^\nu,\qquad
\partial_\nu j^\nu=0,\\
\partial_\mu F_{\nu\rho}+\partial_\nu F_{\rho\mu}+\partial_\rho F_{\mu\nu}&=0 .
\end{aligned}
```

<br><br>

<a id="qcd"></a>
### 3.3 量子色动力学

**色群 $`SU(3)`$**

QCD 的规范群为 $`SU(3)`$。由 (3.7) 取 $`n=3`$，$`\mathfrak{su}(3)`$ 有一组基 $`\{iT^a\}`$，$`a=1,\ldots,8`$，我们取它在 (3.13) 的意义下正交归一。标准的选取是 $`T^a:=\tfrac12\lambda^a`$，其中 Gell-Mann 矩阵为

```math
\begin{aligned}
\lambda^1&=\begin{pmatrix}0&1&0\\1&0&0\\0&0&0\end{pmatrix},&
\lambda^2&=\begin{pmatrix}0&-i&0\\i&0&0\\0&0&0\end{pmatrix},&
\lambda^3&=\begin{pmatrix}1&0&0\\0&-1&0\\0&0&0\end{pmatrix},\\[6pt]
\lambda^4&=\begin{pmatrix}0&0&1\\0&0&0\\1&0&0\end{pmatrix},&
\lambda^5&=\begin{pmatrix}0&0&-i\\0&0&0\\i&0&0\end{pmatrix},&
\lambda^6&=\begin{pmatrix}0&0&0\\0&0&1\\0&1&0\end{pmatrix},\\[6pt]
\lambda^7&=\begin{pmatrix}0&0&0\\0&0&-i\\0&i&0\end{pmatrix},&
\lambda^8&=\frac1{\sqrt3}\begin{pmatrix}1&0&0\\0&1&0\\0&0&-2\end{pmatrix}.
\end{aligned}
```

每个 $`\lambda^a`$ 都是厄米、无迹的，并且 $`\mathop{\rm tr}\nolimits (\lambda^a\lambda^b)=2\delta^{ab}`$，因此 $`\mathop{\rm tr}\nolimits (T^aT^b)=\tfrac12\delta^{ab}`$，与 (3.13) 一致。由 (3.14)，$`f^{abc}=-2i\,\mathop{\rm tr}\nolimits ([T^a,T^b]T^c)`$；在反对称性 (3.15) 的意义下，非零的结构常数为

```math
\begin{aligned}
f^{123}&=1,\\[4pt]
f^{147}=f^{246}=f^{257}=f^{345}&=\tfrac12,\qquad
f^{156}=f^{367}=-\tfrac12,\\[4pt]
f^{458}=f^{678}&=\tfrac{\sqrt3}{2}.
\end{aligned}
```

由于 $`f^{bac}`$ 对 $`a,c`$ 反对称，二次 Casimir 算符 $`T^aT^a`$ 与每个 $`T^b`$ 对易：

```math
[T^b,T^aT^a]=[T^b,T^a]T^a+T^a[T^b,T^a]=if^{bac}\bigl(T^cT^a+T^aT^c\bigr)=0.
```

$`SU(3)`$ 的定义表示不可约，因此由 Schur 引理，$`T^aT^a=C_FI_3`$。利用 (3.13) 取迹，

```math
3C_F=\mathop{\rm tr}\nolimits (T^aT^a)=\tfrac12\cdot8
\quad\Longrightarrow\quad
\boxed{T^aT^a=C_FI_3,\qquad C_F=\tfrac43.}
```

**夸克场**

对每种味 $`f\in\{u,d,s,c,b,t\}`$，夸克场是色三重态，即取 $`n=3`$ 的多重态 (3.16)，其 Dirac 共轭同 (3.17)：

```math
q_f(x):=\begin{pmatrix}\psi_{f,1}(x)\\\psi_{f,2}(x)\\\psi_{f,3}(x)\end{pmatrix},
\qquad
\bar q_f(x):=\bigl(\bar\psi_{f,1}(x),\bar\psi_{f,2}(x),\bar\psi_{f,3}(x)\bigr).
```

本节中 $`\gamma^\mu`$ 作用于每个 $`\psi_{f,a}`$ 的旋量指标，$`3\times3`$ 矩阵 $`T^a`$ 作用于色指标，因此 $`\gamma^\mu`$ 与由 $`T^a`$ 构成的任何矩阵都对易。

**局域 $`SU(3)`$ 变换**

设 $`\theta^a:\mathbb R^4\to\mathbb R`$，$`a=1,\ldots,8`$，并令

```math
g(x):=e^{i\theta^a(x)T^a}\in SU(3).
```

这就是 (1.66) 的内部变换，只是现在 $`g`$ 依赖于 $`x`$。夸克场的变换为

```math
q_f'(x)=g(x)\,q_f(x),\qquad
\bar q_f'(x)=\bar q_f(x)\,g^\dagger(x).
```

由于 $`\partial_\mu(gq_f)=g\,\partial_\mu q_f+(\partial_\mu g)\,q_f`$，(3.18) 的导数项在 (3.34) 下并非不变：

```math
\bar q_f'\,i\gamma^\mu\partial_\mu q_f'
=\bar q_f\,i\gamma^\mu\partial_\mu q_f
+\bar q_f\,i\gamma^\mu g^\dagger(\partial_\mu g)\,q_f.
```

**协变导数与胶子场**

引入八个实矢量场 $`A^a_\mu`$，即胶子场，并定义

```math
A_\mu:=A^a_\mu T^a,\qquad
D_\mu:=\partial_\mu-ig_sA_\mu,
```

其中 $`g_s\in\mathbb R`$ 为强耦合常数，$`D_\mu`$ 作用于色三重态。记变换后的胶子场为 $`A_\mu'`$，并令 $`D_\mu':=\partial_\mu-ig_sA_\mu'`$。要求 $`D_\mu'q_f'=g\,D_\mu q_f`$：

```math
\begin{aligned}
D_\mu'(gq_f)&=g\,\partial_\mu q_f+(\partial_\mu g)\,q_f-ig_sA_\mu'\,g\,q_f,\\[6pt]
g\,D_\mu q_f&=g\,\partial_\mu q_f-ig_s\,gA_\mu\,q_f.
\end{aligned}
```

令两式对所有 $`q_f`$ 相等，得 $`A_\mu'g=gA_\mu-\frac{i}{g_s}\partial_\mu g`$，即

```math
\boxed{
A_\mu'=gA_\mu g^\dagger-\frac{i}{g_s}(\partial_\mu g)\,g^\dagger
=gA_\mu g^\dagger+\frac{i}{g_s}\,g\,\partial_\mu g^\dagger.
}
```

对 $`gg^\dagger=I_3`$ 求导得 $`\bigl((\partial_\mu g)g^\dagger\bigr)^\dagger=-(\partial_\mu g)g^\dagger`$；Jacobi 公式 $`\partial_\mu\det g=\det g\,\mathop{\rm tr}\nolimits (g^\dagger\partial_\mu g)`$ 结合 $`\det g=1`$ 给出 $`\mathop{\rm tr}\nolimits \bigl((\partial_\mu g)g^\dagger\bigr)=0`$。因此 $`A_\mu'`$ 仍是厄米、无迹的，$`A_\mu'=A_\mu'^aT^a`$，其中 $`A_\mu'^a`$ 为实数。

由于 $`D_\mu'(gq_f)=g\,D_\mu q_f`$ 对所有 $`q_f`$ 成立，作为作用于色三重态的算符，有

```math
D_\mu'=g\,D_\mu\,g^\dagger.
```

对无穷小的 $`\theta^a`$，$`g=I_3+i\theta^aT^a+O(\theta^2)`$，由 (3.38) 得

```math
\begin{aligned}
A_\mu'&=A_\mu+i\theta^b[T^b,A_\mu]+\frac1{g_s}(\partial_\mu\theta^a)T^a+O(\theta^2)\\
&=A_\mu-f^{bca}\theta^bA^c_\mu T^a+\frac1{g_s}(\partial_\mu\theta^a)T^a+O(\theta^2),\\[6pt]
\delta A^a_\mu:=A_\mu'^a-A_\mu^a
&=\frac1{g_s}\partial_\mu\theta^a+f^{abc}A^b_\mu\theta^c+O(\theta^2).
\end{aligned}
```

**场强**

用 $`[D_\mu,D_\nu]=:-ig_sF_{\mu\nu}`$ 定义 $`F_{\mu\nu}`$。由于 $`[\partial_\mu,A_\nu]q_f=(\partial_\mu A_\nu)q_f`$，

```math
\begin{aligned}
[D_\mu,D_\nu]
&=[\partial_\mu-ig_sA_\mu,\ \partial_\nu-ig_sA_\nu]\\
&=-ig_s\bigl(\partial_\mu A_\nu-\partial_\nu A_\mu\bigr)-g_s^2[A_\mu,A_\nu],\\[6pt]
F_{\mu\nu}&=\partial_\mu A_\nu-\partial_\nu A_\mu-ig_s[A_\mu,A_\nu].
\end{aligned}
```

按基展开，$`F_{\mu\nu}=F^a_{\mu\nu}T^a`$，其中

```math
\boxed{
F^a_{\mu\nu}=\partial_\mu A^a_\nu-\partial_\nu A^a_\mu+g_sf^{abc}A^b_\mu A^c_\nu.
}
```

由 (3.39)，$`[D_\mu',D_\nu']=g[D_\mu,D_\nu]g^\dagger`$，因此

```math
F_{\mu\nu}'=gF_{\mu\nu}g^\dagger,
\qquad
\delta F^a_{\mu\nu}=f^{abc}F^b_{\mu\nu}\theta^c+O(\theta^2).
```

由迹的循环性及 (3.13)，

```math
\mathop{\rm tr}\nolimits \bigl(F_{\mu\nu}'F'^{\mu\nu}\bigr)
=\mathop{\rm tr}\nolimits \bigl(F_{\mu\nu}F^{\mu\nu}\bigr)
=\tfrac12F^a_{\mu\nu}F^{a\mu\nu}.
```

**QCD 拉氏量**

```math
\boxed{
\mathcal L_{\mathrm{QCD}}
=\sum_{f}\bar q_f\bigl(i\gamma^\mu D_\mu-m_f\bigr)q_f
-\frac12\,\mathop{\rm tr}\nolimits \bigl(F_{\mu\nu}F^{\mu\nu}\bigr)
=\sum_{f}\bar q_f\bigl(i\gamma^\mu D_\mu-m_f\bigr)q_f
-\frac14F^a_{\mu\nu}F^{a\mu\nu},
}
```

其中求和遍及 (3.32) 中的六种味，$`m_f`$ 为味 $`f`$ 的质量，$`D_\mu`$ 作用于其右侧的 $`q_f`$。在 (3.34) 与 (3.38) 下，按构造有 $`D_\mu'q_f'=g\,D_\mu q_f`$，因此

```math
\bar q_f'\bigl(i\gamma^\mu D_\mu'-m_f\bigr)q_f'
=\bar q_f\,g^\dagger\bigl(i\gamma^\mu g\,D_\mu-m_f\,g\bigr)q_f
=\bar q_f\bigl(i\gamma^\mu D_\mu-m_f\bigr)q_f.
```

结合 (3.44)，$`\mathcal L_{\mathrm{QCD}}`$ 在局域变换 (3.34)、(3.38) 下不变。

把 (3.36) 与 (3.42) 代入 (3.45)，即可分出自由项与相互作用项：

```math
\begin{aligned}
\mathcal L_{\mathrm{QCD}}
={}&\sum_f\bar q_f\bigl(i\gamma^\mu\partial_\mu-m_f\bigr)q_f
-\frac14\bigl(\partial_\mu A^a_\nu-\partial_\nu A^a_\mu\bigr)\bigl(\partial^\mu A^{a\nu}-\partial^\nu A^{a\mu}\bigr)\\[6pt]
&+g_sA^a_\mu\sum_f\bar q_f\gamma^\mu T^aq_f
-\frac{g_s}{2}f^{abc}\bigl(\partial_\mu A^a_\nu-\partial_\nu A^a_\mu\bigr)A^{b\mu}A^{c\nu}
-\frac{g_s^2}{4}f^{abc}f^{ade}A^b_\mu A^c_\nu A^{d\mu}A^{e\nu}.
\end{aligned}
```

**运动方程**

把 $`q_f`$、$`\bar q_f`$ 与 $`A^a_\mu`$ 视为独立变量，$`\bar q_f`$ 的 Euler–Lagrange 方程为

```math
\bigl(i\gamma^\mu D_\mu-m_f\bigr)q_f=0.
```

对 $`A^a_\nu`$，定义色流 $`j^{a\nu}:=\sum_f\bar q_f\gamma^\nu T^aq_f`$。由 (3.45) 并利用 (3.42) 与 (3.47)，

```math
\begin{aligned}
\frac{\partial\mathcal L_{\mathrm{QCD}}}{\partial(\partial_\mu A^a_\nu)}
&=-\frac12F^{b\rho\sigma}\,\delta^{ab}\bigl(\delta^\mu_\rho\delta^\nu_\sigma-\delta^\mu_\sigma\delta^\nu_\rho\bigr)
=-F^{a\mu\nu},\\[6pt]
\frac{\partial\mathcal L_{\mathrm{QCD}}}{\partial A^a_\nu}
&=g_sj^{a\nu}-\frac12F^{b\rho\sigma}\,g_s\bigl(f^{bad}\delta^\nu_\rho A^d_\sigma+f^{bca}A^c_\rho\delta^\nu_\sigma\bigr)\\
&=g_sj^{a\nu}-g_sf^{abc}A^c_\mu F^{b\mu\nu}\\
&=g_sj^{a\nu}+g_sf^{abc}A^b_\mu F^{c\mu\nu}.
\end{aligned}
```

于是 Euler–Lagrange 方程 $`\partial_\mu\bigl(\partial\mathcal L_{\mathrm{QCD}}/\partial(\partial_\mu A^a_\nu)\bigr)=\partial\mathcal L_{\mathrm{QCD}}/\partial A^a_\nu`$ 化为

```math
\boxed{
\partial_\mu F^{a\mu\nu}+g_sf^{abc}A^b_\mu F^{c\mu\nu}=-g_sj^{a\nu}.
}
```

左边是 $`\partial_\mu F^{\mu\nu}-ig_s[A_\mu,F^{\mu\nu}]`$ 的 $`a`$ 分量，后者是 $`F^{\mu\nu}`$ 在伴随表示中的协变导数；令 $`j^\nu:=j^{a\nu}T^a`$，(3.50) 即

```math
D_\mu F^{\mu\nu}:=\partial_\mu F^{\mu\nu}-ig_s[A_\mu,F^{\mu\nu}]=-g_s\,j^\nu.
```

<br><br>

<a id="higgs-mechanism"></a>
### 3.4 自发对称性破缺与 Higgs 机制

<a id="higgs-lagrangian"></a>
#### Higgs 拉氏量

设 $`\Phi:=(\phi_1,\ldots,\phi_n)^T`$ 为复标量场构成的多重态。对 $`\mu_H^2\in\mathbb R`$ 与 $`\lambda_H>0`$，Higgs 拉氏量为

```math
\boxed{
\begin{aligned}
\mathcal L_{\mathrm{Higgs}}&=(\partial_\mu\Phi)^\dagger\partial^\mu\Phi-V(\Phi),\\
V(\Phi)&=-\mu_H^2\,\Phi^\dagger\Phi+\lambda_H(\Phi^\dagger\Phi)^2 .
\end{aligned}
}
```

拉氏量 (3.52) 只通过 $`\Phi^\dagger\Phi`$ 与 $`(\partial_\mu\Phi)^\dagger\partial^\mu\Phi`$ 依赖于 $`\Phi`$。对常数 $`g\in U(n)`$，

```math
\begin{aligned}
\Phi'&=g\,\Phi,\\
\Phi'^\dagger\Phi'&=\Phi^\dagger g^\dagger g\,\Phi=\Phi^\dagger\Phi,\\
(\partial_\mu\Phi')^\dagger\partial^\mu\Phi'&=(\partial_\mu\Phi)^\dagger g^\dagger g\,\partial^\mu\Phi=(\partial_\mu\Phi)^\dagger\partial^\mu\Phi,
\end{aligned}
```

因此 $`\mathcal L_{\mathrm{Higgs}}`$ 在全局 $`U(n)`$ 变换下不变。

**物理真空**

经典真空是能量最低的场位形。(3.52) 的能量密度为

```math
\mathcal H=(\partial_0\Phi)^\dagger\partial_0\Phi+\sum_{i=1}^3(\partial_i\Phi)^\dagger\partial_i\Phi+V(\Phi).
```

前两项非负，因此经典真空是使 $`V`$ 取最小值的常数 $`\Phi=\Phi_0`$。由于 $`\partial V/\partial(\Phi^\dagger\Phi)=-\mu_H^2+2\lambda_H\Phi^\dagger\Phi`$ 且 $`\Phi^\dagger\Phi\ge0`$，

```math
\boxed{
\begin{aligned}
\mu_H^2\le0:&\quad\Phi_0=0,\\
\mu_H^2>0:&\quad\Phi_0^\dagger\Phi_0=\frac{v^2}{2},\qquad
v:=\sqrt{\frac{\mu_H^2}{\lambda_H}},\qquad
V(\Phi_0)=-\frac{\lambda_Hv^4}{4}.
\end{aligned}
}
```

当 $`\mu_H^2\le0`$ 时，真空 $`\Phi_0=0`$ 在整个 $`U(n)`$ 下不变。以下取 $`\mu_H^2>0`$：真空构成 $`\mathbb C^n`$ 中的球面 $`\Phi_0^\dagger\Phi_0=v^2/2`$，而 $`\Phi=0`$ 是 $`V`$ 的局部极大点。物理真空是这个球面上的一个点。选取

```math
\boxed{
\Phi_0:=\frac1{\sqrt2}\begin{pmatrix}0\\\vdots\\0\\v\end{pmatrix}
}
```

此后 $`\Phi_0`$ 即表示这一真空。

 任一满足 $`\Phi_0'^\dagger\Phi_0'=v^2/2`$ 的真空 $`\Phi_0'`$ 都等于 $`g\,\Phi_0`$，其中 $`g\in U(n)`$ 的最后一列为 $`\sqrt2\,\Phi_0'/v`$，其余各列把它补全为 $`\mathbb C^n`$ 的正交归一基；由 (3.53)，不同的选取之间由对称变换相联系。

<br><br>

<a id="spontaneous-symmetry-breaking"></a>
#### 自发对称性破缺

若变换 $`g\in U(n)`$ 保持真空不变，则称它是未破缺的。未破缺子群为

```math
\boxed{
G_0:=\{g\in U(n)\mid g\,\Phi_0=\Phi_0\}\cong U(n-1).
}
```

满足 $`g\Phi_0=\Phi_0`$ 的幺正矩阵 $`g`$ 把正交补 $`\Phi_0^\perp:=\{u\in\mathbb C^n\mid\Phi_0^\dagger u=0\}`$ 映到自身，而 $`g\mapsto g|_{\Phi_0^\perp}`$ 把 $`G_0`$ 等同于 $`(n-1)`$ 维空间 $`\Phi_0^\perp`$ 上的幺正群。

若 $`G_0\neq U(n)`$，即拉氏量在 $`U(n)`$ 下不变而真空不是，则称 $`U(n)`$ 自发破缺到 $`G_0`$；由 (3.57)，$`U(n)`$ 自发破缺到 $`G_0\cong U(n-1)`$。

设 $`T^a`$，$`a=1,\ldots,n^2`$，为 $`U(n)`$ 的厄米生成元，满足 $`\mathop{\rm tr}\nolimits (T^aT^b)=\frac12\delta^{ab}`$。若对所有 $`\theta\in\mathbb R`$ 都有 $`e^{i\theta T}\in G_0`$，则称厄米 $`n\times n`$ 矩阵 $`T`$ 为未破缺生成元；将 $`e^{i\theta T}\Phi_0=\Phi_0`$ 在 $`\theta=0`$ 处求导，

```math
e^{i\theta T}\in G_0\ \ \text{对所有 }\theta\in\mathbb R
\iff T\Phi_0=0 .
```

未破缺生成元构成 $`G_0\cong U(n-1)`$ 的李代数，维数为 $`(n-1)^2`$；破缺生成元是这个李代数关于 $`\mathop{\rm tr}\nolimits\,`$ 的正交补中的元素，正交补的维数为 $`n^2-(n-1)^2=2n-1`$。破缺的 $`T\neq0`$ 满足 $`T\Phi_0\neq0`$：否则 $`T`$ 也是未破缺的，从而 $`\mathop{\rm tr}\nolimits (T^2)=0`$。

设 $`G^a`$，$`a=1,\ldots,2n-1`$，为破缺生成元的一组基。矩阵 $`\Phi_0^\dagger\{G^a,G^b\}\Phi_0=2\,\mathop{\rm Re}\nolimits \bigl[(G^a\Phi_0)^\dagger G^b\Phi_0\bigr]`$ 是实对称矩阵。正交基变换 $`G^a\to O^{ab}G^b`$，$`O\in O(2n-1)`$，保持 $`\mathop{\rm tr}\nolimits (G^aG^b)=\frac12\delta^{ab}`$ 不变，并以 $`O(\,\cdot\,)O^T`$ 的方式作用于这个矩阵；选取 $`O`$ 使它对角化，

```math
\begin{aligned}
\mathop{\rm tr}\nolimits (G^aG^b)&=\frac12\delta^{ab},\\
\Phi_0^\dagger\{G^a,G^b\}\Phi_0&=2\,\delta^{ab}\,\Phi_0^\dagger(G^a)^2\Phi_0,\qquad
\Phi_0^\dagger(G^a)^2\Phi_0=(G^a\Phi_0)^\dagger G^a\Phi_0>0 .
\end{aligned}
```

此后对 $`a=1,\ldots,2n-1`$ 取 $`T^a:=G^a`$，而 $`T^a`$，$`a=2n,\ldots,n^2`$，张成未破缺生成元的空间。


**Higgs 场的参数化**

用 Higgs 场 $`h`$ 以及沿破缺生成元方向的 $`\theta^a`$，$`a=1,\ldots,2n-1`$，参数化 $`\Phi`$ 的 $`2n`$ 个实场：

```math
\boxed{
\begin{aligned}
\Phi&=\frac1{\sqrt2}\,e^{i\theta^a(x)G^a}\begin{pmatrix}0\\\vdots\\0\\v+h\end{pmatrix}\\
&=\Bigl(1+\frac hv\Bigr)U(\theta)\,\Phi_0,\\
U(\theta)&:=e^{iX},\qquad X:=\theta^a(x)G^a .
\end{aligned}
}
```

<br><br>

<a id="higgs-mechanism-masses"></a>
#### Higgs 机制

将 $`U(n)`$ 对称性 (3.53) 规范化：生成元取 (3.59) 之后选定的 $`T^a`$，$`a=1,\ldots,n^2`$，规范场为 $`A_\mu^a`$，耦合 $`g_{\mathrm{YM}}`$ 同 (3.19)。把 (3.52) 中的 $`\partial_\mu`$ 换成 $`D_\mu`$，并加上 (3.21) 的规范场动能项，

```math
\boxed{
\begin{aligned}
\mathcal L&=(D_\mu\Phi)^\dagger D^\mu\Phi-V(\Phi)-\frac14F_{\mu\nu}^aF^{a\mu\nu},\\
D_\mu\Phi&=\partial_\mu\Phi-ig_{\mathrm{YM}}A_\mu\Phi,\qquad A_\mu:=A_\mu^aT^a .
\end{aligned}
}
```

由 (3.19)–(3.20)，取 $`T^a`$ 为 $`U(n)`$ 的生成元，$`\mathcal L`$ 在 $`\Phi'=U(\theta)\Phi`$，$`U(\theta)=e^{i\theta^a(x)T^a}`$ 下不变；当 $`\theta^a=0`$，$`a\ge2n`$ 时，这就是 (3.60) 的 $`U(\theta)`$。

把参数化 (3.60) 代入 (3.61)。利用 (3.55) 给出的 $`\mu_H^2=\lambda_Hv^2`$ 以及 $`U^\dagger U=I_n`$，势只依赖于 $`h`$：

```math
\begin{aligned}
\Phi^\dagger\Phi&=\frac{(v+h)^2}2,\\
V&=\lambda_H\Bigl(\Phi^\dagger\Phi-\frac{v^2}2\Bigr)^2-\frac{\lambda_Hv^4}4\\
&=\lambda_Hv^2h^2+\lambda_Hv\,h^3+\frac{\lambda_H}4h^4-\frac{\lambda_Hv^4}4 .
\end{aligned}
```

对动能项，$`\Phi_0^\dagger\Phi_0=v^2/2`$，并且由于下面的 $`A^U_\mu`$ 厄米，$`\partial_\mu h`$ 的线性项相消：

```math
\begin{aligned}
D_\mu\Phi&=\frac{\partial_\mu h}v\,U\Phi_0-ig_{\mathrm{YM}}\Bigl(1+\frac hv\Bigr)UA^U_\mu\Phi_0,\\
A^U_\mu&:=U^\dagger A_\mu U+\frac i{g_{\mathrm{YM}}}U^\dagger\partial_\mu U,\\
(D_\mu\Phi)^\dagger D^\mu\Phi&=\frac12\partial_\mu h\,\partial^\mu h\\
&\quad+\Bigl(1+\frac hv\Bigr)^2g_{\mathrm{YM}}^2\,\Phi_0^\dagger A^U_\mu A^{U\mu}\Phi_0 .
\end{aligned}
```

把 (3.62) 与 (3.63) 代入 (3.61)，

```math
\boxed{
\begin{aligned}
\mathcal L={}&\frac12\partial_\mu h\,\partial^\mu h-\frac12m_h^2h^2\\
&-\lambda_Hv\,h^3-\frac{\lambda_H}4h^4+\frac{\lambda_Hv^4}4\\
&+\Bigl(1+\frac hv\Bigr)^2g_{\mathrm{YM}}^2\,\Phi_0^\dagger A^U_\mu A^{U\mu}\Phi_0\\
&-\frac14F_{\mu\nu}^aF^{a\mu\nu},\\
m_h^2={}&2\lambda_Hv^2=2\mu_H^2 .
\end{aligned}
}
```

由于 $`U^\dagger\partial_\mu U=i\partial_\mu X+O(\theta\,\partial\theta)`$，到一阶有 $`A^U_\mu=A_\mu-\partial_\mu X/g_{\mathrm{YM}}`$。因为 $`a\ge2n`$ 时 $`T^a\Phi_0=0`$，由 (3.59)，$`g_{\mathrm{YM}}^2\Phi_0^\dagger A^U_\mu A^{U\mu}\Phi_0`$ 的二次部分为

```math
\begin{aligned}
&\Phi_0^\dagger\bigl(g_{\mathrm{YM}}A_\mu-\partial_\mu X\bigr)\bigl(g_{\mathrm{YM}}A^\mu-\partial^\mu X\bigr)\Phi_0\\
&\qquad=\frac12\sum_{a=1}^{2n-1}m_a^2\Bigl(A_\mu^a-\frac{\partial_\mu\theta^a}{g_{\mathrm{YM}}}\Bigr)\Bigl(A^{a\mu}-\frac{\partial^\mu\theta^a}{g_{\mathrm{YM}}}\Bigr),\\
&m_a^2:=2g_{\mathrm{YM}}^2\,\Phi_0^\dagger(G^a)^2\Phi_0>0 .
\end{aligned}
```

$`a\ge2n`$ 的 $`A_\mu^a`$ 不出现在 (3.65) 中。由于 $`U(\theta)\in U(n)`$，在规范变换 (3.19)–(3.20) 中取群元 $`U(\theta)^{-1}=U(\theta)^\dagger`$，得

```math
\begin{aligned}
\Phi'&=U^\dagger\Phi=\Bigl(1+\frac hv\Bigr)\Phi_0,\\
A'_\mu&=U^\dagger A_\mu U-\frac i{g_{\mathrm{YM}}}\bigl(\partial_\mu U^\dagger\bigr)U=A^U_\mu,\\
F'_{\mu\nu}&=U^\dagger F_{\mu\nu}U .
\end{aligned}
```

由规范不变性，$`\mathcal L`$ 等于在 (3.64) 中令 $`\theta^a=0`$ 并把 $`A_\mu`$ 换成 $`A'_\mu`$ 所得的结果。利用 (3.59)，

```math
\boxed{
\begin{aligned}
\mathcal L={}&\frac12\partial_\mu h\,\partial^\mu h-\frac12m_h^2h^2\\
&-\lambda_Hv\,h^3-\frac{\lambda_H}4h^4+\frac{\lambda_Hv^4}4\\
&-\frac14F'^a_{\mu\nu}F'^{a\mu\nu}\\
&+\frac12\Bigl(1+\frac hv\Bigr)^2\sum_{a=1}^{2n-1}m_a^2A'^a_\mu A'^{a\mu} .
\end{aligned}
}
```

$`\theta^a`$ 不再出现。到一阶，对 $`a\le2n-1`$ 有 $`A'^a_\mu=A^a_\mu-\partial_\mu\theta^a/g_{\mathrm{YM}}`$，因此 (3.67) 中质量项的二次部分就是 (3.65)。与 (1.85) 及 (1.135) 比较：

- Higgs 场 $`h`$ 的质量为 (3.64) 的 $`m_h`$；
- 沿破缺生成元的 $`2n-1`$ 个规范场 $`A'^a_\mu`$，$`a\le2n-1`$，质量为 (3.65) 的 $`m_a`$；
- 沿未破缺生成元的 $`(n-1)^2`$ 个规范场 $`A'^a_\mu`$，$`a\ge2n`$，无质量。

当 $`n=2`$ 且 $`g_2=g_1=g_{\mathrm{YM}}`$ 时，$`m_a`$ 就是 (3.81) 的 $`m_W`$、$`m_W`$ 与 $`m_Z`$。


<br><br>

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

按照 [1.4 节](#classical-dynamics)中的第二种观点，把 $`t`$ 换成 $`x^\mu`$。

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

上式在 $`t_0=0`$ 时化为 (6.6) 中的 $`\hat U_I(t,0)`$；当 $`\hat H`$ 不显含时间时，由 (2.14)，$`\hat U(t,t_0)=e^{-i\hat H(t-t_0)}`$。由于一般有 $`[\hat V_I(t_1),\hat V_I(t_2)]\neq0`$，适用 [2.4 节](#symmetry) 的情况 (3)，由 (2.20) 得

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

$`\epsilon_\mu^r`$ 为物理偏振矢量。外传播子被截去；对一般的场归一化，需要用到 [6.5 节](#lsz-reduction) 中的极点留数因子。

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

对电子，$`Q_f=-1`$，顶点为 $`-ie\gamma^\mu`$。沿每条费米子线，按与箭头相反的顺序写出各因子，使旋量指标构成矩阵乘积。在每个顶点施加四动量守恒，每个圈动量用 $`\int d^4\ell/(2\pi)^4`$ 积分，并按 (7.3) 延拓到 $`d`$ 维。每个闭合费米子圈给出因子 $`-1`$ 和一个 Dirac 迹；与 [6.3 节](#feynman-diagrams) 相同，交换全同的外费米子改变符号。

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

