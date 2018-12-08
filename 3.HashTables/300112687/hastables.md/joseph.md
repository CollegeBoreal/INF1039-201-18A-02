```
def check_voter(name):
  if voted.get(name):
    print "kick them out"
  else:
    voted[name] = True  
    print "let them vote!"
    
check_voter("joseph")
check_voter("nsomwe")
check_voter("nsomwe")
