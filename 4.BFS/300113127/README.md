```
graph = {}

graph["Romeo"] = ["Didier", "Ibrahima"]
graph["Didier"] = ["Olaitan", "Abas"]
graph["Ibrahima"] = ["Dane", "Cheik"]
graph["Olaitan"] = ["Abdel", "Halima"]
graph["Abas"] = ["Randah", "David"]
graph["Dane"] = ["Armand", "Fabrice"]
graph["Cheik"] = ["Djouma", "Etienne"]
graph["Abdel"] = []
graph["Halima"] = []
graph["Randah"] = []
graph["David"] = []
graph["Armand"] = []
graph["Fabrice"] = []
graph["Djouma"] = []
graph["Etienne"] = []

def person_is_seller(name):
    if (name == "Armand"):
        return True
    else :
        return False
        
from collections import deque
search_queue = deque()
search_queue += graph["Romeo"]

def search(name):
    search_queue = deque()
    search_queue += graph[name]
    searched = []
    while search_queue:
        person = search_queue.popleft()
        if not person in searched:
            if person_is_seller(person):
                print person + " is a mango seller!"
                return True
            else:
                search_queue += graph[person]
                searched.append(person)
    return False
    
search("Romeo")
```        
