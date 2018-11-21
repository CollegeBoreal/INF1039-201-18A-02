'''
graph = {}
graph["ROMEO"] = ["didier", "ibrahima"]
graph["dider"] = [" olaitan", " abs"]
graph["ibrahima"] = ["dane", "cheik"]
graph["olaitan"] = ["abdel", "halima"]
graph["abs"] = ["randah", "david"]
graph["dane"] = ["armand", "fabrice"]
graph["cheik"] = ["djouma", "etienne"]
graph["abdel"] = []
graph["halima"] = []
graph["randah"] = []
graph["david"] = []
graph["armand"] = []
graph["fabrice"] = []
graph["djouma"] = []
graph["etienne"] = []

def person_is_sller(name):
     if (name == "armand"): 
      return true
     else :
      return false 
from collections import deque
search_queue = deque()
search_queue += graph["ROMEO"]
def search(name):
    search_queue = deque()
    search_queue += graph[person]
    searched = []
while search_queue:
     person = search_queue.popleft()
     if  person not  in searched:
        if person[-1] == 'm':
            if person_is_seller(person_is_seller):
             print person + "is a mando seller!"
            
else:
        search_queue += graph[person]
        searched.append(person)
    
search("ROMEO")
