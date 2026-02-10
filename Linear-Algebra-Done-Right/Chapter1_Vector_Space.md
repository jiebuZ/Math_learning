# Linear Algebra Done Right

## Chapter 1: Vector Spaces

### 向量空间(vector space)
一个向量空间是一个集合 $V$ ， $V$ 上的加法和标量乘法满足下列性质：

**1.加法交换律(commutativity)**： $\forall u,v\in V,u+v=v+u.$ 

**2.加法结合律(associativity)**： $\forall u,v,w\in V,(u+v)+w=u+(v+w).$ 

**3.加法恒等元(additive identity)**： $\exists 0\in V,s.t.\forall v\in V,v+0=v.$ 

**4.加法逆元(additive inverse)**： $\forall v\in V,\exists w\in V,s.t.v+w=0.$ 

**5.标量乘法结合律(associativity**)： $\forall a,b\in F,v\in V,(ab)v=a(bv).$ 

**6.标量乘法恒等元(multiplicative identity)**： $\forall v\in V,1v=v.$ 

**7.分配律(distributive properties)**：   $\forall a,b\in F,\forall u,v\in V,a(u+v)=au
+av,(a+b)v=av+bv.$ 

### 加法恒等元唯一
证明：

假设存在两个加法恒等元 $0,0'\in V$ ，则有：
 $0'=0'+0=0+0'=0$

即说明加法恒等元唯一。

### 加法逆元唯一
证明：

对 $v\in V$ ，假设 $v$ 存在两个加法逆元 $w,w'\in V$ ，则有：
$w=w+0=w+v+w'=0+w'=w'$

即说明加法逆元唯一。

### 实向量空间的复化
设 $V$ 是实向量空间， $V$ 的复化(complexification)记为 $V_C$ ，等于 $V\times V$ 。 $V_C$ 中的元素为有序对 $(u,v)$ ，其中 $u,v\in V$ ，不过我们把它写作 $u+iv$ 。

$V_C$ 上的加法定义为

$$(u_1+iv_1)+(u_2+iv_2)=(u_1+u_2)+i(v_1+v_2)$$

对所有 $u_1,v_1,u_2,v_2\in V$ 成立。

$V_C$ 上的复标量乘法定义为

$$(a+bi)(u+iv)=(au-bv)+i(av+bu)$$

对所有 $a,b\in R$ 和所有 $u,v\in V$ 成立。

具有如上加法和标量乘法定义的 $V_C$ 是复向量空间。

### 向量空间 $F^S$
$S$ 是一个集合， $F^S$ 是由 $S$ 到 $F$ 的函数全体构成的集合，容易证明 $F^S$ 是一个向量空间。

### 子空间的条件
当且仅当 $V$ 的子集 $U$ 满足下面三个条件时， $U$ 是 $V$ 的子空间(subspace)。

**1.加法恒等元**： $0\in U.$

**2.对于加法封闭(closed under addition)**： $u,w\in U\Rightarrow u+w\in U.$

**3.对于标量乘法封闭(closed under scalar multiplication)**： $a\in F,u\in U\Rightarrow au\in U.$

### 子空间的和
假设 $V_1,...,V_m$ 是 $V$ 的子空间， $V_1,...,V_m$ 的和是由 $V_1,...,V_m$ 中所有可能的和所构成的集合，记作 $V_1+···+V_m$ ，称之为子空间的和(sum of subspaces)，即：

$$
V_1+···+V_m=\{ v_1+···+v_m:v_1\in V_1,...,v_m\in V_m \}
$$

### 子空间的和是包含这些子空间的最小子空间
假设 $V_1,...,V_m$ 是 $V$ 的子空间，那么 $V_1+···+V_m$ 是最小的包含 $V_1,...V_m$ 的子空间。

### 直和
如果 $V_1+···+V_m$ 中的每个元素都能用 $v_1+···+v_m$ (其中各 $v_k\in V_k$ )这种形式唯一地表示出来，则称子空间之和 $V_1+···+V_m$ 为直和(direct sum)。

如果 $V_1+···+V_m$ 是直和，那么用 $V_1\oplus ···\oplus V_m$ 来表示 $V_1+···+V_m$ ，其中记号 $\oplus$ 表示此处的和是直和。

### 直和的条件
假定 $V_1,...,V_m$ 是 $V$ 的子空间，那么 $V_1+···+V_m$ 是直和，当且仅当用 $v_1+···+v_m$ (其中各 $v_k\in V_k$ )表示 $0$ 的唯一方式是将每个 $v_k$ 都取 $0$ 。

证明：

首先假定 $V_1+...+V_m$ 是直和，那么直和的定义就表明用 $v_1+···+v_m$ (其中各 $v_k\in V_k$ )表示 $0$ 的唯一方式是将每个 $v_k$ 取 $0$ 。

现在假定用 $v_1+···+v_m$ (其中各 $v_k\in V_k$ )表示 $0$ 的唯一方式是将每个 $v_k$ 取 $0$ ，令 $v\in V_1+···+V_m$ ，则对某 $v_1\in V_1,...v_m\in V_m$ ，有

$$v=v_1+···+v_m$$

为了说明这个表示法是唯一的，假设对 $u_1\in V_1,...u_m\in V_m$ ，我们也有

$$v=u_1+···+u_m$$

将两个式子相减得到

$$0=(v_1-u_1)+···+(v_m-u_m)$$

因为 $(v_1-u_1)\in V_1,...,(v_m-u_m)\in V_m$ ，这表明每个 $(v_k-u_k)$ 都等于 $0$ ，进而 $v_1=u_1,...v_m=u_m$ ，唯一性得证。

即 $V_1+...+V_m$ 是直和。

### 两个子空间的直和
假定 $U$ 和 $W$ 是 $V$ 的子空间，那么 $\,$ $U+V$ 是直和等价于 $U\cap W=\{0\}.$

### 例题1
假设 $a\in F,v\in V$ 且 $av=0$ ，证明： $a=0$ 或 $v=0$ .

证明：

只需证明当 $a\ne 0$ 时， $v=0$ 即可。

这是因为 $\exists a'\in F,s.t.\,aa'=1$ ，且

$$v=1v=(a'a)v=a'(av)=0$$

即证明了 $v=0$ 在 $a\ne 0$ 时成立。