#include<stdio.h>
#include<stdlib.h>
struct node
    {
        int info;
        struct node *next;
    };
    typedef struct node NODE;
    NODE *head, *newnode, *temp=0;
    int choice=1;
    int count;

void counts(){
       temp = head;
       count = 0;
       while(temp!=0){
           printf("%d ",temp->info);
           count++;
           temp = temp->next;
    }
       printf("\nno. of nodes are %d",count);
}
void main()
{
   struct node *ploc;
    head = 0;
    printf("enter a sorted list: ");
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
           printf("\nDo you want to continue type 0 or 1: ","\n");
           scanf("%d",&choice);
    }
       temp->next = 0;
       counts();
       newnode = (NODE *)malloc(sizeof(NODE));
       printf("enter the value: ");
       scanf("%d",&newnode->info);
       if(newnode->info<head->info){
        newnode->next = head;
        head = newnode;
       }
       else{
       temp = head;

        while(temp!=0&&newnode->info>temp->info){
            ploc = temp;
            temp = temp->next;
        }
       ploc->next = newnode;
       newnode->next = temp;

       }
       counts();

       printf("\nprogram finished");


}

