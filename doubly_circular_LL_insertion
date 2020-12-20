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

void insert_at_beg()
{
    newnode = (struct node *)malloc(sizeof(struct node));
    printf("\nenter the info: ");
    scanf("%d",&newnode->info);
   temp = head;
    do{
        temp = temp ->flink;
    }while(temp->flink!=head);
    newnode->flink = head;
    newnode->plink = temp;
    head->plink = newnode;
    temp->flink = newnode;
    head = newnode;
}

void insert_at_any_pos()
{
    struct node *ploc;
    int pos;
    int i =1;
    printf("\nenter the position where you want to insert: ");
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
            ploc = temp;
            temp = temp->flink;
            i++;
        }
        newnode = (struct node *)malloc(sizeof(struct node));
        printf("enter the info: ");
        scanf("%d",&newnode->info);
        newnode->flink = temp;
        temp->plink->flink = newnode;
        newnode->plink = ploc;
        temp->plink = newnode;
    }
}

void insert_at_end()
{
   temp = head;
    do{
        temp = temp->flink;
    }while(temp->flink!=head);
     newnode = (struct node *)malloc(sizeof(struct node));
     printf("enter the info: ");
     scanf("%d",&newnode->info);
     newnode->flink = head;
     newnode->plink = temp;
     temp->flink  = newnode;
     head->plink = newnode;
}

void main()
{
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
    printf("\nenter 1 if you want to insert at beg 2 for any position and 3 for end: ");
    scanf("%d",&choice);
    if(choice == 1){
        insert_at_beg();
    }
    else if(choice == 2){
        insert_at_any_pos();
    }
    else{
        insert_at_end();
    }
    counts();
    printf("\nprogram finished");

}
