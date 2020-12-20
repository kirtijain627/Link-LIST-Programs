#include<stdio.h>
#include<stdlib.h>
struct node
{
    int info;
    struct node *next;
};
typedef struct node NODE;
NODE  *head, *newnode, *temp=0, *ploc;
start = 0;
int count;
int choice =1;
void deletion_at_pos()
{
    int i=1;
    int pos;
    printf("\nenter the position of element which you want to delete: ","\n");
    scanf("%d",&pos);
    temp = head;
    while(i<pos){
        ploc = temp;
        temp=temp->next;
        i++;
    }
    if(pos==1)
    {
        deletion_at_beg();
    }
    else if (pos == count){
        deletion_at_end();
    }
    else{
    ploc->next=temp->next;
    count = 0;
    temp = head;
    }
    while(temp!=0){
        printf("%d ",temp->info);
        count++;
        temp = temp->next;
    }
    printf("no. of nodes are %d\n",count);
}

void deletion_at_beg()
{
    head = head->next;
    count = 0;
    temp = head;
    while(temp!=0){
        printf("%d ",temp->info);
        count++;
        temp = temp->next;
    }
    printf("no. of nodes are %d",count);
}

void deletion_at_end()
{
    temp = head;
    while(temp->next!=0){
        ploc = temp;
        temp = temp->next;
    }
    if(temp == head){
        head = 0;
    }
    else{
        ploc->next = 0;
    }
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
    int ch;
    while(choice){
        newnode= (NODE *)malloc(sizeof(NODE));
        printf("enter the data: ","\n");
        scanf("%d",&newnode->info);
        if(head == 0){
            head = temp = newnode;
            }
        else{
            temp->next=newnode;
            temp=newnode;
        }
        printf("\ndo you want to continue type 0 or 1: ");
        scanf("%d",&choice);
    }
    temp->next = 0;
    temp = head;
    while(temp!=0){
        printf("%d ",temp->info);
        count++;
        temp = temp->next;
    }
    printf("no. of nodes are %d\n",count);
    printf("\nif you want to delete from beg enter 1 from any position enter 2 from end enter 3: ");
    scanf("%d",&ch);
    if(ch==2){
        deletion_at_pos();
    }
    else if(ch==1){
        deletion_at_beg();
    }
    else{
        deletion_at_end();
    }

    printf("\nprogram end");
}
