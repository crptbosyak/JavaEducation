TASK:

Working with matrices
Project Setup
Create a file named TestAssignment.java.
For writing a solution for test assignment, it is sufficient to use only basic Java features. Try to implement it using only basic libraries (like java.lang., java.util., java.io.*).
Don't wrap the file in package.
For Unit Testing create a file named Test_TestAssignment.java. You may use any testing library you want for Unit testing.
Add files TestAssignment.java and Test_TestAssignment.java to a .zip archive named NameSurname.zip. For example: JaneDoe.zip
Your solution MUST be in a .zip archive and named as defined above.
Your task will be graded using automatic tests. We should be able to run it as described below.
We WILL NOT grade an assignment submitted omitting these rules.
Matrix Jugglery
The purpose of the task is to implement basic matrix operations: addition, subtraction and multiplication.

PLEASE IMPLEMENT THE TASK IN THE SIMPLEST POSSIBLE WAY!

Program run example
This is the only way we're going to run your program. Please make sure before the submission that it runs as described. You may use our test cases to do so.
Please note: we are using input and output redirection, we are not reading from file or writing to a file!

> java TestAssignment < data01.txt > result01.txt
> cat result01.txt
[5 1 1; 9 0 0]
> java TestAssignment < data02.txt

[2 4; 8 2]
Please note that there is no need to read from a file. You just need to process data from standard input. You can learn about input and output redirection here.

Each matrix is given in the following way: name=[x11 x12 ... x1n; x21 x22 ... x2n;...,xm1 xm2 ... xmm]
Matrix operations expression follows matrix definitions.

Example 01 with comments:

A=[1 2 2; 0 3 1; -1 2 -4]   <- first matrix definition, matrix A is 3x3
B=[2 1 0; -2 -1 -1; 1 1 2]  <- second matrix definition, matrix B is 3x3
<- new line
A+B                         <- matrix operation (addition)
Example 02 with comments:

M=[1 2 2; 0 3 1; -1 2 -4]   <- first matrix definition, matrix M is 3x3
N=[2 1 0; -2 -1 -1; 1 1 2]  <- second matrix definition, matrix N is 3x3
K=[2 3; 5 0; 3 1]           <- third matrix definition, matrix K is 3x2
<- new line
M+K+N+N*N+M+N               <- matrix operations (5 additions and 1 multiplication)
Requirements
Name of the matrix has to be an uppercase letter.
Input should always follow the same pattern: matrix definitions - new line - matrix operations.
Each matrix is defined on a separate line.
Matrix must have valid size to perform operations (see operations definitions below).
You may assume that all matrices are uniform.
Elements are separated by whitespace, rows are separated by semicolon.
Elements are wrapped in square brackets.
Operations are separated from matrix definition with exactly one new line.
Operations may contain arbitrary number of operators and operands.
There are only three operators: +, - and *.
Operators have the following priority: multiplication, addition and subtraction.
Operations are evaluated from left to right.
You can read A+B*C+D*E-F as ((A+(B*C))+(D*E))-F
Output of the program is the result of defined operations.
Number of matrices are limited by the number of letters in English alphabet, length of operation expression is not limited.
Every element in matrix is an integer number.
If any of requirements described above are failing, exception should be thrown and a message should appear in stderr.
Error messages should be formed in the following way:
Exception caught: $exceptionName. Can't $do_something.
More Examples
Example 03:
stdin:

S=[1]
P=[1]

S+P
stdout:

[2]
stderr:

Example 04:
stdin:

B=[5 2 4; 0 2 -1; 3 -5 -4]
E=[-6 -5 -8; -1 -1 -10; 10 0 -7]
R=[-1 -7 6; -2 9 -4; 6 -10 2]

R+E+B
stdout:

[-2 -10 2; -3 10 -15; 19 -15 -9]
stderr:

Example 05:
stdin:

K=[-10 0 2; -6 10 -6; -9 2 0]
D=[0 6 7]
M=[10 -5 -4]

D*K+M
stdout:

[-89 69 -40]
stderr:

Example 06:
stdin:

R=[6 9; -3 9; -9 10]
K=[2 -8 8; -1 2 -4]

K+K*R*K
stdout:

[-96 332 -384; 78 -252 312]
stderr:

Example 07:
stdin:

M=[-9 5 9; -7 8 7; 10 -3 3]

M*M+M-M
stdout:

[136 -32 -19; 77 8 14; -39 17 78]
stderr:

Example 08:
stdin:

M=[-9 5 9; -7 8x 7; 10 -3 3]`

M*M
stdout:

stderr:

Exception caught: IllegalArgumentException. Can't read matrix.
Example 09:
stdin:

P=[6 0 9; -3 1 9; -9 2 10]
Q=[2 -8 8 0; -1 2 -4 2]

P+Q*P+Q
stdout:

stderr:

Exception caught: IllegalArgumentException. Can't perform multiplication.
You can use our test data to test your solution.

We use the following definitions:
Matrix https://mathworld.wolfram.com/Matrix.html
Matrix multiplication https://mathworld.wolfram.com/MatrixMultiplication.html
Matrix addition (and subtraction) https://mathworld.wolfram.com/MatrixAddition.html

Non-functional Requirements
Your solution MUST have an appropriate Javadoc.
You code MUST be readable and follow any of known code conventions.
You MUST cover at least 25% of your methods with unit tests.
Unit Tests MUST be in the separate file.