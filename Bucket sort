#include <stdio.h>
#include <stdlib.h>
typedef struct Node
{
float data;
struct Node *next;
} 
Node;
void insertSorted(Node **head,float value)
{
Node *newNode=(Node *)malloc(sizeof(Node));
newNode->data=value;
newNode->next=NULL;
if(*head==NULL||(*head)->data>=value)
{
newNode->next=*head;
*head=newNode;
return;
}
Node *curr=*head;
while(curr->next!=NULL && curr->next->data<value)
curr=curr->next;
newNode->next=curr->next;
curr->next=newNode;
}
int main()
{
int n;
scanf("%d",&n);
float arr[n];
for(int i=0;i<n;i++)
scanf("%f",&arr[i]);
Node *bucket[n];
for(int i=0;i<n;i++)
bucket[i]=NULL;
for(int i=0;i<n;i++)
{
int index=(int)(arr[i] * n);
if(index>=n)
index=n-1;
insertSorted(&bucket[index],arr[i]);
}
for(int i=0;i<n;i++)
{
Node *temp=bucket[i];
while(temp!=NULL)
{
if(temp->data==(int)temp->data)
printf("%d ",(int)temp->data);
else
printf("%.2f ",temp->data);
Node *del=temp;
temp=temp->next;
free(del);
}
}
return 0;
}
