
#include<stdio.h>
#include<stdlib.h>
void main()
{
    int item;
    struct node
    {
        int info;
        struct node *plink, *flink;
    };
    struct node *head=0, *newnode, *temp=0;
    int count = 0, choice = 1;
    while(choice){
        newnode = (struct node *)malloc(sizeof(struct node));
        printf("enter the info: ");
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
        printf("\ndo you want to cintinue type 0 or 1: ","\n");
        scanf("%d",&choice);
    }
    temp->flink = 0;
    temp = head;
    while(temp!=0){
        printf("%d ",temp->info);
        count++;
        temp = temp->flink;
    }
    printf("no. of nodes are %d",count);
    printf("\nenter the item you want to search: ");
       scanf("%d",&item);
       count = 0;
       temp = head;
       while(temp!=0){
            count++;
            if(temp->info==item){
                break;}
            else{
        temp = temp->flink;

       }
       }
       if(temp==0){
        printf("\nitem not found");
       }
       else{
         printf("\nitem is found at  position %d", count);
       }
}
