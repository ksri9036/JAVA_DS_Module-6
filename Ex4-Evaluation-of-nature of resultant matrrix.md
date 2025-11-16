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
