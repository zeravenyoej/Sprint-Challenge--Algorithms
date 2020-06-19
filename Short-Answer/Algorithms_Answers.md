#### Please add your answers to the ***Analysis of  Algorithms*** exercises here.

## Exercise I

a) O(n)
As the input size increase, the time it takes to complete the algorithm increases linearly. 
If n = 0, it recurses zero times. 
If n = 1, it recurses one time. 
If n = 2, it recurses two times.
If n = 3, it recurses three times. 
if n = 4, it recurses four times. etc. 


b) O(n * logn)
sum = 0
    for i in range(n):   <----0(n)>
      j = 1
      while j < n:   <------O(logn)>
        j *= 2
        sum += 1

The outter loop is O(n) because its efficiency is directly proportional to the input size.
The inner loop is O(logn) because it's cutting down the number of loops disproportionately. 

c) O(n)
The algorithm uses recursion but is still linear, as the computation time is entirely/proportionally/linearly depdendent on the input size. As the input size increase, the time it takes to complete the algorithm increases linearly. 


## Exercise II

The problem seems (deliberately) open ended. I wrote my proposed solution under the assumption that an answer for F already exists, and I am merely searching for it. 

def get_min_of_f (building, floor):
    low = 0                         -----> Get zeroth floor of building 
    high = len(building)            -----> Get highest floor of building via len()

    while low < high              -----> loop through the possibilities of the best "f", but can only do so if high is bigger than low
        mid = (high + low) // 2       -----> find the current middle floor

        if building[mid] == floor:    ------> if the middle of the building is equal to the floor, you've found it, and you return it
            return building[mid]

        elif building[mid] > floor:  ------> if the middle floor of the building is higher than the floor I'm searching for...
            high = mid - 1            ------> ...I get rid of the "high"/top half of the buildings

        elif building[mid] < floor:  --> if the middle floor of the building is lower than the floor I'm searching for...
            low = mid + 1             ------> ...I get rid of the "low"/bottom half of the buildings

runtime complexity: O(n) = The bigger the input size (aka the bigger the building), the longer it will take to search through it.