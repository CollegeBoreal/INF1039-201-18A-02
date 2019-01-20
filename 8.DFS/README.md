# Depth First Search

https://eddmann.com/posts/depth-first-search-and-breadth-first-search-in-python/

```python
graph = {'Romeo': set(['Didier', 'Ibrahima']),
         'Didier': set(['Olaitan', 'Abbas']),
         'Ibrahima': set(['Dane', 'Cheik']),
         'Olaitan': set(['Abdel', 'Halima']),
         'Abbas': set(['Randah', 'David']),
         'Dane': set(['Armand', 'Fabrice']),
        'Cheik': set(['Djouma', 'Etienne']),
        'Abdel': set([]),
        'Halima': set([]),
        'Randah': set([]),
        'David': set([]),
        'Armand': set([]),
        'Fabrice': set([]),
        'Djouma': set([]),
        'Etienne': set([])
}

def dfs(graph, start):
    visited, stack = set(), [start]
    while stack:
        vertex = stack.pop()
        if vertex not in visited:
            visited.add(vertex)
            stack.extend(graph[vertex] - visited)
    return visited
    
a = dfs(graph, "Romeo")
print len(a)
```
