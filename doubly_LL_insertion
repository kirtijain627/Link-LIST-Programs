#include<stdio.h>
#include<stdlib.h>
struct node
{
    int info;
    struct node *plink, *flink;
};
struct node *head = 0, *temp, *newnode;

void count()
{
    int count = 0;
    temp = head;
    while(temp!=0){
        printf("%d ",temp->info);
        count++;
        temp = temp->flink;
    }
    printf("no. of nodes are %d",count);
    printf("\n");
}


void insert_at_beg()
{
    newnode = (struct node *)malloc(sizeof(struct node));
    printf("\nenter the info: ");
    scanf("%d",&newnode->info);
    newnode->plink = 0;
    newnode->flink = head;
    head->plink = newnode;
    head = newnode;
}

void insert_at_pos()
{
    int pos;
    int i=1;
    struct node *loc;
    printf("enter the position where you want to insert: ");
    scanf("%d",&pos);
    if(pos<1||pos>count){
        printf("invalid position");
    }
    else if(pos ==1){
        insert_at_beg();
    }
    else {
        temp = head;
        while(i<pos){
            loc = temp;
            temp = temp->flink;
            i++;
        }
        newnode = (struct node *)malloc(sizeof(struct node));
        printf("\nenter the data: ");
        scanf("%d",&newnode->info);
        newnode->plink = loc;
        newnode->flink = loc->flink;
        loc->flink = newnode;
        temp->plink = newnode;

    }
}

void insert_at_end()
{
    temp = head;
    while(temp->flink!=0){
        temp = temp->flink;
    }
    newnode = (struct node *)malloc(sizeof(struct node));
    printf("\nenter the data: ");
    scanf("%d",&newnode->info);
    temp->flink = newnode;
    newnode->plink = temp;
    newnode->flink = 0;
}


void main()
{
    int ch;
    int choice =1;
    while(choice){
        newnode = (struct node *)malloc(sizeof(struct node));
        printf("enter the info: ","\n");
        scanf("%d",&newnode->info);
        if(head==0){
            head = temp = newnode;
            newnode->plink = 0;
        }
        else{
            temp->flink = newnode;
            newnode->plink = temp;
            temp = newnode;
        }
        printf("do you want to continue type 0 or 1: ","\n");
        scanf("%d",&choice);
    }
    temp->flink = 0;
    count();
    printf("\nif you want to insert at beg select 1 after any loc select 2 for end seelct 3: ");
    scanf("%d",&ch);
    if(ch==1){
        insert_at_beg();
        count();
    }
    else if(ch==2){
        insert_at_pos();
        count();
    }

    else{
        insert_at_end();
        count();
    }
}
