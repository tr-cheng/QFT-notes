> 中文版第 2/4 部分 · [完整文件](QFT-zh.md) · [1](QFT-zh-part-01.md) · [2](QFT-zh-part-02.md) · [3](QFT-zh-part-03.md) · [4](QFT-zh-part-04.md)

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


[1.4 节](QFT-zh-part-01.md#classical-dynamics)中的第一种观点自然导向算符量子化：空间位置标记自由度，而时间仍是演化参数。


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

