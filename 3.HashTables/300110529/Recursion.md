```
def compter(n):
  print('Début de compter(',n,')')
  if n == 0:
    print('Decollage!')
  else:
    print(n)
    compter(n - 1)
  print('Fin de compter(',n,')')

limit = int(input())
compter(limit)
```
