## _printf() > In this project, we recreated a mini-verison of the ```printf``` function found in > the ```stdio.h``` library in the C programming language. This function allows > us to print any argument given to the standard output or terminal and similar > printing functions can be found in any programming language. This means we can > print any combinations of strings, intergers, and other different data types.
Synopsis
This repository holds all the code necessary for our custom _printf function to run. Our mini-version currently handles conversion specifiers: c, s, %, d, i, b, o and does not yet support field width, precision, flag characters, or length modifiers. Unique to our _printf is our r reverse conversion and the R rot13 conversion. In essence, you can print any character, string, integer, or decimal number, reverse your strings, transform any number to binary and octal bases, and encrypt your string with rot13 encryption.

Description of what each file shows:
man_3_printf ----------------------- custom manpage for custom _printf function
print.c ---------------------------- holds custom _printf function
holberton.h ------------------------ holds prototypes of functions spread across all files
getFunc_and_buffer_functions.c ----- holds functions to get appropriate function, and create and write buffer
strcpy.c --------------------------- holds custom-made strcpy function
strlen.c --------------------------- holds custom-made strlen function
string.c --------------------------- handles %s to print a string of characters
char.c ----------------------------- handles %c to print a single character
decimal.c -------------------------- handles %d and %i to print (d)ecimal/(i)ntegers in base 10
binary.c --------------------------- handles %b to convert numbers passed into base 2
octal.c ---------------------------- handles %o to convert numbers passed into base 8
rot13 ------------------------------ handles %R to move each character 13 alphabet letters down
Environment
Language: C
OS: Ubuntu 14.04 LTS
Compiler: gcc 4.8.4
Style guidelines: Betty style
How To Install & Compile
(terminal)$ git clone https://github.com/oluwayoy/printf.git
(terminal)$ cd printf
Sample main program inside print.c:

int main(void)
{
	_printf("%s %c%drld", "Hello", "W", 0);
	return (0);
}
====================================
(terminal)$ gcc -Wall -Werror -Wextra -pedantic -Wno-format *.c -o print
(terminal)$ ./print
Hello W0rld
(terminal)$
To Do
The main _printf function can be separated into more modular shorter functions
More functionality can still be added (e.g. support field width specifiers, etc)
0x011 .C Printf

The aim of the project is to understand the concept of team work and therefore, demisifying the concept of printf



Tasks

These are all the tasks of this project, the ones that are completed link to the corresponding files.

0. I'm not going anywhere. You can print that wherever you want to. I'm here and I'm a Spur for life]
Write a function that produces output according to format.
c : converts input into a character
s : converts input into a string

1. Education is when you read the fine print. Experience is what you get if you don't
Handle the following conversion specifiers:
d : converts input into a base 10 integer
i : converts input into an integer

2. Just because it's in print doesn't mean it's the gospel
Create a man page for your function

3. With a face like mine, I do better in print
Handle the following conversion specifiers:
b : the unsigned int argument is converted to binary

4. What one has not experienced, one will never understand in print
Handle the following conversion specifiers:
u : converts the input into an unsigned integer
o : converts the input into an octal number
x : converts the input into a hexadecimal number
X : converts the input into a hexadecimal number with capital letters

5. Nothing in fine print is ever good news
Use a local buffer of 1024 chars in order to call write as little as possible.

6. My weakness is wearing too much leopard print
Handle the following custom conversion specifier:
S : prints the string
Non printable characters (0 < ASCII value < 32 or >= 127) are printed this way: \x, followed by the ASCII code value in hexadecimal (upper case - always 2 characters)

7. How is the world ruled and led to war? Diplomats lie to journalists and believe these lies when they see them in print
Handle the following conversion specifier:
p : int input is converted to a pointer address

8. The big print gives and the small print takes away
Handle the following flag characters for non-custom conversion specifiers:
+ : adds a + in front of signed positive numbers and a - in front of signed negative numbers
space : same as +, but adds a space (is overwritten by +)
# : adds a 0 in front of octal conversions that don't begin with one, and a 0x or 0X for x or X conversions

9. Sarcasm is lost in print
Handle the following length modifiers for non-custom conversion specifiers:
l : converts d, i, u, o, x, X conversions in short signed or unsigned ints
h : converts d, i, u, o, x, X conversions in long signed or unsigned ints

10. Print some money and give it to us for the rain forests
Handle the field width for non-custom conversion specifiers.

11. The negative is the equivalent of the composer's score, and the print the performance
Handle the precision for non-custom conversion specifiers.

12. It's depressing when you're still around and your albums are out of print
Handle the 0 flag character for non-custom conversion specifiers.

13. Every time that I wanted to give up, if I saw an interesting textile, print what ever, suddenly I would see a collection]
Handle the - flag character for non-custom conversion specifiers.

14. Print is the sharpest and the strongest weapon of our party
Handle the following custom conversion specifier:
r : prints the reversed string

15. The flood of print has turned reading into a process of gulping rather than savoring
Handle the following custom conversion specifier:
R : prints the rot13'ed string

16. *
All the above options work well together.

Authors

Emmanuel  ![image](https://user-images.githubusercontent.com/107483062/183073186-6eca3ea6-249d-48d9-8049-5d25fca2da6d.png)
 paul @ https://github.com/paulsunday
