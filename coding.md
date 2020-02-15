---
title: Coding Standards
nav: coding
---

# C# Program Coding Standards: Projects and Exercises

These are the coding standards we’ll use in IGME 106.
Take the time to read through this, and refer to it whenever you’re unsure of a particular syntax standard.

## Homework Submissions:

-   I expect that any work submitted for grading has been tested fully.
    -   A significant number of points may be lost if your program does not run as intended.
-   Every homework assignment is required to be an **individual** effort. Group efforts are forbidden on homework assignments.
    -   This includes showing someone else your code for the purposes of using the same code base.  This also includes working with others on your program, or sharing your code with others.
    -   Collaborating with others is a violation of our Academic Integrity policy and, as such, may harbor consequences.

## Data Types:

-   Data types must be explicitly declared.  The use of `var` is unacceptable in this course.

## Naming and Case Conventions:

-   Names used for classes, methods and variables are expected to be meaningful.  Loop control variables (like `i` or `x`) can be a single letter.
```csharp
double interestRate;
for(int i = 0; i < 4; i++)
```

-   Variable names start with lowercase letters and utilize camelCase.
```csharp
float speed;
int colliderWidth;
Vector3 velocity;
Vehicle redCar;
```

-   Do not use name multiple times in the same scope, differing only in case:

      `number` vs. `Number` vs. `NUMBER`

-   Multiple classes can use the same name for a class field.

     `class Animal` and `class Car` can both contain a field called `name`

-   Class names are **always** capitalized.  If the name has multiple words, each word is capitalized using UpperCamelCase.
```csharp
class Vehicle { … }
class EnemyShip { … }
```

-   Method names **always** start in uppercase.  If the name has multiple words, each word is capitalized using UpperCamelCase.
```csharp
double CalculateInterest() { … }
bool DetermineCollision() { … }
```

-   Constant names should start with an uppercase letter.
```csharp
const int DaysInWeek = 7;
```

## Comments:

-   You are expected to comment your code. Some percentage of each project’s grade may be based on the comments provided.

-   Each **class** should have a comment block (called a “class header” comment) associated with it.  These headers will contain the following information:

    -   Author (_you!_)
    -   Purpose of the class
    -   Restrictions on the usage or known errors

-   Each **method** should have a comment block (called a “method/function header” comment) associated with it.  You may want to use the magical triple-slash comments. These headers will contain the following information:

    -   Purpose of the method
    -   Restrictions on the usage or known errors
    -   Other appropriate sections, like parameters or return values

-   Comment sections of code where you are doing something clever, unusual or where you are making use of some obscure feature.

-   Don’t comment the obvious unless specifying intent:

    -   Useless Comment:
    ```csharp
    Debug.Log("");  // Prints blank line  (duh!)
    ```
    -   Better Comment
    ```csharp
    Debug.Log("");  // Improve output & input spacing
    ```

## Code Statements:

-   Only one variable declaration per line.

    -   _Good example:_
    ```csharp
    int characterWidth;
    int characterHeight;
    ```

    -   _Unacceptable example:_
    ```csharp
    int characterWidth, characterHeight, speed;
    ```

-   Only one code statement per line.
    -   _Good example:_
    ```csharp
    if(alive)
    {
            shipSpeed += 0.2;
    }
    ```

    -   _Unacceptable example:_
    ```csharp
    if(true) Console.WriteLine("this is true");
    ```

-   Use indentation and curly brackets to indicate the scope of functions and various control structure, like loops, and if statements.
    -   _Good example:_
    ```csharp
    for(int x = 200; x > 10; x = x - 20)
    {
            Console.WriteLine ("x is " + x);
    }
    ```

    -   _Unacceptable examples:_
    ```csharp
    for(int x = 200; x > 10; x = x - 20)
    {
            Console.WriteLine ("x is " + x);
    }
    ```
