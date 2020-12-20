#include<stdio.h>
#include<stdlib.h>
struct node
{
    int info;
    struct node *next;
};
struct node *head, *newnode, * temp;
int counts;
void count()
{
   temp = head;
   counts = 0;
    do{
        printf("%d ",temp->info);
        counts++;
        temp = temp->next;
    }while(temp!=head);
    printf("\ntotal no. of nodes are %d",counts);
}


void insert_at_beg()
{
    newnode = (struct node *)malloc(sizeof(struct node));
    printf("\nenter the info: ");
    scanf("%d",&newnode->info);
    newnode->next = head;
    temp = head;
    while(temp->next!=head){
        temp = temp->next;
}
head = newnode;
temp->next = head;
}


void insert_at_any_position()
{
    int pos;
    struct node *ploc;
    int i=1;
    printf("\nenter the position on which you want to insert: ");
    scanf("%d",&pos);
    if(pos<1||pos>counts+1){
        printf("\ninvalid position");
    }
    else if(pos ==1){
        insert_at_beg();
    }
    else{
        temp = head;
        while(i<pos){
            ploc=temp;
            temp = temp->next;
            i++;
    }
    newnode = (struct node *)malloc(sizeof(struct node));
    printf("\nenter the info: ");
    scanf("%d",&newnode->info);
    ploc->next = newnode;
    newnode->next=temp;
}
}

void insert_at_end()
{
    temp = head;
    while(temp->next!=head){
        temp = temp->next;
    }
    newnode = (struct node *)malloc(sizeof(struct node));
    printf("\nenter the info: ");
    scanf("%d",&newnode->info);
    temp->next = newnode;
    newnode->next = head;
}

void main()
{
    int choice = 1;
    printf("if you want to enter in list type 1 else 0: ");
    scanf("%d",&choice);
    head = 0;
    while(choice){
        newnode = (struct node *)malloc(sizeof(struct node));
        printf("\nenter the info: ");
        scanf("%d",&newnode->info);
        if(head == 0){
            head = temp = newnode;
        }
        else{
            temp->next = newnode;
            temp = newnode;
        }
        temp->next = head;
        printf("if you want to enter more  type 1 else 0: ");
        scanf("%d",&choice);
    }
    count();

    printf("\nenter 1 if you want to insert at beg 2 for any position and 3 for end: ");
    scanf("%d",&choice);
    if(choice==1){
        insert_at_beg();
    }
    else if(choice==2){
        insert_at_any_position();
    }
    else{
        insert_at_end();
    }
    count();
    printf("\nprogram finished");

}
