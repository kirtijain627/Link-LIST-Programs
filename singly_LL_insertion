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
    int count=0;

    void inserting_linked_list_beg()
    {
       newnode = (NODE *)malloc(sizeof(NODE));
       printf("\nenter the info: ");
       scanf("%d",&newnode->info);
       newnode->next = head;
       head = newnode;
       temp = head;
       count = 0;
       while(temp!=0){
          printf("%d ",temp->info);
          count++;
          temp = temp->next;
    }
       printf("no. of nodes are %d",count);
}

void inserting_linked_list_anylocation()
{
    int pos;
    int i=1;
    printf("\nenetr the position after which you want to insert: ");
    scanf("%d",&pos);
    if(pos>count){
        printf("invalid position");
    }
               else{

                temp = head;
                while(i<pos){
                temp = temp->next;
                i++;
                }
            newnode = (NODE *)malloc(sizeof(NODE));
            printf("\nenter the info: ");
            scanf("%d",&newnode->info);

            newnode->next = temp->next;
            temp->next = newnode;}


            temp = head;
            count = 0;
            while(temp!=0){
                 printf("%d ",temp->info);
                 count++;
                 temp = temp->next;
            }
}
void at_end()
{
            newnode = (NODE *)malloc(sizeof(NODE));
            printf("\nenter the info: ");
            scanf("%d",&newnode->info);
            newnode->next = 0;
            temp = head;
            while(temp->next!=0){
                temp = temp->next;
            }
            temp->next=newnode;
            temp = head;
       count = 0;
       while(temp!=0){
          printf("%d ",temp->info);
          count++;
          temp = temp->next;
    }
       printf("no. of nodes are %d",count);
}



void main()
{
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
       temp = head;
       while(temp!=0){
           printf("%d ",temp->info);
           count++;
           temp = temp->next;
    }
       printf("\nno. of nodes are %d",count);
    int ch;
    printf("\nif you want to insert at beg choose 1 after any location chooose 2 for end choose 3: ");
    scanf("%d",&ch);
    if(ch==1){
            inserting_linked_list_beg();
    }
    else if(ch==2){
        inserting_linked_list_anylocation();
    }
    else if (ch == 3){
        at_end();
    }
    else{
            printf("\nfinished");

}
}
