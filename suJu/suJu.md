# 数据结构

[DATA STRUCTURE](https://github.com/xiufengcheng/DATASTRUCTURE)

## 第一章 概论

### 数据的逻辑结构

#### 数据元素

数据元素是数据的基本单位

#### 数据结构的3个内容

1. **逻辑结构：** 数据元素之间的逻辑关系
2. **存储结构：** 数据元素及其关系在计算机存储器内的表示
3. **数据运算：** 对数据施加的操作

#### 逻辑结构分类

1. **集合：** 最简单的数据结构，数据之间只有相似性。
2. **线性结构：**"一对一"的关系。
3. **树形结构：**"一对多"的关系。
4. **图形结构：**"多对多"的关系。

### 数据的存储结构

#### 顺序存储结构

借助元素在存储器中的**对应位置**表示数据元素之间的逻辑关系。

- 可实现对各数据元素的随机访问
- 不利于修改

#### 链式存储结构

借助指示元素存储位置的**指针**表示元素之间的逻辑关系。

- 利于修改
- 不能随机访问

#### 索引存储结构

在原有的存储结构的基础上，附加建立一个索引表，索引表中的每一项都由**关键字和地址**组成

索引表反映了按某一个关键字递增或递减排列的逻辑次序

采取索引存储的主要作用是为了提高数据的**检索**速度

#### 散列存储结构

通过构造散列函数来确定数据存储地址或查找地址

### 算法和算法分析

#### 算法的特性

1. **有穷性：** 没有死循环
2. **确定性：** 无歧义
3. **可行性：** 操作可实现
4. **输入：** >=0
5. **输出：** >=1

#### 算法的效率评价

$T(n)=n+n^2=O(n^2)$

## 第二章 List(线性表)

### 线性表的基本概念

#### 线性表的定义

线性表是具有相同数据类型的n(n≥0)个数据元素的有限序列


#### 线性表的基本操作

初始化、求长度、按地址搜索、按值搜索、插入、删除、显示

### 线性表的顺序存储

#### 顺序表的存储特点

- 逻辑结构和物理结构是一致的
- 任意数据元素都可以随机存取

#### 顺序表插入 ⚠️

1. 检查顺序表是否塞满,防溢出
2. 插入位置应在`a[0] + l`之内
3. 移动必须从最后一个节点开始

### 线性表的链式存储

#### 头节点和head

头节点不属于数据元素

动态申请一个结点空间，链表第一个结点的地址放到了指针变量head中

`head = (LinkList *) malloc (sizeof(LinkList)) ;`

#### 循环链表

最后一个结点的指针域为head

## 第三章 Stack(栈)

它的插入、 删除等操作只能在表的一端进行。固定操作的一端叫**栈顶(top)**，而另一端称为**栈底(bottom)**。

### 顺序栈

表头`a[0]`的一端作为栈底，指针 `top=length-1`

#### 上溢与下溢

##### 上溢(overflow)

栈满的情况下还入栈。对顺序栈进行插入元素之前，需要判断是否“栈满”，否则上溢

##### 下溢(underflow)

栈空的情况下还出栈。对顺序栈进行删除元素之前，需要判断是否“栈空”，否则下溢

#### 多栈共享空间

即两个栈栈底位置为两端，两个栈顶在中间不断变化，由两边往中间延伸。

### 链栈

链栈的**栈顶指针**就是单链表的**头指针**

唯一的约束条件是头指针的操作在头部执行

链栈一般不需要判定栈满，只需要判定栈是否为空。

栈空判定条件是: `S = NULL`

#### 进栈操作

```c++
bool Push_L(LinkStack &S, ElemType e) {
      LinkStack p;
      if((p=(LNode *)malloc(sizeof(LNode)))==NULL) return false;  // 存储分配失败
      p->data=e;  
      p->next=S;                      // 插入新的栈顶元素
      S=p;                            // 修改栈顶指针
      return true;
     }// Push_L
```

#### 出栈操作

```c++
bool Pop_L( LinkStack &S, ElemType &e) {
    LinkStack p;
    if(S) {                    // 栈非空
        p=S;
        S=S->next;             // 修改栈顶指针
	e=p->data;             // 元素e返回其值
	free(p);               // 释放结点空间
	return true; 
    }
   else return false;          // 栈空，出栈失败
 }// Pop_L
```

#### 中缀表达式 > 后缀表达式

1. 读入操作数，直接送入输出符号栈
2. 读入运算符
    - 后进运算符优先级高于先进的，则继续进栈
    - 后进运算符优先级不高于先进的，则将运算符号栈内高于或等于后进运算符级
别的运算符依次弹出后进栈
3. 读入括号
	- 遇到开括号 (，进运算符号栈
	- 遇到闭括号 )， 则把最靠近的开括号 ( 以及其后进栈的运算符依次弹出到符号栈
4. 遇到结束符 “#”，则把运算符号栈内的所有运算符号依次弹出并压入输出符号栈
5. 若输入为+、 –单目运算符，改为 0 与运算对象在前，运算符在后  

## 第四章 Queue(队列)

### 定义

- 允许插入的一端叫**队尾(rear)**
- 允许删除的一端叫**队首(front)**

### 顺序队列

#### 假溢出

队首前还有空间的入队溢出

##### 判断条件

`rear >= maxsize && front > 0`

##### 解决方法

1. 修改出队算法：使每次出队列后都把队列中剩余的元素向front方向移动一个位置。O(n)
2. 修改进队算法：当假溢出时，把队列中的所有元素向front方向移动一个位置。O(n)
3. 顺序循环队列

#### 顺序循环队列

##### 顺序循环队列定义

- 把顺序队列改造成一个头尾相连的循环表
- 入队时，把元素插到rear指示位置，然后rear++
- 出队时，把front指示位置元素删除，然后front++

##### 判空和判满

1.队尾留一个单元

判满：`(rear+1) mod maxsize = front`

判空：`rear == front`

2.标志位

判满：`(rear==front) && (tag==1)`

判空：`(rear==front) && (tag==0)`

3.计数器

判满条件：`(rear==front) && count>0`

判空条件：`count == 0`

##### 元素个数

`N = (rear - front + maxsize) % maxsize`

##### 入队操作

```C++
int inQueue (seqQueue *Q, dataType x){

    if((Q->rear+1) % MAXSIZE == Q->front){
	return 0;
    }
    
    else if((Q->rear+1) % MAXSIZE != Q->front){
	Q->rear = (Q->rear+1) % MAXSIZE;
	Q->data[Q->rear] = x;
	reutn 1;
    }
}
```

### 链队

##### 出链队操作

```c++
bool deQueue_L(kinkQueue &Q, ElemType &e){
    QueuePtr p;
    if(Q.front==NULL)
        return false;
    
    p=Q.front;				// 暂存队首指针以便回收队首结点
    e=p->data;				// e返回队首元素的值
    Q.front = p->next;		
    if(Q.front==NULL)		// 若删除后队列为空，则使队尾指针为空
        Q.rear = NULL;
    
    free(p);
    return true;
}
```

##### 入队操作

```c++
bool enQueue_L(likQueue &Q, ElemType e){
    queuePtr s;
    if((s=(LNode *)malloc(sizeof(LNode)))==NUll)
        return false;					// 存储分配失败
    
    s->data = e;
    s->next = NULL;
    
    if(Q.rear==NULL){
        Q.front = Q.rear = s;			// 若链队为空,则新结点既是队首结点又是队尾结点
    }else if(Q.rear!=NULL){
        Q.rear = Q.rear->next = s; 		// 若链队非空，则新结点被链接到队尾并修改队尾指针
    }
    
}
```

## 第五章 String(串)

### 串

#### 定义

##### 子串

串中任意个连续的字符组成的子序列称为该串的子串

一个串也可以看成是自身的子串

##### 子串个数公式

`n(n+1)/2+1`

##### 真子串个数公式

`n(n+1)/2`

#### 串的比较

从左开始，第一个差异字符的大小关系

##### ASCII码

由**8bit**组成一个字符，共可形成2^8^=256个字符（仅英语）

##### Unicode码

由**16bit**组成一个字符，共可表示2^16^=65536个字符（全世界的字符）

#### 串和线性表的不同点

- 串的数据元素是字符，即每个数据元素都是**一个**字符
- 线性表的主要操作对象是某个**数据元素**
- 串的操作主要操作对象是**整体或某一部分子串**

### 顺序串

#### 静态存储分配的顺序串

用**定长**字符数组存储串值

由于串值空间的大小已经确定，所以对串的插入、连接等不利

```C++
typedef struct{
        char str[MaxStrSize];   //顺序串的最大容量
        int length;             //顺序串的当前长度
}SSqString;                		//静态顺序串类型
```

#### 动态存储分配的顺序串

串值空间的大小是在**程序执行时动态分配**而得

在串处理的应用程序中也常被选用

**Ps：**动态分配的顺序串完全可用动态存储分配的顺序表SqList来表示

```C++
typedef struct {
    char  *str;                  // 先存放非空串的首地址，不分配内存
    int length;                  // 存放串的当前长度
}DSqString;                      //待到程序执行时，再根据插入、删除等操作动态增补空间。
```

#### 串比较

```C++
int StrCompare_Sq(DSqString S,DSqString T){  
    
	int i=0;
	while(i<S.length&&i<T.length){           // 串S和串T对应字符进行比较
		if(S.str[i]>T.str[i]) return 1;
		else if(S.str[i]<T.str[i]) return -1;
		i++;
	}
    
	if(i<S.length) return 1;
	else if(i<T.length) return -1;
    
	return 0;
}// StrCompare_Sq
```

#### 取子串

在顺序串S中从第POS个位置开始，取长度为len的子串sub。

```C++
bool SubString_Sq(DSqString S,DSqString &Sub,int pos,int len){   
	int i;
	if(pos<0||pos>S.length-1||len<0||len>S.length-pos)  
		return false;                          // 取子串的位置或子串的长度不合理
	
    if(Sub.str)   free(Sub.str);               // 释放Sub原有空间
	
    if(len!=0) { Sub.str=NULL; Sub.length=0; }   // 置Sub为空子串
	else {
		if(!(Sub.str=(char *)malloc(len*sizeof(char)))) return false;
		for(i=0;i<len;i++)                     // 将串S中的len个字符复制到Sub中
			Sub.str[i]=S.str[pos+i];
		Sub.length=len;                		   // 子串Sub的串长为len
	}
	return true; 
}// SubString_Sq
```

### 链式串

#### 定义

一个节点可以存放多个字符

**单链结构：**结点大小为1的链式串

**块链结构：**结点大小大于1的链式串

在块链结构中最后一个结点通常填不满，则用#号把串值填满。

#### 块链数据结构

```C++
typedef struct Chunk{      //可由用户定义的节点大小
      char str[Number];    //一个节点存放Number个字符
      struct Chunk  *next;
}Chunk;                    //定义结点类型

typedef struct{
   Chunk  *head, *tail;    //串的头尾指针
   int length;             //串的当前长度
}
```

### KMP算法

[KMP](https://mp.weixin.qq.com/s/kCjRuY6ygYJWWX5HPVLa5A)

## 第六章 Array(数组)