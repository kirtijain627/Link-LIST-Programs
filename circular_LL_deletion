#include<stdio.h>
#include<stdlib.h>
struct node
{
    int info;
    struct node *next;
};
struct node *head, *temp, *newnode;
int count;
void counts()
{
    count = 0;
    temp = head;
    do{
       printf("%d ",temp->info);
       count++;
       temp = temp->next;
    }while(temp!=head);
    printf("\ntotal no. of nodes are: %d",count);
    printf("\n");
}

void deletion_at_beg()
{
   temp=head;
   while(temp->next!=head){
    temp = temp->next;
   }
   temp->next=head->next;
   head = head->next;

}

void del_at_position()
{
    struct node *ploc;
    int pos;
    int i =1;
    printf("\nenter the position of element you want to delete: ");
    scanf("%d",&pos);
    if(pos<1||pos>count){
        printf("invalid position");
    }
       else if(pos==1){
        deletion_at_beg();
    }

    else if(pos==count){
        del_at_end();
    }
        else {
                temp = head;
        while(i<pos){
            ploc = temp;
            temp = temp->next;
            i++;
        }
       ploc->next = temp->next;
        }
}

void del_at_end()
{
    struct node *ploc;
    temp = head;
    while(temp->next!=head){
        ploc= temp;
        temp = temp->next;
    }
    if(temp == head){
        head = 0;
    }

    else{
            ploc->next = head;
    }

}

void main()
{
   int choice = 1;
   printf("if you want to enter in list type 1 else 0: ");
   scanf("%d",&choice);
   if(choice ==1){
   head = 0;
   while(choice){
        newnode = (struct node *)malloc(sizeof(struct node));
   printf("enter the info: ","\n");
   scanf("%d",&newnode->info);
   if(head == 0){
    head = temp = newnode;
   }
   else{
    temp->next = newnode;
    temp = newnode;
   }
   temp->next = head;
   printf("if you want to enter more type 1 else 0:  ");
   scanf("%d",&choice);
   }
   }
   else {
    printf("\nlist is empty");
   }
   counts();
   printf("\nif you want to delete at beg enter 1 at any pos insert 2 for end insert 3: ");
   scanf("%d",&choice);
   if(choice==1){
    deletion_at_beg();
   }
   else if(choice ==2){
    del_at_position();
   }
   else{
    del_at_end();
   }
   counts();
   printf("\nprogram finished");

}
