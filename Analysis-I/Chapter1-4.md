# Analysis I

## Chapter 1: Introduction

## Chapter 2: Starting at the beginning: the natural numbers

### The Peano axioms

**Axiom 2.1**： $0$ 是一个自然数。

**Axiom 2.2**： 如果 $n$ 是一个自然数，那么 $n++$ 也是一个自然数。

**Axiom 2.3**： $0$ 不是任何一个自然数的后继数（successor），即对任何的自然数 $n$ ，$n++\ne 0$ 。

**Axiom 2.4**： 不同的自然数有不同的后继数，即如果 $m,n$ 是自然数且 $m\ne n$ ，则 $n++\ne m++$ 。

**Axiom2.5（数学归纳法原理）**： 设 $P(n)$ 是关于自然数 $n$ 的一个属性，如果 $P(0)$ 为真，且对于某个自然数 $n$ ， $P(n)$ 为真可推出 $P(n+1)$ 也为真，那么对于所有的自然数 $n$ ， $P(n)$ 都为真。

### Addition

**Defination**： 设 $m$ 是一个自然数，为了将零加到 $m$ 上，我们定义 $0+m:=m$ ，现在**归纳地**假设我们已经定义了如何将自然数 $n$ 加到 $m$ 上。那么，我们可以通过定义公式： $(n++)+m:=(n+m)++$ ，将 $n$ 的后继数 $n++$ 加到 $m$ 上。

### Multiplication

**Defination**： 设 $m$ 是一个自然数，为了将零乘以 $m$ ，我们定义 $0\times m:=0$ ，现在**归纳地**假设我们已经定义了如何将 $n$ 乘以 $m$ 。那么，我们可以通过定义公式： $(n++)\times m:=(n\times m)+m$ ，将 $n$ 的后继数 $n++$ 乘以 $m$ 。

## Chapter 3: Set theory

**Axiom of Universal specification（全称分类公理）**： 假设对于每一个对象 $x$ ，我们都有一个关于 $x$ 的属性 $P(x)$ （也就是说，对于每一个 $x$ ， $P(x)$ 要么是一个真命题，要么是一个假命题）。那么，存在一个集合 $\lbrace x:P(x) 为真\rbrace$ ，使得对于每一个对象 $y$ ，都有： $y\in\lbrace x:P(x)为真\rbrace\Leftrightarrow P(y)为真$ 。

**Axiom of Regularity（正则公理）**： 若 $A$ 是一个非空集合，则 $A$ 中至少存在一个元素 $x$ ，使得 $x$ 要么不是一个集合，要么 $x$ 与 $A$ 不相交。

理解：全称分类公理告诉我们“什么样的东西可以组成集合”；而正则公理则规定集合禁止自包含（ $A\in A$ ）与禁止包含死循环（ $A\in B\in C\in A$ ）这两种情况，以避免罗素悖论（Russell's Paradox）。

**Defination**：我们称集合 $X$ 与集合 $Y$ 等势（equal cardinality），当且仅当存在一个双射 $f:X\rightarrow Y$ 。

**Defination**： 设 $n$ 为一个自然数，一个集合 $X$ 被认为具有基数 $n$ ，当且仅当它与集合 $\lbrace i\in N:1\le i\le n\rbrace$（即集合 $\lbrace 1,2,...,n\rbrace$ ）具有相等的基数。我们也说 $X$ 拥有 $n$ 个元素，当且仅当它的基数为 $n$ 。

## Chapter 4: Integers and rationals

