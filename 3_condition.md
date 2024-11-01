
# Decision Making in C

In programming, we often need to perform different sets of actions depending on certain conditions. For example:

- If the weather is fine, go for a walk.
- If the highway is busy, take a diversion.

In C, decision-making is done using conditional statements, which enable the program to decide which path of execution to follow. These include:

- `if` statement,
- `if-else` statement,
- Conditional (`ternary`) operator,
- `switch` statement

Let's dive into the C version of decision control instructions and how we can use them in different scenarios.

---

### if statement
- In C, we use the `if` statement to make decisions. The general form of the `if` statement looks like this:
- Structure of `if` statement:
    ```c
    if(conditional_statement){
        // execute is condition is true
    }
    ```
    - `conditional_statement`:
        - Anything that returns true(non-zero) or false(0).
        - Can be single condition (`i < 10`) or combination of multiple condition (`i>5 && i < 10`), or any function that returns boolean.
    - The `conditional_statement` is enclosed in parentheses `()`.
    - If the `conditional_statement` evaluates to `true`, the block of code inside the braces {} is executed.
    - If the condition is false, the program skips the code inside the braces and continues with the next line.
- Example:
    - Code:
        ```c
        int quantity = 2000;

        if (quantity > 1000) {
            printf("10%% discount\n");
        }
        ```
    - Output:
        ```
        10% discount
        ```

### if-else statement
- The if-else statement allows you to execute one block of code if the condition is true and another block if the condition is false.
- Structure of `if-else` statement is:
    ```c
    if(conditional_statement){
        // execute is condition is true
    }
    else{
        // execute if false
    }
    ```
- Let’s take a scenario where a discount of 10% is given if the quantity purchased is greater than 1000.
    - Code:
        ```c
        int quantity = 2000;

        if (quantity > 1000) {
            printf("10%% discount\n");
        }
        else{
            printf("No discount\n");
        }
        ```
    - Output:
        ```
        10% discount
        ```

### else-if Ladder
- The `else-if` ladder allows us to check multiple conditions in sequence.
- Once a condition is true, the corresponding block of code is executed, and the rest of the ladder is skipped.
- Structure of `else-if` ladder:
    ```c
    if (condition1) {
        // execute if condition1 is true
    }
    else if (condition2) {
        // execute if condition2 is true
    }
    else if (condition3) {
        // execute if condition3 is true
    }
    else {
        // execute if none of the above conditions are true
    }
    ```
- Let's consider a scenario where:
    - A 20% discount is given if the quantity is above 2000.
    - A 10% discount if the quantity is above 1000 but 2000 or below.
    - No discount if the quantity is 1000 or below.
    - Example code:
        ```c
        int quantity = 1500;

        if (quantity > 2000) {
            printf("20%% discount\n");
        }
        else if (quantity > 1000 && quantity <= 2000) {
            printf("10%% discount\n");
        }
        else {
            printf("No discount\n");
        }
        ```
    - Output:
        ```
        10% discount
        ```
    - In this example:
        - If `quantity` is more than 2000, it prints "20% discount".
        - If `quantity` is between 1001 and 2000, it prints "10% discount".
        - If `quantity` is 1000 or below, it prints "No discount".

### Nested if-else Statements in C
- Sometimes we may need to test multiple conditions, one inside another. This is called nesting of if-else statements.
- All of the above statements can be nested.
- Example:
    ```c
    int number = 0;
    if (number >= 0) {
        if (number == 0) {
            printf("The number is zero.\n");
        } else {
            printf("The number is positive.\n");
        }
    } else {
        printf("The number is negative.\n");
    }
    ```
- Output:
    ```
    The number is zero.
    ```

### Ternary Operator
- The conditional or ternary operator (`? :`) offers a quick way to check a condition and choose between two values.
- This operator is often used to replace simple `if-else` statements for readability, especially in assignments and quick checks.
- Structure of `ternary` operator:
    ```c
    condition ? expression_if_true : expression_if_false;
    ```
- How the Ternary Conditional Operator Works
    - `condition` is evaluated first.
    - If the `condition` is true (non-zero), `expression_if_true` is evaluated and becomes the result.
    - If the `condition` is false (0), `expression_if_false` is evaluated and becomes the result.

- Example:
    ```c
    int age = 18;
    const char* eligibility = (age >= 18) ? "Eligible to vote" : "Not eligible to vote";
    printf("%s\n", eligibility);
    ```
- Output:
    ```
    Eligible to vote
    ```
- Explaination:
    ```
    Here, the condition (age >= 18) is evaluated.
    As age >= 18 is true, eligibility is set to "Eligible to vote". If age < 18, the condition would be false, and eligibility would be set to "Not eligible to vote".
    ```

### Summary
- `if` statement: Executes a block if a condition is true.
- `if-else` statement: Executes one block if the condition is true and another if it's false.
- Nested `if-else`: Used when multiple conditions need to be checked, each depending on the previous.
- Ternary is nothing but a shorter version of `if-else`.
- As our programs grow more complex, mastering these control statements will help us handle different situations effectively.


## switch statement
- The `switch` statement allows the program to evaluate an expression (typically an integer or character) and jump directly to the corresponding case label.
- Each case represents a possible value of the expression, and the corresponding block of code is executed when the value matches.
- If no match is found, an optional `default` block is executed.
- Structure of `switch` statement:
    ```c
    switch (expression) {
        case constant1:
            // code to execute if expression matches constant1
            break;
        case constant2:
            // code to execute if expression matches constant2
            break;
        case constant3:
            // code to execute if expression matches constant3
            break;
        default:
            // code to execute if no cases match
    }
    ```
- How the switch Statement Works
    - The expression inside the switch is evaluated.
    - The program compares the result with each case constant, starting from the top.
    - When a match is found, the code inside that case block is executed.
    - The `break` statement ensures that the program exits the switch after executing the matching case.
    - Without the break, execution continues to the next case block.
    - If no case matches, the default block (if present) is executed.

- Example:
    ```c
    int day = 3;

    switch (day) {
        case 1:
            printf("Monday\n");
            break;
        case 2:
            printf("Tuesday\n");
            break;
        case 3:
            printf("Wednesday\n");
            break; // <----------------------(1)
        default:
            printf("Other day\n");
    }
    ```
- Output:
    ```
    Wednesday
    ```
- Output if the break (1) is not used:
    ```
    Wednesday
    Other day
    ```