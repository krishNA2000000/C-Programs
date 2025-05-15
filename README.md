# C-Programs
//first c program

#include<stdio.h>

int main()
{
    printf("Bhagwan Bharose!!");
    
    return 0;
}
Op-Bhagwan Bharose!!



//addition of numbers

#include<stdio.h>

int main()
{
    int a,b,sum;
    
    printf("enter the value of a and b:\n");
    scanf("%d%d",&a,&b);
    
    sum=a+b;
    
    printf("the value of %d and %d is:%d",a,b,sum);
    
    return 0;
}
Op-
enter the value of a and b:
5
6
the value of 5 and 6 is:11

////C program to check whether an alphabet is vowel or consnant.
Note:
*Character Handling-- Uses char data type to deal with single alphabet inputs.
*Conditional Statements --Uses if-else to branch logic based on conditions.
*Simple and efficient logic using || (logical OR) for multiple comparisons.
*Standard I/O --Uses printf() and scanf() for console-based input/output operations.
*Function Structure --The entire logic is wrapped inside main()—the starting point of the program.
*Control Flow --The program decides output based on user input dynamically at runtime.

#include <stdio.h>


int main()
{
	char ch ;
	
	printf("Enter an alphabet to check whether it is vowel or consonant:");
	scanf("%c", &ch);

	
	
	if (ch == 'a' || ch == 'A' || ch == 'e' || ch == 'E'
		|| ch == 'i' || ch == 'I' || ch == 'o' || ch == 'O'
		|| ch == 'u' || ch == 'U') {

		printf("The character %c is a vowel.\n", ch);
	}
	else {
		printf("The character %c is a consonant.\n", ch);
	}

	return 0;
}
o/p-
Enter an alphabet to check whether it is vowel or consonant:I
The character I is a vowel.

Enter an alphabet to check whether it is vowel or consonant:p
The character p is a consonant.


////C Program to demonstrate sum of Natural Numbers using while loops

#include <stdio.h>
int main()
{
    int i, s = 0,n;
    printf("enter the no. of natural numbers you want to find sum of:");
    scanf("%d" , &n);
    i = 1;
    while (i <= n) {
    s += i;
        i++;
    }
    printf("Sum of the first %d natural numbers is = %d",n, s);
    return 0;
}
o/p-
enter the no. of natural numbers you want to find sum of:30
Sum of the first 30 natural numbers is = 465
Other alternatives-
1)using for loop-

Uses a for loop instead of while.

More compact and readable.

Suitable for counting scenarios with known start/end.

e.g., for (i = 1; i <= n; i++)
    sum += i;
2)Using function
Logic is separated into a reusable function:

Good for modularity and maintainability.

The function sumOfNaturalNumbers(n) handles the computation.

Main function handles I/O only.

Promotes code reuse in larger projects.

e.g.,
#include <stdio.h>


int sumOfNaturalNumbers(int n) {
    int sum = 0;
    for (int i = 1; i <= n; i++) {
        sum += i;
    }
    return sum;
}

int main() {
    int n;
    printf("Enter the number of natural numbers you want to find the sum of: ");
    scanf("%d", &n);

    int result = sumOfNaturalNumbers(n);
    printf("Sum of the first %d natural numbers is = %d", n, result);
    return 0;
}
3)Using Mathematical formula
Formula for sum of first n natural numbers: Sum=n(n+1)/2

No loops — executes in constant time (O(1)).

Extremely efficient, especially for large n
e.g.,
#include <stdio.h>

int main() {
    int n;
    printf("Enter the number of natural numbers you want to find the sum of: ");
    scanf("%d", &n);

    int sum = n * (n + 1) / 2;

    printf("Sum of the first %d natural numbers is = %d", n, sum);
    return 0;
}
(or)
for input validation we can do:
Uses a do-while loop for input validation.

Rejects any input <= 0 with a helpful error message.

Ensures correct calculation using the formula only when input is valid.
e.g.,
#include <stdio.h>

int main() {
    int n;

    // Prompt the user until a valid input is given
    do {
        printf("Enter a positive number of natural numbers to find the sum of: ");
        scanf("%d", &n);

        if (n <= 0) {
            printf("Invalid input. Please enter a positive integer greater than 0.\n");
        }

    } while (n <= 0);  // Keep asking until a valid input


    // Calculate sum using the formula
    int sum = n * (n + 1) / 2;

    printf("Sum of the first %d natural numbers is = %d\n", n, sum);
    return 0;
}





////// C program to print ASCII Value of Character using
// implicit conversion with format specifier.
#include <stdio.h>

int main() {
    char c = 'k';

    // %d displays the integer value of
    // a character
    // %c displays the actual character
    printf("The ASCII value of %c is %d", c, c);
    return 0;
}

o/p- The ASCII value of k is 107
#include <stdio.h>
Includes the standard input-output header for using printf().

char c = 'k';
Declares a character variable c and assigns it the character 'k'.

printf("The ASCII value of %c is %d", c, c);
This line prints two representations of the same variable c:

%c → prints the character itself (in this case, 'k').

%d → treats the character as an integer and prints its ASCII (or integer) value.

 Why does %d print the ASCII value?
In C, the char type is internally stored as an integer (usually 1 byte). When %d is used, printf() interprets the char variable as an integer and shows the ASCII code for that character.

So:

'k' is a character.

Its ASCII code is 107.

%d displays that numeric value.

* example of implicit type conversion (char → int).

int ascii = c;
printf("%d", ascii);

////ASCII Values of Characters in a String
user to enter a string, and then it prints the ASCII value of each character in the string.

#include <stdio.h>

int main() {
    char str[100];

  
    printf("Enter a string: ");
    scanf("%s", str);  

    
    for (int i = 0; str[i] != '\0'; i++) {
        printf("The ASCII value of %c is %d\n", str[i], str[i]);
    }

    return 0;
}
o/p-
Enter a string: Computer-c
The ASCII value of C is 67
The ASCII value of o is 111
The ASCII value of m is 109
The ASCII value of p is 112
The ASCII value of u is 117
The ASCII value of t is 116
The ASCII value of e is 101
The ASCII value of r is 114
The ASCII value of - is 45
The ASCII value of c is 99

////C program that reads a full string including spaces and prints the ASCII value of each character, including spaces.

Using fgets-A version that supports spaces in the input string would allow the user to input full sentences or phrases, not just single words. This requires using a safer input method like fgets() instead of scanf("%s"), because scanf("%s") stops reading at the first space.

fgets() reads the entire line including spaces, unlike scanf("%s").

sizeof(str) ensures we don’t exceed the array size.

The newline character ('\n') from pressing Enter is removed/skipped.

#include <stdio.h>

int main() {
    char str[100];

    
    printf("Enter a string: ");
    fgets(str, sizeof(str), stdin);  // Reads input including spaces

    // Print ASCII values of each character
    for (int i = 0; str[i] != '\0'; i++) {
        // Skip newline character if present
        if (str[i] == '\n') {
            continue;
        }
        printf("The ASCII value of '%c' is %d\n", str[i], str[i]);
    }

    return 0;
}
O/P-
Enter a string: Intelligence is GOD!
The ASCII value of 'I' is 73
The ASCII value of 'n' is 110
The ASCII value of 't' is 116
The ASCII value of 'e' is 101
The ASCII value of 'l' is 108
The ASCII value of 'l' is 108
The ASCII value of 'i' is 105
The ASCII value of 'g' is 103
The ASCII value of 'e' is 101
The ASCII value of 'n' is 110
The ASCII value of 'c' is 99
The ASCII value of 'e' is 101
The ASCII value of ' ' is 32
The ASCII value of 'i' is 105
The ASCII value of 's' is 115
The ASCII value of ' ' is 32
The ASCII value of 'G' is 71
The ASCII value of 'O' is 79
The ASCII value of 'D' is 68
The ASCII value of '!' is 33





//representation of integer constants on 16-bit machine

This C program demonstrates how integer constants are represented and handled on a 16-bit machine, particularly focusing on the difference between default int and explicitly declared long int values.

1. 16-bit Machine Integer Limits
On a 16-bit machine:

A standard int is typically 16 bits, which can store values from:

-32,768 to 32,767 (-2¹⁵ to 2¹⁵ - 1)

A long int is usually 32 bits, allowing values from:

-2,147,483,648 to 2,147,483,647

Explanation of Each printf() Section
🔹 printf("%d %d %d\n", 32767, 32767+1, 32767+10);
%d → prints values as int

Values:

32767 → Maximum value for int on a 16-bit machine.

32767 + 1 = 32768 → Overflow, but modern compilers may promote it to int or long as needed.

32767 + 10 = 32777 → Still printed fine because of compiler's internal promotion.

📌 Note: On some strict 16-bit compilers, this might cause overflow and wraparound, giving incorrect/negative results.
🔹 printf("%ld %ld %ld\n", 32767L, 32767L+1L, 32767L+10L);
%ld → prints values as long int

Appending L to a number tells the compiler it's a long literal.

No overflow occurs because long is 32-bit even on most 16-bit compilers.

Output: 32767 32768 32777 → All safe within the long range.

⚙️ How It Works Internally
Expression	   Type  	Output	   Notes
32767	            int  	32767	   Within 16-bit int limit
32767 + 1	    int	        32768	   May overflow on strict 16-bit compilers
32767L + 10L	    long	32777	   Safe, because it's using long integers





#include<stdio.h>

int main()
{
    printf("integer values\n\n");
    printf("%d %d %d\n", 32767, 32767+1, 32767+10);
    
    printf("\n");
    
    printf("long integer values\n\n");
    printf("%ld %ld %ld\n",32767L,32767L+1L,32767L+10L);
    
}
Op-
integer values

32767 32768 32777

long integer values

32767 32768 32777

Summary of Key Points
Integer overflow can occur if constants exceed their type's limit.

Use L suffix for long constants to avoid overflow in critical ranges.

%d for int, %ld for long.

On a true 16-bit compiler, you might see incorrect results (like negative values) without using long.

////// C Program for Checking value is  Prime or not
//Input the number n.

*Check if n is less than or equal to 1:

*If yes, it is not a prime.

*Count how many numbers divide n exactly (i.e., n % i == 0).

*If n has more than 2 divisors, it is not prime.

*A prime number has exactly 2 divisors: 1 and n itself.
#include <stdbool.h>
#include <stdio.h>

int main() {
    int n ;
    printf("enter a value to find prime or not:");
    scanf("%d", &n);

    int cnt = 0;

    
    if (n <= 1)
        printf("%d is NOT prime\n", n);
    else {

        
        for (int i = 1; i <= n; i++) {

            
            if (n % i == 0)
                cnt++;
        }

        
        if (cnt > 2)
            printf("%d is NOT prime\n", n);

    
        else
            printf("%d is prime", n);
    }

    return 0;
}

////To find GCD of 2,3,4,n numbers given, taken by the user.
This function uses the Euclidean algorithm to compute the GCD of two integers:

If the second number b is 0, return a (base case).

Otherwise, recursively call gcd(b, a % b)
Accepts an array nums[] of size n.

Initializes the result with the first element.

Iteratively computes GCD of the result with each of the remaining elements.

Returns the final GCD of all numbers.
This program takes any number of integers from the user and finds their Greatest Common Divisor (GCD) using a combination of recursion and iteration.
#include <stdio.h>

// Function to calculate GCD of two numbers
int gcd(int a, int b) {
    if (b == 0)
        return a;
    return gcd(b, a % b);
}

// Function to calculate GCD of multiple numbers
int gcd_multiple(int nums[], int n) {
    int result = nums[0];
    for (int i = 1; i < n; i++) {
        result = gcd(result, nums[i]);
    }
    return result;
}

int main() {
    int n;
    printf("Enter the number of digits: ");
    scanf("%d", &n);

    int nums[n];
    printf("Enter %d numbers: ", n);
    for (int i = 0; i < n; i++) {
        scanf("%d", &nums[i]);
    }

    int result = gcd_multiple(nums, n);
    printf("GCD of the numbers is: %d\n", result);

    return 0;
}

/////c program to print armstrong number
*An Armstrong number (also known as a narcissistic number, pluperfect number, or pluperfect digital invariant) is a number that is equal to the sum of its own digits each raised to the power of the number of digits.

*Example-
153 = 1^3+5^3+3^3=1+125+27
9474=9^4+4^4+7^4+4^4=6561+256+2401+256


#include <stdio.h>
#include <math.h>

int main() {
    int num, remainder, digits = 0;
    double result = 0.0;

    printf("Enter a number: ");
    scanf("%d", &num);

    

    // Count number of digits
    int temp = num;
    while (temp != 0) {
        temp /= 10;
        digits++;
    }

    temp = num;
    // Calculate sum of each digit raised to the power of number of digits
    while (temp != 0) {
        remainder = temp % 10;
        result += pow(remainder, digits);
        temp /= 10;
    }

    // Compare result with original number
    if ((int)result == num)
        printf("%d is an Armstrong number.\n", num);
    else
        printf("%d is not an Armstrong number.\n", num);

    return 0;
}

o/p-
1)Enter a number: 8208
8208 is an Armstrong number.
2)Enter a number: 9474
9474 is an Armstrong number.
3)Enter a number: 153
153 is an Armstrong number.
4)Enter a number: 371
371 is an Armstrong number.
5)Enter a number: 2222
2222 is not an Armstrong number.
6)Enter a number: 632
632 is not an Armstrong number.

*This program:

Counts the digits in a number,

Calculates the sum of its digits each raised to the power of the number of digits,

Compares that sum to the original number,

Declares whether it is an Armstrong number.
in program-
num stores the user input number.

remainder stores each digit during extraction.

digits keeps track of the number of digits.

result accumulates the sum of each digit raised to the power of the number of digits (can be a decimal, hence double).
A copy of the number is stored in temp.

A while loop divides temp by 10 repeatedly to count how many digits the number has.
Reset temp to the original number.

Extract each digit using % 10.

Raise the digit to the power of the total number of digits using pow().

Add the result to the result variable.

Repeat until all digits are processed.
Converts result to an integer and compares it with the original number.

If they match, it prints that the number is an Armstrong number.

Otherwise, it prints that it is not.






//to print ASCII values use  apostrophe
//here a is not equal to 'a'
//'a' will give the ASCII value of letter a



#include<stdio.h>

int main()
{
    printf("%d",'a'); 
     
    return 0;
}
Op-97



//use of prompt message i.e., using printf and scanf



#include<stdio.h>
int main()
{
    int n;
    printf("enter a number:\n");
    scanf("%d",&n);
    
    if(n<100)
    {
        printf("the number is less than 100!");
    }
    else
    {
        printf("the number contains more than two digits!");
    }
    
    return 0;
}
Op-
enter a number:
666
the number contains more than two digits!




//declarations, assignmentsand values stores in various types of variables.
Concept Behind the Program
Data Type Size & Precision:

float is less precise (~6-7 digits).

double is more precise (~15-16 digits).

int and long int differ in range.

Memory Storage & Truncation:

When assigning a long decimal number to a float, it may lose accuracy beyond 6-7 digits.

double preserves more digits after the decimal point.

Chained Assignment:

p = q = 1.0; assigns the same value to both variables in one line.

Format Specifiers:

%d for int

%ld for long int

%f for float

%.12lf for printing up to 12 decimal places in double

%u for unsigned int

This program demonstrates how different data types store and print values, especially focusing on precision and formatting.


#include<stdio.h>

int main()
{
    float x,p;
    double y,q;
    unsigned k;
    
    int m=54321;
    long int n=1234567890;
    
    x=1.234567890000;
    y=9.87654321;
    k=54321;
    p=q=1.0;
    
    
    printf("m=%d\n",m);
    printf("n=%ld\n",n);
    printf("x=%.12lf\n",x);
    printf("x=%f\n",x);
    printf("y=%.12lf\n",y);
    printf("y=%f\n",y);
    printf("k=%u  p=%f  q=%.12lf\n",k,p,q);
    
    return 0;
    
}
Op-
m=54321
n=1234567890
x=1.234567880630
x=1.234568
y=9.876543210000
y=9.876543
k=54321  p=1.000000  q=1.000000000000

Note:
float x, p; — declares two floating-point variables with single precision (typically 6–7 digits).

double y, q; — declares two floating-point variables with double precision (typically up to 15–16 digits).

unsigned k; — declares an unsigned integer (no negative values).

int m = 54321; — standard 4-byte signed integer.

long int n = 1234567890; — larger range integer (commonly 8 bytes on modern systems).

x is assigned a float value with many digits, but due to float precision, it may lose some accuracy.

y is a double and retains more digits accurately.

k is assigned a positive value that fits within the unsigned int range.

p = q = 1.0; — Both variables p and q are assigned the value 1.0 using chained assignment.

*Type Casting and Implicit Conversion*
The program also illustrates implicit type conversion when variables are passed to printf()—for example, the float x is promoted to double automatically when printed with %f or %.12lf, as per the default promotion rules in C.

This behavior helps explain why float values may sometimes appear more precise in output than they actually are in memory, highlighting the importance of understanding how the compiler handles type promotion and formatting internally.




/////printing even number between 1-100


#include<stdio.h>

int main()
{
    printf("The even numbers between 1 to 100 are:\n");
    for(int i=1;i<=100;i++)
    {
        if(i%2==0)
        {
            printf("%d\n",i);
        }
        
        
        
    }
}

(or)
//without using if
#include <stdio.h>

int main()
{
    printf("The even numbers between 1 to 100 are:\n");
    for(int i = 2; i <= 100; i += 2)
    {
        printf("%d\n", i);
    }
    return 0;
}
The loop starts from i = 2, which is the first even number in the range.

Instead of increasing i by 1, we increment it by 2, so it directly goes to the next even number (e.g., 2, 4, 6, ...).

This removes the need for the if(i % 2 == 0) check, making the code more efficient.
Header File <stdio.h>: Includes standard input/output functions like printf().

Main Function main(): This is the starting point of program execution.

Looping with for: Repeats a block of code for a specific range (i = 2 to 100).

Initialization: Starts from 2 (the first even number).

Condition i <= 100: Ensures the loop runs until 100.

Increment by 2 (i += 2): Skips odd numbers and directly moves to the next even.

printf(): Prints each even number on a new line.

Efficient Approach: Avoids unnecessary condition checks, improving performance.

//C Program: Store and Print Even Numbers in an Array
#include <stdio.h>

int main()
{
    int evenNumbers[50]; // There are 50 even numbers between 1 and 100
    int index = 0;

    // Storing even numbers in the array
    for(int i = 2; i <= 100; i += 2)
    {
        evenNumbers[index] = i;
        index++;
    }

    // Printing even numbers from the array
    printf("The even numbers between 1 and 100 are:\n");
    for(int i = 0; i < index; i++)
    {
        printf("%d\n", evenNumbers[i]);
    }

    // Displaying total count
    printf("Total even numbers between 1 and 100: %d\n", index);

    return 0;
}
int evenNumbers[50]; — Creates an array to store the 50 even numbers between 1 and 100.

index keeps track of where to insert the next even number.

After storing, a second loop prints the stored numbers.

Finally, it prints how many even numbers were found.
Array Declaration: Used to store multiple values of the same type — here, 50 even integers.

Looping with Step Size 2: Efficiently generates only even numbers (2, 4, ..., 100).

Indexing: Tracks array positions where numbers are stored.

Two Loops: One for storing values, another for displaying them.

Separation of Logic: Storing and printing are kept separate for clarity and flexibility.

Memory Efficiency: Fixed-size array as we know in advance there are 50 even numbers.

Total Count Output: Helpful for verification or further processing.

Modular Structure: Easy to modify for other ranges or conditions.





Programming exercise (chapter 1)


//1.1equation of line ax+by=c

This C program prints a linear equation in the form:

ax+by=c
In mathematics, the general equation of a straight line in two dimensions is often written as:
ax+by=c
a, b, and c are constants (integers in this case).

x and y are variables representing coordinates on a 2D plane.

This is a standard form of a linear equation in two variables.
The program simply:

Declares and initializes integers a = 5, b = 8, and c = 18.

Uses printf to format and print the equation.
%d is a format specifier for integers.

The variables are inserted into the equation using printf.


#include<stdio.h>

int main()
{
    int a=5,b=8,c=18;
    
    
    
    printf("%dx + %dy = %d",a,b,c);
    
    return 0;
}

o/p-5x + 8y = 18
////program where the user inputs the values of a, b, and c to display the equation of the line for the above question:

#include <stdio.h>

int main()
{
    int a, b, c;

    // Prompting user to enter coefficients
    printf("Enter the value of a: ");
    scanf("%d", &a);

    printf("Enter the value of b: ");
    scanf("%d", &b);

    printf("Enter the value of c: ");
    scanf("%d", &c);

    // Displaying the linear equation
    printf("The equation of the line is: %dx + %dy = %d\n", a, b, c);

    return 0;
}


////enhance the above program of straight line into a slope-intercept form
ax+by=c into slope intercept form y=mx+c0 where m=-a/b(slope) and c0=c/b(y intercept)

#include <stdio.h>

int main()
{
    float a, b, c;

    // Input coefficients
    printf("Enter the value of a: ");
    scanf("%f", &a);

    printf("Enter the value of b: ");
    scanf("%f", &b);

    printf("Enter the value of c: ");
    scanf("%f", &c);

    // Print standard form
    printf("\nStandard form: %.2fx + %.2fy = %.2f\n", a, b, c);

    // Avoid division by zero
    if (b == 0)
    {
        printf("Cannot convert to y = mx + c form (division by zero).\n");
    }
    else
    {
        float m = -a / b;
        float c0 = c / b;
        printf("Slope-intercept form: y = %.2fx + %.2f\n", m, c0);
    }

    return 0;
}
o/p-
Enter the value of a: 1
Enter the value of b: 2
Enter the value of c: 3

Standard form: 1.00x + 2.00y = 3.00
Slope-intercept form: y = -0.50x + 1.50







//1.2 mailing address in the following form

This C program is a simple example of how to store and display a mailing address using string variables and printf() statements. 
This is a basic I/O (Input/Output) task in C using character arrays (strings) and the printf function



#include <stdio.h>

int main() {
    // Variables to store address components
    char name[] = "Krishna Singh";
    char doorNo[] = "123";
    char street[] = "Jawaharnagar";
    char city[] = "vskp";
    char pinCode[] = "12345";

    // Printing the mailing address
    printf("Name: %s\n", name);
    printf("door no.,street: %s, %s\n", doorNo, street);
    printf("City: %s - %s\n", city, pinCode);

    return 0;
}
o/p-Name: Krishna Singh
door no.,street: 123, Jawaharnagar
City: vskp – 12345
//update of the above program-mailing address program that takes user input using scanf() instead of using hardcoded values.
#include <stdio.h>

int main() {
    // Character arrays to store address components
    char name[50];
    char doorNo[10];
    char street[50];
    char city[30];
    char pinCode[10];

    // Taking input from user
    printf("Enter your name: ");
    fgets(name, sizeof(name), stdin); // To allow full name with spaces

    printf("Enter door number: ");
    scanf("%s", doorNo);

    printf("Enter street name: ");
    scanf("%s", street); // This will stop at the first space

    printf("Enter city name: ");
    scanf("%s", city);

    printf("Enter pin code: ");
    scanf("%s", pinCode);

    // Printing the mailing address
    printf("\n--- Mailing Address ---\n");
    printf("Name: %s", name); // Already has \n if entered via fgets
    printf("door no.,street: %s, %s\n", doorNo, street);
    printf("City: %s - %s\n", city, pinCode);

    return 0;
}
note:
fgets() is used for name to allow spaces in full names.

scanf() is used for other fields where spaces are usually not expected.

note:
 To handle spaces in all input fields like full name, street name, and city name, we’ll use fgets() instead of scanf() for string input. 
 #include <stdio.h>

int main() {
    // Character arrays to store address components
    char name[50];
    char doorNo[10];
    char street[50];
    char city[30];
    char pinCode[10];

    // Taking input from user
    printf("Enter your name: ");
    fgets(name, sizeof(name), stdin);

    printf("Enter door number: ");
    fgets(doorNo, sizeof(doorNo), stdin);

    printf("Enter street name: ");
    fgets(street, sizeof(street), stdin);

    printf("Enter city name: ");
    fgets(city, sizeof(city), stdin);

    printf("Enter pin code: ");
    fgets(pinCode, sizeof(pinCode), stdin);

    // Printing the mailing address
    printf("\n--- Mailing Address ---\n");
    printf("Name: %s", name);
    printf("door no.,street: %s, %s", doorNo, street);
    printf("City: %s - %s", city, pinCode);

    return 0;
}
(or)
note: above program with newline removal logic using a helper function, so  mailing address prints cleanly without extra blank lines or unwanted \n characters
#include <stdio.h>
#include <string.h>

// Helper function to remove trailing newline from fgets input
void removeNewline(char *str) {
    int len = strlen(str);
    if (len > 0 && str[len - 1] == '\n') {
        str[len - 1] = '\0';
    }
}

int main() {
    // Character arrays to store address components
    char name[50];
    char doorNo[10];
    char street[50];
    char city[30];
    char pinCode[10];

    // Taking input from user
    printf("Enter your name: ");
    fgets(name, sizeof(name), stdin);
    removeNewline(name);

    printf("Enter door number: ");
    fgets(doorNo, sizeof(doorNo), stdin);
    removeNewline(doorNo);

    printf("Enter street name: ");
    fgets(street, sizeof(street), stdin);
    removeNewline(street);

    printf("Enter city name: ");
    fgets(city, sizeof(city), stdin);
    removeNewline(city);

    printf("Enter pin code: ");
    fgets(pinCode, sizeof(pinCode), stdin);
    removeNewline(pinCode);

    // Printing the mailing address
    printf("\n--- Mailing Address ---\n");
    printf("Name: %s\n", name);
    printf("door no.,street: %s, %s\n", doorNo, street);
    printf("City: %s - %s\n", city, pinCode);

    return 0;
}
o/p-
Enter your name: Krishna Singh
Enter door number: 123
Enter street name: Jawahar Nagar
Enter city name: Visakhapatnam
Enter pin code: 530002

--- Mailing Address ---
Name: Krishna Singh
door no.,street: 123, Jawahar Nagar
City: Visakhapatnam - 530002




//1.3 multiplication table 
prints the multiplication table of a given number n from 1 to 10:



#include<stdio.h>

int main()
{
    int n,i;
    printf("enter the value of n:\n");
    scanf("%d",&n);
    for(i=1;i<11;++i)
    {
       printf("\n%d X %d = %d",n,i,n*i);
    }
    
    
}
o/p-
enter the value of n:
5

5 X 1 = 5
5 X 2 = 10
5 X 3 = 15
5 X 4 = 20
5 X 5 = 25
5 X 6 = 30
5 X 7 = 35
5 X 8 = 40
5 X 9 = 45
5 X 10 = 50

//above program but this time prints multiplication tables from 1 to n, each up to 10.

#include<stdio.h>

int main()
{
    int n, i, j;
    printf("Enter the limit n (to print tables from 1 to n):\n");
    scanf("%d", &n);

    for(i = 1; i <= n; ++i)
    {
        printf("\nMultiplication Table of %d:\n", i);
        for(j = 1; j <= 10; ++j)
        {
            printf("%d X %d = %d\n", i, j, i * j);
        }
    }

    return 0;
}




//diagonal to zero

#include<stdio.h>
#define S 5

int main()
{
    
    int i,j;
    int a[S][S];
    for(i=0;i<S;i++)
    {
        for(j=0;j<S;j++)
        {
            a[i][j]=((i==j)?1:0);
        }
    }
    printf("the elements are:\n");
    for(i=0;i<5;i++)
    {
        for(j=0;j<5;j++)
        {
            printf("%d",a[i][j]);
        }
        printf("\n");
    }
    return 0;
    
}
o/p-
the elements are:
10000
01000
00100
00010
00001
note:
The program creates a 5×5 identity matrix using nested for loops.

* The main diagonal elements (where i == j) are set to 1; all others are set to 0.

* Uses the ternary operator:
(i == j) ? 1 : 0 → means “if i == j, store 1, else store 0”.

* The matrix is then printed row-by-row without spaces between elements.

* This is a good example of how 2D arrays and conditional logic are used to form structured patterns in C.


//given the values of three variables a,b and c, wirte a c program to compute and display the value of x, where x=a/b-c. execute your program for the following values: a)a=250 ,b=85,c=25. b)a=300, b=70, c=70


#include<stdio.h>

int main()
{
    int a,b,c;
    float x;
    
    printf("Test case 1\n");
    
    a=250;
    b=85;
    c=25;
    x=(float)(a/(b-c));
    printf("For a=%d, b=%d, c=%d, x=%.2f\n",a,b,c,x);
    
    printf("Test case 2\n");
    
    a=300;
    b=70;
    c=70;
    x=(float)a/b-c;
    printf("For a=%d, b=%d, c=%d ,x=%.4f",a,b,c,x);
    
    
}
Output-
Test case 1
For a=250, b=85, c=25, x=4.00
Test case 2
For a=300, b=70, c=70 ,x=-65.7143




//relationship between celsius and fahrenheit is governed by the formula F=9C/5+32. write a c program to convert the temperature a)from Celsius to Fahrenheit and b) From Fahrenheit to Celsius

Concept of the Program
Purpose:
The program converts temperature:

From Celsius to Fahrenheit, or

From Fahrenheit to Celsius
Based on the user's choice.

Formula Used:

To convert Celsius to Fahrenheit: F = (9.0/5.0) * C + 32

To convert Fahrenheit to Celsius: C = (5.0/9.0) * (F - 32)

User Interaction:

The user is prompted to enter a choice:

1 for Celsius to Fahrenheit

2 for Fahrenheit to Celsius

Input Handling:

Based on the user’s choice, the program asks for the relevant temperature input.

Computation:

The program performs the conversion using floating-point arithmetic for better precision.

Output:

It displays the converted temperature result.

Validation:

If the user enters an invalid choice (not 1 or 2), it prints "invalid choice".





#include <stdio.h>

int main()
{
    float c,F;
    int choice;
    
    printf("enter a choice 1,2:\n");
    scanf("%d",&choice);
    
    if(choice==1)
    {
        printf("Enter the celsius tempterature:\n");
        scanf("%f",&c);
        F=(9.0/5.0)*c+32;
        printf("the converted c to F is %f",F);
    }
    else if(choice==2)
    {
        printf("Enter the Farhenheit temperature:\n");
        scanf("%f",&F);
        c=(5.0/9.0)*(F-32);
        printf("the f to c temperature is %f",c);
    }
    else
    {
        printf("invalid choice");
    }
    
}
(or)
using menu based version-
#include <stdio.h>

int main() {
    float celsius, fahrenheit;
    int choice;

    printf("=== Temperature Converter ===\n");
    printf("1. Celsius to Fahrenheit\n");
    printf("2. Fahrenheit to Celsius\n");
    printf("Enter your choice (1 or 2): ");
    scanf("%d", &choice);

    switch (choice) {
        case 1:
            printf("\nEnter temperature in Celsius: ");
            scanf("%f", &celsius);
            fahrenheit = (9.0 / 5.0) * celsius + 32;
            printf("Temperature in Fahrenheit: %.2f°F\n", fahrenheit);
            break;

        case 2:
            printf("\nEnter temperature in Fahrenheit: ");
            scanf("%f", &fahrenheit);
            celsius = (5.0 / 9.0) * (fahrenheit - 32);
            printf("Temperature in Celsius: %.2f°C\n", celsius);
            break;

        default:
            printf("\nInvalid choice. Please enter 1 or 2.\n");
    }

    return 0;
}
(or)
the loop enabled version-allows the user to use multiple conversion until they chose exit
#include <stdio.h>

int main() {
    float celsius, fahrenheit;
    int choice;

    do {
        // Display menu
        printf("\n=== Temperature Converter ===\n");
        printf("1. Celsius to Fahrenheit\n");
        printf("2. Fahrenheit to Celsius\n");
        printf("3. Exit\n");
        printf("Enter your choice (1, 2, or 3): ");
        scanf("%d", &choice);

        switch (choice) {
            case 1:
                printf("Enter temperature in Celsius: ");
                scanf("%f", &celsius);
                fahrenheit = (9.0 / 5.0) * celsius + 32;
                printf("Temperature in Fahrenheit: %.2f°F\n", fahrenheit);
                break;

            case 2:
                printf("Enter temperature in Fahrenheit: ");
                scanf("%f", &fahrenheit);
                celsius = (5.0 / 9.0) * (fahrenheit - 32);
                printf("Temperature in Celsius: %.2f°C\n", celsius);
                break;

            case 3:
                printf("Exiting the program. Goodbye!\n");
                break;

            default:
                printf("Invalid choice. Please enter 1, 2, or 3.\n");
        }

    } while (choice != 3);

    return 0;
}




//given the radius of a circle, write a program to compute and display its area. Use a symbolic constant to define the pi value and assume a suitable value for radius


#include <stdio.h>
#define PI 3.14

int main()
{
    int r;
    float ar;
    
    printf("Enter the radius of the cirlce:\n");
    scanf("%d",&r);
    ar=PI*r*r;
    printf("The area of the circle is: %f",ar);
    
    }

    

//Given two integers 20 and 10, write a c program that uses a function add() to add these two numbers and sub() to find the difference of these two numbers and then  display the sum and difference in the following form:
20+10=30
20-10=10


#include<stdio.h>

int add(int a, int b)
{
    return a+b;
}
int sub(int a, int b)
{
    return a-b;
}
int main()
{
    int x=20,y=10;
    
    int ad=add(x,y);
    int sb=sub(x,y);
    printf("************************\n");
    printf("*%d + %d = %d*\n",x,y,ad);
    printf("*%d - %d = %d*\n",x,y,sb);
    
    printf("************************\n");
    
    return 0;
}
////Pattern questions concept:
 In C programming, pattern printing is a popular exercise to improve understanding of loops, nested loops, and logic
 1. Understand the Pattern Visually
First, draw the pattern on paper.

Identify:

How many rows are there?

What is printed in each column?

How does each row differ from the previous one?

2. Decide the Loop Structure
Most patterns use nested loops:

Outer loop controls the rows.

Inner loop(s) control the columns (what to print in each row).
for (int i = 1; i <= n; i++) {        // outer loop for rows
    for (int j = 1; j <= some_value; j++) { // inner loop for columns
        // print logic
    }
    printf("\n");  // new line after each row
}
3. Figure Out What to Print
Is it a number? A character? A *?

Does it increment, decrement, or stay constant?

Use conditions or expressions like:

printf("* ")

printf("%d ", j)

printf("%c ", 'A' + j - 1)
4. Handle Spaces for Alignment (if needed)
For triangle/pyramid patterns, you often need leading spaces.

Use another inner loop:
for (int s = 1; s <= n - i; s++) {
    printf(" ");
}
5. Test for Small Values (like n = 3 or 4)
Helps you debug and verify the loop logic easily.

*If star patterns then understand nested loops
*Number patterns->print increasing/decreasing number
*Alphabet patterns->ASCII values and loop logic
*Pyramid/Right-Aligned->Use of spaces for formatting
*Pascal’s Triangle->Binomial coefficient logic
*Start simple: single loops, then nested.
*For right-aligned triangles or pyramids, use space-padding.
*Use variables wisely (like i, j, counters).
*Comment your loops during practice to track behavior.

//print the pattern 

*****
*****
*****
*****


#include<stdio.h>

int main()

{
    int i,j;
    for(i=1;i<=5;i++)
    {
        for(j=1;j<=5;j++)
        {
            printf("*");
        }
        printf("\n");
    }
    return 0;
}


//print the pattern
*
**
***
****
*****


#include<stdio.h>

int main()

{
    int i,j;
    for(i=1;i<=5;i++)
    {
        for(j=1;j<=i;j++)
        {
            printf("*");
        }
        printf("\n");
    }
    return 0;
}


//print the pattern

*****
****
***
**
*


#include<stdio.h>

int main()

{
    int i,j;
    for(i=1;i<=5;i++)
    {
        for(j=5;j>=i;j--)
        {
            printf("*");
        }
        printf("\n");
    }
}

(or)

#include<stdio.h>

int main()
{
    int i,j;
    for(i=5;i>=1;i--)
    {
        for(j=1;j<=i;j++)
        {
            printf("*");
        }
        printf("\n");
    }
}


//print the pattern
1
12
123
1234
12345
123456
1234567
12345678
123456789
12345678910


#include<stdio.h>

int main()
{
    int i,j;
    for(i=1;i<=10;i++)
    {
        for(j=1;j<=i;j++)
        {
            printf("%d",j);
        }
        printf("\n");
    }
}


//print the pattern
654321
65432
6543
654
65
6


#include<stdio.h>

int main()
{
    int  i,j;
    for(i=1;i<=6;i++)
    {
        for(j=6;j>=i;j--)
        {
            printf("%d",j);
        }
        printf("\n");
    }
}


//print the pattern
123456
12345
1234
123
12
1


#include<stdio.h>

int main()
{
    int  i,j;
    for(i=6;i>=1;i--)
    {
        for(j=1;j<=i;j++)
        {
            printf("%d",j);
        }
        printf("\n");
    }
}


//print the pattern
      *
    **
   ***
  ****
 *****
******


#include<stdio.h>

int main()
{
    int i,j;
    for(i=1;i<=6;i++)
    {
        for(j=1;j<=6;j++)
        {
            if((i+j)<=6)
            printf(" ");
            else
            printf("*");
        }
        printf("\n");
    }
}



//Print the pattern
1
22
333
4444
55555
666666


#include<stdio.h>

int main()
{
    int i,j;
    for(i=1;i<=6;i++)
    {
        for(j=1;j<=i;j++)
        {
            printf("%d",i);
        }
        printf("\n");
    }
}



//print the pattern
1 
 2  3 
 4  5  6 
 7  8  9  10 
 11  12  13  14  15 
 16  17  18  19  20  21


#include<stdio.h>

int main()
{
    int i,j,n=1;
    for(i=1;i<=6;i++)
    {
        for(j=1;j<=i;j++)
        {
            printf(" %d ",n);
            n++;
        }
        printf("\n");
    }
}


//Print the pattern
     * 
    * * 
   * * * 
  * * * * 
 * * * * * 
* * * * * *


#include<stdio.h>

int main()
{
    int i,j,sp;
    for(i=1;i<=6;i++)
    {
        for(sp=1;sp<=(6-i);sp++)
        {
            printf(" ");
        }
        for(j=1;j<=i;j++)
        {
            printf("* ");
        }
        printf("\n");
    }
}


//print the pattern
      *
    ***
   *****
  *******
 *********
***********


#include<stdio.h>

int main()
{
    int i,j,sp;
    for(i=1;i<=6;i++)
    {
        for(sp=1;sp<=(6-i);sp++)
        {
            printf(" ");
        }
        for(j=1;j<=(2*i-1);j++)
        {
            printf("*");
        }
        printf("\n");
    }
}


//print the pattern
***********
 *********
  *******
   *****
    ***
      *


#include<stdio.h>

int main()
{
    int i,j,sp;
    for(i=6;i>=1;i--)
    {
        for(sp=1;sp<=(6-i);sp++)
        {
            printf(" ");
        }
        for(j=1;j<=(2*i-1);j++)
        {
            printf("*");
        }
        printf("\n");
    }
}


//print the pattern
    *
    ***
   *****
  *******
 *********
***********
 *********
  *******
   *****
    ***
     *

     
#include<stdio.h>

int main()
{
    int i,j,sp;
    for(i=1;i<=6;i++)
    {
        for(sp=1;sp<=(6-i);sp++)
        {
            printf(" ");
        }
        for(j=1;j<=(2*i-1);j++)
        {
            printf("*");
        }
        printf("\n");
    }
    for(i=6-1;i>=1;i--)
    {
        for(sp=1;sp<=(6-i);sp++)
        {
            printf(" ");
        }
        for(j=1;j<=(2*i-1);j++)
        {
            printf("*");
        }
        printf("\n");
    }
}


//print pattern

*
**
***
****
*****
******
*****
****
***
**
*


#include<stdio.h>

int main()
{
    int i,j;
    for(i=1;i<=6;i++)
    {
        for(j=1;j<=i;j++)
        {
            printf("*");
        }
        printf("\n");
        
    }
    for(i=6-1;i>=1;i--)
    {
        for(j=1;j<=i;j++)
        {
            printf("*");
        }
        printf("\n");
    }
}


//print the pattern 
A
AB
ABC
ABCD
ABCDE
ABCDEF


#include<stdio.h>

int main()
{
    int i,j;
    for(i=1;i<=6;i++)
    {
        for(j=1;j<=i;j++)
        {
            printf("%c",64+j);
        }
        printf("\n");
    }
}


//print the pattern

ABCDEF
ABCDE
ABCD
ABC
AB
A


include<stdio.h>

int main()
{
    int i,j;
    for(i=6;i>=1;i--)
    {
        for(j=1;j<=i;j++)
        {
            printf("%c",64+j);
        }
        printf("\n");
    }
}



//print the pattern
A
BB
CCC
DDDD
EEEEE


#include<stdio.h>

int main()
{
    int i,j;
    for(i=1;i<=5;i++)
    {
        for(j=1;j<=i;j++)
        {
            printf("%c",64+i);
        }
        printf("\n");
    }
}



//print the pattern
EEEEE
DDDD
CCC
BB
A


#include<stdio.h>
int main()
{
    int i,j;
    for(i=5;i>=1;i--)
    {
        for(j=1;j<=i;j++)
        {
            printf("%c",64+i);
        }
        printf("\n");
    }
}


1.10 program to print the following figure using suitable characters.
 
//using printf

#include <stdio.h>

int main()
{
    printf("---------           ---------\n");
    printf("|       |           |       |\n");
    printf("|       |           |       |\n");
    printf("|       | >>----->  |       |\n");
    printf("|       |           |       |\n");
    printf("|       |           |       |\n");
    printf("---------           ---------\n");
    
    
}

//without using printf

#include <stdio.h>

int main() {
    // Define the width of each box
    int box_width = 20;

    // Top and bottom of boxes
    for (int i = 0; i < 1; i++) { 
        for (int j = 0; j < box_width; j++) {
            printf("-");
        }
        printf("          "); 
        for (int j = 0; j < box_width; j++) {
            printf("-");
        }
        printf("\n");
    }

    // Sides of boxes
    for (int i = 0; i < 3; i++) { 
        printf("|");
        for (int j = 0; j < box_width - 2; j++) {
            printf(" ");
        }
        printf("|          |");
        for (int j = 0; j < box_width - 2; j++) {
            printf(" ");
        }
        printf("|\n");
    }

    // Arrow in the middle
    printf("|");
    for (int j = 0; j < box_width - 2; j++) {
        printf(" ");
    }
    printf("| >>-----> |");
    for (int j = 0; j < box_width - 2; j++) {
        printf(" ");
    }
    printf("|\n");

    // Sides of boxes (continued)
    for (int i = 0; i < 2; i++) { 
        printf("|");
        for (int j = 0; j < box_width - 2; j++) {
            printf(" ");
        }
        printf("|          |");
        for (int j = 0; j < box_width - 2; j++) {
            printf(" ");
        }
        printf("|\n");
    }

    // Top and bottom of boxes
    for (int i = 0; i < 1; i++) { 
        for (int j = 0; j < box_width; j++) {
            printf("-");
        }
        printf("          "); 
        for (int j = 0; j < box_width; j++) {
            printf("-");
        }
        printf("\n");
    }

    return 0;
}


//aarea of triangle is given by the formula A=square root of s(s-a)(s-b)(s-c) where a,b and c are sides of the triangle and 2s = a+b+c. write a program to compute the area of the triangle given the values of a,b and c. 


#include<stdio.h>
#include<math.h>


int main()
{
    float a,b,c,s,Ar;
    printf("Please enter the 3 values of sides of a triangle:\n");
    scanf("%f\n%f\n%f",&a,&b,&c);
    s=(a+b+c)/2;
    Ar=sqrt(s*(s-a)*(s-b)*(s-c));
    printf("the area of the triangle is : %.2f",Ar);
    
    return 0;
}


//write a c program to display the following simple arithmetic calculator: x=__,y=__,sum=__,difference=__, product=__,division=___



#include<stdio.h>

int main()
{
    printf("------------Simple Calculator-----------\n");
    printf("x=[ ]      y=[ ]");
    printf("\nsum=[ ]");
    printf("\nproduct=[ ]");
    printf("\ndifference=[ ]");
    printf("\ndivision=[ ]");
    int x,y,sum,dif,p;
    float div;
    printf("\nenter the value of x and y:\n");
    scanf("%d\n%d",&x,&y);
    sum=x+y;
    dif=x-y;
    p=x*y;
    div=x/y;
    printf("-------------------------------------------\n");
    printf("x=[ %d ]      y=[ %d ]\n",x,y);
    printf("sum=[ %d ]\n",sum);
    printf("product=[ %d ]\n",p);
    printf("difference=[ %d ]\n",dif);
    printf("division=[ %f ]\n",div);
    return 0;
    
    
}


//distance between two points (x1,y1)and (x2,y2) is governed by the formula D^2=(x2-x1)^2+(y2-y1)^2. write a program to compute the D given the coordinates of the points.


#include <stdio.h>
#include <math.h>

int main() {
    float x1, y1, x2, y2, distance;

    // Get coordinates from the user
    printf("Enter coordinates of point 1 (x1, y1): ");
    scanf("%f %f", &x1, &y1);

    printf("Enter coordinates of point 2 (x2, y2): ");
    scanf("%f %f", &x2, &y2);

    // Calculate distance using the formula
    distance = sqrt(pow(x2 - x1, 2) + pow(y2 - y1, 2));

    // Print the calculated distance
    printf("Distance between the points: %.2f\n", distance);

    return 0;
}


//a point on the circumference of a circle whose centre is(0,0) is (4,5). write a program to compute perimeter and area of the circle.


#include <stdio.h>
#include <math.h>

#define PI 3.14159

int main() {
    int x = 4, y = 5;
    float radius, perimeter, area;

    // Calculate radius
    radius = sqrt(pow(x, 2) + pow(y, 2));

    // Calculate perimeter
    perimeter = 2 * PI * radius;

    // Calculate area
    area = PI * pow(radius, 2);

    // Print results
    printf("Radius: %.2f\n", radius);
    printf("Perimeter: %.2f\n", perimeter);
    printf("Area: %.2f\n", area);

    return 0;
}



//the line joining the points(2,2) and (5,6) which lie on the circumference of a circle is the diameter of the circle. Write a program in c to compute the area of the circle


#include <stdio.h>
#include <math.h>

int main() {
    float x1 = 2, y1 = 2;
    float x2 = 5, y2 = 6;
    float radius, diameter, area;

    // Calculate diameter (distance between points)
    diameter = sqrt(pow(x2 - x1, 2) + pow(y2 - y1, 2));

    // Calculate radius
    radius = diameter / 2;

    // Calculate area of the circle
    area = 3.14159 * radius * radius; 

    // Print the area
    printf("Area of the circle: %.2f\n", area);

    return 0;
}


//write a c program to determine and print the sum of the following harmonic series for a given value of n: 1+1/2+1/3+.......+1/n. the value of n should be given interactively through the terminal.

#include <stdio.h>

int main()
{
    int n;
    float sum=0.0;
    
    printf("enter the value of n:");
    scanf("%d",&n);
    
    if(n<0)
    {
        printf("invalid number,enter a positive number!!");
        
    }
    else{
        for(int i=1;i<=n;i++)
        {
            sum+=1.0/i;
        }
        printf("the series sum is %f",sum);
    }
    return 0;
}


//write a program to read the price of an item in decimal form (like 18.55) and print the output in paise (like 1855)

#include<stdio.h>

int main()
{
    double n;
    int convert;
    printf("enter rupees in deciaml value:");
    scanf("%lf",&n);
    convert=n*100;
    
    printf("the value in paise is: %d",convert);
    return 0;
}

//even numbers from 1 to 100
#include <stdio.h>

int main() {
    int i;

    printf("Even numbers from 1 to 100:\n");

    // Iterate through numbers from 1 to 100
    for (i = 2; i <= 100; i += 2) {
        printf("%d ", i);
    }

    printf("\n");

    return 0;
}

// write a program that requests two float type numbers from the user and then divides the first number by the second and display the result along with the numbers.
#include<stdio.h>

int main()
{
    float x,y,div;
    printf("please enter the float value of x and y:\n");
    scanf("\n%f\n%f",&x,&y);
    div=x/y;
    printf("%.2f / %.2f = %.2f", x,y,div);
}

//the price of one kg of rice is Rs16.75 and one kg of sugar is Rs15. write a c program to get these values from the user and display the prices as follows: ***list of items***\n item Price\n rice rs.16.75\n sugar rs.15.00
#include <stdio.h>

int main() {
    float rice_price, sugar_price;

    printf("Enter the price of 1 kg of rice: ");
    scanf("%f", &rice_price);

    printf("Enter the price of 1 kg of sugar: ");
    scanf("%f", &sugar_price);

    printf("\n*** List of Items ***\n");
    printf("Item\t\tPrice\n");
    printf("Rice\t\tRs.%.2f\n", rice_price);
    printf("Sugar\t\tRs.%.2f\n", sugar_price);

    return 0;
}

//write c program to count and print the number of negative and positive numbers in a given set of numbers. Test your program with a suitable set of numbers. Use Scanf to read the numbers. Reading should be terminated when the value 0 is encountered
#include <stdio.h>

int main() {
    int num, pos_count = 0, neg_count = 0;

    printf("Enter numbers (enter 0 to stop):\n");

    while (1) {
        scanf("%d", &num);

        if (num == 0) {
            break; // Exit the loop when 0 is entered
        }

        if (num > 0) {
            pos_count++;
        } else {
            neg_count++;
        }
    }

    printf("\nNumber of positive numbers: %d\n", pos_count);
    printf("Number of negative numbers: %d\n", neg_count);

    return 0;
}
//write  a c program to do the following:
a)Declare x and y as integer variables and z as a short variable
b)assign two 6 digit numbers x and y
c)assign the sum of x and y to z
d) output the values of x,y and z . comment on the output.
#include <stdio.h>
#include <limits.h>

int main() {
    int x, y;
    short z;

    // Assign 6-digit numbers to x and y
    x = 123456;
    y = 789012;

    // Calculate sum and assign to z
    z = x + y;

    printf("x: %d\n", x);
    printf("y: %d\n", y);
    printf("z: %hd\n", z); 

    // Comment on the output
    printf("\n");
    if (z == x + y) {
        printf("The sum of x and y was successfully stored in z.\n");
    } else {
        printf("Overflow occurred! The sum of x and y exceeds the range of a short integer.\n");
        printf("Expected z: %d\n", x + y);
    }

    return 0;
}

//write a program to read two floating point numbers using a scanf statement, assign their sum to an integer variable and then output the values of all the three variables.
#include <stdio.h>

int main() {
    float num1, num2;
    int sum;

    printf("Enter two floating-point numbers: ");
    scanf("%f %f", &num1, &num2);

    // Calculate sum (implicit conversion of float to int)
    sum = num1 + num2; 

    printf("First number: %.2f\n", num1);
    printf("Second number: %.2f\n", num2);
    printf("Sum (integer): %d\n", sum);

    return 0;
}

//write a program to illustrate the use of typedef declaration in a program.
#include <stdio.h>

// Define a new data type named 'DISTANCE'
typedef float DISTANCE; 

int main() {
    DISTANCE dist1, dist2, total_dist; 

    // Get input distances
    printf("Enter distance 1: ");
    scanf("%f", &dist1);

    printf("Enter distance 2: ");
    scanf("%f", &dist2);

    // Calculate total distance
    total_dist = dist1 + dist2;

    // Print results
    printf("Distance 1: %.2f\n", dist1);
    printf("Distance 2: %.2f\n", dist2);
    printf("Total Distance: %.2f\n", total_dist);

    return 0;
}

//write a program to illustrate the use of symbolic constants in a real life application.
include <stdio.h>

#define PI 3.14159

int main() {
    float radius, area;

    printf("Enter the radius of the circle: ");
    scanf("%f", &radius);

    // Calculate area using the symbolic constant PI
    area = PI * radius * radius;

    printf("Area of the circle: %.2f\n", area);

    return 0;
}

Chapter 2: Exercise programs
// Given the values of the variables x,y, and z write a program to rotate their values such that x has the value of y, y has the value of z, and z has the value of x. in c programming language
#include<stdio.h>

int main()
{
    int x=3,y=6,z=9,temp;
    printf("before swapping the values are:\n");
    printf("x=%d\ny=%d\nz=%d\n",x,y,z);
    temp=x;
    x=y;
    y=z;
    z=temp;
    printf("after swapping the values are:\n");
    printf("x=%d\ny=%d\nz=%d",x,y,z);
    return 0;
    
}

// write a program that reads a floating-point number and then displays the right-most digit of the integral part of the number
#include <stdio.h>

int main() {
    float number;
    int integral_part;
    int rightmost_digit;

    printf("Enter a floating-point number: ");
    scanf("%f", &number);

    // Extract the integral part
    integral_part = (int)number; 

    // Extract the rightmost digit
    rightmost_digit = integral_part % 10; 
    printf("the integral part is %d\n",integral_part);

    printf("The rightmost digit of the integral part is: %d\n", rightmost_digit);

    return 0;
}

// modify the above program to display the two right-most digits of the integral part of the number
#include <stdio.h>

int main() {
    float number;
    int integral_part;
    int last_two_digits;

    printf("Enter a floating-point number: ");
    scanf("%f", &number);

    // Extract the integral part
    integral_part = (int)number; 

    // Extract the last two digits
    last_two_digits = integral_part % 100; 

    printf("The last two digits of the integral part are: %d\n", last_two_digits);

    return 0;
}

//write a program that will obtain the length and width of a rectangle from the user and compute its area and perimeter.
#include <stdio.h>

int main()
{
    int l,b,area,peri;
    printf("enter the value of l and b of a rectangle:\n");
    scanf("%d\n%d",&l,&b);
    
    area=l*b;
    peri=2*(l+b);
    
    printf("the area is : %d\nthe perimeter is: %d",area,peri);
    return 0;
}
////c program : calculator using switch case

#include <stdio.h>

int main() {
    char operator;
    double num1, num2, result;

    printf("Enter an operator (+, -, *, /): ");
    scanf(" %c", &operator); 

    printf("Enter two numbers: ");
    scanf("%lf %lf", &num1, &num2);

    switch (operator) {
        case '+':
            result = num1 + num2;
            printf("Result: %.2lf\n", result);
            break;
        case '-':
            result = num1 - num2;
            printf("Result: %.2lf\n", result);
            break;
        case '*':
            result = num1 * num2;
            printf("Result: %.2lf\n", result);
            break;
        case '/':
            if (num2 != 0) {
                result = num1 / num2;
                printf("Result: %.2lf\n", result);
            } else {
                printf("Error: Division by zero is not allowed.\n");
            }
            break;
        default:
            printf("Error: Invalid operator.\n");
    }

    return 0;
}
o/p-
Enter an operator (+, -, *, /): /
Enter two numbers: 9
7
Result: 1.29


//given an integer number, write a program that displays the number as follows:
First line : all digits
Second line: all except first digit
Third line: all except first two digits 
…..
Last line: the last digit
For example, the number 5678 will be displayed as :
 5 6 7 8
6 7 8
7 8
8

#include <stdio.h>
#include <string.h>

int main() {
    int number;
    printf("Enter an integer number: ");
    scanf("%d", &number);

    // Convert the number to a string for easier manipulation
    char str[20];
    sprintf(str, "%d", number);

    // Find the length of the number
    int length = strlen(str);

    // Print each line as described
    for (int i = 0; i < length; i++) {
        for (int j = i; j < length; j++) {
            printf("%c ", str[j]);
        }
        printf("\n");
    }

    return 0;
}

//the straight-line method of computing the yearly depreciation of the value of an item is given by 
Depreciation=(Prechase price-salvage value)/years of service

Write  a c program the determine the salvage value of an item when the purchase price, years of service, and the annual depreciation are given.

#include <stdio.h>

int main() {
    double purchasePrice, annualDepreciation, salvageValue;
    int yearsOfService;

    // Input the purchase price, years of service, and annual depreciation
    printf("Enter the purchase price of the item: ");
    scanf("%lf", &purchasePrice);

    printf("Enter the years of service: ");
    scanf("%d", &yearsOfService);

    printf("Enter the annual depreciation: ");
    scanf("%lf", &annualDepreciation);

    // Calculate the salvage value
    salvageValue = purchasePrice - (annualDepreciation * yearsOfService);

    // Output the salvage value
    printf("The salvage value of the item is: %.2f\n", salvageValue);

    return 0;
}

//write a program that will read a real number from the keyboard and print the following output in one line:
smallest integer not less than the number        the given number    largest integer not greater than the number

#include <stdio.h>
#include <math.h>

int main() {
    double num;

    printf("Enter a real number: ");
    scanf("%lf", &num);

    int smallest_integer = ceil(num);
    int largest_integer = floor(num);

    printf("Smallest integer not less than the number: %d\t", smallest_integer);
    printf("The given number: %.2lf\t", num);
    printf("Largest integer not greater than the number: %d\n", largest_integer);

    return 0;
}

//the total distance travelled by a vehicle in t seconds is given by 
Distance=ut+(at^2)/2
Where u is the initial velocity (metres per second), a is the accerlation(metres per second^2).write a c program to evaluate the distance travelled at regular intervals of time, given the values of u and a. the program should provide the flexibility to the user to select his own time intervals and repeat the calculations for different values of u and a.
#include <stdio.h>

int main() {
    double u, a, t, distance;
    int num_intervals, repeat;

    do {
        // Input initial velocity and acceleration
        printf("Enter the initial velocity (u) in m/s: ");
        scanf("%lf", &u);
        printf("Enter the acceleration (a) in m/s^2: ");
        scanf("%lf", &a);

        // Input the number of intervals
        printf("Enter the number of time intervals: ");
        scanf("%d", &num_intervals);

        // Calculate and print distances for each interval
        for (int i = 1; i <= num_intervals; i++) {
            printf("Enter the time (t) for interval %d in seconds: ", i);
            scanf("%lf", &t);
            
            // Calculate the distance
            distance = (u * t) + (a * t * t) / 2;

            // Display the result
            printf("At time t = %.2f seconds, Distance = %.2f meters\n", t, distance);
        }

        // Ask if the user wants to repeat the calculations
        printf("Do you want to perform calculations for different values of u and a? (1 for Yes, 0 for No): ");
        scanf("%d", &repeat);

    } while (repeat == 1);

    return 0;
}

//in inventory management, the economic order quantity for a single item is given by 
EOQ = sqrt of (2*demand rate*stepup cos)t/holding cost per item per unit time
And the optimal time between orders
TBO= sqrt(2*setup costs)/(demand rate*holding cost per unit time)
Write a c program to compute EOQ and TBO, given demand rate(items per unit time), setup costs (per order), and the holding cost(per item per unit time).
#include <stdio.h>
#include <math.h>

int main() {
    double demandRate, setupCost, holdingCost;
    double EOQ, TBO;

    // Get input from the user
    printf("Enter demand rate (items per unit time): ");
    scanf("%lf", &demandRate);

    printf("Enter setup cost (per order): ");
    scanf("%lf", &setupCost);

    printf("Enter holding cost (per item per unit time): ");
    scanf("%lf", &holdingCost);

    // Calculate EOQ
    EOQ = sqrt((2 * demandRate * setupCost) / holdingCost);

    // Calculate TBO
    TBO = sqrt((2 * setupCost) / (demandRate * holdingCost));

    // Print the results
    printf("\nEconomic Order Quantity (EOQ): %.2f\n", EOQ);
    printf("Optimal Time Between Orders (TBO): %.2f\n", TBO);

    return 0;
}
// for a certain electrical circuit with an inductance L and resistance R , the demand natural frequency is given by 
Frequency=sqrt of(1/LC)-(R^2/4C^2)
It is desired to study the variation of this frequency with C(capacitance). Write a c program to calculate the frequency for different  values of C starting from 0.01 to 0.1 in steps of 0.01
#include <stdio.h>
#include <math.h>

int main() {
    double L = 1; // Inductance (example value)
    double R = 0.5; // Resistance (example value)
    double C;
    double frequency;

    printf("Capacitance (C)\tFrequency\n");
    for (C = 0.01; C <= 0.1; C += 0.01) {
        // Calculate frequency using the given formula
        frequency = sqrt((1 / (L * C)) - ((R * R) / (4 * C * C)));

        // Check for imaginary frequencies (if the term inside sqrt is negative)
        if (frequency != frequency) { 
            printf("%.2f\t\tImaginary\n", C); 
        } else {
            printf("%.2f\t\t%.4f\n", C, frequency);
        }
    }

    return 0;
}


//write a c program to read a four digit integer and print the sum of its digits

#include<stdio.h>

int main()
{
    int num,digit,sum=0;
    printf("enter the value of num:");
    scanf("%d",&num);
    
    while(num>0)
    {
        digit=num%10;
        sum=sum+digit;
        num/=10;
    }
    printf("the sum of the digits are: %d",sum);
    
}


//write a program to print the size of various data types in C.
#include<stdio.h>
int main()
{
    

printf("the size of integer is:%lu bytes\n",sizeof(int));
printf("the size of float is:%lu bytes\n",sizeof(float));
printf("the size of double is:%lu bytes\n", sizeof(double));
printf("the size of char is:%lu bytes\n",sizeof(char));
printf("the size of short is:%lu bytes\n",sizeof(short));
printf("the size of long is:%lu bytes\n",sizeof(long));
printf("the size of long long is:%lu bytes\n",sizeof(long long));
printf("the size of long double is:%lu bytes\n",sizeof(long double));
printf("the size of void* is:%lu bytes\n",sizeof(void*));
return 0;

}

//write a c program for three values given, to read three values from  keyboard and print out the largest of them without using if statement.
#include <stdio.h>

int main() {
    int a, b, c, max;

    printf("Enter three values: ");
    scanf("%d %d %d", &a, &b, &c);

    // Find the maximum using ternary operator
    max = a > b ? (a > c ? a : c) : (b > c ? b : c); 

    printf("The largest value is: %d\n", max);

    return 0;
}

//write a program to read two integers values m and n and to decide and print whether m is a multiple of n.
#include <stdio.h>

int main() {
    int m, n;

    printf("Enter two integers (m and n): ");
    scanf("%d %d", &m, &n);

    if (m % n == 0) {
        printf("%d is a multiple of %d\n", m, n);
    } else {
        printf("%d is not a multiple of %d\n", m, n);
    }

    return 0;
}

//write a program to read three values using scanf statement and print the following results:
a)sum of the values
b)average of the three values
c)largest of the three
d)smallest of the three

#include<stdio.h>
int main()
{
    int a,b,c;
    printf("enter the value of a and b and c:\n");
    scanf("%d\n%d\n%d",&a,&b,&c);
    
    int sum=a+b+c;
    float average=sum/3.0;
    int largest=(a>b)?(a>c?a:c):(b>c?b:c);
    int smallest=(a<b)?(a<c?a:c):(b<c?b:c);
    printf("the sum is:%d\naverage is:%f\nlargest is:%d\nsmallest is:%d\n",sum,average,largest,smallest);
    return 0;
}

//the cost of one type of mobile service is Rs. 250 plus Rs. 1.25 for each call made over and above 100 calls. Write a program to read customer codes 
and calls made and print the bill for each customer.
#include <stdio.h>

int main() {
    int customer_code, calls_made;
    float bill;

    printf("Enter customer code: ");
    scanf("%d", &customer_code);

    printf("Enter number of calls made: ");
    scanf("%d", &calls_made);

    if (calls_made <= 100) {
        bill = 250.00;
    } else {
        bill = 250.00 + (calls_made - 100) * 1.25;
    }

    printf("Customer Code: %d\n", customer_code);
    printf("Number of Calls: %d\n", calls_made);
    printf("Bill Amount: Rs. %.2f\n", bill);

    return 0;
}

//write a program to print a table of sin and cos functions for the interval form 0 to 180 degrees in increments of 15 .
#include <stdio.h>
#include <math.h>

#define PI 3.14159265

int main() {
    double angle;

    printf("Angle (deg)\tSin\t\tCos\n");
    printf("-----------------------------\n");

    for (angle = 0; angle <= 180; angle += 15) {
        double radians = angle * PI / 180.0; // Convert degrees to radians
        printf("%.0lf\t\t%.4lf\t\t%.4lf\n", angle, sin(radians), cos(radians));
    }

    return 0;
}

//write a program to compute the values of square-roots and squares of the numbers 0 to 100 in steps 10 and print the output in a tabular form
#include <stdio.h>
#include <math.h>

int main() {
    int i;
    double sqrt_value, square_value;

    printf("Number\tSquare Root\tSquare\n");
    printf("-----------------------------\n");

    for (i = 0; i <= 100; i += 10) {
        sqrt_value = sqrt((double)i); // Calculate square root
        square_value = pow(i, 2);     // Calculate square

        printf("%d\t\t%.2lf\t\t%.0lf\n", i, sqrt_value, square_value);
    }

    return 0;
}

//write a c program that determines whether a given integer is odd or even and displays the number and description on the same line.
#include <stdio.h>

int main() {
    int num;

    printf("Enter an integer: ");
    scanf("%d", &num);

    if (num % 2 == 0) {
        printf("%d is even\n", num);
    } else {
        printf("%d is odd\n", num);
    }

    return 0;
}

//write a c program to illustrate the use of cast operator in a real life situation.
//explanation of cast operator and example and then the code
In C programming, the cast operator is a unary operator that allows you to explicitly convert a value from one data type to another.   

Syntax:

C

(type) expression
type: The desired data type to which you want to convert the value.   
expression: The value or variable that you want to cast.   
Example:

C

int x = 10;
float y = (float)x; // Cast x to float before division
float z = x / 3;    // Without casting, integer division occurs

printf("y: %.2f\n", y);  // Output: y: 10.00
printf("z: %.2f\n", z);  // Output: z: 3.00 (integer division) //
now the program
#include <stdio.h>

int main() {
    int total_amount = 1234;
    float average_per_person;
    int num_people = 5;

    // Calculate average amount per person using cast operator
    average_per_person = (float)total_amount / num_people; 

    printf("Total amount: %d\n", total_amount);
    printf("Number of people: %d\n", num_people);
    printf("Average amount per person: %.2f\n", average_per_person);

    return 0;
}

Chapter 4:  Managing input and output operations (programming exercises)
//Given the string “WORDPROCESSING”, write a c program to read the string from the terminal and display the same in the following formats:
a) WORD PROCESSING
b) WORD
PROCESSING
c) W.P.
#include<stdio.h>
#include<string.h>

int main()
{
    char input[50];
    printf("enter the string:");
    scanf("%s",input);
    
    if(strcmp(input,"WORDPROCESSING")!=0)
    {
    printf("invalid! please enter the word -WORDPROCESSING- !! ");
    return 1;
    }
    
    
     printf("a)%.*s %s\n",4,input,input+4);
     printf("b)%.*s\n%s\n",4,input,input+4);
     printf("c)%c. %c.",input[0],input[4]);
     
     return 0;
    
}

//Write a c program to read the values of x and y and print the results of the following expressions in one line:
a)x+y/x-y
b)x+y/2
c)(x+y)(x-y)

#include<stdio.h>

int main()
{
    float x,y;
    printf("enter the value of x and y:\n");
    scanf("%f\n%f",&x,&y);
    
    if(x==y)
    {
        printf("x-y will be zero and division by zero is undefined!");
        return 1;
    }
    printf("a) %f ",(x+y)/(x-y));
    printf("b) %f ",(x+y)/2);
    printf("c) %f ",(x+y)*(x-y));
    return 0;
}

//write a c program to read the following numbers , round them off the nearest integers and print out the results in integer form: 
35.7
50.21
-23.73
-46.45
#include<stdio.h>
#include<math.h>

int main()
{
    float n[]={35.7,50.21,-23.73,-46.45};
    int roundednum[4];
    
    for(int i=0;i<4;i++)
    {
        roundednum[i]=round(n[i]);
        
    }
    
    printf("rounded number:");
    for(int i=0;i<4;i++)
    {
        printf("\n%d",roundednum[i]);
    }
    return 0;
}

//write a c program that reads 4 floating point values in the range, 0.0 to 20.0, and prints a horizontal bar chart to represent these values using the character * as the fill character. For the  purpose of the chart, the values may be rounded off to the nearest integer. For example the value 4.36 should be represented as follows.
*  *  *  *
*  *  *  *   4.36
*  *  *  *
#include<stdio.h>
#include<math.h>

int main()
{
    float values[4];
    int roundvalues[4];
    int i,j;
    
    printf("enter the 4 floating point values(0.0-20.0):\n");
    for(int i=0;i<4;i++)
    {
    scanf("%f",&values[i]);
    
    
    if(values[i]<0.0||values[i]>20.0)
    {
        printf("invalid!Please enter between 0.0 to 20.0 only.\n");
        return 1;
    }
    
    roundvalues[i]=round(values[i]);
    }
    
    printf("\nthe bar chart :\n");
    for(i=0;i<4;i++)
    {
        for(j=0;j<=roundvalues[i];j++)
        {
            printf("* ");
        }
        printf("%f\n",values[i]);
    }
    
    
}


//write a c program to demonstrate the process of multiplication . the program should ask the user to enter two two-digit integers and print the product of integers as shown below.
                                   45
                      *           37
             
                   --------------------------
7*45 is                        315
3*45 is                        135
                    ----------------------
Add them                    1665
                  ------------------------



#include <stdio.h>

int main() {
    int num1, num2;
    int unitDigit, tensDigit, partial1, partial2, product;

    // Input two two-digit integers
    printf("Enter the first two-digit integer: ");
    scanf("%d", &num1);
    printf("Enter the second two-digit integer: ");
    scanf("%d", &num2);

    // Extract the digits of the second number
    unitDigit = num2 % 10;      // Units place of num2
    tensDigit = num2 / 10;      // Tens place of num2

    // Calculate partial products
    partial1 = num1 * unitDigit; // Multiply num1 by the unit digit
    partial2 = num1 * tensDigit; // Multiply num1 by the tens digit

    // Calculate the final product
    product = partial1 + partial2 * 10;

    // Display the process
    printf("\n");
    printf("                %d\n", num1);
    printf("     *          %d\n", num2);
    printf("     --------------------------\n");
    printf("%d * %d is%27d\n", unitDigit, num1, partial1);
    printf("%d * %d is%27d\n", tensDigit, num1, partial2);
    printf("     --------------------------\n");
    printf("Add them%29d\n", product);
    printf("     --------------------------\n");

    return 0;
    
}


//Write a  program to read  three integers from the keyboard using one scanf statement and output them on one line using:
a)three printf statements
b)only one printf with conversion specifiers , and
c) only one printf without conversion specifiers


#include <stdio.h>

int main() {
    int a, b, c;

    // Read three integers from the keyboard using one scanf statement
    printf("Enter three integers: ");
    scanf("%d %d %d", &a, &b, &c);

    // a) Using three printf statements
    printf("a) ");
    printf("%d ", a);
    printf("%d ", b);
    printf("%d\n", c);

    // b) Using only one printf with conversion specifiers
    printf("b) %d %d %d\n", a, b, c);

    // c) Using only one printf without conversion specifiers
    printf("c) ");
    //printf("%d %d %d\n", a, b, c);
    printf("a b c");

    return 0;
}



//write a c program that prints the value 10.45678 in exponential format with the following specifications:
a)correct to two decimal places;
b)correct to four decimal places and
c)correct to eight decimal places


#include<stdio.h>

int main()
{
    double x=10.45678;
    
    printf("\n%.2e",x);
    printf("\n%.4e",x);
    printf("\n%.8e",x);
    printf("\n%e",x);
    return 0;
}


//write a c program to print the value 345.6789 in fixed-point format with the following specifications:
a)correct to two decimal places;
b)correct to five decimal places;
c)correct to zero decimal places


#include <stdio.h>

int main() {
    double value = 345.6789;

    // a) Correct to two decimal places
    printf("a) %.2f\n", value);

    // b) Correct to five decimal places
    printf("b) %.5f\n", value);

    // c) Correct to zero decimal places
    printf("c) %.0f\n", value);

    return 0;
}


//write a c program to read the name ANIL KUMAR GUPTA  in three parts using the scanf statement and to display the same in the following format using the printf statement.
a)	ANIL K. GUPTA
b)	A.K. GUPTA
c)	GUPTA A.K.


#include<stdio.h>

int main()
{
    char fn[10],mn[10],ln[10];
    
    printf("enter the name(first,middle and last):");
    scanf("%s %s %s",fn,mn,ln);
    
    printf("\na)%s %c. %s",fn,mn[0],ln);
    printf("\nb)%c. %c. %s",fn[0],mn[0],ln);
    printf("\nc)%s %c.%c.",ln,fn[0],mn[0]);
    
    return 0;
    
}


//write a c program to read and display the following table of data.
Name               code              price
Fan                  67831          1234.50
Motor              450             5786.70
The name and code must be left-justified and price must be right-justified


#include <stdio.h>

int main() {
    // Declare variables to store name, code, and price
    char name1[20] = "Fan", name2[20] = "Motor";
    int code1 = 67831, code2 = 450;
    double price1 = 1234.50, price2 = 5786.70;

    // Display the table with proper formatting
    printf("%-20s%-10s%10s\n", "Name", "Code", "Price"); // Table headers
    printf("%-20s%-10d%10.2f\n", name1, code1, price1); // First row
    printf("%-20s%-10d%10.2f\n", name2, code2, price2); // Second row

    return 0;
}


Chapter 5: Decision making and branching (exercise questions)

//write a c program to determine whether a given number is ‘odd’ or ‘even’ and print the message NUMBER IS EVEN or NUMBER IS ODD
a)	Without using else option and
b)	With else option
a) #include<stdio.h>


int main()
{
    int m;
    printf("enter a number:");
    scanf("%d",&m);
    if(m%2==0)
    {
        printf("%d is even",m);
    }
    if(m%2!=0)
    
    printf("%d is odd",m);
    return 0;
}

b) #include<stdio.h>

int main()
{
    int m;
    printf("enter a number:");
    scanf("%d",&m);
    if(m%2==0)
    {
        printf("%d is even",m);
    }
    else
    printf("%d is odd",m);
    return 0;
}


//write a c program to find the number of and sum of all integers greater than 100 and less than 200  that are divisible by 7.


#include<stdio.h>

int main()
{
    int i,sum=0,integers;
    
    for(i=101;i<200;i++)
    {
        if(i%7==0)
        sum=sum+i;
        integers++;
        
    }
    printf("\nthe no. of integers from 100 to 200 which are divisible by 7 are:%d\n",integers);
    printf("\nthe sum of all the above integers are:%d",sum);
    return 0;
}


//a set of two linear equations with two unknown x1 and x2 is given below:
 ax1  + bx2=m
cx1+dx2=n
the set has a unique solution
x1=(md-bn)/(ad-cb)
x2=(na-mc)/(ad-cb)
provided the denominator ad-cb is not equal to zero.
Write a c program that will read the values ofconstants of a,b,c,d,m and n and compute the values of x1, and x2. An appropriate message should be printed if ad-cb=0


#include <stdio.h>

int main() {
    // Declare variables
    float a, b, c, d, m, n;
    float x1, x2, denominator;

    // Input the constants
    printf("Enter the values of a, b, c, d, m, and n: ");
    scanf("%f %f %f %f %f %f", &a, &b, &c, &d, &m, &n);

    // Calculate the denominator
    denominator = a * d - c * b;

    // Check if denominator is zero
    if (denominator == 0) {
        printf("The equations have no unique solution (ad - cb = 0).\n");
    } else {
        // Calculate x1 and x2
        x1 = (m * d - b * n) / denominator;
        x2 = (n * a - m * c) / denominator;

        // Print the results
        printf("The solutions are:\n");
        printf("x1 = %.2f\n", x1);
        printf("x2 = %.2f\n", x2);
    }

    return 0;
}


//given a list of marks ranging from 0 to 100, write a c program to compute and print the number of students:
a)who have obtained more than 80 marks,
b) who have obtained more than 60 marks
c)who have obtained more than 40 marks,
d)who have obtained 40 or less marks
e)in the range 81to 100
f)in the range 61 to 80
g) in the range 41 to 60
h) in the range 0 to 40 
the program should use a minimum number of if statements.


#include <stdio.h>

int main() {
    int marks[] = {85, 70, 45, 90, 33, 77, 56, 61, 80, 38, 92, 64, 41}; // Example list of marks
    int n = sizeof(marks) / sizeof(marks[0]); // Calculate number of students
    int moreThan80 = 0, moreThan60 = 0, moreThan40 = 0, lessThanOrEqual40 = 0;
    int range81to100 = 0, range61to80 = 0, range41to60 = 0, range0to40 = 0;

    // Process marks using a single loop and classify them
    for (int i = 0; i < n; i++) {
        if (marks[i] > 80) {
            moreThan80++;
            range81to100++;
        } else if (marks[i] > 60) {
            moreThan60++;
            range61to80++;
        } else if (marks[i] > 40) {
            moreThan40++;
            range41to60++;
        } else {
            lessThanOrEqual40++;
            range0to40++;
        }
    }

    // Print results
    printf("Number of students who:\n");
    printf("a) Have obtained more than 80 marks: %d\n", moreThan80);
    printf("b) Have obtained more than 60 marks: %d\n", moreThan80 + range61to80);
    printf("c) Have obtained more than 40 marks: %d\n", moreThan80 + range61to80 + range41to60);
    printf("d) Have obtained 40 or less marks: %d\n", lessThanOrEqual40);
    printf("e) Are in the range 81 to 100: %d\n", range81to100);
    printf("f) Are in the range 61 to 80: %d\n", range61to80);
    printf("g) Are in the range 41 to 60: %d\n", range41to60);
    printf("h) Are in the range 0 to 40: %d\n", range0to40);

    return 0;
}


//admission to a professional course is subject to   the following conditions:
a)marks in mathematics>=60
b)marks in physics>=50
c)marks in chemistry>=40
d)total in three subjects>=200
or total in mathematics and physics >=150
given the marks in the three subjects, write a program to process the applications to list the eligible candidates.


#include <stdio.h>

int main() {
    int math, physics, chemistry, total, mathPhysicsTotal;

    // Input marks for the three subjects
    printf("Enter marks in Mathematics, Physics, and Chemistry: ");
    scanf("%d %d %d", &math, &physics, &chemistry);

    // Calculate totals
    total = math + physics + chemistry;
    mathPhysicsTotal = math + physics;

    // Check eligibility conditions
    if (math >= 60 && physics >= 50 && chemistry >= 40 &&
        (total >= 200 || mathPhysicsTotal >= 150)) {
        printf("The candidate is eligible for admission.\n");
    } else {
        printf("The candidate is not eligible for admission.\n");
    }

    return 0;
}



//write a c program to print a two-dimensional square root table as shown, to provide the square root of any number from 0 to 9.9. for example, the value of x will give the square root of 3.2 and y the square root of 3.9
Square root table
Number              0.0         0.1         0.2     ………. 0.9
0.0
1.0
2.0
3.0                                                   x                       y
9.0




#include <stdio.h>
#include <math.h>

int main() {
    double x, y;

    // Print table header
    printf("Square Root Table\n");
    printf("Number\t");
    for (x = 0.0; x < 1.0; x += 0.1) {
        printf("%6.1f", x); // Print column headers (0.0, 0.1, ..., 0.9)
    }
    printf("\n");

    // Print the rows of the table
    for (x = 0.0; x <= 9.0; x += 1.0) { // Row headers (0.0, 1.0, ..., 9.0)
        printf("%4.1f\t", x);
        for (y = 0.0; y < 1.0; y += 0.1) {
            printf("%6.2f", sqrt(x + y)); // Compute and print square root
        }
        printf("\n");
    }

    return 0;
}



//print the floyd’s triangle from 1 to 91


#include <stdio.h>

int main() {
    int i, j, c = 1, n = 91;

    for (i = 1; c <= n; i++) { // Rows based on the current value of `c`
        for (j = 1; j <= i && c <= n; j++) { // Columns based on the current row
            printf("%2d ", c++);
        }
        printf("\n");
    }

    return 0;
}


//print the pattern

1
0 1
1 0 1
0 1 0 1
1 0 1 0 1


#include <stdio.h>

int main() {
    int rows = 5; // Number of rows in the pattern

    for (int i = 1; i <= rows; i++) { // Outer loop for rows
        for (int j = 1; j <= i; j++) { // Inner loop for columns
            // Print 1 if (i + j) is odd, 0 if (i + j) is even
            if ((i + j) % 2 == 0) {
                printf("1 ");
            } else {
                printf("0 ");
            }
        }
        printf("\n"); // Move to the next line after each row
    }

    return 0;
}



//a cloth showroom has announced the following seasonal discounts on purchase of item:
Purchase amount                                                       discount
                                             Mill cloth                                           handloom items
0-100                                       --                                                              5%
101-200                                    5%                                                           7.5%
201-300                                     7.5%                                                        10.0%
Above 300                                 10.0%                                                       15.0%

Write a c program using switch and if statements to compute the net amount to be paid by a customer.


#include<stdio.h>

int main()
{
    float purchase_amt,discount,net;
    int itype;
    printf("please enter the purchase amount:");
    scanf("%f",&purchase_amt);
    
    printf("enter the type(1.mill cloth,2.handloom item)");
    scanf("%d",&itype);
    
    switch(itype)
    {
    case 1://mill cloth
    if(purchase_amt>0 && purchase_amt<=100)
    {
        discount=0.0;
    }
    else if(purchase_amt>100 && purchase_amt<=200)
    {
        discount=5.0;
    }
    else if(purchase_amt>200 && purchase_amt<=300)
    {
        discount=7.5;
    }
    else{
        discount=10.0;
    }break;
    case 2://handloom items
    if(purchase_amt>0 && purchase_amt<=100)
    {
        discount=5.0;
    }
    else if(purchase_amt>100 && purchase_amt<=200)
    {
        discount=7.5;
    }
    else if(purchase_amt>200 && purchase_amt<=300)
    {
        discount=10.0;
    }
    else{
        discount=15.0;
    }break;
    default:
    printf("invalid item type!!");
    return 1;
}
    
net=purchase_amt-(purchase_amt*(discount/100));
printf("\nthe purchase amount is %f:",purchase_amt);
printf("\nthe discount u will get is %f:",discount);
printf("\n the net amount after discount is %f:",net);
return 0;
}



//write a c program that will read the value of x and evaluate the following function

1	for x<0
  Y={ 0      for x=0
           -1 for x<0

Using a)nested if statements,b)else if statements c)conditional operator?:


#include <stdio.h>

int main() {
    int x, y;

    // Input the value of x
    printf("Enter the value of x: ");
    scanf("%d", &x);

    // Using nested if statements
    if (x > 0) {
        y = 1;
    } else {
        if (x == 0) {
            y = 0;
        } else {
            y = -1;
        }
    }
    printf("Using nested if: y = %d\n", y);

    // Using else if statements
    if (x > 0) {
        y = 1;
    } else if (x == 0) {
        y = 0;
    } else {
        y = -1;
    }
    printf("Using else if: y = %d\n", y);

    // Using conditional operator
    y = (x > 0) ? 1 : (x == 0 ? 0 : -1);
    printf("Using conditional operator: y = %d\n", y);

    return 0;
}


//write a c program to compute the real roots of a quadratic equation ax^2+bx+c=0.
The roots are given by the equations
X1=-b+(root of (b^2-4ac/2a)
X2=-b-(root of (b^2-4ac/2a)
The program should request for the values of the constants a,b and c and print the values of x1,and x2. Use the following rules:
a)	no solution, if both a and b are zero
b)	there is only one root , if a=0(x=-c/b)
c)	there are no real roots, if b^2-4ac is negative
d)	otherwise , there are two real roots
test your program with appropriate data so that all logical paths are working as per your design. Incorporate appropriate output messages


#include <stdio.h>
#include <math.h>

int main() {
    float a, b, c, discriminant, x1, x2;

    printf("Enter the values of a, b, and c: ");
    scanf("%f %f %f", &a, &b, &c);

    // Check for special cases
    if (a == 0 && b == 0) {
        printf("No solution.\n");
    } else if (a == 0) {
        printf("One root: x = %.2f\n", -c / b);
    } else {
        discriminant = b * b - 4 * a * c;

        if (discriminant < 0) {
            printf("No real roots.\n");
        } else {
            x1 = (-b + sqrt(discriminant)) / (2 * a);
            x2 = (-b - sqrt(discriminant)) / (2 * a);
            printf("Two real roots:\n");
            printf("x1 = %.2f\n", x1);
            printf("x2 = %.2f\n", x2);
        }
    }

    return 0;
}



//Write a c program  to read three integer values from the keyboard and displays the output stating that they  are thesides of right-angled triangle.


#include <stdio.h>
#include <math.h>

int main() {
    int a, b, c;

    // Input the three sides of the triangle
    printf("Enter three integers representing the sides of a triangle: ");
    scanf("%d %d %d", &a, &b, &c);

    // Check if the sides form a right-angled triangle
    if ((a * a + b * b == c * c) || (a * a + c * c == b * b) || (b * b + c * c == a * a)) {
        printf("The sides %d, %d, and %d form a right-angled triangle.\n", a, b, c);
    } else {
        printf("The sides %d, %d, and %d do not form a right-angled triangle.\n", a, b, c);
    }

    return 0;
}


//an electricity board charges the following rates for the use of electricity:
For the first 200 units: 80P per unit
For the next 100 units: 90 P per unit
Beyond 300 units: Rs.1 per unit
All users are charged a minimum of Rs. 100 as meter charge. If the total amount is more than Rs. 400 , then an additional surcharge of 15% of total amount is charged.Write a c program  to read the names of users and number of units consumed and print out the charges with names.


#include <stdio.h>

int main() {
    char name[50];
    int units;
    float total_charge = 0, surcharge = 0;

    // Input user name and units consumed
    printf("Enter the user's name: ");
    scanf("%s", name);

    printf("Enter the number of units consumed: ");
    scanf("%d", &units);

    // Calculate charges based on the number of units consumed
    if (units <= 200) {
        total_charge = units * 0.80;
    } else if (units <= 300) {
        total_charge = (200 * 0.80) + ((units - 200) * 0.90);
    } else {
        total_charge = (200 * 0.80) + (100 * 0.90) + ((units - 300) * 1.00);
    }

    // Add minimum meter charge
    total_charge += 100;

    // Check for surcharge
    if (total_charge > 400) {
        surcharge = total_charge * 0.15;
        total_charge += surcharge;
    }

    // Print the final charges
    printf("User Name: %s\n", name);
    printf("Units Consumed: %d\n", units);
    printf("Total Charges: Rs. %.2f\n", total_charge);

    return 0;
}


//write a c program to compute and display the sum of all integers that are divisible by 6 but not divisible by 4 and lie between 0 and 100. The program should also count and display the number ofsuch values.


#include <stdio.h>

int main() {
    int i, sum = 0, count = 0;

    for (i = 0; i <= 100; i++) {
        if (i % 6 == 0 && i % 4 != 0) {
            sum += i;
            count++;
        }
    }

    printf("Sum of integers divisible by 6 but not by 4: %d\n", sum);
    printf("Number of such integers: %d\n", count);

    return 0;
}


// write a c program that could read a positive integer number and decide whether the number is prime number and display the output accordingly.modify the program to count all  the prime numbers that lie between 100 and 200


#include <stdio.h>

int is_prime(int num) {
    if (num <= 1) {
        return 0; // Numbers less than or equal to 1 are not prime
    }

    for (int i = 2; i * i <= num; i++) {
        if (num % i == 0) {
            return 0; // If divisible by any number other than 1 and itself, it's not prime
        }
    }

    return 1; // If no divisors found, it's prime
}

int main() {
    int num, count_primes = 0;

    // Part 1: Check if a single number is prime
    printf("Enter a positive integer: ");
    scanf("%d", &num);

    if (is_prime(num)) {
        printf("%d is a prime number.\n", num);
    } else {
        printf("%d is not a prime number.\n", num);
    }

    // Part 2: Count prime numbers between 100 and 200
    for (int i = 100; i <= 200; i++) {
        if (is_prime(i)) {
            count_primes++;
        }
    }

    printf("Number of prime numbers between 100 and 200: %d\n", count_primes);

    return 0;
}



Chapter 6 Decision making and looping(exercise questions).

//given a number, write a c program using while loop to reverse the digits of the number. For example , the number 12345 should be written as 54321.
HINT: use modulus operator to extract the last digit and the integer division by 10 to get the n-1 digit number from the n digit number.)


#include <stdio.h>

int main() {
    int num, reversed_num = 0, remainder;

    printf("Enter an integer: ");
    scanf("%d", &num);

    while (num != 0) {
        remainder = num % 10; // Extract the last digit
        reversed_num = reversed_num * 10 + remainder; // Append the digit to the reversed number
        num /= 10; // Remove the last digit from the original number
    }

    printf("Reversed number: %d\n", reversed_num);

    return 0;
}


//the factorial of an integer m is the product of consecutive integers from 1 to m. that is, factorial m=m!=m*(m-1)*…….x1.

Write a c program that computes and prints a table of factorials for any given m.


#include<stdio.h>

int main()
{
    int m,fact=1;
    printf("enter a value to find factorial of it:");
    scanf("%d",&m);
    
    if(m<0){
    printf("factorial of negative number is not there");
    return 1;
    }
    
    for(int i=1;i<=m;i++)
    {
        fact=fact*i;
        printf("\nfactorial of  %d is:%d",i,fact);
    }
    return 0;
    
    
    
}


//write a c program to compute the sum of the digits of a given integers number.


#include<stdio.h>

int main()
{
    int m,digi,sum=0,temp;
    printf("etner a positive integer to find its sum of digits:");
    scanf("%d",&m);
    
    temp=m;
    
    while(temp!=0)
    {
        digi=temp%10;
        sum=sum+digi;
        temp/=10;
        //printf("the sum of digit of %d is:%d",m,sum);
        
    }
    printf("the sum of digit of %d is:%d",m,sum);
    return 0;
}


//the number in the sequence 0 1 1 2 3 5 8 13 21 …. Are called Fibonacci numbers. Write a c program using a do… while loop to  calculate and print the first m Fibonacci numbers.
(hint: after the first two numbers in the series, each number is the sum of the two preceding numbers)


#include<stdio.h>

int main()
{
    int m;
    printf("enter the no. of digits to print in fibonacci series:");
    scanf("%d",&m);
    
    if(m<=0)
    {
        printf("Please enter a positive integer!!");
        return 1;
    }
    
    int a=0,b=1,count=0,next;
    
    printf("\nthe first %d fib series is:",m);
    do
    {
        
        next=a+b;
        a=b;
        b=next;
        count++;
        printf("\n%d",a);
    }
    while(count<m);
    
    return 0;
}


//a program to evaluate the equation y=x^n. when n is a non negative integer. The variable y is initialized to 1 and then multiplied by x,n times using the for loop.


#include<stdio.h>

int main()
{
    int n;
    float x,y=1.0;
    printf("enter the value of x and n:");
    scanf("%f\n%d",&x,&n);
    
    for(int i=1;i<=n;i++)
    {
        y=y*x;
    }
    printf("\nx=%f; n=%d ; x to the power %d =%f\n",x,n,n,y);
    return 0;
}


//write a c program to evaluate the following investment equation v=p(1+r)^n and print the tables which would give the value of v for various combination of the following values of p,r, and n.
p : 1000,2000,3000,….,10000
r:0.10,0.11,0.12……..,0.20
n:1,2,3,….,10
(hint: p is the principal amount and v is the value of money at the end of n years. This equation can be recursively written as v=p(1+r) and p=v, that is , the value of money at the end of first year beomces the principal amount for the next year and so on.)


#include<stdio.h>
#include<math.h>

int main()
{
    double p,r,v;
    int n;
    
    printf("\nthe investment equation table");
    printf("\n%-10s %-10s %-10s %-10s","principal","rate","years","value");
    printf("-----------------------------------------------");
    
    for(p=1000;p<=10000;p+=1000)
    {
        for(r=0.10;r<=0.20;r+=0.01)
        {
            for(n=1;n<=10;n++)
            {
                v=p*pow(1+r,n);
                printf("\n%-10f %-10f %-10d %-10f",p,r,n,v);
            }
        }
    }
    return 0;
    
}



//write a program to print the pattern using for loop
a)	1
22
333
4444
55555
b)*************
     ************
       ***********
           *********
                  *****
                          *
                          
Answer a)

#include<stdio.h>

int main()
{
    for(int i=0;i<6;i++)
    { 
        for(int j=0;j<i;j++)
        {
            printf("%d",i);
        }
        printf("\n");
    }
}


Answer b)

#include<stdio.h>

int main()
{
    int i,j, r=6;
    
    for(i=0;i<6;i++)
    {
        for(j=0;j<i;j++)
        {
            printf(" ");
        }
        for(j=0;j<r-i;j++)
        {
            printf("*");
        }
        printf("\n");
    }
    return 0;
}


//write a c program to read the age of 100 persons and count the  number of persons in the age group 50 to 60. Use for and continue statements
#include <stdio.h>

int main() {
    int age, count = 0;

    for (int i = 0; i < 10; i++) {
        printf("Enter age of person %d: ", i + 1);
        scanf("%d", &age);

        if (age < 50 || age > 60) {
            continue; // Skip to the next iteration if age is not in the desired range
        }

        count++;
    }

    printf("Number of persons in the age group 50 to 60: %d\n", count);

    return 0;
}

//write a program to  print a table of values of the function y=exp(-x) for x varying from 0.0 to 10.0 in steps 0.10. the table should appear as follows:
                                         TABLE FOR Y=EXP(-X)
X               0.1          0.2         0.3 ……………………………..0.9
0.0
1.0
2.0
3.0
.
.
.
.
9.0

#include <stdio.h>
#include <math.h>

int main() {
    // Print the table header
    printf("TABLE FOR Y = EXP(-X)\n\n");
    printf("X\t	");
    for (float step = 0.1; step < 1.0; step += 0.1) {
        printf("%.1f\t", step);
    }
    printf("\n\n");

    // Generate and print values
    for (int x = 0; x < 10; x++) {
        printf("%d.0\t\t", x);
        for (float step = 0.1; step < 1.0; step += 0.1) {
            float y = exp(-(x + step));
            printf("%.4f\t", y);
        }
        printf("\n");
    }

    return 0;
}


//write a c program that will read a positive integer and determine and print its binary equivalent.(hint: the bits of the binary representation of an integer can be generated by repeatedly dividing the number and the successive quotiesnts by 2 and saving the remainder , which is either 0 or 1, after each division.)

#include<stdio.h>

int main()
{
    int i,j,num,quotient;
    int binary[32];
    
    printf("enter the number to find binary equivalent:");
    scanf("%d",&num);
    
    if(num<0)
    {
        printf("invalid!Please enter a positive integer!!");
        return 1;
    }
    
    i=0;
    quotient=num;
    while(quotient!=0)
    {
        binary[i]=quotient%2;
        quotient/=2;
        i++;
    }
    
    printf("the binary representation is:");
    for(j=i-1;j>=0;j--)
    {
        printf("%d",binary[j]);
    }
    printf("\n");
    return 0;
}


//write a c program to compute the value of Euler’s number e, that is used as the base of natural logarithms. Use the following formula.
   e=1+1/1!+1/2!+1/3!+1/4!+………….+1/n!
use a suitable loop construct. The loop must terminate when the difference between two successive values of e is less than 0.00001    

#include <stdio.h>

double factorial(int n) {
    double fact = 1.0;
    for (int i = 1; i <= n; i++) {
        fact *= i;
    }
    return fact;
}

int main() {
    double e = 1.0;  // Starting value for e
    double previous_e = 0.0;  // To keep track of the previous value of e
    int n = 1;  // Start with 1! term
    double term;

    // Loop until the difference between two successive values is less than 0.00001
    while (e - previous_e > 0.00001) {
        previous_e = e;  // Save the previous value of e
        
        // Calculate the next term and add it to e
        term = 1.0 / factorial(n);
        e += term;

        n++;  // Increment to the next factorial term
    }

    // Output the value of e
    printf("Value of Euler's number e: %.5f\n", e);

    return 0;
}

//write a c program to print a square of size 5 by using the character S as shown below:
A)	S SS S S
S S S S S
S S S S S
S S S S S
S S S S S


#include<stdio.h>

int main()
{
    int i,j;
    
    for(i=0;i<6;i++)
    {
        for(j=0;j<6;j++)
        {
            printf(" S");
        }
        printf("\n");
    }
}

b)	 S S S S S
S            S
S            S
S            S
S S S S S    
#include<stdio.h>

int main()
{
    int i,j,width=5,height=5;
    
    for(i=0;i<height;i++)
    {
        for(j=0;j<width;j++)
        
        {
            if(i==0||i==height-1||j==0||j==width-1)
            {
                printf("S");
            }
            else
            {
                printf(" ");
            }
            
        }
        printf("\n");
    }
}

//print pattern
S S S S S
S S S S S
S S O S S
S S S S
S S S S        
#include<stdio.h>

int main()
{
    int i,j;
    for(i=0;i<5;i++)
    {
        for(j=0;j<5;j++)
        {
            if(i==2&&j==2)
            {
                printf("O");
            }
            else
            {
                printf("S");
            }
        }
        printf("\n");
    }
}

//write a c program to print all integers that are not divisible by either 2 or 3 and lie between 1 and 100. Program should also account the number of such integers and print the result.    
#include<stdio.h>

int main()
{
    int i,count=0,sum=0;
    
    printf("integers not divisible by 2 or 3 are:\n");
    for(i=0;i<100;i++)
    {
        if(i%2!=0 && i%3!=0)
        {
            printf(" %d ",i);
            sum+=i;
            count++;
        }
    }
    printf("\nthe sum of all the above integers are:%d",sum);
    printf("\nthe count of all the above is:%d",count);
    return 0;
}

//given a set of 10 two digits integers containing both positive and negative values, write a c program using for loop to compute the sum of all positive values and print the sum and the number of values added. The program should use scanf to read the values and terminate when the sum exceeds 999. Do not use goto statement.    

#include <stdio.h>

int main() {
    int sum = 0, count = 0;
    int num;
    
    // Loop to read and process 10 integers
    for (int i = 0; i < 10; i++) {
        // Reading the integer value
        printf("Enter integer %d: ", i + 1);
        scanf("%d", &num);

        // Check if the number is positive
        if (num > 0) {
            sum += num;  // Add to sum if positive
            count++;     // Increment the count of positive values
        }

        // Terminate the loop if sum exceeds 999
        if (sum > 999) {
            break;
        }
    }

    // Print the result
    printf("Sum of positive values: %d\n", sum);
    printf("Number of positive values added: %d\n", count);

    return 0;
}


Chapter -7 Arrays (exercise questions)

Basic programs of arrays 


1.	To read array elements
#include<stdio.h>

int main()
{
    int a[10];
    int i;
    printf("enter 10 elements to be printed:\n");
    for(i=0;i<10;i++)
    {
        scanf("%d",&a[i]);
    }
    printf("the elements are\n");
    for(i=0;i<10;i++)
    {
        printf(" %d ",a[i]);
    }
    printf("\n");
    
    return 0;
    
}

Second way-
#include <stdio.h>

int main() {
    int n, i;

    // Get the number of elements from the user
    printf("Enter the number of elements: ");
    scanf("%d", &n);

    // Declare an array to store the elements
    int arr[n];

    // Read the elements from the user
    printf("Enter the elements:\n");
    for (i = 0; i < n; i++) {
        scanf("%d", &arr[i]);
    }

    // Print the elements of the array
    printf("The elements of the array are:\n");
    for (i = 0; i < n; i++) {
        printf("%d ", arr[i]);
    }
    printf("\n");

    return 0;
}

//matrix question simple input and output
#include<stdio.h>

int main()
{
    int r,c;
    
    printf("enter the number of rows:");
    scanf("%d",&r);
    printf("enter the number of columns:");
    scanf("%d",&c);
    
    int mat[r][c];
    printf("enter the elements of matrix:");
    for(int i=0;i<r;i++)
    {
        for(int j=0;j<c;j++)
        {
            printf("element at [%d][%d]:",i,j);
            scanf("%d",&mat[i][j]);
        }
    }
    printf("the matrix is:\n");
    for(int i=0;i<r;i++)
    {
        for(int j=0;j<c;j++)
        {
            printf(" %d ",mat[i][j]);
        }
        printf("\n");
}
return 0;
}

//addition of matrix
#include <stdio.h>

int main() {
    int rows, cols;

    // Input the dimensions of the matrices
    printf("Enter the number of rows: ");
    scanf("%d", &rows);
    printf("Enter the number of columns: ");
    scanf("%d", &cols);

    int matrix1[rows][cols], matrix2[rows][cols], sum[rows][cols];

    // Input elements for the first matrix
    printf("Enter elements of the first matrix:\n");
    for (int i = 0; i < rows; i++) {
        for (int j = 0; j < cols; j++) {
            printf("Element at [%d][%d]: ", i + 1, j + 1);
            scanf("%d", &matrix1[i][j]);
        }
    }

    // Input elements for the second matrix
    printf("Enter elements of the second matrix:\n");
    for (int i = 0; i < rows; i++) {
        for (int j = 0; j < cols; j++) {
            printf("Element at [%d][%d]: ", i + 1, j + 1);
            scanf("%d", &matrix2[i][j]);
        }
    }

    // Perform matrix addition
    for (int i = 0; i < rows; i++) {
        for (int j = 0; j < cols; j++) {
            sum[i][j] = matrix1[i][j] + matrix2[i][j];
        }
    }

    // Display the result
    printf("The resulting matrix after addition is:\n");
    for (int i = 0; i < rows; i++) {
        for (int j = 0; j < cols; j++) {
            printf("%d ", sum[i][j]);
        }
        printf("\n");
    }

    return 0;
}

//multiplication of matrix
#include <stdio.h>

int main() {
    int rowsA, colsA, rowsB, colsB;

    // Input dimensions of the first matrix
    printf("Enter the number of rows for the first matrix: ");
    scanf("%d", &rowsA);
    printf("Enter the number of columns for the first matrix: ");
    scanf("%d", &colsA);

    // Input dimensions of the second matrix
    printf("Enter the number of rows for the second matrix: ");
    scanf("%d", &rowsB);
    printf("Enter the number of columns for the second matrix: ");
    scanf("%d", &colsB);

    // Check if matrices can be multiplied
    if (colsA != rowsB) {
        printf("Matrix multiplication not possible. The number of columns of the first matrix must equal the number of rows of the second matrix.\n");
        return 1;
    }

    int matrixA[rowsA][colsA], matrixB[rowsB][colsB], result[rowsA][colsB];

    // Input elements of the first matrix
    printf("Enter elements of the first matrix:\n");
    for (int i = 0; i < rowsA; i++) {
        for (int j = 0; j < colsA; j++) {
            printf("Element at [%d][%d]: ", i + 1, j + 1);
            scanf("%d", &matrixA[i][j]);
        }
    }

    // Input elements of the second matrix
    printf("Enter elements of the second matrix:\n");
    for (int i = 0; i < rowsB; i++) {
        for (int j = 0; j < colsB; j++) {
            printf("Element at [%d][%d]: ", i + 1, j + 1);
            scanf("%d", &matrixB[i][j]);
        }
    }

    // Initialize the result matrix to 0
    for (int i = 0; i < rowsA; i++) {
        for (int j = 0; j < colsB; j++) {
            result[i][j] = 0;
        }
    }

    // Perform matrix multiplication
    for (int i = 0; i < rowsA; i++) {
        for (int j = 0; j < colsB; j++) {
            for (int k = 0; k < colsA; k++) {
                result[i][j] += matrixA[i][k] * matrixB[k][j];
            }
        }
    }

    // Display the resulting matrix
    printf("The resulting matrix after multiplication is:\n");
    for (int i = 0; i < rowsA; i++) {
        for (int j = 0; j < colsB; j++) {
            printf("%d ", result[i][j]);
        }
        printf("\n");
    }

    return 0;
}

//an election is contested by 5 candidates. The candidate are numbered 1 to 5 and the voting is done by marking the candidate number on the ballot paper. Write a c program to read the ballots and count the votes cast for each candidate using an array variable count.In case, a number read is outside the range 1 to 5, the ballot should be considered as a ‘spoilt ballot’ and the program should also count the number of spoilt ballots.

#include <stdio.h>

int main() {
    int votes[5] = {0}; // Array to store the vote count for each candidate (1 to 5)
    int spoilt_ballots = 0;
    int candidate_number;

    printf("Election Voting System\n");

    // Read votes until the user enters 0
    while (1) {
        printf("Enter candidate number (1-5) or 0 to end: ");
        scanf("%d", &candidate_number);

        if (candidate_number == 0) {
            break;
        } else if (candidate_number >= 1 && candidate_number <= 5) {
            votes[candidate_number - 1]++; // Decrement candidate number by 1 to match array index (0-based)
        } else {
            spoilt_ballots++;
            printf("Invalid vote (candidate number must be between 1 and 5).\n");
        }
    }

    // Find the candidate with the maximum votes
    int max_votes = votes[0];
    int winner = 1; // Assume candidate 1 is the winner initially

    for (int i = 1; i < 5; i++) {
        if (votes[i] > max_votes) {
            max_votes = votes[i];
            winner = i + 1; // Adjust winner based on array index
        }
    }

    // Print the vote count for each candidate
    printf("\nElection Results:\n");
    for (int i = 0; i < 5; i++) {
        printf("Candidate %d: %d votes\n", i + 1, votes[i]);
    }

    // Print the number of spoilt ballots
    printf("Spoilt Ballots: %d\n", spoilt_ballots);

    // Print the winner
    printf("Winner: Candidate %d\n", winner);

    return 0;
}

// the annual examination results of 100 students are tabulated as follows:
Roll no            subject 1            subject 2               subject 3                   
.
.
.
.
Write a c program to read the data and determine the following:
a)total marks obtained by each student
b) the highest marks in each subject and the roll no. of the student who secured it
c) the student who obtained the highest total marks

#include <stdio.h>

#define NUM_STUDENTS 10
#define NUM_SUBJECTS 3

int main() {
    int marks[NUM_STUDENTS][NUM_SUBJECTS];
    int roll_no[NUM_STUDENTS];
    int total_marks[NUM_STUDENTS] = {0};
    int highest_marks[NUM_SUBJECTS] = {0};
    int highest_roll_no[NUM_SUBJECTS] = {0};
    int highest_total = 0, highest_total_roll = 0;

    // Input the data
    printf("Enter data for %d students:\n", NUM_STUDENTS);
    for (int i = 0; i < NUM_STUDENTS; i++) {
        printf("\nEnter roll number for student %d: ", i + 1);
        scanf("%d", &roll_no[i]);

        printf("Enter marks for 3 subjects: ");
        for (int j = 0; j < NUM_SUBJECTS; j++) {
            scanf("%d", &marks[i][j]);

            // Update total marks for the student
            total_marks[i] += marks[i][j];

            // Update highest marks for the subject
            if (marks[i][j] > highest_marks[j]) {
                highest_marks[j] = marks[i][j];
                highest_roll_no[j] = roll_no[i];
            }
        }

        // Update the student with the highest total marks
        if (total_marks[i] > highest_total) {
            highest_total = total_marks[i];
            highest_total_roll = roll_no[i];
        }
    }

    // Output the results
    printf("\nResults:\n");

    // (a) Total marks obtained by each student
    printf("\nTotal marks for each student:\n");
    for (int i = 0; i < NUM_STUDENTS; i++) {
        printf("Roll No: %d, Total Marks: %d\n", roll_no[i], total_marks[i]);
    }

    // (b) Highest marks in each subject and the roll number
    printf("\nHighest marks in each subject:\n");
    for (int j = 0; j < NUM_SUBJECTS; j++) {
        printf("Subject %d: Highest Marks: %d, Roll No: %d\n", j + 1, highest_marks[j], highest_roll_no[j]);
    }

    // (c) Student with the highest total marks
    printf("\nStudent with the highest total marks:\n");
    printf("Roll No: %d, Total Marks: %d\n", highest_total_roll, highest_total);

    return 0;
}

//given are two one-dimensional arrays  A and B which are stored in ascending order. Write a c program to merge them into a single sorted array C that contains every item from arrays A and B, in ascending order.
#include <stdio.h>

int main() {
    int A[100], B[100], C[200];
    int m, n, i, j, k;

    // Get the number of elements in arrays A and B
    printf("Enter the number of elements in array A: ");
    scanf("%d", &m);
    printf("Enter the number of elements in array B: ");
    scanf("%d", &n);

    // Read elements of array A
    printf("Enter elements of array A in ascending order:\n");
    for (i = 0; i < m; i++) {
        scanf("%d", &A[i]);
    }

    // Read elements of array B
    printf("Enter elements of array B in ascending order:\n");
    for (j = 0; j < n; j++) {
        scanf("%d", &B[j]);
    }

    // Merge arrays A and B into array C
    i = 0; // Index for array A
    j = 0; // Index for array B
    k = 0; // Index for array C

    while (i < m && j < n) {
        if (A[i] <= B[j]) {
            C[k++] = A[i++];
        } else {
            C[k++] = B[j++];
        }
    }

    // Copy remaining elements of A (if any)
    while (i < m) {
        C[k++] = A[i++];
    }

    // Copy remaining elements of B (if any)
    while (j < n) {
        C[k++] = B[j++];
    }

    // Print the merged array C
    printf("Merged array C:\n");
    for (k = 0; k < m + n; k++) {
        printf("%d ", C[k]);
    }
    printf("\n");

    return 0;
}

//two matrices that have the same number of rows and columns can be multiplied to produce a third matrix. Consider the following two matrices A and B. the product of A and B is a third matrix C of size nxn where each element of C is given by following equation
Cij(summation from k=1 to n) = aik. Bkj
Write a C program that will read the values of elements of A and B and produce the product matrix C

#include<stdio.h>

#define MS 50

int main()
{
    int m, A[MS][MS], B[MS][MS],C[MS][MS]={0};
    
    printf("enter the order of the matrix:");
    scanf("%d",&m);
    
    printf("enter the elements of Matrix A:\n");
    for(int i=0;i<m;i++)
    {
        for(int j=0;j<m;j++)
        {
        scanf("%d",&A[i][j]);
        }
    }
    
    printf("enter  the elements of Matrix B:\n");
    for(int i=0;i<m;i++)
    {
        for(int j=0;j<m;j++)
        {
         scanf("%d",&B[i][j]);   
        }
    }
    printf("\nthe matrix A:\n");
    for(int i=0;i<m;i++)
    {
        for(int j=0;j<m;j++)
        {
            printf(" %d ",A[i][j]);
        }
        printf("\n");
        
    }
    printf("\nthe matrix B:\n");
    for(int i=0;i<m;i++)
    {
        for(int j=0;j<m;j++)
        {
            printf(" %d ",B[i][j]);
        }
        printf("\n");
        
    }
    
    for(int i=0;i<m;i++)
    {
        for(int j=0;j<m;j++)
        {
            for(int k=0;k<m;k++)
            {
                C[i][j]+=A[i][k]*B[k][j];
            }
            
        }
    }
    
    printf("\nThe resultant matrix is:\n");
    for(int i=0;i<m;i++)
    {
        for(int j=0;j<m;j++)
        {
            printf(" %d ",C[i][j]);
        }
        printf("\n");
    }
        
        return 0;
}

//write C a program that fills a five-by-five matrix as follows:
-Upper left triangle with  +1s
-lower right triangle with -1s
-right to left diagonal with zeroes
Display the contents of the matrix using  not  more than two printf statements

#include<stdio.h>
#define m 5

int main()
{
int mat[m][m];

    for(int i=0;i<m;i++)
    {
        for(int j=0;j<m;j++)
        {
            if((i+j)<4)
            {
                mat[i][j]=1;
            }
            else if(i+j>4)
            {
                mat[i][j]=-1;
            }
            else
            {
                mat[i][j]=0;
            }
        }
    }
    
    printf("\nthe matrix is:\n");
    for(int i=0;i<m;i++)
    {
        for(int j=0;j<m;j++)
        {
            printf("%3d",mat[i][j]);
        }
        printf("\n");
    }
    return 0;
}

//write a c program that will compute the length of a given character string
#include<stdio.h>
#include<string.h>

int main()
{
    char st[100];
    
    
    printf("enter a character:");
    scanf("%s",st);
    
   
    
    printf("\nstring length is: %d",strlen(st));
    
    return 0;
    
}
(or)
#include <stdio.h>

int main() {
    char str[100]; // Declare a string with a maximum size of 100 characters
    int length = 0;

    // Input the string
    printf("Enter a string: ");
    fgets(str, sizeof(str), stdin); // Read the string, including spaces

    // Compute the length
    while (str[length] != '\0' && str[length] != '\n') {
        length++;
    }

    // Output the result
    printf("The length of the given string is: %d\n", length);

    return 0;
}

//write a c program that will count the number of occurrences of a specified character in a given line of text. Test your program
#include<stdio.h>


int main()
{
    int count=0;;
    char str[200],ch;
    
    printf("please enter a string:");
    fgets(str,sizeof(str),stdin);
    
    printf("\nenter a character:");
    scanf("%c",&ch);
    
    for(int i=0;str[i]!='\0';i++)
    {
        if(str[i]==ch)
        count++;
    }
    printf("\nthe count of character %c is:%d",ch,count);
    return 0;
}
//write a c program to read a matrix of size mxn and print its transpose
#include<stdio.h>

int main()
{
    int m,n;
    printf("\nenter the rows and columns (m,n):\n");
    scanf("\n%d\n%d",&m,&n);
    
    int mat[m][n],trans[n][m];
    
    for(int i=0;i<m;i++)
    {
        for(int j=0;j<n;j++)
        {
            printf("\nenter the element[%d][%d]:",i,j);
            scanf("%d",&mat[i][j]);
        }
    }
    
    for(int i=0;i<m;i++)
    {
        for(int j=0;j<n;j++)
        {
            trans[j][i]=mat[i][j];
        }
    }
    
    printf("the original matrx is:\n");
    for(int i=0;i<m;i++)
    {
        for(int j=0;j<n;j++)
        {
            printf("%3d",mat[i][j]);
        }
        printf("\n");
    }
    
    printf("the transposed matrx is:\n");
    for(int i=0;i<n;i++)
    {
        for(int j=0;j<m;j++)
        {
            printf("%3d",trans[i][j]);
        }
        printf("\n");
    }
    
    return 0;
}

//every book published by international publishers should carry an international standard book number(ISBN). It is a 10 character 4 part number as shown below.
0-07-041183-2
The first part denotes the regino, the second represents publisher, the third identifies the book and the fourth is the check digit. The check digit is computer as follows:
Sum=(1*first digit)+(2*second digit)+(3*third digit)+…..+(9*ninth digit) 
Check digit is the remainder when sum is divided by 11. Write a c program that reads a given ISBN number and checks whether it represents a valid ISBN NUMBER
#include <stdio.h>
#include <string.h>
#include <ctype.h>

int main() {
    char isbn[20];
    int sum = 0;

    // Input the ISBN number
    printf("Enter the ISBN number (format: x-xx-xxxxx-x): ");
    scanf("%s", isbn);

    // Validate the format and calculate the sum
    int digit_index = 0; // To track digit positions for weight calculation
    for (int i = 0; isbn[i] != '\0'; i++) {
        if (isdigit(isbn[i])) {
            sum += (digit_index + 1) * (isbn[i] - '0');
            digit_index++;
        } else if (isbn[i] != '-') {
            printf("Invalid ISBN format.\n");
            return 1;
        }
    }

    // Check if the number of digits is 10
    if (digit_index != 10) {
        printf("Invalid ISBN: It must have exactly 10 digits.\n");
        return 1;
    }

    // Validate the check digit
    if (sum % 11 == (isbn[strlen(isbn) - 1] - '0')) {
        printf("The ISBN number is valid.\n");
    } else {
        printf("The ISBN number is invalid.\n");
    }

    return 0;
}

//WRITE A C PROGRAM to read two matrices A and B and print the following :
a)A+B
b)A-B
#include <stdio.h>

int main() {
    int m, n;

    // Input matrix dimensions
    printf("Enter the number of rows (m): ");
    scanf("%d", &m);
    printf("Enter the number of columns (n): ");
    scanf("%d", &n);

    int A[m][n], B[m][n], Sum[m][n], Diff[m][n];

    // Input matrix A
    printf("Enter the elements of Matrix A:\n");
    for (int i = 0; i < m; i++) {
        for (int j = 0; j < n; j++) {
            printf("A[%d][%d]: ", i + 1, j + 1);
            scanf("%d", &A[i][j]);
        }
    }

    // Input matrix B
    printf("Enter the elements of Matrix B:\n");
    for (int i = 0; i < m; i++) {
        for (int j = 0; j < n; j++) {
            printf("B[%d][%d]: ", i + 1, j + 1);
            scanf("%d", &B[i][j]);
        }
    }

    // Compute A + B and A - B
    for (int i = 0; i < m; i++) {
        for (int j = 0; j < n; j++) {
            Sum[i][j] = A[i][j] + B[i][j];
            Diff[i][j] = A[i][j] - B[i][j];
        }
    }

    // Print A + B
    printf("\nMatrix A + B:\n");
    for (int i = 0; i < m; i++) {
        for (int j = 0; j < n; j++) {
            printf("%3d", Sum[i][j]);
        }
        printf("\n");
    }

    // Print A - B
    printf("\nMatrix A - B:\n");
    for (int i = 0; i < m; i++) {
        for (int j = 0; j < n; j++) {
            printf("%3d", Diff[i][j]);
        }
        printf("\n");
    }

    return 0;
}

////c program using array to calculate average, max, min of elements in an integer array.

#include <stdio.h>

int main() {
    int arr[100], n, i;
    int sum = 0, max, min;

    printf("Enter number of elements in the array (max 100): ");
    scanf("%d", &n);

    if (n <= 0 || n > 100) {
        printf("Invalid size!\n");
        return 1;
    }

    printf("Enter %d elements:\n", n);
    for (i = 0; i < n; i++) {
        scanf("%d", &arr[i]);
        sum += arr[i];
    }

    max = min = arr[0];

    for (i = 1; i < n; i++) {
        if (arr[i] > max) max = arr[i];
        if (arr[i] < min) min = arr[i];
    }

    printf("Sum = %d\n", sum);
    printf("Average = %.2f\n", (float)sum / n);
    printf("Maximum = %d\n", max);
    printf("Minimum = %d\n", min);

    return 0;
}
o/p-
Enter number of elements in the array (max 100): 5
Enter 5 elements:
1
2
3
4
5
Sum = 15
Average = 3.00
Maximum = 5
Minimum = 1

Chapter 8: Character array and strings (exercise questions)
//write a c program , which reads your name from the keyboard and outputs a list of ASCII codes, which represent your name.
#include <stdio.h>

int main() {
    char name[100];  // Array to store the name

    // Input the name
    printf("Enter your name: ");
    fgets(name, sizeof(name), stdin);  // Using fgets to read the name (supports spaces)

    // Output ASCII codes for each character
    printf("The ASCII codes for your name are:\n");
    for (int i = 0; name[i] != '\0'; i++) {
        printf("'%c' -> %d\n", name[i], name[i]);
    }

    return 0;
}

//write a  c program to do the following:
a)to output the question “who is the inventor of c?”
b)to accept an answer.
c)to print out “Good and then stop, if the answer is correct
d) to output the message “try again” , if the answer is wrong
e)to display the correct answer when the answer is wrong even at the third attempt and stop

#include <stdio.h>
#include <string.h>

int main() {
    char correctAnswer[14] = "Dennis Ritchie"; // Correct answer
    char userAnswer[50];                    // To store user's answer
    int attempts = 0;                       // Number of attempts

    while (attempts < 3) {
        // Output the question
        printf("Who is the inventor of C? ");
        
        // Accept the answer from the user
        fgets(userAnswer, sizeof(userAnswer), stdin);
        
        // Remove the newline character if present
        size_t len = strlen(userAnswer);
        if (len > 0 && userAnswer[len - 1] == '\n') {
            userAnswer[len - 1] = '\0';
        }

        // Check if the answer is correct
        if (strcmp(userAnswer, correctAnswer) == 0) {
            printf("Good!\n");
            return 0; // Stop the program
        } else {
            printf("Try again.\n");
            attempts++;
        }
    }

    // If all three attempts fail, display the correct answer
    printf("The correct answer is: %s\n", correctAnswer);

    return 0;
}

//write a c program to extract a portion of a character string and print the extracted string. Assume that m characters are extracted, starting with the nth character.
#include <stdio.h>
#include <string.h>

int main() {
    char str[100], substr[100];
    int n, m, len;

    printf("Enter a string: ");
    fgets(str, sizeof(str), stdin);

    printf("Enter the starting position (n): ");
    scanf("%d", &n);

    printf("Enter the number of characters to extract (m): ");
    scanf("%d", &m);

    len = strlen(str);

    // Adjust n and m to handle invalid input
    if (n < 0) {
        n = 0;
    }
    if (n >= len) {
        n = len - 1;
    }
    if (n + m > len) {
        m = len - n;
    }

    // Extract the substring
    strncpy(substr, str + n, m);
    substr[m] = '\0';

    printf("Extracted substring: %s\n", substr);

    return 0;
}
(or)
#include <stdio.h>
#include <string.h>

void extractSubstring(char *source, int start, int length, char *destination) {
    int i;
    for (i = 0; i < length && source[start + i] != '\0'; i++) {
        destination[i] = source[start + i];
    }
    destination[i] = '\0'; // Null-terminate the extracted substring
}

int main() {
    char str[100], extracted[100];
    int n, m;

    // Input the string
    printf("Enter a string: ");
    fgets(str, sizeof(str), stdin);

    // Remove the newline character from the input
    size_t len = strlen(str);
    if (len > 0 && str[len - 1] == '\n') {
        str[len - 1] = '\0';
    }

    // Input starting position and number of characters to extract
    printf("Enter the starting position (n): ");
    scanf("%d", &n);
    printf("Enter the number of characters to extract (m): ");
    scanf("%d", &m);

    // Ensure valid input (1-based index for user-friendliness, converted to 0-based)
    if (n < 1 || n > strlen(str)) {
        printf("Invalid starting position.\n");
        return 1;
    }

    // Extract the substring
    extractSubstring(str, n - 1, m, extracted);

    // Output the extracted substring
    printf("Extracted substring: \"%s\"\n", extracted);

    return 0;
}
(Note: rest of this chapter’s questions to be done later  from programming exercise 8.4)
Chapter 9: User – defined Functions (exercise questions)
////write a c function exchange to interchange the values of two variables, say x and y. illustrate the use of this function , in a calling function. Assume that x and y are defined as global variables.
#include<stdio.h>

int x,y;
void exchange()
{
    int temp;
    temp=x;
    x=y;
    y=temp;
}

int main()
{
    printf("please enter the value of x and y to swap:");
    scanf("\n%d\n%d",&x,&y);
    printf("\nthe value before swap: x=%d and y=%d",x,y);
    
    exchange();
    
    
    printf("\nthe value after swap x=%d and y=%d",x,y);
    
    return 0;
}

////write a c function space(x)  that can be used to provide a space of x positions between two output numbers. Demonstrate its application.

#include <stdio.h>

// Function to print x spaces
void space(int x) {
    for (int i = 0; i < x; i++) {
        printf(" ");
    }
}

int main() {
    int num1, num2, spaces;

    // Input two numbers
    printf("Enter the first number: ");
    scanf("%d", &num1);
    printf("Enter the second number: ");
    scanf("%d", &num2);

    // Input the number of spaces
    printf("Enter the number of spaces between the numbers: ");
    scanf("%d", &spaces);

    // Output the numbers with specified spaces
    printf("\nOutput:\n");
    printf("%d", num1);
    space(spaces);
    printf("%d\n", num2);

    return 0;
}

////The Fibonacci numbers are defined recursively as follows:
F1=1
F2=1
Fn=Fn-1 + Fn-2 ,n>2
Write a c function that will generate and print the first n Fibonacci numbers. Test the function for n=5,10,15

#include <stdio.h>

void fibonacci(int n) {
    int first = 0, second = 1, next, i;

    printf("Fibonacci Series:\n");

    for (i = 0; i < n; i++) {
        if (i <= 1) {
            next = i;
        } else {
            next = first + second;
            first = second;
            second = next;
        }
        printf("%d ", next);
    }

    printf("\n");
}

int main() {
    fibonacci(5);
    fibonacci(10);
    fibonacci(15);

    return 0;
}

////write a c function that will round a floating-point number to an indicated decimal place. For example the number 17.457 would yield the value 17.46 when it is rounded off to two decimal places.

#include <stdio.h>
#include <math.h>

// Function to round a floating-point number to a specified decimal place
double roundToDecimal(double number, int decimalPlaces) {
    double factor = pow(10, decimalPlaces); // Calculate the factor for shifting decimals
    return round(number * factor) / factor; // Shift, round, and shift back
}

int main() {
    double number;
    int decimalPlaces;

    // Input the number and the desired decimal places
    printf("Enter a floating-point number: ");
    scanf("%lf", &number);
    printf("Enter the number of decimal places to round to: ");
    scanf("%d", &decimalPlaces);

    // Call the rounding function
    double roundedNumber = roundToDecimal(number, decimalPlaces);

    // Output the result
    printf("The number %.10f rounded to %d decimal places is: %.10f\n", number, decimalPlaces, roundedNumber);

    return 0;
}

////write a c function prime that  returns 1 if its argument is a prime number and returns zero otherwise.
#include<stdio.h>

int prime(int num)
{
    if(num<=1)
    {
        return 0;
    }
    for(int i=2;i*i<=num;i++)
    {
        if(num%i==0)
        {
        return 0;
        }
    }
    return 1;
    
}
int main()
{
    int number;
    printf("enter a number to check prime:");
    scanf("%d",&number);
    
    if(prime(number))
    {
        printf("%d is a prime number",number);
    }
    else
    {
        printf("%d is not a prime number",number);
    }
    
    return 0;
}
    ////write a c function that will scan a character string passed as an argument and convert all lowercase characters into their uppercase equivalents.
#include <stdio.h>
#include <ctype.h> // For the toupper function

void to_uppercase(char *str) {
    for (int i = 0; str[i] != '\0'; i++) {
        if (islower(str[i])) { // Check if the character is lowercase
            str[i] = toupper(str[i]); // Convert to uppercase
        }
    }
}

int main() {
    char str[100];

    printf("Enter a string: ");
    fgets(str, sizeof(str), stdin); // Read a line of input including spaces

    to_uppercase(str);

    printf("String in uppercase: %s", str);

    return 0;
}

////Develop a top_down modular program to implement a calculator.The program should request the user to input two numbers and display one of the following as per the desire of the user:
a)sum of the numbers
b)difference of the numbers
c) product of the number
d)division of the numbers
provide separate functions for performing various tasks such as reading, calculating and displaying. Calculating module should call second level modules to perform the individual mathematical operations. The main function should have only function calls
#include <stdio.h>

// Function prototypes
void readNumbers(double *num1, double *num2);
void displayMenu();
void calculate(int choice, double num1, double num2);
void displayResult(const char *operation, double result);

// Second-level operation functions
double performSum(double a, double b);
double performDifference(double a, double b);
double performProduct(double a, double b);
double performDivision(double a, double b);

int main() {
    double num1, num2;
    int choice;

    readNumbers(&num1, &num2);

    while (1) {
        displayMenu();
        printf("Enter your choice (1-4) or 0 to exit: ");
        scanf("%d", &choice);

        if (choice == 0) {
            printf("Exiting the program.\n");
            break;
        }

        calculate(choice, num1, num2);
    }

    return 0;
}

// Function to read two numbers
void readNumbers(double *num1, double *num2) {
    printf("Enter the first number: ");
    scanf("%lf", num1);
    printf("Enter the second number: ");
    scanf("%lf", num2);
}

// Function to display the menu
void displayMenu() {
    printf("\nCalculator Menu:\n");
    printf("1. Sum\n");
    printf("2. Difference\n");
    printf("3. Product\n");
    printf("4. Division\n");
}

// Function to calculate and call second-level modules
void calculate(int choice, double num1, double num2) {
    double result;
    switch (choice) {
        case 1:
            result = performSum(num1, num2);
            displayResult("Sum", result);
            break;
        case 2:
            result = performDifference(num1, num2);
            displayResult("Difference", result);
            break;
        case 3:
            result = performProduct(num1, num2);
            displayResult("Product", result);
            break;
        case 4:
            if (num2 != 0) {
                result = performDivision(num1, num2);
                displayResult("Division", result);
            } else {
                printf("Error: Division by zero is not allowed.\n");
            }
            break;
        default:
            printf("Invalid choice. Please try again.\n");
    }
}

// Function to display the result
void displayResult(const char *operation, double result) {
    printf("The %s is: %.2f\n", operation, result);
}

// Second-level operation functions
double performSum(double a, double b) {
    return a + b;
}

double performDifference(double a, double b) {
    return a - b;
}

double performProduct(double a, double b) {
    return a * b;
}

double performDivision(double a, double b) {
    return a / b;
}

////develop a modular interactive c program using functions that reads the values of three sides of a triangle and displays either its area or its perimeter as per the request of the user. Given the three sides a,b,c. 
Perimenter=a+b+c
Area=root of(s-a)(s-b)(s-c)
Where s=(a+b+c)/2

#include <stdio.h>
#include <math.h>    // For sqrt()
#include <stdlib.h>  // For exit()

// Function prototypes
void readSides(double *a, double *b, double *c);
double calculatePerimeter(double a, double b, double c);
double calculateArea(double a, double b, double c);
void displayMenu();
void displayResult(const char *type, double value);

int main() {
    double a, b, c;
    int choice;

    readSides(&a, &b, &c);

    while (1) {
        displayMenu();
        printf("Enter your choice (1-2) or 0 to exit: ");
        scanf("%d", &choice);

        switch (choice) {
            case 1:
                displayResult("Perimeter", calculatePerimeter(a, b, c));
                break;
            case 2:
                displayResult("Area", calculateArea(a, b, c));
                break;
            case 0:
                printf("Exiting the program.\n");
                return 0;
            default:
                printf("Invalid choice. Please try again.\n");
        }
    }

    return 0;
}

// Function to read the sides of the triangle
void readSides(double *a, double *b, double *c) {
    printf("Enter the first side of the triangle: ");
    scanf("%lf", a);
    printf("Enter the second side of the triangle: ");
    scanf("%lf", b);
    printf("Enter the third side of the triangle: ");
    scanf("%lf", c);

    // Check if the sides form a valid triangle
    if ((*a + *b <= *c) || (*a + *c <= *b) || (*b + *c <= *a)) {
        printf("Error: The sides entered do not form a valid triangle.\n");
        exit(1); // Terminate the program if invalid triangle
    }
}

// Function to calculate the perimeter of the triangle
double calculatePerimeter(double a, double b, double c) {
    return a + b + c;
}

// Function to calculate the area of the triangle using Heron's formula
double calculateArea(double a, double b, double c) {
    double s = (a + b + c) / 2; // Semi-perimeter
    return sqrt(s * (s - a) * (s - b) * (s - c));
}

// Function to display the menu
void displayMenu() {
    printf("\nTriangle Menu:\n");
    printf("1. Calculate Perimeter\n");
    printf("2. Calculate Area\n");
    printf("0. Exit\n");
}

// Function to display the result
void displayResult(const char *type, double value) {
    printf("The %s of the triangle is: %.2f\n", type, value);
}

////write a c function that can be called to find the largest element of an m by n matrix
#include <stdio.h>

// Function prototype
int findLargest(int matrix[][100], int rows, int cols);

int main() {
    int m, n, i, j;
    int matrix[100][100];  // Assuming maximum size is 100x100

    // Input the dimensions of the matrix
    printf("Enter the number of rows: ");
    scanf("%d", &m);
    printf("Enter the number of columns: ");
    scanf("%d", &n);

    // Input the elements of the matrix
    printf("Enter the elements of the %dx%d matrix:\n", m, n);
    for (i = 0; i < m; i++) {
        for (j = 0; j < n; j++) {
            scanf("%d", &matrix[i][j]);
        }
    }

    // Call the function to find the largest element
    int largest = findLargest(matrix, m, n);
    printf("The largest element in the matrix is: %d\n", largest);

    return 0;
}

// Function to find the largest element in an m x n matrix
int findLargest(int matrix[][100], int rows, int cols) {
    int max = matrix[0][0];  // Initialize max with the first element

    for (int i = 0; i < rows; i++) {
        for (int j = 0; j < cols; j++) {
            if (matrix[i][j] > max) {
                max = matrix[i][j];
            }
        }
    }

    return max;
}


////write a c function that can be called to compute the product of two matrices of size m by n and n by m. the main function provides the values for m and n and two matrices.


#include <stdio.h>

// Function prototypes
void readMatrix(int rows, int cols, int matrix[][100]);
void printMatrix(int rows, int cols, int matrix[][100]);
void multiplyMatrices(int m, int n, int matrix1[][100], int matrix2[][100], int result[][100]);

int main() {
    int m, n;
    int matrix1[100][100], matrix2[100][100], result[100][100];

    // Input dimensions
    printf("Enter the number of rows (m) for the first matrix: ");
    scanf("%d", &m);
    printf("Enter the number of columns (n) for the first matrix: ");
    scanf("%d", &n);

    printf("The second matrix will have %d rows and %d columns.\n", n, m);

    // Input matrices
    printf("Enter the elements of the first matrix (%dx%d):\n", m, n);
    readMatrix(m, n, matrix1);

    printf("Enter the elements of the second matrix (%dx%d):\n", n, m);
    readMatrix(n, m, matrix2);

    // Multiply the matrices
    multiplyMatrices(m, n, matrix1, matrix2, result);

    // Display the result
    printf("The product of the matrices is:\n");
    printMatrix(m, m, result);

    return 0;
}

// Function to read a matrix
void readMatrix(int rows, int cols, int matrix[][100]) {
    for (int i = 0; i < rows; i++) {
        for (int j = 0; j < cols; j++) {
            scanf("%d", &matrix[i][j]);
        }
    }
}

// Function to print a matrix
void printMatrix(int rows, int cols, int matrix[][100]) {
    for (int i = 0; i < rows; i++) {
        for (int j = 0; j < cols; j++) {
            printf("%d ", matrix[i][j]);
        }
        printf("\n");
    }
}

// Function to multiply two matrices
void multiplyMatrices(int m, int n, int matrix1[][100], int matrix2[][100], int result[][100]) {
    // Initialize the result matrix to 0
    for (int i = 0; i < m; i++) {
        for (int j = 0; j < m; j++) {
            result[i][j] = 0;
        }
    }

    // Multiply the matrices
    for (int i = 0; i < m; i++) {
        for (int j = 0; j < m; j++) {
            for (int k = 0; k < n; k++) {
                result[i][j] += matrix1[i][k] * matrix2[k][j];
            }
        }
    }
}

////Design and code an interactive modular program that will use functions to a matrix of m by n size, compute column averages and row averages, and then print the entire matrix with averges shown in respective rows and columns.
#include <stdio.h>

#define MAX_ROWS 100
#define MAX_COLS 100

void inputMatrix(int matrix[MAX_ROWS][MAX_COLS], int rows, int cols);
void computeRowAverages(int matrix[MAX_ROWS][MAX_COLS], int rows, int cols, float rowAverages[MAX_ROWS]);
void computeColumnAverages(int matrix[MAX_ROWS][MAX_COLS], int rows, int cols, float colAverages[MAX_COLS]);
void printMatrixWithAverages(int matrix[MAX_ROWS][MAX_COLS], int rows, int cols, float rowAverages[MAX_ROWS], float colAverages[MAX_COLS]);

int main() {
    int rows, cols;
    int matrix[MAX_ROWS][MAX_COLS];
    float rowAverages[MAX_ROWS];
    float colAverages[MAX_COLS];

    // Input the matrix dimensions
    printf("Enter the number of rows (max %d): ", MAX_ROWS);
    scanf("%d", &rows);

    printf("Enter the number of columns (max %d): ", MAX_COLS);
    scanf("%d", &cols);

    if (rows <= 0 || rows > MAX_ROWS || cols <= 0 || cols > MAX_COLS) {
        printf("Invalid dimensions!\n");
        return 1;
    }

    // Input the matrix
    inputMatrix(matrix, rows, cols);

    // Compute averages
    computeRowAverages(matrix, rows, cols, rowAverages);
    computeColumnAverages(matrix, rows, cols, colAverages);

    // Print matrix with averages
    printMatrixWithAverages(matrix, rows, cols, rowAverages, colAverages);

    return 0;
}

void inputMatrix(int matrix[MAX_ROWS][MAX_COLS], int rows, int cols) {
    printf("Enter the elements of the matrix:\n");
    for (int i = 0; i < rows; i++) {
        for (int j = 0; j < cols; j++) {
            printf("Element [%d][%d]: ", i + 1, j + 1);
            scanf("%d", &matrix[i][j]);
        }
    }
}

void computeRowAverages(int matrix[MAX_ROWS][MAX_COLS], int rows, int cols, float rowAverages[MAX_ROWS]) {
    for (int i = 0; i < rows; i++) {
        int sum = 0;
        for (int j = 0; j < cols; j++) {
            sum += matrix[i][j];
        }
        rowAverages[i] = (float)sum / cols;
    }
}

void computeColumnAverages(int matrix[MAX_ROWS][MAX_COLS], int rows, int cols, float colAverages[MAX_COLS]) {
    for (int j = 0; j < cols; j++) {
        int sum = 0;
        for (int i = 0; i < rows; i++) {
            sum += matrix[i][j];
        }
        colAverages[j] = (float)sum / rows;
    }
}

void printMatrixWithAverages(int matrix[MAX_ROWS][MAX_COLS], int rows, int cols, float rowAverages[MAX_ROWS], float colAverages[MAX_COLS]) {
    printf("\nMatrix with row and column averages:\n");

    for (int i = 0; i < rows; i++) {
        for (int j = 0; j < cols; j++) {
            printf("%5d ", matrix[i][j]);
        }
        printf("| %6.2f\n", rowAverages[i]);
    }

    for (int j = 0; j < cols; j++) {
        printf("-------");
    }
    printf("---------\n");

    for (int j = 0; j < cols; j++) {
        printf("%6.2f ", colAverages[j]);
    }
    printf("\n");
}

////develop your own c functions for performing following operations on strings:
a)copying one string to another
b)comparing two strings
c) adding a string to  the end of another string
write a driver program to test your functions.
#include <stdio.h>
#include <string.h>

// Function prototypes
void copyString(char *destination, const char *source);
int compareStrings(const char *str1, const char *str2);
void concatenateStrings(char *destination, const char *source);

int main() {
    char str1[100], str2[100], result[200];
    int comparison;

    // Test copyString
    printf("Enter the source string to copy: ");
    fgets(str1, sizeof(str1), stdin);
    str1[strcspn(str1, "\n")] = '\0'; // Remove trailing newline

    copyString(result, str1);
    printf("Copied string: %s\n", result);

    // Test compareStrings
    printf("Enter the first string for comparison: ");
    fgets(str1, sizeof(str1), stdin);
    str1[strcspn(str1, "\n")] = '\0';

    printf("Enter the second string for comparison: ");
    fgets(str2, sizeof(str2), stdin);
    str2[strcspn(str2, "\n")] = '\0';

    comparison = compareStrings(str1, str2);
    if (comparison == 0) {
        printf("The strings are equal.\n");
    } else if (comparison < 0) {
        printf("The first string is less than the second string.\n");
    } else {
        printf("The first string is greater than the second string.\n");
    }

    // Test concatenateStrings
    printf("Enter the first string to concatenate: ");
    fgets(str1, sizeof(str1), stdin);
    str1[strcspn(str1, "\n")] = '\0';

    printf("Enter the second string to concatenate: ");
    fgets(str2, sizeof(str2), stdin);
    str2[strcspn(str2, "\n")] = '\0';

    copyString(result, str1); // Initialize result with str1
    concatenateStrings(result, str2);
    printf("Concatenated string: %s\n", result);

    return 0;
}

void copyString(char *destination, const char *source) {
    while (*source) {
        *destination = *source;
        destination++;
        source++;
    }
    *destination = '\0';
}

int compareStrings(const char *str1, const char *str2) {
    while (*str1 && *str2 && (*str1 == *str2)) {
        str1++;
        str2++;
    }
    return *str1 - *str2;
}

void concatenateStrings(char *destination, const char *source) {
    while (*destination) {
        destination++;
    }
    while (*source) {
        *destination = *source;
        destination++;
        source++;
    }
    *destination = '\0';
}

////write a c function that takes an integer parameter m representing the month number of   the year and returns the corresponding name of the month. For istance, , if m=3, the month is March.Test your code.
#include <stdio.h>

void printMonthName(int m) {
    // Using switch statement to print the corresponding month name
    switch (m) {
        case 1:
            printf("The month is: January\n");
            break;
        case 2:
            printf("The month is: February\n");
            break;
        case 3:
            printf("The month is: March\n");
            break;
        case 4:
            printf("The month is: April\n");
            break;
        case 5:
            printf("The month is: May\n");
            break;
        case 6:
            printf("The month is: June\n");
            break;
        case 7:
            printf("The month is: July\n");
            break;
        case 8:
            printf("The month is: August\n");
            break;
        case 9:
            printf("The month is: September\n");
            break;
        case 10:
            printf("The month is: October\n");
            break;
        case 11:
            printf("The month is: November\n");
            break;
        case 12:
            printf("The month is: December\n");
            break;
        default:
            printf("Invalid Month\n");
    }
}

int main() {
    int m;
    
    // Test the function
    printf("Enter a month number (1-12): ");
    scanf("%d", &m);
    
    // Call the function to print the month name
    printMonthName(m);
    
    return 0;
}
////in preparing the calender for a year we need to know whether that particular year is leap or not. Design a function leap() that receives the year as a parameter and returns an appropriate message.

What modifications are required if we want to use the function in preparing the actual calender?
#include <stdio.h>

void leap(int year) {
    // Check if the year is divisible by 4 and not divisible by 100,
    // or divisible by 400.
    if ((year % 4 == 0 && year % 100 != 0) || (year % 400 == 0)) {
        printf("%d is a leap year.\n", year);
    } else {
        printf("%d is not a leap year.\n", year);
    }
}

int main() {
    int year;
    
    // Test the leap function
    printf("Enter a year: ");
    scanf("%d", &year);
    
    // Call the leap function to check if the year is a leap year
    leap(year);
    
    return 0;
}

////write a c function that receives a floating point value x and returns it as a value rounded to two nearest decimal places. For example, the value 123.4567 will be rounded to 123.46(hint: seek help of one the math functions available in math library).
#include <stdio.h>
#include <math.h>

float roundToTwoDecimals(float x) {
    // Multiply by 100, round to the nearest integer, then divide by 100
    return round(x * 100) / 100;
}

int main() {
    float x;
    
    // Input the floating-point value
    printf("Enter a floating-point number: ");
    scanf("%f", &x);
    
    // Call the function and display the result
    printf("Rounded to two decimal places: %.2f\n", roundToTwoDecimals(x));
    
    return 0;
}

Chapter 10- Structures and Unions
----STRUCTURES-----
-In C, a structure (struct) is a user-defined data type that groups different types of variables (called members) under a single name.
-Syntax:

struct StructureName {
    data_type member1;
    data_type member2;
    ...
};
-Each member can be of different type.

-Structures are used to model real-world entities (like a student, book, employee).

-Memory is allocated for all members individually (unlike unions).

-Access members using the dot operator (.) for normal variables or arrow operator (->) for pointers.

---UNIONS---
-A union can hold only one value at a time — the most recently assigned member.

-Memory is shared, so assigning one member overwrites others.

-Size of a union = size of its largest member.

////define a structure data type called time_struct containing three members integer hour, integer minute and integer second. Develop a program that would assign values to the individual members and display the time in the following form:16:40:51
#include <stdio.h>

// Define the structure
typedef struct {
    int hour;
    int minute;
    int second;
} time_struct;

int main() {
    // Declare a variable of type time_struct
    time_struct currentTime;
    
    // Assign values to the structure members
    currentTime.hour = 16;
    currentTime.minute = 40;
    currentTime.second = 51;
    
    // Display the time in the required format
    printf("The time is: %02d:%02d:%02d\n", currentTime.hour, currentTime.minute, currentTime.second);
    
    return 0;
}

////Modify the above program such that a function is used to input values to the members and another function to display the time.
#include <stdio.h>

// Define the structure
typedef struct {
    int hour;
    int minute;
    int second;
} time_struct;

// Function to input time values
time_struct inputTime() {
    time_struct t;
    printf("Enter hours (0-23): ");
    scanf("%d", &t.hour);
    printf("Enter minutes (0-59): ");
    scanf("%d", &t.minute);
    printf("Enter seconds (0-59): ");
    scanf("%d", &t.second);
    return t;
}

// Function to display the time
void displayTime(time_struct t) {
    printf("The time is: %02d:%02d:%02d\n", t.hour, t.minute, t.second);
}

int main() {
    // Declare a variable of type time_struct
    time_struct currentTime;

    // Input time values
    currentTime = inputTime();

    // Display the time
    displayTime(currentTime);

    return 0;
}

////design a function update that would accept the data structure as above and increments time by one second and returns the new time.(if the increments results in 60 seconds, then the second member is set to zero and the minute member is incremented by one. Then, if the result is 60 minutes, then the minutes member is set to zero and the hour member is incremented by one. Finally, when the hour becomes 24, it is set to zero).
#include <stdio.h>

// Define the structure
typedef struct {
    int hour;
    int minute;
    int second;
} time_struct;

// Function to input time values
time_struct inputTime() {
    time_struct t;
    printf("Enter hours (0-23): ");
    scanf("%d", &t.hour);
    printf("Enter minutes (0-59): ");
    scanf("%d", &t.minute);
    printf("Enter seconds (0-59): ");
    scanf("%d", &t.second);
    return t;
}

// Function to display the time
void displayTime(time_struct t) {
    printf("The time is: %02d:%02d:%02d\n", t.hour, t.minute, t.second);
}

// Function to update the time by one second
time_struct update(time_struct t) {
    t.second++;  // Increment the seconds by one

    // Check if seconds exceed 59
    if (t.second == 60) {
        t.second = 0;  // Reset seconds
        t.minute++;    // Increment minutes

        // Check if minutes exceed 59
        if (t.minute == 60) {
            t.minute = 0;  // Reset minutes
            t.hour++;      // Increment hours

            // Check if hours exceed 23
            if (t.hour == 24) {
                t.hour = 0;  // Reset hours
            }
        }
    }

    return t;  // Return the updated time
}

int main() {
    // Declare a variable of type time_struct
    time_struct currentTime;

    // Input the initial time
    currentTime = inputTime();

    // Display the current time
    printf("Before update:\n");
    displayTime(currentTime);

    // Update the time by one second
    currentTime = update(currentTime);

    // Display the updated time
    printf("After update:\n");
    displayTime(currentTime);

    return 0;
}
////C program demonstrating both structures and unions — showing their syntax, memory usage difference, and basic usage
#include <stdio.h>
#include <string.h>

// Define a structure
struct Student {
    int id;
    char name[20];
    float marks;
};

// Define a union
union Data {
    int i;
    float f;
    char str[20];
};

int main() {
    // Using Structure
    struct Student s1;
    s1.id = 101;
    strcpy(s1.name, "Alice");
    s1.marks = 95.5;

    printf("Structure:\n");
    printf("ID: %d\n", s1.id);
    printf("Name: %s\n", s1.name);
    printf("Marks: %.2f\n", s1.marks);

    // Using Union
    union Data d1;

    d1.i = 10;
    printf("\nUnion:\n");
    printf("Integer: %d\n", d1.i);

    d1.f = 220.5;
    printf("Float (overwrites int): %.2f\n", d1.f);

    strcpy(d1.str, "Hello");
    printf("String (overwrites float): %s\n", d1.str);

    // Size comparison
    printf("\nSize of structure: %lu bytes\n", sizeof(s1));
    printf("Size of union: %lu bytes\n", sizeof(d1));

    return 0;
}
o/p-
Structure:
ID: 101
Name: Alice
Marks: 95.50

Union:
Integer: 10
Float (overwrites int): 220.50
String (overwrites float): Hello

Size of structure: 28 bytes
Size of union: 20 bytes

Chapter 11-Pointer

////write a c program using pointers to read in an array of integers and print its elements in reverse order.

#include <stdio.h>

void printReverse(int *arr, int size) {
    printf("Array in reverse order:\n");
    for (int *ptr = arr + size - 1; ptr >= arr; ptr--) {
        printf("%d ", *ptr);
    }
    printf("\n");
}

int main() {
    int n;

    // Input the size of the array
    printf("Enter the number of elements in the array: ");
    scanf("%d", &n);

    int arr[n];

    // Input the elements of the array
    printf("Enter %d integers:\n", n);
    for (int i = 0; i < n; i++) {
        scanf("%d", &arr[i]);
    }

    // Call the function to print the array in reverse order
    printReverse(arr, n);

    return 0;
}

///C simple pointer program to add two numbers:
#include <stdio.h>

int main() {
    int num1, num2, sum;
    int *ptr1, *ptr2;

    // Input numbers
    printf("Enter first number: ");
    scanf("%d", &num1);

    printf("Enter second number: ");
    scanf("%d", &num2);

    // Pointers point to the variables
    ptr1 = &num1;
    ptr2 = &num2;

    // Add using pointers
    sum = *ptr1 + *ptr2;

    // Output result
    printf("Sum = %d\n", sum);

    return 0;
}
o/p- 
Enter first number: 2
Enter second number: 6
Sum = 8

///C pointer program to swap two numbers:

#include <stdio.h>

void swap(int *x, int *y) {
    int temp;

    temp = *x;
    *x = *y;
    *y = temp;
}

int main() {
    int a, b;

    // Input values
    printf("Enter value for a: ");
    scanf("%d", &a);

    printf("Enter value for b: ");
    scanf("%d", &b);

    // Before swap
    printf("Before swap: a = %d, b = %d\n", a, b);

    // Swap using pointers
    swap(&a, &b);

    // After swap
    printf("After swap: a = %d, b = %d\n", a, b);

    return 0;
}
o/pp-
Enter value for a: 3
Enter value for b: 5
Before swap: a = 3, b = 5
After swap: a = 5, b = 3


////write a function (using pointer parameters) that compares two integer arrays to see whether they are identical . The function returns 1 if they are identical, 0 otherwise.
#include <stdio.h>

// Function to compare two integer arrays
int compareArrays(int *arr1, int *arr2, int size) {
    for (int i = 0; i < size; i++) {
        if (*(arr1 + i) != *(arr2 + i)) { // Compare elements using pointers
            return 0; // Return 0 if any element is different
        }
    }
    return 1; // Return 1 if all elements are identical
}

int main() {
    int size;

    // Input the size of the arrays
    printf("Enter the size of the arrays: ");
    scanf("%d", &size);

    int arr1[size], arr2[size];

    // Input elements for the first array
    printf("Enter elements of the first array:\n");
    for (int i = 0; i < size; i++) {
        scanf("%d", &arr1[i]);
    }

    // Input elements for the second array
    printf("Enter elements of the second array:\n");
    for (int i = 0; i < size; i++) {
        scanf("%d", &arr2[i]);
    }

    // Compare the arrays
    if (compareArrays(arr1, arr2, size)) {
        printf("The arrays are identical.\n");
    } else {
        printf("The arrays are not identical.\n");
    }

    return 0;
}











