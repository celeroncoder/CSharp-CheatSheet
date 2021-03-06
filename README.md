# C# CheatSheet

## Create a new Console .NET Application

- **change to the dir** where you want the application.

- Run the command in the terminal :-

  ```
  $dotnet new console
  ```

- To **run** the console app,
  ```
  dotnet run
  ```

## How C# execute a program?

- In the **.cs** file the compiler finds the the line

  ```
  static void Main(string[] args)
  ```

- In the _main block of code_ it will execute **line-by-line**.

- In the end it will **automatically terminate the program**.

## Variables

Variables in C# are _the container to store data_ in the _program_.

### Defining variables in C#

- First, define the **type of data to be stored in the variable**.
- **Name** the variable.

- Now you can initialize the var in the same line,

  ```
  string name = "john doe";
  ```

- Or, you can first **declare the var** and then set the value at some other line.
  ```
  string name;
  name = "john doe";
  ```

## Data types in C#

### Text

- **string** = _plain text_
- **char** = _a single character_ or basically a _string with a single character_

#### handy stuff with Strings

- **\n** = _new line character_

  ```
  Console.WriteLine("First\nSecond");
  ```

- **\\** = to store or print **preserved characters**

  ```
  Console.WriteLine("Giraffe \" Academy");
  ```

- **String Concatenation** = to append any other string to a strings

  ```
  string phrase = "First" + "Second";
  ```

- **String Interpolation** = _using variables in the string without concatenation_
  ```
  Console.WriteLine($"this is a var in the string { phrase } and { var }");
  ```

#### String Methods

- **Length** = to find out how many chars are there in a string

  ```
  string phrase = "This is a phrase.";
  Console.WriteLine(phrase.Length);
  ```

- **Changing Case** = changing the _case of all the char in a string_ to lower or upper case.

  ```
  Console.WriteLine(stringVar.ToUpper());
  Console.WriteLine(stringVar.ToLower());
  ```

- **Contain** = to find that the _string contains a subset of string_, returns a boolean value.

  ```
  Console.WriteLine(phrase.Contains("phrase"))
  ```

- **Indexing Char of String** = to access _a single char in the string_ by putting in the index of the character

  ```
  Console.WriteLine(phrase[0]); // returns the first char of the string phrase.
  ```

- **IndexOf** = tells us _if the string contains a string and the index of it_ if **not present returns -1**

  ```
  Console.WriteLine(phrase.IndexOf("phrase")); // returns the index of the first letter of the string.
  ```

- **Substring** = returns the _substring from the index and how many chars to grab given as params_
  ```
  Console.WriteLine(phrase.Substring(8, 9)) // starts from 8 and returns the 9 char after that.
  ```

### Numbers

- **int** = _integer_

#### Decimal Numbers

- **float** = _less precise_
  ```
  float gpa = 3.1;
  ```
- **double** = _medium precise_
  ```
  double marks = 3.2;
  ```
- **decimal** = _most precise_
  ```
  decimal money = 34.35;
  ```
- If a var is declared as a float, double, decimal it **must contain decimal point**, to define a single number you can use like,
  ```
  double gpa = 3.0;
  ```

#### Finding the remainder

- To find the remainder of the division operation we use **modulus operator (%)**
  ```
  Console.WriteLine(5 % 5); // returns 0 as reminder is zero!
  ```

#### Order of Mathematical Operations

- By _default_ there is a **priority system** like multiplication goes first.

- To **change** the _order of operation_ use **parentheses** as the _operation in the parentheses will execute first_.

- An operation between _two integers will return an integer_.

  ```
  Console.WriteLine(5 / 2); // returns 2 not 2.5
  ```

- Operations _between and integer or a decimal or a decimal and a decimal will return a decimal_.
  ```
  Console.WriteLine(5 / 2.0 ); // returns 2.5
  Console.WriteLine(21.0 / 2) // returns a decimal.
  ```

#### The Math Library

##### In order to get access to higher order mathematical operations we can use the Math library **inbuilt** in C# and calling Methods, some of them are-

- **Abs** - It returns _the absolute value_ of a var or some math number.

  ```
  Console.WriteLine(Math.Abs(-40)); // returns 40
  ```

- **Pow** - Takes two number and _returns the first to the power of the other number_. (also, _works with decimal Numbers_).

  ```
  Console.WriteLine(Math.Pow(3, 2)); // returns 9 as 3 raised to the power of 2 is 9
  ```

- **Sqrt** - Returns the _square root of the number given_.

  ```
  Console.WriteLine(Math.Sqrt(36)); // returns 6
  ```

- **Max** & **Min** - returns _the greatest(**Max**) or the smallest(**min**) number that is passed in it_.

  ```
  Console.WriteLine(Math.Max(4, 90)); // returns 90 as 90 > 4
  ```

- **Round** - returns the _rounded off number_.
  ```
  Console.WriteLine(Math.Round(4.3)); // returns 4
  ```

### Boolean

- **bool** = only have **true** or **false**
  ```
  bool isEmployed = false;
  ```

### Arrays

- It is a data-structure that allows us to store _multiple values in a single container_.

#### Creating an array

- First declare the _type of data_ it is going to hold.

- Then, put an _open and close square brackets_ to let C# know that this going to be an array.

- Give a _name to the array_.

- There are multiple ways you can declare an array the simplest one is to use _open and close curly braces_.

  ```
  int [] arrayOfNum = { 4, 4, 4, 456, 454, 854 };
  ```

- If we don't have values to pass on to the array to _declare an empty array we can use **the constructor function of array** like in the following example by passing how many elements the array will hold beforehand_.
  ```
  string[] arrayOfNumbers = new String[45]; // 45 is the number of elements the array can hold.
  ```

#### Indexing an array

- To gain access to _individual element of an array_ we use _indexing_

  ```
  Console.WriteLine(myArray[0]); // returns the first element
  ```

- the **indexing starts with 0**.

### Constant

- **not a var type** just using data without any declaration like
  ```
  Console.WriteLine("string");
  Console.WriteLine(true);
  ```

## User Input

### Getting user input in a ConsoleApp

- **Console.ReadLine** - Get the _user input **string** into the console_.

  ```
  string userInput = Console.ReadLine();
  Console.WriteLine(userInput);
  ```

- anything passed in the ReadLine method is a _type of string_.

- **Converting** _string to a number_ using **Convert** library's **ToInt32** method, it has to be a number.

  ```
  int num = Convert.ToInt32("34");
  ```

- **Converting** _string to a decimal_ using Convert Library **ToDouble method**.
  ```
  double number = Convert.ToDouble("4.56"); // also takes int as an argument
  ```

## Logging

- **Console.Write** - writes the line given in the parentheses but don't changes the line.

- **Console.WiteLine** - writes the line passed into the parentheses and _takes or use the whole line_ and takes to a _new line_.

## .gitignore

- to _create a .gitignore for .NET application go to the terminal in the project dir and type the command_
  ```
  dotnet new gitignore
  ```
