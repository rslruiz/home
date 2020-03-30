## Work in progress

- 100daysofcode
- ProjectEuler
- codewars
- DATALGO in DBTC

### ProjectEuler
[GitHub link](https://rslruiz.github.io/ProjectEuler/)

```
# Problem 5: Smallest multiple
from functools import reduce

def gcd(a, b):
    while b:
        a, b = b, a % b
    return a

def lcm(a, b):
    return a * b // gcd(a, b)

def smallestMult(n):
    return reduce(lcm,range(1,n+1))
```


```
# Problem 4: Largest palindrome product
def largestPalindromeProduct(n):
    max = int('9'*n)
    min = 9*10**(n-1)
    for i in range(max, min, -1):
        for j in range(i, min, -1):
            prod = i*j
            if ispalindrome(prod):
                return prod
    return -1

def ispalindrome(n):
    pal = palin = n; drome = 0
    while pal != 0: 
        drome = drome*10 + pal%10
        pal //= 10
    if palin - drome == 0:
        return True
    else: return False
```


```
# Problem 3: Largest prime factor
def largestPrimeFactor(n):
    for d in range(2, n):
        while n%d == 0:
            n //= d

        if d*d > n: break
    return n
```

```
# Problem 2: Even fibonacci numbers
def fibonacci(n):
    a, b = 1, 0
    while a <= n:
        yield a
        a, b = a+b, a

def fiboEvenSum(n):
    return sum(i for i in fibonacci(n) if not i%2 )
```

```
# Problem 1: Multiples of 3 and 5
def multiplesOf3and5(number):
    return sum(i for i in range(number) if i%3 == 0 or i%5 ==0)
```

### Website

[www.rslruiz.com](http://www.rslruiz.com)

### Contact

rslruiz@icloud.com, rslruiz@one-bosco.org
