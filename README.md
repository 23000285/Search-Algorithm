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
#Program for linear search method to match the item in a list
#Developed by: VENKATANATHAN P R
#RegisterNumber: 23000285

def linearSearch(array,n,k):
    for i in range(0,n):
        if(array[i]==k):
            return i
    return -1
    
array = eval(input())
# k-item to be seared for
k = eval(input()) 
# get the length of array and store in the variable n
n=len(array)
# sort the array
array.sort()
#use the function for linear search
result = linearSearch(array,n,k)
'''use if-else to print sorted array and "Element not found" if the item is not present in 
the list otherwise print sorted array and "Element found at index: ", result'''
if(result==-1):
    print(array,"\nElement not found")
else:
    print(array,"\nElement found at index: ",result)

```
ii)	# Find the element in a list using Binary Search(Iterative Method).
```
#Program to find the element in a list using Binary Search(Iterative Method)..
#Developed by: VENKATANATHAN P R
#RegisterNumber: 23000285

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
#k-item to be searched
k = eval(input())
# sort the array
array.sort()
low=0
high=len(array)-1
# use the binary search function to find the item in the list
result=binarySearchIter(array,k,low,high)
'''use if-else to print sorted array and "Element not found" if the item is not present in the 
list otherwise print sorted array and "Element found at index: ", result'''
if result==-1:
    print(array,"\nElement not found")
else:
    print(array,"\nElement found at index: ",result)

```
iii)	# Find the element in a list using Binary Search (recursive Method).
```
#Program to find the element in a list using Binary Search (recursive Method).
#Developed by: VENKATANATHAN P R
#RegisterNumber: 23000285

def BinarySearch(arr, k, low, high):
    if high>=low:
        mid=low+(high-low)//2
        if arr[mid]==k:
            return mid
        elif arr[mid]>k:
            return BinarySearch(arr,k,low,mid-1)
        else:
            return BinarySearch(arr,k,mid+1,high)
    return -1
    
arr = eval(input())
#sort the array
arr.sort()
# k is the element to be searched for
k = eval(input())
# use the binary search function to find the result
result=BinarySearch(arr,k,0,len(arr)-1)
'''use if-else to print sorted array and "Element not found" if the item is not present in the list 
otherwise print sorted array and "Element found at index: ", result'''
if(result==-1):
    print(arr,"\nElement not found")
else:
    print(arr,"\nElement found at index: ",result)

```
## Sample Input and Output

![image](https://github.com/23000285/Search-Algorithm/assets/138970859/bfda7b8f-6601-4abc-a742-b8908781bb65)

![image](https://github.com/23000285/Search-Algorithm/assets/138970859/5c0167de-63a7-4fc6-88d1-2bc0a2b07cc6)

![image](https://github.com/23000285/Search-Algorithm/assets/138970859/1c521453-eecc-45ae-b58d-283fabdd84d4)


## Result
Thus the linear search and binary search algorithm is implemented using python programming.
