#include <stdio.h>
#define MAX 10
void swapList(int *m,int *n){
   int temp;
   temp = *m;
   *m = *n;
   *n = temp;
}
/* Function for Bubble Sort */
void bub_sort(int list[], int n){
   int i,j;
   for(i=0;i<(n-1);i++)
      for(j=0;j<(n-(i+1));j++)
         if(list[j] > list[j+1])
            swapList(&list[j],&list[j+1]);
   }
   void readlist(int list[],int n){
   int j;
   printf("
Enter the elements: 
");
   for(j=0;j<n;j++)
      scanf("%d",&list[j]);
   }
   /* Showing the contents of the list */
   void printlist(int list[],int n){
      int j;
   for(j=0;j<n;j++)
      printf("%d\t",list[j]);
}
void main(){
   int list[MAX], num;
   printf(" Enter the number of elements 
");
   scanf("%d",&num);
   readlist(list,num);
   printf("

Elements in the list before sorting are:
");
   printlist(list,num);
   bub_sort(list,num);
   printf("

Elements in the list after sorting are:
");
   printlist(list,num);
}
