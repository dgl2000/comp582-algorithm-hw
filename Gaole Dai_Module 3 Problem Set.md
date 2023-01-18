# Answer to Module 3 Problem Set

* Student Name: Gaole Dai
* Student ID: S01435587

### Problem 1

Selection Sort:

| Times         | Last Step                                 | Trace                   |
| ------------- | ----------------------------------------- | ----------------------- |
| Original      | /                                         | T H I S Q U E S T I O N |
| First Sort    | <u>T</u> H I S Q U <u>E</u> S T I O N     | E H I S Q U T S T I O N |
| Second Sort   | **E** <u>H</u> I S Q U T S T I O N        | E H I S Q U T S T I O N |
| Third Sort    | **E** **H** <u>I</u> S Q U T S T I O N    | E H I S Q U T S T I O N |
| Fourth Sort   | **E H I** <u>S</u> Q U T S T <u>I</u> O N | E H I I Q U T S T S O N |
| Fifth Sort    | **E H I I** <u>Q</u> U T S T S O <u>N</u> | E H I I N U T S T S O Q |
| Sixth Sort    | **E H I I N** <u>U</u> T S T S <u>O</u> Q | E H I I N O T S T S U Q |
| Seventh Sort  | **E H I I N O** <u>T</u> S T S U <u>Q</u> | E H I I N O Q S T S U T |
| Eighth Sort   | **E H I I N O Q** <u>S</u> T S U T        | E H I I N O Q S T S U T |
| Ninth Sort    | **E H I I N O Q S** <u>T</u> <u>S</u> U T | E H I I N O Q S S T U T |
| Tenth Sort    | **E H I I N O Q S S** <u>T</u> U T        | E H I I N O Q S S T U T |
| Eleventh Sort | **E H I I N O Q S S T** <u>U</u> <u>T</u> | E H I I N O Q S S T T U |
| Final         | **E H I I N O Q S S T T U**               | E H I I N O Q S S T T U |

### Problem 2

Insertion Sort:

| Times         | Last Step                   | Trace                       |
| ------------- | --------------------------- | --------------------------- |
| Original      | /                           | T H I S Q U E S T I O N     |
| First Sort    | T **H** I S Q U E S T I O N | H T I S Q U E S T I O N     |
| Second Sort   | H T **I** S Q U E S T I O N | H I T S Q U E S T I O N     |
| Third Sort    | H I T **S** Q U E S T I O N | H I S T Q U E S T I O N     |
| Fourth Sort   | H I S T **Q** U E S T I O N | H I Q S T U E S T I O N     |
| Fifth Sort    | H I Q S T **U** E S T I O N | H I Q S T U E S T I O N     |
| Sixth Sort    | H I Q S T U **E** S T I O N | E H I Q S T U S T I O N     |
| Seventh Sort  | E H I Q S T U **S** T I O N | E H I Q S S T U T I O N     |
| Eighth Sort   | E H I Q S S T U **T** I O N | E H I Q S S T T U I O N     |
| Ninth Sort    | E H I Q S S T T U **I** O N | E H I I Q S S T T U O N     |
| Tenth Sort    | E H I I Q S S T T U **O** N | E H I I O Q S S T T U N     |
| Eleventh Sort | E H I I O Q S S T T U **N** | E H I I N O Q S S T T U     |
| Final         | E H I I N O Q S S T T U     | **E H I I N O Q S S T T U** |

### Problem 3

M U C H L O N G E R Q U E S T I O N

| Times    | Last Step                                                    | Trace                                                        | h-seq |
| -------- | ------------------------------------------------------------ | ------------------------------------------------------------ | ----- |
| Original | /                                                            | M U C H L O N G E R Q U E S T I O N                          |       |
| 1        | <u>M</u> U C H L <u>O</u> N G E R <u>Q</u> U E S T <u>I</u> O N | <u>I</u> U C H L <u>M</u> N G E R <u>O</u> U E S T <u>Q</u> O N | 5     |
| 2        | I <u>U</u> C H L M <u>N</u> G E R O <u>U</u> E S T Q <u>O</u> N | I <u>N</u> C H L M <u>O</u> G E R O <u>U</u> E S T Q <u>U</u> N | 5     |
| 3        | I N <u>C</u> H L M O <u>G</u> E R O U <u>E</u> S T Q U <u>N</u> | I N <u>C</u> H L M O <u>E</u> E R O U <u>G</u> S T Q U <u>N</u> | 5     |
| 4        | I N C <u>H</u> L M O E <u>E</u> R O U G <u>S</u> T Q U N     | I N C <u>E</u> L M O E <u>H</u> R O U G <u>S</u> T Q U N     | 5     |
| 5        | I N C E <u>L</u> M O E H <u>R</u> O U G S <u>T</u> Q U N     | I N C E <u>L</u> M O E H <u>R</u> O U G S <u>T</u> Q U N     | 5     |
| 6        | I N C E L <u>M</u> O E H R <u>O</u> U G S T <u>Q</u> U N     | I N C E L <u>M</u> O E H R <u>O</u> U G S T <u>Q</u> U N     | 5     |
| 7        | I N C E L M <u>O</u> E H R O <u>U</u> G S T Q <u>U</u> N     | I N C E L M <u>O</u> E H R O <u>U</u> G S T Q <u>U</u> N     | 5     |
| 8        | I N C E L M O <u>E</u> H R O U <u>G</u> S T Q U <u>N</u>     | I N C E L M O <u>E</u> H R O U <u>G</u> S T Q U <u>N</u>     | 5     |
| 9        | I N C E L M O E <u>H</u> R O U G <u>S</u> T Q U N            | I N C E L M O E <u>H</u> R O U G <u>S</u> T Q U N            | 5     |
| 10       | I N C E L M O E H <u>R</u> O U G S <u>T</u> Q U N            | I N C E L M O E H <u>R</u> O U G S <u>T</u> Q U N            | 5     |
| 11       | I N C E L M O E H R <u>O</u> U G S T <u>Q</u> U N            | I N C E L M O E H R <u>O</u> U G S T <u>Q</u> U N            | 5     |
| 12       | I N C E L M O E H R O <u>U</u> G S T Q <u>U</u> N            | I N C E L M O E H R O <u>U</u> G S T Q <u>U</u> N            | 5     |
| 13       | I N C E L M O E H R O U <u>G</u> S T Q U <u>N</u>            | I N C E L M O E H R O U <u>G</u> S T Q U <u>N</u>            | 5     |
| 14       | <u>I</u> N <u>C</u> E <u>L</u> M <u>O</u> E <u>H</u> R <u>O</u> U <u>G</u> S <u>T</u> Q <u>U</u> N | <u>C</u> N <u>G</u> E <u>H</u> M <u>I</u> E <u>L</u> R <u>O</u> U <u>O</u> S <u>T</u> Q <u>U</u> N | 2     |
| 15       | C <u>N</u> G <u>E</u> H <u>M</u> I <u>E</u> L <u>R</u> O <u>U</u> O <u>S</u> T <u>Q</u> U <u>N</u> | C <u>E</u> G <u>E</u> H <u>M</u> I <u>N</u> L <u>N</u> O <u>Q</u> O <u>R</u> T <u>S</u> U <u>U</u> | 2     |
| 16       | C E <u>G</u> E <u>H</u> M <u>I</u> N <u>L</u> N <u>O</u> Q <u>O</u> R <u>T</u> S <u>U</u> U | C E <u>G</u> E <u>H</u> M <u>I</u> N <u>L</u> N <u>O</u> Q <u>O</u> R <u>T</u> S <u>U</u> U | 2     |
| 17       | C E G <u>E</u> H <u>M</u> I <u>N</u> L <u>N</u> O <u>Q</u> O <u>R</u> T <u>S</u> U <u>U</u> | C E <u>G</u> E <u>H</u> M <u>I</u> N <u>L</u> N <u>O</u> Q <u>O</u> R <u>T</u> S <u>U</u> U | 2     |
| 18       | C E G E <u>H</u> M <u>I</u> N <u>L</u> N <u>O</u> Q <u>O</u> R <u>T</u> S <u>U</u> U | C E G E <u>H</u> M <u>I</u> N <u>L</u> N <u>O</u> Q <u>O</u> R <u>T</u> S <u>U</u> U | 2     |
| 19       | C E G E H <u>M</u> I <u>N</u> L <u>N</u> O <u>Q</u> O <u>R</u> T <u>S</u> U <u>U</u> | C E G E H <u>M</u> I <u>N</u> L <u>N</u> O <u>Q</u> O <u>R</u> T <u>S</u> U <u>U</u> | 2     |
| 20       | C E G E H M <u>I</u> N <u>L</u> N <u>O</u> Q <u>O</u> R <u>T</u> S <u>U</u> U | C E G E H M <u>I</u> N <u>L</u> N <u>O</u> Q <u>O</u> R <u>T</u> S <u>U</u> U | 2     |
| 21       | C E G E H M I <u>N</u> L <u>N</u> O <u>Q</u> O <u>R</u> T <u>S</u> U <u>U</u> | C E G E H M I <u>N</u> L <u>N</u> O <u>Q</u> O <u>R</u> T <u>S</u> U <u>U</u> | 2     |
| 22       | C E G E H M I N <u>L</u> N <u>O</u> Q <u>O</u> R <u>T</u> S <u>U</u> U | C E G E H M I N <u>L</u> N <u>O</u> Q <u>O</u> R <u>T</u> S <u>U</u> U | 2     |
| 23       | C E G E H M I N L <u>N</u> O <u>Q</u> O <u>R</u> T <u>S</u> U <u>U</u> | C E G E H M I N L <u>N</u> O <u>Q</u> O <u>R</u> T <u>S</u> U <u>U</u> | 2     |
| 24       | C E G E H M I N L N <u>O</u> Q <u>O</u> R <u>T</u> S <u>U</u> U | C E G E H M I N L N <u>O</u> Q <u>O</u> R <u>T</u> S <u>U</u> U | 2     |
| 25       | C E G E H M I N L N O <u>Q</u> O <u>R</u> T <u>S</u> U <u>U</u> | C E G E H M I N L N O <u>Q</u> O <u>R</u> T <u>S</u> U <u>U</u> | 2     |
| 26       | C E G E H M I N L N O Q <u>O</u> R <u>T</u> S <u>U</u> U     | C E G E H M I N L N O Q <u>O</u> R <u>T</u> S <u>U</u> U     | 2     |
| 27       | C E G E H M I N L N O Q O <u>R</u> T <u>S</u> U <u>U</u>     | C E G E H M I N L N O Q O <u>R</u> T <u>S</u> U <u>U</u>     | 2     |
| 28       | C E G E H M I N L N O Q O R <u>T</u> S <u>U</u> U            | C E G E H M I N L N O Q O R <u>T</u> S <u>U</u> U            | 2     |
| 29       | C E G E H M I N L N O Q O R T <u>S</u> U <u>U</u>            | C E G E H M I N L N O Q O R T <u>S</u> U <u>U</u>            | 2     |
| 30       | <u>C</u> <u>E</u> <u>G</u> <u>E</u> <u>H</u> <u>M</u> <u>I</u> <u>N</u> <u>L</u> <u>N</u> <u>O</u> <u>Q</u> <u>O</u> <u>R</u> <u>T</u> <u>S</u> <u>U</u> <u>U</u> | <u>C</u> <u>E</u> <u>E</u> <u>G</u> <u>H</u> <u>I</u> <u>I</u> <u>L</u> <u>N</u> <u>N</u> <u>O</u> <u>O</u> <u>Q</u> <u>R</u> <u>S</u> <u>T</u> <u>U</u> <u>U</u> | 1     |

### Problem 4

**Yes**. 

* For selection sort, it always picked the highest or lowest element from the unsorted part and putting it at the beginning. Thus, whenever all the keys are identical, the complexity for making **comparison** is  $n-1 + n-2 + n-3 + ... +1 = \mathcal{O}(n^2)$, and the complexity for **exchange** is $\mathcal{O}(m)$. 
* For insertion sort, its complexity of making **comparison** is the same as selection sort. However, since all the keys are identical, it did **not need to make any** **exchange**.
* Thus, if all keys are identical, insertion sort work better than selection sort.

### Problem 5

**No**.

* For selection sort, as problem 4 stated, its **comparison** is always  $n-1 + n-2 + n-3 + ... +1 = \mathcal{O}(n^2)$, and the complexity for **exchange** is $\mathcal{O}(m)$. 
* For insertion sort, the **comparison** is the same as selection sort. However, since all keys are in reverse order, the complexity for keys exchange is at worst  $n-1 + n-2 + n-3 + ... +1 = \mathcal{O}(m^2)$. The total cost of comparison and exchange for insertion sort is worse than selection sort.
* Thus, if all keys are in reverse order, selection sort work better than insertion sort.

### Problem 6

Steps:

1. Sort the list
2. Iterate through the sorted list, check and eliminating duplicates by looking the item next to each other. The cost is $\mathcal{O}(n)$.

Python code is shown below:

```python
def removeDuplicates(inputList):
    inputList.sort()
    i = 0
    while i < len(inputList)-1:
        if (inputList[i] == inputList[i+1]):
            inputList.remove(inputList[i+1])
        else:
            i += 1
    return inputList
```



### Problem 7

Steps:

1. Sort letters of each string. 
   1. String a, sting b: a'= sort string a'; b'=sort string b'; if a == b  then a and b originally are jumbles
2. Sort letter, then sort the **signature** to put jumbles together. The complexity for printing out the result is $\mathcal{O}(N)$.

Python code is shown below:

```python
def jumbleWords(inputList):
    # Sort the string elements in the input list
    res = [''.join(sorted(element)) for element in inputList]
    # Join the key and sorted value into signature
    tuple_list = list(zip(res, inputList))
    # Sort the tuple to put jumbles together
    tuple_list.sort(key = lambda x: x[0])
    # Print out the jubmle words
    prev = tuple_list[0][0]
    for i, (a, b) in enumerate(tuple_list):
        if (a == prev):
            print(b, end =" ")
        else:
            print('\n')
            print(b, end =" ")
        prev = a 
```

### Problem 8

* Because the h-seq is efficient only under situation whatever the min value of the odd is larger then the max value of the even value.
* For example, if the given list is $1\space5\space 2\space 7\space 3\space 9$ , where the both the even and odd sequences are in order. The even index values never compared with odd numbered indices before h= 1.
* The h-seq is valid when the arrange for even index subsequence and odd index subsequence to be out of order relative to each other.
* However, the input list is never be sure with the order. Thus, $1, 2, 4, 8, 16, ..., 2^k$ is bad for shell sort.

### Problem 9

* In overall, insertion sort works better than selection sort. 
* Insertion sort is faster on inputs that are **partially-sorted**. If array is partially-sorted, the cost for insertion sort is at best $\mathcal{O}(n)$, which indicates that insertion sort make $n$ comparison (scenario also includes Problem 4).
* But the cost for selection sort always take $\mathcal{O}(n^2)$ for worst case and average case.

