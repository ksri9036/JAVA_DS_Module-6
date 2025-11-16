# Ex5 Count Inversions in an Array
## DATE: 16-11 25
## AIM:
To write a Java program  to Count the number of inversions in an array where inversion is defined as: arr[i] > arr[j] and i < j

## Algorithm
1.Read the array size and elements from the user.

2.Set a counter to 0.

3.Compare each element with every element to its right.

4.If arr[i] > arr[j] and i < j, increase the counter.

5.Print the total inversion count. 

## Program:
```
/*
Program toto Count the number of inversions in an array where inversion is defined as: arr[i] > arr[j] and i < j
Developed by: VIMALA SAHANA W
RegisterNumber: 212223040241
*/
import java.util.Scanner;

public class CountInversions {

    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);

        // Input array size
        System.out.print("Enter array size: ");
        int n = sc.nextInt();

        int[] arr = new int[n];

        // Input array elements
        System.out.println("Enter " + n + " elements:");
        for (int i = 0; i < n; i++) {
            arr[i] = sc.nextInt();
        }

        int count = 0;

        // Count inversions using simple nested loops
        for (int i = 0; i < n; i++) {
            for (int j = i + 1; j < n; j++) {
                if (arr[i] > arr[j]) {
                    count++;
                }
            }
        }

        System.out.println("Number of inversions: " + count);

        sc.close();
    }
}

```

## Output:
<img width="455" height="274" alt="image" src="https://github.com/user-attachments/assets/b78e8aaa-d3c5-4398-a278-46d596a9d8ff" />



## Result:
Thus the Java program to to Count the number of inversions in an array where inversion is defined as: arr[i] > arr[j] and i < jis implemented successfully.
