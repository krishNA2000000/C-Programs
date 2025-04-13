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
