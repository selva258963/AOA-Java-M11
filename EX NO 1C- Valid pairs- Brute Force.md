
# EX 1C Valid Pairs using Brute Force Approach
## DATE:13/08/25
## AIM:
Given an array of integers nums and an integer k, return the number of unique k-diff pairs in the array.

A k-diff pair is an integer pair (nums[i], nums[j]), where the following are true:

0 <= i, j < nums.length
i != j
|nums[i] - nums[j]| == k

## Algorithm
1.Start and read the array nums and integer k.


2.Sort the array in non-decreasing order to easily detect duplicates and compare differences.


3.For each index i, skip it if it is a duplicate of the previous element.


4.For each i, scan forward with index j = i+1 to find the first value where |nums[i] - nums[j]| == k; if found, increment the count and stop checking for that i.


5.Continue until all possible pairs are checked, return the count, and end the program.

 

## Program:
```
/*
Program - Valid Pairs using Brute Force Approach
Developed by: selvamuthu Kumaran V
Register Number: 212222040151
*/
```
```
import java.util.Arrays;
import java.util.Scanner;
public class Solution {
    public int findPairs(int[] nums, int k) {
       int result = 0;
        Arrays.sort(nums);
        for (int i = 0; i < nums.length; i++) {
            if (i > 0 && nums[i] == nums[i - 1]) {
                continue;
            }
            for (int j = i + 1; j < nums.length; j++) {
                if (Math.abs(nums[i] - nums[j]) == k) {
                    result++;
                    break;   
                }
            }
        }
        return result;
    }
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);
        int n = scanner.nextInt();
        int[] nums = new int[n];
        for (int i = 0; i < n; i++) {
            nums[i] = scanner.nextInt();
        }
        int k = scanner.nextInt();
        Solution sol = new Solution();
        int result = sol.findPairs(nums, k);
        System.out.println(result);
        scanner.close();
    }
}

```

## Output:
<img width="503" height="300" alt="image" src="https://github.com/user-attachments/assets/f5568266-cae8-4725-b38e-f4dc1117af0c" />



## Result:
The program successfully implemented and the expected output is verified.
