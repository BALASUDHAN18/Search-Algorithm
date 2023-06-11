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

''' 
Program for linear search method to match the item in a list
Developed by: BALASUDHAN P
RegisterNumber: 212222240017
'''
def linearSearch(array,n,k):
    for i in range(0,n):
        if (array[i]==k):
            return i
    return -1
    
array = eval(input())
k = eval(input()) 
n=len(array)
array.sort()
result = linearSearch(array,n,k)
if(result==-1):
    print(array)
    print("Element not found")
else:
    print(array)
    print("Element found at index: ",result)
# use if-else to print sorted array and "Element not found" if the item is not present in the list otherwise print sorted array and "Element found at index: ", result



```
ii)	# Find the element in a list using Binary Search(Iterative Method).
```

''' 
Program to find the element in a list using Binary Search(Iterative Method)..
Developed by: BALASUDHAN P
RegisterNumber: 212222240017
'''
def binarySearchIter(array, k, low, high):
    while low <= high:
        mid = low+(high - low)//2
        if array[mid]==k:
            return mid
        elif array[mid]<k:
            low=mid+1
        else:
            high=mid -1
    return -1
    
array = eval(input())
array.sort()
k = eval(input()) 

result = binarySearchIter(array,k,0,len(array)-1)
if(result == -1):
    print(array)
    print("Element not found")
else:
    print(array)
    print("Element found at index: ",result)




```
iii)	# Find the element in a list using Binary Search (recursive Method).
```
''' 
Program to find the element in a list using Binary Search(Recursive Method)..
Developed by: BALASUDHAN P
RegisterNumber: 212222240017
'''
def BinarySearch(arr,k,low,high):
    if high >= low:
        mid = low+(high - low)//2
        if arr[mid]==k:
            return mid
        elif arr[mid]>k:
            return BinarySearch(arr,k,low,mid-1)
        else:
            return BinarySearch(arr,k,mid+1,high)
    else:
      return -1
arr=eval(input())
arr.sort()
k =eval(input())
result=BinarySearch(arr,k,0,len(arr)-1)
if(result == -1):
    print(arr)
    print("Element not found")
else:
    print(arr)
    print("Element found at index: ",result)

```
## Sample Input and Output
![Screenshot 2023-06-11 095153](https://github.com/BALASUDHAN18/Search-Algorithm/assets/118807740/0ba86c9c-f519-46b3-ac69-f90362a59797)


![Screenshot 2023-06-11 095244](https://github.com/BALASUDHAN18/Search-Algorithm/assets/118807740/a7c7fd9a-3fad-46ed-ba7b-0b3569749d78)


![Screenshot 2023-06-11 095321](https://github.com/BALASUDHAN18/Search-Algorithm/assets/118807740/b416964a-67e7-4ca9-ae14-35adcf0ce1b9)

## Result
Thus the linear search and binary search algorithm is implemented using python programming.
