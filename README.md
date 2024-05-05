#include<stdio.h>
int main()
{
    int n,i,item,last,middle,first,a[100];
    printf("Enter the number of elements you want in an array\n");
    scanf("%d",&n);
    printf("enter the element in an array\n");
    for(i=0;i<n;i++)
    {
        scanf("%d",&a[i]);
    }
    printf("looking for an item:-");
    scanf("%d",&item);
    first = 0;
    last = n-1;
    middle=(first+last)/2;
    while(first<=last)
    {
        if(a[middle]<item)
        {
            first=middle+1;
            middle=(first-last)+last/2;
        }
        else if(a[middle]==item)
        {
            printf("\nthe number,%d found at position %d",item,middle+1);
            break;
        }
        else
        {
            last=middle-1;
            middle=(first-last)+last/2;
        }
    }
    if(first>last)
    printf("\n the number %d is not found in a given array",item); 
    return 0;
} 
