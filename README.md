![Script](https://github.com/internashionalist/atlas-TS_SHELLiot/blob/main/simple_shell_script2.jpg)

# T.S. SHELLiot - Is it Code... or Poetry?

>*"If you aren't in over your head, how do you know how tall you are?"*<br>
\-T.S. Eliot

## Contents

[Synopsis](#synopsis)<br>
[Description](#description)<br>
[Authors](#authors)<br>
[Instructions](#instructions)<br>
[Features](#features)<br>
[Flowchart](#flowchart)<br>
[Challenges](#challenges)<br>
[About-the-Developer](#about-the-developer)<br>
[Authors](#authors)<br>
[License](#license)

## Synopsis

This project creates a simple Unix-like shell program, codenamed T.S. SHELLiot (Thames-Sexton Shell), taking in user input and executing the given commands.

## Description

T.S. SHELLiot implements a simple command-line shell that mimics basic Unix shell functionality. It continuously displays a prompt ($) and allows users to execute commands by typing them into the terminal. The shell can handle interactive and non-interactive modes, parsing user input and executing commands using execve. It also gracefully handles end-of-file (EOF) signals and displays appropriate error messages for invalid commands.

## Instructions

**Clone into T.S. SHELLiot's Repository:**
```
git clone https://github.com/internashionalist/atlas-TS_SHELLiot.git
```
**Open the Shell Directory:**
```
cd atlas-TS_SHELLiot
```
**Compile Contents:**
```
gcc -Wall -Werror -Wextra -pedantic -std=gnu89 *.c -o hsh
```
**Run Shell Program:**
```
./hsh
```
**Command Shell:**
```
What we call the beginning is often the end.
TS SHELLIOT $ /bin/ls
```
**Exit Shell:**
```
TS SHELLIOT $ exit
The end is where we start from.

TS SHELLIOT $ ^D
This is the way the world ends,
Not with a bang but a whimper.
```

## Features
```
•Interactive and Non-Interactive Modes:
  - Interactive: Displays a prompt
  - Non-Interactive: Can process input from scripts or files

•Input Handling:
  - Reads input from the user using getline
	- Differentiates between NULL and End-Of-File with flag
	- Trims newline characters from the input

•Tokenization:
	- Splits input into tokens for further processing
	- Resizes the token array if number of tokens exceeds initial allocation

•Built-in Command Handling:
	- Processes exit and env commands
  - Executes built-in commands directly without creating a new process

•Command Execution:
	- Checks the status of the last executed command
	- Supports executing commands with arguments
  - Uses fork and execve to create child processes for command execution
  - Handles failures gracefully, allowing shell to continue

•Memory Management:
  - Frees allocated memory for input and tokens after each command execution
	- Allocates memory dynamically based on input size, ensuring efficient memory usage

•Modular Structure:
	- Uses a header file to declare function prototypes
	- Separates implementation into multiple source files

•Graceful Exit:
	- Exits gracefully whether upon encountering EOF or utilizing the exit built-in command
```


## Flowchart

![FlowChart](https://github.com/internashionalist/atlas-TS_SHELLiot/blob/main/flowchart.jpg)

## Challenges

Developing T.S. SHELLiot came with a unique set of challenges. One major difficulty was
understanding and correctly using the `fork` and `execve` system calls to manage child processes
while ensuring the parent shell remained responsive. Handling memory management efficiently was
another challenge, as dynamically allocating and freeing memory after each command execution
required careful attention to avoid leaks. Input parsing and tokenization also proved tricky,
particularly when dealing with variable-length commands and edge cases such as empty input or
invalid commands. Finally, balancing simplicity with robustness in a limited timeframe pushed us
to make clear design choices while still ensuring the shell mimicked essential Unix functionality.

## About the Developer

Nash Thames is an aspiring software developer with a strong foundation in computer science,
including advanced algorithms, systems programming, and Linux environments. 
He is passionate about problem-solving and dedicated to developing reliable, efficient, and
well-architected software. He is engaged in continuous learning and is interested in
contributing to research or projects that explore the intersection of software engineering,
distributed systems, and emerging technologies.

## Authors

- **Nash Thames**  
  [GitHub](https://github.com/internashionalist)  
  [LinkedIn](https://www.linkedin.com/in/nashthames)  
  [Email](taylor.thames@atlasschool.com)
- **Clay Sexton**  
  [GitHub](https://github.com/seer9)  
  [LinkedIn](https://www.linkedin.com/in/seer9)  
  [Email](clay.sexton@atlasschool.com)

## License

This project is released under the Public Domain - no copyright protections.
