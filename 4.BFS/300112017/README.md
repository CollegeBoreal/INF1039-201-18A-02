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
while search_queue:
    person = search_queue.popleft()
    if person_is_seller(person):
        print person + " is a mango seller!"
    else:
        search_queue += graph[person]
        print False
        ```
