# Answer to Module 2 Problem Set

* Student Name: Gaole Dai
* Student ID: S01435587

### Problem 1

The complexity is $\mathcal{O}(P)$.

$C(P) = 1+3+3^2+3^3+...+3^k$

$P = 3^{k}$

$C(P)= \frac{3^{k+1} - 1}{3-1} = \frac{3^{k+1} - 1}{2}=\frac{3P-1}{2}=\mathcal{O}(P)$

### Problem 2

The complexity is $\mathcal{O}(P)$.

$C(P) = 1+11+11^2+11^3+...+11^k$

$P = 11^{k}$

$C(P)= \frac{11^{k+1} - 1}{11-1} = \frac{11^{k+1} - 1}{10}=\frac{11P-1}{10}=\mathcal{O}(P)$

### Problem 3

<img src="C:\Users\Gloria DAI\AppData\Roaming\Typora\typora-user-images\image-20220901203903950.png" alt="image-20220901203903950" style="zoom: 67%;" />

### Problem 4

**No**. Re-organize the connection to the tree below.

<img src="C:\Users\Gloria DAI\AppData\Roaming\Typora\typora-user-images\image-20220901213925477.png" alt="image-20220901213925477" style="zoom:67%;" />

According to the important theorem,  which is $h(T)\leq \log_{2}(|T|)$, the depth of tree is at most $\log_{2}(T)$, and the longer nodes are never linked to the shorter nodes. However, in this tree, the height $h(T)$ is 4, the total number of nodes is **10**, while $4 \gt \log_{2}{10}$, the tree is impossible to to be the result of running weighted quick union.

### Problem 5

The complexity is $\mathcal{O}(M\log^*(N))$, where $\log^*(N)$ denotes the iterative algorithm.

For the `add_new_set()` operation, it takes $\mathcal{O}(1)$ per op. Assume the total number of `add`, `union and find` operations are $M$, and the total number of `add` operation is $i$, the number of `union-find` operations is then $M-i$. Applying weighted quick union and find with path compression, for a stream of $(M-i)$ `union-find` operations, the complexity is $\mathcal{O}((M-i)\log^*{(N)})$.

Total cost $=T_{Add} + T_{UF} =\mathcal{O}(i) + \mathcal{O}((M-i)\log^{*}(N)) = \mathcal{O}(M\log^{*}(N))$.