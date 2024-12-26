PRINTING PATTERN:
7*8*9*10

4*5*6

2*3

1

PREREQUISITE:
Basic knowledge of C language and use of loops.

ALGORITHM:
Take the number of rows/columns as input from the user and store it in any variable.(‘r‘ in this case).
Run a loop ‘r’ number of times to iterate through each of the rows. From i=0 to i<r The loop should be structured as for( i=0 ; i<r: i++).
and add the ‘i’ value to count.
Run another loop ‘r’ number of times to iterate through each of the rows. From i=0 to i<r The loop should be structured as for( i=0 ; i<r: i++).
Reinitialise the value of count as count=count-r+1  then give the same value to count1
Run a nested loop to iterate through the columns. From j=0 to j<r. The loop should be structured as for(j=0 ; j<r; j++).
increment count and run an if condition if(j!=r).
if true then print star and count else print only count.
outside the nested loop print a newline
Then give value of count1 to count
CODE IN C:
#include<stdio.h>
int main()
{
int i,j,r,count,count1;                      //declaring integer variables i,j for loops , r for number of rows and count for increment in value
count=0;                                     //initialising count
printf("Enter the number of rows :\n");      //Asking user for input
scanf("%d",&r);                              //taking number of rows and saving it in variable r
for(i=1;i<=r;i++)                            //loop to calculate max value of count
  {
    count+=i;                                //incrementing count
  }
for(i=0;i<r;i++)                             // loop for number of rows
  {
    count=count-r+i;                         //changing value of count 
    count1=count;                            //giving value of count to count1
    for(j=r;j>i;j--)                         // loop for digits per each row
     {
       count++;                              //incrementing count
       if(j!=r)                              //if condition to print star and digit
       printf("*%d",count);                  //printng star and digit
       else                                  //else condition to print only digit
       printf("%d",count);                   //printing digits
     }
    printf("\n");                            //printing newline
    count =count1;                            // giving count its original value
  }
}
TAKING INPUT:DISPLAYING OUTPUT:
