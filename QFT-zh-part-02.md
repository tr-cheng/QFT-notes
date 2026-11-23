> 中文版第 2/4 部分 · [完整文件](QFT-zh.md) · [1](QFT-zh-part-01.md) · [2](QFT-zh-part-02.md) · [3](QFT-zh-part-03.md) · [4](QFT-zh-part-04.md)

<a id="scalar-field"></a>
### 1.6 标量场

<a id="scalar-lagrangian"></a>
#### 拉氏量

**实标量场**

```math
\left.
\boxed{
\mathcal L=\frac12\partial_\mu\phi\,\partial^\mu\phi-V(\phi),
\qquad
\partial_\mu\partial^\mu\phi+V'(\phi)=0.
}
\qquad
V(\phi)=\frac12m^2\phi^2
\ \Longrightarrow\
(\partial_\mu\partial^\mu+m^2)\phi=0.
\right.
\tag{1.91}
```

```math
\left.
\pi=\dot\phi,
\qquad
\boxed{
\mathcal H=\frac12\pi^2+\frac12|\boldsymbol\nabla\phi|^2+V(\phi),
\qquad
H=\int d^3x\,\mathcal H.
}
\right.
\tag{1.92}
```

**复标量场**

把 $`\phi`$ 与 $`\phi^*`$ 看作独立变量：

```math
\left.
\boxed{
\begin{aligned}
\mathcal L&=\partial_\mu\phi^*\partial^\mu\phi-m^2\phi^*\phi,\\
(\partial_\mu\partial^\mu+m^2)\phi&=0,\qquad
(\partial_\mu\partial^\mu+m^2)\phi^*=0,\\
\pi_\phi&=\dot\phi^*,\qquad \pi_{\phi^*}=\dot\phi,\\
\mathcal H&=\pi_\phi\pi_{\phi^*}
+|\boldsymbol\nabla\phi|^2+m^2|\phi|^2.
\end{aligned}}
\right.
\tag{1.93}
```

**守恒量：时空对称性**

平移给出 (1.75) 中的正则能动张量：

```math
\left.
\boxed{\begin{aligned}
T^\mu{}_\nu&=\partial^\mu\phi\,\partial_\nu\phi-\delta^\mu{}_\nu\mathcal L
&&\text{（实场）},\\
T^\mu{}_\nu&=\partial^\mu\phi^*\,\partial_\nu\phi
+\partial^\mu\phi\,\partial_\nu\phi^*-\delta^\mu{}_\nu\mathcal L
&&\text{（复场）},\\
\partial_\mu T^\mu{}_\nu&=0,\qquad
P_\nu=\int d^3x\,T^0{}_\nu,\qquad \frac{dP_\nu}{dt}=0.
\end{aligned}}
\right.
\tag{1.94}
```

对两种场，$`T^{\mu\nu}:=T^\mu{}_\rho\eta^{\rho\nu}`$ 都是对称的。Lorentz 对称性给出转动荷与 boost 荷

```math
\left.
\boxed{
J^{\mu\nu}=\int d^3x\,
\bigl(x^\mu T^{0\nu}-x^\nu T^{0\mu}\bigr),
\qquad
\frac{dJ^{\mu\nu}}{dt}=0.
}
\right.
\tag{1.95}
```

其中 $`P_0`$ 是能量，$`P^i`$ 是空间动量，$`J^{ij}`$ 生成转动，$`J^{0i}`$ 生成 boost。这些守恒律在壳成立，并要求积分收敛、边界通量为零。

**守恒量：内部对称性与规范对称性**

实标量场没有复场那样的 $`U(1)`$ 相位对称性。复场拉氏量 (1.93) 具有全局 $`U(1)`$ 对称性；没有规范场时，它在任意局域相位 $`\lambda(x)`$ 下并非不变。对常数 $`\lambda`$，守恒流与荷为

```math
\left.
\phi'=e^{i\lambda}\phi,
\qquad
\boxed{
j^\mu=i\bigl(\phi^*\partial^\mu\phi-\phi\,\partial^\mu\phi^*\bigr),
\qquad
\partial_\mu j^\mu=0,
\qquad
Q=\int d^3x\,j^0.
}
\right.
\tag{1.96}
```


<br><br>

<a id="scalar-field-solutions"></a>
#### Klein–Gordon 方程的解

对实场取 $`V(\phi)=\tfrac12m^2\phi^2`$；(1.93) 中的复场本身已是自由场。定义 $`\Box:=\partial_\mu\partial^\mu`$。平面波满足

```math
\left.
(\Box+m^2)e^{\mp ip\cdot x}=(m^2-p^2)e^{\mp ip\cdot x}=0,
\qquad
p^2=m^2,\qquad
p^0=E_{\mathbf p}:=\sqrt{\mathbf p^2+m^2}>0.
\right.
\tag{1.97}
```

采用下式中显式写出的 Lorentz 不变测度，实波包的展开为

```math
\left.
\boxed{
\phi(x)=\int\frac{d^3p}{(2\pi)^3\,2E_{\mathbf p}}
\left[a(\mathbf p)e^{-ip\cdot x}+a^*(\mathbf p)e^{+ip\cdot x}\right].
}
\right.
\tag{1.98}
```

对复场，两种频率的振幅相互独立：

```math
\left.
\boxed{\begin{aligned}
\phi(x)&=\int\frac{d^3p}{(2\pi)^3\,2E_{\mathbf p}}
\left[a(\mathbf p)e^{-ip\cdot x}+b^*(\mathbf p)e^{+ip\cdot x}\right],\\
\phi^*(x)&=\int\frac{d^3p}{(2\pi)^3\,2E_{\mathbf p}}
\left[a^*(\mathbf p)e^{+ip\cdot x}+b(\mathbf p)e^{-ip\cdot x}\right].
\end{aligned}}
\right.
\tag{1.99}
```

这些系数是经典复振幅。实场条件为 $`b=a`$。这些自由场展开不适用于一般的非线性势 $`V(\phi)`$。

<br><br>

<a id="dirac-field"></a>
### 1.7 Dirac 场 $`\psi`$

<a id="dirac-lagrangian"></a>
#### 拉氏量

Dirac 场的拉氏量具有如下形式：

```math
\left.
\boxed{
\mathcal L=\bar\psi\bigl(i\gamma^\mu\partial_\mu-m\bigr)\psi,
}
\right.
\tag{1.100}
```

其中 $`\psi:\mathbb R^4\to\mathbb C^4`$ 是 Dirac 场，$`\bar\psi:=\psi^\dagger\gamma^0`$ 是它的 Dirac 共轭，$`\gamma^\mu`$ 由 (0.10) 给出，$`m`$ 是质量。

把 $`\psi`$ 与 $`\bar\psi`$ 看作相互独立，Euler–Lagrange 方程给出 Dirac 方程及其共轭方程：

```math
\left.
\boxed{\begin{aligned}
\bigl(i\gamma^\mu\partial_\mu-m\bigr)\psi&=0,\\
i(\partial_\mu\bar\psi)\gamma^\mu+m\bar\psi&=0.
\end{aligned}}
\right.
\tag{1.101}
```

**哈密顿量**

把 $`\psi`$ 与 $`\bar\psi`$ 看作相互独立，它们的共轭动量为

```math
\left.
\boxed{\begin{aligned}
\pi_\psi&:=\frac{\partial\mathcal L}{\partial\dot\psi}
=i\bar\psi\gamma^0=i\psi^\dagger,\\
\pi_{\bar\psi}&:=\frac{\partial\mathcal L}{\partial\dot{\bar\psi}}=0.
\end{aligned}}
\right.
\tag{1.102}
```

**守恒量：时空对称性**

平移给出正则能动张量与四动量

```math
\left.
\boxed{\begin{aligned}
T^\mu{}_\nu&=i\bar\psi\gamma^\mu\partial_\nu\psi-\delta^\mu{}_\nu\mathcal L,
&\partial_\mu T^\mu{}_\nu&=0,\\
P_\nu&=\int d^3x\,T^0{}_\nu,
&\frac{dP_\nu}{dt}&=0.
\end{aligned}}
\right.
\tag{1.103}
```

记 $`T^{\mu\nu}:=T^\mu{}_\rho\eta^{\rho\nu}`$，Lorentz 对称性给出

```math
\left.
\boxed{\begin{aligned}
J^{\mu\nu}&=\int d^3x\left[
x^\mu T^{0\nu}-x^\nu T^{0\mu}
+\frac{i}{4}\psi^\dagger[\gamma^\mu,\gamma^\nu]\psi
\right],\\
\frac{dJ^{\mu\nu}}{dt}&=0.
\end{aligned}}
\right.
\tag{1.104}
```

最后一项是自旋贡献。$`J^{ij}`$ 与 $`J^{0i}`$ 分别是转动荷与 boost 荷。守恒性在壳成立，并要求积分收敛、边界通量为零。

**守恒量：内部对称性与规范对称性**

自由 Dirac 拉氏量具有全局 $`U(1)`$ 对称性。对常数 $`\lambda`$，

```math
\left.
\boxed{\begin{aligned}
\psi'&=e^{i\lambda}\psi,\qquad
\bar\psi'=e^{-i\lambda}\bar\psi,\\
j^\mu&=\bar\psi\gamma^\mu\psi,\qquad \partial_\mu j^\mu=0,\\
Q&=\int d^3x\,j^0=\int d^3x\,\psi^\dagger\psi,
\qquad \frac{dQ}{dt}=0.
\end{aligned}}
\right.
\tag{1.105}
```

对局域相位 $`\lambda(x)`$，$`\mathcal L'=\mathcal L-j^\mu\partial_\mu\lambda`$；局域规范不变性要求与规范场耦合。

<br><br>

<a id="weyl-spinor-solutions"></a>
#### Weyl 表示下 Dirac 方程的解

**Lorentz 群的旋量表示**

对 Dirac 场，(1.46) 中的 $`D(\Lambda)`$ 为

```math
\left.
\Lambda_{\frac12}=\exp\Bigl(-\frac i2\omega_{\mu\nu}S^{\mu\nu}\Bigr),
\qquad
S^{\mu\nu}:=\frac i4[\gamma^\mu,\gamma^\nu],
\right.
\tag{1.106}
```

其中 $`\omega_{\mu\nu}`$ 与 (0.35) 中相同。在 Weyl 表示下，每个 $`S^{\mu\nu}`$ 都是分块对角的：

```math
\left.
S^{0i}=-\frac i2\begin{pmatrix}\sigma^i&0\\0&-\sigma^i\end{pmatrix},
\qquad
S^{ij}=\frac12\epsilon^{ijk}\begin{pmatrix}\sigma^k&0\\0&\sigma^k\end{pmatrix}.
\right.
\tag{1.107}
```

非紧的 Lorentz 群 $`SO(1,3)^+`$ 没有非平凡的有限维幺正表示；在 Weyl 表示下 $`(S^{0i})^\dagger=-S^{0i}`$，因此快度非零时，有限 boost 矩阵不是幺正的。

因此 $`\Lambda_{\frac12}`$ 是分块对角的：记 $`\psi=\begin{pmatrix}\psi_L\\\psi_R\end{pmatrix}`$，左手与右手 Weyl 旋量 $`\psi_L,\psi_R`$ 各自独立地变换。对无穷小变换，与 (0.34) 一样取 $`\omega_{ij}=\epsilon_{ijk}\theta^k`$、$`\omega_{0i}=b^i`$，

```math
\left.
\begin{aligned}
\Lambda_{\frac12}
&\simeq I_4-\frac i2\omega_{\mu\nu}S^{\mu\nu}\\
&=I_4-\frac i2\begin{pmatrix}\boldsymbol\theta\cdot\boldsymbol\sigma&0\\0&\boldsymbol\theta\cdot\boldsymbol\sigma\end{pmatrix}
-i\Bigl(-\frac i2\Bigr)\begin{pmatrix}\mathbf b\cdot\boldsymbol\sigma&0\\0&-\mathbf b\cdot\boldsymbol\sigma\end{pmatrix}\\
&=\begin{pmatrix}I_2-i\boldsymbol\theta\cdot\frac{\boldsymbol\sigma}2-\mathbf b\cdot\frac{\boldsymbol\sigma}2&0\\0&I_2-i\boldsymbol\theta\cdot\frac{\boldsymbol\sigma}2+\mathbf b\cdot\frac{\boldsymbol\sigma}2\end{pmatrix},
\end{aligned}
\right.
\tag{1.108}
```

于是

```math
\left.
\begin{aligned}
\psi_L&\xrightarrow{\ \Lambda\ }\Bigl(I_2-i\boldsymbol\theta\cdot\frac{\boldsymbol\sigma}2-\mathbf b\cdot\frac{\boldsymbol\sigma}2\Bigr)\psi_L,\\
\psi_R&\xrightarrow{\ \Lambda\ }\Bigl(I_2-i\boldsymbol\theta\cdot\frac{\boldsymbol\sigma}2+\mathbf b\cdot\frac{\boldsymbol\sigma}2\Bigr)\psi_R.
\end{aligned}
\right.
\tag{1.109}
```

用 $`\psi_L,\psi_R`$ 表示，Dirac 方程 (1.101) 为

```math
\left.
\begin{pmatrix}-m&i\sigma^\mu\partial_\mu\\i\bar\sigma^\mu\partial_\mu&-m\end{pmatrix}
\begin{pmatrix}\psi_L\\\psi_R\end{pmatrix}=0
\quad\Longleftrightarrow\quad
\begin{cases}
i\sigma^\mu\partial_\mu\psi_R-m\psi_L=0,\\
i\bar\sigma^\mu\partial_\mu\psi_L-m\psi_R=0.
\end{cases}
\right.
\tag{1.110}
```

$`m=0`$ 时，它化为 Weyl 方程

```math
\left.
\begin{cases}
i\bigl(\partial_t-\boldsymbol\sigma\cdot\nabla\bigr)\psi_L=0,\\
i\bigl(\partial_t+\boldsymbol\sigma\cdot\nabla\bigr)\psi_R=0.
\end{cases}
\right.
\tag{1.111}
```

**Dirac 方程的平面波解**

将 $`-i\gamma^\mu\partial_\mu-m`$ 作用于 (1.101) 的左边：

```math
\left.
\begin{aligned}
\bigl(-i\gamma^\mu\partial_\mu-m\bigr)\bigl(i\gamma^\nu\partial_\nu-m\bigr)\psi
&=\bigl(\gamma^\mu\gamma^\nu\partial_\mu\partial_\nu+m^2\bigr)\psi\\
&=\bigl(\eta^{\mu\nu}\partial_\mu\partial_\nu+m^2\bigr)\psi\\
&=\bigl(\Box+m^2\bigr)\psi,
\end{aligned}
\right.
\tag{1.112}
```

其中 $`\Box:=\eta^{\mu\nu}\partial_\mu\partial_\nu=\partial_t^2-\nabla^2`$。由 (1.101)，(1.112) 的左边为零，因此 $`\psi`$ 的每个分量都满足 Klein–Gordon 方程

```math
\left.
\bigl(\Box+m^2\bigr)\psi=0.
\right.
\tag{1.113}
```

平面波 $`e^{-ip\cdot x}`$ 只有在 $`p^2=m^2`$ 时才满足 (1.113)。因此在 Weyl 表示 (0.10) 下，(1.101) 的平面波解具有如下形式

```math
\left.
\psi(x)=\begin{pmatrix}u_L\\u_R\end{pmatrix}e^{-ip\cdot x},
\qquad
p^0=\pm E_{\mathbf p},\quad
E_{\mathbf p}:=\sqrt{\mathbf p^2+m^2},
\right.
\tag{1.114}
```

其中 $`u_L,u_R\in\mathbb C^2`$ 为常量。把 (1.114) 代入 (1.101)，得到

```math
\left.
\bigl(\not p-m\bigr)\begin{pmatrix}u_L\\u_R\end{pmatrix}=0,
\qquad
\not p:=\gamma\cdot p=p^\mu\gamma_\mu.
\right.
\tag{1.115}
```

**(1) 静止系**

取 $`m>0`$，在静止系 $`\mathbf p=\mathbf 0`$ 中讨论；此时把 (1.114) 中的常量记为 $`u_L(\mathbf 0)`$ 和 $`u_R(\mathbf 0)`$。先考虑 $`p^0>0`$。这时 $`p^\mu=(m,\mathbf 0)`$，$`e^{-ip\cdot x}=e^{-imt}`$，$`\not p=m\gamma^0`$，于是 (1.115) 化为

```math
\left.
\begin{aligned}
\bigl(m\gamma^0-m\bigr)\begin{pmatrix}u_L(\mathbf 0)\\u_R(\mathbf 0)\end{pmatrix}
&=\begin{pmatrix}-mI_2&mI_2\\mI_2&-mI_2\end{pmatrix}
\begin{pmatrix}u_L(\mathbf 0)\\u_R(\mathbf 0)\end{pmatrix}=0\\[6pt]
\Longrightarrow\quad u_L(\mathbf 0)&=u_R(\mathbf 0).
\end{aligned}
\right.
\tag{1.116}
```

记 $`u:=\begin{pmatrix}u_L\\u_R\end{pmatrix}`$，共有两个独立解

```math
\left.
u^s(\mathbf 0)=\sqrt m\begin{pmatrix}\xi^s\\\xi^s\end{pmatrix},\qquad s=1,2,
\right.
\tag{1.117}
```

其中 $`\{\xi^s\}`$ 是 $`\mathbb C^2`$ 的一组基，满足 $`\xi^{r\dagger}\xi^s=\delta^{rs}`$。

**(2) Boost**

沿 $`z`$ 方向做快度为 $`\eta`$ 的 boost，即在 (1.106) 中取 $`\omega_{03}=\eta`$，从而 $`\mathbf p=(0,0,p^3)`$，$`\tanh\eta=v=p^3/E_{\mathbf p}`$。于是

```math
\left.
\begin{aligned}
\Lambda_{\frac12}=e^{-i\eta S^{03}}
&=\exp\Bigl[-i\eta\Bigl(-\frac i2\Bigr)\begin{pmatrix}\sigma^3&0\\0&-\sigma^3\end{pmatrix}\Bigr]
=\begin{pmatrix}e^{-\frac12\eta\sigma^3}&0\\0&e^{\frac12\eta\sigma^3}\end{pmatrix}\\
&=\mathop{\rm diag}\nolimits \bigl(e^{-\eta/2},\,e^{\eta/2},\,e^{\eta/2},\,e^{-\eta/2}\bigr),
\end{aligned}
\right.
\tag{1.118}
```

```math
\left.
\tanh\eta=v
\ \Longrightarrow\
e^{\pm\eta}=\sqrt{\frac{1\pm v}{1\mp v}}=\frac{E_{\mathbf p}\pm p^3}{m},
\qquad
e^{\pm\eta/2}=\sqrt{\frac{E_{\mathbf p}\pm p^3}{m}}.
\right.
\tag{1.119}
```

因此

```math
\left.
u^s(p)=\Lambda_{\frac12}u^s(\mathbf 0)
=\mathop{\rm diag}\nolimits \Bigl(\sqrt{E_{\mathbf p}-p^3},\,\sqrt{E_{\mathbf p}+p^3},\,\sqrt{E_{\mathbf p}+p^3},\,\sqrt{E_{\mathbf p}-p^3}\Bigr)
\begin{pmatrix}\xi^s\\\xi^s\end{pmatrix}.
\right.
\tag{1.120}
```

取 $`\xi^1=\begin{pmatrix}1\\0\end{pmatrix}`$，$`\xi^2=\begin{pmatrix}0\\1\end{pmatrix}`$，

```math
\left.
u^1(p)=\begin{pmatrix}\sqrt{E_{\mathbf p}-p^3}\\0\\\sqrt{E_{\mathbf p}+p^3}\\0\end{pmatrix}
\xrightarrow{\ \eta\to\infty\ }\sqrt{2E_{\mathbf p}}\begin{pmatrix}0\\0\\1\\0\end{pmatrix},
\qquad
u^2(p)=\begin{pmatrix}0\\\sqrt{E_{\mathbf p}+p^3}\\0\\\sqrt{E_{\mathbf p}-p^3}\end{pmatrix}
\xrightarrow{\ \eta\to\infty\ }\sqrt{2E_{\mathbf p}}\begin{pmatrix}0\\1\\0\\0\end{pmatrix}.
\right.
\tag{1.121}
```

**(3) 任意动量**

由于 $`\mathop{\rm diag}\nolimits \bigl(\sqrt{E_{\mathbf p}-p^3},\sqrt{E_{\mathbf p}+p^3}\bigr)=\sqrt{E_{\mathbf p}-p^3\sigma^3}`$，$`\mathop{\rm diag}\nolimits \bigl(\sqrt{E_{\mathbf p}+p^3},\sqrt{E_{\mathbf p}-p^3}\bigr)=\sqrt{E_{\mathbf p}+p^3\sigma^3}`$，对任意 $`\mathbf p`$ 有

```math
\left.
\sqrt m\,\Lambda_{\frac12}=\begin{pmatrix}\sqrt{p\cdot\sigma}&0\\0&\sqrt{p\cdot\bar\sigma}\end{pmatrix},
\qquad
p\cdot\sigma:=p_\mu\sigma^\mu=p^0I_2-\mathbf p\cdot\boldsymbol\sigma,
\quad
p\cdot\bar\sigma:=p_\mu\bar\sigma^\mu=p^0I_2+\mathbf p\cdot\boldsymbol\sigma,
\right.
\tag{1.122}
```

其中取正平方根。正能解为

```math
\left.
\boxed{
\psi=u^s(p)\,e^{-ip\cdot x},\qquad
u^s(p)=\begin{pmatrix}\sqrt{p\cdot\sigma}\,\xi^s\\\sqrt{p\cdot\bar\sigma}\,\xi^s\end{pmatrix},\qquad
p^0=E_{\mathbf p}.
}
\right.
\tag{1.123}
```

**验证**

```math
\left.
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
\right.
\tag{1.124}
```

**负能解**

对 $`p^0=-E_{\mathbf p}`$，(1.115) 化为

```math
\left.
\bigl(-\gamma^0E_{\mathbf p}-\boldsymbol\gamma\cdot\mathbf p-m\bigr)u(p)=0
\quad\Longleftrightarrow\quad
\bigl(\gamma^0E_{\mathbf p}-\boldsymbol\gamma\cdot(-\mathbf p)+m\bigr)u(p)=0,
\right.
\tag{1.125}
```

这正是正能方程 $`\bigl(\gamma^0E_{\mathbf p}-\boldsymbol\gamma\cdot\mathbf p-m\bigr)u=0`$ 作代换 $`\mathbf p\to-\mathbf p`$、$`m\to-m`$ 的结果。因此

```math
\left.
u^s(p)=\begin{pmatrix}\sqrt{E_{\mathbf p}I_2+\mathbf p\cdot\boldsymbol\sigma}\,\xi^s\\-\sqrt{E_{\mathbf p}I_2-\mathbf p\cdot\boldsymbol\sigma}\,\xi^s\end{pmatrix}
=\begin{pmatrix}\sqrt{-p\cdot\sigma}\,\xi^s\\-\sqrt{-p\cdot\bar\sigma}\,\xi^s\end{pmatrix},
\qquad p^0=-E_{\mathbf p}.
\right.
\tag{1.126}
```

**反粒子解**

定义

```math
\left.
u^c(p):=\begin{pmatrix}i\sigma^2&0\\0&-i\sigma^2\end{pmatrix}\gamma^0\,u(p),
\qquad
i\sigma^2=\begin{pmatrix}0&1\\-1&0\end{pmatrix}.
\right.
\tag{1.127}
```

对 $`\mathbf p=(0,0,p^3)`$，

```math
\left.
i\sigma^2\sqrt{p\cdot\bar\sigma}
=\begin{pmatrix}0&1\\-1&0\end{pmatrix}\begin{pmatrix}\sqrt{E_{\mathbf p}+p^3}&0\\0&\sqrt{E_{\mathbf p}-p^3}\end{pmatrix}
=\begin{pmatrix}0&\sqrt{E_{\mathbf p}-p^3}\\-\sqrt{E_{\mathbf p}+p^3}&0\end{pmatrix}
=\sqrt{p\cdot\sigma}\;i\sigma^2,
\right.
\tag{1.128}
```

同理 $`i\sigma^2\sqrt{p\cdot\sigma}=\sqrt{p\cdot\bar\sigma}\;i\sigma^2`$。将 (1.127) 用于 (1.123)，并记 $`\eta^s:=i\sigma^2\xi^s`$，

```math
\left.
u^c(p)=\begin{pmatrix}i\sigma^2\sqrt{p\cdot\bar\sigma}\,\xi^s\\-i\sigma^2\sqrt{p\cdot\sigma}\,\xi^s\end{pmatrix}
=\begin{pmatrix}\sqrt{p\cdot\sigma}\,\eta^s\\-\sqrt{p\cdot\bar\sigma}\,\eta^s\end{pmatrix},
\qquad p^0=E_{\mathbf p},
\right.
\tag{1.129}
```

这正是 (1.126) 取在 $`-p`$ 处、并作代换 $`\xi^s\to\eta^s`$ 的结果。对任意 $`\mathbf p`$，反粒子解为

```math
\left.
\boxed{
\psi=v^s(p)\,e^{+ip\cdot x},\qquad
v^s(p):=\begin{pmatrix}\sqrt{p\cdot\sigma}\,\eta^s\\-\sqrt{p\cdot\bar\sigma}\,\eta^s\end{pmatrix},\qquad
\bigl(\not p+m\bigr)v^s(p)=0,\qquad
p^0=E_{\mathbf p}.
}
\right.
\tag{1.130}
```

**解的性质**

**(1) 正交归一性**

由 (1.123)，$`u^\dagger u=2E_{\mathbf p}\,\xi^\dagger\xi`$，$`\bar uu=2m\,\xi^\dagger\xi`$。利用 $`\xi^{r\dagger}\xi^s=\eta^{r\dagger}\eta^s=\delta^{rs}`$，

```math
\left.
\boxed{
\begin{aligned}
u^{r\dagger}(p)\,u^s(p)&=2E_{\mathbf p}\,\delta^{rs}, &\qquad \bar u^r(p)\,u^s(p)&=2m\,\delta^{rs},\\
v^{r\dagger}(p)\,v^s(p)&=2E_{\mathbf p}\,\delta^{rs}, &\qquad \bar v^r(p)\,v^s(p)&=-2m\,\delta^{rs},\\
u^{r\dagger}(p)\,v^s(p')&=v^{r\dagger}(p')\,u^s(p)=0, &\qquad p'&:=(p^0,-\mathbf p).
\end{aligned}
}
\right.
\tag{1.131}
```

**(2) 完备性（自旋求和）**

利用 $`\sum_s\xi^s\xi^{s\dagger}=I_2`$，

```math
\left.
\boxed{
\sum_s u^s(p)\,\bar u^s(p)=\not p+m,\qquad
\sum_s v^s(p)\,\bar v^s(p)=\not p-m.
}
\right.
\tag{1.132}
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
\left.
\gamma^5=\frac{i}{4!}\epsilon_{\mu\nu\rho\sigma}\gamma^\mu\gamma^\nu\gamma^\rho\gamma^\sigma,
\qquad \epsilon_{0123}=+1,
\right.
\tag{1.133}
```

这与 (0.14) 一致。在 $`\psi\to\Lambda_{\frac12}\psi`$、$`\bar\psi\to\bar\psi\Lambda_{\frac12}^{-1}`$ 下，

```math
\left.
\begin{aligned}
\bar\psi\psi&\xrightarrow{\ \Lambda\ }\bar\psi\psi,\\
\bar\psi\gamma^\mu\psi&\xrightarrow{\ \Lambda\ }\bar\psi\Lambda_{\frac12}^{-1}\gamma^\mu\Lambda_{\frac12}\psi=\Lambda^\mu{}_\nu\,\bar\psi\gamma^\nu\psi,\\
\bar\psi S^{\mu\nu}\psi&\xrightarrow{\ \Lambda\ }\Lambda^\mu{}_\rho\Lambda^\nu{}_\sigma\,\bar\psi S^{\rho\sigma}\psi,\\
\bar\psi\gamma^5\gamma^\mu\psi&\xrightarrow{\ \Lambda\ }\det[\Lambda]\,\Lambda^\mu{}_\nu\,\bar\psi\gamma^5\gamma^\nu\psi\qquad\text{（赝矢量）},\\
\bar\psi\gamma^5\psi&\xrightarrow{\ \Lambda\ }\det[\Lambda]\,\bar\psi\gamma^5\psi\qquad\text{（赝标量）}.
\end{aligned}
\right.
\tag{1.134}
```

**证明**（$`\gamma^5`$ 的情形）

```math
\left.
\begin{aligned}
\Lambda_{\frac12}^{-1}\gamma^5\Lambda_{\frac12}
&=\frac{i}{4!}\epsilon_{\mu\nu\rho\sigma}\Lambda^\mu{}_\alpha\Lambda^\nu{}_\beta\Lambda^\rho{}_\kappa\Lambda^\sigma{}_\lambda\,\gamma^\alpha\gamma^\beta\gamma^\kappa\gamma^\lambda\\
&=\frac{i}{4!}\det[\Lambda]\,\epsilon_{\alpha\beta\kappa\lambda}\gamma^\alpha\gamma^\beta\gamma^\kappa\gamma^\lambda
=\det[\Lambda]\,\gamma^5.
\end{aligned}
\right.
\tag{1.135}
```

**手征**

```math
\left.
\gamma^5\begin{pmatrix}\psi_L\\0\end{pmatrix}=-\begin{pmatrix}\psi_L\\0\end{pmatrix},
\qquad
\gamma^5\begin{pmatrix}0\\\psi_R\end{pmatrix}=\begin{pmatrix}0\\\psi_R\end{pmatrix}.
\right.
\tag{1.136}
```

左手与右手投影算符为

```math
\left.
P_L:=\frac{I_4-\gamma^5}2,\qquad P_R:=\frac{I_4+\gamma^5}2
\quad\Longrightarrow\quad
\begin{cases}
P_L+P_R=I_4,\\
P_LP_R=P_RP_L=0,\\
P_L^n=P_L,\quad P_R^n=P_R.
\end{cases}
\right.
\tag{1.137}
```

**矢量流与轴矢流**

```math
\left.
j^\mu:=\bar\psi\gamma^\mu\psi,\qquad
j^{\mu5}:=\bar\psi\gamma^\mu\gamma^5\psi.
\right.
\tag{1.138}
```

(1.100) 关于 $`\psi`$ 的 Euler–Lagrange 方程为 $`-i\partial_\mu\bar\psi\gamma^\mu-m\bar\psi=0`$。结合 (1.101)，

```math
\left.
\partial_\mu j^\mu=(\partial_\mu\bar\psi)\gamma^\mu\psi+\bar\psi\gamma^\mu\partial_\mu\psi
=im\bar\psi\psi-im\bar\psi\psi=0
\quad\Longrightarrow\quad
\int d^3x\,\bar\psi\gamma^0\psi=\text{const}.
\right.
\tag{1.139}
```

**螺旋度**

```math
\left.
h:=\frac{\mathbf p}{|\mathbf p|}\cdot\mathbf S,\qquad
\mathbf S:=\frac12\begin{pmatrix}\boldsymbol\sigma&0\\0&\boldsymbol\sigma\end{pmatrix}.
\right.
\tag{1.140}
```

对 $`\mathbf p=(0,0,p^3)`$ 且 $`p^3>0`$，旋量 (1.121) 满足 $`h\,u^1=\frac12u^1`$，$`h\,u^2=-\frac12u^2`$。


<br><br>

<a id="proca-field"></a>
### 1.8 Proca 场

<a id="proca-lagrangian"></a>
#### 拉氏量

对 $`m>0`$ 的实矢量场，

```math
\left.
F_{\mu\nu}:=\partial_\mu A_\nu-\partial_\nu A_\mu,
\qquad
\boxed{
\mathcal L=-\frac14F_{\mu\nu}F^{\mu\nu}
+\frac12m^2A_\mu A^\mu.
}
\right.
\tag{1.141}
```

```math
\left.
\boxed{
\partial_\mu F^{\mu\nu}+m^2A^\nu=0,
\qquad
\partial_\mu A^\mu=0,
\qquad
(\partial_\mu\partial^\mu+m^2)A^\nu=0.
}
\right.
\tag{1.142}
```

其中 $`\partial_\mu A^\mu=0`$ 由运动方程推出。

**正则动量与哈密顿量**

取 $`A_\mu`$ 为正则坐标。下面的括号都是等时括号：

```math
\left.
\Pi^\mu:=\frac{\partial\mathcal L}{\partial\dot A_\mu}=F^{\mu0},
\qquad
\Pi^0=0,
\qquad
\Pi^i=\dot A_i-\partial_iA_0,
\qquad
\{A_\mu(\mathbf x),\Pi^\nu(\mathbf y)\}_{\mathrm{PB}}
=\delta_\mu{}^\nu\delta^{(3)}(\mathbf x-\mathbf y).
\right.
\tag{1.143}
```

在空间表面项为零的条件下，

```math
\left.
\boxed{
\begin{aligned}
H_c&=\int d^3x\left[
\frac12\sum_i(\Pi^i)^2+\frac14\sum_{i,j}(F_{ij})^2
+\frac{m^2}{2}\sum_i(A_i)^2
-\frac{m^2}{2}A_0^2-A_0\partial_i\Pi^i\right],\\
H_T&=H_c+\int d^3x\,u\,\Pi^0.
\end{aligned}}
\right.
\tag{1.144}
```

**第二类约束**

```math
\left.
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
\right.
\tag{1.145}
```

保持 $`\chi_2`$ 成立的条件定出 $`u=\sum_i\partial_iA_i`$；此后不再有新的约束。

其中 $`\chi_1`$ 是初级约束，$`\chi_2`$ 是次级约束；两者都是第二类的。

**约化哈密顿量**

消去 $`\Pi^0`$ 和 $`A_0`$，得到

```math
\left.
A_0=-\frac{\partial_i\Pi^i}{m^2},
\qquad
\boxed{
H_{\mathrm{red}}=\int d^3x\left[
\frac12\sum_i(\Pi^i)^2+\frac14\sum_{i,j}(F_{ij})^2
+\frac{m^2}{2}\sum_i(A_i)^2
+\frac{(\partial_i\Pi^i)^2}{2m^2}
\right]\ge0.
}
\right.
\tag{1.146}
```

**守恒量：时空对称性**

以 $`A_\mu`$ 为正则变量，平移给出

```math
\left.
\boxed{\begin{aligned}
T^\mu{}_\nu&=-F^{\mu\rho}\partial_\nu A_\rho-\delta^\mu{}_\nu\mathcal L,
&\partial_\mu T^\mu{}_\nu&=0,\\
P_\nu&=\int d^3x\,T^0{}_\nu,
&\frac{dP_\nu}{dt}&=0.
\end{aligned}}
\right.
\tag{1.147}
```

记 $`T^{\mu\nu}:=T^\mu{}_\rho\eta^{\rho\nu}`$，Lorentz 荷包含矢量场的自旋贡献：

```math
\left.
\boxed{
J^{\mu\nu}=\int d^3x\left[
x^\mu T^{0\nu}-x^\nu T^{0\mu}
+\Pi^\mu A^\nu-\Pi^\nu A^\mu
\right],
\qquad
\frac{dJ^{\mu\nu}}{dt}=0.
}
\right.
\tag{1.148}
```

它们在壳守恒，并要求积分收敛、边界通量为零。

**守恒量：内部对称性与规范对称性**

$`m>0`$ 时，质量项破坏 Maxwell 规范对称性 $`A_\mu\mapsto A_\mu+\partial_\mu\lambda(x)`$。实 Proca 场没有复 $`U(1)`$ 相位对称性，因此该模型没有相应的相位荷。其约束 $`\partial_i\Pi^i+m^2A_0=0`$ 是第二类的，如 (1.145)。

<br><br>

<a id="proca-field-solutions"></a>
#### Proca 方程的解

对 $`A^\mu(x)=\epsilon^\mu(p)e^{-ip\cdot x}`$，场方程化为

```math
\left.
\begin{aligned}
(m^2-p^2)\epsilon^\mu+p^\mu(p_\nu\epsilon^\nu)&=0,\\
m^2p_\mu\epsilon^\mu&=0.
\end{aligned}
\quad\Longrightarrow\quad
\boxed{p^2=m^2,\qquad p_\mu\epsilon^\mu=0}
\right.
\tag{1.149}
```

这对 $`m>0`$ 的非零模式成立。

**偏振**

对 $`p^2=m^2`$、$`p^0>0`$，共有三个偏振矢量，$`r=1,2,3`$：

```math
\left.
\boxed{
p_\mu\epsilon_r^\mu(p)=0,
\qquad
\epsilon_{r\mu}^*(p)\epsilon_s^\mu(p)=-\delta_{rs},
\qquad
\sum_{r=1}^3\epsilon_r^\mu(p)\epsilon_r^{\nu*}(p)
=-\eta^{\mu\nu}+\frac{p^\mu p^\nu}{m^2}.
}
\right.
\tag{1.150}
```


静止时，可取 $`\epsilon_r^\mu=(0,\mathbf e_r)`$，其中 $`\mathbf e_r`$ 是空间的一组正交归一基。对 $`\mathbf p\ne0`$，取 $`\mathbf e_1,\mathbf e_2`$ 垂直于 $`\mathbf p`$，且 $`\mathbf e_a\cdot\mathbf e_b=\delta_{ab}`$。记 $`E_{\mathbf p}=\sqrt{\mathbf p^2+m^2}`$，由两个横偏振和一个纵偏振构成的基为

```math
\left.
\boxed{
\epsilon_a^\mu(p)=(0,\mathbf e_a)\quad(a=1,2),
\qquad
\epsilon_3^\mu(p)=\left(\frac{|\mathbf p|}{m},
\frac{E_{\mathbf p}}{m}\frac{\mathbf p}{|\mathbf p|}\right).
}
\right.
\tag{1.151}
```

实场是这三个模式的叠加，其中 $`p^0=E_{\mathbf p}`$：

```math
\left.
\boxed{
A^\mu(x)=\sum_{r=1}^3\int\frac{d^3p}{(2\pi)^3\,2E_{\mathbf p}}
\left[
a_r(\mathbf p)\epsilon_r^\mu(p)e^{-ip\cdot x}
+a_r^*(\mathbf p)\epsilon_r^{\mu*}(p)e^{+ip\cdot x}
\right].
}
\right.
\tag{1.152}
```

其中 $`a_r(\mathbf p)`$ 是经典复振幅；横向条件来自场方程，而非规范选择。

<br><br>

<a id="vector-field"></a>
### 1.9 矢量场

<a id="maxwell-lagrangian"></a>
#### 拉氏量

```math
\left.
\boxed{
\mathcal L=-\frac14F_{\mu\nu}F^{\mu\nu},
\qquad
\partial_\mu F^{\mu\nu}=0,
\qquad
A_\mu'=A_\mu+\partial_\mu\lambda(x).
}
\right.
\tag{1.153}
```

**哈密顿量与第一类约束**

```math
\left.
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
\right.
\tag{1.154}
```

两个约束都是第一类的：

```math
\left.
\{\chi_a(\mathbf x),\chi_b(\mathbf y)\}_{\mathrm{PB}}=0,
\qquad a,b=1,2,
\qquad
\boxed{N_{\mathrm{physical}}=4-2=2.}
\right.
\tag{1.155}
```

**Coulomb 规范与物理哈密顿量**

在无源且场在空间无穷远衰减的情况下，

```math
\left.
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
\right.
\tag{1.156}
```

剩下的正则变量是横向的。

**守恒量：时空对称性**

正则能动张量与四动量为

```math
\left.
\boxed{\begin{aligned}
T^\mu{}_\nu&=-F^{\mu\rho}\partial_\nu A_\rho-\delta^\mu{}_\nu\mathcal L,
&\partial_\mu T^\mu{}_\nu&=0,\\
P_\nu&=\int d^3x\,T^0{}_\nu,
&\frac{dP_\nu}{dt}&=0.
\end{aligned}}
\right.
\tag{1.157}
```

记 $`T^{\mu\nu}:=T^\mu{}_\rho\eta^{\rho\nu}`$，转动荷与 boost 荷为

```math
\left.
\boxed{
J^{\mu\nu}=\int d^3x\left[
x^\mu T^{0\nu}-x^\nu T^{0\mu}
+\Pi^\mu A^\nu-\Pi^\nu A^\mu
\right],
\qquad
\frac{dJ^{\mu\nu}}{dt}=0.
}
\right.
\tag{1.158}
```

当积分收敛且边界通量为零时，这些荷在壳守恒。正则密度依赖于规范；积分后的荷在边界项为零的规范变换下不变。

**守恒量：内部对称性与规范对称性**

(1.153) 中的局域变换给出一个 Noether 恒等式以及 Gauss 约束。对于在整个 $`\mathbb R^3`$ 上光滑且无源的场，

```math
\left.
\boxed{\begin{aligned}
\partial_\nu\partial_\mu F^{\mu\nu}&\equiv0,
&\partial_i\Pi^i&=0,\\
Q_{\mathrm{el}}&:=\lim_{R\to\infty}\oint_{|\mathbf x|=R}\Pi^i\,dS_i=0.
\end{aligned}}
\right.
\tag{1.159}
```

这一自由场模型中没有独立的物质 $`U(1)`$ 粒子数。非零电通量需要源、奇点或不同的边界条件。

<br><br>

<a id="maxwell-field-solutions"></a>
#### Maxwell 方程的解

**Lorenz 规范**

```math
\left.
\partial_\mu A^\mu=0
\quad\Longrightarrow\quad
\partial_\mu\partial^\mu A^\nu=0,
\qquad
A_\mu\mapsto A_\mu+\partial_\mu\lambda,
\qquad
\partial_\mu\partial^\mu\lambda=0
\quad\text{（剩余规范自由度）。}
\right.
\tag{1.160}
```


**平面波与物理偏振**

对 Lorenz 规范下的平面波 $`A^\mu(x)=\epsilon^\mu(p)e^{-ip\cdot x}`$，

```math
\left.
\boxed{
p^2=0,\qquad p^0=|\mathbf p|>0,\qquad
p_\mu\epsilon^\mu=0,\qquad
\epsilon^\mu\sim\epsilon^\mu+\lambda p^\mu.
}
\right.
\tag{1.161}
```

最后一式中，$`\lambda`$ 是剩余平面波规范变换的任意复系数。该约束与这一等价关系留下两个物理偏振。Coulomb 规范下的一组基满足

```math
\left.
\boxed{\begin{aligned}
\epsilon_r^0(p)&=0,\qquad
\mathbf p\cdot\boldsymbol\epsilon_r(p)=0,\qquad
\boldsymbol\epsilon_r^*(p)\cdot\boldsymbol\epsilon_s(p)=\delta_{rs},
\qquad r,s=1,2,\\
\sum_{r=1}^2\epsilon_r^i(p)\epsilon_r^{j*}(p)
&=\delta^{ij}-\frac{p^ip^j}{|\mathbf p|^2}.
\end{aligned}}
\right.
\tag{1.162}
```

对无源波包，取 $`p^0=|\mathbf p|`$，该规范下的实场为：

```math
\left.
\boxed{
A^\mu(x)=\sum_{r=1}^2\int\frac{d^3p}{(2\pi)^3\,2|\mathbf p|}
\left[
a_r(\mathbf p)\epsilon_r^\mu(p)e^{-ip\cdot x}
+a_r^*(\mathbf p)\epsilon_r^{\mu*}(p)e^{+ip\cdot x}
\right].
}
\right.
\tag{1.163}
```

$`a_r(\mathbf p)`$ 是经典复振幅。加上 $`\partial^\mu\lambda(x)`$ 即得其他规范代表元。

<br><br>

<a id="qft-ch2"></a>
## 2. 算符量子化


[1.4 节](QFT-zh-part-01.md#classical-dynamics)中的第一种观点自然导向算符量子化：空间位置标记自由度，而时间仍是演化参数。


<br><br>
<a id="pictures-of-time-evolution"></a>
### 2.1 绘景

以下推导均约定各绘景在 $`t=0`$ 时重合。

In the Hamiltonian formalism the dynamics is given by the Hamiltonian $`\hat H`$. The time dependence of an observable therefore has two sources:

1. The first is the dynamics of the system, i.e. the time evolution generated by $`\hat H`$, which differs from system to system: a different Hamiltonian gives the observable a different time dependence. 

2. The second is a change in the form of the observable itself, which appears as an explicit time dependence and is described mathematically by the partial derivative with respect to $`t`$.

For example, the position and momentum operators are the most basic observables. Their form is fixed by their own definition, so they carry no explicit time dependence, but they can still evolve in time. The form of an interaction, by contrast, can change with time: for a charged system, varying the strength of an external magnetic field by hand changes the form of the interaction.

<br>

<a id="schrodinger-picture"></a>
#### Schrödinger 绘景

**动力学完全由态承担；算符不随时间演化。**

```math
\left.
\frac{d \hat O}{dt} - \frac{\partial \hat O}{\partial t} = 0
\right.
\tag{2.1}
```

因此

```math
\left.
\frac{d\hat q_i}{dt}=\frac{\partial\hat q_i}{\partial t}=0,
\qquad
\frac{d\hat p_i}{dt}=\frac{\partial\hat p_i}{\partial t}=0.
\right.
\tag{2.2}
```

态对时间的依赖来自于动力学，作为量子力学的公理之一，由大名鼎鼎的 Schrödinger 方程给出

```math
\left.
i\frac{\partial}{\partial t}|\psi_S(t)\rangle=\hat H_S|\psi_S(t)\rangle.

\right.
\tag{2.3}
```

注意到，方程的 $`\hat H_S `$ 的形式可以随时间改变，为此我们的 Schrödinger 方程的解有三种形式

(1) $`\frac{\partial \hat H_S}{\partial t} = 0`$ 



```math
\left.
|\psi_S(t)\rangle=e^{-i\hat H_S(t-t_0)}\,|\psi_S(t_0)\rangle .
\right.
\tag{2.4}
```

其中，算符的指数由幂级数定义：

```math
\left.
e^{\hat O}:=\sum_{n=0}^{\infty}\frac{1}{n!}\,\hat O^n.
\right.
\tag{2.5}
```

(2) $`\frac{\partial\hat H_S}{\partial t}\neq0`$，但对任意 $`t,t'`$ 有 $`[\hat H_S(t),\hat H_S(t')]=0`$

```math
\left.
|\psi_S(t)\rangle=\exp\Bigl(-i\int_{t_0}^{t}d\tau\,\hat H_S(\tau)\Bigr)\,|\psi_S(t_0)\rangle ,
\right.
\tag{2.6}
```

其中

```math
\left.
\langle \psi_1 | \int_{t_0}^{t}d\tau\,\hat H_S(\tau) |  \psi_2  \rangle  := \int_{t_0}^{t}d\tau\,\langle\psi_1 |\hat H_S(\tau)|\psi_2\rangle
\right.
\tag{2.7}
```

可以证明

```math
\left.
\langle \psi_1 | [\int_{t_0}^{t}d\tau\,\hat H_S(\tau)]^n |  \psi_2  \rangle  = \int_{t_0}^{t}...\int_{t_0}^{t}d\tau_1 ... d\tau_n\,\langle\psi_1 |\hat H_S(\tau_1)...\hat H_S(\tau_n)|\psi_2\rangle
\right.
\tag{2.8}
```



```math
\left.
\begin{aligned}
\frac{\partial}{\partial t}\Bigl(\int_{t_0}^{t}d\tau\,\hat H_S(\tau)\Bigr)^n
&=\sum_{k=0}^{n-1}\Bigl(\int_{t_0}^{t}d\tau\,\hat H_S(\tau)\Bigr)^k\,\hat H_S(t)\,\Bigl(\int_{t_0}^{t}d\tau\,\hat H_S(\tau)\Bigr)^{n-1-k}\\
&=n\,\hat H_S(t)\Bigl(\int_{t_0}^{t}d\tau\,\hat H_S(\tau)\Bigr)^{n-1}.
\end{aligned}
\right.
\tag{2.9}
```

因此

```math
\left.
\begin{aligned}
\frac{\partial}{\partial t}\exp\Bigl(-i\int_{t_0}^{t}d\tau\,\hat H_S(\tau)\Bigr)
&=\sum_{n=1}^{\infty}\frac{(-i)^n}{n!}\,n\,\hat H_S(t)\Bigl(\int_{t_0}^{t}d\tau\,\hat H_S(\tau)\Bigr)^{n-1}\\
&=-i\hat H_S(t)\exp\Bigl(-i\int_{t_0}^{t}d\tau\,\hat H_S(\tau)\Bigr).
\end{aligned}
\right.
\tag{2.10}
```

使用上面的式子就可以验证解的形式的确如上所述。



(3) 存在 $`t,t'`$ 使 $`[\hat H_S(t),\hat H_S(t')]\neq0`$

```math
\left.
|\psi_S(t)\rangle=\mathcal T\exp\Bigl(-i\int_{t_0}^{t}d\tau\,\hat H_S(\tau)\Bigr)\,|\psi_S(t_0)\rangle ,
\right.
\tag{2.11}
```

其中，编时指数由级数（Dyson 级数）定义：

```math
\left.
\mathcal T\exp\Bigl(-i\int_{t_0}^{t}d\tau\,\hat H_S(\tau)\Bigr)
:=\sum_{n=0}^{\infty}\frac{(-i)^n}{n!}\int_{t_0}^{t}d\tau_1\cdots\int_{t_0}^{t}d\tau_n\,
\mathcal T[\hat H_S(\tau_1)\cdots\hat H_S(\tau_n)],
\right.
\tag{2.12}
```

编时乘积 $`\mathcal T`$ 把算符按时间从左到右递减排列：

```math
\left.
\mathcal T[\hat H_S(\tau_1)\hat H_S(\tau_2)]
:=\theta(\tau_1-\tau_2)\,\hat H_S(\tau_1)\hat H_S(\tau_2)+\theta(\tau_2-\tau_1)\,\hat H_S(\tau_2)\hat H_S(\tau_1),
\right.
\tag{2.13}
```

$`n`$ 个算符的情形同理。

可以证明

```math
\left.
\frac{\partial}{\partial t}\int_{t_0}^{t}d\tau_1\cdots\int_{t_0}^{t}d\tau_n\,
\mathcal T[\hat H_S(\tau_1)\cdots\hat H_S(\tau_n)]
=n\,\hat H_S(t)\int_{t_0}^{t}d\tau_1\cdots\int_{t_0}^{t}d\tau_{n-1}\,
\mathcal T[\hat H_S(\tau_1)\cdots\hat H_S(\tau_{n-1})],
\right.
\tag{2.14}
```

因此

```math
\left.
\begin{aligned}
\frac{\partial}{\partial t}\mathcal T\exp\Bigl(-i\int_{t_0}^{t}d\tau\,\hat H_S(\tau)\Bigr)
&=\sum_{n=1}^{\infty}\frac{(-i)^n}{n!}\,n\,\hat H_S(t)\int_{t_0}^{t}d\tau_1\cdots\int_{t_0}^{t}d\tau_{n-1}\,
\mathcal T[\hat H_S(\tau_1)\cdots\hat H_S(\tau_{n-1})]\\
&=-i\hat H_S(t)\,\mathcal T\exp\Bigl(-i\int_{t_0}^{t}d\tau\,\hat H_S(\tau)\Bigr).
\end{aligned}
\right.
\tag{2.15}
```

若对任意 $`t,t'`$ 有 $`[\hat H_S(t),\hat H_S(t')]=0`$，则可去掉 $`\mathcal T`$，上式化为情况 (2)；不对易时，情况 (2) 中幂次求导恒等式的第二个等号不成立，必须保留 $`\mathcal T`$。

这一级数可以由对 Schrödinger 方程积分并迭代得到：

```math
\left.
\begin{aligned}
|\psi_S(t)\rangle
&=|\psi_S(t_0)\rangle-i\int_{t_0}^{t}d\tau_1\,\hat H_S(\tau_1)\,|\psi_S(\tau_1)\rangle\\
&=\Bigl[1+(-i)\int_{t_0}^{t}d\tau_1\,\hat H_S(\tau_1)
+(-i)^2\int_{t_0}^{t}d\tau_1\int_{t_0}^{\tau_1}d\tau_2\,\hat H_S(\tau_1)\hat H_S(\tau_2)+\cdots\Bigr]|\psi_S(t_0)\rangle ,
\end{aligned}
\right.
\tag{2.16}
```

其中第 $`n`$ 项的积分区域为 $`t\ge\tau_1\ge\cdots\ge\tau_n\ge t_0`$，较晚时刻的算符在左边。

$`\mathcal T[\hat H_S(\tau_1)\cdots\hat H_S(\tau_n)]`$ 在 $`\tau_1,\ldots,\tau_n`$ 的置换下对称；按 $`\tau_i`$ 的大小次序，立方体 $`[t_0,t]^n`$ 分成 $`n!`$ 个区域，各区域的贡献相等，而在 $`\tau_1>\cdots>\tau_n`$ 上，编时乘积就是有序乘积。

因此

```math
\left.
\int_{t_0}^{t}d\tau_1\int_{t_0}^{\tau_1}d\tau_2\cdots\int_{t_0}^{\tau_{n-1}}d\tau_n\,
\hat H_S(\tau_1)\cdots\hat H_S(\tau_n)
=\frac1{n!}\int_{t_0}^{t}d\tau_1\cdots\int_{t_0}^{t}d\tau_n\,
\mathcal T[\hat H_S(\tau_1)\cdots\hat H_S(\tau_n)],
\right.
\tag{2.17}
```

代入后即得编时指数的定义式。

**演化算符**

每种情形下，解都线性依赖于 $`|\psi_S(t_0)\rangle`$：

```math
\left.
|\psi_S(t)\rangle=\hat U_S(t,t_0)\,|\psi_S(t_0)\rangle,
\right.
\tag{2.18}
```

其中
```math
\left.
i\frac{\partial}{\partial t}\hat U_S(t,t_0)=\hat H_S(t)\,\hat U_S(t,t_0),
\qquad
\hat U_S(t_0,t_0)=1.
\right.
\tag{2.19}
```

演化算符 $`\hat U_S(t,t_0)`$ 就是前面三种情况中作用在 $`|\psi_S(t_0)\rangle`$ 上的算符指数。

不难证明
```math
\left.
\hat U_S(t_2,t_0) = \hat U_S(t_2,t_1) \hat U_S(t_1,t_0)
\right.
\tag{2.20}
```

```math
\left.
\hat U_S(t,t_0)^\dagger  \hat U_S(t,t_0) = \hat 1
\right.
\tag{2.21}
```


```math
\left.
\hat U_S(t,t_0)^\dagger = \hat U_S(t_0,t)
\right.
\tag{2.22}
```

<br><br>

<a id="heisenberg-picture"></a>
#### Heisenberg 绘景

**动力学完全由算符承担；态不随时间演化。**

Heisenberg 绘景由 Schrödinger 绘景经如下变换得到

```math
\left.
\boxed{
\begin{gathered}
|\psi_H(t)\rangle:=\hat U_S(t,0)^\dagger\,|\psi_S(t)\rangle=|\psi_S(0)\rangle,\\[4pt]
\hat O_H(t):=\hat U_S(t,0)^\dagger\,\hat O_S(t)\,\hat U_S(t,0).
\end{gathered}
}
\right.
\tag{2.23}
```

由于约定好绘景中时间 t = 0 时重合，下面可以将 $`\hat U_S(t,0)`$ 简记为 $`\hat U_S`$。

两个绘景给出相同的物理可观测量

```math
\left.
\langle\psi_H(t)| \hat O_H(t) |\psi_H(t)\rangle =
\langle\psi_H(t)|\hat U_S^\dagger \hat U_S \hat O_H(t) \hat U_S^\dagger \hat U_S|\psi_H(t)\rangle=\langle\psi_S(t)|\hat O_S(t)|\psi_S(t)\rangle
\right.
\tag{2.24}
```

进一步计算 Heisenberg Picture 中态与算符对时间的依赖关系

```math
\left.
\begin{aligned}
\frac{d\hat O_H}{dt}
&=\Bigl(\frac{\partial\hat U_S}{\partial t}\Bigr)^\dagger\hat O_S\,\hat U_S
+\hat U_S^\dagger\,\frac{d\hat O_S}{dt}\,\hat U_S
+\hat U_S^\dagger\hat O_S\,\frac{\partial\hat U_S}{\partial t}\\
&=i\,\hat U_S^\dagger\bigl[\hat H_S(t),\hat O_S\bigr]\hat U_S
+\hat U_S^\dagger\,\frac{\partial\hat O_S}{\partial t}\,\hat U_S\\
&=i\bigl[\hat H_H(t),\hat O_H\bigr]+\Bigl(\frac{\partial\hat O_S}{\partial t}\Bigr)_H,
\end{aligned}
\right.
\tag{2.25}
```

其中 $`\hat H_H(t):=\hat U_S^\dagger\hat H_S(t)\,\hat U_S`$，$`(\partial\hat O_S/\partial t)_H:=\hat U_S^\dagger(\partial\hat O_S/\partial t)\,\hat U_S`$。

在情形 (1) 和 (2) 中，$`\hat U_S(t,0)`$ 与 $`\hat H_S(t)`$ 对易，因此 $`\hat H_H(t)=\hat H_S(t)`$。



<br><br>

<a id="canonical-quantization"></a>
<a id="canonical-commutation-relations"></a>
### 2.2 正则量子化

考虑无 Dirac 约束的场 $`\phi:\mathbb R^4\to\mathbb R^n`$，分量为 $`\phi_a`$。

拉氏量密度是光滑的多元函数

```math
\left.
\begin{aligned}
\mathcal L:\mathbb R^n\times(\mathbb R^n)^4&\to\mathbb R,\\
(x,y^\mu)&\mapsto\mathcal L(x,y^\mu),
\end{aligned}
\right.
\tag{2.26}
```

其中 $`y^\mu\in\mathbb R^n`$，$`\mu=0,\ldots,3`$。

将 $`\mathcal L`$ 及其偏导数在 $`\bigl(\phi(x),\partial_\mu\phi(x)\bigr)`$ 处的取值记为 $`\mathcal L|_\phi`$、$`\frac{\partial\mathcal L}{\partial y^\mu_a}\big|_\phi`$，它们是 $`x`$ 的函数。

拉氏量为

```math
\left.
L(t):=\int d^3x\,\mathcal L|_\phi(t,\mathbf x).
\right.
\tag{2.27}
```

在每个固定时刻，场值构成无穷多个广义坐标：

```math
\left.
i\longleftrightarrow(a,\mathbf x),
\qquad
q_i(t)\longleftrightarrow\phi_a(t,\mathbf x).
\right.
\tag{2.28}
```

**共轭动量**

与 $`\phi_a(t,\mathbf x)`$ 共轭的动量密度为

```math
\left.
\pi_a(t,\mathbf x)
:=
\frac{\partial\mathcal L}{\partial y^0_a}\Big|_\phi(t,\mathbf x).
\right.
\tag{2.29}
```

**Poisson 括号与对易关系**

经典场满足等时正则 Poisson 括号

```math
\left.
\begin{aligned}
\{\phi_a(t,\mathbf x),\pi_b(t,\mathbf y)\}_{\mathrm{PB}}
&=\delta_{ab}\delta^{(3)}(\mathbf x-\mathbf y),\\
\{\phi_a(t,\mathbf x),\phi_b(t,\mathbf y)\}_{\mathrm{PB}}
&=\{\pi_a(t,\mathbf x),\pi_b(t,\mathbf y)\}_{\mathrm{PB}}=0.
\end{aligned}
\right.
\tag{2.30}
```

正则量子化把场及其共轭动量提升为算符，并把这些基本 Poisson 括号按下式替换

```math
\left.
\{\ ,\ \}_{\mathrm{PB}}
\longrightarrow
\frac{1}{i}[\ ,\ ].
\right.
\tag{2.31}
```

于是，

```math
\left.
\boxed{
\begin{aligned}
[\hat\phi_a(t,\mathbf x),\hat\pi_b(t,\mathbf y)]
&=i\,\delta_{ab}\delta^{(3)}(\mathbf x-\mathbf y),\\
[\hat\phi_a(t,\mathbf x),\hat\phi_b(t,\mathbf y)]
&=[\hat\pi_a(t,\mathbf x),\hat\pi_b(t,\mathbf y)]=0.
\end{aligned}}
\right.
\tag{2.32}
```

这里 $`\delta_{ab}\delta^{(3)}(\mathbf x-\mathbf y)`$ 把 Kronecker δ 符号 $`\delta_{ij}`$ 推广到场标签 $`(a,\mathbf x)`$。

<br><br>

<a id="free-real-scalar-field-quantization"></a>
#### 自由实标量场量子化

对质量为 $`m`$ 的自由场，采用 Lorentz 不变测度 $`d\Pi_{\mathbf p}`$ 与正能四动量 $`p`$：

```math
\left.
\begin{aligned}
E_{\mathbf p}&=\sqrt{\mathbf p^2+m^2},\qquad p^0=E_{\mathbf p},\qquad d\Pi_{\mathbf p}:=\frac{d^3p}{(2\pi)^3\,2E_{\mathbf p}},\\
\hat\phi_I(x)&=\int d\Pi_{\mathbf p}\left(\hat a_{\mathbf p}e^{-ip\cdot x}+\hat a_{\mathbf p}^\dagger e^{+ip\cdot x}\right).
\end{aligned}
\right.
\tag{2.33}
```

真空归一化为 1。产生算符定义协变归一化的单粒子态：

```math
\left.
\boxed{\begin{aligned}
[\hat a_{\mathbf p},\hat a_{\mathbf q}^\dagger]&=2E_{\mathbf p}(2\pi)^3\delta^{(3)}(\mathbf p-\mathbf q),\qquad
[\hat a_{\mathbf p},\hat a_{\mathbf q}]=[\hat a_{\mathbf p}^\dagger,\hat a_{\mathbf q}^\dagger]=0,\\
\hat a_{\mathbf p}|0\rangle&=0,\qquad |\mathbf p\rangle:=\hat a_{\mathbf p}^\dagger|0\rangle,\\
\langle\mathbf p|\mathbf q\rangle&=2E_{\mathbf p}(2\pi)^3\delta^{(3)}(\mathbf p-\mathbf q).
\end{aligned}}
\right.
\tag{2.34}
```

正规序用冒号表示，它把产生算符放在湮灭算符的左边。减去真空能后，

```math
\left.
\begin{aligned}
:\hat H_0:&=\int d\Pi_{\mathbf p}\,E_{\mathbf p}\,\hat a_{\mathbf p}^\dagger\hat a_{\mathbf p},\qquad
:\hat{\mathbf P}:=\int d\Pi_{\mathbf p}\,\mathbf p\,\hat a_{\mathbf p}^\dagger\hat a_{\mathbf p},\\
\hat N&=\int d\Pi_{\mathbf p}\,\hat a_{\mathbf p}^\dagger\hat a_{\mathbf p}.
\end{aligned}
\right.
\tag{2.35}
```

<br><br>

<a id="quantization-with-dirac-brackets"></a>
### 2.3 用 Dirac 括号量子化

<a id="complex-scalar-field-quantization"></a>
#### 复标量场的量子化

<br><br>

<a id="dirac-field-quantization"></a>
#### Dirac 场的量子化

**自由 Dirac 场**

采用 [1.7 节](#dirac-field)的旋量及其归一化，算符 $`\hat b_{\mathbf p}^s`$ 与 $`\hat c_{\mathbf p}^s`$ 分别湮灭粒子与反粒子：

```math
\left.
\hat\psi_I(x)=\sum_{s=1}^{2}\int d\Pi_{\mathbf p}\left(\hat b_{\mathbf p}^s u^s(p)e^{-ip\cdot x}+\hat c_{\mathbf p}^{s\dagger}v^s(p)e^{+ip\cdot x}\right).
\right.
\tag{2.36}
```

费米子的量子化使用反对易子；下面的 $`\alpha,\beta`$ 是 Dirac 分量指标。未列出的模式反对易子都为零，并且两种湮灭算符都湮灭 $`|0\rangle`$。

```math
\left.
\boxed{\begin{aligned}
\{\hat b_{\mathbf p}^r,\hat b_{\mathbf q}^{s\dagger}\}&=\{\hat c_{\mathbf p}^r,\hat c_{\mathbf q}^{s\dagger}\}=2E_{\mathbf p}(2\pi)^3\delta^{rs}\delta^{(3)}(\mathbf p-\mathbf q),\\
\{\hat\psi_{I,\alpha}(t,\mathbf x),\hat\psi_{I,\beta}^\dagger(t,\mathbf y)\}&=\delta_{\alpha\beta}\delta^{(3)}(\mathbf x-\mathbf y),\\
\{\hat\psi_{I,\alpha}(t,\mathbf x),\hat\psi_{I,\beta}(t,\mathbf y)\}&=0.
\end{aligned}}
\right.
\tag{2.37}
```

费米子的正规序每交换一次费米子算符就引入一个负号。正规序后的能量、动量与净费米子数为

```math
\left.
\begin{aligned}
:\hat H_0:&=\sum_s\int d\Pi_{\mathbf p}\,E_{\mathbf p}\left(\hat b_{\mathbf p}^{s\dagger}\hat b_{\mathbf p}^s+\hat c_{\mathbf p}^{s\dagger}\hat c_{\mathbf p}^s\right),\\
:\hat{\mathbf P}:&=\sum_s\int d\Pi_{\mathbf p}\,\mathbf p\left(\hat b_{\mathbf p}^{s\dagger}\hat b_{\mathbf p}^s+\hat c_{\mathbf p}^{s\dagger}\hat c_{\mathbf p}^s\right),\\
\hat Q&:=\int d^3x:\hat\psi_I^\dagger\hat\psi_I:
=\sum_s\int d\Pi_{\mathbf p}\left(\hat b_{\mathbf p}^{s\dagger}\hat b_{\mathbf p}^s-\hat c_{\mathbf p}^{s\dagger}\hat c_{\mathbf p}^s\right).
\end{aligned}
\right.
\tag{2.38}
```

<br><br>

<a id="proca-field-quantization"></a>
#### Proca 场的量子化

<br><br>

<a id="gupta-bleuler-quantization"></a>
### 2.4 Gupta–Bleuler 量子化

<br><br>

<a id="symmetry"></a>
### 2.5 对称性

<a id="ward-identity"></a>
#### Ward 恒等式

<br><br>

<a id="qft-ch3"></a>
## 3. 路径积分

<a id="path-integrals-in-quantum-mechanics"></a>
### 3.1 量子力学中的路径积分

**原理**

考虑具有 $`n`$ 个自由度的系统。

- **位形空间**：$`\mathrm{Conf}=\mathbb R^n`$。
- **动力学结构**：拉氏量

```math
\left.
\begin{aligned}
L:\mathbb R^n\times\mathbb R^n&\to\mathbb R,\\
(x,y)&\mapsto\sum_{a=1}^n\frac12m_ay_a^2-V(x),
\end{aligned}
\right.
\tag{3.1}
```

其中 $`m_a>0`$，$`V:\mathbb R^n\to\mathbb R`$ 光滑。

- **路径**：对 $`t_i<t_f`$，

```math
\left.
\begin{aligned}
C:[t_i,t_f]&\to\mathrm{Conf},\\
t&\mapsto C(t).
\end{aligned}
\right.
\tag{3.2}
```

- **作用量**：路径上的泛函

```math
\left.
\begin{aligned}
S:\{\text{路径}\}&\to\mathbb R,\\
C&\mapsto S[C]:=\int_{t_i}^{t_f}dt\,L\bigl(C(t),\dot C(t)\bigr).
\end{aligned}
\right.
\tag{3.3}
```

**量子化**

- **初位形**：

```math
\left.
\begin{aligned}
Q_i:\{t_i\}&\to\mathrm{Conf},\\
t_i&\mapsto q_i.
\end{aligned}
\right.
\tag{3.4}
```

- **末位形**：

```math
\left.
\begin{aligned}
Q_f:\{t_f\}&\to\mathrm{Conf},\\
t_f&\mapsto q_f.
\end{aligned}
\right.
\tag{3.5}
```

- **跃迁核**：对具有上述端点的路径的积分，

```math
\left.
\boxed{K(Q_f,Q_i):=\int_{C(t_i)=Q_i(t_i)}^{C(t_f)=Q_f(t_f)}\mathcal DC\,e^{iS[C]},}
\right.
\tag{3.6}
```

也记作 $`\int_{Q_i}^{Q_f}\mathcal DC\,e^{iS[C]}`$。

**跃迁核的精确定义**

把 $`[t_i,t_f]`$ 分成 $`N+1`$ 步。

- **测度**：

```math
\left.
\begin{gathered}
\Delta t:=\frac{t_f-t_i}{N+1},\qquad t_k:=t_i+k\,\Delta t\quad(k=0,\ldots,N+1),\\
\mathcal DC:=\lim_{N\to\infty}\mathcal N_N\prod_{k=1}^Nd^nC(t_k),\qquad
\mathcal N_N:=\prod_{a=1}^n\Bigl(\frac{m_a}{2\pi i\,\Delta t}\Bigr)^{\frac{N+1}{2}},
\end{gathered}
\right.
\tag{3.7}
```

于是 $`t_0=t_i`$，$`t_{N+1}=t_f`$，其中 $`d^nC(t_k):=\prod_{a=1}^ndC_a(t_k)`$。

- **作用量**：

```math
\left.
S[C]=\lim_{N\to\infty}\Delta t\sum_{k=0}^NL\Bigl(C(t_k),\frac{C(t_{k+1})-C(t_k)}{\Delta t}\Bigr).
\right.
\tag{3.8}
```

因此 (3.6) 的含义是

```math
\left.
\boxed{
K(Q_f,Q_i)=\lim_{N\to\infty}\mathcal N_N\int\prod_{k=1}^Nd^nC(t_k)\,
\exp\biggl[i\,\Delta t\sum_{k=0}^NL\Bigl(C(t_k),\frac{C(t_{k+1})-C(t_k)}{\Delta t}\Bigr)\biggr],}
\right.
\tag{3.9}
```

其中 $`C(t_0):=q_i`$，$`C(t_{N+1}):=q_f`$，每个 $`C(t_k)`$，$`1\le k\le N`$，都在 $`\mathrm{Conf}`$ 上积分。

**泛函导数**

对源 $`J:[t_i,t_f]\to\mathbb R^n`$，记 $`J\cdot C:=\sum_{a=1}^nJ_aC_a`$，

```math
\left.
K^J(Q_f,Q_i):=\int_{Q_i}^{Q_f}\mathcal DC\,\exp\Bigl(i\int_{t_i}^{t_f}dt\,\bigl[L\bigl(C(t),\dot C(t)\bigr)+J(t)\cdot C(t)\bigr]\Bigr).
\right.
\tag{3.10}
```

在切片形式 (3.9) 中，源在指数中加入 $`i\,\Delta t\sum_{k=0}^NJ(t_k)\cdot C(t_k)`$，因此 $`J`$ 只通过 $`J(t_0),\ldots,J(t_N)`$ 进入。对 $`t_i<t<t_f`$ 定义

```math
\left.
\frac{\delta}{\delta J_a(t)}:=\lim_{N\to\infty}\frac{1}{\Delta t}\frac{\partial}{\partial J_a(t_k)},\qquad t_k\to t.
\right.
\tag{3.11}
```

记 $`L_j:=L\bigl(C(t_j),[C(t_{j+1})-C(t_j)]/\Delta t\bigr)`$，

```math
\left.
\begin{aligned}
\frac{\delta}{\delta J_a(t)}K^J(Q_f,Q_i)
&=\lim_{N\to\infty}\mathcal N_N\int\prod_{j=1}^Nd^nC(t_j)\,
\frac{1}{\Delta t}\frac{\partial}{\partial J_a(t_k)}\exp\biggl[i\,\Delta t\sum_{j=0}^N\bigl(L_j+J(t_j)\cdot C(t_j)\bigr)\biggr]\\
&=\lim_{N\to\infty}\mathcal N_N\int\prod_{j=1}^Nd^nC(t_j)\,
iC_a(t_k)\exp\biggl[i\,\Delta t\sum_{j=0}^N\bigl(L_j+J(t_j)\cdot C(t_j)\bigr)\biggr]\\
&=\int_{Q_i}^{Q_f}\mathcal DC\,iC_a(t)\exp\Bigl(i\int_{t_i}^{t_f}dt'\,\bigl[L\bigl(C(t'),\dot C(t')\bigr)+J(t')\cdot C(t')\bigr]\Bigr).
\end{aligned}
\right.
\tag{3.12}
```


**例：一维自由粒子**

在 (3.1) 中取 $`n=1`$，$`V=0`$：

```math
\left.
L(x,y)=\frac12my^2,\qquad Q_i(t_i)=q_i,\qquad Q_f(t_f)=q_f.
\right.
\tag{3.13}
```

由 (3.7)–(3.9)，其中 $`C(t_0)=q_i`$，$`C(t_{N+1})=q_f`$，$`\mathcal N_N=\bigl(\frac{m}{2\pi i\,\Delta t}\bigr)^{\frac{N+1}{2}}`$，

```math
\left.
\begin{aligned}
K(Q_f,Q_i)&=\int_{Q_i}^{Q_f}\mathcal DC\,e^{i\int_{t_i}^{t_f}dt\,\frac12m\dot C^2}\\
&=\lim_{N\to\infty}\mathcal N_N\int\prod_{k=1}^{N}dC(t_k)\,e^{\frac{i}{\Delta t}\sum_{k=0}^{N}\frac12m\left(C(t_{k+1})-C(t_k)\right)^2}\\
&=\lim_{N\to\infty}\mathcal N_N\int\prod_{k=1}^{N}dC(t_k)\,
e^{\frac{i}{\Delta t}\left[\frac12mq_i^2+\frac12mq_f^2+mC^2(t_1)+\cdots+mC^2(t_N)\right]}\,
e^{\frac{i}{\Delta t}(-m)\left[q_iC(t_1)+C(t_1)C(t_2)+\cdots+C(t_N)q_f\right]}.
\end{aligned}
\right.
\tag{3.14}
```

对 $`C(t_1)`$ 积分，并利用对 $`a>0`$ 成立的 $`\int_{-\infty}^{\infty}dx\,e^{iax^2}=\sqrt{\pi i/a}`$ ($`a\to a+i\varepsilon`$, $`\varepsilon\to0^+`$)：

```math
\left.
\begin{aligned}
\int dC(t_1)\,e^{\frac{i}{\Delta t}\left[mC^2(t_1)-mC(t_1)\left(q_i+C(t_2)\right)\right]}
&=\int dC(t_1)\,e^{\frac{im}{\Delta t}\left(C(t_1)-\frac{q_i+C(t_2)}{2}\right)^2}\,e^{-\frac{im}{4\Delta t}\left(q_i+C(t_2)\right)^2}\\
&=\sqrt{\frac{2\pi i\,\Delta t}{m}\cdot\frac12}\;e^{-\frac{im}{4\Delta t}\left(q_i+C(t_2)\right)^2}.
\end{aligned}
\right.
\tag{3.15}
```

积分掉 $`C(t_1),\ldots,C(t_{j-1})`$ 之后，$`1\le j\le N`$：

```math
\left.
K(Q_f,Q_i)=\lim_{N\to\infty}\mathcal N_N\Bigl(\frac{2\pi i\,\Delta t}{m}\Bigr)^{\frac{j-1}{2}}\frac{1}{\sqrt j}
\int\prod_{k=j}^{N}dC(t_k)\,
e^{\frac{im}{2\Delta t}\left[\frac{\left(C(t_j)-q_i\right)^2}{j}+C^2(t_j)+2C^2(t_{j+1})+\cdots+2C^2(t_N)+q_f^2\right]}\,
e^{\frac{im}{2\Delta t}(-2)\left[C(t_j)C(t_{j+1})+\cdots+C(t_N)q_f\right]}.
\right.
\tag{3.16}
```

对 $`C(t_j)`$ 积分：

```math
\left.
\begin{aligned}
\frac{\left(C(t_j)-q_i\right)^2}{j}+C^2(t_j)-2C(t_j)C(t_{j+1})
&=\frac{j+1}{j}\Bigl(C(t_j)-\frac{q_i+jC(t_{j+1})}{j+1}\Bigr)^2+\frac{\left(C(t_{j+1})-q_i\right)^2}{j+1}-C^2(t_{j+1}),\\
\int dC(t_j)\,e^{\frac{im}{2\Delta t}\frac{j+1}{j}\left(C(t_j)-\frac{q_i+jC(t_{j+1})}{j+1}\right)^2}
&=\sqrt{\frac{2\pi i\,\Delta t}{m}\cdot\frac{j}{j+1}},
\end{aligned}
\right.
\tag{3.17}
```

这就给出 $`j+1`$ 时的 (3.16)；当 $`j=N`$ 时，$`C(t_{N+1})=q_f`$，方括号化为 $`\frac{(q_f-q_i)^2}{N+1}`$。因此，利用 $`(N+1)\Delta t=t_f-t_i`$，

```math
\left.
\begin{aligned}
K(Q_f,Q_i)&=\lim_{N\to\infty}\Bigl(\frac{m}{2\pi i\,\Delta t}\Bigr)^{\frac{N+1}{2}}\Bigl(\frac{2\pi i\,\Delta t}{m}\Bigr)^{\frac N2}\frac{1}{\sqrt{N+1}}\,
e^{\frac{im\left(q_f-q_i\right)^2}{2(N+1)\Delta t}}\\
&=\boxed{\sqrt{\frac{m}{2\pi i\,(t_f-t_i)}}\;e^{\frac{im\left(q_f-q_i\right)^2}{2(t_f-t_i)}}.}
\end{aligned}
\right.
\tag{3.18}
```

这个例子说明了为什么路径积分的定义 (3.7) 中要包含预因子 $`\mathcal N_N`$。结果 (3.18) 有限，而按定义 $`\mathcal N_N`$ 在 $`N\to\infty`$ 时发散；若没有这个预因子，(3.18) 中剩下的因子 $`\bigl(\frac{2\pi i\,\Delta t}{m}\bigr)^{\frac N2}\frac{1}{\sqrt{N+1}}`$ 趋于零，$`K(Q_f,Q_i)`$ 也将趋于零。

**与算符量子化的关系**

设 $`\hat H:=\sum_{a=1}^n\hat p_a^2/(2m_a)+V(\hat q)`$，其中 $`[\hat q_a,\hat p_b]=i\delta_{ab}`$，$`\hat q_a|q\rangle=q_a|q\rangle`$，并设 $`\hat U_S(t_f,t_i)=e^{-i\hat H(t_f-t_i)}`$ 为其演化算符 (2.18)。于是，记 $`q_i=Q_i(t_i)`$，$`q_f=Q_f(t_f)`$，

```math
\left.
\boxed{K(Q_f,Q_i)=\langle q_f|\hat U_S(t_f,t_i)|q_i\rangle=\langle q_f,t_f|q_i,t_i\rangle}
\right.
\tag{3.19}
```

两种写法分别对应 Schrödinger 绘景与 Heisenberg 绘景，其中由 (2.23)，$`|q,t\rangle:=\hat U_S(t,0)^\dagger|q\rangle`$ 满足 $`\hat q_H(t)|q,t\rangle=q\,|q,t\rangle`$。

<br><br>

<a id="path-integrals-in-field-theory"></a>
### 3.2 量子场论中的路径积分

按照 [1.4 节](QFT-zh-part-01.md#classical-dynamics)中的第二种观点，把 $`t`$ 换成 $`x^\mu`$。

**原理**

- **位形空间**：$`\mathrm{Conf}=\mathbb R^n`$。
- **动力学结构**：拉氏量密度

```math
\left.
\begin{aligned}
\mathcal L:\mathbb R^n\times(\mathbb R^n)^4&\to\mathbb R,\\
(x,y^\mu)&\mapsto\sum_{a=1}^n\frac12y_a^\mu y_{a\mu}-V(x),
\end{aligned}
\right.
\tag{3.20}
```

其中 $`y^\mu\in\mathbb R^n`$，$`\mu=0,\ldots,3`$，$`V:\mathbb R^n\to\mathbb R`$ 光滑。

- **路径**：对 $`t_i<t_f`$，

```math
\left.
\begin{aligned}
\phi:[t_i,t_f]\times\mathbb R^3&\to\mathrm{Conf},\\
x&\mapsto\phi(x),
\end{aligned}
\right.
\tag{3.21}
```

其中 $`\phi(t):=\phi(t,\cdot\,)`$ 为时刻 $`t`$ 的位形。

- **作用量**：路径上的泛函

```math
\left.
\begin{aligned}
S:\{\text{路径}\}&\to\mathbb R,\\
\phi&\mapsto S[\phi]:=\int_{\mathbb R^3}d^3x\int_{t_i}^{t_f}dt\,\mathcal L\bigl(\phi(x),\partial_\mu\phi(x)\bigr).
\end{aligned}
\right.
\tag{3.22}
```

在路径积分中，场取代了路径的地位：路径 (3.21) 就是限制在 $`[t_i,t_f]\times\mathbb R^3`$ 上的经典场 (1.44)。因此路径记为 $`\phi`$，下面的积分都是对场位形的积分。

以下 $`\int d^4x:=\int_{t_i}^{t_f}dt\int_{\mathbb R^3}d^3x`$。

**量子化**

- **初位形**：

```math
\left.
\begin{aligned}
\Phi_i:\{t_i\}\times\mathbb R^3&\to\mathrm{Conf},\\
(t_i,\mathbf x)&\mapsto\Phi_i(t_i,\mathbf x).
\end{aligned}
\right.
\tag{3.23}
```

- **末位形**：

```math
\left.
\begin{aligned}
\Phi_f:\{t_f\}\times\mathbb R^3&\to\mathrm{Conf},\\
(t_f,\mathbf x)&\mapsto\Phi_f(t_f,\mathbf x).
\end{aligned}
\right.
\tag{3.24}
```

- **跃迁核**：

```math
\left.
\boxed{K(\Phi_f,\Phi_i):=\int_{\phi(t_i,\mathbf x)=\Phi_i(t_i,\mathbf x)}^{\phi(t_f,\mathbf x)=\Phi_f(t_f,\mathbf x)}\mathcal D\phi\,e^{iS[\phi]},}
\right.
\tag{3.25}
```

也记作 $`\int_{\Phi_i}^{\Phi_f}\mathcal D\phi\,e^{iS[\phi]}`$；边界条件对每个 $`\mathbf x\in\mathbb R^3`$ 成立。

**关联函数**

与 (3.19) 同理，

```math
\left.
K(\Phi_f,\Phi_i)=\langle\Phi_f|\hat U_S(t_f,t_i)|\Phi_i\rangle,
\right.
\tag{3.26}
```
 在算符量子化中，真空可按这组基展开，由此定义真空泛函 $`\Psi[\Phi]`$：

```math
\left.
|\mathrm{vac}\rangle=\int\mathcal D\Phi\,|\Phi\rangle\langle\Phi|\mathrm{vac}\rangle=\int\mathcal D\Phi\,|\Phi\rangle\,\Psi[\Phi],\qquad
\Psi[\Phi]:=\langle\Phi|\mathrm{vac}\rangle.
\right.
\tag{3.27}
```

因此

```math
\left.
\begin{aligned}
K(\mathrm{vac}_f,\mathrm{vac}_i)&:=\langle\mathrm{vac}_f|\hat U_S(t_f,t_i)|\mathrm{vac}_i\rangle\\
&=\int\mathcal D\Phi_f\,\mathcal D\Phi_i\,\Psi^*[\Phi_f]\,\Psi[\Phi_i]\,K(\Phi_f,\Phi_i).
\end{aligned}
\right.
\tag{3.28}
```




- **关联函数**：

```math
\left.
\boxed{
\begin{aligned}
G_{a_1\cdots a_r}(x_1,\ldots,x_r)&:=\langle \phi_{a_1}(x_1)\cdots\phi_{a_r}(x_r)\rangle_{\mathrm{vac}}\\
&=\frac{\int_{\mathrm{vac}}^{\mathrm{vac}}\mathcal D\phi\,\phi_{a_1}(x_1)\cdots\phi_{a_r}(x_r)\,e^{iS[\phi]}}{\int_{\mathrm{vac}}^{\mathrm{vac}}\mathcal D\phi\,e^{iS[\phi]}},
\end{aligned}}
\right.
\tag{3.29}
```

其中 $`t_i<x_k^0<t_f`$。

上述定义中的分母源自于对真空归一化的要求，在上述定义下，<1>=真空的模=1

- **生成泛函**：对源 $`J:[t_i,t_f]\times\mathbb R^3\to\mathbb R^n`$，$`J\cdot\phi`$ 的含义同 (3.10)，

```math
\left.
K^J(\Phi_f,\Phi_i):=\int_{\Phi_i}^{\Phi_f}\mathcal D\phi\,\exp\Bigl(iS[\phi]+i\int d^4x\,J(x)\cdot\phi(x)\Bigr),
\right.
\tag{3.30}
```

并且，取 (3.28) 中的真空端点，

```math
\left.
\boxed{
Z[J]:=K^J(\mathrm{vac}_f,\mathrm{vac}_i)
=\int\mathcal D\Phi_f\,\mathcal D\Phi_i\,\Psi^*[\Phi_f]\,\Psi[\Phi_i]\,K^J(\Phi_f,\Phi_i),}
\right.
\tag{3.31}
```

于是 $`Z[0]=K(\mathrm{vac}_f,\mathrm{vac}_i)`$。

与 (3.12) 同理，每个 $`\delta/\delta J_a(x)`$ 作用于 (3.30) 都拉下一个 $`i\phi_a(x)`$，因此由 (3.31) 与 (3.29)，

```math
\left.
\boxed{G_{a_1\cdots a_r}(x_1,\ldots,x_r)=\frac{1}{Z[0]}\left.\Bigl(-i\frac{\delta}{\delta J_{a_1}(x_1)}\Bigr)\cdots\Bigl(-i\frac{\delta}{\delta J_{a_r}(x_r)}\Bigr)Z[J]\right|_{J=0}.}
\right.
\tag{3.32}
```

**连通函数**

对单个实标量场，

```math
\left.
\begin{aligned}
G_n(x_1,\ldots,x_n)&:=\langle\Omega|\mathcal T[\hat\phi_H(x_1)\cdots\hat\phi_H(x_n)]|\Omega\rangle
=\left.\frac{1}{Z[0]}\frac{1}{i^n}\frac{\delta^n Z[J]}{\delta J(x_1)\cdots\delta J(x_n)}\right|_{J=0},\\
W[J]&:=-i\ln Z[J],\qquad
G_{n,\mathrm c}=\left.\frac{1}{i^{n-1}}\frac{\delta^nW}{\delta J(x_1)\cdots\delta J(x_n)}\right|_{J=0}.
\end{aligned}
\right.
\tag{3.33}
```

这里 $`|\Omega\rangle`$ 是归一化的相互作用真空，$`J(x)`$ 是对易的外源。泛函积分需要正规子；下面的表达式定义了它们在微扰论中的用法。

**有效作用量与 Schwinger--Dyson 方程**

Legendre 变换生成单粒子不可约 (1PI) 顶点；1PI 图是指切断任意一条内线后仍保持连通的图：

```math
\left.
\phi_c(x):=\frac{\delta W}{\delta J(x)},\qquad
\Gamma[\phi_c]:=W[J]-\int d^4x\,J\phi_c,\qquad
\boxed{\frac{\delta\Gamma}{\delta\phi_c(x)}=-J(x).}
\right.
\tag{3.34}
```

当标量泛函测度平移不变且不存在泛函边界项时，

```math
\left.
\left[
\left.\frac{\delta S}{\delta\phi(x)}\right|_{\phi\,\to\,(1/i)\delta/\delta J}
+J(x)\right]Z[J]=0.
\right.
\tag{3.35}
```

**欧氏延拓与费米子**

当时间围道可以转动而不越过奇点时，对 $`\mathcal L=\tfrac12\partial_\mu\phi\partial^\mu\phi-V(\phi)`$，$`t=-i\tau`$ 给出：

```math
\left.
e^{iS}\longrightarrow e^{-S_E},\qquad
S_E=\int d\tau\,d^3x\left[\frac12(\partial_\tau\phi)^2
+\frac12(\boldsymbol\nabla\phi)^2+V(\phi)\right].
\right.
\tag{3.36}
```

泛函积分中的费米子场是独立的 Grassmann 变量。在测度次序固定时，二次 Dirac 作用量给出

```math
\left.
\int\mathcal D\bar\psi\,\mathcal D\psi\,
e^{i\int d^4x\,\bar\psi(i\gamma^\mu\partial_\mu-m)\psi}\ \propto\ \det(i\gamma^\mu\partial_\mu-m),
\right.
\tag{3.37}
```

其中与场无关的归一化因子被吸收进 $`Z[0]`$，$`i\gamma^\mu\partial_\mu-m`$ 的逆采用费曼处方。

**规范固定与 Faddeev--Popov 鬼场**

对平凡规范位形附近的微扰 $`SU(3)`$ 理论，Lorenz 规范引入规范参数 $`\xi`$ 以及反对易的标量鬼场 $`c^a,\bar c^a`$：

```math
\left.
\begin{aligned}
\mathcal L_{\mathrm{gf}}&=-\frac{1}{2\xi}(\partial^\mu A^a_\mu)^2,\\
\mathcal L_{\mathrm{gh}}&=-\bar c^a\partial^\mu(D_\mu^{ab}c^b),\qquad
D_\mu^{ab}:=\delta^{ab}\partial_\mu+g_s f^{acb}A^c_\mu,\\
\Delta_{\mathrm{FP}}[A]&=\det[-\partial^\mu D_\mu^{ab}].
\end{aligned}
\right.
\tag{3.38}
```

对这种线性规范下的阿贝尔规范场，该行列式与场无关，鬼场退耦。这种局域的微扰构造不能消除全局的规范复本歧义。

<br><br>

