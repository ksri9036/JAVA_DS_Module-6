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

# Ex4 You are given a Java program that performs matrix addition. If Matrix A has all odd numbers and Matrix B has all even numbers of the same dimension, what will be the nature (even/odd/mixed) of the resulting matrix?
## DATE: 16-11-25
## AIM:
To write a java function to evaluate weather the given Matrix A has all odd numbers and Matrix B has all even numbers of the same dimension and find the nature of resultant matrrix.

## Algorithm
1.Read Matrix A and Matrix B.

2.Check if every element in Matrix A is odd.

3.Check if every element in Matrix B is even.

4.If A is all odd and B is all even → the result matrix will have all odd numbers.

5.Otherwise → the result matrix will be mixed.
  

## Program:
```
/*
Program to ind the nature of resultant matrrix.
Developed by: VIMALA SAHANA W
RegisterNumber: 212223040241 
*/
import java.util.Scanner;

public class MatrixAddition {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        int rows, cols;

       
        rows = sc.nextInt();
        cols = sc.nextInt();

        int[][] A = new int[rows][cols];
        int[][] B = new int[rows][cols];
        int[][] sum = new int[rows][cols];

        
        for (int i = 0; i < rows; i++)
            for (int j = 0; j < cols; j++)
                A[i][j] = sc.nextInt();

        
        for (int i = 0; i < rows; i++)
            for (int j = 0; j < cols; j++)
                B[i][j] = sc.nextInt();

        for (int i = 0; i < rows; i++)
            for (int j = 0; j < cols; j++)
                sum[i][j] = A[i][j] + B[i][j];

        
        for (int i = 0; i < rows; i++) {
            for (int j = 0; j < cols; j++)
                System.out.print(sum[i][j] + " ");
            System.out.println();
        }
        sc.close();
    }
}

```

## Output:

<img width="831" height="654" alt="image" src="https://github.com/user-attachments/assets/91838513-df70-4b73-af5a-c482e43e6d57" />


## Result:
Thus, the java program to evaluate weather the given Matrix A has all odd numbers and Matrix B has all even numbers of the same dimension and find the nature of resultant matrrix is implemented successfully.

