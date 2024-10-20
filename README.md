<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=>, initial-scale=1.0">
    <title>Document</title>
</head>
<body>
    <p>
        1A)Create an application that obtains four int values from the
user and displays the product.

using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
namespace ConsoleApplication1
{
class Program
{
static void Main(string[] args)
{
int num1, num2, num3, num4, prod;
Console.Write("Enter number 1: ");
num1 = Int32.Parse(Console.ReadLine());
Console.Write("Enter number 2: ");
num2 = Convert.ToInt32(Console.ReadLine());
Console.Write("Enter number 3: ");
num3 = Convert.ToInt32(Console.ReadLine());
Console.Write("Enter number 4: ");
num4 = Convert.ToInt32(Console.ReadLine());
prod = num1 * num2 * num3 * num4;
Console.WriteLine(num1 + "*" + num2 + "*" + num3 + "*" + num4 +
"=" + prod);
Console.ReadKey();
}
}
}

1B)

using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;

namespace ConsoleApp1
{

    internal class Program
    {
        static void Main(string[] args)
        {
            Console.WriteLine("Enter String ");
            string s = Console.ReadLine();
            Console.WriteLine(s.ToUpper());
            Console.WriteLine(s.ToLower());
            Console.WriteLine(s.Contains("More"));
            Console.WriteLine(s.Length);
            Console.WriteLine(s.TrimStart().Length);
            Console.WriteLine(s.TrimEnd().Length);
            Console.WriteLine(s.Trim().Length);
            Console.ReadKey();

        }
    }
}

C) Create an application that receives the (Student Id, Student Name, Course Name, Date of Birth) information from a set of students.  The application should also display the information of all the students once the data entered.
using System;
namespace ArrayOfStructs
{
    class Program
    {
        struct Student
        {
            public string studid, name, cname;
            public int day, month, year;
        }
        static void Main(string[] args)
        {
            Student[] s = new Student[5];
            int i;
            for (i = 0; i < 5; i++)
            {
                Console.Write("Enter Student Id:");
                s[i].studid = Console.ReadLine();
                Console.Write("Enter Student name : ");
                s[i].name = Console.ReadLine();
                Console.Write("Enter Course name : ");
                s[i].cname = Console.ReadLine();
                Console.Write("Enter date of birth\n Enter day(1-31):");
                s[i].day = Convert.ToInt32(Console.ReadLine());
                Console.Write("Enter month(1-12):");
                s[i].month = Convert.ToInt32(Console.ReadLine());
                Console.Write("Enter year:");
                s[i].year = Convert.ToInt32(Console.ReadLine());
            }
            Console.WriteLine("\n\nStudent's List\n");
            for (i = 0; i < 5; i++)
            {
                Console.WriteLine("\nStudent ID : " + s[i].studid);
                Console.WriteLine("\nStudent name : " + s[i].name);
                Console.WriteLine("\nCourse name : " + s[i].cname);
                Console.WriteLine("\nDate of birth(dd-mm-yy) : " + s[i].day + "-" + s[i].month +
                "-" + s[i].year);
            }
        }
    }
}

D) Create an application to demonstrate following operations
[i] Fibonacci Series

using System;

namespace ConsoleApplication3
{
    class Program
    {
        static void Main(string[] args)
        {
            int num1 = 0, num2 = 1, num3, num, counter;

            Console.Write("Upto how many numbers do you want in the Fibonacci series: ");
            num = int.Parse(Console.ReadLine());

            if (num <= 0)
            {
                Console.WriteLine("Please enter a positive integer.");
                return;
            }

            if (num == 1)
            {
                Console.WriteLine(num1);
                return;
            }

            // Print the first two numbers
            Console.Write(num1 + "\t" + num2);

            counter = 2; // We have already printed the first two numbers

            while (counter < num)
            {
                num3 = num1 + num2;
                Console.Write("\t" + num3);
                num1 = num2;
                num2 = num3;
                counter++;
            }

            // Wait for user input before closing
            Console.WriteLine();
            Console.WriteLine("Press any key to exit...");
            Console.ReadKey();
        }
    }
}

[ii] Test for prime numbers.
using System;

namespace testprime
{
    class Program
    {
        static void Main(string[] args)
        {
            int num;
            bool isPrime = true;

            Console.Write("Enter a number: ");
            num = int.Parse(Console.ReadLine());

            // Handle edge cases
            if (num <= 1)
            {
                Console.WriteLine(num + " is neither prime nor composite");
                return;
            }

            // Check for factors from 2 up to the square root of num
            for (int counter = 2; counter <= Math.Sqrt(num); counter++)
            {
                if (num % counter == 0)
                {
                    isPrime = false;
                    break;
                }
            }

            if (isPrime)
            {
                Console.WriteLine(num + " is a prime number");
            }
            else
            {
                Console.WriteLine(num + " is not a prime number");
            }

            // Optional: Wait for user input before closing
            Console.WriteLine("Press any key to exit...");
            Console.ReadKey();
        }
    }
}
[iii] Test for vowels.
using System;
namespace vowels
{
    class Program
    {
        static void Main(string[] args)
        {
            char ch;
            Console.Write("Enter a character : ");
            ch = (char)Console.Read();
            switch (ch)
            {
                case 'a':
                case 'A':
                case 'e':
                case 'E':
                case 'i':
                case 'I':
                case 'o':
                case 'O':
                case 'u':
                case 'U':
                    Console.WriteLine(ch + "is vowel");
                    break;
                default:
                    Console.Write(ch + "is not a vowel");
                    break;
            }
            Console.ReadKey();
        }
    }
}

[iv]Use of foreach loop with arrays.
using System;

namespace ForeachLoopDemo
{
    class Program
    {
        static void Main(string[] args)
        {
            // Create an array of strings
            string[] fruits = { "Apple", "Banana", "Cherry", "Date", "Elderberry" };

            // Use foreach loop to iterate over the array
            Console.WriteLine("List of fruits:");
            foreach (string fruit in fruits)
            {
                Console.WriteLine(fruit);
            }

            // Keep the console window open
            Console.WriteLine("\nPress any key to exit...");
            Console.ReadKey();
        }
    }
}

[v] Reverse a number and find sum of digits of a number.

using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
namespace std
{
class Program
{
static void Main(string[] args)
{
int num,actualnumber,revnum=0,digit,sumDigits=0;
Console.Write("Enter number:");
num = int.Parse(Console.ReadLine());
actualnumber = num;
while (num > 0)
{
digit = num % 10;
revnum = revnum * 10 + digit;
sumDigits=sumDigits+digit;
num = num / 10;
}
Console.WriteLine("Reverse of " + actualnumber + "=" + revnum);
Console.WriteLine("Sum of its digits:" + sumDigits);}}}

2A) Create simple application to perform following operations.
[i] Finding Factorial Value

using System.Collections.Generic;
using System.Linq;
using System.Text;
using System;

namespace factorial
{
    class Program
    {
        static void Main(string[] args)
        {
            int i, number, fact;
            Console.WriteLine("Enter the Number");
            number = int.Parse(Console.ReadLine());
            fact = number;
            for (i = number - 1; i >= 1; i--)
            {
                fact = fact * i;
            }
            Console.WriteLine("\nFactorial of Given Number is: " + fact);
            Console.ReadLine();

        }
    }
}




[ii] Money Conversion
[iii] Quadratic Equation
using System;

namespace example
{
    class Quadraticroots
    {
        double a, b, c;

        public void read()
        {
            Console.WriteLine(" \n To find the roots of a quadratic equation of the form a*x*x + b*x + c = 0");
            Console.Write("\n Enter value for a : ");
            a = double.Parse(Console.ReadLine());
            Console.Write("\n Enter value for b : ");
            b = double.Parse(Console.ReadLine());
            Console.Write("\n Enter value for c : ");
            c = double.Parse(Console.ReadLine());
        }
        public void compute()
        {
            int m;
            double r1, r2, d1;
            d1 = b * b - 4 * a * c;
            if (a == 0)
                m = 1;
            else if (d1 > 0)
                m = 2;
            else if (d1 == 0)
                m = 3;
            else
                m = 4;
            switch (m)
            {
                case 1: Console.WriteLine("\n Not a Quadratic equation, Linear equation");
                    Console.ReadLine();
                    break;
                case 2: Console.WriteLine("\n Roots are Real and Distinct");
                    r1 = (-b + Math.Sqrt(d1)) / (2 * a);
                    r2 = (-b - Math.Sqrt(d1)) / (2 * a);
                    Console.WriteLine("\n First root is {0:#.##}", r1);
                    Console.WriteLine("\n Second root is {0:#.##}", r2);
                    Console.ReadLine();
                    break;
                case 3: Console.WriteLine("\n Roots are Real and Equal");
                    r1 = r2 = (-b) / (2 * a);
                    Console.WriteLine("\n First root is {0:#.##}", r1);
                    Console.WriteLine("\n Second root is {0:#.##}", r2);
                    Console.ReadLine();
                    break;
                case 4: Console.WriteLine("\n Roots are Imaginary");
                    r1 = (-b) / (2 * a);
                    r2 = Math.Sqrt(-d1) / (2 * a);
                    Console.WriteLine("\n First root is {0:#.##} + i {1:#.##}", r1, r2);
                    Console.WriteLine("\n Second root is {0:#.##} - i {1:#.##}", r1, r2);
                    Console.ReadLine();
                    break;
            }
        }
    }

    class Roots
    {
        public static void Main()
        {
            Quadraticroots qr = new Quadraticroots();
            qr.read();
            qr.compute();
        }
    }
}

[iv] Temperature Conversion

using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;

namespace temperatureconversion
{
    class Program
    {
        static void Main(string[] args)
        {
            int celsius, faren;
            Console.WriteLine("Enter the Temperature in Celsius(°C) : ");
            celsius = int.Parse(Console.ReadLine());
            faren = (celsius * 9) / 5 + 32;
            Console.WriteLine("0Temperature in Fahrenheit is(°F) : " + faren);
            Console.ReadLine();
        }
    }
}

2B)	Create simple application to demonstrate use of following concepts.

[i] Function Overloading

using System;
namespace swap
{
class Overloading
{
public void swap(ref int n, ref int m)
{
int t;
t = n;
n = m;
m = t;
}
public void swap(ref float f1, ref float f2)
{
float f;
f = f1;
f1 = f2;
f2 = f;
}
}
class program
{
static void Main(string[] args)
{
Overloading objOverloading = new Overloading();
int n = 10, m = 20;
objOverloading.swap(ref n, ref m);
Console.WriteLine("N=" + n + "\tM=" + m);
float f1 = 10.5f, f2 = 20.6f;
objOverloading.swap(ref f1, ref f2);
Console.WriteLine("F1=" + f1 + "\tF2=" + f2);
}
 } 
}

Heirarchical Inheritance
using System;

namespace HeirarchicalInheritance
{
    class Employee
    {
        public virtual void Display()
        {
            Console.WriteLine("Display of Employee class called");
        }
    }

    class Programmer : Employee
    {
        public override void Display()
        {
            Console.WriteLine("Display of Programmer class called");
        }
    }

    class Manager : Employee
    {
        public override void Display()
        {
            Console.WriteLine("Display of Manager class called");
        }
    }

    class Program
    {
        static void Main(string[] args)
        {
            Console.Write("Whose details do you want to see? \n 1. Programmer \n 2. Manager\n");
            int choice = int.Parse(Console.ReadLine());

            if (choice == 1)
            {
                Programmer objProgrammer = new Programmer();
                objProgrammer.Display();
            }
            else if (choice == 2)
            {
                Manager objManager = new Manager();
                objManager.Display();
            }
            else
            {
                Console.WriteLine("Wrong choice entered");
            }

            Console.ReadLine();
        }
    }
}




Single Inheritance:
using System;
public class Animal
{

    public void eat() { Console.WriteLine("Eating..."); }
}
public class Dog : Animal
{
    public void bark() { Console.WriteLine("Barking..."); }
}
class TestInheritance2
{
    public static void Main(string[] args)
    {
        Dog d1 = new Dog();
        d1.eat();
        d1.bark();
        Console.ReadLine();
    
    }
  
}



    </p>
</body>
</html>
