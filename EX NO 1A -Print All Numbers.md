
# EX 1A Print All Numbers
 
## DATE:06/08/2025
## AIM:
Write a Java program that takes an integer input N from the user and prints all the numbers from 1 to N, separated by spaces, on a single line.

## Algorithm
1. Start the program and initialize all required variables
2. Prompt the user to enter an integer value **N** and read the input
3. Set a loop control variable **i = 1** to begin iterating from the first number
4. Repeat the process of printing the current value of **i** followed by a space, and increment **i** by 1
5. Continue the loop until **i** exceeds **N**, then terminate the program successfully
  

## Program:

```
Program - Print All Numbers
Developed by: Selvamuthu Kumaran V
Register Number:  212222040151
```
```
import java.util.*;
public class main{
    public static void main(String[] args){
        Scanner sc = new Scanner(System.in);
        int a = sc.nextInt();
        for(int i=1;i<=a;i++){
            System.out.print(i+" ");
        }
    }
}

```
## Output:

<img width="501" height="244" alt="image" src="https://github.com/user-attachments/assets/4f6dc9e8-2240-47f4-8a1b-52b81cdd1945" />


## Result:


Thus the program successfully prints all the numbers from 1 to N in a single line, separated by spaces.
