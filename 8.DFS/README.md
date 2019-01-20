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

# BFS

```
graph = {
    'A': set(['B', 'C']),
    'B': set(['A', 'D', 'E']),
    'C': set(['A', 'F']),
    'D': set(['B']),
    'E': set(['B', 'F']),
    'F': set(['C', 'E'])
}

def bfs_paths(graph, start, goal):
    queue = [(start, [start])]
    while queue:
        (vertex, path) = queue.pop(0)
        for next in graph[vertex] - set(path):
            if next == goal:
                yield path + [next]
            else:
                queue.append((next, path + [next]))

def shortest_path(graph, start, goal):
    try:
        return next(bfs_paths(graph, start, goal))
    except StopIteration:
        return None

print shortest_path(graph, 'A', 'F') # ['A', 'C', 'F']
```
