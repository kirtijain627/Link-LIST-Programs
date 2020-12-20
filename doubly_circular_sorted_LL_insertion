#include<stdio.h>
#include<stdlib.h>
 struct node
    {
        int info;
        struct  node *plink, *flink;
    };
    struct node *head, *temp, *newnode;
    int choice = 1;
    int count;

void counts()
    {
        count = 0;
        temp = head;
    do{
        printf("%d ",temp->info);
        temp = temp->flink;
        count++;
    }while(temp!=head);
     printf("\nno. of nodes are %d",count);
    }

void main()
{
   printf("enter a sorted list\n");
   head = 0;
    printf("if you want to enter in list type 1 else 0: ","\n");
    scanf("%d",&choice);
    while(choice){
       newnode = (struct node *)malloc(sizeof(struct node));
       printf("enter the info :");
       scanf("%d",&newnode->info);
       if(head==0){
        head = temp = newnode;
       }
       else{
        temp->flink = newnode;
        newnode->plink = temp;
        temp = newnode;
       }
       newnode->flink = head;
       head->plink = newnode;
       printf("if you want to enter more type 1 else 0: ");
       scanf("%d",&choice);
    }
    counts();

temp = head;
newnode = (struct node *)malloc(sizeof(struct node));
printf("\nenter the element you want to insert: ");
scanf("%d",&newnode->info);
if(newnode->info<head->info){
    newnode->flink = head;
    newnode->plink = head->plink;
    head->plink->flink = newnode;
    head->plink = newnode;
    head = newnode;
}
else {

             do{
                    temp = temp->flink;
             } while(newnode->info>temp->info&&temp->flink!=head);
        if(temp == head){
    newnode->flink = head;
    newnode->plink = temp;
    temp->flink = newnode;
    head->plink = newnode;
}

else {
    newnode->flink = temp;
temp->plink->flink = newnode;
temp->plink = newnode;
newnode->plink = temp->plink;
}}
counts();
printf("\nprogram finished");
}
