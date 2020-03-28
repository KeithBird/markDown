# 高数2

---

## 第八章  向量代数与空间解析几何

### 8.1 向量及其线性运行

#### 向量的概念

##### 共面

设有k个向量，当把它们的起点放在同一点时，k个终点和公共起点在同一平面。

#### 向量的线性运算

向量的加法及数乘向量统称为向量的**线性运算**

#### 方向余弦

$$
\vec{e_\tau}=(cos\alpha,cos\beta,cos\gamma)=\frac{\vec{\tau}}{|\vec{\tau}|}
$$

### 8.2 数量积 & 向量积

向量积 $|\vec{c}|=|\vec{a}||\vec{b}|sin\theta$ $~~~~~\vec{c}$ 的方向由右手规则求得 

1. $|\vec{a}\times\vec{a}|=|\vec{a}|^2sin0=0$
2. $\vec{a}\times\vec{b}=\vec{0}~\Leftrightarrow~\vec{a}~//~\vec{b}$

### 8.3 平面及其方程

#### 点法式

$$
n\cdot\vec{MM_0}=A(x-x_0)+B(y-y_0)+C(z-z_0)=0
$$

#### 一般式

$$
Ax+By+Cz+D=0
$$

#### 截距式

$$
\frac{x}{a}+\frac{y}{b}+\frac{z}{c}=1
$$

#### 平面束

### 8.4 空间直线及其方程

#### 一般式

$$
\left\{
	\begin{array}{c}
		A_1x+B_1y+C_1z+D_1=0\\
		A_2x+B_2y+C_2z+D_2=0
	\end{array}
\right.
$$

#### 点向式

$$
\vec{M_0M}~//~(m,n,p)\Rightarrow\frac{x-x_0}{m}=\frac{y-y_0}{n}=\frac{z-z_0}{p}
$$

#### 参数方程

$(m,n,p)$ 为方向数
$$
\left\{
	\begin{array}{c}
		x=x_0+mt\\
		y=y_0+nt\\
		z=z_0+pt
	\end{array}
\right.
$$

### 8.5 曲面及其方程

#### 曲面研究的基本问题 ？

#### 旋转曲面 ？

#### 柱面 ？

#### 二次曲面 ？

### 8.6 空间曲线及其方程

#### 空间曲线的一般方程

两曲面的交线:
$$
\left\{
	\begin{array}{c}
		F(x,y,z)=0\\
		G(x,y,z)=0
	\end{array}
\right.
$$

####  空间曲线的参数方程

$$
\left\{
	\begin{array}{c}
		x=x(t)\\
		y=y(t)\\
		z=z(t)
	\end{array}
\right.
$$

#### 空间曲面在坐标面上的投影

$$
\left\{
	\begin{array}{c}
		H(x,y)=0\\
		z=0\\
	\end{array}
\right.
$$

## 第九章 多元函数微分法及其应用

### 9.1 多元函数的基本概念

#### 平面点集

##### 领域

$$
U(P_0)=U(P_0,\delta)={P (|)0<|PP_0|<\delta}
$$

##### 边界点

如果点 $P$ 的任一邻域内都既含有属于$E$ 的点，又含有不属于$E$ 的点，那么称 $P$ 为$E$ 的边界点。

##### 聚点

如果对于任意给定的 $\delta>0$ ，点 $P$ 的去心邻域 $\mathring{U}(P,\delta)$ 内总有$E$ 中的点，那么称 $P$ 是$E$ 的聚点。 (点集$E$ 和边界 $\partial E$ 上的所有点)

##### 开集

点集 $E$ 的点都是 $E$ 的内点

##### 闭集

点集 $E$ 的边界 $\partial E \subset E$

##### 联通集

点集 $E$ 内任何两点可以通过属于 $E$ 的折线联结

##### 区域

联通的**开集**

##### 闭区域

开区域连同它的边界

#### 多元函数的概念

##### 自然定义域

使等式有意义的 $x$ 的集合

##### 二元函数的图形

$$
z = f(x,y) \Leftrightarrow M(x,y,x)
$$

二元函数的图形是空间曲面

#### 多元函数的极限

$$
\lim \limits_{(x,y) \to (x_0,y_o)}f(x,y)=A
$$

#### 多元函数的连续性

如果$ \lim \limits_{(x,y) \to (x_0,y_0)} = f(x_0,y_0)$ ，则$f(x,y)$ 在点 $P_0(x_0,y_0)$连续

##### 介值定理

在有界闭区域 $D$ 上的多元连续性函数必取得介于最大值和最小值之间的**任何值**

### 9.2 偏导数

#### 偏导数的定义及其计算方法

##### 偏导数

$$
\frac{\partial f}{\partial x}\bigg|_{(x_0,y_0)}= f'_x(x_0, y_0)=\lim \limits_{\Delta x \to 0} \frac{f(x_0 + \Delta x, y_0) - f(x_0, y_0)}{\Delta x}
$$

##### 偏导函数

对于每一点 $(x,y)$ 处的偏导数都存在

##### 求法

求 $\frac{\partial f}{\partial x}$ ，**将 $y$ 当作常数**，用一元求导法，对 $x$ 求导。  

#### 高阶偏导数

高阶混合偏导数在偏导数连续的条件下与求导次序无关。

### 9.3 全微分

#### 全微分的定义

##### 偏增量

$$
f(x,y+\Delta y)-f(x,y)
$$

##### 偏微分

$$
f'_y(x,y) \Delta y
$$

##### 全增量

$$
\Delta z = f(x+\Delta x,y+\Delta y)-f(x,y)
$$

##### 全微分

$$
dz=A \Delta x + B \Delta y\\
A = \frac{\partial z}{\partial x}~~~B = \frac{\partial z}{\partial y}
$$

##### 证明可微 ⚠️

$\Delta z - dz = o(p) $ ，$p=\sqrt{(\Delta x)^2+(\Delta y)^2}$ ， $o(p)$ 为高阶无穷小

即证：
$$
\lim \limits_{\Delta x \to 0\Delta y \to 0} \frac{\Delta z-(\frac{\partial z}{\partial x} \Delta x + \frac{\partial z}{\partial y} \Delta y)}{p}=0
$$
`偏导存在 + 连续 -> 全微分存在`

### 9.4 多元复合函数的求导法则

#### 一元函数与多元函数复合

$z=f(\varphi(t),~\psi(t))$
$$
\frac{dz}{dt}=\frac{\partial z}{\partial u}\cdot \frac{\partial u}{\partial t}+\frac{\partial z}{\partial v}\cdot \frac{\partial v}{\partial t}
$$

#### 多元函数与多元函数复合

$z=f(\varphi(x,y),~\psi(x,y))$
$$
\frac{\partial z}{\partial x}=\frac{\partial z}{\partial u}\cdot \frac{\partial u}{\partial x}+\frac{\partial z}{\partial v}\cdot \frac{\partial v}{\partial x}
$$

$$
\frac{\partial z}{\partial y}=\frac{\partial z}{\partial u}\cdot \frac{\partial u}{\partial y}+\frac{\partial z}{\partial v}\cdot \frac{\partial v}{\partial y}
$$

### 9.5 隐函数的求导法则

#### 一个方程的情形

#### 方程组的情形

### 9.6 多元函数微分学的几何应用

#### 一元向量值函数及其导数

#### 空间曲线的切线与法平面

#### 曲面的切平面与法线

### 9.7 方向导数与梯度

#### 方向导数

#### 梯度

### 9.8 多元函数的极值及其求法

#### 多元函数的极值及最大值和最小值

#### 条件极值 拉格朗日乘数法





