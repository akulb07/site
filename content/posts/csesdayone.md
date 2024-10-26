---
title: "Solving the CSES Problem Set: Day 1"
date: "2024-10-26"
draft: false
---


# Introductory Problems

## [Weird Algorithm](https://cses.fi/problemset/task/1068)

In this problem, we're given an integer `n`. If `n` is even, we have to divide it by 2, and if `n` is odd, we have to multiply it by 3 and add 1. This process is to be repeated until `n` is one.

Fairly straightforward, nothing much to say here.
```py 
n = int(input(""))
print(n, end = " ")
while n != 1:
    if n % 2 == 0:
        n = n // 2
    else:
        n =  n*3 + 1
    print(n, end = " ")
```

## [Missing Number](https://cses.fi/problemset/task/1083)

In this problem, we’re given a list of numbers from `1` to `n`, with one missing integer. The goal is to find this missing number efficiently.

### Approach 1
The first approach uses the formula for the sum of the first `n` natural numbers.

By calculating this expected sum and subtracting the sum of the given numbers, we can find the missing number in constant time.

Here, "Constant time" means the time it takes to solve a problem does not increase as the input size grows. In this case, finding the missing number takes the same amount of time, no matter how large `n` is, because it uses a fixed formula without loops or extensive calculations.

```python
n = int(input(""))
l = list(map(int, input("").split()))
print((n * (n + 1)) // 2 - sum(l))
```

### Approach 2
The second approach involves using a set to store all the numbers in the input list. We then iterate from `1` to ``n`` and check if each number is in the set. The number that isn't in the set is the missing one.

Here, using a list is not recommended as to check if an item is there in a list, Python must go through each item one by one until it finds a match (or determines that the item is not present), which is extremely slow.

```python
n = int(input(""))
numbers = set(map(int, input().split()))
 
for i in range(1, n + 1):
    if i not in numbers:
        print(i)
```

## [Repetitions](https://cses.fi/problemset/task/1069)

In this problem, we have to find the length of the longest consecutive sequence of identical characters in a given string.

This problem is also fairly simple, we can iterate through the string comparing each character to the previous one.

We will need two variables:  one to track the current count of consecutive repetitions and another to store the maximum count found so far.

Here, we cannot check if the current character is equal to the next one (`n[i] == n[i+1]`), because when we reach the last character (at index `len(n) - 1`), trying to access `n[i+1]` would result in an out-of-bounds error.


```python
n = input("")
count = 1
max_l = 1

for i in range(1, len(n)):
    if n[i] == n[i-1]:
        count += 1
        max_l = max(count, max_l)
    else:
        count = 1
print(max_l)
```


This concludes this post. I will be writing more as I solve additional problems. You can also check out my solutions in my [GitHub repository](https://github.com/akulb07/CompetitiveProgramming), which I will be updating regularly.

