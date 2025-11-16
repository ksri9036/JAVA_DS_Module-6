# EX 1 You’re creating a health monitoring device which stores several sensor readings in an array. To determine the minimum value (e.g., lowest heartbeat), implement a recursive method.
## DATE: 16-11-2025
## AIM:
To write a JAVA program To determine the minimum value (e.g., lowest heartbeat), implement a recursive method.

## Algorithm:
1. Start with the array and begin at the first element.
   
2.If you are at the last element, return that value.

3.Otherwise, find the minimum value in the rest of the array using recursion.

4.Compare the current element with the minimum of the remaining elements.

5.Return the smaller value as the minimum.
   

## Program:
```
/*
Program To determine the minimum value (e.g., lowest heartbeat), implement a recursive method.
Developed by: VIMALA SAHANA W
RegisterNumber: 212223040241
*/
import java.util.Scanner;

public class MinValueRecursive {
    static int findMin(int arr[], int n) {
        if (n == 1)
            return arr[0];
        return Math.min(arr[n - 1], findMin(arr, n - 1));
    }

    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        System.out.print("Enter number of readings: ");
        int n = sc.nextInt();
        int arr[] = new int[n];
        System.out.println("Enter the readings:");
        for (int i = 0; i < n; i++)
            arr[i] = sc.nextInt();
        System.out.println("Minimum value (lowest heartbeat): " + findMin(arr, n));
        sc.close();
    }
}

```

## Output:
<img width="514" height="281" alt="image" src="https://github.com/user-attachments/assets/5caf869d-6c42-4ff6-85a0-52e66d99665b" />

## Result:
Thus the JAVA program to  find the minimum value (e.g., lowest heartbeat), implement a recursive method has implemented successfully.
