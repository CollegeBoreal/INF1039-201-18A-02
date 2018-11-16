graph = {}
graph["Romeo"] = ["Didier", "Ibrahima"]
graph["Didier"] = ["Olaiton", "Abbas"]
graph["Ibrahima"] = ["Dane", "Cheik"]
graph["Olaiton"] = ["Abdel", "Halima"]
graph["Abbas"] = ["Randah", "David"]
graph["Dane"] = ["Armand", "Fabrice"]
graph["Cheik"] = ["Djouma", "Etienne"]
graph["Abdel"] = []
graph["Halima"] = []
graph["Randah"] = []
graph["David"] = []
graph["Fabrice"] = []
graph["Djouma"] = []
graph["Etienne"] = []
graph["Armand"] = []
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
