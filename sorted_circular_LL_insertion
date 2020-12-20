#include<stdio.h>
#include<stdlib.h>
    struct node
    {
        int info;
        struct node *next;
    };
    struct node *newnode, *head, *temp;
    int choice = 1;
    int count;
void counts(){
temp = head;
count = 0;
do{
    printf("%d ",temp->info);
    count++;
    temp = temp->next;
}while(temp!=head);
printf("\ntotal no. of nodes are %d",count);
}
void main(){
    struct node *ploc;
    printf("enter a sorted list\n");
   head = 0;
   while(choice){
    newnode = (struct node *)malloc(sizeof(struct node));
printf("\nenetr the data: ");
scanf("%d",&newnode->info);
if(head==0){
    head = temp = newnode;
}
else{
     temp->next = newnode;
     temp = newnode;
}
temp->next = head;
printf("if you want to insert more type 1 else 0: ");
scanf("%d",&choice);
}
counts();
temp = head;
newnode = (struct node *)malloc(sizeof(struct node));
printf("\nenter the element you want to insert: ");
scanf("%d",&newnode->info);
if(newnode->info<head->info){
       while(temp->next!=head){
        temp =temp->next;
       }
       newnode->next = head;
       temp->next = newnode;
       head = newnode;
       }
       else{
        do{
            ploc = temp;
            temp = temp->next;
        }while(temp!=head&&newnode->info>temp->info);
        if(temp == head){
            ploc->next = newnode;
            newnode->next = head;
        }
        else{
       ploc->next = newnode;
       newnode->next = temp;
       }}
       counts();
       printf("\nprogram finished");
}
