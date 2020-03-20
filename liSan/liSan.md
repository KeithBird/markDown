# 离散数学

---

## 第一部分 数理逻辑

### 第一章 命题逻辑的基本概念

#### 1.1 命题与连接词

##### 优先级

$（），\lnot，\wedge，\vee，\to，\leftrightarrow$

##### p $\to$ q

q为p的必要条件，1 $\to$ 0 $\Leftrightarrow$ 0

#### 命题公式及其赋值

##### 命题层次

1. A = $\lnot$ B，$n+1$
2. A = B $\wedge$ C，$\vee,\to,\gets,\leftrightarrow$ ， $max(i,j)+1$
3. p为0层

##### 公式类型

1. 重言式：真值表全为1
2. 矛盾式：真值表全为0
3. 可满足式：真值表至少一项为1

### 第二章 命题逻辑等值演算

#### 2.1 等值式

##### 等值试模式

|      定律      |                                    |                                   |
| :------------: | :--------------------------------: | :-------------------------------: |
|   蕴涵等值式   |             $A \to B$              |         $\lnot A \vee B$          |
|     分配律     |       $A \vee (B \wedge C)$        |  $(A \vee B) \wedge (A \vee C)$   |
|     分配律     |       $A \wedge (B \vee C)$        | $(A \wedge B) \vee (A \wedge C)$  |
|    德摩根律    |         $\lnot (A \vee B)$         |     $\lnot A \wedge \lnot B$      |
|    德摩根律    |         $\lnot (A \vee B)$         |     $\lnot A \wedge \lnot B$      |
|     吸收律     |       $A \vee (A \wedge B)$        |                $A$                |
|     吸收律     |       $A \wedge (A \vee B)$        |                $A$                |
|     结合律     |        $(A \vee B) \vee C$         |        $A \vee (B \vee C)$        |
|     结合律     |      $(A \wedge B) \wedge C$       |      $A \wedge (B \wedge C)$      |
|   双重否定律   |                $A$                 |             $\lnot A$             |
|     幂等律     |                $A$                 |            $A \vee A$             |
|     幂等律     |                $A$                 |           $A \wedge A$            |
|     交换律     |             $A \vee B$             |            $B \vee A$             |
|     交换律     |            $A \wedge B$            |           $B \wedge A$            |
|      零律      |             $A \vee 1$             |                $1$                |
|      零律      |            $A \wedge 0$            |                $0$                |
|     同一律     |             $A \vee 0$             |                $A$                |
|     同一律     |            $A \wedge 1$            |                $A$                |
|     排中律     |          $A \vee \lnot A$          |                $1$                |
|     矛盾律     |         $A \wedge \lnot A$         |                $0$                |
|    假言易位    |             $A \to B$              |       $\lnot A \to \lnot B$       |
|     归谬论     | $(A \to B) \wedge (A \to \lnot B)$ |             $\lnot A$             |
|   等价等值式   |       $A \leftrightarrow B$        |    $(A \to B)\wedge(B \to A)$     |
| 等价否定等值试 |       $A \leftrightarrow B$        | $\lnot A \leftrightarrow \lnot B$ |

#### 2.2 析取范式与合取范式

##### 文字

命题变项及其否定

##### 简单析(合)取式

由有限个文字构成的析取式

##### 析(合)取范式

有限个简单析取式构成的析取式

##### 求范式

1. 消去连结词 $$\to ~ \leftrightarrow$$
2. 用德摩根内移否定符
3. 使用分配律

##### 极小(大)项

每个极小项有且仅有一个成真赋值

![极小项](liSan.assets/极小项.png)

##### 主析取范式

所有简单合取式都是极小值的析取范式








