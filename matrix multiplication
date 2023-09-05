#include <stdio.h>
#include<stdlib.h>  
 
void main()
{  
 
int a[10][10],b[10][10],c[10][10],r1,c1,r2,c2,i,j,k;    
 
printf("Enter the number of rows in first matrix: ");    
scanf("%d",&r1);
 
printf("Enter the number of columns in first matrix: ");    
scanf("%d",&c1);    
 
printf("Enter the first matrix: \n");    
 
for(i=0;i<r1;i++)    
{    
for(k=0;k<c1;k++)    
{    
scanf("%d",&a[i][k]);    
}    
}    
 
printf("Enter the number of rows in second matrix: ");    
scanf("%d",&r2);
 
printf("Enter the number of columns in second matrix: ");    
scanf("%d",&c2);    
 
printf("Enter the second matrix: \n");    
 
for(k=0;k<r2;k++)    
{    
for(j=0;j<c2;j++)    
{    
scanf("%d",&b[k][j]);    
}    
}    
 
if (c1==r2)
{
 
for(i=0;i<r1;i++)    
{    
for(j=0;j<c2;j++)    
{    
c[i][j] = 0;
 
for(k=0;k<c1;k++)    
{    
c[i][j] += a[i][k] * b[k][j];    
}   
}
}
 
printf ("Matrix after Multiplication:\n");
for(i=0;i<r1;i++)    
{    
for(j=0;j<c2;j++)    
{    
printf ("%d",c[i][j]);  
printf ("\n");
}
}
}
 
else
printf ("Multiplication not possible.");
}
