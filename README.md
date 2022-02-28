# DAA
#include <stdio.h>
int main()
{
    int n , i , min , max;
    int a[10];
    printf("enter the size of an element\n");
    scanf("%d",&n);
    printf("enter an element in array: \n");
    for(i=0; i<n; i++)
    {
        scanf("%d",&a[i]);
    }
    max=a[0];
    for(i=0; i<n; i++)
    {
        if(a[i]>max)
        {
            max=a[i];
        }
        
    }
    min=a[0];
    for(i=0; i<n; i++)
    {
        if(a[i]<min)
        {
            min=a[i];
        }
    }
    printf("%d max number\n",max);
    printf("%d min number\n",min);
}
