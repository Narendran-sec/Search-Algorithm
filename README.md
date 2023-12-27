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
i)	#Use a linear search method to match the item in a list.
```
Program for linear search method to match the item in a list
Developed by:Narendran.K
RegisterNumber: 23013500
def linearSearch(array,k):
    for i in range(len(array)):
        if array[i]==k:
            return i
    return -1
array = eval(input())
k=eval(input())
array.sort()
result=linearSearch(array,k)
if(result==-1):
    print(array)
    print("Element not found")
else:
    print(array)
    print("Element found at index: ",result)


```
ii)	# Find the element in a list using Binary Search(Iterative Method).
```
Program to find the element in a list using Binary Search(Iterative Method)..
Developed by:Narendran.K
RegisterNumber: 23013500
def binarySearchIter(array, k):
    low=0
    high=len(array)-1
    mid=0
    while low<=high:
        mid=(high+low)//2
        if array[mid]<k:
            low=mid+1
        elif array[mid]>k:
            high=mid-1
        else:
            return mid
    return -1
array = eval(input())
array.sort()
k = eval(input()) #k-item to be searched
result=binarySearchIter(array, k)
if (result==-1):
    print (array)
    print("Element not found")
else:
    print(array)
    print("Element found at index: ",str(result))
```
iii)	# Find the element in a list using Binary Search (recursive Method).
```
Developed by: Narendran.K
RegisterNumber: 23013500

def BinarySearch(arr, k, low, high):
    if high>=low:
        mid=(high+low)//2
        if arr[mid]==k:
            return mid
        elif arr[mid]>k:
            return BinarySearch(arr, k, low, mid-1)
        else:
            return BinarySearch(arr, k, mid+1, high)
    else:
        return -1
arr = eval(input())
arr.sort()
k = eval(input()) 
low=0
high=len(arr)-1
result=BinarySearch(arr, k, low, high)
if(result==-1):
    print(arr)
    print("Element not found")
else:
    print(arr)
    print("Element found at index: ",result)
```
## Sample Input and Output:

![Screenshot 2023-12-27 183631](https://github.com/Narendran-sec/Search-Algorithm/assets/147473131/c20c2155-70b0-493f-b031-f9250cb965fc)


![output 2 in search](https://github.com/Narendran-sec/Search-Algorithm/assets/147473131/f25feada-c8c0-4625-8f74-ac5d1fa6baaf)

![output 3 in search](https://github.com/Narendran-sec/Search-Algorithm/assets/147473131/b3ab4db8-51cc-4c82-88e8-fd3e356a993a)



## Result
Thus the linear search and binary search algorithm is implemented using python programming.
