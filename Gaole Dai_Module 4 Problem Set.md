# Module 4 Problem Set

* Student Name: Gaole Dai
* Student ID: S01435587

### Problem 1

 $T(n) = 3 T(\frac{n}{2}) + n^2$

According to the master theorem,

$a = 3, b=2, k=2, p=0$

Since $3<2^2$ and $0 \ge 0$, 

$T(n) = \mathcal{O}(n^k\log^{p}(n))=\mathcal{O}(n^2)$

### Problem 2

 $T(n) = 4 T(\frac{n}{2}) + n^2$

According to the master theorem,

$a=4, b=2, k=2, p=0$

Since $4=2^2$ and $0>-1$, 

$T(n) = \mathcal{O}(n^{\log_{b}^{(a)}} \log^{p+1}(n)) = \mathcal{O}(n^2\log(n))$

### Problem 3

$T(n) = T(\frac{n}{2}) + n^2$

According to the master theorem,

$a=1, b=2, k=2, p=0$

Since $1<2^2$ and $0\ge0$, 

$T(n) = \mathcal{O}(n^k\log^{p}(n))=\mathcal{O}(n^2)$

### Problem 4

$T(n) = 16 T(\frac{n}{4}) + n$

According to the master theorem,

$a=16, b=4, k=1, p=0$

Since $16>4^1$ , 

$T(n) = \mathcal{O}(n^{\log_{b}^{(a)}}) = \mathcal{O}(n^2)$

### Problem 5

$T(n) = 2 T(\frac{n}{2}) + n \log(n)$

According to the master theorem,

$a=2, b=2, k=1, p=1$

Since $2=2^1$ and $1>-1$, 

$T(n) = \mathcal{O}(n^{\log_{b}^{(a)}} \log^{p+1}(n)) = \mathcal{O}(n\log^2(n))$

### Problem 6

$T(n) = 2 T(\frac{n}{2}) + \frac{n}{\log(n)}$

According to the master theorem,

$a=2, b=2, k=1, p=-1$

Since $2=2^1$ and $-1=-1$, 

$T(n) = \mathcal{O}(n^{\log_{b}^{(a)}} \log(\log(n)) = \mathcal{O}(n\log(\log(n)))$

### Problem 7

$T(n) = 2 T(\frac{n}{4}) + n^{0.51}$

According to the master theorem,

$a=2, b=4, k=0.51, p=0$

Since $2<4^{0.51}$ and $0\ge0$, 

$T(n) = \mathcal{O}(n^k\log^{p}(n))=\mathcal{O}(n^{0.51})$

### Problem 8

$T(n) = 6 T(\frac{n}{3}) + n^{2}\log(n)$

According to the master theorem,

$a=6, b=3, k=2, p=1$

Since $6<3^{2}$ and $1\ge0$, 

$T(n) = \mathcal{O}(n^k\log^{p}(n))=\mathcal{O}(n^2\log(n))$

### Problem 9

$T(n) = 7 T(\frac{n}{3}) + n^2$

According to the master theorem,

$a=7, b=3, k=2, p=0$

Since $7 < 3^2$ and $0 \ge 0$, 

$T(n) = \mathcal{O}(n^k\log^{p}(n))=\mathcal{O}(n^2)$

### Problem 10

$T(n) = \sqrt{2} T(\frac{n}{2}) + \log(n)$

According to the master theorem,

$a=\sqrt{2}, b=2, k=0, p=1$

Since $\sqrt{2} > 2^0$ , 

$T(n) = \mathcal{O}(n^{\log_{b}^{(a)}}) = \mathcal{O}(n^{\frac{1}{2}})$

### Problem 11

**Answer**:  $T(n) = \frac{5}{2}n - \frac{1}{2}$



According to the master theorem,

$a=3, b=3, k=0, p=0$

Since $3 < 3^0$, $T(n) = \theta(n^{\log_{b}^{(a)}}) = \theta(n)$

Thus, $T(n) = c_{1}n + c_{0}$



Since $T(1) = 2$, then $T(1) = c_1 + c_{0} =2$

So first set $c_{1} =2$ and $c_{0}=0$,

Then, $T(n)=2n$

However, confirm with coefficients, $3T(\frac{n}{3}) + 1 = 3(\frac{2n}{3}) + 1\neq 2n$



$T(n)=c_{1}n+c_{0}$

$3T(\frac{n}{3})+1 = 3(c_{1}\frac{n}{3}+c_{0})+1=c_{1}n+c_{0} = c_{1}n + 3c_{0}+1$

Then, $-1=2c_{0}$, $c_{0}=-\frac{1}{2}$

Since $c_{1}+c_{0}=2$, then $c_{1}=\frac{5}{2}$

Confirm with coefficients, try with $c_{0}=-\frac{1}{2}$, $c_{1}=\frac{5}{2}$

$T(n)=\frac{5}{2}n - \frac{1}{2}$

$3T(\frac{n}{3})+1 = 3(\frac{5}{2}\times\frac{n}{3}-\frac{1}{2})$

$=\frac{5}{2}n - \frac{3}{2}+1$

$=\frac{5}{2}n - \frac{3}{2}+1=T(n)$

Thus,   $T(n) = \frac{5}{2}n - \frac{1}{2}$

### Problem 12

**Answer**: $T(n) = 75n!$

Try $cn^{k}$

$T(n-1)=c(n-1)^{k}$, $nT(n-1)=cn(n-1)^k$

No, polynomials different degree.

Then, try $T(n) = cn!$

$nT(n-1)=nc(n-1)!$

$T(n) = nc(n-1)!$

Since $T(2)=150$

$T(2) = 2c =150$

$c = 75$

Confirm with coefficient $c=75$

Then, $T(n) = 75n!$

$nT(n-1) = n \times 75\times (n-1)!=75n!$

Confirmed, thus $T(n) = 75n!$

### Problem 13

**Answer**: $T(n) = \mathcal{O}(n\log(n))$



Main recurence is true for all $n$, so substitute '9n/10' for s in the template, then substitude 'n/10' for s, add together to give a new recurrence

$T(\frac{9n}{10}) = T(\frac{81n}{100})+T(\frac{9n}{100}) + \frac{9n}{10}$

$T(\frac{9n}{100}) = T(\frac{81n}{100})+T(\frac{9n}{100})+\frac{9n}{10}$

$T(\frac{n}{10})=T(\frac{9n}{100})+T(\frac{n}{100})+\frac{n}{10}$

$T(n)=T(\frac{9n}{10})+T(\frac{n}{10})+n$

$=T(\frac{81n}{100})+T(\frac{9n}{100})+\frac{9n}{10}+T(\frac{9n}{100})+T(\frac{n}{100})+\frac{n}{10}+n$

$=T(\frac{81n}{100})+2T(\frac{9n}{100})+T(\frac{n}{100})+\frac{9n}{10}+\frac{n}{10}+n$

$=T(\frac{81n}{100})+2T(\frac{9n}{100})+T(\frac{n}{100})+2n$

$(\frac{9}{10})^k(n)\leq 1$, $k-\log_{\frac{10}{9}}(n)\geq 0$, and $\mathcal{O}(n\log_{\frac{10}{9}}(n))$

Thus, $T(n) = \mathcal{O}(n\log(n))$

### Problem 14

**Answer**: $T(n) = \mathcal{O}(n\log(n))$



According to Problem 13

$T(n)=cn\log(n)$

$T(\frac{9n}{10})=c(\frac{9n}{10})\log(\frac{9n}{10})$

$=\frac{9n}{10}cn\log(\frac{9n}{10})$

$=\frac{9n}{10}cn(\log(n) + \log(\frac{9n}{10}))$

$=\frac{9n}{10}cn\log(n) + \frac{9}{10}cn\log(\frac{9n}{10})$



$T(\frac{n}{10})=c(\frac{n}{10})\log(\frac{n}{10})$

$=(\frac{1}{10})cn\log(\frac{1}{10}n)$

$=(\frac{1}{10})cn(\log(n)+\log(\frac{1}{10}))$

$=(\frac{1}{10})cn\log(n)+(\frac{1}{10})cn\log(\frac{1}{10})$



$T(\frac{9n}{10})+T(\frac{n}{10})=cn\log(n)+cn(\frac{9}{10})\log(\frac{9}{10})+cn(\frac{1}{10})\log(\frac{1}{10})$



Let $A=(\frac{9}{10})\log(\frac{9}{10})+(\frac{1}{10})\log(\frac{1}{10})$



Then, $T(\frac{9n}{10})+T(\frac{n}{10})=cn\log(n)+cAn$

So, $T(\frac{9n}{10})+T(\frac{n}{10})+n=cn\log(n)+(cA+1)n$

This means that,

$cA+1=0$, $c=-\frac{1}{A}$

Solution is $T(n)=-\frac{1}{A}n\log(n)$, where $A$ as above, also, since A is a negative number, $T(n) = \mathcal{O}(n\log(n))$