# Linear Search and Binary search

## Aim:

To write a program to perform linear search and binary search using python programming.

## Equipment’s required:

1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Moodle-Code Runner

## Algorithm:

## Linear Search:

1. Start from the leftmost element of array[] and compare k with each element of array[] one by one.
2. If k matches with an element in array[] , return the index.
3. If k doesn’t match with any of elements in array[], return -1 or element not found.

## Binary Search:

1. Set two pointers low and high at the lowest and the highest positions respectively.
2. Find the middle element mid of the array ie. arr[(low + high)/2]
3. If x == mid, then return mid.Else, compare the element to be searched with m.
4. If x > mid, compare x with the middle element of the elements on the right side of mid. This is done by setting low to low = mid + 1.
5. Else, compare x with the middle element of the elements on the left side of mid. This is done by setting high to high = mid - 1.
6. Repeat steps 2 to 5 until low meets high

## Program:

i) #Use a linear search method to match the item in a list.

```python
# Program to search the item in a list using linear search.
# Developed by : Pragadeeswaran L
# RegisterNumber : 212223240120
def linear_search(array,n,k):
    for i in range(0,k):
        if n==array[i]:
            return i
    return -1
array=eval(input())
n=eval(input())
array.sort()
k=len(array)
result=linear_search(array,n,k)
if (result == -1):
    print(array)
    print("Element not found")
else:
    print(array)
    print("Element found at index: ",result)


```

ii) # Find the element in a list using Binary Search(Iterative Method).

```python
# Program to find the element in a list using Binary Search(Iterative Method).
# Developed by : Pragadeeswaran L
# RegisterNumber : 212223240120
def binary_search(array,n,low,high):
    while(low<=high):
        mid=low+(high-low)//2
        if array[mid]==n:
            return mid
        elif array[mid]>n:
            high=mid-1
        else:
            low=mid+1
    return -1
array=eval(input())
n=eval(input())
array.sort()
result=binary_search(array,n,0,len(array)-1)
if(result== -1):
    print(array)
    print("Element not found")
else:
    print(array)
    print("Element found at index: ",result)




```

iii) # Find the element in a list using Binary Search (recursive Method).

```python
# Program to find the element in a list using Binary Search(recursive Method).
# Developed by : Pragadeeswaran L
# RegisterNumber : 212223240120
def binarysearch(array,k,low,high):
    if low<=high:
        mid=low+(high-low)//2
        if array[mid]==k:
            return mid
        elif array[mid]>k:
            return binarysearch(array,k,low,mid-1)
        else:
            return binarysearch(array,k,mid+1,high)
    return -1
array=eval(input())
array.sort()
k=eval(input())
result=binarysearch(array,k,0,len(array)-1)
if(result==-1):
    print(array)
    print("Element not found")
else:
    print(array)
    print("Element found at index: ",result)


```

## Sample Input and Output

i) #Use a linear search method to match the item in a list.
![Screenshot 2024-04-17 204150](https://github.com/Pragadeeswaran-bit/Search-Algorithms/assets/147473828/75f96f76-5a8c-46ea-9f03-f77332e4892d)
![Screenshot 2024-04-17 204202](https://github.com/Pragadeeswaran-bit/Search-Algorithms/assets/147473828/1d94f37e-2d82-4dac-9b40-674b63c2a483)


ii) # Find the element in a list using Binary Search(Iterative Method).
![Screenshot 2024-04-17 204309](https://github.com/Pragadeeswaran-bit/Search-Algorithms/assets/147473828/acabde3e-c00a-4601-8987-2ddcf89f68b3)
![Screenshot 2024-04-17 204321](https://github.com/Pragadeeswaran-bit/Search-Algorithms/assets/147473828/8c75b352-98c9-4560-a7e8-eb6771f65f25)


iii) # Find the element in a list using Binary Search (recursive Method).
![Screenshot 2024-04-17 204413](https://github.com/Pragadeeswaran-bit/Search-Algorithms/assets/147473828/4c3e0718-5a33-4f2c-8e51-d896146ebb03)
![Screenshot 2024-04-17 204420](https://github.com/Pragadeeswaran-bit/Search-Algorithms/assets/147473828/bef252bb-6399-4a42-8ffd-671ddccb947f)



## Result

Thus the linear search and binary search algorithm is implemented using python programming.
