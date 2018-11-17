''' graph = {}

 graph["ROMEO"] = ["didier", "ibrahima"]
 graph["dider"] = [" olaitan", " abs"]
 graph["ibrahima"] = ["dane", "cheik"]
 graph["olaitan"] = ["abdel", "halima"]
 graph["abs"] = ["randah", "david"]
 graph["dane"] = ["armand", "fabrice"]
 graph["cheik'] = ["djouma", "etienne"]
 graph["abdel"] = []
 graph["halima"] = []
 graph["randah"] = []
 graph["david] = []
 garph["armand"] = []
 graph["fabrice"] = []
 graph["djouma"] = []
 graph["etienne"] = []

 def person_is_sller(name):
     if (name == "armand"):
      retrun true
 eles :
      retrun false 
    
 from collections import deque
 search_queue = deque()
 search_queue += graph["ROMEO"]
 wihle search_queue
     person = search_queue.poplef()
     if not person in searched :
         if person_is_seller(person):
             print person + "is a mando seller!"
             retrun true
     else:
        search_queue += graph[person]
        searched.append(person)
 retrun false
search("ROMEO")
