### Output in C Programming: Displaying Text
#### Understanding Output in C
 - When we talk about output in C, we mean displaying text or results on the console of your device. To achieve this, we use the `printf` function. Think of `printf` as your way to communicate with the user through messages or results.
- Key Rule:
  - Whenever you want to print text, it must be enclosed within double quotation marks `""`.
  - Example:
    ```c
    printf("Welcome to C programming!"); // Text wrapped in double quotes
    ```
  - Output:
    ```
    Welcome to C programming!
    ```
- Common Mistake is to forget the Double Quotes.
- If you forget to enclose your text in double quotes, you’ll get an error:
  ```
  printf("This line works!"); //This is correct
  printf(This line will cause an error.); // Missing double quotes
  ```
### Multiple Outputs in a Single Program
- You can use as many printf() statements as you want.
- But note that it won’t automatically add a new line between outputs unless you specifically tell it to do so.
- Example:
  ```
  printf("Welcome to C programming!");
  printf("Let's learn step-by-step.");
  printf("Keep coding!");
  ```
- Output:
  ```
  Welcome to C programming!Let's learn step-by-step.Keep coding!
  ```
- To solve this add a newline using `\n`.
  - The newline character (`\n`) is known as an escape sequence.
  - It moves the cursor to the beginning of the next line on the screen, creating a new line.
- Updated previous example:
  ```
  printf("Welcome to C programming!\n");
  printf("Let's learn step-by-step.\n");
  printf("Keep coding!\n");
  ```
- Output:
  ```
  Welcome to C programming!
  Let's learn step-by-step.
  Keep coding!
  ```
- Above three lines can be printed using single `printf`.
  - Example:
    ```
    printf("Welcome to C programming!\nLet's learn step-by-step.\nKeep coding!\n");
    ```
  - Output (same as previous):
    ```
    Welcome to C programming!
    Let's learn step-by-step.
    Keep coding!
    ```
- Other Common Escape Sequences
  - `\t` ---- Creates a horizontal tab
  - `\\` ---- Inserts a backslash character
  - `\”` ---- Inserts a double quote
- Example using Escape Sequences
  ```c
  printf("Hello\tWorld!\n"); // Inserts a tab between words
  printf("Backslash: \\\n"); // Prints a single backslash
  printf("He said, \"Keep learning!\"\n"); // Prints quotes
  ```
- Output:
  ```
  Hello World! Backslash: \
  He said, "Keep learning!"
  ```

### Comments
- Comments are like notes in your code that help you explain what’s going on.
- They make the code easier to read and understand.
- You can also use comments to temporarily disable code while testing something new.
- Think of them as little reminders or explanations that only you or other programmers can see.
- In C, comments can be single-line or multi-line. Let’s explore both!
  - #### Single-Line Comments
    - Start with two forward slashes (`//`).
    - Everything that comes after these slashes, until the end of the line, will be ignored by the compiler. 
    - This means it won’t be executed as part of your program.
    - Example: Single-Line Comment before a line  & at the End of a Line
      ```
      // This line of code displays a greeting message 
      printf("Hello, C Programmers!");
      printf("Welcome to C!"); // This prints a Welcome to C!
      ```
    - Here, the compiler ignores everything after the `//`, so it only prints the message.
  - #### Multi-Line Comments
    - Start with `/*` and end with `*/`.
    - This is useful for adding longer explanations or multiple lines of comments.
    - Example: Multi-Line Comment
      ```      
      /*for all beginner programmers in C.
      Keep up the great work! */
      printf("You are doing great! Keep it up!");
      ```
    - Output:
      ```
      You are doing great! Keep it up!
      ```
    - In this case, everything between `/*` and `*/` is ignored by the compiler.
    - You can write as many lines of comments as you need between them.
- When to Use Single-Line vs. Multi-Line Comments?
  - It’s really up to you!
  - Generally, we use `//` for short comments and `/* */` for longer explanations.

# Variables and Keywords

### Introduction to Variables
- Variables are like containers that hold data values, such as numbers, characters.
- They allow you to store information in your programs.
- Think of them as labeled boxes where you can store information that your program needs to remember.

### Declaring and Initializing Variables
- When you declare a variable, you’re telling the computer, “I want to reserve space in memory for this type of data.”
- The basic syntax is:
  - Syntax:
    ```
    type variableName = value;
    ```
  - `type`: Defines the kind of data the variable will hold (like `int` for whole numbers, `float` for decimal numbers, and `char` for characters).
  - `variableName`: The name of the variable, which should follow naming rules.
- Examples:
  - Declaring and assigning a value immediately:
    ```
    int age = 21; // Declares an integer variable and assigns a value of 21
    ```
  - Declaring first and assigning a value later:
    ```
    int age; // Declares the variable
    age = 21; // Assigns a value later
    ```
  - Explanation
    - Declaring a variable without assigning a value is like setting up an empty container.
    - Assigning a value fills it with data.
  
### Types of Variables in C
- C programming offers different types of variables based on the data you want to store.
- Here are the most common ones:
  - `int`: For storing whole numbers, like 100, -45, or 0.
  - Example:
    ```
    int score = 85; // Stores the whole number 85
    ```
  - `float`: For storing numbers with decimals, like 3.14 or -2.71.
  - Example:
    ```
    float price = 4.99; // Stores the decimal number 4.99
    ```
  - `char`: For storing single characters like 'A', 'b', or '5'.
  - Example:
    ```
    char grade = 'A'; // Stores the character 'A'
    ```
  
### Naming Rules for Variables (Identifiers)
- In C programming, the names you choose for your variables are known as identifiers.
- Here's what you need to know:
  - Variable names should start with a letter (lowercase or uppercase) or an underscore _.
    - Example:
      ```
      int age; // Correct
      int _score; // Correct
      int 3rdValue; // Incorrect - starts with a number
      ```
  - Identifiers are case-sensitive, meaning variables named `Age` and `age` are treated as different.
    - Example:
      ```
      int Age = 21; // Correct
      int age = 18; // Correct but different from 'Age'
      ```
  - No Special Characters or Spaces
    - Avoid using special characters like #, !, @, &, or spaces. Stick to letters, digits, and underscores.
    - Example:
      ```
      int first_name; // Correct
      int first-name; // Incorrect - contains a dash
      ```
  - Avoid Using Reserved Keywords
      - Some words are reserved for special purposes in C, such as `int`, `char`, and `float`, `case`.
      - You cannot use them as variable names.
      - Example:
        ```
        int return; // Incorrect - 'return' is a reserved keyword
        int num; // Correct
        ```
    
### Format Specifiers in C
- Format specifiers are special characters used with the `printf()` function to specify the type of data you want to print.
- They act like placeholders to inform the compiler what type of data it should expect.
  - `%d`: For printing integers.
  - `%f`: For printing floating-point numbers (decimals).
  - `%c`: For printing characters.
  - `%s`: For printing strings (text).

### Outputting Variables in C
- You can print variable values using the `printf()` function with appropriate format specifiers:
- Example:
  ```
  int score = 85;
  char grade = 'B';
  printf("Score: %d, Grade: %c", score, grade); // Outputs: Score: 85, Grade: B
  ```
- Printing Values Without Variables
  - You can print values directly without storing them in variables, as long as you use the correct format specifier:
  - Example:
    ```    
    printf("My lucky number is: %d", 25); // Outputs: My lucky number is: 25
    printf("My favorite letter is: %c", 'M'); // Outputs: My favorite letter is: M
    ```

### Declare Multiple Variables
- Sometimes, you may want to create several variables of the same type at once.
- Instead of writing multiple lines, you can declare them in a single line using a comma-separated list:
  - Example:
    ```
    int x = 20, y=8, z=60;
    printf("%d", x + y + z); 
    ```
- Assign the Same Value to Multiple Variables
  - You can also assign the same value to multiple variables of the same type in one line.
  - This is useful when you want several variables to start with an identical value.
  - Example:
    ```
    int x, y, z;
    x = y = z = 100;
    printf("%d", x + y + z);
    ```

### Assiging and updating values
- Changing Variable Values
  - Example:
    ```  
    int score = 90; // Initially, the score is 90
    printf("Score=%d\n", score);
    score = 95; // Now, the score is updated to 95
    printf("New Score=%d", score);
    ```
- Assigning One Variable's Value to Another
  - Example:
    ```
    int points = 30;
    int bonus = 50;
    points = bonus; // Now, points holds the value 50
    printf("%d", points); // Outputs: 50
    ```

## Keywords
- Keywords are special words in the C programming language that have specific meanings.
- You can think of them as building blocks that help you create your programs.
- Since these words are reserved for special purposes, you cannot use them as names for your own variables or functions.
- Keywords help the computer understand what you want to do in your program.
- For example, they can tell the computer about the type of data you’re working with, how to make decisions, and how to repeat actions.
- Here are some important things to know about keywords:
  - Reserved Words
    - You can’t use keywords as names for your variables or functions.
    - For instance, you can't name a variable `int` or `return`.
  - Predefined Meaning
    - Each keyword has a fixed meaning that the computer understands.
    - You cannot change what a keyword does.
  - Case Sensitivity
    - Keywords are case-sensitive, meaning that `Int` and `int` are different.
    - Only the correct lowercase spelling works as a keyword.
- Few common keywords are: `int`, `float`, `double`, `if`, `else`, `char`, `return`, `case`, `default` etc
- Understanding keywords is important because they help you write clear and correct C programs. 

## Data Types
- In C programming, every variable must have a specific data type. 
- This data type tells the program what kind of value the variable can hold.
- For example, it could be a whole number, a number with decimals, or a single character.
- Understanding data types is important because it helps the program use memory efficiently and perform calculations correctly.

- ### Basic Data Types
  - Here are the most common data types you will encounter in C programming:
  - `int`
    - Size: 2 or 4 bytes
    - Format specifier: `%d` or `%i`
    - Exampel: 1, 100, -25
  - `float`
    - Size: 4 bytes,
    - Format specifier: %f or %F
    - Example: 1.99, 3.14
  - `double`
    - Size: 8 bytes
    - Stores fractional numbers with one or more decimals, capable of holding up to 15 decimal digits.
    - Format specifier: %lf
    - Example: 1.99999999999999, 2.71828
  - `char`
    - Size: 1 byte
    - Used for storing a single character or symbol. This includes letters, numbers, and other symbols.
    - Format specifier: `%c`
    - Exampel: 'A', '1', '#'

### Working with Numeric Types in C
- In C programming, you will often need to store numbers in variables.
- Depending on whether you want to store whole numbers or decimal values, you have different options like `int`, `float`, and `double`.
- Storing Whole Numbers: int Type
  - Use the int type when you need to store a whole number without decimals, such as 25 or 500.
  - Example:
  ```
  int age = 25;
  printf("%d", age); // Output: 25
  ```
- Storing Decimal Numbers: `float` and `double` Types
  - When working with decimal numbers, C offers two main types: `float` and `double`.
  - A float can store up to 6-7 decimal digits, while a double provides a higher precision of around 15 decimal digits.
  - Example:
    ```    
    float price = 4.99;
    double largeValue = 123456789.123456;
    printf("%f\n", price); // Output: 4.990000
    printf("%lf", largeValue); // Output: 123456789.123456
    ```
- Controlling Decimal Precision in Output
  - By default, printing a floating-point number will display up to 6 decimal places.
  - You can control this by using a dot (.) followed by a number that specifies how many digits to display after the decimal point.
  - Example:
    ```  
    float temperature = 36.5;
    printf("%f\n", temperature); // Output: 36.500000 (Default)
    printf("%.1f\n", temperature); // Output: 36.5 (1 decimal place)
    printf("%.2f\n", temperature); // Output: 36.50 (2 decimal places)
    printf("%.4f", temperature); // Output: 36.5000 (4 decimal places)
    ```
- Scientific Notation in C
  - C allows you to use scientific notation to represent large or small floating-point numbers.
  - This notation uses an `e` or `E` to indicate the power of 10.
  - Example:
    ```    
    float largeNumber = 3.5e2; // Equivalent to 3.5 * 10^2 (350)
    double smallNumber = 1.2E-3; // Equivalent to 1.2 * 10^-3 (0.0012)
    printf("%f\n", largeNumber); // Output: 350.000000
    printf("%lf", smallNumber); // Output: 0.001200
    ```
- Handling Characters in C
  - The `char` Type for Single Characters.
  - The `char` data type is used to store a single character, such as a letter, number, or symbol.
  - You must enclose the character in single quotes.
  - Example:
    ```
    char grade = 'B';
    printf("%c", grade); // Output: B
    ```
- Using ASCII Values with char
  - You can also use ASCII values directly to represent characters.
  - ASCII (American Standard Code for Information Interchange) is a coding system that represents characters with numerical values.
  - Remember that ASCII values are just numbers, so you don’t need to use quotes around them.
  - Example:
    ```
    char firstLetter = 65; // ASCII value for 'A'
    char secondLetter = 66; // ASCII value for 'B'
    char thirdLetter = 67; // ASCII value for 'C'
    printf("%c", firstLetter); // Output: A
    printf("%c", secondLetter); // Output: B
    printf("%c", thirdLetter); // Output: C
    ```
- Limitations of the `char` Type
  - A `char` variable is intended to hold a single character, which occupies exactly 1 byte of memory.
  - If you try to store more than one character, it will only keep the last character.
  - Example:
    ```
    char myChar = 'Hello'; // Incorrect: only the last character 'o' is stored
    printf("%c", myChar); // Output: o
    ```
- Overcoming the Limitation of char with Strings
  - To store more than a single character or entire words, you should use strings instead of the char data type.
  - In C, strings are represented as arrays of characters, and they must be enclosed in double quotes.
  - Example:
    ```
    char greeting[] = "Welcome"; // Correct way to define a string
    printf("%s", greeting); // Output: Welcome
    ```
  - This way, you can store and handle multiple characters or words efficiently without facing the limitations of the `char` type. 
  - We will learn more about strings and how to work with them in a later section.

### Type Conversion in C
- In programming, sometimes we need to change a variable’s type from one to another.
- This is called type conversion. Let’s explore how this works in C.
- For example, if you divide two whole numbers like 7 and 3, you might expect a result like 2.33. However, since these numbers are integers, the output will only show 2.
- Example:
  ```  
  int a = 7;
  int b = 3;
  int result = a / b;
  printf("%d", result); // Outputs: 2
  ```
- There are two types of conversion in C:
  - **Implicit Conversion**
    - Done automatically by the compiler.
    - If you assign an integer to a float, the compiler will automatically convert it to a float.
    - Example:
    ```
    float myFloat = 8; // Automatically converts to 8.000000
    printf("%f", myFloat); // 8.000000
    int myInt = 5.89; // The decimal part is cut off
    printf("%d", myInt); // Outputs: 5
    ```
    - Be careful with it.
      - When conversions happen automatically, you might lose valuable data.
      - For example, if you perform calculations involving two integers but need a precise result with decimals, the output won’t be what you expect:
      - Example:
        ```
        float result = 7 / 3;
        printf("%f", result); // Outputs: 2.000000 (not 2.33)
        ```

      - The numbers being divided are still integers, so C only gives the whole number part in the result.
  - **Explicit Conversion**
    - Done manually by the programmer.
    - Explicit conversion means you tell the compiler exactly what type to use.
    - You do this by putting the type in parentheses before the variable or value.
    - Let’s fix the division problem:
      ```
      float result = (float) 7 / 3;
      printf("%f", result); // Outputs: 2.333333
      You can also use explicit conversion on variables:
      Example:
      int a = 7;
      int b = 3;
      float result = (float) a / b;

      printf("%f", result); // Outputs: 2.333333
      ```

### Operators
- Operators are special symbols used to perform operations on variables and values.
- They help us manipulate data and perform tasks like addition, subtraction, and comparison.
- Types of Operators in C:
  - Arithmetic operators
    - Example: `+`, `-`, `*`, `/`, `%`
  - Assignment operators
    - Examples:
      - Simple Assignment Operator (`=`):
        - `X = 10`
      - Addition Assignment Operator (`+=`):
        - `X += 5` is same as `X = X + 5`
      - Subtraction Assignment Operator (`-=`):
        - `X -= 5` is same as `X = X - 5`
      - Multiplication Assignment Operator (`*=`):
        - `X *= 5` is same as `X = X * 5`
      - Division Assignment Operator (`/=`):
        - `X /= 5` is same as `X = X / 5`
      - Modulus Assignment Operator (`%=`):
        - `X %= 5` is same as `X =X % 5`
      - Bitwise AND Assignment Operator (`&=`):
        - `X &= 5` is same as `X = X & 5`.
      - Bitwise OR Assignment Operator (`|=`):
        - `X |= 5` is same as `X = X | 5`
      - Bitwise XOR Assignment Operator (`^=`):
        - `X ^= 5` is same as `X = X ^ 5`
      - Right Shift Assignment Operator(`>>=`):
        - `X >>= 5` is same as `X = X >> 5`
      - Left Shift Assignment Operator(`<<=`):
        - `X <<= 5` is same as `X = X << 5`.
  - Comparison operators
    - Comparison operators are used to compare two values or variables.
    - They help the program decide what to do based on the comparison result.
    - When a comparison is made, it returns either non zero (true) or 0 (false), which are also called Boolean values.
    - Examples:
      - Equal to (`==`)
        - `X == Y` Returns 1 if X is equal to Y
      - Not equal (`!=`)
        - `X != Y` Returns 1 if X is not equal to Y
      - Greater than(`>`)
        - `X > Y` Returns 1 if X is greater than Y
      - Less than (`<`):
        - `X < Y` Returns 1 if X is less than Y
      - Greater than or equal to(`>=`):
        - `X >= Y` Returns if X is greater than or equal to Y
      - Less than or equal to(`<=`):
        - `X <= Y` Returns 1 if X is less than or equal to Y
  - Logical operators
    - Logical operators allow you to check multiple conditions at the same time.
    - They help make decisions based on whether certain conditions are true or false.
    - Examples:
      - AND(`&&`):
        - `COND1 && COND2` Returns 1 if both conditions are true
      - OR(`||`):
        - `COND1 || COND2` Returns 1 if one of the conditions are true
      - NOT(`!`):
        - `!COND` Reverses the result; returns 0 if the result was 1
  - Bitwise operators
    - Used to perform operation on bit level after converting into binary.
    - Examples:
      - Bitwise AND (`&`):
        - Compares each bit of two operands and returns a new number, with bits set to 1 only where both operands have corresponding bits set to 1.
        - Example: 5 & 3 (binary: 0101 & 0011 results in 0001, which is 1 in decimal).
      - Bitwise OR (`|`):
        - Compares each bit of two operands and returns a new number, with bits set to 1 where at least one of the operands has a corresponding bit set to 1.
        - Example: 5 | 3 (binary: 0101 | 0011 results in 0111, which is 7 in decimal).

      - Bitwise NOT (~):
        - Inverts all bits of the operand, turning 1s into 0s and 0s into 1s.
        - Example: ~5 (binary: ~0101 results in 1010, which is -6 in decimal when considering signed integers due to two's complement representation).


## User Input C Programming:
- You've already learned that `printf()` is used to display output in C.
- But what if you want to get input from the user? This is where the `scanf()` function comes in handy.
- Getting User Input with `scanf()`:
  - To take input from the user, the `scanf()` function is used.
  - It reads the input based on format specifiers and assigns it to a variable.
  - It takes two arguments:
    - A format specifier that specifies the data type of the variable.
    - The address operator to store the variable's value at its memory address.
  - Both single and multiple input can be taken using it
    - Example:
      ```      
      // Create two variables
      int score; char grade;
      // Ask the user to enter a score and a grade
      
      printf("Enter your score and grade (like 95 A): ");
      // Get and save both inputs
      
      scanf("%d %c", &score, &grade);
      // Print the score and grade
      printf("Your score is: %d\n", score);
      printf("Your grade is: %c\n", grade);
      ```
    - Output before giving input:
      ```
      Enter your score and grade (like 95 A): |
      ```
    - Output after giving input:
      ```      
      Enter your score and grade (like 95 A): 97 A
      Your score is: 97 Your grade is: A
      ```
  - `scanf()` can also take string input as well.
    - When taking strings as input, `scanf()` reads until it encounters a whitespace character (like a space or tab). This means it can only read one word at a time.
    - Example:
      ```      
      // Create a string to store the name
      char Name [30];
      // Prompt the user to input their name
      printf("Enter your first name: ");
      // Get and save the name
      scanf("%s", Name);
      // Output the name
      printf("Hello %s", Name);
      ```
    - Output:
      ```      
      Enter your first name: Tasnim
      Hello Tasnim
      ```
    - When using `scanf()` with strings, you don’t need the `&` operator.
    - However, you must specify the size of the string to avoid storing more characters than the array can hold.

  - Limitations of `scanf()` with Strings
    - `scanf()` stops reading a string when it encounters a space, which means it only captures the first word entered.
    - If we input multiple word, only the first one is taken.
    - To overcome the limitations Use `fgets()` to Take Multi-Word Input
      - Example:
        ```        
        char fullName [30];
        printf("Type your full name: ");
        fgets (fullName, sizeof(fullName), stdin);
        printf("Hello %s", fullName);
        ```
      - Output:
        ```        
        Type your full name: John Doe
        Hello John Doe
        ```
      - How `fgets()` Works:
        -  It takes three arguments:
        - The name of the string variable (fullName).
        - The size of the string (sizeof(fullName)).
        - The input stream (`stdin`), which refers to the standard input (keyboard).


<!-- 8/10 -->
<!-- Too long -->