# Pattern
## Aim:
Develop a C# program to print Pascal's Triangle.

## Algorithm:
## STEP 1: 
Create the class and assign the number of rows to be as 5. <br>
## STEP 2:
Run the outer for loop n times. <br>
## STEP 3:
The first inner for loop should print the spaces first. <br>
## STEP 4: 
The second inner for loop should print number using the combination formula. <br>
## STEP 5: 
Display the Results. <br>

## Program:
```cs

using System;
namespace Pattern{
  class Program {

      public int factorial(int i)
      {
          if (i == 0)
              return 1;
          return i * factorial(i - 1);
      }
      public static void Main(string[] args)
      {
          int n = 5, i, j;
          Program g = new Program();
          for (i = 0; i <= n; i++) {
              for (j = 0; j <= n - i; j++) {
                   Console.Write(" ");
              }
              for (j = 0; j <= i; j++) {

                  // nCr formula
                  Console.Write(" " + g.factorial(i) / (g.factorial(i - j) * g.factorial(j)));
              }

              Console.WriteLine();
          }
     }
  }
}
```
## Output:
![cs](https://user-images.githubusercontent.com/75234646/189409355-16f46483-b838-4f34-8093-40b8195763e5.PNG)

## Result:
Thus the C# program to print the first 5 rows in a Pascal's traingle has been implemented successfully.
