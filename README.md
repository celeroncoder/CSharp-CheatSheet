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

### Boolean

- **bool** = only have **true** or **false**
  ```
  bool isEmployed = false;
  ```

### Constant

- **not a var type** just using data without any declaration like
  ```
  Console.WriteLine("string");
  Console.WriteLine(true);
  ```

## .gitignore

- to _create a .gitignore for .NET application go to the terminal in the project dir and type the command_
  ```
  dotnet new gitignore
  ```
