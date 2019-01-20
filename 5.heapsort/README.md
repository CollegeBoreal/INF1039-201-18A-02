# heapsort

A heapsort can be implemented by pushing all values onto a heap and then popping off the smallest values one at a time:

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

# smallest element

Heap elements can be tuples. This is useful for assigning comparison values (such as task priorities) alongside the main record being tracked:



```
import heapq

h = []
heapq.heappush(h, (5, 'write code'))
heapq.heappush(h, (7, 'release product'))
heapq.heappush(h, (1, 'write spec'))
heapq.heappush(h, (3, 'create tests'))
print heapq.heappop(h)
(1, 'write spec')
```
