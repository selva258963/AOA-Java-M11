
# EX 1B Power of 2
## DATE: 17/11/2025
## AIM:
Given an integer n, return true if it is a power of two. Otherwise, return false.
An integer n is a power of two, if there exists an integer x such that n == 2x.
## Algorithm

1.Start and read the integer num from the user.

2.Compute sq as the integer value of the square root of num.

3.Check whether sq * sq is equal to num.

4.If equal, return true; otherwise, return false.

5.Print the returned result and end the program.

## Program:
```
/*
Program - Power of 2
Developed by: Selvamuthu Kumaran V
Register Number:  212222040151
*/
import java.util.Scanner;

public class Solution {

    public boolean isPowerOfTwo(int n) {
     //Type your code here
     if(n<=0){
         return false;
     }
     return(n&(n-1))==0;
     
     
     
    }

    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);
        Solution sol = new Solution();
        int n = scanner.nextInt();

        boolean result = sol.isPowerOfTwo(n);
        System.out.println(result);

        scanner.close();
    }
}


   
```

## Output:

<img width="507" height="201" alt="image" src="https://github.com/user-attachments/assets/0fbda797-4ee8-4e5f-80cf-5be8b8754b66" />


## Result:
The program successfully implemented and the expected output is verified.
