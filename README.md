# blind-8-75
Search in rotated sorted array
Obviously we use binary search.

variables : l,r,mid

initially l=0,r=n-1

find mid index.

if the value at mid index is equal to target , return mid index.

else, we need to reduce(half) the sample size.



Key thing:



When we rotate a sorted array,(has 2 sorted subarrays), we are left with only one sorted subarray.(either left half is sorted or right half is sorted).



Find which half is sorted using condition: if nums[mid]>nums[r]

if condition is true, left half is sorted.

else, right half is sorted.( there might be case where still both halves are sorted ,but that need not be analysed in this program).



1)if left half is sorted, check if target element is present in that sorted sub array.

i.e  a) if nums[l]<=target<nums[mid], eliminate right half. i.e r=mid-1 

 one more thing is , 'equal to condition' with respect to left index element is important. ( with respect to mid index element , we have already checked earlier).

  b)else target element is in the right sub array.



2)else, right half will be sorted. check if target element is present in that sorted sub array. 

i.e a) if nums[mid]<target<=nums[r] , eliminate left half. i.e l=mid+1.

Equal to condition with respect to right index element is important.

   b) else target element is in the left sub array.



Time complexity: O(logn)

Space complexity: O(1)
