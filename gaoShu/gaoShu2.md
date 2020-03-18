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

$(m,n,p)$ 为方向数
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

$U(P_0)=U(P_0,\delta)=\{P~|~0<|PP_0|<\delta\}$

##### 边界点

如果点 $P$ 的任一邻域内都既含有属于$E$ 的点，又含有不属于$E$ 的点，那么称 $P$ 为$E$ 的边界点。

##### 聚点

如果对于任意给定的 $\delta>0$ ，点 $P$ 的去心邻域 $\mathring{U}(P,\delta)$ 内总有$E$ 中的点，那么称 $P$ 是$E$ 的聚点。 (点集$E$ 和边界 $\partial E$ 上的所有点)

