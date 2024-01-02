# Linear Search and Binary search
## Aim:
To write a program to perform linear search and binary search using python programming.
## Equipment’s required:
1.	Hardware – PCs
2.	Anaconda – Python 3.7 Installation / Moodle-Code Runner
## Algorithm:
## Linear Search:
1.	Start from the leftmost element of array[] and compare k with each element of array[] one by one.
2.	If k matches with an element in array[] , return the index.
3.	If k doesn’t match with any of elements in array[], return -1 or element not found.
## Binary Search:
1.	Set two pointers low and high at the lowest and the highest positions respectively.
2.	Find the middle element mid of the array ie. arr[(low + high)/2]
3.	If x == mid, then return mid.Else, compare the element to be searched with m.
4.	If x > mid, compare x with the middle element of the elements on the right side of mid. This is done by setting low to low = mid + 1.
5.	Else, compare x with the middle element of the elements on the left side of mid. This is done by setting high to high = mid - 1.
6.	Repeat steps 2 to 5 until low meets high
## Program:
### i)Use a linear search method to match the item in a list.
```
''' 
Program for linear search method to match the item in a list
Developed by: Jerowin Geo J A
RegisterNumber: 212223100016
'''
def linearSearch(array,n,k):
    for i in range(n):
        if k==array[i]:
            return i
    return -1
    
array = eval(input())
array.sort()

k = eval(input()) 
n=len(array)
print(array)
result = linearSearch(array,n,k)
if result ==-1:
    print("Element not found")
else:
    print("Element found at index: ",result)
```
### ii)Find the element in a list using Binary Search(Iterative Method).
```
''' 
Program to find the element in a list using Binary Search(Iterative Method)..
Developed by: Jerowin Geo J A
RegisterNumber: 212223100016
'''
def binarySearchIter(array, k, low, high):
    while low<=high:
        mid=low+(high-low)//2
        if array[mid]==k:
            return mid
        elif array[mid]<k:
            low=mid+1
        else:
            high=mid-1
    return -1
array = eval(input())
array.sort()
k = eval(input()) #k-item to be searched
print(array)
n=len(array)
t=binarySearchIter(array, k, 0,n-1)
if t==-1:
    print("Element not found")
else:
    print("Element found at index: ",t)

```
### iii)Find the element in a list using Binary Search (recursive Method).
```
''' 
Program to find the element in a list using Binary Search (recursive Method).
Developed by: Jerowin Geo J A
RegisterNumber: 212223100016
'''
def BinarySearch(arr, k, low, high):
    if low<=high:
        mid=low+(high-low)//2
        if arr[mid]==k:
            return mid
        elif arr[mid]<k:
            return BinarySearch(arr, k, mid+1, high)
        else:
            return BinarySearch(arr, k, low, mid-1)
    else:
        return -1
arr = eval(input())
arr.sort()
print(arr)
k = eval(input())
result=BinarySearch(arr, k, 0, len(arr)-1)
if result == -1:
    print("Element not found")
else:
    print("Element found at index: ", result)

```
## Sample Input
### (i)Use a linear search method to match the item in a list.
![image](https://github.com/JerowinGeo/Search-Algorithm/assets/147139744/ba9ca74e-d467-4e3c-b340-821e240762f5)

### (ii)Find the element in a list using Binary Search(Iterative Method).
![image](https://github.com/JerowinGeo/Search-Algorithm/assets/147139744/d67d88e9-3de9-4338-8069-33bbcaea92df)

### (iii)Find the element in a list using Binary Search (recursive Method).
![image](https://github.com/JerowinGeo/Search-Algorithm/assets/147139744/014d0da8-47e9-4cc1-94cd-33f197288c50)

### Output
### (i)Use a linear search method to match the item in a list.
![image](https://github.com/JerowinGeo/Search-Algorithm/assets/147139744/83b9e4b7-457d-4a43-88ad-717cede9abc2)

### (ii)Find the element in a list using Binary Search(Iterative Method).
![image](https://github.com/JerowinGeo/Search-Algorithm/assets/147139744/158c57b0-8b1f-4d03-8502-2312d5c06e03)

### (iii)Find the element in a list using Binary Search (recursive Method).
![image](https://github.com/JerowinGeo/Search-Algorithm/assets/147139744/475e2660-7289-4d60-a151-c83feae0a2bd)


## Result
Thus the linear search and binary search algorithm is implemented using python programming.
