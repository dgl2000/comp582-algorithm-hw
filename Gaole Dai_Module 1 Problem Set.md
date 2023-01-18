# Answer to Module 1 Problem Set

* Student Name: Gaole Dai

* Student ID: S01435587

### Problem 1

**b) Procedure A is NOT an algorithm**

The program will never halt. Since the while statement is always True, the codes inside the while loop will execute, but they never break, which result in an infinite loop.

### Problem 2

**a) Procedure A is an algorithm**

Though the while statement is always True, the variable $$i$$ increases each time, and when it reaches 10000000000 the program will halt.

### Problem 3

**c) It is not possible to decide of procedure A is an algorithm**

While the program external_procedure() halts, program 3 is an algorithm, otherwise not. Because if external_procedure() halts, program 3 will halt while $$i\geq 10000000$$.

### Problem 4

$$\mathcal{O}(N^2)$$

the outer and inner for loops both execute N times, thus the computational complexity is $$\mathcal{O}(N^2)$$.

### Problem 5

$$\mathcal{O}(N^2)$$

For every $$0\leq i \lt N$$, the inner loop executes $$(N-i)$$ times, thus the total cost could be calculated with different $$i$$ value.

Total Cost $$= N [i=0] + N-1 [i=1] + N-2[i=2] +...+ 1$$

$$= \frac{(N+1)\times N}{2} = \frac{1}{2} (N^2 + N) = \mathcal{O}(N^2)$$

### Problem 6

$$\mathcal{O}(N)$$

For the outer loop, the program executes $$N$$ times, for the inner loop, the program executes $$M$$ times, the total cost is $M \times N$. However, since "$$M$$ is a symbolic constant completely independent of $$N$$", the Big Oh is $$\mathcal{O}(N)$$.

### Problem 7

**Algorithm:**

Input: Base integer x and exponent non-negative integer m.

Output: The calculated value of $x^m$.

```python
def myPow(x, m):
    if m == 0:
        return 1
    if m == 1:
        return x
    if m % 2 == 0:
        temp = pow(x, m // 2)
        return temp * temp
    temp = pow(x, m // 2)
    return x * temp * temp
```

**Proof sketch:**

Proof $x^m = myPow(x, m)$, where m is non-negative integer.

* Base case 1 - m = 0: $left = x^0 = 1$;  $right = myPow(x, 0) = 1$ $\Rightarrow$ $left = right$

* Base case 2 - m = 1: $left = x^1 = x$; $ right = myPow(x, 1) = x$ $\Rightarrow$ $left = right$

* Assume proved for all $m\leq z \space(z\geq 2)$ 

* For m = z + 1:
  * Case 1 - if z is even, then m is odd. The program goes to $temp = myPow(x, m // 2)$, $z//2 = (z+1)//2$, since the correctness is proved for $m=z$, and the return value is known as $temp * temp =x^z$. The program would execute exactly the same iterations as $m = z$, except for the last recursive execute, return $x * temp * temp = x * x^z$, which is $x^{z+1}$, correctness for this case proved. 
  * Case 2 -  if z is odd, then m is even. The program also goes to $temp = myPow(x, m // 2)$. However, in this case, $z//2 +1 =(z+1)//2$
    * if $z//2$ is odd, then $myPow(x, z)$ returns $x * temp * temp$ every time until reach the base case and produce result $x * x^k * x^k = x^z \Rightarrow x^{k} * x^{k} = x^{z-1}$, where $k$ is **odd**; while $myPow(x, z+1)$ returns $temp * temp$ every time and iterate one more time than $myPow(x, z)$, thus, the return value is $x^{k+1} * x^{k+1} = x^{k} * x^{k} * x^2$, as $x^{k} * x^{k} = x^{z-1}$ , the return value is then $x^{z+1}$, correctness for this sub-case proved.
    * if $z//2$ is even, then $myPow(x, z)$ executes $x * temp * temp$ for only the **first** recursion case and return $temp * temp$ for the remaining recursion cases, thus the return value is $x * x^{k} * x^k = x^z \Rightarrow x^{k} * x^{k} = x^{z-1}$ where $k$ is **even**; while $myPow(x, z)$ executes $x * temp * temp$ for only the **last** recursion case and return $temp*temp$ for the remaining recursion cases, thus the return value is $x^{k+1} * x^{k+1} = x^{k} * x^{k} * x^2$, as $x^{k} * x^{k} = x^{z-1}$ , the return value is then $x^{z+1}$, correctness for this sub-case proved.

Thus, program $myPow(x, m)$ could halt under each case (while executing recursively and reaching the base case), and the correctness of the algorithm is proved.

**Complexity**:

$\mathcal{O}(\log_{2}(m))$

Case 1 - m = 0: $\mathcal{O}(1)$;

Case 2 - m = 1: $\mathcal{O}(1)$;

Case 3 - m is odd: The algorithm recursively divide 2 until reach the base case, thus, the total execution time is $\log_{2}(m)$; complexity is : $\mathcal{O}(\log_2{m})$;

Case 4 - m is even: Same as case 3, The algorithm recursively divide 2 until reach the base case, thus, the total execution time is also $\log_{2}(m)$;  complexity is : $\mathcal{O}(\log_2{m})$;

Total cost = $\mathcal{O}(1) + \mathcal{O}(1) + \mathcal{O}(\log_2{m}) + \mathcal{O}(\log_2{m})$ = $\mathcal{O}(\log_2{m})$.

### Problem 8

**Algorithm:**

Input: An array of numbers that were in ascending order, has rearranged the list to "cycle around" from some middle point.

Output: The index of the original starting point.

```python
def findStart(A):
    length = len(A)
    if length == 0 or length == 1:
        return 0
    else:
        value = findStartHelper(A, 0, length - 1)
        return A.index(value)

# Binary search, slide the array to two sides (left and right) each time, A[start, middle] and A[middle+1, end]
def findStartHelper(A, start, end):
    if end - start == 0:
        return A[start]
    
    middle = start + (end - start) // 2

    # if any side is not in ascending order (compare the start element and middle element), go to that side.
    if A[start] > A[middle]:
        return findStartHelper(A, start, middle)
    if A[middle + 1] > A[end]:
        return findStartHelper(A, middle + 1, end)

    # if both side are in ascending order, go to the side with min start value.
    if A[start] < A[middle + 1]:
        return findStartHelper(A, start, middle)
    else:
        return findStartHelper(A, middle + 1, end)

```

**Proof Sketch:**

Proof findStart(A) function which uses binary search function findStartHelper(A, start, end) halts and returns the index of the original starting point in the array.

* Special cases: when array length is 0 or 1, return 0.
* For array length larger than 2, it goes to findStartHelper(A, start, end).
* Induction on length of function findStartHelper(A, start, end):
  * where length is the size of the array and equals to (end - start + 1).
* Base case: end = start
  * Algorithm returns the start value
* Assume proved for length = k
* For length = k+1
  * Case 1: Start value > middle value;
    * The left slide values are not in ascending order, which means the starting point lies in the left slide A[start, middle], goes to the left slide and recursively executes.
  * Case 2: Middle left1 value > end value;
    * The right slide values are not in ascending order, which means the starting point lies in the right slide A[middle, end], goes to the right slide and recursively executes.
  * Case 3: Start value < Middle left1 value
    * When not in case 1 or 2, this indicates both two slides are in ascending order, if left slide first value is smaller than the right slide first value, the starting point lies in the left slide, goes to the right slide and recursively executes.
  * Case 4: Middle left1 <  end value
    * Similar to case 4, if right slide first value is smaller than the left slide first value, the starting point lies in the right slide, goes to the right slide and recursively executes.

Thus, under every case, the slide interval goes strictly smaller than the original interval, and halt when find the smallest value (starting point), the correctness is also proved.

**Complexity**:

$\mathcal{O}(\log_{2}(N))$

Case 1 - length = 0: $\mathcal{O}(1)$;

Case 2 - length = 1: $\mathcal{O}(1)$;

Case 3 - length $\geq$ 2: For each if case, the array is divided into two slides each time, the algorithm could be regarded as recursively divide 2 until reach the base case, thus, the total execution number is $\log_{2}(N)$; complexity is : $\mathcal{O}(\log_2{N})$;

Total cost = $\mathcal{O}(1) + \mathcal{O}(1) + \mathcal{O}(\log_2{N})$ = $\mathcal{O}(\log_2{N})$.