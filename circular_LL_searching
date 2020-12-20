
#include<stdio.h>
#include<stdlib.h>
void main()
{
    struct node
    {
        int info;
        struct node *next;
    };
    struct node *newnode, *head, *temp;
    int choice = 1;
    int count = 0;
    int item;
    printf("if youn want to insert data enetr 1 else 0: ","\n");
    scanf("%d",&choice);
   head = 0;
   while(choice){
    newnode = (struct node *)malloc(sizeof(struct node));
printf("enetr the data: ");
scanf("%d",&newnode->info);
if(head==0){
    head = temp = newnode;

}
else{

     temp->next = newnode;
     temp = newnode;
}
temp->next = head;
printf("\nif you want to insert more type 1 else 0: ");
scanf("%d",&choice);}
temp = head;
do{
    printf("%d ",temp->info);
    count++;
    temp = temp->next;
}while(temp!=head);
printf("\ntotal no. of nodes are %d",count);

 printf("\nenter the item you want to search: ");
       scanf("%d",&item);
       count = 0;
       temp = head;
      do{
            count++;
            if(temp->info==item){
                break;}
            else{
         temp = temp->next;
}
       }while(temp!=head);
       if(temp->next!=head){
        printf("item is found at position %d",count);
       }
       else if(temp==head){
        printf("\nitem not found");
       }
       else{
         printf("\nitem is found at  position %d", count);
       }



    printf("\nfinished");



}
