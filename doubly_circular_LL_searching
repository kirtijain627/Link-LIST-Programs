
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


void main()
{
   int item;
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

    printf("\nenter the item you want to search: ");
       scanf("%d",&item);
       count = 0;
       temp = head;
      do{
            count++;
            if(temp->info==item){
                break;}
            else{
         temp = temp->flink;
}
       }while(temp!=head);
       if(temp->flink!=head){
        printf("item is found at position %d",count);
       }
       else if(temp==head){
        printf("\nitem not found");
       }
       else{
         printf("\nitem is found at  position %d", count);
       }

    printf("\nprogram finished");

}
