## Problems

### 3-1 Asymptotic behavior of polynomials

> Let
> 
> $$p(n)=\sum_{i=0}^d a_i n^i$$,
> 
> where $$a_d > 0$$, be a degree-$$d$$ polynomial in $$n$$, and let $$k$$ be a constant. Use the definitions of the asymptotic notations to prove the following properties.

> __a__. If $$k \ge d$$, then $$p(n)=O(n^k)$$

$$p(n)=\sum_{i=0}^d a_i n^i \le \sum_{i=0}^d a_i n^k$$

> __b__. If $$k \le d$$, then $$p(n)=\Omega(n^k)$$

$$p(n)=\sum_{i=0}^d a_i n^i \ge \sum_{i=k}^d a_i n^i$$

> __c__. If $$k = d$$, then $$p(n)=\Theta(n^k)$$

$$p(n)=O(n^k)$$ and $$p(n)=\Theta(n^k)$$

> __d__. If $$k > d$$, then $$p(n)=o(n^k)$$

$$p(n)=\sum_{i=0}^d a_i n^i < \sum_{i=0}^d a_i n^k$$

> __e__. If $$k < d$$, then $$p(n)=\omega(n^k)$$

$$p(n)=\sum_{i=0}^d a_i n^i > \sum_{i=k}^d a_i n^i$$

### 3-2 Relative asymptotic growths

> Indicate, for each pair of expressions $$(A,B)$$ in the table below, whether $$A$$ is $$O$$, $$o$$, $$\Omega$$, $$\omega$$, or $$\Theta$$ of $$B$$. Assume that $$k \le 1$$, $$\epsilon > 0$$, and $$c > 1$$ are constants. Your answer
should be in the form of the table with "yes" or "no" written in each box.

| $$A$$ | $$B$$ | $$O$$ | $$o$$ | $$\Omega$$ | $$\omega$$ | $$\Theta$$ |
|:-:|:-:|:-:|:-:|:-:|:-:|:-:|
| $$\lg^kn$$ | $$n^\epsilon$$ | yes | yes | no | no | no |
| $$n^k$$ | $$c^n$$ | yes | yes | no | no | no |
| $$\sqrt{n}$$ | $$n^{\sin n}$$ | no | no | no | no | no |
| $$2^n$$ | $$2^{n/2}$$ | no | no | yes | yes | no |
| $$n^{\lg c}$$ | $$c^{\lg n}$$ | yes | no | yes | no | yes |
| $$\lg(n!)$$ | $$\lg(n^n)$$ | yes | no | yes | no | yes |

### 3-3 Ordering by asymptotic growth rates

> __a__. Rank the following functions by order of growth; that is, find an arrangement $$g_1, g_2, \dots ,g_{30}$$ of the functions satisfying $$g_1 = \Omega(g2)$$, $$g_2 = \Omega(g3)$$, $$\dots$$ , $$g_{29} = \Omega(g_{30})$$. Partition your list into equivalence classes such that functions $$f(n)$$ and $$g(n)$$ are in the same class if and only if $$f(n) = \Theta(g(n))$$.

$$2^{2^{n+1}}$$ $$>$$ $$2^{2^n}$$ $$>$$ $$(n+1)!$$ $$>$$ $$n!$$ $$>$$ $$e^n$$ $$>$$ $$n \cdot 2^n$$ $$>$$ $$2^n$$ $$>$$ $$(\frac{3}{2})^n$$ $$>$$ $$n^{\lg \lg n}$$ $$=$$ $$(\lg n)^{\lg n}$$ $$(\lg n)!$$ $$>$$ $$n^3$$ $$n ^ 2$$ $$=$$ $$4^{\lg n}$$ $$>$$ $$n \ln n$$ $$>$$ $$=$$ $$\lg(n!)$$ $$>$$ $$n$$ $$=$$ $$2^{\lg n}$$ $$>$$ $$(\sqrt{2})^{\lg n}$$ $$>$$ $$2^{\sqrt{2 \lg n}}$$ $$>$$ $$\lg^2n$$ $$>$$ $$\ln n$$ $$>$$ $$\sqrt{\lg n}$$ $$>$$ $$\ln \ln n$$ $$>$$ $$2^{\lg^\ast n}$$ $$>$$ $$\lg^\ast (\lg n)$$ $$=$$ $$\lg^\ast n$$ $$>$$ $$\lg(\lg^\ast n)$$ $$>$$ $$1$$ $$=$$ $$n^{1/\lg n}$$

> __b__. Give an example of a single nonnegative function $$f(n)$$ such that for all functions $$g_i(n)$$ in part (a), $$f(n)$$ is neither $$O(g_i(n))$$ nor $$\Omega(g_i(n))$$.

$$n^{\sin n}$$

### 3-4 Asymptotic notation properties

> Let $$f(n)$$ and $$g(n)$$ be asymptotically positive functions. Prove or disprove each of the following conjectures.

> __a__. $$f(n)=O(g(n))$$ implies $$g(n)=O(f(n))$$.

False, $$f(n)=1$$, $$g(n)=n$$.

> __b__. $$f(n)+g(n)=\Theta(\min(f(n), g(n)))$$.

False, $$f(n)=1$$, $$g(n)=n$$.

> __c__. $$f(n)=O(g(n))$$ implies $$\lg(f(n))=O(\lg(g(n)))$$, where $$\lg(g(n)) \ge 1$$ and $$f(n) \ge 1$$ for all sufficiently large $$n$$.

True.

$$f(n) \le cg(n)$$

$$\lg(f(n)) \le \lg c + \lg g(n) = O(\lg g(n))$$

> __d__. $$f(n)=O(g(n))$$ implies $$2^{f(n)}=O(2^{g(n)})$$.

False, $$f(n)=2n$$, $$g(n)=n$$.

> __e__. $$f(n)=O((f(n))^2)$$

False, $$f(n)=1/n$$.

> __f__. $$f(n)=O(g(n))$$ implies $$g(n)=\Omega(f(n))$$.

True.

$$f(n) \le cg(n)$$

$$g(n) \ge \frac{1}{c}f(n)$$

> __g__. $$f(n)=\Theta(f(n/2))$$.

False, $$f(n)=4^n$$, $$f(n/2)=2^n$$.

> __h__. $$f(n)+o(f(n))=\Theta(f(n))$$.

False.

### 3-5 Variations on $$O$$ and $$\Omega$$

> Some authors define $$\Omega$$ in a slightly different way than we do; let’s use $$\overset{\infty}{\Omega}$$ (read "omega infinity") for this alternative definition. We say that $$f(n) = \overset{\infty}{\Omega}(g(n))$$ if there exists a positive constant c such that $$f(n) \ge cg(n) \ge 0$$ for infinitely many
integers $$n$$.

### 3-6 Iterated functions

> We can apply the iteration operator $$\ast$$ used in the $$\lg^\ast$$ function to any monotonically increasing function $$f(n)$$ over the reals. For a given constant $$c \in \mathbb{R}$$, we define the iterated function $$f_c^\ast$$ by
>
> $$f_c^\ast(n)=\min\{i \ge 0: f^{(i)}(n) \le c\}$$,
>
> which need not be well defined in all cases. In other words, the quantity $$f_c^\ast(n)$$ is the number of iterated applications of the function f required to reduce its argument down to $$c$$ or less.
>
> For each of the following functions $$f(n)$$ and constants $$c$$, give as tight a bound as possible on $$f_c^\ast(n)$$.

|$$f(n)$$|$$c$$|$$f_c^\ast(n)$$|
|:-:|:-:|:-:|
|$$n-1$$|0|$$n$$|
|$$\lg n$$|1|$$\lg^\ast n$$|
|$$n/2$$|1|$$\lg n$$|
|$$n/2$$|2|$$(\lg n)-1$$|
|$$\sqrt{n}$$|2|$$2 \log_n2$$|
|$$\sqrt{n}$$|1|$$2 \log_n1$$|
|$$n^{1/3}$$|2|$$3 \log_n2$$|
|$$n/\lg n$$|2|$$?$$|