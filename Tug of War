#include<stdio.h>
#include<stdlib.h>
int main()
{
int n;
scanf("%d",&n);
int a[n];
for(int i=0;i<n;i++)
{
scanf("%d",&a[i]);
}
int sum=0;
for(int i=0;i<n;i++)
{
sum=sum+a[i];
}
int min=a[0];
for(int i=0;i<=sum;i++)
{
int a=i;
int b=sum-a;
int diff=abs(a-b);
if(diff<min)
min=diff;
}
printf("%d",min);
return 0;
}
