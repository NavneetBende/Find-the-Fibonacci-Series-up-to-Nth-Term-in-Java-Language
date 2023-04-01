# Find-the-Fibonacci-Series-up-to-Nth-Term-in-Java-Language

Given an integer input for the Nth value, the objective is to Find the Fibonacci Series up to the Nth term using Loops and recursion in Java Language. To do so we’ll use the following methods,

Method 1: Using Iteration
Method 2: Using Recursion
Method 3: Using Formula
We’ll discuss the above mentioned methods in detail in the upcoming sections. For better understanding, checkout the section below.

Fibonacci Series
A series of numbers in which each number is the sum of the two preceding numbers is known as a Fibonacci Series.

General Formula to find the Nth term of a Series 
F0 = 0 and F1 = 1 be the seed values
The Nth term of a Fibonacci series is given as Fn = Fn-1 + Fn-2 .
Example, 
Input : 5
Fibonacci Series : 0 1 1 2 3
Explanation:
For 3rd term it's 2nd term + 1st term.
For 4th term it's 3rd term + 2nd term.
for 5th term it's 4th term + 3rd term.
×Dismiss alert
Method 1: Using Iteration
Java Code
Run
public class Main
 {
   public static void main (String[]args)
   {

     int num = 15;
     int a = 0, b = 1;

     // Here we are printing 0th and 1st terms
       System.out.print (a + " , " + b + " , ");

     int nextTerm;

     // printing the rest of the terms here
     for (int i = 2; i < num; i++)
       {
      nextTerm = a + b;
      a = b;
          b = nextTerm;
          System.out.print (nextTerm + " , ");
       }


   }
 }
Output
0 , 1 , 1 , 2 , 3 , 5 , 8 , 13 , 21 , 34 , 55 , 89 , 144 , 233 , 377
Related Pages
Armstrong number

Armstrong number in a given range

Fibonacci Series upto nth term 

Find the Nth Term of the Fibonacci Series

Factorial of a number

Power of a number

Method 2: Using Recursion
Java Code
Run
Run
public class Main
 {
   static int a = 0, b = 1, nextTerm;
   public static void main (String[]args)
   {

     int n = 15;
     // Here we are printing 0th and 1st terms
       System.out.print (a + " , " + b + " , ");

     // n-2 as 2 terms already printed
       Fib (n - 2);
   }

   static int Fib (int n)
   {
     if (n > 0)
       {
      nextTerm = a + b;
      a = b;
      b = nextTerm;

      System.out.print (nextTerm + " , ");
      Fib (n - 1);
       }
     return 0;

   }

 }
Output
0 , 1 , 1 , 2 , 3 , 5 , 8 , 13 , 21 , 34 , 55 , 89 , 144 , 233 , 377
Method 3: Using Formula
Java Code
Run
public class Main
{
  static int a = 0, b = 1, nextTerm;
  public static void main (String[]args)
  {

    int n = 15;

      fib (n);
  }

  static void fib (int n)
  {

    int f[] = new int[n + 1];

    f[0] = 0;
    f[1] = 1;

    System.out.print (f[0] + " , " + f[1] + " , ");

    for (int i = 2; i < n; i++)
      {
	    f[i] = f[i - 1] + f[i - 2];
    	System.out.print (f[i] + " , ");
      }
  }

}
Output
0 , 1 , 1 , 2 , 3 , 5 , 8 , 13 , 21 , 34 , 55 , 89 , 144 , 233 , 377
Prime Course Trailer

Related Banners
Get PrepInsta Prime & get Access to all 200+ courses offered by PrepInsta in One Subscription

Get Prime
