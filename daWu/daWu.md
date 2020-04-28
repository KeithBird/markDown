# 大物

## 第一章 质点运动

### 1-1 质点运动描述

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

### 1-2 圆周运动

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

### 1-3 相对运动

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

## 第二章 牛顿定律

### 2-1 牛顿定律

#### 牛顿第一定律

不受外力的物体，运动状态保持不变

如果物体炸裂成多个部分，动量保持不变
$$
m\vec{v}=m_1\vec{v_1}+m_2\vec{v_2}
$$

##### 惯性系

参考系以**恒定速度**相对惯性系运动，惯性定律成立

##### 非惯性系

参考系相对惯性系作加速运动，地球不是严格的惯性系

#### 牛顿第二定律

动量随时间的变化率应当等于作用于物体的合力
$$
\vec{F}=\frac{d\vec{p}}{dt}=\frac{d(m\vec{v})}{dt}
$$

当 $m$ 为常量：
$$
\frac{d(m\vec{v})}{dt}=m\frac{d\vec{v}}{dt}=m\vec{a}
$$

#### 牛顿第三定律

$$
F=-F'
$$

### 2-2 物理量的单位和量纲

#### 国际单位制（SI）

|                      物理量名称                       |   物理量符号    | 物理量单位 |                     单位的名称                     | 单位的符号 |
| :---------------------------------------: | :--------: | :--------: | :-----------------------------------: | :---------------------------------------: |
|       [长度](https://baike.baidu.com/item/长度)       |      **L**      |     1m     |       [米](https://baike.baidu.com/item/米)        | m |
| [质量](https://baike.baidu.com/item/质量/2640907) | **m** | 1kg | [千克](https://baike.baidu.com/item/千克) | kg |
| [时间](https://baike.baidu.com/item/时间/25651) | **t** | 1s | [秒](https://baike.baidu.com/item/秒) | s |
| [电流](https://baike.baidu.com/item/电流) | **Ι** | 1A | [安培](https://baike.baidu.com/item/安培/5489921) | A |
| [热力学温度](https://baike.baidu.com/item/热力学温度) | **T** | 1K | [开尔文](https://baike.baidu.com/item/开尔文/5470) | K |
| [物质的量](https://baike.baidu.com/item/物质的量) | **n**（**ν**） | 1mol | [摩尔](https://baike.baidu.com/item/摩尔/22424) | mol |
| [发光强度](https://baike.baidu.com/item/发光强度) | **I**（**Iv**） | 1cd | [坎德拉](https://baike.baidu.com/item/坎德拉/5471) | cd |

### 2-3 几种常见的力

#### 万有引力

$$
\vec{F}=-G\frac{m_1m_2}{r^2}\vec{e_r}
$$

#### 弹性力

$$
\vec{F}=-kx\vec{i}
$$

### 2-4 牛顿定律的应用举例

#### 隔离体法

将所研究的物体从与之联系的其他物体中隔离出来，标明力的方向

### 2-0 例题

#### 例题-弹性力下的运动

$F_x=-kx$
$$
\begin{align}
		F_x=ma_x&=m\frac{dv_x}{dt}\\
		-kx&=m\frac{dv_x}{dt}\\
		-kxdx&=mv_xdv_x\\
		积分：-kx^2&=mv_x^2
\end{align}
$$

**Ps**: 对于力是**坐标函数**的情况，方程的两边要乘以**dx**

#### 例题-阻尼力下的运动

$f=-kv$
$$
\begin{align}
-kv&=m\frac{dv}{dt}\\
-\frac{k}{m}dt&=\frac{dv}{v}\\
-\frac{k}{m}\int_0^tdt&=\int_{v_0}^{v}\frac{dv}{v}\\
-\frac{k}{m}t&=In(v)-In(v_0)\\
v&=v_0e^{-\frac{k}{m}t}\\\\\\
v&=\frac{dx}{dt}\\
dx&=vdt\\
x&=x_0+\frac{m}{k}v_0(1-e^{-\frac{k}{m}t})
\end{align}
$$

**Ps:** 对于力是**速度函数**的情况，要把**相同的变量移动到同一边**后积分

## 第三章 动量和能量

### 质点的动量定理

$$
I=\int_{t_2}^{t_1}\vec{F}dt=\vec{p_2}-\vec{p_1}=m\vec{v_2}-m\vec{v_1}
$$

### 动量守恒定律

$$
\vec{p}=\sum_{i=1}^{n}m_i\vec{v_i}=常矢量
$$

### 动能定理

#### 功

$$
dW=\vec{F}\cdot d\vec{r}=F|d\vec{r}|cos\theta\\
\theta=位移与力的方向夹角
$$

$$
W=\int dW=\int^B_A \vec{F} \cdot d \vec{r}=\int^A_B(F_xdx+F_ydy+F_Zdz)
$$

#### 动能

$$
E_k=\int_{v_1}^{v_2}Fcos\theta|d\vec{r}|=\int m\frac{dv}{dt}ds=\int_{v_1}^{v_2}mvdv=\frac{1}{2}mv_2^2-\frac{1}{2}mv_1^2\\
E_k=\int mvdv=\int m\omega r \cdot d\omega r=mr^2\cdot\frac{1}{2}\omega^2=\frac{1}{2}J\omega^2
$$

### 保守力&势能

#### 保守力

做功只与质点**始末位置**有关的力

力的环量为0  $W=\oint_i \vec F \cdot d \vec r = 0$

万有引力、弹性力

#### 弹性势能

$$
E_p = -\int_0^x \vec F_x \cdot d \vec r = -\int_0^x (-kx) \cdot dx = \frac{1}{2}kx^2+C
$$

#### 引力势能

$$
E_p= -\int_0^r (G \frac{mm_0}{r^2}\vec{e_\tau})\cdot d \vec{\tau}=-G \int_0^r \frac{mm_0}{r^2}dr=-G\frac{mm_0}{r}+C
$$

### 碰撞

#### 完全弹性碰撞

$$
\left\{
 \begin{array}{c}
 	v_1'=\frac{m_1-m_2}{m_1+m_2}v_1+\frac{2m_2}{m_1+m_2}v_2\\
	v_2'=\frac{m_2-m_1}{m_1+m_2}v_2+\frac{2m_1}{m_1+m_2}v_1
 \end{array}
\right.
$$

#### 完全非弹性碰撞

$$
v = \frac{m_1v_1+m_2v_2}{m_1+m_2}
$$

## 第四章 刚体的转动

### 角动量

$$
\vec L = \vec r \times \vec p=m\vec{v}\vec{r}=m\vec{\omega} \vec{r}^2=J\vec{\omega}
$$

### 力矩

力的方向逆时针为正

$$
\vec M = \vec r \times \vec F = \frac{d\vec L}{dt}
$$
$$
\vec{M}=\sum \limits_{i=1}^n(\vec{F}_i\vec{R}_i)\\
$$

### 转动惯量

$$
J=mr^2~(末端物体)
$$

$$
\vec M=\frac{\vec L}{t}=J\vec\alpha
$$

| 物体形状 | 转轴位置           | 转动惯量                    |
|:--------:|:------------------:|:---------------------------:|
| 细杆     | 通过一端垂直于杆   | $\frac{1}{3}ml^2$           |
| 细杆     | 通过中心垂直于杆   | $\frac{1}{12}ml^2$          |
| 薄圆环   | 通过环心垂直于环面 | $mR^2$                      |
| 薄圆环   | 通过环心平行于环面 | $\frac{1}{2}mR^2$           |
| 圆环     | 通过环心垂直于环面 | $\frac{1}{2}m(R_1^2+R_2^2)$ |
| 圆盘     | 通过盘心垂直于盘面 | $\frac{1}{2}mR^2$           |
| 薄球壳   | 直径               | $\frac{2}{3}mR^2$           |
| 球体     | 直径               | $\frac{2}{5}mR^2$           |

### 角动量守恒

系统所受力都**与转轴平行**或**经过转动中心**

$$
\vec L = m\vec{r}_1\vec{v}_1(质点)+J_1\vec{\omega}_1(转动体)
= m\vec{r}_2\vec{v}_2+J_2\vec{\omega}_2
$$

### 力矩对刚体做的功
$$
A = \int_{\theta_1}^{\theta_2} Md\theta
$$

### 转动动能
$$
E_k = \frac{1}{2}J\omega^2
$$

## 第五章 机械振动与机械波

### 震动

#### 文字描述求初相

1. 以振幅 $A$为半径做圆

2. 标出圆的方向 $\omega$，统一为逆时针

3. 在图像中表示初始位置

4. 根据**运动方向**和圆的方向确定待求点

5. 连接圆心，求 $\varphi$

#### 图像描述求初相

1. 以振幅 $A$ 为半径做圆

2. 标出圆的方向 $\omega$，统一为逆时针

3. 在圆中表示初始位置

4. 根据**运动方向**和圆的方向确定待求点

5. 连接圆心，求 $\varphi$

#### 求简谐震动方程

将初相 $\varphi$ 和振幅 $A$ 代入方程求出 $\omega$

$$
\omega = \frac{2\pi}{T}=2\pi f
$$

#### 求运动时间

1. 作图

2. 在圆中表示始末位置

3. 根据**运动方向**和圆的方向确定待求点

4. $t = \theta / \omega$

#### 根据弹簧参数求震动方程

1. 求出 $A$ 和 $\omega$
$$
\omega  = \sqrt{\frac{k}{m}}~~~~~A=\sqrt{x_0^2+\frac{v_0^2}{\omega^2}}
$$

2. 代入方程求出可能的 $\varphi$，作图表示出两个 $\varphi$

3. 根据**运动方向**和圆的方向确定待求点

#### 简谐运动的能量

##### 机械能
$$
E = \frac{1}{2}kA^2
$$

##### 动能
$$
E_k = \frac{1}{2}kA^2sin^2(\omega t + \varphi)
$$

##### 势能
$$
E_p = \frac{1}{2}kA^2cos^2(\omega t + \varphi)
$$

##### 平均动能和平均势能

$$
\overline{E_k} = \overline{E_p} = \frac{1}{4}kA^2
$$

#### 震动的合成 $(\omega_1 = \omega_2)$
$$
A = \sqrt{{A_1}^2 + {A_2}^2 + 2A_1A_2cos(\varphi_2 - \varphi_1)}
$$
$$
\varphi = arctan \frac{A_1sin\varphi_1+A_2sin\varphi_2}
{A_1cos\varphi_1+A_2cos\varphi_2}
$$

#### 震动的拍频 $(\omega_1 \neq \omega_2)$
$$
\Delta f = \frac{\omega_1}{2 \pi} - \frac{\omega_2}{2 \pi}
$$

#### 单摆频率
$$
\omega = \sqrt{\frac{g}{l}}~~~~~T=\frac{2\pi}{\omega}~~~~~f=\frac{\omega}{2\pi}
$$

### 波动













