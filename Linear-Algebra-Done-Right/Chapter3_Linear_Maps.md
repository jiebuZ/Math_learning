# Linear Algebra Done Right

## Chapter 3: Linear Maps

### 线性映射

一个从 $V$ 到 $W$ 的线性映射是一个函数 $T:V\rightarrow W$ ，其具有一下性质：

$(1)T(u+v)=Tu+Tv~~\forall u,v\in V$ ；

$(2)T(\lambda v)=\lambda(Yv)~~\forall\lambda\in F,v\in V$ 。

记从 $V$ 到 $W$ 的所有线性映射构成的集合为 $L(V,W)$ ，且简记 $L(V,V)$ 为 $L(V)$ 。

定义在 $L(V,W)$ 上的加法与数量乘法，设 $S,T\in L(V,W),\lambda\in F,\forall v\in V$ ，则定义：

$$(S+T)(v)=Sv+Tv~~~~(\lambda T)(v)=\lambda(Tv)$$

不难证明， $L(V,W)$ 是一个线性空间。

### 线性映射引理

假设 $v_1,...,v_n$ 是 $V$ 的一组基，且 $w_1,...,w_n$ 是 $W$ 中的任意向量。那么，存在唯一地一个线性映射 $T:V\rightarrow W$ ，满足：对于每一个 $k=1,...,n$ ，都有 $Tv_k=w_k$ 。

### 线性映射的性质

**线性映射将 $0$ 映射到 $0$**：设 $T$ 是一个从 $V$ 到 $W$ 的线性映射，则 $T(0)=0$ 。

### 零空间

对于 $T\in L(V,W)$ ， $T$ 的零空间记为 $null T$ ，是 $V$ 的子集，其由被 $T$ 映射到 $0$ 的所有向量构成：

$$null T=\lbrace v\in V:Tv=0\rbrace$$

零空间 $null T$ 是 $V$ 的一个子空间。

令 $T\in L(V,W)$ ，那么 $T$ 是单射当且仅当 $null T=\lbrace 0\rbrace$ 。

### 值域

对于 $T\in L(V,W)$ ， $T$ 的值域是 $W$ 的子集，由所有等于 $Tv$ （其中 $v\in V$ ）的向量构成：

$$range T=\lbrace Tv:v\in V\rbrace$$

值域 $T$ 是 $W$ 的一个子空间。

### 线性映射基本定理

假设 $V$ 是有限维的且 $T\in L(V,W)$ ，那么 $range T$ 是有限维的，且

$$dim V=dim~nullT+dim~rangeT$$

### 线性映射的矩阵

假设 $T\in L(V,W)$ ， $v_1,...,v_n$ 是 $V$ 的基， $T$ 关于这些基的矩阵是 $m\times n$ 矩阵 $M(T)$ ，其中各元素 $A_{j,k}$ 由下式定义：

$$Tv_k=A_{1,k}w_1+···+A_{m,k}w_m$$

如果从上下文无法明确得知基 $v_1,...,v_n$ 和 $w_1,...,w_n$ 取什么，那么就用 $M(T,(v_1,...,v_n),(w_1,...,w_m))$ 这个记号。

$M(T)$ 的第 $k$ 列包含了将 $T_{v_k}$ 写成 $w_1,...,w_m$ 的线性组合所需的各标量： $Tv_k=\sum\limits_{j=1}^m A_{j,k}w_j$ 。

线性映射之和的矩阵：假设 $S,T\in L(V,W)$ ，那么 $M(S+T)=M(S)+M(T)$ 。

标量与线性映射之积的矩阵：假设 $\lambda\in F$ 且 $T\in L(V,W)$ ，那么 $M(\lambda T)=\lambda M(T)$ 。

### 矩阵乘法

假设 $A$ 是 $m\times n$ 矩阵且 $B$ 是 $n\times p$ 矩阵，那么 $AB$ 定义为一个 $m\times p$ 矩阵，其中第 $j$ 行第 $k$ 列的元素由下式给出：

$$(AB)_{j,k}=\sum\limits_{r=1}^nA_{j,r}B_{r,k}$$

线性映射之积的矩阵：如果 $T\in L(U,V)$ 且 $S\in L(V,W)$ ，那么 $M(ST)=M(S)M(T)$ 。

### $F^{m,n}$

对于正整数 $m$ 和 $n$ ，各元素均属于 $F$ 的所有 $m\times n$ 矩阵构成的集合记作 $F^{m,n}$ 。

容易证明， $F^{m.n}$ 是维数为 $mn$ 的向量空间。