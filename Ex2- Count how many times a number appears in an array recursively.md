# Ex2 Count how many times a number appears in an array recursively.
## DATE: 16-11-25
## AIM:
To write a Java program to Count how many times a number appears in an array recursively.

## Algorithm
1.Read the array size, array elements, and the number to be counted.

2.Start from index 0 of the array.

3.If the index reaches the end of the array, return 0.

4.Recursively count in the remaining part of the array.

5.If the current element matches the number, add 1 to the count; otherwise, add 0.  

## Program:
```
/*
Program Count how many times a number appears in an array recursively.
Developed by: VIMALA SAHANA W 
RegisterNumber: 212223040241 
*/
import java.util.Scanner;

public class CountOccurrencesRecursive {

    
    public static int countNumber(int[] arr, int index, int target) {
        
        if (index == arr.length) {
            return 0;
        }

        
        int count = (arr[index] == target) ? 1 : 0;
        return count + countNumber(arr, index + 1, target);
    }

    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);

        
        System.out.print("Enter array size: ");
        int size = sc.nextInt();

        int[] arr = new int[size];

        
        System.out.println("Enter " + size + " numbers:");
        for (int i = 0; i < size; i++) {
            arr[i] = sc.nextInt();
        }

        
        System.out.print("Enter number to count: ");
        int target = sc.nextInt();

        
        int result = countNumber(arr, 0, target);

        
        System.out.println("The number " + target + " appears " + result + " times.");

        sc.close();
    }
}

```

## Output:

<img width="652" height="305" alt="image" src="https://github.com/user-attachments/assets/cc1cf6f6-c0ae-4c9b-9b02-fa66fc4ef6dc" />


## Result:
Thus, the Java program to Count how many times a number appears in an array recursively is implemented successfully.
