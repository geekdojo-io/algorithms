# Algorithms

```python
 list('algorithms').sort() == list('logarithms').sort()
``` 

### Sieve of Eratosthenes
The sieve of Eratosthenes is an algorithm for finding all prime numbers to a given upper limit efficiently.

```python

def sieve(n):
    primes = []
    sieve = [False, False] + [True] * (n - 1)
    for p in range(2, n + 1):
        if sieve[p]: # prime number
            primes.append(p)
            for i in range(p, n + 1, p):
                sieve[i] = False
    return primes

print(sieve(100))

```


### Insertion Sort

#### insertion_sort.py
```python

def insertion_sort(ar):
    for i in range(1, len(ar)):
        j = i
        while j > 0 and ar[j-1] > ar[j]:
            ar[j-1], ar[j] = ar[j], ar[j-1]
            j -= 1
    return ar

ar = list(map(int, input().split()))
insertion_sort(ar)
print(ar)

```
