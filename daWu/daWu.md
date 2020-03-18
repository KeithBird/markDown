# 大物

---

## 第一章  质点运动

### 1-1  质点运动描述

#### 位置矢量

$$
\vec{r} = x\vec{i}+y\vec{j}+z\vec{k}
$$

#### 位矢余弦

$$
cos\alpha=\frac{x}{|~\vec{r}~|}~~~~~cos\beta=\frac{y}{|~\vec{r}~|}~~~~~cos\gamma=\frac{z}{|~\vec{r}~|}
$$

#### 速度方程

$$
\vec{r}~=~\vec{r}(t)~=~x(t)\vec{i}+y(t)\vec{j}+z(t)\vec{k}
$$

#### 分速度

$$
\vec{v}~~=~~\vec{v_x}+\vec{v_y}+\vec{v_z}~~=~~v_x\vec{i}+v_y\vec{j}+v_z\vec{k}
$$

### 1-2  圆周运动

#### 切向单位矢量

$$
\vec{v}=v\vec{e_\tau}=\frac{ds}{dt}\vec{e_\tau}=|\vec{v}|\vec{e_\tau}
$$

#### 切向加速度

描述由速度大小变化快慢，方向为$\vec{e_t}$，与速度$\vec{v}$方向相同
$$
\vec{a_\tau}=\frac{dv}{dt}\vec{e_\tau}~~~~~~~~~~a_\tau=\frac{dv}{dt}~~~~~~~~~~
$$

#### 角加速度

$$
\alpha=\frac{d\omega}{dt}=\frac{d^2\theta}{dt^2}~~~~~~~~~~\vec{\alpha_\tau}=r\alpha\vec{e_\tau}
$$

#### 法向单位矢量

$\Delta\vec{e_t}$ 与 $\vec{e_t}$ 的方向垂直，所以法向单位矢量指向圆心
$$
\lim \limits_{\Delta t\rightarrow0}\frac{\Delta \vec{e_\tau}}{\Delta t} = \frac{d\vec{e_\tau}}{dt}=\frac{d\theta}{dt}\vec{e_n}
$$

#### 法向加速度

反映速度方向变化快慢
$$
\vec{a_n}=v\frac{d\theta}{dt}\vec{e_n}=r\omega^2\vec{e_n}=\frac{v^2}{r}\vec{e_n}
$$

#### 加速度

$$
\vec{\alpha}=\vec{a_\tau}+\vec{a_n}=\frac{dv}{dt}\vec{e_\tau}+\frac{v^2}{r}\vec{e_n}=r\alpha\vec{e_\tau}+r\omega^2\vec{e_n}
$$

#### 变速圆周运动

$$
\alpha=\sqrt{a_n^2+a_\tau^2}~~~~~~~~~~tan\varphi=\frac{a_n}{a_\tau}
$$

#### 自然坐标系

以动点为原点，以切向单位矢量 $\vec{e_t}$ 和法向单位矢量 $\vec{e_n}$ 为坐标轴建立的坐标系。

#### 匀加速运动

$\vec{\alpha}$ 为常矢量
$$
\vec{\tau}=\vec{\tau_0}+\vec{v_0}t+\frac{1}{2}
\vec{\alpha}t^2
$$

#### 匀变速圆周运动

$$
\left\{
 \begin{array}{c}
  \omega=\omega_0+\alpha_\tau\\
  \theta=\theta_0+\omega_0t+\frac{1}{2}\alpha t^2\\
  \omega^2=\omega_0^2+2\alpha(\theta-\theta_0)
 \end{array}
\right.
$$

### 1-3  相对运动

质点相对基本参考系的绝对速度 $\vec{v}$ ，等于运动参考系相对绝对参考系的牵连速度 $\vec{u}$ 与质点相对速度参考系的相对速度 $\vec{v'}$ 之和。

### 1-0 错题

1. 质点沿$X$轴正向运动，加速度 $\vec{a}=k\vec{v}$，$k$ 为常数。设从原点出发时速度为 $\vec{v_0}$，求运动方程 $\vec{x}=x(t)$。

$$
\begin{align}
		  &\frac{d\vec{v}}{dt}=-k\vec{v}\\
     	&=>-\frac{d\vec{v}}{k\vec{v}}=dt\\
     	两边积分：&=>\frac{1}{k}ln(\frac{\vec{v}}{\vec{v_0}})=t\\
     	&=>\vec{v}=\vec{v_0}e^{-kt}\\
     	两边积分：&=>\vec{x}=-\frac{\vec{v_0}}{k}e^{-kt}+C\\
     	带入~t=0~,~x=0~解得:~&C=\frac{\vec{v_0}}{k}\\
     	&\vec{x}=\frac{\vec{v_0}}{k}(1-e^{-kt})
\end{align}
$$



2. 质点作曲线运动的方程为 $x=2t,~y=4-t^2(SI)$ ，求 $t$ 时刻质点的 $a_\tau$ 和 $a_\tau$ 
   $$
   \begin{align}
   		\vec{v}&=2\vec{e_x}-2t\vec{e_y}\\
   		\vec{a}&=-2\vec{e_y}\\\\
   		\vec{e_\tau}&=\frac{\vec{v}}{|\vec{v}|}\\
   		&=\frac{2\vec{e_x}-2t\vec{e_y}}{\sqrt{2^2+(2t)^2}}\\
   		&=\frac{\vec{e_x}-t\vec{e_y}}{\sqrt{1+t^2}}\\\\
   		\vec{a_\tau}&=\frac{dv}{dt}\vec{e_\tau}\\
   		&=(-2\vec{e_y})\frac{(\vec{e_x}-t\vec{e_y})}{1+t^2}\\
   		&=\frac{2t}{\sqrt{1+t^2}}\\\\
   		\vec{a_n}&=\sqrt{|\vec{a}|^2-(\vec{a_\tau})^2}\\
   		&=\frac{2}{\sqrt{1+t^2}}
   		
   \end{align}
   $$
   

