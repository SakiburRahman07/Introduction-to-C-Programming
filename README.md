
### Goal
- Our goal is NOT to teach you everything about the language C.
- Our goal is to make you understand
    - How computer interpret a language,
    - How the language get executed,
    - What a language can do

### What is programming?
Programming is the process of **creating instructions for a computer to follow**, to perform specific tasks/goal.
Let us understand via a simple real-life example:
- Our goal is to **teach a robot to make tea**.
- Assumption:
    - Hardware part is handled by system.
    - We will focus on software part only.
- Before we continue, remember
    - Computer is dumb, it doesn't know what to do until a clear, precise instruction is given.
    - For example:
        - We can't just ask computer to **take two numbers from user, and perform addition, then show the result**.
        - It's a vague instruction.
        - What can be the precise instructions then? -----`(a)`
            - Allocate two memory addresses,
            - Take the first number and store in the first address,
            - Take the second number and store in the second address,
            - Add those two numbers and save in another memory address,
            - Show the result to user from the memory location.
        - You may still think, the precise instructions are not precise enough. Yes, they are not. Because
            - Dumb computer don't know how to allocate memory addresses,
            - We have to tell how to do each and every sub step to complete a step.
            - Fortunately, these are done by operating system and the programming language.
            - So, at the language level, instructions at `(a)` can be considered as precise for that language.
- Back to **teaching a robot to make tea**
    - The robot is as dumb as the computer. So we have to give it clear, step-by-step instructions.
    - Let us see how it might look in programming terms in each step: The instructions are to ask robot to
        - **Boil Water**
        - **pour hot water into a cup**
        - **Add a tea bag**
        - **Wait** to give the tea some time to get properly brewed.
        - **Add Sugar or Milk (if required)**
        - **Serve**
- In summary:
    - Programming is the process of giving computers specific instructions to solve problems or perform tasks.
    - It is like writing a detailed list of steps for the computer to follow, which allows it to do things automatically, like performing calculations, organizing data, or running apps and games.

### What is programming language?
- A set of instruction to enable human to communicate with computer.
- Remember, computer only understand 0 and 1. And it's very hard for us to write instruction using 0,1 only.
- Here a programming language saves us by allowing us to write instructions without dealing with low level machine code(0,1).
- So, programming language stays in between us and computer. We write instrucitons using the language, then the compiler(discussed later) converts the instructions into binary code.
- As it is a language, so it has its own structure and syntax for defining instructions. Right?


### Comparison of High-Level and Low-Level Languages

Programming languages can be categorized into high-level and low-level languages, each serving different purposes in software development. High-level languages are closer to human languages and are designed to be more programmer-friendly, whereas low-level languages are closer to machine code and are more efficient for hardware-level programming. The following table outlines the key differences between these two types of languages.

| Feature                              | High-Level Language                         | Low-Level Language                          |
|--------------------------------------|--------------------------------------------|--------------------------------------------|
| Programmer Friendliness              | It is programmer-friendly.                 | It is machine-friendly.                    |
| Memory Efficiency                    | Less memory efficient.                     | High memory efficient.                     |
| Ease of Understanding                | Easy to understand.                        | Tough to understand.                       |
| Debugging                            | Debugging is easy.                         | Debugging is complex comparatively.        |
| Maintenance                          | Simple to maintain.                        | Complex to maintain comparatively.         |
| Portability                          | Portable.                                  | Non-portable.                              |
| Translation Requirement              | Needs a compiler or interpreter.           | Needs an assembler.                        |
| Usage                                | Widely used for programming.               | Not commonly used in modern programming.   |

### Difference Between Compiler and Interpreter

| Aspect                                   | Compiler                                                                                                         | Interpreter                                                                                             |
|------------------------------------------|------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------|
| **Steps of Programming**                 |1. Program Creation. <br>2. Analyzes language and throws errors if any.<br>  3. Converts source code to Machine Code if no errors.<br>  4. Links code files into a runnable program. <br> 5. Runs the program. | 1. Program Creation. <br> 2. Linking or Machine Code generation not required.<br>  3. Executes source statements one by one. |
| **Storage of Machine Language**          | Saves Machine Code to disk.                                                                                     | Does not save Machine Code.                                                                             |
| **Speed**                                | Compiled code runs faster than interpreted code.                                                                | Interpreted code runs slower than compiled code.                                                        |
| **Basic Working Model**                  | Linking-Loading Model.                                                                                          | Interpretation Model.                                                                                   |
| **Output**                               | Generates an executable file (.exe).                                                                            | Does not generate an executable output.                                                                 |
| **Recompilation**                        | Requires recompiling the entire code if changes are made in the source program.                                 | Does not require retranslating the entire code when changes are made.                                   |
| **Error Display**                        | Errors are displayed together after compilation.                                                                | Errors are displayed line by line during execution.                                                     |
| **Optimization**                         | Optimizes by analyzing entire code upfront, making execution faster.                                            | Optimizes more slowly as it interprets code line by line.                                               |
| **Source Code Requirement**              | Does not need source code for later execution.                                                                  | Requires source code for each execution.                                                                |
| **Execution Timing**                     | Executes only after entire program is compiled.                                                                 | Executes after each line is checked or evaluated.                                                       |
| **Analysis Time**                        | Takes more time for source code analysis.                                                                       | Takes less time for source code analysis.                                                               |
| **CPU Utilization**                      | Higher CPU utilization.                                                                                         | Lower CPU utilization.                                                                                  |
| **Environment**                          | Mostly used in production environments.                                                                         | Mostly used in programming and development environments.                                                |
| **Object Code**                          | Saves object code for future use.                                                                               | Does not save object code for future use.                                                               |
| **Example Languages**                    | C, C++, C#, etc.                                                                                                | Python, Ruby, Perl, SNOBOL, MATLAB, etc.                                                                |

### What is C?
- It is a programming language.
- It allows us to work closely with the computer’s hardware.
- It gives us direct control over memory through features like pointers (variables that store memory addresses) and let us perform operations to manipulate data at the memory level.
- C is widely used in building Operating Systems, Embedded Systems, Game Development, Compiler Development etc.

### Why C?
- It helps us to understand how computer works at low level.
- It helps us understand the core programming concepts, like managing memory and working with low-level data, which are essential for developing efficient software. 
- Many modern languages, like C++, Java, and Python are directly influenced by C’s syntax and structure.
- So understanding C makes it much easier to learn these languages and grasp advanced programming principles. 

### Structure of a C Program

The structure of a C program is divided into six main sections, each of which serves a specific purpose. This organized approach makes programs easier to read, modify, document, and debug.

---

## 1. Documentation

The documentation section provides information about the program, such as its description, author name, and creation date. This information is placed in the form of comments at the beginning of the program. Documentation is ignored by the compiler and serves as a guide for anyone reading the code.

```c
// Program: Sum of two numbers
// Author: Your Name
// Date: YYYY-MM-DD

/*
    Program: Sum of two numbers
    Author: Your Name
    Date: YYYY-MM-DD
    Description: This program calculates the sum of two numbers.
*/
```

## Preprocessor Section

The **Preprocessor Section** is where all header files and macro definitions are included at the start of a C program. These files and definitions are processed before the compilation phase, allowing the program to use library functions, constants, and macros.

### Header Files

Header files contain declarations of standard library functions, macros, and types. Including them in a program enables access to predefined functionality, such as input/output operations, mathematical functions, and memory allocation.

**Example:**

```c
#include <stdio.h>    // Standard I/O library for functions like printf() and scanf()
#include <stdlib.h>   // Standard library for memory allocation and process control
#include <math.h>     // Math library for functions like sqrt(), pow(), etc.

```
### Definition

Preprocessors are programs that process source code before compilation. There are multiple steps involved in writing and executing a program. Preprocessor directives start with the `#` symbol. The `#define` preprocessor is used to create a constant throughout the program. Whenever this name is encountered by the compiler, it is replaced by the actual piece of defined code.

**Example:**

```c
#define PI 3.14
```

### Global Declaration

The global declaration section contains global variables, function declarations, and static variables. Variables and functions declared in this scope can be used anywhere in the program.

**Example:**

```c
int num = 18;
```
### Main() Function

Every C program must have a `main` function. The `main()` function of the program is written in this section. Operations such as declaration and execution are performed inside the curly braces of the main program. The return type of the `main()` function can be either `int` or `void`. The `void main()` tells the compiler that the program will not return any value, while `int main()` indicates that the program will return an integer value.

**Example:**

```c
void main()
```

### Sub Programs

User-defined functions are called in this section of the program. The control of the program is shifted to the called function whenever it is invoked from the `main()` or outside the `main()` function. These functions are specified according to the requirements of the programmer.

**Example:**

```c
int sum(int x, int y)
{
    return x + y;
}
```

### Structure of a C Program with Example

**Example:** Below is a C program to find the sum of two numbers:

```c
// Documentation
/**                     
 * file: sum.c
 * author: you
 * description: program to find sum.
 */

// Link
#include <stdio.h>      

// Definition
#define X 20 

// Global Declaration
int sum(int y);   

// Main() Function
int main(void)       
{
    int y = 55;
    printf("Sum: %d", sum(y));
    return 0;
}

// Subprogram
int sum(int y) 
{
    return y + X;
}

```
### Output
**75**


### Explanation of the Above Program

Below is the explanation of the program, describing its meaning and use.

| Sections | Description |
|----------|-------------|
| `/**`<br> `* file: sum.c`<br> `* author: you`<br> `* description: program to find sum.`<br> `*/` | This is the comment section and part of the documentation for the code. |
| `#include <stdio.h>` | This header file is used for standard input-output. It belongs to the preprocessor section. |
| `#define X 20` | This is the definition section. It allows the use of the constant `X` in the code. |
| `int sum(int y);` | This is the global declaration section, which includes the function declaration that can be used anywhere in the program. |
| `int main()` | The `main()` function is the first function executed in a C program. |
| `{…}` | These curly braces mark the beginning and end of the `main` function. |
| `printf("Sum: %d", sum(y));` | The `printf()` function is used to print the sum on the screen. |
| `return 0;` | Since `int` is used as the return type, we must return `0`, indicating that the program executed successfully without errors. |
| `int sum(int y)`<br>`{`<br>`    return y + X;`<br>`}` | This is the subprogram section, which includes the user-defined function that is called in the `main()` function. |

### Steps Involved in the Compilation and Execution of a C Program:

1. **Program Creation**
2. **Compilation of the Program**
3. **Execution of the Program**
4. **Output of the Program**


### First C program
- Let us create a simple program that will print "Hello World!" to the console.
- Code:
    ```c
    #include <stdio.h>   // Includes standard I/O library

    int main() {         // Main function starts here
        printf("Hello, World!\n");  // Print statement
        return 0;        // Program ends, returning 0 to the OS
    }
    ```
- Explanation:
    - `#include <stdio.h>`: Includes the standard input-output library for using `printf`.
    - `int main()`: Declares the main function where execution begins.
    - `printf("Hello, World!\n");`: Prints "Hello, World!" followed by a newline character.
    - `return 0;`: Indicates successful completion of the program.

### Program Execution
This is the part where our code written in C, is converted into computer understandable format. In short, it does the translation from C code to binary code. The steps are:

- **Writing the Code** 
    - At first, we write the C code in a text editor and saves it with a `.c` extension.
    - Let us solve a problem that **convert degree into radian**.
    - Let's name the file `bit2byte.c` with the following content(No need to understand now):
        ```c
        #include<stdio.h>
        #define PI 3.14159

        int main(){

            float angle;

            // Taking the angle input from user in degree
            scanf("%f", &angle);

            // Converting into radian
            float rad = (PI / 180) * angle;

            printf("Angle in radian is %f\n", rad);
            return 0;
        }
        ```
- **Preprocessing**
    - This steps involves the following substeps:
        - Remove comment(discussed later) from code.
            - `//comment` and `/*comment*/` are removed.
            - Before:
                ```
                // Taking the angle input from user in degree
                ```
            - After:
                ```
                ```
        - Expand macros.
            - Constant defined using `#define` are replaced with it values in the program.
            - Before:
                ```
                float rad = (PI / 180) * angle;
                ```
            - After:
                ```
                float rad = (3.14159 / 180) * angle;
                ```
        - Expansion of included files.
            - Content of the header file is added inside the program.
            - Before:
                ```
                #include<stdio.h>
                ```
            - All content from the `stdio.h` is added into the `bit2byte.c` file.
            - After: (Note there are many other functions. For simplicity we are showing only two)(Only two are used in our code).
                ```
                void printf(const char *format, ...);
                int scanf(const char *format, ...);
                ```
        - Conditional compilation.
            - `#ifdef`, `#endif` are part are processed here based on definition.
            - Before:
                ```c
                #define DEBUG

                #ifdef DEBUG
                    printf("Debugging information.\n");
                #endif
                ```
            - After:(since `DEBUG` is defined).
                ```c
                printf("Debugging information.\n");
                ```
    - Output after preprocessing:(`bit2byte.i`)
        ```c
        # 1 "bit2byte.c"
        # 1 "<built-in>"
        # 1 "<command-line>"
        # 1 "bit2byte.c"
        ... ... ...
        int main(){

            float angle;


            scanf("%f", &angle);



            float rad = (3.14159 / 180) * angle;

            printf("Angle in radian is %f\n", rad);
            return 0;
        }
        ```
    - We can get the code by running the following command in the folder containing the `.c` file:
        ```bash
        gcc -E bit2byte.c -o bit2byte.i
        ```
- **Compilation**
    - The compiler translates the preprocessed code from C into assembly language (low-level language)
    - It checks for syntax errors and optimize the code for efficiency.
    - If errors are found, the compiler provides messages containing the error message.
    - Output after compiling the preprocessed file:(`bit2byte.s`)
        ```
            .file	"bit2byte.c"
            .text
            .def	__main;	.scl	2;	.type	32;	.endef
            .section .rdata,"dr"
        ... ... ...
        .LC1:
            .long	-1525816720
            .long	1066524485
            .ident	"GCC: (x86_64-posix-seh-rev0, Built by MinGW-W64 project) 8.1.0"
            .def	scanf;	.scl	2;	.type	32;	.endef
            .def	printf;	.scl	2;	.type	32;	.endef
        ```
    - Command for getting the assembly code
        ```bash
        gcc -S bit2byte.i -o bit2byte.s
        ```

- **Assembly**
    - The assembler converts the assembly code into machine code, creating an object file.
    - Output after generating machine code(`bit2byte.o`)
        ```o
        d†      ~        .text           p   ,  $           P`.data                               @ PÀ.bss                                € PÀ.rdata          0   œ              @ P@.xdata             Ì              @ 0@.pdata             Ø  `         @ 0@/4              @   ä              @ P@UH‰åHƒì0è    HEøH‰ÂH
        è    óEøóZÈò    òYÁòZÐóUüóZEüfH~ÀH‰ÂfHnÊH‰ÂH
           è    ¸    HƒÄ0]Ã%f Angle in radian is %f
            pâ
        ¥Eß‘?        RP      j       GCC: (x86_64-posix-seh-rev0, Built by MinGW-W64 project) 8.1.0  	          
                -   
         V   
         [                             .file       þÿ  gbit2byte.c        main                             .text          j                .data                            .bss                             .rdata         (                 .xdata                          .pdata                                        ?                 __main           scanf            printf              .rdata$zzz .rdata$zzz 
        ```
    - Command for generating the object file:
        ```bash
        gcc -c bit2byte.s -o bit2byte.o
        ```
- **Linking**
    - The linker combines object files and libraries to produce a complete executable file, typically named `output.out` on Unix/Linux or `output.exe` on Windows.
    - Few lines of the output(`output.exe`)
        ```
        MZ       ÿÿ  ¸       @                                   €   º ´	Í!¸LÍ!This program cannot be run in DOS mode.
        $       PE  d† 	J!g h  œ  ð ' 
            8   
        ```
    - Why the output contains other things except 0,1? It actually contains 0,1 only. But our editor tries to show us in human readable format. Thats why we are seeing something strange, instead of random.
    - Command for generating:
        ```
        gcc bit2byte.o -o output
        ```
- **Loading** 
    - When we run the `output.exe` file, the loader is invoked.
    - The operating system loads the executable file into memory, allocating space for the code and data.
    - Command for running(windows):
        ```
        output.exe
        ```
    - We can see the same behaviour as if we are running the code from ide.

- **Execution**
    - After the program is loaded into memory, the CPU start execution from entry point `main()` function, and interacts with the system until it completes or is terminated.
- **Termination**
    - The program ends with an exit status to the operating system(usually 0 for success), and the OS frees any used resourcess.


### main() function
- Remember, our code can have different function and instructions between them.
- We can't start executing randomly from anywhere. It doesn't make sense.
- That's why the `main()` function is executed at the first.
- This is the entry point of our code.