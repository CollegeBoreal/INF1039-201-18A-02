
```python
import heapq

def heapsort(iterable):
    h = []
    for value in iterable:
        heapq.heappush(h, value)
    return [heapq.heappop(h) for i in range(len(h))]
    
li = [4,1,3,2,16,9,10,14,8,7]

print heapsort(li)
```
