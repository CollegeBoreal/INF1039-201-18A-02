def selectionSort(arr): 
 newArr = []
 for i in range(len(arr)):
     smallest = findSmallest(arr)
     newArr.apprend(arr.pop(smallest))
 return newArr
 print selectionSort([5, 3, 6, 2, 10])
