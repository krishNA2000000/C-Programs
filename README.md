# C-ProgramsAndProjects
//first c program

#include<stdio.h>

int main()
{
    printf("Seedha betho, Apna dekho, Mehnat karo!!");
    
    return 0;
}
Op-Seedha betho, Apna dekho, Mehnat karo!!



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

//representation of integer constants on 16-bit machine
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
//printing even number between 1-100
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
Programming exercise (chapter 1)
//1.1equation of line ax+by=c
#include<stdio.h>

int main()
{
    int a=5,b=8,c=18;
    
    
    
    printf("%dx + %dy = %d",a,b,c);
    
    return 0;
}

o/p-5x + 8y = 18

//1.2 mailing address in the following form
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
//1.3 multiplication table 
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

