# LaTeX

---

[Typora中利用LaTeX 插入数学公式](https://blog.csdn.net/happyday_d/article/details/83715440)

### 希腊字母表

![希腊字母表](LaTeX.assets/希腊字母表.jpeg) 

### 符号

[LaTeX 各种命令，符号](https://blog.csdn.net/GarfieldEr007/article/details/51646604?depth_1-utm_source=distribute.pc_relevant.none-task&utm_source=distribute.pc_relevant.none-task)

|  |      | | |
| :-------: | :---------: | :-------: | :-------: |
| $x_i$ | `x_i` |  |  |
|   $x^2$   |   `x^2`   |  |  |
| $\sqrt[123]{ x^2+y^2 }$ | `\sqrt[123]{ x^2+y^2 }` | $\perp$ | `perp` |
| $\dots$ |`\dots`| $\vee$ | `$\vee$` |
| $\cdots$ |`\cdots`|     $\wedge$      | `$wedge$` |
| $\sum \limits_{i=1}^n$​ |`\sum \limits_{i=1}^n`| $\leftrightarrow$ | `$\leftrightarrow$` |
| $\int_1^n$ |`$\int_1^n$`| $\lnot$ | `$\lnot$` |
| $\lim \limits_{x \to \infty}$ |`\lim \limits_{x \to \infty}`| $\gets$ | `$\gets$` |
| $\frac{3}{8}$ |`$frac{3}{8}$`| $\to$ | `$\to$` |
| $\mathring{U}$ |`$\mathring{U}$`| $\times$ | `$\times$` |
| $\partial$ |`$\partial$`| $\cdot$ | `$\cdot$` |
| $\bigg|$ |`$\bigg|$`| $\div $ | `$\div$` |
| $\approx$ |`$\approx$`| $\mid$ | `$\mid$` |
| $\oint$ |`$\oint$`| $\in$ | `$\in$` |
| $\infty$ |`$\infty$`| $\notin$ | `$\notin$` |
| $\pm$ |`$\pm$`| $\subset$ | `$\subset$` |
| $\overline{x}$ |`$\overline{x}$`| $\subsetneqq$ | `$\ubsetneqq$` |
| $\underline{x}$ |`$\underline{x}$`| $\supset$ | `$\supset$` |
| $\hat{A}$ |`$\hat{y}$`| $\cap$ | `$\cap$` |
| $\widehat{A}$ |`$\widehat{A}$`| $\cup$ | `$\cup$` |
| $\tilde{A}$ |`$\tilde{A}$`| $\mathbb{R}$ | `$\mathbb{R}$` |
| $\widetilde{A}$ |`$\widetilde{A}$`| $\emptyset$ | `$\emptyset$` |
| $\dot{U}$ |`\dot{U}`| $\ang$ | `$\ang$` |
| $\ddot{U}$ |`\ddot{U}`| $\forall$ | `\forall` |
| $\bar{x}$ |`\bar{x}`| $\exists$ | `\exists` |

### 矩阵与行列式

$$
\begin{matrix}
	1 & x & x^2\\
	1 & y & y^2\\
	1 & z & z^2\\
	\end{matrix}
$$


$$
X=\left|
	\begin{matrix}
		x_{11} & x_{12} & \cdots & x_{1d}\\
		x_{21} & x_{22} & \cdots & x_{2d}\\
		\vdots & \vdots & \ddots & \vdots \\
		x_{11} & x_{12} & \cdots & x_{1d}\\
	\end{matrix}
\right|
$$

### 箭头

![](LaTeX.assets/箭头.JPG)



### 分段函数

$$
f(n)=
	\begin{cases}
		n/2, & \text{$x$ = 7}\\
		3n+1,& \text{$x$ != 7}
	\end{cases}
$$



### 方程组
$$
P =  
\left\{
	\begin{array}{c}
		a_1x+b_1y+c_1z=d_1\\
		a_2x+b_2y+c_2z=d_2\\
		a_3x+b_3y+c_3z=d_3
	\end{array}
\right.
$$

### 推导过程

$$
\begin{align}
		\frac{\partial J(\theta)}{\partial\theta_j}
		& = -\frac1m\sum_{i=0}^m(y^i - h_\theta(x^i)) \frac{\partial}{\partial\theta_j}(y^i-h_\theta(x^i))\\
		& = -\frac1m\sum_{i=0}^m(y^i-h_\theta(x^i)) \frac{\partial}{\partial\theta_j}(\sum_{j=0}^n\theta_j x^i_j-y^i)\\
		& = -\frac1m\sum_{i=0}^m(y^i -h_\theta(x^i)) x^i_j
\end{align}
$$


### 字符下标

$$
\max \limits_{a<x<b}\{f(x)\}
$$





 