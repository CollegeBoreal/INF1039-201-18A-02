```
voted = {}
def check_voter(name):
   if voted.get(name):
    print ("kick them out")


   else:
    voted[name] = True
    print ("let them vote!")
check_voter ("tom")

check_voter ("mike")

check_voter ("mike")
def fact (number):
    if number <= 1:
        return 1
    else:
    
        return number * (number-1)
print(fact(200))

```
