# OS-EX.9-IMPLEMENTATION-OF-PAGING---MEMORY-MANAGEMENT-

AIM:
To write a c program to implement Paging technique for memory management.
ALGORITHM:
* Read all the necessary input from the keyboard.
* Pages - Logical memory is broken into fixed - sized blocks.
* Frames – Physical memory is broken into fixed – sized blocks.
* Calculate the physical address using the logical address.
* Physical address = (Frame number * Frame size) + offset.
* Display the physical address.
* Stop the process.

PROGRAM:
```python
#include<stdio.h>
int main()
{
int i,j,n,a[50],frame[10],no,k,avail,count=0;
printf("\n ENTER THE NUMBER OF PAGES:\n");
scanf("%d",&n);
printf("\n ENTER THE PAGE NUMBER :\n");
for(i=1;i<=n;i++)
scanf("%d",&a[i]);
printf("\n ENTER THE NUMBER OF FRAMES :");
scanf("%d",&no);
for(i=0;i<no;i++)
frame[i]= -1;
j=0;
printf("\tRef string\t Page Frames\n");
for(i=1;i<=n;i++)
{
printf("%d\t\t\t",a[i]);
avail=0;
for(k=0;k<no;k++)
if(frame[k]==a[i])
avail=1;
if (avail==0)
{
frame[j]=a[i];
j=(j+1)%no;
count++;
for(k=0;k<no;k++)
printf("%d\t",frame[k]);
}
printf("\n");
}
printf("\nPage Fault Is %d",count);
return 0;
}
```
OUTPUT:
![image](https://github.com/Raja8334/OS-EX.9-IMPLEMENTATION-OF-PAGING---MEMORY-MANAGEMENT-/assets/120719634/df59bdf5-57ad-492f-b244-0bc1c273c353)

RESULT:
Thus, the implementation of paging technique for memory management is executed successfully.
