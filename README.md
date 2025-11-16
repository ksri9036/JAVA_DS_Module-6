# EX3 Write a program to count the number of digits in an integer.
## DATE: 16-11 25
## AIM:
To write a java program to count the number of digits in an integer.

## Algorithm
1.Read the integer from the user.

2.Convert the number to its absolute value (to ignore minus sign).

3.If the number is 0, set digit count = 1.

4.Otherwise, repeatedly divide the number by 10 and increase the count each time.

5.When the number becomes 0, stop and display the count. 

## Program:
```
/*
Program to to count the number of digits in an integer
Developed by: VIMALA SAHANA W
RegisterNumber: 212223040241 
*/
import java.util.Scanner;

public class CountDigits {

    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);

        System.out.print("Enter an integer: ");
        int num = sc.nextInt();

        int count = 0;
        int temp = Math.abs(num);  // Handle negative numbers

        // Special case: number = 0
        if (temp == 0) {
            count = 1;
        } else {
            // Count digits
            while (temp > 0) {
                temp = temp / 10;
                count++;
            }
        }

        System.out.println("Number of digits: " + count);
        sc.close();
    }
}

```

## Output:

<img width="377" height="124" alt="image" src="https://github.com/user-attachments/assets/3edf6a43-7811-4284-ae8b-3700ef928e49" />


## Result:
Thus, the Java program to to count the number of digits in an integer is implemented successfully.
