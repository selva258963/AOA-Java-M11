
# EX 1D Sorted Array using Divide and Conquer Approach.
## DATE:15/08/2025
## AIM:
To write a Java program to for given constraints.
Median of Two Sorted Arrays
Given two sorted arrays nums1 and nums2 of size m and n respectively, return the median of the two sorted arrays.
The overall run time complexity should be O(log (m+n)).
Example 1:

Input: nums1 = [1,3], nums2 = [2]
Output: 2.00000
Explanation: merged array = [1,2,3] and median is 2.
The overall run time complexity should be O(log (m+n)).

## Algorithm
1.Start and read the two sorted arrays nums1 and nums2.

2.Initialize two pointers p1 = 0 and p2 = 0 to track the current positions in both arrays.

3.Use a helper function getMin() that returns the smaller of the current elements from both arrays and moves the corresponding pointer forward.

4.Compute the total length of both arrays;If total length is even, discard the first (total/2 - 1) elements using getMin(), then take the next two values and return their average.If total length is odd, discard the first (total/2) elements using getMin() and return the next value.

5.Output the median and end the program.

## Program:
```
/*
Program - Sorted Array using Divide and Conquer Approach
Developed by: Selvamuthu Kumaran V
Register Number: 212222040151
*/
```
```import java.util.Scanner;
public class Solution {
    private int p1 = 0, p2 = 0;
    private int getMin(int[] nums1, int[] nums2) {
        if (p1 < nums1.length && p2 < nums2.length) {
            return nums1[p1] < nums2[p2] ? nums1[p1++] : nums2[p2++];
        } else if (p1 < nums1.length) {
            return nums1[p1++];
        } else if (p2 < nums2.length) {
            return nums2[p2++];
        }
        return -1; 
    }
    public double findMedianSortedArrays(int[] nums1, int[] nums2) {
       int total=nums1.length+nums2.length;
       if(total%2==0)
       {
           for(int i=0;i<total/2-1;i++)
           getMin(nums1,nums2);
           return (double) ((getMin(nums1,nums2)+getMin(nums1,nums2))/2.0);
       }
       else
       {
       for(int i=0;i<total/2;i++)
           getMin(nums1,nums2);
       }
       return getMin(nums1,nums2);
    }
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        Solution sol = new Solution();
        int m = sc.nextInt();
        int[] nums1 = new int[m];
        for (int i = 0; i < m; i++) {
            nums1[i] = sc.nextInt();
        }
        int n = sc.nextInt();
        int[] nums2 = new int[n];
        for (int i = 0; i < n; i++) {
            nums2[i] = sc.nextInt();
        }
        double median = sol.findMedianSortedArrays(nums1, nums2);
        System.out.println("Median of the two sorted arrays = " + median);
        
        sc.close();
    }
}
```

## Output:

<img width="921" height="346" alt="image" src="https://github.com/user-attachments/assets/b21b2907-c364-4f21-b45d-b01d5297f88a" />


## Result:
The program successfully implemented and the expected output is verified.
