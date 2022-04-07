# core-code-from-scratch-readme

///Thuesday challenge///

1) Interpreted And Compiled Programming Languages

-Compiled langauges are those that can be read more directly by a machine's logical processor there is a "build" formed to execute a set of instructions the environment/machine need to construct the "build" every time you request the program to run 

-Interpreted languages use a structure and resources in a way where the machine is able to read and perform instructions line by line without the need
to read the whole of a "build" and can adopt to changes on the run like in pythoh, javascript and others

2) Is Java an interpreted or compiled langauge?

Java uses a process where there is first a source code is compiled to bytecode by an environment compiler
then the bytecode is executed or interpreted on the Java virtual machine , in the present Java virtual machines can use a "Just in time" compiulation of instructions to execute instructions on the fly.
Therefore it can be said that Java is both interpreted and compiled 

3) pseudocode- currency converter:

START

PRINT "Enter an ammount of dollars"

AMMOUT <-- GET

BTCVAL <-- 0.000033

CONVERSION<-- AMMOUNT * BTCVAL

PRINT "ammount is equal to $" CONVERSION

END 


4) Translate Date of birth to binary , we divide each number by 2 and leave a remainder for each of the non divisible by 2 operations
such as:
for example, 1993/2 =  remainder 1
             996 /2 =            0
             498 /2 =            0 
             249 /2 =            1
             124 /2 =            0
             62  /2 =            0
             31  /2 =            1
             15  /2 =            1
             7   /2 =            1
             3   /2 =            1
             1   / 2=            1
taking the numbers from the lowest result leaves us wi the answer of : 11111001001

5) MIPS challenge, make a program that adds 2 numbers

#Add two numbers 

.data
    numo1: .asciiz "Write your first number: "
    numo2: .asciiz "Write your second number: "
    resultado: .asciiz "the result of the sum is: "

.text
    #get first number
    la $a0, numo1
    li $v0, 4
    syscall
    li $v0, 5
    syscall
    move $t0, $v0

    #get second number
    la $a0, numo2
    li $v0, 4
    syscall
    li $v0, 5
    syscall
    move $t1, $v0

    #calculate and show a result
    la $a0, resultado
    li $v0, 4
    syscall
    add $t2, $t0, $t1
    move $a0, $t2
    li $v0, 1
    syscall

    #finalize program
    li $v0, 10
    syscall

