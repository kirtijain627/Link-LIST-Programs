#include<stdio.h>
#include<stdlib.h>
struct node
    {
        int info;
        struct node *next;
    };
    typedef struct node NODE;
    NODE *head = 0, *newnode, *temp;
    int count;
    void counts(){
           count = 0;
       temp = head;
       while(temp!=0){
           printf("%d ",temp->info);
           count++;
           temp = temp->next;
    }
       printf("\nno. of nodes are %d",count);}





void main()
{
   int choice = 1;
   int item;

    while(choice){

           newnode = (NODE *)malloc(sizeof(NODE));
           printf("enter the info: ");
           scanf("%d",&newnode->info);
           if(head==0){
               head = temp = newnode;
        }
           else{
               temp->next = newnode;
               temp = newnode;
        }
           printf("Do you want to continue type 0 or 1: ","\n");
           scanf("%d",&choice);
    }
       temp->next = 0;
       counts();

       printf("\nenter the item you want to search: ");
       scanf("%d",&item);
       count = 0;
       temp = head;
       while(temp!=0){
            count++;
            if(temp->info==item){
                break;}
            else{
        temp = temp->next;

       }
       }
       if(temp==0){
        printf("\nitem not found");
       }
       else{
         printf("\nitem is found at  position %d", count);
       }



    printf("\nfinished");

}

