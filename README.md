# algorithms



### Insertion Sort

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
