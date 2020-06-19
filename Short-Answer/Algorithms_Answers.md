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

n = size of building
e = number of eggs
f = floor number


def get_min_of_f (n, e, f)

found = false

while floor is not found:
    if 


