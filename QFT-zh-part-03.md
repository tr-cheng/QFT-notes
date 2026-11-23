> 中文版第 3/4 部分 · [完整文件](QFT-zh.md) · [1](QFT-zh-part-01.md) · [2](QFT-zh-part-02.md) · [3](QFT-zh-part-03.md) · [4](QFT-zh-part-04.md)

<a id="phi-cubed-theory"></a>
### 3.3 $`\phi^3`$ 理论

**作用量**

在 (3.20) 中取 $`n=1`$，$`\mathrm{Conf}=\mathbb R`$，$`V(\phi)=\frac12m^2\phi^2+\frac1{3!}\lambda\phi^3`$。利用 (1.97) 中的 $`\Box:=\partial_\mu\partial^\mu`$，

```math
\left.
\begin{aligned}
S[\phi]&=\int d^4x\,\mathcal L\bigl(\phi(x),\partial_\mu\phi(x)\bigr)\\
&=\int d^4x\,\Bigl[\frac12\partial_\mu\phi\,\partial^\mu\phi-\frac12m^2\phi^2-\frac1{3!}\lambda\phi^3\Bigr]\\
&=\int d^4x\,\Bigl[-\frac12\phi(\Box+m^2)\phi-\frac1{3!}\lambda\phi^3\Bigr]
+\frac12\int d^3x\,\bigl[\phi\,\partial_0\phi\bigr]_{x^0=t_i}^{x^0=t_f}.
\end{aligned}
\right.
\tag{3.39}
```

$`S_0[\phi]`$ 表示 (3.39) 取 $`\lambda=0`$ 的情形。

**费曼传播子**

```math
\left.
\begin{aligned}
(\Box+m^2)\Delta_F(x)&=-i\delta^{(4)}(x),\\
\Delta_F(x)&=\int\frac{d^4p}{(2\pi)^4}\,\frac{-i}{-p^2+m^2-i\varepsilon}\,e^{-ip\cdot x}
=\int\frac{d^4p}{(2\pi)^4}\,\frac{i}{p^2-m^2+i\varepsilon}\,e^{-ip\cdot x},
\end{aligned}
\right.
\tag{3.40}
```

其中 $`\varepsilon\to0^+`$；这就是 (4.12) 中的函数。

**自由生成泛函**

此后 $`\mathrm{vac}`$ 指 $`S_0`$ 的真空，且 $`J`$ 在 $`x^0=t_i`$ 与 $`x^0=t_f`$ 附近为零。令

```math
\left.
K_0^J(\Phi_f,\Phi_i):=\int_{\Phi_i}^{\Phi_f}\mathcal D\phi\,\exp\Bigl(iS_0[\phi]+i\int d^4x\,J(x)\phi(x)\Bigr),
\qquad K_0:=K_0^J\big|_{J=0}.
\right.
\tag{3.41}
```

在 $`K_0^J(\mathrm{vac}_f,\mathrm{vac}_i)`$ 中把路径连同 $`\Phi_f`$ 与 $`\Phi_i`$ 一起作平移

```math
\left.
\phi(x)\to\phi(x)+i\int d^4y\,\Delta_F(x-y)J(y),
\right.
\tag{3.42}
```

这不改变 (3.28) 中的测度。由 (3.40)，指数中 $`\int d^4x`$ 的被积函数变为

```math
\left.
\begin{aligned}
&-\frac12\phi(\Box+m^2)\phi+J\phi\\
&\to-\frac12\phi(\Box+m^2)\phi+J\phi
\underbrace{-\frac i2\int d^4y\,\Delta_F(x-y)J(y)\,(\Box+m^2)\phi(x)}_{-\frac12J\phi}\\
&\qquad+J(x)\,i\int d^4y\,\Delta_F(x-y)J(y)
\underbrace{-\frac12\phi(x)\,i\int d^4y\,\bigl(-i\delta^{(4)}(x-y)\bigr)J(y)}_{-\frac12J\phi}\\
&\qquad\underbrace{+\frac12\int d^4y\,\Delta_F(x-y)J(y)\,(\Box+m^2)\int d^4\bar y\,\Delta_F(x-\bar y)J(\bar y)}_{-\frac i2J\Delta_FJ}\\
&\to-\frac12\phi(\Box+m^2)\phi+\frac i2\int d^4y\,J(y)\Delta_F(x-y)J(x),
\end{aligned}
\right.
\tag{3.43}
```

其中第一个下花括号在对 $`x`$ 分部积分后成立，至多相差 $`x^0=t_i,t_f`$ 处的项。把平移 (3.42) 记为 $`\chi(x):=i\int d^4y\,\Delta_F(x-y)J(y)`$，则由 (3.40) 有 $`(\Box+m^2)\chi=J`$。计入来自 (3.39) 以及这次分部积分的 $`x^0=t_i,t_f`$ 处的项，平移后 (3.41) 的指数恰为

```math
\left.
\begin{aligned}
iS_0[\phi+\chi]+i\int d^4x\,J(\phi+\chi)
&=iS_0[\phi]-\frac12\int d^4x\,d^4y\,J(x)\Delta_F(x-y)J(y)\\
&\quad+i\int d^3x\,\Bigl[\bigl(\phi+\tfrac12\chi\bigr)\partial_0\chi\Bigr]_{x^0=t_i}^{x^0=t_f}.
\end{aligned}
\right.
\tag{3.44}
```

把 (3.40) 的 $`p^0`$ 围道在 $`x^0>0`$ 时闭合于下半平面、在 $`x^0<0`$ 时闭合于上半平面，围绕极点 $`p^0=\pm(E_{\mathbf p}-i\varepsilon')`$，其中 $`E_{\mathbf p}`$ 同 (2.33)，$`\varepsilon'\to0^+`$，

```math
\left.
\Delta_F(x)=\int\frac{d^3p}{(2\pi)^3\,2E_{\mathbf p}}\,e^{i\mathbf p\cdot\mathbf x-iE_{\mathbf p}|x^0|}.
\right.
\tag{3.45}
```

令 $`\mathcal E:=(-\nabla^2+m^2)^{1/2}`$，即 $`\mathcal E\,e^{i\mathbf p\cdot\mathbf x}=E_{\mathbf p}\,e^{i\mathbf p\cdot\mathbf x}`$。由于 $`J`$ 在 $`t_i`$ 与 $`t_f`$ 附近为零，由 (3.45) 得

```math
\left.
\partial_0\chi\big|_{x^0=t_f}=-i\mathcal E\chi\big|_{x^0=t_f},\qquad
\partial_0\chi\big|_{x^0=t_i}=+i\mathcal E\chi\big|_{x^0=t_i},
\right.
\tag{3.46}
```

因此 $`\chi`$ 在 $`t_f`$ 处只含正频，在 $`t_i`$ 处只含负频。

对 $`S_0`$，真空为 (2.34) 的 $`|0\rangle`$。由 (4.2) 与 (1.92)，在 $`t=0`$ 时 Schrödinger 绘景的算符为 $`\hat\phi(\mathbf x)=\hat\phi_I(0,\mathbf x)`$ 与 $`\hat\pi(\mathbf x)=\partial_0\hat\phi_I(0,\mathbf x)`$。反解 (2.33)，并令 $`\hat\pi(\mathbf x)`$ 以 $`-i\,\delta/\delta\Phi(\mathbf x)`$ 的形式作用于 $`\Psi[\Phi]=\langle\Phi|0\rangle`$，

```math
\left.
\begin{aligned}
\hat a_{\mathbf p}&=\int d^3x\,e^{-i\mathbf p\cdot\mathbf x}\bigl[E_{\mathbf p}\hat\phi(\mathbf x)+i\hat\pi(\mathbf x)\bigr],\\
0=\langle\Phi|\hat a_{\mathbf p}|0\rangle&=\int d^3x\,e^{-i\mathbf p\cdot\mathbf x}\Bigl[(\mathcal E\Phi)(\mathbf x)+\frac{\delta}{\delta\Phi(\mathbf x)}\Bigr]\Psi[\Phi]\quad\text{对所有 }\mathbf p,\\
\Psi[\Phi]&=\Psi[0]\exp\Bigl(-\frac12\int d^3x\,\Phi\,\mathcal E\,\Phi\Bigr),
\end{aligned}
\right.
\tag{3.47}
```

其中第二行用到 $`\int d^3x\,f\,\mathcal E\,g=\int d^3x\,(\mathcal Ef)\,g`$，该行即 $`\delta\Psi/\delta\Phi(\mathbf x)=-(\mathcal E\Phi)(\mathbf x)\Psi[\Phi]`$。记 $`\chi_{f,i}:=\chi(t_{f,i},\cdot\,)`$，平移把 $`\Psi^*[\Phi_f]\Psi[\Phi_i]`$ 变为 $`\Psi^*[\Phi_f+\chi_f]\Psi[\Phi_i+\chi_i]`$，而 $`\phi(t_{f,i},\cdot\,)=\Phi_{f,i}`$。由 (3.46) 与 (3.47)，

```math
\left.
\begin{aligned}
i\int d^3x\,\Bigl[\bigl(\phi+\tfrac12\chi\bigr)\partial_0\chi\Bigr]_{x^0=t_i}^{x^0=t_f}
&=\int d^3x\,\Bigl[\bigl(\Phi_f+\tfrac12\chi_f\bigr)\mathcal E\chi_f+\bigl(\Phi_i+\tfrac12\chi_i\bigr)\mathcal E\chi_i\Bigr],\\
\ln\frac{\Psi^*[\Phi_f+\chi_f]\,\Psi[\Phi_i+\chi_i]}{\Psi^*[\Phi_f]\,\Psi[\Phi_i]}
&=-\int d^3x\,\Bigl[\bigl(\Phi_f+\tfrac12\chi_f\bigr)\mathcal E\chi_f+\bigl(\Phi_i+\tfrac12\chi_i\bigr)\mathcal E\chi_i\Bigr],
\end{aligned}
\right.
\tag{3.48}
```

因此 (3.44) 中 $`x^0=t_i,t_f`$ 处的项与 $`\Psi^*[\Phi_f]\Psi[\Phi_i]`$ 的变化相消。于是

```math
\left.
K_0^J(\mathrm{vac}_f,\mathrm{vac}_i)=K_0(\mathrm{vac}_f,\mathrm{vac}_i)\,
\exp\Bigl[-\frac12\int d^4x\,d^4y\,J(x)\Delta_F(x-y)J(y)\Bigr],
\right.
\tag{3.49}
```

以及

```math
\left.
\boxed{
\begin{aligned}
Z_0[J]&:=K_0^J(\mathrm{vac}_f,\mathrm{vac}_i)
=\int\mathcal D\Phi_f\,\mathcal D\Phi_i\,\Psi^*[\Phi_f]\,\Psi[\Phi_i]\,K_0^J(\Phi_f,\Phi_i)\\
&=Z_0[0]\,\exp\Bigl[-\frac12\int d^4x\,d^4y\,J(x)\Delta_F(x-y)J(y)\Bigr],
\end{aligned}}
\right.
\tag{3.50}
```

其中由 (3.49)，$`Z_0[0]=K_0(\mathrm{vac}_f,\mathrm{vac}_i)`$。

**两点函数**

对 $`S_0`$ 及 $`t_i<z_1^0,z_2^0<t_f`$，由 (3.32) 与 (3.50)，

```math
\left.
\boxed{
\begin{aligned}
\langle\phi(z_1)\phi(z_2)\rangle_{\mathrm{vac}}
&=\frac{1}{Z_0[0]}\Bigl(-i\frac{\delta}{\delta J(z_1)}\Bigr)\Bigl(-i\frac{\delta}{\delta J(z_2)}\Bigr)Z_0[J]\Big|_{J=0}\\
&=\Bigl(-i\frac{\delta}{\delta J(z_1)}\Bigr)\Bigl(-i\frac{\delta}{\delta J(z_2)}\Bigr)
\exp\Bigl[-\frac12\int d^4x\,d^4y\,J(x)\Delta_F(x-y)J(y)\Bigr]\Big|_{J=0}\\
&=\frac12\Delta_F(z_1-z_2)+\frac12\Delta_F(z_2-z_1)\\
&=\Delta_F(z_1-z_2).
\end{aligned}}
\right.
\tag{3.51}
```

**微扰展开**

由 (3.12)，每个 $`-i\,\delta/\delta J(z)`$ 作用于 (3.41) 都插入一个 $`\phi(z)`$，因此

```math
\left.
\begin{aligned}
K(\Phi_f,\Phi_i)
&=\int_{\Phi_i}^{\Phi_f}\mathcal D\phi\,\exp\Bigl(iS_0[\phi]+i\int d^4z\,\Bigl(-\frac{\lambda}{3!}\Bigr)\phi^3\Bigr)\\
&=\int_{\Phi_i}^{\Phi_f}\mathcal D\phi\,e^{iS_0[\phi]}\sum_{m=0}^\infty\frac1{m!}\Bigl(i\int d^4z\,\Bigl(-\frac{\lambda}{3!}\Bigr)\phi(z)^3\Bigr)^m\\
&=\sum_{m=0}^\infty\frac1{m!}\Bigl(-\frac{i\lambda}{3!}\Bigr)^m\prod_{k=1}^m\int d^4z_k\Bigl(-i\frac{\delta}{\delta J(z_k)}\Bigr)^3K_0^J(\Phi_f,\Phi_i)\Big|_{J=0}\\
&=\sum_{m=0}^\infty\frac1{m!}\Bigl(\frac{\lambda}{3!}\Bigr)^m\prod_{k=1}^m\int d^4z_k\Bigl(\frac{\delta}{\delta J(z_k)}\Bigr)^3K_0^J(\Phi_f,\Phi_i)\Big|_{J=0}.
\end{aligned}
\right.
\tag{3.52}
```

两端都取 $`S_0`$ 的真空，由 (3.49) 得

```math
\left.
\boxed{
\begin{aligned}
K(\mathrm{vac}_f,\mathrm{vac}_i)
&=\sum_{m=0}^\infty\frac1{m!}\Bigl(\frac{\lambda}{3!}\Bigr)^m\prod_{k=1}^m\int d^4z_k\Bigl(\frac{\delta}{\delta J(z_k)}\Bigr)^3\\
&\qquad\exp\Bigl[-\frac12\int d^4x\,d^4y\,J(x)\Delta_F(x-y)J(y)\Bigr]\Big|_{J=0}\cdot K_0(\mathrm{vac}_f,\mathrm{vac}_i).
\end{aligned}}
\right.
\tag{3.53}
```

<br><br>

<a id="path-integrals-for-fermion-fields"></a>
### 3.4 费米子场的路径积分

<a id="grassmann-algebra"></a>
#### Grassmann 代数

**代数**

设 $`\mathbb K=\mathbb R`$ 或 $`\mathbb C`$。

- **代数**：$`\mathbb K`$ 上的向量空间 $`\mathcal A`$，带有乘积

```math
\left.
\begin{aligned}
\mathcal A\times\mathcal A&\to\mathcal A,\\
(u,v)&\mapsto uv,
\end{aligned}
\right.
\tag{3.54}
```

且乘积是双线性的：对所有 $`\alpha,\beta\in\mathbb K`$ 与 $`u,v,w\in\mathcal A`$，

```math
\left.
\begin{aligned}
u(\alpha v+\beta w)&=\alpha\,uv+\beta\,uw,\\
(\alpha v+\beta w)u&=\alpha\,vu+\beta\,wu.
\end{aligned}
\right.
\tag{3.55}
```

- **含幺代数**：含有元素 $`1\in\mathcal A`$ 的代数，使得对所有 $`u\in\mathcal A`$ 都有 $`1u=u=u1`$。
  - 对 $`\alpha\in\mathbb K`$，把 $`\alpha1`$ 记为 $`\alpha`$。
- **结合代数**：对所有 $`u,v,w\in\mathcal A`$ 都有 $`(uv)w=u(vw)`$ 的代数。

**生成元**

- **生成子代数**：对 $`\mathbb K`$ 上的含幺结合代数 $`\mathcal A`$ 以及元素为 $`u_a`$ 的子集 $`\Sigma\subset\mathcal A`$，由 $`\Sigma`$ 生成的子代数为

```math
\left.
\mathcal A(\Sigma):=\Bigl\{f_0+\sum_{k\ge1}\sum_{a_1,\ldots,a_k}f_{a_1\cdots a_k}\,u_{a_1}\cdots u_{a_k}\;:\;f_0,\,f_{a_1\cdots a_k}\in\mathbb K\Bigr\},
\right.
\tag{3.56}
```

其中只有有限个系数非零。

- **生成集**：若 $`\mathcal A(\Sigma)=\mathcal A`$，则称 $`\Sigma`$ 为 $`\mathcal A`$ 的生成集。

**Grassmann 代数**

- **Grassmann（外）代数**：$`\mathbb K`$ 上具有生成集 $`\{\zeta_1,\ldots,\zeta_n\}`$ 的含幺结合代数，满足

```math
\left.
\zeta_a\zeta_b+\zeta_b\zeta_a=0,\qquad a,b=1,\ldots,n,
\right.
\tag{3.57}
```

特别地，$`\zeta_a^2=0`$。不再附加其他关系：$`\zeta_a`$ 之间的任何关系都由 (3.57) 推出。该代数记为 $`\mathcal G(\zeta_1,\ldots,\zeta_n)`$，或 $`\mathcal G_n`$。

- **基**：有序单项式 $`1`$ 与满足 $`a_1<\cdots<a_k`$ 的 $`\zeta_{a_1}\cdots\zeta_{a_k}`$ 在 $`\mathbb K`$ 上线性无关，且

```math
\left.
\begin{aligned}
\mathcal G_n&=\mathop{\rm span}\nolimits\,_{\mathbb K}\{1,\ \zeta_{a_1}\cdots\zeta_{a_k}\mid 1\le a_1<\cdots<a_k\le n\},\\
\dim_{\mathbb K}\mathcal G_n&=2^n.
\end{aligned}
\right.
\tag{3.58}
```

- **展开**：每个 $`f\in\mathcal G_n`$ 都有唯一的展开

```math
\left.
f=\sum_{k=0}^n\sum_{1\le a_1<\cdots<a_k\le n}f_{a_1\cdots a_k}\,\zeta_{a_1}\cdots\zeta_{a_k},\qquad f_{a_1\cdots a_k}\in\mathbb K,
\right.
\tag{3.59}
```

其中 $`k=0`$ 的项为 $`f_0`$。

<br><br>

<a id="grassmann-calculus"></a>
#### Grassmann 代数上的微积分

<br><br>

<a id="symmetry-in-path-integrals"></a>
### 3.5 路径积分中的对称性

<br><br>

<a id="scattering-theory-in-path-integrals"></a>
### 3.6 路径积分中的散射理论

<br><br>

<a id="qft-ch4"></a>
## 4. 散射理论

<a id="interaction-picture-dyson"></a>
<a id="perturbation-theory"></a>
<a id="interaction-picture"></a>
### 4.1 相互作用绘景

设哈密顿量为

```math
\left.
\hat H=\hat H_0+\hat V
\right.
\tag{4.1}
```

相互作用绘景用 (4.1) 中的 $`\hat H_0`$ 而不是 $`\hat H`$ 来演化算符：

```math
\left.
\boxed{
\begin{gathered}
\hat O_I(t):=e^{i\hat H_0t}\,\hat O_S\,e^{-i\hat H_0t},\\[4pt]
|\psi_I(t)\rangle:=e^{i\hat H_0t}\,|\psi_S(t)\rangle .
\end{gathered}
}
\right.
\tag{4.2}
```

三个绘景在 $`t=0`$ 时重合，且 $`\langle\psi_I(t)|\hat O_I(t)|\psi_I(t)\rangle=\langle\psi_S(t)|\hat O_S|\psi_S(t)\rangle`$。

对 (4.2) 的第一式求导，

```math
\left.
\frac{d\hat O_I}{dt}=i\,[\hat H_0,\hat O_I].
\right.
\tag{4.3}
```

特别地，$`\hat H_{0,I}=\hat H_0`$，而相互作用项变为含时的。对 (4.2) 的第二式求导，并利用 $`i\partial_t|\psi_S\rangle=\hat H|\psi_S\rangle`$，

```math
\left.
i\partial_t|\psi_I(t)\rangle
=e^{i\hat H_0t}\bigl(\hat H-\hat H_0\bigr)|\psi_S(t)\rangle
=e^{i\hat H_0t}\hat Ve^{-i\hat H_0t}\,|\psi_I(t)\rangle,
\right.
\tag{4.4}
```

即

```math
\left.
\boxed{
i\partial_t|\psi_I(t)\rangle=\hat V_I(t)\,|\psi_I(t)\rangle,
\qquad
\hat V_I(t):=e^{i\hat H_0t}\,\hat V\,e^{-i\hat H_0t}.
}
\right.
\tag{4.5}
```

把 $`\hat O_S=e^{-i\hat H_0t}\hat O_I(t)e^{i\hat H_0t}`$ 代入 (2.23)，

```math
\left.
\hat O_H(t)=\hat U_I(t,0)^\dagger\,\hat O_I(t)\,\hat U_I(t,0),
\qquad
\hat U_I(t,0):=e^{i\hat H_0t}\,\hat U_S(t,0).
\right.
\tag{4.6}
```

对场算符，(4.6) 写作 $`\hat\phi_H(t,\mathbf x)=\hat U_I(t,0)^\dagger\,\hat\phi_I(t,\mathbf x)\,\hat U_I(t,0)`$，且由 (4.3)，$`\hat\phi_I(t,\mathbf x)`$ 满足仅由 $`\hat H_0`$ 给出的 Heisenberg 方程。

**Dyson 级数**

态方程 (4.5) 就是把 (2.3) 中的 $`\hat H_S`$ 换成 $`\hat V_I(t)`$ 所得的方程。因此，由 $`|\psi_I(t)\rangle=\hat U_I(t,t_0)|\psi_I(t_0)\rangle`$ 定义的相互作用绘景演化算符 $`\hat U_I(t,t_0)`$，就是在 (2.18) 的 $`\hat U_S(t,t_0)`$ 中作替换 $`\hat H_S\to\hat V_I(t)`$ 所得的算符：它是幺正的，满足 $`\hat U_I(t_1,t_2)\hat U_I(t_2,t_3)=\hat U_I(t_1,t_3)`$，且 $`\hat U_I(t,t_0)^\dagger=\hat U_I(t_0,t)`$。由 (4.2) 与 (2.18)，

```math
\left.
\hat U_I(t,t_0)=e^{i\hat H_0t}\,\hat U_S(t,t_0)\,e^{-i\hat H_0t_0},
\right.
\tag{4.7}
```

上式在 $`t_0=0`$ 时化为 (4.6) 中的 $`\hat U_I(t,0)`$；当 $`\hat H`$ 不显含时间时，由 (2.4)，$`\hat U_S(t,t_0)=e^{-i\hat H(t-t_0)}`$。由于一般有 $`[\hat V_I(t_1),\hat V_I(t_2)]\neq0`$，适用 [2.1 节](QFT-zh-part-02.md#schrodinger-picture) 的情况 (3)，由 (2.11) 得

```math
\left.
\boxed{
\hat U_I(t,t_0)=\mathcal T\exp\Bigl(-i\int_{t_0}^{t}dt'\,\hat V_I(t')\Bigr).
}
\right.
\tag{4.8}
```

在场论中，$`\hat V=\int d^3x\,\hat{\mathcal H}_{\mathrm{int}}\bigl(\hat\phi_S(\mathbf x)\bigr)`$。由 (4.2)，$`\hat V_I(t)=\int d^3x\,\hat{\mathcal H}_{\mathrm{int}}\bigl(\hat\phi_I(t,\mathbf x)\bigr)`$，于是 (4.8) 化为

```math
\left.
\hat U_I(t,t_0)=\mathcal T\exp\Bigl(-i\int_{t_0}^{t}dt'\int d^3x\,\hat{\mathcal H}_{\mathrm{int}}\bigl(\hat\phi_I(x)\bigr)\Bigr).
\right.
\tag{4.9}
```

对不含导数耦合的相互作用，$`\hat{\mathcal H}_{\mathrm{int}}=-\hat{\mathcal L}_{\mathrm{int}}`$。

<br><br>

<a id="s-matrix-and-wick-theorem"></a>
### 4.2 S 矩阵与 Wick 定理

**渐近态与 S 矩阵**

假设渐近粒子是稳定的，且自由粒子波包极限存在。入态在 $`t\to-\infty`$ 时趋于相应的自由态，出态在 $`t\to+\infty`$ 时趋于相应的自由态。在微扰论中，采用绝热开关并去掉真空相位，

```math
\left.
\begin{aligned}
S_{fi}&:=\langle f,\mathrm{out}|i,\mathrm{in}\rangle=\langle f|\hat S|i\rangle,\\
\hat S&=\hat U_I(+\infty,-\infty)
=\mathcal T\exp\left(-i\int_{-\infty}^{+\infty}dt\,\hat V_I(t)\right).
\end{aligned}
\right.
\tag{4.10}
```

设 $`p_i`$ 与 $`p_f`$ 分别为初态与末态的总四动量。连通不变振幅 $`\mathcal M_{fi}`$ 与跃迁算符 $`\hat T`$ 由下式定义

```math
\left.
\boxed{\begin{aligned}
\hat S&=1+i\hat T,\qquad
\langle f|\hat T|i\rangle_{\mathrm c}=(2\pi)^4\delta^{(4)}(p_f-p_i)\,\mathcal M_{fi},\\
\hat S^\dagger\hat S&=1\quad\Longrightarrow\quad -i(\hat T-\hat T^\dagger)=\hat T^\dagger\hat T.
\end{aligned}}
\right.
\tag{4.11}
```

**正规序、收缩与 Wick 定理**

正规序相对于自由真空 $`|0\rangle`$ 定义。对自由实标量场，其收缩即费曼传播子；默认 $`\varepsilon\to0^+`$：

```math
\left.
\begin{aligned}
\Delta_F(x-y)&:=\langle0|\mathcal T[\hat\phi_I(x)\hat\phi_I(y)]|0\rangle\\
&=\mathcal T[\hat\phi_I(x)\hat\phi_I(y)]-:\hat\phi_I(x)\hat\phi_I(y):\\
&=\int\frac{d^4p}{(2\pi)^4}\,\frac{i\,e^{-ip\cdot(x-y)}}{p^2-m^2+i\varepsilon}.
\end{aligned}
\right.
\tag{4.12}
```

Wick 定理把自由场的编时乘积表示为对所有不相交收缩的求和，其中包括不作任何收缩的项。记 $`\hat\phi_j:=\hat\phi_I(x_j)`$，

```math
\left.
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
\right.
\tag{4.13}
```

对费米子，编时与 Wick 收缩都要带上重排费米子算符所需置换的符号。自由真空期望值只保留完全收缩的项。


<br><br>

<a id="feynman-diagrams"></a>
### 4.3 费曼图与费曼规则

**标量的例子**

对四次耦合为 $`\lambda`$ 的实标量场，动量空间中的规则给出对 $`i\mathcal M`$ 的贡献。树级下，

```math
\left.
\begin{aligned}
\mathcal L&=\frac12\partial_\mu\phi\,\partial^\mu\phi-\frac12m^2\phi^2-\frac{\lambda}{4!}\phi^4,\qquad
\hat{\mathcal H}_{\mathrm{int}}=\frac{\lambda}{4!}\hat\phi_I^4,\\
\text{标量内线}:&\quad\widetilde\Delta_F(p)=\frac{i}{p^2-m^2+i\varepsilon},\qquad
\text{四标量顶点}:\quad -i\lambda,\\
 i\mathcal M_{\phi\phi\to\phi\phi}^{\mathrm{tree}}&=-i\lambda.
\end{aligned}
\right.
\tag{4.14}
```

**传播子与外态**

定义 $`S_F(x-y):=\langle0|\mathcal T[\hat\psi_I(x)\overline{\hat\psi}_I(y)]|0\rangle`$ 与 $`D_{\mu\nu}(x-y):=\langle0|\mathcal T[\hat A_{I,\mu}(x)\hat A_{I,\nu}(y)]|0\rangle`$，其 Fourier 变换为

```math
\left.
\begin{aligned}
\widetilde S_F(p)&=\frac{i(\not p+m)}{p^2-m^2+i\varepsilon},\\
\widetilde D_{\mu\nu}^{(\xi)}(p)&=\frac{-i}{p^2+i\varepsilon}\left[\eta_{\mu\nu}-(1-\xi)\frac{p_\mu p_\nu}{p^2+i\varepsilon}\right],
\qquad \mathcal L_{\mathrm{gf}}=-\frac1{2\xi}(\partial_\mu A^\mu)^2,\\
\widetilde D_{\mu\nu}^{\mathrm{Proca}}(p)&=\frac{-i}{p^2-m_V^2+i\varepsilon}\left(\eta_{\mu\nu}-\frac{p_\mu p_\nu}{m_V^2}\right),\qquad m_V>0.
\end{aligned}
\right.
\tag{4.15}
```

其中 $`\xi`$ 为协变规范参数（$`\xi=1`$ 为费曼规范），$`m_V`$ 为 Proca 质量。对单粒子极点留数为 1 的场，外态因子为

```math
\left.
\begin{array}{c|cc}
\text{外态}&\text{入射}&\text{出射}\\ \hline
\text{标量}&1&1\\
\text{费米子}&u^s(p)&\bar u^s(p)\\
\text{反费米子}&\bar v^s(p)&v^s(p)\\
\text{矢量}&\epsilon_\mu^r(p)&\epsilon_\mu^{r*}(p)
\end{array}
\right.
\tag{4.16}
```

$`\epsilon_\mu^r`$ 为物理偏振矢量。外传播子被截去；对一般的场归一化，需要用到 [4.5 节](#lsz-reduction) 中的极点留数因子。

**图的规则**

在每个顶点施加四动量守恒，每个独立圈动量用 $`d^4\ell/(2\pi)^4`$ 积分，并对连通截肢图求和。去掉整体因子 $`(2\pi)^4\delta^{(4)}(p_f-p_i)`$，即得 $`i\mathcal M`$。每个图都要除以外腿固定时的对称因子。每个闭合费米子圈额外贡献一个负号；交换全同的外费米子也改变符号。

例如，$`s`$ 道单圈四标量图的对称因子为 $`2`$：

```math
\left.
i\mathcal M_s^{\mathrm{1\,loop}}
=\frac{(-i\lambda)^2}{2}\int\frac{d^4\ell}{(2\pi)^4}
\frac{i}{\ell^2-m^2+i\varepsilon}
\frac{i}{(\ell+p_1+p_2)^2-m^2+i\varepsilon},
\qquad s:=(p_1+p_2)^2.
\right.
\tag{4.17}
```

圈积分需要正规子，在重整化的振幅中还需要相应的反项。完整的单圈四点振幅也包含交叉道。


<br><br>

<a id="correlation-functions"></a>
### 4.4 关联函数

<a id="perturbative-correlation-functions"></a>
#### 微扰真空关联函数

**真空关联函数**

设 $`|\Omega\rangle`$ 为相互作用真空，$`|0\rangle`$ 为自由真空。

```math
\left.
\begin{aligned}
G_n(x_1,\ldots,x_n)&:=\frac{\langle\Omega|\mathcal T[\hat\phi_H(x_1)\cdots\hat\phi_H(x_n)]|\Omega\rangle}{\langle\Omega|\Omega\rangle}\\
&=\frac{\langle0|\mathcal T\left[\hat\phi_I(x_1)\cdots\hat\phi_I(x_n)\exp\left(-i\int dt\,\hat V_I(t)\right)\right]|0\rangle}
{\langle0|\mathcal T\exp\left(-i\int dt\,\hat V_I(t)\right)|0\rangle}.
\end{aligned}
\right.
\tag{4.18}
```

分母消去不连通的真空泡。若每个连通分支都带有外部场插入，对 $`G_n`$ 有贡献的图仍可以是不连通的。

**生成泛函与连通函数**

对实标量源 $`J(x)`$，

```math
\left.
\begin{aligned}
Z[J]&:=\frac{\langle\Omega|\mathcal T\exp\left(i\int d^4x\,J(x)\hat\phi_H(x)\right)|\Omega\rangle}{\langle\Omega|\Omega\rangle},\qquad Z[0]=1,\qquad W[J]:=-i\ln Z[J],\\
G_n(x_1,\ldots,x_n)&=\left.\frac1{i^n}\frac{\delta^nZ[J]}{\delta J(x_1)\cdots\delta J(x_n)}\right|_{J=0},\\
G_{n,\mathrm c}(x_1,\ldots,x_n)&=\left.i^{1-n}\frac{\delta^nW[J]}{\delta J(x_1)\cdots\delta J(x_n)}\right|_{J=0}.
\end{aligned}
\right.
\tag{4.19}
```

当 $`G_1=0`$ 时，四点函数按下式分解为连通贡献与不连通贡献

```math
\left.
\begin{aligned}
G_4(x_1,x_2,x_3,x_4)
&=G_{4,\mathrm c}(x_1,x_2,x_3,x_4)
+G_2(x_1,x_2)G_2(x_3,x_4)\\
&\quad+G_2(x_1,x_3)G_2(x_2,x_4)
+G_2(x_1,x_4)G_2(x_2,x_3).
\end{aligned}
\right.
\tag{4.20}
```




<br><br>

<a id="nonperturbative-correlation-functions"></a>
#### 非微扰真空关联函数





<br><br>

<a id="lsz-reduction"></a>
### 4.5 LSZ 约化公式



**单粒子极点**

考虑一个实标量场，其真空期望值为零，有一个物理质量为 $`m_{\mathrm{phys}}>0`$ 的孤立稳定单粒子极点，且与该粒子有非零交叠。选取粒子态的相位，使得

```math
\left.
\begin{aligned}
\langle\Omega|\hat\phi_H(0)|\mathbf p\rangle&=\sqrt{Z_{\mathrm{pole}}},\qquad Z_{\mathrm{pole}}>0,\qquad \langle\Omega|\Omega\rangle=1,\\
\widetilde G_2(p)&:=\int d^4x\,e^{ip\cdot x}G_2(x,0)
=\frac{iZ_{\mathrm{pole}}}{p^2-m_{\mathrm{phys}}^2+i\varepsilon}
+\text{在极点处正则的项}.
\end{aligned}
\right.
\tag{4.21}
```

其中 $`Z_{\mathrm{pole}}`$ 为所选场归一化下的极点留数。假设相应的渐近散射态存在。

**约化公式**

对 $`r`$ 个入射动量 $`p_a`$ 与 $`s`$ 个出射动量 $`q_b`$（物理能量均为正），把每个位置都用 $`e^{+ik\cdot x}`$ 作 Fourier 变换，由此定义 $`\widetilde G_{r+s,\mathrm c}`$。对 $`r+s>2`$ 的连通散射过程，

```math
\left.
\boxed{\begin{aligned}
&i(2\pi)^4\delta^{(4)}\left(\sum_{b=1}^{s}q_b-\sum_{a=1}^{r}p_a\right)\mathcal M_{fi}\\
&\quad=\lim_{\mathrm{on\ shell}}
\left[\prod_{b=1}^{s}\frac{q_b^2-m_{\mathrm{phys}}^2}{i\sqrt{Z_{\mathrm{pole}}}}\right]
\left[\prod_{a=1}^{r}\frac{p_a^2-m_{\mathrm{phys}}^2}{i\sqrt{Z_{\mathrm{pole}}}}\right]
\widetilde G_{r+s,\mathrm c}(q_1,\ldots,q_s,-p_1,\ldots,-p_r).
\end{aligned}}
\right.
\tag{4.22}
```

这里的极限是指：先按费曼处方同时提取所有外腿极点的留数，再令所有外动量在壳。每个因子去掉一条外传播子及其场交叠。归一化为单位极点留数的场有 $`Z_{\mathrm{pole}}=1`$。


<br><br>

<a id="cross-sections-and-decay-rates"></a>
### 4.6 截面与衰变率

**相空间与态求和**

对末态总动量 $`P`$ 与 $`n`$ 个在壳出射动量 $`k_j`$，

```math
\left.
d\Phi_n(P;k_1,\ldots,k_n):=(2\pi)^4\delta^{(4)}\left(P-\sum_{j=1}^{n}k_j\right)
\prod_{j=1}^{n}\frac{d^3k_j}{(2\pi)^3\,2E_{\mathbf k_j}},\qquad
E_{\mathbf k_j}=\sqrt{\mathbf k_j^2+m_j^2}.
\right.
\tag{4.23}
```

用 $`\overline{|\mathcal M|^2}`$ 表示对未观测的末态自旋与内部量子数求和、并对等概率分布的初态求平均的结果。对两个非极化的初态粒子，若它们分别有 $`N_1,N_2`$ 个这样的态，

```math
\left.
\overline{|\mathcal M|^2}:=\frac1{N_1N_2}\sum_{\text{初态、末态}}|\mathcal M|^2,
\qquad C_{\mathrm{id}}:=\prod_a\nu_a!.
\right.
\tag{4.24}
```

其中 $`\nu_a`$ 为末态中第 $`a`$ 种全同粒子的个数。对带标记的末态动量在完整相空间上积分时，要除以 $`C_{\mathrm{id}}`$；若积分区域已使每个物理末态位形只计一次，则省去这一因子。固定的初态偏振不作平均。

**截面与衰变率**

对 $`1+2\to n`$ 散射，以及质量为 $`M`$ 的静止粒子的衰变，

```math
\left.
\boxed{\begin{aligned}
d\sigma&=\frac{\overline{|\mathcal M|^2}}{4\sqrt{(p_1\cdot p_2)^2-m_1^2m_2^2}}\,\frac{d\Phi_n(p_1+p_2)}{C_{\mathrm{id}}},\\
d\Gamma&=\frac{\overline{|\mathcal M|^2}}{2M}\,\frac{d\Phi_n(P)}{C_{\mathrm{id}}},\qquad P=(M,\mathbf0).
\end{aligned}}
\right.
\tag{4.25}
```

在衰变公式中，若要得到非极化的衰变率，只对母粒子的初态求平均。对两体末态，用质心系中初态与末态的单粒子三动量大小 $`|\mathbf p_1|`$ 与 $`|\mathbf k_1|`$：

```math
\left.
\begin{aligned}
\frac{d\sigma_{2\to2}}{d\Omega}
&=\frac1{64\pi^2s\,C_{\mathrm{id}}}\frac{|\mathbf k_1|}{|\mathbf p_1|}\,\overline{|\mathcal M|^2},\qquad s=(p_1+p_2)^2,\\
\frac{d\Gamma_{1\to2}}{d\Omega}
&=\frac{|\mathbf k_1|}{32\pi^2M^2\,C_{\mathrm{id}}}\,\overline{|\mathcal M|^2},\\
\Gamma_{1\to2}&=\frac{|\mathbf k_1|}{8\pi M^2\,C_{\mathrm{id}}}\,\overline{|\mathcal M|^2}\qquad\text{若振幅平方与角度无关}.
\end{aligned}
\right.
\tag{4.26}
```

在衰变公式中，$`|\mathbf k_1|`$ 在母粒子静止系中取值。立体角积分采用与完整相空间相同的全同粒子计数约定。


<br><br>

<a id="qft-ch5"></a>
## 5. 标准模型

<a id="yang-mills"></a>
### 5.1 Yang–Mills 理论

**李群**

```math
\left.
\begin{aligned}
U(n)&=\{A\in M_n(\mathbb C)\mid A^\dagger A=I\},\\[6pt]
SU(n)&=\{A\in M_n(\mathbb C)\mid \det A=1,\ A^\dagger A=I\}.
\end{aligned}
\right.
\tag{5.1}
```


**$`U(n)`$**

考虑单参数子群

```math
\left.
\begin{aligned}
g(\theta)&=e^{i\theta T},\qquad \theta\in\mathbb R,\quad T\in M_n(\mathbb C),\\[6pt]
\left.\frac{d}{d\theta}g(\theta)\right|_{\theta=0}&=iT,\\[6pt]
g^\dagger(\theta)g(\theta)=I\quad\text{对所有 }\theta\in\mathbb R
&\Longrightarrow i(T-T^\dagger)=0
\Longrightarrow T^\dagger=T.
\end{aligned}
\right.
\tag{5.2}
```

 李代数为

```math
\left.
\mathfrak{u}(n)=\{iT\in M_n(\mathbb C)\mid T^\dagger=T\}.
\right.
\tag{5.3}
```


**$`SU(n)`$**

单参数子群及其生成元为

```math
\left.
\begin{aligned}
g(\theta)&=e^{i\theta T},\qquad \theta\in\mathbb R,\quad T\in M_n(\mathbb C),\\[6pt]
\left.\frac{d}{d\theta}g(\theta)\right|_{\theta=0}&=iT.
\end{aligned}
\right.
\tag{5.4}
```


```math
\left.
0=\left.\frac{d}{d\theta}\bigl[g^\dagger(\theta)g(\theta)\bigr]\right|_{\theta=0}
=i(T-T^\dagger)
\quad\Longrightarrow\quad T^\dagger=T.
\right.
\tag{5.5}
```

我们用到定理 $`\det(e^{i\theta T})=e^{i\theta\,\mathop{\rm tr}\nolimits\,T}`$，它对任意 $`T\in M_n(\mathbb C)`$ 和 $`\theta\in\mathbb C`$ 成立。

```math
\left.
0=\left.\frac{d}{d\theta}\det g(\theta)\right|_{\theta=0}
=\left.\frac{d}{d\theta}e^{i\theta\,\mathop{\rm tr}\nolimits\,T}\right|_{\theta=0}
=i\,\mathop{\rm tr}\nolimits\,T
\quad\Longrightarrow\quad \mathop{\rm tr}\nolimits\,T=0.
\right.
\tag{5.6}
```

因此 $`T`$ 是无迹的厄米矩阵，李代数为

```math
\left.
\mathfrak{su}(n)=\{iT\in M_n(\mathbb C)\mid
\mathop{\rm tr}\nolimits\,T=0,\ T^\dagger=T\}.
\right.
\tag{5.7}
```

为保持反厄米性，数乘取在 $`\mathbb R`$ 上；因此 $`\mathfrak{su}(n)`$ 和 $`\mathfrak{u}(n)`$ 都是实李代数。

<a id="ym-4"></a>
**结构常数**

设 $`\{iT^a\}`$ 是实李代数 $`\mathfrak{su}(n)`$ 的一组基，其中 $`a=1,\ldots,n^2-1`$。
结构常数 $`f^{abc}`$ 由 $`[T^a,T^b]=if^{abc}T^c`$ 定义。

**实性：$`f^{abc}\in\mathbb R`$。**

由于矩阵 $`T^a`$ 厄米，

```math
\left.
\begin{aligned}
([T^a,T^b])^\dagger&=-[T^a,T^b],\qquad
\mathop{\rm tr}\nolimits [T^a,T^b]=0,\\[6pt]
[T^a,T^b]&\in\mathfrak{su}(n),\\[6pt]
[T^a,T^b]&=f^{abc}(iT^c),\qquad f^{abc}\in\mathbb R.
\end{aligned}
\right.
\tag{5.8}
```

由于 $`\{iT^c\}`$ 是 $`\mathbb R`$ 上的基，展开系数为实数。

<a id="ym-orthonormal"></a>
**$`\mathfrak{su}(n)`$ 的正交归一基**

对 $`iT_1,iT_2\in\mathfrak{su}(n)`$，定义

```math
\left.
\begin{aligned}
(\cdot,\cdot)&:\mathfrak{su}(n)\times\mathfrak{su}(n)\longrightarrow\mathbb R,\\[6pt]
(iT_1,iT_2)&:=-2\,\mathop{\rm tr}\nolimits \bigl[(iT_1)(iT_2)\bigr]\\
&=2\,\mathop{\rm tr}\nolimits (T_1T_2).
\end{aligned}
\right.
\tag{5.9}
```

**证明** (5.9) 满足内积公理



*(i) 实值性。*

利用 $`T_1^\dagger=T_1`$、$`T_2^\dagger=T_2`$ 以及迹的循环性，

```math
\left.
\begin{aligned}
\bigl[\mathop{\rm tr}\nolimits (T_1T_2)\bigr]^*
&=\mathop{\rm tr}\nolimits \bigl[(T_1T_2)^\dagger\bigr]
=\mathop{\rm tr}\nolimits (T_2^\dagger T_1^\dagger)\\
&=\mathop{\rm tr}\nolimits (T_2T_1)
=\mathop{\rm tr}\nolimits (T_1T_2),
\end{aligned}
\right.
\tag{5.10}
```

因此 $`(iT_1,iT_2)=2\,\mathop{\rm tr}\nolimits (T_1T_2)\in\mathbb R`$。

*(ii) 对称性。*

由迹的循环性，

```math
\left.
\begin{aligned}
(iT_1,iT_2)&=2\,\mathop{\rm tr}\nolimits (T_1T_2)\\
&=2\,\mathop{\rm tr}\nolimits (T_2T_1)=(iT_2,iT_1).
\end{aligned}
\right.
\tag{5.11}
```

*(iii) 双线性。*

对 $`a,b\in\mathbb R`$，有 $`a\,iT_1+b\,iT_2=i(aT_1+bT_2)`$，
再由迹的线性得 $`(a\,iT_1+b\,iT_2,\,iT_3)=2\,\mathop{\rm tr}\nolimits \bigl[(aT_1+bT_2)T_3\bigr]=a\,(iT_1,iT_3)+b\,(iT_2,iT_3)`$。由 (ii)，该形式对第二个宗量也是线性的。

*(iv) 正定性。* 利用 $`T=T^\dagger`$，

```math
\left.
\begin{aligned}
(iT,iT)&=2\,\mathop{\rm tr}\nolimits (T^2)=2\,\mathop{\rm tr}\nolimits (T^\dagger T)\\
&=2\sum_{j,k}|T_{jk}|^2\ge0.
\end{aligned}
\right.
\tag{5.12}
```

等号成立当且仅当对所有 $`j,k`$ 都有 $`T_{jk}=0`$，即 $`iT=0`$。$`\square`$

既然已证明该形式是 $`\mathfrak{su}(n)`$ 上的内积，就可以选取满足 $`(iT^a,iT^b)=\delta^{ab}`$ 的正交归一基 $`\{iT^a\}`$。等价地，

```math
\left.
\boxed{\mathop{\rm tr}\nolimits (T^aT^b)=\frac12\delta^{ab}.}
\right.
\tag{5.13}
```

**全反对称性**。利用这一归一化与迹的循环性，得到

```math
\left.
\begin{aligned}
\mathop{\rm tr}\nolimits ([T^a,T^b]T^c)&=\frac{i}{2}f^{abc},\\
f^{abc}&=-2i\,\mathop{\rm tr}\nolimits ([T^a,T^b]T^c),\\
f^{bac}&=-f^{abc},\\
f^{acb}
&=-2i\,\mathop{\rm tr}\nolimits (T^aT^cT^b-T^cT^aT^b)\\
&=-2i\,\mathop{\rm tr}\nolimits (T^bT^aT^c-T^aT^bT^c)
=-f^{abc}.
\end{aligned}
\right.
\tag{5.14}
```

```math
\left.
\boxed{
f^{abc}=f^{[abc]}\in\mathbb R
}
\right.
\tag{5.15}
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
\left.
\Psi(x):=\begin{pmatrix}
\psi_1(x)\\
\vdots\\
\psi_n(x)
\end{pmatrix}.
\right.
\tag{5.16}
```

Dirac 共轭定义为

```math
\left.
\begin{aligned}
\bar\Psi(x)&:=\bigl(\bar\psi_1(x),\ldots,\bar\psi_n(x)\bigr),\\[6pt]
\bar\psi_a(x)&:=\psi_a^\dagger(x)\gamma^0.
\end{aligned}
\right.
\tag{5.17}
```

拉氏量密度的动能项为

```math
\left.
\begin{aligned}
\mathcal L_{\mathrm{kin}}
&=\bar\Psi\,i\gamma^\mu I_n\partial_\mu\Psi\\[6pt]
&=\sum_{a=1}^{n}\bar\psi_a\,i\gamma^\mu\partial_\mu\psi_a.
\end{aligned}
\right.
\tag{5.18}
```



对定义表示 $`U`$ 下的 $`SU(n)`$，设 $`g_{\mathrm{YM}}`$ 为耦合常数，$`U(\theta)`$ 为局域群元的表示。联络及其变换为

```math
\left.
\begin{aligned}
U(\theta)&:=e^{i\theta^a(x)T^a},\qquad \theta^a(x)\in\mathbb R,\\
A_\mu&:=A_\mu^aT^a,\qquad D_\mu:=\partial_\mu-ig_{\mathrm{YM}}A_\mu,
\qquad \Psi'=U(\theta)\Psi,\\
A_\mu'&=U(\theta)A_\mu U(\theta)^\dagger-\frac{i}{g_{\mathrm{YM}}}\bigl(\partial_\mu U(\theta)\bigr)U(\theta)^\dagger,\\
D_\mu'&=U(\theta)D_\mu U(\theta)^\dagger .
\end{aligned}
\right.
\tag{5.19}
```

场强为

```math
\left.
\begin{aligned}
[D_\mu,D_\nu]&=:-ig_{\mathrm{YM}}F_{\mu\nu},\\
F_{\mu\nu}&=\partial_\mu A_\nu-\partial_\nu A_\mu-ig_{\mathrm{YM}}[A_\mu,A_\nu],\\
F_{\mu\nu}^a&=\partial_\mu A_\nu^a-\partial_\nu A_\mu^a
+g_{\mathrm{YM}}f^{abc}A_\mu^bA_\nu^c,\\
F_{\mu\nu}'&=U(\theta)F_{\mu\nu}U(\theta)^\dagger .
\end{aligned}
\right.
\tag{5.20}
```

计入规范场后，动能项 (5.18) 变为

```math
\left.
\boxed{
\begin{aligned}
\mathcal L_{\mathrm{kin}}
&=\bar\Psi\,i\gamma^\mu D_\mu\Psi
-\frac12\,\mathop{\rm tr}\nolimits (F_{\mu\nu}F^{\mu\nu})\\[6pt]
&=\bar\Psi\,i\gamma^\mu D_\mu\Psi-\frac14F_{\mu\nu}^aF^{a\mu\nu}.
\end{aligned}
}
\right.
\tag{5.21}
```

对取矩阵值的伴随场 $`X`$，定义 $`D_\mu X:=\partial_\mu X-ig_{\mathrm{YM}}[A_\mu,X]`$。

利用以上定义，场方程与 Bianchi 恒等式简化为

```math
\left.
\begin{aligned}
i\gamma^\mu D_\mu\Psi&=0,\qquad
D_\mu F^{\mu\nu}=-g_{\mathrm{YM}}j^\nu,\qquad
j^\nu:=(\bar\Psi\gamma^\nu T^a\Psi)T^a,\\
D_\mu F_{\nu\rho}+D_\nu F_{\rho\mu}+D_\rho F_{\mu\nu}&=0 .
\end{aligned}
\right.
\tag{5.22}
```

<br><br>

<a id="qed"></a>
### 5.2 量子电动力学


**规范群 $`U(1)`$**

QED 的规范群是 $`U(1)`$，即 (5.1) 取 $`n=1`$；其李代数 $`\mathfrak u(1)=i\mathbb R`$ 是阿贝尔的。

设 $`e>0`$ 为元电荷，$`\theta:\mathbb R^4\to\mathbb R`$。该变换是味单态：它对三代的作用相同。它在 $`U(1)`$ 的不同表示上取不同的形式，这些表示以荷标记：如 (1.100) 的 Dirac 场 $`\psi_f`$ 带荷 $`Q_fe`$，对每个 $`f`$ 取同一个 $`\theta`$，其变换为

```math
\left.
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
\right.
\tag{5.23}
```

**协变导数与场强**

光子场 $`A_\mu`$ 是实场。在 (5.19)–(5.20) 中取 $`U(\theta)=e^{iQ\theta}`$，并把 $`g_{\mathrm{YM}}A_\mu`$ 换成 $`eQA_\mu`$，得到

```math
\left.
\begin{aligned}
D_\mu&:=\partial_\mu-ieQA_\mu,\qquad
D_\mu'\psi'=e^{iQ\theta}D_\mu\psi,\\
A_\mu'&=A_\mu+\frac1e\,\partial_\mu\theta,\\
[D_\mu,D_\nu]&=-ieQF_{\mu\nu},\qquad
F_{\mu\nu}=\partial_\mu A_\nu-\partial_\nu A_\mu=F_{\mu\nu}'.
\end{aligned}
\right.
\tag{5.24}
```



**QED 拉氏量**

```math
\left.
\boxed{
\mathcal L_{\mathrm{QED}}
=\bar\psi\bigl(i\gamma^\mu D_\mu-m\bigr)\psi
-\frac14F_{\mu\nu}F^{\mu\nu},
}
\right.
\tag{5.25}
```

其中 $`m`$ 是 $`\psi`$ 的质量，$`D_\mu`$ 作用于其右侧的 $`\psi`$。由 (5.23)–(5.24)，$`\mathcal L_{\mathrm{QED}}`$ 是规范不变的。代入 $`D_\mu`$，

```math
\left.
\mathcal L_{\mathrm{QED}}
=\bar\psi\bigl(i\gamma^\mu\partial_\mu-m\bigr)\psi
-\frac14F_{\mu\nu}F^{\mu\nu}
+eQA_\mu\bar\psi\gamma^\mu\psi,
\right.
\tag{5.26}
```

即 Dirac 拉氏量 (1.100)、Maxwell 拉氏量 (1.153) 与相互作用项之和。



**运动方程**

取 (1.138) 中的 $`j^\nu=\bar\psi\gamma^\nu\psi`$，则 $`\partial\mathcal L_{\mathrm{QED}}/\partial(\partial_\mu A_\nu)=-F^{\mu\nu}`$，$`\partial\mathcal L_{\mathrm{QED}}/\partial A_\nu=eQ\,j^\nu`$。Euler–Lagrange 方程与 Bianchi 恒等式为

```math
\left.
\begin{aligned}
\bigl(i\gamma^\mu D_\mu-m\bigr)\psi&=0,\qquad
\partial_\mu F^{\mu\nu}=-eQ\,j^\nu,\qquad
\partial_\nu j^\nu=0,\\
\partial_\mu F_{\nu\rho}+\partial_\nu F_{\rho\mu}+\partial_\rho F_{\mu\nu}&=0 .
\end{aligned}
\right.
\tag{5.27}
```

<br><br>

<a id="qcd"></a>
### 5.3 量子色动力学

**色群 $`SU(3)`$**

QCD 的规范群为 $`SU(3)`$。由 (5.7) 取 $`n=3`$，$`\mathfrak{su}(3)`$ 有一组基 $`\{iT^a\}`$，$`a=1,\ldots,8`$，我们取它在 (5.13) 的意义下正交归一。标准的选取是 $`T^a:=\tfrac12\lambda^a`$，其中 Gell-Mann 矩阵为

```math
\left.
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
\right.
\tag{5.28}
```

每个 $`\lambda^a`$ 都是厄米、无迹的，并且 $`\mathop{\rm tr}\nolimits (\lambda^a\lambda^b)=2\delta^{ab}`$，因此 $`\mathop{\rm tr}\nolimits (T^aT^b)=\tfrac12\delta^{ab}`$，与 (5.13) 一致。由 (5.14)，$`f^{abc}=-2i\,\mathop{\rm tr}\nolimits ([T^a,T^b]T^c)`$；在反对称性 (5.15) 的意义下，非零的结构常数为

```math
\left.
\begin{aligned}
f^{123}&=1,\\[4pt]
f^{147}=f^{246}=f^{257}=f^{345}&=\tfrac12,\qquad
f^{156}=f^{367}=-\tfrac12,\\[4pt]
f^{458}=f^{678}&=\tfrac{\sqrt3}{2}.
\end{aligned}
\right.
\tag{5.29}
```

由于 $`f^{bac}`$ 对 $`a,c`$ 反对称，二次 Casimir 算符 $`T^aT^a`$ 与每个 $`T^b`$ 对易：

```math
\left.
[T^b,T^aT^a]=[T^b,T^a]T^a+T^a[T^b,T^a]=if^{bac}\bigl(T^cT^a+T^aT^c\bigr)=0.
\right.
\tag{5.30}
```

$`SU(3)`$ 的定义表示不可约，因此由 Schur 引理，$`T^aT^a=C_FI_3`$。利用 (5.13) 取迹，

```math
\left.
3C_F=\mathop{\rm tr}\nolimits (T^aT^a)=\tfrac12\cdot8
\quad\Longrightarrow\quad
\boxed{T^aT^a=C_FI_3,\qquad C_F=\tfrac43.}
\right.
\tag{5.31}
```

**夸克场**

对每种味 $`f\in\{u,d,s,c,b,t\}`$，夸克场是色三重态，即取 $`n=3`$ 的多重态 (5.16)，其 Dirac 共轭同 (5.17)：

```math
\left.
q_f(x):=\begin{pmatrix}\psi_{f,1}(x)\\\psi_{f,2}(x)\\\psi_{f,3}(x)\end{pmatrix},
\qquad
\bar q_f(x):=\bigl(\bar\psi_{f,1}(x),\bar\psi_{f,2}(x),\bar\psi_{f,3}(x)\bigr).
\right.
\tag{5.32}
```

本节中 $`\gamma^\mu`$ 作用于每个 $`\psi_{f,a}`$ 的旋量指标，$`3\times3`$ 矩阵 $`T^a`$ 作用于色指标，因此 $`\gamma^\mu`$ 与由 $`T^a`$ 构成的任何矩阵都对易。

**局域 $`SU(3)`$ 变换**

设 $`\theta^a:\mathbb R^4\to\mathbb R`$，$`a=1,\ldots,8`$，并令

```math
\left.
g(x):=e^{i\theta^a(x)T^a}\in SU(3).
\right.
\tag{5.33}
```

这就是 (1.72) 的内部变换，只是现在 $`g`$ 依赖于 $`x`$。夸克场的变换为

```math
\left.
q_f'(x)=g(x)\,q_f(x),\qquad
\bar q_f'(x)=\bar q_f(x)\,g^\dagger(x).
\right.
\tag{5.34}
```

由于 $`\partial_\mu(gq_f)=g\,\partial_\mu q_f+(\partial_\mu g)\,q_f`$，(5.18) 的导数项在 (5.34) 下并非不变：

```math
\left.
\bar q_f'\,i\gamma^\mu\partial_\mu q_f'
=\bar q_f\,i\gamma^\mu\partial_\mu q_f
+\bar q_f\,i\gamma^\mu g^\dagger(\partial_\mu g)\,q_f.
\right.
\tag{5.35}
```

**协变导数与胶子场**

引入八个实矢量场 $`A^a_\mu`$，即胶子场，并定义

```math
\left.
A_\mu:=A^a_\mu T^a,\qquad
D_\mu:=\partial_\mu-ig_sA_\mu,
\right.
\tag{5.36}
```

其中 $`g_s\in\mathbb R`$ 为强耦合常数，$`D_\mu`$ 作用于色三重态。记变换后的胶子场为 $`A_\mu'`$，并令 $`D_\mu':=\partial_\mu-ig_sA_\mu'`$。要求 $`D_\mu'q_f'=g\,D_\mu q_f`$：

```math
\left.
\begin{aligned}
D_\mu'(gq_f)&=g\,\partial_\mu q_f+(\partial_\mu g)\,q_f-ig_sA_\mu'\,g\,q_f,\\[6pt]
g\,D_\mu q_f&=g\,\partial_\mu q_f-ig_s\,gA_\mu\,q_f.
\end{aligned}
\right.
\tag{5.37}
```

令两式对所有 $`q_f`$ 相等，得 $`A_\mu'g=gA_\mu-\frac{i}{g_s}\partial_\mu g`$，即

```math
\left.
\boxed{
A_\mu'=gA_\mu g^\dagger-\frac{i}{g_s}(\partial_\mu g)\,g^\dagger
=gA_\mu g^\dagger+\frac{i}{g_s}\,g\,\partial_\mu g^\dagger.
}
\right.
\tag{5.38}
```

对 $`gg^\dagger=I_3`$ 求导得 $`\bigl((\partial_\mu g)g^\dagger\bigr)^\dagger=-(\partial_\mu g)g^\dagger`$；Jacobi 公式 $`\partial_\mu\det g=\det g\,\mathop{\rm tr}\nolimits (g^\dagger\partial_\mu g)`$ 结合 $`\det g=1`$ 给出 $`\mathop{\rm tr}\nolimits \bigl((\partial_\mu g)g^\dagger\bigr)=0`$。因此 $`A_\mu'`$ 仍是厄米、无迹的，$`A_\mu'=A_\mu'^aT^a`$，其中 $`A_\mu'^a`$ 为实数。

由于 $`D_\mu'(gq_f)=g\,D_\mu q_f`$ 对所有 $`q_f`$ 成立，作为作用于色三重态的算符，有

```math
\left.
D_\mu'=g\,D_\mu\,g^\dagger.
\right.
\tag{5.39}
```

对无穷小的 $`\theta^a`$，$`g=I_3+i\theta^aT^a+O(\theta^2)`$，由 (5.38) 得

```math
\left.
\begin{aligned}
A_\mu'&=A_\mu+i\theta^b[T^b,A_\mu]+\frac1{g_s}(\partial_\mu\theta^a)T^a+O(\theta^2)\\
&=A_\mu-f^{bca}\theta^bA^c_\mu T^a+\frac1{g_s}(\partial_\mu\theta^a)T^a+O(\theta^2),\\[6pt]
\delta A^a_\mu:=A_\mu'^a-A_\mu^a
&=\frac1{g_s}\partial_\mu\theta^a+f^{abc}A^b_\mu\theta^c+O(\theta^2).
\end{aligned}
\right.
\tag{5.40}
```

**场强**

用 $`[D_\mu,D_\nu]=:-ig_sF_{\mu\nu}`$ 定义 $`F_{\mu\nu}`$。由于 $`[\partial_\mu,A_\nu]q_f=(\partial_\mu A_\nu)q_f`$，

```math
\left.
\begin{aligned}
[D_\mu,D_\nu]
&=[\partial_\mu-ig_sA_\mu,\ \partial_\nu-ig_sA_\nu]\\
&=-ig_s\bigl(\partial_\mu A_\nu-\partial_\nu A_\mu\bigr)-g_s^2[A_\mu,A_\nu],\\[6pt]
F_{\mu\nu}&=\partial_\mu A_\nu-\partial_\nu A_\mu-ig_s[A_\mu,A_\nu].
\end{aligned}
\right.
\tag{5.41}
```

按基展开，$`F_{\mu\nu}=F^a_{\mu\nu}T^a`$，其中

```math
\left.
\boxed{
F^a_{\mu\nu}=\partial_\mu A^a_\nu-\partial_\nu A^a_\mu+g_sf^{abc}A^b_\mu A^c_\nu.
}
\right.
\tag{5.42}
```

由 (5.39)，$`[D_\mu',D_\nu']=g[D_\mu,D_\nu]g^\dagger`$，因此

```math
\left.
F_{\mu\nu}'=gF_{\mu\nu}g^\dagger,
\qquad
\delta F^a_{\mu\nu}=f^{abc}F^b_{\mu\nu}\theta^c+O(\theta^2).
\right.
\tag{5.43}
```

由迹的循环性及 (5.13)，

```math
\left.
\mathop{\rm tr}\nolimits \bigl(F_{\mu\nu}'F'^{\mu\nu}\bigr)
=\mathop{\rm tr}\nolimits \bigl(F_{\mu\nu}F^{\mu\nu}\bigr)
=\tfrac12F^a_{\mu\nu}F^{a\mu\nu}.
\right.
\tag{5.44}
```

**QCD 拉氏量**

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
\tag{5.45}
```

其中求和遍及 (5.32) 中的六种味，$`m_f`$ 为味 $`f`$ 的质量，$`D_\mu`$ 作用于其右侧的 $`q_f`$。在 (5.34) 与 (5.38) 下，按构造有 $`D_\mu'q_f'=g\,D_\mu q_f`$，因此

```math
\left.
\bar q_f'\bigl(i\gamma^\mu D_\mu'-m_f\bigr)q_f'
=\bar q_f\,g^\dagger\bigl(i\gamma^\mu g\,D_\mu-m_f\,g\bigr)q_f
=\bar q_f\bigl(i\gamma^\mu D_\mu-m_f\bigr)q_f.
\right.
\tag{5.46}
```

结合 (5.44)，$`\mathcal L_{\mathrm{QCD}}`$ 在局域变换 (5.34)、(5.38) 下不变。

把 (5.36) 与 (5.42) 代入 (5.45)，即可分出自由项与相互作用项：

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
\tag{5.47}
```

**运动方程**

把 $`q_f`$、$`\bar q_f`$ 与 $`A^a_\mu`$ 视为独立变量，$`\bar q_f`$ 的 Euler–Lagrange 方程为

```math
\left.
\bigl(i\gamma^\mu D_\mu-m_f\bigr)q_f=0.
\right.
\tag{5.48}
```

对 $`A^a_\nu`$，定义色流 $`j^{a\nu}:=\sum_f\bar q_f\gamma^\nu T^aq_f`$。由 (5.45) 并利用 (5.42) 与 (5.47)，

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
\tag{5.49}
```

于是 Euler–Lagrange 方程 $`\partial_\mu\bigl(\partial\mathcal L_{\mathrm{QCD}}/\partial(\partial_\mu A^a_\nu)\bigr)=\partial\mathcal L_{\mathrm{QCD}}/\partial A^a_\nu`$ 化为

```math
\left.
\boxed{
\partial_\mu F^{a\mu\nu}+g_sf^{abc}A^b_\mu F^{c\mu\nu}=-g_sj^{a\nu}.
}
\right.
\tag{5.50}
```

左边是 $`\partial_\mu F^{\mu\nu}-ig_s[A_\mu,F^{\mu\nu}]`$ 的 $`a`$ 分量，后者是 $`F^{\mu\nu}`$ 在伴随表示中的协变导数；令 $`j^\nu:=j^{a\nu}T^a`$，(5.50) 即

```math
\left.
D_\mu F^{\mu\nu}:=\partial_\mu F^{\mu\nu}-ig_s[A_\mu,F^{\mu\nu}]=-g_s\,j^\nu.
\right.
\tag{5.51}
```

<br><br>

<a id="higgs-mechanism"></a>
### 5.4 自发对称性破缺与 Higgs 机制

<a id="higgs-lagrangian"></a>
#### Higgs 拉氏量

设 $`\Phi:=(\phi_1,\ldots,\phi_n)^T`$ 为复标量场构成的多重态。对 $`\mu_H^2\in\mathbb R`$ 与 $`\lambda_H>0`$，Higgs 拉氏量为

```math
\left.
\boxed{
\begin{aligned}
\mathcal L_{\mathrm{Higgs}}&=(\partial_\mu\Phi)^\dagger\partial^\mu\Phi-V(\Phi),\\
V(\Phi)&=-\mu_H^2\,\Phi^\dagger\Phi+\lambda_H(\Phi^\dagger\Phi)^2 .
\end{aligned}
}
\right.
\tag{5.52}
```

拉氏量 (5.52) 只通过 $`\Phi^\dagger\Phi`$ 与 $`(\partial_\mu\Phi)^\dagger\partial^\mu\Phi`$ 依赖于 $`\Phi`$。对常数 $`g\in U(n)`$，

```math
\left.
\begin{aligned}
\Phi'&=g\,\Phi,\\
\Phi'^\dagger\Phi'&=\Phi^\dagger g^\dagger g\,\Phi=\Phi^\dagger\Phi,\\
(\partial_\mu\Phi')^\dagger\partial^\mu\Phi'&=(\partial_\mu\Phi)^\dagger g^\dagger g\,\partial^\mu\Phi=(\partial_\mu\Phi)^\dagger\partial^\mu\Phi,
\end{aligned}
\right.
\tag{5.53}
```

因此 $`\mathcal L_{\mathrm{Higgs}}`$ 在全局 $`U(n)`$ 变换下不变。

**物理真空**

经典真空是能量最低的场位形。(5.52) 的能量密度为

```math
\left.
\mathcal H=(\partial_0\Phi)^\dagger\partial_0\Phi+\sum_{i=1}^3(\partial_i\Phi)^\dagger\partial_i\Phi+V(\Phi).
\right.
\tag{5.54}
```

前两项非负，因此经典真空是使 $`V`$ 取最小值的常数 $`\Phi=\Phi_0`$。由于 $`\partial V/\partial(\Phi^\dagger\Phi)=-\mu_H^2+2\lambda_H\Phi^\dagger\Phi`$ 且 $`\Phi^\dagger\Phi\ge0`$，

```math
\left.
\boxed{
\begin{aligned}
\mu_H^2\le0:&\quad\Phi_0=0,\\
\mu_H^2>0:&\quad\Phi_0^\dagger\Phi_0=\frac{v_{\mathrm{SM}}^2}{2},\qquad
v_{\mathrm{SM}}:=\sqrt{\frac{\mu_H^2}{\lambda_H}},\qquad
V(\Phi_0)=-\frac{\lambda_Hv_{\mathrm{SM}}^4}{4}.
\end{aligned}
}
\right.
\tag{5.55}
```

当 $`\mu_H^2\le0`$ 时，真空 $`\Phi_0=0`$ 在整个 $`U(n)`$ 下不变。以下取 $`\mu_H^2>0`$：真空构成 $`\mathbb C^n`$ 中的球面 $`\Phi_0^\dagger\Phi_0=v_{\mathrm{SM}}^2/2`$，而 $`\Phi=0`$ 是 $`V`$ 的局部极大点。物理真空是这个球面上的一个点。选取

```math
\left.
\boxed{
\Phi_0:=\frac1{\sqrt2}\begin{pmatrix}0\\\vdots\\0\\v_{\mathrm{SM}}\end{pmatrix}
}
\right.
\tag{5.56}
```

此后 $`\Phi_0`$ 即表示这一真空。

 任一满足 $`\Phi_0'^\dagger\Phi_0'=v_{\mathrm{SM}}^2/2`$ 的真空 $`\Phi_0'`$ 都等于 $`g\,\Phi_0`$，其中 $`g\in U(n)`$ 的最后一列为 $`\sqrt2\,\Phi_0'/v_{\mathrm{SM}}`$，其余各列把它补全为 $`\mathbb C^n`$ 的正交归一基；由 (5.53)，不同的选取之间由对称变换相联系。

<br><br>

<a id="spontaneous-symmetry-breaking"></a>
#### 自发对称性破缺

若变换 $`g\in U(n)`$ 保持真空不变，则称它是未破缺的。未破缺子群为

```math
\left.
\boxed{
G_0:=\{g\in U(n)\mid g\,\Phi_0=\Phi_0\}\cong U(n-1).
}
\right.
\tag{5.57}
```

满足 $`g\Phi_0=\Phi_0`$ 的幺正矩阵 $`g`$ 把正交补 $`\Phi_0^\perp:=\{u\in\mathbb C^n\mid\Phi_0^\dagger u=0\}`$ 映到自身，而 $`g\mapsto g|_{\Phi_0^\perp}`$ 把 $`G_0`$ 等同于 $`(n-1)`$ 维空间 $`\Phi_0^\perp`$ 上的幺正群。

若 $`G_0\neq U(n)`$，即拉氏量在 $`U(n)`$ 下不变而真空不是，则称 $`U(n)`$ 自发破缺到 $`G_0`$；由 (5.57)，$`U(n)`$ 自发破缺到 $`G_0\cong U(n-1)`$。

设 $`T^a`$，$`a=1,\ldots,n^2`$，为 $`U(n)`$ 的厄米生成元，满足 $`\mathop{\rm tr}\nolimits (T^aT^b)=\frac12\delta^{ab}`$。若对所有 $`\theta\in\mathbb R`$ 都有 $`e^{i\theta T}\in G_0`$，则称厄米 $`n\times n`$ 矩阵 $`T`$ 为未破缺生成元；将 $`e^{i\theta T}\Phi_0=\Phi_0`$ 在 $`\theta=0`$ 处求导，

```math
\left.
e^{i\theta T}\in G_0\ \ \text{对所有 }\theta\in\mathbb R
\iff T\Phi_0=0 .
\right.
\tag{5.58}
```

未破缺生成元构成 $`G_0\cong U(n-1)`$ 的李代数，维数为 $`(n-1)^2`$；破缺生成元是这个李代数关于 $`\mathop{\rm tr}\nolimits\,`$ 的正交补中的元素，正交补的维数为 $`n^2-(n-1)^2=2n-1`$。破缺的 $`T\neq0`$ 满足 $`T\Phi_0\neq0`$：否则 $`T`$ 也是未破缺的，从而 $`\mathop{\rm tr}\nolimits (T^2)=0`$。

设 $`G^a`$，$`a=1,\ldots,2n-1`$，为破缺生成元的一组基。矩阵 $`\Phi_0^\dagger\{G^a,G^b\}\Phi_0=2\,\mathop{\rm Re}\nolimits \bigl[(G^a\Phi_0)^\dagger G^b\Phi_0\bigr]`$ 是实对称矩阵。正交基变换 $`G^a\to O^{ab}G^b`$，$`O\in O(2n-1)`$，保持 $`\mathop{\rm tr}\nolimits (G^aG^b)=\frac12\delta^{ab}`$ 不变，并以 $`O(\,\cdot\,)O^T`$ 的方式作用于这个矩阵；选取 $`O`$ 使它对角化，

```math
\left.
\begin{aligned}
\mathop{\rm tr}\nolimits (G^aG^b)&=\frac12\delta^{ab},\\
\Phi_0^\dagger\{G^a,G^b\}\Phi_0&=2\,\delta^{ab}\,\Phi_0^\dagger(G^a)^2\Phi_0,\qquad
\Phi_0^\dagger(G^a)^2\Phi_0=(G^a\Phi_0)^\dagger G^a\Phi_0>0 .
\end{aligned}
\right.
\tag{5.59}
```

此后对 $`a=1,\ldots,2n-1`$ 取 $`T^a:=G^a`$，而 $`T^a`$，$`a=2n,\ldots,n^2`$，张成未破缺生成元的空间。


**Higgs 场的参数化**

用 Higgs 场 $`h`$ 以及沿破缺生成元方向的 $`\theta^a`$，$`a=1,\ldots,2n-1`$，参数化 $`\Phi`$ 的 $`2n`$ 个实场：

```math
\left.
\boxed{
\begin{aligned}
\Phi&=\frac1{\sqrt2}\,e^{i\theta^a(x)G^a}\begin{pmatrix}0\\\vdots\\0\\v_{\mathrm{SM}}+h\end{pmatrix}\\
&=\Bigl(1+\frac h{v_{\mathrm{SM}}}\Bigr)U(\theta)\,\Phi_0,\\
U(\theta)&:=e^{iX},\qquad X:=\theta^a(x)G^a .
\end{aligned}
}
\right.
\tag{5.60}
```

<br><br>

<a id="higgs-mechanism-masses"></a>
#### Higgs 机制

将 $`U(n)`$ 对称性 (5.53) 规范化：生成元取 (5.59) 之后选定的 $`T^a`$，$`a=1,\ldots,n^2`$，规范场为 $`A_\mu^a`$，耦合 $`g_{\mathrm{YM}}`$ 同 (5.19)。把 (5.52) 中的 $`\partial_\mu`$ 换成 $`D_\mu`$，并加上 (5.21) 的规范场动能项，

```math
\left.
\boxed{
\begin{aligned}
\mathcal L&=(D_\mu\Phi)^\dagger D^\mu\Phi-V(\Phi)-\frac14F_{\mu\nu}^aF^{a\mu\nu},\\
D_\mu\Phi&=\partial_\mu\Phi-ig_{\mathrm{YM}}A_\mu\Phi,\qquad A_\mu:=A_\mu^aT^a .
\end{aligned}
}
\right.
\tag{5.61}
```

由 (5.19)–(5.20)，取 $`T^a`$ 为 $`U(n)`$ 的生成元，$`\mathcal L`$ 在 $`\Phi'=U(\theta)\Phi`$，$`U(\theta)=e^{i\theta^a(x)T^a}`$ 下不变；当 $`\theta^a=0`$，$`a\ge2n`$ 时，这就是 (5.60) 的 $`U(\theta)`$。

把参数化 (5.60) 代入 (5.61)。利用 (5.55) 给出的 $`\mu_H^2=\lambda_Hv_{\mathrm{SM}}^2`$ 以及 $`U^\dagger U=I_n`$，势只依赖于 $`h`$：

```math
\left.
\begin{aligned}
\Phi^\dagger\Phi&=\frac{(v_{\mathrm{SM}}+h)^2}2,\\
V&=\lambda_H\Bigl(\Phi^\dagger\Phi-\frac{v_{\mathrm{SM}}^2}2\Bigr)^2-\frac{\lambda_Hv_{\mathrm{SM}}^4}4\\
&=\lambda_Hv_{\mathrm{SM}}^2h^2+\lambda_Hv_{\mathrm{SM}}\,h^3+\frac{\lambda_H}4h^4-\frac{\lambda_Hv_{\mathrm{SM}}^4}4 .
\end{aligned}
\right.
\tag{5.62}
```

对动能项，$`\Phi_0^\dagger\Phi_0=v_{\mathrm{SM}}^2/2`$，并且由于下面的 $`A^U_\mu`$ 厄米，$`\partial_\mu h`$ 的线性项相消：

```math
\left.
\begin{aligned}
D_\mu\Phi&=\frac{\partial_\mu h}{v_{\mathrm{SM}}}\,U\Phi_0-ig_{\mathrm{YM}}\Bigl(1+\frac h{v_{\mathrm{SM}}}\Bigr)UA^U_\mu\Phi_0,\\
A^U_\mu&:=U^\dagger A_\mu U+\frac i{g_{\mathrm{YM}}}U^\dagger\partial_\mu U,\\
(D_\mu\Phi)^\dagger D^\mu\Phi&=\frac12\partial_\mu h\,\partial^\mu h\\
&\quad+\Bigl(1+\frac h{v_{\mathrm{SM}}}\Bigr)^2g_{\mathrm{YM}}^2\,\Phi_0^\dagger A^U_\mu A^{U\mu}\Phi_0 .
\end{aligned}
\right.
\tag{5.63}
```

把 (5.62) 与 (5.63) 代入 (5.61)，

```math
\left.
\boxed{
\begin{aligned}
\mathcal L={}&\frac12\partial_\mu h\,\partial^\mu h-\frac12m_h^2h^2\\
&-\lambda_Hv_{\mathrm{SM}}\,h^3-\frac{\lambda_H}4h^4+\frac{\lambda_Hv_{\mathrm{SM}}^4}4\\
&+\Bigl(1+\frac h{v_{\mathrm{SM}}}\Bigr)^2g_{\mathrm{YM}}^2\,\Phi_0^\dagger A^U_\mu A^{U\mu}\Phi_0\\
&-\frac14F_{\mu\nu}^aF^{a\mu\nu},\\
m_h^2={}&2\lambda_Hv_{\mathrm{SM}}^2=2\mu_H^2 .
\end{aligned}
}
\right.
\tag{5.64}
```

由于 $`U^\dagger\partial_\mu U=i\partial_\mu X+O(\theta\,\partial\theta)`$，到一阶有 $`A^U_\mu=A_\mu-\partial_\mu X/g_{\mathrm{YM}}`$。因为 $`a\ge2n`$ 时 $`T^a\Phi_0=0`$，由 (5.59)，$`g_{\mathrm{YM}}^2\Phi_0^\dagger A^U_\mu A^{U\mu}\Phi_0`$ 的二次部分为

```math
\left.
\begin{aligned}
&\Phi_0^\dagger\bigl(g_{\mathrm{YM}}A_\mu-\partial_\mu X\bigr)\bigl(g_{\mathrm{YM}}A^\mu-\partial^\mu X\bigr)\Phi_0\\
&\qquad=\frac12\sum_{a=1}^{2n-1}m_a^2\Bigl(A_\mu^a-\frac{\partial_\mu\theta^a}{g_{\mathrm{YM}}}\Bigr)\Bigl(A^{a\mu}-\frac{\partial^\mu\theta^a}{g_{\mathrm{YM}}}\Bigr),\\
&m_a^2:=2g_{\mathrm{YM}}^2\,\Phi_0^\dagger(G^a)^2\Phi_0>0 .
\end{aligned}
\right.
\tag{5.65}
```

$`a\ge2n`$ 的 $`A_\mu^a`$ 不出现在 (5.65) 中。由于 $`U(\theta)\in U(n)`$，在规范变换 (5.19)–(5.20) 中取群元 $`U(\theta)^{-1}=U(\theta)^\dagger`$，得

```math
\left.
\begin{aligned}
\Phi'&=U^\dagger\Phi=\Bigl(1+\frac h{v_{\mathrm{SM}}}\Bigr)\Phi_0,\\
A'_\mu&=U^\dagger A_\mu U-\frac i{g_{\mathrm{YM}}}\bigl(\partial_\mu U^\dagger\bigr)U=A^U_\mu,\\
F'_{\mu\nu}&=U^\dagger F_{\mu\nu}U .
\end{aligned}
\right.
\tag{5.66}
```

由规范不变性，$`\mathcal L`$ 等于在 (5.64) 中令 $`\theta^a=0`$ 并把 $`A_\mu`$ 换成 $`A'_\mu`$ 所得的结果。利用 (5.59)，

```math
\left.
\boxed{
\begin{aligned}
\mathcal L={}&\frac12\partial_\mu h\,\partial^\mu h-\frac12m_h^2h^2\\
&-\lambda_Hv_{\mathrm{SM}}\,h^3-\frac{\lambda_H}4h^4+\frac{\lambda_Hv_{\mathrm{SM}}^4}4\\
&-\frac14F'^a_{\mu\nu}F'^{a\mu\nu}\\
&+\frac12\Bigl(1+\frac h{v_{\mathrm{SM}}}\Bigr)^2\sum_{a=1}^{2n-1}m_a^2A'^a_\mu A'^{a\mu} .
\end{aligned}
}
\right.
\tag{5.67}
```

$`\theta^a`$ 不再出现。到一阶，对 $`a\le2n-1`$ 有 $`A'^a_\mu=A^a_\mu-\partial_\mu\theta^a/g_{\mathrm{YM}}`$，因此 (5.67) 中质量项的二次部分就是 (5.65)。与 (1.91) 及 (1.141) 比较：

- Higgs 场 $`h`$ 的质量为 (5.64) 的 $`m_h`$；
- 沿破缺生成元的 $`2n-1`$ 个规范场 $`A'^a_\mu`$，$`a\le2n-1`$，质量为 (5.65) 的 $`m_a`$；
- 沿未破缺生成元的 $`(n-1)^2`$ 个规范场 $`A'^a_\mu`$，$`a\ge2n`$，无质量。

当 $`n=2`$ 且 $`g_2=g_1=g_{\mathrm{YM}}`$ 时，$`m_a`$ 就是 (5.81) 的 $`m_W`$、$`m_W`$ 与 $`m_Z`$。


<br><br>

