# Programming_Assingment-7


1. Write a Python Program to find sum of array?
sol:
l = [1,2,3,-412, 123, 369, 111]

arraySum = 0
for i in l:
    arraySum += i
    
print("Sum of array: ", arraySum)
Sum of array:  197



2. Write a Python Program to find largest element in an array?
sol:
l = [1,2,3,-412, 123, 369, 111]

arrayMax = -9999999999999

for i in l:
    if i > arrayMax:
        arrayMax = i

arrayMax
369



3. Write a Python Program for array rotation?
sol:
l = [1,2,3,-412, 123, 369, 111]

print("Rotated array:")
print(l[::-1])
Rotated array:
[111, 369, 123, -412, 3, 2, 1]





4. Write a Python Program to Split the array and add the first part to the end?
sol:
def splitAdd(l, split):
    '''
    l = list
    split = splitIndex
    '''
    out = []
    for i in range(len(l)):
        index = (i+len(l)+split)%len(l)
        out.append(l[index])
        
    return out
l = [1,2,3,-412, 123, 369, 111]
splitIndex = 2
splitAdd(l, splitIndex)
[3, -412, 123, 369, 111, 1, 2]





5. Write a Python Program to check if given array is Monotonic?
sol:
def monotonicCheck(array):
    flag = True
    
    if array[0] >= array[len(array)-1]:
        for i in range(len(array)-2):
            if array[i] < array[i+1]:
                flag = False
    else:
        for i in range(len(array)-2):
            if array[i] > array[i+1]:
                flag = False
                
    return flag
array = [1,2,3,56, 124, 369]

monotonicCheck(array)
True
array = [123,43, 12, 2, -23,-345]
monotonicCheck(array)
True
array = [123,-23, 783, -98,0, 12]
monotonicCheck(array)
False



